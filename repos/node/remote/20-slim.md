## `node:20-slim`

```console
$ docker pull node@sha256:83e53269616ca1b22cf7533e5db4e2f1a0c24a8e818b21691d6d4a69ec9e2c6d
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

### `node:20-slim` - linux; amd64

```console
$ docker pull node@sha256:1779b45aa618898c30b3d24a7b8bc812119652a32da3416a9155b95546386743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71103380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c6e3eb0c2b93a8c5a7d7c2e60398f3c21c032d6a902fd212ab25622c54d8d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 22 Apr 2025 12:08:47 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 22 Apr 2025 12:08:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
ENV NODE_VERSION=20.19.1
# Tue, 22 Apr 2025 12:08:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
ENV YARN_VERSION=1.22.22
# Tue, 22 Apr 2025 12:08:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 12:08:47 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c889a5e6143de08865ecca8a2a7615b7050daa6f9fa502ce48cf1a5c82e5988`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdabde5c430cba279ae277ea741cd8a685e405683c3fdea29abe8344677c9ef`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 41.2 MB (41159594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c750a98ab3c150e621f478236977983066d6c7ab1965d7ecf14c8397daf560`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 1.7 MB (1712389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322ae2fb7527057ada622ab2f3ab6d57f74cc0210c46112ddeec03f93197112f`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-slim` - unknown; unknown

```console
$ docker pull node@sha256:2a58517a9b0a8504d08749bd8120a53e91e202156b968528c6876b81d1e36fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2567067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c57d895c0abd49c825af61dc0daa072915ea08dc2308cac96748f1c77a2204`

```dockerfile
```

-	Layers:
	-	`sha256:72795483b977f588bd71ac2632239554bbc28c724869e29bccd1377c42ed5556`  
		Last Modified: Thu, 08 May 2025 21:18:39 GMT  
		Size: 2.5 MB (2540528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:135b2f2e9f800e135183621c2c45962e8f23db2c0a0f66c2c7795c513bfdd826`  
		Last Modified: Thu, 08 May 2025 21:18:39 GMT  
		Size: 26.5 KB (26539 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-slim` - linux; arm variant v7

```console
$ docker pull node@sha256:c3da08c1bed3378c4a66e1134d8ec9c5bfd944ad86afe4a5c36404138f5a6a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62888907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d124da0d3f835d1851b81d100566988a8c0780b4eecf028e4c5bf33f9f20a877`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 22 Apr 2025 12:08:47 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Tue, 22 Apr 2025 12:08:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
ENV NODE_VERSION=20.19.1
# Tue, 22 Apr 2025 12:08:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
ENV YARN_VERSION=1.22.22
# Tue, 22 Apr 2025 12:08:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 12:08:47 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Thu, 08 May 2025 17:05:07 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d1b3bbf741190270efc46410f38b5f8819d917654ce6e078db321721187239`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d4d2ff621e5202ab52a046deb7136eb71337de6737c8e47c0332de5a0a22bc`  
		Last Modified: Thu, 08 May 2025 18:03:29 GMT  
		Size: 37.2 MB (37234343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b454ea7b34689374441940c5d0684fa22fe0856d7b59f60bafc26d96cffd4b89`  
		Last Modified: Thu, 08 May 2025 18:03:25 GMT  
		Size: 1.7 MB (1712733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ee734c346baa585f84d6e45d0b3f430f61201c89c2b7441291cb3bd188a5b`  
		Last Modified: Thu, 08 May 2025 18:03:24 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-slim` - unknown; unknown

```console
$ docker pull node@sha256:970bed74e2ba35f68b5a491112a6de7f34d3b5fd9d7f4a088efea4ead415865b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dfc1856cf2f68ab293a5a8206e9cd97ed678fb957b29dcbc6e9377d218dbbea`

```dockerfile
```

-	Layers:
	-	`sha256:6473145cc0fdf349e8269465611ff7922b99efc410990e28076a5da0478fc098`  
		Last Modified: Thu, 08 May 2025 21:18:42 GMT  
		Size: 2.5 MB (2546030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f73591ab1e56cd8292a62e8061e2081dd41b788b9806be184a471871dd20289`  
		Last Modified: Thu, 08 May 2025 21:18:43 GMT  
		Size: 26.7 KB (26673 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:0f6f4e9389a14af676a643055e5ba2d7d105e89b964bc57ddb923a8e2e2b0975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70895514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfa49acebd89937dfef29dc6bf3aaafacaef26727c056af572bb4df19c845c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 22 Apr 2025 12:08:47 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 22 Apr 2025 12:08:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
ENV NODE_VERSION=20.19.1
# Tue, 22 Apr 2025 12:08:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
ENV YARN_VERSION=1.22.22
# Tue, 22 Apr 2025 12:08:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 12:08:47 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f94b241558a269157c87a3c504b0d5de1ebf1678a3c51786509e22e336c4b8c`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837499215e39de504f117f3779658bee38eabdea5ff72d5494286219d7099bc6`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 41.1 MB (41112533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f516e55f4b90cd98ec83c2c1b6cde9b02b882620c4b300b81b7e96a0ef34763e`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 1.7 MB (1712605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527d5a862a37a33494eaea191d601c1b52d015004dfd97aa0870002959acc6c0`  
		Last Modified: Thu, 08 May 2025 17:04:56 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-slim` - unknown; unknown

```console
$ docker pull node@sha256:23fb2a4e2a292223a226f50b172539f2aab3891cbecaf4639e0766769fb4e2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2567547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2045adf01bca4b4725514c145990efa66764046b7ee84570a28a25778d0158d2`

```dockerfile
```

-	Layers:
	-	`sha256:c0f15c3c2ffc178c190f07f74614a9402cd1ee58591ae32b4a05c1a8731fa798`  
		Last Modified: Thu, 08 May 2025 21:18:46 GMT  
		Size: 2.5 MB (2540827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c48c9e8d61d792988f418b2eadac1f2e2633c4f95cd1f9f7ac0084da0f79a86`  
		Last Modified: Thu, 08 May 2025 21:18:46 GMT  
		Size: 26.7 KB (26720 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-slim` - linux; ppc64le

```console
$ docker pull node@sha256:fac3f286977a1deaab4235486c0ade0004d5d8495b99536b887fe831d330591d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77407409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a760546ea154ea8ad26e85c4225e3a06fc7ba876098b5519fdc4d74acd566be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 22 Apr 2025 12:08:47 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 22 Apr 2025 12:08:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
ENV NODE_VERSION=20.19.1
# Tue, 22 Apr 2025 12:08:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
ENV YARN_VERSION=1.22.22
# Tue, 22 Apr 2025 12:08:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 12:08:47 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Thu, 08 May 2025 17:09:00 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38597daee156cf3f1ac2f8ab454a0b041b66d30d4ac35206b03333a6126ee853`  
		Last Modified: Tue, 29 Apr 2025 00:53:46 GMT  
		Size: 3.3 KB (3317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5877c532a3fb22609a6d5a2af80c4c99bf27215981bb497ed0e97bf56ca5800a`  
		Last Modified: Tue, 29 Apr 2025 07:56:15 GMT  
		Size: 43.6 MB (43622481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1a7d41b1068a4ecfd32d608608510ccab6a406484ca75f04ec80b18b7a219b`  
		Last Modified: Tue, 29 Apr 2025 07:56:14 GMT  
		Size: 1.7 MB (1712718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f990cc0e1d09c4558ab5fd4e79dcd3c3869bae65fd0f8fc66fe5d224788474d`  
		Last Modified: Tue, 29 Apr 2025 07:56:13 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-slim` - unknown; unknown

```console
$ docker pull node@sha256:530b2dd652fcb811df1d38691c68accb9ed99b1905e68abb18d2057fa1c0b6c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431599acf8a02aa6421afcc039c98264be5b7687fe9a237ac013399098540047`

```dockerfile
```

-	Layers:
	-	`sha256:c7890417e88970363f8ee0c34962280b7a82774676fa8141e0f3726cd6bb7165`  
		Last Modified: Thu, 08 May 2025 21:18:49 GMT  
		Size: 2.5 MB (2544810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d920b6cb20f4cda5e524ce463f23b928ddb0b7640880cefa0209af4aa9937ee`  
		Last Modified: Thu, 08 May 2025 21:18:50 GMT  
		Size: 26.6 KB (26611 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-slim` - linux; s390x

```console
$ docker pull node@sha256:feda73ab38eb715ffa2cd771db16a928aafa832bfe51f9d7762dbba23139acc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70003979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c55db9712bf87816e7bfdcfd427455d30e0ae6ec33c802cb6fce9ec6d1b09d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 22 Apr 2025 12:08:47 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 22 Apr 2025 12:08:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
ENV NODE_VERSION=20.19.1
# Tue, 22 Apr 2025 12:08:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
ENV YARN_VERSION=1.22.22
# Tue, 22 Apr 2025 12:08:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 12:08:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 12:08:47 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Thu, 08 May 2025 17:09:11 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9608a827473802af8b915ee8fee097bcbebce106315d05a446e5d4988d68ef97`  
		Last Modified: Tue, 29 Apr 2025 00:16:49 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c89621ac297d546e8179f9716b26b06de6b259d4cd5416406da1dbeb2fdc1`  
		Last Modified: Tue, 29 Apr 2025 00:18:47 GMT  
		Size: 41.4 MB (41402787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033d8aa3216fe6b52e501e8a4fded91b384e3a9af557535ea033372cfeb81f91`  
		Last Modified: Tue, 29 Apr 2025 00:18:47 GMT  
		Size: 1.7 MB (1712565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed632fdbfd4906455bd9fddc92bd69b9b059b490fe8969d57ce890d93564b914`  
		Last Modified: Tue, 29 Apr 2025 00:18:46 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-slim` - unknown; unknown

```console
$ docker pull node@sha256:f73aba89b7ae709f06f1ba0dcc27d83df9f9d8e7588fa9a57f20e4c558771802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2566797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79984ce346791f0845d45674e573e7bc836869c6e3931feea39d777c33bb607`

```dockerfile
```

-	Layers:
	-	`sha256:208b646975b4249ee2dc344916d6c907075cba784d69b31096efd7f09b342de5`  
		Last Modified: Thu, 08 May 2025 21:18:53 GMT  
		Size: 2.5 MB (2540258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e0829a1491cc33bb999e4e551664e28771cd7e720c7eec7e4ffb62d123e549`  
		Last Modified: Thu, 08 May 2025 21:18:53 GMT  
		Size: 26.5 KB (26539 bytes)  
		MIME: application/vnd.in-toto+json

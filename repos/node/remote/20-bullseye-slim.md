## `node:20-bullseye-slim`

```console
$ docker pull node@sha256:45c768d29a41e321d43ff8f93ae4e3442dea73ca42c48566ae529548e11eade1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:20-bullseye-slim` - linux; amd64

```console
$ docker pull node@sha256:969cb55a5ccee6dc1b69f5df78b919a235d269e41792d1bc140fa9d22e4100b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73000982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a730283e50c85651998fae3e29eb6a7b037959d508d5f8fb40b189ee926cfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Wed, 03 Sep 2025 19:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b594fa7e14e224b37365bafde922a37d845042d6f3e8bc2da5ed4daf87d2b43`  
		Last Modified: Wed, 03 Sep 2025 20:29:18 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803b66320933ab66fe5e017665435b3c2aa246e9cece4d3bded79ee65ea29918`  
		Last Modified: Wed, 03 Sep 2025 20:29:22 GMT  
		Size: 41.0 MB (41002857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b37e9fdf8119845547a31f33e4fac66306c3f5d14d28d738e6faf53959c193d`  
		Last Modified: Wed, 03 Sep 2025 20:29:19 GMT  
		Size: 1.7 MB (1737486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54431b07eb3c283c7707d766233fe1619f5d3de1239799fb0c9fc27b102d4c1d`  
		Last Modified: Wed, 03 Sep 2025 20:29:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:1ed619e0abc8049df1c239d40c23bf8606221ab93ca5f1cd5b776c8d1dca7167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b07d0517b7226545c901dfda6b4ae64e5c72a11bc3212382db80416a415515`

```dockerfile
```

-	Layers:
	-	`sha256:965ad2cb286dc60b40f599447ab4b661ba8a9bb59cf2b38df61f21f4a4a61d5a`  
		Last Modified: Wed, 03 Sep 2025 21:38:57 GMT  
		Size: 3.0 MB (2956824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a50655290d7cc37b773d9a0d4858f5dd704052e7e051ee8e24ddefce8e9f16d`  
		Last Modified: Wed, 03 Sep 2025 21:38:58 GMT  
		Size: 25.8 KB (25767 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-bullseye-slim` - linux; arm variant v7

```console
$ docker pull node@sha256:34c01413b18dd606294b099f7afa985a81c9851506a464361779850b8655d898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64376412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ca678be2f8dff45094b2efa90bb70d9d3d935d4dce8b8bd3244ce1dadc7c1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1754870400'
# Wed, 03 Sep 2025 19:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:42c6883fd732cb484051b4fff6157db32a689c12264945da05c930608a6fe450`  
		Last Modified: Tue, 12 Aug 2025 20:47:00 GMT  
		Size: 25.5 MB (25544117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095c04b67642b7da4bacaef9f7ed3847f7cafbb0adf765155310b10be5b4429a`  
		Last Modified: Fri, 29 Aug 2025 02:45:59 GMT  
		Size: 4.1 KB (4061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bcde9518262e45ab36188e3e6d836d5e53d9066f0c4106a274688a2118c6f6`  
		Last Modified: Thu, 04 Sep 2025 00:56:50 GMT  
		Size: 37.1 MB (37090117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7234934f8b395455b4369389dfddc724f092d807e34c12fbe54b2d7939905c`  
		Last Modified: Wed, 03 Sep 2025 23:01:04 GMT  
		Size: 1.7 MB (1737668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d8edd6797e50fa9af446f2c5f076f88429d8778df94f0f20eb8fc264be649d`  
		Last Modified: Wed, 03 Sep 2025 22:16:42 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:ec9d136e18a44354ed83f5c7215409afa46954e1a85bde8fc14025376e513256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df8c00c385adf1fc485cc4eaf4b65fba2e4ee696a0491431b206c2b1d34c03e`

```dockerfile
```

-	Layers:
	-	`sha256:691a22d8a0fa6a56bd1909d3d683a2565f61023d6eb8d694627f3697dd5bf655`  
		Last Modified: Thu, 04 Sep 2025 00:39:30 GMT  
		Size: 3.0 MB (2962600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef77444b8d282765d2e0033543b109f9fb19c4ce173cd7ffe29dee8487069d30`  
		Last Modified: Thu, 04 Sep 2025 00:39:31 GMT  
		Size: 25.9 KB (25869 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:49afebf5de5182aea806692d89fc5936de29db7eaf8e037826056b4f01371eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71456414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8d63a27d9a7ee7bb98e41fe154e7c4b190f0795abddd92373269a99ff8e0fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Wed, 03 Sep 2025 19:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV NODE_VERSION=20.19.5
# Wed, 03 Sep 2025 19:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENV YARN_VERSION=1.22.22
# Wed, 03 Sep 2025 19:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 19:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 19:47:58 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eec96efa93c5c2a463c83eb2f3c4f61ce23d403069fcd14ecfbb697e81e9f62`  
		Last Modified: Thu, 28 Aug 2025 14:43:54 GMT  
		Size: 4.1 KB (4078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474456cdafd1d401273a923d83b90b09ad9e2fcf223dcb554959afdd5199cd67`  
		Last Modified: Wed, 03 Sep 2025 21:26:04 GMT  
		Size: 41.0 MB (40963933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930a95f7daab9f4eb4b9811546aa215619d9b4c97c9846f18e3d27dea68129b5`  
		Last Modified: Wed, 03 Sep 2025 21:26:01 GMT  
		Size: 1.7 MB (1737463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c16ec12d7fcba487c0414c207044cd7f71fae881caba7418297aeb27d4097c`  
		Last Modified: Wed, 03 Sep 2025 22:16:05 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:ae03e5860840dfa4e68a0893cf72a5244c2b331de407b937abe0f36cb78a7fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3563ec1c509751564c53214d0b4852d38e07826b31e39d55175a664d1fbdd87`

```dockerfile
```

-	Layers:
	-	`sha256:cda38ad1291a24f7acb10ebe5c3db58842fb2f8472274ba37c3f19e335b70d31`  
		Last Modified: Thu, 04 Sep 2025 00:39:35 GMT  
		Size: 3.0 MB (2957075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e095e0e15de437d9cb3d00650958bced12fa7d593ef13a83a140070b9dcf68ae`  
		Last Modified: Thu, 04 Sep 2025 00:39:36 GMT  
		Size: 25.9 KB (25901 bytes)  
		MIME: application/vnd.in-toto+json

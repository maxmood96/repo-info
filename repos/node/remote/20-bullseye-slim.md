## `node:20-bullseye-slim`

```console
$ docker pull node@sha256:e9f838bdf8a71f5a5d50581e9aff3225e7a129b77ba89dba02c20c693dee4b2d
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
$ docker pull node@sha256:60836a52c263f2001a202cebed49d6bc202ab287ef6d951ca8a847bcd82881ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73179694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d38d8b835f311c0a44adc3889fcc04b06dce1932e2652a4f58fec291f76352b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Thu, 13 Mar 2025 14:48:02 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 13 Mar 2025 14:48:02 GMT
ENV NODE_VERSION=20.19.0
# Thu, 13 Mar 2025 14:48:02 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 13 Mar 2025 14:48:02 GMT
ENV YARN_VERSION=1.22.22
# Thu, 13 Mar 2025 14:48:02 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 13 Mar 2025 14:48:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 14:48:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Mar 2025 14:48:02 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207f745d676daed9a51ec6e6c94280d7e9b9fe2b7962b27f9f9ca7f01478f177`  
		Last Modified: Thu, 13 Mar 2025 17:08:59 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d4eec7ce373cfb65a92b1bceff646c3e6e263bc70de34a9352201a23d6cfb8`  
		Last Modified: Thu, 13 Mar 2025 17:09:00 GMT  
		Size: 41.2 MB (41185278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ba840f2e3770e7a497817a223a027dc9481bf6d2f7e14395781aa92569b514`  
		Last Modified: Thu, 13 Mar 2025 17:08:59 GMT  
		Size: 1.7 MB (1735964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43a9f1f8ccd7933da2524c7f14a1be73162d82c380b7fe95370dec2217a9bf2`  
		Last Modified: Thu, 13 Mar 2025 17:08:59 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:e04a8fb9a92aa117ba15af79694853d6adb9a716415ccd048bda0253aea01b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2875271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3848d65842f8a9b550f6ad2eda8ceb0a532bc30f4abdf66058c29bbd77295d60`

```dockerfile
```

-	Layers:
	-	`sha256:ebaed1edcda22ad3fe106fb3a4af9768078ebe4cf9b1f8e1ec3f50e0a6685c0a`  
		Last Modified: Thu, 13 Mar 2025 17:08:59 GMT  
		Size: 2.9 MB (2850039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17e005911985e37383ac6e7e1610946a711751d80eee70967a33f9f0aa074c41`  
		Last Modified: Thu, 13 Mar 2025 17:08:59 GMT  
		Size: 25.2 KB (25232 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-bullseye-slim` - linux; arm variant v7

```console
$ docker pull node@sha256:134cda0099078e6bdc049c159c4be474bc97b30d07a74d84a251c36e58b565a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64531492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2871155820fc3c3b1a3dcf9f0e3137715411d1f955c2ec3397e192006e988698`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Thu, 13 Mar 2025 14:48:02 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 13 Mar 2025 14:48:02 GMT
ENV NODE_VERSION=20.19.0
# Thu, 13 Mar 2025 14:48:02 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 13 Mar 2025 14:48:02 GMT
ENV YARN_VERSION=1.22.22
# Thu, 13 Mar 2025 14:48:02 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 13 Mar 2025 14:48:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 14:48:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Mar 2025 14:48:02 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:b0ca501b624d9dae81049df15e1024733ee21141b25f8ca123d98e0d13df5d12`  
		Last Modified: Tue, 25 Feb 2025 01:31:18 GMT  
		Size: 25.5 MB (25535432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c234f41a62b528016dffb044e3ce0f5d6ea94d53a086bc4da7ad107852e5500`  
		Last Modified: Tue, 25 Feb 2025 07:43:09 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498078781c27baf5e312f9b6c7929d919c982a3b96aad078c27a5a9e3b4df47`  
		Last Modified: Thu, 13 Mar 2025 17:59:58 GMT  
		Size: 37.3 MB (37255384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34ff353fab9391554075ad10400790a2f1f677cf92c83373fa1d1d58b636566`  
		Last Modified: Thu, 13 Mar 2025 17:59:56 GMT  
		Size: 1.7 MB (1736167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b81aa0b56674cf284201c6bf489025ce11d5b90cd6686c771d492b0d3ab850f`  
		Last Modified: Thu, 13 Mar 2025 17:59:56 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:bf96747554697671304da6c8b32ca34bb2956f828423b1c80d6385a5fecdb8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2880858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd8a9994c8873b5d07420b1ec72bc02e71b20bc35ce0a0b83dd2dcfa2e4cdbd`

```dockerfile
```

-	Layers:
	-	`sha256:4ee133b0f7039df892366223ed9e0d8188775b255dbec5f35051a0212658a7e8`  
		Last Modified: Thu, 13 Mar 2025 17:59:56 GMT  
		Size: 2.9 MB (2855525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa2a3022195d7334d3e9046728c62b05b16d5a791e765a2e31668886690f77d7`  
		Last Modified: Thu, 13 Mar 2025 17:59:56 GMT  
		Size: 25.3 KB (25333 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:0e79f43bada4bda687152ba2836e743d76e83b63d9cbeceeccc0b418cb8d4f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71626280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda945ee70427cc4b3456d9591741dcf3df6b55f2c169edd2c37bef8f02fd628`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Thu, 13 Mar 2025 14:48:02 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 13 Mar 2025 14:48:02 GMT
ENV NODE_VERSION=20.19.0
# Thu, 13 Mar 2025 14:48:02 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Thu, 13 Mar 2025 14:48:02 GMT
ENV YARN_VERSION=1.22.22
# Thu, 13 Mar 2025 14:48:02 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 13 Mar 2025 14:48:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 14:48:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Mar 2025 14:48:02 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998dc71dd90f3e987955396fce361e0a7fd8b5938f25e02a25738df305121f6d`  
		Last Modified: Thu, 13 Mar 2025 17:34:29 GMT  
		Size: 4.1 KB (4082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a52a61f791a685f2daf4152dcb0aede00e7ecd1bb3548c756d86159dec0e30b`  
		Last Modified: Thu, 13 Mar 2025 17:34:31 GMT  
		Size: 41.1 MB (41139803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eded9cc3f948d97c3d6cf98c8d9b809ffe02c1b2c5cd51ea9843dc059e07753`  
		Last Modified: Thu, 13 Mar 2025 17:34:30 GMT  
		Size: 1.7 MB (1735959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e8d5ee2e0d7d6fb9db06e7398febd0d97178f6af86b4dadd8db4dc8353f599`  
		Last Modified: Thu, 13 Mar 2025 17:34:29 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:ac74e264c3ce91ec05589c416a4daa6e245d1260daef78410bfdaf4805b08477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2875655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be22ec9ecc6a99ee791499880a4ce5af0bd55afd701c31671b5b69d4f94c12f9`

```dockerfile
```

-	Layers:
	-	`sha256:356ecdcfe8c1b9edddedf10d3293d8d55e5845998837887143474a8fc1f6f692`  
		Last Modified: Thu, 13 Mar 2025 17:34:30 GMT  
		Size: 2.9 MB (2850290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a41990f4d9086cc76981e1a5a5a23dcb4c4ddd4dafeeb16a79aca56cd45658ff`  
		Last Modified: Thu, 13 Mar 2025 17:34:29 GMT  
		Size: 25.4 KB (25365 bytes)  
		MIME: application/vnd.in-toto+json

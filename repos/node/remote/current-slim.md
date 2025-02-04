## `node:current-slim`

```console
$ docker pull node@sha256:1689e36f172387959094ba85a435f7eaa731ae0cba6fe00e61b0cdc2cfe52d51
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

### `node:current-slim` - linux; amd64

```console
$ docker pull node@sha256:a67cd0174af168eb7a5ff8fde4811e1e57ff2fe104185ce5c9c927f62aaa99c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79738711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b920e33c5289ec8d7d5ec17af6dfca4b43344ac36b4a47a8293ab71327626a87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 31 Jan 2025 17:21:26 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Fri, 31 Jan 2025 17:21:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENV NODE_VERSION=23.7.0
# Fri, 31 Jan 2025 17:21:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENV YARN_VERSION=1.22.22
# Fri, 31 Jan 2025 17:21:26 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Jan 2025 17:21:26 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3278698e8085610d7310ff72c3247479eb46f50eefcee6ec2446f37ccbaa578d`  
		Last Modified: Tue, 04 Feb 2025 04:43:05 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d603fdea2dc627cb9dea589f8c85f8f0b4cfc322d8e1b79bfc0915e7d80faa`  
		Last Modified: Tue, 04 Feb 2025 04:43:06 GMT  
		Size: 49.8 MB (49810151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45b504d77a5574a016557051e28f59c5c5fd69213f5646f29bcb72233188891`  
		Last Modified: Tue, 04 Feb 2025 04:43:05 GMT  
		Size: 1.7 MB (1712499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8656c5f9e6372db2b9de0915f8c2baea3869fcd23765919e11bc121d8bccd4a`  
		Last Modified: Tue, 04 Feb 2025 04:43:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-slim` - unknown; unknown

```console
$ docker pull node@sha256:986ab426eebb1720be8cb1e88de9c0fe63e91593d34a2318c558251084d93545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d5e94e7d2bd17cb4a91fbbf9a82e082ffcc26763d2251ddd4d52bc11873c12`

```dockerfile
```

-	Layers:
	-	`sha256:58cd4d2d31db6b1e12557429a7c4d89b8e53ca985839435e739f2c215e0eeda3`  
		Last Modified: Tue, 04 Feb 2025 04:43:05 GMT  
		Size: 2.6 MB (2556964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d6e4aa7e854e4bd27341d0a2c5c52eec6df575966ac66882a8dfc3786cfb7a`  
		Last Modified: Tue, 04 Feb 2025 04:43:05 GMT  
		Size: 27.0 KB (27036 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-slim` - linux; arm variant v7

```console
$ docker pull node@sha256:e28238bf406a28a4b926bf92990a4f8d4c11348ac463c1039a2bfe67d1b2ed97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70065523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2de0653314e46882a77fc974fbcb64e7159dbbcb3ba01a19029cf361f94f4f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Fri, 31 Jan 2025 17:21:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENV NODE_VERSION=23.7.0
# Fri, 31 Jan 2025 17:21:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENV YARN_VERSION=1.22.22
# Fri, 31 Jan 2025 17:21:26 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Jan 2025 17:21:26 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f285995e799be4f2b80199a18ba1da9200c37db49b5a907574d3b951f08d72e9`  
		Last Modified: Tue, 14 Jan 2025 09:26:22 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30679df82d2cedb92c54786a1ce0f99450f8e7a61b59b9605a53c9bf325d392`  
		Last Modified: Fri, 31 Jan 2025 21:57:28 GMT  
		Size: 44.4 MB (44434473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd074492ee2f739f6e55e402219563e38cc327d3343a76e8ef1af173400ec8c8`  
		Last Modified: Fri, 31 Jan 2025 21:57:26 GMT  
		Size: 1.7 MB (1712689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84dda384c2a12ecdacd7bfaa6055a4d7535d9a21dcbcb5cf5942438e69b43b9f`  
		Last Modified: Fri, 31 Jan 2025 21:57:26 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-slim` - unknown; unknown

```console
$ docker pull node@sha256:e519ef54f8457c648e39e2b4102baea08f979efc80a8dcd39b87c14c4406bd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e144cca58f15edb0af86ffa9e525bb31073499ef72565fa2077f0502c7586df`

```dockerfile
```

-	Layers:
	-	`sha256:6359350bd25584f9946532ebcf2b86438dcfe2181ec775d819551290ea424cba`  
		Last Modified: Fri, 31 Jan 2025 21:57:26 GMT  
		Size: 2.6 MB (2562482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e651d256f947c2ba428417969bfcf5486965b722771369d609ed06bf791e99fe`  
		Last Modified: Fri, 31 Jan 2025 21:57:26 GMT  
		Size: 27.2 KB (27184 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:d16b95ac4e4b438ae1199aedb9116df2737f735a5c9ff27f1a8fa747908a9303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (79049758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133f774253fcf12d7a442e6e497150a0c85a98b2a5822a171cc95d8464feab25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Fri, 31 Jan 2025 17:21:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENV NODE_VERSION=23.7.0
# Fri, 31 Jan 2025 17:21:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENV YARN_VERSION=1.22.22
# Fri, 31 Jan 2025 17:21:26 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Jan 2025 17:21:26 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9524bf8a101864d9f7c571c82e0a231cf10c637147370c2c86ac7e3c2e401d7`  
		Last Modified: Wed, 22 Jan 2025 17:21:22 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a377412a13ee39f3cca268fbae1c223abb37b78b678f558c291aad683da80`  
		Last Modified: Fri, 31 Jan 2025 20:25:22 GMT  
		Size: 49.3 MB (49292479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59dcc31b503553f4c711e033dff28455e7705e75d0b76f6643c5673742957c79`  
		Last Modified: Fri, 31 Jan 2025 20:25:21 GMT  
		Size: 1.7 MB (1712487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675a5d88499d1d2d27f2f1eb5edc5289089d9af8fa905cc16edf6e84ed34a962`  
		Last Modified: Fri, 31 Jan 2025 20:25:20 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-slim` - unknown; unknown

```console
$ docker pull node@sha256:ce72679f01b9acc7421edecd4321c81703d3493875bc9b792abc98d23fa81ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8359d760190aa67fd1582d2b70ce48db5b829b12472a05057078b9a6c02dbbd0`

```dockerfile
```

-	Layers:
	-	`sha256:da9c5c7a0e30178ea75f6368ac2c225ca682d83334e00fde78f86b2f67ab78cb`  
		Last Modified: Fri, 31 Jan 2025 20:25:21 GMT  
		Size: 2.6 MB (2557287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1568ad8010768148d99cb9c8791ddfce927e8cd994031d1e6ebbb6b479e48b8`  
		Last Modified: Fri, 31 Jan 2025 20:25:20 GMT  
		Size: 27.2 KB (27242 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-slim` - linux; ppc64le

```console
$ docker pull node@sha256:0c75817ea11403e6100a272218e1814a6263d904adc060f2d269e59afe54a82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (86018199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eda837d7afc715d98bebd76ddef5e8a00392ae7717b5aa40616e149b126a16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 31 Jan 2025 17:21:26 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Fri, 31 Jan 2025 17:21:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENV NODE_VERSION=23.7.0
# Fri, 31 Jan 2025 17:21:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENV YARN_VERSION=1.22.22
# Fri, 31 Jan 2025 17:21:26 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Jan 2025 17:21:26 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ecbb60402874ad66e741d07585a6fd93f30fc346715f34f4789a39e3f61114`  
		Last Modified: Tue, 04 Feb 2025 08:37:09 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95a0534d459302939cd0cd89b88bfa2dcb2782d7386a3c136cd1b1fdf50e3df`  
		Last Modified: Tue, 04 Feb 2025 08:37:11 GMT  
		Size: 52.3 MB (52256968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de0425cf8af35d5804628a98bf11c20901d28fec739713f42945e0c836394de`  
		Last Modified: Tue, 04 Feb 2025 08:37:09 GMT  
		Size: 1.7 MB (1712692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b98fecfc6ddbc3d81b86a047ba575e8ea47a325423684c2ffd71f2468ff37e`  
		Last Modified: Tue, 04 Feb 2025 08:37:09 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-slim` - unknown; unknown

```console
$ docker pull node@sha256:4c514b497d82f465d65fe15101bb1b0f6131c714f07b8e0c3c596cb8325ab97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e42f67f2342ca30c1f8838f1b4e46d46a30551823a55e385e31f9b6d64c3ae9`

```dockerfile
```

-	Layers:
	-	`sha256:a31a2661b077de2f935c84e269fbd0c5f88f43055fe1bb1562bf5ea9e5445733`  
		Last Modified: Tue, 04 Feb 2025 08:37:09 GMT  
		Size: 2.6 MB (2561258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b37cefbe12e89d84e93cdaab63d7a6301f6987ac31d12758a2fbb930272bf3`  
		Last Modified: Tue, 04 Feb 2025 08:37:09 GMT  
		Size: 27.1 KB (27119 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-slim` - linux; s390x

```console
$ docker pull node@sha256:0c3b67863983f1b61f36a3bcc31ac977af591c03d489be0b498fa7c4f6178571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77916944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadd262f3f43a930c02845cc858ad2772274fcf02493e19be135a461c9621a6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 31 Jan 2025 17:21:26 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Fri, 31 Jan 2025 17:21:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENV NODE_VERSION=23.7.0
# Fri, 31 Jan 2025 17:21:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENV YARN_VERSION=1.22.22
# Fri, 31 Jan 2025 17:21:26 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Jan 2025 17:21:26 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe85f93807913fb27941b07310899db6000b3d90e2f8e97db7c9f4d8e4459dd`  
		Last Modified: Tue, 04 Feb 2025 08:42:29 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0301faebf0116b56db873ca68c127bd923abfc8196d2946b8709ed3350abe69c`  
		Last Modified: Tue, 04 Feb 2025 08:42:30 GMT  
		Size: 49.3 MB (49342027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9719333cb7e4650f0e01a1aaa5697781c80e70d576915efcbafd242ee9abeed3`  
		Last Modified: Tue, 04 Feb 2025 08:42:30 GMT  
		Size: 1.7 MB (1712531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40ad4209f023370cfd7b01906e6966427a54aea5cfa584932d37d1697eb4181`  
		Last Modified: Tue, 04 Feb 2025 08:42:30 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-slim` - unknown; unknown

```console
$ docker pull node@sha256:038bd0b46e310319e12e95dd03f5c74168bc7afb5a52c1162928689bc7c6e34d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba0e22ab0f6c43b1f17035441ea2000f208f44aad9e4b377c699f0cbd03f49a`

```dockerfile
```

-	Layers:
	-	`sha256:3ea674d3fe639c88b5ab618be2b9dbcd7dc5b08e32d442f6f158c2675880c18b`  
		Last Modified: Tue, 04 Feb 2025 08:42:30 GMT  
		Size: 2.6 MB (2556694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:716dd5878072fd949b5a0515a445a09617f16ffca6ee43cbaab9a96f8dffc9ee`  
		Last Modified: Tue, 04 Feb 2025 08:42:29 GMT  
		Size: 27.0 KB (27036 bytes)  
		MIME: application/vnd.in-toto+json

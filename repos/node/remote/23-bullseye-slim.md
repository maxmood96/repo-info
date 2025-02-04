## `node:23-bullseye-slim`

```console
$ docker pull node@sha256:9b04ccc8d2fb14843e77446c1a0625b88cf2b5e5091bad4d987faa2a8180ebed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:23-bullseye-slim` - linux; amd64

```console
$ docker pull node@sha256:7b8eb2064b1ba87aeae1aba9a34e4e756640e9aa6750c3322bf948f387599c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81827573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3979a55cd90c8c5f183cbbb534b5edab7733b86e2db63311c49ece7f3a62d70a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 31 Jan 2025 17:21:26 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbc1f50214bf6e0bba4fb65aefe7b650ca8afa5a0ac9cfe3294e08195bf8d85`  
		Last Modified: Tue, 04 Feb 2025 04:43:09 GMT  
		Size: 4.1 KB (4071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e536c60837bec406a333d65fbc15341fc74a9c9b6107e5aef9f84cb822a188`  
		Last Modified: Tue, 04 Feb 2025 04:43:10 GMT  
		Size: 49.8 MB (49834507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416cceee9faf89dd33e75d3247f81fd0b5d1030a388f9410d252dff1b29810d8`  
		Last Modified: Tue, 04 Feb 2025 04:43:09 GMT  
		Size: 1.7 MB (1735959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a495cc1a43b4a62fd19e217a8039801f20be015784b6cb86587341fc83ebb663`  
		Last Modified: Tue, 04 Feb 2025 04:43:09 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:23-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:a65756b42570f9053c5a7f75d58eca06213fb18444774956ef9efd7d55be59d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2893085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a469d8182580b6123b015b09cc88a9bc27375c9cff2074565907f6bd4ab07f`

```dockerfile
```

-	Layers:
	-	`sha256:2141720a8ac6c4074f20e4104c0f13f0abf9593b1b872a6f81e770f647c138db`  
		Last Modified: Tue, 04 Feb 2025 04:43:09 GMT  
		Size: 2.9 MB (2867545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f9ac0968b97354fd84404f3fc104db54ae1118433ad6c59feb58c8479b008bd`  
		Last Modified: Tue, 04 Feb 2025 04:43:09 GMT  
		Size: 25.5 KB (25540 bytes)  
		MIME: application/vnd.in-toto+json

### `node:23-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:21f1d51cd74e2ac107f9c3fc011a9fe2eff006fdd9dda74c86e11ce057c116de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79802288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fda4088b914051e4a3a8db3c6070b57d76a3c41930759fc60d1bc4d3e36946b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3336daccb5e834a3a840eb303aca0fd10b80f877b9862b94c60767329cc5686`  
		Last Modified: Wed, 22 Jan 2025 17:23:35 GMT  
		Size: 4.1 KB (4076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed522ebc4199c550bfa4025c38ab353963d10670a44954a63092c2962ebbc76e`  
		Last Modified: Fri, 31 Jan 2025 20:27:34 GMT  
		Size: 49.3 MB (49316942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4d352823e5f261815a473d9b6b4fa1d16f206c164bbe61b302d85d50ebd313`  
		Last Modified: Fri, 31 Jan 2025 20:27:33 GMT  
		Size: 1.7 MB (1735911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c032e72e28f8a6676a4ece59b4d112c92029ce4278e00ae41b7044b0c916ae5`  
		Last Modified: Fri, 31 Jan 2025 20:27:33 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:23-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:dfd97b9037e9109b4d539fdbf5c3e582bc7c2c6122f5a56a1ea7df0de1716a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2893494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96cd3a7e1010cbc76f5718d7bae5e84ef624bf858ebab45b7bcc73c0f0a1b242`

```dockerfile
```

-	Layers:
	-	`sha256:dcb488b2b9efdb32832fa10897e3613e17f0aa131ae0df29b9eb724e374abcad`  
		Last Modified: Fri, 31 Jan 2025 20:27:33 GMT  
		Size: 2.9 MB (2867808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7888d9b344a8c2da616771a4c76fa475d6cafda47df93192c116957ba59be50c`  
		Last Modified: Fri, 31 Jan 2025 20:27:33 GMT  
		Size: 25.7 KB (25686 bytes)  
		MIME: application/vnd.in-toto+json

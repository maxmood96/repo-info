## `node:iron-slim`

```console
$ docker pull node@sha256:b2c8e0eb8a6aeeae33b2711f8f516003e27ee45804e270468d937b3214f2f0cc
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

### `node:iron-slim` - linux; amd64

```console
$ docker pull node@sha256:35eccf0e5cdb40b8ba3531e1b756d0ed52ec6e9d74c1756cc6503e8734effd27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70683740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36ac8e813923331fe4783b6e28577471c99c5592c77d678a7df52e848257e0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 20 Nov 2024 16:05:40 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 20 Nov 2024 16:05:40 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
ENV NODE_VERSION=20.18.1
# Wed, 20 Nov 2024 16:05:40 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
ENV YARN_VERSION=1.22.22
# Wed, 20 Nov 2024 16:05:40 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Nov 2024 16:05:40 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ffe8c091b844bba6a9580c8cbb701e6e643d119cca163ca7fae3cabbc4689a`  
		Last Modified: Tue, 14 Jan 2025 02:36:17 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6620872b7cde31772116d3abf20dccc7f7b63e072382fe443ae7005972946a33`  
		Last Modified: Tue, 14 Jan 2025 20:33:03 GMT  
		Size: 40.8 MB (40755099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab511d14ed3865233934f79d79208ab0712e2c6cb158faef10d4ffd63ee38aae`  
		Last Modified: Tue, 14 Jan 2025 02:36:17 GMT  
		Size: 1.7 MB (1712466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3351a9c5c3d730f4b269936b24914e8ba2ceda25202be81a49c0f65aab17fb16`  
		Last Modified: Tue, 14 Jan 2025 02:36:17 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:iron-slim` - unknown; unknown

```console
$ docker pull node@sha256:9102f441262511fef27c741aebc168e9989cee2fb6a8d0d190de14403ca4aca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2565601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d87c43042e1cbb0cf3c0bf3e530f027909445e7ca2fb80c36851316c1eccd9`

```dockerfile
```

-	Layers:
	-	`sha256:926295c41548f206fa7937ecf1c4ff58b7916db2b58c071291534fbeb22f5917`  
		Last Modified: Tue, 14 Jan 2025 02:36:17 GMT  
		Size: 2.5 MB (2539166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0f38f0f4f7c668ebc27f6c4d6b142bc444a467f6f57eae87fe74ef4bf10391a`  
		Last Modified: Tue, 14 Jan 2025 02:36:17 GMT  
		Size: 26.4 KB (26435 bytes)  
		MIME: application/vnd.in-toto+json

### `node:iron-slim` - linux; arm variant v7

```console
$ docker pull node@sha256:85529960cea5d3c646de6cf144e7830143212bc0c4f1c65ab2887ffa95dc24ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62485475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614b3a5619cf9841b738a652f6b900bc3c94a0a338d97ac236d7ac4dacb1a13b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 20 Nov 2024 16:05:40 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 20 Nov 2024 16:05:40 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
ENV NODE_VERSION=20.18.1
# Wed, 20 Nov 2024 16:05:40 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
ENV YARN_VERSION=1.22.22
# Wed, 20 Nov 2024 16:05:40 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Nov 2024 16:05:40 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f285995e799be4f2b80199a18ba1da9200c37db49b5a907574d3b951f08d72e9`  
		Last Modified: Tue, 14 Jan 2025 21:04:36 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbd1b01645a40e32c3c912401fa7a891cab97050da05f5246d64023d6b9f1e9`  
		Last Modified: Tue, 14 Jan 2025 21:07:39 GMT  
		Size: 36.9 MB (36854458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6798afb0b5853f0010b98cfd6491a89342487d10a746c830b4c0e14631fab4e2`  
		Last Modified: Tue, 14 Jan 2025 09:30:13 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f9f9b82d1cb33ff329bb7025606a402fae56cbe76e31e58e86b162795533c7`  
		Last Modified: Tue, 14 Jan 2025 09:30:12 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:iron-slim` - unknown; unknown

```console
$ docker pull node@sha256:029a41e1978703abb83d65a1baab0723fa55d967ba3eea3b4716e30b0b7f8866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb9499148392ddb653828beda78ed52520d3e982dc2234f7bbf6ba1c16dba72`

```dockerfile
```

-	Layers:
	-	`sha256:6e7ddbba285376f2397f40aef8d07d5e41f38ba2f8e4bc8784f2fe03fe044fd2`  
		Last Modified: Tue, 14 Jan 2025 09:30:13 GMT  
		Size: 2.5 MB (2544668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4387394c1a75fa3f2c405126d52b06abc47cc1d805ee991294a33eee34f13d9`  
		Last Modified: Tue, 14 Jan 2025 09:30:12 GMT  
		Size: 26.6 KB (26570 bytes)  
		MIME: application/vnd.in-toto+json

### `node:iron-slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:6f69e0695f627086a2105d375cfa9fc27ec90782cc2cb5ddafa920fbdef4dacf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70482668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7678d60a1a5c7279ed248bbd528dc1471c2086945ff58f5ae00fdc8534e4d089`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 20 Nov 2024 16:05:40 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 20 Nov 2024 16:05:40 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
ENV NODE_VERSION=20.18.1
# Wed, 20 Nov 2024 16:05:40 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
ENV YARN_VERSION=1.22.22
# Wed, 20 Nov 2024 16:05:40 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Nov 2024 16:05:40 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a58c8645b4304ad465a00d0dae6b3425953ebbf13bb69428a33a15911c3ada`  
		Last Modified: Tue, 14 Jan 2025 07:32:05 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525cf29e35f24474f87e2d17dc4d7c20b3c6c1ca7fffbcb5d4eeb2a6aa58a91`  
		Last Modified: Tue, 14 Jan 2025 20:34:14 GMT  
		Size: 40.7 MB (40725393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b313f531029241d2fca507e007300f50a7cba2896e953b3fd4677960121e89f9`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 1.7 MB (1712487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553f9dc4d06a7919c2e54bac7daedf7a4bb89f12e5883b924c4962dce88a8e0`  
		Last Modified: Tue, 14 Jan 2025 07:36:12 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:iron-slim` - unknown; unknown

```console
$ docker pull node@sha256:0c7712329a8bddf836613145df31371f6cc9cd63831de2c9708adbedc9099fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2566083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3215aa1ed6f06a85551769e87426d2c19383746207098d8ea066832a7c02a6`

```dockerfile
```

-	Layers:
	-	`sha256:0d46862ce87013fd87dfeae724725f0747dda4abf3aea001de0fa81a3c3d35b0`  
		Last Modified: Tue, 14 Jan 2025 21:00:54 GMT  
		Size: 2.5 MB (2539465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fbe232d5ad6cd8a0b5169a9fa73c072fd2339b0e028c775b6644c52e3c085bb`  
		Last Modified: Tue, 14 Jan 2025 21:01:00 GMT  
		Size: 26.6 KB (26618 bytes)  
		MIME: application/vnd.in-toto+json

### `node:iron-slim` - linux; ppc64le

```console
$ docker pull node@sha256:8c989284d39740183d55869009ebcc5385817b681bdb487a5b9ce1a23b569784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77001795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad830e5f8b467f8ab6f13e6880af932b1c357f4b0e4b6ac32bd2168a04f7bcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 20 Nov 2024 16:05:40 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 20 Nov 2024 16:05:40 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
ENV NODE_VERSION=20.18.1
# Wed, 20 Nov 2024 16:05:40 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
ENV YARN_VERSION=1.22.22
# Wed, 20 Nov 2024 16:05:40 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Nov 2024 16:05:40 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5523dfe9336d555c5e0afc6ca4656e8ac78255582723643b6b4c529a944d66aa`  
		Last Modified: Tue, 14 Jan 2025 05:49:17 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cee83d562bcc951616a8cc8711061b840947894af22cc88f9a9cdc8ad06cf59`  
		Last Modified: Tue, 14 Jan 2025 22:29:03 GMT  
		Size: 43.2 MB (43240582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5655f7406b7783a661c766cd758b0e4abc885b1e975a5119a68eff9e26f3fff`  
		Last Modified: Tue, 14 Jan 2025 22:29:01 GMT  
		Size: 1.7 MB (1712609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119ea4cfb48c7934b9c374a545010bc6b05a14661ff7c63b95708fe546b73db8`  
		Last Modified: Tue, 14 Jan 2025 22:29:00 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:iron-slim` - unknown; unknown

```console
$ docker pull node@sha256:4f47cd3b81df3df9c4414df0d2334bc0495aa9a60690646ec52044d5bb33dbce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2569956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54cd982a3b7e782e4486af078baaddb22cc98454f8c12cf33d4fd226a2c1b66`

```dockerfile
```

-	Layers:
	-	`sha256:9e8d00bf360bd4b46789aada38b3807569c20310891ef1ad691bf1c05269aa03`  
		Last Modified: Tue, 14 Jan 2025 05:53:33 GMT  
		Size: 2.5 MB (2543448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b95ce2a17c807cb47ab8c98bc40c2ed685a2de8c1d597620c07a1f55d2e9108`  
		Last Modified: Tue, 14 Jan 2025 21:00:56 GMT  
		Size: 26.5 KB (26508 bytes)  
		MIME: application/vnd.in-toto+json

### `node:iron-slim` - linux; s390x

```console
$ docker pull node@sha256:004931618988578d5e3e16b142e562bdcf8907bd101140600f05d94aa3903f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69579388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3f70c53605d4e877960aebb380a06980b87f0d453df6243b68ac75c3c89c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 20 Nov 2024 16:05:40 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 20 Nov 2024 16:05:40 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
ENV NODE_VERSION=20.18.1
# Wed, 20 Nov 2024 16:05:40 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
ENV YARN_VERSION=1.22.22
# Wed, 20 Nov 2024 16:05:40 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 16:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Nov 2024 16:05:40 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2a614653c4a5b67d69cef861fd45d07a6cca5360d0bf79d929fad8b001e758`  
		Last Modified: Tue, 14 Jan 2025 21:12:42 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce50288b1d69551918bd98a67f180cb1fd4324893e5d0ecf1cc119d2a8a2ac6e`  
		Last Modified: Tue, 14 Jan 2025 05:27:57 GMT  
		Size: 41.0 MB (41004413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a7295b118b49dfb52672393419d40f694330b5a080a1c2b4d71fb5f5e5054d`  
		Last Modified: Tue, 14 Jan 2025 22:29:02 GMT  
		Size: 1.7 MB (1712471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6a8b17ca0a0ef674f72ac16fd38e0617fac747adb3041134eb660068baa354`  
		Last Modified: Tue, 14 Jan 2025 05:27:56 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:iron-slim` - unknown; unknown

```console
$ docker pull node@sha256:5f6fa57b8d04ef89399acfeaa7d89578e5fa1634927b62db9bb71ed49e3a7662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2565332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6dc86de79c4a0033db81c8e3334feadcf1ebd86edb2b25925eeda8e02ef61b`

```dockerfile
```

-	Layers:
	-	`sha256:f51ba401f42494e66f9a4454e86c4b7b9abc2cab1deef0cd51e817906b872c2a`  
		Last Modified: Tue, 14 Jan 2025 05:27:56 GMT  
		Size: 2.5 MB (2538896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31d7a160e4e1fd77c4e1e21748a8199b9eee35525f0e0b211655adacb6f6f584`  
		Last Modified: Tue, 14 Jan 2025 21:00:58 GMT  
		Size: 26.4 KB (26436 bytes)  
		MIME: application/vnd.in-toto+json

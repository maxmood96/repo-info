## `node:20-bullseye-slim`

```console
$ docker pull node@sha256:65587343a439fe681ecd2e0446a9467df0165027f2b22337bbcc060b812fccda
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
$ docker pull node@sha256:39c9c05c1d210528330fd0c6449e320783236ba70732df98aefce7e6e5f78b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72772625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8acf90ea584f7a9829dfa2df712192b85084d47f2d5bd3e55b37292f9d6265c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 20 Nov 2024 16:05:40 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3448e5a7eb4e0eada9227262702537ce11064704ed69d75512357ca92b1c3fde`  
		Last Modified: Tue, 24 Dec 2024 22:30:09 GMT  
		Size: 4.1 KB (4063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004ba9b44b432f9bb9316e089b71c6dc12baa02f21ee1c342ba1f60609650593`  
		Last Modified: Tue, 24 Dec 2024 22:30:11 GMT  
		Size: 40.8 MB (40779520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a30d52194e70219a34ed16b7339142029aa4ecc88656b3dc07d6d44b040506`  
		Last Modified: Tue, 24 Dec 2024 22:30:10 GMT  
		Size: 1.7 MB (1735953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a02c3c0914f8a8d02aa98292250b6e38dae98f5f902bec76cb5db1479a258`  
		Last Modified: Tue, 24 Dec 2024 22:30:09 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:c50508b08f84012e874f49c14ee6c0ae0eaf3f29997ba02b1557c7edc7054683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2875269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dac6e3a799800eecd941d62f441b4bd9f92c836ad6f6fac0b079e9086ea679f`

```dockerfile
```

-	Layers:
	-	`sha256:c20c2e1b787fe7a6ccb044b6614db71ffc6c7f9355664e0016713d8904d5faa4`  
		Last Modified: Tue, 24 Dec 2024 22:30:10 GMT  
		Size: 2.9 MB (2850039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19cb271461e108177a6873198722259838a250209e1fd39050abc3fd9892620c`  
		Last Modified: Tue, 24 Dec 2024 22:30:09 GMT  
		Size: 25.2 KB (25230 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-bullseye-slim` - linux; arm variant v7

```console
$ docker pull node@sha256:19b037e3be2cd639b4f395af83692b76e8eddce1fb5f43d180e0bf78cb573aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64152830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352cdcc8632803de4e7dcd20225b824c5f288d578ebb773303a7cc9ab2e481d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 20 Nov 2024 16:05:40 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
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
	-	`sha256:0d436ac8a1fac914a00940d8604851d3414adc2ed370af15a8a5e6b319671b5b`  
		Last Modified: Tue, 24 Dec 2024 21:34:33 GMT  
		Size: 25.5 MB (25533937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47318865258b56c8f423e6c285736b44391c561f13893512a99985198498c47e`  
		Last Modified: Wed, 25 Dec 2024 04:14:14 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec05e40e49d37af60d4c11b6758a3d9a23f1c309305c6dd7d14c17a4f20d94e1`  
		Last Modified: Wed, 25 Dec 2024 04:16:36 GMT  
		Size: 36.9 MB (36878233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3215f4200d45a9e003c58ede214f93cf75acd96c212e4cdcf0b085825d1a5051`  
		Last Modified: Wed, 25 Dec 2024 04:16:35 GMT  
		Size: 1.7 MB (1736154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9fca1c9a9e83a9c4fa22a508abfe7e946b2f86b9f2729349b60e459d38a50e5`  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:576a5a0c392b7743675d84e5c42bb7531b124bb28d8c048b3b265af54e282612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2880859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703054d5840c0d0d5c8a984ebf07272d99ab5676112a4403c00447980af2ead0`

```dockerfile
```

-	Layers:
	-	`sha256:be15e31f56e1af5071edeb34964110336f30df4a96453930e59ba3aa250d4977`  
		Last Modified: Wed, 25 Dec 2024 04:16:35 GMT  
		Size: 2.9 MB (2855525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9893ebd4804b0af7420d56b71f5bdd1d5dd91a3196b294d2c42739735327b2b4`  
		Last Modified: Wed, 25 Dec 2024 04:16:35 GMT  
		Size: 25.3 KB (25334 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:e0c1158f524d606c7f9d4b51bd9253c34caa2070eadec2554c95ece024519bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71234577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3fd373344592ae90fc743c39180cbe36e5be56e6297938a190ffb5596636c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 20 Nov 2024 16:05:40 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb412e3b2b202d43dad301b615d095a2aeac586e7afba3cb90d6fd43ea294bb`  
		Last Modified: Wed, 25 Dec 2024 02:22:34 GMT  
		Size: 4.1 KB (4076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39310fd3ec97456fae02b7210353a6acb07fb18f197348ed1baa46de28dfca31`  
		Last Modified: Wed, 25 Dec 2024 02:26:39 GMT  
		Size: 40.7 MB (40749241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e15e776e701ee6346397f2ebafc093ecc3fba983ad6a4342ca7576129a1bbdb`  
		Last Modified: Wed, 25 Dec 2024 02:26:38 GMT  
		Size: 1.7 MB (1735960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e260dd5dbb9c864238aa5a71e77f9e9dbedd39b46056c9d9143afec3b8607ba`  
		Last Modified: Wed, 25 Dec 2024 02:26:38 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:815486dcd7d05953560b762f3fa7d4b1791612a46bde8bc88c1a4e5df84d271e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2875656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e05c1d7f933e9be5d2df867b73cbf5588bcbed70f2277631d0297284fe1f56`

```dockerfile
```

-	Layers:
	-	`sha256:f53fdce6898f2ae30def6287d95b8eb415a8bdd27a2649a5424981203c7128e9`  
		Last Modified: Wed, 25 Dec 2024 02:26:38 GMT  
		Size: 2.9 MB (2850290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c3f8d349f5631ef2b15d9acd7b93cc945a54e34e6d8db89fcb9fde5325174ef`  
		Last Modified: Wed, 25 Dec 2024 02:26:38 GMT  
		Size: 25.4 KB (25366 bytes)  
		MIME: application/vnd.in-toto+json

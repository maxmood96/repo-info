## `node:24-bullseye-slim`

```console
$ docker pull node@sha256:04661f7bb4bc68dafa620e06ce37c479585f455baf10e578be5032a1e24cbe24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:24-bullseye-slim` - linux; amd64

```console
$ docker pull node@sha256:440616cc91d77f4d0618fa1ebea7f824f5ea4148484e23dc829cd22a4136f82e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83111312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe6119b17f15220e277eee3b02c145787714121da403a90bd88fb486c17fdb1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Wed, 02 Jul 2025 21:10:14 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 02 Jul 2025 21:10:14 GMT
ENV NODE_VERSION=24.3.0
# Wed, 02 Jul 2025 21:10:14 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 02 Jul 2025 21:10:14 GMT
ENV YARN_VERSION=1.22.22
# Wed, 02 Jul 2025 21:10:14 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 02 Jul 2025 21:10:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 21:10:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jul 2025 21:10:14 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf495cbc928e049b5877dfea72bbb2e37f253b53666aa69e9bffa3b1f8ad01d`  
		Last Modified: Mon, 07 Jul 2025 20:56:39 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200923e907594b441baa0a0bf6ac210257b0d96b0aa0981ab22fe86fe751c045`  
		Last Modified: Mon, 07 Jul 2025 20:56:52 GMT  
		Size: 51.1 MB (51113244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278d8762c4e6b1a56ae83b82be6dff9cca3e05f3303d74e6631df9bbbec1494b`  
		Last Modified: Mon, 07 Jul 2025 20:56:39 GMT  
		Size: 1.7 MB (1737502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536e91f87b0539d0463b6455060108665d8bf9e1b4fb9e772d2df79dd05cd4fd`  
		Last Modified: Mon, 07 Jul 2025 20:56:39 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:24-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:c5d5c5a294169ace370ba993bdbdd81c59e5d34c7d76193dae053e130226d825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aff44ea9bdd4ba04e07a5d9dde62e9a8c3a338423b73bea43d9488768b74414`

```dockerfile
```

-	Layers:
	-	`sha256:fa0576dc572c912fb754aca06d265130fb72e30a51e0095db85363b5d4154860`  
		Last Modified: Mon, 07 Jul 2025 21:41:06 GMT  
		Size: 3.0 MB (2965800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7bb8a33f962f2f2b8bb7820cd7f78b3689b09666cd9ea825dd0d9dee703d4cb`  
		Last Modified: Mon, 07 Jul 2025 21:41:06 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `node:24-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:63b0feee19bd99b16dd2240f3763c5436a467f6b0b8c93c13a8cedcaa1405b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81088496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c289ad52f877cbf64b2a398898c1e1b74247720f2e3fbfdf2e8e4018b0fbc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 25 Jun 2025 02:25:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Wed, 25 Jun 2025 02:25:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENV NODE_VERSION=24.3.0
# Wed, 25 Jun 2025 02:25:22 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENV YARN_VERSION=1.22.22
# Wed, 25 Jun 2025 02:25:22 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 02:25:22 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2372e42b3fd94480b9a5d512a633db71dead07be1f38861d85e844344bd1ee8`  
		Last Modified: Tue, 01 Jul 2025 07:27:11 GMT  
		Size: 4.1 KB (4079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41e00cbef8229e341f6903c3aff9d2fa5b6f43ccafec4510836b7b636569bcc`  
		Last Modified: Tue, 01 Jul 2025 07:27:21 GMT  
		Size: 50.6 MB (50602414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74a21a88e2213a0b56bd6b7342115a38c761c4985094b5c84d4bc10d240d407`  
		Last Modified: Tue, 01 Jul 2025 07:27:12 GMT  
		Size: 1.7 MB (1737417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7fbb4c4d851aa26f2b40c32d090126bde3ec57790a8f86a4b97d476db5ed22`  
		Last Modified: Tue, 01 Jul 2025 07:27:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:24-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:01fbff1bb48c06e94b894fa02bd3c8e8a10f530e515c706392274839e633fbbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12d8df57a30eeef8dc26d492b801826d95aa9ef30c301fca729af0cfc2c9638`

```dockerfile
```

-	Layers:
	-	`sha256:06bcdadc987ed11df0b6db7ce3342bab3ab01d1be8467883e459bb5019ecff6f`  
		Last Modified: Tue, 01 Jul 2025 09:39:43 GMT  
		Size: 3.0 MB (2966063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64b05a3c72272c26441b70befc2b277e4f054e582eb664b74234d3d4c691c375`  
		Last Modified: Tue, 01 Jul 2025 09:39:44 GMT  
		Size: 25.8 KB (25789 bytes)  
		MIME: application/vnd.in-toto+json

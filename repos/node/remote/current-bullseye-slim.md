## `node:current-bullseye-slim`

```console
$ docker pull node@sha256:d4127ff3b5d336cb963c12ed4f76a7334e169e0223469b67a3dbaa4d632f5c10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:current-bullseye-slim` - linux; amd64

```console
$ docker pull node@sha256:96d83bc83222c80ffe4d13a19167e2af0a80eb7a78e00d4ea4f01b72628b33f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81078764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d80876e0e3f3363503f44090e97f8789cb448633874c98422609cf0ee4d4cbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:44:59 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:45:19 GMT
ENV NODE_VERSION=25.8.1
# Mon, 16 Mar 2026 22:45:19 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:19 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:45:30 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:45:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:30 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1743692f3a3eeae1ded67834da75c5a70a094f6f720a5848fd45f8b6e518bd`  
		Last Modified: Mon, 16 Mar 2026 22:45:44 GMT  
		Size: 4.1 KB (4070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cb8fa432846f4c8f43d8c836984f29a793905752c2bf3dc32021237ea72d8d`  
		Last Modified: Mon, 16 Mar 2026 22:45:46 GMT  
		Size: 49.1 MB (49080138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167519a04ad2f9663240aa50c32f8eba02df1a61636029ed6e1f83df231a9af8`  
		Last Modified: Mon, 16 Mar 2026 22:45:45 GMT  
		Size: 1.7 MB (1736281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66891ebc2706cf9c31e45b16970f950f5edf446a977ec85441c7ef26373359c1`  
		Last Modified: Mon, 16 Mar 2026 22:45:45 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:b13a68d74282889b6badc40259ce46d0f276b4a486a767a63e3c25d7bcbcf1f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2918379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70fad19e4bbe25a5722ff76ed8cfa3a3dbd3aac9c9382054c50bef9a925f214f`

```dockerfile
```

-	Layers:
	-	`sha256:ac9e2fef52d04eb9e8633b8d73a5f2cd0c876cbd0703ceec62a00a2ab80c79c5`  
		Last Modified: Mon, 16 Mar 2026 22:45:45 GMT  
		Size: 2.9 MB (2892353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea22da2af14942781b867a41797ae22901b6c714f54098e45f039d36c9ea8232`  
		Last Modified: Mon, 16 Mar 2026 22:45:44 GMT  
		Size: 26.0 KB (26026 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:263101af7a11043115ccdc8dad77a760ee3db4f784f25ebfe5f6e456e762ea99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79867051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f2af0f9fb61302c27e4277a9de2b52298aeac1996948052d8bdb58e34ae14a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:47:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:47:27 GMT
ENV NODE_VERSION=25.8.1
# Mon, 16 Mar 2026 22:47:27 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:47:27 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:47:38 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:47:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:47:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:47:38 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5e037c1560eca86d0c93fbbd24936a83edd0fce9851f24d3bc86a31103cf7e`  
		Last Modified: Mon, 16 Mar 2026 22:47:52 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e111e9dc68e48b8def58dce15c87196ccfad88188d2a778c3f3cdd0d587d50`  
		Last Modified: Mon, 16 Mar 2026 22:47:54 GMT  
		Size: 49.4 MB (49381809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e4f3a49663dea6ebe0473c1b022d298a5ea9f0f9dec3e33efdf2e41103347f`  
		Last Modified: Mon, 16 Mar 2026 22:47:53 GMT  
		Size: 1.7 MB (1736196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e47197beedcb7d9b8f1d9a5cc2acd874a9450801f89a1d7686f82b0f35de5b`  
		Last Modified: Mon, 16 Mar 2026 22:47:52 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:3a60ee72c74a486e37f39dd12f88c6d0e5a5140e72f46809cfcae41f482f7ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2918791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877c520e2f4fe3a71a8a86c460c2d9928fca7fe11306116a51c09f0decb14b2b`

```dockerfile
```

-	Layers:
	-	`sha256:025372351a8002a81efd5cc6d2605dc9d16db2fab6de2360dcb02fa6bbed9428`  
		Last Modified: Mon, 16 Mar 2026 22:47:53 GMT  
		Size: 2.9 MB (2892617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2c9a593738267ef5cb6afb437a250909081108c3aeea893f4ba6ecb65f7d5ae`  
		Last Modified: Mon, 16 Mar 2026 22:47:52 GMT  
		Size: 26.2 KB (26174 bytes)  
		MIME: application/vnd.in-toto+json

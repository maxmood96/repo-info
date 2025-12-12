## `node:krypton-bullseye-slim`

```console
$ docker pull node@sha256:99c26b45ed43541718e38d5778792f38c0f3655dd0e1415f24c61782a62b0a1a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:krypton-bullseye-slim` - linux; amd64

```console
$ docker pull node@sha256:548ec1c93913139d3729bec2ae3fe43f9521745ecad300135aa1ecd169fbcf1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81135061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb2eddbf9b0e609cc1ff1e4cc28b5eef0e205255512b5e1fd31230c2e2aa6f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 19:35:59 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 11 Dec 2025 19:36:17 GMT
ENV NODE_VERSION=24.12.0
# Thu, 11 Dec 2025 19:36:17 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 11 Dec 2025 19:36:17 GMT
ENV YARN_VERSION=1.22.22
# Thu, 11 Dec 2025 19:36:26 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 11 Dec 2025 19:36:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Dec 2025 19:36:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Dec 2025 19:36:26 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358fbbd1a34b3b42c29ec8f7b13f2fe108fe95879f20f21a41b2f6e71a2de201`  
		Last Modified: Thu, 11 Dec 2025 19:36:47 GMT  
		Size: 4.1 KB (4067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4523204bdab7f4e3a140b3e2bd7179574b4f35829bf9311ddcf4e199c8cb5d1a`  
		Last Modified: Thu, 11 Dec 2025 19:36:51 GMT  
		Size: 49.1 MB (49136055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec79c3348d67448090a70af696e51bad738542c0bc1d3339de1cde0ba1a11350`  
		Last Modified: Thu, 11 Dec 2025 19:36:47 GMT  
		Size: 1.7 MB (1736027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb29022251261d4bfc4325e180c514467cb46179da02d288c26a62a5a67ed792`  
		Last Modified: Thu, 11 Dec 2025 19:36:47 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:krypton-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:f1bdb75314b13381904e61e58c65db4c44087f4c9e382eb778af69fd18294e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7b9889ff5c6b86eaf7bec774ca46e01f4468b216fb12aa5fd2df0783879b44`

```dockerfile
```

-	Layers:
	-	`sha256:019d191b642cc109430440cf2a889246743e0d328d5065d0ad0667f938157d55`  
		Last Modified: Thu, 11 Dec 2025 22:40:24 GMT  
		Size: 3.0 MB (2956798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec9c0d99618b512c8f8a3e381dd00962036d09eee5ac9a4272fe2edef3e9d663`  
		Last Modified: Thu, 11 Dec 2025 22:40:43 GMT  
		Size: 26.0 KB (26046 bytes)  
		MIME: application/vnd.in-toto+json

### `node:krypton-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:74d10b7d56214455ce9792fcd4774aa007c99186d82e2be354b8f5eb0c1ad339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79639096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b116302f8e8909c1af9bd0bb8e6c264b62576ebfe5c4abad545d8c558c38d9cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 19:34:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 11 Dec 2025 19:34:27 GMT
ENV NODE_VERSION=24.12.0
# Thu, 11 Dec 2025 19:34:27 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 11 Dec 2025 19:34:27 GMT
ENV YARN_VERSION=1.22.22
# Thu, 11 Dec 2025 19:34:38 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 11 Dec 2025 19:34:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Dec 2025 19:34:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Dec 2025 19:34:38 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77a850dbc055855fb9c037665d86a2d8a7dfd6f0459feefcaf1c852567bfc75`  
		Last Modified: Thu, 11 Dec 2025 19:34:59 GMT  
		Size: 4.1 KB (4075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd11b37317bf603062ed5d7155e00b541d1567fad17db9f70518a5ae88b3555`  
		Last Modified: Thu, 11 Dec 2025 19:35:03 GMT  
		Size: 49.2 MB (49150131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d9cc5472918503f1853e332f64403f0d91ad4d9c6b1281b0f5c3c4de256190`  
		Last Modified: Thu, 11 Dec 2025 19:34:59 GMT  
		Size: 1.7 MB (1735963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c677dc52d8982fc57ba6213ebab0cfa08d9ac6c3d1aa5f520c756299057f6ec6`  
		Last Modified: Thu, 11 Dec 2025 19:34:59 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:krypton-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:0cfe70acd82441c5066696c9916031ac9fdf8b4d9156003d15f33327aa03997c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688b5136acb21bb56f4176da425213c67463bb5ddedfb2ea666c66fff7a7c2a0`

```dockerfile
```

-	Layers:
	-	`sha256:7dbc3b119ce97a9e235d107d7030a8533ef94eb02106247a28585c977fd81d37`  
		Last Modified: Thu, 11 Dec 2025 22:41:05 GMT  
		Size: 3.0 MB (2957061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:031ec93515c54222af5903953cab558106058008ac30399eb502ee5a2d4a012d`  
		Last Modified: Thu, 11 Dec 2025 22:41:06 GMT  
		Size: 26.2 KB (26192 bytes)  
		MIME: application/vnd.in-toto+json

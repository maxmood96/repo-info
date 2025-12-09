## `node:iron-bullseye-slim`

```console
$ docker pull node@sha256:8cb658a3772883ecba0391fe1249689372622fbd40660130ab3d47105f89fc20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:iron-bullseye-slim` - linux; amd64

```console
$ docker pull node@sha256:7c35f679b5bdace0d6a60d7b8f76db58e0935088f722eab15c0ef55720daa7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73008795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b0f86d1a8c5efd0ef2feebdd514742de89b03b2882dba9f2e5606ca1d6152a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 25 Nov 2025 16:52:38 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 25 Nov 2025 16:52:56 GMT
ENV NODE_VERSION=20.19.6
# Tue, 25 Nov 2025 16:52:56 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 25 Nov 2025 16:52:56 GMT
ENV YARN_VERSION=1.22.22
# Tue, 25 Nov 2025 16:53:07 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 25 Nov 2025 16:53:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Nov 2025 16:53:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Nov 2025 16:53:07 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d467d4605f2a07f6b14e870fd315c43e2834ca3c9241f69b8a41a9b1322b6e57`  
		Last Modified: Tue, 25 Nov 2025 16:53:28 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a989c3c1e315cc7b9ec09a1fd137c3ff2d518242d178ded127afea7f4d0eff`  
		Last Modified: Tue, 25 Nov 2025 16:53:40 GMT  
		Size: 41.0 MB (41009713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7075d62dcb5a35ac7fa8df035957d1e66ce701395955b6bb2e9e610ce92e4aa3`  
		Last Modified: Tue, 25 Nov 2025 16:53:29 GMT  
		Size: 1.7 MB (1736078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e713a3751b047f8abc24b839fb41b3fa7096d756135dc4fa4d215e768838fd2`  
		Last Modified: Tue, 25 Nov 2025 16:53:29 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:iron-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:2041eb08d5772f5cecacc11ad5a518cee95b919cc7910cc5b3b554bd1016fc77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac06dfbf551dd905e3aa7e25ecd953f701a63181695637cdfc409e90a742d1c`

```dockerfile
```

-	Layers:
	-	`sha256:c215a4716f19ebde7e423113e5d399600b9fa165faef3a9aea887723282a7387`  
		Last Modified: Tue, 25 Nov 2025 19:39:51 GMT  
		Size: 3.0 MB (2956824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:331e8ee713e6b5f4f411fe5ec4a486d5e3c3bbf664eb6a9a850c2959287e2aad`  
		Last Modified: Tue, 25 Nov 2025 19:39:52 GMT  
		Size: 25.7 KB (25724 bytes)  
		MIME: application/vnd.in-toto+json

### `node:iron-bullseye-slim` - linux; arm variant v7

```console
$ docker pull node@sha256:cb5f2ed616cc9ae081cc9d063fee3bf1b6a4026ad8651a87ef1af1814b0b8883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64375551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ea22e41331009a43b258ec916298602a967fedeea62a2433705a63a477c6cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:23:29 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Dec 2025 00:23:50 GMT
ENV NODE_VERSION=20.19.6
# Tue, 09 Dec 2025 00:23:50 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 09 Dec 2025 00:23:50 GMT
ENV YARN_VERSION=1.22.22
# Tue, 09 Dec 2025 00:24:02 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Dec 2025 00:24:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:24:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:24:02 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:189d7c8243253070696fcc5bcaa526823c4016a5dd57614057cc9107756082b2`  
		Last Modified: Mon, 08 Dec 2025 22:16:40 GMT  
		Size: 25.5 MB (25546219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abd443f31f401aec926c8a7e18337b295ef34893568941266ee21cf75a69c6a`  
		Last Modified: Tue, 09 Dec 2025 00:24:21 GMT  
		Size: 4.1 KB (4056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf460c15889a46559c89ca23738d825b46da2571ab2e4c2339c18343c4c86be`  
		Last Modified: Tue, 09 Dec 2025 00:24:26 GMT  
		Size: 37.1 MB (37088604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b344f254a6db0e116a8fba8e91e2095abe3cb2c45f64e97d468a1c5cee53ac74`  
		Last Modified: Tue, 09 Dec 2025 00:24:21 GMT  
		Size: 1.7 MB (1736226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153dfb1b06edbebd7b19f0ff20c5312993dba47e62174a185acb412d3738eacd`  
		Last Modified: Tue, 09 Dec 2025 00:24:23 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:iron-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:726f7ec791f81ef135c8d57f2fb13717bef26ccaf6a1766497bfa36096067212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a892654431225c7adb9ce44f5f7046d248d777a070817c1356ecfbc55ebf51`

```dockerfile
```

-	Layers:
	-	`sha256:fd65cf64bbb2b437fff804ad24c6719f80342e61ef90623f967c8fc1b30aa53d`  
		Last Modified: Tue, 09 Dec 2025 01:39:06 GMT  
		Size: 3.0 MB (2962600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db3ae47c136c789a658f9827455e3ffd69a05778e12e0ec5278d8e006beb64f8`  
		Last Modified: Tue, 09 Dec 2025 01:39:06 GMT  
		Size: 25.8 KB (25830 bytes)  
		MIME: application/vnd.in-toto+json

### `node:iron-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:d14f6e9155e393ad78d80c8d11e9a3a119e122d769c6aa47f8f9dbd8e0fcdd31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71450962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d82b43ec9559c40037ee7b48075fd2eee153fbc072c2e64d7c85e306ef2c61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 25 Nov 2025 16:58:23 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 25 Nov 2025 16:58:41 GMT
ENV NODE_VERSION=20.19.6
# Tue, 25 Nov 2025 16:58:41 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 25 Nov 2025 16:58:41 GMT
ENV YARN_VERSION=1.22.22
# Tue, 25 Nov 2025 16:58:51 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 25 Nov 2025 16:58:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Nov 2025 16:58:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Nov 2025 16:58:51 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255572700069098c063df2489efa06653592dfba46a3adfab323f9ffcc4853b0`  
		Last Modified: Tue, 25 Nov 2025 16:59:17 GMT  
		Size: 4.1 KB (4077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a677e49d3a3e735d7b08d3b7c0e3171932158b7c2fd91519a3bf793ee141d4b`  
		Last Modified: Tue, 25 Nov 2025 16:59:28 GMT  
		Size: 41.0 MB (40962000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493d88cca09b64b296bc4913af739a53daac27d70b32bf5626f1f16d3e877bec`  
		Last Modified: Tue, 25 Nov 2025 16:59:18 GMT  
		Size: 1.7 MB (1735971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6a1b03234d88e6766854eba2d8d7f3438644b37391be030b2d60d42b6df9db`  
		Last Modified: Tue, 25 Nov 2025 16:59:17 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:iron-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:02a693ee76fe4f609da113b13e3e74646e1a9d1dff5f7c253b5d6562133323e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1698d195f14b530d2e0eea5bcbe0418b1519ba047a5f52ca723f68c5383b2664`

```dockerfile
```

-	Layers:
	-	`sha256:81c0655d07a742cc7ca22308a16ced106bfb49d1b214b021295fe299d402921b`  
		Last Modified: Tue, 25 Nov 2025 19:40:52 GMT  
		Size: 3.0 MB (2957075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2a8c5de5494cecbadd6543f1f1260b012a38c5eeb5d604c5f78e6f0aff6da4b`  
		Last Modified: Tue, 25 Nov 2025 19:40:53 GMT  
		Size: 25.9 KB (25858 bytes)  
		MIME: application/vnd.in-toto+json

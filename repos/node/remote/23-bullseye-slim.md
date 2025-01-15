## `node:23-bullseye-slim`

```console
$ docker pull node@sha256:b460321361086df4aed3f33127901451fdfd34bac7a7c38d2c5a4c33f2c0faf3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:23-bullseye-slim` - linux; amd64

```console
$ docker pull node@sha256:13ef9e96fff22dbc0fe227fcee0b141a539d423bab3dc9a466bc4b2e680b7005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81751197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a5a70dd38aaa472f024d2a55bfddd6c13c5a79935121c292fb1379921cb95d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 07 Jan 2025 23:47:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Tue, 07 Jan 2025 23:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 07 Jan 2025 23:47:58 GMT
ENV NODE_VERSION=23.6.0
# Tue, 07 Jan 2025 23:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 07 Jan 2025 23:47:58 GMT
ENV YARN_VERSION=1.22.22
# Tue, 07 Jan 2025 23:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 07 Jan 2025 23:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 23:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jan 2025 23:47:58 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 20:33:08 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d409117160282638980171911fa112a419bbcfcd4acb3e1c40c287256b05b00a`  
		Last Modified: Tue, 14 Jan 2025 02:36:18 GMT  
		Size: 4.1 KB (4068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b5ccd5b8fcfd0644349285d81f5ea1e92eb2da20bf1cad593a663507719753`  
		Last Modified: Tue, 14 Jan 2025 20:34:20 GMT  
		Size: 49.8 MB (49758080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ba6382e625bdc268fa60a2507c77583e4d605a72bb785352a22204ac4a1b4`  
		Last Modified: Tue, 14 Jan 2025 20:34:17 GMT  
		Size: 1.7 MB (1735937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0210a9b8139a865324c21af8ff3daec39ea9774187a452d89baa6906d9f3a0a0`  
		Last Modified: Tue, 14 Jan 2025 20:34:16 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:23-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:541df630ae391faf382b2ede39517b095fa4a6f779d5bc33cc6d0e95cf91c849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2893085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc35b70252f60f0003015ee053a8be4d58b3544b38ea47a659aec2746b67330`

```dockerfile
```

-	Layers:
	-	`sha256:bde7601b72daa3da464423cd34935171c88df3b66d9606b563a2c315e6af3eed`  
		Last Modified: Wed, 15 Jan 2025 00:38:52 GMT  
		Size: 2.9 MB (2867545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b547121e0b40fe61fda6fac1081a56a5c4c8b053602a5533209fa84ed2b325d`  
		Last Modified: Tue, 14 Jan 2025 02:36:18 GMT  
		Size: 25.5 KB (25540 bytes)  
		MIME: application/vnd.in-toto+json

### `node:23-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:3bc767f5131c359655e0ab753cf28cb492027127fc39ec63c181af9a5c2c1540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79725056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6911d739dd2fb325f287f55cb4138d5e3ecac724b6f67c0b54c57573dd79e745`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 07 Jan 2025 23:47:58 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Tue, 07 Jan 2025 23:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 07 Jan 2025 23:47:58 GMT
ENV NODE_VERSION=23.6.0
# Tue, 07 Jan 2025 23:47:58 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Tue, 07 Jan 2025 23:47:58 GMT
ENV YARN_VERSION=1.22.22
# Tue, 07 Jan 2025 23:47:58 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 07 Jan 2025 23:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 23:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jan 2025 23:47:58 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 20:33:33 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f00206607918e028d5458011dfafffa79b61f1beecad6f41bc19154e29a670`  
		Last Modified: Tue, 14 Jan 2025 07:33:08 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e2fd8513fd51b2c024431596d60eb0e0d58204d20e5cc1265f1a02fb2e826e`  
		Last Modified: Tue, 14 Jan 2025 21:20:27 GMT  
		Size: 49.2 MB (49239702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb43a1c6b6b0eae01e6f506d760680e364864e4b0c3f19bd617a94a801563c77`  
		Last Modified: Tue, 14 Jan 2025 21:02:04 GMT  
		Size: 1.7 MB (1735920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3cd911be5fc6d02355ccf2dd5b7c1824a63b5d6d03dee85b1fbfd29df274ac`  
		Last Modified: Tue, 14 Jan 2025 07:33:08 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:23-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:4d9353c108f0c46b35ce426218f1112b0ca3b5674232245538306bd50a77140c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2893494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2519750dd8eaf30bf061cc0f054cbf22e1663967312b2a1435dd8d0f2c3538e`

```dockerfile
```

-	Layers:
	-	`sha256:23e445d4e66db32cf3152bedb1ec22d05c8167994023e6ef70abde106136313c`  
		Last Modified: Tue, 14 Jan 2025 07:33:08 GMT  
		Size: 2.9 MB (2867808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a68dcd4a2b7c5710d0fe7f0fd61c9894e8dd6a9951bc13e3d8c3f6f949e9a1a`  
		Last Modified: Tue, 14 Jan 2025 07:33:08 GMT  
		Size: 25.7 KB (25686 bytes)  
		MIME: application/vnd.in-toto+json

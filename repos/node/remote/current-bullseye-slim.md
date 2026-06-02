## `node:current-bullseye-slim`

```console
$ docker pull node@sha256:21a8644a91de29482126d1290cbe17cbf879e8dc9a18c00888af4e0e9b62dc82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:current-bullseye-slim` - linux; amd64

```console
$ docker pull node@sha256:a7d8a5a63e24f8f1db3147b5389ff65b9f372f86f504c39842c06a5214d2d3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84832728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60655a12505dd21653644474e9e167efde65563db474bbe942afb3d8c9916443`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Mon, 01 Jun 2026 22:46:53 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 01 Jun 2026 22:47:10 GMT
ENV NODE_VERSION=26.3.0
# Mon, 01 Jun 2026 22:47:10 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 01 Jun 2026 22:47:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jun 2026 22:47:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:47:10 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad230436996a4ef513270d160a8a4afd0be769031672acdd45b373ec6121a4ae`  
		Last Modified: Mon, 01 Jun 2026 22:47:24 GMT  
		Size: 4.1 KB (4077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d13df81928c5b67ff1c473b80ebe0ac7e9fe5a3128e4b6d8bb81a390f38ff1`  
		Last Modified: Mon, 01 Jun 2026 22:47:26 GMT  
		Size: 54.6 MB (54570606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079aa4c308960a04ae9dfb67ed2e7f5fbf39b4a6fb234e8ae62ea87cea549b35`  
		Last Modified: Mon, 01 Jun 2026 22:47:24 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:1015bc02e7a7eb089dae2af1773450ea0c5a2aa75f0ec029b6026f49dcb0038a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2899119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625c70f79f029ddf3b6eb1ad745c4071544ab811d888b9513ad58b13624e9a18`

```dockerfile
```

-	Layers:
	-	`sha256:3309b852dc9399452bc44a4e21544a9e9273e9944c4034a3ac07c018af78dc6f`  
		Last Modified: Mon, 01 Jun 2026 22:47:25 GMT  
		Size: 2.9 MB (2880405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feb877543897c5f4af29a0edb1d4cd2f9fb1c5771d5ed3fed55bd5cb81188173`  
		Last Modified: Mon, 01 Jun 2026 22:47:24 GMT  
		Size: 18.7 KB (18714 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:b76826c1d9672e9dd24368d44a0af06517a364c3a3a3f9ed3a2ce15c26d54d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83505846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64c9dce6c305f1d6f4807a6437e1c31ba464f8f3b77c58286ac31ccb10b9602`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Mon, 01 Jun 2026 22:46:51 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 01 Jun 2026 22:47:09 GMT
ENV NODE_VERSION=26.3.0
# Mon, 01 Jun 2026 22:47:09 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 01 Jun 2026 22:47:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jun 2026 22:47:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:47:09 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f0d33d9462b7b5e930ef8222e92316de7b6bc0856658472c0f7b1ace882306`  
		Last Modified: Mon, 01 Jun 2026 22:47:25 GMT  
		Size: 4.1 KB (4078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a49e884806d7037cb164bcafd9c94061cd48f1385b386f1539af22cd55d81`  
		Last Modified: Mon, 01 Jun 2026 22:47:27 GMT  
		Size: 54.8 MB (54758350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee02cc725c5c9cf2424b8798d2f59e9129a677ad3caee0618886bccef5d4cb6a`  
		Last Modified: Mon, 01 Jun 2026 22:47:25 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-bullseye-slim` - unknown; unknown

```console
$ docker pull node@sha256:8870fe64232555efc67d52019ffde5ee942d7f93cd71b939374db04b1beebc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2899515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19aa41ef57b3beb26a2f2067aad1cb7e913dd4ab628f3d6168bf9744188e8708`

```dockerfile
```

-	Layers:
	-	`sha256:e2d7efa3a2cff57ab48ed86da258c2c0b51be7878d78d547785ba1e8e869bd37`  
		Last Modified: Mon, 01 Jun 2026 22:47:26 GMT  
		Size: 2.9 MB (2880669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca89e3b7bb907656dd8339828f9135903eb1377cef7c1e827f52edd2c5b37350`  
		Last Modified: Mon, 01 Jun 2026 22:47:26 GMT  
		Size: 18.8 KB (18846 bytes)  
		MIME: application/vnd.in-toto+json

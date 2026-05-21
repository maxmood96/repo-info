## `node:slim`

```console
$ docker pull node@sha256:1e738cb88890a15c71880323fbc35a739b7bbc703d72e8bfd1613128f8182f78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `node:slim` - linux; amd64

```console
$ docker pull node@sha256:d7c0ad47d5035cf088ef219b95a7a56731c59d040796cd6caa870fd500a080a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84187426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f06df0593a9a4643a9114dab53d9e2238514931546fed52590ac01516773b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 20:11:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 20 May 2026 20:11:59 GMT
ENV NODE_VERSION=26.2.0
# Wed, 20 May 2026 20:11:59 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 20 May 2026 20:12:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 20:12:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 20:12:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b282f6f0f8050994f2db9ed9b7dab7e65c18a033bf33092ee8be1180cb8859`  
		Last Modified: Wed, 20 May 2026 20:12:14 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0582d06cd92d0eca5d2153c3fc98b8dced38c59dc4696fd73fda50cd94cb71df`  
		Last Modified: Wed, 20 May 2026 20:12:16 GMT  
		Size: 54.4 MB (54403736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcecaf24afa9836600691386a34c2d0eb088a4e1751a54dd5344108aa3f3ac4`  
		Last Modified: Wed, 20 May 2026 20:12:14 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:slim` - unknown; unknown

```console
$ docker pull node@sha256:92a89f0781a4572e1a1d8ea581741e19c310a0e8230eb83ee43cc5897b5a2af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4254700bcd8edde3988d160bdf8ccca78cd7704312ff889b104477b04d19b2c0`

```dockerfile
```

-	Layers:
	-	`sha256:d1007f17d61ab370aae848d0671ddb7beee4b03f88b70a428528fe8dbddfb003`  
		Last Modified: Wed, 20 May 2026 20:12:14 GMT  
		Size: 2.2 MB (2201397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0fa9cd0573fd82e59f4336cbfd3c4035edcfda4385a600d4c573418e3bb50fd`  
		Last Modified: Wed, 20 May 2026 20:12:14 GMT  
		Size: 20.2 KB (20183 bytes)  
		MIME: application/vnd.in-toto+json

### `node:slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:65ba0c768d01e188fb904588ad65e7e396a7d27ba3b457fa65285b2de4295a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84733697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce737f1767fbb731f073f64fa2cfe0232954efdd79c2a28bc09107d2e2729ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 20:12:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 20 May 2026 20:12:57 GMT
ENV NODE_VERSION=26.2.0
# Wed, 20 May 2026 20:12:57 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 20 May 2026 20:12:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 20:12:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 20:12:57 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53821bcef7b6ae94eebce76921abed2bad0aa0cdbbb436afa023690cf583a353`  
		Last Modified: Wed, 20 May 2026 20:13:12 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdfa616d6eadfbc7ea794ab67ca53917d2593b0edef42a95091e327072e97f6`  
		Last Modified: Wed, 20 May 2026 20:13:15 GMT  
		Size: 54.6 MB (54588022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1c7e4eb3278fbd3eff1dfb6ab5416f2c393c07f74db19cc343d95824c39da4`  
		Last Modified: Wed, 20 May 2026 20:13:12 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:slim` - unknown; unknown

```console
$ docker pull node@sha256:4a9149a2fa499b473cb299d42f12c5b6fb14ebc904690c0f031501f6c9fe4d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc707095bd566686c55ce6f74b3493857cf4690fad8fe5b5f05df708c999fd29`

```dockerfile
```

-	Layers:
	-	`sha256:798770b0db3147aec0af9673f66f8fac922be0e5a1e25075aa15e14ffafdfbb0`  
		Last Modified: Wed, 20 May 2026 20:13:13 GMT  
		Size: 2.2 MB (2201720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e9ed06dfb7d8b1aec24f9d27f14400e305e8eda3210891d0db6fbeecef535a1`  
		Last Modified: Wed, 20 May 2026 20:13:12 GMT  
		Size: 20.4 KB (20374 bytes)  
		MIME: application/vnd.in-toto+json

### `node:slim` - linux; ppc64le

```console
$ docker pull node@sha256:fb717eb61fdf882560595427560ec3811ff2ceb5cc71c77e6188f2b5188963a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90304339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd83a67fda67dfc453cc0dba8266fdd0569a504d31b75a0aab7562a09dcd481c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:27:40 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 20 May 2026 20:11:28 GMT
ENV NODE_VERSION=26.2.0
# Wed, 20 May 2026 20:11:28 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 20 May 2026 20:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 20:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 20:11:28 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c1e8f1e5873cf1532c3945663b6287ea6f6ea91abd4225bfbcf116e5c0af15`  
		Last Modified: Wed, 20 May 2026 01:30:28 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4510145f23fb35362c4c85fd156b622fb1c8511aa36bdefa543228a533f2925`  
		Last Modified: Wed, 20 May 2026 20:12:01 GMT  
		Size: 56.7 MB (56700129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd32f36b541c0964992f465032153bfc988ae1dbdec73557147b1ca7be64806`  
		Last Modified: Wed, 20 May 2026 20:11:59 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:slim` - unknown; unknown

```console
$ docker pull node@sha256:aa35a0eeb498f8fd3642fa3e8285cf583e6af3197d0f7367802f7b69e9eef51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2225218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350d20d5315a3b7e69886e961c5147588b4f0c01a89d9c950179569cd3db7e84`

```dockerfile
```

-	Layers:
	-	`sha256:a4e845e0b646fb5c051d7b08bc98315d3055462b42bd8f203ad2b368bfa78ed5`  
		Last Modified: Wed, 20 May 2026 20:11:59 GMT  
		Size: 2.2 MB (2204953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc664276b213ae74c5066a29cab436a4f9ac294c57ad184a79314180a0ab7b6`  
		Last Modified: Wed, 20 May 2026 20:11:59 GMT  
		Size: 20.3 KB (20265 bytes)  
		MIME: application/vnd.in-toto+json

### `node:slim` - linux; s390x

```console
$ docker pull node@sha256:c6d3aeb64a865f29dc902c3dae6bde4196fda6146a15ac7899b0266860405567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86248530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaad8ca1cc46cf7f61206871f4323bdbb152a4bf8d6a786b101d593f744ff07`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:24:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 20 May 2026 20:10:09 GMT
ENV NODE_VERSION=26.2.0
# Wed, 20 May 2026 20:10:09 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 20 May 2026 20:10:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 20:10:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 20:10:09 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dda7c421ec4e1e84087911636bde652a1aa21ee63ae56f3e1f524b5d0a59b6`  
		Last Modified: Wed, 20 May 2026 00:25:20 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fb484ca2141aca1f9699ace45ef6197578b74b1cb1a55aaa7b95e3ca761999`  
		Last Modified: Wed, 20 May 2026 20:10:36 GMT  
		Size: 56.4 MB (56398848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf126b025fa0cbae2722fdc2b9b9bf4c1f151917797b1cbfc62280c913a68828`  
		Last Modified: Wed, 20 May 2026 20:10:35 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:slim` - unknown; unknown

```console
$ docker pull node@sha256:be16255a920d384daf4fd699aab969e9bd88eafe149f22d345f14b8cd052cc51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2223025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d919b9c9fe9afa0fc7978208accd1968ea647e2cda4e79f30cc2143f5befb0f`

```dockerfile
```

-	Layers:
	-	`sha256:e66cebbf036ccfea5d7824337839ce6cbabfeded99f96e080f6d6a69e6adbb08`  
		Last Modified: Wed, 20 May 2026 20:10:35 GMT  
		Size: 2.2 MB (2202843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eddfbe0105a76870a49ab96ac63f0eb54719c1866c589fd8cd011e1d107776f2`  
		Last Modified: Wed, 20 May 2026 20:10:35 GMT  
		Size: 20.2 KB (20182 bytes)  
		MIME: application/vnd.in-toto+json

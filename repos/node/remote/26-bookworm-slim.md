## `node:26-bookworm-slim`

```console
$ docker pull node@sha256:79723b41edbedf595f62e943a9f8b0ba9af5b1e61045c5f8f59c2c02c1212a16
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

### `node:26-bookworm-slim` - linux; amd64

```console
$ docker pull node@sha256:3101b78c867e29d6975bd96eac672ef9f1d75efe29973b430231c22ef9d1b47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82783684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8217a5cb61ba5df4790f99a428fed34425b4cd8960eebf9aaf66e89cc13b870`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Mon, 01 Jun 2026 22:46:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 01 Jun 2026 22:46:40 GMT
ENV NODE_VERSION=26.3.0
# Mon, 01 Jun 2026 22:46:40 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 01 Jun 2026 22:46:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jun 2026 22:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:46:40 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139b7e23849efcd709afe27201630e31043d92f7c93c4871dec379ada96d9fd0`  
		Last Modified: Mon, 01 Jun 2026 22:46:54 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba3529ad7a861601fec85fdf2caa3bdbfd33a9c06a37384e57eb939b63f41cc`  
		Last Modified: Mon, 01 Jun 2026 22:46:56 GMT  
		Size: 54.5 MB (54546382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9268b708d860d13a510a51c9985c686665348656026c7e6a18322c6f420a8f1`  
		Last Modified: Mon, 01 Jun 2026 22:46:54 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:26-bookworm-slim` - unknown; unknown

```console
$ docker pull node@sha256:9358a85f5c1c4281cda55609970e2cd20aa8098274df5d08a09e6152827bbf25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2591648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3fae8078594eb05c2a95fcc448573d65b5fd2d123f5d3ede42567a4f3ff07c`

```dockerfile
```

-	Layers:
	-	`sha256:376266b8562d4b67a4842e90e7af202d817706e2b98312ed23e8858f1574a4b7`  
		Last Modified: Mon, 01 Jun 2026 22:46:55 GMT  
		Size: 2.6 MB (2572933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:637b0475b897646737dd25bdcc08e236d157c1d077296a73a5d249b260d9835c`  
		Last Modified: Mon, 01 Jun 2026 22:46:54 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

### `node:26-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:cef0ae4e4ae8c6b7153a0372640fad4adcf2597ffb8ab9f4fc77efdf6d588e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82853198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:566a1e5bfd0d6a41b3e254e43ff7f1da6d94e667bc7e21402a19bd5b166ad870`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Mon, 01 Jun 2026 22:46:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 01 Jun 2026 22:46:26 GMT
ENV NODE_VERSION=26.3.0
# Mon, 01 Jun 2026 22:46:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 01 Jun 2026 22:46:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jun 2026 22:46:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:46:26 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667930ccb993058f57b7c0f2f918a529c7f66334ad9d684247ec4da2ef9343f1`  
		Last Modified: Mon, 01 Jun 2026 22:46:42 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d7d9063dba360d0b0d200362aa274a087cc40b4f797010e427caaec621d05f`  
		Last Modified: Mon, 01 Jun 2026 22:46:43 GMT  
		Size: 54.7 MB (54734394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1ece234c1b6658ae7a1587ad7d6972789affdd19016fd500692e3cfaf4fba4`  
		Last Modified: Mon, 01 Jun 2026 22:46:42 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:26-bookworm-slim` - unknown; unknown

```console
$ docker pull node@sha256:a21090536134148512219a886759151d6591bc6c8054bb74b6a206b35f8f2966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2592043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150025ee3ceca37927d9ce870e2cbb7a55bf5b1fac3a12a176e956a2a4918546`

```dockerfile
```

-	Layers:
	-	`sha256:c5a9e81431f291981dddffdc2b40b116a4b2dc59224a36564dd8a06ecaa6da13`  
		Last Modified: Mon, 01 Jun 2026 22:46:42 GMT  
		Size: 2.6 MB (2573197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4070c3e649b56c3eedddc4e3647ad75a386bff2e164c2a41de651bd14f6bd532`  
		Last Modified: Mon, 01 Jun 2026 22:46:42 GMT  
		Size: 18.8 KB (18846 bytes)  
		MIME: application/vnd.in-toto+json

### `node:26-bookworm-slim` - linux; ppc64le

```console
$ docker pull node@sha256:1259c5e78f3624cfe933cfd8822ddb9ef47602871c3b4517461cc63c358454f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88923669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2220181304a21e198dd6e6094ccb60c496c7e75041f8c31d9f4686f53d0a9b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Mon, 01 Jun 2026 22:45:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 01 Jun 2026 22:46:29 GMT
ENV NODE_VERSION=26.3.0
# Mon, 01 Jun 2026 22:46:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 01 Jun 2026 22:46:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jun 2026 22:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:46:30 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf55bf2230c58bf375ee8df6efa30194776af9c6e06a5655b3277ed3c8ae6fc`  
		Last Modified: Mon, 01 Jun 2026 22:47:20 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2a9d999e2c56b2a40895c4acaf5d67b49b4e0b0d219473bdf71861a4b7b486`  
		Last Modified: Mon, 01 Jun 2026 22:47:22 GMT  
		Size: 56.8 MB (56844164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19487b5d14ca6891443bf1e97333ee35475b996a3d440c5af56201d922a1487d`  
		Last Modified: Mon, 01 Jun 2026 22:47:20 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:26-bookworm-slim` - unknown; unknown

```console
$ docker pull node@sha256:8b826693813fd382006eaa572ec84c2f770be0db91e8ced5a0ad1a11e34762a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42c3e32cfac82699f50d4de7140cf7d50e8f9595ff799406e0809a6734ad2ba`

```dockerfile
```

-	Layers:
	-	`sha256:0056abae1d1c8a36591a3ba61104f992af0f6264cd3005087c1f965a19a587e2`  
		Last Modified: Mon, 01 Jun 2026 22:47:21 GMT  
		Size: 2.6 MB (2577296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f72e1f2b5aaf32163b5ac13cdf9e49f1444dd4eec3406d2755aa24c6fb6a7f8d`  
		Last Modified: Mon, 01 Jun 2026 22:47:20 GMT  
		Size: 18.8 KB (18767 bytes)  
		MIME: application/vnd.in-toto+json

### `node:26-bookworm-slim` - linux; s390x

```console
$ docker pull node@sha256:1c72520dcf5ffc3e27effee316eb96f36c1693840724bf5ea7863ee5684bb31f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83438600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6e250033f6f5cc1cb9d826231de2e88b6411d66b75bd09c1e413e80b6760d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Mon, 01 Jun 2026 22:45:59 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 01 Jun 2026 22:46:19 GMT
ENV NODE_VERSION=26.3.0
# Mon, 01 Jun 2026 22:46:19 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 01 Jun 2026 22:46:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jun 2026 22:46:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:46:19 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f773959a94a433b9bc5d2b820dabec89a05df71e29cee42caf2ad2d94483e005`  
		Last Modified: Mon, 01 Jun 2026 22:46:47 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998c0997c62a6bf4887bf99f231491f95b2666acf406a0eaa55128dc174e6db8`  
		Last Modified: Mon, 01 Jun 2026 22:46:48 GMT  
		Size: 56.5 MB (56546248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a891fbc77d29188dc90086cf2a6544c6c9834ea6a9a3a9c8385e887258bb2bd9`  
		Last Modified: Mon, 01 Jun 2026 22:46:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:26-bookworm-slim` - unknown; unknown

```console
$ docker pull node@sha256:06208f26d686505f6a99dabaa0743b052246f6268bea1ea08aed1a0756271ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e722a93d424000bc3e76a78396ef6ecdcfd8af299cbdca41aca51c8221e076df`

```dockerfile
```

-	Layers:
	-	`sha256:b1e9fc2e26b83b5f1d58b6e32fa83b68bf8b2ab0a1bbb1de240b4a6edb9eb9f3`  
		Last Modified: Mon, 01 Jun 2026 22:46:47 GMT  
		Size: 2.6 MB (2569770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d5cfb167f3f18ed3dcefae6ca9fe83246505a02325a436717b2c2ecb241891`  
		Last Modified: Mon, 01 Jun 2026 22:46:47 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

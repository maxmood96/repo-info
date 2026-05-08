## `node:bookworm-slim`

```console
$ docker pull node@sha256:04e5bcc234b5edbc76b26ef710e629ac425c1f5b4563beac49b48369d0954bc9
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

### `node:bookworm-slim` - linux; amd64

```console
$ docker pull node@sha256:9fca02653872d8b07968a8e5c08f40ccb7964d291a63386748943aa5ad552bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82520250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51bb1c11fb5cdfb2c9bc90e0a72c5d4daf6a7f25dd51ffb7aef9bc95becab73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Thu, 07 May 2026 17:59:54 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 07 May 2026 18:00:15 GMT
ENV NODE_VERSION=26.1.0
# Thu, 07 May 2026 18:00:15 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 07 May 2026 18:00:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 18:00:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 May 2026 18:00:15 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7344dae8d68bc6c61c97d57a920da38cf8d3bcee0a3f8a6575b4a0cf3408468f`  
		Last Modified: Thu, 07 May 2026 18:00:31 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ed08ef6cac2b03c6261bf81e5350930e6934d9c875a6fa6fde2b2c758b2704`  
		Last Modified: Thu, 07 May 2026 18:00:32 GMT  
		Size: 54.3 MB (54280241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab5c3af079f1f4294099d631a5039ca7fc14cff6f9441eff0b69e2c12c1f79b`  
		Last Modified: Thu, 07 May 2026 18:00:30 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm-slim` - unknown; unknown

```console
$ docker pull node@sha256:d38c4db67be281490fc81a6f34ff9d8fee1058c219cc49a2a850e2cdbf817c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2591790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785756a4a9b38bd063f2bb8f94c58139966009e022417f8a1781af7b6d2b8af5`

```dockerfile
```

-	Layers:
	-	`sha256:c9b0629c622795ee5ccd38da569d550263341fff3f2514ff7a8d3425a97a1de1`  
		Last Modified: Thu, 07 May 2026 18:00:30 GMT  
		Size: 2.6 MB (2572913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4710f39b4a570c267e75cd1c7335a5136768eb5b77737ae171f7eb101c2756f0`  
		Last Modified: Thu, 07 May 2026 18:00:29 GMT  
		Size: 18.9 KB (18877 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:2c220896daa8f99b32348942c7fe486e1fe9d6ef2d494bbebb9e51a585612633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82639226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15de84b4b1399694d79fd7523d908f1e3fe6b81e7ac1f261a9f9c5699d9cd180`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:46:50 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 08 May 2026 19:47:10 GMT
ENV NODE_VERSION=26.1.0
# Fri, 08 May 2026 19:47:10 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 08 May 2026 19:47:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:47:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:47:10 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ec51bc60d0bdf09140d3ca06a7ce3b9ee6880f254b9b1ad8c47cba231d2353`  
		Last Modified: Fri, 08 May 2026 19:47:26 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a26aa231fd86b636084dd120863e496e261af97e4d69109b908084eb5028d2`  
		Last Modified: Fri, 08 May 2026 19:47:28 GMT  
		Size: 54.5 MB (54519302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477da7fe5eba6d3a460fd3f3a008a80fc8bd180d37178a2c9cb6f11f9d9475ae`  
		Last Modified: Fri, 08 May 2026 19:47:26 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm-slim` - unknown; unknown

```console
$ docker pull node@sha256:c2f43acc12d8a2534e1668c712f34b12e7ac1b4d73720e66bc70cb50633a457c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2592184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804e25375caf6d1b68bb52726b680407eda36a54bae86a9a083bc85506988061`

```dockerfile
```

-	Layers:
	-	`sha256:386a5b3b48b62702cf6a9fc28bee4d07b514ad501f060672c5560eec522d32a6`  
		Last Modified: Fri, 08 May 2026 19:47:26 GMT  
		Size: 2.6 MB (2573177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b28e28b102b03fbe7e28d37779f27e021d57ff084d971b1ac5c28103edf0e06a`  
		Last Modified: Fri, 08 May 2026 19:47:26 GMT  
		Size: 19.0 KB (19007 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm-slim` - linux; ppc64le

```console
$ docker pull node@sha256:8c64dc7cd70385969ec06788266a140b712c61e6ef0f53ca2b72bfb1c6fdf724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88433326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ad7eb2a2feeb80ad1bb93775cd22011fd950c4da958fae6d9bbd9453b89874`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 06 May 2026 17:19:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 07 May 2026 21:24:48 GMT
ENV NODE_VERSION=26.1.0
# Thu, 07 May 2026 21:24:48 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 07 May 2026 21:24:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 21:24:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 May 2026 21:24:48 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded56d76a6cc13f72e61d2028c9b30481bfa9be62a30d8327d75eb7d5f97290a`  
		Last Modified: Wed, 06 May 2026 17:31:13 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8688f3cd32f95ee2b4a15debe6878a10999b562a1fdbc361f923cc46b5ebc281`  
		Last Modified: Thu, 07 May 2026 21:25:26 GMT  
		Size: 56.4 MB (56351142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b3c60f8d40d16c705e555b5ce9d492b5ca293823d643752014c9fba9c3a6c1`  
		Last Modified: Thu, 07 May 2026 21:25:24 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm-slim` - unknown; unknown

```console
$ docker pull node@sha256:8347388d6a0c1556540285748c1493fe686f915db8fb865bdd5cb6138f815a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a012148386f16bc1d724e0e6ff68b2d0a5548be09c5b3c8da3844f3baeb49545`

```dockerfile
```

-	Layers:
	-	`sha256:7c47ae7ac669bdbc7ff39f09c3e71bb0ad1ce5d224b40548286a00fb8478c7cd`  
		Last Modified: Thu, 07 May 2026 21:25:24 GMT  
		Size: 2.6 MB (2577276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc25c187e2e117321511a2c3c4c5369c6b2f9bc35f06ce4321add6ed14e024b8`  
		Last Modified: Thu, 07 May 2026 21:25:34 GMT  
		Size: 18.9 KB (18929 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm-slim` - linux; s390x

```console
$ docker pull node@sha256:a33456f1d39b5e60066e224da390171ee7a512af364481801bcb46393bd98c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87622242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34120b453ee4116795eac6a6b80fadf53f05f2c9618db8055a241450ebe32bbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 06 May 2026 18:11:21 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 07 May 2026 19:47:38 GMT
ENV NODE_VERSION=26.1.0
# Thu, 07 May 2026 19:47:38 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 07 May 2026 19:47:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 19:47:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 May 2026 19:47:38 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c5030ca628d400ad59d758dd40668151446a1b70fc283b44afa133e64bc637`  
		Last Modified: Wed, 06 May 2026 18:18:20 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52480e30b217fe8e38b9d8e983dd67304fdbff5d6fdb1a3010cd00032ea5ce8`  
		Last Modified: Thu, 07 May 2026 19:48:10 GMT  
		Size: 60.7 MB (60726908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446c86f48eef77014d2fd51a4e6c99bf77a3a603e62aa572b64408b59b681d74`  
		Last Modified: Thu, 07 May 2026 19:48:08 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm-slim` - unknown; unknown

```console
$ docker pull node@sha256:0eb3a73c5cb4ffc13304b9d9cf65145036204b7297894191776a1c98aed51358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8fcf5a0aea99618c1c3d00f850ae89da612befa715ab13ffe8636b1c60484e`

```dockerfile
```

-	Layers:
	-	`sha256:687e4ecdd06c0736fb3bf35f3531fd1a81ab43b28eda92b4efda7e9452d3a95a`  
		Last Modified: Thu, 07 May 2026 19:48:09 GMT  
		Size: 2.6 MB (2569750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f3c9ebe860c49a31233ebee75b3e53ce6f053413583d364ecd13f2c7bfd1e0a`  
		Last Modified: Thu, 07 May 2026 19:48:08 GMT  
		Size: 18.9 KB (18877 bytes)  
		MIME: application/vnd.in-toto+json

## `node:slim`

```console
$ docker pull node@sha256:118496f497b25d759dca01ea9b4470ef8dd2f4e89e33898022be35408834453d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `node:slim` - linux; amd64

```console
$ docker pull node@sha256:e8f4e2b76ae4e476ba4836dd858bae3034b39663eec50a8849d85d2c0fd67915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79811583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d64c97814804e07c8b217d1f237ecde57b734fa4fda69fd6e0fdba90125fcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 25 Oct 2024 06:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
CMD ["bash"]
# Fri, 25 Oct 2024 06:01:46 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
ENV NODE_VERSION=23.1.0
# Fri, 25 Oct 2024 06:01:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
ENV YARN_VERSION=1.22.22
# Fri, 25 Oct 2024 06:01:46 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Oct 2024 06:01:46 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212f687a7072357fe57d48a551de48e802744be9e127601f64b4fe921af9aa1`  
		Last Modified: Tue, 12 Nov 2024 02:39:59 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a45e26a14122d9af65dc51112be9434546df483f134b96f91cdf5d835c79f46`  
		Last Modified: Tue, 12 Nov 2024 02:39:59 GMT  
		Size: 49.0 MB (48967425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593492f7391289e3272cd1f2d0f40e34a37d6e6e33eed99aee1cc37845c861ab`  
		Last Modified: Tue, 12 Nov 2024 02:39:59 GMT  
		Size: 1.7 MB (1712403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c5cddd0333327a11847e8a4b3c04293ddfe22e3d37b667a832581edad7ab93`  
		Last Modified: Tue, 12 Nov 2024 02:39:59 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:slim` - unknown; unknown

```console
$ docker pull node@sha256:7eb27d3fd60328fd862a591d07ff05ac9cf48ef4c7ec2bac70f1e3ef3fd9f256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739a615a1d29d46395f7a8deef05076b22847069be9ed3fcd381e837edc21125`

```dockerfile
```

-	Layers:
	-	`sha256:139b25676cf0b1769969f3392287a3f5e0852ab5a37cd58fae656e770f6507c2`  
		Last Modified: Tue, 12 Nov 2024 02:39:59 GMT  
		Size: 2.6 MB (2588539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5684de58aa3a5f0c550ea353bf21448b7303d48c3f2b36705c5e229bf6b331`  
		Last Modified: Tue, 12 Nov 2024 02:39:59 GMT  
		Size: 27.0 KB (27036 bytes)  
		MIME: application/vnd.in-toto+json

### `node:slim` - linux; arm variant v7

```console
$ docker pull node@sha256:a2eaf0139f15992a1200629a21ce3fd2563f817175a2aea6562ed1c7d3ff05eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70359671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e7d17ade9301dd3f23a6127a569a88d31d9a12bbda3cdb2415075562dc354d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 25 Oct 2024 06:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
CMD ["bash"]
# Fri, 25 Oct 2024 06:01:46 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
ENV NODE_VERSION=23.1.0
# Fri, 25 Oct 2024 06:01:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
ENV YARN_VERSION=1.22.22
# Fri, 25 Oct 2024 06:01:46 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Oct 2024 06:01:46 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12e8f4279bfa57e91b124afb54540f003f2bca339945f6a92e0fe2521df05e`  
		Last Modified: Tue, 12 Nov 2024 19:56:38 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d29558ba0bba6cf85ac46744a2274f2bb95129d5a9782099660d83905c49947`  
		Last Modified: Tue, 12 Nov 2024 19:56:39 GMT  
		Size: 43.9 MB (43924339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbf7b1423e6768b4f1760168e2de379e94e59d38e58d608b42593726d4e78df`  
		Last Modified: Tue, 12 Nov 2024 19:56:38 GMT  
		Size: 1.7 MB (1712661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f035ab30aa9a20132acd956e76eeba4a2531b4fff8186294bee6bd8fe5f9d1c`  
		Last Modified: Tue, 12 Nov 2024 19:56:38 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:slim` - unknown; unknown

```console
$ docker pull node@sha256:678342e762e80739a4ec9b831eecdc91f5493b442a25d114d5e868cad82cd0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2621242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda0c19865ffbdb3759a360ad874e953c39c4aa54e31437d459f4d81e09efd64`

```dockerfile
```

-	Layers:
	-	`sha256:055dcb9a4b9f7a2142d9ae73859d0e09b800f4efa9ea4690a202d178c4d25476`  
		Last Modified: Tue, 12 Nov 2024 19:56:38 GMT  
		Size: 2.6 MB (2594056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:961eaac0ef72f6c8a0f2f426817033d15654b460f9cefd06b327afc7f0e434c3`  
		Last Modified: Tue, 12 Nov 2024 19:56:38 GMT  
		Size: 27.2 KB (27186 bytes)  
		MIME: application/vnd.in-toto+json

### `node:slim` - linux; arm64 variant v8

```console
$ docker pull node@sha256:148f0a6e7fd8560a485987bb4b37e20cde76ad2cd48d64fbdfc49d55f212c7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79582810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b62640d162f6722096cd4d99d38e82497e1d7e3c173b226d86bba7a38f5efc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 25 Oct 2024 06:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
CMD ["bash"]
# Fri, 25 Oct 2024 06:01:46 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
ENV NODE_VERSION=23.1.0
# Fri, 25 Oct 2024 06:01:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
ENV YARN_VERSION=1.22.22
# Fri, 25 Oct 2024 06:01:46 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Oct 2024 06:01:46 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a18e35815a230920e7c08533e3c3c02ac27fa4add044f140e32a114df942e2`  
		Last Modified: Tue, 12 Nov 2024 15:27:41 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25f51c95c0e75d3cba2fa0d8102a640627b3f61444c84ada1314d73d3aebf93`  
		Last Modified: Tue, 12 Nov 2024 15:27:42 GMT  
		Size: 48.7 MB (48709275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a285dcd9e7daf152a0f2a5f364a97c358de7f77f6a4f0a952171ab95ba432b7`  
		Last Modified: Tue, 12 Nov 2024 15:27:41 GMT  
		Size: 1.7 MB (1712418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e589f4e614ede8d9a6e3fc96e7c380a96ff536551ba91a84d3407a2b00279dd`  
		Last Modified: Tue, 12 Nov 2024 15:27:41 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:slim` - unknown; unknown

```console
$ docker pull node@sha256:478a77b9b50fb13f0d945ac06f383a5caf1ed4852dae08aaba935a3a9a247217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94b9af38f7779c318f806b3c66dcc2a1434895fd204c6c3f97fb9ae64b6d49f`

```dockerfile
```

-	Layers:
	-	`sha256:5354f6a0937689c9dc9ed280df6767389b0aff26a23291af241f178c59c8cc11`  
		Last Modified: Tue, 12 Nov 2024 15:27:41 GMT  
		Size: 2.6 MB (2588861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc2246fe3ae870a7b0d2ad0f23f8038b4d6c5a52d4230d47377076faa7f95b62`  
		Last Modified: Tue, 12 Nov 2024 15:27:41 GMT  
		Size: 27.2 KB (27242 bytes)  
		MIME: application/vnd.in-toto+json

### `node:slim` - linux; ppc64le

```console
$ docker pull node@sha256:e1134b4d3a81ee0caef58b4375dbec0fb73a06fba215563cdc266fd56fd93647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86515478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dcd0fffa21dcb639cc61533b5c1f6903505d0ad644ac2038841ac0f23a43a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Fri, 15 Nov 2024 23:05:55 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 15 Nov 2024 23:05:55 GMT
ENV NODE_VERSION=23.2.0
# Fri, 15 Nov 2024 23:05:55 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 15 Nov 2024 23:05:55 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 23:05:55 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 23:05:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 23:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 23:05:55 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b818420b8b420d93637d67bd46b71029bfb1e062b744b14c8f79e7a7cb6589`  
		Last Modified: Tue, 12 Nov 2024 09:03:45 GMT  
		Size: 3.3 KB (3317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739a9a4de5dd513e5359078424b9253a6a9bbb64a8d16d0a57ded45cf38bf23`  
		Last Modified: Mon, 18 Nov 2024 15:08:01 GMT  
		Size: 51.7 MB (51673742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c641a4befc71689649715312bbad272209c6fef437247281534ae1fe889c3950`  
		Last Modified: Mon, 18 Nov 2024 15:07:59 GMT  
		Size: 1.7 MB (1712617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb62ccb612f56e565a3c0a623e33066b9e9f88e18dc706a1ba1e49b20b341808`  
		Last Modified: Mon, 18 Nov 2024 15:07:58 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:slim` - unknown; unknown

```console
$ docker pull node@sha256:611ef1bf1897e295633980c03f96040c3a99b5a5bd00803d97de8fa7d567d58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2619952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3a9289fedf39b395b36557ea8132e79ccc0e90488b0ca3c380a77aa5580ed9`

```dockerfile
```

-	Layers:
	-	`sha256:c704316e037f11850cfd1097d3e8f8e2b3e3eb551c4ef8320e9f17c17a9503fd`  
		Last Modified: Mon, 18 Nov 2024 15:07:59 GMT  
		Size: 2.6 MB (2592832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:055ae497deec8f564c8f7b138b21ee19dd19c462629f065f5de2f0f09d184479`  
		Last Modified: Mon, 18 Nov 2024 15:07:58 GMT  
		Size: 27.1 KB (27120 bytes)  
		MIME: application/vnd.in-toto+json

### `node:slim` - linux; s390x

```console
$ docker pull node@sha256:3114067cd38ad85e1c50663e8cece34e6b774bd06dada7884485cd1993210a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77972958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a489713d59ba2465b69e3fec2566f9250b4982777702a07b8d72650005684e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 25 Oct 2024 06:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
CMD ["bash"]
# Fri, 25 Oct 2024 06:01:46 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
ENV NODE_VERSION=23.1.0
# Fri, 25 Oct 2024 06:01:46 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
ENV YARN_VERSION=1.22.22
# Fri, 25 Oct 2024 06:01:46 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Oct 2024 06:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Oct 2024 06:01:46 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5936a9967200e38b9edc3158d32d0bd35fcdadb6ce24041a0fd1a4c31f82bac`  
		Last Modified: Tue, 12 Nov 2024 12:15:56 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccd2dbf8806066cd194a5abb16653b0af1d26386093ba78b042a2d3e3480066`  
		Last Modified: Tue, 12 Nov 2024 12:15:57 GMT  
		Size: 48.8 MB (48765076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea914dbe5438c7c6941e60a20d5d86904dcc0a19c932647042d2e0e32ee1a8`  
		Last Modified: Tue, 12 Nov 2024 12:15:57 GMT  
		Size: 1.7 MB (1712495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db8ffe4fbb0b7d7a2bc358ce4625a71374a87dd04d1d7524c99155db8b398a0`  
		Last Modified: Tue, 12 Nov 2024 12:15:57 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:slim` - unknown; unknown

```console
$ docker pull node@sha256:627c52fbfe03513b3a9f8c58cb49fe3ec0341ffa3385152819a421be1d091c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ec9ce5062e4b3c974040099c80f7ca9dd56434b3bf44d6abc2011002a97973`

```dockerfile
```

-	Layers:
	-	`sha256:5624df85a9e7340aa581f9aa6cbde797d3644771336c1c40c33f48dbc15974b4`  
		Last Modified: Tue, 12 Nov 2024 12:15:57 GMT  
		Size: 2.6 MB (2588270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bb63bb627cc8a5f0cbd2834e77ff6f06f9996bd35d65fc04247ce6be86a6189`  
		Last Modified: Tue, 12 Nov 2024 12:15:56 GMT  
		Size: 27.0 KB (27036 bytes)  
		MIME: application/vnd.in-toto+json

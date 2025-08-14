<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rocket.chat`

-	[`rocket.chat:7`](#rocketchat7)
-	[`rocket.chat:7.4`](#rocketchat74)
-	[`rocket.chat:7.4.5`](#rocketchat745)
-	[`rocket.chat:7.5`](#rocketchat75)
-	[`rocket.chat:7.5.4`](#rocketchat754)
-	[`rocket.chat:7.6`](#rocketchat76)
-	[`rocket.chat:7.6.5`](#rocketchat765)
-	[`rocket.chat:7.7`](#rocketchat77)
-	[`rocket.chat:7.7.8`](#rocketchat778)
-	[`rocket.chat:7.8`](#rocketchat78)
-	[`rocket.chat:7.8.4`](#rocketchat784)
-	[`rocket.chat:7.9`](#rocketchat79)
-	[`rocket.chat:7.9.3`](#rocketchat793)
-	[`rocket.chat:latest`](#rocketchatlatest)

## `rocket.chat:7`

```console
$ docker pull rocket.chat@sha256:4210ac55198da06aa5d271be1e8187d1f870cdd2f7a90dbadcc9cf2c18e6397b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:88c1cc18ede781afa0d05f2afb6310d245d4ee0f4fd058b27119004830036969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.4 MB (494448639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438df727799a05ee82b5f148c458407fc1d67b29321977e613b73168ca8bc2a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 01 Aug 2025 10:06:16 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 01 Aug 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV NODE_VERSION=22.18.0
# Fri, 01 Aug 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Fri, 01 Aug 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Aug 2025 10:06:16 GMT
CMD ["node"]
# Tue, 12 Aug 2025 22:03:11 GMT
ENV DENO_VERSION=1.43.5
# Tue, 12 Aug 2025 22:03:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 12 Aug 2025 22:03:11 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Tue, 12 Aug 2025 22:03:11 GMT
VOLUME [/app/uploads]
# Tue, 12 Aug 2025 22:03:11 GMT
WORKDIR /app
# Tue, 12 Aug 2025 22:03:11 GMT
ENV NODE_ENV=production
# Tue, 12 Aug 2025 22:03:11 GMT
ENV RC_VERSION=7.9.3
# Tue, 12 Aug 2025 22:03:11 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Tue, 12 Aug 2025 22:03:11 GMT
USER rocketchat
# Tue, 12 Aug 2025 22:03:11 GMT
WORKDIR /app/bundle
# Tue, 12 Aug 2025 22:03:11 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Tue, 12 Aug 2025 22:03:11 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 12 Aug 2025 22:03:11 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0731002e5f78a5a17484bce03c29cb6e053875de4a31ff3244b6e5e7880e68`  
		Last Modified: Tue, 12 Aug 2025 21:26:46 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27ae6f53ba4439325ee069de45f39b873e39a177c8116f2e317adfc666f0a4e`  
		Last Modified: Tue, 12 Aug 2025 21:26:56 GMT  
		Size: 49.0 MB (48967524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb4f79935d9398dc2bf52eb9dd2d2898be4ae2f19428dcfd200ee4b0c59387`  
		Last Modified: Tue, 12 Aug 2025 21:26:48 GMT  
		Size: 1.7 MB (1712539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d741e5a2c15f09f73507900c996aa5bacf9d2ea2811bc5222075fefa6217431`  
		Last Modified: Tue, 12 Aug 2025 21:26:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bacb3a7e614d9e648c1efee9fb7c317d25dfa7c5967d5d8aa8e9c6209b4449b`  
		Last Modified: Tue, 12 Aug 2025 23:41:04 GMT  
		Size: 48.7 MB (48723619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3992bf184b1f8dd4d65abeb153a9bb869e468e1617581930d155e2c5b0ef347`  
		Last Modified: Tue, 12 Aug 2025 23:41:00 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6baaba14b8edf9a68cd800d883cfa965179903886aaa91c36860d293cfc90eb`  
		Last Modified: Wed, 13 Aug 2025 01:43:34 GMT  
		Size: 366.8 MB (366809703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:c2660495bed46462e20e29a8611225caf3a94c158a67aa57453f9d79239e4b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becc7672735b348cd32e0383ebaa65dba006964e4a93d093e29f9e899c56de24`

```dockerfile
```

-	Layers:
	-	`sha256:132f3bc6df9de16ef56c3961503a35d7248178257d87f29947db03fa83755084`  
		Last Modified: Wed, 13 Aug 2025 01:42:20 GMT  
		Size: 23.7 KB (23708 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.4`

```console
$ docker pull rocket.chat@sha256:553fa6f062a8ce860f64d710dee8c73c05bc8d1ff1e910e3198a45880f51df5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.4` - linux; amd64

```console
$ docker pull rocket.chat@sha256:2a9f89df9a9d25aa5e84e8b3bfeee261c3dffe9aab7f52de3cbbb1d075888b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.7 MB (511692418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f521f59082c7415769959712301645b10f948b3aee7fc1e7546e0b2aedaee6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 01 Aug 2025 10:06:16 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 01 Aug 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV NODE_VERSION=22.18.0
# Fri, 01 Aug 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Fri, 01 Aug 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Aug 2025 10:06:16 GMT
CMD ["node"]
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DENO_VERSION=1.43.5
# Wed, 06 Aug 2025 13:26:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
VOLUME [/app/uploads]
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app
# Wed, 06 Aug 2025 13:26:41 GMT
ENV NODE_ENV=production
# Wed, 06 Aug 2025 13:26:41 GMT
ENV RC_VERSION=7.4.5
# Wed, 06 Aug 2025 13:26:41 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
USER rocketchat
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app/bundle
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Wed, 06 Aug 2025 13:26:41 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 06 Aug 2025 13:26:41 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0731002e5f78a5a17484bce03c29cb6e053875de4a31ff3244b6e5e7880e68`  
		Last Modified: Tue, 12 Aug 2025 21:26:46 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27ae6f53ba4439325ee069de45f39b873e39a177c8116f2e317adfc666f0a4e`  
		Last Modified: Tue, 12 Aug 2025 21:26:56 GMT  
		Size: 49.0 MB (48967524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb4f79935d9398dc2bf52eb9dd2d2898be4ae2f19428dcfd200ee4b0c59387`  
		Last Modified: Tue, 12 Aug 2025 21:26:48 GMT  
		Size: 1.7 MB (1712539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d741e5a2c15f09f73507900c996aa5bacf9d2ea2811bc5222075fefa6217431`  
		Last Modified: Tue, 12 Aug 2025 21:26:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a73f28aa68610e1eebb5830d1176d87babd6f6bbe3a959b8f13a360bbcf3d00`  
		Last Modified: Tue, 12 Aug 2025 22:22:14 GMT  
		Size: 48.7 MB (48723627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879ead1c481f853ce917f1ab127207966d757483b3b47d901145d79b2b8e334c`  
		Last Modified: Tue, 12 Aug 2025 22:22:09 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7473fc1ece852b96a63583a818b2fa26035afdbbd0d1755fb4ed0853279a10`  
		Last Modified: Wed, 13 Aug 2025 01:44:28 GMT  
		Size: 384.1 MB (384053476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.4` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:1de82e39ae1c1ae2ccebecce085c92d3e1c390bdf0467f5fd8b5d448a280c2e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba976aaae7bafff72a4e7259b15daf7ad6fc69815f222eec32c26a18d4632027`

```dockerfile
```

-	Layers:
	-	`sha256:f42e996ce48b4c4bf58b4c2f1505851be164ee6623d2459fc180051bbfc02521`  
		Last Modified: Wed, 13 Aug 2025 01:42:21 GMT  
		Size: 23.1 KB (23103 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.4.5`

```console
$ docker pull rocket.chat@sha256:553fa6f062a8ce860f64d710dee8c73c05bc8d1ff1e910e3198a45880f51df5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.4.5` - linux; amd64

```console
$ docker pull rocket.chat@sha256:2a9f89df9a9d25aa5e84e8b3bfeee261c3dffe9aab7f52de3cbbb1d075888b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.7 MB (511692418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f521f59082c7415769959712301645b10f948b3aee7fc1e7546e0b2aedaee6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 01 Aug 2025 10:06:16 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 01 Aug 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV NODE_VERSION=22.18.0
# Fri, 01 Aug 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Fri, 01 Aug 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Aug 2025 10:06:16 GMT
CMD ["node"]
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DENO_VERSION=1.43.5
# Wed, 06 Aug 2025 13:26:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
VOLUME [/app/uploads]
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app
# Wed, 06 Aug 2025 13:26:41 GMT
ENV NODE_ENV=production
# Wed, 06 Aug 2025 13:26:41 GMT
ENV RC_VERSION=7.4.5
# Wed, 06 Aug 2025 13:26:41 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
USER rocketchat
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app/bundle
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Wed, 06 Aug 2025 13:26:41 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 06 Aug 2025 13:26:41 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0731002e5f78a5a17484bce03c29cb6e053875de4a31ff3244b6e5e7880e68`  
		Last Modified: Tue, 12 Aug 2025 21:26:46 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27ae6f53ba4439325ee069de45f39b873e39a177c8116f2e317adfc666f0a4e`  
		Last Modified: Tue, 12 Aug 2025 21:26:56 GMT  
		Size: 49.0 MB (48967524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb4f79935d9398dc2bf52eb9dd2d2898be4ae2f19428dcfd200ee4b0c59387`  
		Last Modified: Tue, 12 Aug 2025 21:26:48 GMT  
		Size: 1.7 MB (1712539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d741e5a2c15f09f73507900c996aa5bacf9d2ea2811bc5222075fefa6217431`  
		Last Modified: Tue, 12 Aug 2025 21:26:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a73f28aa68610e1eebb5830d1176d87babd6f6bbe3a959b8f13a360bbcf3d00`  
		Last Modified: Tue, 12 Aug 2025 22:22:14 GMT  
		Size: 48.7 MB (48723627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879ead1c481f853ce917f1ab127207966d757483b3b47d901145d79b2b8e334c`  
		Last Modified: Tue, 12 Aug 2025 22:22:09 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7473fc1ece852b96a63583a818b2fa26035afdbbd0d1755fb4ed0853279a10`  
		Last Modified: Wed, 13 Aug 2025 01:44:28 GMT  
		Size: 384.1 MB (384053476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.4.5` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:1de82e39ae1c1ae2ccebecce085c92d3e1c390bdf0467f5fd8b5d448a280c2e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba976aaae7bafff72a4e7259b15daf7ad6fc69815f222eec32c26a18d4632027`

```dockerfile
```

-	Layers:
	-	`sha256:f42e996ce48b4c4bf58b4c2f1505851be164ee6623d2459fc180051bbfc02521`  
		Last Modified: Wed, 13 Aug 2025 01:42:21 GMT  
		Size: 23.1 KB (23103 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.5`

```console
$ docker pull rocket.chat@sha256:4cd1442ca3f7b4071ca34acb54db877987154a9451794e7e5b9876d8d297d13c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.5` - linux; amd64

```console
$ docker pull rocket.chat@sha256:a2b3ac84e1d30fbfb58cf371c21b4d834e384f3a8dfb69c5fe3258a5d07e37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.8 MB (515847811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c6c6d3ade4fa9d65a6fb710b2bdcc69a015f537e4e097fa97ca1e90aed3b67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 01 Aug 2025 10:06:16 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 01 Aug 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV NODE_VERSION=22.18.0
# Fri, 01 Aug 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Fri, 01 Aug 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Aug 2025 10:06:16 GMT
CMD ["node"]
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DENO_VERSION=1.43.5
# Wed, 06 Aug 2025 13:26:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
VOLUME [/app/uploads]
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app
# Wed, 06 Aug 2025 13:26:41 GMT
ENV NODE_ENV=production
# Wed, 06 Aug 2025 13:26:41 GMT
ENV RC_VERSION=7.5.4
# Wed, 06 Aug 2025 13:26:41 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
USER rocketchat
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app/bundle
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Wed, 06 Aug 2025 13:26:41 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 06 Aug 2025 13:26:41 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0731002e5f78a5a17484bce03c29cb6e053875de4a31ff3244b6e5e7880e68`  
		Last Modified: Tue, 12 Aug 2025 21:26:46 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27ae6f53ba4439325ee069de45f39b873e39a177c8116f2e317adfc666f0a4e`  
		Last Modified: Tue, 12 Aug 2025 21:26:56 GMT  
		Size: 49.0 MB (48967524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb4f79935d9398dc2bf52eb9dd2d2898be4ae2f19428dcfd200ee4b0c59387`  
		Last Modified: Tue, 12 Aug 2025 21:26:48 GMT  
		Size: 1.7 MB (1712539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d741e5a2c15f09f73507900c996aa5bacf9d2ea2811bc5222075fefa6217431`  
		Last Modified: Tue, 12 Aug 2025 21:26:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c84be7ed8c51ee1af5bcf0f192bed5762e3969cb1d90a70fefd3032f6f48aa`  
		Last Modified: Tue, 12 Aug 2025 22:24:43 GMT  
		Size: 48.7 MB (48723632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2423339af7fa644550253e9d2ba6f8af88092f492ba86c1df335c3ab7e8e66`  
		Last Modified: Tue, 12 Aug 2025 22:24:38 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8161ddf1ccc61145742e5dbeee6dbad3f658fea0b601d445183c71dc4bb501`  
		Last Modified: Wed, 13 Aug 2025 01:44:35 GMT  
		Size: 388.2 MB (388208868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.5` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:2800ac79743bc86143d2553af336c44899a7f318ed67bb8133f11830619915e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec68d2fb10644fa94755ba14acc77f3223e6682cb93d52f051b1dcf55fed91d`

```dockerfile
```

-	Layers:
	-	`sha256:dc2bf7e51ab4cb3e8d5da8d1bb575470f3aa3c66217ecee4c77dbfaa8d2dcbc0`  
		Last Modified: Wed, 13 Aug 2025 01:42:28 GMT  
		Size: 23.1 KB (23103 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.5.4`

```console
$ docker pull rocket.chat@sha256:4cd1442ca3f7b4071ca34acb54db877987154a9451794e7e5b9876d8d297d13c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.5.4` - linux; amd64

```console
$ docker pull rocket.chat@sha256:a2b3ac84e1d30fbfb58cf371c21b4d834e384f3a8dfb69c5fe3258a5d07e37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.8 MB (515847811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c6c6d3ade4fa9d65a6fb710b2bdcc69a015f537e4e097fa97ca1e90aed3b67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 01 Aug 2025 10:06:16 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 01 Aug 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV NODE_VERSION=22.18.0
# Fri, 01 Aug 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Fri, 01 Aug 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Aug 2025 10:06:16 GMT
CMD ["node"]
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DENO_VERSION=1.43.5
# Wed, 06 Aug 2025 13:26:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
VOLUME [/app/uploads]
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app
# Wed, 06 Aug 2025 13:26:41 GMT
ENV NODE_ENV=production
# Wed, 06 Aug 2025 13:26:41 GMT
ENV RC_VERSION=7.5.4
# Wed, 06 Aug 2025 13:26:41 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
USER rocketchat
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app/bundle
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Wed, 06 Aug 2025 13:26:41 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 06 Aug 2025 13:26:41 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0731002e5f78a5a17484bce03c29cb6e053875de4a31ff3244b6e5e7880e68`  
		Last Modified: Tue, 12 Aug 2025 21:26:46 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27ae6f53ba4439325ee069de45f39b873e39a177c8116f2e317adfc666f0a4e`  
		Last Modified: Tue, 12 Aug 2025 21:26:56 GMT  
		Size: 49.0 MB (48967524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb4f79935d9398dc2bf52eb9dd2d2898be4ae2f19428dcfd200ee4b0c59387`  
		Last Modified: Tue, 12 Aug 2025 21:26:48 GMT  
		Size: 1.7 MB (1712539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d741e5a2c15f09f73507900c996aa5bacf9d2ea2811bc5222075fefa6217431`  
		Last Modified: Tue, 12 Aug 2025 21:26:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c84be7ed8c51ee1af5bcf0f192bed5762e3969cb1d90a70fefd3032f6f48aa`  
		Last Modified: Tue, 12 Aug 2025 22:24:43 GMT  
		Size: 48.7 MB (48723632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2423339af7fa644550253e9d2ba6f8af88092f492ba86c1df335c3ab7e8e66`  
		Last Modified: Tue, 12 Aug 2025 22:24:38 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8161ddf1ccc61145742e5dbeee6dbad3f658fea0b601d445183c71dc4bb501`  
		Last Modified: Wed, 13 Aug 2025 01:44:35 GMT  
		Size: 388.2 MB (388208868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.5.4` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:2800ac79743bc86143d2553af336c44899a7f318ed67bb8133f11830619915e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec68d2fb10644fa94755ba14acc77f3223e6682cb93d52f051b1dcf55fed91d`

```dockerfile
```

-	Layers:
	-	`sha256:dc2bf7e51ab4cb3e8d5da8d1bb575470f3aa3c66217ecee4c77dbfaa8d2dcbc0`  
		Last Modified: Wed, 13 Aug 2025 01:42:28 GMT  
		Size: 23.1 KB (23103 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.6`

```console
$ docker pull rocket.chat@sha256:68569fd6f5f39c925fcd171ae70071bf3a6b135786e5f884f098df16fc03b0d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.6` - linux; amd64

```console
$ docker pull rocket.chat@sha256:793bd87cc19c45d8234e9ab9c15724e48fc65081167d65e4e882c0493ca46464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.0 MB (516985981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2cdc0e30df8153901ad29e1a1846bbe20eadb440426b6fa2dd97c0ea428667`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 01 Aug 2025 10:06:16 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 01 Aug 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV NODE_VERSION=22.18.0
# Fri, 01 Aug 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Fri, 01 Aug 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Aug 2025 10:06:16 GMT
CMD ["node"]
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DENO_VERSION=1.43.5
# Wed, 06 Aug 2025 13:26:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
VOLUME [/app/uploads]
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app
# Wed, 06 Aug 2025 13:26:41 GMT
ENV NODE_ENV=production
# Wed, 06 Aug 2025 13:26:41 GMT
ENV RC_VERSION=7.6.5
# Wed, 06 Aug 2025 13:26:41 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
USER rocketchat
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app/bundle
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Wed, 06 Aug 2025 13:26:41 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 06 Aug 2025 13:26:41 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0731002e5f78a5a17484bce03c29cb6e053875de4a31ff3244b6e5e7880e68`  
		Last Modified: Tue, 12 Aug 2025 21:26:46 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27ae6f53ba4439325ee069de45f39b873e39a177c8116f2e317adfc666f0a4e`  
		Last Modified: Tue, 12 Aug 2025 21:26:56 GMT  
		Size: 49.0 MB (48967524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb4f79935d9398dc2bf52eb9dd2d2898be4ae2f19428dcfd200ee4b0c59387`  
		Last Modified: Tue, 12 Aug 2025 21:26:48 GMT  
		Size: 1.7 MB (1712539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d741e5a2c15f09f73507900c996aa5bacf9d2ea2811bc5222075fefa6217431`  
		Last Modified: Tue, 12 Aug 2025 21:26:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ba3d6af52921afcd67b93cbd837e337bb5f458b9545044ca8e1ddb666fe1cd`  
		Last Modified: Tue, 12 Aug 2025 22:51:03 GMT  
		Size: 48.7 MB (48723623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e961aa30a94bf44d8e89517e4b5af2eb196344ee7f8ac84a0cc42b18b2f07faf`  
		Last Modified: Tue, 12 Aug 2025 22:50:55 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ffb7f8f63757e1fc16fe76ca02b803beb85c0e1c6e6520b7cb4ceb13909e78`  
		Last Modified: Wed, 13 Aug 2025 01:47:49 GMT  
		Size: 389.3 MB (389347043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.6` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:edbad7dbfae7a35819ba3110f32afe7a26d4e00fe7ae8af7017b69334f1d9cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb315fb27e851a4280e8a80efe48984afb81dbda6c94438caca91e55ec8238a`

```dockerfile
```

-	Layers:
	-	`sha256:4fa72f905b689130d9c6e2188363ccaab3a0af74d0e87ea16d9c685c94c9eab2`  
		Last Modified: Wed, 13 Aug 2025 01:42:35 GMT  
		Size: 23.1 KB (23103 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.6.5`

```console
$ docker pull rocket.chat@sha256:68569fd6f5f39c925fcd171ae70071bf3a6b135786e5f884f098df16fc03b0d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.6.5` - linux; amd64

```console
$ docker pull rocket.chat@sha256:793bd87cc19c45d8234e9ab9c15724e48fc65081167d65e4e882c0493ca46464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.0 MB (516985981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2cdc0e30df8153901ad29e1a1846bbe20eadb440426b6fa2dd97c0ea428667`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 01 Aug 2025 10:06:16 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 01 Aug 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV NODE_VERSION=22.18.0
# Fri, 01 Aug 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Fri, 01 Aug 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Aug 2025 10:06:16 GMT
CMD ["node"]
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DENO_VERSION=1.43.5
# Wed, 06 Aug 2025 13:26:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
VOLUME [/app/uploads]
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app
# Wed, 06 Aug 2025 13:26:41 GMT
ENV NODE_ENV=production
# Wed, 06 Aug 2025 13:26:41 GMT
ENV RC_VERSION=7.6.5
# Wed, 06 Aug 2025 13:26:41 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
USER rocketchat
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app/bundle
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Wed, 06 Aug 2025 13:26:41 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 06 Aug 2025 13:26:41 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0731002e5f78a5a17484bce03c29cb6e053875de4a31ff3244b6e5e7880e68`  
		Last Modified: Tue, 12 Aug 2025 21:26:46 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27ae6f53ba4439325ee069de45f39b873e39a177c8116f2e317adfc666f0a4e`  
		Last Modified: Tue, 12 Aug 2025 21:26:56 GMT  
		Size: 49.0 MB (48967524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb4f79935d9398dc2bf52eb9dd2d2898be4ae2f19428dcfd200ee4b0c59387`  
		Last Modified: Tue, 12 Aug 2025 21:26:48 GMT  
		Size: 1.7 MB (1712539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d741e5a2c15f09f73507900c996aa5bacf9d2ea2811bc5222075fefa6217431`  
		Last Modified: Tue, 12 Aug 2025 21:26:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ba3d6af52921afcd67b93cbd837e337bb5f458b9545044ca8e1ddb666fe1cd`  
		Last Modified: Tue, 12 Aug 2025 22:51:03 GMT  
		Size: 48.7 MB (48723623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e961aa30a94bf44d8e89517e4b5af2eb196344ee7f8ac84a0cc42b18b2f07faf`  
		Last Modified: Tue, 12 Aug 2025 22:50:55 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ffb7f8f63757e1fc16fe76ca02b803beb85c0e1c6e6520b7cb4ceb13909e78`  
		Last Modified: Wed, 13 Aug 2025 01:47:49 GMT  
		Size: 389.3 MB (389347043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.6.5` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:edbad7dbfae7a35819ba3110f32afe7a26d4e00fe7ae8af7017b69334f1d9cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb315fb27e851a4280e8a80efe48984afb81dbda6c94438caca91e55ec8238a`

```dockerfile
```

-	Layers:
	-	`sha256:4fa72f905b689130d9c6e2188363ccaab3a0af74d0e87ea16d9c685c94c9eab2`  
		Last Modified: Wed, 13 Aug 2025 01:42:35 GMT  
		Size: 23.1 KB (23103 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.7`

```console
$ docker pull rocket.chat@sha256:6a9f0c497f4ecd6f7152b8a1e660cd733ef2c9c8b11027c9a60e5eb703b864cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:d137a9e40d8b8f0ef5980812a1908139f4c2b39d86c44f4df6abafa1f1d0f3ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.2 MB (512179057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83bbd07c0ec1ede833b4ddd35586bd2821ed2cd4d864d7ef657bd40ac53409b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 01 Aug 2025 10:06:16 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 01 Aug 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV NODE_VERSION=22.18.0
# Fri, 01 Aug 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Fri, 01 Aug 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Aug 2025 10:06:16 GMT
CMD ["node"]
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DENO_VERSION=1.43.5
# Wed, 06 Aug 2025 13:26:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
VOLUME [/app/uploads]
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app
# Wed, 06 Aug 2025 13:26:41 GMT
ENV NODE_ENV=production
# Wed, 06 Aug 2025 13:26:41 GMT
ENV RC_VERSION=7.7.8
# Wed, 06 Aug 2025 13:26:41 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
USER rocketchat
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app/bundle
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Wed, 06 Aug 2025 13:26:41 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 06 Aug 2025 13:26:41 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0731002e5f78a5a17484bce03c29cb6e053875de4a31ff3244b6e5e7880e68`  
		Last Modified: Tue, 12 Aug 2025 21:26:46 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27ae6f53ba4439325ee069de45f39b873e39a177c8116f2e317adfc666f0a4e`  
		Last Modified: Tue, 12 Aug 2025 21:26:56 GMT  
		Size: 49.0 MB (48967524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb4f79935d9398dc2bf52eb9dd2d2898be4ae2f19428dcfd200ee4b0c59387`  
		Last Modified: Tue, 12 Aug 2025 21:26:48 GMT  
		Size: 1.7 MB (1712539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d741e5a2c15f09f73507900c996aa5bacf9d2ea2811bc5222075fefa6217431`  
		Last Modified: Tue, 12 Aug 2025 21:26:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8469eb69cd15c5e6bd4872bff0e1d4e30651ad9e71f039e59bd3c8fc8ad21507`  
		Last Modified: Tue, 12 Aug 2025 22:53:05 GMT  
		Size: 48.7 MB (48723588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3707c010b89cabd9388a650772aaadd63fece2855d4b777fe9b23ca4d8bce563`  
		Last Modified: Tue, 12 Aug 2025 22:52:58 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0529b0efc426c8fdd42a7d3b00fba987887c20d6ef769c214ccdc9ec601757f9`  
		Last Modified: Wed, 13 Aug 2025 01:47:50 GMT  
		Size: 384.5 MB (384540156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.7` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:00ca90f892f8d5724bb5bd0dc8d55781aef447bb2e22c15dd40797adf4b58048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b018f1d63b60abf2f3cf868dbe3543e8cf29bdd16a710ede105e4b5d969dcde0`

```dockerfile
```

-	Layers:
	-	`sha256:c82fa6fb116c5842bcb3e1303a18c650dd29dad13013ae2a508597f41febe466`  
		Last Modified: Wed, 13 Aug 2025 01:42:40 GMT  
		Size: 23.1 KB (23103 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.7.8`

```console
$ docker pull rocket.chat@sha256:6a9f0c497f4ecd6f7152b8a1e660cd733ef2c9c8b11027c9a60e5eb703b864cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.7.8` - linux; amd64

```console
$ docker pull rocket.chat@sha256:d137a9e40d8b8f0ef5980812a1908139f4c2b39d86c44f4df6abafa1f1d0f3ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.2 MB (512179057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83bbd07c0ec1ede833b4ddd35586bd2821ed2cd4d864d7ef657bd40ac53409b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 01 Aug 2025 10:06:16 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 01 Aug 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV NODE_VERSION=22.18.0
# Fri, 01 Aug 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Fri, 01 Aug 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Aug 2025 10:06:16 GMT
CMD ["node"]
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DENO_VERSION=1.43.5
# Wed, 06 Aug 2025 13:26:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
VOLUME [/app/uploads]
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app
# Wed, 06 Aug 2025 13:26:41 GMT
ENV NODE_ENV=production
# Wed, 06 Aug 2025 13:26:41 GMT
ENV RC_VERSION=7.7.8
# Wed, 06 Aug 2025 13:26:41 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
USER rocketchat
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app/bundle
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Wed, 06 Aug 2025 13:26:41 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 06 Aug 2025 13:26:41 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0731002e5f78a5a17484bce03c29cb6e053875de4a31ff3244b6e5e7880e68`  
		Last Modified: Tue, 12 Aug 2025 21:26:46 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27ae6f53ba4439325ee069de45f39b873e39a177c8116f2e317adfc666f0a4e`  
		Last Modified: Tue, 12 Aug 2025 21:26:56 GMT  
		Size: 49.0 MB (48967524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb4f79935d9398dc2bf52eb9dd2d2898be4ae2f19428dcfd200ee4b0c59387`  
		Last Modified: Tue, 12 Aug 2025 21:26:48 GMT  
		Size: 1.7 MB (1712539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d741e5a2c15f09f73507900c996aa5bacf9d2ea2811bc5222075fefa6217431`  
		Last Modified: Tue, 12 Aug 2025 21:26:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8469eb69cd15c5e6bd4872bff0e1d4e30651ad9e71f039e59bd3c8fc8ad21507`  
		Last Modified: Tue, 12 Aug 2025 22:53:05 GMT  
		Size: 48.7 MB (48723588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3707c010b89cabd9388a650772aaadd63fece2855d4b777fe9b23ca4d8bce563`  
		Last Modified: Tue, 12 Aug 2025 22:52:58 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0529b0efc426c8fdd42a7d3b00fba987887c20d6ef769c214ccdc9ec601757f9`  
		Last Modified: Wed, 13 Aug 2025 01:47:50 GMT  
		Size: 384.5 MB (384540156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.7.8` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:00ca90f892f8d5724bb5bd0dc8d55781aef447bb2e22c15dd40797adf4b58048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b018f1d63b60abf2f3cf868dbe3543e8cf29bdd16a710ede105e4b5d969dcde0`

```dockerfile
```

-	Layers:
	-	`sha256:c82fa6fb116c5842bcb3e1303a18c650dd29dad13013ae2a508597f41febe466`  
		Last Modified: Wed, 13 Aug 2025 01:42:40 GMT  
		Size: 23.1 KB (23103 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.8`

```console
$ docker pull rocket.chat@sha256:11e3c705b81705a0d2560b9c45ab7e6fb8be4d06a2a1b574843569fd7d4483bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.8` - linux; amd64

```console
$ docker pull rocket.chat@sha256:5a82cd139b9ee59facf644b94acca896b69cba682a51bda3182af42a4250f906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **471.0 MB (471002697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94db8e013ccac954025bf49b486082366bc36fc5e58af4b4f268f958f91adf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 01 Aug 2025 10:06:16 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 01 Aug 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV NODE_VERSION=22.18.0
# Fri, 01 Aug 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Fri, 01 Aug 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Aug 2025 10:06:16 GMT
CMD ["node"]
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DENO_VERSION=1.43.5
# Wed, 06 Aug 2025 13:26:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
VOLUME [/app/uploads]
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app
# Wed, 06 Aug 2025 13:26:41 GMT
ENV NODE_ENV=production
# Wed, 06 Aug 2025 13:26:41 GMT
ENV RC_VERSION=7.8.4
# Wed, 06 Aug 2025 13:26:41 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
USER rocketchat
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app/bundle
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Wed, 06 Aug 2025 13:26:41 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 06 Aug 2025 13:26:41 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0731002e5f78a5a17484bce03c29cb6e053875de4a31ff3244b6e5e7880e68`  
		Last Modified: Tue, 12 Aug 2025 21:26:46 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27ae6f53ba4439325ee069de45f39b873e39a177c8116f2e317adfc666f0a4e`  
		Last Modified: Tue, 12 Aug 2025 21:26:56 GMT  
		Size: 49.0 MB (48967524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb4f79935d9398dc2bf52eb9dd2d2898be4ae2f19428dcfd200ee4b0c59387`  
		Last Modified: Tue, 12 Aug 2025 21:26:48 GMT  
		Size: 1.7 MB (1712539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d741e5a2c15f09f73507900c996aa5bacf9d2ea2811bc5222075fefa6217431`  
		Last Modified: Tue, 12 Aug 2025 21:26:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbc61901c19568d140b7215998b0c16c128abb2d04d1bd60bfc671eb3a5970a`  
		Last Modified: Wed, 13 Aug 2025 01:46:41 GMT  
		Size: 48.7 MB (48723589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9f7a611e3696cd387e504dff8c8c46706e8fc1c81a698e675a8abaca53ae19`  
		Last Modified: Tue, 12 Aug 2025 23:31:57 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c034c183122dd2a9fdf52ce969039f138317a95bb0bbcb8b532d84abb46bba2d`  
		Last Modified: Wed, 13 Aug 2025 01:47:36 GMT  
		Size: 343.4 MB (343363795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.8` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:0dc7d5fbff4bbedf27d288a23e944133b40e49da700f1eee3f7ef3a4e4f266da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c909213cd26c1e61dc03fca9535f87091ed304979544e639bfcb60f1f8a6f066`

```dockerfile
```

-	Layers:
	-	`sha256:e0f19a3b5d0c170f470df3de68358663aeaa5e25ba237f2ebe8703ce9ce65376`  
		Last Modified: Wed, 13 Aug 2025 01:42:45 GMT  
		Size: 23.1 KB (23103 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.8.4`

```console
$ docker pull rocket.chat@sha256:11e3c705b81705a0d2560b9c45ab7e6fb8be4d06a2a1b574843569fd7d4483bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.8.4` - linux; amd64

```console
$ docker pull rocket.chat@sha256:5a82cd139b9ee59facf644b94acca896b69cba682a51bda3182af42a4250f906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **471.0 MB (471002697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94db8e013ccac954025bf49b486082366bc36fc5e58af4b4f268f958f91adf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 01 Aug 2025 10:06:16 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 01 Aug 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV NODE_VERSION=22.18.0
# Fri, 01 Aug 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Fri, 01 Aug 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Aug 2025 10:06:16 GMT
CMD ["node"]
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DENO_VERSION=1.43.5
# Wed, 06 Aug 2025 13:26:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
VOLUME [/app/uploads]
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app
# Wed, 06 Aug 2025 13:26:41 GMT
ENV NODE_ENV=production
# Wed, 06 Aug 2025 13:26:41 GMT
ENV RC_VERSION=7.8.4
# Wed, 06 Aug 2025 13:26:41 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Wed, 06 Aug 2025 13:26:41 GMT
USER rocketchat
# Wed, 06 Aug 2025 13:26:41 GMT
WORKDIR /app/bundle
# Wed, 06 Aug 2025 13:26:41 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Wed, 06 Aug 2025 13:26:41 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 06 Aug 2025 13:26:41 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0731002e5f78a5a17484bce03c29cb6e053875de4a31ff3244b6e5e7880e68`  
		Last Modified: Tue, 12 Aug 2025 21:26:46 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27ae6f53ba4439325ee069de45f39b873e39a177c8116f2e317adfc666f0a4e`  
		Last Modified: Tue, 12 Aug 2025 21:26:56 GMT  
		Size: 49.0 MB (48967524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb4f79935d9398dc2bf52eb9dd2d2898be4ae2f19428dcfd200ee4b0c59387`  
		Last Modified: Tue, 12 Aug 2025 21:26:48 GMT  
		Size: 1.7 MB (1712539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d741e5a2c15f09f73507900c996aa5bacf9d2ea2811bc5222075fefa6217431`  
		Last Modified: Tue, 12 Aug 2025 21:26:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbc61901c19568d140b7215998b0c16c128abb2d04d1bd60bfc671eb3a5970a`  
		Last Modified: Wed, 13 Aug 2025 01:46:41 GMT  
		Size: 48.7 MB (48723589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9f7a611e3696cd387e504dff8c8c46706e8fc1c81a698e675a8abaca53ae19`  
		Last Modified: Tue, 12 Aug 2025 23:31:57 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c034c183122dd2a9fdf52ce969039f138317a95bb0bbcb8b532d84abb46bba2d`  
		Last Modified: Wed, 13 Aug 2025 01:47:36 GMT  
		Size: 343.4 MB (343363795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.8.4` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:0dc7d5fbff4bbedf27d288a23e944133b40e49da700f1eee3f7ef3a4e4f266da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c909213cd26c1e61dc03fca9535f87091ed304979544e639bfcb60f1f8a6f066`

```dockerfile
```

-	Layers:
	-	`sha256:e0f19a3b5d0c170f470df3de68358663aeaa5e25ba237f2ebe8703ce9ce65376`  
		Last Modified: Wed, 13 Aug 2025 01:42:45 GMT  
		Size: 23.1 KB (23103 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.9`

```console
$ docker pull rocket.chat@sha256:4210ac55198da06aa5d271be1e8187d1f870cdd2f7a90dbadcc9cf2c18e6397b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.9` - linux; amd64

```console
$ docker pull rocket.chat@sha256:88c1cc18ede781afa0d05f2afb6310d245d4ee0f4fd058b27119004830036969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.4 MB (494448639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438df727799a05ee82b5f148c458407fc1d67b29321977e613b73168ca8bc2a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 01 Aug 2025 10:06:16 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 01 Aug 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV NODE_VERSION=22.18.0
# Fri, 01 Aug 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Fri, 01 Aug 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Aug 2025 10:06:16 GMT
CMD ["node"]
# Tue, 12 Aug 2025 22:03:11 GMT
ENV DENO_VERSION=1.43.5
# Tue, 12 Aug 2025 22:03:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 12 Aug 2025 22:03:11 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Tue, 12 Aug 2025 22:03:11 GMT
VOLUME [/app/uploads]
# Tue, 12 Aug 2025 22:03:11 GMT
WORKDIR /app
# Tue, 12 Aug 2025 22:03:11 GMT
ENV NODE_ENV=production
# Tue, 12 Aug 2025 22:03:11 GMT
ENV RC_VERSION=7.9.3
# Tue, 12 Aug 2025 22:03:11 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Tue, 12 Aug 2025 22:03:11 GMT
USER rocketchat
# Tue, 12 Aug 2025 22:03:11 GMT
WORKDIR /app/bundle
# Tue, 12 Aug 2025 22:03:11 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Tue, 12 Aug 2025 22:03:11 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 12 Aug 2025 22:03:11 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0731002e5f78a5a17484bce03c29cb6e053875de4a31ff3244b6e5e7880e68`  
		Last Modified: Tue, 12 Aug 2025 21:26:46 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27ae6f53ba4439325ee069de45f39b873e39a177c8116f2e317adfc666f0a4e`  
		Last Modified: Tue, 12 Aug 2025 21:26:56 GMT  
		Size: 49.0 MB (48967524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb4f79935d9398dc2bf52eb9dd2d2898be4ae2f19428dcfd200ee4b0c59387`  
		Last Modified: Tue, 12 Aug 2025 21:26:48 GMT  
		Size: 1.7 MB (1712539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d741e5a2c15f09f73507900c996aa5bacf9d2ea2811bc5222075fefa6217431`  
		Last Modified: Tue, 12 Aug 2025 21:26:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bacb3a7e614d9e648c1efee9fb7c317d25dfa7c5967d5d8aa8e9c6209b4449b`  
		Last Modified: Tue, 12 Aug 2025 23:41:04 GMT  
		Size: 48.7 MB (48723619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3992bf184b1f8dd4d65abeb153a9bb869e468e1617581930d155e2c5b0ef347`  
		Last Modified: Tue, 12 Aug 2025 23:41:00 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6baaba14b8edf9a68cd800d883cfa965179903886aaa91c36860d293cfc90eb`  
		Last Modified: Wed, 13 Aug 2025 01:43:34 GMT  
		Size: 366.8 MB (366809703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.9` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:c2660495bed46462e20e29a8611225caf3a94c158a67aa57453f9d79239e4b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becc7672735b348cd32e0383ebaa65dba006964e4a93d093e29f9e899c56de24`

```dockerfile
```

-	Layers:
	-	`sha256:132f3bc6df9de16ef56c3961503a35d7248178257d87f29947db03fa83755084`  
		Last Modified: Wed, 13 Aug 2025 01:42:20 GMT  
		Size: 23.7 KB (23708 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.9.3`

```console
$ docker pull rocket.chat@sha256:4210ac55198da06aa5d271be1e8187d1f870cdd2f7a90dbadcc9cf2c18e6397b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.9.3` - linux; amd64

```console
$ docker pull rocket.chat@sha256:88c1cc18ede781afa0d05f2afb6310d245d4ee0f4fd058b27119004830036969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.4 MB (494448639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438df727799a05ee82b5f148c458407fc1d67b29321977e613b73168ca8bc2a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 01 Aug 2025 10:06:16 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 01 Aug 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV NODE_VERSION=22.18.0
# Fri, 01 Aug 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Fri, 01 Aug 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Aug 2025 10:06:16 GMT
CMD ["node"]
# Tue, 12 Aug 2025 22:03:11 GMT
ENV DENO_VERSION=1.43.5
# Tue, 12 Aug 2025 22:03:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 12 Aug 2025 22:03:11 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Tue, 12 Aug 2025 22:03:11 GMT
VOLUME [/app/uploads]
# Tue, 12 Aug 2025 22:03:11 GMT
WORKDIR /app
# Tue, 12 Aug 2025 22:03:11 GMT
ENV NODE_ENV=production
# Tue, 12 Aug 2025 22:03:11 GMT
ENV RC_VERSION=7.9.3
# Tue, 12 Aug 2025 22:03:11 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Tue, 12 Aug 2025 22:03:11 GMT
USER rocketchat
# Tue, 12 Aug 2025 22:03:11 GMT
WORKDIR /app/bundle
# Tue, 12 Aug 2025 22:03:11 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Tue, 12 Aug 2025 22:03:11 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 12 Aug 2025 22:03:11 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0731002e5f78a5a17484bce03c29cb6e053875de4a31ff3244b6e5e7880e68`  
		Last Modified: Tue, 12 Aug 2025 21:26:46 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27ae6f53ba4439325ee069de45f39b873e39a177c8116f2e317adfc666f0a4e`  
		Last Modified: Tue, 12 Aug 2025 21:26:56 GMT  
		Size: 49.0 MB (48967524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb4f79935d9398dc2bf52eb9dd2d2898be4ae2f19428dcfd200ee4b0c59387`  
		Last Modified: Tue, 12 Aug 2025 21:26:48 GMT  
		Size: 1.7 MB (1712539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d741e5a2c15f09f73507900c996aa5bacf9d2ea2811bc5222075fefa6217431`  
		Last Modified: Tue, 12 Aug 2025 21:26:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bacb3a7e614d9e648c1efee9fb7c317d25dfa7c5967d5d8aa8e9c6209b4449b`  
		Last Modified: Tue, 12 Aug 2025 23:41:04 GMT  
		Size: 48.7 MB (48723619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3992bf184b1f8dd4d65abeb153a9bb869e468e1617581930d155e2c5b0ef347`  
		Last Modified: Tue, 12 Aug 2025 23:41:00 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6baaba14b8edf9a68cd800d883cfa965179903886aaa91c36860d293cfc90eb`  
		Last Modified: Wed, 13 Aug 2025 01:43:34 GMT  
		Size: 366.8 MB (366809703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.9.3` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:c2660495bed46462e20e29a8611225caf3a94c158a67aa57453f9d79239e4b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becc7672735b348cd32e0383ebaa65dba006964e4a93d093e29f9e899c56de24`

```dockerfile
```

-	Layers:
	-	`sha256:132f3bc6df9de16ef56c3961503a35d7248178257d87f29947db03fa83755084`  
		Last Modified: Wed, 13 Aug 2025 01:42:20 GMT  
		Size: 23.7 KB (23708 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:latest`

```console
$ docker pull rocket.chat@sha256:4210ac55198da06aa5d271be1e8187d1f870cdd2f7a90dbadcc9cf2c18e6397b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:latest` - linux; amd64

```console
$ docker pull rocket.chat@sha256:88c1cc18ede781afa0d05f2afb6310d245d4ee0f4fd058b27119004830036969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.4 MB (494448639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438df727799a05ee82b5f148c458407fc1d67b29321977e613b73168ca8bc2a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Fri, 01 Aug 2025 10:06:16 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 01 Aug 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV NODE_VERSION=22.18.0
# Fri, 01 Aug 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Fri, 01 Aug 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Aug 2025 10:06:16 GMT
CMD ["node"]
# Tue, 12 Aug 2025 22:03:11 GMT
ENV DENO_VERSION=1.43.5
# Tue, 12 Aug 2025 22:03:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 12 Aug 2025 22:03:11 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Tue, 12 Aug 2025 22:03:11 GMT
VOLUME [/app/uploads]
# Tue, 12 Aug 2025 22:03:11 GMT
WORKDIR /app
# Tue, 12 Aug 2025 22:03:11 GMT
ENV NODE_ENV=production
# Tue, 12 Aug 2025 22:03:11 GMT
ENV RC_VERSION=7.9.3
# Tue, 12 Aug 2025 22:03:11 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Tue, 12 Aug 2025 22:03:11 GMT
USER rocketchat
# Tue, 12 Aug 2025 22:03:11 GMT
WORKDIR /app/bundle
# Tue, 12 Aug 2025 22:03:11 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Tue, 12 Aug 2025 22:03:11 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 12 Aug 2025 22:03:11 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0731002e5f78a5a17484bce03c29cb6e053875de4a31ff3244b6e5e7880e68`  
		Last Modified: Tue, 12 Aug 2025 21:26:46 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27ae6f53ba4439325ee069de45f39b873e39a177c8116f2e317adfc666f0a4e`  
		Last Modified: Tue, 12 Aug 2025 21:26:56 GMT  
		Size: 49.0 MB (48967524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb4f79935d9398dc2bf52eb9dd2d2898be4ae2f19428dcfd200ee4b0c59387`  
		Last Modified: Tue, 12 Aug 2025 21:26:48 GMT  
		Size: 1.7 MB (1712539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d741e5a2c15f09f73507900c996aa5bacf9d2ea2811bc5222075fefa6217431`  
		Last Modified: Tue, 12 Aug 2025 21:26:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bacb3a7e614d9e648c1efee9fb7c317d25dfa7c5967d5d8aa8e9c6209b4449b`  
		Last Modified: Tue, 12 Aug 2025 23:41:04 GMT  
		Size: 48.7 MB (48723619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3992bf184b1f8dd4d65abeb153a9bb869e468e1617581930d155e2c5b0ef347`  
		Last Modified: Tue, 12 Aug 2025 23:41:00 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6baaba14b8edf9a68cd800d883cfa965179903886aaa91c36860d293cfc90eb`  
		Last Modified: Wed, 13 Aug 2025 01:43:34 GMT  
		Size: 366.8 MB (366809703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:latest` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:c2660495bed46462e20e29a8611225caf3a94c158a67aa57453f9d79239e4b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becc7672735b348cd32e0383ebaa65dba006964e4a93d093e29f9e899c56de24`

```dockerfile
```

-	Layers:
	-	`sha256:132f3bc6df9de16ef56c3961503a35d7248178257d87f29947db03fa83755084`  
		Last Modified: Wed, 13 Aug 2025 01:42:20 GMT  
		Size: 23.7 KB (23708 bytes)  
		MIME: application/vnd.in-toto+json

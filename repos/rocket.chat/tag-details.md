<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rocket.chat`

-	[`rocket.chat:7`](#rocketchat7)
-	[`rocket.chat:7.10`](#rocketchat710)
-	[`rocket.chat:7.10.9`](#rocketchat7109)
-	[`rocket.chat:7.12`](#rocketchat712)
-	[`rocket.chat:7.12.7`](#rocketchat7127)
-	[`rocket.chat:7.13`](#rocketchat713)
-	[`rocket.chat:7.13.6`](#rocketchat7136)
-	[`rocket.chat:8`](#rocketchat8)
-	[`rocket.chat:8.0`](#rocketchat80)
-	[`rocket.chat:8.0.5`](#rocketchat805)
-	[`rocket.chat:8.1`](#rocketchat81)
-	[`rocket.chat:8.1.4`](#rocketchat814)
-	[`rocket.chat:8.2`](#rocketchat82)
-	[`rocket.chat:8.2.3`](#rocketchat823)
-	[`rocket.chat:8.3`](#rocketchat83)
-	[`rocket.chat:8.3.3`](#rocketchat833)
-	[`rocket.chat:8.4`](#rocketchat84)
-	[`rocket.chat:8.4.1`](#rocketchat841)
-	[`rocket.chat:latest`](#rocketchatlatest)

## `rocket.chat:7`

```console
$ docker pull rocket.chat@sha256:5feb2d5416eafaca62ca72025449758d77d17280b8bd4e767f71046939956b6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:a281e61487e3b1eb5d65c6ce0d0848e7e5cc8078ea0831c0eb0b92d204ad2a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.2 MB (472168140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4e40b3368cefc1f6ae68259b8a386feab247c86df6036342bb532ef710415f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:16:18 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:16:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:16:18 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:16:18 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:16:18 GMT
WORKDIR /app
# Thu, 14 May 2026 17:16:18 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:16:18 GMT
ENV RC_VERSION=7.13.6
# Thu, 14 May 2026 17:17:20 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:17:20 GMT
USER rocketchat
# Thu, 14 May 2026 17:17:20 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:17:20 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:17:20 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:17:20 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006ff2416b3003914a0767e7d73b79505098d1e5df80912fc93026b99213a88e`  
		Last Modified: Thu, 14 May 2026 17:18:05 GMT  
		Size: 48.7 MB (48723813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c688d2eaa9541b6512fcc21f4221306b648fd29b3e863041386e25587923cf`  
		Last Modified: Thu, 14 May 2026 17:18:02 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1168456c255d3a6bc22ce1cf7bd4db0644c3f6c8525b408bf3f1b0af0850025b`  
		Last Modified: Thu, 14 May 2026 17:18:11 GMT  
		Size: 343.6 MB (343564263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:64ea9a4996cabc040ff2fe9b0b3e2118b1fb62b0d962dd852284016acd494ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 KB (23365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7dbaa6b2ec6884d2144e328fd50d5516fa4119d791f2c5c9e6161dc7b8cd3c`

```dockerfile
```

-	Layers:
	-	`sha256:01f6886165c4b5bd4698a6f130f593c3693f7dfd08050aba7db6959fe7f9f115`  
		Last Modified: Thu, 14 May 2026 17:18:02 GMT  
		Size: 23.4 KB (23365 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.10`

```console
$ docker pull rocket.chat@sha256:77e05ea293a95a319aae3f562dc8130a286b099aec6b86a7e2fe8e8c8f44f1b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.10` - linux; amd64

```console
$ docker pull rocket.chat@sha256:00fe49ee22473ec422e488048521a2a114e9ae42b4f30217658e28a924863b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.4 MB (472413903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21fd231e89ae7c920ea702afb10bfe0e3178161c2b574229e99e28605e19b168`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:16:34 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:16:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:16:34 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:16:34 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:16:34 GMT
WORKDIR /app
# Thu, 14 May 2026 17:16:34 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:16:34 GMT
ENV RC_VERSION=7.10.9
# Thu, 14 May 2026 17:17:41 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:17:41 GMT
USER rocketchat
# Thu, 14 May 2026 17:17:41 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:17:41 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:17:41 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:17:41 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfe298be14163cab1efd6b466423231c2e5ed5f4b22be3fe03d5a8ec7019749`  
		Last Modified: Thu, 14 May 2026 17:18:27 GMT  
		Size: 48.7 MB (48723804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d54074f2fa492145041175fc326897a33baa3e8f65ec1d8707276c01d4114ff`  
		Last Modified: Thu, 14 May 2026 17:18:24 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e4351f8ad0474dd3fb4d0a74a53af80b7de5909a31d75c32db4d05277fb0ad`  
		Last Modified: Thu, 14 May 2026 17:18:35 GMT  
		Size: 343.8 MB (343810033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.10` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:535d69af7dc3ad57a46cec27ae017ab77487890364c1976e00ebf5426c94d39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577f934b377aecaf0add1026469140406d05a87862e893d4ca381cf2e0d42d00`

```dockerfile
```

-	Layers:
	-	`sha256:ee09ec1a62f400c8aed3559d5a15b66cd61af1e4f1a2d75acfaad751317351ef`  
		Last Modified: Thu, 14 May 2026 17:18:24 GMT  
		Size: 23.1 KB (23066 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.10.9`

```console
$ docker pull rocket.chat@sha256:77e05ea293a95a319aae3f562dc8130a286b099aec6b86a7e2fe8e8c8f44f1b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.10.9` - linux; amd64

```console
$ docker pull rocket.chat@sha256:00fe49ee22473ec422e488048521a2a114e9ae42b4f30217658e28a924863b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.4 MB (472413903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21fd231e89ae7c920ea702afb10bfe0e3178161c2b574229e99e28605e19b168`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:16:34 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:16:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:16:34 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:16:34 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:16:34 GMT
WORKDIR /app
# Thu, 14 May 2026 17:16:34 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:16:34 GMT
ENV RC_VERSION=7.10.9
# Thu, 14 May 2026 17:17:41 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:17:41 GMT
USER rocketchat
# Thu, 14 May 2026 17:17:41 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:17:41 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:17:41 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:17:41 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfe298be14163cab1efd6b466423231c2e5ed5f4b22be3fe03d5a8ec7019749`  
		Last Modified: Thu, 14 May 2026 17:18:27 GMT  
		Size: 48.7 MB (48723804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d54074f2fa492145041175fc326897a33baa3e8f65ec1d8707276c01d4114ff`  
		Last Modified: Thu, 14 May 2026 17:18:24 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e4351f8ad0474dd3fb4d0a74a53af80b7de5909a31d75c32db4d05277fb0ad`  
		Last Modified: Thu, 14 May 2026 17:18:35 GMT  
		Size: 343.8 MB (343810033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.10.9` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:535d69af7dc3ad57a46cec27ae017ab77487890364c1976e00ebf5426c94d39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577f934b377aecaf0add1026469140406d05a87862e893d4ca381cf2e0d42d00`

```dockerfile
```

-	Layers:
	-	`sha256:ee09ec1a62f400c8aed3559d5a15b66cd61af1e4f1a2d75acfaad751317351ef`  
		Last Modified: Thu, 14 May 2026 17:18:24 GMT  
		Size: 23.1 KB (23066 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.12`

```console
$ docker pull rocket.chat@sha256:612a83788d6e085adfe6c59e0c757bc8fe27a42d1ea71b6fae06198e00722966
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.12` - linux; amd64

```console
$ docker pull rocket.chat@sha256:417a5b009fd1411b6787e696a1e097da60711f17cff0c6f1badfc55df21cc614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.9 MB (494890990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71247bc1cc5ff7b6a6fee9d4a6a2830964319be17f7a05406d36c090609c5802`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:16:22 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:16:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:16:22 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:16:22 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:16:22 GMT
WORKDIR /app
# Thu, 14 May 2026 17:16:22 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:16:22 GMT
ENV RC_VERSION=7.12.7
# Thu, 14 May 2026 17:17:34 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:17:34 GMT
USER rocketchat
# Thu, 14 May 2026 17:17:35 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:17:35 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:17:35 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:17:35 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a3958fc3ccdd5a0cc7569dbe6a0cf80dd4c95e47579fd8332f406139d9f2f3`  
		Last Modified: Thu, 14 May 2026 17:18:28 GMT  
		Size: 48.7 MB (48723778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3339a925a06269e09f987bbd1589967c2332def1621d89a7e505608134fdcd`  
		Last Modified: Thu, 14 May 2026 17:18:26 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f8bc4e05e0515da73d044e4963be7c50e38a7d94c520d995938d9ef9c3362`  
		Last Modified: Thu, 14 May 2026 17:18:35 GMT  
		Size: 366.3 MB (366287149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.12` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:08da8b2a95e7ef6ab8072e9854a18706e497ab9634b6db8c7115d4528447cb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369d02f3b19e30c293c95cf2f83a41e4fec43b801a14e7f102679eaf9cceb903`

```dockerfile
```

-	Layers:
	-	`sha256:f9ca98bd65eb6a28f440d7abb0ac0b8d34642dd9fa34cbf80b0e63e61fe61c27`  
		Last Modified: Thu, 14 May 2026 17:18:26 GMT  
		Size: 23.1 KB (23066 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.12.7`

```console
$ docker pull rocket.chat@sha256:612a83788d6e085adfe6c59e0c757bc8fe27a42d1ea71b6fae06198e00722966
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.12.7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:417a5b009fd1411b6787e696a1e097da60711f17cff0c6f1badfc55df21cc614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.9 MB (494890990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71247bc1cc5ff7b6a6fee9d4a6a2830964319be17f7a05406d36c090609c5802`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:16:22 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:16:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:16:22 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:16:22 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:16:22 GMT
WORKDIR /app
# Thu, 14 May 2026 17:16:22 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:16:22 GMT
ENV RC_VERSION=7.12.7
# Thu, 14 May 2026 17:17:34 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:17:34 GMT
USER rocketchat
# Thu, 14 May 2026 17:17:35 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:17:35 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:17:35 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:17:35 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a3958fc3ccdd5a0cc7569dbe6a0cf80dd4c95e47579fd8332f406139d9f2f3`  
		Last Modified: Thu, 14 May 2026 17:18:28 GMT  
		Size: 48.7 MB (48723778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3339a925a06269e09f987bbd1589967c2332def1621d89a7e505608134fdcd`  
		Last Modified: Thu, 14 May 2026 17:18:26 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f8bc4e05e0515da73d044e4963be7c50e38a7d94c520d995938d9ef9c3362`  
		Last Modified: Thu, 14 May 2026 17:18:35 GMT  
		Size: 366.3 MB (366287149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.12.7` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:08da8b2a95e7ef6ab8072e9854a18706e497ab9634b6db8c7115d4528447cb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369d02f3b19e30c293c95cf2f83a41e4fec43b801a14e7f102679eaf9cceb903`

```dockerfile
```

-	Layers:
	-	`sha256:f9ca98bd65eb6a28f440d7abb0ac0b8d34642dd9fa34cbf80b0e63e61fe61c27`  
		Last Modified: Thu, 14 May 2026 17:18:26 GMT  
		Size: 23.1 KB (23066 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.13`

```console
$ docker pull rocket.chat@sha256:5feb2d5416eafaca62ca72025449758d77d17280b8bd4e767f71046939956b6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.13` - linux; amd64

```console
$ docker pull rocket.chat@sha256:a281e61487e3b1eb5d65c6ce0d0848e7e5cc8078ea0831c0eb0b92d204ad2a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.2 MB (472168140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4e40b3368cefc1f6ae68259b8a386feab247c86df6036342bb532ef710415f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:16:18 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:16:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:16:18 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:16:18 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:16:18 GMT
WORKDIR /app
# Thu, 14 May 2026 17:16:18 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:16:18 GMT
ENV RC_VERSION=7.13.6
# Thu, 14 May 2026 17:17:20 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:17:20 GMT
USER rocketchat
# Thu, 14 May 2026 17:17:20 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:17:20 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:17:20 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:17:20 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006ff2416b3003914a0767e7d73b79505098d1e5df80912fc93026b99213a88e`  
		Last Modified: Thu, 14 May 2026 17:18:05 GMT  
		Size: 48.7 MB (48723813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c688d2eaa9541b6512fcc21f4221306b648fd29b3e863041386e25587923cf`  
		Last Modified: Thu, 14 May 2026 17:18:02 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1168456c255d3a6bc22ce1cf7bd4db0644c3f6c8525b408bf3f1b0af0850025b`  
		Last Modified: Thu, 14 May 2026 17:18:11 GMT  
		Size: 343.6 MB (343564263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.13` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:64ea9a4996cabc040ff2fe9b0b3e2118b1fb62b0d962dd852284016acd494ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 KB (23365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7dbaa6b2ec6884d2144e328fd50d5516fa4119d791f2c5c9e6161dc7b8cd3c`

```dockerfile
```

-	Layers:
	-	`sha256:01f6886165c4b5bd4698a6f130f593c3693f7dfd08050aba7db6959fe7f9f115`  
		Last Modified: Thu, 14 May 2026 17:18:02 GMT  
		Size: 23.4 KB (23365 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.13.6`

```console
$ docker pull rocket.chat@sha256:5feb2d5416eafaca62ca72025449758d77d17280b8bd4e767f71046939956b6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.13.6` - linux; amd64

```console
$ docker pull rocket.chat@sha256:a281e61487e3b1eb5d65c6ce0d0848e7e5cc8078ea0831c0eb0b92d204ad2a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.2 MB (472168140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4e40b3368cefc1f6ae68259b8a386feab247c86df6036342bb532ef710415f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:16:18 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:16:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:16:18 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:16:18 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:16:18 GMT
WORKDIR /app
# Thu, 14 May 2026 17:16:18 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:16:18 GMT
ENV RC_VERSION=7.13.6
# Thu, 14 May 2026 17:17:20 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:17:20 GMT
USER rocketchat
# Thu, 14 May 2026 17:17:20 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:17:20 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:17:20 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:17:20 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006ff2416b3003914a0767e7d73b79505098d1e5df80912fc93026b99213a88e`  
		Last Modified: Thu, 14 May 2026 17:18:05 GMT  
		Size: 48.7 MB (48723813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c688d2eaa9541b6512fcc21f4221306b648fd29b3e863041386e25587923cf`  
		Last Modified: Thu, 14 May 2026 17:18:02 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1168456c255d3a6bc22ce1cf7bd4db0644c3f6c8525b408bf3f1b0af0850025b`  
		Last Modified: Thu, 14 May 2026 17:18:11 GMT  
		Size: 343.6 MB (343564263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.13.6` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:64ea9a4996cabc040ff2fe9b0b3e2118b1fb62b0d962dd852284016acd494ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 KB (23365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7dbaa6b2ec6884d2144e328fd50d5516fa4119d791f2c5c9e6161dc7b8cd3c`

```dockerfile
```

-	Layers:
	-	`sha256:01f6886165c4b5bd4698a6f130f593c3693f7dfd08050aba7db6959fe7f9f115`  
		Last Modified: Thu, 14 May 2026 17:18:02 GMT  
		Size: 23.4 KB (23365 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:8`

```console
$ docker pull rocket.chat@sha256:5372d4a2eb7d01235661360f48afac3f2ce6e1dbdd66511ec0d7f71b52576254
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:8` - linux; amd64

```console
$ docker pull rocket.chat@sha256:9b63ddec180ae8e9f29ab546f279047800aa58476da29dd3f5861fae9f5af413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.3 MB (415286262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3339b1fa003434c5b41b87d1d82de10d7c5ff7434c4d6a5638bb395cf7661b41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:15:58 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:15:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:15:58 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:15:58 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:15:58 GMT
WORKDIR /app
# Thu, 14 May 2026 17:15:58 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:15:58 GMT
ENV RC_VERSION=8.4.1
# Thu, 14 May 2026 17:17:07 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:17:07 GMT
USER rocketchat
# Thu, 14 May 2026 17:17:08 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:17:08 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:17:08 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:17:08 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d29ba0093f68a32f72394af37461f20c9860c52822b542bfed8513b72936ac`  
		Last Modified: Thu, 14 May 2026 17:17:47 GMT  
		Size: 48.7 MB (48723749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6b0997c2b24978e7346f4d6a897b1e9530c0498c6d7c325286d43c0c6c4245`  
		Last Modified: Thu, 14 May 2026 17:17:45 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be49e58ed3bf6a925e3c2453fd20e6186e562c97b7464c5e1f0834e2d6deeac`  
		Last Modified: Thu, 14 May 2026 17:17:52 GMT  
		Size: 286.7 MB (286682449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:8` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:6fba49a3990192cfcc9b1c6e3d3395b05461f4d0df710c16c156dcb892fdb5dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102c8c8dbd18cbbad31b0b29932826639bcee03c05c360c67f3acdb672b06fe3`

```dockerfile
```

-	Layers:
	-	`sha256:613df46d5b23176a530883cf41ffa444f234153a99127b7d2064dea12a39bb3b`  
		Last Modified: Thu, 14 May 2026 17:17:44 GMT  
		Size: 23.7 KB (23666 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:8.0`

```console
$ docker pull rocket.chat@sha256:1546f62ab3ad9b85ee18c6608f965bc769f882ec3f622a6ff30537d97b7eda34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:8.0` - linux; amd64

```console
$ docker pull rocket.chat@sha256:db12bc6b6a6482c2e8f873f74627e8fac724158580bb41695a8d92af6295f32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.5 MB (458511239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7af99f59bd394a0836dc92e4eb696a5f15d93b025476a813ebd23dee11053a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:16:14 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:16:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:16:14 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:16:14 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:16:14 GMT
WORKDIR /app
# Thu, 14 May 2026 17:16:14 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:16:14 GMT
ENV RC_VERSION=8.0.5
# Thu, 14 May 2026 17:17:17 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:17:17 GMT
USER rocketchat
# Thu, 14 May 2026 17:17:18 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:17:18 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:17:18 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:17:18 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a035c80d3f4c907741dbb1a807a6b5b8fa5c1f642aa71a13667ce315de7d18fb`  
		Last Modified: Thu, 14 May 2026 17:18:02 GMT  
		Size: 48.7 MB (48723776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0f732a21a88cedf97dde82b1b4c78da5bbe4718d2636bdca8751dc852a3ba2`  
		Last Modified: Thu, 14 May 2026 17:18:00 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85118b2cc7a6d8a09772d0752e22f1d4b2e786a13d06d6c0233d74ab50106e15`  
		Last Modified: Thu, 14 May 2026 17:18:09 GMT  
		Size: 329.9 MB (329907400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:8.0` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:be6200c7a6539275bba85eb2f1c595ce894900d1996b4a77f30f02bace82a1a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30af44130b1ffe4c4e2a5941a87dae444493374073d0e45aaab15bb0b8fe9f1f`

```dockerfile
```

-	Layers:
	-	`sha256:4d053ad2049d6ca9b97a0da7f91e7d398ed799b76c660d61506063be5537ddd5`  
		Last Modified: Thu, 14 May 2026 17:18:00 GMT  
		Size: 23.1 KB (23058 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:8.0.5`

```console
$ docker pull rocket.chat@sha256:1546f62ab3ad9b85ee18c6608f965bc769f882ec3f622a6ff30537d97b7eda34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:8.0.5` - linux; amd64

```console
$ docker pull rocket.chat@sha256:db12bc6b6a6482c2e8f873f74627e8fac724158580bb41695a8d92af6295f32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.5 MB (458511239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7af99f59bd394a0836dc92e4eb696a5f15d93b025476a813ebd23dee11053a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:16:14 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:16:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:16:14 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:16:14 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:16:14 GMT
WORKDIR /app
# Thu, 14 May 2026 17:16:14 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:16:14 GMT
ENV RC_VERSION=8.0.5
# Thu, 14 May 2026 17:17:17 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:17:17 GMT
USER rocketchat
# Thu, 14 May 2026 17:17:18 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:17:18 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:17:18 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:17:18 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a035c80d3f4c907741dbb1a807a6b5b8fa5c1f642aa71a13667ce315de7d18fb`  
		Last Modified: Thu, 14 May 2026 17:18:02 GMT  
		Size: 48.7 MB (48723776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0f732a21a88cedf97dde82b1b4c78da5bbe4718d2636bdca8751dc852a3ba2`  
		Last Modified: Thu, 14 May 2026 17:18:00 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85118b2cc7a6d8a09772d0752e22f1d4b2e786a13d06d6c0233d74ab50106e15`  
		Last Modified: Thu, 14 May 2026 17:18:09 GMT  
		Size: 329.9 MB (329907400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:8.0.5` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:be6200c7a6539275bba85eb2f1c595ce894900d1996b4a77f30f02bace82a1a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30af44130b1ffe4c4e2a5941a87dae444493374073d0e45aaab15bb0b8fe9f1f`

```dockerfile
```

-	Layers:
	-	`sha256:4d053ad2049d6ca9b97a0da7f91e7d398ed799b76c660d61506063be5537ddd5`  
		Last Modified: Thu, 14 May 2026 17:18:00 GMT  
		Size: 23.1 KB (23058 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:8.1`

```console
$ docker pull rocket.chat@sha256:12888c6cf7d7a192020a21a1070e2c7fa9e867751f880a602ce22473c8758a02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:8.1` - linux; amd64

```console
$ docker pull rocket.chat@sha256:020990703ce575c91fc058ff8d0070636c48078ddfdeeaa93bc4d13058b7bc41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.1 MB (459112644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60e5d8d53a2bd2cf9803e2ae951f9fc464f99bd46f360d725c10ca69ab1e6d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:16:06 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:16:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:16:06 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:16:06 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:16:06 GMT
WORKDIR /app
# Thu, 14 May 2026 17:16:06 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:16:06 GMT
ENV RC_VERSION=8.1.4
# Thu, 14 May 2026 17:17:10 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:17:10 GMT
USER rocketchat
# Thu, 14 May 2026 17:17:11 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:17:11 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:17:11 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:17:11 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa120d095067fb1fe8c2dddb9ad9068fdc2cb7dbf80185512a6829d9eec7ac4`  
		Last Modified: Thu, 14 May 2026 17:17:55 GMT  
		Size: 48.7 MB (48723821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8580e607601141fc40f625728e9bfdb1f9b9afd5a4718d651108fb3b5d5b6706`  
		Last Modified: Thu, 14 May 2026 17:17:53 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445c02735fa80b00b19e90fab4f0bbc50827722560e7f98c3ee87b3eb3fe5daa`  
		Last Modified: Thu, 14 May 2026 17:18:01 GMT  
		Size: 330.5 MB (330508757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:8.1` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:4512ba77216b44bf5a35226136fef5584691ec6120ed030d0fce62860c07dd2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74850f6b9ab0cbd95cd6a979b02ba2b0f0a3f487a1e05a443c2c441e3c0d3b6`

```dockerfile
```

-	Layers:
	-	`sha256:ae4a0e9598c19e079d0293970280993ac07a5dd19d0005506e03620a2ed9647e`  
		Last Modified: Thu, 14 May 2026 17:17:53 GMT  
		Size: 23.1 KB (23060 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:8.1.4`

```console
$ docker pull rocket.chat@sha256:12888c6cf7d7a192020a21a1070e2c7fa9e867751f880a602ce22473c8758a02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:8.1.4` - linux; amd64

```console
$ docker pull rocket.chat@sha256:020990703ce575c91fc058ff8d0070636c48078ddfdeeaa93bc4d13058b7bc41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.1 MB (459112644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60e5d8d53a2bd2cf9803e2ae951f9fc464f99bd46f360d725c10ca69ab1e6d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:16:06 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:16:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:16:06 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:16:06 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:16:06 GMT
WORKDIR /app
# Thu, 14 May 2026 17:16:06 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:16:06 GMT
ENV RC_VERSION=8.1.4
# Thu, 14 May 2026 17:17:10 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:17:10 GMT
USER rocketchat
# Thu, 14 May 2026 17:17:11 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:17:11 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:17:11 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:17:11 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa120d095067fb1fe8c2dddb9ad9068fdc2cb7dbf80185512a6829d9eec7ac4`  
		Last Modified: Thu, 14 May 2026 17:17:55 GMT  
		Size: 48.7 MB (48723821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8580e607601141fc40f625728e9bfdb1f9b9afd5a4718d651108fb3b5d5b6706`  
		Last Modified: Thu, 14 May 2026 17:17:53 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445c02735fa80b00b19e90fab4f0bbc50827722560e7f98c3ee87b3eb3fe5daa`  
		Last Modified: Thu, 14 May 2026 17:18:01 GMT  
		Size: 330.5 MB (330508757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:8.1.4` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:4512ba77216b44bf5a35226136fef5584691ec6120ed030d0fce62860c07dd2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74850f6b9ab0cbd95cd6a979b02ba2b0f0a3f487a1e05a443c2c441e3c0d3b6`

```dockerfile
```

-	Layers:
	-	`sha256:ae4a0e9598c19e079d0293970280993ac07a5dd19d0005506e03620a2ed9647e`  
		Last Modified: Thu, 14 May 2026 17:17:53 GMT  
		Size: 23.1 KB (23060 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:8.2`

```console
$ docker pull rocket.chat@sha256:41b990c1a244ce42e79e6ee71212f50195c73c6d99819556f38ad3d407e30679
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:8.2` - linux; amd64

```console
$ docker pull rocket.chat@sha256:9976dd99cff0747f3d9ea526967bce148624ea404cd476420e552d020c6f1276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.8 MB (474752039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df218f543a062d3723b486a7b0e4c25210716a527613115f81c73941afc4cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:16:02 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:16:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:16:02 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:16:02 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:16:02 GMT
WORKDIR /app
# Thu, 14 May 2026 17:16:02 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:16:02 GMT
ENV RC_VERSION=8.2.3
# Thu, 14 May 2026 17:16:56 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:16:56 GMT
USER rocketchat
# Thu, 14 May 2026 17:16:57 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:16:57 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:16:57 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:16:57 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab9dd9457b5d798737934b3113622b8efcf76699318c2a776f2af3b4fa089db`  
		Last Modified: Thu, 14 May 2026 17:17:42 GMT  
		Size: 48.7 MB (48723790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddcb3944159e47a850cd19c41d545269f78579b522b8f28032bfd50888a72b8`  
		Last Modified: Thu, 14 May 2026 17:17:40 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72a911ce54ade3921029cf0776c93fb7ded9c36baeca75627d2a167c0db3908`  
		Last Modified: Thu, 14 May 2026 17:17:48 GMT  
		Size: 346.1 MB (346148183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:8.2` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:7c05a9136514ae25565d882e6f80dad83a40891e1baffa8deb02d95e952d4b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f2eaceaede5e536e049f76a31a79237fe59ade862a9382e6cb199772ae8f4b`

```dockerfile
```

-	Layers:
	-	`sha256:d7c23ef1c7797d18ce5aabe4787e63dbdefba0092ae3080ce778d65a17e6e137`  
		Last Modified: Thu, 14 May 2026 17:17:40 GMT  
		Size: 23.1 KB (23060 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:8.2.3`

```console
$ docker pull rocket.chat@sha256:41b990c1a244ce42e79e6ee71212f50195c73c6d99819556f38ad3d407e30679
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:8.2.3` - linux; amd64

```console
$ docker pull rocket.chat@sha256:9976dd99cff0747f3d9ea526967bce148624ea404cd476420e552d020c6f1276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.8 MB (474752039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df218f543a062d3723b486a7b0e4c25210716a527613115f81c73941afc4cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:16:02 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:16:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:16:02 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:16:02 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:16:02 GMT
WORKDIR /app
# Thu, 14 May 2026 17:16:02 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:16:02 GMT
ENV RC_VERSION=8.2.3
# Thu, 14 May 2026 17:16:56 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:16:56 GMT
USER rocketchat
# Thu, 14 May 2026 17:16:57 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:16:57 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:16:57 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:16:57 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab9dd9457b5d798737934b3113622b8efcf76699318c2a776f2af3b4fa089db`  
		Last Modified: Thu, 14 May 2026 17:17:42 GMT  
		Size: 48.7 MB (48723790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddcb3944159e47a850cd19c41d545269f78579b522b8f28032bfd50888a72b8`  
		Last Modified: Thu, 14 May 2026 17:17:40 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72a911ce54ade3921029cf0776c93fb7ded9c36baeca75627d2a167c0db3908`  
		Last Modified: Thu, 14 May 2026 17:17:48 GMT  
		Size: 346.1 MB (346148183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:8.2.3` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:7c05a9136514ae25565d882e6f80dad83a40891e1baffa8deb02d95e952d4b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f2eaceaede5e536e049f76a31a79237fe59ade862a9382e6cb199772ae8f4b`

```dockerfile
```

-	Layers:
	-	`sha256:d7c23ef1c7797d18ce5aabe4787e63dbdefba0092ae3080ce778d65a17e6e137`  
		Last Modified: Thu, 14 May 2026 17:17:40 GMT  
		Size: 23.1 KB (23060 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:8.3`

```console
$ docker pull rocket.chat@sha256:85fcfc866031122f12fbebbcad614e4713e1d4f92238c086dbb236aa07e81f39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:8.3` - linux; amd64

```console
$ docker pull rocket.chat@sha256:b1094b76bd59eb507370331cd8f66ee936610b3d05ef170e072a6c3c9954cb24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.4 MB (531356290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d5ea29d524586309cd83ab9711de4121bcf0ee14ea02c2c64dd6f136e72aa9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:15:59 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:15:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:15:59 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:15:59 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:15:59 GMT
WORKDIR /app
# Thu, 14 May 2026 17:15:59 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:15:59 GMT
ENV RC_VERSION=8.3.3
# Thu, 14 May 2026 17:16:53 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:16:53 GMT
USER rocketchat
# Thu, 14 May 2026 17:16:54 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:16:54 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:16:54 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:16:54 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2a19d4ec8ae6789f2ba59fa55205abae65ed72e1d370b37919a783eee8e1b7`  
		Last Modified: Thu, 14 May 2026 17:17:39 GMT  
		Size: 48.7 MB (48723758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f578f3f2fc5edd8956b9e0917f975ade6367baade1acca4717ee419aadd687d8`  
		Last Modified: Thu, 14 May 2026 17:17:37 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5226061e3cf6fed6ea9d9614642e70917a76574aff11a3a2a7ab4bdc02c78bf1`  
		Last Modified: Thu, 14 May 2026 17:17:46 GMT  
		Size: 402.8 MB (402752466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:8.3` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:6a5beeb4518fd59cd337438c398096addadbf4caa8d827dd5c929e0133c13011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411d0efab31adfb444378fff7ea27c78e4acb5544124432a274e2b6242718515`

```dockerfile
```

-	Layers:
	-	`sha256:8f078c260a1f469fca9bfc04562bfbd4ce98c2571adf4d74c78925581598efee`  
		Last Modified: Thu, 14 May 2026 17:17:37 GMT  
		Size: 23.1 KB (23060 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:8.3.3`

```console
$ docker pull rocket.chat@sha256:85fcfc866031122f12fbebbcad614e4713e1d4f92238c086dbb236aa07e81f39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:8.3.3` - linux; amd64

```console
$ docker pull rocket.chat@sha256:b1094b76bd59eb507370331cd8f66ee936610b3d05ef170e072a6c3c9954cb24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.4 MB (531356290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d5ea29d524586309cd83ab9711de4121bcf0ee14ea02c2c64dd6f136e72aa9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:15:59 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:15:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:15:59 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:15:59 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:15:59 GMT
WORKDIR /app
# Thu, 14 May 2026 17:15:59 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:15:59 GMT
ENV RC_VERSION=8.3.3
# Thu, 14 May 2026 17:16:53 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:16:53 GMT
USER rocketchat
# Thu, 14 May 2026 17:16:54 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:16:54 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:16:54 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:16:54 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2a19d4ec8ae6789f2ba59fa55205abae65ed72e1d370b37919a783eee8e1b7`  
		Last Modified: Thu, 14 May 2026 17:17:39 GMT  
		Size: 48.7 MB (48723758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f578f3f2fc5edd8956b9e0917f975ade6367baade1acca4717ee419aadd687d8`  
		Last Modified: Thu, 14 May 2026 17:17:37 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5226061e3cf6fed6ea9d9614642e70917a76574aff11a3a2a7ab4bdc02c78bf1`  
		Last Modified: Thu, 14 May 2026 17:17:46 GMT  
		Size: 402.8 MB (402752466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:8.3.3` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:6a5beeb4518fd59cd337438c398096addadbf4caa8d827dd5c929e0133c13011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411d0efab31adfb444378fff7ea27c78e4acb5544124432a274e2b6242718515`

```dockerfile
```

-	Layers:
	-	`sha256:8f078c260a1f469fca9bfc04562bfbd4ce98c2571adf4d74c78925581598efee`  
		Last Modified: Thu, 14 May 2026 17:17:37 GMT  
		Size: 23.1 KB (23060 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:8.4`

```console
$ docker pull rocket.chat@sha256:5372d4a2eb7d01235661360f48afac3f2ce6e1dbdd66511ec0d7f71b52576254
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:8.4` - linux; amd64

```console
$ docker pull rocket.chat@sha256:9b63ddec180ae8e9f29ab546f279047800aa58476da29dd3f5861fae9f5af413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.3 MB (415286262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3339b1fa003434c5b41b87d1d82de10d7c5ff7434c4d6a5638bb395cf7661b41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:15:58 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:15:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:15:58 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:15:58 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:15:58 GMT
WORKDIR /app
# Thu, 14 May 2026 17:15:58 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:15:58 GMT
ENV RC_VERSION=8.4.1
# Thu, 14 May 2026 17:17:07 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:17:07 GMT
USER rocketchat
# Thu, 14 May 2026 17:17:08 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:17:08 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:17:08 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:17:08 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d29ba0093f68a32f72394af37461f20c9860c52822b542bfed8513b72936ac`  
		Last Modified: Thu, 14 May 2026 17:17:47 GMT  
		Size: 48.7 MB (48723749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6b0997c2b24978e7346f4d6a897b1e9530c0498c6d7c325286d43c0c6c4245`  
		Last Modified: Thu, 14 May 2026 17:17:45 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be49e58ed3bf6a925e3c2453fd20e6186e562c97b7464c5e1f0834e2d6deeac`  
		Last Modified: Thu, 14 May 2026 17:17:52 GMT  
		Size: 286.7 MB (286682449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:8.4` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:6fba49a3990192cfcc9b1c6e3d3395b05461f4d0df710c16c156dcb892fdb5dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102c8c8dbd18cbbad31b0b29932826639bcee03c05c360c67f3acdb672b06fe3`

```dockerfile
```

-	Layers:
	-	`sha256:613df46d5b23176a530883cf41ffa444f234153a99127b7d2064dea12a39bb3b`  
		Last Modified: Thu, 14 May 2026 17:17:44 GMT  
		Size: 23.7 KB (23666 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:8.4.1`

```console
$ docker pull rocket.chat@sha256:5372d4a2eb7d01235661360f48afac3f2ce6e1dbdd66511ec0d7f71b52576254
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:8.4.1` - linux; amd64

```console
$ docker pull rocket.chat@sha256:9b63ddec180ae8e9f29ab546f279047800aa58476da29dd3f5861fae9f5af413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.3 MB (415286262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3339b1fa003434c5b41b87d1d82de10d7c5ff7434c4d6a5638bb395cf7661b41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:15:58 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:15:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:15:58 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:15:58 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:15:58 GMT
WORKDIR /app
# Thu, 14 May 2026 17:15:58 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:15:58 GMT
ENV RC_VERSION=8.4.1
# Thu, 14 May 2026 17:17:07 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:17:07 GMT
USER rocketchat
# Thu, 14 May 2026 17:17:08 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:17:08 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:17:08 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:17:08 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d29ba0093f68a32f72394af37461f20c9860c52822b542bfed8513b72936ac`  
		Last Modified: Thu, 14 May 2026 17:17:47 GMT  
		Size: 48.7 MB (48723749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6b0997c2b24978e7346f4d6a897b1e9530c0498c6d7c325286d43c0c6c4245`  
		Last Modified: Thu, 14 May 2026 17:17:45 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be49e58ed3bf6a925e3c2453fd20e6186e562c97b7464c5e1f0834e2d6deeac`  
		Last Modified: Thu, 14 May 2026 17:17:52 GMT  
		Size: 286.7 MB (286682449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:8.4.1` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:6fba49a3990192cfcc9b1c6e3d3395b05461f4d0df710c16c156dcb892fdb5dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102c8c8dbd18cbbad31b0b29932826639bcee03c05c360c67f3acdb672b06fe3`

```dockerfile
```

-	Layers:
	-	`sha256:613df46d5b23176a530883cf41ffa444f234153a99127b7d2064dea12a39bb3b`  
		Last Modified: Thu, 14 May 2026 17:17:44 GMT  
		Size: 23.7 KB (23666 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:latest`

```console
$ docker pull rocket.chat@sha256:5372d4a2eb7d01235661360f48afac3f2ce6e1dbdd66511ec0d7f71b52576254
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:latest` - linux; amd64

```console
$ docker pull rocket.chat@sha256:9b63ddec180ae8e9f29ab546f279047800aa58476da29dd3f5861fae9f5af413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.3 MB (415286262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3339b1fa003434c5b41b87d1d82de10d7c5ff7434c4d6a5638bb395cf7661b41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 16:57:10 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:57:29 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:57:42 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:57:42 GMT
CMD ["node"]
# Thu, 14 May 2026 17:15:58 GMT
ENV DENO_VERSION=1.43.5
# Thu, 14 May 2026 17:15:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 14 May 2026 17:15:58 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 14 May 2026 17:15:58 GMT
VOLUME [/app/uploads]
# Thu, 14 May 2026 17:15:58 GMT
WORKDIR /app
# Thu, 14 May 2026 17:15:58 GMT
ENV NODE_ENV=production
# Thu, 14 May 2026 17:15:58 GMT
ENV RC_VERSION=8.4.1
# Thu, 14 May 2026 17:17:07 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 14 May 2026 17:17:07 GMT
USER rocketchat
# Thu, 14 May 2026 17:17:08 GMT
WORKDIR /app/bundle
# Thu, 14 May 2026 17:17:08 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 14 May 2026 17:17:08 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 14 May 2026 17:17:08 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6acbc8e716cc5694f625839d460f1dfe85a3030a8a78a229401d90b3998df1`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17245302a67c86a8e0c56fd0d14d0ae2d22118d7b877e7733664cc8f1274fe33`  
		Last Modified: Thu, 14 May 2026 16:57:57 GMT  
		Size: 49.9 MB (49926125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b703c5d9722f593717d3cac6b674658d874128a390845765a355eb888889191`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 1.7 MB (1712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26afb99d23d061f41a5b1411c587ee878d03ac9ab40c54f3de5842ffba5331`  
		Last Modified: Thu, 14 May 2026 16:57:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d29ba0093f68a32f72394af37461f20c9860c52822b542bfed8513b72936ac`  
		Last Modified: Thu, 14 May 2026 17:17:47 GMT  
		Size: 48.7 MB (48723749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6b0997c2b24978e7346f4d6a897b1e9530c0498c6d7c325286d43c0c6c4245`  
		Last Modified: Thu, 14 May 2026 17:17:45 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be49e58ed3bf6a925e3c2453fd20e6186e562c97b7464c5e1f0834e2d6deeac`  
		Last Modified: Thu, 14 May 2026 17:17:52 GMT  
		Size: 286.7 MB (286682449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:latest` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:6fba49a3990192cfcc9b1c6e3d3395b05461f4d0df710c16c156dcb892fdb5dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102c8c8dbd18cbbad31b0b29932826639bcee03c05c360c67f3acdb672b06fe3`

```dockerfile
```

-	Layers:
	-	`sha256:613df46d5b23176a530883cf41ffa444f234153a99127b7d2064dea12a39bb3b`  
		Last Modified: Thu, 14 May 2026 17:17:44 GMT  
		Size: 23.7 KB (23666 bytes)  
		MIME: application/vnd.in-toto+json

<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rocket.chat`

-	[`rocket.chat:7`](#rocketchat7)
-	[`rocket.chat:7.10`](#rocketchat710)
-	[`rocket.chat:7.10.7`](#rocketchat7107)
-	[`rocket.chat:7.11`](#rocketchat711)
-	[`rocket.chat:7.11.3`](#rocketchat7113)
-	[`rocket.chat:7.12`](#rocketchat712)
-	[`rocket.chat:7.12.4`](#rocketchat7124)
-	[`rocket.chat:7.13`](#rocketchat713)
-	[`rocket.chat:7.13.4`](#rocketchat7134)
-	[`rocket.chat:8`](#rocketchat8)
-	[`rocket.chat:8.0`](#rocketchat80)
-	[`rocket.chat:8.0.2`](#rocketchat802)
-	[`rocket.chat:8.1`](#rocketchat81)
-	[`rocket.chat:8.1.1`](#rocketchat811)
-	[`rocket.chat:8.2`](#rocketchat82)
-	[`rocket.chat:8.2.0`](#rocketchat820)
-	[`rocket.chat:latest`](#rocketchatlatest)

## `rocket.chat:7`

```console
$ docker pull rocket.chat@sha256:ce73d73899e82cf3a41907b2c5a541cc7e82bfb6fab5d743bedb9df6a6da6e67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:214d99f2d735d7ccebe14c24549d256e0ba4077d56989db3ccc2ac7a3149bd67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.0 MB (471978885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0610567ba788f52608da35cd6a599a6c25651b14ce3f756a2e54339bb9e43065`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 24 Feb 2026 19:27:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 24 Feb 2026 19:27:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:27:48 GMT
CMD ["node"]
# Thu, 05 Mar 2026 17:49:01 GMT
ENV DENO_VERSION=1.43.5
# Thu, 05 Mar 2026 17:49:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Mar 2026 17:49:02 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 05 Mar 2026 17:49:02 GMT
VOLUME [/app/uploads]
# Thu, 05 Mar 2026 17:49:02 GMT
WORKDIR /app
# Thu, 05 Mar 2026 17:49:02 GMT
ENV NODE_ENV=production
# Thu, 05 Mar 2026 17:49:02 GMT
ENV RC_VERSION=7.13.4
# Thu, 05 Mar 2026 17:50:05 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 05 Mar 2026 17:50:05 GMT
USER rocketchat
# Thu, 05 Mar 2026 17:50:06 GMT
WORKDIR /app/bundle
# Thu, 05 Mar 2026 17:50:06 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 05 Mar 2026 17:50:06 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 05 Mar 2026 17:50:06 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef911690312930412fa6687ed5845b144712e48ec9f731ec2b559df54292b65e`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad6122b53c749b2f4fd187cb01dff4c30c2a3be0865e6ef9f2c62ce9b7ca08`  
		Last Modified: Tue, 24 Feb 2026 19:28:04 GMT  
		Size: 49.5 MB (49472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d84623d331a71d48eb8fe59bfd056b652991559c0aac28197dc29faf3baf7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 1.7 MB (1712639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c136321f37e6f430bac7bea3dab43762845b587e759149b4fc6057c6163fc7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00875cfbdd5a414309a3516aeb47bfafd356e96c0c51f90c179cef6060f45183`  
		Last Modified: Thu, 05 Mar 2026 17:50:50 GMT  
		Size: 48.7 MB (48723730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbd9ea29961c0529455e963d4e49f4bf4659a15fa1c06b554591d63014581c1`  
		Last Modified: Thu, 05 Mar 2026 17:50:48 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f74e8008bfe3453dd56e2208ac00cff3949fe8b268179354f373ae95bbc821`  
		Last Modified: Thu, 05 Mar 2026 17:50:55 GMT  
		Size: 343.8 MB (343828549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:78a5a12a25a1b4e17306fe1598e7014b113ed306d48c1abb6376b4d04d6abb2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 KB (23365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da306b7717bd69191e7c6b616e91141c9fe3857e65b9db3f9ee7ec5fc4cd8342`

```dockerfile
```

-	Layers:
	-	`sha256:0d9a2a38f93d48b4643c11113148ff150b875b7b18754844036aa830629fc987`  
		Last Modified: Thu, 05 Mar 2026 17:50:48 GMT  
		Size: 23.4 KB (23365 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.10`

```console
$ docker pull rocket.chat@sha256:2eea7a93764d24298ced19e1878183ea16950828ffbdbaba53a95915503fd569
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.10` - linux; amd64

```console
$ docker pull rocket.chat@sha256:736240b4ba2c0fba76b9247ecfc8c4538f37f2fe0c8fc2ca02b9987a7c513fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.2 MB (472235754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065a751c4f950e5b353e2fc085884c79888f21e74d038f97d63b5eb101f615a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 24 Feb 2026 19:27:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 24 Feb 2026 19:27:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:27:48 GMT
CMD ["node"]
# Tue, 24 Feb 2026 20:16:46 GMT
ENV DENO_VERSION=1.43.5
# Tue, 24 Feb 2026 20:16:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 20:16:46 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Tue, 24 Feb 2026 20:16:46 GMT
VOLUME [/app/uploads]
# Tue, 24 Feb 2026 20:16:46 GMT
WORKDIR /app
# Tue, 24 Feb 2026 20:16:46 GMT
ENV NODE_ENV=production
# Tue, 24 Feb 2026 20:16:46 GMT
ENV RC_VERSION=7.10.7
# Tue, 24 Feb 2026 20:17:42 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Tue, 24 Feb 2026 20:17:42 GMT
USER rocketchat
# Tue, 24 Feb 2026 20:17:42 GMT
WORKDIR /app/bundle
# Tue, 24 Feb 2026 20:17:42 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Tue, 24 Feb 2026 20:17:42 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 24 Feb 2026 20:17:42 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef911690312930412fa6687ed5845b144712e48ec9f731ec2b559df54292b65e`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad6122b53c749b2f4fd187cb01dff4c30c2a3be0865e6ef9f2c62ce9b7ca08`  
		Last Modified: Tue, 24 Feb 2026 19:28:04 GMT  
		Size: 49.5 MB (49472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d84623d331a71d48eb8fe59bfd056b652991559c0aac28197dc29faf3baf7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 1.7 MB (1712639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c136321f37e6f430bac7bea3dab43762845b587e759149b4fc6057c6163fc7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6122b18591216fccbf0ab85deee16d2c3e0cb29eed1b06814f918ccb31aec95c`  
		Last Modified: Tue, 24 Feb 2026 20:19:48 GMT  
		Size: 48.7 MB (48723734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86ef9b62861cd5c395df8dd5ebf9a68ec9e7f7e50fee262502108449ca4c9fd`  
		Last Modified: Tue, 24 Feb 2026 20:18:33 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd0e520f3afa8c13f01e5a4eb66b69d09c5734c36cc57819f101b4627509e9f`  
		Last Modified: Tue, 24 Feb 2026 20:20:10 GMT  
		Size: 344.1 MB (344085422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.10` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:cd63c41d923e865f09aa21c22a3106d327ef5a9cc46e1332d4fcae8a4a5e462d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126c99d1b63c6317fcc6ab9abc64eb134ad574ed469782a67f705a0985a08066`

```dockerfile
```

-	Layers:
	-	`sha256:6ae8b58d25b95c75e775a2de374066ea22789148edec416c1fab8e41eddb3fa6`  
		Last Modified: Tue, 24 Feb 2026 20:18:32 GMT  
		Size: 23.1 KB (23067 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.10.7`

```console
$ docker pull rocket.chat@sha256:2eea7a93764d24298ced19e1878183ea16950828ffbdbaba53a95915503fd569
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.10.7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:736240b4ba2c0fba76b9247ecfc8c4538f37f2fe0c8fc2ca02b9987a7c513fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.2 MB (472235754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065a751c4f950e5b353e2fc085884c79888f21e74d038f97d63b5eb101f615a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 24 Feb 2026 19:27:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 24 Feb 2026 19:27:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:27:48 GMT
CMD ["node"]
# Tue, 24 Feb 2026 20:16:46 GMT
ENV DENO_VERSION=1.43.5
# Tue, 24 Feb 2026 20:16:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 20:16:46 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Tue, 24 Feb 2026 20:16:46 GMT
VOLUME [/app/uploads]
# Tue, 24 Feb 2026 20:16:46 GMT
WORKDIR /app
# Tue, 24 Feb 2026 20:16:46 GMT
ENV NODE_ENV=production
# Tue, 24 Feb 2026 20:16:46 GMT
ENV RC_VERSION=7.10.7
# Tue, 24 Feb 2026 20:17:42 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Tue, 24 Feb 2026 20:17:42 GMT
USER rocketchat
# Tue, 24 Feb 2026 20:17:42 GMT
WORKDIR /app/bundle
# Tue, 24 Feb 2026 20:17:42 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Tue, 24 Feb 2026 20:17:42 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 24 Feb 2026 20:17:42 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef911690312930412fa6687ed5845b144712e48ec9f731ec2b559df54292b65e`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad6122b53c749b2f4fd187cb01dff4c30c2a3be0865e6ef9f2c62ce9b7ca08`  
		Last Modified: Tue, 24 Feb 2026 19:28:04 GMT  
		Size: 49.5 MB (49472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d84623d331a71d48eb8fe59bfd056b652991559c0aac28197dc29faf3baf7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 1.7 MB (1712639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c136321f37e6f430bac7bea3dab43762845b587e759149b4fc6057c6163fc7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6122b18591216fccbf0ab85deee16d2c3e0cb29eed1b06814f918ccb31aec95c`  
		Last Modified: Tue, 24 Feb 2026 20:19:48 GMT  
		Size: 48.7 MB (48723734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86ef9b62861cd5c395df8dd5ebf9a68ec9e7f7e50fee262502108449ca4c9fd`  
		Last Modified: Tue, 24 Feb 2026 20:18:33 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd0e520f3afa8c13f01e5a4eb66b69d09c5734c36cc57819f101b4627509e9f`  
		Last Modified: Tue, 24 Feb 2026 20:20:10 GMT  
		Size: 344.1 MB (344085422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.10.7` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:cd63c41d923e865f09aa21c22a3106d327ef5a9cc46e1332d4fcae8a4a5e462d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126c99d1b63c6317fcc6ab9abc64eb134ad574ed469782a67f705a0985a08066`

```dockerfile
```

-	Layers:
	-	`sha256:6ae8b58d25b95c75e775a2de374066ea22789148edec416c1fab8e41eddb3fa6`  
		Last Modified: Tue, 24 Feb 2026 20:18:32 GMT  
		Size: 23.1 KB (23067 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.11`

```console
$ docker pull rocket.chat@sha256:e3e30a10994d4993afacabf988333fc9f600eb01b6cdb073baba52f99d766a6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.11` - linux; amd64

```console
$ docker pull rocket.chat@sha256:3418e0f9aa13660782655d6f6dc3e2215120a038da7b86396450bdaeb61f8608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.5 MB (484542429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfdd97369c10f11cdd001c8ce87dced070663207e20fd91914ea49c79073d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 24 Feb 2026 19:27:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 24 Feb 2026 19:27:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:27:48 GMT
CMD ["node"]
# Tue, 24 Feb 2026 20:16:36 GMT
ENV DENO_VERSION=1.43.5
# Tue, 24 Feb 2026 20:16:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 20:16:36 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Tue, 24 Feb 2026 20:16:36 GMT
VOLUME [/app/uploads]
# Tue, 24 Feb 2026 20:16:36 GMT
WORKDIR /app
# Tue, 24 Feb 2026 20:16:36 GMT
ENV NODE_ENV=production
# Tue, 24 Feb 2026 20:16:36 GMT
ENV RC_VERSION=7.11.3
# Tue, 24 Feb 2026 20:17:30 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Tue, 24 Feb 2026 20:17:30 GMT
USER rocketchat
# Tue, 24 Feb 2026 20:17:31 GMT
WORKDIR /app/bundle
# Tue, 24 Feb 2026 20:17:31 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Tue, 24 Feb 2026 20:17:31 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 24 Feb 2026 20:17:31 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef911690312930412fa6687ed5845b144712e48ec9f731ec2b559df54292b65e`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad6122b53c749b2f4fd187cb01dff4c30c2a3be0865e6ef9f2c62ce9b7ca08`  
		Last Modified: Tue, 24 Feb 2026 19:28:04 GMT  
		Size: 49.5 MB (49472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d84623d331a71d48eb8fe59bfd056b652991559c0aac28197dc29faf3baf7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 1.7 MB (1712639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c136321f37e6f430bac7bea3dab43762845b587e759149b4fc6057c6163fc7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d6bfabf756d294624c8c8fde60a96e925632a48dcaf6d178b730e0bda8364c`  
		Last Modified: Tue, 24 Feb 2026 20:18:16 GMT  
		Size: 48.7 MB (48723720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd299e042ef7d083729dadf1f3630bc5b05ffa66e70119a93a7e0287d263397`  
		Last Modified: Tue, 24 Feb 2026 20:18:13 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8494788e0aad1d42d1eb41c68b2c83891fe29d20ab5472da06bbeeec82e2e969`  
		Last Modified: Tue, 24 Feb 2026 20:18:50 GMT  
		Size: 356.4 MB (356392109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.11` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:b912e2fad20ffc86a08b99244e467e8ed1f17072cf97e16018ddb6ad2b869372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf5830297e763d04d5153650bbd5e9f19312b3d5f040f39099fabd6b07c05b2`

```dockerfile
```

-	Layers:
	-	`sha256:ee2fb938acc59feb37ae02dc4f2cac6ca187bd70f7e18667d8f78d05599cbb4d`  
		Last Modified: Tue, 24 Feb 2026 20:18:13 GMT  
		Size: 23.1 KB (23067 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.11.3`

```console
$ docker pull rocket.chat@sha256:e3e30a10994d4993afacabf988333fc9f600eb01b6cdb073baba52f99d766a6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.11.3` - linux; amd64

```console
$ docker pull rocket.chat@sha256:3418e0f9aa13660782655d6f6dc3e2215120a038da7b86396450bdaeb61f8608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.5 MB (484542429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfdd97369c10f11cdd001c8ce87dced070663207e20fd91914ea49c79073d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 24 Feb 2026 19:27:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 24 Feb 2026 19:27:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:27:48 GMT
CMD ["node"]
# Tue, 24 Feb 2026 20:16:36 GMT
ENV DENO_VERSION=1.43.5
# Tue, 24 Feb 2026 20:16:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 20:16:36 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Tue, 24 Feb 2026 20:16:36 GMT
VOLUME [/app/uploads]
# Tue, 24 Feb 2026 20:16:36 GMT
WORKDIR /app
# Tue, 24 Feb 2026 20:16:36 GMT
ENV NODE_ENV=production
# Tue, 24 Feb 2026 20:16:36 GMT
ENV RC_VERSION=7.11.3
# Tue, 24 Feb 2026 20:17:30 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Tue, 24 Feb 2026 20:17:30 GMT
USER rocketchat
# Tue, 24 Feb 2026 20:17:31 GMT
WORKDIR /app/bundle
# Tue, 24 Feb 2026 20:17:31 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Tue, 24 Feb 2026 20:17:31 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 24 Feb 2026 20:17:31 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef911690312930412fa6687ed5845b144712e48ec9f731ec2b559df54292b65e`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad6122b53c749b2f4fd187cb01dff4c30c2a3be0865e6ef9f2c62ce9b7ca08`  
		Last Modified: Tue, 24 Feb 2026 19:28:04 GMT  
		Size: 49.5 MB (49472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d84623d331a71d48eb8fe59bfd056b652991559c0aac28197dc29faf3baf7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 1.7 MB (1712639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c136321f37e6f430bac7bea3dab43762845b587e759149b4fc6057c6163fc7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d6bfabf756d294624c8c8fde60a96e925632a48dcaf6d178b730e0bda8364c`  
		Last Modified: Tue, 24 Feb 2026 20:18:16 GMT  
		Size: 48.7 MB (48723720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd299e042ef7d083729dadf1f3630bc5b05ffa66e70119a93a7e0287d263397`  
		Last Modified: Tue, 24 Feb 2026 20:18:13 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8494788e0aad1d42d1eb41c68b2c83891fe29d20ab5472da06bbeeec82e2e969`  
		Last Modified: Tue, 24 Feb 2026 20:18:50 GMT  
		Size: 356.4 MB (356392109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.11.3` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:b912e2fad20ffc86a08b99244e467e8ed1f17072cf97e16018ddb6ad2b869372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf5830297e763d04d5153650bbd5e9f19312b3d5f040f39099fabd6b07c05b2`

```dockerfile
```

-	Layers:
	-	`sha256:ee2fb938acc59feb37ae02dc4f2cac6ca187bd70f7e18667d8f78d05599cbb4d`  
		Last Modified: Tue, 24 Feb 2026 20:18:13 GMT  
		Size: 23.1 KB (23067 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.12`

```console
$ docker pull rocket.chat@sha256:2a3e11c7ae4f56d3aa989aa6707f1e933712ee0866900330cbb321ed230bd308
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.12` - linux; amd64

```console
$ docker pull rocket.chat@sha256:a3dbc0983ac322d439ab6ebd8cba72b33d23fd90575412f2aaea1e9903eaf107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.7 MB (494706690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173908344109bd94081f4c98c95e027a70b0f1392e45b24cb05bc5726132a4fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 24 Feb 2026 19:27:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 24 Feb 2026 19:27:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:27:48 GMT
CMD ["node"]
# Tue, 24 Feb 2026 20:16:37 GMT
ENV DENO_VERSION=1.43.5
# Tue, 24 Feb 2026 20:16:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 20:16:37 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Tue, 24 Feb 2026 20:16:37 GMT
VOLUME [/app/uploads]
# Tue, 24 Feb 2026 20:16:37 GMT
WORKDIR /app
# Tue, 24 Feb 2026 20:16:37 GMT
ENV NODE_ENV=production
# Tue, 24 Feb 2026 20:16:37 GMT
ENV RC_VERSION=7.12.4
# Tue, 24 Feb 2026 20:17:43 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Tue, 24 Feb 2026 20:17:43 GMT
USER rocketchat
# Tue, 24 Feb 2026 20:17:44 GMT
WORKDIR /app/bundle
# Tue, 24 Feb 2026 20:17:44 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Tue, 24 Feb 2026 20:17:44 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 24 Feb 2026 20:17:44 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef911690312930412fa6687ed5845b144712e48ec9f731ec2b559df54292b65e`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad6122b53c749b2f4fd187cb01dff4c30c2a3be0865e6ef9f2c62ce9b7ca08`  
		Last Modified: Tue, 24 Feb 2026 19:28:04 GMT  
		Size: 49.5 MB (49472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d84623d331a71d48eb8fe59bfd056b652991559c0aac28197dc29faf3baf7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 1.7 MB (1712639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c136321f37e6f430bac7bea3dab43762845b587e759149b4fc6057c6163fc7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b91f24fe9dd238c270537897726cead65e00d391341a665dd24d1fbb1ca0b`  
		Last Modified: Tue, 24 Feb 2026 20:18:36 GMT  
		Size: 48.7 MB (48723795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4074eb82d1be81ea77c434ef7a1b304e0fa84cc803a2156b876e0cf6ef9360ce`  
		Last Modified: Tue, 24 Feb 2026 20:18:34 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9edfeeeb2a9e99629aca9bf1bc91b2a74261412636fe607b5a8d3da96731819`  
		Last Modified: Tue, 24 Feb 2026 20:18:41 GMT  
		Size: 366.6 MB (366556294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.12` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:167622f703891fc005fbc31e73fccb743cc568e4b473b80531df121b6849cd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6c15fd5c9bb0d15db517cf8bfb24d8c44f29ab41872bd3befd8ddd330875d7`

```dockerfile
```

-	Layers:
	-	`sha256:5afb55ab67562c4caa089fd6e7ee7b1bb4b74e744a4a4d6a78b050fb3926c1c2`  
		Last Modified: Tue, 24 Feb 2026 20:18:34 GMT  
		Size: 23.1 KB (23067 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.12.4`

```console
$ docker pull rocket.chat@sha256:2a3e11c7ae4f56d3aa989aa6707f1e933712ee0866900330cbb321ed230bd308
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.12.4` - linux; amd64

```console
$ docker pull rocket.chat@sha256:a3dbc0983ac322d439ab6ebd8cba72b33d23fd90575412f2aaea1e9903eaf107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.7 MB (494706690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173908344109bd94081f4c98c95e027a70b0f1392e45b24cb05bc5726132a4fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 24 Feb 2026 19:27:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 24 Feb 2026 19:27:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:27:48 GMT
CMD ["node"]
# Tue, 24 Feb 2026 20:16:37 GMT
ENV DENO_VERSION=1.43.5
# Tue, 24 Feb 2026 20:16:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 20:16:37 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Tue, 24 Feb 2026 20:16:37 GMT
VOLUME [/app/uploads]
# Tue, 24 Feb 2026 20:16:37 GMT
WORKDIR /app
# Tue, 24 Feb 2026 20:16:37 GMT
ENV NODE_ENV=production
# Tue, 24 Feb 2026 20:16:37 GMT
ENV RC_VERSION=7.12.4
# Tue, 24 Feb 2026 20:17:43 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Tue, 24 Feb 2026 20:17:43 GMT
USER rocketchat
# Tue, 24 Feb 2026 20:17:44 GMT
WORKDIR /app/bundle
# Tue, 24 Feb 2026 20:17:44 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Tue, 24 Feb 2026 20:17:44 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 24 Feb 2026 20:17:44 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef911690312930412fa6687ed5845b144712e48ec9f731ec2b559df54292b65e`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad6122b53c749b2f4fd187cb01dff4c30c2a3be0865e6ef9f2c62ce9b7ca08`  
		Last Modified: Tue, 24 Feb 2026 19:28:04 GMT  
		Size: 49.5 MB (49472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d84623d331a71d48eb8fe59bfd056b652991559c0aac28197dc29faf3baf7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 1.7 MB (1712639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c136321f37e6f430bac7bea3dab43762845b587e759149b4fc6057c6163fc7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b91f24fe9dd238c270537897726cead65e00d391341a665dd24d1fbb1ca0b`  
		Last Modified: Tue, 24 Feb 2026 20:18:36 GMT  
		Size: 48.7 MB (48723795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4074eb82d1be81ea77c434ef7a1b304e0fa84cc803a2156b876e0cf6ef9360ce`  
		Last Modified: Tue, 24 Feb 2026 20:18:34 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9edfeeeb2a9e99629aca9bf1bc91b2a74261412636fe607b5a8d3da96731819`  
		Last Modified: Tue, 24 Feb 2026 20:18:41 GMT  
		Size: 366.6 MB (366556294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.12.4` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:167622f703891fc005fbc31e73fccb743cc568e4b473b80531df121b6849cd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6c15fd5c9bb0d15db517cf8bfb24d8c44f29ab41872bd3befd8ddd330875d7`

```dockerfile
```

-	Layers:
	-	`sha256:5afb55ab67562c4caa089fd6e7ee7b1bb4b74e744a4a4d6a78b050fb3926c1c2`  
		Last Modified: Tue, 24 Feb 2026 20:18:34 GMT  
		Size: 23.1 KB (23067 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.13`

```console
$ docker pull rocket.chat@sha256:ce73d73899e82cf3a41907b2c5a541cc7e82bfb6fab5d743bedb9df6a6da6e67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.13` - linux; amd64

```console
$ docker pull rocket.chat@sha256:214d99f2d735d7ccebe14c24549d256e0ba4077d56989db3ccc2ac7a3149bd67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.0 MB (471978885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0610567ba788f52608da35cd6a599a6c25651b14ce3f756a2e54339bb9e43065`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 24 Feb 2026 19:27:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 24 Feb 2026 19:27:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:27:48 GMT
CMD ["node"]
# Thu, 05 Mar 2026 17:49:01 GMT
ENV DENO_VERSION=1.43.5
# Thu, 05 Mar 2026 17:49:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Mar 2026 17:49:02 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 05 Mar 2026 17:49:02 GMT
VOLUME [/app/uploads]
# Thu, 05 Mar 2026 17:49:02 GMT
WORKDIR /app
# Thu, 05 Mar 2026 17:49:02 GMT
ENV NODE_ENV=production
# Thu, 05 Mar 2026 17:49:02 GMT
ENV RC_VERSION=7.13.4
# Thu, 05 Mar 2026 17:50:05 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 05 Mar 2026 17:50:05 GMT
USER rocketchat
# Thu, 05 Mar 2026 17:50:06 GMT
WORKDIR /app/bundle
# Thu, 05 Mar 2026 17:50:06 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 05 Mar 2026 17:50:06 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 05 Mar 2026 17:50:06 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef911690312930412fa6687ed5845b144712e48ec9f731ec2b559df54292b65e`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad6122b53c749b2f4fd187cb01dff4c30c2a3be0865e6ef9f2c62ce9b7ca08`  
		Last Modified: Tue, 24 Feb 2026 19:28:04 GMT  
		Size: 49.5 MB (49472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d84623d331a71d48eb8fe59bfd056b652991559c0aac28197dc29faf3baf7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 1.7 MB (1712639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c136321f37e6f430bac7bea3dab43762845b587e759149b4fc6057c6163fc7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00875cfbdd5a414309a3516aeb47bfafd356e96c0c51f90c179cef6060f45183`  
		Last Modified: Thu, 05 Mar 2026 17:50:50 GMT  
		Size: 48.7 MB (48723730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbd9ea29961c0529455e963d4e49f4bf4659a15fa1c06b554591d63014581c1`  
		Last Modified: Thu, 05 Mar 2026 17:50:48 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f74e8008bfe3453dd56e2208ac00cff3949fe8b268179354f373ae95bbc821`  
		Last Modified: Thu, 05 Mar 2026 17:50:55 GMT  
		Size: 343.8 MB (343828549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.13` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:78a5a12a25a1b4e17306fe1598e7014b113ed306d48c1abb6376b4d04d6abb2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 KB (23365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da306b7717bd69191e7c6b616e91141c9fe3857e65b9db3f9ee7ec5fc4cd8342`

```dockerfile
```

-	Layers:
	-	`sha256:0d9a2a38f93d48b4643c11113148ff150b875b7b18754844036aa830629fc987`  
		Last Modified: Thu, 05 Mar 2026 17:50:48 GMT  
		Size: 23.4 KB (23365 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:7.13.4`

```console
$ docker pull rocket.chat@sha256:ce73d73899e82cf3a41907b2c5a541cc7e82bfb6fab5d743bedb9df6a6da6e67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:7.13.4` - linux; amd64

```console
$ docker pull rocket.chat@sha256:214d99f2d735d7ccebe14c24549d256e0ba4077d56989db3ccc2ac7a3149bd67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.0 MB (471978885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0610567ba788f52608da35cd6a599a6c25651b14ce3f756a2e54339bb9e43065`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 24 Feb 2026 19:27:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 24 Feb 2026 19:27:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:27:48 GMT
CMD ["node"]
# Thu, 05 Mar 2026 17:49:01 GMT
ENV DENO_VERSION=1.43.5
# Thu, 05 Mar 2026 17:49:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Mar 2026 17:49:02 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 05 Mar 2026 17:49:02 GMT
VOLUME [/app/uploads]
# Thu, 05 Mar 2026 17:49:02 GMT
WORKDIR /app
# Thu, 05 Mar 2026 17:49:02 GMT
ENV NODE_ENV=production
# Thu, 05 Mar 2026 17:49:02 GMT
ENV RC_VERSION=7.13.4
# Thu, 05 Mar 2026 17:50:05 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 05 Mar 2026 17:50:05 GMT
USER rocketchat
# Thu, 05 Mar 2026 17:50:06 GMT
WORKDIR /app/bundle
# Thu, 05 Mar 2026 17:50:06 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 05 Mar 2026 17:50:06 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 05 Mar 2026 17:50:06 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef911690312930412fa6687ed5845b144712e48ec9f731ec2b559df54292b65e`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad6122b53c749b2f4fd187cb01dff4c30c2a3be0865e6ef9f2c62ce9b7ca08`  
		Last Modified: Tue, 24 Feb 2026 19:28:04 GMT  
		Size: 49.5 MB (49472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d84623d331a71d48eb8fe59bfd056b652991559c0aac28197dc29faf3baf7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 1.7 MB (1712639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c136321f37e6f430bac7bea3dab43762845b587e759149b4fc6057c6163fc7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00875cfbdd5a414309a3516aeb47bfafd356e96c0c51f90c179cef6060f45183`  
		Last Modified: Thu, 05 Mar 2026 17:50:50 GMT  
		Size: 48.7 MB (48723730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbd9ea29961c0529455e963d4e49f4bf4659a15fa1c06b554591d63014581c1`  
		Last Modified: Thu, 05 Mar 2026 17:50:48 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f74e8008bfe3453dd56e2208ac00cff3949fe8b268179354f373ae95bbc821`  
		Last Modified: Thu, 05 Mar 2026 17:50:55 GMT  
		Size: 343.8 MB (343828549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:7.13.4` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:78a5a12a25a1b4e17306fe1598e7014b113ed306d48c1abb6376b4d04d6abb2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 KB (23365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da306b7717bd69191e7c6b616e91141c9fe3857e65b9db3f9ee7ec5fc4cd8342`

```dockerfile
```

-	Layers:
	-	`sha256:0d9a2a38f93d48b4643c11113148ff150b875b7b18754844036aa830629fc987`  
		Last Modified: Thu, 05 Mar 2026 17:50:48 GMT  
		Size: 23.4 KB (23365 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:8`

```console
$ docker pull rocket.chat@sha256:14d59bec3de4ed3d7cdacc70d737462915d9f841680ed5cb56a39ee645c3ebcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:8` - linux; amd64

```console
$ docker pull rocket.chat@sha256:21874737a333bb5a08b04d111676ebea7024165f5c92fc8058170f44fed40d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.6 MB (459596805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6261e257c469d198ab3aa5ff93135ff102fb47bd3c552f7cc37a0a3cfdbe5fbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 24 Feb 2026 19:27:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 24 Feb 2026 19:27:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:27:48 GMT
CMD ["node"]
# Thu, 05 Mar 2026 17:47:22 GMT
ENV DENO_VERSION=1.43.5
# Thu, 05 Mar 2026 17:47:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Mar 2026 17:47:23 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 05 Mar 2026 17:47:23 GMT
VOLUME [/app/uploads]
# Thu, 05 Mar 2026 17:47:23 GMT
WORKDIR /app
# Thu, 05 Mar 2026 17:47:23 GMT
ENV NODE_ENV=production
# Thu, 05 Mar 2026 17:47:23 GMT
ENV RC_VERSION=8.2.0
# Thu, 05 Mar 2026 17:48:25 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 05 Mar 2026 17:48:25 GMT
USER rocketchat
# Thu, 05 Mar 2026 17:48:26 GMT
WORKDIR /app/bundle
# Thu, 05 Mar 2026 17:48:26 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 05 Mar 2026 17:48:26 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 05 Mar 2026 17:48:26 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef911690312930412fa6687ed5845b144712e48ec9f731ec2b559df54292b65e`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad6122b53c749b2f4fd187cb01dff4c30c2a3be0865e6ef9f2c62ce9b7ca08`  
		Last Modified: Tue, 24 Feb 2026 19:28:04 GMT  
		Size: 49.5 MB (49472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d84623d331a71d48eb8fe59bfd056b652991559c0aac28197dc29faf3baf7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 1.7 MB (1712639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c136321f37e6f430bac7bea3dab43762845b587e759149b4fc6057c6163fc7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff7f994ce8f542e9b5f936ca4075f8140361c9cba04e40d0034690ed90a6e54`  
		Last Modified: Thu, 05 Mar 2026 17:49:10 GMT  
		Size: 48.7 MB (48723815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea49161d3e45f4a137c00156934f382ea8581d5f9d1111f65db604c50014997`  
		Last Modified: Thu, 05 Mar 2026 17:49:08 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab534160a871c9f0948890b82e036eb531ac496d75a9b47ab9edae50e663ca3`  
		Last Modified: Thu, 05 Mar 2026 17:49:15 GMT  
		Size: 331.4 MB (331446386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:8` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:f72b60673f4c66299674276fcc986f6369e84883a1887d8dcc3c2535df42d953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935cb684dedabb8fa2c979f7c1878d8078468e3df97755e7fc5ce38a3a5fd24f`

```dockerfile
```

-	Layers:
	-	`sha256:c85a70d8ef01098ab72e38ea75d114105aa0e30ac6dfe49db6572fde307397bf`  
		Last Modified: Thu, 05 Mar 2026 17:49:07 GMT  
		Size: 23.7 KB (23665 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:8.0`

```console
$ docker pull rocket.chat@sha256:f79e343d1d494db7cf945dd31ee1d76540683ac854cfc557cc6bae0ca3eb3922
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:8.0` - linux; amd64

```console
$ docker pull rocket.chat@sha256:79536e2876700e8bd5d5e91b4ae25df9143fcc7662654fc0659709d6bb159410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.3 MB (458311640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b9d1459d37b4030e08ff0567cd172d028d06dee5839c8250a53bcfa233ee22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 24 Feb 2026 19:27:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 24 Feb 2026 19:27:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:27:48 GMT
CMD ["node"]
# Thu, 05 Mar 2026 17:47:38 GMT
ENV DENO_VERSION=1.43.5
# Thu, 05 Mar 2026 17:47:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Mar 2026 17:47:38 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 05 Mar 2026 17:47:38 GMT
VOLUME [/app/uploads]
# Thu, 05 Mar 2026 17:47:38 GMT
WORKDIR /app
# Thu, 05 Mar 2026 17:47:38 GMT
ENV NODE_ENV=production
# Thu, 05 Mar 2026 17:47:38 GMT
ENV RC_VERSION=8.0.2
# Thu, 05 Mar 2026 17:48:35 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 05 Mar 2026 17:48:35 GMT
USER rocketchat
# Thu, 05 Mar 2026 17:48:36 GMT
WORKDIR /app/bundle
# Thu, 05 Mar 2026 17:48:36 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 05 Mar 2026 17:48:36 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 05 Mar 2026 17:48:36 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef911690312930412fa6687ed5845b144712e48ec9f731ec2b559df54292b65e`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad6122b53c749b2f4fd187cb01dff4c30c2a3be0865e6ef9f2c62ce9b7ca08`  
		Last Modified: Tue, 24 Feb 2026 19:28:04 GMT  
		Size: 49.5 MB (49472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d84623d331a71d48eb8fe59bfd056b652991559c0aac28197dc29faf3baf7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 1.7 MB (1712639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c136321f37e6f430bac7bea3dab43762845b587e759149b4fc6057c6163fc7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d881e90390f4c93a5b354ea424b58279d944bfd5e94ec75730b4c496bb3952a`  
		Last Modified: Thu, 05 Mar 2026 17:49:20 GMT  
		Size: 48.7 MB (48723738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1514071a8637b034410357884f5f1d8c18520f19aa2806a899aa48e1d5ee21c8`  
		Last Modified: Thu, 05 Mar 2026 17:49:18 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942da3e860264daa92d0f238af9174dc22d451c27e4f1725c3bec7fa21769f8`  
		Last Modified: Thu, 05 Mar 2026 17:49:30 GMT  
		Size: 330.2 MB (330161298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:8.0` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:7373324e741218001d92dd89ad5f828a920e67a3a272b9c78fa589f810736b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f13f50de8a547f903d8431e6c32afcb6621a9a9914e5171ce3b609c02a3a86`

```dockerfile
```

-	Layers:
	-	`sha256:2e688926484446541f2c06f8f667bf3dded0cb9332e6a3594e2d854b0cc4c7cd`  
		Last Modified: Thu, 05 Mar 2026 17:49:18 GMT  
		Size: 23.1 KB (23060 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:8.0.2`

```console
$ docker pull rocket.chat@sha256:f79e343d1d494db7cf945dd31ee1d76540683ac854cfc557cc6bae0ca3eb3922
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:8.0.2` - linux; amd64

```console
$ docker pull rocket.chat@sha256:79536e2876700e8bd5d5e91b4ae25df9143fcc7662654fc0659709d6bb159410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.3 MB (458311640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b9d1459d37b4030e08ff0567cd172d028d06dee5839c8250a53bcfa233ee22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 24 Feb 2026 19:27:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 24 Feb 2026 19:27:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:27:48 GMT
CMD ["node"]
# Thu, 05 Mar 2026 17:47:38 GMT
ENV DENO_VERSION=1.43.5
# Thu, 05 Mar 2026 17:47:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Mar 2026 17:47:38 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 05 Mar 2026 17:47:38 GMT
VOLUME [/app/uploads]
# Thu, 05 Mar 2026 17:47:38 GMT
WORKDIR /app
# Thu, 05 Mar 2026 17:47:38 GMT
ENV NODE_ENV=production
# Thu, 05 Mar 2026 17:47:38 GMT
ENV RC_VERSION=8.0.2
# Thu, 05 Mar 2026 17:48:35 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 05 Mar 2026 17:48:35 GMT
USER rocketchat
# Thu, 05 Mar 2026 17:48:36 GMT
WORKDIR /app/bundle
# Thu, 05 Mar 2026 17:48:36 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 05 Mar 2026 17:48:36 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 05 Mar 2026 17:48:36 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef911690312930412fa6687ed5845b144712e48ec9f731ec2b559df54292b65e`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad6122b53c749b2f4fd187cb01dff4c30c2a3be0865e6ef9f2c62ce9b7ca08`  
		Last Modified: Tue, 24 Feb 2026 19:28:04 GMT  
		Size: 49.5 MB (49472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d84623d331a71d48eb8fe59bfd056b652991559c0aac28197dc29faf3baf7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 1.7 MB (1712639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c136321f37e6f430bac7bea3dab43762845b587e759149b4fc6057c6163fc7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d881e90390f4c93a5b354ea424b58279d944bfd5e94ec75730b4c496bb3952a`  
		Last Modified: Thu, 05 Mar 2026 17:49:20 GMT  
		Size: 48.7 MB (48723738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1514071a8637b034410357884f5f1d8c18520f19aa2806a899aa48e1d5ee21c8`  
		Last Modified: Thu, 05 Mar 2026 17:49:18 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942da3e860264daa92d0f238af9174dc22d451c27e4f1725c3bec7fa21769f8`  
		Last Modified: Thu, 05 Mar 2026 17:49:30 GMT  
		Size: 330.2 MB (330161298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:8.0.2` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:7373324e741218001d92dd89ad5f828a920e67a3a272b9c78fa589f810736b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f13f50de8a547f903d8431e6c32afcb6621a9a9914e5171ce3b609c02a3a86`

```dockerfile
```

-	Layers:
	-	`sha256:2e688926484446541f2c06f8f667bf3dded0cb9332e6a3594e2d854b0cc4c7cd`  
		Last Modified: Thu, 05 Mar 2026 17:49:18 GMT  
		Size: 23.1 KB (23060 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:8.1`

```console
$ docker pull rocket.chat@sha256:842ffa44db378fb056c8ab614d524e911985fc9e795979021700402ddd6c40af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:8.1` - linux; amd64

```console
$ docker pull rocket.chat@sha256:e719f010f53d76b116dc15d997e57c4187b3b82cdf8182013350822afad5336d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.9 MB (458912365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d7caa159a51937197f215af73cfadd878321220241e35bd61acccbd5a30a3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 24 Feb 2026 19:27:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 24 Feb 2026 19:27:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:27:48 GMT
CMD ["node"]
# Tue, 24 Feb 2026 20:16:27 GMT
ENV DENO_VERSION=1.43.5
# Tue, 24 Feb 2026 20:16:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 20:16:28 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Tue, 24 Feb 2026 20:16:28 GMT
VOLUME [/app/uploads]
# Tue, 24 Feb 2026 20:16:28 GMT
WORKDIR /app
# Tue, 24 Feb 2026 20:16:28 GMT
ENV NODE_ENV=production
# Tue, 24 Feb 2026 20:16:28 GMT
ENV RC_VERSION=8.1.1
# Tue, 24 Feb 2026 20:17:28 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Tue, 24 Feb 2026 20:17:28 GMT
USER rocketchat
# Tue, 24 Feb 2026 20:17:28 GMT
WORKDIR /app/bundle
# Tue, 24 Feb 2026 20:17:28 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Tue, 24 Feb 2026 20:17:28 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 24 Feb 2026 20:17:28 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef911690312930412fa6687ed5845b144712e48ec9f731ec2b559df54292b65e`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad6122b53c749b2f4fd187cb01dff4c30c2a3be0865e6ef9f2c62ce9b7ca08`  
		Last Modified: Tue, 24 Feb 2026 19:28:04 GMT  
		Size: 49.5 MB (49472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d84623d331a71d48eb8fe59bfd056b652991559c0aac28197dc29faf3baf7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 1.7 MB (1712639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c136321f37e6f430bac7bea3dab43762845b587e759149b4fc6057c6163fc7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeebe0958e79202ce2e5c4b1597a0ecffa1df3fe994d2c44a69037f40a263d68`  
		Last Modified: Tue, 24 Feb 2026 20:18:08 GMT  
		Size: 48.7 MB (48723745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e55f7262f24ea415ade17524c24ce834f76c721560634cf099d4b3e1783c9a6`  
		Last Modified: Tue, 24 Feb 2026 20:18:05 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c036770e555ca8bbe9bd6c735cce7bab512ef799c9aa324f7e6cefe549d2f011`  
		Last Modified: Tue, 24 Feb 2026 20:18:19 GMT  
		Size: 330.8 MB (330762020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:8.1` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:5374c8271c750459577ac3f8383aae38d865f8ae21240ba8b60ec9f49a4ea1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899eae80129590e040d7ff6edbf22d795779bc7a50f8f1cd57bdd5a39004ab5d`

```dockerfile
```

-	Layers:
	-	`sha256:ccb619d57c33c3f60951db842ac64044365f1cf5beadc350895fade934b01df5`  
		Last Modified: Tue, 24 Feb 2026 20:18:05 GMT  
		Size: 23.7 KB (23666 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:8.1.1`

```console
$ docker pull rocket.chat@sha256:842ffa44db378fb056c8ab614d524e911985fc9e795979021700402ddd6c40af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:8.1.1` - linux; amd64

```console
$ docker pull rocket.chat@sha256:e719f010f53d76b116dc15d997e57c4187b3b82cdf8182013350822afad5336d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.9 MB (458912365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d7caa159a51937197f215af73cfadd878321220241e35bd61acccbd5a30a3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 24 Feb 2026 19:27:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 24 Feb 2026 19:27:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:27:48 GMT
CMD ["node"]
# Tue, 24 Feb 2026 20:16:27 GMT
ENV DENO_VERSION=1.43.5
# Tue, 24 Feb 2026 20:16:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 20:16:28 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Tue, 24 Feb 2026 20:16:28 GMT
VOLUME [/app/uploads]
# Tue, 24 Feb 2026 20:16:28 GMT
WORKDIR /app
# Tue, 24 Feb 2026 20:16:28 GMT
ENV NODE_ENV=production
# Tue, 24 Feb 2026 20:16:28 GMT
ENV RC_VERSION=8.1.1
# Tue, 24 Feb 2026 20:17:28 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Tue, 24 Feb 2026 20:17:28 GMT
USER rocketchat
# Tue, 24 Feb 2026 20:17:28 GMT
WORKDIR /app/bundle
# Tue, 24 Feb 2026 20:17:28 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Tue, 24 Feb 2026 20:17:28 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 24 Feb 2026 20:17:28 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef911690312930412fa6687ed5845b144712e48ec9f731ec2b559df54292b65e`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad6122b53c749b2f4fd187cb01dff4c30c2a3be0865e6ef9f2c62ce9b7ca08`  
		Last Modified: Tue, 24 Feb 2026 19:28:04 GMT  
		Size: 49.5 MB (49472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d84623d331a71d48eb8fe59bfd056b652991559c0aac28197dc29faf3baf7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 1.7 MB (1712639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c136321f37e6f430bac7bea3dab43762845b587e759149b4fc6057c6163fc7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeebe0958e79202ce2e5c4b1597a0ecffa1df3fe994d2c44a69037f40a263d68`  
		Last Modified: Tue, 24 Feb 2026 20:18:08 GMT  
		Size: 48.7 MB (48723745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e55f7262f24ea415ade17524c24ce834f76c721560634cf099d4b3e1783c9a6`  
		Last Modified: Tue, 24 Feb 2026 20:18:05 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c036770e555ca8bbe9bd6c735cce7bab512ef799c9aa324f7e6cefe549d2f011`  
		Last Modified: Tue, 24 Feb 2026 20:18:19 GMT  
		Size: 330.8 MB (330762020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:8.1.1` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:5374c8271c750459577ac3f8383aae38d865f8ae21240ba8b60ec9f49a4ea1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899eae80129590e040d7ff6edbf22d795779bc7a50f8f1cd57bdd5a39004ab5d`

```dockerfile
```

-	Layers:
	-	`sha256:ccb619d57c33c3f60951db842ac64044365f1cf5beadc350895fade934b01df5`  
		Last Modified: Tue, 24 Feb 2026 20:18:05 GMT  
		Size: 23.7 KB (23666 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:8.2`

```console
$ docker pull rocket.chat@sha256:14d59bec3de4ed3d7cdacc70d737462915d9f841680ed5cb56a39ee645c3ebcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:8.2` - linux; amd64

```console
$ docker pull rocket.chat@sha256:21874737a333bb5a08b04d111676ebea7024165f5c92fc8058170f44fed40d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.6 MB (459596805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6261e257c469d198ab3aa5ff93135ff102fb47bd3c552f7cc37a0a3cfdbe5fbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 24 Feb 2026 19:27:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 24 Feb 2026 19:27:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:27:48 GMT
CMD ["node"]
# Thu, 05 Mar 2026 17:47:22 GMT
ENV DENO_VERSION=1.43.5
# Thu, 05 Mar 2026 17:47:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Mar 2026 17:47:23 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 05 Mar 2026 17:47:23 GMT
VOLUME [/app/uploads]
# Thu, 05 Mar 2026 17:47:23 GMT
WORKDIR /app
# Thu, 05 Mar 2026 17:47:23 GMT
ENV NODE_ENV=production
# Thu, 05 Mar 2026 17:47:23 GMT
ENV RC_VERSION=8.2.0
# Thu, 05 Mar 2026 17:48:25 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 05 Mar 2026 17:48:25 GMT
USER rocketchat
# Thu, 05 Mar 2026 17:48:26 GMT
WORKDIR /app/bundle
# Thu, 05 Mar 2026 17:48:26 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 05 Mar 2026 17:48:26 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 05 Mar 2026 17:48:26 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef911690312930412fa6687ed5845b144712e48ec9f731ec2b559df54292b65e`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad6122b53c749b2f4fd187cb01dff4c30c2a3be0865e6ef9f2c62ce9b7ca08`  
		Last Modified: Tue, 24 Feb 2026 19:28:04 GMT  
		Size: 49.5 MB (49472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d84623d331a71d48eb8fe59bfd056b652991559c0aac28197dc29faf3baf7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 1.7 MB (1712639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c136321f37e6f430bac7bea3dab43762845b587e759149b4fc6057c6163fc7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff7f994ce8f542e9b5f936ca4075f8140361c9cba04e40d0034690ed90a6e54`  
		Last Modified: Thu, 05 Mar 2026 17:49:10 GMT  
		Size: 48.7 MB (48723815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea49161d3e45f4a137c00156934f382ea8581d5f9d1111f65db604c50014997`  
		Last Modified: Thu, 05 Mar 2026 17:49:08 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab534160a871c9f0948890b82e036eb531ac496d75a9b47ab9edae50e663ca3`  
		Last Modified: Thu, 05 Mar 2026 17:49:15 GMT  
		Size: 331.4 MB (331446386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:8.2` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:f72b60673f4c66299674276fcc986f6369e84883a1887d8dcc3c2535df42d953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935cb684dedabb8fa2c979f7c1878d8078468e3df97755e7fc5ce38a3a5fd24f`

```dockerfile
```

-	Layers:
	-	`sha256:c85a70d8ef01098ab72e38ea75d114105aa0e30ac6dfe49db6572fde307397bf`  
		Last Modified: Thu, 05 Mar 2026 17:49:07 GMT  
		Size: 23.7 KB (23665 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:8.2.0`

```console
$ docker pull rocket.chat@sha256:14d59bec3de4ed3d7cdacc70d737462915d9f841680ed5cb56a39ee645c3ebcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:8.2.0` - linux; amd64

```console
$ docker pull rocket.chat@sha256:21874737a333bb5a08b04d111676ebea7024165f5c92fc8058170f44fed40d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.6 MB (459596805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6261e257c469d198ab3aa5ff93135ff102fb47bd3c552f7cc37a0a3cfdbe5fbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 24 Feb 2026 19:27:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 24 Feb 2026 19:27:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:27:48 GMT
CMD ["node"]
# Thu, 05 Mar 2026 17:47:22 GMT
ENV DENO_VERSION=1.43.5
# Thu, 05 Mar 2026 17:47:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Mar 2026 17:47:23 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 05 Mar 2026 17:47:23 GMT
VOLUME [/app/uploads]
# Thu, 05 Mar 2026 17:47:23 GMT
WORKDIR /app
# Thu, 05 Mar 2026 17:47:23 GMT
ENV NODE_ENV=production
# Thu, 05 Mar 2026 17:47:23 GMT
ENV RC_VERSION=8.2.0
# Thu, 05 Mar 2026 17:48:25 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 05 Mar 2026 17:48:25 GMT
USER rocketchat
# Thu, 05 Mar 2026 17:48:26 GMT
WORKDIR /app/bundle
# Thu, 05 Mar 2026 17:48:26 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 05 Mar 2026 17:48:26 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 05 Mar 2026 17:48:26 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef911690312930412fa6687ed5845b144712e48ec9f731ec2b559df54292b65e`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad6122b53c749b2f4fd187cb01dff4c30c2a3be0865e6ef9f2c62ce9b7ca08`  
		Last Modified: Tue, 24 Feb 2026 19:28:04 GMT  
		Size: 49.5 MB (49472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d84623d331a71d48eb8fe59bfd056b652991559c0aac28197dc29faf3baf7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 1.7 MB (1712639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c136321f37e6f430bac7bea3dab43762845b587e759149b4fc6057c6163fc7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff7f994ce8f542e9b5f936ca4075f8140361c9cba04e40d0034690ed90a6e54`  
		Last Modified: Thu, 05 Mar 2026 17:49:10 GMT  
		Size: 48.7 MB (48723815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea49161d3e45f4a137c00156934f382ea8581d5f9d1111f65db604c50014997`  
		Last Modified: Thu, 05 Mar 2026 17:49:08 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab534160a871c9f0948890b82e036eb531ac496d75a9b47ab9edae50e663ca3`  
		Last Modified: Thu, 05 Mar 2026 17:49:15 GMT  
		Size: 331.4 MB (331446386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:8.2.0` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:f72b60673f4c66299674276fcc986f6369e84883a1887d8dcc3c2535df42d953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935cb684dedabb8fa2c979f7c1878d8078468e3df97755e7fc5ce38a3a5fd24f`

```dockerfile
```

-	Layers:
	-	`sha256:c85a70d8ef01098ab72e38ea75d114105aa0e30ac6dfe49db6572fde307397bf`  
		Last Modified: Thu, 05 Mar 2026 17:49:07 GMT  
		Size: 23.7 KB (23665 bytes)  
		MIME: application/vnd.in-toto+json

## `rocket.chat:latest`

```console
$ docker pull rocket.chat@sha256:14d59bec3de4ed3d7cdacc70d737462915d9f841680ed5cb56a39ee645c3ebcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rocket.chat:latest` - linux; amd64

```console
$ docker pull rocket.chat@sha256:21874737a333bb5a08b04d111676ebea7024165f5c92fc8058170f44fed40d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.6 MB (459596805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6261e257c469d198ab3aa5ff93135ff102fb47bd3c552f7cc37a0a3cfdbe5fbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV NODE_VERSION=22.22.0
# Tue, 24 Feb 2026 19:27:34 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:34 GMT
ENV YARN_VERSION=1.22.22
# Tue, 24 Feb 2026 19:27:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:27:48 GMT
CMD ["node"]
# Thu, 05 Mar 2026 17:47:22 GMT
ENV DENO_VERSION=1.43.5
# Thu, 05 Mar 2026 17:47:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in   amd64) ARCH='x86_64';;   arm64) ARCH='aarch64';;   *) echo "unsupported Deno architecture"; exit 1 ;;   esac   && set -ex   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl unzip && rm -rf /var/lib/apt/lists/*   && curl -fsSL https://dl.deno.land/release/v${DENO_VERSION}/deno-${ARCH}-unknown-linux-gnu.zip --output /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && echo "246bf818932c5e11adb85afaaf3c90e65d5cbe14bcaa8ea14d35fc085869775d /tmp/deno-x86_64-unknown-linux-gnu.zip" | sha256sum -c -   && unzip /tmp/deno-${ARCH}-unknown-linux-gnu.zip -d /tmp   && rm /tmp/deno-${ARCH}-unknown-linux-gnu.zip   && chmod 755 /tmp/deno   && mv /tmp/deno /usr/local/bin/deno   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Mar 2026 17:47:23 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads # buildkit
# Thu, 05 Mar 2026 17:47:23 GMT
VOLUME [/app/uploads]
# Thu, 05 Mar 2026 17:47:23 GMT
WORKDIR /app
# Thu, 05 Mar 2026 17:47:23 GMT
ENV NODE_ENV=production
# Thu, 05 Mar 2026 17:47:23 GMT
ENV RC_VERSION=8.2.0
# Thu, 05 Mar 2026 17:48:25 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python3 ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install --unsafe-perm=true   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app # buildkit
# Thu, 05 Mar 2026 17:48:25 GMT
USER rocketchat
# Thu, 05 Mar 2026 17:48:26 GMT
WORKDIR /app/bundle
# Thu, 05 Mar 2026 17:48:26 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000
# Thu, 05 Mar 2026 17:48:26 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 05 Mar 2026 17:48:26 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef911690312930412fa6687ed5845b144712e48ec9f731ec2b559df54292b65e`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad6122b53c749b2f4fd187cb01dff4c30c2a3be0865e6ef9f2c62ce9b7ca08`  
		Last Modified: Tue, 24 Feb 2026 19:28:04 GMT  
		Size: 49.5 MB (49472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d84623d331a71d48eb8fe59bfd056b652991559c0aac28197dc29faf3baf7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 1.7 MB (1712639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c136321f37e6f430bac7bea3dab43762845b587e759149b4fc6057c6163fc7`  
		Last Modified: Tue, 24 Feb 2026 19:28:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff7f994ce8f542e9b5f936ca4075f8140361c9cba04e40d0034690ed90a6e54`  
		Last Modified: Thu, 05 Mar 2026 17:49:10 GMT  
		Size: 48.7 MB (48723815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea49161d3e45f4a137c00156934f382ea8581d5f9d1111f65db604c50014997`  
		Last Modified: Thu, 05 Mar 2026 17:49:08 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab534160a871c9f0948890b82e036eb531ac496d75a9b47ab9edae50e663ca3`  
		Last Modified: Thu, 05 Mar 2026 17:49:15 GMT  
		Size: 331.4 MB (331446386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rocket.chat:latest` - unknown; unknown

```console
$ docker pull rocket.chat@sha256:f72b60673f4c66299674276fcc986f6369e84883a1887d8dcc3c2535df42d953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935cb684dedabb8fa2c979f7c1878d8078468e3df97755e7fc5ce38a3a5fd24f`

```dockerfile
```

-	Layers:
	-	`sha256:c85a70d8ef01098ab72e38ea75d114105aa0e30ac6dfe49db6572fde307397bf`  
		Last Modified: Thu, 05 Mar 2026 17:49:07 GMT  
		Size: 23.7 KB (23665 bytes)  
		MIME: application/vnd.in-toto+json

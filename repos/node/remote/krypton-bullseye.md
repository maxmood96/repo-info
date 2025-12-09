## `node:krypton-bullseye`

```console
$ docker pull node@sha256:5583cbe5d3347db372d9a9100eba272b548ca1f53246b9b769334bcd0eef2c26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:krypton-bullseye` - linux; amd64

```console
$ docker pull node@sha256:1e5c6d40b92ab645e5dddbe5b62b1bdf5a64024b5d42ec7e4b1dd323a641b1ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 MB (380653878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93e2d8e74a32e79a9b822733b5624c18a1a1781081cfae4bbf486bf5cd231283`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:07:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:43:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:30:59 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Dec 2025 01:32:00 GMT
ENV NODE_VERSION=24.11.1
# Tue, 09 Dec 2025 01:32:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Dec 2025 01:32:00 GMT
ENV YARN_VERSION=1.22.22
# Tue, 09 Dec 2025 01:32:02 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Dec 2025 01:32:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 01:32:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 01:32:02 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:437b5b60e3a4b64e2c621589a67483eeef6d4b3fc4926655006ef41bd44f71dd`  
		Last Modified: Mon, 08 Dec 2025 22:16:49 GMT  
		Size: 53.8 MB (53756413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291bf09cec80aaf3d13eefc3fba3a6cb13a44cdce91da75e0e2c3d8b72348e79`  
		Last Modified: Mon, 08 Dec 2025 23:07:20 GMT  
		Size: 15.8 MB (15764219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17ff9cfdab33e1021de93428c7968b682c4bb6322df919b3c6622b8ac14ec0b`  
		Last Modified: Tue, 09 Dec 2025 00:06:29 GMT  
		Size: 54.8 MB (54755559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853b40334c538bcc5e2df110b0fecfb8423a3bbe5081982d24d096846277413`  
		Last Modified: Tue, 09 Dec 2025 01:40:24 GMT  
		Size: 197.2 MB (197205872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1973d99d512c75c8f291bb7adaed4af9a51900436bf4f7f06c35b675524471`  
		Last Modified: Tue, 09 Dec 2025 01:31:47 GMT  
		Size: 4.1 KB (4087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d0ca79484509f3fb202de31cd334ddbbc3daf74fbb6667aa1160fd8e951a5a`  
		Last Modified: Tue, 09 Dec 2025 01:32:46 GMT  
		Size: 57.9 MB (57916609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aea37f4cbfed734ea4245e1e440feafb015e68f10ac800016c41dfd70e00ccd`  
		Last Modified: Tue, 09 Dec 2025 01:32:34 GMT  
		Size: 1.3 MB (1250675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7049f0c6d25baef531cb00428a7ed89a06a05faacbe9533e57117bea485af28`  
		Last Modified: Tue, 09 Dec 2025 01:32:33 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:krypton-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:cb754104caefeded05089f602579e9e36e436a2bea9fd431bf942677b16f328d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15773830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31aacf9a56ee68ec6099f526702fdb16b00e0c6268ea3449062c50f238adc77`

```dockerfile
```

-	Layers:
	-	`sha256:eecd1b8647c9e61e6c787fc5051d5efac2c33aae2e77cc70aa06ae0a40521532`  
		Last Modified: Tue, 09 Dec 2025 04:43:22 GMT  
		Size: 15.8 MB (15750770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec388058bad4e1cf768858a32d8960428a8cd3092ddddd528f10f759c212d8d`  
		Last Modified: Tue, 09 Dec 2025 04:43:23 GMT  
		Size: 23.1 KB (23060 bytes)  
		MIME: application/vnd.in-toto+json

### `node:krypton-bullseye` - linux; arm64 variant v8

```console
$ docker pull node@sha256:604589661b8254fa1f6719b2bf3aa1d11a9d059fef9859fea179a358141184fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.2 MB (372172565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a0e0a82d008a0487c8633b20bf8c125d1b93ba96929883ec7bb704287cc3e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:10:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:14:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:20:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Dec 2025 02:21:33 GMT
ENV NODE_VERSION=24.11.1
# Tue, 09 Dec 2025 02:21:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Dec 2025 02:21:33 GMT
ENV YARN_VERSION=1.22.22
# Tue, 09 Dec 2025 02:21:35 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Dec 2025 02:21:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 02:21:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 02:21:35 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:24bca79f74a34f86894c8fcdc6ce8d7dc3c11dd0c76b7e9fa80c7c64df65d166`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 52.3 MB (52257713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b879966726dc963ee08cbddddb10287e93034fcf9e3ddf7a290b1b7e42538c`  
		Last Modified: Mon, 08 Dec 2025 23:10:44 GMT  
		Size: 15.7 MB (15749537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9cd25be3019ce9576369c1d01896d355c209a13773e0054363e0e12e57b0e1`  
		Last Modified: Tue, 09 Dec 2025 00:11:43 GMT  
		Size: 54.9 MB (54866122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8012df9f3f9ffe1b4b7749d91d60381788bf2363eb4b53d656bc467a3673fef5`  
		Last Modified: Tue, 09 Dec 2025 01:15:34 GMT  
		Size: 190.1 MB (190104139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de1ffd48ef02bcb9c96afa9d1785b6664d58e6e3105ad7b616e9364c85ad506`  
		Last Modified: Tue, 09 Dec 2025 02:21:07 GMT  
		Size: 4.1 KB (4085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aedb9d5323af03fd538434cc4b237c6bb9a5c8eb96bfb5d928662382435f30`  
		Last Modified: Tue, 09 Dec 2025 02:22:12 GMT  
		Size: 57.9 MB (57939854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73443cccb7412944a6d339457426ce66b919a0a20d57c8390fdc6ad9965f597e`  
		Last Modified: Tue, 09 Dec 2025 02:22:09 GMT  
		Size: 1.3 MB (1250671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecc9754797e03b5a00a51b4e56bcc7a6f027eb8f3a972e93a01e43c137ae530`  
		Last Modified: Tue, 09 Dec 2025 02:22:09 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:krypton-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:1d2bd9b7aa0966715f856582daac3b3c6c6bc0064eddda87dff8cef3f11e03d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15775957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238dd005d7ee7e83f291a44566a4d7137d38e202ba5f5234f4d4babbadd7a27e`

```dockerfile
```

-	Layers:
	-	`sha256:3d01327608b1388c95ef45dc6342a79b846b30b52272688fabcf77d6081a2f1c`  
		Last Modified: Tue, 09 Dec 2025 04:43:37 GMT  
		Size: 15.8 MB (15752751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cecab2bc01e7612f1a7f63869d33c29ea169709a61db3e564ca4ff2eadd7845b`  
		Last Modified: Tue, 09 Dec 2025 04:43:38 GMT  
		Size: 23.2 KB (23206 bytes)  
		MIME: application/vnd.in-toto+json

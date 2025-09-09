## `node:trixie`

```console
$ docker pull node@sha256:f50080f773a3ac473b4e75f2902a08a8cb8e857d94f6fa113896f664c577dbb4
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

### `node:trixie` - linux; amd64

```console
$ docker pull node@sha256:32ab50b61b2ca2258a491c8cbd7190f9f6d5c428dc25e7ef1860d4fa748f4a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.3 MB (440347999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1ab51edc4786cb533cb7278bd5a2253787467e5abb624b3099a113fa4fd418`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
ENV NODE_VERSION=24.7.0
# Wed, 27 Aug 2025 23:04:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 27 Aug 2025 23:04:59 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Aug 2025 23:04:59 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22718812f617084a0c5e539e02723b75bf79ea2a589430f820efcbb07f45b91b`  
		Last Modified: Mon, 08 Sep 2025 21:55:17 GMT  
		Size: 25.6 MB (25613635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401a98f7495bee3e8e6943da9f52f0ab1043c43eb1d107a3817fc2a4b916be97`  
		Last Modified: Mon, 08 Sep 2025 22:13:47 GMT  
		Size: 67.8 MB (67776756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad446e7df19acd39290d995e6d78ccbfde171596237968a140518b183d94c04f`  
		Last Modified: Mon, 08 Sep 2025 22:39:48 GMT  
		Size: 235.9 MB (235911680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dd200fa1c102e1767b3adab5bd8387bd6420367851f2d90ef6ada8ab606dbf`  
		Last Modified: Mon, 08 Sep 2025 23:21:31 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a717b5e99d98205e7e5afa7cda40b62df9a9bc71096443ade8c46f3dcb0212e9`  
		Last Modified: Tue, 09 Sep 2025 00:42:26 GMT  
		Size: 60.5 MB (60511957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6b137de86a0247d16f95119ebf17eab1da92b3092255ec97751581975a547`  
		Last Modified: Mon, 08 Sep 2025 23:21:36 GMT  
		Size: 1.3 MB (1250674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae6c015231566b047f6e884c73b6a2f1df698e93eabb3d4b022709ac2ae394e`  
		Last Modified: Mon, 08 Sep 2025 23:21:40 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:trixie` - unknown; unknown

```console
$ docker pull node@sha256:d5be3d933b7134c847f93c8565a0384344df194b444256f70f05e13610c16cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17527331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9f358fd4552e5ec2886305c85fa71011b1882648dc8ff1572bb58bcae4b568`

```dockerfile
```

-	Layers:
	-	`sha256:182f30fbdea19f24a315a6fce9a64c248fe0ce04f1f96a6b812806cff8ee4f16`  
		Last Modified: Tue, 09 Sep 2025 00:42:21 GMT  
		Size: 17.5 MB (17504275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f45dc56996e1c5a3a07dc625d2020ed155fc719eefb79879a89d3e09a97fbd9`  
		Last Modified: Tue, 09 Sep 2025 00:42:22 GMT  
		Size: 23.1 KB (23056 bytes)  
		MIME: application/vnd.in-toto+json

### `node:trixie` - linux; arm64 variant v8

```console
$ docker pull node@sha256:16d6e6d924e67af9dc81c90d20efd6e441a3c8854d26df72a09f0b4af3364ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.0 MB (429966980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d23cdfae1e7c624fbb5a3560ed7131348dd2582e57c596f75958f7d5cb4853`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
ENV NODE_VERSION=24.7.0
# Wed, 27 Aug 2025 23:04:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 27 Aug 2025 23:04:59 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Aug 2025 23:04:59 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9923852056eb09462c3344515191318e7aa33ff28057c946bc41a414ee57df0b`  
		Last Modified: Wed, 13 Aug 2025 07:30:07 GMT  
		Size: 25.0 MB (25014610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcc8bff74cbeacbac9c6869b6a9def273b93cc67de196b347688de2a9185de0`  
		Last Modified: Wed, 13 Aug 2025 15:31:50 GMT  
		Size: 67.6 MB (67593628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997d2d68e2fc83df067d8e29a4a06bab06bb202146e47bac816a352ad1d30c04`  
		Last Modified: Wed, 13 Aug 2025 23:52:34 GMT  
		Size: 226.0 MB (226017512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37965d30b3f3b899c074989655ce4860fbaa0361d93145db957ae65bc3396997`  
		Last Modified: Thu, 28 Aug 2025 14:45:10 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29694d62341466e702d61100347c568c95bfe3f17949c2e1016f8ac3f23c5c5f`  
		Last Modified: Thu, 28 Aug 2025 14:45:34 GMT  
		Size: 60.4 MB (60445179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2db39f04009dbfeacddd7ab24fae7e79e08ecba0356f3b2a45ce5a573236e8`  
		Last Modified: Thu, 28 Aug 2025 14:45:10 GMT  
		Size: 1.3 MB (1250673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c387a03e1096f40d45230a60b503149b715cba5e3f028df4ff23d4161de575fa`  
		Last Modified: Thu, 28 Aug 2025 14:45:11 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:trixie` - unknown; unknown

```console
$ docker pull node@sha256:77d1f31a0ab29be3f87c41c8cbe4be798b577e99fc6bcc2afec0bf748c00541f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17606388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a0f85abd27588a6273f88419b925d73c6e3030d92c3fdca9317503e646b350`

```dockerfile
```

-	Layers:
	-	`sha256:fe6e8566ade1b67a33cbe988664acaaf8c19e57e4cc34dd25e1f009f43f406e3`  
		Last Modified: Thu, 28 Aug 2025 15:40:52 GMT  
		Size: 17.6 MB (17583185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c0c291d907b162c83ea841e6fa042e41cb7157e04de9b3604d4c240426ff0cc`  
		Last Modified: Thu, 28 Aug 2025 15:40:53 GMT  
		Size: 23.2 KB (23203 bytes)  
		MIME: application/vnd.in-toto+json

### `node:trixie` - linux; ppc64le

```console
$ docker pull node@sha256:957b21aa07a7ffc6ef2f4e1914cd9b237d4b8e9f9b31a7f9c88a6917cf90367e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.5 MB (448488330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ceafa9117b59d518775c7d3f40e3afb252d3262f5565702adad500f9480b312`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
ENV NODE_VERSION=24.7.0
# Wed, 27 Aug 2025 23:04:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 27 Aug 2025 23:04:59 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Aug 2025 23:04:59 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a327675583423e2c44eae4c02a88be15dbeac36073deb88700ba487e0c0e35`  
		Last Modified: Wed, 13 Aug 2025 15:15:16 GMT  
		Size: 27.0 MB (26992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf20d9e1e5f16d7552d637dd4a12484b22e52928311f81dd13c82b6838c2ae7`  
		Last Modified: Wed, 13 Aug 2025 21:23:59 GMT  
		Size: 73.0 MB (73018659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e609a63b79cb97e868edf62a4c9454838befd7ede70ebc96840a505bc31e1518`  
		Last Modified: Thu, 14 Aug 2025 04:25:41 GMT  
		Size: 231.0 MB (231013234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e0396f415832fde463d0a19268aeda711de665fc2504f2f29a1abeb13c0004`  
		Last Modified: Thu, 28 Aug 2025 13:40:28 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d4101afed963489c83a59d228c1cd542df2e21b8bc7a10c3980cba800e4e8a`  
		Last Modified: Thu, 28 Aug 2025 15:55:11 GMT  
		Size: 63.1 MB (63105734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc96a60e0b8e5416ecdfc103413494343e17088f4555eda442cde253ae0e18a7`  
		Last Modified: Thu, 28 Aug 2025 13:40:41 GMT  
		Size: 1.3 MB (1250676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f438695429a0ddc72b7112c75628aea4e3d88cca05f6890e4ee04bc99349959`  
		Last Modified: Thu, 28 Aug 2025 13:40:27 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:trixie` - unknown; unknown

```console
$ docker pull node@sha256:bf13f4e96246eada18adf5e1936f4fa0d81f27928eb6b6f3c108ad0c1399b219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17507539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f46879e224ca108eee325f713228c6683542359a224972cba32bd92d1df56a`

```dockerfile
```

-	Layers:
	-	`sha256:ba6129381ec82f0517c3560cd6528cb38269a788496b78cebb43b92bba9620a9`  
		Last Modified: Thu, 28 Aug 2025 15:41:14 GMT  
		Size: 17.5 MB (17484428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fadeab35b72d680a7491a174ecc5eef6f397d7e53b9d25725263b47085aa3fa4`  
		Last Modified: Thu, 28 Aug 2025 15:41:15 GMT  
		Size: 23.1 KB (23111 bytes)  
		MIME: application/vnd.in-toto+json

### `node:trixie` - linux; s390x

```console
$ docker pull node@sha256:33a26da33df050321fe04969b9f18e4b539dbe8e362990b8ab81ca323aca8327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.8 MB (411820904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e789c697b4c3b784c6179cd35f65e60abcd7503b56c7312da5e61124f4896a44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
ENV NODE_VERSION=24.7.0
# Wed, 27 Aug 2025 23:04:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 27 Aug 2025 23:04:59 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Aug 2025 23:04:59 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47181ddd75754adfc74e4f58b4a898ec33ad906976b71219b567efd19470677`  
		Last Modified: Wed, 13 Aug 2025 03:27:04 GMT  
		Size: 26.8 MB (26779580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415f63d435cf750f4bda1af6afa07ce9f812fa19c74e6f9f050da85f47eb36e7`  
		Last Modified: Wed, 13 Aug 2025 17:21:16 GMT  
		Size: 68.6 MB (68619998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0559cbb94826f8b1e5c377d0a644ba7cd24eee336fc5523a414d8ad448427fe2`  
		Last Modified: Wed, 13 Aug 2025 17:19:38 GMT  
		Size: 206.4 MB (206400871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefdd16ee47d7ede10c2ec7fc8628b48d5484a7b5375306bd4273bcfb8e3fcf0`  
		Last Modified: Thu, 28 Aug 2025 14:11:08 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca336860d8026b639861302d2305728e8c5b3c93e830462b2f1287ecc00998b`  
		Last Modified: Thu, 28 Aug 2025 15:54:50 GMT  
		Size: 59.4 MB (59420847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e60e568684175cba17926ac6140cff3d27fb8a2ea8c3617f729d017e956e465`  
		Last Modified: Thu, 28 Aug 2025 14:11:12 GMT  
		Size: 1.3 MB (1250674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287802f0557ba433502b1c18c00cd0afbccbf9358b726a9f39c472bb112c596f`  
		Last Modified: Thu, 28 Aug 2025 14:11:20 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:trixie` - unknown; unknown

```console
$ docker pull node@sha256:693fa5d0f7eb104b7b9a1e40838676438360916c82076d41224f2ce2c080e2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17299157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18146ed8cc33531b9ab96bba91389a241f5be67a087abec872af7a5ddb02245`

```dockerfile
```

-	Layers:
	-	`sha256:65f79aa5b9791c314dc89cb8a3b3a092ad601646fcf661454453fa69f29c1edf`  
		Last Modified: Thu, 28 Aug 2025 15:41:29 GMT  
		Size: 17.3 MB (17276100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8887263b202f939b41b7b9df8c5dc0af9233704160ba65980511df03944c4cab`  
		Last Modified: Thu, 28 Aug 2025 15:41:29 GMT  
		Size: 23.1 KB (23057 bytes)  
		MIME: application/vnd.in-toto+json

## `node:bookworm`

```console
$ docker pull node@sha256:b23e4062187077a3b5921ea87412301c10f4d11afc30f913ee622e19529873f1
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

### `node:bookworm` - linux; amd64

```console
$ docker pull node@sha256:761f4cb0b9e5912819e614c1bcda1fe0d19829be4a48d3f6f35df4f055c413c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.1 MB (408063017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe07b8f64dd4a209293f782a117604aa60017030c827f41e09e74256a385110`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENV NODE_VERSION=24.3.0
# Wed, 25 Jun 2025 02:25:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENV YARN_VERSION=1.22.22
# Wed, 25 Jun 2025 02:25:22 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 02:25:22 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe9c1abe6f3b8ca9fc6abe710405f830f95262f1d356e8f6545d823b5840a5c`  
		Last Modified: Tue, 01 Jul 2025 05:12:07 GMT  
		Size: 211.4 MB (211373500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce1b37249dd92d2493f77215adf0e75eb4c3c8ca891eb1dd951021523a52fbe`  
		Last Modified: Tue, 01 Jul 2025 05:14:40 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6ed2269348d2b5e0192514ba2f10d2936cd51acb25391699988f53b884db8`  
		Last Modified: Tue, 01 Jul 2025 05:14:44 GMT  
		Size: 58.5 MB (58520221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5471b55d22e8a9852f936e34df9d8b8a371fd843c5e8e7ae18400893bf7bf249`  
		Last Modified: Tue, 01 Jul 2025 05:14:43 GMT  
		Size: 1.3 MB (1250673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf69e3ecc1c4a732d74464a6b82afef86228e63a345857e1784eee10a5e35cc`  
		Last Modified: Tue, 01 Jul 2025 05:14:40 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:c3f1971763de077c7ae2078890717c2d2888c64f7ff1903c44b6bdfd3e7d6c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16183944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3a12a50b548112e3a02372c174809206db021054e98570d9bd120d058f5d74`

```dockerfile
```

-	Layers:
	-	`sha256:c8949660f7ccba855cfddc415092c37d8cd68683ca15a789acfb1b64c4a3c6b5`  
		Last Modified: Tue, 01 Jul 2025 06:39:44 GMT  
		Size: 16.2 MB (16159827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bc61eaec9bc19e076503155c650483b19dc10614c42308ba7c19e97c031b9bc`  
		Last Modified: Tue, 01 Jul 2025 06:39:45 GMT  
		Size: 24.1 KB (24117 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm` - linux; arm64 variant v8

```console
$ docker pull node@sha256:fc4e99daf8d51dc7a15cee233e84f25a1245400e5fdd85199b59beae30a21653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.3 MB (398277125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e9a34e8bd40d42016e471ce3aaa0a2bbbf826ea618ee62b3a852e393e06824`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENV NODE_VERSION=24.3.0
# Wed, 25 Jun 2025 02:25:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENV YARN_VERSION=1.22.22
# Wed, 25 Jun 2025 02:25:22 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 02:25:22 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f00d2fce1661cc6f10e2982ec23164c04e8216c9b6becd72c7dfa2c1500773`  
		Last Modified: Wed, 11 Jun 2025 16:22:16 GMT  
		Size: 202.8 MB (202765551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b59f82c036ebd7bc80cd269cc1316ad7ccae918fb18a4157ea0fe70444747d3`  
		Last Modified: Wed, 11 Jun 2025 23:13:22 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82af3fd3abf26069e038055d8721594e16771a81d0f5dc3656089f08b97275b5`  
		Last Modified: Wed, 25 Jun 2025 18:00:18 GMT  
		Size: 58.0 MB (58003864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfb590010b42de9d10b3c72c4943878de2b938c557a381f22926513c35f7066`  
		Last Modified: Wed, 25 Jun 2025 18:00:15 GMT  
		Size: 1.3 MB (1250677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9eb2c15ece4747e2f3842407e89492c51b0acedd564642a847c00969f03074`  
		Last Modified: Wed, 25 Jun 2025 18:00:15 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:ef4461f87ba13e51f555ecc82b3d1d9c97911a2e4f9be9f08a7a46a204568554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16211320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b775a3bf3835abd6bb764ec9be1617ab3f7efdcd19eeca3fdf1f11db7f7bd2e1`

```dockerfile
```

-	Layers:
	-	`sha256:90bdfe0d7e9e5a39c4c3cf84ac95d79cd82f70034e5dd6e0b8c139d89edb9c43`  
		Last Modified: Wed, 25 Jun 2025 18:40:43 GMT  
		Size: 16.2 MB (16186997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69a380b72e84603095979fa3996535eb447d134f26362a26e7f6bbd4bd50daa0`  
		Last Modified: Wed, 25 Jun 2025 18:40:44 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm` - linux; ppc64le

```console
$ docker pull node@sha256:e0c0eb7f1a5f0cc41459d7412d9dd9f27d9978d614bc6a01dfbdc5327e1a185e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.6 MB (424578496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7079eca46c7e91588e7a424ff717c88472b2b2273d8171b37189b7e8ca17e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENV NODE_VERSION=24.3.0
# Wed, 25 Jun 2025 02:25:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENV YARN_VERSION=1.22.22
# Wed, 25 Jun 2025 02:25:22 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 02:25:22 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bcd3217ebdd78ee7f5f6a67c7b4b49ee252ec2305007272d04d562f9e83004`  
		Last Modified: Wed, 11 Jun 2025 17:40:53 GMT  
		Size: 25.7 MB (25657425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5e3e648b0af066a27f67ff1ab192ecc1e665ef5dd174521d0a856b9bff018`  
		Last Modified: Wed, 11 Jun 2025 22:39:56 GMT  
		Size: 69.8 MB (69839696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad59f4a8d63a9a6d3a38c0e8051f843741fd0dabd3b5114b4175e24dd0aab6f`  
		Last Modified: Wed, 11 Jun 2025 22:32:07 GMT  
		Size: 214.4 MB (214421221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6b3079bdb7be1c75ab2accb79173310d136783d62ea3100b8b81791062180f`  
		Last Modified: Thu, 12 Jun 2025 02:45:47 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6761c8bbb52e5bd7cfbd6bddf49aba152263968721b3eabc6b91a27fb434b41f`  
		Last Modified: Wed, 25 Jun 2025 18:49:17 GMT  
		Size: 61.1 MB (61068361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59c1b27cfae9974051cb0980691ac512dffa1550a526ba2d84b5eefeaf505c2`  
		Last Modified: Wed, 25 Jun 2025 15:43:33 GMT  
		Size: 1.3 MB (1250671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923133780df82fa3adfc84cd700add2c0baf0a1415974b15f35f684068d7b725`  
		Last Modified: Wed, 25 Jun 2025 15:43:38 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:2ccc31285523c94fd061cb52f7a444641d81490411400893a47734acd8e579a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16159145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96cf123baf6ac8f6cfe1548ae18a5354c89aeddfdd46f6d244c2df830960ff6b`

```dockerfile
```

-	Layers:
	-	`sha256:38959c36e15222b8f5dc86ee2d8bc576c381ac7f460cd5d5255076bcfae64782`  
		Last Modified: Wed, 25 Jun 2025 18:40:57 GMT  
		Size: 16.1 MB (16134944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d3fd83a640b8c69308cf83baa4043e99d3ddffbaf362f76d0a0a54df3ffc33a`  
		Last Modified: Wed, 25 Jun 2025 18:40:58 GMT  
		Size: 24.2 KB (24201 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm` - linux; s390x

```console
$ docker pull node@sha256:b4b0e0e3224f1088af31fd484ee5e3719f970508eeed9265c939b165d0a35ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.9 MB (376877600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33478f651892ff62bb4fc37adb4954bfaae4cbd86e29f23f12d26ce68472afbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENV NODE_VERSION=24.3.0
# Wed, 25 Jun 2025 02:25:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENV YARN_VERSION=1.22.22
# Wed, 25 Jun 2025 02:25:22 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 02:25:22 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dca9cef3741351ad228dc4986e66f3e324bfb88d5cc9e2b190dd3a3abf7dcf`  
		Last Modified: Tue, 01 Jul 2025 05:30:26 GMT  
		Size: 24.0 MB (24020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff1e32b479a11528098c70ba4af6292099abafcb29e0823d2861c86032c9b0b`  
		Last Modified: Tue, 01 Jul 2025 13:41:28 GMT  
		Size: 63.5 MB (63497964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2254c2dc3c53615f5f6a5adcfafb558670473622cb504cb0a6d02fd2b89d2667`  
		Last Modified: Tue, 01 Jul 2025 14:10:41 GMT  
		Size: 183.4 MB (183421934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be87451d3f3f792e8b8e55d217064d92432be45c05667d32dbe91a8feea5ae97`  
		Last Modified: Tue, 01 Jul 2025 17:31:09 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0167b1f0c43629826ab10b32333239dd5741f1b63fb11cce69c943c2982dcd0b`  
		Last Modified: Tue, 01 Jul 2025 17:31:14 GMT  
		Size: 57.5 MB (57533431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b30eb13cdcd7e726f6ae6f1f91c8a2b8a99b5f991993748e414dd47b2b9d8`  
		Last Modified: Tue, 01 Jul 2025 17:31:09 GMT  
		Size: 1.3 MB (1250672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4f6c3ee00fae7d89cd68545d589eb10efab42c86e97155922ee247a5bd4646`  
		Last Modified: Tue, 01 Jul 2025 17:31:09 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:2465ef913243a35dac4f6ed646ae537cda7187c8c4cb9eebf10b2053fb4e7606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15991542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0f89c1c9a43be8de160cd1a957f0be9e115481facbc5a3532bc4dabbb1478a`

```dockerfile
```

-	Layers:
	-	`sha256:23871f421aa805b92e60bce15891aa31ccf17e4085d69b63425bce2ef343f2c5`  
		Last Modified: Tue, 01 Jul 2025 18:39:49 GMT  
		Size: 16.0 MB (15967425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f950185647dcdfc709955b379e31747c5c0099e3ccba884cc1b71268881e92`  
		Last Modified: Tue, 01 Jul 2025 18:39:50 GMT  
		Size: 24.1 KB (24117 bytes)  
		MIME: application/vnd.in-toto+json

## `node:iron-bullseye`

```console
$ docker pull node@sha256:a41f5166878ab966de6b3a4719f38bdfceaaaa298ecc337856baa0cd52b06f7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:iron-bullseye` - linux; amd64

```console
$ docker pull node@sha256:0fb471d1e05216a263672e3280d343c8e779dc7aa2accda805ba1b4c78dc3280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.4 MB (371445654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feaf191333a6a8e9c7f6969d9aeb34c5d63bbff84e51917fb6b145d55d978dc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:42:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:23:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:24:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 07 Apr 2026 04:24:55 GMT
ENV NODE_VERSION=20.20.2
# Tue, 07 Apr 2026 04:24:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Tue, 07 Apr 2026 04:24:55 GMT
ENV YARN_VERSION=1.22.22
# Tue, 07 Apr 2026 04:24:57 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 07 Apr 2026 04:24:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 04:24:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 04:24:57 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847d9f854f908f28a433fd2d5b08b5e68ee58c9ec953dac233ca6864ced59f24`  
		Last Modified: Tue, 07 Apr 2026 01:47:01 GMT  
		Size: 15.8 MB (15790676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14034e66ee3f8bcfd399019612c7f333cc777166161c3dee1a945ac1f0659fd6`  
		Last Modified: Tue, 07 Apr 2026 02:43:11 GMT  
		Size: 54.8 MB (54760196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067d6a857ea26ea67633cd59e0209cb6a54e70a1e95d19e8ae6c6b0a15b3d8d6`  
		Last Modified: Tue, 07 Apr 2026 03:24:05 GMT  
		Size: 197.3 MB (197253868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce52285571014ff2e98341b79db122d8d91a886bc42c2cf1faffddf2e36a904`  
		Last Modified: Tue, 07 Apr 2026 04:25:22 GMT  
		Size: 4.1 KB (4096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72a8bf897aef78016bd221891212b083a0425167763f84a599728589a95a04f`  
		Last Modified: Tue, 07 Apr 2026 04:25:24 GMT  
		Size: 48.6 MB (48622904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884ec4f0f0edf780e50e181e18d543a7ad88766dfad4b29da666d86c5e555a3f`  
		Last Modified: Tue, 07 Apr 2026 04:25:22 GMT  
		Size: 1.3 MB (1250672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324b8c36827e29e5181202dc9b11617b03cfabb56814a5f2a104ec8950931b4`  
		Last Modified: Tue, 07 Apr 2026 04:25:22 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:iron-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:5a887673da09d1a3b18d3c09837e9d9c09ea95ea966e915319ab0173d5992467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15782797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297d73f7a1888611fb8441993155c0a7300b1a2433332fbcfb7423c1889e207c`

```dockerfile
```

-	Layers:
	-	`sha256:4d38b0120b561d9684505256ede237006e5644ad59978be5526cb7856d35e0a3`  
		Last Modified: Tue, 07 Apr 2026 04:25:23 GMT  
		Size: 15.8 MB (15760049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f04d7735cca933337b9501eaadf396f3d345fa8a5645b233c62592875f0e672`  
		Last Modified: Tue, 07 Apr 2026 04:25:22 GMT  
		Size: 22.7 KB (22748 bytes)  
		MIME: application/vnd.in-toto+json

### `node:iron-bullseye` - linux; arm variant v7

```console
$ docker pull node@sha256:acc77e84f94397a4308a71fecd16a1e632ee6329191c9e9c338c22a7e595a718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328286269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73acee6bb2ffa7859cb48eb1af4373905b1892a2c6ea2349d33066f5d3348d0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:00:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:49:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:28:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:19:56 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 07 Apr 2026 05:20:52 GMT
ENV NODE_VERSION=20.20.2
# Tue, 07 Apr 2026 05:20:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Tue, 07 Apr 2026 05:20:52 GMT
ENV YARN_VERSION=1.22.22
# Tue, 07 Apr 2026 05:20:54 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 07 Apr 2026 05:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 05:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:20:55 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:dc8695d526078f14ae00d8def0c6b77226df91b02937f7fe93806b494d0eed07`  
		Last Modified: Tue, 07 Apr 2026 00:59:40 GMT  
		Size: 49.1 MB (49053930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2f7a30a3127c8f109eb33c9b6e0a069dc1bbaf940f09c9ad55a2749c25bb59`  
		Last Modified: Tue, 07 Apr 2026 02:00:52 GMT  
		Size: 14.9 MB (14905095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4649005b124b78e09f68f36f64106a1bba3934081637a27e5d71125cf525a33`  
		Last Modified: Tue, 07 Apr 2026 03:49:27 GMT  
		Size: 50.6 MB (50640954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6122c866086b093947a61d79c835272268c5d8658470d831be42a283accef235`  
		Last Modified: Tue, 07 Apr 2026 04:28:59 GMT  
		Size: 167.7 MB (167730640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472d7959e3417e01fdfe7692014d845cdec905ffc162908a7a9a8d4470b24135`  
		Last Modified: Tue, 07 Apr 2026 05:20:34 GMT  
		Size: 4.1 KB (4079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c9c60ad456d6983aa6291e2254fe1907fe49fb7e3adc91064949ad453d2249`  
		Last Modified: Tue, 07 Apr 2026 05:21:17 GMT  
		Size: 44.7 MB (44700454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd794b41846c66fec908bb600235cfb2078c2b744d808db643a7f588f3019754`  
		Last Modified: Tue, 07 Apr 2026 05:21:16 GMT  
		Size: 1.3 MB (1250670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf7b509e3ce65558d0ec25274904105b82399bcd9dc07de386c90d2c5e26112`  
		Last Modified: Tue, 07 Apr 2026 05:21:16 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:iron-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:d6492fbb5e9a954b45b2950640924722eeb8ce83f1de602368225950f1310999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15582237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c59d84ea7892be3a590de49d5c8c4c4f1651aae0525eae7b4b6ef7069c7c2d`

```dockerfile
```

-	Layers:
	-	`sha256:c5dd2f8e6928fc6c0769cb5b98a2a2635b341a328b94a2d3ada0a03b4427838c`  
		Last Modified: Tue, 07 Apr 2026 05:21:16 GMT  
		Size: 15.6 MB (15559383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e242faac8389e2db528f070bf33c4343da6d56881676688a75928d63c47ad0ba`  
		Last Modified: Tue, 07 Apr 2026 05:21:16 GMT  
		Size: 22.9 KB (22854 bytes)  
		MIME: application/vnd.in-toto+json

### `node:iron-bullseye` - linux; arm64 variant v8

```console
$ docker pull node@sha256:4a30fa1ab95146db549d909e56f98d10de749e66eb7dc8fa92069e4b822cc353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.9 MB (362947050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2e9277155d93ec0df32672ff9601b0900d79f43f42755f9eedfaa85f824908`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:42:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:17:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:20:44 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 22 Apr 2026 04:21:41 GMT
ENV NODE_VERSION=20.20.2
# Wed, 22 Apr 2026 04:21:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 22 Apr 2026 04:21:41 GMT
ENV YARN_VERSION=1.22.22
# Wed, 22 Apr 2026 04:21:44 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 22 Apr 2026 04:21:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 04:21:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 04:21:44 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8876687e9899211f85cbf406fe17625833ba27c454fedd4275ac8a0a58206e1d`  
		Last Modified: Wed, 22 Apr 2026 01:43:08 GMT  
		Size: 15.8 MB (15774737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41762a69c06632f02d051591b8561619178cda30090272dff52f65c2d6157695`  
		Last Modified: Wed, 22 Apr 2026 02:32:20 GMT  
		Size: 54.9 MB (54886521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba12cf159babc02fc1c9dadaf51e2fca9d51183009dbc801190af3b460b98dc`  
		Last Modified: Wed, 22 Apr 2026 03:17:52 GMT  
		Size: 190.2 MB (190190591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1e5a4a8b57d4bb18714135869b0a07b170d4b6c8d243759f7dc741e1b1f20f`  
		Last Modified: Wed, 22 Apr 2026 04:21:23 GMT  
		Size: 4.1 KB (4092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d455dca2c09df963cca7edf8c1ad78d438b7bd3c727d3241d14fdfa0ba8006`  
		Last Modified: Wed, 22 Apr 2026 04:22:08 GMT  
		Size: 48.6 MB (48586986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4771f0dea5683bfc54a282a39b3174afe746f60db5743f7f8b276c7777d00a8`  
		Last Modified: Wed, 22 Apr 2026 04:22:06 GMT  
		Size: 1.3 MB (1250676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e8053377add7aef05ef0ca580c1c4922756bdaceadedbf5d0cd5222f069900`  
		Last Modified: Wed, 22 Apr 2026 04:22:06 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:iron-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:78a88dd1921984bf298826c952a936d3527fde87529884cb9f50c488cd61f45c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15784900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85be0151d5467939f25d0dc450185d7f715707ebe05cd3599320a462199b39af`

```dockerfile
```

-	Layers:
	-	`sha256:3522942114fa6761fac696709e257b9fef01680259e89c461922951eeff485c1`  
		Last Modified: Wed, 22 Apr 2026 04:22:07 GMT  
		Size: 15.8 MB (15762018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfe559f142c464af8e183c3ec16ccae0e6f5a26371de1c41f98f91f844c6c121`  
		Last Modified: Wed, 22 Apr 2026 04:22:06 GMT  
		Size: 22.9 KB (22882 bytes)  
		MIME: application/vnd.in-toto+json

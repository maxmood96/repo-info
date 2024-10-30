## `node:jod-bullseye`

```console
$ docker pull node@sha256:56b4427fd940afa92dd7b5fbfbd544318b3cef9e79d1c8585c0d240d3bd752c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `node:jod-bullseye` - linux; amd64

```console
$ docker pull node@sha256:b874f619aa7c949203e45335fcdf70b360be224ca055dfac088ef8511bbaa3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.5 MB (378503403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45944a0ac6845233687048744b4bc6b989c80297c72f5b93187505b1e76fd440`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
ENV NODE_VERSION=22.11.0
# Tue, 29 Oct 2024 20:39:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
ENV YARN_VERSION=1.22.22
# Tue, 29 Oct 2024 20:39:22 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 20:39:22 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07a20b182d5672c6ec8dca30220175ce5c60e45bf630d6adae50504d92368ad`  
		Last Modified: Sat, 19 Oct 2024 02:06:22 GMT  
		Size: 54.7 MB (54725293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54dcdbbe5c1d62201fcee2dd2ca8ca09ec165f840a8a7a9fe05e7875b49b468`  
		Last Modified: Sat, 19 Oct 2024 02:53:29 GMT  
		Size: 197.1 MB (197069718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b8cef6a103be161db68ca6e207c0f25f0a02d06a80cb194afc76f5bcbf998e`  
		Last Modified: Tue, 29 Oct 2024 21:58:23 GMT  
		Size: 4.1 KB (4091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aeb2922852a80f37887ca07df9cdc371bb50b50447cbe63ddd7043228dc3bb`  
		Last Modified: Tue, 29 Oct 2024 21:58:24 GMT  
		Size: 54.6 MB (54610258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b93bcf9e4c2dd8c86458a8a26bc0906c5d53f4731543eaa52d815afb93a1e0`  
		Last Modified: Tue, 29 Oct 2024 21:58:23 GMT  
		Size: 1.3 MB (1250675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4052b9ca5cba4d132aa06a575f37d24b469b9e5453893176d3486f5282f44608`  
		Last Modified: Tue, 29 Oct 2024 21:58:22 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:jod-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:ae792c36d3e7a573a7bc4ade76245b572c74d005288ffc0a2c83f0d4393faee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15454722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28af1b88259f85e4ca3a87a89903962f19aa8fade233d971164a6ac7d71184e`

```dockerfile
```

-	Layers:
	-	`sha256:83fa662e0415d4c89465e3ebd9ed12d34b5d20da6b2dde8e23d3c5e0dea2ff8b`  
		Last Modified: Tue, 29 Oct 2024 21:58:23 GMT  
		Size: 15.4 MB (15432156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe20e83b68f9c6b739f63e8cabbca52095bc6295518293f1c11a549942cf2aab`  
		Last Modified: Tue, 29 Oct 2024 21:58:22 GMT  
		Size: 22.6 KB (22566 bytes)  
		MIME: application/vnd.in-toto+json

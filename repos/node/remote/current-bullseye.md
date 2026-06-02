## `node:current-bullseye`

```console
$ docker pull node@sha256:ab48de2bea90d93062d4c16045aaa8715160936211e8a5357ef3169bd0ba566c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:current-bullseye` - linux; amd64

```console
$ docker pull node@sha256:29330fd66837236f9337cdf5fa6478f73138dd1332045a736441af4575f3731b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.8 MB (384761540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307fe02f17b2fe6b341f1c938bce919540e41cd043ab92baf567b1f58a858d42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:23:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:15:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jun 2026 22:46:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 01 Jun 2026 22:46:46 GMT
ENV NODE_VERSION=26.3.0
# Mon, 01 Jun 2026 22:46:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Mon, 01 Jun 2026 22:46:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jun 2026 22:46:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:46:46 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a725631376ff1c8c144d62e01c2dd134ff006899cd43c1aff2afbb3141faf91b`  
		Last Modified: Tue, 19 May 2026 23:23:13 GMT  
		Size: 15.8 MB (15790858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5942943df443b1bc1e709676d52a57b0a7ddee0c58a1602ecf5e2e8b271916d`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 54.7 MB (54743262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecc88763ad50d1ab5c41218bf6aa5893d2c739925d42b6eb8f2c52823019e44`  
		Last Modified: Wed, 20 May 2026 01:16:23 GMT  
		Size: 197.3 MB (197307874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94de1598fba678705c480cba2a08b7126a375a21bd92a158b1def583d8ed3fc`  
		Last Modified: Mon, 01 Jun 2026 22:47:13 GMT  
		Size: 4.1 KB (4094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644d571f64b0a5558cf8f6ac63370a6f3a76ee65af673d72952ce553ad729404`  
		Last Modified: Mon, 01 Jun 2026 22:47:15 GMT  
		Size: 63.1 MB (63146154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8518b9941fc9f19a1253341de3579290895ddef4da77ef2d01e41c2e6d318a9c`  
		Last Modified: Mon, 01 Jun 2026 22:47:13 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:2d262f8fda768c5070947e4fd9e7f02d884dd682c6dd5bcc9ac176f73d7d4d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15697705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c54ddb3ebc87cc211c61386347d66d67fc69b4b7ca8739047903fab31a2253`

```dockerfile
```

-	Layers:
	-	`sha256:3c4be8aef054fd33f87cf21beaaee676eb09e0eaff5b29b97fa491052a4fda80`  
		Last Modified: Mon, 01 Jun 2026 22:47:14 GMT  
		Size: 15.7 MB (15680176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75ad23e48202e114cee4defe2f856c13c056926065feded12fe6bed0033d1165`  
		Last Modified: Mon, 01 Jun 2026 22:47:13 GMT  
		Size: 17.5 KB (17529 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-bullseye` - linux; arm64 variant v8

```console
$ docker pull node@sha256:9e6f96316299fcb238db529064fa923e084b761fed45631f1550599837691f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.5 MB (376459156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc464e2dcdbd6e5a6d8dab6fb29ce672bfa23ba48807dcd6668c84deea316089`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:15:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jun 2026 22:46:49 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 01 Jun 2026 22:46:59 GMT
ENV NODE_VERSION=26.3.0
# Mon, 01 Jun 2026 22:46:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Mon, 01 Jun 2026 22:46:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jun 2026 22:46:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:46:59 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b862d1986560a28dd19f86c2aee630b1502d7f508a9266ed7d99d6f03a48419`  
		Last Modified: Tue, 19 May 2026 23:26:59 GMT  
		Size: 15.8 MB (15774880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522a0e24f23d039a1a5ae21822bccb045bfdedf83da569dc13fb1992e903bbcb`  
		Last Modified: Wed, 20 May 2026 00:27:11 GMT  
		Size: 54.9 MB (54879862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5578d03844480631fb598cecf497312529f7e21642b612b605246de4df178882`  
		Last Modified: Wed, 20 May 2026 01:16:01 GMT  
		Size: 190.2 MB (190209386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48d1e3595d7a6e9575c54e2662f58a2c3e18b169cc2b8206cef61919cdda065`  
		Last Modified: Mon, 01 Jun 2026 22:47:27 GMT  
		Size: 4.1 KB (4098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d216ed7f0cc10814a62923a98f03d058827a8c9e13f08ebc6a2a12c7fff00bde`  
		Last Modified: Mon, 01 Jun 2026 22:47:29 GMT  
		Size: 63.3 MB (63333907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f7003770552d262e20a94f78aeaa3f36f0836aaa8ef0872c4bef9f50929d68`  
		Last Modified: Mon, 01 Jun 2026 22:47:27 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:bde60e4e63d2028a0d8268e400cc60e6462719405ffc2d7a36951a42a283687e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15699819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dcae1e90472a54a6321ba20ccc5d87c9a34c0f912adb1debdeb5110728eb1a1`

```dockerfile
```

-	Layers:
	-	`sha256:93c73ec4e3caa22c6d3c0167b6798a54a47848b0a1c9f1e54217bd476889a024`  
		Last Modified: Mon, 01 Jun 2026 22:47:28 GMT  
		Size: 15.7 MB (15682157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6318f1c01d9889653a4a5958075835191a9ec2f35189fba6e147de58f46ccc08`  
		Last Modified: Mon, 01 Jun 2026 22:47:27 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json

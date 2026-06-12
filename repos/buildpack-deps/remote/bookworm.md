## `buildpack-deps:bookworm`

```console
$ docker pull buildpack-deps@sha256:7d9a7601d4e042e3578d7557186c745e03524bd3c751680618639db99d7e9ced
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:bookworm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b931ed58d07d1ecfeba2d6c72b07b6c38007309ca2e0a1f8a9f8e917798fe30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.6 MB (348554756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ba07cc904f828b1dbfdbc7319378f60ccd974ab435751aa147b237958bd8e3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:16:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbaeeb62b9d03a1204b85c3b257aa3e1ce2c4ccfeea479fb2e659211019c29d`  
		Last Modified: Thu, 11 Jun 2026 02:24:43 GMT  
		Size: 64.4 MB (64404116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7044c1cf2c0cb824c5cdae28ae059e28d1bfd83182a096356a06ced450dfb7b`  
		Last Modified: Thu, 11 Jun 2026 03:16:50 GMT  
		Size: 211.6 MB (211604598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f39d9a43c52d0cf0c7722da2ab438137a1d3ad721620534f6f412ec350caf08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15876501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372f554564fb7baf41a5d1c8b32d5652a94428bcb9548fc10cb63a963666ef85`

```dockerfile
```

-	Layers:
	-	`sha256:e651280d84d9bf31cb2e319c362faaa5b86957fd1b965a27a0c04ea460909d40`  
		Last Modified: Thu, 11 Jun 2026 03:16:45 GMT  
		Size: 15.9 MB (15866312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dba36334fa8c3a9c0188785c84f52256d8ee3a483450b40f38e59eeb8487f9d8`  
		Last Modified: Thu, 11 Jun 2026 03:16:45 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a93a6f651e2bceb04c5c6fc7a96b062d384dd5b35c42fb89656554001c37bfa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 MB (315631040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324f1aeccaf66b4666965ba931f9b381488d71597e1dceaf420b559048c0b958`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:17:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3683b8a7792857dc507c3398919097537c8d564a235824e722ff16657599fe21`  
		Last Modified: Wed, 10 Jun 2026 23:38:13 GMT  
		Size: 46.0 MB (46038189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c451565562cd00a6664508aa8323b184e76b5b0de69ee46d3c1372a759dd2d`  
		Last Modified: Thu, 11 Jun 2026 01:21:09 GMT  
		Size: 22.7 MB (22717990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a91f6061b18b13afa05f640b62518105d726e8abf295d2ddec34351f6d93ff`  
		Last Modified: Thu, 11 Jun 2026 02:46:57 GMT  
		Size: 62.0 MB (62022483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1deef53be99de8a953b0ebc76a6433371b9cccd8382d3222bb831fa657199f`  
		Last Modified: Thu, 11 Jun 2026 03:18:02 GMT  
		Size: 184.9 MB (184852378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:18d387d2b9698cca36b0c110edd22d54beaf8b509d13770b60f36c59b1cc71a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15673549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f5ad8927702ad98fca5e58f774ff255c5ecc3a3ef5d5e53f2ea1a466d12511`

```dockerfile
```

-	Layers:
	-	`sha256:3e6b9ad20565750e746aded07d516e8d7d0822db1ccb6a47156b4a4877cc6718`  
		Last Modified: Thu, 11 Jun 2026 03:17:58 GMT  
		Size: 15.7 MB (15663296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2989acdb153bc9199178af3e352216a699fad61082189a882a191cde07dd02f`  
		Last Modified: Thu, 11 Jun 2026 03:17:57 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b7e46ca6d5b66b2e56275cd8b319bfc87355efad36b4b089601c771674b79b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301313019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d660b015e4c9397d5317495d87a07affcc4d1ff4aaeb0812d73f2f217eb568`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:23:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:43:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:20:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c0213091aa87e4be7caed06dd364889c231dab5ba50fa1e54365eb7a94390261`  
		Last Modified: Wed, 10 Jun 2026 23:39:46 GMT  
		Size: 44.2 MB (44208065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14356188705148a948907491c78974967557826c6ca92209148b3bc14f0f659`  
		Last Modified: Thu, 11 Jun 2026 01:23:38 GMT  
		Size: 21.9 MB (21949873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f917f7c68aa5629a37a99de2287c5dada27c5ba0cd553e5b4f28471c0e6c213`  
		Last Modified: Thu, 11 Jun 2026 02:43:46 GMT  
		Size: 59.7 MB (59661587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c987777ba37da55122efb8c5b9f10389679928b55add66edc84af27b2e7365`  
		Last Modified: Thu, 11 Jun 2026 03:20:46 GMT  
		Size: 175.5 MB (175493494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5aa28442347abda40f4043f1545d46cea17c0c74889fe40b107348f5f289c183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15679025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ddc2229445949de4b79c12e8bfe430a44bc7d449385803ec9067a3cd63ac97`

```dockerfile
```

-	Layers:
	-	`sha256:33e60fa401384a6a46a5100eaf7635e6be20962b0fbfa29f1b306477e552dc6d`  
		Last Modified: Thu, 11 Jun 2026 03:20:42 GMT  
		Size: 15.7 MB (15668772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636883de5cda5f621073539ceb48093d174756e531f60d65fea8f85937a3b402`  
		Last Modified: Thu, 11 Jun 2026 03:20:41 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:22e6f90b138866051d4209b774fe28813483a8b67b431b4cb6475176ebe06a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339616443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce4fd825f45d07935fc27b047562963683d7b0507e67ab9acf725d5594657c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:15:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b715a6712db064e97302c819acd7a39c0c72f8a315ff83c6ad1c27bfa1b275e`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 64.5 MB (64487878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90f867a17df01b0040907a3eb5559d294e5f4cd3aec55151ab788dafceece2a`  
		Last Modified: Thu, 11 Jun 2026 03:16:23 GMT  
		Size: 203.1 MB (203126253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:026498b4cd3bf0436c2f80845595eeea93dcb5ff9ddc7da16ed3cf51462fd4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15905083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c6fa37c6f5535166819eb12737dfd89ee5b583ec7f4af82927df2189d606bb7`

```dockerfile
```

-	Layers:
	-	`sha256:bbaca21e2349d79dc7d5fe65d3c3890db0daf1cda0616a75d2ec4f3dcd343d47`  
		Last Modified: Thu, 11 Jun 2026 03:16:19 GMT  
		Size: 15.9 MB (15894814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb623bc1cf8ec9e84bc5f6b9c7d055f089d62bc1c67af2707813306468d9e98`  
		Last Modified: Thu, 11 Jun 2026 03:16:19 GMT  
		Size: 10.3 KB (10269 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3f9f60bc2beb22c3b65c32847585538a52fd3ad753607ee3271fdd3cc77ac476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351153557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73f7f89a07a77d5bcf772f61b8e30add131aac3d77a31ee84b54c13500ca247`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:16:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:08773a2e9b0fe592ef47b4e93c883d32a351ff89ea9cd33f1ad47abd4081b4ca`  
		Last Modified: Wed, 10 Jun 2026 23:39:44 GMT  
		Size: 49.5 MB (49491206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1abb617cf69e81d401bea3de65ddcc50a1ac250e94890ec9ab61cb42a18679`  
		Last Modified: Thu, 11 Jun 2026 00:44:59 GMT  
		Size: 24.9 MB (24879714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cc4b12d03ab32e6c96be6bc5f6e0fc347b431b1f7686aa5f92f4cd1a5cccbc`  
		Last Modified: Thu, 11 Jun 2026 02:24:53 GMT  
		Size: 66.2 MB (66244000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1729487cb56c8b006710daa9885bc2a752aaefd220eb96d098a1584056aaad7b`  
		Last Modified: Thu, 11 Jun 2026 03:16:59 GMT  
		Size: 210.5 MB (210538637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b417ed991459c0a4940e3bb605bbcbd69ab4be7158c9a055adc7b4d5616f441e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15854707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b53a56a0cfb49102911318026528571dc204d23d881cee0eb744fcbec456923`

```dockerfile
```

-	Layers:
	-	`sha256:5fcaa6ae3d87e710d9badd91911fa31ab4b70d86e4f0da3c803535974a7a2445`  
		Last Modified: Thu, 11 Jun 2026 03:16:55 GMT  
		Size: 15.8 MB (15844540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40167603b16f90566f63fad5e0c6cdd03136064e93866c29df7dfef499471183`  
		Last Modified: Thu, 11 Jun 2026 03:16:54 GMT  
		Size: 10.2 KB (10167 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1ee7e111a792fed0e89a2e13e6793c090a42d4522ba00dc54dbbefdead6ea177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.1 MB (326087537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dba5f2ccf4c06ed300a9e024810f6f6523f21d0ba8913d075f7d50181d5b476`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 17:08:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 01:00:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 01:25:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c4a18bb29be3659c76b4d9b55eb7f69e2b6fcb341523ef1670ac059503a592b9`  
		Last Modified: Wed, 10 Jun 2026 23:39:38 GMT  
		Size: 48.8 MB (48792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d391bb145fa329ccce2ad9a5e686a519ff55f48ee4a211ba2c146ad64db56d80`  
		Last Modified: Thu, 11 Jun 2026 17:09:36 GMT  
		Size: 23.6 MB (23624039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270c086020bbce3335fe9eece6ed9bd8f5bc1e45eed6579e81e64181addffb83`  
		Last Modified: Fri, 12 Jun 2026 01:02:23 GMT  
		Size: 63.3 MB (63315954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabc0d09590f6c3174b92d8abd0703508147f87e3c896edd58df6a33c30e4c61`  
		Last Modified: Fri, 12 Jun 2026 01:28:57 GMT  
		Size: 190.4 MB (190354833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:95cf5b8480cc1cf847ae328afcede785ff94ce703bb8466d2eb3df983d4940df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df6da4adffe8636c02ad3e29cf4eeec5b97a48040ba6802016feea6cc34e474`

```dockerfile
```

-	Layers:
	-	`sha256:35a7254e104e48c84908c0f3c9b1164ffe296041991bfc28fd718e1d6cc060e2`  
		Last Modified: Fri, 12 Jun 2026 01:28:37 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a53d7ab953dd916e3b992567b8862b596c8e7365bb729ec15dc26adf5db1af97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.5 MB (362527201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a27562a20d811ddd964236ad6df05b50c3ca4fffa52a95f0cbb23a33b175d40`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 04:43:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 10:26:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 12:45:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45654aeab75acaade8b0e13728139de28feb7f503c7e094076fcb9a6e4ed987e`  
		Last Modified: Thu, 11 Jun 2026 04:43:46 GMT  
		Size: 25.7 MB (25686794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b3af7c755dce470b1c44918153cc71bc2ea3bed1cbf9108bce1ad1d4579fb5`  
		Last Modified: Thu, 11 Jun 2026 10:27:04 GMT  
		Size: 69.9 MB (69853632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea21655a17d2ee83d21538915d2102860b4542a5b2c3753a90e0b3aa19415b42`  
		Last Modified: Thu, 11 Jun 2026 12:46:18 GMT  
		Size: 214.6 MB (214640105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f40af3ec79f3fd29c1cedb0952ee616d8b798241ddb2c1509e33c16231e9cb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15853034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09029ff5fd2fda2f1642aa415d82aeaafa6b694df2049ef66555eebf352fa640`

```dockerfile
```

-	Layers:
	-	`sha256:eb128ecca6883b0d49860e7393e2e85049e21b91538493b17e9a1b8cac43fcfd`  
		Last Modified: Thu, 11 Jun 2026 12:46:11 GMT  
		Size: 15.8 MB (15842815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e42ef91178e1afde7f747c88c4750894c3bc8cd09571175d2724c4287fb40ee3`  
		Last Modified: Thu, 11 Jun 2026 12:46:11 GMT  
		Size: 10.2 KB (10219 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:211ac0f6c220bec83327359716b3a359c9e91cfa817dc8b8e54c352ca67fd9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318322139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b4f5b1cbd527fc721a122c5267a2334065fe3b4a24f03c3e314ef7f698c00ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:15:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc0f0bf9684619796dace2f15b323a1fcec3fdfd4a5712e33f82ae28ed815bf`  
		Last Modified: Thu, 11 Jun 2026 01:43:58 GMT  
		Size: 24.0 MB (24038950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f33cb3e3ab28182d2640ab8d60069099e6c4d1dd9ee3f806d20e366f1901797`  
		Last Modified: Thu, 11 Jun 2026 03:26:38 GMT  
		Size: 63.5 MB (63498201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ff3f7a67e23169f7ca69b49e30014a5c74ff53c62dbec259b93c844556a24a`  
		Last Modified: Thu, 11 Jun 2026 04:16:09 GMT  
		Size: 183.6 MB (183623488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d0baa5702f7f2f9a6e829909718f29142fc085687c51cff7a9b15257c38ca0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15684099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d1f27d7486f39e98ff77c4afce954bc204964fd2391032d663265277895c8f`

```dockerfile
```

-	Layers:
	-	`sha256:09a3ae60a9963cf547789f09207aa12f1d0bd613ea3d3f1dd5b72f5099667dd5`  
		Last Modified: Thu, 11 Jun 2026 04:16:06 GMT  
		Size: 15.7 MB (15673910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da280339c81be0472fcc9d0c4221b0926bb214f867a773b53ee525ea69154646`  
		Last Modified: Thu, 11 Jun 2026 04:16:05 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.in-toto+json

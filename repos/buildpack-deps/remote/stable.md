## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:08d61da2eb4b661e95088f6999704803985f9bd7be23b3c5d7acce26cd2d521b
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

### `buildpack-deps:stable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d7d6286e853f4cad78b9bacc9962ed13b3fae93c940bc951a473bf59f7f1e406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.1 MB (348060715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fffceae85e2c8f384b15a112be85e0068e283d5c5a20b5b6569421c24c2d23f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551df7f94f9c131f2fec0e8063142411365f0a1c88b935b9fac22be91af227e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 64.4 MB (64391508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce82e98d553dd62ca6a12bebfe83992ae9f9ae2748275e74b66a68cc094f868b`  
		Last Modified: Tue, 03 Dec 2024 04:31:20 GMT  
		Size: 211.3 MB (211306121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:22a0e2166ec5a7010a99174c9c5a4b92eb963a4c9b850ffc869e3ae672a4dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15507109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e432f0cc69ae07b4e7a310d24f8c071f75c5c31a75f80f558a30a9de615e1d90`

```dockerfile
```

-	Layers:
	-	`sha256:28a6ec7885ff79f670b70218ace6d532c8d6d4ee96e883c5eea08d923c243220`  
		Last Modified: Tue, 03 Dec 2024 04:31:18 GMT  
		Size: 15.5 MB (15496569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4526bb391e6ae70edf822e4ae77d44dce58b597a0adf995d87ca2061831eafe0`  
		Last Modified: Tue, 03 Dec 2024 04:31:17 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5493da36ae1be44ee45e6f2a21e8eb7a1651f02980e111eb4b77fcc9de0a28a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315162492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1431cc1ab0a9621e4af9c733d49b9b97de509516dcbcd2b4c7b5b24edab2124`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a8ab0b752e573ceb3480052f24bc5fe3f4f4665c13a338db39c1d51f749528e9`  
		Last Modified: Tue, 03 Dec 2024 01:27:04 GMT  
		Size: 46.0 MB (46024374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff6779451547ba3f0647f15a65068290fed53b6a4ac506257de98e02857bea6`  
		Last Modified: Tue, 03 Dec 2024 05:23:42 GMT  
		Size: 22.5 MB (22540382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536c3cdef529f6d2993cf137c109a079266cd3effbffc602a136a2a60ee743a0`  
		Last Modified: Tue, 03 Dec 2024 08:40:08 GMT  
		Size: 62.0 MB (61996814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f689132b2bca5271eb471905bd9f8eeca3a8c74df88b2f1c85f7c43568f20e7f`  
		Last Modified: Tue, 03 Dec 2024 10:05:05 GMT  
		Size: 184.6 MB (184600922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9c4417f2e99d2695ac62a5424fe36d0c44cca3243f219bea81261e45beaf3b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15305788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153481c7eaadccabe24fb8bb164c037031dfbfdd932085326ec034ee9a386d98`

```dockerfile
```

-	Layers:
	-	`sha256:5aa70f8227a7f0f719920d36ec18fa8bd67edfb3e40293ba3716fb81b5aef76b`  
		Last Modified: Tue, 03 Dec 2024 10:05:01 GMT  
		Size: 15.3 MB (15295180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b8c7629b4f7dd625175f4302ed859bd0ad93857f5dbca59a30b70d298562b4e`  
		Last Modified: Tue, 03 Dec 2024 10:05:00 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:437e11f7b48081f9d3169d3f0b57c19ccbf5d90f78824f50b59ee48d4e0d9fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300850185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1add49ced00435fc4e660bf2b8efd6d6f065f88334295c8dc979ad7f0ab8297f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4d43724a324f138c88a78ca6df0a39ab6868bf1f121eb974439c5a51284e1ac2`  
		Last Modified: Tue, 03 Dec 2024 01:27:59 GMT  
		Size: 44.2 MB (44200109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0e53b92c3d0f5c370d71aeac1be1d23e475f1afba41d896ace0ff6eeefc90`  
		Last Modified: Tue, 03 Dec 2024 07:36:14 GMT  
		Size: 21.8 MB (21767161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9625bef464ab08848044651374e04f75d37ada02fe71387c3f9f83d0c9376c59`  
		Last Modified: Tue, 03 Dec 2024 17:15:53 GMT  
		Size: 59.6 MB (59641126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d83c079d9e82f91aeec2e9d84797bc47fa7f3b69f4094b837cbb4a9c25c5613`  
		Last Modified: Tue, 03 Dec 2024 20:03:34 GMT  
		Size: 175.2 MB (175241789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c37a07b310ce0346c0b105b93643ae7804934f50b5803137d2397fda42284ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15311262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212be7441ad84dc59844b2e1479e05aaff0604670d910cd493e41a9ee0f3f9a6`

```dockerfile
```

-	Layers:
	-	`sha256:d6a56c836aa67f6706e6eacb06bc1edf226a862c6df77e58f7a17171c9494731`  
		Last Modified: Tue, 03 Dec 2024 20:03:30 GMT  
		Size: 15.3 MB (15300654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20d1d9165217046eef0f65fd0f02af670a48e312e840cc150c0713c8769cc7b5`  
		Last Modified: Tue, 03 Dec 2024 20:03:29 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:39b25cdea8a4133052cf8976d884cd9f4a28c36fc7ea1d200a82c3054510ff15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.8 MB (338766544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14cf9bca2791cef90a5b1313fb25c31438e4cf72dfec291fec9d3abfcc7b8674`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261351ed796deb9fdad22dc734919eaf6726dd79a8dea99327d9e1376ecdcbce`  
		Last Modified: Tue, 03 Dec 2024 11:50:22 GMT  
		Size: 64.3 MB (64347852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d319298afc8bd728b8009e80320fe04e864fe92783eb06238a3b9f67dac7c3`  
		Last Modified: Tue, 03 Dec 2024 16:19:47 GMT  
		Size: 202.7 MB (202687199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d273ba454f05ac7b5489806499d16a8fc8ebf4171d5b07f144b245ce6d48a92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15535745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a83186039bd3ea2e021d2749e90f67f3e94a9e21027127ab2af7156513301e0`

```dockerfile
```

-	Layers:
	-	`sha256:578a4e71415013356a8cd37b5030e980c95edd8780c5a2f5a02a5d3585b92925`  
		Last Modified: Tue, 03 Dec 2024 16:19:42 GMT  
		Size: 15.5 MB (15525113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c493ff614776a1782e0bbac3137f383ef0eaad4fffed2bc981261fb4770db246`  
		Last Modified: Tue, 03 Dec 2024 16:19:42 GMT  
		Size: 10.6 KB (10632 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0ab7c71d79bd872a655352313f52121a6bcff2ffbac86045c95275339c23dd99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.6 MB (350616786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3ef764469eb7f8569265b9f9540132de83292a18992941d2995b96bcb6332e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0c73f75a815ce87bbf2841b694fdc4c29bcd072480b8752e8e91f0b59097b`  
		Last Modified: Tue, 03 Dec 2024 03:23:49 GMT  
		Size: 24.7 MB (24706896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2cf0351f309a0cf554972555b46b2ed97868d801e25eeed28a9f742a5e555c`  
		Last Modified: Tue, 03 Dec 2024 04:29:18 GMT  
		Size: 66.2 MB (66211191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adec659d61840fa9345456f332914b715e5d645a246d8ebd23b1c1c4b49b4996`  
		Last Modified: Tue, 03 Dec 2024 05:13:33 GMT  
		Size: 210.2 MB (210222547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:beeefbfff2ab941591ca7b91831c773ed391314b2de8511095bed0ee45cc98dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15485661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8bad9e7072ba65013bcf0c51e6857d3cbf652a07f0e5daa83e3d046e94995f`

```dockerfile
```

-	Layers:
	-	`sha256:87a64892961d327a139e2c8827b6f3f38d3383d5f173df4dfebfbfa09ef41385`  
		Last Modified: Tue, 03 Dec 2024 05:13:28 GMT  
		Size: 15.5 MB (15475148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e958a20d62bb83ee3421e3a3e2d16608731c94121983988380170f328b7e9f2c`  
		Last Modified: Tue, 03 Dec 2024 05:13:27 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9a4df2f86567815e32dbc326f5e5710e33ae4f7e2c64c4ce81c28b6ee888b1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325389432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3307c2bfac9eb9bd9ffeca8fbb60c761663449db1d61e6b4628d2dc291c3d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8f7c3140f4f3af477253c748b229283137cca4214e1c3df21109b821f9227620`  
		Last Modified: Tue, 03 Dec 2024 01:27:53 GMT  
		Size: 48.8 MB (48771844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa54d74c5fddb1e648e0a4d95fcc8338f5800ff817646baaa9e6e65596d80c5a`  
		Last Modified: Tue, 03 Dec 2024 15:45:04 GMT  
		Size: 23.5 MB (23458105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279e7254de3fa3935af4b6008753d14fcd8db605c58b83903cf8c5f880324cd`  
		Last Modified: Tue, 03 Dec 2024 23:22:12 GMT  
		Size: 63.3 MB (63283098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dffedca1364b4f303c66eee15c30c1fe70fb1db9416edf06602e694b41c50f8`  
		Last Modified: Wed, 04 Dec 2024 04:38:35 GMT  
		Size: 189.9 MB (189876385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0b9e0ac2a57702f5a76c6ff8a70e27672e95eabbe67a9141687c6917de5e0b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aad0047efd61ce3266f344221ab7efa1e1390e8fa64a6831adff99b0275fcfb`

```dockerfile
```

-	Layers:
	-	`sha256:10d62b0e0d641ac025f308f802b13bf87690a2a5ecfbbc2f4f58a5d28559ba58`  
		Last Modified: Wed, 04 Dec 2024 04:38:18 GMT  
		Size: 10.4 KB (10382 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4ff5e7a9649060e6cec9389c3206397b83ccf21a3ef73f6da914d6a2b64f07fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.0 MB (362005295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f8e120cfb46d308aaefc2f3eb5e8f7580c23131f19cd4b52ef9a90bfce89cb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c84d784fe3c6c2bd95dea1c0d6eeba7c981bfb75bd53f81e83bcaadd87bba6f9`  
		Last Modified: Tue, 03 Dec 2024 01:28:03 GMT  
		Size: 52.3 MB (52328222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f0cfea13db30ebc69124696ada25182d1141398cd301a47a2cbf3c10d7fa9b`  
		Last Modified: Tue, 03 Dec 2024 04:36:57 GMT  
		Size: 25.5 MB (25523892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac73bc765d61ec6125ff5203c6c3d44543e6c3030684bfed0cb8f169640ae757`  
		Last Modified: Tue, 03 Dec 2024 09:41:44 GMT  
		Size: 69.8 MB (69812337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96099d400daf72e276203923fc855b1b1e5db81df04082e3505683bb398ec9ca`  
		Last Modified: Tue, 03 Dec 2024 16:12:55 GMT  
		Size: 214.3 MB (214340844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c38259992ff8adb65a540669780917a3ab0b4eb2a7bacfc0defc08aabe1954a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15483450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f228c3be5f23d0c8799c7a0da21c5bdc94a05195f09c48ab4f5756a9444da4d3`

```dockerfile
```

-	Layers:
	-	`sha256:4440c44dd5ab1d5632e5b9c675b3baff9156597169f4d38bade9241401960420`  
		Last Modified: Tue, 03 Dec 2024 16:12:35 GMT  
		Size: 15.5 MB (15472872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0489521282efca47f374796943fd138778aa10144bb693e59944fe88b32e855c`  
		Last Modified: Tue, 03 Dec 2024 16:12:31 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cea2ed2882f4bb7184acceea3fb0d08f2c273af35929de4d26ec1770b8329e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.8 MB (317814279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df084175632dd7bf0baf95424425d7b56f2dc329be6919e564076bfc0c0b66e7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53a5c0dbd93a4a7f540e18bbe49ba3d7fadaa390ebbce009c756e34c5b1ae048`  
		Last Modified: Tue, 03 Dec 2024 01:27:55 GMT  
		Size: 47.1 MB (47149767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ded5bb0b377b736e6c5f45164fe8916ada3485441e963fe2fc0671949650049`  
		Last Modified: Tue, 03 Dec 2024 04:07:42 GMT  
		Size: 23.9 MB (23864625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b626037a925f80e453161d124c98cc5578e9d47f3f90a050168552e9727a34e`  
		Last Modified: Tue, 03 Dec 2024 07:53:40 GMT  
		Size: 63.5 MB (63473216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877241890f0b72dfe408c616ea9dde1f1c0afbbe3e7b91d9ceab73e7963ef0eb`  
		Last Modified: Tue, 03 Dec 2024 10:39:34 GMT  
		Size: 183.3 MB (183326671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ebbeeed93d90a07f2bf61c939dc6239ec6d8f6061e3eb49598381e313d2fb582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15319550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017d6c05bd78e755bb45830a2c4afd3694c60f8b2019aa34942d6d1c91f3951b`

```dockerfile
```

-	Layers:
	-	`sha256:a14fcfe55eaddefca48b5c90a0ebb9e879a4899937c7f283124a5b4f9155e8fe`  
		Last Modified: Tue, 03 Dec 2024 10:39:31 GMT  
		Size: 15.3 MB (15309010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a7f4e3bcc82457c7631f0aa274731bcc28c78bab41b2d89951556c508a2a32`  
		Last Modified: Tue, 03 Dec 2024 10:39:31 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

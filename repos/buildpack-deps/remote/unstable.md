## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:0101a3ac396f923b26c3e61c29df8e188b809587ca66d760cea9f07d34a42ace
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:662b6334c16de163e0b580501bc92071c1313477f537415a08f3fbee0d280541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350950145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27719bd33c5a93aae866d36ebc263ce7ce858898a8f0f4d0622d6a3879708045`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:39:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:45:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:13:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a10f86d641494b5e6b1c3b8b85409baab7c4d325c9d6b292a94180331dd6b765`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 48.7 MB (48670580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bf1407f5d0a1803a6c62439e0f74bbbc4e011619cdf8ff34937549c5edb22d`  
		Last Modified: Wed, 22 Apr 2026 01:39:36 GMT  
		Size: 26.9 MB (26858023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb520314033b68a9910f325620ed50a6717748b6e8e41c11cc49b358fe8947f`  
		Last Modified: Wed, 22 Apr 2026 04:45:33 GMT  
		Size: 77.0 MB (76973825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4aa447559ff0eb737d74e199cf6b7af9d10433145136ced3c42e5c4fcc2f709`  
		Last Modified: Wed, 22 Apr 2026 05:13:48 GMT  
		Size: 198.4 MB (198447717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ecb40c97f79a02a19e06f3fb767b98ddff4360a0d2ee77af95a88766fa9e7a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16891273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89daf9640646a297187394c2f03bffd597160a9eaf3dd7e1f0a5fb79e40835b3`

```dockerfile
```

-	Layers:
	-	`sha256:d55c8a43626ad669ff15b6dfb7692b8eab6f6f72376cebbfeb9eeca0156c5817`  
		Last Modified: Wed, 22 Apr 2026 05:13:43 GMT  
		Size: 16.9 MB (16881140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101ac5ae85414e46870c986f447cf92218bf51ff6ae8cb1589c7d6f042e7e2d5`  
		Last Modified: Wed, 22 Apr 2026 05:13:43 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e1fe6842a931be20b5e479b82993b403b11dd4bd0aa6f473a6b12def0523eb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.2 MB (296159891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e433b24ab35f05b4996c7c4d76888d366c9820f65d121d7a9b286b26d9944515`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 02:19:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:15:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:954ecf3bb623246e76e048be8db255040be0be61ff8078225017790f93fc2baf`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 45.6 MB (45607386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4a57ff6691b334a65a098db05baf2d825403eba2a4b68b46ed1f8e5631b721`  
		Last Modified: Wed, 22 Apr 2026 02:19:27 GMT  
		Size: 24.6 MB (24571415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7503e8d389d3b018f5a8af46a1adf37cfb06de0bf229b0de9a3c362974c271e`  
		Last Modified: Wed, 22 Apr 2026 03:52:38 GMT  
		Size: 71.5 MB (71484386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5addc4f780acde4341c6e9ceb84f8cb970e4a3916cd86791a1e6fbecac62d5b`  
		Last Modified: Wed, 22 Apr 2026 04:16:26 GMT  
		Size: 154.5 MB (154496704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8c592cb6afa1d13c6fd6b9464ecf83b06e9d2f49a6fd107c0236078a62778bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16646426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af3116bbd8f1a9215e5371d20e4b5b4152b7d667eb15ead10399660af38583f`

```dockerfile
```

-	Layers:
	-	`sha256:858aaffa70726d01b28a78eacb47fa73868f95e32f02e946c0a597b555bcfe16`  
		Last Modified: Wed, 22 Apr 2026 04:16:22 GMT  
		Size: 16.6 MB (16636229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e0e89a4cbac5746f613b0cff28c833192edb1ddf3f5ca45f02f9bf666ee4214`  
		Last Modified: Wed, 22 Apr 2026 04:16:21 GMT  
		Size: 10.2 KB (10197 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:39a66ef96b47b73f362e143b0f0a7749c8bff45876681085b155bdeb633a0980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339201535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69e954df6368309ed7530c30dcdf3f2f2a636b8fb879e3e486776f7c01a559f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:17:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f7ead27882db0d1de6eb6e496d384f406d278f217abdf3e3c50a235ce7737146`  
		Last Modified: Wed, 22 Apr 2026 00:16:20 GMT  
		Size: 48.7 MB (48711371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36d1ad0e4ab39e59341cbcc6c49601be7cf05a2f81f334bc0215a0d3ddd3d6e`  
		Last Modified: Wed, 22 Apr 2026 01:43:34 GMT  
		Size: 26.1 MB (26142281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5418b7c9b07059adb828d8a810a5c248d9886119502e1a246c8454ec1d4f00e8`  
		Last Modified: Wed, 22 Apr 2026 02:32:51 GMT  
		Size: 76.1 MB (76099498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd4a97cd37f749c1a411aea0afd1afa23738cf546059c0682088f3d75bef9d4`  
		Last Modified: Wed, 22 Apr 2026 03:18:12 GMT  
		Size: 188.2 MB (188248385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8d3719e749e951946521190a54cdcf1711cde7e994a974ef3572a6d08836e8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16973740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484cd117f03a1a43525af1cae6d310441c8c66cd9a4475f7705b689261521452`

```dockerfile
```

-	Layers:
	-	`sha256:6bff7b4453841d0f12cba01790ab04e77d78f16bf0d3bf550467e581bf131bb4`  
		Last Modified: Wed, 22 Apr 2026 03:18:09 GMT  
		Size: 17.0 MB (16963527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cfb4c175eebdaa20fde98e3fc7ccc8215e7009c2069e39c33fa6a8d08b462cb`  
		Last Modified: Wed, 22 Apr 2026 03:18:08 GMT  
		Size: 10.2 KB (10213 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5b5e2ff338c1d962a606acc37c77cdcc8ed52240119c2432efbaaac52a8467f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359097363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fa319444fe783fcdfc4ef6c8e95e5edca41c9ff62369c12741b5777e2525b2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 01:46:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:41:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:19:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0c3eef9d9722af9b5785c5725c5b18d448456ee05c327ddf5310134754139706`  
		Last Modified: Tue, 07 Apr 2026 00:11:45 GMT  
		Size: 50.0 MB (49993711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c9bb2730bc0ff710016a40d05d0bbd6ab5db1f6ed39dbb5569902bdddb97cb`  
		Last Modified: Tue, 07 Apr 2026 01:46:36 GMT  
		Size: 28.3 MB (28287053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61d37ae8d9569041f72a5d94976af076721a00ef2857d8844925e31d049b859`  
		Last Modified: Tue, 07 Apr 2026 02:41:38 GMT  
		Size: 79.3 MB (79338598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f118897ad1cad22ffbc07eea21e56c9dba3b363c220c4464bc468f0a8ca57`  
		Last Modified: Tue, 07 Apr 2026 03:20:26 GMT  
		Size: 201.5 MB (201478001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:404f5ba49f9f83d56221fb27fe93f99874d8d49645a551cee354c4c8fad2d14d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16840346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d574dbaf89cdece4e7639c1619f2343892105df4dcbbf6385373e3372ed8b3e`

```dockerfile
```

-	Layers:
	-	`sha256:6d9cd8bf765f1501d02a3a65b3da8023e2e905676753e0c3fa68c8056094d8c1`  
		Last Modified: Tue, 07 Apr 2026 03:20:22 GMT  
		Size: 16.8 MB (16830235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27a2e8d90b3967baa2c7dda33c2a3f6daa8384395974fc330119e74c774414ee`  
		Last Modified: Tue, 07 Apr 2026 03:20:22 GMT  
		Size: 10.1 KB (10111 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5b4928f1105718f64d49f9260f5415c04f48e2848e6adaebb1d31210d3388a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.4 MB (359422699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c2e9ea180a08bf5af2e4619f028260b45ac483c7c14e33810a4ad0457f2dfb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 04:22:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 09:53:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 18:12:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8091a6b5ece83586bfb56b6975e0b2d9bc01c78d84b526c5c6e82463bb755232`  
		Last Modified: Tue, 07 Apr 2026 00:11:11 GMT  
		Size: 54.0 MB (54001950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3485868c65e901d140674210bf2ba257ab5ac6120dded36f6536c4e9c5178623`  
		Last Modified: Tue, 07 Apr 2026 04:23:16 GMT  
		Size: 29.4 MB (29412504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03748ec5472f740753f922099fd48a5c13afbc87f15362a543b090bfa949e6b`  
		Last Modified: Tue, 07 Apr 2026 09:54:16 GMT  
		Size: 83.8 MB (83763893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025c0f95360ce011930b4e5c1251aeb95e6c660c0d7b16f1d863f0eafd278973`  
		Last Modified: Tue, 07 Apr 2026 18:13:31 GMT  
		Size: 192.2 MB (192244352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:345757d37078fa63d220123f94d68fcc0541df3ef22d308f0be804723aa7bbb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe77bf335dce5b86cbe64059d459156489df4421f9757460e78556650f452e1`

```dockerfile
```

-	Layers:
	-	`sha256:7a35b258e2d74022d399695e9b9af36615073df88ac09d4559ae159c991d8e89`  
		Last Modified: Tue, 07 Apr 2026 18:13:27 GMT  
		Size: 16.8 MB (16811993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c538a50620f49b50785bc27c82f4b203287063a9d8351a4dda04b7fbee4425c9`  
		Last Modified: Tue, 07 Apr 2026 18:13:26 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:816b6c729a21ab359a55b4b25f19ae5642195be096a69bde8114c6b17237d763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.1 MB (476110125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b66db7925ffdfeaf01302c6d4006a2d6ca1666c7e95b206f02d546448e96c88`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1775433600'
# Thu, 09 Apr 2026 01:50:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 11 Apr 2026 02:52:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 08:41:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fd96dd3de127541ef7e3bc5f9bc63bfe49b8f35d0526495ebca95ce89fe40405`  
		Last Modified: Tue, 07 Apr 2026 01:43:52 GMT  
		Size: 46.8 MB (46786906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9b785d28162b0b158cf1aa6f3a70ac887d4e1f003e08018a8a82c545e382db`  
		Last Modified: Thu, 09 Apr 2026 01:52:08 GMT  
		Size: 26.6 MB (26587111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346b9eb0dbc30d738e4ada815d4c1a60b004d3e4e257ce261f7e827b021d2d90`  
		Last Modified: Sat, 11 Apr 2026 02:56:20 GMT  
		Size: 75.6 MB (75595011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4b5026b2d0cbc65ab21d092e5985b01fd87278c99914368b614695184a2744`  
		Last Modified: Sun, 12 Apr 2026 08:57:13 GMT  
		Size: 327.1 MB (327141097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fee3dbf150499ce32bacd6b74b1b70c8aa975d209ac0c982678aaba8248da6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16927903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a832b3bff63ad5384bc42944daf33851e11c07c4af4d260c71c346997ad248f4`

```dockerfile
```

-	Layers:
	-	`sha256:38e2c1a5b6137ab164713e8263cdcd1520a09f028fb01a23d1434bcc96ac8a2a`  
		Last Modified: Sun, 12 Apr 2026 08:56:27 GMT  
		Size: 16.9 MB (16917739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e2099f0934a7b1e5c4066a198a3b83b1d6335279ecad59573b33436a1852842`  
		Last Modified: Sun, 12 Apr 2026 08:56:21 GMT  
		Size: 10.2 KB (10164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b0992a25762c699266b7f8e25dd5d74e20bd5de191980b636503983777c5244e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.1 MB (324061037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d03c7ebdbd2ecab99fedcb63e3ced5b6517b08ec94c339e0be655e56da0fed1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 03:05:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:54:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 06:00:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0f4e3a27ede4ed598ceeca73aae5842ded1c7c01f18c06d6c08d11ba5ee2f57e`  
		Last Modified: Tue, 07 Apr 2026 00:12:04 GMT  
		Size: 48.4 MB (48425378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3603919d864d726efd51563d3638c0f58e2671f83ef3d775155f64a94b910d45`  
		Last Modified: Tue, 07 Apr 2026 03:05:17 GMT  
		Size: 26.8 MB (26795763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae2afc6f5b4c5dd73680a5531235390e280e79ddf6ea03c9527bb4f35951d71`  
		Last Modified: Tue, 07 Apr 2026 04:55:17 GMT  
		Size: 77.7 MB (77717531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad6cb06f53e66da0009e766994bcd14606d4553c79c26dbff4c59333828f219`  
		Last Modified: Tue, 07 Apr 2026 06:01:09 GMT  
		Size: 171.1 MB (171122365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:434b7d8c4eda503143b939c4a4b3f7013d4c581f167b402a8b0ed71964cf6356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16626229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a226e17b86fda26d07c1a446dbd8b9238a6956fe89cebc3cd0c22129e675e87`

```dockerfile
```

-	Layers:
	-	`sha256:a6bb1ad1279f9fbac1e02b5de48e1000cf7d126dae9bb8a40f15bbfbba8f37dc`  
		Last Modified: Tue, 07 Apr 2026 06:01:05 GMT  
		Size: 16.6 MB (16616097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:534a1d3fe41475e38271409594c13a7de2a7dffdcddf1ac6f2e1dfd53319ee8b`  
		Last Modified: Tue, 07 Apr 2026 06:01:04 GMT  
		Size: 10.1 KB (10132 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:7a6090ffb69105ac7c5f0c2e8711577dbd925da5e4e059020aa40e9355d3d722
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

### `buildpack-deps:sid` - linux; amd64

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

### `buildpack-deps:sid` - unknown; unknown

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

### `buildpack-deps:sid` - linux; arm variant v7

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

### `buildpack-deps:sid` - unknown; unknown

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

### `buildpack-deps:sid` - linux; arm64 variant v8

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

### `buildpack-deps:sid` - unknown; unknown

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

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:82d4bcb374c7fd1af1ee8747c28b0366eb60f181b92fa85f80cf009d5debabf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358642936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14dd5610930902d66692fd0e9d640b59eafee012932c816119ecaba2e058c952`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:42:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:03:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 08:19:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a68ed28706ac755be40447c885e7277b571939be826b0bcf8abd61cb9be646c1`  
		Last Modified: Wed, 22 Apr 2026 00:17:10 GMT  
		Size: 50.0 MB (49978211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7cfb20f6b3b5390ccac8a81632157b49e22d10f507d3bbe6cf94610b6b670b`  
		Last Modified: Wed, 22 Apr 2026 01:42:58 GMT  
		Size: 28.2 MB (28174088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98a7761248e7742b078bc0b24d539eab94bafcae0d639821bda25ab2a661d30`  
		Last Modified: Wed, 22 Apr 2026 05:03:53 GMT  
		Size: 79.1 MB (79132936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6488df43b4d31ce198b01bd44f6204bd1ef14cb679dd9647286c27a1d3fba852`  
		Last Modified: Wed, 22 Apr 2026 08:20:30 GMT  
		Size: 201.4 MB (201357701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:618207df7178230666739ebb6a2b9766a735053a93355a7953edf8c4681cafa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16860286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb528a8f22807729edd70facf1c0ced2e6a60ed8939354977377f4de08263b46`

```dockerfile
```

-	Layers:
	-	`sha256:d9ca7485de9532031dbd3504f4f13a8aa5957b16bf16e8557f79b95254e6dc0d`  
		Last Modified: Wed, 22 Apr 2026 08:20:26 GMT  
		Size: 16.9 MB (16850175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80d8abc0696fa5e8d59fbc71009e83a54add3edbd691fc740f34900f2dc96078`  
		Last Modified: Wed, 22 Apr 2026 08:20:25 GMT  
		Size: 10.1 KB (10111 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

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

### `buildpack-deps:sid` - unknown; unknown

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

### `buildpack-deps:sid` - linux; riscv64

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

### `buildpack-deps:sid` - unknown; unknown

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

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1c463076187f2d0f464212d8a46e87b4a4af8d9cacc0380dbfcb8ea60b0e5a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.7 MB (323656483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6650868ae8629baf35877cebf6a5045bf42e48d5bd6d1258d3a221a080fa79e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 02:32:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:21:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:13:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7b993b1f311a8e0a662fe34124c78c97a70f47ef43d775021c60d64af67fe6f9`  
		Last Modified: Wed, 22 Apr 2026 00:16:09 GMT  
		Size: 48.4 MB (48410950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03da841295960c3b83bccaa55b6f75ac7e7d9ef75a26fbbd602f5481561c77d3`  
		Last Modified: Wed, 22 Apr 2026 02:32:24 GMT  
		Size: 26.7 MB (26657576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb23502aa51fc401ba9db804ddee38956ccdeceac365b46a11019e1d90b6bfe3`  
		Last Modified: Wed, 22 Apr 2026 04:21:30 GMT  
		Size: 77.5 MB (77478239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f14699de287ba8e9d13954dd38ec2dee73aec87be8e7ddddb9840abbf20544`  
		Last Modified: Wed, 22 Apr 2026 05:14:48 GMT  
		Size: 171.1 MB (171109718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1280d42a982adeffd7fb0ad40e9b932828433397cc5afa620b8e81e2e97b4a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16645389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97718d70936680fc343410502143a381e554ff6ad973a615be00e41a9055484`

```dockerfile
```

-	Layers:
	-	`sha256:1a433fa3d693d47784dc9463a3ee0cf089f75fc73b8c397e9ff5cddb026eb5ae`  
		Last Modified: Wed, 22 Apr 2026 05:14:45 GMT  
		Size: 16.6 MB (16635256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b608a32cda2cb749e227e2207c3629770febacae242c0648f927fab61f08e6`  
		Last Modified: Wed, 22 Apr 2026 05:14:43 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json

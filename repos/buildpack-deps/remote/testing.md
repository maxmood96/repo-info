## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:e86561fc8dd7220da0513f98adaffcfece1ac33f88273edf0ca0989ddb5dd9ae
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

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b96355b5470b3f409c20dd72a21f7d4e96a56cb7adf0366222bfbcdcd7749618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342769424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17222fd34f8f1d36284f483681517937dd0261045c9f7f2330158de82e38fe15`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:42:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:28:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:17:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e7ee730174f13176a4a2ca706f251743bedcb5459da1b8f275d5b6bcc67c0aef`  
		Last Modified: Tue, 03 Feb 2026 01:14:19 GMT  
		Size: 48.7 MB (48655735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8e2c9590f8317f5d54b9d2db2e9be22b3330f9ceb6219eb4096cfb413265a8`  
		Last Modified: Tue, 03 Feb 2026 02:42:39 GMT  
		Size: 27.2 MB (27196128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aa17b0ddc50d395845bdd09d93ab894b9905dd95eafe4736c08407b106537d`  
		Last Modified: Tue, 03 Feb 2026 03:28:40 GMT  
		Size: 68.5 MB (68503635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3159aabad69c9ff3db2673a5df9405fc087bf9c7dc9295608d333dd0c9a9d0ce`  
		Last Modified: Tue, 03 Feb 2026 04:18:13 GMT  
		Size: 198.4 MB (198413926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:90a34a0c6803242f5405ca802a6002cc75072c2203218d005f4c8c891c699d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16380205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1239cb7098d0260aeca1453b61dd6f05b272238f68a00d05b318ee9a9759e8`

```dockerfile
```

-	Layers:
	-	`sha256:89870cac10f2dd93c8e9619358ba3fb2bd709e35a646f41dd25138318eda0261`  
		Last Modified: Tue, 03 Feb 2026 04:18:06 GMT  
		Size: 16.4 MB (16370061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04dec6218c81794d71467d120a02d8bd1ca63183d92cbe68c59651a54387ac50`  
		Last Modified: Tue, 03 Feb 2026 04:18:05 GMT  
		Size: 10.1 KB (10144 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0394737a43abf30a650b2a37647c9891a7e36a9eb405d6ac578893b14df2d464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291676371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b614020705b5c0f1b0dbc3774ef27695f6422b00013c737e6b3e7ec226ca8de1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 03:31:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:00:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:21:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8ad4a919778d324780b6dee51af6abcf1139f6d57c0ba625c1995bf19d763478`  
		Last Modified: Tue, 03 Feb 2026 01:14:27 GMT  
		Size: 45.6 MB (45620616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70526fc33f5a0e4c0788e8433d79a8b805fd260b73e79eaf814e95eb7da57f6c`  
		Last Modified: Tue, 03 Feb 2026 03:31:37 GMT  
		Size: 24.9 MB (24909019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba24a1b1a8d776bf814627fa1af9e3e64f0dc70fb3fb856759b225c8fbc0bd5`  
		Last Modified: Tue, 03 Feb 2026 05:00:57 GMT  
		Size: 63.3 MB (63349339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f0a917deaf01bd0be6d7699117faeab85be72857d50727c6943169f735649a`  
		Last Modified: Tue, 03 Feb 2026 05:22:32 GMT  
		Size: 157.8 MB (157797397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:300142d432f0d8945f7a6c8949785c53420b04f8c12fdab8602fa6b6c592bd96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16135846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096618ca30a8e2f854ae5563e0ab861f819bfe7245619daddb3d9bfd73eb13ad`

```dockerfile
```

-	Layers:
	-	`sha256:f7635d2c2c75df46a3f5f8bd4205c3d5ed4c7663b1531765924d0ba836c16680`  
		Last Modified: Tue, 03 Feb 2026 05:22:28 GMT  
		Size: 16.1 MB (16125637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c12f41b215cd5098ed4b886b42e9010da2f7c121c26042630884adda5583a69b`  
		Last Modified: Tue, 03 Feb 2026 05:22:27 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:61479b52d4305f786f1b332297d7c49b847908ef4a130075dda2ac742b7a08c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.4 MB (331395307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b956cfdf604a35cd4fc68e370040e19c409e61674ec652da8d5ad586b9c20f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:20:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2309f92dd0c61c985b2d0f865b8d146291a99f7a179b5a243da4f72d2cb33817`  
		Last Modified: Tue, 03 Feb 2026 01:14:24 GMT  
		Size: 48.7 MB (48678525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5e89716ddee93a128c0808e16d7143a2c6bbe2184dc60f5736259c43d5203b`  
		Last Modified: Tue, 03 Feb 2026 02:45:45 GMT  
		Size: 26.5 MB (26513511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e2d41dedbf747e0d83a9125640a712f58e6c37b51e5ef213a2ac2c43d302fd`  
		Last Modified: Tue, 03 Feb 2026 03:47:11 GMT  
		Size: 68.0 MB (68001160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8910dc4ece7875faacf8c3e126c081accd1e4b2f8c8cb7a6d1f20bcf27dec3bf`  
		Last Modified: Tue, 03 Feb 2026 04:20:43 GMT  
		Size: 188.2 MB (188202111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3de90251f55ecdb5ad6a045e099ce0de7bb1a8732b93c6944a96813005cfce75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16469285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10de4d36739d08560c8d0aaa82ec9a5771dbe0b53b2c84dab854184bb2cc25ee`

```dockerfile
```

-	Layers:
	-	`sha256:28103e696860f5beac0a88063f40e60060c9cb84a51806133ebf07320dae656f`  
		Last Modified: Tue, 03 Feb 2026 04:20:39 GMT  
		Size: 16.5 MB (16459060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:381f107747186f0a65b9d1d861f107d6df7644e4d7c456c9c24b4c2fef42e833`  
		Last Modified: Tue, 03 Feb 2026 04:20:38 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ee6fe9c0bf7d22677fe5e3e6ffb3a5b99296863d618a5414af897e8227351699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350469417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618f1d37404038141b566e017b8c1be8325ee417085564cba7b9a8a8448f734c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:49:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:17:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bd6304d6e56f66e13385dc7464436c6e3933118a9e5b697acc2b57e9b6d5e5cc`  
		Last Modified: Tue, 03 Feb 2026 01:14:23 GMT  
		Size: 50.0 MB (49981936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1219332a3ab84c1a8edc635c16cc9d1b762a36e8636831f5a2cc5683909cd520`  
		Last Modified: Tue, 03 Feb 2026 02:49:49 GMT  
		Size: 28.5 MB (28480618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240b56e3bcda90a106c71ebee75f0a510a0954e32f6c4d9c0c5b11c14481cd05`  
		Last Modified: Tue, 03 Feb 2026 03:25:16 GMT  
		Size: 70.5 MB (70456532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94da87e7b0541d5e9792b0f95b143f480e5fc15a76b42700adb8889e90de32b`  
		Last Modified: Tue, 03 Feb 2026 04:18:20 GMT  
		Size: 201.6 MB (201550331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cfda5557398d6afc975ddad838fd8db278432f32c8607cf33b5559b2daa3f166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16349865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f891b6f40be1c27addaf999c4fdd7032d358873109e10e5939676c14890d92`

```dockerfile
```

-	Layers:
	-	`sha256:e6deefb78cd27718f4eafe3435d96024a2854aa338b12ee060a3b48bc5b27aa5`  
		Last Modified: Tue, 03 Feb 2026 04:18:14 GMT  
		Size: 16.3 MB (16339742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33e497c7e6f0a319106708b06043435605f9d8a8e6dda0767a97f07da17bbf5d`  
		Last Modified: Tue, 03 Feb 2026 04:18:13 GMT  
		Size: 10.1 KB (10123 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:243eb73ce490724d24bd2c4d73a61a8f15c633e32c3ba9ba4b719d9ef4442bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.1 MB (355080406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddcafea609b2778c00416427393c42a9b43699d1379f24a5f2876c111d6a1f7b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 05:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 10:35:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 12:40:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3a0a026d4bb771de47d622d680861a5062bd4e0c02e6c2d817a503a12b7411ab`  
		Last Modified: Tue, 03 Feb 2026 01:13:26 GMT  
		Size: 53.6 MB (53582665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f4250e1c3eb2c2760041ecc5b52913cec79884bf114b72d39c757b1f167fd2`  
		Last Modified: Tue, 03 Feb 2026 05:23:27 GMT  
		Size: 29.5 MB (29483172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f3c68e830ed82187035ea008bb468634ad1302ffceb34266c98b8993788f30`  
		Last Modified: Tue, 03 Feb 2026 10:36:27 GMT  
		Size: 74.0 MB (73996483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49458d34d80c1d44d17866871fbb87343aef3d605fff689e370d26f985e28bff`  
		Last Modified: Tue, 03 Feb 2026 12:41:44 GMT  
		Size: 198.0 MB (198018086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c4fac6ab5ee36b6962a62be173ae4c373d8507397d108eaa07fc7277b15c2b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16356398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc91b670e83ea50f1e8ae7cd7e6ae63561f5f710457a8de6442f3ca20c66bee`

```dockerfile
```

-	Layers:
	-	`sha256:c002a9ca3267159439164414f97de8b4876bddd977180c6dfb0fe9f864772bd3`  
		Last Modified: Tue, 03 Feb 2026 12:41:40 GMT  
		Size: 16.3 MB (16346222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07aecae8ac62eaa92053bda69636b6e8fef928b2ff7bbbe82ee083e0804feccc`  
		Last Modified: Tue, 03 Feb 2026 12:41:39 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:2836a5546aac7c049d5ea1a1082d11b0e48a9235dca10169a14ddddc856b1736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.0 MB (461984265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc862beaccf7384110c76cb048fafe7f13d611841223fc59f76b3694632b5b9c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1769990400'
# Thu, 05 Feb 2026 03:11:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 06 Feb 2026 07:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 07 Feb 2026 23:08:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ece60484d1aaeb903414963cab1787d15893d1a58b4ec6ec87b0134b50ef7435`  
		Last Modified: Tue, 03 Feb 2026 06:58:42 GMT  
		Size: 46.9 MB (46895192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f88f8722794589cf75351e2b9fadf7d30449a05a8e6dfa935a1d316b807054`  
		Last Modified: Thu, 05 Feb 2026 03:12:58 GMT  
		Size: 26.7 MB (26744489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910a4d2ff1b6362b5eaa0d4cd74b0f9a8b4bc0c6abf971675b4857305059353d`  
		Last Modified: Fri, 06 Feb 2026 07:47:55 GMT  
		Size: 67.2 MB (67239350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49586937bb1dbe1c78767b42f350975041264d816e925ea343c4cef0dca87a0`  
		Last Modified: Sat, 07 Feb 2026 23:23:58 GMT  
		Size: 321.1 MB (321105234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:70964b934d50dc9f70514f64046ffa784ff799580fd25f2c5074c469960b295e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16425786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd387279892e76381f8419bb29a98d181588bab917da7f7957ffe169e9c159a`

```dockerfile
```

-	Layers:
	-	`sha256:29f9d656c9a24b3f19e1b5b596b45663e73d0fe5db817b65357e4f75d2466034`  
		Last Modified: Sat, 07 Feb 2026 23:23:15 GMT  
		Size: 16.4 MB (16415611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401035021764c1686b6ef81e2bf980a0e6bf17fb5e34855e8b7672caa22a90dd`  
		Last Modified: Sat, 07 Feb 2026 23:23:10 GMT  
		Size: 10.2 KB (10175 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0b63cb1de609b0cd48a43891a15ec17af0fa96d25adb034cdcf8b1cda962974f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 MB (315737528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060c34ce7323c6d6258b5c15df21b83513f8ea8ca3ef9118659147e6442e04f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 03:44:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:28:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 06:14:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:616d765aba14d266e800a78cc4d0cdbfd95c5d967a141135b80d41a64ad5ee62`  
		Last Modified: Tue, 03 Feb 2026 01:12:49 GMT  
		Size: 48.4 MB (48429330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc16728429c562a41c48a34a273412791fb028a15a3f8cb028d1c50e5d9cdd3a`  
		Last Modified: Tue, 03 Feb 2026 03:44:50 GMT  
		Size: 27.0 MB (27000391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdd7874b8fd05d992321a432b1fb0884fd4964892aa7c7c8d0f46e49bee7f92`  
		Last Modified: Tue, 03 Feb 2026 05:29:20 GMT  
		Size: 69.2 MB (69167422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a4b52125a3551d5742c691558f28b9fed046d3ab754724dee0f76fa934cd63`  
		Last Modified: Tue, 03 Feb 2026 06:15:28 GMT  
		Size: 171.1 MB (171140385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9ae012685b9cff8c9e314b1a7a412c2bbacfce25de11513e0897972d78bfc639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16155580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ce5cdcd116d68fa192ed9cd21aeaf06e212b490d2659c9ce633f9db91760f1`

```dockerfile
```

-	Layers:
	-	`sha256:3fc12ae571147500e0a96231d52b8fb922b2207825e2ca421350a770864f9978`  
		Last Modified: Tue, 03 Feb 2026 06:15:25 GMT  
		Size: 16.1 MB (16145435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c7e26867c5fa51039761bd8ba07fbe1e7f5e106f13c7788db6024c617ff0e1`  
		Last Modified: Tue, 03 Feb 2026 06:15:24 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json

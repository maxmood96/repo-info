## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:2b7b8dd02c5666d23a990b714a066b79f973963b03aa0e214ac03fbf3f75607b
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
$ docker pull buildpack-deps@sha256:8eed693b06aae14f4862f9437aa3a5aa29978076f14a6bc125cfbd410269b542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.4 MB (353430182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f618a3aebc097bd55a1bbe917c291a509dbcc59e4df4b6519c5fcbb164726869`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:04:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:36:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:501906f379a13fc3675791cbd6304f648074973affcb965be0bef8b0aaa34ab5`  
		Last Modified: Tue, 24 Feb 2026 18:43:03 GMT  
		Size: 48.7 MB (48677181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9812e820910835e26da6ba184eb7321a186fd35437a98105291c93a0a34f38b7`  
		Last Modified: Tue, 24 Feb 2026 19:19:41 GMT  
		Size: 27.2 MB (27222255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36180328906d965e580f744725c6261f12098fe1efe44eeb2da08199e6ee80d0`  
		Last Modified: Tue, 24 Feb 2026 20:04:28 GMT  
		Size: 75.9 MB (75871742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b7966813dde68548ab619d9e4140fd1eccd2db329f344d64a2cf80f6a346fa`  
		Last Modified: Tue, 24 Feb 2026 20:37:15 GMT  
		Size: 201.7 MB (201659004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f9adb3fe94a52aa0dc1cbbe03b1403d020e2bef71d96e0dab33e73883402920a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16856053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ebc9b98c1f1f715ec23c71c22f74ba3528f7451ce27c2d3ca7b1a073eee5b0`

```dockerfile
```

-	Layers:
	-	`sha256:54d8f813fdde94526dc46d7fec19c946dfa834aa735a91952c0e5a27b8f6abb7`  
		Last Modified: Tue, 24 Feb 2026 20:37:11 GMT  
		Size: 16.8 MB (16845908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:669a44813c6776786aef7258f3f8ae36435356a5943e9c6f3e7bcc14dbc8c7b1`  
		Last Modified: Tue, 24 Feb 2026 20:37:10 GMT  
		Size: 10.1 KB (10145 bytes)  
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
$ docker pull buildpack-deps@sha256:1c72430a075caecb1976f8333a21d520319320affd2fa8baf7df29d5d50b8cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.4 MB (361447201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3400b5fd5cbc4012de066ddc23afeed9424a11e1d205721606e79f347264fea4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:24:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:57:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:18:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:143f133830d056570eb26009a5886b146c40a6e16bbee60113f54a6baa1643eb`  
		Last Modified: Tue, 24 Feb 2026 18:42:19 GMT  
		Size: 50.0 MB (50011968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9094d4208101e32ebf3f9d4d940d804f0a8bcef435b536316812340ebc9e6f8d`  
		Last Modified: Tue, 24 Feb 2026 19:24:54 GMT  
		Size: 28.5 MB (28495165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00249243cc2c65987ecc868e9f3e1513e31c071138c52e8314c3d36de9f9f3c8`  
		Last Modified: Tue, 24 Feb 2026 19:57:24 GMT  
		Size: 77.9 MB (77874431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b53f4a780a89c1e71eec3050de17871c483e596e73f9450b679a77e16993fce`  
		Last Modified: Tue, 24 Feb 2026 20:19:36 GMT  
		Size: 205.1 MB (205065637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cfe62629ea511aa3fac7adbe4eff572e07ca694a85fa14dee0e35dc6f0ccace1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16825106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e1407a042fba059229073a511d92ff167beb985ad3da08ea256af2c1f48e06`

```dockerfile
```

-	Layers:
	-	`sha256:d5c0ec31351dfc1a150685f7d9415a1f82a4522b3151e0e1bc262ff193eade06`  
		Last Modified: Tue, 24 Feb 2026 20:19:31 GMT  
		Size: 16.8 MB (16814983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef5a5597968b0316817a15cc3be29b8ce53f538fc23a571d16a57402aaaf22ea`  
		Last Modified: Tue, 24 Feb 2026 20:19:30 GMT  
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

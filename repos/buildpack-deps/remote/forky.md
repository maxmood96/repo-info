## `buildpack-deps:forky`

```console
$ docker pull buildpack-deps@sha256:1ce85c61469d7764866ef45f3b2b8afddc7522cc1414ff6c44619c05fcc2501c
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

### `buildpack-deps:forky` - linux; amd64

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

### `buildpack-deps:forky` - unknown; unknown

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

### `buildpack-deps:forky` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8cd6198cba8f4dae6db2cacf3867b0cfce2393baa912a32780098ca5deac3292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301821371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958aad2cd61c7ff36fa324cac352f376d113c27ec691f847e5ba6128db13017a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 20:04:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 22:16:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b74010850dba4ef4e0d65d4c6bda126a2de154bff6afcac42cad46a2cbe16fc5`  
		Last Modified: Tue, 24 Feb 2026 18:42:08 GMT  
		Size: 45.7 MB (45653048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e2692d078b62360ce66efa48798cce1ada6ffaf0e61c3560fb4e15c2ba9d74`  
		Last Modified: Tue, 24 Feb 2026 20:04:20 GMT  
		Size: 24.9 MB (24920360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25208c70da66ab3bb8d85158eb796fdadd82a017ba00747c64f1e57f5bb9ee99`  
		Last Modified: Tue, 24 Feb 2026 21:35:08 GMT  
		Size: 70.5 MB (70451873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3361c9a8435117b262175d66e39e3c547c91d72dc70c01581d1cabdc179abe0b`  
		Last Modified: Tue, 24 Feb 2026 22:17:31 GMT  
		Size: 160.8 MB (160796090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3db7239a1d75acf2fb6ba91ade7aee080711e42362e99dc4838bca9d721d154d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16611210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48ba45b840f64e4c2a2a8b363b2ae327015f2664305ca209c8649e190eebc46`

```dockerfile
```

-	Layers:
	-	`sha256:c9cc7fa08b949ad2671d13e2c2708eb226da44b44dd7b9bff6e36fbe6f182140`  
		Last Modified: Tue, 24 Feb 2026 22:17:28 GMT  
		Size: 16.6 MB (16601001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:855b8c362f0d400dc02d50ff61bd31690b5549e0f59ba9853943d9f76e2c1fd9`  
		Last Modified: Tue, 24 Feb 2026 22:17:27 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c2d00d778487916dd7e7045c064ebedbf0079c39a42029a6f0525ffe974ed598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.2 MB (342191935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b24fdf5c53f56e8f216f2ccffed003468a1b290966ce8316eb0b9960f696a3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:24:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:14:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:30:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:dc3ce43fbcc581a6cb3e0909e03d7e31c0ff1d4d76469e15d6610d1403f2a7e0`  
		Last Modified: Tue, 24 Feb 2026 18:42:39 GMT  
		Size: 48.7 MB (48705026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa1e5eafe63e2070e8b626137e2f3ba642d42241f716e9259b73098475d4205`  
		Last Modified: Tue, 24 Feb 2026 19:24:42 GMT  
		Size: 26.5 MB (26532448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a430476590752e06253b24b421667dbd99ccf0ed685081b9027c9e6c0c4608`  
		Last Modified: Tue, 24 Feb 2026 20:15:06 GMT  
		Size: 75.2 MB (75176455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb85baa2df047cfa33556a25e0ba093a4fae8bf0edfcffe5b1166c9ea9cec56b`  
		Last Modified: Tue, 24 Feb 2026 21:31:09 GMT  
		Size: 191.8 MB (191778006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f17f963eb091684a4f892a6bd8ffc610da2d1b1ff47c359f2162e0f1c9a2ae7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16943797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80f2a02b6db06902956f1905c0da0460b65169a4fbe2ca7b6f3283dfbdab0d4`

```dockerfile
```

-	Layers:
	-	`sha256:0b84f281ee5ce84be7af5fb6d2eb9548aa9ea6bb276096d6b991e500e9ad9a79`  
		Last Modified: Tue, 24 Feb 2026 21:31:06 GMT  
		Size: 16.9 MB (16933572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efde5fa27b5a6c82114b97cfe7647b7b4df3945594d8755083f9d5da70181532`  
		Last Modified: Tue, 24 Feb 2026 21:31:05 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; 386

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

### `buildpack-deps:forky` - unknown; unknown

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

### `buildpack-deps:forky` - linux; ppc64le

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

### `buildpack-deps:forky` - unknown; unknown

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

### `buildpack-deps:forky` - linux; riscv64

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

### `buildpack-deps:forky` - unknown; unknown

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

### `buildpack-deps:forky` - linux; s390x

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

### `buildpack-deps:forky` - unknown; unknown

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

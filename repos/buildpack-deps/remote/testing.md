## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:1dc0363bc5064b871f3b2cf393a33cbfd026436f5717fbbfa2728feddf813401
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

### `buildpack-deps:testing` - unknown; unknown

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

### `buildpack-deps:testing` - linux; arm64 variant v8

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

### `buildpack-deps:testing` - unknown; unknown

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
$ docker pull buildpack-deps@sha256:748fd37df666ae003407b04af603cef02f5c80b6494f41353151a628d6a377e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.0 MB (362027964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0176afa3c9169cc86f0d1ff3d6a04d23b5a71255dcd8b731e8282bc604888311`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 21:20:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 02:56:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 06:17:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f1e7241652efbb83270036a6221c3c25c51e9feb8307ee3c94f7e0d52832e1af`  
		Last Modified: Tue, 24 Feb 2026 18:42:31 GMT  
		Size: 53.6 MB (53641787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa31de94cb423730059f9604b4ef3f6954ef0ad086f5d48144efd62317b2c2e`  
		Last Modified: Tue, 24 Feb 2026 21:20:56 GMT  
		Size: 29.5 MB (29513933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930837d0aa6df8d34e08c85803ff9b80030a83f236fe93d9e1ea4d7134b958c3`  
		Last Modified: Wed, 25 Feb 2026 02:57:28 GMT  
		Size: 81.9 MB (81942342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d73cceefa5bd4d8a06262c2034e237feabf6df22280dc171af731959b407ec`  
		Last Modified: Wed, 25 Feb 2026 06:18:38 GMT  
		Size: 196.9 MB (196929902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7040a61a3dcfac5fb066bf230cc51f933f48453cc4c0c43f80a9fa5e8ba72497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16807529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09408b21b30828860ad5879c2c4fbfc979c62f46a7cdd2f7fdc12cd8070d8130`

```dockerfile
```

-	Layers:
	-	`sha256:83a88d668ebc5f3c235e4ce7bb968b3dc9b3f5f2a662f055ba4c9e34e6f7d023`  
		Last Modified: Wed, 25 Feb 2026 06:18:34 GMT  
		Size: 16.8 MB (16797352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4abc4788eaf5e708445d092ac34a53694004810cd34b6e99ec01494b7d5c63`  
		Last Modified: Wed, 25 Feb 2026 06:18:33 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4a07117c40a71eeafa1f067471830ee9ccb74bbfb1ecbdfe13343c477789d153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **468.6 MB (468648172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5eb31e6cb42fe103ddad7a3bfee8af7c4702874d08084e10bf4d7c95a1bd75`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:07:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 26 Feb 2026 21:34:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 28 Feb 2026 19:33:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:db31b4401b1ad39bc8394e302320dc063e12e2c0464e6a8103701611daac2f3e`  
		Last Modified: Tue, 24 Feb 2026 18:43:31 GMT  
		Size: 46.9 MB (46914404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce7ea7a6a4533bb42137b98ae7cf7eb86a1fd6eefe9d713522264d613c05e62`  
		Last Modified: Tue, 24 Feb 2026 19:09:30 GMT  
		Size: 26.8 MB (26774378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ebef486f83ee0c702c262a6d5550673a0f1b78368f99bd1ce71d5e966d05ab`  
		Last Modified: Thu, 26 Feb 2026 21:38:15 GMT  
		Size: 74.4 MB (74379205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b16e39d37471c692ac6df897b04bb474eee60d703290f4752935fdc10a24d`  
		Last Modified: Sat, 28 Feb 2026 19:49:17 GMT  
		Size: 320.6 MB (320580185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f9c0e5337687790a07200eaa00aabb33cf8944c46444832b572dd6b2d85efb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16895223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b6b0f3fdfb70563f37211e755d59a2be7a26138c5c9864d87d89778a2e301a`

```dockerfile
```

-	Layers:
	-	`sha256:92c278ac18d4279c06690a127db5174d7096668ba4c3c52040137a99c5a1957b`  
		Last Modified: Sat, 28 Feb 2026 19:48:33 GMT  
		Size: 16.9 MB (16885046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:173fb54d825398d0145365446ef33f196c28634bbdfc9c52cd0bc87d9443c491`  
		Last Modified: Sat, 28 Feb 2026 19:48:28 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:335b3335f4d8360f00c28bf66c700be02143a00d1e0101ba1a37655062b66064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.3 MB (326314477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a152d0b3c1b0031ec18178927f97728106bd3d0186e06e1f5fc7abc57b9e7dcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 20:57:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 23:52:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 02:14:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f21354992e07f04a7de86938f41ff3c72cb8dc33252e2b2320b4169695270de1`  
		Last Modified: Tue, 24 Feb 2026 18:41:36 GMT  
		Size: 48.4 MB (48448352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bc3d23a1ad94963e56617c5ddcf27c1a360185386d60459632a29eefc99c91`  
		Last Modified: Tue, 24 Feb 2026 20:58:20 GMT  
		Size: 27.0 MB (27005253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96339ee6032387e57235bad6fbe6a63b35d2154d0ed8853524ee337a527c18b6`  
		Last Modified: Tue, 24 Feb 2026 23:52:57 GMT  
		Size: 76.4 MB (76433018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a970d5e9476197853dc258a861178bcf66850ea686e04fa4b573683a2fd87c4`  
		Last Modified: Wed, 25 Feb 2026 02:16:04 GMT  
		Size: 174.4 MB (174427854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b31b4c156f6ad13de5cb0bdfede20293b8ec0cbb96e8cbf9368b938e2697d6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16609992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c5aee1bb6eeb6eebf9ac23ead06e41d5c7f97451dc5dce167e8d8c04eaee9d`

```dockerfile
```

-	Layers:
	-	`sha256:ed66a42a8a64c7aef04c433d6f13024c2ef2d61cb6e7e216e148435e119f9fc8`  
		Last Modified: Wed, 25 Feb 2026 02:16:01 GMT  
		Size: 16.6 MB (16599847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28447f1f73823925c0ffdf309e57974701c8add19b813d288e34f9db7c650886`  
		Last Modified: Wed, 25 Feb 2026 02:15:59 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json

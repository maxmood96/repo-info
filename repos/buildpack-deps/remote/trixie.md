## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:209f968dfb1653e3ef8da539f96fc15efd52ddd60345dee3d04312cccaebacd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:57da03b95f7355a9bc8124edf56c88e1555d4e608f9391ffb226dfb42ada38d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.6 MB (367601750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538c285f33aeb3fc060e2d1e47eeca09205a2e163513b6cbb0e07b6965fd530d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:22:22 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Thu, 17 Oct 2024 00:22:23 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:07:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:08:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:08:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3af942d5f32a53d271e49824c635bd83b9f44545e34efa1a534acbcd19cf8c`  
		Last Modified: Thu, 17 Oct 2024 01:12:47 GMT  
		Size: 20.6 MB (20646136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631e0c8c5d1c8cd92a1b3ac1bedbfcfae442b261c1dd65bb2161aa4ce066fbfa`  
		Last Modified: Thu, 17 Oct 2024 01:13:04 GMT  
		Size: 66.3 MB (66301624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66dcbf6d205d4049f9b052c64fc66e09ad5794833cc4cfddc0b57bfe225e317`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 227.4 MB (227415249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a702af9257ea6649053fdb5c5801607a829b7d01672205b726401c8128e958bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.5 MB (335462987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322342ca71be45e54db169d641b33b9049fb9f8e9e2db499781674dd529d1c99`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:20:21 GMT
ADD file:3b9d682e7d68f9176882ad1aa7f4dcae0a81c3f93bb197b8d0a3982c411d2ae0 in / 
# Fri, 27 Sep 2024 03:20:22 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:01:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 04:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 04:02:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:655ea019a1ac93e4a06df6c69d688fcb77e3e8581a9c73eaec0ab2559d7233f0`  
		Last Modified: Fri, 27 Sep 2024 03:23:36 GMT  
		Size: 50.1 MB (50140675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5a645996979bd86734316a948faaa2699705e7844398497f9933957b686774`  
		Last Modified: Fri, 27 Sep 2024 04:05:36 GMT  
		Size: 19.3 MB (19272320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e33a076b656ffa1590cb3af11ac35caa4cafc5418c987ee43ff730ce6667124`  
		Last Modified: Fri, 27 Sep 2024 04:05:55 GMT  
		Size: 63.7 MB (63678959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b391cda3e9681d641f974d78e09b872a28e4dbbc868b58887bc63c79773685ef`  
		Last Modified: Fri, 27 Sep 2024 04:06:30 GMT  
		Size: 202.4 MB (202371033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cf5f7f2b3d1e7e053937847cd1d54aae5660d0b109ec06b1e37407c516026f08
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.9 MB (316886587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908e66f98eb6616f1e3e4995f88f43cac97b623cdf136f562ae4b5605d03b26d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:15:43 GMT
ADD file:13242b1f67d07c997aa23e4b688f29c3a6c6dd2678f15f8738e88d4e66cd5ad8 in / 
# Fri, 27 Sep 2024 05:15:45 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:35:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:36:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:37:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2e00dc0285e0f577d99c5fb34081dcf709cc26a9e85129b9e7bf7486f41e9f93`  
		Last Modified: Fri, 27 Sep 2024 05:20:03 GMT  
		Size: 47.6 MB (47633953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39e04951abf97af56dedf87c98cd7cc72052708138c6c90da2eaa7628520ed6`  
		Last Modified: Fri, 27 Sep 2024 07:42:12 GMT  
		Size: 18.6 MB (18628870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4d47835426771c44b0620b149b078b002436d04ae0a9cfd024e98d0dfd4660`  
		Last Modified: Fri, 27 Sep 2024 07:42:31 GMT  
		Size: 61.2 MB (61160733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d985eaffb50a16b04f512a5978f60707cec0ee2ee400d8df8eed0a4f2ae4e7bb`  
		Last Modified: Fri, 27 Sep 2024 07:43:04 GMT  
		Size: 189.5 MB (189463031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6eb1f5a4d0fbaa0738de62ec4ce5cad85bc0deab8318212832033be1d4e44227
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.8 MB (360841180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5170670a1b59e433d47ac1c2f5b6cbd4cb569be345029c90a37adc178439fa3c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:39:36 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
# Fri, 27 Sep 2024 04:39:37 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:23:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56925e2753eebe331e1e7850cdb33fa7fabb783a0365763734fb7f7fa68594e0`  
		Last Modified: Fri, 27 Sep 2024 05:27:28 GMT  
		Size: 20.0 MB (20038741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf179f048ad941b2de420899978ae9515fad2b4c8b83bc1eee392b5b7291c03`  
		Last Modified: Fri, 27 Sep 2024 05:27:49 GMT  
		Size: 66.2 MB (66249547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46608e24e871aeb173029569f11931335886e512f79bc654f51a4aa982f67d8`  
		Last Modified: Fri, 27 Sep 2024 05:28:17 GMT  
		Size: 220.9 MB (220936291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2b91b2c4a3bad4d9ca539d5e66c88676c35905609f44859fcd5aea80a2045fe9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.2 MB (372196464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1c3fe28c36742862af8a09005c05047fe29c002515384397afbcc1839dc6fc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:40:55 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Thu, 17 Oct 2024 00:40:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:07:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:08:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:09:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8bca6b1029fb346ac8c3fd8fd0242c8617b39ff467401ae5be38d72823e794`  
		Last Modified: Thu, 17 Oct 2024 01:13:34 GMT  
		Size: 21.8 MB (21756980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a074313195f31eafdde1ef7f85c59bf5ee3996435610f09e54f50d51a3f12d`  
		Last Modified: Thu, 17 Oct 2024 01:13:55 GMT  
		Size: 68.1 MB (68104739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d565f48f6689005ab9b62ffa6410974dc132aa18fbe0b32353a3060ae04731e9`  
		Last Modified: Thu, 17 Oct 2024 01:14:42 GMT  
		Size: 228.3 MB (228257287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e8b34340c491b168793c8194cf3ba79c7c8f75ea8811169bd87769e85581458f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345169031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b036904e38b7604d964773dc03770759f4897eb01f8881dc506b7ed1a27a90`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:07:36 GMT
ADD file:36ad397edf2d75e04dad5f0c65abe533f9f2e989bf5ea18e70a4df00cc6e490b in / 
# Fri, 27 Sep 2024 09:07:41 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:53:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 10:54:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 11:00:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b62fd707f1ed2218f3c1012d35ec60cef1c2b262cc2ca3f48b17a6725ccdf4b3`  
		Last Modified: Fri, 27 Sep 2024 09:15:53 GMT  
		Size: 52.1 MB (52096393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033fb77739bc0534e9ca7a6324d61a359557ff7525765c989f7fe43292a70678`  
		Last Modified: Fri, 27 Sep 2024 11:08:13 GMT  
		Size: 20.6 MB (20611217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816183487bc68f313f38e3315ac6bc39afe27875baa50865d4d9f7b974ebbe24`  
		Last Modified: Fri, 27 Sep 2024 11:09:04 GMT  
		Size: 65.0 MB (64999739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a51967b8f4cf1b2d850d26a139c5f1d7e8e41b709c161d9eee6061bc4dc74f3`  
		Last Modified: Fri, 27 Sep 2024 11:11:17 GMT  
		Size: 207.5 MB (207461682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7436b5b7db65cd5a624600a1deeef5c873d96bdad3f435f9fef4b991fa46a014
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.6 MB (377576280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3c82a2612f21cfb3e020d6a1179a1339b2674541a1bdbe7f3aae822f6e52ba`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:34:36 GMT
ADD file:330305dfad891b7801b7bc1444b22086f483c0101ecad9aa8a8e0d005896f0fd in / 
# Fri, 27 Sep 2024 05:34:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 06:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 06:01:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 06:03:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1c9d9c0ae5911d02f7f099685f31c9a3bdecfb20000d904113c26e622dbe3be3`  
		Last Modified: Fri, 27 Sep 2024 05:38:22 GMT  
		Size: 57.1 MB (57100357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02cae32b1fb8881345e1371c36b7be22b1f7ed12f1c0b8c022946020ef2ea67`  
		Last Modified: Fri, 27 Sep 2024 06:06:52 GMT  
		Size: 22.9 MB (22941201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c552054a471b4255e6efa87c7bc0c63ba0466655c5644bfdade3677310ec65c`  
		Last Modified: Fri, 27 Sep 2024 06:07:11 GMT  
		Size: 71.6 MB (71553163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f28b4807d4b640478c00c941befcc03e7516d529f7038a9e613825c62ecd05`  
		Last Modified: Fri, 27 Sep 2024 06:07:52 GMT  
		Size: 226.0 MB (225981559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9d5b8b5e2291d7c8cc065f3f18775309ccd2ba7d9bd1efaa8de0eb044d6793b0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.2 MB (342226166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397ef9bf1106f34529cc7819079b623b933e37a3488161ce834b76eec5ab53c8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:45:24 GMT
ADD file:62bc4f2057452df8dde276d456f3954e7e27a723040dd9314069695b18b4c75a in / 
# Fri, 27 Sep 2024 02:45:26 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:17:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d4e554dd357d755b1103e6fac1ca2fe641d4ec4ce0581cc222f4bffe8b54c0c`  
		Last Modified: Fri, 27 Sep 2024 02:48:50 GMT  
		Size: 52.8 MB (52771035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f683d43e465332ea4b3a44a602cd96364371abbd8a8e9766b4a056ad242572`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 21.4 MB (21394423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d90646a4948c3fa2abf48c8eaeef129e9547574cf2370fa04ecaed53f76dfb4`  
		Last Modified: Fri, 27 Sep 2024 03:22:17 GMT  
		Size: 67.3 MB (67256930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f620222e1943a71639f47a8405e2a62c61af833945aaefd53d6e4523b5853a8`  
		Last Modified: Fri, 27 Sep 2024 03:22:45 GMT  
		Size: 200.8 MB (200803778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

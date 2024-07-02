## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:9e130051835fd679038ebda5d0f146ed1a5777447beb8588aafb2142c27fafd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0ad72948407db9556b9fc94b4be240f2c3be0be497540d00b2ee1a189defe3a6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.9 MB (351938951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efc61521a2162fd787759eb5907af774c967afca63a8422d0e17b2bdc9748e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:57 GMT
ADD file:cf83030bc061e8d24d8a36b4edb2846333916985361600a06dfb635fd59c8068 in / 
# Tue, 02 Jul 2024 01:25:58 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:52:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:53:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2d149d696b13b9c3df064cbc77767f81d4635c7804547d50ff7da0c45c51990a`  
		Last Modified: Tue, 02 Jul 2024 01:30:17 GMT  
		Size: 52.6 MB (52634573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141f0a6d32a670095c08b9b66b2a2940431d5dfb05055fa488081211c5c31c55`  
		Last Modified: Tue, 02 Jul 2024 02:02:19 GMT  
		Size: 19.0 MB (19022788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282b146ad3f3822c7f15a1f42f4cecceab568029d29f1dfea9f25a23cbe136e0`  
		Last Modified: Tue, 02 Jul 2024 02:02:35 GMT  
		Size: 66.9 MB (66900352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af5a203fe34b4a4bf097ad0c1752a3468486e952dda35276e611017ba92da3d`  
		Last Modified: Tue, 02 Jul 2024 02:03:08 GMT  
		Size: 213.4 MB (213381238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:800ae82f42f4ae9145cc208c6b071b35aa39312a5ff1ef81fe5144f3d8eb38e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.2 MB (321216391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8714d40d259c2a0268c09819b2146228c7afbdbf5ce7067e4becae57264799cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:49:07 GMT
ADD file:e97cbdca31cc34df027df8a29da79dec8686613556a85f9e94434bf7952452ff in / 
# Tue, 02 Jul 2024 00:49:07 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:20:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:00d6074b8078def64a01fe6a6ae8b9b4c88fda262cf81e16d90c7e7f16541209`  
		Last Modified: Tue, 02 Jul 2024 00:53:08 GMT  
		Size: 49.7 MB (49697271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60563593e8bb3a3fcfcd7d9061a4aacccb82aa350743f3290a168dd08c3e89f`  
		Last Modified: Tue, 02 Jul 2024 01:24:52 GMT  
		Size: 18.0 MB (17969872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23186f8262bd00e188269c09360563f198acc4d7d678c6f5cf647da05eb8668`  
		Last Modified: Tue, 02 Jul 2024 01:25:10 GMT  
		Size: 64.4 MB (64364052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86df761666ea6f39ce81fd1b9937bcc09d0d9da8b71caea34f060cdab37e5e30`  
		Last Modified: Tue, 02 Jul 2024 01:25:46 GMT  
		Size: 189.2 MB (189185196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:da86615efc8fd15f6682e0f36eb526db71aec51c7f7ce1b323e0700eb4ce1bea
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.2 MB (304225756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f837ae763b43abf518703c5c531c5cd8e10b08a9d635603f41c6916c80b018`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:51 GMT
ADD file:204b9bd9d9bd808b15b0257739243338e223ade24ac2085e9c4ee95ac07d2795 in / 
# Tue, 02 Jul 2024 01:00:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:28:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:28:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:29:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5771d15f45cf5483d59c36ac7d7cc82b87747d80582fa22fc972b5752cd511a6`  
		Last Modified: Tue, 02 Jul 2024 01:04:51 GMT  
		Size: 47.2 MB (47183831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0863392378e09c6e3f61df0d322c322e2bcb582a29f5b7e95a77fce23a171076`  
		Last Modified: Tue, 02 Jul 2024 01:41:23 GMT  
		Size: 17.4 MB (17360749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fc9810575d09cc1a531b36b6dc5a6732c2497822817a275fa6e0f052b85729`  
		Last Modified: Tue, 02 Jul 2024 01:41:44 GMT  
		Size: 61.7 MB (61727269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2f2a40bf5c5afe0273e5577873d1b44cd80be9996d863a0e0accce07aff45b`  
		Last Modified: Tue, 02 Jul 2024 01:42:17 GMT  
		Size: 178.0 MB (177953907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:daa240adc3a26e2cfccc8f82dd71f77925f6e95bc18d608dd874c8899a15943f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.9 MB (369902961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9399dafa2937341b2f8e58f15cff1becc501382148d41cfe86b2f9edcbdb6e9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:53 GMT
ADD file:0df3518c1c665e2879ed3c7b7c5961b53fc28709cc135a245b209411a275c037 in / 
# Thu, 13 Jun 2024 00:40:54 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:25:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:26:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:27:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:844667f4b2125bd419ff2157667c09ca5b8d442b399e2db99e62277881555d82`  
		Last Modified: Thu, 13 Jun 2024 00:45:41 GMT  
		Size: 52.7 MB (52683111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de631d800a2d5597fbeefa6256f2a1b9ec1248adc1daeb69a836e05978fa6d5c`  
		Last Modified: Thu, 13 Jun 2024 01:32:52 GMT  
		Size: 18.8 MB (18771377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d43c1cffc0bde8580055dfb72c20e5ff7b0e65c7530d279c7ccb77fada1a6f`  
		Last Modified: Thu, 13 Jun 2024 01:33:07 GMT  
		Size: 67.0 MB (66991284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2611f13f4ded7c5c4db9cec62d32aa647f19b894c8d49a71181242d891cdaa`  
		Last Modified: Thu, 13 Jun 2024 01:33:37 GMT  
		Size: 231.5 MB (231457189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b32fb16bb40f1c4609bc89a615b719c282fad4a161ac76d1ae0f6ee4fd448145
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.4 MB (355373297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53360042872fbfafdf053ae3dec1848d385dab1ebd0af3604bbd023a65d6357`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:49 GMT
ADD file:a08584f3c5024aeb655047534f24f132994ce1978bc3c1b585197931050df05d in / 
# Tue, 02 Jul 2024 00:39:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:09:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:09:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:11:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fcc722c6a8b995b7f273820b7fc927164f6709bd0e428b87e24702a321694439`  
		Last Modified: Tue, 02 Jul 2024 00:44:25 GMT  
		Size: 53.5 MB (53522389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8e6a38c0f75fbaa782155e3b94e2d74aeb59d307bc3e812b341c5dda4c716e`  
		Last Modified: Tue, 02 Jul 2024 01:16:36 GMT  
		Size: 20.0 MB (20029986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bd1c9fa39223666daa0aa317ef8df03f991cf958cadb2ed6c76caa40dcb40c`  
		Last Modified: Tue, 02 Jul 2024 01:16:57 GMT  
		Size: 68.8 MB (68750804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1c5f563fde57de0746970470920b77fe237787bf2778b750a1e1bc51968dcd`  
		Last Modified: Tue, 02 Jul 2024 01:17:41 GMT  
		Size: 213.1 MB (213070118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:40c3656face54fea61efa09f88d14275309eaf2f728af49bf188790b67253f49
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.3 MB (353271641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6988d0814284ba42eaf3dbd77589908052c2766caa764b6924d0cbff4d5b133`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:13:44 GMT
ADD file:bc1c5f4f7dc974780be655fc08cd2e36c5d04921a942dd0065534fe0f2520661 in / 
# Thu, 13 Jun 2024 01:13:50 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:17:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 02:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 02:26:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:371a3512d511da5522a67af4d5945c86f5bf5015bc3be3dfc08ea50797400367`  
		Last Modified: Thu, 13 Jun 2024 01:25:20 GMT  
		Size: 51.3 MB (51279195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e19ab65511529aa4e809a989c916e7d1eea56540a36758da55666b6d063b69`  
		Last Modified: Thu, 13 Jun 2024 02:42:33 GMT  
		Size: 19.5 MB (19513685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a59683027da59c0bb0526447861a6a715f53ce57d4a231feeedcc859064169e`  
		Last Modified: Thu, 13 Jun 2024 02:43:27 GMT  
		Size: 65.8 MB (65791634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1a82d886848eaaf9a129b694b52bc6d423bcd3a15d74fbbe168f5b1822eadf`  
		Last Modified: Thu, 13 Jun 2024 02:45:53 GMT  
		Size: 216.7 MB (216687127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e311aac450f93914dc6d7518752093aa86374c5929cf1f608f935ff6ce8b0ff5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 MB (363981675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9043412e3720007b5fc8ed5443e03568afc60a3bb33ae9ef224ddc6d8f1ad4b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:42 GMT
ADD file:3dace89583571d938fe26db69a8298f77892aebb1a70e0e70c4df0d920e6711e in / 
# Tue, 02 Jul 2024 01:18:45 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:50:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:51:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:53:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6b25364bfef282c79118e14cd54dbe5b982558a5939e2bdf63d94df980561937`  
		Last Modified: Tue, 02 Jul 2024 01:23:45 GMT  
		Size: 56.6 MB (56550979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebf3b5ee4fc7445cb77fdf4fb4cb47ba2202118afdd12c9717312c0f227d074`  
		Last Modified: Tue, 02 Jul 2024 02:06:50 GMT  
		Size: 21.0 MB (20981632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26016ae5937fe37740b3fd6ff9a34640437bb4bff44a1627455139be3fe4ca32`  
		Last Modified: Tue, 02 Jul 2024 02:07:11 GMT  
		Size: 72.4 MB (72391083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25579f52f716700e4d889f849e711f10daa1e91575689b6ed851435eb1669a1a`  
		Last Modified: Tue, 02 Jul 2024 02:07:48 GMT  
		Size: 214.1 MB (214057981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:fb402c32a0d7a46239e4bac3ae4e9e2b837d472557bf87726ea5b90311c856a3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.0 MB (416991573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e097f8a7c9e4cbba83e8a7b30a72328b9a87eb9536f56670761a9a4c282bf1ca`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:31:50 GMT
ADD file:5f145818f2852834c826623d73119954ead96eb9bce2d43c78acb87643e22613 in / 
# Thu, 13 Jun 2024 01:31:53 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:02:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 02:05:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 02:13:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6ac783982847dc2f82c444819c90a10bdd382db79de84981f527e1462e567adf`  
		Last Modified: Thu, 13 Jun 2024 01:36:23 GMT  
		Size: 50.7 MB (50715744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1659c611213bc35c1eb01ea12d4ad271643ffd53f1e2e2bc4b26608a2487a2b`  
		Last Modified: Thu, 13 Jun 2024 02:14:02 GMT  
		Size: 18.7 MB (18705876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fc926fbb86329f17c9d7a8101110c3dcd41d78ea4ae3f1d9f5edba14dde6dd`  
		Last Modified: Thu, 13 Jun 2024 02:15:27 GMT  
		Size: 66.3 MB (66255342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf57fed0a12235ec4e26b0c6ef510c211f6a00747da09d3b16578daa501a8e5`  
		Last Modified: Thu, 13 Jun 2024 02:22:49 GMT  
		Size: 281.3 MB (281314611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7d6828765ddb211d089c8c568462983c15929fe5a3e05cfac4465d0fcc822861
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.9 MB (357869320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8efad1c598bdb9690d423caa245cc20dc6c795ff5b044d7755e183c453da1d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:44:00 GMT
ADD file:48df1edc9b73475781ccac0eb967ca97c87c5a3132a7c9058519fad686260867 in / 
# Thu, 13 Jun 2024 00:44:02 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 05:25:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 05:25:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 05:26:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f539c970b22ae85b0b82128798f27249002cae24f6d005cd8df7e2098a346a0d`  
		Last Modified: Thu, 13 Jun 2024 00:48:56 GMT  
		Size: 52.1 MB (52054394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98301e222cdd3787932e298432980b45832dc8bafb525d89b9f56907acf79064`  
		Last Modified: Thu, 13 Jun 2024 05:32:33 GMT  
		Size: 20.2 MB (20215760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c89dc2e12ec49de6459e71f70fedab5f35e68d27cc98813aad170a96c48ead`  
		Last Modified: Thu, 13 Jun 2024 05:32:48 GMT  
		Size: 68.0 MB (68038589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134d2b36b41b12c9ddb990af467b2ca013c33007b06f18dfccd4a144948d6e85`  
		Last Modified: Thu, 13 Jun 2024 05:33:20 GMT  
		Size: 217.6 MB (217560577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

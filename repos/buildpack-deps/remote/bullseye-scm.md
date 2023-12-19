## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:63c47df5da5d153750eb9cbba150a497a730ee6e2d164a7edb6f68335463613b
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

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4054e904ff87db4d4cd59ce1a799a6bc4dc8dc4d574f08516d17a8eb6da06295
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125417592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8751ba61510c6429a6fe455c2a78766f760206df597fc71174d4a0ea8745ad1d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:38 GMT
ADD file:d3a2f1f42338ba7066e352cea3b7bf4c7576e6b96fef785e8da763114f337c0e in / 
# Tue, 19 Dec 2023 01:20:38 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:33:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:18f2c3b7ca52caba205d748b9ce41784eb010ca83ece9e84e2a09130a5ec3cbc`  
		Last Modified: Tue, 19 Dec 2023 01:25:17 GMT  
		Size: 55.1 MB (55057340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8988ac7a69cc18b80883227d1cddd6babff98a5fce88b591500f8727dd26ff0d`  
		Last Modified: Tue, 19 Dec 2023 04:42:17 GMT  
		Size: 15.8 MB (15764812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d278fc41a93b35689afe55f7bbeda81194c3ed9d7162d8adf2ed2af1e042ea`  
		Last Modified: Tue, 19 Dec 2023 04:42:32 GMT  
		Size: 54.6 MB (54595440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:32c0afc692587a880c866a2873aeee60904b2952de835a39c9910900a9229804
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120270005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77a9c21fec3461a0186b839f920493c85c3891eed172a6bfdcdf6428e120fb6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:29 GMT
ADD file:10a67a16f03367965d9105db3d368f8cf27493769f1551c2bfdc274485bd7f6d in / 
# Tue, 19 Dec 2023 01:55:30 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:24:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:476954b0dbc0bbf3e36983f98ae01dfefa01670a85ffcb7ed6916095b71bdd38`  
		Last Modified: Tue, 19 Dec 2023 01:58:55 GMT  
		Size: 52.6 MB (52562242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c916e9180fcbf9c89ebfd7938abc54ad079641855f038c298e679cb1d772eec`  
		Last Modified: Tue, 19 Dec 2023 05:32:39 GMT  
		Size: 15.4 MB (15376057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d33e8d4b6c3b1604296a932879e7916cac6072efd2b9383ab5b5cad23e3a50f`  
		Last Modified: Tue, 19 Dec 2023 05:32:57 GMT  
		Size: 52.3 MB (52331706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c55f5aacac15134f491ec1c03c9fce488ec4f3cd3b947627d72f413b4adfab7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115449651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf4687982e25d88e2d58798fb818ca082ef68660782413d90e36bc04c737c59`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:07:59 GMT
ADD file:3b623bed8ec2536cb513edda1de6f79d2c8e06d6f82df2543202544dbba3ae3e in / 
# Tue, 19 Dec 2023 02:08:00 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:57:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:57:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1b42212018867046767b36eb95cf15c4b66bbb7b4fb552aab446d9822de5765c`  
		Last Modified: Tue, 19 Dec 2023 02:12:11 GMT  
		Size: 50.2 MB (50215775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344f6b88eeb188b9948991d7a318480a17a477fd684c6fbdc230ad9a217fed92`  
		Last Modified: Tue, 19 Dec 2023 08:07:28 GMT  
		Size: 14.9 MB (14880518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36372cf5bdff61f93cd6e14b66d2512eebf0c58b08179f661fbb89bdd34a5ca`  
		Last Modified: Tue, 19 Dec 2023 08:07:48 GMT  
		Size: 50.4 MB (50353358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4c31c30101307643083260a13676c9b804d3e7ef36d1a686648e409c20321f17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124158270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8070300f18d5fec49e0b81e8038727ea235cec304d470c68072754a4b17c9123`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:17 GMT
ADD file:06ba7e39a2f8e1a7bcbb929fa9d1e6fb1f8bdcf5096dc903576af8f7014e353b in / 
# Tue, 19 Dec 2023 01:41:18 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:35:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:396a672fee8bade1a7c9f228d919717447f110f39046d8b5ed21ad45ae13ab61`  
		Last Modified: Tue, 19 Dec 2023 01:44:57 GMT  
		Size: 53.7 MB (53708091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010797996cc86cf2cf7495aebc22e5be7d18a10bde1e11562dbe5283c226c0e9`  
		Last Modified: Tue, 19 Dec 2023 11:43:17 GMT  
		Size: 15.8 MB (15750308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70092c2a6b382a0cc0bd2adeb187b94d74c8bcf2ceb6f33bb8e4e4e9c6561141`  
		Last Modified: Tue, 19 Dec 2023 11:43:31 GMT  
		Size: 54.7 MB (54699871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ef0490bf126cc792a87619e071c478855a1e91401af0ff7c7e8da38762cc3ce2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128252439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44472fb72edf1f4fd0e9d0cb13f8ac12288109eecb18aeb11483cdd421aaba0a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:19 GMT
ADD file:8a328fced7ae3a6fc868bbb95c23191103e595c9d22b2626c16f155bc48b51a8 in / 
# Tue, 19 Dec 2023 01:39:20 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:26:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:27:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a789657fd5416b1ccfd519597a8f5e57bd5a80d04d1b1b7b2770df4469f4dd44`  
		Last Modified: Tue, 19 Dec 2023 01:44:07 GMT  
		Size: 56.0 MB (56046336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0386e6c873ad0aec679cfb967e1449dc2223a2543dd9923e9491c8d4dfe25ff9`  
		Last Modified: Tue, 19 Dec 2023 03:37:37 GMT  
		Size: 16.3 MB (16268921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a344c33a496f0c80e861246ac1b15db106b888d28c7bb89d17b87d06a5f1abc`  
		Last Modified: Tue, 19 Dec 2023 03:37:57 GMT  
		Size: 55.9 MB (55937182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:12102b0ad56b679bdcb5dba9c67c2d93229d41aea8fe0b985d1bc7161d1abf62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122121986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da07e60f6d913cbd8660233af63d0d5648e8da5236bc1f6530597f66cbbb2fa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:14:09 GMT
ADD file:95472c5be6ea30c4b6d715a3000e1bafb8e371897a96c9115040c4a7d2bb2c80 in / 
# Tue, 19 Dec 2023 02:14:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:59:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d8f97806f78898e256ac429d0634dfcccbd6f6e81547afde1469a5968e33b18`  
		Last Modified: Tue, 19 Dec 2023 02:25:21 GMT  
		Size: 53.3 MB (53289008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6729089c3e56fc6fa74aeb41283960af5e717a1e32232fb0de332e8b8393fc37`  
		Last Modified: Tue, 19 Dec 2023 03:22:13 GMT  
		Size: 15.5 MB (15530289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e24f65044fa0f3a3c6a2bf5c15dd5d639173537bdcd52919cfc676d1bbd685`  
		Last Modified: Tue, 19 Dec 2023 03:22:58 GMT  
		Size: 53.3 MB (53302689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f76473553925b44bb2e42060047aa8f781e320e65967f38e26621878a5e6a1e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134563639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3c709db6478e21bc7f416f4eba34fc5482913d90a7383dadee432dc7546ca4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:03 GMT
ADD file:240a318dbc8a7ec4b3a6af5afec173d3579c94c27738b0f79750242acce5dd2f in / 
# Tue, 19 Dec 2023 01:22:06 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:51:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:53:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bdab4f9926bc1dc6c30480616baa760641ee4feeca1b5215d5c420b718c5a1a3`  
		Last Modified: Tue, 19 Dec 2023 01:26:44 GMT  
		Size: 58.9 MB (58929912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5180a9882628ce87cf92f22142ff50ab10a6b9836f1ee8b3f4a4db8afab99f62`  
		Last Modified: Tue, 19 Dec 2023 12:24:04 GMT  
		Size: 16.8 MB (16766736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ffb56ddbf3543b23b4a70af435c61ab9572ba994a4a98817b5efec8daf4084`  
		Last Modified: Tue, 19 Dec 2023 12:24:23 GMT  
		Size: 58.9 MB (58866991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:101021628707aaf2ce18c1b8956e45257e001f6248491ec34315a02231753a3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123004005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7339678f96af115a841a4eb11128a2ec7692ea81ffe0571a0378bc6cff26ea73`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:51 GMT
ADD file:f3ff7311d9c8e7c83e0b7746d9402fed156fb05bd0c704d49535b4ece7f33177 in / 
# Tue, 19 Dec 2023 01:42:55 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:45:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:45:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a7334865824cce0a21e0af9d1f48eaee160e0ac01a54ca220a9814e8d2059646`  
		Last Modified: Tue, 19 Dec 2023 01:47:52 GMT  
		Size: 53.3 MB (53295959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e096c63fd53eae4f8f314ef4db6a5af5579dae607952ecf51910447be347d0bf`  
		Last Modified: Tue, 19 Dec 2023 07:54:24 GMT  
		Size: 15.6 MB (15642144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008c491e9bc699339e05fa0f22fa74aacc65ae31563bf94ba464e87cb6d543a4`  
		Last Modified: Tue, 19 Dec 2023 07:54:39 GMT  
		Size: 54.1 MB (54065902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

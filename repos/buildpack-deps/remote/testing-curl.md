## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:9dd867106f842c7a5e1b6c2d1a9a7ef41e03094f7a5b3dece3b20c74fcf4a1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0d41d0e5e3c4f7f68a8ffdfd6745472d1082dcaddc9c7c8835611b978ca4ab0b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71294180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f13d29a1bc71ba8f009d7fce8405a653b81d484322d1d775d30fefe226ed625`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:02:39 GMT
ADD file:1fda4c82a4eaecf44b3fc4eb92bb0aac8d81c1c87822bd86f8b52b3620b70420 in / 
# Wed, 22 Jul 2020 02:02:40 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:58:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 02:58:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c07b17c5753ba5920876a4091c37318cc0787c8027550cb13d9c1bd7ebfab87f`  
		Last Modified: Wed, 22 Jul 2020 02:09:11 GMT  
		Size: 54.1 MB (54102477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d597760a8071b7dad395d547ed7915e05c7d4fba09ba2c81e36fcf54c4a712d2`  
		Last Modified: Wed, 22 Jul 2020 03:15:18 GMT  
		Size: 6.6 MB (6607399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e255324867b8c5356029c240f78c0cf753ace14e42bbc98bb34675857b8afaa5`  
		Last Modified: Wed, 22 Jul 2020 03:15:18 GMT  
		Size: 10.6 MB (10584304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8f8c66f3cfa32c3174d039df047f76d7b7bc9134e3c86f4df75ab6365d960794
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68540697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf288d4e7e1761f5f62c5cb4de090959a792fc37b6f8e16314332b83f896a580`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:49:13 GMT
ADD file:057073afde8372e5586242898989764dc7739ad5fc93c170548a9831952368b5 in / 
# Wed, 22 Jul 2020 00:49:17 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:21:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:22:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a9cdb0a98bd26018b67bc273d7a9bbd7c5d47c8ed8ba0b72c2024f049430a2e1`  
		Last Modified: Wed, 22 Jul 2020 00:57:48 GMT  
		Size: 51.8 MB (51782291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77dbfe5f595e23e67fa5c93bcef27e0855291352f61d2818001054fe906d1f1`  
		Last Modified: Wed, 22 Jul 2020 02:00:55 GMT  
		Size: 6.5 MB (6486760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2244202796f405d730ccf4e2e91cedd51e3cb380515ba202422d289179a182`  
		Last Modified: Wed, 22 Jul 2020 02:00:56 GMT  
		Size: 10.3 MB (10271646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c0ed990a814967574dfb279b5953d98ad928a49f304eb575050c79cfcab5f8d9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65677558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a281adf932cf9806b62dcc5c937b08a8108b708840c901c4e05889c349ecd21`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:16:07 GMT
ADD file:b12e6ee23a8c36af2c020959d86c9277008b6b54ceff80954502340dee6e145e in / 
# Wed, 22 Jul 2020 01:16:12 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:21:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:21:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:9142e33629754cf85d79355e893c9c07e344f32f4fbe710c344514aada5f1b92`  
		Last Modified: Wed, 22 Jul 2020 01:39:35 GMT  
		Size: 49.5 MB (49461754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab191c0042bdb971560c33a6e7bee561ff37ce4309087897cad70ea149a1c831`  
		Last Modified: Wed, 22 Jul 2020 06:00:20 GMT  
		Size: 6.3 MB (6296595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588773c504d467808703f4e8fb464799ea4ce5a0db4e5d91e73995846917d34b`  
		Last Modified: Wed, 22 Jul 2020 06:00:22 GMT  
		Size: 9.9 MB (9919209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f9973ac4ed4fe780e84953d52e3ca19724e7d15feced4c55fae39715289f8c3f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70112792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6199d5b5b70a31680ae943a0aad5a02f0672fb8cef9b4fef5917ae1dbf2eaee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:39:52 GMT
ADD file:19b87dac8088f103e1a9992c229b17344439af0da8af45bc6d678f69471077d4 in / 
# Wed, 22 Jul 2020 00:39:54 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:08:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:09:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:508fd3fb95b7fcde22f3f927caabf293cc04dcbdb4c45b85a5130d5122e12a0c`  
		Last Modified: Wed, 22 Jul 2020 00:46:40 GMT  
		Size: 52.9 MB (52886369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5915a33a39d2dc36bde47815617bc03c29dc80e9539719e24091c59faeb64f73`  
		Last Modified: Wed, 22 Jul 2020 01:33:46 GMT  
		Size: 6.6 MB (6634801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ea5d467b9d2286b1dcd428b411982c7ca3d5a2471f013ef721842af48ec9b`  
		Last Modified: Wed, 22 Jul 2020 01:33:46 GMT  
		Size: 10.6 MB (10591622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9c48bb4dcc7d81316a0d41e6e5f40c04e8577a4707969f4a28018bd24716f1d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72998529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54c96bba171ad4a86ec122f9491afe355f777a054ed53ad7d9ef5863591d4d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:08:16 GMT
ADD file:ca0e279e6fd6eb980b9731b695496074a130913346e67625acec79226fc6c10b in / 
# Wed, 22 Jul 2020 02:08:17 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:17:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:18:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0f7fe72ad45ca30a1e73e494824a081709c2e449cb1bac8b4deb1b1a29c62e6c`  
		Last Modified: Wed, 22 Jul 2020 02:14:35 GMT  
		Size: 55.2 MB (55225022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3647f8e1aff936bbcccf16d2eb142f694cf4736d8d8adfaf3114569bc553035`  
		Last Modified: Wed, 22 Jul 2020 03:38:03 GMT  
		Size: 6.8 MB (6808980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a520a2450f762082c65c471256beae8c5f1c15f69b32c692c574b4c4caa4a20d`  
		Last Modified: Wed, 22 Jul 2020 03:38:03 GMT  
		Size: 11.0 MB (10964527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6168b7c1602a61c3ee33297a956b8cb7ed179af43412c99bcb982951728a8c46
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68114967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5979abf488ef443bcfb20d48981fde2897a26df2a7930fb8c2412e57a3231916`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:08:53 GMT
ADD file:080fe104a5c84718f0c41015a3a4bf48ef0d94088beb50e3b0346ea572302008 in / 
# Tue, 09 Jun 2020 01:08:54 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4295b4a99b75e24118d0a604e63b142af1639be17451d6724215fd11e6fdd041`  
		Last Modified: Tue, 09 Jun 2020 01:16:09 GMT  
		Size: 50.2 MB (50162108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6b19c74224bd3e9030de803cd7b2cf6f938ee3548998819522a786837b1caf`  
		Last Modified: Tue, 09 Jun 2020 02:06:44 GMT  
		Size: 7.4 MB (7447679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e65e61fe718bcf10bce9dbbedd4844ba55e178913be199a5e4cd26a5ca17f1`  
		Last Modified: Tue, 09 Jun 2020 02:06:44 GMT  
		Size: 10.5 MB (10505180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3c13b98d4c0074da2dc89aeb38cb9d915a230c9c563555ccd158b6b2817627bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76274886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbf4e79855dcdb365e1a8837af311229d912ca7a5a3e745c714ca8a41d8944e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:13:38 GMT
ADD file:92efdcf349a6f1580ab27a2612939d75fc0e449e05e20e6385f5f7e409cd6684 in / 
# Wed, 22 Jul 2020 02:13:52 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:52:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 04:53:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1eb910fa0fdd2afbde1007491a0fe3461e3029a0c5950e2a5ea3a69d15cab80c`  
		Last Modified: Wed, 22 Jul 2020 02:22:28 GMT  
		Size: 58.0 MB (57953394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e46d2506c2944fcb5f8a4602131b518bc797e95e34ec5068a32eea4f31d2db6`  
		Last Modified: Wed, 22 Jul 2020 05:52:43 GMT  
		Size: 7.0 MB (6990284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2b78285d9f403581b34af8b80dc4d9f5f258ba139298995ee9c8fc3bf6a899`  
		Last Modified: Wed, 22 Jul 2020 05:52:43 GMT  
		Size: 11.3 MB (11331208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:afb557fb3c64a2554edfaa6819479e46dd9046b7d44fc903a3dfa31a6432bef0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69466020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2163ce7bb496edf661d0e926676f20700cae3b6f88c3f5e359478cbf35a88d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:41:56 GMT
ADD file:64e5f3d6bda82e2ceaeaede4b9646a695e0b5c2daf32f3ceac3f8404c189999e in / 
# Wed, 22 Jul 2020 00:41:58 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:03:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:03:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:eec92be71167cbdfe66ed0a95cf2650cfae8fc7e2f6d3c038707f63a74aa347f`  
		Last Modified: Wed, 22 Jul 2020 00:45:06 GMT  
		Size: 52.4 MB (52406289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c7d5f37f3ba0ac86762ed35d75a67c2913a5142f0395028219243aee7bb41b`  
		Last Modified: Wed, 22 Jul 2020 01:11:26 GMT  
		Size: 6.6 MB (6599170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76cc1489ae85b994163f909e22b33f76692a45947a1fba3d3d821d5327b317c`  
		Last Modified: Wed, 22 Jul 2020 01:11:26 GMT  
		Size: 10.5 MB (10460561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

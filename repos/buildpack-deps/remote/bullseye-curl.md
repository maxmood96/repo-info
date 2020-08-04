## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:053e554f7f8a0fdab9b8d4ee3a0beaeaf3379afba50cabcb192ab6e7ffb5acd0
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

### `buildpack-deps:bullseye-curl` - linux; amd64

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

### `buildpack-deps:bullseye-curl` - linux; arm variant v5

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

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

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

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

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

### `buildpack-deps:bullseye-curl` - linux; 386

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

### `buildpack-deps:bullseye-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9c4c4bd7063deb0bbc36085c627df9df8813574f7bbaa567706a2d26c80afb18
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69529467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e78ed111614e2d250420c071ee735964cd3deac6527ea9f7eda705e0ecb392`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:08:31 GMT
ADD file:7401625ebd06dafb2256bbcc5a70246e5e6282bcc356478f05fd7ddcaa55003c in / 
# Wed, 22 Jul 2020 01:08:32 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 10:28:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 10:28:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c240b05d7ff10891b36c505769b275684894e6a8ed8b5d40f20220a3da221e14`  
		Last Modified: Wed, 22 Jul 2020 01:14:40 GMT  
		Size: 52.4 MB (52358232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f2b31f704addd955e451fd2986f5159585f197625488725aac773df35e8478`  
		Last Modified: Wed, 22 Jul 2020 10:43:19 GMT  
		Size: 6.6 MB (6568575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30eb65f190ba6e9a301c9609ece037a9e82a8414a773e19a288860911d2d844`  
		Last Modified: Wed, 22 Jul 2020 10:43:21 GMT  
		Size: 10.6 MB (10602660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; ppc64le

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

### `buildpack-deps:bullseye-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:482700f81baeecafc3e0eee9ff9f598a1e55ade167734f1829b5ecdb79235597
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68463450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f00c57c2e4134baee033121e817d02ecc23ba2f1a62a69daedb69c32cd8f3c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 01:16:37 GMT
ADD file:be061a89b8959a241d8303ec83a6494b37d71fe20736b073046173371101421e in / 
# Tue, 04 Aug 2020 01:16:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 02:19:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 02:19:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:67f968df5fed9ab1993b2cba53f4810f984f47936fce947baf7ef2e7d8a5a20c`  
		Last Modified: Tue, 04 Aug 2020 01:19:19 GMT  
		Size: 50.4 MB (50416822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789709f3eb6ec781e7bd5d546a438d9f93b42d8201f34934bb917541d98545eb`  
		Last Modified: Tue, 04 Aug 2020 02:27:09 GMT  
		Size: 7.6 MB (7590147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17405c3991955650e0612638adcfcaec522e3c07552eb6b1924bd354bc8e608`  
		Last Modified: Tue, 04 Aug 2020 02:27:09 GMT  
		Size: 10.5 MB (10456481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:1a1c5b6e84c132eeb77dc09722245633694f655072df10ef6a837cb75a59064b
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6943f938d9951b7d261762647568d3778d3ed55905019227091541b7889e9fa6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72178551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654515af3131c5fcf8190e81562db736635066cccdbc3dac39e30ca8a39491ad`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:05:54 GMT
ADD file:20b1068c276c223839818edd0aca3981a1b8139130064d19f9ec38e26a94ff27 in / 
# Thu, 17 Mar 2022 04:05:54 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:33:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:33:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ab40a96ab944197ee11d696f776db9c1130db9825e9996a5e8939611fcf5e470`  
		Last Modified: Thu, 17 Mar 2022 04:12:27 GMT  
		Size: 56.0 MB (55984715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214f624759443498bdf804a19e1294b81976d28ed00d521e85a6ef33658ab378`  
		Last Modified: Fri, 18 Mar 2022 07:05:57 GMT  
		Size: 5.3 MB (5269458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59203613ecfdfcaa48f715e4d48dfb31fde19bed9d8d6dd6886973ca3d859f7`  
		Last Modified: Fri, 18 Mar 2022 07:05:57 GMT  
		Size: 10.9 MB (10924378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4bb272a6ebaaa0a79167b0b2ee6cbd8a7e70a9318992c7dd4cce7bbf43f6a2a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69155478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b65e3b02efe40bbefb5f21eee3ee01b5d1b4705371e621e152ca738f8dd885`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:23:03 GMT
ADD file:a9d4a5aa739c9c980a2e0b3342f616a0ef24327457038a7d2d1f054b47bb869d in / 
# Thu, 17 Mar 2022 05:23:04 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:24:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c1b1560f4e7f4d5dc335516eb5f16007a5ba8efcbedcc5584f361684738e508d`  
		Last Modified: Thu, 17 Mar 2022 05:39:40 GMT  
		Size: 53.4 MB (53393523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3688991f52d334055cd012a6287b39073e9b4ac6c7cd7012b2c8be6c4cf410`  
		Last Modified: Thu, 17 Mar 2022 19:44:30 GMT  
		Size: 5.2 MB (5164495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247526418f56b9d635ff39e99bd9d2058cdf75fa52ee8a6fb0e2a007868a5e12`  
		Last Modified: Thu, 17 Mar 2022 19:44:32 GMT  
		Size: 10.6 MB (10597460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d041850d214909c62d8aafed7afe3a77fa93d972c337e10e6f7a06ec34ec1af9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66276584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab3b8d262225dd1f7aaef964f2aa9178b5d13734c52430c7b6e1527389ea098`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:34:34 GMT
ADD file:9aa47fa903f49c3cddd2c04ea6dfc8adc7cb3e1b8f49392eb4ef30199e306b55 in / 
# Thu, 17 Mar 2022 09:34:36 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 02:59:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 02:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d5abaa3393d9da88a4f8667cc7ed186e0fcf756926f31ba33f3b531a2db42031`  
		Last Modified: Thu, 17 Mar 2022 09:51:00 GMT  
		Size: 51.0 MB (51008095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a92e937e95ec8c4708c51bf5b42788af6dc7933017024adfe3755af9a222a4`  
		Last Modified: Sat, 19 Mar 2022 03:34:48 GMT  
		Size: 5.0 MB (5023856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f9c704ba15933d332549e911b8ecf5197b7956ef44f600fb06943964d50581`  
		Last Modified: Sat, 19 Mar 2022 03:34:50 GMT  
		Size: 10.2 MB (10244633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fe0129a4c5f9d9d223e94383888c344f377cd2762f33dc7accebefe230cc39bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70865563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d077ad99748ee748b802513089e80e0d67ec10fa7b9b79135fda0bfa1481a294`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:23:19 GMT
ADD file:1d38d88879da25d9a1bc7a4c5e36bc54d45209f4c931e6da3f7a5121498cecf5 in / 
# Thu, 17 Mar 2022 03:23:20 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:13:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:13:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d1bb23fb7eb3b065e76a0f28cfe8d85ecc762b7cff467fdbcda2f70363c88087`  
		Last Modified: Thu, 17 Mar 2022 03:31:11 GMT  
		Size: 54.9 MB (54916866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c42e541f9a190ed5b1572f38d77d9a07c7899f7b9640e25460c12e849991f1`  
		Last Modified: Thu, 17 Mar 2022 22:23:20 GMT  
		Size: 5.3 MB (5255457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556c64db2922b5a87b5591ed9b67221014a21677b094903b77fc24099a5a1f3c`  
		Last Modified: Thu, 17 Mar 2022 22:23:21 GMT  
		Size: 10.7 MB (10693240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8498ffa6b9df8cc9dc4658b68624301d53db0209301c5f549123c4b468580ffa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73755493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae5dbed79aae03c92282f8d9f4f093f12832dfb4adeff77866a5799458da609`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:17:34 GMT
ADD file:2cb9c8978846d8941a8213d064afc34b86f2f04e601b9ab365a29fff596c2aa5 in / 
# Thu, 17 Mar 2022 08:17:35 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 14:30:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 14:30:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:23f252c494b0d56260da77f35c850c42d26d01946241721f649418fdd13ddb96`  
		Last Modified: Thu, 17 Mar 2022 08:26:58 GMT  
		Size: 57.0 MB (57031438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713c087b701c0e96ba52a634dca0b79b7bfc26336946b8ef9b7bb6deda31d1c1`  
		Last Modified: Fri, 18 Mar 2022 14:46:45 GMT  
		Size: 5.4 MB (5401519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c902ee6ab20573e3958bbd0b3e2ec3a189d08dc0fdac8987424bf548e32cde9`  
		Last Modified: Fri, 18 Mar 2022 14:46:45 GMT  
		Size: 11.3 MB (11322536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:76e4ba4f0f4227dc356e98d2b19d6b38806c0bf8c7368b8952a7117bc4a746fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70532432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df2597a07c8932d760644ad5adb1de05d3e26e7f9d1651f298de4c082fd05d1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:55:47 GMT
ADD file:2015a98f802a1e28eca2c4eba0b574f58c2cd7844c0d94dbf0e29e8180aea210 in / 
# Thu, 17 Mar 2022 08:55:51 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:39:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3d194d6caec7e92bc6e1448edd24c61790b7372a62bd6808d5cd0c5a6eda1736`  
		Last Modified: Thu, 17 Mar 2022 10:46:33 GMT  
		Size: 54.6 MB (54636832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6d8d6c495a88dc95c7cdb4d3ae2e01617fbe355ec506b682a16ac6bd71546a`  
		Last Modified: Thu, 17 Mar 2022 19:57:08 GMT  
		Size: 5.2 MB (5222583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91053236c731557db21c8cae8dadcde7f25967ff5d460c9f67f4789ecb8b3be7`  
		Last Modified: Thu, 17 Mar 2022 19:57:10 GMT  
		Size: 10.7 MB (10673017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:88f9e52f460feeacefb82cad4b2dfa316825762b17751ce6849ef1f97f1da206
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77652334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdea446dd5a4baf3ec553a78cf940cab02bd15792e13ff7d34ecec557026edb8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 11:20:22 GMT
ADD file:52ac257bb3e9b43a436c32541c15e9c3a00323e3e1d0b20273b81a572fb8d66f in / 
# Thu, 17 Mar 2022 11:20:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 05:59:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 05:59:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d022277e505c1e9a57478a80b1b82e11b58551ebc0afcb5e723535b6ee105cc8`  
		Last Modified: Thu, 17 Mar 2022 11:30:38 GMT  
		Size: 60.4 MB (60406211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5191baf63a49f74aafee330281325a08a8d65451cc0ac632e8aa56129d9dca63`  
		Last Modified: Sat, 19 Mar 2022 06:45:43 GMT  
		Size: 5.5 MB (5543862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471dd71263fc10a8a1efc9a8fc7652bc8d0e227dafa1f6f9493a5a9779600d7a`  
		Last Modified: Sat, 19 Mar 2022 06:45:43 GMT  
		Size: 11.7 MB (11702261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c3980de3ed3b025c0d84d5e38516aaccca3a7acdeb4125424201686281a029b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67060604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650dfff09d8b84ea9c4bbf1943958bb863e0d56c07c84dfaeb67baf2ec1491a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 01:14:42 GMT
ADD file:a994e723b30499cbdba960284559bdde2e3abee2fdcb763fdd233da95dafe147 in / 
# Thu, 17 Mar 2022 01:14:44 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 02:01:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 02:02:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:271cb4a0cf55f464e243d145aec35f35f8228420ef9aefb2a52eaabc09bf5c50`  
		Last Modified: Thu, 17 Mar 2022 01:33:41 GMT  
		Size: 51.7 MB (51661116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cead6fedbff27583eae8cbd457b531667d28b94bafbb24b1402d794d4c55ec0`  
		Last Modified: Thu, 17 Mar 2022 02:34:04 GMT  
		Size: 5.1 MB (5077182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8e5e53be16547420594001f871619cc0c003f8d23528375b0f6c4550aaa2f2`  
		Last Modified: Thu, 17 Mar 2022 02:34:07 GMT  
		Size: 10.3 MB (10322306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:71adb0264e2f56a313869a4d1c35ba7e8c550b5786fb9286fd6ae3cfd04bf22c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70312008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d276887bea2c86045740e207e7f8d0a86772f49f7531a5cb9a3872fe238c6125`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:08:11 GMT
ADD file:4a7b0c9e8bc60d35d06240af5417427853918fe6624688050d4aca10a22b433f in / 
# Thu, 17 Mar 2022 03:08:14 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 18:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:23:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8e1d6cb1e553f745f248c4d7a409401acdb697f1bd597e8c1c08d6fcd5db0f2d`  
		Last Modified: Thu, 17 Mar 2022 03:13:59 GMT  
		Size: 54.2 MB (54246705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99267e3e8ccd599670f5059d59cf2f80cafc0773fc8b74ba953d5d5cb2189fed`  
		Last Modified: Thu, 17 Mar 2022 18:30:46 GMT  
		Size: 5.2 MB (5245707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3282440b854d7908290c041b1619604c86d6fb3ec5e2ed67356bbd4ef1847863`  
		Last Modified: Thu, 17 Mar 2022 18:30:47 GMT  
		Size: 10.8 MB (10819596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

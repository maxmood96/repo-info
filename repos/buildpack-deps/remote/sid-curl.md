## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:8672031f2e90dab19946e7a1397e7ff65d06630a20ccbc5dec5f6298f8a3595a
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:91218e30a5dc07b1a689ff2160c8299d9d2a4327649004db0270a9d901fa9f7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70923345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ad60349c2eb2853dfc3931198c3f78e7bfc2b5d651d847ce671aab0c8eb390`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:41 GMT
ADD file:635f36e1a46e6c28b2a6ab0637cca9e47837c3547b17916d1dbb2595fbeb0821 in / 
# Tue, 25 Oct 2022 01:44:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:26:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:26:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d90f8b044e56f2589b41d1fe9b249b85bde027855731c6f512f0f9401c99e68d`  
		Last Modified: Tue, 25 Oct 2022 01:49:42 GMT  
		Size: 50.6 MB (50641226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e6bcc62372cb6ad18c098f8dda6e9c5b3707abc6e74f2dae7f8032bf929e4d`  
		Last Modified: Tue, 25 Oct 2022 09:49:51 GMT  
		Size: 9.1 MB (9101445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d43887f8917a514e50f8816ba51125c208418ba87167de7d84979146bf6e06e`  
		Last Modified: Tue, 25 Oct 2022 09:49:51 GMT  
		Size: 11.2 MB (11180674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:38a9b9c598a27fc56851dabc393c6e67e8b296ad02f1c656343864375e369666
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68770559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c5a96396ede69f2d6b03b0782e907a9516662142c06edd3c217531aa4118c0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:49:31 GMT
ADD file:08f8312faaa666d9d1d3cdf1e0ac577979317e8784c264b29b4d3399045d2adb in / 
# Tue, 15 Nov 2022 01:49:32 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:44:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 05:44:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:351340891f63641ac5516af46a2dfb6b370ea5971d604352dfe16a498646eb52`  
		Last Modified: Tue, 15 Nov 2022 01:54:51 GMT  
		Size: 49.3 MB (49284160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989d5b3af22bb23168efd5d127277e94392a88454e93916c8136bdbbbfdb6c07`  
		Last Modified: Tue, 15 Nov 2022 05:49:45 GMT  
		Size: 8.5 MB (8471398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae7d5b628dfd536fe95d650285c66873a6d0e49fe2d657c2e7317203d6f01c9`  
		Last Modified: Tue, 15 Nov 2022 05:49:45 GMT  
		Size: 11.0 MB (11015001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bb617337e43971cf9b202d7766de841d6d32089c90ccecb3ffc15f13fb5f32f5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66074895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77af218d32f087fa0334e592452da48d87c960d00f10b9457da49b6c3fa5a492`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:15:36 GMT
ADD file:072a31b7cfe6ee4e4a8e0832259c68a602abda7e1a6682cdcb28eba7f0705383 in / 
# Tue, 25 Oct 2022 03:15:36 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 04:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 04:39:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c9040ceaeef63642a4aa2653b1350e028be0db975aa9a23c7e441aaa7dc5a11a`  
		Last Modified: Tue, 25 Oct 2022 03:23:25 GMT  
		Size: 47.4 MB (47411564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13b466f981f25c2e1938044e245a8dca528315fa39d2e8a80709f09075fa43e`  
		Last Modified: Wed, 26 Oct 2022 05:13:18 GMT  
		Size: 8.2 MB (8204920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c85fa3e21298caffbfd811747b3acc6991bda175e560e8f8d9c2a8152d1eef`  
		Last Modified: Wed, 26 Oct 2022 05:13:19 GMT  
		Size: 10.5 MB (10458411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ee5e36107f8dbb0014f2be3fb5a9b6d8fb6b903885b498baef286d9d66d650c6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70553982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34321eb368f5c3a811c2bd715f2b1f5eda6d3f63239813faaf0467cafb0a4ddd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:54 GMT
ADD file:ba227e9990636bcf4ac74991aee2f89f076de2adf7a651c75b55b2dc145b5340 in / 
# Tue, 15 Nov 2022 01:41:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:39:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 05:39:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a4831e9d6ed52920992a4dda63cbeb8f430d77a27377294be499a02b93fb1e3b`  
		Last Modified: Tue, 15 Nov 2022 01:46:00 GMT  
		Size: 50.4 MB (50371180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28af2f647d544013c2979fcc9bb3234c113dc9496fa976cc4a2fdf6d0622b2d5`  
		Last Modified: Tue, 15 Nov 2022 05:44:45 GMT  
		Size: 8.8 MB (8849884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70069958d3a3ba34e8ab2a47caf5d5f7b8a3be5ff9bb2a50385ea0deceeff91`  
		Last Modified: Tue, 15 Nov 2022 05:44:45 GMT  
		Size: 11.3 MB (11332918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7a92edc5d0d1d9b005fc402881b8f8eddac8e13c8f5adf57fb62e1a26d00983d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72287451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1893a81cbf84a850be47ff4f28e1dd4035b9c2256bdedf86584fb4079c771d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 02:23:38 GMT
ADD file:80dabb60a37b1d88f3750adb85c9e159d00b55293f70ad93512f94bd3cfd99bc in / 
# Tue, 25 Oct 2022 02:23:39 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 05:18:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 05:18:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:367799113badd94b9683087d6086436649a1fb7127698c42b0d730f5bbedcf86`  
		Last Modified: Tue, 25 Oct 2022 02:30:22 GMT  
		Size: 51.6 MB (51625321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564d2fccc59969c0b37e3bb8384bc6545a4cce125daa11c7e8b599ec0acac788`  
		Last Modified: Tue, 25 Oct 2022 05:30:00 GMT  
		Size: 9.3 MB (9282393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09be9213196e288bdcccf553107591d6fe4f04fccea4da55faea35dd79cfff15`  
		Last Modified: Tue, 25 Oct 2022 05:30:00 GMT  
		Size: 11.4 MB (11379737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d0af0e5267dab120726e36ffd9b6ba7ea2fa149c129dc040b5a610b44046757d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70300715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9243ca7d5700b38c3f1e5e5a037ba36432503c6189c32782b9101fb3014f8a29`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 04:39:58 GMT
ADD file:da7998228f2661dd3490a7bee754b7aaed5cf07ebe582e97b32c3985ad0d283c in / 
# Tue, 25 Oct 2022 04:40:04 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:39:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:40:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c2275c195d2a35a07739822efcd752aad4e9580392e4129bbac1f6cfe608ee1b`  
		Last Modified: Tue, 25 Oct 2022 04:48:12 GMT  
		Size: 50.9 MB (50901534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45280c218956111f5980d1b17036f589a29dca56a64f196bd8f0bfabf7b2966a`  
		Last Modified: Tue, 25 Oct 2022 09:55:12 GMT  
		Size: 8.5 MB (8465620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cd0404c18893ceb6c37012f16133ba8b3c876fa90176ae85b3f9d94f25dafd`  
		Last Modified: Tue, 25 Oct 2022 09:55:12 GMT  
		Size: 10.9 MB (10933561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:124e076bd786711b687044fd136c24af7bc4500c1e67e6e1f0f4086eedfced08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76327268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce644126cccec0395c556b7c4763b65ccbe0344029fc1fc5a5a1c93e9d1c4787`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:07 GMT
ADD file:6e9efd6bb77c835520332c88cb412f38f0d8573ec3347b090b77965e17131780 in / 
# Tue, 25 Oct 2022 03:14:10 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:17:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:17:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7a3962f6ac5b86fa159789ea1e9241ecbb956b3223e8312f7d92d7fbb8bf5485`  
		Last Modified: Tue, 25 Oct 2022 03:20:03 GMT  
		Size: 54.7 MB (54704717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c5225e6c97e35e08afc065bed0fb4156a1727da9a3e12b4a611189682c919a`  
		Last Modified: Tue, 25 Oct 2022 06:50:49 GMT  
		Size: 9.7 MB (9684744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39fe7c3b495d9320ca99478bfddf7a3fa0412a37c56ca95a4cc891ceb738e62`  
		Last Modified: Tue, 25 Oct 2022 06:50:49 GMT  
		Size: 11.9 MB (11937807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:20837254e0924117334eafd2ce6a296c897e796ceacc170d92b82d8540a87493
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65429748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1cdd599eca8933f09bec0ba7d28d27e9dfd0a4b3e75c6cea7bd6a207fdc09ff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 02:10:35 GMT
ADD file:3605614f06115edb2ee0a2db052ccf985f2ee967592a4a9eb4f53585907a0c01 in / 
# Tue, 15 Nov 2022 02:10:37 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 02:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 02:57:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:85e0ffe5757d11394c39fa959f3a2cb0a9d1e43dd8d00be2c77fd6fdd43a4041`  
		Last Modified: Tue, 15 Nov 2022 02:28:37 GMT  
		Size: 46.6 MB (46576018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55dc9b61880194396d69e084a5b3a8cf11c21be0f9286759993ddf4345099ff`  
		Last Modified: Tue, 15 Nov 2022 03:27:59 GMT  
		Size: 8.1 MB (8110952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaa050e3d5eeb4149cde6a3c170a41a310d6c07d1eaddc43ac45cc21d7d888e`  
		Last Modified: Tue, 15 Nov 2022 03:28:00 GMT  
		Size: 10.7 MB (10742778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:459e259ac9d973e273d44f4977a901a7c57dce7f749c5caf0ade7837350bf940
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68792946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8919e63d46a3758bb8046627e26a7d852ed8e26e8b044f56948b519863d33fd4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:14:54 GMT
ADD file:7dba2ae439c9f5da3fe962e867cee94eafc0b12a74939e13fdf987965ef8191c in / 
# Tue, 25 Oct 2022 01:14:57 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:32:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1430653806baea9ab2928a0d226c10ba8e7bf4b9b93398f9082ba16edfb2d4b8`  
		Last Modified: Tue, 25 Oct 2022 01:19:17 GMT  
		Size: 49.0 MB (49012977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa67452e329e71787509a1583923b8e1e83b22a2fb76e48111393a03205d4c20`  
		Last Modified: Tue, 25 Oct 2022 02:50:30 GMT  
		Size: 8.7 MB (8738304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7be163526b121ed701b3595b33b6d8755aba04a12b0fd801f9c899cbd3ebd0`  
		Last Modified: Tue, 25 Oct 2022 02:50:30 GMT  
		Size: 11.0 MB (11041665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

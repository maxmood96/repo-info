## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:d64cdd4f304c084ef964d624fc59254823180493c16da26e161ee2de0ebede1b
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:993c09037932672ae5a8ea72f7495dd558b7ae66aa9cf41457912c71b31708ae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70906218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6999481b2d3adddd601438ce8f18013dc50c5eb41ec3825f8796d6ef5f7ab36d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:01 GMT
ADD file:3d2836abb42f177ad29a584ba02ccc6421b1613f73325823603fc98578f17445 in / 
# Tue, 30 Mar 2021 21:50:02 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:05:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:05:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ff28f9110f9a07cc7303cdae0cac6dceebc733170af8336bff099af5e4b0eed1`  
		Last Modified: Tue, 30 Mar 2021 21:55:15 GMT  
		Size: 54.9 MB (54868057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b440922f9fc7a15146adf7cc4d35ea9d0bc9a6a6004a905f240fcad22cfe0bcd`  
		Last Modified: Tue, 30 Mar 2021 23:15:47 GMT  
		Size: 5.2 MB (5169284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd6e01879bcee5c3b6f0a9e069f1f61a436d7e55e344931794bbe2af8c7fde1`  
		Last Modified: Tue, 30 Mar 2021 23:15:48 GMT  
		Size: 10.9 MB (10868877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c74f625fc2632cb866705627945d23572d32948b27d22da47a54ee9c7678cb37
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68046255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a293f49c1682cbb3c0e39505073cf5985571e0b059df0a85ceef7253fd10af8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:52:17 GMT
ADD file:c74b1cfc1e5bf1a62d213de82dd043a95a19f0f67a947b54c449d8ee5d53fb37 in / 
# Tue, 30 Mar 2021 21:52:19 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:51:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:51:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:06ea7b1cac1276634323a37913fac1e0f60820f2aae1fd14d07c2c573bfbce6d`  
		Last Modified: Tue, 30 Mar 2021 21:59:54 GMT  
		Size: 52.4 MB (52402138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d6173e3da10cc42bd51156af90984c02eeb52327364153f9648d30fe084fec`  
		Last Modified: Wed, 31 Mar 2021 00:03:10 GMT  
		Size: 5.1 MB (5073685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918922db8190bce87e065be6997a39e948ef367b3b3f4ab60ced0d40e98f335f`  
		Last Modified: Wed, 31 Mar 2021 00:03:12 GMT  
		Size: 10.6 MB (10570432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b8f7b5b436096f185a90340087617addbfa9e70b7442d497fdbd218f126f0788
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65223551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862f6183aa2f7e335540fc44a1a1cac010a6aebf1f7d1754653b3d1eaee8f3b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:09:57 GMT
ADD file:3c49310ff7c2a9c21073b7ca0884f4b8e783606a6653a2d74d1aa04196a3ed8f in / 
# Tue, 30 Mar 2021 23:10:01 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:25:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 01:26:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f41ab33290e85402afe03e9a82d0262689d71eccbba0d79246595731d24f2688`  
		Last Modified: Tue, 30 Mar 2021 23:17:34 GMT  
		Size: 50.1 MB (50070962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d173ac9612777e7e6d56bd74819357eb0a74fdd29dd54af742a5652ae5ac6d`  
		Last Modified: Wed, 31 Mar 2021 01:38:18 GMT  
		Size: 4.9 MB (4934354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b41bd459aeb849bf22b88bf2563aeffb2527f25a09c92049467c43605bdc30`  
		Last Modified: Wed, 31 Mar 2021 01:38:16 GMT  
		Size: 10.2 MB (10218235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c1430d9141ac99974332a354d4451160fa9c2052749c185c4dba51073b2922df
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69581095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f6ea7ff9d1a70982397729fa7ef9e36309d85d24001f4d6d8b5280b45855f9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:48:22 GMT
ADD file:367b87909b67093178b79312d10fd1e5f34fd8f2d88ff86d5db05018c84e1de6 in / 
# Tue, 30 Mar 2021 21:48:25 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:18:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:19:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2f6f2092d4e11ede8755fdc276c7abb424692833ac06435c47705ad7024c2459`  
		Last Modified: Tue, 30 Mar 2021 21:55:24 GMT  
		Size: 53.6 MB (53555909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7329ddb16965a8f564ba84df809cf2bf57cef4de5272f15c7ea208a725068c`  
		Last Modified: Wed, 31 Mar 2021 00:31:34 GMT  
		Size: 5.2 MB (5156631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800c7b57132ff5a24ff23004e5ee11478f43b53d722d70dab97db2330112cbaa`  
		Last Modified: Wed, 31 Mar 2021 00:31:32 GMT  
		Size: 10.9 MB (10868555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7e1d9840bf16a395503e5f6c978ea7813c8e1e39df35757dc5d023f8b5717d6a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72428844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4aa35de62e2c24c3d8c093a8d0e4a590e99a81ae1825186ccd3b810c96a164`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:40:35 GMT
ADD file:1f041945ff890476db13a1209d904306e018db9cc0c3ddd68afde8ba20721441 in / 
# Tue, 30 Mar 2021 21:40:35 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:59:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c1abc0a07df2794b8c01aadbeeb9293997b8a54aaa313f435b4d2d676f888235`  
		Last Modified: Tue, 30 Mar 2021 21:47:59 GMT  
		Size: 55.9 MB (55881675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc5ab305c1c154665b02986b2328de2fd181084b0c296c4d76f131107ddef04`  
		Last Modified: Wed, 31 Mar 2021 00:09:46 GMT  
		Size: 5.3 MB (5298115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95df009a7c979f03789affbb069b0972638a182a6594760beb04e5d621ca33b`  
		Last Modified: Wed, 31 Mar 2021 00:09:47 GMT  
		Size: 11.2 MB (11249054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e508864ca39f8dbaee96371a8ec8c3dbe61bbbd1aeb3299f4cb31d09a18221a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69126266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36dbe3ae2bf1f4c9c1353429bfea53b1212171e3b3404b89b1b8870f1afabcf2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:10:14 GMT
ADD file:4d20c8e17f6123a0d4b72a62f938dec2586886ad6d87f246ee55a11ea923b684 in / 
# Tue, 30 Mar 2021 22:10:15 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:14:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:15:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ec4a0a6790f3ff962dc7c25a161644b3cc5e5b8758356dab4f112068aa643317`  
		Last Modified: Tue, 30 Mar 2021 22:17:08 GMT  
		Size: 53.1 MB (53127307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90333279e95c41e8d6dddbd8d32157d7b6e64b62fb5b735d17ca9d796904a82f`  
		Last Modified: Tue, 30 Mar 2021 23:25:27 GMT  
		Size: 5.1 MB (5127929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af84110c224d7e9e68767940402f621ab1b3a77a6c7b483749668ff6fccc186`  
		Last Modified: Tue, 30 Mar 2021 23:25:29 GMT  
		Size: 10.9 MB (10871030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fee251b9e090c12a2c321f5008b2779dcbece0ea9097886743718aee9b261ae6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75823780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c690bafab12c24f7664b05904a5733dbdf5d48400a1fe99dc16ceb9b99c684c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:36:24 GMT
ADD file:169fa80cdaf558a1257d6751dc92cc0e23d49d492d49b2b3ee54f7402eccc5f4 in / 
# Tue, 30 Mar 2021 22:36:34 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:54:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 02:56:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:9192555ba03aa965b78e644fac9cb4305e27386da5748f2669982c47d7b4c5ba`  
		Last Modified: Tue, 30 Mar 2021 22:43:07 GMT  
		Size: 58.8 MB (58782965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754d65100617a4401cecee0e9aab2c897181d1ae44b0233afd31cb0bb4003f0f`  
		Last Modified: Wed, 31 Mar 2021 03:28:09 GMT  
		Size: 5.4 MB (5419626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5eb7e11b59e3e544a1588a8f7ce7715a221932c63d82819800360e78a0246a`  
		Last Modified: Wed, 31 Mar 2021 03:28:10 GMT  
		Size: 11.6 MB (11621189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a91676c9960fb162dc72e51871637a030b983bc5dca5951f2e6c0539f9bdba1c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69057191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257af8772141f0e489cdf9e46f7eacfd10836bee6ba5795dec0e8e4f45b96526`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:42:56 GMT
ADD file:c96fcc34ba5121a1c8780b0148c4b2ceaaa9ce733fac0a9830e3f557d45d7c9c in / 
# Tue, 30 Mar 2021 21:42:59 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:44:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 22:44:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:bcb476920ff38aa084b50cb5a5e43afc962acdfea91e11abaaef6fc258b79a0c`  
		Last Modified: Tue, 30 Mar 2021 21:46:39 GMT  
		Size: 53.1 MB (53147808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9941cdff622917fbf0a7a90b9b9bd51d58de5471a94cf52add39fa8b62837d6d`  
		Last Modified: Tue, 30 Mar 2021 22:50:37 GMT  
		Size: 5.2 MB (5150758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bd7897b18d3d481ba626f3a769e62e5ba9a769adc21d00817aec4735d3e628`  
		Last Modified: Tue, 30 Mar 2021 22:50:37 GMT  
		Size: 10.8 MB (10758625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

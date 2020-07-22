## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:0c98e93a7d57fc7c4adb137c7647cebcdea6fbb535f12159a205cc505d23edda
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
$ docker pull buildpack-deps@sha256:b9b20c5a55ac15095f95ed1da0773811ea9a0dbb041a5b8d1a839ef2c5ed25d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70027528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ef20525f2e3a5ae857d73e288591b2275f389c3f6f7dd5463b3c74e6de48d6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:22:28 GMT
ADD file:49aaad883f9932e76df5604c9353bdbc51cd2c74b986b57b2dbb4f3aeaa46404 in / 
# Tue, 09 Jun 2020 01:22:28 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:54:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:54:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:516091449b2853b301713d61c7a73bfbe7ae63ace598e76e1d5e9da246f88b37`  
		Last Modified: Tue, 09 Jun 2020 01:27:16 GMT  
		Size: 51.5 MB (51526780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3385de445fd2842a13718698d3fa721fdd723aaede5f9cc079f9bc763e815830`  
		Last Modified: Tue, 09 Jun 2020 02:01:38 GMT  
		Size: 7.9 MB (7920994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd8a6c64c26854ad6d393a2096bb413e86391dc5861cc5a961eb2c55eaa1f63`  
		Last Modified: Tue, 09 Jun 2020 02:01:40 GMT  
		Size: 10.6 MB (10579754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:30a749f4c7f66da5e6f31da95d9ee9f68956d4581a5cf2950d6f3cce00ceb241
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67271752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59c6340d3ea8789957913f23e11bccf5b0bfb6c1522ec5858883bd7e3789d67`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 00:54:09 GMT
ADD file:333f6925c41655ef86c1c55aa4628d69f324c5f263e27174c329a670a7408728 in / 
# Tue, 09 Jun 2020 00:54:11 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:39:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:40:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e514d65a1f93d9b21040cfb52628de87401493f0b2eb92f1a22c9d381f15df3b`  
		Last Modified: Tue, 09 Jun 2020 01:01:40 GMT  
		Size: 49.5 MB (49505780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da95254689f8f0bf61ba2fb5802bcfd31293fb3a56d7c3ee6b7653d100b6e62f`  
		Last Modified: Tue, 09 Jun 2020 02:00:49 GMT  
		Size: 7.5 MB (7500859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e156bd6d1d602264fe07ee2e4da6116f3627a0cdcb05d3f8452ab7e6a15fc5`  
		Last Modified: Tue, 09 Jun 2020 02:00:50 GMT  
		Size: 10.3 MB (10265113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f7067e3e95b49d917f577be3658080b7a86d40a09a0c6b3f474f9b39739e229b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64486247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7dd9f276027b2fe04cb5552ec0d96dca729665892678f6779b4614fd121476`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:04:25 GMT
ADD file:f137ab200a6655933430876a9a0f3c675ed39dbf4a73be4750579b0c66812888 in / 
# Tue, 09 Jun 2020 01:04:32 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:59:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:369ddd165e2326d11cacb52bac2afd8d2277bc9506399fb693a5a5eb336716ee`  
		Last Modified: Tue, 09 Jun 2020 01:12:30 GMT  
		Size: 47.3 MB (47326325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ada3ce7a1b468f31af8a1aa9f083d4521fbeedd0d46757dc5d1f97c49ebf17`  
		Last Modified: Tue, 09 Jun 2020 02:13:48 GMT  
		Size: 7.2 MB (7243269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab399397acddc3f7ce3a847871519a272a15f91ee26bd786a485bf8a41dc870`  
		Last Modified: Tue, 09 Jun 2020 02:13:50 GMT  
		Size: 9.9 MB (9916653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0a8ef4e73d140ec302562a650384a262c0c993b49794922a30f31f033c692109
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69083967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc8434f98245925c03f22f2d68834302044c7db1b8fb9c120bfd1a919e0400f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:42:14 GMT
ADD file:0f4a1ab6b889d98f711b241dde31787e633494e233067fe98dce73de73c2d7f3 in / 
# Wed, 22 Jul 2020 00:42:17 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:21:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:22:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3af651ddf153ddf8519b20c192d158afb60045252366ddc81e15c938b792982e`  
		Last Modified: Wed, 22 Jul 2020 00:48:41 GMT  
		Size: 50.7 MB (50699554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cbb2a684c92e31711be180ca45ac19643d88c12a51b2ffb58b6f120bc5ded2`  
		Last Modified: Wed, 22 Jul 2020 01:37:00 GMT  
		Size: 7.8 MB (7796374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdf66380a30dc7828150f57df61c812d1fd653b195e8f5d57dcfb885adedbf`  
		Last Modified: Wed, 22 Jul 2020 01:37:01 GMT  
		Size: 10.6 MB (10588039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b48f5a94b0a7c8a3ba287d786a4222d29c1e1f6de749a39fd037efaa3fa406f6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71704413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc17b2d4da31a481be444dd42f5fb8b471d92b25885d3a3701e1e3b820d79ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:41:24 GMT
ADD file:e46d18aaa3cf0eb6320c1b26b025ee8fbec78b2c4e4b3f5d4343393f1cbc769b in / 
# Tue, 09 Jun 2020 01:41:24 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:23:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:24:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c73d5896f1a36fe56b17fa2ffd2771c0b97b78e1b086e696cfa14b05618bbeee`  
		Last Modified: Tue, 09 Jun 2020 01:47:08 GMT  
		Size: 52.6 MB (52644936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf148f44d6df7cce1b2964667971df2c24df9d24505794d9324b303eff4da0b`  
		Last Modified: Tue, 09 Jun 2020 02:35:07 GMT  
		Size: 8.1 MB (8099472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa8c598f01778284c7219a5d6e3853bc2247c68a8e1ce0851af567867177c31`  
		Last Modified: Tue, 09 Jun 2020 02:35:07 GMT  
		Size: 11.0 MB (10960005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1b964419cf8dba4f97a895e3ea6a592442853ae0304ef3d6d8e89051ef550d6e
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68311260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39beed23589f41c91a82b8b807081bef8913fcd8fb5bbc9fd25f3d2e34bdc67a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:11:18 GMT
ADD file:2c0e5d72dc26223a4df660e91acd4c8c70d1b0ee1139c92fb9cb3f041d81bdc2 in / 
# Tue, 09 Jun 2020 01:11:19 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:56:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:56:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:78e0a34f3ecd34b89d20cdb0b915427acd1691184f4f7649f816759737ddb842`  
		Last Modified: Tue, 09 Jun 2020 01:20:19 GMT  
		Size: 50.3 MB (50264875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff174bb9582ec89056fe600d1820b6c6e7445d74e52537dfea39a4dd2b4324e`  
		Last Modified: Tue, 09 Jun 2020 02:14:03 GMT  
		Size: 7.4 MB (7447530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a44807d6533dba987e8712d4b69466283e5bbe760298ac86ccbe1ed4ea542e2`  
		Last Modified: Tue, 09 Jun 2020 02:14:05 GMT  
		Size: 10.6 MB (10598855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4e73fa23589a03cf252fe9b81936d7cf4ae1dde313722e519b1a29c953db0c6b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74947391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0440180d986d7fc31935111d60f702429c96990a0156321c1a4514c6af8f34`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:47 GMT
ADD file:04723d2d8de7d77c2c146c6af521e4a3124ca84c794e6ab9811528805e9f8a16 in / 
# Tue, 09 Jun 2020 01:23:54 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:13:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:13:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:57bdb75510f480914b31ba736d52f2bab13d126b2808f87359f0678e25b38717`  
		Last Modified: Tue, 09 Jun 2020 01:33:30 GMT  
		Size: 55.3 MB (55274450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c7f2f7dc07ba0a3435ca28dca3bc46cfbf238c2fd76e208d4b394f7a1de537`  
		Last Modified: Tue, 09 Jun 2020 03:46:48 GMT  
		Size: 8.3 MB (8346012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17a7d75882c1ba6c6a4c7b499aa5bd492b3bfebc6670ca2c2c3dac6675be974`  
		Last Modified: Tue, 09 Jun 2020 03:46:47 GMT  
		Size: 11.3 MB (11326929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:53c5ebde101bf80a9e4a408239365134b10b4932c82fee713de80d2f3a12949d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68949431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a26495d1dc34594a20e873692bc983bd8cb1829bdb20d9084e892aa05d7a32e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:42:53 GMT
ADD file:7128ed6ae7cb1b0852460f972a83bd593194b874b85235f9646a9357791b1514 in / 
# Wed, 22 Jul 2020 00:42:56 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:08:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:08:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:bcd13ccd7a5817e6de826ec69afa4d569b06c9f7beae2283db3d6ec9bf769fab`  
		Last Modified: Wed, 22 Jul 2020 00:46:01 GMT  
		Size: 50.9 MB (50903176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a0892473ebc7a0e196a8c4a4d81834a4ab9b414220c38331720f27f28c42e3`  
		Last Modified: Wed, 22 Jul 2020 01:13:10 GMT  
		Size: 7.6 MB (7590034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c697dc02560deb46fb2199992fe714a6a4f7df7f834fec55dac3ce014e699dbf`  
		Last Modified: Wed, 22 Jul 2020 01:13:15 GMT  
		Size: 10.5 MB (10456221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

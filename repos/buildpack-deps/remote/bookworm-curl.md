## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:69db317b7b9c8a0e054d8075321d84123af1e8d11740047f9c5a2c5f49407079
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

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d10628689f5130dcdfb760ae6565d9c614a2b638f23630ddf3ae221368f4de1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72207945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb44151dba504160187e304f53eb2765ebf72e0cab5b36cf8fb177e4f171371`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:19:44 GMT
ADD file:daaac4875b34dee73ff062c17a4763b2cf5726753df4e9700bbcefa0f88153e6 in / 
# Wed, 11 May 2022 01:19:45 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:47:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:47:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d68396ae84f0ca729923a79943893f43492725d77e7b329170777a2bdbb6752b`  
		Last Modified: Wed, 11 May 2022 01:24:08 GMT  
		Size: 52.9 MB (52944400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f77feabfdca5ac1aeded64e65a1943aee6d39af1ab6f3081de4bdd78eb986f`  
		Last Modified: Wed, 11 May 2022 01:56:13 GMT  
		Size: 8.0 MB (7999176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ce0f5a715fdcaa40b523d43006725581030728153a1a16199ef5a3097bd43`  
		Last Modified: Wed, 11 May 2022 01:56:13 GMT  
		Size: 11.3 MB (11264369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5377dce73de2174ec38309f94c864746db84bdc0a0010eb8fb4fc171083ee396
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69201021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b0d9e7ae24c971ec79c92a799784c5ce866e082441d7e847701b79c4eef969`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:49:02 GMT
ADD file:14b16b308b28ed8604a9f98d47e92522f709988224084eb5d2dfd30d3511e4a4 in / 
# Wed, 11 May 2022 00:49:03 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:01:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0baf2800ae4e68af843862199b558f14eac2766cea5651c0837cbd8ee827981f`  
		Last Modified: Wed, 11 May 2022 01:03:42 GMT  
		Size: 50.7 MB (50737437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1cacfec2c73325f6ee9727f3ee99a764a10620c61e467c786773e82fac2589`  
		Last Modified: Wed, 11 May 2022 02:26:52 GMT  
		Size: 7.5 MB (7536108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9a878bece2839158834198a327d030c397685382713b32bee43b9de34889dc`  
		Last Modified: Wed, 11 May 2022 02:26:52 GMT  
		Size: 10.9 MB (10927476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d6094de38834d6919a2a0846b6279f63e24e50f38fdf207fc00ba4f6358f1702
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66678836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579b3de38f3738fa85053125bc92610e39b9110fba4d08b84e764e07057b7ee9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:47:29 GMT
ADD file:ae0b1a579333a3c7912430243fe91f71f32d0e234d52667dd937f7cd23a8d3d2 in / 
# Wed, 11 May 2022 01:47:30 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:18:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:18:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1fdc9e441250146f7b7c78b0264138dc69a0b46d264373157ac1c2cdba7a552d`  
		Last Modified: Wed, 11 May 2022 02:02:37 GMT  
		Size: 48.5 MB (48475916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb8d2e8ff6478f1fc3388064baa5d6e059276c7a093a627bc6dc36d79ed4107`  
		Last Modified: Wed, 11 May 2022 03:43:50 GMT  
		Size: 7.3 MB (7269457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864281f702c002b286df6a1ef302fe0c7cde6323a4e78ec43b18718d930be2b8`  
		Last Modified: Wed, 11 May 2022 03:43:51 GMT  
		Size: 10.9 MB (10933463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2bdb08c18302d24323126613fbd20e3387a995aae955fcd2545cb4ecc2e1835e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70936670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40068327e4941832a318e33dc677f367ed31328bf68e03dd821b2fafa7fff65c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:46:19 GMT
ADD file:a50b6ecf9ed84e6e3bb43f96fd036c7ebaad7f94df16c3637d6dd19a6dc91701 in / 
# Wed, 11 May 2022 00:46:20 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:23:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:23:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:45306f5029ed7ce5685e65dccfaecf3f4a79040520f3ffb65eac76781218fea1`  
		Last Modified: Wed, 11 May 2022 00:52:36 GMT  
		Size: 52.0 MB (52041343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5de1fe22d36e48b637912dbd432cf236f1d956231296b275af61bc5cc951b1a`  
		Last Modified: Wed, 11 May 2022 01:34:36 GMT  
		Size: 7.9 MB (7853647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f57f959274f20ecbbfac9d0dd7e9dcbbc904e7eaf49a4ff37e3149afcbb2247`  
		Last Modified: Wed, 11 May 2022 01:34:37 GMT  
		Size: 11.0 MB (11041680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:dd0c5cc28cce5ced5483a39f67159af94687c6a51c1e1a872b4f0ac7c0b6cd3d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73586751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db94eb26a865acde44aedd65be4e194b77e8017990dd59bfab0a4fe82d9f1962`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:38:30 GMT
ADD file:ba0a6f659c101ad7b3c77be40e790f4ec4576f59a39c794974d82b28b115788d in / 
# Wed, 11 May 2022 01:38:31 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:08:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:08:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ca5b88a4b2f0398218cdfea0aee4d6b7cd7ae535feeb27719eb9603a02ef7752`  
		Last Modified: Wed, 11 May 2022 01:45:11 GMT  
		Size: 53.9 MB (53944746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8f042cf42269dcb19e8d0bd96f00d64f1515c06c0da6b2f1a0038169d0b453`  
		Last Modified: Wed, 11 May 2022 02:20:32 GMT  
		Size: 8.2 MB (8177691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70fbb27fa740e35a981b580f8380ae286a64f2544917232dc1ff6abfccce82f6`  
		Last Modified: Wed, 11 May 2022 02:20:33 GMT  
		Size: 11.5 MB (11464314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b55945fcc268fbfbe7591812e769b68a6ecb3c84b0e14cdcbc3fb8c9e062b552
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70733755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18a55f9640a6522cba5ccae6e59ec23227e3f18198e9d1a039bc25d4ac575ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 02:21:42 GMT
ADD file:023ba5f785e781bda7875c3b4c2f163666fe7b1a6a0fde74103b7799380a55c3 in / 
# Wed, 11 May 2022 02:21:47 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:58:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:59:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1315838dc3fae911b53ad8b9fdb88cdc4a2988e4a4924922837b71b52b18d1fa`  
		Last Modified: Wed, 11 May 2022 02:31:44 GMT  
		Size: 52.1 MB (52066926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2722654f4b60f68f8cf6d835f62f8bbadd36e2eae5b31ec1b4cd273785fa9368`  
		Last Modified: Wed, 11 May 2022 03:34:01 GMT  
		Size: 7.5 MB (7508574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4489d5ecab6698b42b344d5e72df6f74ea21c3b4a125cdee3c103f8e742b642`  
		Last Modified: Wed, 11 May 2022 03:34:02 GMT  
		Size: 11.2 MB (11158255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:82740ab2784f26262948ac13e96b6d92462f1593a8881b27f32b4fbcbf8a9ba8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77712430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7851d7fdcdd6838e60cf8c9f7afaf67fbfd152682acfcb26cfba3324767910d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:30:46 GMT
ADD file:151ed5fad83d0b4f27c9bb34e41c649df7b7b9cbe789e3036c44d12cf1f53a71 in / 
# Wed, 11 May 2022 01:30:51 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:07:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:08:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:49991d23fb52aaf7937c711b0196364a5011e41402f3ea986702027fadd27e0e`  
		Last Modified: Wed, 11 May 2022 01:41:30 GMT  
		Size: 57.2 MB (57150441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac162b59dc7eb516878ceab4828d006f42ec802f1755cbd5bc3126bf8d03c9e`  
		Last Modified: Wed, 11 May 2022 03:46:29 GMT  
		Size: 8.5 MB (8496430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f4172550a38e5e5676e20f279186dcd1ebf123a9b2693d032e98814590d62a`  
		Last Modified: Wed, 11 May 2022 03:46:29 GMT  
		Size: 12.1 MB (12065559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6c867a05cecf911a91697fe1a92e8fbe198efc7873580112c139467e5ae9b257
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70303809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb64a56a6d850dbdc9930256c4ebd47af9b1fbf76907d1be93249801519a593`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:43:27 GMT
ADD file:d38e77e014746a6349342f7d1cb5eada86f6e06423bf095efa6f182b4d038b77 in / 
# Wed, 11 May 2022 00:43:31 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:13:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:13:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b3467d807091357239fe13d54d3572c25afe85ac06c182eba9268af6bac8f48a`  
		Last Modified: Wed, 11 May 2022 00:49:13 GMT  
		Size: 51.5 MB (51483972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100136ea0fb238c9c9013ef4e514f31fc2bf960000bae26e543ca80d01ae2e12`  
		Last Modified: Wed, 11 May 2022 01:23:52 GMT  
		Size: 7.7 MB (7662307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d34880cfc5b88a3b84c6d27165e8e6e19b4a2668efdb3f9e2b27a5422d12f2`  
		Last Modified: Wed, 11 May 2022 01:23:52 GMT  
		Size: 11.2 MB (11157530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

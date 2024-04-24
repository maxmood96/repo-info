## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:2b948de8201eb7575c6cb5bc0a587d46a48972a504160ef7815cf3f6ace4f717
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

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:90ac5caaafde2debfc650ba977536ac0f43501cab0924b10b6bfe5454ca1bf85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76499330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd0bace3ff31ba1ffafba5575dfd019e01201b257f098eac7c768e5bb89752b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:30:44 GMT
ADD file:9465a54824a47fac7a8656f1a1d95dc38be8c06ce3809b905d67ff7ce345ce64 in / 
# Wed, 24 Apr 2024 03:30:45 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:18:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0e07e2723f97d31d3cc6945b2518b9912a7301e652e09eaac68f1eec11330efa`  
		Last Modified: Wed, 24 Apr 2024 03:36:47 GMT  
		Size: 52.3 MB (52338632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95ad0980b95c8ae82ca2a8d74a4757e86cf14913e53a8be04dbf6519d8fcdc3`  
		Last Modified: Wed, 24 Apr 2024 04:25:04 GMT  
		Size: 24.2 MB (24160698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:3722005cd02b40df5892e2c14e9bdf9fc0997f6e90ae0e9a1a2ed208beb42c9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72475099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019c0b19d318ffcace2fdee159dbcf3d536a6588f7916347c0aa2dc912552e67`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:54:47 GMT
ADD file:cc1e9468e81e521d409dd8b88fafcaaa5f105f627b1eaef62c896e916213ebc7 in / 
# Wed, 24 Apr 2024 03:54:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:65330d4a78bd6d548d7f0dc559b639551ef46dee6b7d5b6d0366a8e6d22f8ac4`  
		Last Modified: Wed, 24 Apr 2024 03:59:41 GMT  
		Size: 49.4 MB (49434297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcaaad035748a99175cae78a5b89744fde3b0a273b1aaa1a736ed21b63fea6e8`  
		Last Modified: Wed, 24 Apr 2024 04:31:48 GMT  
		Size: 23.0 MB (23040802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0a217dd9e1e37c8cd38a799210dcbe99740abc35c41d911b1e4eee963217fbb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69285729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1221941150f6f6fc31476dc7a7392f9a069df92ad0d75d1b35605213949f6c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:09:21 GMT
ADD file:68fc8102f9cd1f1d24d4c270a545146ee6a7ba7fb9d8b6f00d511cc30cae87d3 in / 
# Wed, 24 Apr 2024 04:09:21 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c2f00d681f2c70b358e621ba07e5f58c2068fd56d05bd0f1fac5a67972fc1624`  
		Last Modified: Wed, 24 Apr 2024 04:15:19 GMT  
		Size: 46.9 MB (46930352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9505d03d248caf9d52b35ec3ac69ec1aa253a9f5ad5518bad0ae8fd609e08b`  
		Last Modified: Wed, 24 Apr 2024 05:07:26 GMT  
		Size: 22.4 MB (22355377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:237011cb0e8b7cbbaac3052faf5ba301f216bcb4c318db3c384e02e32d1d2fd9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76072974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eecf5b3feff7578bc58f0490e1659c0f395a0f6df1f6480789622be1263bd77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:42:14 GMT
ADD file:d3b8312bf9d9df431c2580a0add351c37786bf532e919d2af2638c2fb93062ff in / 
# Wed, 10 Apr 2024 00:42:15 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:29:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:782f2de9bf3353a68116b53b16ae9a2387174b31cc46b4c9b4cf99de0a6e1af4`  
		Last Modified: Wed, 10 Apr 2024 00:48:17 GMT  
		Size: 52.2 MB (52193812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ae77305c2bd54ea5f2ca2a76ab1cd96f744878b54d2b45e6edd47242bfa248`  
		Last Modified: Wed, 10 Apr 2024 04:35:41 GMT  
		Size: 23.9 MB (23879162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3706cd66b1b99ed3cda116743e493d770a7a052c89767f469977c99f62b45386
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78466898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce352ed55a94925e6599783d61078815c435902467869a71d4a373648b7e3ee4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:41:36 GMT
ADD file:ed473d3b605a6b0948955f74f5dca4dccb14a7d6cf9d219891c6110ba6572f94 in / 
# Wed, 24 Apr 2024 03:41:37 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:38:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d51399cd19ce178fe1bb087a7ed5b07667b07b1dd98716723177809157778ffd`  
		Last Modified: Wed, 24 Apr 2024 03:48:34 GMT  
		Size: 53.2 MB (53187646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9cbfbb03c89e50483bc6f14d5feeea6ad8da1d06153c1bb027ef0f401de94d`  
		Last Modified: Wed, 24 Apr 2024 04:46:54 GMT  
		Size: 25.3 MB (25279252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5a90f774aa20ef7bee869374c6ce6ce67bb7cd271f7104ac8f0069e7907e586f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76035399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6774a01d3cff2ad2403fd9775c5b9a54b26e609da8002839a46c89c0d72ad9a3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:02 GMT
ADD file:3528147ed2ff17c452628f4992045437579a2eb00d2eac617b8542d7706b58f9 in / 
# Wed, 24 Apr 2024 03:21:07 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:21:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3d9ec6cbd0472de02f68ab46797d6a2b9840ccc575c40d8562ede5007cd7622b`  
		Last Modified: Wed, 24 Apr 2024 03:32:27 GMT  
		Size: 51.4 MB (51411293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a78282402894106b7f446ef7995bf01264e8c063d4dc3f3d1cae34bb31b7f5`  
		Last Modified: Wed, 24 Apr 2024 04:40:34 GMT  
		Size: 24.6 MB (24624106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:507d22c0a16e21d46626642b55333c87a18fd753a06777345bab369677dd5a40
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82509816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e19de28f2d5140dc40df071a469dfec142da290ba4bc00d3e31377f77c061ff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:23:55 GMT
ADD file:49f2825f9c5b50843535acfc958249a70e087e06e06eb89df8fcaddcbf45564c in / 
# Wed, 24 Apr 2024 03:24:01 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:15:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e5bb82112ecd21be1be5a4a97a1beabfa110a5d5eb34d4561d4a17294d7f44c6`  
		Last Modified: Wed, 24 Apr 2024 03:30:40 GMT  
		Size: 56.3 MB (56253273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d091ba74dd77c332622f47e69c38784baad91176e28aa55e464ca78ff6b4b3`  
		Last Modified: Wed, 24 Apr 2024 04:26:37 GMT  
		Size: 26.3 MB (26256543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:26bb164a4f2832899655c5cf4d1decde16b8491dc19e2dd2b8f35da472af2139
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77061783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d58c758dab604899a390641bc56de9eb153597b2741cfb6ecc379c6728cad5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:46:49 GMT
ADD file:13427baa96123e72c30f8ac6ca708a7f7d3be7f0ac0833390d7414c8d1e438e2 in / 
# Wed, 24 Apr 2024 03:46:55 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:18:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3f21e8a280ca933b265ed896c2cfa5317f05fac17b7b290b87455ee5b3f92921`  
		Last Modified: Wed, 24 Apr 2024 03:51:44 GMT  
		Size: 51.8 MB (51766843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cd83a1cb8c7c3071ddfefcd98acfb1745aa44bd51fc629f0c9a3a31f182565`  
		Last Modified: Wed, 24 Apr 2024 04:25:56 GMT  
		Size: 25.3 MB (25294940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

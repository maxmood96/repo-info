## `debian:rc-buggy`

```console
$ docker pull debian@sha256:bba204104b84c0c7cdaef633bf9f29524fa1a971c57651f1274a6baa7210f469
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:f2e3288e6e5b3d51b836dd268ffdbd958c7b27b68eef22ad7460a0dafc8e2a0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49534529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a32f0ec79ce02a49ce08315c4f6c0669ded844d7e658aa97cf224c6b8a21d85`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:22:27 GMT
ADD file:69815228666696b3cd3b2799492e3d9cdf4f513ccca5c1cc9282f6c569cc8730 in / 
# Wed, 01 Nov 2023 00:22:28 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:24:10 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bf371b8152e5df155015cbda7e76bcf445a8be262f7017a9c2cd27a64c3bd875`  
		Last Modified: Wed, 01 Nov 2023 00:28:24 GMT  
		Size: 49.5 MB (49534303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977ce4908ac3ee3a8c081a74c314c0fde02358bce0ca20dee97da86c2bcd7f4b`  
		Last Modified: Wed, 01 Nov 2023 00:31:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:56968abee0993d5c33fbd2464646383ef03641d05a0319e6c6670003e6339eb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47192684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b794a4d18296c727c66aa9dbd79519f3e8ebab0f8447062184219f3e1b3d4c4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:49:10 GMT
ADD file:3dfec265d80292cf14629bdbd49822be7a5672ab8299d43e9ec734f6e032c8df in / 
# Wed, 01 Nov 2023 00:49:10 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:50:21 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0609920749c8743a3627a0a7a377598014123518f5e0ed7f1443c78c8c9f3446`  
		Last Modified: Wed, 01 Nov 2023 00:53:10 GMT  
		Size: 47.2 MB (47192458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047a9515bd11731fc153996a3fdc5750fdf835087f55b414cc4c80c57b064a94`  
		Last Modified: Wed, 01 Nov 2023 00:55:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:269c1f1eab0aa927257f3730c121061071d00c5fbbc5c1710552d9ce520f888b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44981635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884f29af2a0d8cca590ec012eaa1ae717a78b4228db50a3198caacf0b8224e5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:59:14 GMT
ADD file:a72fe3de4b178dd8b7c48a1dc98d4c14520570e5edb66049dfe2cd6bb0a5dd6c in / 
# Wed, 01 Nov 2023 00:59:15 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:00:38 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f6e9a66eb905933433a5a2a8c16e480468f3731f107d5854bac12ef9a79bc271`  
		Last Modified: Wed, 01 Nov 2023 01:05:19 GMT  
		Size: 45.0 MB (44981409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241ad68737ee0b1a9436df9cc162586e0eb9cee909fd6e05fcb7f392fc8133ec`  
		Last Modified: Wed, 01 Nov 2023 01:08:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:bb6cf6363f358d74aa42addd8a1e6d7e6bb53cf7c39f6f8d16f20bd50a8db55b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49553064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206d15c70b9ee40e17687b45761d705ddc6a8add78aa0258a97b061981b19715`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:45 GMT
ADD file:1a4ef85bba464538c4f87a65a055d954fc8edc51f26efd06b43d8ae9f7e54f7a in / 
# Wed, 01 Nov 2023 00:40:46 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:41:52 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ba6956ade110f0fe56bbad19a8d10b1eb0ae1b1006ccba5fadff0026a00dbc20`  
		Last Modified: Wed, 01 Nov 2023 00:45:46 GMT  
		Size: 49.6 MB (49552835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4d3b0683784a0a94f80a8cf1e354ff976389a7b79d74f679437f39a3d0629f`  
		Last Modified: Wed, 01 Nov 2023 00:48:16 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:8eda941c91bbecfc15b4c4332dc14729239a9738a3d1222c1c7490b1077a71f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50516711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a918e0c410bbc6268dc0d88fb1f32bf42eb8a1a0c69d9f77883a18d879b1a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:31 GMT
ADD file:0aa90abbd80c68d937903de7ac8fdcce0f516fdd70f080b677af1e2322c000b9 in / 
# Wed, 01 Nov 2023 00:40:32 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:42:03 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:96660bac4658b1bffb27e96ac8ecc86753a1844f042ede32c4f1faef702dc202`  
		Last Modified: Wed, 01 Nov 2023 00:46:42 GMT  
		Size: 50.5 MB (50516486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651939b5e4b021a7baedc6901bcf6708f6f2c0b9dcbc402aa79b41b2031f892d`  
		Last Modified: Wed, 01 Nov 2023 00:49:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:e6c513cae49bbd3018ad42558f76d4c51f14d84e5da053e46756d6466cd7891a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49326963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a759bd311d7ac908495a5862e2f89a5ff4e2b7ab6facca25183c19a692bd60`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 01:12:08 GMT
ADD file:e27a157c42d1aedcb0f6cf695f1f5c31d442488e049826c940509e2288537427 in / 
# Wed, 01 Nov 2023 01:12:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:17:40 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0eacf4d958160d2729e1bb31fbb12227afa7536ce6304928b13c2c65d297f9b9`  
		Last Modified: Wed, 01 Nov 2023 01:23:11 GMT  
		Size: 49.3 MB (49326735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15704b72446682e29b63116a2bea68c800a78ca1cd336f97d53a59dd6293030f`  
		Last Modified: Wed, 01 Nov 2023 01:28:52 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:05421ee8fd6e85b003709f0f94dd17efb2068fa9b61b335dd7ad6bc46fb9a718
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53438388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8cf6d1e21d50bc28da47e5f9a9bdf96165f461fe0c71edd8a19f5b6a9faf38`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:22:46 GMT
ADD file:b4e182cbec02f1d3bb7c8ff0ef09924ac255ba6717bdd73f24d0a6114ff305d6 in / 
# Wed, 01 Nov 2023 00:22:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:24:54 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:46cca77d78176c861335b7b91e20d7b4cb2b3a75a124c300124de5818b724a9d`  
		Last Modified: Wed, 01 Nov 2023 00:27:59 GMT  
		Size: 53.4 MB (53438164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84917881199efc19928d732dee6a6c18a7f83d0090bc5a2154def3d459beae`  
		Last Modified: Wed, 01 Nov 2023 00:31:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:b302a85a3582e71719a7a80717ef72379422b961784e56de7c6c5ea7c2ee103d
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47903906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb83e93c0b808407063a612eeb108f6c1e1eb652a7d5da26e9df02f56f5ecded`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 01:10:39 GMT
ADD file:10aac34e5379cbca42071631c10447895ece01063babea5769d7a1ca12c1d5e1 in / 
# Wed, 01 Nov 2023 01:10:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:12:25 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8b987d803641183eb947c3e5f17a8a822be136b9081a3e13a881ea93c5b5c153`  
		Last Modified: Wed, 01 Nov 2023 01:13:28 GMT  
		Size: 47.9 MB (47903676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62875ab43e010da4eb22e353fd874041bd878ef9b186fb8fc065673885d65af`  
		Last Modified: Wed, 01 Nov 2023 01:15:46 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:b10d882632ab2a6f1408dbd72b650fb80271cb81b026ef871907694d42d5431e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48967202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcec7c59d87fc304307635be7b2f63492a3b9aa890b44043b40ace645f8f3d2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:44:04 GMT
ADD file:e94f75ffd7aa648bb85fefcceb02afa58747273f05e89c473c1ad438c3ba2345 in / 
# Wed, 01 Nov 2023 00:44:07 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:46:40 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:43e2d693d4cc2a3e58c2344ef771699434d5f0e6ffb98ac8bdb822ee0e2534fa`  
		Last Modified: Wed, 01 Nov 2023 00:49:25 GMT  
		Size: 49.0 MB (48966976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1c8e6da3e0cfed9a1d2340fc5fd47fd045356a13d349b34e7bbf45d027ba08`  
		Last Modified: Wed, 01 Nov 2023 00:51:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

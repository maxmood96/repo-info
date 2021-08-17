## `debian:stretch-backports`

```console
$ docker pull debian@sha256:99ceba876e4734fdbc25d548b66eaf6d583d125cb0bb6c17f4336fde6d61a362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:79439258d71423c2cdb60669be27a80fa573c729f65cbe1d78bf709827a62b61
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45380187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cdee665c2be0d45a30418831ae904d16ae31466126cefb1197c43cff1159f16`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:25:56 GMT
ADD file:0d0aa1ebd07b0f301aaf1077d1e9f2e9be1859510dd8535e143571b347a2a379 in / 
# Tue, 17 Aug 2021 01:25:56 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 01:26:00 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:eb18d230e067c240479c6a3f842e7f9d4ff1088e3072d0a3245829c4e356623f`  
		Last Modified: Tue, 17 Aug 2021 01:33:03 GMT  
		Size: 45.4 MB (45379966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e3558a2b290f8037f7ebd5b6c30b59cef977ff677fee6c454285844228f17d`  
		Last Modified: Tue, 17 Aug 2021 01:33:18 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:558cb9ac6e74f1ec9bf5652c2faab80d3b85933402074078f14786156435a65e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44092122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472babcb2b3b13d4eb7c7f8e583c3b5f58e459a8e266110f5e8ab6b14be73a74`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 02:00:50 GMT
ADD file:77054e1fc1091d0e0800f856514f36121a7b447fd1e2df32e6c8ff77e6136c66 in / 
# Tue, 17 Aug 2021 02:00:51 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 02:01:05 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bfc6a97ccb61e1bee683ec639f55514bc40b09ef15dcd73c928632c03b3df06c`  
		Last Modified: Tue, 17 Aug 2021 02:18:40 GMT  
		Size: 44.1 MB (44091900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b38538e75bcf118cf0562c3d53e420af15657f398a9b3154d946f33f273ea1a`  
		Last Modified: Tue, 17 Aug 2021 02:19:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:73fd8813243bb6d441bf69a2192353227d143e0bf73ffa7c91a61737a4d8bfc4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42119969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2452d13b01278f3cc29117ec55e5ef96022fd3263e0d985234dea55b28d7592`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 02:19:00 GMT
ADD file:5e5e5a4e13ae8e36740009c29111838a32d9901b28809b485c841d25d550698b in / 
# Tue, 17 Aug 2021 02:19:01 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 02:19:15 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:30d3c67f4f95a7d99559389477234b45c05024484d59cec2d66264610a623fe9`  
		Last Modified: Tue, 17 Aug 2021 02:36:17 GMT  
		Size: 42.1 MB (42119745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd7a6db236c36b3cb6c15ce09518f04730db360cc9a617d5dfb04ca2ced27a8`  
		Last Modified: Tue, 17 Aug 2021 02:36:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:697af511c9c06e1d0c0befc0dee9e99cf4deceef077bcaa68d6f10c8c8a5e4a9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43177877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f13eee19fb4e258e984afa24786a12d3e01bc8d10776d7826bf3cce4edd2a45`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:17 GMT
ADD file:79e0d0ec943ec405612e2310514d8f0c72cf83483eea6d5f1a7c28b36fa21cf8 in / 
# Tue, 17 Aug 2021 01:48:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 01:48:24 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a410f7a7fb8af899e64ef008ec59cc8062766e91abbf21ba5cee65faac7ba3fa`  
		Last Modified: Tue, 17 Aug 2021 01:57:32 GMT  
		Size: 43.2 MB (43177652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ca5819706f75e3d25fd6999123dc5f1b3d709fbb8ced56de32cb094211644f`  
		Last Modified: Tue, 17 Aug 2021 01:57:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:4b76c53340cdf5e1901747f0e9a5c3b62b826448ec5eb6e4304d27c7d2b401ab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46097444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652d14990e5e1ee5c9dc9600b38f076851141b5b3a79a637cc6b3525a067f3f0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:43:45 GMT
ADD file:e05a48da77b08cb5622f87152f4378e29fbb9bc65a76c762d45e488e30adb647 in / 
# Tue, 17 Aug 2021 01:43:46 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 01:43:53 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fd774782ceed955e627fdc8415668afabdebb5525036f0dc871ec023eb317787`  
		Last Modified: Tue, 17 Aug 2021 01:54:38 GMT  
		Size: 46.1 MB (46097220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ca004e8d0aa480d092fc59934558c252a730cdcbe1c0c3932b019e1d7fb9d0`  
		Last Modified: Tue, 17 Aug 2021 01:54:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:61010f6d5dcf2c784892d643bf44764c7444eba9e025445efcba8efff6186020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:57c5d4498d16a489a761cb0efd2287972d7cdf191a0804d19b312f31764fba55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50498339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe1efded4486af4230953127157b95956260555864414c5de11b119b24e140f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:42 GMT
ADD file:f3bf588464e496d00fb3562c0d42f6d5bd09898f67637b65d8de6d81906fa9a9 in / 
# Wed, 16 Aug 2023 01:00:42 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:00:46 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c42cdd0c9d611863facf1c5246bc75505fd18ab237ed9ff0a23dd3bc37d1eb94`  
		Last Modified: Wed, 16 Aug 2023 01:06:11 GMT  
		Size: 50.5 MB (50498109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18130f89a7405494aa8494630183599ac036369faa981dd78ea6e2508c3ee0f1`  
		Last Modified: Wed, 16 Aug 2023 01:06:20 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:3b0ae0ea4a4a911bd3346c7f891fe7125965420df13fbd3e2fbfffad29ac5f4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45966432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7768f5a26e3cae96b4259e349be16e22c70a56b7e5adc568e4522b44ad0cc17e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:18:02 GMT
ADD file:ae35db5b00abb4a7b5f558b7adaac3c859c5654ce7b80ddceaee9af0fc482c77 in / 
# Wed, 16 Aug 2023 00:18:03 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:18:05 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:55478191438ae746a1d7b9f9c190aa0bca5405b130ad9bf7401d1fc3d471e21b`  
		Last Modified: Wed, 16 Aug 2023 00:23:06 GMT  
		Size: 46.0 MB (45966205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d1d600834ca54cb61f31c030dfe01f46ee122f8e3092d7d642fd54ca7b2ff4`  
		Last Modified: Wed, 16 Aug 2023 00:23:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7499de3f0216ce0ab613355a5c3bd857e5a6f1881eeb3eea17c59438b361315d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49291185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588673c298c1540d9f5b512ff947f502d1d96bcacf774e587d76d4f420e5c1f5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:32 GMT
ADD file:652930b08ffd1d8976a47ed7e4ea264b79e2c216bbdb53069fbd9af2dfe4e5d3 in / 
# Tue, 15 Aug 2023 23:40:32 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:40:35 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:18753a02e00a94d798f7f321b3e48c192a039e1d188042a5a2990c52ab5c5b2a`  
		Last Modified: Tue, 15 Aug 2023 23:44:53 GMT  
		Size: 49.3 MB (49290957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b75186aea109c014f21ec5352e16f2be1c6c254bfea9e319151214f07ca929e`  
		Last Modified: Tue, 15 Aug 2023 23:45:02 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:9d2d3cc1f09ebfc2485db25d89820924d45d6221bd7482fefe53985b57a49811
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51255689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6ab7b40d38f0347ffbdd0f595bfa7ad48ce39fdfe1b59ec77c10dc9cec8152`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:53 GMT
ADD file:5e5c60db439ac2712e5cc3c01b553d0a0712fcbf936793c0a7e942d7480c148f in / 
# Tue, 15 Aug 2023 23:39:53 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:39:56 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:77ed33e8d735fc81e4fd83df07b93ff059e1da209645d4ec93fd47938b69bf8c`  
		Last Modified: Tue, 15 Aug 2023 23:45:17 GMT  
		Size: 51.3 MB (51255462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d716e6e1ffd7dbbe286b8f6bf589082b13ecc874730e2cf1d4b28cf4d4dac62`  
		Last Modified: Tue, 15 Aug 2023 23:45:25 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

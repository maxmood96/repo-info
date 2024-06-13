## `debian:testing-backports`

```console
$ docker pull debian@sha256:e6d684c45634b310b29108588772a8873f6bb21c9489bf7cabd4689e4fd24d1d
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:cdc4479038f0c327071e5a84f543981117f3a6fe22477dbef698b9baa38bd7c2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52277993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267cc43af3f7d6df330a5e1083e1ab9fdf98fdd8eea800d70ceb4c1b870e8078`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:23:10 GMT
ADD file:641543c898704e70b2f0fdc6960cf28865c10fff8d9e502bca973f3032f48ee5 in / 
# Thu, 13 Jun 2024 01:23:11 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:23:15 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:86f6cd73387be605d114f6a6b93a5a5db028ff60a33da4e42acb4d10aa73746f`  
		Last Modified: Thu, 13 Jun 2024 01:29:06 GMT  
		Size: 52.3 MB (52277771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018a76bc384c0d11d64969d1940120e7c6e267183e23c1e7ebbbf2bb1aaafcba`  
		Last Modified: Thu, 13 Jun 2024 01:29:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:2afe516196c461caf4da4ec74a77a964c45bce716b3988bf82e11032c0341527
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49352642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003836e2bf9cf8d7f30ee2e3f57322c697e58bd3a17116651767678dbd983de7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:42 GMT
ADD file:95de34bbd076618336102788b5fcb306d4a121f298ddad1bd2ece4c4b3fc3968 in / 
# Thu, 13 Jun 2024 00:49:43 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:49:46 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:484c015040269bba2f83c5c3a4d5c5e4a6c8003a6319123d7fb13e97b3c0d215`  
		Last Modified: Thu, 13 Jun 2024 00:54:19 GMT  
		Size: 49.4 MB (49352420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c862b721b55ed78e87e1bea526a56e86163742edab149dc12afd27d8eb2357a7`  
		Last Modified: Thu, 13 Jun 2024 00:54:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ac8e962aa6db32d244280312c10ee2fd1dde565ed8f3c2bf21405181adb739f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46856399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cf2a4b1aeacb3a56c4a3e61361cc01d0a0bac6ae2af3dc9eeb383e65dd9b07`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:59:30 GMT
ADD file:6e93a848a7544abb1cd1505650e56cd33dd297a0c61d1d21a578ec1e725fb264 in / 
# Thu, 13 Jun 2024 00:59:31 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:59:33 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d1d6a687a0988c1208470b4319f472e5f98a5004a928d571b18196b1ad380174`  
		Last Modified: Thu, 13 Jun 2024 01:05:20 GMT  
		Size: 46.9 MB (46856175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd03eb75f0b4d710f24b4d2d0b78a8ee28243f3ad00e830dd9dde2ff26da7e44`  
		Last Modified: Thu, 13 Jun 2024 01:05:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f0add804e585f615d53265c616f6c5af0a1e3bcfb1e00289bcd684f3b8ab6048
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52514625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5bf1cb1d398f4d680c66c83094af7e8cf7f7b994ca22ffe2b186f1500cad97c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:20 GMT
ADD file:01c0f4d76bf24fca2751abe72efa9c7df45d0b92b1a1e4ec04166ae4f86e0e5e in / 
# Thu, 13 Jun 2024 00:41:21 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:41:24 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bf8309700f9bbb327bede604070aa78243b4af661147b0f82fa09c9fee807790`  
		Last Modified: Thu, 13 Jun 2024 00:46:35 GMT  
		Size: 52.5 MB (52514403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18702e9088899472cd4d42905614814b137e4f4f44bc5390052f40866414f3e4`  
		Last Modified: Thu, 13 Jun 2024 00:46:44 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:2eaa28f6a4dca323ec1cc52ba2e49c2b4a7f8c47519d6f2f22697289126d386b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53147697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e07b007293827bafd1acd834811552ad43f5649b567aed6db9426051c3792c0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:09 GMT
ADD file:685dcbc6178be098b9ed64d37b8948db65fae7e07d56359994a6b0c00171bffb in / 
# Thu, 13 Jun 2024 00:41:10 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:41:14 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d415acb192e85e271bbf788c65fe917f7b79913443ff392958f72944a6e59f70`  
		Last Modified: Thu, 13 Jun 2024 00:47:20 GMT  
		Size: 53.1 MB (53147473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38475fdaf46e81846cc3976238dc83bca327da2eabe63a55f920e1421eb59475`  
		Last Modified: Thu, 13 Jun 2024 00:47:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:82d65dab2eda23d2791dda448e9f249ac43500b8f20548c8ab08769307ef1604
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51137471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34250124dae55c86265010db3efcee003c35a87d3b00dab6c24a18bd90912acf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:16:10 GMT
ADD file:3f8d6b4afebbf2d367fc66ce07b35e3a5e81c6b1bda346ebcc03ef171b92d042 in / 
# Thu, 13 Jun 2024 01:16:16 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:16:30 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e22f176e69174ee92c123c29b2b857d3dea8c9c20d1e82514f48264837808c24`  
		Last Modified: Thu, 13 Jun 2024 01:27:48 GMT  
		Size: 51.1 MB (51137246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99fc1090f9701b8085ca928b5878b04c7381ba6e9018e0a3be8b2ba02858821`  
		Last Modified: Thu, 13 Jun 2024 01:27:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:e66d634887710ef143250c4306a0f019bb1e7abda6db07d637c749d32708836a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56146741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8ef7584c9ede8a287d790c9aa12f0f945a07691dd15b4e944fed22f8e5a3ca`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:18:57 GMT
ADD file:a0c25580162c011cc186a00ff527d3dccd6ebde9583f49d925d9c4a0bcf07470 in / 
# Thu, 13 Jun 2024 01:19:00 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:19:05 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c17ef498846c0b5766aa996aaf6ece599537a2132a98b21abc95e98de5797774`  
		Last Modified: Thu, 13 Jun 2024 01:24:41 GMT  
		Size: 56.1 MB (56146522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aaa40e47a5ea3ea096653a979de3a4676c1950a260ddbe57304744a223095ad`  
		Last Modified: Thu, 13 Jun 2024 01:24:49 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:68319cfce1c3a8a8356cb580576013565b8316a500c5bed272cbe4589e215b93
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51895567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39534e3381c3cc3a8dc1cb7cd29375c30bfbb124d3161c6f9234b06c41c690bb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:44:54 GMT
ADD file:10228c4b34e8ce576af7bd79fcb17c133b1ea50ced4c4e3086c0d133e54eb0a8 in / 
# Thu, 13 Jun 2024 00:44:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:45:03 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6eb6b57af9d4e65be8055ff33f3b560adcb2c0d5f354553283f30c55e9a081f3`  
		Last Modified: Thu, 13 Jun 2024 00:49:43 GMT  
		Size: 51.9 MB (51895345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c046694e3f8cf539d64a77d663312447c384258b536ca8db6d85c5efc544f86`  
		Last Modified: Thu, 13 Jun 2024 00:49:50 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

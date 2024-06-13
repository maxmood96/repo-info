## `debian:testing-backports`

```console
$ docker pull debian@sha256:074b013e3185db0e462f924eeb1a5d2e1c0d972ad062fb452c3eba4ba053814b
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
$ docker pull debian@sha256:9298beaebf2aedd4746fd1599d5a72d2c1e7a2f6dbb259b9db810273dff85e10
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52640983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a0a7891eee53879e06e20984bf162fc8025235f16871c93959b3cc805801c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:30:16 GMT
ADD file:7496a8a75f4744a39550a0ba17dae1225503232d27a03ceffdd47b5c7496d5de in / 
# Tue, 14 May 2024 01:30:16 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:30:21 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b6f1021887c3594f59c8eb101447edb6c5351c38c0cf447c87e410dc535562a8`  
		Last Modified: Tue, 14 May 2024 01:36:12 GMT  
		Size: 52.6 MB (52640763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211a30900ee60495d700e97d82e3323b2a2e495c852bf5b4814e93cf20c6bbdb`  
		Last Modified: Tue, 14 May 2024 01:36:21 GMT  
		Size: 220.0 B  
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
$ docker pull debian@sha256:98849477b67100992c40fb24040ce005627d84a4f65d9b9c9c219102ccbc1532
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51533917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409141119330ee63d87491e2f28ccae18eed2e56f8ea92cbd7a29b05a7b6ab06`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:16:42 GMT
ADD file:ac7d1ed39533cc3bc7624aef54cf7553e1500273a4a8df8143d4f3e4f1cf95ff in / 
# Tue, 14 May 2024 01:16:48 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:17:01 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f4cd48e7b4274d56787be10735d547cb60a8df883b0118003da4600c0d0b1070`  
		Last Modified: Tue, 14 May 2024 01:28:11 GMT  
		Size: 51.5 MB (51533694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367f4d0f58fb5cb2e4fbd4a7b9f13a280876738f4b17e79f7a0a3d0f04a977af`  
		Last Modified: Tue, 14 May 2024 01:28:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:fe502f591d769bfb6797c55b47ad5858d8a5da718648907fc58d310abf670b50
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56531720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6562534c972b033bf83e95120f51a8ed56feb3ab33fba89aab5221c95131887f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:21:47 GMT
ADD file:1e419951dadece1f9151a37e9ad50f8131769e122c138fa53d258e388386961d in / 
# Tue, 14 May 2024 01:21:49 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:21:54 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d17c53859f4c9ab9a4d5fad8696f2c0eb323a7e2f067d4d131095bd5ef2b0f91`  
		Last Modified: Tue, 14 May 2024 01:27:03 GMT  
		Size: 56.5 MB (56531498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261304f6ffc126ebe16d9af78f6190797fc75976d4103577bd8f9d9fa8cd3db6`  
		Last Modified: Tue, 14 May 2024 01:27:12 GMT  
		Size: 222.0 B  
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

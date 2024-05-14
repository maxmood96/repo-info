## `debian:testing-backports`

```console
$ docker pull debian@sha256:51a2d8090ca3e7505f6a133694dbd5f252e1b0c513fc51aa9599e07b5c43460b
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
$ docker pull debian@sha256:f7d09c503302629b2ee53ad70e19771070bd3d4a37389533f845f01dadabb98e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49744988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8c38514c0d92357c4ea6d9114f75e86891cdb86c02037e631d6f25e0fa94ea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:49:44 GMT
ADD file:c9afe5b0a108631c043e9eb0d4e5e257843ed802ae7705c0851e82e73d538611 in / 
# Tue, 14 May 2024 00:49:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:49:48 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f0c10670fab205862628f1e7a3f0e32d0a10c09fe90e24279f858b7f1f447b9a`  
		Last Modified: Tue, 14 May 2024 00:54:13 GMT  
		Size: 49.7 MB (49744768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b5b39da926b4599866cc9650d5efba9ddc734a5409372eeb40fbf32b5f66a7`  
		Last Modified: Tue, 14 May 2024 00:54:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e8c23c16faf1f39d51cc6d3b6a4d16e75fc868633525d129e86bf7c8f2b39851
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47252750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd45ae1432cb751bcde7bf4b02b77013be6c1a3dca30b7fc7cc2c99b9192ecd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:10:34 GMT
ADD file:5550cf56499f0435dbdc5db1d53fe83d5b85d3431ca6cb0ff86a6226354a3463 in / 
# Tue, 14 May 2024 01:10:35 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:10:39 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6ed9cec5e878340c03c975ea9c661a894ef98374f8ef9f19235757460d7a58ce`  
		Last Modified: Tue, 14 May 2024 01:16:22 GMT  
		Size: 47.3 MB (47252528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f4a3722752f88b43d8bc174caa50d197d8d9e6da9705bf621313774e80297f`  
		Last Modified: Tue, 14 May 2024 01:16:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f740d9b039179946b8201cbfc645c5c7c4487793e369408bc0128055256e387b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52912298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98af461e087c21a81bd36ba2d9969b6a12984e71d4a410551b86c06737bd39d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:41:08 GMT
ADD file:d7aee0a25e3d206c1ca526373ab1236a244025e76ee8802b2de9c7851fc7fc80 in / 
# Tue, 14 May 2024 00:41:09 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:41:12 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:25b146dc3d2d8d07e05474869061ffbe0ccb76a9c19a029a9eb03dfe587453f9`  
		Last Modified: Tue, 14 May 2024 00:46:09 GMT  
		Size: 52.9 MB (52912074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430c3e309fc08b47a5a9c4055cf762826fe348bf04d5712d2e45c83f3d78cf5d`  
		Last Modified: Tue, 14 May 2024 00:46:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:4ccd1a2f83a768225f630a2eddaf3253ce43b18429cda9c18c406ca844770fd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53536835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5e4469d10ea0e14586ba996a031b0e10b078b0581e00375fc685dfbb137906`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:49:30 GMT
ADD file:6faa0308dec78b7bf27c8098473df2d1d3bf3fdf83099a1a13f777a963b69ba1 in / 
# Tue, 14 May 2024 00:49:31 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:49:35 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e05023f22044acc27df160b1a20bd50e4de5074e0a396d66d1428472a62b2746`  
		Last Modified: Tue, 14 May 2024 00:56:15 GMT  
		Size: 53.5 MB (53536612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7405aed4d1601ffdb0b5f77fc11cf6400ab60cdf2600fef82a83226caf3b8f40`  
		Last Modified: Tue, 14 May 2024 00:56:24 GMT  
		Size: 223.0 B  
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
$ docker pull debian@sha256:0e8e40ffc0a1dbfd0371a5cc5722eedb7d855ed7b95b35fa52a961b82e2f2bd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52291273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8a0af26846b46fce9ea347bfc320edaab17e1865a5d4d145cac00c2808522f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:44:50 GMT
ADD file:4648ccf21b5ed0ffb91f4df711a7a846c609705bfcc60f590fcd41b3c5fab226 in / 
# Tue, 14 May 2024 00:44:53 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:45:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b6988741f7ba3983b538f656a90da504a35a297351fdda81be0d7cec90e792d9`  
		Last Modified: Tue, 14 May 2024 00:49:38 GMT  
		Size: 52.3 MB (52291052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6fe5e08df169627e7e714292ab53447725ef198e98336a77c55674489c233a`  
		Last Modified: Tue, 14 May 2024 00:49:44 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

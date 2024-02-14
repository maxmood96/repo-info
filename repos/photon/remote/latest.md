## `photon:latest`

```console
$ docker pull photon@sha256:b392becf195f6edd12ebc51529018f406e0d039d64660b496b95a1eb026b83e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:4e8442697c9f98751a3d3dc053bd9bd87477260cef43c4ad251a4965f6f9092c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15942320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa23d21c4ad2b1167983b261fb4bef50a76b233a8e7e1418b2afe421765503d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 Feb 2024 01:50:38 GMT
ADD file:ee5adc42013f044650b78886d6a968bb5c9141a1cdd5b714f3e8ef3da1e3c76e in / 
# Wed, 14 Feb 2024 01:50:38 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20240213
# Wed, 14 Feb 2024 01:50:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:94dce31f034e790a27c0c596c7a3b2096228cc5603a950fe9bd3c1af8e1b6d26`  
		Last Modified: Wed, 14 Feb 2024 01:50:56 GMT  
		Size: 15.9 MB (15942320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:d94ba2048ac9663ee1c50ef96f95ed9d6aaff2264da5f0b4430e46292e73f0fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14939915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97970ddd752d6b3ae231a0a160a6c8203ae911e78c09ae614cc627736b76148d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:37 GMT
ADD file:2c09ab1910ab37a9470e393aaed2c766e48856114c19c67f8a32e95e6d4392ab in / 
# Wed, 14 Feb 2024 01:47:38 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20240213
# Wed, 14 Feb 2024 01:47:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2416e094f64ad56dfc356e196900f7bc56b0fe7840256f44a70b0a6f85497986`  
		Last Modified: Wed, 14 Feb 2024 01:47:52 GMT  
		Size: 14.9 MB (14939915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

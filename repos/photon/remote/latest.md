## `photon:latest`

```console
$ docker pull photon@sha256:f48f1cd0c54ca4bfd90e0ae7a8faa53df39be7f645b898f275e086002a52783a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:7f1c37f67082c9096d9de15fe45b374595b489bb1094a2ee4dc9eeb1dcbf7b90
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15937045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a9dd77beebdb8f960d4330a8de1104a998efabab62a2c8a43f93704e34c4f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 04 Sep 2021 15:12:13 GMT
ADD file:0254b55163f05c288fbdbc8e68fd26ebeee8a11c3c67200d4d48b770d360da00 in / 
# Sat, 04 Sep 2021 15:12:13 GMT
LABEL name=Photon OS x86_64/4.0 Base Image vendor=VMware build-date=20210903
# Sat, 04 Sep 2021 15:12:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4f75ef0afbf51bc5aa8fa9d7ef0eebac925ca96179c903f265d4d81f42b472bb`  
		Last Modified: Sat, 04 Sep 2021 15:13:04 GMT  
		Size: 15.9 MB (15937045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:81fc9a4408f0763269f195e13bb73a89e174755609cb8dde7b914fcf1572adfd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14979428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d579314b2538e14e745adcaf325ba62934e38c31e8ccb7917f3ae64ec238e7e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 04 Sep 2021 05:30:53 GMT
ADD file:d0e1eb08602195cddb25f231933bf1595e7822ecc9af271a45e490c0f64be8fb in / 
# Sat, 04 Sep 2021 05:30:53 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20210903
# Sat, 04 Sep 2021 05:30:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:917f1d8e71a898c84d18fee3ff4f26a5b13a1971a64840aea40290f1de6904b8`  
		Last Modified: Sat, 04 Sep 2021 05:31:21 GMT  
		Size: 15.0 MB (14979428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

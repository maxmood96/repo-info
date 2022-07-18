## `photon:latest`

```console
$ docker pull photon@sha256:1db94cc46388d9f75fc7739ede4c19731cd623c24a10130cc3b0ddc25ac3d444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:ad5aaae2af99be9f1306b5db763084b9252e432918161a61beae27f861a0c1c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15995375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a39265e67feab103a90ec0c1a291a42b9b9684769353c05654df4ece88d3f68`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 18 Jul 2022 19:47:04 GMT
ADD file:cf990e54a2388b5ea0efc7e06e02394c7f726d42e4f5cb68d5ac0a3cbc59e45f in / 
# Mon, 18 Jul 2022 19:47:04 GMT
LABEL name=Photon OS x86_64/4.0 Base Image vendor=VMware build-date=20220715
# Mon, 18 Jul 2022 19:47:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:82e98bb7840e5cd2652cfa6609944e0c9784ac5970e3d80d50977885f5413714`  
		Last Modified: Mon, 18 Jul 2022 19:47:41 GMT  
		Size: 16.0 MB (15995375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:e3f924673b983cd9918f233ee0f3e6884964035e1246544df3e610706ee56718
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15067299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b426c5b7baa7a04be41ae773d2850a43ceb1e3e7697fe6e54976cd87b708d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 18 Jul 2022 18:55:12 GMT
ADD file:f74c93edafb288746ae31fce9ecad94509f8bbf06794cc529cddda11774ff3bd in / 
# Mon, 18 Jul 2022 18:55:12 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20220715
# Mon, 18 Jul 2022 18:55:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a1c0818e6ff03599c51552f5b5a9be7d141d815735a0a4f785f777fbd31a7073`  
		Last Modified: Mon, 18 Jul 2022 18:55:43 GMT  
		Size: 15.1 MB (15067299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

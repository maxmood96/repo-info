## `archlinux:base`

```console
$ docker pull archlinux@sha256:7ceb7563e81e5c67b30cadace8d7f1b5734b2260ef2c5ece00783bb66b540434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:b1d3e02f5c63bd4642003823f3c19925de39b8fc40934a842a04134a5068ed2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132576440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762c53a7e486d503351cd1d60099f8c2f0c34020e562e687114bf05ea7c79901`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 02 May 2022 18:20:00 GMT
COPY dir:010379bdb2bb294b64b6d6a2d639303c11c66e14e5d1c86e615dadf249518251 in / 
# Mon, 02 May 2022 18:20:02 GMT
RUN ldconfig
# Mon, 02 May 2022 18:20:02 GMT
ENV LANG=en_US.UTF-8
# Mon, 02 May 2022 18:20:02 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:24974d9ad28a636276c5ca11cac5463451bc74a8f35fb4b30552fe529d8f1929`  
		Last Modified: Mon, 02 May 2022 18:21:46 GMT  
		Size: 132.6 MB (132569331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c23eabe5bf70160ecbc993ad67ac865639f888f1d90e20d07cd931cb69181d2`  
		Last Modified: Mon, 02 May 2022 18:21:26 GMT  
		Size: 7.1 KB (7109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

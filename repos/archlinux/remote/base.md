## `archlinux:base`

```console
$ docker pull archlinux@sha256:3ac6d1abecb740c95fe990b0cc15cb6d261cb2b18ab2c541119778f5de71d08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:d55718619f76254b25ccd714f810c8685cac5395415a8f1bfa8994766f77aa30
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134781693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee4060b887664215a4b9d98e5acb89e400d4b167db9cbfc71a4d7406bb154b6`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 06 Dec 2021 19:20:02 GMT
COPY dir:5e3203639c31aa7378c83429783e99901d193103ef56fcdf31202c3be05735a5 in / 
# Mon, 06 Dec 2021 19:20:04 GMT
RUN ldconfig
# Mon, 06 Dec 2021 19:20:04 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Dec 2021 19:20:04 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6229dc59ea429357ae6ac177eb722751726938cc4d7534121668d6e3b902b51f`  
		Last Modified: Mon, 06 Dec 2021 19:21:51 GMT  
		Size: 134.8 MB (134774929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acd0343898385ea224cf3c5ea54da564e708f5388128bcb8bc19549163cc4c3`  
		Last Modified: Mon, 06 Dec 2021 19:21:30 GMT  
		Size: 6.8 KB (6764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:39dc9ee5698c3ed77bb439fba5b8ba33121b5aa8187d2b473c7dd1d644bdd8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:c6e53510368fd6ebb9295c6a11e12404d0d975d84476a349af898faf6ef8bb63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (88988810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175f839e5f2279cee77f0a29e0d668adc62860dbb0c517b6bbb690c6c941c0e0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 24 Apr 2023 19:23:22 GMT
ADD file:3c17da1cb3881285da2a59409e47c98d0b3862f241956a263100859f2133d9c8 in / 
# Mon, 24 Apr 2023 19:23:23 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 24 Apr 2023 19:23:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ae56675ade9f086fbb09dad7e3026bfb2d2defb564b4d3796b405be3d1fe729c`  
		Last Modified: Mon, 24 Apr 2023 19:23:43 GMT  
		Size: 89.0 MB (88988593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f28d5a7eff8720cd85ae1feef689d1df9ef4087a9bb44828bab367d7c7dad5`  
		Last Modified: Mon, 24 Apr 2023 19:23:32 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

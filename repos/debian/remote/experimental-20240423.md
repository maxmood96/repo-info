## `debian:experimental-20240423`

```console
$ docker pull debian@sha256:2266e6e454ebfbbc05d8b45b0bd01a48997d6c1badcaaa2461a979f954fb5c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; riscv64

### `debian:experimental-20240423` - linux; riscv64

```console
$ docker pull debian@sha256:e45dd5de4890a0ad3a4b9a414b322ff663d137f229ef8793bb8d8d2715d1e015
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50665633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a40fc9c6c0ac1d95b8bccfaa6cce21595290f4646d072982e50d5286c41588`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:10:43 GMT
ADD file:a95faf1f554ae0b300491cecf4c6673ac4513e69d5a04e655b5889bd1c72bd65 in / 
# Wed, 24 Apr 2024 03:10:45 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:11:21 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:aa8b4e50fe262518d117b4f920dcd7ede0214f4a5910bd41e86ba9e6b178aef4`  
		Last Modified: Wed, 24 Apr 2024 03:13:45 GMT  
		Size: 50.7 MB (50665410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704c7c754175ddd831b2168dbb146fde3bf7413c2d95fd24473ebd85a0989740`  
		Last Modified: Wed, 24 Apr 2024 03:14:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base`

```console
$ docker pull archlinux@sha256:275fb964508b7a2812f43a4dfa2cfa27cb06a4a453d72675270e2222b43f2a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:076c0233d1996165721320957be9a037a760574d6334281354b07b3b3c9440b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145779572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4866169dc4e4f2e7b4df90fe25da927da7f3449631308ce7dcee386efb1aba`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 19:19:49 GMT
COPY dir:2a2cee4496b10b29beccf62c1cbddb51c8d75fcda0dde03222162678028be8ee in / 
# Mon, 22 May 2023 19:19:51 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 22 May 2023 19:19:51 GMT
ENV LANG=C.UTF-8
# Mon, 22 May 2023 19:19:51 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:352736306209cb0acfcf56d39f9711d6086388ce7720593490fa00a241130f2d`  
		Last Modified: Mon, 22 May 2023 19:21:31 GMT  
		Size: 145.8 MB (145771544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e04a7b46863cc79a97a92473912a8e039644f962e50fb8a581c5a06b7bf3ff`  
		Last Modified: Mon, 22 May 2023 19:21:12 GMT  
		Size: 8.0 KB (8028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

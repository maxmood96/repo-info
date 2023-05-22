## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:3ff3ea426aae58c222197972999bfec55871937af57b8d5a083d94906fe8afaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:34e5eff85e35956f4832344161c7e28d3d65a564573623d064d0af8591ed7367
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252800803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed89e4f5fecb96251e46a0e28625fdd4df3e1724242b1027690e9c66d802efc`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 19:20:50 GMT
COPY dir:d02c9573519a7585fb8e77c3d63575e1e947893a113d9ecafc9356fdd2a9518a in / 
# Mon, 22 May 2023 19:20:54 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 22 May 2023 19:20:54 GMT
ENV LANG=C.UTF-8
# Mon, 22 May 2023 19:20:54 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cd4fcb5c4c907b09a037c9f567f24093ebce70585c8cc84b64b16f70a12b8c32`  
		Last Modified: Mon, 22 May 2023 19:22:15 GMT  
		Size: 252.8 MB (252792096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224c0c490b5f8acb56d7c9ea7f259214e77af8d3edd6c4fb1e1db8fe0a35808b`  
		Last Modified: Mon, 22 May 2023 19:21:42 GMT  
		Size: 8.7 KB (8707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

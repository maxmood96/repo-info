## `archlinux:base-devel-20221120.0.103865`

```console
$ docker pull archlinux@sha256:edc85ab8aca021f10e4c1cde0c7e8fee1cf5ba06f1c35e95548951734fa9e8f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20221120.0.103865` - linux; amd64

```console
$ docker pull archlinux@sha256:d8b519a56143e1effcc578ec70f4aa8fffd299f8ed3b30ec9c44854d1c0fb72e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243038466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8081dcb4ed80b08ba4840fd8a01d8aa5474b80907bec01120bb40dff751796d8`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 21 Nov 2022 19:22:41 GMT
COPY dir:98fb3009f9c7f9a83ff303ebfdc4cf40b4ebafdbea31741327bd4b8fbf93629c in / 
# Mon, 21 Nov 2022 19:22:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 21 Nov 2022 19:22:44 GMT
ENV LANG=C.UTF-8
# Mon, 21 Nov 2022 19:22:45 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2949cabf88761e050f296e873f3dc3220b14f3119ab2de5578ce220e93b3d0ff`  
		Last Modified: Mon, 21 Nov 2022 19:24:10 GMT  
		Size: 243.0 MB (243029833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a4d6c177105fc09d8a72f786c0bbbdcbdb2a0ba4debc2733246dc6beb6ea8f`  
		Last Modified: Mon, 21 Nov 2022 19:23:37 GMT  
		Size: 8.6 KB (8633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

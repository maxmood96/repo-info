## `archlinux:base-devel-20221030.0.98412`

```console
$ docker pull archlinux@sha256:8e91ae3cdf71607b3fb3bf68987ea02c36689e8c7a9c6c5c775bf4c9cafa0d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20221030.0.98412` - linux; amd64

```console
$ docker pull archlinux@sha256:0d5c4d8c67ff0d0e6fc1300622f0ade7d2d64737a15f3d7a1868257872a0485e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238895820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ad726a254e4b793c77093f7a2e6361d6a74f4dba3022a1db15914835e9bf78`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 31 Oct 2022 19:22:18 GMT
COPY dir:a025c87a1f4f0e296ce35569b702641010c23b46dd748a108a7b067629f0c3c6 in / 
# Mon, 31 Oct 2022 19:22:21 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 31 Oct 2022 19:22:21 GMT
ENV LANG=C.UTF-8
# Mon, 31 Oct 2022 19:22:21 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:37e5c2addda4602ab7cd53c40ebe6fae9e0da05020d21e2560ce3f5ffbe13612`  
		Last Modified: Mon, 31 Oct 2022 19:23:49 GMT  
		Size: 238.9 MB (238887201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28dbae0cf3b9eabc35e3c1aa80bd21cd5d91715125fda9018d14bf80c81320a`  
		Last Modified: Mon, 31 Oct 2022 19:23:14 GMT  
		Size: 8.6 KB (8619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

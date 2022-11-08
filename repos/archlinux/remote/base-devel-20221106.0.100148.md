## `archlinux:base-devel-20221106.0.100148`

```console
$ docker pull archlinux@sha256:22c370e3730dac7979934ef484f9453b19ed878198465b63ff18be9641cd5cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20221106.0.100148` - linux; amd64

```console
$ docker pull archlinux@sha256:d2ae7915a7bc5453b9b14bff4f51b881dd49b50e6c9952c1977b62b742408294
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239808788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524aa6d819014515df265f10f955fbf9bd8d69c7a779bc7c66ab99bb1b673821`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 07 Nov 2022 19:21:45 GMT
COPY dir:847933db4a93cfe4812d7a39f3f9e446cb404f19685fbf1d2e0f5a7b3cdb4ec6 in / 
# Mon, 07 Nov 2022 19:21:48 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 07 Nov 2022 19:21:49 GMT
ENV LANG=C.UTF-8
# Mon, 07 Nov 2022 19:21:49 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b8752a179dbea981eeb7f8e1714b5e02943f6f8e8d7b5ea8f13fd01cc6ba01e3`  
		Last Modified: Mon, 07 Nov 2022 19:23:20 GMT  
		Size: 239.8 MB (239800159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3cfd835c9e9525552ae2796f29f60ce7f25662f7ab0fcf5d5adbbb01460f6b`  
		Last Modified: Mon, 07 Nov 2022 19:22:44 GMT  
		Size: 8.6 KB (8629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

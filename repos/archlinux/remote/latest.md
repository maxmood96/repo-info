## `archlinux:latest`

```console
$ docker pull archlinux@sha256:5679ee886aa411a371147a95667fa74c26819197f6d52c673201100c134e0b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:c40bbb2c68ce6128f762d0cce87c80fcd5be40048c1df0cc5cf4c662300766ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127390377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317e584e3c26ecf862bb8b5662db75d5564bb041a55e08fe60621c11686b3dd6`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 18 Jul 2022 18:24:20 GMT
COPY dir:11b761f1b802cdfda693c5153e66230180b5c81784ddc972fc678a956a5364ef in / 
# Mon, 18 Jul 2022 18:24:22 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 18 Jul 2022 18:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 18:24:22 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8ed695e65781f424db075f6696f419bbdf8c64e86806b03b41880aa42355bf8d`  
		Last Modified: Mon, 18 Jul 2022 18:26:03 GMT  
		Size: 127.4 MB (127382826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ecfa4e94531ad7b63b2c1cb26b9658b1e8421ca818e3089e979504eeb9a4de`  
		Last Modified: Mon, 18 Jul 2022 18:25:43 GMT  
		Size: 7.6 KB (7551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

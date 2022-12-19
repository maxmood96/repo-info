## `archlinux:base-devel-20221218.0.111778`

```console
$ docker pull archlinux@sha256:6e9462165318980bb51b4fef364c4d093f096b714086a9c3c50004bcb07478e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20221218.0.111778` - linux; amd64

```console
$ docker pull archlinux@sha256:48f5fbb8f8a2aa859afc7f4f9d7c3fab5ad4306106473b2d480ed056eaaea0d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243180174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95eb6d8ea438c5d4245230a40975a56c49bd52def7bc93c5d912f208b6007e3f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 19 Dec 2022 21:21:11 GMT
COPY dir:5b88c748f8c8d162f66e651b5a610067d92b6d26ec6b5f56f5a807a1dd9b1ca3 in / 
# Mon, 19 Dec 2022 21:21:14 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 19 Dec 2022 21:21:14 GMT
ENV LANG=C.UTF-8
# Mon, 19 Dec 2022 21:21:14 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7bd6cc0cd5459e1f45c2d713eb253d449e241de39c5822f89fca9202005e52a2`  
		Last Modified: Mon, 19 Dec 2022 21:22:43 GMT  
		Size: 243.2 MB (243171533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddfcd1a35926a13703d7a367e31e14a5dcf9d61406ea492748f2d974c22994b`  
		Last Modified: Mon, 19 Dec 2022 21:22:08 GMT  
		Size: 8.6 KB (8641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

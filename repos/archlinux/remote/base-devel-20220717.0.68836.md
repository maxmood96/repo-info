## `archlinux:base-devel-20220717.0.68836`

```console
$ docker pull archlinux@sha256:595be001ae6ce5e4ed1e83056cf007bde6193835062bd8cb2d78113b8091298b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20220717.0.68836` - linux; amd64

```console
$ docker pull archlinux@sha256:bd9fd97df8c6ea0048df745bdbdc3a67a23c1ced5cbc5833ee0bfeb383d71b82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223784491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872725140a4ba0f73d785675b6d62648416479a74adb7739f9a1822f17885e22`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 18 Jul 2022 18:25:21 GMT
COPY dir:3a91d5869d166e8400cda2be2e1fb4b4f4a6e1e1d896aa69b037306a4a7e1a26 in / 
# Mon, 18 Jul 2022 18:25:24 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 18 Jul 2022 18:25:24 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 18:25:24 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d5fbd488eb038da4cbb8c29dc282f92ce3145dbf078f408d9ee596195e08345a`  
		Last Modified: Mon, 18 Jul 2022 18:26:51 GMT  
		Size: 223.8 MB (223776321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a894abae66fa66e2041bf2eeb5242b381ab0602c969b218b4fbb8e4c109acedb`  
		Last Modified: Mon, 18 Jul 2022 18:26:15 GMT  
		Size: 8.2 KB (8170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

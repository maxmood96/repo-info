## `archlinux:base-devel-20230423.0.144989`

```console
$ docker pull archlinux@sha256:95c40214ce1571caa314f1c93edc15c2713793e9d07505d091d7eafc3f9f9118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20230423.0.144989` - linux; amd64

```console
$ docker pull archlinux@sha256:4f673dd1fcb0af245d2bf7c20bdd1b5bd55c2af3d7ac8debeb3f13ef76c14b19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246155374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c23c945367b182e392cf5fa3ad19d324b08c9d32395d4466d9b13a225b451e0`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 24 Apr 2023 19:21:19 GMT
COPY dir:30fccad4db02a015dc3df87dee72c3888f4204c039a92c8a0fcb1fa6db65e609 in / 
# Mon, 24 Apr 2023 19:21:22 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 24 Apr 2023 19:21:22 GMT
ENV LANG=C.UTF-8
# Mon, 24 Apr 2023 19:21:22 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:0d8eac793e0eb6945ddd359a1ccc66f9ab275c17fb398b5b36cb48151d73ffc5`  
		Last Modified: Mon, 24 Apr 2023 19:22:45 GMT  
		Size: 246.1 MB (246146666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f0e5644a5f513d342d9575c950b326f55e81119988d388bd703082ce2a2af2`  
		Last Modified: Mon, 24 Apr 2023 19:22:11 GMT  
		Size: 8.7 KB (8708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

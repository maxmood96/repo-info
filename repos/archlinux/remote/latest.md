## `archlinux:latest`

```console
$ docker pull archlinux@sha256:27f132b602ba42dd597637d716b59f1cc2b31cf3af69325201a2168a288501d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:b0e145cbe10ce4c7ad6a1373b8fcc1ce97b02f8fb9d5450b6796617d01b6e18c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141993959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067b0bfd114e531542878e636b1bbbd3eec28621bc6737be90a287f4a22849f6`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 13 Feb 2023 20:20:38 GMT
COPY dir:f5b23aef4d1612d34ba6b7dc4110aa200b24a6c91c560e209e4ea099f514c2c6 in / 
# Mon, 13 Feb 2023 20:20:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 13 Feb 2023 20:20:40 GMT
ENV LANG=C.UTF-8
# Mon, 13 Feb 2023 20:20:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:31236c5f9bf47a34b3d104d8a890cc7fff5bf3cd7e287f2341e6e395482d85da`  
		Last Modified: Mon, 13 Feb 2023 20:22:23 GMT  
		Size: 142.0 MB (141985993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7551fe27d5768b830b411e614a23f491afb0249369c4163f5211df3133e971aa`  
		Last Modified: Mon, 13 Feb 2023 20:22:03 GMT  
		Size: 8.0 KB (7966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

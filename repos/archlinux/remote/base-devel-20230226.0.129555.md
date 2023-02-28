## `archlinux:base-devel-20230226.0.129555`

```console
$ docker pull archlinux@sha256:75530fea67eba5a9a357a227260dc8b2a39e9c9264815590278f5d51be6a7e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20230226.0.129555` - linux; amd64

```console
$ docker pull archlinux@sha256:85788a9187ae6bcc4ae51f1eb3d438321dc256d98c645cacbf93f9fa0bf91685
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 MB (245222341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8210c3dd9b953ed5fa71ffdb39d9eb0c58659da4f0d7c79594831501465ed9b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 27 Feb 2023 19:21:21 GMT
COPY dir:0d662118041bc1c4891705615ccda7e087b2d72beb0596608e1374c166081cfe in / 
# Mon, 27 Feb 2023 19:21:24 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 27 Feb 2023 19:21:24 GMT
ENV LANG=C.UTF-8
# Mon, 27 Feb 2023 19:21:24 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:83eeb10c39a706e13080778568173f963d7ae098691529d4de6ff36d29f76fd3`  
		Last Modified: Mon, 27 Feb 2023 19:22:50 GMT  
		Size: 245.2 MB (245213630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11ef0e339bfca4900615d9b09d685aa562f61b6dfa15d4f986daf8c52140556`  
		Last Modified: Mon, 27 Feb 2023 19:22:17 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

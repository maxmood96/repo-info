## `archlinux:base`

```console
$ docker pull archlinux@sha256:bfea13060936b76221aae038ff35e1f1744632096ad4686ea34fce31ee758ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:f8e36cb82b199dab15997891e74c4b50a47192d3ff8e7b06067d262276a3f8e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134358355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d003eb9263d822d5f09d16e7eb72d0264ca37f2fa825bf59fc3e863e0e55149d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 05 Oct 2021 17:28:45 GMT
COPY dir:e9c64e576cb0250f4bd7fab12c4602b507f8c0a7bcad61d705234206ba6e807b in / 
# Tue, 05 Oct 2021 17:28:47 GMT
RUN ldconfig
# Tue, 05 Oct 2021 17:28:47 GMT
ENV LANG=en_US.UTF-8
# Tue, 05 Oct 2021 17:28:47 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ad213cdd3e6037a8810012f3e0a50045b4f4eb9101bef417bb29589379ff08be`  
		Last Modified: Tue, 05 Oct 2021 17:30:36 GMT  
		Size: 134.4 MB (134351592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f61155419df7ae00afa0e01f8bf7928b51e91bccd8922440ab22896c699d30`  
		Last Modified: Tue, 05 Oct 2021 17:30:15 GMT  
		Size: 6.8 KB (6763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base`

```console
$ docker pull archlinux@sha256:4fd4f24aca01dc4ed1bd472b62a90dd93ff08102eb2c20a938b7383ab39baa0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:9167ec489f207c80e953375d3c5554c4846ef6cfe3869a536e710e2be6b405de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141900901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85818b4587a6ca0e318afb34128413ffcf0e357b3eccec38da07d7387df2e92f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Jan 2023 17:16:13 GMT
COPY dir:1f1f4c75a214a83f54b051bed4277bf05e6e77f94e4d15ab5141354f8551e948 in / 
# Mon, 09 Jan 2023 17:16:15 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 09 Jan 2023 17:16:15 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jan 2023 17:16:15 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e7df3e3edb8d7af5bc407f49d0006ae41775c2c769b06522aeeb27d7347c300d`  
		Last Modified: Mon, 09 Jan 2023 17:18:03 GMT  
		Size: 141.9 MB (141892940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4edb241ab322c11c79375b887fba1407f1baa652f9537000c2c18231a9bde4`  
		Last Modified: Mon, 09 Jan 2023 17:17:42 GMT  
		Size: 8.0 KB (7961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

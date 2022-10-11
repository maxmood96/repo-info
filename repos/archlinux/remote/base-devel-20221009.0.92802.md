## `archlinux:base-devel-20221009.0.92802`

```console
$ docker pull archlinux@sha256:ee3f9caa2cf0e486fcd9d9e2ab5c320dd3c18c5ff6f3e991d0b1c9cd10905031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20221009.0.92802` - linux; amd64

```console
$ docker pull archlinux@sha256:55d9290e712a82a33aa224bffe050b35f59cff3fdff3f294e23ed4665cbfd09c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.1 MB (238094222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ebaeefa4e260614f3fd2778ede945030b924de5266f45b4abdbea1db106806`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 17:23:03 GMT
COPY dir:422925168f99906522086eaa7837020f9195938fa7b42b159778baf1fa1fa064 in / 
# Tue, 11 Oct 2022 17:23:07 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Tue, 11 Oct 2022 17:23:07 GMT
ENV LANG=C.UTF-8
# Tue, 11 Oct 2022 17:23:07 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:894d2f6cfd58b797b0d48826332dc1c2e31d9070df6a15e33d5b8d99996ef00a`  
		Last Modified: Tue, 11 Oct 2022 17:24:33 GMT  
		Size: 238.1 MB (238085658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fa33182d19415d28de41f8d580c51217021cbf4d94fb737196a88e665b53cc`  
		Last Modified: Tue, 11 Oct 2022 17:23:58 GMT  
		Size: 8.6 KB (8564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

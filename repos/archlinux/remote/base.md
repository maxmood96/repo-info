## `archlinux:base`

```console
$ docker pull archlinux@sha256:cf2d6abbc42d2799621f23d54ea7211a1d754d3a0bbe0fb8128e8fce14466640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:0a8d47564756247c8157e725d9cd6fe3443af221c45c436f202269f2c1e1ebc6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127238572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cda16b1dfdbbc2860d7197a979f73c5e5d170c3d539455e7101973962fc67db`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 27 Jun 2022 17:19:57 GMT
COPY dir:95121058d363bcfc16fc95b536238522b88503cc05034576a546b09aa026bcef in / 
# Mon, 27 Jun 2022 17:19:59 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 27 Jun 2022 17:19:59 GMT
ENV LANG=C.UTF-8
# Mon, 27 Jun 2022 17:19:59 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:5583f0cd8281ed022497500faa2f19022df8ed576aa2fc0aa16c057887966856`  
		Last Modified: Mon, 27 Jun 2022 17:21:32 GMT  
		Size: 127.2 MB (127231005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bab413c2806f6e3fb944fe1f746abae1bdc073ad68ab4e9df4486b46b8f5ce`  
		Last Modified: Mon, 27 Jun 2022 17:21:13 GMT  
		Size: 7.6 KB (7567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

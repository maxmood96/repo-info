## `archlinux:base`

```console
$ docker pull archlinux@sha256:8b7477e7092dd2be68cb289a40f733f6c9e60ed0a886b8dcdbd36bad733eff6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:b017e59a270792be7d1dd659acd122c9eee04a881b1676ee91ac6eecdee66f7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145330216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510e0fdeb1f4d5772de5d496def012a7bc129c899637fdaf8ce14173f24d39ba`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 08 May 2023 19:20:14 GMT
COPY dir:1a2a494407923dffdd93dc41d51c38884bb1c797b68a1e567bcec5d093eee981 in / 
# Mon, 08 May 2023 19:20:16 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 08 May 2023 19:20:16 GMT
ENV LANG=C.UTF-8
# Mon, 08 May 2023 19:20:16 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:aec56a96bd8d99d56be44519d02077109cdda66f47d506e2268631295677aa74`  
		Last Modified: Mon, 08 May 2023 19:21:49 GMT  
		Size: 145.3 MB (145322284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b90a012a4ca5415fb6da2dcfbb8e2563358be0cabf02e79a62f5ca196ff3c47`  
		Last Modified: Mon, 08 May 2023 19:21:30 GMT  
		Size: 7.9 KB (7932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

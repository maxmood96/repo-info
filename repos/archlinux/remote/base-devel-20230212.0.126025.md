## `archlinux:base-devel-20230212.0.126025`

```console
$ docker pull archlinux@sha256:9dd936a5a5358fa2e3515e1daabe4c0e6b4c1e9fcf369528d229955590c93472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20230212.0.126025` - linux; amd64

```console
$ docker pull archlinux@sha256:281b8d7a7fb081e97ff77ce51a20fdce6b9e3d4e0dd0eb64f9709e37a5ebacad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245053097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96e8d772c84de9eb63dc7e8a6abb7bb9e667ddd46463a7a0ea661c4cf9ef392`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 13 Feb 2023 20:21:39 GMT
COPY dir:0c01d60dfc09a8bffe3ec055f8f68dcbf61b0711f9cd6afe8d79daf5f83dc738 in / 
# Mon, 13 Feb 2023 20:21:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 13 Feb 2023 20:21:42 GMT
ENV LANG=C.UTF-8
# Mon, 13 Feb 2023 20:21:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:04dc004165810067cd038f8b6066e0efd55154b29e57d6154b28a0889a4a5b23`  
		Last Modified: Mon, 13 Feb 2023 20:23:10 GMT  
		Size: 245.0 MB (245044377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f353a4755ef87c4a30a4aa03216a34e16e9cb8cafdee1bd9206ab31e7f0c72fa`  
		Last Modified: Mon, 13 Feb 2023 20:22:34 GMT  
		Size: 8.7 KB (8720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:237b422a483e2c655249dc58ac03975e4df0e05525edda4e7a8e2b577003fd9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:69c51ee01d773061ad96978231edaec097475ac900516272557290a93ff3d7dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.7 MB (223711228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f9c5ee9af2612240b9063083a9e4e4d14d1588fe43613b609b25b1b43a9d44`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 11 Jul 2022 22:20:55 GMT
COPY dir:0ee90ae7aed6f9006861e259dbc288ea7ed10ccbde527a8e925fe29df6e1c030 in / 
# Mon, 11 Jul 2022 22:20:58 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 11 Jul 2022 22:20:58 GMT
ENV LANG=C.UTF-8
# Mon, 11 Jul 2022 22:20:58 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b8df6b19916f34e335fbd9550123d1a4ad91942d28dc629c07fe37beb4f906ef`  
		Last Modified: Mon, 11 Jul 2022 22:22:16 GMT  
		Size: 223.7 MB (223703084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7665b2f2f4f669917d5a26d25f50ed8f69da7d54f73b8214256595921b3af6`  
		Last Modified: Mon, 11 Jul 2022 22:21:42 GMT  
		Size: 8.1 KB (8144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

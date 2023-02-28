## `archlinux:latest`

```console
$ docker pull archlinux@sha256:05ed3673a60ad4c7c61d185bde40d0f99e27ad204d1c6edba6ae3baba130f8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:3748e881908d6f0badcbc986301a787055ef38ae55970b061ac6a554b2bd68df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142217120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee0316a37dbfeb3fd23528b9f16b110b5073b94eaae11f8b55e3cd7dc24d132`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 27 Feb 2023 19:20:21 GMT
COPY dir:65137edd80e791dce1f20e275f5b8b295f10bb0175de344bed69dcb18828bb85 in / 
# Mon, 27 Feb 2023 19:20:23 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 27 Feb 2023 19:20:23 GMT
ENV LANG=C.UTF-8
# Mon, 27 Feb 2023 19:20:23 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:5096e92a2103167a9efca205e45e3bd390235ab98ef9ce69d1084c353b216b5c`  
		Last Modified: Mon, 27 Feb 2023 19:22:05 GMT  
		Size: 142.2 MB (142209158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4689879585b8128bc583fc1f0c9c8af8db059b8510193c2132483529a563da8`  
		Last Modified: Mon, 27 Feb 2023 19:21:46 GMT  
		Size: 8.0 KB (7962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

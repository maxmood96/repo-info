## `archlinux:base`

```console
$ docker pull archlinux@sha256:d64fb9a168150b8d84f917ac4caef125b1fcca7b4159b3eb9cc7495e98bfe074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:39abc75080eb33687194f20ffa25afd200811ccd1d2eef805e101ff70e506c7e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134048379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a6125f42cb406637a82717080c2b5794c5a7b9aded83d5ef18a47540ada54b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 18 Apr 2022 18:19:58 GMT
COPY dir:8ae07b76ccd5b0352706f0485f152b4960626d735d292b35204587a9b166a4bd in / 
# Mon, 18 Apr 2022 18:20:00 GMT
RUN ldconfig
# Mon, 18 Apr 2022 18:20:00 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Apr 2022 18:20:00 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6ec64a80b16c44140d053d8469b4ba2e5f1d24ec028e06f7102f8c9cf616f8a4`  
		Last Modified: Mon, 18 Apr 2022 18:21:36 GMT  
		Size: 134.0 MB (134041263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1750758d1f2f443b1af40eb1d5d40d2bb84aa3387f20bd5c45e602f78a4e29f`  
		Last Modified: Mon, 18 Apr 2022 18:21:16 GMT  
		Size: 7.1 KB (7116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

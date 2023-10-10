## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:df6b011919eec36f5c29d7722a8983492fac6deca0cac196b6a71e0492fe1f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:759a7e737c80784cbfc98af8c30aec79be3245c0fa515be3addaa436c78b7ec7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67832882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975c87e42e80467783410ee9c303eb7e166c9f6e449bef5ae2ab8be110006284`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 10 Oct 2023 00:19:55 GMT
ADD file:e2037c043a03dceb80bff4e6aa7b020e5c0241bf3d7055650331d9f04c42b78f in / 
# Tue, 10 Oct 2023 00:19:56 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Tue, 10 Oct 2023 00:19:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0013c697d67a10896ef676ce278bb6ee416117d2c185f370ed6ddc53c2b89b32`  
		Last Modified: Tue, 10 Oct 2023 00:20:14 GMT  
		Size: 67.8 MB (67832665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb365d475eb0313564c082562033a14b0751506f2171771fb8718bf21ba62845`  
		Last Modified: Tue, 10 Oct 2023 00:20:05 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:45462b0b226afc6721aef55f50c6398d12b5af7f3b66bd298f0b93e4e3a595aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:9b2821c66abc256474821b813a6212ddfae1b3299d28ad794f299fb39c0676f3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69628858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c939e691eb531f28b9ba9ca36f7385df2905d21be019b2f1d12ae7f2566ee4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 08 Jul 2024 17:19:47 GMT
ADD file:d8352f32c23a8775c612dcd3717df2671c9ee3a319d509106b18f114c70ba7ba in / 
# Mon, 08 Jul 2024 17:19:49 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 08 Jul 2024 17:19:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:118b06771317600cd661e989cc8cc390afc5246038ee5cfc7b27203b511fa903`  
		Last Modified: Mon, 08 Jul 2024 17:20:06 GMT  
		Size: 69.6 MB (69628645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0659875dcb604e196f12b805c993b3c0de5625831317b2740805a2aea2c89e4`  
		Last Modified: Mon, 08 Jul 2024 17:19:57 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

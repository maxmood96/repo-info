## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:31fd4b44368f75bc0ab8d54e61616e6a4e985d354b0ed1c6b727bc0a106d2288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:4d32350d083981227cbbf3316d3ca334a6146bcfc4bf98f1bbf8375a7c88ae0f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71936534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ac1541ebf3718b6f0cc38b942d246701286e7540d3650f7b1f1dc3ef0b1d07`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 16 Sep 2024 18:19:48 GMT
ADD file:2ccb25f54e47d9ee1bb1564233bdc85da46b63d278bf633b2c6ffdbb30c41a23 in / 
# Mon, 16 Sep 2024 18:19:49 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 16 Sep 2024 18:19:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8f02d4bd3d9c4cc608afee7473da1d2cdde53e1155c6382febd66d2bb7a33bba`  
		Last Modified: Mon, 16 Sep 2024 18:20:05 GMT  
		Size: 71.9 MB (71936321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0309dd98a54ebb834ee4aef5d964238c31a6e9107c5ef246f5fb8bcbbaad3351`  
		Last Modified: Mon, 16 Sep 2024 18:19:56 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

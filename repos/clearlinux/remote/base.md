## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:a1cced7a2ca64fc2c9d3da72c5663430e6821168fd872fa96a9fdd964ffe3f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:f65d1bb8e9fe242235c801ff73e6ecd0a65c47ba9dba22c0a25922ba2847519a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72030133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1b51c10181f1f6192368203d9f8611bf3b5bbd81d60907029ae40bc4da2e85`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 19 Aug 2024 18:19:32 GMT
ADD file:cac14f885043b8f98531be3a2ee031649135060bb12898de6e245807f8ff7f40 in / 
# Mon, 19 Aug 2024 18:19:33 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 19 Aug 2024 18:19:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8be6c5db46967ca486d4949d65bd24b011f801c9ea34609b03189bfd57ca8a32`  
		Last Modified: Mon, 19 Aug 2024 18:19:51 GMT  
		Size: 72.0 MB (72029920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9a7c0ce416fa72495bbb05681fe67e973b1dd7bff000844fe6e0aef0bb66ac`  
		Last Modified: Mon, 19 Aug 2024 18:19:42 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

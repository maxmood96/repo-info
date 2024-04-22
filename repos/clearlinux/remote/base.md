## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:d051bb4c304b7868a852a114c3b10ff7fdd7552ee23ebdfcd31a42beaa2289c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:1c5e60f1788d539c634be111ada8450e51e15201ede6f32b161d7d0dd6bd0aaf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68939398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e20a754fcf065f4fb37630e77afb57e4ce27b1f21552e63266571339a8c0e9e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 22 Apr 2024 17:23:55 GMT
ADD file:b54766b33c57ecf0b9e4c2814085f30bc51a0107447f559a98500c88a7ea5bd6 in / 
# Mon, 22 Apr 2024 17:23:57 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 22 Apr 2024 17:23:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:18fa676a0ac5ae103bc321878b985b0a8fcb5a29271e1265f60044f1f6a30b5c`  
		Last Modified: Mon, 22 Apr 2024 17:24:14 GMT  
		Size: 68.9 MB (68939185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251124cc57403184ce79e47bd309eea86c8f103766e03b51ede494ca5cc74a4e`  
		Last Modified: Mon, 22 Apr 2024 17:24:05 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

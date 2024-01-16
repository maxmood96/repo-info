## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:b5f03873e3e926b49a8c6aa34993d5c5a7c0fd5ef0075014263a04fc75838cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:500aea560f03cfa04b5b096beba9be83cf2a27a6fec7cb1d4fce678ec334eb61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69306369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09991c5925a697d2b8a7e8658a500fc234b9a3645333ee54e0c620b7edb31de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 16 Jan 2024 18:31:14 GMT
ADD file:ee47d801f8a283129816ea60972ee6d01ae43cab02faed315a705b0475b4708f in / 
# Tue, 16 Jan 2024 18:31:15 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Tue, 16 Jan 2024 18:31:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b55ae4bd6a5138f336f061f57a4753e44424560c4f87b9f0dda6a97bf97dfcba`  
		Last Modified: Tue, 16 Jan 2024 18:31:35 GMT  
		Size: 69.3 MB (69306158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b856888eb3399188bd7d4fadcefa1a74c8a202b3bf45d4bcd6f0d03509e43be`  
		Last Modified: Tue, 16 Jan 2024 18:31:24 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

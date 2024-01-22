## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:3f54ce27c617675bd5767c839005ae1f15f0e92a5b278118665070ff2a237406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:0e977d7cbae334f5e04a1a8957e30e2a9cc7a9a90e8a806ce4a5a026f4e77461
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69351687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8636860a8a9883c2146add6c55a0691e5b36acc6923bf326a1723015bf950e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 22 Jan 2024 19:37:37 GMT
ADD file:24c9f6a2a7b4493615fef9bdef2933119d75f17a4b700fe847747087f1b65b62 in / 
# Mon, 22 Jan 2024 19:37:38 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 22 Jan 2024 19:37:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9f3ed75c4ba3a6455a8525c3dc485e214d02cc4a67ed267ee5b2750f90982262`  
		Last Modified: Mon, 22 Jan 2024 19:37:55 GMT  
		Size: 69.4 MB (69351474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf5a70f13930f0c51ad160e57e3ea6e9fe1dc43a6c312dd01655ec954f707d1`  
		Last Modified: Mon, 22 Jan 2024 19:37:47 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:bb6f4db604a645dd987ba0e473ca8078883861c772c19fa8bde7cf1e70ce1b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:d7645e8c854057a935ac71023d1445ee5f56d18125ebb133d3ba5320c86a20c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63788615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6744419730d9e00bd2e1c482f4f15006f50c8282d6c0be18c39b64cc45ee62`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 26 Feb 2024 18:51:41 GMT
ADD file:6293f30e8dd767042544c726526ad2e81d12eaf55e9fe44a88994552df8ecc2f in / 
# Mon, 26 Feb 2024 18:51:42 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 26 Feb 2024 18:51:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:07d772fa681aad151eb70c5a3392967c747cf1b1be898f7270b3faecf521ace7`  
		Last Modified: Mon, 26 Feb 2024 18:52:01 GMT  
		Size: 63.8 MB (63788403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a25d5ebd26abb6371b295f7e3234e4cf4c9f24adf94b383ce20f02c59260e46`  
		Last Modified: Mon, 26 Feb 2024 18:51:51 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

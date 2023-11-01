## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:661bd1fd11f58500f33e2f67478dd2e9fdcbacf4912243ece406a0f8166fffc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:6985e0c5a249ecefcc9976dd2555634d64ec43a481aebe9953b9176550d8a4f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67985666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393d572f209ec4c2e249c09c9fa76a3184c6953fccaa85a0740a8efeaa97e0ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Wed, 01 Nov 2023 00:31:39 GMT
ADD file:dbb1899d68e67c2d90a44fa00c8d0d60f7a67faa30a6eeeffe15e0dd11085d8e in / 
# Wed, 01 Nov 2023 00:31:40 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Wed, 01 Nov 2023 00:31:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:94a8612ca10eeede16c67151e513893f0c99df0d89762dfd6b1670bb0c50e102`  
		Last Modified: Wed, 01 Nov 2023 00:31:56 GMT  
		Size: 68.0 MB (67985445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680d2eb7df0f7aaa6fd1c2ae42fcd44553634e376570bf4fdb41696d6a6ce711`  
		Last Modified: Wed, 01 Nov 2023 00:31:47 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

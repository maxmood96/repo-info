## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:631a92559c3d443221c01de9279f62af3c170d9b793f7e5a64660053ddd41258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:191a9bb5cb19fa4f3d076091dc7e202447022b46fe58517008239576397f7ca8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95261159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b244821e8b341323d7d207b1a8fb195b70adb9146ef81d58020426da7e0aa65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 01 Aug 2022 21:23:16 GMT
ADD file:a8898e2b7adf6a3978624e91c6f5ddbe885fa48d6bc2ead0d7a6de030e072e29 in / 
# Mon, 01 Aug 2022 21:23:18 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 01 Aug 2022 21:23:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1faa8e0a052a0bfd92b1aad3c52264c5d5390df2c6df3d3b3fa23ec92039cd43`  
		Last Modified: Mon, 01 Aug 2022 21:23:39 GMT  
		Size: 95.3 MB (95260942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e4c3f9661fab8a2411106ec3d1339494e7ea8708b2d0d16fe680259da9bbda`  
		Last Modified: Mon, 01 Aug 2022 21:23:27 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:8fb3141f91b3467378e3a2510d01d7f2dcc2984e8b491cb1bb80c289e70b41d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:4cfadd9c3c038b8cb9dee21289d92bc19122c8d77f5e12b269678c2ae53711b9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71639046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24493bcb35b0c6f37811273fa9afabdd42c7105f960ba10f3444552eaf22b606`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 15 Jul 2024 20:19:33 GMT
ADD file:61ce41d5de0cbac010e699412803313527c5d9394c98745dcafa70b8e488ca9a in / 
# Mon, 15 Jul 2024 20:19:34 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 15 Jul 2024 20:19:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:35cbf358679bdecc34cfc9b8d4892b1a5bfb811ed0fb961efcc010a4c2b94743`  
		Last Modified: Mon, 15 Jul 2024 20:19:50 GMT  
		Size: 71.6 MB (71638832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d409d7a95948d235bb1214f4a0973a170bd7b9741d0f27469f2862c963232ae`  
		Last Modified: Mon, 15 Jul 2024 20:19:41 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

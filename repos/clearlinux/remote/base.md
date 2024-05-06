## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:4ab98a43a7e8d83923598e4e3a97e9c7440c3f6346903b8147514366750de2e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:c249665dc979bc2ce2afededebb4e308a1fc29a602c9c8b642f3c7e1c04b07b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69124026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39f85833a14f5aeb3f6c402cf2eeb4f68a45e44fd46d40590768376f3feed27`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 06 May 2024 18:37:26 GMT
ADD file:adaac1a0c3f6d40e978f0efbd94e70a6cd3ad25a2f0c057c72d46caf851dbf45 in / 
# Mon, 06 May 2024 18:37:27 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 06 May 2024 18:37:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6504d760d0d3574a505903a1e55983bbd081f6005076bcbea9304e48cc07a871`  
		Last Modified: Mon, 06 May 2024 18:37:44 GMT  
		Size: 69.1 MB (69123813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d34de1fac5c6d55b615be8a13b32117d4ae9661a23264608b177dc5deafcfe7`  
		Last Modified: Mon, 06 May 2024 18:37:35 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

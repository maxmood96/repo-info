## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:42aba270c71612089fbabe77228c0043846d1c706785cb2a03a40b1461ee357d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:28460730370dc35a2de3e767c7f32415d2f9ba4f9dad863f95f130ed56b3b2c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 MB (83663543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078b2b6ca376a8a0304c6404c0c45ebcfc3b8682c0aff4e9012b8e7ee86f8735`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 08 May 2023 19:23:25 GMT
ADD file:29ff5ea37e043961a8144adb34b0378c074880265b4c1ce11f7986d0f350a3a7 in / 
# Mon, 08 May 2023 19:23:26 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 08 May 2023 19:23:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e46da67d171a3a9b40155d3921f713212bc4997c251903179fc2a30b8bbc2da7`  
		Last Modified: Mon, 08 May 2023 19:23:44 GMT  
		Size: 83.7 MB (83663326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61629710100e85e2422be88213bab60c31649c1342b28a06e8fd0d06d607a609`  
		Last Modified: Mon, 08 May 2023 19:23:34 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

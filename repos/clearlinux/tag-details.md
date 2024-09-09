<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:941431b6f9bbda20c52610d87708d9b7c6c0faf41754e9004c874c7d876b41ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:322dd6e628fbb959041466f8e248f2accfd41729af38798800807b551bfce096
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71937349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc0cfcaa8ed8ae4e995ed24d74b1894cc40217b6d2b115ac4155a0bda9f83b5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 09 Sep 2024 19:19:31 GMT
ADD file:a157bbbdfb727e21c1b84b1cd560d02459cb13838d87f6f0eb44479c2c606ee8 in / 
# Mon, 09 Sep 2024 19:19:33 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 09 Sep 2024 19:19:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1d01e40be5a4354ec912aa2ca7504f026b3d32e40fc3e4ced5f2c69607f5e658`  
		Last Modified: Mon, 09 Sep 2024 19:19:49 GMT  
		Size: 71.9 MB (71937138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bb0600878ed3b71a139dec1f47e1e34cc5a324ad8cc1d5f2d5dda8cc21a8e4`  
		Last Modified: Mon, 09 Sep 2024 19:19:40 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:941431b6f9bbda20c52610d87708d9b7c6c0faf41754e9004c874c7d876b41ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:322dd6e628fbb959041466f8e248f2accfd41729af38798800807b551bfce096
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71937349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc0cfcaa8ed8ae4e995ed24d74b1894cc40217b6d2b115ac4155a0bda9f83b5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 09 Sep 2024 19:19:31 GMT
ADD file:a157bbbdfb727e21c1b84b1cd560d02459cb13838d87f6f0eb44479c2c606ee8 in / 
# Mon, 09 Sep 2024 19:19:33 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 09 Sep 2024 19:19:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1d01e40be5a4354ec912aa2ca7504f026b3d32e40fc3e4ced5f2c69607f5e658`  
		Last Modified: Mon, 09 Sep 2024 19:19:49 GMT  
		Size: 71.9 MB (71937138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bb0600878ed3b71a139dec1f47e1e34cc5a324ad8cc1d5f2d5dda8cc21a8e4`  
		Last Modified: Mon, 09 Sep 2024 19:19:40 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

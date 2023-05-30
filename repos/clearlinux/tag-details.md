<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:2a55c84400050d18cb8f6dad5700b11725e5a6315ab9268df6c4e1195f632068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:cba815e2236b6b9c88a0f3f25a7fa76508c4ade1048eda5a320f8ce32b7752f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72040736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1400a67ae1b619f888c37737c5533dd2cc22062256435235fdfaaa158e6b0e6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 30 May 2023 22:19:28 GMT
ADD file:34f83766d1b652e9c22c9b6c5885c2916462d988aea9a3d5c2d985f98c81bbef in / 
# Tue, 30 May 2023 22:19:28 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Tue, 30 May 2023 22:19:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f300a9983f432869653205d8c47ec01ff1bcc26a76d1cd7d9b9a5d597a435731`  
		Last Modified: Tue, 30 May 2023 22:19:45 GMT  
		Size: 72.0 MB (72040518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835748c3d487ab3693a134f7d00ca613ad24601b6c4850676a6c6bb07d26db2e`  
		Last Modified: Tue, 30 May 2023 22:19:36 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:2a55c84400050d18cb8f6dad5700b11725e5a6315ab9268df6c4e1195f632068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:cba815e2236b6b9c88a0f3f25a7fa76508c4ade1048eda5a320f8ce32b7752f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72040736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1400a67ae1b619f888c37737c5533dd2cc22062256435235fdfaaa158e6b0e6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 30 May 2023 22:19:28 GMT
ADD file:34f83766d1b652e9c22c9b6c5885c2916462d988aea9a3d5c2d985f98c81bbef in / 
# Tue, 30 May 2023 22:19:28 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Tue, 30 May 2023 22:19:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f300a9983f432869653205d8c47ec01ff1bcc26a76d1cd7d9b9a5d597a435731`  
		Last Modified: Tue, 30 May 2023 22:19:45 GMT  
		Size: 72.0 MB (72040518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835748c3d487ab3693a134f7d00ca613ad24601b6c4850676a6c6bb07d26db2e`  
		Last Modified: Tue, 30 May 2023 22:19:36 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

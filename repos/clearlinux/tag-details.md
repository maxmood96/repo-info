<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:c98e97d043ce59c1175220540a14f5f4265b41a712e73191804ad4e43b6b4a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:775289f0df29b7731b59d98ce70363f577e9e8bf8ef5faed7b1da811e8a327e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87887143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a80bdafe536381ccb2ca478501de1eb949ca16bbe5432f9a09eb0df68a20fc3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 07 Mar 2022 19:25:24 GMT
ADD file:7437bcc6a8a4f1ffb03fa2ebdd84ffb9bf89717db04d430a74f0a542191801f2 in / 
# Mon, 07 Mar 2022 19:25:25 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 07 Mar 2022 19:25:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6c6e19565a9d6e2bd55419bc0db9c8d874593e415f1d35070d7abd674397e634`  
		Last Modified: Mon, 07 Mar 2022 19:25:46 GMT  
		Size: 87.9 MB (87886926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d363dcd2615e669e423cc4ce51ba3fdfaa29ed41e88f5e2ac282bf71538f80f`  
		Last Modified: Mon, 07 Mar 2022 19:25:34 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:c98e97d043ce59c1175220540a14f5f4265b41a712e73191804ad4e43b6b4a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:775289f0df29b7731b59d98ce70363f577e9e8bf8ef5faed7b1da811e8a327e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87887143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a80bdafe536381ccb2ca478501de1eb949ca16bbe5432f9a09eb0df68a20fc3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 07 Mar 2022 19:25:24 GMT
ADD file:7437bcc6a8a4f1ffb03fa2ebdd84ffb9bf89717db04d430a74f0a542191801f2 in / 
# Mon, 07 Mar 2022 19:25:25 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 07 Mar 2022 19:25:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6c6e19565a9d6e2bd55419bc0db9c8d874593e415f1d35070d7abd674397e634`  
		Last Modified: Mon, 07 Mar 2022 19:25:46 GMT  
		Size: 87.9 MB (87886926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d363dcd2615e669e423cc4ce51ba3fdfaa29ed41e88f5e2ac282bf71538f80f`  
		Last Modified: Mon, 07 Mar 2022 19:25:34 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

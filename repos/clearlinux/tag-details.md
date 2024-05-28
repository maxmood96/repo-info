<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:cb33b9ffdb3209d73180cacd1d5b79be3e361d53caa35483c759a87b4c294d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:0f9cbcb789eb6ea44a7f964d1f3aef6555891fd57122849c5a5e53f78dbb7be4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69292440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1baa6bb36b89e1d974e534c56645445dcdf73f80410389afdbec024581f51661`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 28 May 2024 19:38:45 GMT
ADD file:a79c448585720b0b948c358a3c0ce2e65bb6501f73bf21a49ceb3a4b6ea77128 in / 
# Tue, 28 May 2024 19:38:46 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Tue, 28 May 2024 19:38:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6be0ada221e3c09542e21ccbdb28b6926efa8feb8706ced50474787b420e1952`  
		Last Modified: Tue, 28 May 2024 19:39:02 GMT  
		Size: 69.3 MB (69292227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b785e9c4ed1f0f7bea983a25e002a95d34ba8ae4903a0f05061fde1966fcdbc`  
		Last Modified: Tue, 28 May 2024 19:38:53 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:cb33b9ffdb3209d73180cacd1d5b79be3e361d53caa35483c759a87b4c294d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:0f9cbcb789eb6ea44a7f964d1f3aef6555891fd57122849c5a5e53f78dbb7be4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69292440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1baa6bb36b89e1d974e534c56645445dcdf73f80410389afdbec024581f51661`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 28 May 2024 19:38:45 GMT
ADD file:a79c448585720b0b948c358a3c0ce2e65bb6501f73bf21a49ceb3a4b6ea77128 in / 
# Tue, 28 May 2024 19:38:46 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Tue, 28 May 2024 19:38:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6be0ada221e3c09542e21ccbdb28b6926efa8feb8706ced50474787b420e1952`  
		Last Modified: Tue, 28 May 2024 19:39:02 GMT  
		Size: 69.3 MB (69292227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b785e9c4ed1f0f7bea983a25e002a95d34ba8ae4903a0f05061fde1966fcdbc`  
		Last Modified: Tue, 28 May 2024 19:38:53 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

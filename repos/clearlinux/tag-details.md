<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:4a99464b107e54ff8a2b9a970bda85d28c0bcd5f40e56f83b36343cca7bb24d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:42ef70f3e44a457bed4375bf8d2dbcc26593acd312a387c9264fcf20eecf1d19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88288664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64473bf30a74cbf7e67ca0caec7718c6316d65fa0bbfd9e9fa5d6891c02fd42`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 04 Apr 2023 00:13:08 GMT
ADD file:27575c202a2abd89600901c39a7353b2d48b6aa0a74e824b622d13f996c40aac in / 
# Tue, 04 Apr 2023 00:13:09 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Tue, 04 Apr 2023 00:13:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:45c184ce6ed90ef470846527c3ca80229708c497b7853b4f7d3d14313f2d3add`  
		Last Modified: Tue, 04 Apr 2023 00:13:28 GMT  
		Size: 88.3 MB (88288447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77085683b72643f0dcfbf685f719d8a5e3fbfc902e111f12474e18c13fe55be8`  
		Last Modified: Tue, 04 Apr 2023 00:13:17 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:4a99464b107e54ff8a2b9a970bda85d28c0bcd5f40e56f83b36343cca7bb24d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:42ef70f3e44a457bed4375bf8d2dbcc26593acd312a387c9264fcf20eecf1d19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88288664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64473bf30a74cbf7e67ca0caec7718c6316d65fa0bbfd9e9fa5d6891c02fd42`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 04 Apr 2023 00:13:08 GMT
ADD file:27575c202a2abd89600901c39a7353b2d48b6aa0a74e824b622d13f996c40aac in / 
# Tue, 04 Apr 2023 00:13:09 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Tue, 04 Apr 2023 00:13:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:45c184ce6ed90ef470846527c3ca80229708c497b7853b4f7d3d14313f2d3add`  
		Last Modified: Tue, 04 Apr 2023 00:13:28 GMT  
		Size: 88.3 MB (88288447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77085683b72643f0dcfbf685f719d8a5e3fbfc902e111f12474e18c13fe55be8`  
		Last Modified: Tue, 04 Apr 2023 00:13:17 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

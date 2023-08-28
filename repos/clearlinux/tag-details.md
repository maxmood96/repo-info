<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:bbaaedc9e9362228453e4e3e94ceb8053b445caef540de661a762e8ca2f3da6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:6adbd80beef6c6ee32c073bf7bb84970b8041327481db45b4c30442c3e3f4b21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67527116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fca667941c85b1bd26a968173c5fff6b60002b3a1a2489ae28aee73f0097e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 28 Aug 2023 21:35:52 GMT
ADD file:be92ec6b4bb02c918eb527d7686106dbbcb3f8256b56c8b5dc64ada2e9e5ec98 in / 
# Mon, 28 Aug 2023 21:35:53 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 28 Aug 2023 21:35:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9de2edb2a26a66b296a412a2e5b43071cdb0337aacd573d758a3b6f9208dfb2f`  
		Last Modified: Mon, 28 Aug 2023 21:36:10 GMT  
		Size: 67.5 MB (67526900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b75fe4e71f768a5f8b610ead83adf414bd21063d5dc5d7ee47d9c3d9b5dee2`  
		Last Modified: Mon, 28 Aug 2023 21:36:02 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:bbaaedc9e9362228453e4e3e94ceb8053b445caef540de661a762e8ca2f3da6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:6adbd80beef6c6ee32c073bf7bb84970b8041327481db45b4c30442c3e3f4b21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67527116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fca667941c85b1bd26a968173c5fff6b60002b3a1a2489ae28aee73f0097e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 28 Aug 2023 21:35:52 GMT
ADD file:be92ec6b4bb02c918eb527d7686106dbbcb3f8256b56c8b5dc64ada2e9e5ec98 in / 
# Mon, 28 Aug 2023 21:35:53 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 28 Aug 2023 21:35:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9de2edb2a26a66b296a412a2e5b43071cdb0337aacd573d758a3b6f9208dfb2f`  
		Last Modified: Mon, 28 Aug 2023 21:36:10 GMT  
		Size: 67.5 MB (67526900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b75fe4e71f768a5f8b610ead83adf414bd21063d5dc5d7ee47d9c3d9b5dee2`  
		Last Modified: Mon, 28 Aug 2023 21:36:02 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

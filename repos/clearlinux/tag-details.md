<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:0b66b964ad34340a6371ca7fa570ba7b5fb8a95c609ba92fc78677bf306e0096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:02016c5ea706ef6871bf1e8ff0c3f032e4a602939390a57854f97e28ac141ff1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71976643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b21e855b63e083c3927a348317eff5c97204f72fbcaf49a8b1d4cb3e32ff98a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 24 Sep 2024 01:19:31 GMT
ADD file:93fc58ed4a61cfd7e1e66244bb2528aa0d1a071d65a50793078f7d3bb547b34e in / 
# Tue, 24 Sep 2024 01:19:33 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Tue, 24 Sep 2024 01:19:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:af4cc291fb9e224e452390575eb4f9414aacedad0298b43095ca0b3ca737a138`  
		Last Modified: Tue, 24 Sep 2024 01:19:48 GMT  
		Size: 72.0 MB (71976432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3459b59be1664f4c1dd23a812fc33176bfcbacd680615ebd158ad70a8fd5fbe0`  
		Last Modified: Tue, 24 Sep 2024 01:19:40 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:0b66b964ad34340a6371ca7fa570ba7b5fb8a95c609ba92fc78677bf306e0096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:02016c5ea706ef6871bf1e8ff0c3f032e4a602939390a57854f97e28ac141ff1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71976643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b21e855b63e083c3927a348317eff5c97204f72fbcaf49a8b1d4cb3e32ff98a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 24 Sep 2024 01:19:31 GMT
ADD file:93fc58ed4a61cfd7e1e66244bb2528aa0d1a071d65a50793078f7d3bb547b34e in / 
# Tue, 24 Sep 2024 01:19:33 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Tue, 24 Sep 2024 01:19:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:af4cc291fb9e224e452390575eb4f9414aacedad0298b43095ca0b3ca737a138`  
		Last Modified: Tue, 24 Sep 2024 01:19:48 GMT  
		Size: 72.0 MB (71976432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3459b59be1664f4c1dd23a812fc33176bfcbacd680615ebd158ad70a8fd5fbe0`  
		Last Modified: Tue, 24 Sep 2024 01:19:40 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

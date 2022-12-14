<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:f7f49614dc80208c5404dfa320f7b1b1473734b33ed8defeefbaa76a9460f1a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:8585c9d338ed8f011c5d675a33326fecc9704078f38dc12c0670d47835fdbd6f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67750581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347742f59794ae575ca668e98a6dec2f321f9049aa8fa476ea50952cceb5b5f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 12 Dec 2022 20:26:03 GMT
ADD file:978af8154b6155803c7ce7e0c6715fa5c74eaf18d1f1e595e133616b96b43b98 in / 
# Mon, 12 Dec 2022 20:26:04 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 12 Dec 2022 20:26:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6e573c00357cde21a5f115a6e09ba8a0dbdb5161a0e806f707b37d7824b904d7`  
		Last Modified: Mon, 12 Dec 2022 20:26:23 GMT  
		Size: 67.8 MB (67750364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a034f3d5214e6996df6fd98f5c79cde5f6e10c8cda7fc386bb2c61cc752fa3`  
		Last Modified: Mon, 12 Dec 2022 20:26:13 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:f7f49614dc80208c5404dfa320f7b1b1473734b33ed8defeefbaa76a9460f1a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:8585c9d338ed8f011c5d675a33326fecc9704078f38dc12c0670d47835fdbd6f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67750581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347742f59794ae575ca668e98a6dec2f321f9049aa8fa476ea50952cceb5b5f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 12 Dec 2022 20:26:03 GMT
ADD file:978af8154b6155803c7ce7e0c6715fa5c74eaf18d1f1e595e133616b96b43b98 in / 
# Mon, 12 Dec 2022 20:26:04 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 12 Dec 2022 20:26:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6e573c00357cde21a5f115a6e09ba8a0dbdb5161a0e806f707b37d7824b904d7`  
		Last Modified: Mon, 12 Dec 2022 20:26:23 GMT  
		Size: 67.8 MB (67750364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a034f3d5214e6996df6fd98f5c79cde5f6e10c8cda7fc386bb2c61cc752fa3`  
		Last Modified: Mon, 12 Dec 2022 20:26:13 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

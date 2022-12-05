<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:f80c5f759272d4292238f30fc3d4258a471e4c082605fd0dece7ecea50270ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:f6f1cbbe03ffe42bc1abf0ed2a7126929e611f88f38b6f29c6bd3c3b50023ad1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67763561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c6b35c3ad455f682617a6815a3c0485494bd3d48d1c39fab6e3f5a7fab6b2e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 05 Dec 2022 20:24:14 GMT
ADD file:97a4d354b5fddfa169b16cd279326d5c5ec4a3733009e7925587243193e91b37 in / 
# Mon, 05 Dec 2022 20:24:15 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 05 Dec 2022 20:24:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b93ae971c23d0ab1108f7723f54374a233316109fdd50e83c1c20e8231a38c73`  
		Last Modified: Mon, 05 Dec 2022 20:24:35 GMT  
		Size: 67.8 MB (67763343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76415ad42ba036965beba6408fec22217729f79db52120af6e6c80a970680150`  
		Last Modified: Mon, 05 Dec 2022 20:24:24 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:f80c5f759272d4292238f30fc3d4258a471e4c082605fd0dece7ecea50270ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:f6f1cbbe03ffe42bc1abf0ed2a7126929e611f88f38b6f29c6bd3c3b50023ad1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67763561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c6b35c3ad455f682617a6815a3c0485494bd3d48d1c39fab6e3f5a7fab6b2e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 05 Dec 2022 20:24:14 GMT
ADD file:97a4d354b5fddfa169b16cd279326d5c5ec4a3733009e7925587243193e91b37 in / 
# Mon, 05 Dec 2022 20:24:15 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 05 Dec 2022 20:24:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b93ae971c23d0ab1108f7723f54374a233316109fdd50e83c1c20e8231a38c73`  
		Last Modified: Mon, 05 Dec 2022 20:24:35 GMT  
		Size: 67.8 MB (67763343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76415ad42ba036965beba6408fec22217729f79db52120af6e6c80a970680150`  
		Last Modified: Mon, 05 Dec 2022 20:24:24 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

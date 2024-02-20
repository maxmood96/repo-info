## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:36c0bcd654022ca5cea84fb344cfc6f5e4b3e4c6685052709f599a51e5a4a030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:4e777ee9d0c7b7ac8cf6d7127d998b39c53309fda94a868619c8e0129531f31a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64155612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507e729679aae632b331562f647f04c786e3cd83f97ebbd615c4fb96e417924d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 20 Feb 2024 20:51:49 GMT
ADD file:12650be020952097b8c74607c06b5d8c6e3ee5fdf875e27b2bdf80cbf6d8095c in / 
# Tue, 20 Feb 2024 20:51:50 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Tue, 20 Feb 2024 20:51:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6520c4a82c8e778eccfa200f2340cac19933fa1d6324d345899bde3290a85b9f`  
		Last Modified: Tue, 20 Feb 2024 20:52:06 GMT  
		Size: 64.2 MB (64155399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e62ca971d7cc2a148c979ced9e132abfe7dfcd72b72ac0c4084fa8f53a3665`  
		Last Modified: Tue, 20 Feb 2024 20:51:58 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

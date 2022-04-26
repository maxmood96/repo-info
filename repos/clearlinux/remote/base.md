## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:1d6ed1cf54763afed4271626d989e0463825de396f827bf5670a66cb4c0d279e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:1a88668b734f7764eca0f372bb3ea59b5185ad27cd9c0f45412cd32401b0b0ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88170220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa823bd740bf36eb41798f0f58433742c4b06ed03537404d1e5a0076e25e66af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 26 Apr 2022 00:27:38 GMT
ADD file:6c0e9897f20e99d6a8607ace8a0dfdb8b0f416355e753dc1191ca16b0ffbe02a in / 
# Tue, 26 Apr 2022 00:27:39 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Tue, 26 Apr 2022 00:27:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:779cb7d029bbc5af977954db78d8bca619a8470f7f305a83de85f6f53884e357`  
		Last Modified: Tue, 26 Apr 2022 00:28:00 GMT  
		Size: 88.2 MB (88170003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b50c25ce7e061bb0d85418eff22fc810e45af90b7ad3ca1c3324e34ec4967da`  
		Last Modified: Tue, 26 Apr 2022 00:27:48 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

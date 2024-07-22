## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:e53de78f4d68bd92cfa181e94735475030a2e9eb643aeab0a7abfb40587013f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:5007c169e3d376ae6db72a12ba8c55353d89c56f7c46896ed081c1dbba56bd3e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71653769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57576e3d5571ef9c5fe7c9854fa30a594262ce9ade5c2396e9f981eb2f88b646`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 22 Jul 2024 19:19:46 GMT
ADD file:cce4a74a41b48c373a881881cc696180076f81429d5e2b6d0df132e042f8e85d in / 
# Mon, 22 Jul 2024 19:19:47 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 22 Jul 2024 19:19:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:126d80e6104420c40dec44d55f0df6f6a39efeba4ac12e7eb89072de870ae86b`  
		Last Modified: Mon, 22 Jul 2024 19:20:04 GMT  
		Size: 71.7 MB (71653556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6b7b92fcae53b4db19b8ec775529975f4e71b84f1f2e9930c392ff51c87378`  
		Last Modified: Mon, 22 Jul 2024 19:19:55 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

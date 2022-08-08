## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:2ff048cc5ead7c511a6590d0a461b16d9d2542f5bad8a3f80b8f66ebac24f0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:dfea13124be2d6d57a112759b6f14823883b9618ea2253bf5686ef3107b51e7f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.1 MB (95060633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bc5fc9ea7dd280555f24c531e2121b7e7755da43664f9ec78938d2238a0754`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 08 Aug 2022 19:23:52 GMT
ADD file:3bcc0645e2a991a67972ff3e2c4fa2183a57dd43e0470f0c74f99c32d4bd7a6d in / 
# Mon, 08 Aug 2022 19:23:53 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 08 Aug 2022 19:23:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d508ba1b55e68e326a72ce128f5afe0b850d5cbeaa927cfd6987a5a9bbea60be`  
		Last Modified: Mon, 08 Aug 2022 19:24:16 GMT  
		Size: 95.1 MB (95060416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f987f252941bbb5f874fa0a11a1bb09f99fe31112a09c93ab3654eb6d5e41e0`  
		Last Modified: Mon, 08 Aug 2022 19:24:02 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:11b3b3fe9f21b8ecfb1e40fc2690daf0c748107c4ea1025a2bacc2c04c43ac78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:56dc5d3857ea94c4126ce4fc0bd659cffb927730a1242114c00865ed2ddc6b37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66277835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c025081e36f1198c8c63929c968585ac72204ce7847e8246d9ca2ad5404930`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 10 Jul 2023 19:26:20 GMT
ADD file:0528d71a3e795be6bfd19a18a57a6ecc3be252574c6467ca3a5afc8e2f7a9a51 in / 
# Mon, 10 Jul 2023 19:26:21 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 10 Jul 2023 19:26:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b1f98f8b070c1311ffb375ca1758f4af32cef06d07c0c5e0e2d264443ade558f`  
		Last Modified: Mon, 10 Jul 2023 19:26:39 GMT  
		Size: 66.3 MB (66277617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6790428d368ba733e6b400c4eb4ae76dd9c6f9355164d8a155dcc1cb3932bd7b`  
		Last Modified: Mon, 10 Jul 2023 19:26:30 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

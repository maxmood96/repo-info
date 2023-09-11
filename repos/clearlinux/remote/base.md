## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:c823303674b0ecdabe4f493f4c8fd9f389192e796fd76675b8d8920044b1db63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:173a55c490b8fd32c2e51d1511eac0d17892dc62668e2fdabd33bb6b81c86547
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67557425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6c2ee54f5109e953cec11dd61ba0f501da869b110cecb253b7d78954ea45f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 11 Sep 2023 19:23:24 GMT
ADD file:af2ebd8edcc69a75e40def324e6d6815d0e71955e3d71f25720053eaa120cbaf in / 
# Mon, 11 Sep 2023 19:23:25 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 11 Sep 2023 19:23:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0142c9b4b1e70b7ac983bc0a3237d2f006ecc3dbf80a856306b503ac89cbcf3f`  
		Last Modified: Mon, 11 Sep 2023 19:23:43 GMT  
		Size: 67.6 MB (67557209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915fd3f8ec9d18c8b9213d38124a6eb4f0008e0820e4f5297474af2200f6da6a`  
		Last Modified: Mon, 11 Sep 2023 19:23:34 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

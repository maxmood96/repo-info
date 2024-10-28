## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:f83c329901bef1a1584ef0ae4954a0e4a91b8c96323da0445e067ee84b87da59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:ef94badad818fb201d7eab9d6c4b26358d8f64c65dfd236cdb4580e42b3627b2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72126654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1c05d983c684009c8a333d60235a502213ecd313979d99a2b5df723f2dc5a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 28 Oct 2024 18:21:02 GMT
ADD file:27ae8ee42929e1e6c2cebfe5fe70bcc154475eaa6b66bd4343e95be4028c9f65 in / 
# Mon, 28 Oct 2024 18:21:03 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 28 Oct 2024 18:21:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d36fb7dc33391e6da885cd9e22972b1201345856083e570f45f4e16629977869`  
		Last Modified: Mon, 28 Oct 2024 18:21:20 GMT  
		Size: 72.1 MB (72126442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6635763edc91463f5efefbc27f322a868f2be84fb69870b018aaecafa36225b`  
		Last Modified: Mon, 28 Oct 2024 18:21:11 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

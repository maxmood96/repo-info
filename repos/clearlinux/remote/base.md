## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:b378ae9ccb03b26976c13594200e679b5457fb11c9d7c72798f67d2a70519e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:df47d4a288aded5381f57c469da899cc8f2b99086077717e442085dafb5d0eb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66487279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc2f60cf24100cb878c9b78c6d1e9c9ea0d16c92909f2997c01c1c9eb546bd0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 17 Jul 2023 19:23:58 GMT
ADD file:bbae4a803890482b995f4e671262c934a60de338681cc176a6b04c7598cba8cd in / 
# Mon, 17 Jul 2023 19:23:59 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 17 Jul 2023 19:23:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:94399da0895abe2b03914aaa6d7b453eafd78e48fae0bf737826bd7484da45bb`  
		Last Modified: Mon, 17 Jul 2023 19:24:16 GMT  
		Size: 66.5 MB (66487063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75370fbf789efe55c60f149d3a5ac18f32f98dc10fd247e08d8f86ac1aaf49e9`  
		Last Modified: Mon, 17 Jul 2023 19:24:08 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

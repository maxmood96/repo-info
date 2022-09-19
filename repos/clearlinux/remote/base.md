## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:364ea5b71f8b15328ed448df931e8964e0732f7f3c823ad44355ce388ef32d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:8dc0cee1ff454101028952152481f01e5999cd8e79573f6f0682bbaf975192c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69817797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8911b292b56f7dd43f8fc6df067509910d625d18e282d802857d9f346bcf28ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 19 Sep 2022 17:46:30 GMT
ADD file:4b823dcd1979da64f8f41fdcbf3712da74d861e676dafb9088337d6b779b56d0 in / 
# Mon, 19 Sep 2022 17:46:31 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 19 Sep 2022 17:46:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ad8f4be916f3228c9e4e92e7d73ed14e684660d6728ca855efbb29312faa8468`  
		Last Modified: Mon, 19 Sep 2022 17:46:51 GMT  
		Size: 69.8 MB (69817579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaa9be6d9aecb4b3ccb54367f034d83ab73bb6cbc81583a6554086aa6c55094`  
		Last Modified: Mon, 19 Sep 2022 17:46:41 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

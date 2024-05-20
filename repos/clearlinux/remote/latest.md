## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:ca43c92e37798b863c65a43a35b73ecde7f5f47af03d2b08de4c21a7e9691b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:683443060f924791f107b52c5a1701bf154b0b59c746fdc1e9e24d36339b7589
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69292386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdc9a5e22baab937ce4c837a409c36116e9feaacad90bbc016538afb39f1777`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 20 May 2024 17:30:22 GMT
ADD file:998a70900d3f3a1bf84706124bed23f4626b936d311a93d27efbe97041b248e0 in / 
# Mon, 20 May 2024 17:30:23 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 20 May 2024 17:30:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e959db6772fd2563f7ed2c8c969ebded00f958ab5b2699101cd008eace17bfa3`  
		Last Modified: Mon, 20 May 2024 17:30:40 GMT  
		Size: 69.3 MB (69292173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb690f9c4570f25b4ccaf0f683b34dc26cbf4704819ba7aead0df53bb2bc3e4`  
		Last Modified: Mon, 20 May 2024 17:30:32 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

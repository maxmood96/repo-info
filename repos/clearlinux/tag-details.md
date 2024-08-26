<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:8ae451c51e10dd71bc471380ea336c101cb52377f0a4a258689e03cef5288c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:7d71a15a6db4db67a23788b2e662720d96e3a7f1131f90b1c03c2e041be8d401
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72011806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d212ba6f387e8f53178e3931cd94bfd2438d864f75fcaa153197904555e195b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 26 Aug 2024 20:19:32 GMT
ADD file:2b9c21074f6700e724f81fbdaefc3d23a8f2e47d9c9e06e50a17ab72ab41164a in / 
# Mon, 26 Aug 2024 20:19:34 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 26 Aug 2024 20:19:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e4fcaa52bf3df3541f23ec66b1234801bcf6c27b16a1c04481eb3aedf10575a3`  
		Last Modified: Mon, 26 Aug 2024 20:19:51 GMT  
		Size: 72.0 MB (72011593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9283b4920c43fbe9bdb9e961b879a69f5533b8f2948748a0d5bb3aef5e433fc`  
		Last Modified: Mon, 26 Aug 2024 20:19:42 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:8ae451c51e10dd71bc471380ea336c101cb52377f0a4a258689e03cef5288c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:7d71a15a6db4db67a23788b2e662720d96e3a7f1131f90b1c03c2e041be8d401
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72011806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d212ba6f387e8f53178e3931cd94bfd2438d864f75fcaa153197904555e195b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 26 Aug 2024 20:19:32 GMT
ADD file:2b9c21074f6700e724f81fbdaefc3d23a8f2e47d9c9e06e50a17ab72ab41164a in / 
# Mon, 26 Aug 2024 20:19:34 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 26 Aug 2024 20:19:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e4fcaa52bf3df3541f23ec66b1234801bcf6c27b16a1c04481eb3aedf10575a3`  
		Last Modified: Mon, 26 Aug 2024 20:19:51 GMT  
		Size: 72.0 MB (72011593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9283b4920c43fbe9bdb9e961b879a69f5533b8f2948748a0d5bb3aef5e433fc`  
		Last Modified: Mon, 26 Aug 2024 20:19:42 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

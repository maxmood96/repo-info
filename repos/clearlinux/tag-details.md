<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:c72587afede9974f490232c0fd434403dd4f331c138622eb92fe13158f06e672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:f63acad2737b62dace32a65d74c7ce0efce633e0777d9db14c0cb88c9d694dd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67238571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c4bbd390e68432431a057da905259b23660d6e393d5d6ea1cc9220be0ec3d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 01 Apr 2024 17:53:21 GMT
ADD file:a851ca66a46fc3b7e7aefdc497e4a50d7a4f8baa5ca58db7f22d48d241b24a11 in / 
# Mon, 01 Apr 2024 17:53:22 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 01 Apr 2024 17:53:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:22310d7f9c25327f62cda519b6195dca122d270189aa73cbc5c0fa48d5147bcc`  
		Last Modified: Mon, 01 Apr 2024 17:53:38 GMT  
		Size: 67.2 MB (67238359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8551285416eeec63b20c4680b3d42b86079a9e4daa6f067d79771e2819bd4455`  
		Last Modified: Mon, 01 Apr 2024 17:53:30 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:c72587afede9974f490232c0fd434403dd4f331c138622eb92fe13158f06e672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:f63acad2737b62dace32a65d74c7ce0efce633e0777d9db14c0cb88c9d694dd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67238571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c4bbd390e68432431a057da905259b23660d6e393d5d6ea1cc9220be0ec3d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 01 Apr 2024 17:53:21 GMT
ADD file:a851ca66a46fc3b7e7aefdc497e4a50d7a4f8baa5ca58db7f22d48d241b24a11 in / 
# Mon, 01 Apr 2024 17:53:22 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 01 Apr 2024 17:53:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:22310d7f9c25327f62cda519b6195dca122d270189aa73cbc5c0fa48d5147bcc`  
		Last Modified: Mon, 01 Apr 2024 17:53:38 GMT  
		Size: 67.2 MB (67238359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8551285416eeec63b20c4680b3d42b86079a9e4daa6f067d79771e2819bd4455`  
		Last Modified: Mon, 01 Apr 2024 17:53:30 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

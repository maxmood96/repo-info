<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:dbd0eca9a5c02a4756e5be8fa0a0ee63052a1b534cb3517334d3abe79c057885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:61776319e03f9427ef3590dc141bba5b9bc0b0ab1b087c9087e53170a70dc85e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72032204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60ad17b6cd27fed4dd76aa97b148492d7054bfebe83cef7a6e6791d287feebc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 12 Aug 2024 17:19:29 GMT
ADD file:03a41b9593d2149b8757da6ea7e86e8259a58f6b084fc0a1808f03ef6863cf1d in / 
# Mon, 12 Aug 2024 17:19:30 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 12 Aug 2024 17:19:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a783a3d28d1f9be0dc9b70cc827b82c7ae5269917df17c02484a73afc9a08529`  
		Last Modified: Mon, 12 Aug 2024 17:19:47 GMT  
		Size: 72.0 MB (72031990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49222ae9ec4aeb26359478fc893eaeda0fb521a66904192175d6952a35d1a89b`  
		Last Modified: Mon, 12 Aug 2024 17:19:38 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:dbd0eca9a5c02a4756e5be8fa0a0ee63052a1b534cb3517334d3abe79c057885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:61776319e03f9427ef3590dc141bba5b9bc0b0ab1b087c9087e53170a70dc85e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72032204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60ad17b6cd27fed4dd76aa97b148492d7054bfebe83cef7a6e6791d287feebc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 12 Aug 2024 17:19:29 GMT
ADD file:03a41b9593d2149b8757da6ea7e86e8259a58f6b084fc0a1808f03ef6863cf1d in / 
# Mon, 12 Aug 2024 17:19:30 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 12 Aug 2024 17:19:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a783a3d28d1f9be0dc9b70cc827b82c7ae5269917df17c02484a73afc9a08529`  
		Last Modified: Mon, 12 Aug 2024 17:19:47 GMT  
		Size: 72.0 MB (72031990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49222ae9ec4aeb26359478fc893eaeda0fb521a66904192175d6952a35d1a89b`  
		Last Modified: Mon, 12 Aug 2024 17:19:38 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

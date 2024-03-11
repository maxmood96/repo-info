<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:4804931034e4949da1f1b983b3c9af69fd0cd192d286cd7c0c651dc4d1a8c06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:53f408b2d59e384899f1b1eb3c037238d5dc6cd9a34a57c60d19e590b1c6da33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65306237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c27f684e5f386585f0144a348ffdfaa03ee6a5218eacb3f3eb83db388211a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 11 Mar 2024 19:51:15 GMT
ADD file:76662cb08c3e57e079ea924073f84be014ddb050c253fdefd5bef653e822eff8 in / 
# Mon, 11 Mar 2024 19:51:16 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 11 Mar 2024 19:51:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5b8f84368ff11d325385881fb1ecd7ec551da9fea6f39ce0da367e0aa50b5abf`  
		Last Modified: Mon, 11 Mar 2024 19:51:33 GMT  
		Size: 65.3 MB (65306024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839a61c6e9f6f0bb0cfddb4975a90a3f4e4e04020799e643a4a318cc8dff99c1`  
		Last Modified: Mon, 11 Mar 2024 19:51:24 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:4804931034e4949da1f1b983b3c9af69fd0cd192d286cd7c0c651dc4d1a8c06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:53f408b2d59e384899f1b1eb3c037238d5dc6cd9a34a57c60d19e590b1c6da33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65306237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c27f684e5f386585f0144a348ffdfaa03ee6a5218eacb3f3eb83db388211a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 11 Mar 2024 19:51:15 GMT
ADD file:76662cb08c3e57e079ea924073f84be014ddb050c253fdefd5bef653e822eff8 in / 
# Mon, 11 Mar 2024 19:51:16 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 11 Mar 2024 19:51:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5b8f84368ff11d325385881fb1ecd7ec551da9fea6f39ce0da367e0aa50b5abf`  
		Last Modified: Mon, 11 Mar 2024 19:51:33 GMT  
		Size: 65.3 MB (65306024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839a61c6e9f6f0bb0cfddb4975a90a3f4e4e04020799e643a4a318cc8dff99c1`  
		Last Modified: Mon, 11 Mar 2024 19:51:24 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

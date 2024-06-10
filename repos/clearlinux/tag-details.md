<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:cf5bb8bbc9726fec462ef2e63b661bb3b7e84bb74c79828da844e45cb68d0f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:141e9b6fd6665173fa73261c30d49c8276dc00a5c3737e69d6398e10a70c12cb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69484354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:279adab5b6833aee7089d9e6c7f80ba9fee42f068fd01b6336a08feeab3edfce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 10 Jun 2024 19:58:58 GMT
ADD file:5a573e0f5139ecd18c2fd23f5b5c9823a21d101d4f9a10bf5633fd2527fd9994 in / 
# Mon, 10 Jun 2024 19:58:59 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 10 Jun 2024 19:58:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c1cea996e584973aa2245a8078e88132b11e65c524544aa53911d7c5177e2ff8`  
		Last Modified: Mon, 10 Jun 2024 19:59:17 GMT  
		Size: 69.5 MB (69484140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f67ad38bd318019cc8434735cd901809b41f7c9f80bb0e02ab51b3617bdf04f`  
		Last Modified: Mon, 10 Jun 2024 19:59:09 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:cf5bb8bbc9726fec462ef2e63b661bb3b7e84bb74c79828da844e45cb68d0f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:141e9b6fd6665173fa73261c30d49c8276dc00a5c3737e69d6398e10a70c12cb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69484354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:279adab5b6833aee7089d9e6c7f80ba9fee42f068fd01b6336a08feeab3edfce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 10 Jun 2024 19:58:58 GMT
ADD file:5a573e0f5139ecd18c2fd23f5b5c9823a21d101d4f9a10bf5633fd2527fd9994 in / 
# Mon, 10 Jun 2024 19:58:59 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 10 Jun 2024 19:58:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c1cea996e584973aa2245a8078e88132b11e65c524544aa53911d7c5177e2ff8`  
		Last Modified: Mon, 10 Jun 2024 19:59:17 GMT  
		Size: 69.5 MB (69484140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f67ad38bd318019cc8434735cd901809b41f7c9f80bb0e02ab51b3617bdf04f`  
		Last Modified: Mon, 10 Jun 2024 19:59:09 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

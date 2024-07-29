<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:d9176f3ddc59098a32badb035dc68f51717c7173cbc2ebc8d75492fd1c5eb1a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:edffe731dfaa13ec829bfc4b5bfe61d207ee7330d723ff8c81a87b0fd43997ff
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71654399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1671429cf3125a41b9b6745ff67d6ebfd15717cc61a40be85f15bcd523516a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 29 Jul 2024 17:19:49 GMT
ADD file:7fcd0777b784707f3ca8906cdb113b3b53d05e5836f036eda51a588d64928d56 in / 
# Mon, 29 Jul 2024 17:19:50 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 29 Jul 2024 17:19:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:13752de0b879df3da9da13f1c417c63ed3b4ffa9535acc479779d1c4f069081c`  
		Last Modified: Mon, 29 Jul 2024 17:20:07 GMT  
		Size: 71.7 MB (71654187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677cebad298f45efa61bb3b03d5aac2a1a7d881508b6495a62ad41963cb60f47`  
		Last Modified: Mon, 29 Jul 2024 17:19:58 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:d9176f3ddc59098a32badb035dc68f51717c7173cbc2ebc8d75492fd1c5eb1a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:edffe731dfaa13ec829bfc4b5bfe61d207ee7330d723ff8c81a87b0fd43997ff
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71654399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1671429cf3125a41b9b6745ff67d6ebfd15717cc61a40be85f15bcd523516a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 29 Jul 2024 17:19:49 GMT
ADD file:7fcd0777b784707f3ca8906cdb113b3b53d05e5836f036eda51a588d64928d56 in / 
# Mon, 29 Jul 2024 17:19:50 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 29 Jul 2024 17:19:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:13752de0b879df3da9da13f1c417c63ed3b4ffa9535acc479779d1c4f069081c`  
		Last Modified: Mon, 29 Jul 2024 17:20:07 GMT  
		Size: 71.7 MB (71654187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677cebad298f45efa61bb3b03d5aac2a1a7d881508b6495a62ad41963cb60f47`  
		Last Modified: Mon, 29 Jul 2024 17:19:58 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

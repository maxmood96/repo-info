<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:32dc34659a454622d39998d85c857522030e8fd8f3d49ce55a04f14a5c0a958b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:c86d158fba27af45055c7f64587b94c0f64f840ae7de4788201510cb37e40e12
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88156302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d4afa6eea0baf9b77aaa93698899769fc55d48115c8bbd60a1f026104311b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 06 Jun 2022 18:24:40 GMT
ADD file:76c1a1053f72d9dc323c19b1ba84f128eff82b18e4faf30ccd798990c91047e6 in / 
# Mon, 06 Jun 2022 18:24:42 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 06 Jun 2022 18:24:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ac8a9f38ec8f6a3e8b3f34593f52a520835ab0234156c019b3fa479aaa81199a`  
		Last Modified: Mon, 06 Jun 2022 18:25:04 GMT  
		Size: 88.2 MB (88156084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06f30b65dc759cf87e6d178c2ef80074aa3c78a0c571fe298e4610b09fc88e2`  
		Last Modified: Mon, 06 Jun 2022 18:24:52 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:32dc34659a454622d39998d85c857522030e8fd8f3d49ce55a04f14a5c0a958b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:c86d158fba27af45055c7f64587b94c0f64f840ae7de4788201510cb37e40e12
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88156302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d4afa6eea0baf9b77aaa93698899769fc55d48115c8bbd60a1f026104311b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 06 Jun 2022 18:24:40 GMT
ADD file:76c1a1053f72d9dc323c19b1ba84f128eff82b18e4faf30ccd798990c91047e6 in / 
# Mon, 06 Jun 2022 18:24:42 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 06 Jun 2022 18:24:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ac8a9f38ec8f6a3e8b3f34593f52a520835ab0234156c019b3fa479aaa81199a`  
		Last Modified: Mon, 06 Jun 2022 18:25:04 GMT  
		Size: 88.2 MB (88156084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06f30b65dc759cf87e6d178c2ef80074aa3c78a0c571fe298e4610b09fc88e2`  
		Last Modified: Mon, 06 Jun 2022 18:24:52 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:3bb78c908000dc9b1b3d578ce5bc006c3f15dff23710fa2f51abf18a32780d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:c2712258badc683ce193d4a335115d70cb2cf284a4f8aafb51d8d38f0e75df65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67525112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37435fdaad1afb1f1c06e321612f6f81e4b054bbe20f1be18fa3832e98cb3b81`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 14 Aug 2023 18:21:51 GMT
ADD file:9c119753324a4d0a707d95060cf95afdb8d7c56ee835c5baf1ba2b93c2988670 in / 
# Mon, 14 Aug 2023 18:21:52 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 14 Aug 2023 18:21:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ed40ee1c4fc3158371e9acd646b107cfb346f973933064376be657d7d7b3f0d4`  
		Last Modified: Mon, 14 Aug 2023 18:22:09 GMT  
		Size: 67.5 MB (67524895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee747e0d04fcea4d841c1a7fede1fed722c981f1dfb47af81923a2b340fb58d`  
		Last Modified: Mon, 14 Aug 2023 18:22:01 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

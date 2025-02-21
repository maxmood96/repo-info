## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:7b651a0d390ef81a2e5c9d086cb1ff161d3c8efd6891f88428c320ae9dd3c023
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:04a40b43f845e54ddcc155b84320fc9854c63c8a355d2db9793dcf9a15804a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72393244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b0f3f7c7050406d5c003983a7625e4f1b06fe949d5478e65ee24a0f3de439c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Feb 2025 23:56:33 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Fri, 14 Feb 2025 23:56:33 GMT
ADD base.tar.xz / # buildkit
# Fri, 14 Feb 2025 23:56:33 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Fri, 14 Feb 2025 23:56:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:48e316792ab9147f178f867974ad7499e1b052680a24d18a6979145c4538fef8`  
		Last Modified: Tue, 18 Feb 2025 20:30:09 GMT  
		Size: 72.4 MB (72393027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60064d076caba0094d77b5a2ac9cc898dd7ce4902a756733a068e90a7cb494b3`  
		Last Modified: Tue, 18 Feb 2025 20:30:08 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:481f6078d5f2cf1c869bc1d506c67b273a358f4e7c5c7dee2909ac57b6eba4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f9cde6ed412e3389c0accd53a763526b904827c38aad97133966e03b3d6e97`

```dockerfile
```

-	Layers:
	-	`sha256:184b761288d8346480dcaa376706be8dfa5a9bf871cf05d787bbd0ec2fb7c563`  
		Last Modified: Tue, 18 Feb 2025 20:30:08 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json

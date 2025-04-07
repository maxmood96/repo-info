<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:3e8dc8d3596ae3ee57e038157b39257ffe0ea46d63101050b8d852198bc24cbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:1a4368aec1d8756044f957d05e727deefa9531387b94e50b074622acd52663dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73421001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c34a6b896ef15ae55c9c8f9c4dd9b5766cf44caa629a77990f768475a22807f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Apr 2025 20:30:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Wed, 02 Apr 2025 20:30:39 GMT
ADD base.tar.xz / # buildkit
# Wed, 02 Apr 2025 20:30:39 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Wed, 02 Apr 2025 20:30:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6c56b4be6b025a148191b4f15d34f218030fa1cd2f299737510797a39486fd1d`  
		Last Modified: Mon, 07 Apr 2025 18:18:08 GMT  
		Size: 73.4 MB (73420787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038e3a8131e37c00809e1c1369ef98af65f3af64642dd4ffadffac6906c8ef77`  
		Last Modified: Mon, 07 Apr 2025 18:18:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:bdcfdcc1e0789026df746ecc0cff9d996192c0448b097ae90d28ae4464984467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f85f1bcb943bb32da4a84b36fb2bd833ff7f01a278203a1d2c3c4dd788021a`

```dockerfile
```

-	Layers:
	-	`sha256:1939da54e0c0a47ee94c6f2a1028775432ddd12d3aee7713d83b0a2bc91d982b`  
		Last Modified: Mon, 07 Apr 2025 18:18:06 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:3e8dc8d3596ae3ee57e038157b39257ffe0ea46d63101050b8d852198bc24cbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:1a4368aec1d8756044f957d05e727deefa9531387b94e50b074622acd52663dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73421001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c34a6b896ef15ae55c9c8f9c4dd9b5766cf44caa629a77990f768475a22807f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Apr 2025 20:30:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Wed, 02 Apr 2025 20:30:39 GMT
ADD base.tar.xz / # buildkit
# Wed, 02 Apr 2025 20:30:39 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Wed, 02 Apr 2025 20:30:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6c56b4be6b025a148191b4f15d34f218030fa1cd2f299737510797a39486fd1d`  
		Last Modified: Mon, 07 Apr 2025 18:18:08 GMT  
		Size: 73.4 MB (73420787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038e3a8131e37c00809e1c1369ef98af65f3af64642dd4ffadffac6906c8ef77`  
		Last Modified: Mon, 07 Apr 2025 18:18:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:bdcfdcc1e0789026df746ecc0cff9d996192c0448b097ae90d28ae4464984467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f85f1bcb943bb32da4a84b36fb2bd833ff7f01a278203a1d2c3c4dd788021a`

```dockerfile
```

-	Layers:
	-	`sha256:1939da54e0c0a47ee94c6f2a1028775432ddd12d3aee7713d83b0a2bc91d982b`  
		Last Modified: Mon, 07 Apr 2025 18:18:06 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json

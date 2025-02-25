<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:c36e55a8cc5e678943ef86a32c4ae848eb7fbda423583bb877d728c4c02f3edb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:b183d96f03c03739bfc15c8c11fbefe49821fcccd181ca7b8567e8a72f36b4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72373699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43397ef61df70072890c6776c9d07a62a0cd40760489c873b989f0b433f13ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Feb 2025 18:21:34 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 18 Feb 2025 18:21:34 GMT
ADD base.tar.xz / # buildkit
# Tue, 18 Feb 2025 18:21:34 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Tue, 18 Feb 2025 18:21:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3c002503d7861cde41e618f15014952b58340585d6995d0d0273eae6fbb30871`  
		Last Modified: Mon, 24 Feb 2025 20:28:39 GMT  
		Size: 72.4 MB (72373485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e191daf97a1bf8eff61688fbefed1008eb340924fa68391a7bb6512122d3227`  
		Last Modified: Mon, 24 Feb 2025 20:28:38 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:f891da1330d403a2d0a82e1d6063bcf95a8ae7079f06fd48d8cc48b0713fd13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef25ad9cc7a263a901ee3108be849d378b8dcb7e2cf6e4e036c10df4d814414f`

```dockerfile
```

-	Layers:
	-	`sha256:04ef123962e149223434aa3a68fa81a040244965410d3286df7bf4f21f3afd5c`  
		Last Modified: Mon, 24 Feb 2025 20:28:38 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:c36e55a8cc5e678943ef86a32c4ae848eb7fbda423583bb877d728c4c02f3edb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:b183d96f03c03739bfc15c8c11fbefe49821fcccd181ca7b8567e8a72f36b4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72373699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43397ef61df70072890c6776c9d07a62a0cd40760489c873b989f0b433f13ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Feb 2025 18:21:34 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 18 Feb 2025 18:21:34 GMT
ADD base.tar.xz / # buildkit
# Tue, 18 Feb 2025 18:21:34 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Tue, 18 Feb 2025 18:21:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3c002503d7861cde41e618f15014952b58340585d6995d0d0273eae6fbb30871`  
		Last Modified: Mon, 24 Feb 2025 20:28:39 GMT  
		Size: 72.4 MB (72373485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e191daf97a1bf8eff61688fbefed1008eb340924fa68391a7bb6512122d3227`  
		Last Modified: Mon, 24 Feb 2025 20:28:38 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:f891da1330d403a2d0a82e1d6063bcf95a8ae7079f06fd48d8cc48b0713fd13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef25ad9cc7a263a901ee3108be849d378b8dcb7e2cf6e4e036c10df4d814414f`

```dockerfile
```

-	Layers:
	-	`sha256:04ef123962e149223434aa3a68fa81a040244965410d3286df7bf4f21f3afd5c`  
		Last Modified: Mon, 24 Feb 2025 20:28:38 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json

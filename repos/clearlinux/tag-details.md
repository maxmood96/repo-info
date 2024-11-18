<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:b868a7403fdeca14b66fa988faf1af6fe2049b71b40247808e16a0910c145adb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:a293372120e023d002494569523755c6ccb05dd095a1d75569be6d8c9cf02666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72146954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d62d2db97807cca4022b03e325bc067e5f2e9765d1812562a8f91a7707c77c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Nov 2024 17:07:13 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Wed, 13 Nov 2024 17:07:13 GMT
ADD base.tar.xz / # buildkit
# Wed, 13 Nov 2024 17:07:13 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Wed, 13 Nov 2024 17:07:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6ec6a50996e602d49fc51121f062c3302737bed63feae7cdb949b8624cbb01de`  
		Last Modified: Mon, 18 Nov 2024 19:05:08 GMT  
		Size: 72.1 MB (72146740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a660f7519f75a84a13b8a20df2b16a0ecf26349cf8fb85d3afd31b6fdba706d5`  
		Last Modified: Mon, 18 Nov 2024 19:05:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:5804eb355ac184ef188ac7cc6ccca035dcb4b1337e9045323ebba0b40fa92182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80052703397e11e807c5f1728e79751ee7808361d9cce830f143a21bb887cce5`

```dockerfile
```

-	Layers:
	-	`sha256:95b47eaf76b909c7c20243b2ec489b17162e9ea1a6bd5c8f6847375af2faaa2b`  
		Last Modified: Mon, 18 Nov 2024 19:05:06 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:b868a7403fdeca14b66fa988faf1af6fe2049b71b40247808e16a0910c145adb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:a293372120e023d002494569523755c6ccb05dd095a1d75569be6d8c9cf02666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72146954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d62d2db97807cca4022b03e325bc067e5f2e9765d1812562a8f91a7707c77c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Nov 2024 17:07:13 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Wed, 13 Nov 2024 17:07:13 GMT
ADD base.tar.xz / # buildkit
# Wed, 13 Nov 2024 17:07:13 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Wed, 13 Nov 2024 17:07:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6ec6a50996e602d49fc51121f062c3302737bed63feae7cdb949b8624cbb01de`  
		Last Modified: Mon, 18 Nov 2024 19:05:08 GMT  
		Size: 72.1 MB (72146740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a660f7519f75a84a13b8a20df2b16a0ecf26349cf8fb85d3afd31b6fdba706d5`  
		Last Modified: Mon, 18 Nov 2024 19:05:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:5804eb355ac184ef188ac7cc6ccca035dcb4b1337e9045323ebba0b40fa92182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80052703397e11e807c5f1728e79751ee7808361d9cce830f143a21bb887cce5`

```dockerfile
```

-	Layers:
	-	`sha256:95b47eaf76b909c7c20243b2ec489b17162e9ea1a6bd5c8f6847375af2faaa2b`  
		Last Modified: Mon, 18 Nov 2024 19:05:06 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json

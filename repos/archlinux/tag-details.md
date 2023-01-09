<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20230108.0.116909`](#archlinuxbase-202301080116909)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20230108.0.116909`](#archlinuxbase-devel-202301080116909)
-	[`archlinux:latest`](#archlinuxlatest)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:4fd4f24aca01dc4ed1bd472b62a90dd93ff08102eb2c20a938b7383ab39baa0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:9167ec489f207c80e953375d3c5554c4846ef6cfe3869a536e710e2be6b405de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141900901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85818b4587a6ca0e318afb34128413ffcf0e357b3eccec38da07d7387df2e92f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Jan 2023 17:16:13 GMT
COPY dir:1f1f4c75a214a83f54b051bed4277bf05e6e77f94e4d15ab5141354f8551e948 in / 
# Mon, 09 Jan 2023 17:16:15 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 09 Jan 2023 17:16:15 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jan 2023 17:16:15 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e7df3e3edb8d7af5bc407f49d0006ae41775c2c769b06522aeeb27d7347c300d`  
		Last Modified: Mon, 09 Jan 2023 17:18:03 GMT  
		Size: 141.9 MB (141892940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4edb241ab322c11c79375b887fba1407f1baa652f9537000c2c18231a9bde4`  
		Last Modified: Mon, 09 Jan 2023 17:17:42 GMT  
		Size: 8.0 KB (7961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-20230108.0.116909`

```console
$ docker pull archlinux@sha256:4fd4f24aca01dc4ed1bd472b62a90dd93ff08102eb2c20a938b7383ab39baa0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-20230108.0.116909` - linux; amd64

```console
$ docker pull archlinux@sha256:9167ec489f207c80e953375d3c5554c4846ef6cfe3869a536e710e2be6b405de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141900901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85818b4587a6ca0e318afb34128413ffcf0e357b3eccec38da07d7387df2e92f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Jan 2023 17:16:13 GMT
COPY dir:1f1f4c75a214a83f54b051bed4277bf05e6e77f94e4d15ab5141354f8551e948 in / 
# Mon, 09 Jan 2023 17:16:15 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 09 Jan 2023 17:16:15 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jan 2023 17:16:15 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e7df3e3edb8d7af5bc407f49d0006ae41775c2c769b06522aeeb27d7347c300d`  
		Last Modified: Mon, 09 Jan 2023 17:18:03 GMT  
		Size: 141.9 MB (141892940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4edb241ab322c11c79375b887fba1407f1baa652f9537000c2c18231a9bde4`  
		Last Modified: Mon, 09 Jan 2023 17:17:42 GMT  
		Size: 8.0 KB (7961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:f4fc58a84ec2e29271102a33bcf3962d5c70552310aa591dd979da9685511b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:67dd2be8af0822f71718561c0bbf69ab8743b5ab82780f26c2492bc0e9defe7e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243271028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ce6eba7acb2d8cc10c3d1cfd10db85d4c82bd3fc0e96fc77fb79d23421c2db`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Jan 2023 17:17:19 GMT
COPY dir:a22a9b6e2ee82e5afa4d43150399a5e969d62591e3727d50e37258259c7af39a in / 
# Mon, 09 Jan 2023 17:17:22 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 09 Jan 2023 17:17:23 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jan 2023 17:17:23 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:3592e1daa93a821124e36d08301e7ef52e5b0959e2826a1c5ba237f1ae1d021d`  
		Last Modified: Mon, 09 Jan 2023 17:18:49 GMT  
		Size: 243.3 MB (243262433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07a0af1ce2a5e4c7582476c53b57847a46835008aaf9a7e5d6636a5cd845913`  
		Last Modified: Mon, 09 Jan 2023 17:18:13 GMT  
		Size: 8.6 KB (8595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel-20230108.0.116909`

```console
$ docker pull archlinux@sha256:f4fc58a84ec2e29271102a33bcf3962d5c70552310aa591dd979da9685511b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20230108.0.116909` - linux; amd64

```console
$ docker pull archlinux@sha256:67dd2be8af0822f71718561c0bbf69ab8743b5ab82780f26c2492bc0e9defe7e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243271028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ce6eba7acb2d8cc10c3d1cfd10db85d4c82bd3fc0e96fc77fb79d23421c2db`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Jan 2023 17:17:19 GMT
COPY dir:a22a9b6e2ee82e5afa4d43150399a5e969d62591e3727d50e37258259c7af39a in / 
# Mon, 09 Jan 2023 17:17:22 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 09 Jan 2023 17:17:23 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jan 2023 17:17:23 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:3592e1daa93a821124e36d08301e7ef52e5b0959e2826a1c5ba237f1ae1d021d`  
		Last Modified: Mon, 09 Jan 2023 17:18:49 GMT  
		Size: 243.3 MB (243262433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07a0af1ce2a5e4c7582476c53b57847a46835008aaf9a7e5d6636a5cd845913`  
		Last Modified: Mon, 09 Jan 2023 17:18:13 GMT  
		Size: 8.6 KB (8595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:4fd4f24aca01dc4ed1bd472b62a90dd93ff08102eb2c20a938b7383ab39baa0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:9167ec489f207c80e953375d3c5554c4846ef6cfe3869a536e710e2be6b405de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141900901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85818b4587a6ca0e318afb34128413ffcf0e357b3eccec38da07d7387df2e92f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Jan 2023 17:16:13 GMT
COPY dir:1f1f4c75a214a83f54b051bed4277bf05e6e77f94e4d15ab5141354f8551e948 in / 
# Mon, 09 Jan 2023 17:16:15 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 09 Jan 2023 17:16:15 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jan 2023 17:16:15 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e7df3e3edb8d7af5bc407f49d0006ae41775c2c769b06522aeeb27d7347c300d`  
		Last Modified: Mon, 09 Jan 2023 17:18:03 GMT  
		Size: 141.9 MB (141892940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4edb241ab322c11c79375b887fba1407f1baa652f9537000c2c18231a9bde4`  
		Last Modified: Mon, 09 Jan 2023 17:17:42 GMT  
		Size: 8.0 KB (7961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

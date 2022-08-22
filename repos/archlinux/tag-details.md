<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20220821.0.76637`](#archlinuxbase-20220821076637)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20220821.0.76637`](#archlinuxbase-devel-20220821076637)
-	[`archlinux:latest`](#archlinuxlatest)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:307381d5a138e224fb791fc60cdd2bced09fe29f6c6f0eb7f6f6ee96f9317d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:3e320259227a127cb7a5a8bfaf2f6028adf561f349f74d486c03fb0dbfd9c44a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136515821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371ccd6e42c56fc21d493fc6b7d5ec3737064324f91897c5fb94027f4918aca2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Aug 2022 17:20:01 GMT
COPY dir:8b10b6f1b41f4b5bc03fd85480e5d03df3759d57da2d6fb1eb834c09a009e2b3 in / 
# Mon, 15 Aug 2022 17:20:02 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 15 Aug 2022 17:20:03 GMT
ENV LANG=C.UTF-8
# Mon, 15 Aug 2022 17:20:03 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a8a7a6b18b0fac477b83b13f60275b367f888d79353c38bfd50ca86868ddeb98`  
		Last Modified: Mon, 15 Aug 2022 17:21:44 GMT  
		Size: 136.5 MB (136507730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3f0c8c4c3bf70fec51b852830248a133b374ed1d20e9392dc6ba0890648cdb`  
		Last Modified: Mon, 15 Aug 2022 17:21:24 GMT  
		Size: 8.1 KB (8091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-20220821.0.76637`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:4a4c2f757bd8473c80bcaeec267256341cd12f2ca7604878bf7bcec3b9e33e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:4cd182ccd16aa29003e6c2963990221440d2eb72983516a4f7a35ef100761c71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234728768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d1db2a0a38544bd41ddc8163bdf478df307112aa07cb0b228ac5201e8222fc`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Aug 2022 17:21:02 GMT
COPY dir:0b7c107cc59bfa9305fdfce0cfebac2c8fb4de067e66d0150a73afb5c526e7fc in / 
# Mon, 15 Aug 2022 17:21:05 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 15 Aug 2022 17:21:05 GMT
ENV LANG=C.UTF-8
# Mon, 15 Aug 2022 17:21:05 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a525ed39c6cedd07c843b01208d121a9523302137b9a615ca72fa5b13ca6a6fd`  
		Last Modified: Mon, 15 Aug 2022 17:22:31 GMT  
		Size: 234.7 MB (234719982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ad8fcc39a8473762fef6e5e43bfb6624e9f7da430fd7f4667078b002eedd28`  
		Last Modified: Mon, 15 Aug 2022 17:21:56 GMT  
		Size: 8.8 KB (8786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel-20220821.0.76637`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:307381d5a138e224fb791fc60cdd2bced09fe29f6c6f0eb7f6f6ee96f9317d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:3e320259227a127cb7a5a8bfaf2f6028adf561f349f74d486c03fb0dbfd9c44a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136515821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371ccd6e42c56fc21d493fc6b7d5ec3737064324f91897c5fb94027f4918aca2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Aug 2022 17:20:01 GMT
COPY dir:8b10b6f1b41f4b5bc03fd85480e5d03df3759d57da2d6fb1eb834c09a009e2b3 in / 
# Mon, 15 Aug 2022 17:20:02 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 15 Aug 2022 17:20:03 GMT
ENV LANG=C.UTF-8
# Mon, 15 Aug 2022 17:20:03 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a8a7a6b18b0fac477b83b13f60275b367f888d79353c38bfd50ca86868ddeb98`  
		Last Modified: Mon, 15 Aug 2022 17:21:44 GMT  
		Size: 136.5 MB (136507730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3f0c8c4c3bf70fec51b852830248a133b374ed1d20e9392dc6ba0890648cdb`  
		Last Modified: Mon, 15 Aug 2022 17:21:24 GMT  
		Size: 8.1 KB (8091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

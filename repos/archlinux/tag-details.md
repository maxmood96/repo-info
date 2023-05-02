<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20230430.0.146624`](#archlinuxbase-202304300146624)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20230430.0.146624`](#archlinuxbase-devel-202304300146624)
-	[`archlinux:latest`](#archlinuxlatest)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:f88544eecbe2b463e8e74c68241ef7ce0a5340fa93395abc05d4083036ece9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:595a8241225577ea4b5f59525a90162a605dae30a9ab9407a458e6464a644cc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143087297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131484c87d34b86f8fee051730fc272af52cdf601088db8bfcdeafb25471ca04`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 24 Apr 2023 19:20:10 GMT
COPY dir:711e487feaff3aace3eed1534ac4c28ec247530f292c0e5fa7e5e5a7c9b30714 in / 
# Mon, 24 Apr 2023 19:20:12 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 24 Apr 2023 19:20:12 GMT
ENV LANG=C.UTF-8
# Mon, 24 Apr 2023 19:20:12 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:0b6e80fc7ef7ba341bd8106e1a07e9d326554fc5d43f17a5b12231f517f2b692`  
		Last Modified: Mon, 24 Apr 2023 19:22:01 GMT  
		Size: 143.1 MB (143079342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be24523ca07449101615d90f4b4ebb99892f0ba2296b98cca8c2b086ca5ae0d7`  
		Last Modified: Mon, 24 Apr 2023 19:21:41 GMT  
		Size: 8.0 KB (7955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-20230430.0.146624`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:95c40214ce1571caa314f1c93edc15c2713793e9d07505d091d7eafc3f9f9118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:4f673dd1fcb0af245d2bf7c20bdd1b5bd55c2af3d7ac8debeb3f13ef76c14b19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246155374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c23c945367b182e392cf5fa3ad19d324b08c9d32395d4466d9b13a225b451e0`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 24 Apr 2023 19:21:19 GMT
COPY dir:30fccad4db02a015dc3df87dee72c3888f4204c039a92c8a0fcb1fa6db65e609 in / 
# Mon, 24 Apr 2023 19:21:22 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 24 Apr 2023 19:21:22 GMT
ENV LANG=C.UTF-8
# Mon, 24 Apr 2023 19:21:22 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:0d8eac793e0eb6945ddd359a1ccc66f9ab275c17fb398b5b36cb48151d73ffc5`  
		Last Modified: Mon, 24 Apr 2023 19:22:45 GMT  
		Size: 246.1 MB (246146666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f0e5644a5f513d342d9575c950b326f55e81119988d388bd703082ce2a2af2`  
		Last Modified: Mon, 24 Apr 2023 19:22:11 GMT  
		Size: 8.7 KB (8708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel-20230430.0.146624`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:f88544eecbe2b463e8e74c68241ef7ce0a5340fa93395abc05d4083036ece9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:595a8241225577ea4b5f59525a90162a605dae30a9ab9407a458e6464a644cc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143087297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131484c87d34b86f8fee051730fc272af52cdf601088db8bfcdeafb25471ca04`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 24 Apr 2023 19:20:10 GMT
COPY dir:711e487feaff3aace3eed1534ac4c28ec247530f292c0e5fa7e5e5a7c9b30714 in / 
# Mon, 24 Apr 2023 19:20:12 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 24 Apr 2023 19:20:12 GMT
ENV LANG=C.UTF-8
# Mon, 24 Apr 2023 19:20:12 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:0b6e80fc7ef7ba341bd8106e1a07e9d326554fc5d43f17a5b12231f517f2b692`  
		Last Modified: Mon, 24 Apr 2023 19:22:01 GMT  
		Size: 143.1 MB (143079342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be24523ca07449101615d90f4b4ebb99892f0ba2296b98cca8c2b086ca5ae0d7`  
		Last Modified: Mon, 24 Apr 2023 19:21:41 GMT  
		Size: 8.0 KB (7955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

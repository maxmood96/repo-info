## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:107b4701efe5c4b336d9f47b9df7c4eb6fb0fdb642b3662bab2bf5b93a83cdbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:f3ac43095dc15e59d7f57b201b66ef2c496386bb1e4ceed8bb86bb05aee17d01
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51262007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53da2ee1ffaec303e7fb884f50d27bbd585c234aad69c57d34e28c8a3f3c39eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:22 GMT
ADD file:3b158c11a921c91aa3cebf5651e59c21fe59da295d3edc56147fefaa760329ff in / 
# Tue, 25 Oct 2022 01:43:23 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 01:43:26 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3721e3e259583b8b78cfdeb51a553c189938925b902bceaa1f4f92e837fb9a23`  
		Last Modified: Tue, 25 Oct 2022 01:46:52 GMT  
		Size: 51.3 MB (51261783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85aa58c44af92ec3fdeaafb16bc38ebd1b2b94a81f22e0176d091f9d4692a1d4`  
		Last Modified: Tue, 25 Oct 2022 01:47:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:36615e452b4f44177192c68c333c0c1b5c21f1101ab6ba36629410618b8eea7b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50178599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc97d0fc184b6e53b8ca0288964311e9742ddb55277388e48de34662bc3326f9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:05:47 GMT
ADD file:226ff5e5e8066a03822e2865c6f72c554de94710c5664ee8bebd127d8aa32388 in / 
# Tue, 25 Oct 2022 03:05:48 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:05:55 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cff7bd795d206b13b585de0da179a0c9616a5278eb7d74a97c97746085567403`  
		Last Modified: Tue, 25 Oct 2022 03:10:30 GMT  
		Size: 50.2 MB (50178371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e499e2dcb9010f9acad60f243efffbd839fb7ea80e50200305909a787f52b04b`  
		Last Modified: Tue, 25 Oct 2022 03:10:41 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:f91fbf5496c210edea7382c9aad9523d5725d5160873df92c2c2249cd7d45251
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47997718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe6d4ccecdbc2fbeb134baaf8936290e3eae45bb1eb268264747ffd6ef9b3a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:13:33 GMT
ADD file:5ab258b263409915dc783ead8a52ab1b91eb5dce1d1cfcadf9234ce60b961a00 in / 
# Tue, 25 Oct 2022 03:13:34 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:13:40 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ea7580981dc6864bb654386e5ab137ff58cf1c1fc085457388952e4e7debac2c`  
		Last Modified: Tue, 25 Oct 2022 03:19:57 GMT  
		Size: 48.0 MB (47997492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31820435026ff97b5a3ce2d057c5e2a0b9cdb36e9161077547e4e82ed56629fb`  
		Last Modified: Tue, 25 Oct 2022 03:20:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:de7edda3869da606bef00abf3e698b8b7c74b963910ec8cd4382b44514b66eb0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52980614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5e0a2e6106379cee018cd6be71b75d67d9ed1c1d623c96262fb30e004f4a0a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:00 GMT
ADD file:269c8bec4871d84b9133706a2f391209619d53c0bfa56121c740757cf5798fcb in / 
# Tue, 04 Oct 2022 23:44:02 GMT
CMD ["bash"]
# Tue, 04 Oct 2022 23:44:08 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2debf9e7f23054c81a936da9b01c5db9f72a55d4810f7bf0e5641bd1748d90b7`  
		Last Modified: Tue, 04 Oct 2022 23:49:11 GMT  
		Size: 53.0 MB (52980389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a707182dfba1c22a9f7523d22112a259d318c0b9d2153746676c30d25446001a`  
		Last Modified: Tue, 04 Oct 2022 23:49:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:7261b9329912d7ad6952d5864931afeb44f90b15598d2d1f0716f81277859524
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52224896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1991442b86061cddff356e9fde3201fc3e166fe9b1ed5797b97b7f7f3772c7fd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 02:21:54 GMT
ADD file:f47fc1d53965bb08e38b482e78bd79e3cbeecc53e586ffd88bff0e6fed0a1f3c in / 
# Tue, 25 Oct 2022 02:21:55 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:22:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:11f88873ba86e184f57ba78457d36c4f22e16eaffb9c293964adc7905e18bfe5`  
		Last Modified: Tue, 25 Oct 2022 02:27:09 GMT  
		Size: 52.2 MB (52224672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2721d0909811f42d3b8fddb3d6a28f6802dd1335930f4e2ae672aeb4923bd1`  
		Last Modified: Tue, 25 Oct 2022 02:27:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:b8d62a950ae039a77a8df9396ee9391ec1d974a8a98f11b4858ac7691ac377f5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51259868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2424fd1df84bc6f1558f4266ea4cc4f15b15da7ba1918ba8f4fd47b4a1ce81`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 04:37:41 GMT
ADD file:a1c9e78f0a426fb245eff7a26706bf5500c9afba4a267812a4b2ec71113c371c in / 
# Tue, 25 Oct 2022 04:37:46 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:37:58 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:132042cf7d4760fcfc85f263dd04337e03e7c8105a5e98f7b530ac7170f31a8e`  
		Last Modified: Tue, 25 Oct 2022 04:45:25 GMT  
		Size: 51.3 MB (51259641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5c5935e5208dc08b0a72b2f6e72a45f13620ddb56dfd0a9269d22cdfd0fa6b`  
		Last Modified: Tue, 25 Oct 2022 04:45:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:1d124271323c8f0d72ab769cfe92bcb34347ae5c8269c5d878942c1356845741
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55339028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701c3613a2606a64318e6c0a085a66d4ea79f1aff63ac13b836c68de9cb87f63`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:12:50 GMT
ADD file:1f55ca9aa64d69398e6bff99fdfd63dbf022ecefc46450a6fd32ae46e9718557 in / 
# Tue, 25 Oct 2022 03:12:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:12:59 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:264fa02db63011b604885c7feecaeb78fbee4ce4d8191fa5050f4fef88c74001`  
		Last Modified: Tue, 25 Oct 2022 03:18:00 GMT  
		Size: 55.3 MB (55338800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3855318dde18ac35b01a84f8fbb8667e7b4089ffd2ea81f973ab7c80f880b98`  
		Last Modified: Tue, 25 Oct 2022 03:18:12 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:46f681f24aec1a69ea11dd21ef7e0c45d84809ae3a593ee67a51069f9ba7c57a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49578725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39feb8386d979253006a1b6d4e549b75b5ea104752015308b5edadd309713bf4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:13:56 GMT
ADD file:92a462945d4b32c30f41478992b9ab30d452ac37b0ecef64e2325e4e99296ea8 in / 
# Tue, 25 Oct 2022 01:13:58 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 01:14:05 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e544dc28605cf962b36f5ba4703f824c022460d64f8973e49764cd76163df5ff`  
		Last Modified: Tue, 25 Oct 2022 01:18:08 GMT  
		Size: 49.6 MB (49578501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2496bacf19fbe6379edbe13aeda89ecfc123f3050d0c3650cf9458cb456b1293`  
		Last Modified: Tue, 25 Oct 2022 01:18:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

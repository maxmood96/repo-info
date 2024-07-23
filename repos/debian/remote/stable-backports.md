## `debian:stable-backports`

```console
$ docker pull debian@sha256:822b594b33b05472a5aff61cf663fd8b18fbc7eff4ef2421fc9e3cd4c86bbaa6
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:e96dd2c734871899fa7cbe1be63080011b296abc124db15fdc09846f8a70be7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49554296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c9bd39ab76d48f675eaed5b53d5d5ed7849636f463a64c2024e4c984b6808c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:26:16 GMT
ADD file:213de1af48b6d18cba944529abd780af1a9ebea6f32558e442e88a1521fcf01d in / 
# Tue, 02 Jul 2024 01:26:16 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:26:21 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7752f0ba46cc8263552f036c7e8e5194360d5d56286b9c8fda5416fc84a9bcff`  
		Last Modified: Tue, 02 Jul 2024 01:30:43 GMT  
		Size: 49.6 MB (49554074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4a3b08964b0ca066855fed0a58d8c1995ef686901afb4caa56a22afd6ea479`  
		Last Modified: Tue, 02 Jul 2024 01:30:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:dd43ce25ca256375a7f692a1a2076d3314896907f301b0da2a8abe66018464c0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47320560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f955c02d3f196b51f9d5410c5c11e0019a350b05e2101bd84c9c6b30d9d7eef2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:58:25 GMT
ADD file:96c16e2a5b0f354a34704f6c5349c0b886f6bcc9873b497a6798c92d99d6c083 in / 
# Mon, 22 Jul 2024 23:58:26 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 23:58:31 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:46078a3d0c8b8370839d00725d49531249f17c1b2cf595efc2f337d0f0364cd8`  
		Last Modified: Tue, 23 Jul 2024 00:03:31 GMT  
		Size: 47.3 MB (47320337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeff9534d6b15c8f85b828474c42dc9206ebc1ae47406c43fd3403b9bdb6ab71`  
		Last Modified: Tue, 23 Jul 2024 00:03:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c9bc6305b29e3fc541cc101cba3f840690f2f5492c155baa7ba8dcf944cb34e2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45148330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7575758ee6b4d85dd19ee08f228e5755512e27b5b78b7220d3d4e8915e810743`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:04:23 GMT
ADD file:18ea02442792ee6aefc5884d5bb55a8ac9d30913a2b1c087bfff6fe148ec83a2 in / 
# Tue, 23 Jul 2024 03:04:23 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:04:26 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5dadf66fe55f94902a960b6159358650ac5b25dc710db75ade114fa6b6119df0`  
		Last Modified: Tue, 23 Jul 2024 03:08:53 GMT  
		Size: 45.1 MB (45148108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c0a6adba8f1e1eb96b7cb4cedcbb9f9594b21386ff0fb4c4ed49a058e4c719`  
		Last Modified: Tue, 23 Jul 2024 03:09:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ecd62c9b532c062dbd1cf8ebcccc67a912f2bda1b4b5b7d8ae1c4c13e334035a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49588664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c8e17124222006db131839841085caccc3aed16b84198420e1f3feb34f586d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:26 GMT
ADD file:fd907743f6505b73bcc7d3b66ce062008bff02f12d1b59a8f272641290c5e474 in / 
# Tue, 02 Jul 2024 00:40:27 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:40:30 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dcf4a1279be907cb629c2e75ab78e4c71a46e913164b2ffd9e497af49b3546e5`  
		Last Modified: Tue, 02 Jul 2024 00:44:20 GMT  
		Size: 49.6 MB (49588443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4d95fdf6f87e7379db649999a4bca4b981d6428f04fffceff784d6a32008ef`  
		Last Modified: Tue, 02 Jul 2024 00:44:29 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:7be0a335f2ab553d276896786bc86b58186b8918317ce229994f1c9cda964e82
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50579641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40ecfd30493fb670b2daa34b23e2a588c105ac4f15a4c0c37c0d479f72adaa6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:55:27 GMT
ADD file:7ee44e4e909002824af1c45c44d7cafd5af1a66abc39256923fa97bd14dc1516 in / 
# Tue, 23 Jul 2024 03:55:28 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:55:32 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c43e1f7c4cc5aca896ea2c237eb1f1c2a85ec7b91096881a02e6cf3e67d7fa3a`  
		Last Modified: Tue, 23 Jul 2024 04:00:02 GMT  
		Size: 50.6 MB (50579418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b85fae372ea8df8db55bd4cedfdf55cca19825d60fdb8272466bfa0be857084`  
		Last Modified: Tue, 23 Jul 2024 04:00:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:2e3c45a01a33ff6e5f49849c4088c001952c941012f13c8a6db81e0bb1deb7db
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49563444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec24c5f5a1c6ee677b0b457fae91340b4d114defdeb5a2a9b618af52e76e719d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:42:11 GMT
ADD file:98ee38d669ab2689eff78a0f4e38fb68aea26b2a26bca8a2f224afe6acd6299f in / 
# Tue, 23 Jul 2024 00:42:17 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 00:42:32 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8ae4b02c4376ee5ad3446599305898029cd4f6371935f5914ea3a14dabe13488`  
		Last Modified: Tue, 23 Jul 2024 00:53:43 GMT  
		Size: 49.6 MB (49563219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da512a368fec55977d4dcf9c08169feebb40552020ebc0f9b9d8494e42103c4f`  
		Last Modified: Tue, 23 Jul 2024 00:53:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:88577c7d71f5b835003555248c68d7d88e6c2988e681c983e002f576941afce6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53557241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b1aa353f14e39a27d4e8fb21bae67f95fd9571a70d9828cc96aaada0b83d63`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:28:25 GMT
ADD file:b2bbe15ba9e02c32c973856355f1fba8463b073ba226f69d4ab573dfa5ebbde0 in / 
# Tue, 23 Jul 2024 01:28:28 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:28:33 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0f25680a849e1096d5f2dff5839c35e229e794088a56a55315ee898ff4509f38`  
		Last Modified: Tue, 23 Jul 2024 01:33:19 GMT  
		Size: 53.6 MB (53557021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18aeac7dd75c4f8835741a12ed1e1ce69d28079dfae0e3de2b865f4295311537`  
		Last Modified: Tue, 23 Jul 2024 01:33:27 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:11c5795d21faa712685feffd79d9638a7e6bb0cd5e6ccdffde1ff60fb54d5595
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47931687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7a3fac6c97a2ac6267bb97d0e53b87b33b4488e29abb4a48ae5ffee3fce806`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:29:41 GMT
ADD file:7a1254313ec9425e7f350b108fb0a8a3bb331e557cc36b9ff187995ae0657d1f in / 
# Tue, 23 Jul 2024 02:29:44 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:29:52 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0eddd7d6f2cdff4ec861f6d5870c5d4efaa8e814d4f6dfe470912340a2587a39`  
		Last Modified: Tue, 23 Jul 2024 02:34:12 GMT  
		Size: 47.9 MB (47931465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704543198ae96483498f4c90b84256a125b5116cc81567a9c81503a0948ef72c`  
		Last Modified: Tue, 23 Jul 2024 02:34:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

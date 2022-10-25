## `debian:rc-buggy`

```console
$ docker pull debian@sha256:cd01b5d4b1f8bb9f31f455bc268e6f59e7395bb52b5ee1c3cc46fd544d887a1c
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:ba560aa422c54c440912dda300abe4fe299a61ee2739ef4f632a24cab827a810
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50641454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:117ea039b9c5209f2b9978e52bed53c34d34f66ace5c5af857e662fc163cd14c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:41 GMT
ADD file:635f36e1a46e6c28b2a6ab0637cca9e47837c3547b17916d1dbb2595fbeb0821 in / 
# Tue, 25 Oct 2022 01:44:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 01:45:53 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d90f8b044e56f2589b41d1fe9b249b85bde027855731c6f512f0f9401c99e68d`  
		Last Modified: Tue, 25 Oct 2022 01:49:42 GMT  
		Size: 50.6 MB (50641226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a01cb3408bd32f8e1becd0ff9a98c693f2466f55cc745fa93ea1d980b25730`  
		Last Modified: Tue, 25 Oct 2022 01:51:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:1a40b18858a3ed28806d71e738f19f72120ea79a742523dd877e45f28f43b0e8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49579113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04eabfe85cbbdfea5427953b9ed26ba112fb067fb541ae113dba7901543cd053`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:06:50 GMT
ADD file:829f8e96e527611e85aa710b19c01c75a4760a27c651fb439f8cdb5609db64aa in / 
# Tue, 25 Oct 2022 03:06:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:08:37 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:513ea4862e78a8cc07ed6d320f10e746ca770eb039dec1548c31a9de19d1f7ce`  
		Last Modified: Tue, 25 Oct 2022 03:12:19 GMT  
		Size: 49.6 MB (49578888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc4d71420503ea65f44b1cfd3af823f6c9b4b70f947dc46f7e7c08a3e86890a`  
		Last Modified: Tue, 25 Oct 2022 03:15:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:b76a8579e94bca5f9d4388ea9f9c42398441d58c3e5c616c5d583d0a6f5187d2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47411792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cbc0c4abd5a7f4f9062439ecdbbc25388c2bcd162dbfcada76300e1a43c312`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:15:36 GMT
ADD file:072a31b7cfe6ee4e4a8e0832259c68a602abda7e1a6682cdcb28eba7f0705383 in / 
# Tue, 25 Oct 2022 03:15:36 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:17:24 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c9040ceaeef63642a4aa2653b1350e028be0db975aa9a23c7e441aaa7dc5a11a`  
		Last Modified: Tue, 25 Oct 2022 03:23:25 GMT  
		Size: 47.4 MB (47411564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8047e22139f1614ce4cfd8c5cbad1b5e613bb10773ee5166e2c448361b84cb7a`  
		Last Modified: Tue, 25 Oct 2022 03:26:08 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6a0d3170dcc081fdf9280e8a03f983f36e41addea5005abe8ded52891c25f211
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50643960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99f9ac596ca22c153b6e443ea3d15e9a22b28ec021273eb8ca4fe0d5a1e1e87`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:29 GMT
ADD file:6a2d69a5a731490271c915d99634a89755f7236ef56712924ea061730d8552c4 in / 
# Tue, 25 Oct 2022 05:46:30 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 05:47:11 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:63a396bb133ce57141398b6c6d776ce17e3e973085b5a1b746d76407240a376a`  
		Last Modified: Tue, 25 Oct 2022 05:50:38 GMT  
		Size: 50.6 MB (50643735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea77cd7536972f81b86e21cac712f20d14592ac5b3d20c76d4196404e7f4e7e`  
		Last Modified: Tue, 25 Oct 2022 05:52:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:6f950c15b49d8fa79bf94abe7046dba88febdc84575d227be715f1b23bdb5696
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51625546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b332cd02bc18486984471b0c6457086d2385a7dc1c1265d3df01ca0bbc3e09`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 02:23:38 GMT
ADD file:80dabb60a37b1d88f3750adb85c9e159d00b55293f70ad93512f94bd3cfd99bc in / 
# Tue, 25 Oct 2022 02:23:39 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:25:13 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:367799113badd94b9683087d6086436649a1fb7127698c42b0d730f5bbedcf86`  
		Last Modified: Tue, 25 Oct 2022 02:30:22 GMT  
		Size: 51.6 MB (51625321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac0107c6ac33d9c99bbe6b83733d6f8cb51171013b5c3bb089b38ab4f50d1e7`  
		Last Modified: Tue, 25 Oct 2022 02:32:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:dd22b41645d0d485cbc68535937c1af3d6e257a2a1a76fe7372fe8248331d546
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50901762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57d3882e69c486a2063145f2515ac9c41348eb48ee1abccb3cf150247235c6f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 04:39:58 GMT
ADD file:da7998228f2661dd3490a7bee754b7aaed5cf07ebe582e97b32c3985ad0d283c in / 
# Tue, 25 Oct 2022 04:40:04 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:44:17 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c2275c195d2a35a07739822efcd752aad4e9580392e4129bbac1f6cfe608ee1b`  
		Last Modified: Tue, 25 Oct 2022 04:48:12 GMT  
		Size: 50.9 MB (50901534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce8f285f1f02a7dc42bfc0cae9f9c6b8989c736d029f15dc808bfd29ea21982`  
		Last Modified: Tue, 25 Oct 2022 04:52:49 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:a4bdaa071f51ea9408f08af93d3a660926aff63aeeebf2b3eff1f1b2ff8a108d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54704944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314cce142adfb2c259db653ad2754fa311523124c048c50e87032a4140a35d5c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:07 GMT
ADD file:6e9efd6bb77c835520332c88cb412f38f0d8573ec3347b090b77965e17131780 in / 
# Tue, 25 Oct 2022 03:14:10 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:16:23 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:7a3962f6ac5b86fa159789ea1e9241ecbb956b3223e8312f7d92d7fbb8bf5485`  
		Last Modified: Tue, 25 Oct 2022 03:20:03 GMT  
		Size: 54.7 MB (54704717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea915dae8e4e8fc1d71dda087fcf35607312c2e52a161bf9a3b775326ea7831`  
		Last Modified: Tue, 25 Oct 2022 03:23:17 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:e5820ed8d0cb96d731ae6fcaa30387956dc6a3e1dc6c0d3ab3422794874daa85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49013200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f1782aac87e5db1bf4bccca5a0092fdb518efd3ec8cf43bf398ee3edd0bb27`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:14:54 GMT
ADD file:7dba2ae439c9f5da3fe962e867cee94eafc0b12a74939e13fdf987965ef8191c in / 
# Tue, 25 Oct 2022 01:14:57 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 01:16:40 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1430653806baea9ab2928a0d226c10ba8e7bf4b9b93398f9082ba16edfb2d4b8`  
		Last Modified: Tue, 25 Oct 2022 01:19:17 GMT  
		Size: 49.0 MB (49012977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c1767501079f5541e1767fe7c7ad7d6065fa06797b104712dabc65166177d6`  
		Last Modified: Tue, 25 Oct 2022 01:21:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

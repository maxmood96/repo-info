## `debian:buster-backports`

```console
$ docker pull debian@sha256:352c83eb9e1a422a210076e443ebfe3fb592b56914f837456960ef727400b103
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

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:8377585b800bbca237f95efd697dbae4a63d073d6344413711e2c4e8d552ab1d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50437359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:287f26fe16e4b6eb19e9955f7974924fc0aef44f9686bbc4599ca8649aac7cf8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:53 GMT
ADD file:be998d04a8927e9c4b105995e3b9d6800ea798807389f7c5921c0f4774328e21 in / 
# Tue, 21 Dec 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:22:57 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9b99af5931b39ce167150ad668cfa57ddf7664697be9996cb7e0e6aebbf05843`  
		Last Modified: Tue, 21 Dec 2021 01:28:07 GMT  
		Size: 50.4 MB (50437136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a8632baa66ce489c1c76cb8553890c7a4ce215c5cfea67f0d827348e5c9f14`  
		Last Modified: Tue, 21 Dec 2021 01:28:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:791e5d0fd3e151e72cca4a4c1f45599ea137956fe3a398b8257ce63fa2ce08a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48154593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6543fdb39e5f7c57c6e818673b2f07eb0ea660999ef8f9d373820dabdb01c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:50:59 GMT
ADD file:f13b1e11ddbb56252b3e6e03b983781bdb18391decd8e7fe849d9ef411ee19d2 in / 
# Tue, 21 Dec 2021 01:51:00 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:51:15 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f72054d57c0f356b780c117a8b1bcec66a89bbe239433df38bd1177b987f011d`  
		Last Modified: Tue, 21 Dec 2021 02:06:39 GMT  
		Size: 48.2 MB (48154368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b738d060b3a5bcbadef2470d1f3ecf33a6ce8c04b9ed5a5549c1184acc437d`  
		Last Modified: Tue, 21 Dec 2021 02:06:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:56483d416e540676796779a0abce6b3fd380519cae3c04aca6015885f0072eab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45918328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01cf553285d577a739d453127721cea312f1c849cf47617c843be13eae30ce4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:00:17 GMT
ADD file:36bf5b8bdd9066b06cc35d26df3f4dad2b1cbcb41985b85f070ed97a3e85f8a9 in / 
# Tue, 21 Dec 2021 02:00:18 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:00:33 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:328389035fdd79ece4f520541a84b3de974050fe012ed1566da6b869dd34ea29`  
		Last Modified: Tue, 21 Dec 2021 02:16:11 GMT  
		Size: 45.9 MB (45918102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604109bd4d568f3b066967d9c5ec7267c8c1998e00303716ae10374b83379886`  
		Last Modified: Tue, 21 Dec 2021 02:16:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:bebbf2b66e6fcf2f8404d7aa1440aa1dabef966a73cbd9c43dbcf8d1a9f90f73
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49223366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f9c32f364c01fbf45f4f7af55b7fb642a20beb94466f8eb8135d8e4a218b22`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:34 GMT
ADD file:73bd5e773b257a6ea5d29845b2b112ebce468878a9467e7c0fe61c69994bb47f in / 
# Tue, 21 Dec 2021 01:42:35 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:42:41 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:741eb94195433e00f9799629cc66740c97d607d6f3ed207e5738995897c52959`  
		Last Modified: Tue, 21 Dec 2021 01:49:16 GMT  
		Size: 49.2 MB (49223144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ec21062ae1bacebe036938aec4d637240135165d590aade39f0b245bff692f`  
		Last Modified: Tue, 21 Dec 2021 01:49:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:a1f36cbad02fe2f2625ab07e2b1f4368cebdfe39512c745fcfce8b501d1b7178
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51207989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1842d7f4a73acba4bc19601ef7a49ac214c36c2b50d88204e8647927e0b40a0a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:40:24 GMT
ADD file:4e982be228380a8d7632e31f19e39ed55ee76fb1db32130fa88d696904d6acde in / 
# Tue, 21 Dec 2021 01:40:25 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:40:34 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:342b01a61e0af68dc09681004efdfcf66d0443632988d6f247dd7b34bc18b1db`  
		Last Modified: Tue, 21 Dec 2021 01:49:14 GMT  
		Size: 51.2 MB (51207766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3227714e683b3fa5de430d865638d7b05157ead4eee2626034a5b15647d38d9d`  
		Last Modified: Tue, 21 Dec 2021 01:49:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; mips64le

```console
$ docker pull debian@sha256:e7da13d54f65837b57ece6a272d32f204b5eac9b769a63ba6145fdb757dc838e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49079856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74389a68e3ebe5e38c715edb995eb755bd7a890472ce56a11d8cfdab5cc75609`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:09:33 GMT
ADD file:f955c235588264a795d4f22cd0b6e343cc7b64c6c545c65ca1634fe8a1c664a1 in / 
# Tue, 21 Dec 2021 02:09:34 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:09:42 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c8948017ab035edb3d02daf180d7bc682ff63bc2ed281155da62060a3202c19b`  
		Last Modified: Tue, 21 Dec 2021 02:19:09 GMT  
		Size: 49.1 MB (49079634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042a97c4f52e3dcf31492f19626e1d57e6ce53262827e63cc08cd15ae8d18259`  
		Last Modified: Tue, 21 Dec 2021 02:19:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ce89b300c599ab1739a4a93c3a506576c13db4acbd2ef3a0f458ed4fb08b9278
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54183993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4910983e9e3fcb450d706d9b5bdfc352fa11668068ef4c7048fa70376a191bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:20:42 GMT
ADD file:8056891c6381c1ff352984edda0a56834740c6dd16fb5d53cf6b6c2b4b3aad81 in / 
# Tue, 21 Dec 2021 02:20:48 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:20:59 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b07d0e315feadfc6b984834ea9bd062e7d0b75d60ca9fe83ac8516760c195fc8`  
		Last Modified: Tue, 21 Dec 2021 02:29:46 GMT  
		Size: 54.2 MB (54183767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d9458d0446cb3c6a034bb6ec147a6f8e64e401a6e934584db383d8f8adb77d`  
		Last Modified: Tue, 21 Dec 2021 02:30:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; s390x

```console
$ docker pull debian@sha256:0e94357714d925c57008c212d10d1bc6110615574ecf04d2868055af9d25b541
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49005665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356b73f36aee3ff7b27e6273d470a0f76ce040acc7aa3a36a9b67bed5a83dad4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:39 GMT
ADD file:def95923e24cb6059ca87ed32edda32704debf3cdd64fb6c50e156b7528dce0f in / 
# Tue, 21 Dec 2021 01:42:42 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:42:49 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:506fcc46017f6aa41ccd20bb2ea02ae7698abd4e52104cd94243f7aa64ce5ee0`  
		Last Modified: Tue, 21 Dec 2021 01:48:31 GMT  
		Size: 49.0 MB (49005442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3d3c9cc1fc56ba5b1bb1e204b57cedcdd204158db3d283659ddf89fddbf16e`  
		Last Modified: Tue, 21 Dec 2021 01:48:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

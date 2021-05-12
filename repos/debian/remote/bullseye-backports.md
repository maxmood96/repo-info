## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:5b3aae925028af1b1447c4117cf55b668cfcc524d39e3a9023fdf571494fb16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:eb9299037c3ff065f6014c3baaa8b6f879ef0d1392deba305142b5ed01768712
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54897923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2aee8cbed209510278da65c0d9b0aa40e88c4322696122cde898929063afd5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:20:32 GMT
ADD file:22ed184e421fcac775f322850c24589ef2e78ddd12900395d44b2ea74220a62e in / 
# Wed, 12 May 2021 01:20:33 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:20:37 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ad4592a9cb6deb788f794c7bc60f66d77280e79869f13e9eccbf34e1d381b95d`  
		Last Modified: Wed, 12 May 2021 01:26:05 GMT  
		Size: 54.9 MB (54897696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef3e03180674c28c94c5942f08a4f896f935e8bf0bcbaaebea210827b7ee7d5`  
		Last Modified: Wed, 12 May 2021 01:26:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:ee39ab98ae86a8e2006dc5af052a7005d8c85564e26ce70388552a04448e241d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52439413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c423989da7abd279da4644ded744870b549c71f7eab5034f043c05ddd07daa6e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:53:46 GMT
ADD file:776704b0dea7e9c9856d53c5db99eb2cac12414a59e66258c549cd32602f5f15 in / 
# Wed, 12 May 2021 00:53:53 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:54:10 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4470c8b9361b9718aac07fcf9a711d40000613ef3e0f694e3da9f5ae091dd9ff`  
		Last Modified: Wed, 12 May 2021 01:08:50 GMT  
		Size: 52.4 MB (52439186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6acf070fdb4b5cca0c0c8b1bf9dfb800da6549350c5c0c112c74f1f4bd1f16e`  
		Last Modified: Wed, 12 May 2021 01:09:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:edb9541f1a999143cada6edefadf408d0c9d6709de550317b9af2a7c3f4988e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50101946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c88b14e26ec221a9b5d17d0f54fb2f7faa18f4957062ff28492ff579c0b287`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:00:23 GMT
ADD file:8ed6f13e7955c981e57f2e063b7bfca16927ded9fed3cbd231923f2fc092555d in / 
# Wed, 12 May 2021 01:00:25 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:01:04 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:50de689ded7920797496a1e9f831f07c907224f7c629bb02a03a96ae30d367de`  
		Last Modified: Wed, 12 May 2021 01:18:10 GMT  
		Size: 50.1 MB (50101718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e2df8434e6e96713c039fff0189646b726b36d6b6f5aff52955a4d928270d6`  
		Last Modified: Wed, 12 May 2021 01:18:17 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:54dbf5cccdfcf8fbc3304e53779bd5ab2ea98a08b09caaf78d9071db5125febf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53582772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81108afa1308e6a62aeb065a14b45ce75668d7dfcd272cd3a7d85cdcb7474931`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:49:45 GMT
ADD file:ebff33fc47ad7105db0adddceb61f0a2042e3c68d687b2d2c7b6b3f500274d6f in / 
# Wed, 12 May 2021 00:49:48 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:50:05 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d62e7e7f99652da0bce9de07c43607f6addba9ce6fe0e71326f752a74878fa68`  
		Last Modified: Wed, 12 May 2021 01:01:01 GMT  
		Size: 53.6 MB (53582545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0375ef19ba1de966ed70cb7641c8540d0d5bd92dbd197e80b45f2633c3a73a8`  
		Last Modified: Wed, 12 May 2021 01:01:08 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:eca3dd48e7350c8d681752efb7e1aa79bb76407abebab8fea8a8550cd9b490d8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55909643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba95d75e3daac32772fd1830821a8fd6878af65e529014714167cc303eafac0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:39:01 GMT
ADD file:ceaf0ce8046ef8c7fbc7c677196bc18e90f63d579058f7d2979a7346253dbb7c in / 
# Wed, 12 May 2021 00:39:01 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:39:07 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:09ce53911ae087d5d7231ced04f50f7ae7747f7ef80c2d4b4090d0cc6617c7d2`  
		Last Modified: Wed, 12 May 2021 00:45:16 GMT  
		Size: 55.9 MB (55909415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7b849ff2866bb3d12e4a921e5c293167760536cd5a3a165d525157c4a90a11`  
		Last Modified: Wed, 12 May 2021 00:45:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:931d64e3fec92ec77b650fd78daee0baa719fe27f6b636ffa775cab005cea1a0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53151992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e4d3830c94e909e0efa449eee65ab0d06d237d7dcc42698549c39fb49a1235`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:08:19 GMT
ADD file:922c33f98e349794ce38a7ac625e9bc65d1f794fd84e1f2ab7c83977a0de89af in / 
# Wed, 12 May 2021 01:08:20 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:08:29 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:24f0fe8ca8f36e5a839c5b70a3bbaed367aa46cbcc14b99b83c845ad805743eb`  
		Last Modified: Wed, 12 May 2021 01:14:33 GMT  
		Size: 53.2 MB (53151765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1a562e04d75932549d78c7a32a4c2b907d5c582fa658dff230f2dae3261a49`  
		Last Modified: Wed, 12 May 2021 01:14:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:541f88a4fe7b9b43ab37d70a75247ab976ee4e16ca5cf120b901bfbdd147b09f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58795478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af921c2e551c1352bb285074c3dc0a8b81b2a86ab36b0f3c5d16dd69208a82e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:32:59 GMT
ADD file:dd3e802ee39ef6460fa54303399ebc1f08919c4011f872a9ea00cdee78e2e6eb in / 
# Wed, 12 May 2021 01:33:04 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:33:32 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:79c001f710a199bddecf6231e4c1152e873413174cb20e083729089e3d15e400`  
		Last Modified: Wed, 12 May 2021 01:41:18 GMT  
		Size: 58.8 MB (58795251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a37bc279136e0e3ad38ebdcae2cd5085b8fc174ed007f31cfb7df48fad2b9e`  
		Last Modified: Wed, 12 May 2021 01:41:29 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:a82f9759b5c33737a7471b222533aeabfca196c8218d11ba036cea0216e6e1c8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53177479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d802f3d5fe89a8809357072736c5332c4956ac24caa2001ed449fde5c02d8ad8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:42:28 GMT
ADD file:2c5346f49f9df572a683f8c527b35a6f38363fdcdc3f84dd717e4350111f9062 in / 
# Wed, 12 May 2021 00:42:33 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:42:45 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:71407cbee72f89deadd67bbdd36cc0d4779120d71ced9bce9ac9372831cbba70`  
		Last Modified: Wed, 12 May 2021 00:47:20 GMT  
		Size: 53.2 MB (53177252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275d80c7b4ca7aa0c0e8f6fcea22aed5cdac2ddde56cd9bc977d1dedb4aa2ca1`  
		Last Modified: Wed, 12 May 2021 00:47:26 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

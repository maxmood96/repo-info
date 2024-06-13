## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:60296ffbcd688e3f20082f932dc4cc72724ede2b7d9c60f7b652ec95ddc1309b
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:3f802a72af111e9ea360876f2385d25dc8a76d87048f4dbca94c44e848fa0e03
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55099418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e60fcd7bf9611918c462101b7eb474fe78a9ef646364d1d90821bc77ee1baa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:22:05 GMT
ADD file:ee2e7b4a8df59a5ab0eb1f79bc5398cfe312862485ad527dce8fbbc93c07a307 in / 
# Thu, 13 Jun 2024 01:22:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:10 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:db96211368ad0a32f83f6249ec9c886108f8c724b06641b0ac3c73f7dfe594c1`  
		Last Modified: Thu, 13 Jun 2024 01:27:36 GMT  
		Size: 55.1 MB (55099194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a8d8e6159292d913f7668e513743a83f3a9d431175d9597dbd038fa330b2e1`  
		Last Modified: Thu, 13 Jun 2024 01:27:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:2f8f6b03da7d7dd5b2d035dccc3a5d6e8fbaf0a513ffc4a13ca49e32bad00daa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52603254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99467acbd602a25dfb67641a31aa0857419ed01704092f35c4a4783a6a84e574`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:56 GMT
ADD file:85b771f78fc61f453ec615acac644806927f88f14a903fa0941e35bb5f200603 in / 
# Thu, 13 Jun 2024 00:48:57 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:48:59 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5d177cb9450518cf089afb2b30976bcd063fafaacf5320fc5059c11995b24344`  
		Last Modified: Thu, 13 Jun 2024 00:52:42 GMT  
		Size: 52.6 MB (52603031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ad9ef76e4d339b705f4e7b5217c10c672a3f2c841c2ad87ee5368f171ba8b8`  
		Last Modified: Thu, 13 Jun 2024 00:52:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:9236025d96ce886bd80572273120af4d10afb6e8c192b2a65804efc1c2be036c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50256658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7193a275c6d38ec2a57fb1cd262a9b148d24fb8cf99d9ee3b6c631f7258bfdd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:39 GMT
ADD file:ba5e10d1f3128bb5aab9a44719832d6ff95a2bc72b8b3531b975e5d411cc28fa in / 
# Thu, 13 Jun 2024 00:58:40 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:58:43 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:08139b5af748e317135f7a55b29b72fcdc515fc8af77d9136d30c35613bde5d2`  
		Last Modified: Thu, 13 Jun 2024 01:03:49 GMT  
		Size: 50.3 MB (50256434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac45aa13215144dda1b09269554d3d70861427eab89dec287887c919b9b3903`  
		Last Modified: Thu, 13 Jun 2024 01:03:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:97ce389352dc242b58a8d60fd5d6d27eefb57d3eff03574e8de0a783738b2373
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53739771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716bc779c98c6104bb7f46c3d85047cabb9a70b501e240ab454f322df92c1d0c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:38 GMT
ADD file:8edc3fa1a78d8a490e87f8e97333d1817db44c41fc91ad262b2565a901c6567e in / 
# Thu, 13 Jun 2024 00:40:38 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:40:41 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:62f5f57d5ba80ea6912b37f47071f5933df0fd97c44280e13a4263796f61dd91`  
		Last Modified: Thu, 13 Jun 2024 00:45:10 GMT  
		Size: 53.7 MB (53739547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10db115be412ecfe67cc0e216994b4f229b3bfe61751b639ce04bcd6e19035fb`  
		Last Modified: Thu, 13 Jun 2024 00:45:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:98e752c01b0a6564f3580083c95e808748b57d2af8f2df46ca424ed38258f929
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56076767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af90fa4581fdf12bb3afd41715db85b204d12a1d79c11d938bba1f4624ef5848`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:05 GMT
ADD file:5399452beebf63a70261cd5f6454f6f756ac2ead5f518d7507d461667ecc8d61 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:40:11 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:22c9d4349f1184d53776661c0d00810f6578ac7b4cea9a25790116f5aa176b16`  
		Last Modified: Thu, 13 Jun 2024 00:45:35 GMT  
		Size: 56.1 MB (56076541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba393fa8438551e2f3e3c8b6727fbf80f814287289e8bfcf6578281a1acec24`  
		Last Modified: Thu, 13 Jun 2024 00:45:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:84a834e75f59446b245a13855ac8f193e377ac1c02b08631b9e28effd75b8db0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53322690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a376ff291ce41085dc5d8613c9abe1d607521414705019e263a40021a934d968`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:12:26 GMT
ADD file:dee2b8bb006a00d4497d9252c88b6ad65545b651eaf9824f3f66e3fbefe6a0b1 in / 
# Thu, 13 Jun 2024 01:12:32 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:12:48 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:842c2ba503b9bd2cc9f1f9f7af77fe26f862358172a5d63f1ed8c8a22b65e9ef`  
		Last Modified: Thu, 13 Jun 2024 01:24:03 GMT  
		Size: 53.3 MB (53322463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92954bd1365fa5a1ad3d2c0fb9bb6647152c7399521a894516736b35d2560f84`  
		Last Modified: Thu, 13 Jun 2024 01:24:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:0ea72c4812ad2a5ff2c4daf17cb84310701c28f571f6772db7eda8caa6d608b5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58969194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0f8e4ecfe381d7516251eb26d33c1b1a39a135720312b98425330657af946a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:17:43 GMT
ADD file:9df98f12c45a86c5a7515a000dadc38fce393318bd4bb342cb5d68d2824c5f7f in / 
# Thu, 13 Jun 2024 01:17:46 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:17:50 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:93e82d87f492429f85ae3475df9ba2acefa27d6414cc02a8079f03debe50a21b`  
		Last Modified: Thu, 13 Jun 2024 01:22:43 GMT  
		Size: 59.0 MB (58968967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:decb9233f1e855e27e5b9b8e35f725f64c0f66b1bc33a6ea342a59fdc067bd32`  
		Last Modified: Thu, 13 Jun 2024 01:22:51 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:eb55d47764e8d82eee4851f4f1aaac80cf8faac247b16b0d19379ad97fce8769
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53337747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0969e1bdef140a8edd8b02acaad14fec8b65a6e56958dc658e577fcbfaa4225c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:43:28 GMT
ADD file:6c022691ac37437b1bfff5a9a25e3023e298f40b508ad285e2d1e2c7fac73ce7 in / 
# Thu, 13 Jun 2024 00:43:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:43:37 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b623070bdd8d31a31cd19c256e11f00a3a4eb55c625ca7d91715315accbb15ea`  
		Last Modified: Thu, 13 Jun 2024 00:48:32 GMT  
		Size: 53.3 MB (53337523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c26522b2dcdc9a25651f0cbad9d561d4ff8b647ec15552d37035dfc9010185`  
		Last Modified: Thu, 13 Jun 2024 00:48:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

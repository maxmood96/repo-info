## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:d6e1dd2dc952ecfa71e0e4460cbcf80548b9595287ddcadb2d96c8ec027d476e
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
$ docker pull debian@sha256:abb0d45273c3cb063af46d0159fc7549ba87b6376fd9a3be24f8863502bbce80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55099655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feaea0218483221f068f46995457c8deae5adebfcfa95cfd0b116091bd3d691c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:29:13 GMT
ADD file:7b9ec2bc447148065c15856f9e732b94f2b534011ede5939002e904bada7044a in / 
# Tue, 14 May 2024 01:29:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:29:18 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ce314f7c9291d3ef0af89e3d92b5458ee154a39ea5bb198e51813bd983a6a20e`  
		Last Modified: Tue, 14 May 2024 01:34:30 GMT  
		Size: 55.1 MB (55099434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d65cd28b616f33428b6d9ceebeefb735fe9dcb789a3b98afe2a2dc5ff90c39`  
		Last Modified: Tue, 14 May 2024 01:34:39 GMT  
		Size: 221.0 B  
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
$ docker pull debian@sha256:5602e7dd6ab8a95e81a8c77ffd9124307ca8c7912e0d612a40630641696bedbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53322315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839ba624d42ed673f449500093abcc4f4bd66ead1c21be2e39323066b24f3b51`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:12:58 GMT
ADD file:ab7a7c4552b9baec3a6fc2725df0719e4757e6cb0d4c64e6815e8a3fe56daa91 in / 
# Tue, 14 May 2024 01:13:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:13:19 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7d2eb60f220e5c6c125a56679db08e8c2523f7d15e5aedb0ac08449c8d08010e`  
		Last Modified: Tue, 14 May 2024 01:24:28 GMT  
		Size: 53.3 MB (53322088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caebc8ffbc8a56bf851fe3189785bd65a72a6db6cbce1b41ed7335abc509dee7`  
		Last Modified: Tue, 14 May 2024 01:24:38 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:c767dd11563b1c20a11e63ccbc383dce79ab04bb71817cf820362b7fad6c62af
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58969624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f0fa92758a5f51a1b3fa90c6651a156a07495fd6a48dd6d36603bf8d0e0e1e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:20:38 GMT
ADD file:61a3bb0f165b7e140ed2c521846c9df5fb991727c11a84df84186ee94577b5be in / 
# Tue, 14 May 2024 01:20:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:20:45 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3d6813d8fcfdcf2e2360325d7bffcea01864d894227093b951de3e18038b743e`  
		Last Modified: Tue, 14 May 2024 01:25:13 GMT  
		Size: 59.0 MB (58969400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cab1bf915795064b5a64b8f7f4796f32883e9bfef249dbcc849a918c9eed692`  
		Last Modified: Tue, 14 May 2024 01:25:22 GMT  
		Size: 224.0 B  
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

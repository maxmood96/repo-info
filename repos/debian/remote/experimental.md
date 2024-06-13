## `debian:experimental`

```console
$ docker pull debian@sha256:adbaf001f6e1db57cfecd277fc37d688ca9f65774aa592ad3a90d48e1ef0ea55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:2d694ee186878a6b2636637eb3981b94b0763057b1c97ac6f20e8e2d648c85d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52643112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b33936d8b9c52b8e4e88634847503076c69db1791ec9f21a8fc01f863dd120`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:31:01 GMT
ADD file:8c5a6d2567e5604b8b6f318a76325c760f880352c4be7862ec514c65aeec1f30 in / 
# Tue, 14 May 2024 01:31:02 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:31:15 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:17977f56026a1758cabf2eea1e3430a4269a6724ab7249f48b97efe2d60ee11d`  
		Last Modified: Tue, 14 May 2024 01:37:19 GMT  
		Size: 52.6 MB (52642894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293ab4f64cf4a279db9e88f07669f959717ac1b6e34f7e4ebc4981eaa928fdd4`  
		Last Modified: Tue, 14 May 2024 01:37:39 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:a6cbe8c8bca94e2330e859ca02621a21ec06d09a00f5c82b16b6b5c2bfa83511
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49497948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4f031361e79eaf6ff1ba91063be163ce6a7c131ec21be1abb7f4a02d9ba93d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:50:15 GMT
ADD file:8220399af7e4dac5b20511baf0f7e41ec5497bb049c252b12df487975c998ed0 in / 
# Thu, 13 Jun 2024 00:50:16 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:50:24 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:75707ab2c3205293345df9598e07e04ba5f0de0e27278a19483e6462d8a689d1`  
		Last Modified: Thu, 13 Jun 2024 00:55:24 GMT  
		Size: 49.5 MB (49497728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a474ea4f07a1f85d9d764988ddf925a842411286a4d9da80f8b6d15f5d3399`  
		Last Modified: Thu, 13 Jun 2024 00:55:44 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:861e1e8c8f094229c6fc409e1a31c1a836d902c012b84c2356577abc1068a85f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47253632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b080539b69be353960046182cdedd30994ca350fbce0e02fd4c35d73ab2c6d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:11:12 GMT
ADD file:4fec029a0e9a4469a7492392e38f441eabeacefc2b4a00d64d5ea996b473c922 in / 
# Tue, 14 May 2024 01:11:13 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:11:23 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:af066d968dde063742fc240a83507ed6043abcb22ad2fb9fe3a20fd13016d392`  
		Last Modified: Tue, 14 May 2024 01:17:28 GMT  
		Size: 47.3 MB (47253414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0146c6e71cb664fc5244c3112e841ea474624a0e8a06225793fecc9245888a5c`  
		Last Modified: Tue, 14 May 2024 01:17:48 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:fe4f90bc84e078ea54cf263e0053c8739bdc9f2367bd85104408c1ec2bbe5499
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52683338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9da6d6972f1500d319a7d6e43c47c3d5de70dc40b435e9ac521b8f0f779007`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:50 GMT
ADD file:e2515159d6b834a66909c60f24e550c86184ad739c792a452011306effdc8fd6 in / 
# Thu, 13 Jun 2024 00:41:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:42:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b6c619a1513a6517126a1a9da5e700e69d3542c73ba74f6fdb7d1148e7d04ae6`  
		Last Modified: Thu, 13 Jun 2024 00:47:36 GMT  
		Size: 52.7 MB (52683114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d62b9c95012152309a3cc31a4b9981600fd5045dd875addb566d1a7229c5730`  
		Last Modified: Thu, 13 Jun 2024 00:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:babd55a8cddb60e49b0647f731f4232900a52a63b2490369fcb678ba529f4416
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53304527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7c0f34ba69c775d4ff95c80590e695c5bef2984e5aa821262a8dbeaef69bf9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:54 GMT
ADD file:d1fdb0b9ed021eb7269ce6cfe09244166cc99a859401d9045ed096abe376a631 in / 
# Thu, 13 Jun 2024 00:41:55 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:42:08 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0079983cf187ab06fc29ea2245b355e72b8261ccbcd555b98c457c2560f5bf18`  
		Last Modified: Thu, 13 Jun 2024 00:48:34 GMT  
		Size: 53.3 MB (53304306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320559339114c4bc10293d3902d93c365b2243096379e60a48b9229253376283`  
		Last Modified: Thu, 13 Jun 2024 00:48:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:87d155045c4a1ddeb159182956374c301e3f7623f1c0f6a484f5a311d3983375
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51536578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f970ee5f2150409c87c66b66318a23c9dac5ef2ae17d37c8e5fbd3fcf3b549`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:19:17 GMT
ADD file:8160485a5370d25087efc65221162d5363ad160ca7b295e96fb148655998826f in / 
# Tue, 14 May 2024 01:19:23 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:20:03 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:4b4bccb18e94d5701f253b8234c9e51b4a9f16c580a70d1da39d4213f612ab7b`  
		Last Modified: Tue, 14 May 2024 01:30:46 GMT  
		Size: 51.5 MB (51536356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d509075870cfd4801547757365bc642bd87f5ddd346176375f10a624b046515e`  
		Last Modified: Tue, 14 May 2024 01:31:25 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:e7267db2518f073238611cb49e8ba6cdd31aaee3c139ea4e6cde9daeda6b7cf1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56538401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b2b05403f03d4b35af0a1a3fcfb8497dbb8a2fd15c49b70de398f8e6c1619c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:22:34 GMT
ADD file:1e01a0c99ae6c0194d5d2d285035c000deeacabc71c49e8c8c25286577c14b1b in / 
# Tue, 14 May 2024 01:22:37 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:22:51 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:01c6c75c5a9a3459977939d0bdc7230f881bae3296210978fa6ebaa06b400600`  
		Last Modified: Tue, 14 May 2024 01:28:20 GMT  
		Size: 56.5 MB (56538180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4660a3827751394b2e7b53b46e1a431cfe21babdd846dd899412dc8e6ad5e02`  
		Last Modified: Tue, 14 May 2024 01:28:44 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:279970fe02bbf2458e872a7b55b84521a5853bf6799a272444e0cfda23f2fa14
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50961630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a9f3a1e84895718170a51087889de8e8fa8d77ca34a2be5e3c7847801b33c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:10:01 GMT
ADD file:bbac7ea25590f7d684c08a4f559ac07e491e8d699b07d397618cc55c15e08502 in / 
# Tue, 14 May 2024 01:10:03 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:10:40 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a2146c63627cca301014431602e9545f03af50832b99fd4e0a7f0a8152cbf0e2`  
		Last Modified: Tue, 14 May 2024 01:12:57 GMT  
		Size: 51.0 MB (50961407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178ab4264b324ed2965d8e1c91aeac5493b557cbc1a60b6ac9196261b7783c55`  
		Last Modified: Tue, 14 May 2024 01:13:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:fe13dd9173997c3c635ab38e8b750447dc00470cb4f71b8566f5fd331aee7803
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52054625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96818ab0be8408472d1391e28d5696003b59d1e17fbdad2400807212687cbcae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:45:56 GMT
ADD file:1cbd288c9973cca24a784013268a6407731c6606f529134567c162da1d143fa4 in / 
# Thu, 13 Jun 2024 00:45:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:46:17 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a0759db133a573847da61ab8e01bdc49bfcfd141d195de276e707216b4f465b2`  
		Last Modified: Thu, 13 Jun 2024 00:50:35 GMT  
		Size: 52.1 MB (52054405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3daca2c4a7cf4dd9ebbbc3235af238e6141faa007561b6e9a450ff8eb02560c5`  
		Last Modified: Thu, 13 Jun 2024 00:50:51 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

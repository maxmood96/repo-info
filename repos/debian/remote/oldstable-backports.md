## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:ce3633d1452c523d874ca002a8c870546664de8b560b3749de481be97101eecb
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
$ docker pull debian@sha256:dde1ffaa95474a5c21761aa15e45e8ac886c8529fa51240a9fa2b54021c6bf8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55056850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2f214f32d45ed178faf8c30961b8f4fa8056afbac1162625904ffee4d7d026`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:01:04 GMT
ADD file:434ca64d2c088dcd5f15f2b334f3dfa94586339ba21a3a98e5dff759f6193803 in / 
# Wed, 16 Aug 2023 01:01:05 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:01:08 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c9723da4cca55281aa9bc21068374b677501d737f4722c8b350ae42b3cca5e28`  
		Last Modified: Wed, 16 Aug 2023 01:06:45 GMT  
		Size: 55.1 MB (55056625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54bf28710b600728449d45a96f168dbc3843db8e770a057bcd80719417059266`  
		Last Modified: Wed, 16 Aug 2023 01:06:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:8cefd662aacb0cdafd175551258963737a08bf8e8af5e486b4e7697e6d9a1702
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52558370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528445383747c93fb31dffcc1e2a94d54afb3b69293da0eb060efa2d054bd61d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:48:56 GMT
ADD file:e6753fde0869f0f5afc29d8db288a9ce529874089560fba3f5aabf812b0fc278 in / 
# Tue, 15 Aug 2023 23:48:56 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:48:59 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:67f24ee25b6f816ab234b14c1a8f78303187fe1928975945689db3ff437614d8`  
		Last Modified: Tue, 15 Aug 2023 23:52:34 GMT  
		Size: 52.6 MB (52558147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e3f6ee751016093be369ec93a414882644bc6764ec26638c7091e314c63b21`  
		Last Modified: Tue, 15 Aug 2023 23:52:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:6f0e58913eeb04cf51386d2df819cce201eddcaf6b0f961e513d3df5d0959532
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50219719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5f1f7ae45971fbb991c95a6496dfbc1230feb426dc746c5a94dac81ba579f4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:18:23 GMT
ADD file:eb9e6e973bccf784a47fd8f437c42aa64b2845c8d9b92d4baa6e94e9c5b80ee4 in / 
# Wed, 16 Aug 2023 00:18:23 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:18:26 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9faed8566e0215a85ef6dee0f78e2810e791f973fc2c05b9619ed567e8cbeff6`  
		Last Modified: Wed, 16 Aug 2023 00:23:38 GMT  
		Size: 50.2 MB (50219494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa5b22dc19fbaca83b7196e2e5c3cc328b912e3f006023c232284b85acd3aff`  
		Last Modified: Wed, 16 Aug 2023 00:23:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b7803fa646f61fab54125972f58a9b4a302f14137ecd0c8f7b895158d7caf97b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53705010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3472dd36b8906ec2cfaf698c0c1d763eda61bed5a8b35a76682583369de7255f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:46 GMT
ADD file:34a36ee946cf6f98b44632ef4bc6c0d3362d611d35c4541abd8b683957da0423 in / 
# Tue, 15 Aug 2023 23:40:47 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:40:49 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a10af57736c05ea7055aa2bccee0cf5869549bd35cbca2cc9360afb611d6427d`  
		Last Modified: Tue, 15 Aug 2023 23:45:24 GMT  
		Size: 53.7 MB (53704785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ce1ac1e56aa3475bf873cec0f775303854aa249f1767a749e7885423e8eeda`  
		Last Modified: Tue, 15 Aug 2023 23:45:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:0b938358115e756d5dc638a231847d914534ee6af7f430c8e373f7ae40b8f93c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56040746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b8a0a2d4bb699377fce391994f3601367e27c97f83e73555105036be3c0f33`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:13 GMT
ADD file:be80506a012b48af460817cf4bafbce09ce49837492dadd0d729dfd35d7f2627 in / 
# Tue, 15 Aug 2023 23:40:14 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:40:17 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e47d27a26101bfcb6857b31fe3ba89e0ef8d7fd4063dc5b0e44eb1d58b1b765a`  
		Last Modified: Tue, 15 Aug 2023 23:45:55 GMT  
		Size: 56.0 MB (56040521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2628f5835cd4765d83b77d414a83614224f010a82012159916a39a5997d6c37b`  
		Last Modified: Tue, 15 Aug 2023 23:46:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:ebc723d379bbe94c57e8f5c67019074e03748c6aa77f28f9eb26cc110d29aebe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53271793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebd884ab28e744062b811f873d18ca66ef5c4d7be2badf144167b959094d94b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:10:31 GMT
ADD file:1b0f910f06e77d48d742060cea74c34f9dcab095b4f21304a227e9a307b89804 in / 
# Wed, 16 Aug 2023 00:10:38 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:10:51 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a285fcedf211c6f1c66304f1eb9c1478f9fc4659786eb942eb7cad595c09d7a0`  
		Last Modified: Wed, 16 Aug 2023 00:21:44 GMT  
		Size: 53.3 MB (53271565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd74486eef0b7cfcc0bf1646e275000b312e0044794a93f81a8fd1dfc8bf983a`  
		Last Modified: Wed, 16 Aug 2023 00:21:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:95e0fdf1a5bf214b71cc1319198590465557c0ca02da9d7c726f39b80661227c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58928671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1d0b46546c8b9e962f2a72d14bd7d3b41b65e0dae44fecb49790a953e84154`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:10:30 GMT
ADD file:142c48b248e5f95641e09b46661d0e8cf4084992ded654a9ba639158d5e162fe in / 
# Wed, 16 Aug 2023 01:10:33 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:10:40 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8f6e54f0c20f3f4c4d02ba4ba207ac548a20332e57aeb1784bbe9c898ac81848`  
		Last Modified: Wed, 16 Aug 2023 01:17:35 GMT  
		Size: 58.9 MB (58928444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ab19611ed96dc1b316afdafb4dfd59675a2cfff67ecc0825287453763f71a2`  
		Last Modified: Wed, 16 Aug 2023 01:17:48 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:65fc66c47b426a11ac3fafeca0701b776cb7bc16b2c040ead2f4d740ff5fd842
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53290861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d4d1798d2a13924dee715505b61034ea170fd09896db517778fb6233db5fe1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:43:16 GMT
ADD file:aa6aefd4db318e04c7ee34bec123fe1ad5bdfabae3dcbf3ba41b9ed515367def in / 
# Tue, 15 Aug 2023 23:43:21 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:43:28 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:79fd05fa321bd107f698cc0f80675f45b52b06193c08b8cf3f4fba1c1544fe2e`  
		Last Modified: Tue, 15 Aug 2023 23:48:36 GMT  
		Size: 53.3 MB (53290638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7448a9c4cb74c1642ed31996606401b04c6dfb2dff0a1269c069a6b54e1cab7f`  
		Last Modified: Tue, 15 Aug 2023 23:48:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

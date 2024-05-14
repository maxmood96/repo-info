## `debian:experimental`

```console
$ docker pull debian@sha256:591a0f8e581128c11b98b06135093a8b0c6bdae680e95d670340908591de75b6
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
$ docker pull debian@sha256:0668ccf49cabed88a3a04714b45376759b03c54f650998b214b1345937cb7c15
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49745382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2eab483a0e3f8b1e7ab3659f7994fe80371ecea29e2c899a49d820b1358bfd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:50:17 GMT
ADD file:521734357b4e269a7cccf4adccbbd4daa760954a4b217aeeb9b49671638b4235 in / 
# Tue, 14 May 2024 00:50:17 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:50:26 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f8921a756223f341386642e5fc17db8ecb3053a0e841396e2b5311ea042f7c6a`  
		Last Modified: Tue, 14 May 2024 00:55:21 GMT  
		Size: 49.7 MB (49745162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c7cb0c0879088932709c672d68ed25f600eb0ac62ebb65f6af6ba46776f3ae`  
		Last Modified: Tue, 14 May 2024 00:55:43 GMT  
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
$ docker pull debian@sha256:688a66c857e765546e689221c11e0d9af5ce3e2f55be7027636c13490896a76a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52930506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a93b5e7ea55995bf1b4608e3cfdfc5702c534239930ebae2ce83da77188235`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:41:38 GMT
ADD file:6c54381ec578a9f57036074fb948edeef7611c02bf29d34f212fab376078813a in / 
# Tue, 14 May 2024 00:41:39 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:41:47 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:cbcdfed4b85cce0d6fb37326a97d75504908bc768ddb092ec6e95591b57c661d`  
		Last Modified: Tue, 14 May 2024 00:47:13 GMT  
		Size: 52.9 MB (52930286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb740826b14f0c7b180aa4cfbfc572ae080489b009f988724508f60ceb2d216`  
		Last Modified: Tue, 14 May 2024 00:47:37 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:a29e952638bf01085cd342437b605f89ccf62efae9f54c4b475a02f9f38adcfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53540159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db527ea6f0a5cb0ae3962b5e202681591085d6e419927be52b48fc5cff2da8a6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:50:17 GMT
ADD file:826e7bcbf08f9ff2dc0b9ce63104c53184d5d6387c42ada2162d2ec51e68f4b3 in / 
# Tue, 14 May 2024 00:50:17 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:50:30 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3edf4a10c208a633ebd0b77ce4c2cacf895ebc393e6d0e36e5939cfc8f4595ad`  
		Last Modified: Tue, 14 May 2024 00:57:35 GMT  
		Size: 53.5 MB (53539939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9f5e64cd5d43f05ebf956f9dd4c6a7aafadeaa9daef41e8fec628947916037`  
		Last Modified: Tue, 14 May 2024 00:58:00 GMT  
		Size: 220.0 B  
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
$ docker pull debian@sha256:b70285bcbc25e852120e5e01e2135d1e410f20bdc60b6a0271a3f6fe2ffc0c27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52293504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deff9e019300f92f74f2ff2798b12905e8d654a26729885ab213bdaa03e2fef0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:45:53 GMT
ADD file:39996ceefd01e3c041f2eca344ee84f600a0ab67c058a6eaf088784805639943 in / 
# Tue, 14 May 2024 00:45:55 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:46:13 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d46d86ebff408f9c6b07805c1a092479e08885dd71224f34f876559c9a617552`  
		Last Modified: Tue, 14 May 2024 00:50:31 GMT  
		Size: 52.3 MB (52293285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc0f7651df0162097faa37eb635cc874945e76c4a279f2a98395f42c1e6391a`  
		Last Modified: Tue, 14 May 2024 00:50:48 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

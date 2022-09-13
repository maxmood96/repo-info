## `debian:testing-backports`

```console
$ docker pull debian@sha256:2505b237c4912f833327cd08154a9a26686bd323128d6bb2a06fdc0fc4710605
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:a8a2693471bcb4a925dd51a5928d97100ef656057e76432fd97c8361f8d7d678
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52983807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bac03a2da30bd3a7c55822486a10692ea269b259704da8bb09f2cfb8f7e7d30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 00:57:53 GMT
ADD file:eab284d675ebe571774a405e2773ad309e7992babbcee7da7353360819720c79 in / 
# Tue, 13 Sep 2022 00:57:53 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 00:57:57 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d81669dcf8a7f2d2d267e74db5db6aea7ca548ce5117280e5e7e6c5abeb0b222`  
		Last Modified: Tue, 13 Sep 2022 01:03:18 GMT  
		Size: 53.0 MB (52983583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764c8e3fa1332ea3bbf84a38f2f810d7008e333d5ca19f6731caaa02e623e14a`  
		Last Modified: Tue, 13 Sep 2022 01:03:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:673acecf7fd9ee70432da3d1a97d4e5d5bdd248cd4c411e19b04e2121426a0f1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52122767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3e2f643a20f57871cc36323e15936b7fec936ed8e5e01342f3457f07cc11cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 00:55:28 GMT
ADD file:8a5271643c4e7a06124d169d69237ff785175fa358687fe70569fbdb6019b4d6 in / 
# Tue, 13 Sep 2022 00:55:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 00:55:36 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:81baa9e2df41ce6d109b1642aa8ac546cb2767115f02971dae2b8b49647e82d5`  
		Last Modified: Tue, 13 Sep 2022 01:03:33 GMT  
		Size: 52.1 MB (52122545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe87e8cdbbf80a1c29de79f722c073671d0c9ccb7cb15b3d7551311eaa71d63d`  
		Last Modified: Tue, 13 Sep 2022 01:03:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ac3829e4299166326f3968ca10440070b648b869485503faaff81c3c65a86039
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49856404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c25aea149d140cafbefc435b526cc90ab86fe6f6bac5c709f5e5c618242988`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 03:45:03 GMT
ADD file:5b41f0913711127f44628a171aff60ba821f503d71695a7270b888a82d5f1f53 in / 
# Tue, 13 Sep 2022 03:45:04 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:45:09 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7b4cfe0111bcd53deb48d02a2988e5268c50776e0128f7d5dd4e262a47cbd6c9`  
		Last Modified: Tue, 13 Sep 2022 03:53:41 GMT  
		Size: 49.9 MB (49856183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7655483dc304d0ca155b4adcad80a50408c101675b3a405ec5e1f8eb9fbdc162`  
		Last Modified: Tue, 13 Sep 2022 03:53:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4a4be23dfa03fe2397d9db1713a8957dbab64fe78168f7d3a9d6ada8b015a13e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53446146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac67248fb1fc394005d60455fe470c56f18c50aa327beed00b5efc138c8e5f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 02:12:36 GMT
ADD file:5955efbf853f56b46dd0a0f888cd895ed17e7e0569a5f5e3d6e1533677876cb8 in / 
# Tue, 13 Sep 2022 02:12:37 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 02:12:43 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fc1b14792d866d5d906ac93becc6848dfb2457dba55175d662abe52ddca9c73a`  
		Last Modified: Tue, 13 Sep 2022 02:19:22 GMT  
		Size: 53.4 MB (53445925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6545c096713bb02b9dd6ba8b0cd74b2c4d904d7e307570717ab42f6559acc364`  
		Last Modified: Tue, 13 Sep 2022 02:19:32 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:5b349a817135922cdcc521ccd3a61d9a8bc43c070187fec19476c84387cbf056
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54342131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1bb602a1c6565e9d41f6a47f6a63ab71edd7c9a38d211b92925590c9503b70`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 01:41:34 GMT
ADD file:27f4f7054429d8539edaf3eab52c665b1ce6e04051637ae9ea4f7504b045eaec in / 
# Tue, 13 Sep 2022 01:41:35 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:41:41 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e20007d0545ad56958646309202d133d627fbdcdb69ecd65e9f8de91f13acf86`  
		Last Modified: Tue, 13 Sep 2022 01:48:27 GMT  
		Size: 54.3 MB (54341910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4beac173270d06abab5ea00a6f0ef7aefb0a1ae6c34956ec21c53a2063678da`  
		Last Modified: Tue, 13 Sep 2022 01:48:37 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:4cb50a67b2079a45be31f3a83b0c159318ce5050b7e188c8d3ed1bcfa85201e5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53424469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c48536771afa3440a20a26a6dc12c2ae5b060454fd0a0a10f13eb64119643cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 01:13:37 GMT
ADD file:92c0fec84b36436afd88ecaf3993912b8883d0c1efcf11e7a45692af754ff7d1 in / 
# Tue, 13 Sep 2022 01:13:42 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:13:51 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bd2127b47d683ee6019a9dd69b2cf5a50be868500d0f68848564cdd84fa2cb96`  
		Last Modified: Tue, 13 Sep 2022 01:22:04 GMT  
		Size: 53.4 MB (53424244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95285c12adbed852b8ca39a3cc5e951c64eec8d202609907f770284bfc824136`  
		Last Modified: Tue, 13 Sep 2022 01:22:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a45605d0edf57f5ca0ff9e0099b642603a3692ec56fc2a8818ad4268a1d42104
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57546096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631be5b259340fda0b0bbcd8a4df419c9a3dbe683c3dad0f62e8e9e3405f941c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 02:09:25 GMT
ADD file:889da29311d0cb07e18ff577e10bcce3408f61d3c98beded1256cbf338a21ad1 in / 
# Tue, 13 Sep 2022 02:09:28 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 02:09:34 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dd519797888890826b8802054e0382a0eb34bea2319d183ee4271916d6cd5c2b`  
		Last Modified: Tue, 13 Sep 2022 02:15:51 GMT  
		Size: 57.5 MB (57545874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59cb7dcdfb892b5e5e2adc0139e33439f10bf3bd65fc7d495e21b6ef3f32ebe8`  
		Last Modified: Tue, 13 Sep 2022 02:16:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:3b341ce3791311654c0a2ebd7a58942b5d941bda7871d7b6967faa100833e760
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51793976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea9e4072be11a39a2b0f77386261842200bc48f92780b3e7e7f299d1975c850`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 00:49:12 GMT
ADD file:66f44d68f978fe3b9abd2ff209f09412b83ce5518ee28f77b480bea6ca41fd47 in / 
# Tue, 13 Sep 2022 00:49:15 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 00:49:22 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:72862deaf676befb9cc285a47088524f14e8d520d3f66531de063d495dd63aa3`  
		Last Modified: Tue, 13 Sep 2022 00:53:48 GMT  
		Size: 51.8 MB (51793754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9531bdc635a5ed6091b2356b0c90d77a2fe92dd1476c9b313803b3bfdb0416b5`  
		Last Modified: Tue, 13 Sep 2022 00:53:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

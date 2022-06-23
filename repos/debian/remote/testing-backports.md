## `debian:testing-backports`

```console
$ docker pull debian@sha256:b5745ea6467eb23a6024fde1cf832702b03af059dd181845eeaffd6f01fd3faf
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
$ docker pull debian@sha256:3438cf3d1b3f6f66b5d28bc476ea2c9f7011a15d95c83366f5644aac85d1ccc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52994201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916bfac9005b659481c493a0539c5c70d231e92f87f5f14beb456e03612c16f0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:29 GMT
ADD file:5c4e113e3abcb5aeb9438cdaf07c7d900b95e2a30e114fab835f40ea836e1ecb in / 
# Thu, 23 Jun 2022 00:22:30 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:22:33 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d21669d6bdb9702ceaeab2d3a60e86f23e6da7994b114ec5e684413e2628cb52`  
		Last Modified: Thu, 23 Jun 2022 00:30:22 GMT  
		Size: 53.0 MB (52993978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c05dfa858a179e24a8038674c39414380cc0f2129fdb387626e0a723a7ffed`  
		Last Modified: Thu, 23 Jun 2022 00:30:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:880213b506db4e544227ecc456856d9d4b2cc7ec53483538159122e162e4e710
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50768074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19c8a0278cfd5a6f131d21cf953445d0a85d5d42bc9cece10ab03a32233bf75`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:56:37 GMT
ADD file:c07e7c61fd09302fad7297860b6b3eba1cb39f1f856c07f548a7bc5f178da0e0 in / 
# Thu, 23 Jun 2022 00:56:38 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:56:50 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b74fe02a543a99a7a06712e27d16ef69b0202ee328e6c8c07d7ccce5e20cfa2f`  
		Last Modified: Thu, 23 Jun 2022 01:14:21 GMT  
		Size: 50.8 MB (50767848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487cacba5354225ba46f595d9d6def0437b680f75c48aa626ebf302409279e37`  
		Last Modified: Thu, 23 Jun 2022 01:14:32 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:7334196c26083f06c33460cc8e9169d5300470fc9bf4ef1dcb55a83ec561010e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48476635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7855b424dc327a00f2a1327500fd69decb38caed94ffd316afc0723069664b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:06:23 GMT
ADD file:ec90a19450a4b3174d662c6df3d034488e52773bda79988366e79bf6ac179803 in / 
# Sat, 28 May 2022 01:06:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:06:36 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8e10f53774ef90fce803a05457ec21c9be85884019be903eeed2eba672058603`  
		Last Modified: Sat, 28 May 2022 01:22:58 GMT  
		Size: 48.5 MB (48476410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3754c9b025727de20960f9cd09ef91541685dddba7f11ee2f1f1a3d02403b5b1`  
		Last Modified: Sat, 28 May 2022 01:23:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:51e8924a6441ce56fafaf6680aa291ed679452f44637fa0d585d334d9c3ab6cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52074824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16ae8deac41a04b094b140ad36e71888fac52ceef14aedcd2019cfbac3b31a3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:43:09 GMT
ADD file:53311373f4d1abfcaa16b8c6fdad786327061f1e5003db1d3c6bdbf5b2c73333 in / 
# Thu, 23 Jun 2022 00:43:10 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:43:15 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:04df16d59bbc997b9cf53108e57268f1beac69c21eb10fac7036d92a38799d9c`  
		Last Modified: Thu, 23 Jun 2022 00:52:10 GMT  
		Size: 52.1 MB (52074599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0564e9c76d53dbb4e40f436f0c4b1197b15b93c2a37bab43aa0e5dd8748f1f6`  
		Last Modified: Thu, 23 Jun 2022 00:52:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:2bc32807dc95e5a7cabc012a80b1c9d9c33a6e4dfd6df1eabc49dd25e94026eb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53963722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87eb8c81cd0eb5431796d16ff0ad559dfb647a8e73b65dbe285c25fecf3aeb0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:09 GMT
ADD file:375ae69f0d485e805c6f4304159d9a397d793c68b3a88d1a357ed44c47ecde68 in / 
# Thu, 23 Jun 2022 00:42:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:42:15 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b381ba72dd0238fbfeb4804fc30597036ee80aa0ecbfb82beb546f1824fcc671`  
		Last Modified: Thu, 23 Jun 2022 00:51:45 GMT  
		Size: 54.0 MB (53963500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1899152a2b46e827ff41b524a0287f235e877377352f23d6e6296930d16235`  
		Last Modified: Thu, 23 Jun 2022 00:51:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:10a139b089bcde60f6dea6078e9d280b9b67595ceb4ee65f77229787fd5fc45d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52061751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02cf66d72c11eccbf905331a064453bddab397ba9749d2504aea6948ed12dd6c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:16:20 GMT
ADD file:750180a6aa4a39bf911865e098608b764a75b2c50c00426efecdab074d6108b8 in / 
# Sat, 28 May 2022 01:16:25 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:16:35 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7cb5df6daf04a8d6061a3059f38de0f503140d437089f54459799cd3d1d80736`  
		Last Modified: Sat, 28 May 2022 01:27:18 GMT  
		Size: 52.1 MB (52061526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf5a681f228150ffe7fad4dd9f6867ae147fe99d64651bc317d7caf4218c365`  
		Last Modified: Sat, 28 May 2022 01:27:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:5518506b13061064f86c0cd6efc52467e153897864b9cb91cd5ebb995502336f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57161810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83815a9fe561145424b30cc855571a8ce47f3baf299a5377ec73453fe75cd690`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:26:41 GMT
ADD file:c839faac39e30677565fb631dd4f40114392a7a667b8db7f85ca4d8aaeb32ad9 in / 
# Sat, 28 May 2022 01:26:46 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:26:57 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f5e0403edf3ce1164c65241f62272268585e383702736c781adae79230ef3422`  
		Last Modified: Sat, 28 May 2022 01:36:21 GMT  
		Size: 57.2 MB (57161585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792635adddbd4dc72f42008b9ae6fdf2562c007ff11a1ae6c744cc1cb0fee0a5`  
		Last Modified: Sat, 28 May 2022 01:36:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:52f20e6869b38ebfce5e2fd7c614671990da821d7f3dbdc7e5e0ac1fa8198ec3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51530871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fa17c39ea9f064ca9827c0795624307c565664c30fee3e6d7d42ed400cf1b0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:46:56 GMT
ADD file:c00b81c115a6c1391868dbe0ec890701d2f39e6559e809c5bb3713590bd1108e in / 
# Thu, 23 Jun 2022 00:47:03 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:47:12 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a020494a73fce189d7327ea16251dde415c3d854a3d9f6bd50af5d239febdb9f`  
		Last Modified: Thu, 23 Jun 2022 00:54:13 GMT  
		Size: 51.5 MB (51530646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db29084806c4e0854decc5ece0e74a15234fd4d3a1f751e52e5e8ab44fd0750`  
		Last Modified: Thu, 23 Jun 2022 00:54:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

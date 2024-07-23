## `debian:rc-buggy`

```console
$ docker pull debian@sha256:fc1cd7d70431e783c525b73697d8f5c0d1d9d961e08242d3cf9cf718a17d4010
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:e681d65030ecdc1d81861c05275451c59833b14d14656ba5f05986087ebea191
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52634796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98feb0e3a55965942ded4d5647d50cf8b834a6defc5a34015f1ceb6816deb5d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:57 GMT
ADD file:cf83030bc061e8d24d8a36b4edb2846333916985361600a06dfb635fd59c8068 in / 
# Tue, 02 Jul 2024 01:25:58 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:27:40 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2d149d696b13b9c3df064cbc77767f81d4635c7804547d50ff7da0c45c51990a`  
		Last Modified: Tue, 02 Jul 2024 01:30:17 GMT  
		Size: 52.6 MB (52634573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91094bf032ad28b8220f73a02b948b0b67d5c0a918e77e332865ee54e66e1e7f`  
		Last Modified: Tue, 02 Jul 2024 01:32:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:c1b0937b24896baf5a0180b058eeaea49982dfcf2d651599c062c85e2c11b519
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49829081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4ea27c959c08ecdfa901fc4ec2c3b1d59566b08455204ddf37e3d5d167dd12`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:58:01 GMT
ADD file:95d0230b78af5d334bd0243ce6197c2140ec2471924e5ef4413707038e18e143 in / 
# Mon, 22 Jul 2024 23:58:02 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 23:59:56 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ec2b125127e6f8d49325b626aa909fcd3b43a8d6c77bc97a74c5f2018c245546`  
		Last Modified: Tue, 23 Jul 2024 00:03:01 GMT  
		Size: 49.8 MB (49828856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783c6343481b1aab2ce8620fef6a5fea33b86e6d6109e5f27d6130c922895cf5`  
		Last Modified: Tue, 23 Jul 2024 00:05:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:ea114feb7f4491fe5e66cc0c3f8279c745c64b68c71f1ea58c8f704ee6d2c70a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47184058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2269ae2e62a75922dc0dac8f427740d2a710a6c5ae9dbb22b729690ec1095ed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:51 GMT
ADD file:204b9bd9d9bd808b15b0257739243338e223ade24ac2085e9c4ee95ac07d2795 in / 
# Tue, 02 Jul 2024 01:00:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:02:16 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5771d15f45cf5483d59c36ac7d7cc82b87747d80582fa22fc972b5752cd511a6`  
		Last Modified: Tue, 02 Jul 2024 01:04:51 GMT  
		Size: 47.2 MB (47183831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0bf528ad76d75255154f5124193b16a0f41559b9c067c77ee6dc6b4f6fb0b7`  
		Last Modified: Tue, 02 Jul 2024 01:07:17 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d31887cc3b135d3a2c70c04cf5e7ad2fe51c291cc5bf317bcc0f466038e8ffc1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52888982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae2970deaf2c64307b3c4ac4c0e8b6fed5590bbf877e891954eb8cc8492775d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:14 GMT
ADD file:13d2e6714604c76eb37d955b64f923c5e9360ac3b98a7115cf15ce9e648a1a56 in / 
# Tue, 02 Jul 2024 00:40:14 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:41:23 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5c22b1ba66cae5b1ecf15ba852e6873679650dcd639327a03cf68963e082f4be`  
		Last Modified: Tue, 02 Jul 2024 00:43:55 GMT  
		Size: 52.9 MB (52888757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320ddbf3f0b65fd9902a80dc192a3a05da430039f5fe2a61179bf7bb54a8516a`  
		Last Modified: Tue, 02 Jul 2024 00:46:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:787a49bf71aba9664988a747dee036ea1a3f671b8049f493357e1f9276e87ded
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53522614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800250e0c4fbd1ac50996a7efa10bb7e25983dfa155b8ed24355d6eb97d362e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:49 GMT
ADD file:a08584f3c5024aeb655047534f24f132994ce1978bc3c1b585197931050df05d in / 
# Tue, 02 Jul 2024 00:39:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:41:30 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:fcc722c6a8b995b7f273820b7fc927164f6709bd0e428b87e24702a321694439`  
		Last Modified: Tue, 02 Jul 2024 00:44:25 GMT  
		Size: 53.5 MB (53522389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5532a24f9dee1a094dd7bad3f5497a2c10b67735b6c851ea1975174bca0fd8`  
		Last Modified: Tue, 02 Jul 2024 00:47:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:103df92e5376d43613c6c98c9b55ce1c88083d3524c574eebf9205e1d46ffe67
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51498312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35bcf7c2672e6a1d39ad07f750f1b01509c7ff825d8c98d7dbdf146f999a537`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:21:34 GMT
ADD file:38ebbca2b69d1a13c63e4290834a1071ff05cbc6ca9d34fccc4e1db7ea4e713f in / 
# Tue, 02 Jul 2024 01:21:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:27:32 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:976737d71ea9234bc2fbae831a70295b014d7172cbb319c0c5e34bbba1f27f2c`  
		Last Modified: Tue, 02 Jul 2024 01:32:52 GMT  
		Size: 51.5 MB (51498083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818e70d791bef7390b9aa7170202a950ca594cc4a21c5c52d70ff1ef9137c0c9`  
		Last Modified: Tue, 02 Jul 2024 01:38:34 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:4d7d2c63b4ec9f6d28861dad148b62b8e49588502e89731223eb3f785f1e8cc7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56551203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff30bf0c011abc5b1582aaadff7fa3da2dc46d20d4544531b84dc6c0a15ccbc4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:42 GMT
ADD file:3dace89583571d938fe26db69a8298f77892aebb1a70e0e70c4df0d920e6711e in / 
# Tue, 02 Jul 2024 01:18:45 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:20:41 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:6b25364bfef282c79118e14cd54dbe5b982558a5939e2bdf63d94df980561937`  
		Last Modified: Tue, 02 Jul 2024 01:23:45 GMT  
		Size: 56.6 MB (56550979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f614a3490515a7d1941d3773b3deb588d2c3a921bc896ad116d97be54a8a2d2`  
		Last Modified: Tue, 02 Jul 2024 01:26:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:e7d8710761445c08f47066ea517f1b447db0230c3eb66f4ce42970ef2efa044a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50937377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4404996351fb0be4934c668c16a4bf53dfd5bab1ae4dca122ca27b542d2ea80b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 06:00:05 GMT
ADD file:cb8450d273e9ca21e77fb71fa8d82d31fec1f23d51cec9972814bdc76724935c in / 
# Tue, 02 Jul 2024 06:00:07 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 06:01:58 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bdd8e78a3c764042cf6937012c6bcfab521fa52691a33dc6b9d4a6306b03976a`  
		Last Modified: Tue, 02 Jul 2024 06:02:52 GMT  
		Size: 50.9 MB (50937149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf8c2787951018b599f2fe45c7b602fb869d7055657f68f3aa9d15d93def8d4`  
		Last Modified: Tue, 02 Jul 2024 06:04:55 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:714dff720e2f85485129bc4ac722b1a067293f079b43a7277b37e4868f46bdae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52278423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5804203730e8cb1fc140d06801d2cdf4f4c3e23c32e724f203fa8b0b02a9909`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:44:56 GMT
ADD file:474217365b4afce182f60b776ab37f3a44774c328ea278e1c48bc8410023f4c4 in / 
# Tue, 02 Jul 2024 00:44:58 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:47:16 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c5f70336c1fb5eed68802971c844bdd7f3b8e20b7504d889927c061344c0235a`  
		Last Modified: Tue, 02 Jul 2024 00:49:53 GMT  
		Size: 52.3 MB (52278198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308ef18c279d80e3910b05b5db87ebf840bd5bae5522aba66150dc52664fb9c`  
		Last Modified: Tue, 02 Jul 2024 00:51:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

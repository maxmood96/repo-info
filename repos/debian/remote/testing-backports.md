## `debian:testing-backports`

```console
$ docker pull debian@sha256:ee4e16b717198dde25b3540f1ecb1eb3b8271f94623d264442478a8b91d6d505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:0a525a07ad8bbfa6c61e44956787747444c4fd2de9c2d460cd2939e7be663026
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51922920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5eca466c4245c675e0437093d727d7ff1c9eebcb801e68abcce368194d0f74`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:24 GMT
ADD file:ef6d0ed43a7e57298514883c056f9c35630c293bcd6a5189ade9a7c839492abf in / 
# Tue, 31 Mar 2020 01:24:24 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:24:29 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c551897442bae279f3dc3299b5e89627f556d06912d81bd777e18eb066414c32`  
		Last Modified: Tue, 31 Mar 2020 01:29:45 GMT  
		Size: 51.9 MB (51922694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9f3509d0d7e4901d568e013123371bedfd18333aee6d0e509fdc7359df07cc`  
		Last Modified: Tue, 31 Mar 2020 01:29:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:464ca60f77a04b658ab564e2f49615d7404b01a84b8694a3520b10d2a2def617
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49920770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f66b8e614d584229e41b26d5d307d1eac0ec5682714b4532c87cc78d0ab297`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:29:41 GMT
ADD file:72432e2adc17377522ed5bd7284a99d1a306fc7fda20e3ae3ff6acb629c8373f in / 
# Tue, 31 Mar 2020 01:29:44 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:29:50 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:637393d371ef87aef232a263eaeafef838cfcdfb05f877bbca55053834c5854b`  
		Last Modified: Tue, 31 Mar 2020 01:37:14 GMT  
		Size: 49.9 MB (49920545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9df4416d89271315028297f3bf7998c92276b184a4046d3e5e87034bdb1ece`  
		Last Modified: Tue, 31 Mar 2020 01:37:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:784a4c3913c8eecf241ea96967450141132fa7a2a2486a3331d183a47f0de36c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47645880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f980e187a4684596e0f583a8d198235f84b98818f1dc74a2dfc0651219d015`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:53:13 GMT
ADD file:a6c3a50dd960803f54d78dc6a1d7fd8f910688aab796b3549ea238d1ec35021b in / 
# Tue, 31 Mar 2020 01:53:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:53:22 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1882e0424a17dfa83ea0d8c7129f15789153d87611298f92b130359227c76feb`  
		Last Modified: Tue, 31 Mar 2020 02:00:37 GMT  
		Size: 47.6 MB (47645655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6cff7a8475faac3df4b17a402856e1f16a25ea35d9fd8e2ee715abcacbc886`  
		Last Modified: Tue, 31 Mar 2020 02:00:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:38e308c3ad1dec33557ded42f6c2c73b4de6e21a094f30ae619334af74149790
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50858835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da01de20c43c7535e67796fb3559927e8ad38897a7bc5a32708762bf1948c4db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 02:09:03 GMT
ADD file:bc1f805aa9a29690e572913287441bb951b8906746724af8b91242eb4d61ce6f in / 
# Tue, 31 Mar 2020 02:09:07 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:09:16 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:83486a75c02795f350f5cf9f87dd8ff5c602a68ce117775785d6344f3ed716a7`  
		Last Modified: Tue, 31 Mar 2020 02:14:57 GMT  
		Size: 50.9 MB (50858609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873955e6a4d17fac2aa9931595c86599a59346aa9d16e0088f681f884842fb7c`  
		Last Modified: Tue, 31 Mar 2020 02:15:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:a636a4243384fe77adf5b11547e99effdde0de9e77a7480b74c73be83f598a52
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53061933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf1be8a795d472293d99884894dfbaaa0b728b84a49b89ddc360f89c299f276`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 00:43:06 GMT
ADD file:6af65e70dee2ece6c8bab709088366f7f1eb0168ca4eb5c785aa134af7b81f4c in / 
# Tue, 31 Mar 2020 00:43:06 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 00:43:10 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dc20cd2f0dca1e157deafc04af62b4b870124970dcf959af791ad62d9b0eb6fd`  
		Last Modified: Tue, 31 Mar 2020 00:49:05 GMT  
		Size: 53.1 MB (53061711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb5fe010c8aeb859753313499df261c820b3fd30f8e5eb61067ce1721700cdc`  
		Last Modified: Tue, 31 Mar 2020 00:49:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:38a8c5a0f82298702eaec61df1a085ada2347e31efc666d738ea7fca5c765935
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55810525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a443df0dd136cc4e890c12b4ce530f71e59ede62f824371391240680601f17`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:37:11 GMT
ADD file:77cf0aa70faefbfae994d0b99a486ba9898b6088a9f210c04a87d796217868da in / 
# Tue, 31 Mar 2020 01:37:19 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:37:38 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1a6dd0e62bd792646cbc752305dc49fd89fd3583c096d7978405477d6492b543`  
		Last Modified: Tue, 31 Mar 2020 01:55:52 GMT  
		Size: 55.8 MB (55810300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e20b93fe5fcfab0040a1d1db660ada700e8ab9681e42775214169025234aa7d`  
		Last Modified: Tue, 31 Mar 2020 01:56:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:cbeb5770c7c012a1a3c2e41633e4c4d759663254b077cd159fa179928187bb26
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50522847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e476ee3fea63e2705dce73221cd6edc347030eaca16399e1efbf5640e37695c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:10:45 GMT
ADD file:9282e16e5d20b602cdbf0ade679b2ac203ec4d0e0a6a32f9817ffa1a0ef3a86c in / 
# Tue, 31 Mar 2020 01:10:48 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:10:52 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8235e0dd8f7c6de8f2c09d582d564a6d032df3a51b3174b4499da5b9ead67a2f`  
		Last Modified: Tue, 31 Mar 2020 01:14:31 GMT  
		Size: 50.5 MB (50522624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f393902f20c64ce5dfa2f57b4a2ffb0907031204305905ec2910fc4ae9f63045`  
		Last Modified: Tue, 31 Mar 2020 01:14:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

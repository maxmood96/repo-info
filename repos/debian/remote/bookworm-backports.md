## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:c3e0d4c1ee12709ae26410660bc404c3b1e8044a060a3a2d0840952e0d9470c0
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:62c1fbb96a9427b6b12274d195a27068e6a5fd4dd490cd31c7e4835ed8adc537
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55754525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b442e481a91d090845ac31b569493816c7e6a56ad2b93c9f5308530370b5cfa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:22 GMT
ADD file:2a92eda55857403475e71c7e72e14b8332b700683b753b80998c67de8059b01b in / 
# Thu, 17 Mar 2022 04:03:23 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 04:03:27 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:66fb1aabb4c03c1a8502c7ab4d442a4602f465cee7eccf27eb706178ce2859a6`  
		Last Modified: Thu, 17 Mar 2022 04:08:59 GMT  
		Size: 55.8 MB (55754297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725ff4fae98b9b4e7e87e7c504958549c42a7003f6beb974f026ecc9e8224015`  
		Last Modified: Thu, 17 Mar 2022 04:09:08 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:bdf1a4c4816c7c2878916c09317e71df61cdeaeb1b3fac2f6388d7dee87c1874
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53139238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397f206d75a6838983ea89cc321f3a608c977f6d31d5e1505127d432eec663cf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:18:12 GMT
ADD file:990567084063731033d76e2ad1efcd558f47300ad1e9848197a4365f45d534b5 in / 
# Thu, 17 Mar 2022 05:18:13 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 05:18:26 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e5c18c3be596e08b764befc1ff336d017f3a31c10bf139ca155094240de76a8c`  
		Last Modified: Thu, 17 Mar 2022 05:32:53 GMT  
		Size: 53.1 MB (53139012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6b7108ce7a21826de5deb312be269032e77b6283da24d69f4dd5a83e8feecf`  
		Last Modified: Thu, 17 Mar 2022 05:33:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:6937ffe264e524d939f1d355682e060b7475f5e264479bc7d8db5cb7f889b4db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50761932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddad0a48b014e8de53833f9dcab9f0656738f956f31a3435554bc48b604949cf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:29:27 GMT
ADD file:819f7eacc6077672fc50aade09ce96ce0ef1e2b4d9bd84e706ea22d90d73799a in / 
# Thu, 17 Mar 2022 09:29:28 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 09:29:40 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7fca9c92eb5afd37d0b08a4fba4dd30ea576686d945af655ae46133854768127`  
		Last Modified: Thu, 17 Mar 2022 09:44:45 GMT  
		Size: 50.8 MB (50761706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8825d14c558fbb846f6ccde9883c7a06091b9224e67f0d97708fb57061602ae`  
		Last Modified: Thu, 17 Mar 2022 09:44:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:761af6e829cac60d186447da55a5d49264652bb65b44e2d5ca628c18e8ae3cf8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54668466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b66f05fb1a436e8a9d2c1e5ae1c1540fec752bb49bf753683b75a2073f93182`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:18 GMT
ADD file:c8087b65b6b61e4854699fe41f5bd7f307c0e0710204b586e85fd8176523d9bb in / 
# Thu, 17 Mar 2022 03:21:19 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 03:21:24 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:906df7cbb9fee5eb5d79c51ae55b6a857335ddd1b44645e3a59b3a50862f4317`  
		Last Modified: Thu, 17 Mar 2022 03:27:23 GMT  
		Size: 54.7 MB (54668239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dd22deda1593362267ffbc64530cd8a2a5ec35814b11515ca847c52547cc9d`  
		Last Modified: Thu, 17 Mar 2022 03:27:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:9a9d8d812b615c666266ae694707454d2d20048ac5e3fc545e64422ce45a78fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56786134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f5ec2567a00a28477d6c4fc2a1368f8105b1bb976711cee766d77b382c7593`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:15:04 GMT
ADD file:c9a7a9e937edd061f998b5105810e08dea3a6f43e552e3a4feaf23d0590fd33a in / 
# Thu, 17 Mar 2022 08:15:04 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:15:09 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:045d843908fafe2096fc32cf80758472d8ff231ce73aa1a0cc649fa4cb8d0e37`  
		Last Modified: Thu, 17 Mar 2022 08:22:37 GMT  
		Size: 56.8 MB (56785910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2604396e28a04d269a97ce1b010cc21febd0dd9cae95e79d6f3e493b25d1e3`  
		Last Modified: Thu, 17 Mar 2022 08:22:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:ec04aac659110ff0d16d859c8dd5fe83169023189ae9e095c07157b7fcfb4566
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54339389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20fd1f0c77bf581bc8c2f47be04361166d7c5e6aacb0d6bc2ad3b513d83199c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:51:08 GMT
ADD file:550d1d8a058f07f217e9d0ec1e582f897b1cd24ad6c6c3697d5c89039c5ae265 in / 
# Thu, 17 Mar 2022 08:51:13 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:51:33 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f4e5d74924161483e853a5bf08fcf297bf47b3124d7d1840e280c5f487a8750d`  
		Last Modified: Thu, 17 Mar 2022 10:41:21 GMT  
		Size: 54.3 MB (54339160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb49043182bf319c24e01b82b438cda684de59f98da186692abc812b40e48a4`  
		Last Modified: Thu, 17 Mar 2022 10:41:31 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:9dd5c942ab18bdc9349c14b3c629c871a331cbcb2f158d2628fbbd0dfdfc1e57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60182027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be41a91fe9bebab54b52ceac052aec7475e0909a39f39dca2b25cf199e6183ce`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 11:16:03 GMT
ADD file:f36cb09b5dc4cc09d85cfa372e4eab4761ae2e6db21140cd04ae6ac162780fa9 in / 
# Thu, 17 Mar 2022 11:16:14 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 11:16:31 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:829e07eac0f4532ec122618377e35dc25b8df14f3a8c8760107a868520ea7977`  
		Last Modified: Thu, 17 Mar 2022 11:26:42 GMT  
		Size: 60.2 MB (60181798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87437cabfd1f72e375962db8153f1e3a6b6e533d3b73c6f09c49c859bd2e7f5`  
		Last Modified: Thu, 17 Mar 2022 11:26:56 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:dee2b895786e0fb0d02e629a39f1ae3c32decd926152f1c8aad04701e4065aa9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54001147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acec31ae6f2383dfb49d4bae9891125758194a7b3fd6aa07646ebb86483fe92d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:02 GMT
ADD file:82d5e48a017e9f867dce69500059071538b25dc5395a355bb79bfed992fb8cab in / 
# Thu, 17 Mar 2022 03:06:09 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 03:06:16 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:91cc6fa8b00e7facc9855a15de9dbb6211a8692978d893a028e487ca7988379b`  
		Last Modified: Thu, 17 Mar 2022 03:11:59 GMT  
		Size: 54.0 MB (54000921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56964ce2b62dc3e1830e9d995de3ef87d18d4c3fb863c645c7bc4b6550a2270`  
		Last Modified: Thu, 17 Mar 2022 03:12:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

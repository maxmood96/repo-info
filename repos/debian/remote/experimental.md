## `debian:experimental`

```console
$ docker pull debian@sha256:bd514d8a478de46e51cb7d3dc056c20464b81d794221ab0e298d2539a80a79b1
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
$ docker pull debian@sha256:61bb4c8b0a8a8925f81269d63dfa87985812776fb1e5de5f74a60d666952bef2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49040961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954b2d3030589a7d68db242b93feb772405f1eab6bba877d02855b2cd4671b98`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:36:48 GMT
ADD file:a472be541f4793676ca4459eecc1317f0a0a37318f675b0a0fcb25651bef94de in / 
# Wed, 11 Jan 2023 02:36:49 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 02:37:01 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2ea704eb82faab6fb3931c69ced55d3151ba782c09e34f82ee3f517a70bdf0de`  
		Last Modified: Wed, 11 Jan 2023 02:42:17 GMT  
		Size: 49.0 MB (49040739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15e7038da5a7a69a3e99e905d905d9a29f88e7fa5934495fa1e4ba2c25306a3`  
		Last Modified: Wed, 11 Jan 2023 02:42:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:3179663a7e61b6b83eb09d8098b346007bb021c2aa34eba49690bfd3d3e70cda
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48018183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c9f2d7613eae444b27895c80fc3e1fcc0cb6d36cff3977bd8e71643eb66cea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 01:57:08 GMT
ADD file:f8addf0f27d3efc8283bc4e3a7ca9f06b6cc9b4fcbcd09ba7ed7d39c9c16c5a0 in / 
# Wed, 11 Jan 2023 01:57:09 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 01:57:23 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8b3394d1cdf2a55f5514dc0fddd06a144e5ef0a0ed6b78a11bb2363f9f66d3c5`  
		Last Modified: Wed, 11 Jan 2023 02:03:09 GMT  
		Size: 48.0 MB (48017961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a89375b610348f4f7c93b4fb7a666d3114a508d7b77c8e4e7e35861d6502201`  
		Last Modified: Wed, 11 Jan 2023 02:03:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:442c03e9bffb0955bbeafeb851073d4b11ce90034433edd8516f1a6866e698e2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47080907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857c22df76842a82ffb908543b5005e390469a0a147333e9694f14d5b8fd018e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 02:00:53 GMT
ADD file:930ee3b81511945e2edcb3a338f86509cc60ea700a56fbcd07cc50656542dcf6 in / 
# Wed, 21 Dec 2022 02:00:54 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:01:09 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:4f2eabba05374c21c57c8a7a2273ec974af5f0a843cd07b34fee8f5d01d8be04`  
		Last Modified: Wed, 21 Dec 2022 02:09:05 GMT  
		Size: 47.1 MB (47080685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c5a03ffd20d362f94e11512751f84da17118c4c8b0a0cc7b4de5481b4666d8`  
		Last Modified: Wed, 21 Dec 2022 02:09:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:351770a99ee8f402e1e2134044921d7fff85aa4e5da47078e62f0161448ba98d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49084770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d884efce7a0826d706d0c490e79ef96a61d863429a3ff204d43da4e575834293`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:59:01 GMT
ADD file:340469c7e9d21ec908d8b07fb16fba1e70836f1b72c18a65eda82e4aa37d7084 in / 
# Wed, 11 Jan 2023 02:59:02 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 02:59:11 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:62cda9971d1a0fbbfef8e70c8535d75041604d167dfa6996f54b284133b006e6`  
		Last Modified: Wed, 11 Jan 2023 03:04:22 GMT  
		Size: 49.1 MB (49084549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97763a913c163086254eb5381b54a88ff1472cd717e097588c0c3cfed7b6375f`  
		Last Modified: Wed, 11 Jan 2023 03:04:43 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:d98cbd4e3851de3c2dc094691d2264adcb0d89f80bfa0747256938978e728a2f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51340351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77fadace25ec54d4a429fbe7cb9f33ae821376a6f43d1af439aa2e050504b7c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:41:25 GMT
ADD file:6ffac3795480c354a83ea1968885ebf1616928a69fa293f4011e2f7613766fa8 in / 
# Wed, 21 Dec 2022 01:41:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:41:40 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b614aec88bf425675376d4c25f6a3f9d7c7e9b6d631307ea564765270b6f8c59`  
		Last Modified: Wed, 21 Dec 2022 01:48:21 GMT  
		Size: 51.3 MB (51340129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b74b9e33a0be187b745c8b6e9d6fc5fd1b2197f09988ac4195cb8441a0ea2de`  
		Last Modified: Wed, 21 Dec 2022 01:48:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:f9e06349289968e72b817e9fc0511a6059db60d427232035483bc8059c0f0fea
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50293171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75a28d29ae62f6c840a5af603020882890c8196a724cb963db47c3805b6d22c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:14:36 GMT
ADD file:d86f0e28d7ea72ca80aec16cc53a8efebf43b4802fbbed1b6452a0730f13e73d in / 
# Wed, 21 Dec 2022 01:14:42 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:15:19 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c1a8c1357338f60ee5392f4bf29f089ea8ef5e17f25a0a3f49fce091aebf025f`  
		Last Modified: Wed, 21 Dec 2022 01:23:08 GMT  
		Size: 50.3 MB (50292947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20db7e5faa75df970592e05e4ee9d6d361a077f5366dd189fd1c1647b5386cc3`  
		Last Modified: Wed, 21 Dec 2022 01:23:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:d13786dbd0794f96615d49d73460d1758b68638789e62e39e91c00f264e180ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54333208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be450ff8289b2ffa2f6fd60a6fea7cb75b0de56f30069c462563183929fa278a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:19:45 GMT
ADD file:612c98671138c70184edbcfb1f44b94a372b37b35f1c8dff90447173af466a1a in / 
# Wed, 21 Dec 2022 01:19:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:20:09 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ca12868e5e41d7731e085119b02b75faf07b2b4658b7358f856ec9071294c19c`  
		Last Modified: Wed, 21 Dec 2022 01:26:12 GMT  
		Size: 54.3 MB (54332988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e0c38f047a733206800328e3128eea83c8be7aa2833a96e617ee463866bac5`  
		Last Modified: Wed, 21 Dec 2022 01:26:42 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:ba5cb019da23d5fa175c5e0edbf7358d27e05768ed3086bc9945890bc808d178
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46453774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e89a88090721ab9591f082335fa251eb936435b61c5ad32822be7ac5c4e132`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:13:00 GMT
ADD file:27d33d404549e4270b8c18ff79b55c32563a2158aefa90426337e47b36c81041 in / 
# Wed, 21 Dec 2022 01:13:02 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:16:17 GMT
RUN echo 'deb http://deb.debian.org/debian-ports experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:90f749bea8c8145751b0e1cb50ea7f16f0f18855f572fb4f1ffe67ceb9d6d7db`  
		Last Modified: Wed, 21 Dec 2022 01:30:24 GMT  
		Size: 46.5 MB (46453544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ee7be808be18abe9a9090f32b38245347c9e366a0d55cf87411793a86c61c6`  
		Last Modified: Wed, 21 Dec 2022 01:33:22 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:b9cf6538294881b8d7727c53a17a525afddd2d464be92f9436e9faa97fa2a25f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47434307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa52dd895d0ea4b580208ac14a2b650d5053cf58a8315ff74363239763b7d4f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:24:11 GMT
ADD file:8a39e7d372aafafec15540b4371fb3e5d10767a2938856a7ec6d49761815a2f5 in / 
# Wed, 11 Jan 2023 02:24:15 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 02:24:32 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:83741c7534d43b1ff77d8fd7a8f11f5add467189dec5a410d7310b6c372f90d2`  
		Last Modified: Wed, 11 Jan 2023 02:28:24 GMT  
		Size: 47.4 MB (47434087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4932f50c96a8d8f03b99575743a0d2b45c868e3b23953a2675fcb89af53b09`  
		Last Modified: Wed, 11 Jan 2023 02:28:41 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

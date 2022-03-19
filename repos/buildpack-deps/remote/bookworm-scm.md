## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:1d66b3d648b57f8921bd8195eae578a1656de1d4381aa15430ae632df0343211
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

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fbd4faff4c64adff22f06291f00419d9295fe4ab7516ac5d2cc2622b922258da
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129398024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658015c41cfdf4734192f825e3f9f197a271f389ad0dc38eaa2780e5ff450c72`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:22 GMT
ADD file:2a92eda55857403475e71c7e72e14b8332b700683b753b80998c67de8059b01b in / 
# Thu, 17 Mar 2022 04:03:23 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:27:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:27:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:28:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:66fb1aabb4c03c1a8502c7ab4d442a4602f465cee7eccf27eb706178ce2859a6`  
		Last Modified: Thu, 17 Mar 2022 04:08:59 GMT  
		Size: 55.8 MB (55754297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeea17ea14a09712ca5b490a0c64f57af435ba10cdb9a1a7c56af17b85ac9361`  
		Last Modified: Fri, 18 Mar 2022 07:01:56 GMT  
		Size: 5.3 MB (5270513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72b20718d5e8e4adb64ab4e1a41c30a4e311400c1e600e19792c50c1522420f`  
		Last Modified: Fri, 18 Mar 2022 07:01:57 GMT  
		Size: 11.2 MB (11186321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fce5439f6b2566f7bd6851706b38c1201c994ac1ec57ad8725cb0f08c28be9c`  
		Last Modified: Fri, 18 Mar 2022 07:02:17 GMT  
		Size: 57.2 MB (57186893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:691d785e88a68815ccb914e95dfa26df316fee9b085e5d9cb2c67680b7c078e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123701441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18b1f6a378157830f90ca3105df8bc94685cf66569201053164736fe73e4620`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:18:12 GMT
ADD file:990567084063731033d76e2ad1efcd558f47300ad1e9848197a4365f45d534b5 in / 
# Thu, 17 Mar 2022 05:18:13 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:11:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 19:12:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e5c18c3be596e08b764befc1ff336d017f3a31c10bf139ca155094240de76a8c`  
		Last Modified: Thu, 17 Mar 2022 05:32:53 GMT  
		Size: 53.1 MB (53139012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0040329b3b511cc0d15a0ae2eb2bbcd344c2c8291532ddd0f333b1e142b464`  
		Last Modified: Thu, 17 Mar 2022 19:37:02 GMT  
		Size: 5.2 MB (5169031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c800c571bbaa0a9c8eae64db9691f97d467f0bd06250b5da62e182b97753f497`  
		Last Modified: Thu, 17 Mar 2022 19:37:04 GMT  
		Size: 10.6 MB (10579460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c11a7f3fcd6560f12b114a08e246f8b4f4e6893de096371b829d51f149731af`  
		Last Modified: Thu, 17 Mar 2022 19:37:53 GMT  
		Size: 54.8 MB (54813938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:66bae13fab412347a2cbfb241f5efc782ae483eab0ef04602c7f2c56ab69a114
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119096156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc57abffc4609497efa38a7ebb3d2388189066f8a44fdbabf5f73731b87e504`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:29:27 GMT
ADD file:819f7eacc6077672fc50aade09ce96ce0ef1e2b4d9bd84e706ea22d90d73799a in / 
# Thu, 17 Mar 2022 09:29:28 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 02:48:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 02:49:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 02:50:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7fca9c92eb5afd37d0b08a4fba4dd30ea576686d945af655ae46133854768127`  
		Last Modified: Thu, 17 Mar 2022 09:44:45 GMT  
		Size: 50.8 MB (50761706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5383ea443f2740a52246a5eee4a417a2b1244a1f912208d4c96428520670a4`  
		Last Modified: Sat, 19 Mar 2022 03:26:13 GMT  
		Size: 5.0 MB (5030714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d3f50feb52a7829302a09f9e4f362e90c5b18f7be314c43c43c6b1cbb89dea`  
		Last Modified: Sat, 19 Mar 2022 03:26:14 GMT  
		Size: 10.5 MB (10475768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66566945e25367a4d188cff5f444e5c148cf8c32c44b9a8b417c7c6950ce026`  
		Last Modified: Sat, 19 Mar 2022 03:27:01 GMT  
		Size: 52.8 MB (52827968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9663cd5092c2ac699e9d940b6a868933053ad1f1276e0c322b240191989835ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127823810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9597b8d3b875c18ffcaaed1c710cfca60cb6101b8a9503e9c66fdbc35df501`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:18 GMT
ADD file:c8087b65b6b61e4854699fe41f5bd7f307c0e0710204b586e85fd8176523d9bb in / 
# Thu, 17 Mar 2022 03:21:19 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:08:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:08:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 22:09:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:906df7cbb9fee5eb5d79c51ae55b6a857335ddd1b44645e3a59b3a50862f4317`  
		Last Modified: Thu, 17 Mar 2022 03:27:23 GMT  
		Size: 54.7 MB (54668239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2bee854a2c1d4d436485263d8648a3eb5c0a4cdc26326102c680903b409889d`  
		Last Modified: Thu, 17 Mar 2022 22:19:48 GMT  
		Size: 5.3 MB (5256412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f88519bd8fe148fde1d5a9917fbea41afdd523e19fcecf2dc8f2f39c86cfbe`  
		Last Modified: Thu, 17 Mar 2022 22:19:49 GMT  
		Size: 10.7 MB (10676785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679d36783a2b174a0e8ee03bc292d3fdd5d57461299a881aa3561e5313ff763f`  
		Last Modified: Thu, 17 Mar 2022 22:20:09 GMT  
		Size: 57.2 MB (57222374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:282028c0911e5e1109abb2e472121f347283a2dbe39836b2cf5bf66630f059c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132386029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12761bef49ae4395b5c1592d2a37c856eb004153a418ae7df3b75a1d41c6e6c9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:15:04 GMT
ADD file:c9a7a9e937edd061f998b5105810e08dea3a6f43e552e3a4feaf23d0590fd33a in / 
# Thu, 17 Mar 2022 08:15:04 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 14:25:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 14:25:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 14:25:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:045d843908fafe2096fc32cf80758472d8ff231ce73aa1a0cc649fa4cb8d0e37`  
		Last Modified: Thu, 17 Mar 2022 08:22:37 GMT  
		Size: 56.8 MB (56785910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a0b6dcc5493b8666da65f0faac2f840449310f2870d5182a9dfa3fcb71e4b6`  
		Last Modified: Fri, 18 Mar 2022 14:42:01 GMT  
		Size: 5.4 MB (5401951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c538217939c052ebc81d9422f1b5cb8bd2b1994fd5386f00b69b05322dbf99e3`  
		Last Modified: Fri, 18 Mar 2022 14:42:02 GMT  
		Size: 11.6 MB (11594126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2882b228853b6be840a3097da97d1aa9612a648702d39d367b8e1850b7146830`  
		Last Modified: Fri, 18 Mar 2022 14:42:33 GMT  
		Size: 58.6 MB (58604042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:09b11a97a1fdf943f8eee722c062da1391c1cff5cb4967c5510541ff65525702
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.1 MB (126147721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6d9b482ab5a47c29d6026369929be54e0fed6a46df862c1e166faacae8550b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:51:08 GMT
ADD file:550d1d8a058f07f217e9d0ec1e582f897b1cd24ad6c6c3697d5c89039c5ae265 in / 
# Thu, 17 Mar 2022 08:51:13 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:10:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:11:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 19:12:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f4e5d74924161483e853a5bf08fcf297bf47b3124d7d1840e280c5f487a8750d`  
		Last Modified: Thu, 17 Mar 2022 10:41:21 GMT  
		Size: 54.3 MB (54339160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88c2306400a47802f9098940358dd510c9d432998ff5d8b9ef4eb54da37c1b1`  
		Last Modified: Thu, 17 Mar 2022 19:47:35 GMT  
		Size: 5.2 MB (5225142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894a35eaaf609861da62a9d25299ce8269925d4e205b08c5c62d7e99d19b7d6f`  
		Last Modified: Thu, 17 Mar 2022 19:47:38 GMT  
		Size: 10.7 MB (10654797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8024f4d3131917cacabab09dbe180853b42f8410b118be783211c6db8a987f9a`  
		Last Modified: Thu, 17 Mar 2022 19:48:25 GMT  
		Size: 55.9 MB (55928622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:06e4870a4a2e294b7284a317b5c0834909295a2dd8c09e09bf12d49205c20fd5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139638128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfb6e7a411e5d97e100d014eb5d96aedec1a3c0f4c3591e588067730c64129a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 11:16:03 GMT
ADD file:f36cb09b5dc4cc09d85cfa372e4eab4761ae2e6db21140cd04ae6ac162780fa9 in / 
# Thu, 17 Mar 2022 11:16:14 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 05:28:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 05:29:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 05:30:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:829e07eac0f4532ec122618377e35dc25b8df14f3a8c8760107a868520ea7977`  
		Last Modified: Thu, 17 Mar 2022 11:26:42 GMT  
		Size: 60.2 MB (60181798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6b3254a8b049acdfea0695e77b1a65674284fb016e967d686cd004440b01c8`  
		Last Modified: Sat, 19 Mar 2022 06:36:37 GMT  
		Size: 5.5 MB (5538587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4496ff18aa5cb8cfce7705eb961453fcba1af247cee4d0ead60d54b6fdebda`  
		Last Modified: Sat, 19 Mar 2022 06:36:38 GMT  
		Size: 12.0 MB (11998277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9c5aeb5958db68933e2187c1ff6579c1f3c96b4e0fe8c7d451d5628430942b`  
		Last Modified: Sat, 19 Mar 2022 06:37:35 GMT  
		Size: 61.9 MB (61919466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b5d57020bf7d82becf0eb6cb8ee79dbc249a40c06f9571cb616e8c31c33b721c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126615494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a78f49734fdca9d2c21da03858e07c0ab4453b6a8e49addbe3bde606ea4326a7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:02 GMT
ADD file:82d5e48a017e9f867dce69500059071538b25dc5395a355bb79bfed992fb8cab in / 
# Thu, 17 Mar 2022 03:06:09 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 18:19:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:19:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 18:19:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91cc6fa8b00e7facc9855a15de9dbb6211a8692978d893a028e487ca7988379b`  
		Last Modified: Thu, 17 Mar 2022 03:11:59 GMT  
		Size: 54.0 MB (54000921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2c6272c85978c4b20b105a7a33a11881628bc38840c72128a526cdc6b709ab`  
		Last Modified: Thu, 17 Mar 2022 18:28:20 GMT  
		Size: 5.3 MB (5250449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900da87743fe44ae1fee0a700fae42c07e9ade18d95f98fbace40ab318fb4846`  
		Last Modified: Thu, 17 Mar 2022 18:28:20 GMT  
		Size: 10.8 MB (10803619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895f1b87cddc9e80df0130457e34d2b02b2e3a3700aab72bc40ee7ce09612250`  
		Last Modified: Thu, 17 Mar 2022 18:28:33 GMT  
		Size: 56.6 MB (56560505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

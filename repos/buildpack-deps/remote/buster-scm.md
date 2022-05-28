## `buildpack-deps:buster-scm`

```console
$ docker pull buildpack-deps@sha256:3c2f331e6746f61dae06d1e2655ddc3b45b0e59018c0f249c91693026791ed4c
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

### `buildpack-deps:buster-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:276bfcd0bff770d50b10bb35b9bf3a7639b1a462796f76cccffd93616d7d0461
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120138076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8c4fbe4ba8bf86b127414fba2bda9a56e928245f0d1d91b1f77cd7d7dca2f4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:32 GMT
ADD file:5c5cde050dbdbd5c7c0d9c723f436d37ab4a8b1a498647a719771eccce99d9cb in / 
# Sat, 28 May 2022 01:20:33 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:42:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:42:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:42:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:982cba7e471c6d3ce96014cf58b2e4e115a525e60da2e1e08716818f2c057a6b`  
		Last Modified: Sat, 28 May 2022 01:25:39 GMT  
		Size: 50.4 MB (50440422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02d86f59850f3e13d394072350625a8526b912af24b3bfc0e50e9a8862a79d0`  
		Last Modified: Sat, 28 May 2022 02:50:21 GMT  
		Size: 7.9 MB (7856653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b047e8f2e47bdf998a952572ae5e9d64edf8e29b716be0ee50a15e6d21cb2ce`  
		Last Modified: Sat, 28 May 2022 02:50:21 GMT  
		Size: 10.0 MB (9997224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478cfe935c2fb922eb2a95131ad8a2f1e6ff472bbdecdf94709edc3a85f74dfd`  
		Last Modified: Sat, 28 May 2022 02:50:38 GMT  
		Size: 51.8 MB (51843777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:2b6b36741047f18523b10a87d0e6c1f40662c5ad95708a36645303e7f8f188e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114829480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15df936ed63ad08a25128c9ad00ddf565cd09217b42e66e338638c6f72edfc8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:51:01 GMT
ADD file:8292d961a3aa3c4584c010be23306dbea6f52d4f69fe30d2b3ae6d2f8cb91f98 in / 
# Wed, 11 May 2022 00:51:02 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:10:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:11:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:11:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c49f9a696043c9b0e9c645a07e1bd105d319cdcc2a580c36b676431549349006`  
		Last Modified: Wed, 11 May 2022 01:06:38 GMT  
		Size: 48.2 MB (48157520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e1558e9432b31779c9f8031852fa3d04976b885da3cb16b17df0306315d71a`  
		Last Modified: Wed, 11 May 2022 02:33:16 GMT  
		Size: 7.4 MB (7400470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a934c6b94649dc17b407a076ca8c0c7bcec34754b3ebb8a184af9bdd71a7b51`  
		Last Modified: Wed, 11 May 2022 02:33:16 GMT  
		Size: 9.7 MB (9687677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaaace8b36f9b1d3eb3b5996d8ce055793ead0ddf31c444be7594a8310b7860c`  
		Last Modified: Wed, 11 May 2022 02:34:03 GMT  
		Size: 49.6 MB (49583813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ca51bc421b88bd23bb9aff1c1a38dc3ba93f582f4fb08e88a6be213aa9cefe53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109758247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b42918712dd3d1b48fe99a2bafa66ad0d65fd903eae126226f3f5bd2951afc6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:49:37 GMT
ADD file:9c75d7f24328b3f84cd700813a0a8ff5af16399f4475d24da9b0a859d584614c in / 
# Wed, 11 May 2022 01:49:38 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:25:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:25:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 03:26:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f328f2671b27c760193a9d82808b176a8a7420205e8eb884e1fee20d2ac57ff0`  
		Last Modified: Wed, 11 May 2022 02:05:20 GMT  
		Size: 45.9 MB (45910176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e554a91160b4bf86ab199d7a5f5f105c5ffecc37b098c4274d98c264f677799`  
		Last Modified: Wed, 11 May 2022 03:49:35 GMT  
		Size: 7.1 MB (7145025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1b07ef419c0604851908ed718983760891b21a649a1b8758b871522e7d3e48`  
		Last Modified: Wed, 11 May 2022 03:49:36 GMT  
		Size: 9.3 MB (9343816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398961d3cf225ff82b93bd457012e308b756c455d1dbe1191bca51a54483f1d7`  
		Last Modified: Wed, 11 May 2022 03:50:19 GMT  
		Size: 47.4 MB (47359230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:640d49dc7639215beb5f9b1590a6ce26492140219e8a9cf0ef6e5bfdfc6960d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118890205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa36a71cdf20adb10f0efa0a17f6531e6a1f4a376e8b812af5c38a025b0d2698`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:47:11 GMT
ADD file:5389b77733b44ebc41850baff3ebfc491726af264a745f108d5f16076a0f04ab in / 
# Wed, 11 May 2022 00:47:11 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:26:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:26:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:27:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5528d23e3f315103c99c14258e007a025d09bb4fd587c2d8a32d6dbb6047b891`  
		Last Modified: Wed, 11 May 2022 00:54:09 GMT  
		Size: 49.2 MB (49228300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b2d66a1dbe5960c6de4181ca3512467d3303dfb9cde3d92ecf7a85111cf68b`  
		Last Modified: Wed, 11 May 2022 01:37:01 GMT  
		Size: 7.7 MB (7719789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9244ac9f9851b43ddc1032930666d339c3a5d9b934e2ca42ecd2e8ef3dd680`  
		Last Modified: Wed, 11 May 2022 01:37:01 GMT  
		Size: 9.8 MB (9767329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06885dc77f03f05a5f98ceb35e871f027525d932d32027ed9d4ffb0cbd29786c`  
		Last Modified: Wed, 11 May 2022 01:37:21 GMT  
		Size: 52.2 MB (52174787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5ad20a1ceb888a167db5224adf12929d9bfbf7a4c6d659591b682c64734a893b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122792730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26fae3e495734e0ab20f81261a8c746665577d16eca5a76c375f9a42320ff9a8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:39:45 GMT
ADD file:3995ccc1e3f12a1e3f28dd818223bdc5454a7651248bfb98fae7c14961c49bba in / 
# Sat, 28 May 2022 00:39:45 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:12:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:12:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 01:12:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:045913a916496008850e7e3b499b9acc93c72b4018eda833a11c562a6d8413b5`  
		Last Modified: Sat, 28 May 2022 00:47:08 GMT  
		Size: 51.2 MB (51204248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8b88cac678bf7c61d66ca5c565ceb244ff4764b8651c88bf3e1ae159872dd0`  
		Last Modified: Sat, 28 May 2022 01:22:38 GMT  
		Size: 8.0 MB (8022586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfbc00efc59e7dbf25d25c6c5d412bc1115e1d5d65c61cb6e2c9d65b1f39faf8`  
		Last Modified: Sat, 28 May 2022 01:22:39 GMT  
		Size: 10.1 MB (10121911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7916ade5bb54b5ab127448e4b330bab4425569af949deb035ba142298784c147`  
		Last Modified: Sat, 28 May 2022 01:23:00 GMT  
		Size: 53.4 MB (53443985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f9a52cceab91c5239f79cbdf2cdf184a22c5d6a8128fec2737ee3a9d71babb14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117007838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805510241fb709c471a57bbe173e3f678392e30f470657ccc0af595d4261bd03`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:11:47 GMT
ADD file:e86c610403bdbc84066b42627ffdf92eb051badd2f3d1fcc964fba096215c297 in / 
# Sat, 28 May 2022 01:11:52 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:03:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:03:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:05:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ab17b7e8f7dffe546de1529b66b42c5d3aaa0aca409effcd962eae29b834d3e`  
		Last Modified: Sat, 28 May 2022 01:22:17 GMT  
		Size: 49.1 MB (49073373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d8359db5e9434db65ff74cbeb6fb2a3c11834bea89c8bc0c7a81edce49d561`  
		Last Modified: Sat, 28 May 2022 02:27:30 GMT  
		Size: 7.3 MB (7272979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11e4fd36af841919e6113b762dace3a649390107a2ed9224e952e9b71cec164`  
		Last Modified: Sat, 28 May 2022 02:27:30 GMT  
		Size: 9.8 MB (9800289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4e1559e22aa070dc273c40b7ca110c836f73f219de789819c50db5abf12294`  
		Last Modified: Sat, 28 May 2022 02:28:18 GMT  
		Size: 50.9 MB (50861197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1980bc0e75071b7f56f4b904fa1621f99b9a8c2d9f9a98b5ba769cc99a1edcc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130649782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1e01be55616016a8611d47c905dbd8fd15057485f6b630d5c55ee72a52878c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:32:53 GMT
ADD file:73ff2a18e50b226a862b74c50f091d80ddcd29f404879c4937887c560fdf624d in / 
# Wed, 11 May 2022 01:33:00 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:54:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:55:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:58:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:88d357d3afb8b0de721a4298ddb31fe73077663376e53d241a3d5217080e1f73`  
		Last Modified: Wed, 11 May 2022 01:43:32 GMT  
		Size: 54.2 MB (54170196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad446f507e97c97d9b6d29a8cd467c962ad6b7baa48356927e7afec937107eb`  
		Last Modified: Wed, 11 May 2022 03:49:39 GMT  
		Size: 8.3 MB (8293358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8784653a0c174d00c413056e723bd1a8692a8c27bfbe6508e37152d86bb395f4`  
		Last Modified: Wed, 11 May 2022 03:49:39 GMT  
		Size: 10.7 MB (10727832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8e974e0992db0fc98b88da2883b630af2407799183b4fe45d51e044b60ccf7`  
		Last Modified: Wed, 11 May 2022 03:50:04 GMT  
		Size: 57.5 MB (57458396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cd76bcc1cecc0df304ca25714f105dc1d765a61f33bceb8f69e399ab867573fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117696451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686b6ad0d61ba5e1e4f6a8caeede5b4788494797b1e015963b82c4848dfa5edd`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:43:20 GMT
ADD file:65712051a170cb9d0b18d0085bc26171598119b8946fa55b5ee959661b48a5d2 in / 
# Sat, 28 May 2022 00:43:26 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:25:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:25:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:25:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:771d2d61f47933c8d05a5f7e35dcb16848a6225e7531db8e5971d528982538e9`  
		Last Modified: Sat, 28 May 2022 00:50:02 GMT  
		Size: 49.0 MB (49006810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df770b877bc8966d8f5d52cb3a7ab3f8bbd879f885cd61e637b2561657af7817`  
		Last Modified: Sat, 28 May 2022 02:36:01 GMT  
		Size: 7.4 MB (7423705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfa8ac3a66d83a9351be236e2dad0b6305f4fc7f162891629ed852f205e884e`  
		Last Modified: Sat, 28 May 2022 02:36:01 GMT  
		Size: 9.9 MB (9883325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bc90555bb48ea3318f33a26a32ad4a827ace919e55dd094bd11e93c555a857`  
		Last Modified: Sat, 28 May 2022 02:36:17 GMT  
		Size: 51.4 MB (51382611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

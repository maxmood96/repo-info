## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:b6b102e4990f41c7bb99b002fee5c45995ea53fa96b7133045bad4c24179bb7b
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

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c80788d67dc0882a20d88fa5159539e04898fe3a7960766921a4b15f69806133
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120135318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b79cdd308968ac158a3dcac083f82bc1391e366152af4335dfcdd0a7d3a19dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:20:26 GMT
ADD file:54d60144d251caa916ff50606bc2364131d47d6b10ed83d08c81c647ab56cc40 in / 
# Wed, 11 May 2022 01:20:26 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:50:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:50:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b03a94565ecb6e02edf716307f25a0ea5090e3e2f7acec6a3687b95415378a30`  
		Last Modified: Wed, 11 May 2022 01:25:33 GMT  
		Size: 50.4 MB (50437966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7bcede80b1916d73be58ae0a2af8321770c4ce0c8ada05c39271e292355325`  
		Last Modified: Wed, 11 May 2022 01:58:28 GMT  
		Size: 7.9 MB (7856436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37471fc83c2dc382a8aec5dc1c1f0f2f8156f4df529cd1aea7647cbaee4b25fa`  
		Last Modified: Wed, 11 May 2022 01:58:28 GMT  
		Size: 10.0 MB (9997259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0162432a49c07aa492d3e1031af58a9a9f9b22acde859829434e5a54d019aa1c`  
		Last Modified: Wed, 11 May 2022 01:58:46 GMT  
		Size: 51.8 MB (51843657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

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

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

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

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

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

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8d3629e9bc6e29ecfcfa1c9ef5a6ce688959dab147551cdf90306294631ae899
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122786313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98e27f00c637590b9717865dff2217543ef9df45ce0fae8742b26138497bcd8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:39:25 GMT
ADD file:03855eb19b36aa184d26264c1416a11ac7661faddae3436aad12661bb4c6e656 in / 
# Wed, 11 May 2022 01:39:26 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:12:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:12:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:13:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b096db137216fbea3d646b6cad3959b69b6a1d27ff5f31bd01048df4a7e6c0a`  
		Last Modified: Wed, 11 May 2022 01:46:53 GMT  
		Size: 51.2 MB (51199249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aea31d1a573a95302db6857fc201016b7c6b8f21d0f56e011ec26f49e9d36b6`  
		Last Modified: Wed, 11 May 2022 02:23:08 GMT  
		Size: 8.0 MB (8022259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1841293ac8ab91433085e85c8c899e4324ca8f84a2cf4300cb5410542e39f4`  
		Last Modified: Wed, 11 May 2022 02:23:08 GMT  
		Size: 10.1 MB (10121987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c221acbd6711627d003a42bc75312b3994313814f1ba7a82f10f1e0e37b30b8`  
		Last Modified: Wed, 11 May 2022 02:23:28 GMT  
		Size: 53.4 MB (53442818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7e69c5e84b1896b76c12d9b4183f408a2dd559c17b68ced2ca1cb547ebc84f48
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117008271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a950ca7cabbb98139a0498fb3e5b57baa6acacc1d08efda0b78751c2db72b493`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 02:24:09 GMT
ADD file:8196bde1e8989094969bcfd079f2fceac263a32d24556ea55bb20a53b915b112 in / 
# Wed, 11 May 2022 02:24:14 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:16:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:17:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 03:19:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:737cd4f99975def8d1d06011f9f8adfb43e6149a232c24f0bcfac82bbb3d809c`  
		Last Modified: Wed, 11 May 2022 02:34:25 GMT  
		Size: 49.1 MB (49073768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5aa50fe74813ad1c212b9d93aaec284182c36ee0a9c1396c829c0cb4a914c3`  
		Last Modified: Wed, 11 May 2022 03:40:26 GMT  
		Size: 7.3 MB (7272760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e33346bc90837c57612ab94c57f4ada05199130494a326a1c665e9d38811a8d`  
		Last Modified: Wed, 11 May 2022 03:40:26 GMT  
		Size: 9.8 MB (9800318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e4fc355d43116148b88c95ecf294b953540521f03ba2ff14441034f5a10b6`  
		Last Modified: Wed, 11 May 2022 03:41:12 GMT  
		Size: 50.9 MB (50861425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; ppc64le

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

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a9275d55922b58ddce43da1a00c1b0a52c9f8b3fed2dfc53acea10ddeacbebd8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117689154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2b29fdcccfd83a184b0772093f9d687d98b12396c13993ecb73aff9dd0437`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:44:30 GMT
ADD file:07d3aef2824f4da48dcf6a17e3ce265bea63e6140027ebee5f70b13eecd9a5fd in / 
# Wed, 11 May 2022 00:44:32 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:16:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:17:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:17:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:af98d4d7820a7b3b0a2afec4a171d8071d01877d1ce618b888a5a3c404ee8648`  
		Last Modified: Wed, 11 May 2022 00:50:25 GMT  
		Size: 49.0 MB (49000380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0761beea0e804b4a5a7dd37c5da5cffa31a45f325fe7c770cc1c3715ae3276`  
		Last Modified: Wed, 11 May 2022 01:25:43 GMT  
		Size: 7.4 MB (7423580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a570562b6ab9a24ab0bb1315e332237b14913dcc94de19fdf130826c8f5fb5a`  
		Last Modified: Wed, 11 May 2022 01:25:43 GMT  
		Size: 9.9 MB (9883171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d536289d3aa14d9486b1863430b9752f3884a4ed0dc74f4e73ce7355514e43d`  
		Last Modified: Wed, 11 May 2022 01:25:57 GMT  
		Size: 51.4 MB (51382023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:35c0bb4c15da53b94cac17182dbefaf4a89331ed913b20a7ab9b1ee948ccee69
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

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:55138634169afcaf8baf30a15f982e275ae8d8dfe6faf653aacdedde91cb2950
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137747718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475b30305b46bba3d41b5724d92aa12b1de528fd0e25464499ea43a2689b0ac9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:24:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:25:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be374d06f38273b62ddd7aa5bc3ce3f9c781fd49a1f5a5dd94a46d2986920d7a`  
		Last Modified: Wed, 10 Apr 2024 05:35:08 GMT  
		Size: 64.1 MB (64140565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6567d08469639bf81018900f69b5fb706ec25fe62145c4cd9cb769f96bdc3e97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131556986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9814788dea5ba907b2dad4091f56a21b042e991dde5c18ff6c822d1ccc68b669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:48:43 GMT
ADD file:b0965dc0b90d6c10055f9e01eee401939303a005eff01dfc0ac17671ac10c89e in / 
# Wed, 10 Apr 2024 00:48:43 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:43:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:43:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:db9b031fc6f21cd210f5feeda489a6e10c26355e778fbdaeca7ec9da4a730942`  
		Last Modified: Wed, 10 Apr 2024 00:54:05 GMT  
		Size: 47.3 MB (47316142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ffbd9696eb657ee7a1f58c3ba55b7068e9217f964a268f6c9f74a7dd54e30c`  
		Last Modified: Wed, 10 Apr 2024 04:55:15 GMT  
		Size: 22.7 MB (22725022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a129a04f2d6b83a7f3a316a17496ec1b1a884022ea93fc33decc4cb7520e38`  
		Last Modified: Wed, 10 Apr 2024 04:55:38 GMT  
		Size: 61.5 MB (61515822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ffe584719ae34c9007d522ecba57a0a557c03942015db96d9f3d7095175d06f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126322202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619a7d793881392cecaaca32283c00e4e4781cc30fa4128e34e1b3597083236b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:54 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Wed, 10 Apr 2024 00:57:55 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:42:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:43:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea816b946832e576a6e2cfe5a7a28caeea429092724dc7daabb1e183ddd4817a`  
		Last Modified: Wed, 10 Apr 2024 07:00:21 GMT  
		Size: 59.2 MB (59213244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f57830e97e105bffa0968c7119ea811dd637c63961568447f6bcd7ca7cb13093
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137170129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f170e9739ef64dc0fe1983446577b2d0ed8efb8661eae7384d4775c2cf2b093`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:22:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:22:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421c44fab18bc9f4c62ca481e074d50b3a036e7c95c7607b6d036c34d67c5264`  
		Last Modified: Wed, 10 Apr 2024 04:32:17 GMT  
		Size: 64.0 MB (63990996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:259303ac5a8f163d58d9a8d29c50524cba9397a55bdc804a941d92e948500f3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141459038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c84e03f1be24e737f68da66f02beec3754ab55c318160961131399920642fb6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:56:58 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
# Wed, 10 Apr 2024 00:56:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:53:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3845b288d815c745f12b9d8f5713e916e9d585644e3574c14b698e39da51082a`  
		Last Modified: Wed, 10 Apr 2024 08:05:45 GMT  
		Size: 24.9 MB (24884730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e5c516778392288fdc27cfc451916d0d1153e04fbb6687af2b9622dea744f5`  
		Last Modified: Wed, 10 Apr 2024 08:06:09 GMT  
		Size: 66.0 MB (65987074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ec7d8d2bcbf996999928dfb4a7cb55881b3526cddc7a6b496c4e9d8baf76ca29
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136163705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0096b3e0032be86a05298f9e076ce0af1697b781d97ba1f5679d284894d362`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:09:22 GMT
ADD file:236d3683476bb8b0b7aeab0fd57eb85cfd2718deaba78d6113f3cfd93778c6ae in / 
# Wed, 10 Apr 2024 01:09:28 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 15:11:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 15:13:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8d3071232c2d967757129e1e890a482a53bf14992ca2a151a61f4661b0ac445c`  
		Last Modified: Wed, 10 Apr 2024 01:21:15 GMT  
		Size: 49.6 MB (49567247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6c10adc206ee143e79f0f22af100821851954909d39ecb2784d730c08e7d42`  
		Last Modified: Wed, 10 Apr 2024 15:46:22 GMT  
		Size: 23.6 MB (23630649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59038da844051badb769294af562fc6d5228b2a6133802cc157f8ba7e99b38a6`  
		Last Modified: Wed, 10 Apr 2024 15:47:16 GMT  
		Size: 63.0 MB (62965809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a1bab58e7bb59b2cb3164a22fe8fce6cd32a4fb70bdc83667c3da79827f89ae8
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148840229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa475b0f1d5e0969185166382a3fc05baf42f087b96d6a35b0989ec5baa8847`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:26:15 GMT
ADD file:12519205a7ecc1a9b92b9b26c967bf9f7204f2e0b9c81cb9a147b10a29b0715c in / 
# Wed, 10 Apr 2024 01:26:17 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:28:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:29:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6dcf23c0df5604eb9aa3050ab9c36d44dec4ab1448d2c229f4beaaf0f7fa503`  
		Last Modified: Wed, 10 Apr 2024 01:30:37 GMT  
		Size: 53.6 MB (53562477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9a49dc2918c681cd1306002e0306d198b0ab9f74366235b251cb85c930eaaa`  
		Last Modified: Wed, 10 Apr 2024 07:16:20 GMT  
		Size: 25.7 MB (25696598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7558a95a0d29869e7f316194c1d23abcbbe4d8c3340f4d3103f670b9d4af3eef`  
		Last Modified: Wed, 10 Apr 2024 07:16:43 GMT  
		Size: 69.6 MB (69581154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d9f5c148cf2b28bc0ff3f0c998a4a5663b076bbbdac23b35b8ebcdb539a99123
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135093126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca5437119de04081f9b59f5ba0b70fe0012a48fd7491690c86397d5484c4603`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:11:40 GMT
ADD file:4b6b256d3328c1d19403b3eb0f375b5d33724b65f790edd27be4adca49c66e4b in / 
# Wed, 10 Apr 2024 01:11:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:50:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:51:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:17f5c0a7be3d447b0aca6569b534fabcb69c578072a0cdb81f078fd4872eba70`  
		Last Modified: Wed, 10 Apr 2024 01:48:11 GMT  
		Size: 47.9 MB (47922706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a94fdcea32a650c77c01028838d670a5840f3ead5a1cf5526e922967f0df66`  
		Last Modified: Wed, 10 Apr 2024 07:30:52 GMT  
		Size: 24.0 MB (24043531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdaec0019454e24574ad418259f50f0d68508dcf92f31f05ca5d5ad33dcf43bb`  
		Last Modified: Wed, 10 Apr 2024 07:31:10 GMT  
		Size: 63.1 MB (63126889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

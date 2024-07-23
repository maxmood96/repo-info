## `debian:experimental`

```console
$ docker pull debian@sha256:d9ee9623ebe5e26814bb43d9af5b27c1dc3b05b9254239d7ee04cebac5678f95
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
$ docker pull debian@sha256:a9c6cd2bde08c29772e2c6083180525c3a0b72be7356b6bb38589823a2255ade
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52634801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39577cfc514165db95b786a0fc4a3ea540b09b54259c2659e0ce669b4a0740b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:27:23 GMT
ADD file:a1ca0b73691fca25554e4fe69ba4bf9645767248dbac7a4fc08739a03a5a48ec in / 
# Tue, 02 Jul 2024 01:27:23 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:27:37 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:91e525dba966e81e964d726faf9cf6bccf6540de433804618e2fbc398a705f15`  
		Last Modified: Tue, 02 Jul 2024 01:32:17 GMT  
		Size: 52.6 MB (52634582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fadc00186fe87882f76212226f4f4ff1338ad8e70e01b46212bc8d1905da6b1f`  
		Last Modified: Tue, 02 Jul 2024 01:32:40 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:b4be955acce84a54996a66b1ddef6208a730df64edd7c16cca82c79075ff78b8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49829070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ce57ee8b511589e7f5fef09dd2f5ecccc2ec9d797f69754507245b121c2cc3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:59:37 GMT
ADD file:b7dee3cae68ec5b68cbf4203b7915b3fdbdbd18c57197bc477af2bcc51091103 in / 
# Mon, 22 Jul 2024 23:59:37 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 23:59:53 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ac278e94839effcbf29dea60649ffd4beddf76d58e50d95a6a923683376a0b87`  
		Last Modified: Tue, 23 Jul 2024 00:05:17 GMT  
		Size: 49.8 MB (49828849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e979dc2dcec23b083707698e2eef10b041f9a56006bbe533bbecbf253b0f01`  
		Last Modified: Tue, 23 Jul 2024 00:05:38 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:91e99ebcac3a45e28201096f6976aa59c5c3d758ddea0a114c16d5367178e493
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47312198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b97bd178864f1d8b0717b2f1e5b20cf613d3bf057da018ae4a56f1874e0e69`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:05:33 GMT
ADD file:847382adbf83963ce1a9a2d8ce2b658bf75cf6cf4f746cec41afe06fba7fbf15 in / 
# Tue, 23 Jul 2024 03:05:33 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:46 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:57bd4a7b08ddd08cadc55c8f07989c57700b9a764c421e215fd9c0b35b7e01f6`  
		Last Modified: Tue, 23 Jul 2024 03:10:37 GMT  
		Size: 47.3 MB (47311977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6238160ad98d408cf5d93c070c1abb58fe799d39fa958a4b8c9507ae8443e83`  
		Last Modified: Tue, 23 Jul 2024 03:10:57 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c596dcba3d0ed157fe419eed296c0a6e0b337be825999f1d08371a5d289fade6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52888978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667d3f7a8a58465bc4084959373fba7026ccb1496c84e6fe32d2d62d49fd7260`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:41:12 GMT
ADD file:37a3ec80e65267ec9d7c28bd0b750192c2487497e693e6a1ff33c1c6577a5f73 in / 
# Tue, 02 Jul 2024 00:41:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:41:21 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5fe80dcf0eeb355dcaadb0826495e624bd860783d79819def799bff077c8399b`  
		Last Modified: Tue, 02 Jul 2024 00:45:47 GMT  
		Size: 52.9 MB (52888756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8081d8f930e2749d752b5e53b89017ec11f8fbde56756a0dbf2276db9a52ad0`  
		Last Modified: Tue, 02 Jul 2024 00:46:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:c2424388c3580beeedaf247520defe26f319d4379cc79bd9e8630d502a216a1d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53700973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1898735fbc3e766f876603f725cffadd32a9832153991dce08644d5462e46c3a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:56:34 GMT
ADD file:ad9e5eae5d24c2706270e7a1f61e4e68e564faddc2f20dde67423f28f9ce76d0 in / 
# Tue, 23 Jul 2024 03:56:35 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:56:47 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c27fd4786122906641795ab65420bb7a79788bfceeb6ae809a1ba696ca4ababf`  
		Last Modified: Tue, 23 Jul 2024 04:01:53 GMT  
		Size: 53.7 MB (53700753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4bcf5e7d21e30e7a3776518d527110f8e51790e00a9338279d2e260f3bdfa69`  
		Last Modified: Tue, 23 Jul 2024 04:02:14 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:61d6edeab9343c5424233246af55f15bac8d71328123d165154bcaf161287824
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51646766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4590ae3f740fefce66b3bf1aeab5540d801c01a8e0c5a77fd0fadee9857b454`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:46:06 GMT
ADD file:4fbd9c92c58a06ad8c03d39015be4f25cf142c1b42c81f2aa2f5176a23a166b3 in / 
# Tue, 23 Jul 2024 00:46:12 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 00:46:55 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:def2a5d993c9504094a578a8fab758300f4a56b5801297fe3423ec27ebf34b6a`  
		Last Modified: Tue, 23 Jul 2024 00:57:30 GMT  
		Size: 51.6 MB (51646543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8c7b12e5b03281489b72fcc0a10b5134795c376e6c7ed3ed153fa643668403`  
		Last Modified: Tue, 23 Jul 2024 00:58:10 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:39b765637fc1315d4a22ac263ac4e7f6b125ee23074999fad05ee2239d0c16f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56726705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeda7928f1105c407ef50c39e7b5da726f5e635d3bc5fe2ddc0c7a27068fe024`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:29:47 GMT
ADD file:0b9923e8e40660a2a8ba61aa96e9b0375388c0fc44432a85ea231ea633260271 in / 
# Tue, 23 Jul 2024 01:29:49 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:30:04 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:cc4ef1069b8dcb50816c7b106a4691f2c54c2d98d836b2d4a2432f639102a208`  
		Last Modified: Tue, 23 Jul 2024 01:35:04 GMT  
		Size: 56.7 MB (56726482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc9cb98b5f46fc6e152b494e4fb6061bb74a28c5986b514e8725d19b8a18caf`  
		Last Modified: Tue, 23 Jul 2024 01:35:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:4617d3e458761892e5882423f03f4d96ff59181f8d4a0244a1e0053ae7add259
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50937369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6577f0011c59d15b3c5d52905dff3496da41b870509f00400274e6889ae5b816`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 06:01:10 GMT
ADD file:2bc6646075798fba4249987a649f10bfaf642abb0392198c44b854ffcb5f0b5a in / 
# Tue, 02 Jul 2024 06:01:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 06:01:50 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:fdfde59d7e58ec2a6b9646f2b66c645b9eea9a179c364d9e58fd9f79816a66c6`  
		Last Modified: Tue, 02 Jul 2024 06:04:06 GMT  
		Size: 50.9 MB (50937148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5e577299f751aa330dafcf7b2f582912848772b0413aab6642c40e66c6fcca`  
		Last Modified: Tue, 02 Jul 2024 06:04:46 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:4daa4118b8087c8d564fe37f9595d7a99815f7078c8b86b282ec5598d7e61a48
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52435730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c09f71c1210f2ee1b7e4931709307a97d723fdfee6b8cadf2a6a48b5087943`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:31:19 GMT
ADD file:fb4980b66a184ccda2a46a660ec95e25701ee3acabf099d4695104da9122c416 in / 
# Tue, 23 Jul 2024 02:31:22 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:31:41 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:809ce47586a00df03723b18d62d1e775de5b317a1436688b6eb9a5f6a634417b`  
		Last Modified: Tue, 23 Jul 2024 02:35:25 GMT  
		Size: 52.4 MB (52435512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ec35fec14dc80c46a3d751d9b29b441ea84bbca1e5dbd877ea5f13e11acad1`  
		Last Modified: Tue, 23 Jul 2024 02:35:40 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

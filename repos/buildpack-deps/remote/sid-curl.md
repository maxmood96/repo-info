## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:380709bb631bae62afa8903f1739784552769f0bbe6f3c5d944a9dfeccf7db08
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:992315758e202516f7cdcb07fafaa7df8fdf7cc56ec8b0672d1dbab9264d6d9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76934711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b80e5c5d460f4058fedee74639979f6c061ceb3f7ae64f89b714e9555480f32`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:29:41 GMT
ADD file:2bdf145484732bc44972c30edbf4ac0d4400e2c23e993bf3575794199944fc3c in / 
# Wed, 24 Apr 2024 03:29:42 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:15:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7930dce44f2f1c310f4efe60708c4f2a496a0490b6d354b92c75cd37256dc108`  
		Last Modified: Wed, 24 Apr 2024 03:35:15 GMT  
		Size: 52.6 MB (52577130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c3089ddefcf0649afab1586a63316626ceab1a3c9c24149732b4a3c6ece786`  
		Last Modified: Wed, 24 Apr 2024 04:23:55 GMT  
		Size: 24.4 MB (24357581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1f3d904f4305c0f2578c127175ae749a839e5cc3e132f50654d5ad573c3522a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72906153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a20b4aab38537e5a32c68d9ad0947aa6a414b3b9b6f41a2d7a33991da20d81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:55 GMT
ADD file:6d78ef568e1b0c99bde27819bc47c6a881dad9dfdcbb9902ef13727853e9b7f9 in / 
# Wed, 24 Apr 2024 03:53:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:21:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4094711d041a5e7837195f3f8afff735217273c55a635f8ee4943e12e12227f1`  
		Last Modified: Wed, 24 Apr 2024 03:58:08 GMT  
		Size: 49.7 MB (49688192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8792d659774a6541128013c278d8cb8c341bfa5be0e802c3b2f7bb339d4e2f05`  
		Last Modified: Wed, 24 Apr 2024 04:30:40 GMT  
		Size: 23.2 MB (23217961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0079cbce49a8318dbcf30daece51f1970ea6c0fdb184bc8a9fca9c8d4c950bec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69734506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6446bfe11d8867ca1c4fc35c6441eefbc2c9d14cec9d8f8126b1c6d0e5edb5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:08:27 GMT
ADD file:2777c4d68da3c72783e92f5c8fb23b016abe830ec194eef61314095668218e31 in / 
# Wed, 24 Apr 2024 04:08:27 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:56:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:074f397c7ca8667adffc9dadeb0bf349fdf0c55e27384ed869e827a03f001b2d`  
		Last Modified: Wed, 24 Apr 2024 04:13:47 GMT  
		Size: 47.2 MB (47214198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a2c3a13a72b3631b18e4e4bb1d3ae07a820c21ef7bb4eca8f6e1faf17aa094`  
		Last Modified: Wed, 24 Apr 2024 05:06:14 GMT  
		Size: 22.5 MB (22520308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:beefa2ded7ef51612db5ec825b62b529563e4038d95f33767a7827d28d65f101
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77083124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f853bfc9fb4d2bd9214e0a8c434905db38c97ace674a62731792bc126c7815f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:41:31 GMT
ADD file:69ea41e74fa7a7601d1adbbdf992359f0c16c551447466cb4aaeac1914dc2377 in / 
# Wed, 10 Apr 2024 00:41:32 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:26:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:de2b6ae488daf95901751cee985416dfee51a36f7f9f15e60031279618e00a20`  
		Last Modified: Wed, 10 Apr 2024 00:46:49 GMT  
		Size: 52.1 MB (52136998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5adedb09bcdae19c9c078aeaa62769929c3099af358e94efbac1473c079342b`  
		Last Modified: Wed, 10 Apr 2024 04:34:38 GMT  
		Size: 24.9 MB (24946126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c2aebe46546f87abcae4741ad7b9e644347b02d0b184bd7611ef066c5d46423d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78929710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d6bdcd11b5afa388391aaf8578553909eed8f12a36ad1da453e4369a66637f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:40:33 GMT
ADD file:d8ee7d4701df61ad645e587b8b9747ac72c6dbdc2d358f14834282481c37711b in / 
# Wed, 24 Apr 2024 03:40:34 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:35:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1468f2e7ad62241109cfe49228c179a1529c8ad99c7e30f87c274cdba78b9582`  
		Last Modified: Wed, 24 Apr 2024 03:46:38 GMT  
		Size: 53.5 MB (53469174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144edd757523296cb31098e2810dc280c84b00a08c610e64b30e8ef6a374dad0`  
		Last Modified: Wed, 24 Apr 2024 04:45:21 GMT  
		Size: 25.5 MB (25460536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:eb7ac57ab97d938af38f1cc8b2bd22f98e562de90d4159c142197de225d2bac8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76341580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ea2c8543abcfddfd53575d84fa053c68b83b5134803bce1db79832d8e08232`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:17:23 GMT
ADD file:6ee5f04f14b1e874e152ce4477f27a16f4f4f6e4e49473d9e0d4f54bc8c7736d in / 
# Wed, 24 Apr 2024 03:17:28 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:04e21b74f69d4354ef0e677ec5dab4b460bf993f23d559662b8fd1e622263e43`  
		Last Modified: Wed, 24 Apr 2024 03:28:44 GMT  
		Size: 51.5 MB (51498447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9270daa8a7463a9ee3bd00970502d053092f544e14318daa6b1a128a03093d`  
		Last Modified: Wed, 24 Apr 2024 04:36:52 GMT  
		Size: 24.8 MB (24843133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6ade96fb7efc9207e7753577126fded9f4dc743ad6ab82a653345bad7a010610
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (82986981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca85cde550e995dc782e9d92d5c447f92050e61541e21e8fd24c5118cdb0228`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:22:30 GMT
ADD file:7b560eb5bd2a2213add3248349e22fae85a27ecd1155298a4bddb816d7a54856 in / 
# Wed, 24 Apr 2024 03:22:34 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:06:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:765cbb6e5130c0f3c7d92d3db7754f09101ef280d3dc88044ce2e4f3d010efb2`  
		Last Modified: Wed, 24 Apr 2024 03:28:43 GMT  
		Size: 56.5 MB (56489230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6fa79c129cad4bd59d629f88c921580acc125030e6aafddd7a75821316e889`  
		Last Modified: Wed, 24 Apr 2024 04:25:20 GMT  
		Size: 26.5 MB (26497751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:73717050aefb6e48ba2e4e077bbd31fad43d7f31f02911571c01a6df4b1ad72d
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74845046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c671d2001d6cc9e8d6303772f118203bb6371094293cebd7a6af64f329996a4b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:08:58 GMT
ADD file:cf8b9266fc4180144feb816ff584ba8b6b03b244743764b117ff119f451aa497 in / 
# Wed, 10 Apr 2024 01:09:00 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:30:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c8bfd6a26c3a37b6a00ea3d238fb8eed745384d2bb98efaff22428174a68f6a1`  
		Last Modified: Wed, 10 Apr 2024 01:11:44 GMT  
		Size: 49.9 MB (49941022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a180df00bec725b09dac77cce3dc37d1d711ae817d8b4a36f2aa34d8d552ed`  
		Last Modified: Wed, 10 Apr 2024 01:39:42 GMT  
		Size: 24.9 MB (24904024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:af3824c6306eb0030272086be291694c37a9ad0961c0e58797ac99d558dae77b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77530547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642f6ee4a5b54f67b9bbfc7ee393a3235b9879e6a0543209f454a3d12b6f4c8f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:44:58 GMT
ADD file:59f3ea732a9a69e000f55f6c77572ee58d91ef44832ade7eaf9ef53517342662 in / 
# Wed, 24 Apr 2024 03:45:07 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9460d35145d54c9079287c32e655a7ef3ab5a3e0db954bbf6e5f0d93a023ea21`  
		Last Modified: Wed, 24 Apr 2024 03:50:29 GMT  
		Size: 52.0 MB (51981898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23876b9d6d63bb4279671d4c44b46b1cc4dfb89f276b6263811ed4a02ccc137`  
		Last Modified: Wed, 24 Apr 2024 04:24:52 GMT  
		Size: 25.5 MB (25548649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

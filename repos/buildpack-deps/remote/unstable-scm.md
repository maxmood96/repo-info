## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:89b9ae52379910b2817b8d45aac9985eec93fcaa558beb1317da4b0995f999a8
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

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a1b211bdd46b2e04b132e0c4db0d2a9f3dd72db81a4ce8032e1f6cb754b68709
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143081353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f026ee1d71d1eaade60543a559f00e5e1c423e0b400425a1d198b182334b509f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:29:41 GMT
ADD file:2bdf145484732bc44972c30edbf4ac0d4400e2c23e993bf3575794199944fc3c in / 
# Wed, 24 Apr 2024 03:29:42 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:15:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:16:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:7bdb1aff73f8d0491e28548dbdc40c634193d1a6a547da17a6cae76298aa835e`  
		Last Modified: Wed, 24 Apr 2024 04:24:13 GMT  
		Size: 66.1 MB (66146642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:66662987b303c5396251c57d43bd24449b698b7055ec63c6181810420ab3a759
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136769839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a46dfe421161c07e5740558e20cd9ecccc4e4bd8895394656763cd7fc50f162`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:55 GMT
ADD file:6d78ef568e1b0c99bde27819bc47c6a881dad9dfdcbb9902ef13727853e9b7f9 in / 
# Wed, 24 Apr 2024 03:53:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:21:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:22:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:ba1dc3e5588a7f459e8d13bc6ad84c0a78b459ca0a25e743c4830031ba730699`  
		Last Modified: Wed, 24 Apr 2024 04:30:59 GMT  
		Size: 63.9 MB (63863686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:33d2787bf3607797cbc485dab1503ee59d4d8c915980fb9822a1744583d8620f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131008711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac107d1e1563bfd9640e03aca46ebfcb6bc90a43fdb3af441a0f3f7c1364b8fe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:08:27 GMT
ADD file:2777c4d68da3c72783e92f5c8fb23b016abe830ec194eef61314095668218e31 in / 
# Wed, 24 Apr 2024 04:08:27 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:56:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:56:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:bedbc07723990d22c0cd6d9122fd097d207ca0dad96183381ddb86be97ba429c`  
		Last Modified: Wed, 24 Apr 2024 05:06:34 GMT  
		Size: 61.3 MB (61274205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:804f2945ada6f548ce8019cbbd47f0d142a356db488137e71b3c8dc9f8651743
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143307731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6672f39e93d2ae658f2c0454392683d03e7d14ac6ea471b796f96152c6a241`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:40 GMT
ADD file:58d167eb75df26d368d9ef63173440fad7973e18049ffb23841be9cf507ee614 in / 
# Wed, 24 Apr 2024 04:11:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:36:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 08:36:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9914f5e7b79b9a6b9b6b7b39565cb50b06e8e20c51fa6732d67575dc53227762`  
		Last Modified: Wed, 24 Apr 2024 04:16:38 GMT  
		Size: 52.9 MB (52860803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94272953b95f66f135ff7dd1a6ec33b2857c99098e7a4551525e77bd85c1a86c`  
		Last Modified: Wed, 24 Apr 2024 08:44:08 GMT  
		Size: 24.1 MB (24095089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ced9ec581cda3952707837b15092ae80cb6726a0e48558502a4f816830828e`  
		Last Modified: Wed, 24 Apr 2024 08:44:23 GMT  
		Size: 66.4 MB (66351839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:47391c36a1c09b944ccffaf27a95d485db2236cb68599984d7f3ae76a09fc031
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146840440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8ef3899c4594fac277516501c683b09fa1b6f3d3c68ce1a680b742a05ad90d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:40:33 GMT
ADD file:d8ee7d4701df61ad645e587b8b9747ac72c6dbdc2d358f14834282481c37711b in / 
# Wed, 24 Apr 2024 03:40:34 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:35:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:35:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:da546e814b4a47376355f7febbd8c7322b4602812cd0a1e20a6157f99dde6cfd`  
		Last Modified: Wed, 24 Apr 2024 04:45:45 GMT  
		Size: 67.9 MB (67910730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:40eec1f8dd5bc4dc334f4322637535d05941f4321df04d3492f19b0f52b6f416
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141538157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a8d15b30c55498f847c52ba24aa4883395a385f84b1bbb36779ef67a23a78e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:17:23 GMT
ADD file:6ee5f04f14b1e874e152ce4477f27a16f4f4f6e4e49473d9e0d4f54bc8c7736d in / 
# Wed, 24 Apr 2024 03:17:28 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:12:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:e7244517ebd2754772a6a989d9c67a40bdae29fcea42ce3077fc6aada675a574`  
		Last Modified: Wed, 24 Apr 2024 04:37:46 GMT  
		Size: 65.2 MB (65196577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7e64ddb4fcb9c269fa8200de585c3c89fd2faaaf2b1a95938a9b9863bce8cca7
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154697469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb75dd61a790bc9dc9ae33fa4c6ce973c106e175e630a2e88cbb865c32e7aca5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:22:30 GMT
ADD file:7b560eb5bd2a2213add3248349e22fae85a27ecd1155298a4bddb816d7a54856 in / 
# Wed, 24 Apr 2024 03:22:34 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:06:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:72634af07399406fe0304b207bbb9254c5911e6205393a808954739c72f6fe3e`  
		Last Modified: Wed, 24 Apr 2024 04:25:41 GMT  
		Size: 71.7 MB (71710488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a73fc886602408a3d34d34c4105b53b05286a7e00b62ae1f72028abfef3039d6
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142821949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97da67fcb719578fc81020c41c51228bdcbcf5866752eaebb2877bd1ac932d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:08:58 GMT
ADD file:cf8b9266fc4180144feb816ff584ba8b6b03b244743764b117ff119f451aa497 in / 
# Wed, 10 Apr 2024 01:09:00 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:30:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 01:32:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:a3ce99732b9cfa4521c0ab9070c5af6f235f8b3d7977ca84c4ec174dba2588aa`  
		Last Modified: Wed, 10 Apr 2024 01:40:47 GMT  
		Size: 68.0 MB (67976903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ff62790bab03d54e29cf1ef322c8d55e76902d428964b99a9abcf1e47ae405e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (144980625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c61c08caeea9c630e17ca490e20c9226b04c6ecc161492092db6234a6076c27`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:44:58 GMT
ADD file:59f3ea732a9a69e000f55f6c77572ee58d91ef44832ade7eaf9ef53517342662 in / 
# Wed, 24 Apr 2024 03:45:07 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:15:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:0750028e9d601779122fdda713cdebbb465f0ee3d6b8725eb49f07f4e3a20134`  
		Last Modified: Wed, 24 Apr 2024 04:25:07 GMT  
		Size: 67.5 MB (67450078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

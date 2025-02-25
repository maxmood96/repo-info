## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:87c792460b682262b3c69a167cd6a77974273017fd1e6d4dc394c23c5bd04656
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2b9caef99c207ae749c91dab899f2713ef524e7b5d7ab03c625219fbeeab1694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141186355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ce9e910bd72f43d6f9314a169a3fd04b87704c4dc52de56d647cb7bd61a6e0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:950923b83892d84e409583fe8acab5a43a4ded92172eb9eeccc75b10012df546`  
		Last Modified: Tue, 25 Feb 2025 01:29:43 GMT  
		Size: 47.5 MB (47450585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8896ab25253a01ccf34a69a21881e74b41a25ff808e9b6217bda2404edb01961`  
		Last Modified: Tue, 25 Feb 2025 02:12:39 GMT  
		Size: 26.2 MB (26209855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41757968bd034488636645b2f5f31edb844db8e61d6402ac8aa7b5539e2ea59`  
		Last Modified: Tue, 25 Feb 2025 03:13:39 GMT  
		Size: 67.5 MB (67525915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:828ca798b0dc369d3899d6de163424c82be42ad397593130dab7a0b148483f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7588699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be13ad76afb8b112267393cd90484a8098c97244328a87139769aaf2284e5d4a`

```dockerfile
```

-	Layers:
	-	`sha256:686338719a915449381335cdb004ecf24e748d9462de61a5ee7ffaf16a8d9d5e`  
		Last Modified: Tue, 25 Feb 2025 03:13:38 GMT  
		Size: 7.6 MB (7581402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff96ca5373aa1f7006ba3df260cf7092bb78caa9a86752115743c557897945a`  
		Last Modified: Tue, 25 Feb 2025 03:13:38 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:84e24c852d00a207988799b1ad4a7cf719bd43f200246dedf394b1cb43ffcede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136620306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f68cffa395db19a15f11e2e54c002061f0eb04cf08a399d55f3be0d0214dba2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:969faa28a060b3165779eb5369b5e31931290ad408fa4e8e60d177e2f80c2611`  
		Last Modified: Tue, 04 Feb 2025 01:38:51 GMT  
		Size: 46.7 MB (46706175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd2fe3d3c4202f31101bc1bc73cd3af8a62f52a1188e729c8a3228780cf83d0`  
		Last Modified: Tue, 04 Feb 2025 08:03:51 GMT  
		Size: 24.7 MB (24746488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b0ffd764a137045323ce5b430a010c0f27d927825897343bc94eb266304a12`  
		Last Modified: Tue, 04 Feb 2025 10:21:56 GMT  
		Size: 65.2 MB (65167643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c25d78ad7955120511cf4a3329704af325854f4bcbc68110298967b337614378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7672250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b251aa22b2c24e45824d63d1866f50eb24f3fab6da989e814c81d535476a01`

```dockerfile
```

-	Layers:
	-	`sha256:0cc201c117d3c9d6a6d128311bc553cbb8f8288c95b25dc23d9056096e64f723`  
		Last Modified: Tue, 04 Feb 2025 10:21:51 GMT  
		Size: 7.7 MB (7664893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a9af14d91087ed924e26d790d458c6c4e9088eb5e6fea94d4bfe8a661552b19`  
		Last Modified: Tue, 04 Feb 2025 10:21:50 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:57bf4f850fb87ea5a2396ac50103bd962d196e27fff6995c620e4789811f1b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131295711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43d46f95240bed4877be1ac3991bd836c22e165e59d54b1553be79c80b7e45c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:eaba0613b673e68ada7f5f2b5e4971d3556823043148e63c2a6887ee2d5edef0`  
		Last Modified: Tue, 04 Feb 2025 01:39:12 GMT  
		Size: 44.8 MB (44838928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6395c61799d55a9640c01c9ef3b8549d20d61a975f9340e0353ec8e6422685f`  
		Last Modified: Tue, 04 Feb 2025 10:43:02 GMT  
		Size: 23.9 MB (23892297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f786aba56916535ebc6b771a35d47d2175891c3c573a3fe39933177009842ff`  
		Last Modified: Tue, 04 Feb 2025 16:22:53 GMT  
		Size: 62.6 MB (62564486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f7155396623e67d95ae83013541e913c28796be17eeb9b0448f5ec87c22cf62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7665818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b9ec6cec1bc04bf13cf3ca05e15fe0da0a5f7297ac1e9b64efcd630afb8456`

```dockerfile
```

-	Layers:
	-	`sha256:4736833bc88e2deffb2be4f51dc63966557b471084e9c19d4b1dcf881a842575`  
		Last Modified: Tue, 04 Feb 2025 16:22:51 GMT  
		Size: 7.7 MB (7658461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4fc997321fb704cc5dd30ddfb55a91e374aa5a6c9e44df28303bd8dd0d05588`  
		Last Modified: Tue, 04 Feb 2025 16:22:50 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ce7a7f6e66fc83f43311087ce7363b36522fa7ce97cc027a9e68e29926df94ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141890878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9051aeecaeb5bf8a13674219ac022eb236ac4c017bf4407ce9249b03878885`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f518c8f510cd10fda797c5ee77280d7c81b61ff1077c267de12ce9c337ddbe7b`  
		Last Modified: Tue, 04 Feb 2025 01:39:15 GMT  
		Size: 48.9 MB (48874714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b09bd24e474d679cb3c70ae42560294c37e17235d92a739791f20279494fa5e`  
		Last Modified: Tue, 04 Feb 2025 09:01:04 GMT  
		Size: 25.5 MB (25502640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5736977a6a976908d4675041b7224f0f03bcf47bf47293685f8218698d9a2d23`  
		Last Modified: Tue, 04 Feb 2025 19:03:18 GMT  
		Size: 67.5 MB (67513524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:58e6c64662de71cff5a6a96d98836cb4e8d77ad9b58d3b5d459d776b51e5de67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7673623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e140f182f0625351a5789f3a6b70cdf125b07eccccc0c592cc0519f9aa32aed`

```dockerfile
```

-	Layers:
	-	`sha256:2160fae6cc12a90d366a10eeb4aa8a22792aaebd966cc9fd5a61d3b202dc40a3`  
		Last Modified: Tue, 04 Feb 2025 19:03:15 GMT  
		Size: 7.7 MB (7666246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2751a302ee27871c011001fcda33b9e5ed3150173df02f9ef3c04b36589e788`  
		Last Modified: Tue, 04 Feb 2025 19:03:15 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2f767eb3adc8f82a2c493933702300404050f41f67fe46119057191938105f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145580394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf28fa39a7309f76e5c3857f77211d8b3c238c6188010bc08edaa275918fdd3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:aae1e98269b26509d10518853922a459fafd0d625e12a0e3bd33654e86d19bf9`  
		Last Modified: Tue, 25 Feb 2025 01:29:54 GMT  
		Size: 48.8 MB (48759296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75db5fe14e7f8d4a4352afc6fbce8a608d64e144a93abb709938695801d5f5c`  
		Last Modified: Tue, 25 Feb 2025 02:12:27 GMT  
		Size: 27.3 MB (27342554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f104786b18cd811e268777c977024df12ef2dfaf94dcd9d61ac70c26e3948f`  
		Last Modified: Tue, 25 Feb 2025 03:13:41 GMT  
		Size: 69.5 MB (69478544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:74569a6cd6d4e37732c2953ae0efbdf23f9a9b1223ba0d972a043d5348eb8968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7583440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02830f35a7a27e2fb48c01d7efaca7957eb77cc150a2971f998632eb78f24ed`

```dockerfile
```

-	Layers:
	-	`sha256:5dd960d34fd11395e597c5fed6da5533d383ec0e4be521dc21fd7b3ff54a0cd6`  
		Last Modified: Tue, 25 Feb 2025 03:13:39 GMT  
		Size: 7.6 MB (7576166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d05dd853b68bac1ad937eca7d174eb04e138fdb5f7f5167162e82dc54e9fe37f`  
		Last Modified: Tue, 25 Feb 2025 03:13:39 GMT  
		Size: 7.3 KB (7274 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0f92cc0cb64e2b9ed2dfd5ef76d95f91cb381c5eb26fbd778377ed625c48e96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141379817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1b3f1700a0eee8fb226f6c2eb285944a1eb1ea1302d89194974e14f3334c5c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ba41641f188bb1d74522008f197d258fe218bbf039fa1f236165286ebcda75a`  
		Last Modified: Tue, 04 Feb 2025 01:39:07 GMT  
		Size: 48.7 MB (48680970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1214950258d5885930b9bdcaedc26eedd6794e5ab349aac8800d95c05105fa89`  
		Last Modified: Tue, 04 Feb 2025 19:27:31 GMT  
		Size: 26.1 MB (26068631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46162e9940e0d980c469abb7969964a7334e5e0da594584952af4acfefef17d1`  
		Last Modified: Wed, 05 Feb 2025 02:57:00 GMT  
		Size: 66.6 MB (66630216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a07e1374401b63443088f43da17707a3d02dc688211a57b3adf68d54d182c671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3cbcab9c6a90ba788e51fed20b99caaabc6c7aa4cdfe48fa1300d61227b7932`

```dockerfile
```

-	Layers:
	-	`sha256:f8ae29f5adc2d43e0f8bfc1a61639046b8229a3ab53ab2196ec675bb5a18d9ed`  
		Last Modified: Wed, 05 Feb 2025 02:56:53 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b13ac9bdb2e347aa9710d4eab12eebfe3cf9e514783d29766a08044fd0392d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152778611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b969ced58302e77af9ae87640a70a5f21eaaafddbf45e5e8d9d1c925950e1aa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:20ee406f6988f44113bcc71bae5adfb439e360c88b767260000751228a498e00`  
		Last Modified: Tue, 04 Feb 2025 01:38:35 GMT  
		Size: 52.3 MB (52287301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089b8eaf628cc7675b29225b3b455c5d86d2c6a1f5fa29d78dfb7f3bfa69b3ec`  
		Last Modified: Tue, 04 Feb 2025 07:25:22 GMT  
		Size: 27.6 MB (27594542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e93e140d3d694402e568de11fc711950a112421628cf6102d07cd3e104fdd3a`  
		Last Modified: Tue, 04 Feb 2025 15:48:07 GMT  
		Size: 72.9 MB (72896768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1ff3cfa95a460bfb449e2a932ec5a43d50d582aa573e31d2afe5a4af765a92a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7678484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b746ab680c43c301cb8c99f3f581c643785323e959781158d174fad00b65cdcf`

```dockerfile
```

-	Layers:
	-	`sha256:1ece0e2a1d836da1c125fc755b18a6e7a44c01d56894cc469f34116d6111b5fb`  
		Last Modified: Tue, 04 Feb 2025 15:48:05 GMT  
		Size: 7.7 MB (7671156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95a21db4ec2629d1a56a109798ca17155cfa8da1e9745ca1b48098c9d6252172`  
		Last Modified: Tue, 04 Feb 2025 15:48:05 GMT  
		Size: 7.3 KB (7328 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:68889cfad176e17647b54d2fd1663f4b39d774325ab3b56d396024fa7fd2ab49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138099517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf11c3e7b39d1d68ba0623b85b5053278accbbb294c08f00c58730a27de4659`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5f390d4530b68a73e13f0b8647d2db7253fa60266e1fb90ae3f587c71a006f52`  
		Last Modified: Tue, 25 Feb 2025 01:32:10 GMT  
		Size: 46.0 MB (46003542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6542aac923569c10399fd56cc5e2363a56a89b5180e2dddd54f84754ded5a213`  
		Last Modified: Tue, 25 Feb 2025 02:36:30 GMT  
		Size: 25.5 MB (25547766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770a9d99da8ffce3a0f64384e37db6e3b77d3cebe38de8bd53a185b9f5807f6b`  
		Last Modified: Tue, 25 Feb 2025 03:19:47 GMT  
		Size: 66.5 MB (66548209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:94e663d9d2be5b75ce27c4cf9f679773d72124a4558a7da3109997b56cef494f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7577398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca0d824b6d8c871d843b569935ae56b9d1ead95ca5d241914193ecc4379a62d`

```dockerfile
```

-	Layers:
	-	`sha256:0240e2c37586586671040c4d9b89115b901c8ec89d870456936be0c9e15224fa`  
		Last Modified: Tue, 25 Feb 2025 03:19:39 GMT  
		Size: 7.6 MB (7570069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef48d06855aefbbb40fdef62235aa1ad694c74695c67c8de76f5a2940d8ca3fa`  
		Last Modified: Tue, 25 Feb 2025 03:19:37 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b1208175ff3c9ed58b24956475df5fe8c32398bdc3def6eb72e778b9a3f01b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143363850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccfbea6fb3322ae174c785d2d2fbeba59139f04e18896899da08fed7dfff4f5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bb029d344ac2942bf1f98be4221b2466495c100c4662a25e8e6338cf9c0f606e`  
		Last Modified: Tue, 25 Feb 2025 01:30:43 GMT  
		Size: 47.5 MB (47498543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a284e667f853bfd37a5b5f735f1448b941efd88d6ca35d51858f3d1bc02320`  
		Last Modified: Tue, 25 Feb 2025 04:05:10 GMT  
		Size: 27.4 MB (27368553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ea831fd4fc9eb25ca53ba663df8f3da6dd8286d4c4b7fb35d757ed455e00f`  
		Last Modified: Tue, 25 Feb 2025 07:17:55 GMT  
		Size: 68.5 MB (68496754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:14712d7371fd11e68796285fbccd184c7ddbe5d8d7c6171d512401e0bbb48aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7594530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f522c3145e867f0ad570f7ed1efae9e06fcd661def6e424a0cbd1f50d97b663c`

```dockerfile
```

-	Layers:
	-	`sha256:a20b50a21c700b175c5ef5a2ac9a409abdf05ac9a02f5be34bac016212d8bd2f`  
		Last Modified: Tue, 25 Feb 2025 07:17:54 GMT  
		Size: 7.6 MB (7587233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:546fa3845715f8acfa93c408e29e4addb8687f2fe948d37e62047a84d945f6e0`  
		Last Modified: Tue, 25 Feb 2025 07:17:54 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

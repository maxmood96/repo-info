## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:7709e1ff2c779fb5672525b7446ad8d4b6f59a0ead062e0f22391ed84f6579d3
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
$ docker pull buildpack-deps@sha256:49050b174b7c280c7397a668862e7b07e65d41029fffd9a4289f0ba89f51830e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141983228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de9e7ceb22c36a43a1fe888d57519e4006cca29fa80a1a9bbd024ae5aa7a57f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9a66d07ec06276723a9d844f79110db2c04e99b6e7ca9f2467ee7789a25614bc`  
		Last Modified: Tue, 04 Feb 2025 07:09:27 GMT  
		Size: 48.5 MB (48478504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37249eb6f9b3505b2330ba5132b480155ccfe125c06c5def806fca9a9daeec74`  
		Last Modified: Tue, 04 Feb 2025 12:01:09 GMT  
		Size: 26.0 MB (26036380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4fa6b03ff4cb7e858ff5a14c844d64841c23889c0d907ba3b0dff91e9902c`  
		Last Modified: Wed, 05 Feb 2025 03:36:54 GMT  
		Size: 67.5 MB (67468344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:36ce389bcf9326720dbf7ecbf7a2a66e2953fbc3a32824120544ffc68c1a1f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7666507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fcf6cb261b3b8b8689b31075e7690f118d26a8b64a4ab267a858e5255a765c`

```dockerfile
```

-	Layers:
	-	`sha256:18e8f73b18c7f8320da0a5c85645371cd9b3056ba3baf871fe86c4167ab951f9`  
		Last Modified: Tue, 04 Feb 2025 05:19:10 GMT  
		Size: 7.7 MB (7659210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20734c0cd4a50db3c1fe6185badc40dcd0819cdd78875967da043713cbe216fc`  
		Last Modified: Tue, 04 Feb 2025 05:19:09 GMT  
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
		Last Modified: Tue, 04 Feb 2025 21:20:32 GMT  
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
		Last Modified: Wed, 05 Feb 2025 06:15:39 GMT  
		Size: 44.8 MB (44838928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6395c61799d55a9640c01c9ef3b8549d20d61a975f9340e0353ec8e6422685f`  
		Last Modified: Wed, 05 Feb 2025 08:49:48 GMT  
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
		Last Modified: Tue, 04 Feb 2025 21:15:40 GMT  
		Size: 48.9 MB (48874714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b09bd24e474d679cb3c70ae42560294c37e17235d92a739791f20279494fa5e`  
		Last Modified: Wed, 05 Feb 2025 03:23:16 GMT  
		Size: 25.5 MB (25502640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5736977a6a976908d4675041b7224f0f03bcf47bf47293685f8218698d9a2d23`  
		Last Modified: Tue, 18 Feb 2025 12:29:23 GMT  
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
$ docker pull buildpack-deps@sha256:6678694174d4f8eeeffa050f0fc716c554ad11fc7f6a029f8ebb4797c6fbe517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146471670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80da4043c23e99d797e3ac30aa56c3125b9748c66f5e6d89758cdbf9d9828488`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:51741382468681fc53992e03a5e8ce7f591198e39599d81f3b698e3652a63db4`  
		Last Modified: Wed, 05 Feb 2025 12:01:47 GMT  
		Size: 49.9 MB (49883916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4227754a1dcb648ed5c4c8f40f8d60f655bb96ef669b5da48ad50132dc9621`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 27.2 MB (27185942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bb38fe259cd8a9e1ef2a45c45f0372cb16ddaf5c5facf3363ca9cfcede2c4d`  
		Last Modified: Tue, 04 Feb 2025 05:15:50 GMT  
		Size: 69.4 MB (69401812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:179c2eca5debb1d945c5b9eeaf22c0e8db8339553ed7d92bea95b044f525ea1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7661234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4a4108ec78cddbd0969cb329e129c9a6c49ee083712bc2b3c5c2803e244549`

```dockerfile
```

-	Layers:
	-	`sha256:7ce5bd96b9500a5bf64ca90b6006bd7805c45b65a27e6928eac71f99c067ff43`  
		Last Modified: Tue, 04 Feb 2025 05:15:49 GMT  
		Size: 7.7 MB (7653959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d21eccae88899113b9e0126cb64255aca549e84521b34ecc5fc1d7c273a2b36`  
		Last Modified: Tue, 04 Feb 2025 05:15:48 GMT  
		Size: 7.3 KB (7275 bytes)  
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
		Last Modified: Tue, 18 Feb 2025 23:19:03 GMT  
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
		Last Modified: Tue, 04 Feb 2025 22:22:01 GMT  
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
$ docker pull buildpack-deps@sha256:21b580e6d49c7e93d393cc4183b7953507a0d14a2c772cb813a045e6585ce821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138946644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4fe23c7e5e0a9ff767ebb38c7e80622244bde6575d34e79b828167a5c05e51`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:41a19e48936e10f226b6bfe61097156b74f03101f788496e8860f0d4806f05ba`  
		Last Modified: Wed, 05 Feb 2025 12:01:49 GMT  
		Size: 47.0 MB (47040914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a706305f90a9f6f5a4662ef1063ca9b1d12e77b9f1482c3925294e4989eea2f`  
		Last Modified: Tue, 04 Feb 2025 04:38:37 GMT  
		Size: 25.4 MB (25411970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2279830c9cdcc3d6d50a4a0308903e5819e1f53fc61863f2bc9dae664a4b8e0e`  
		Last Modified: Tue, 04 Feb 2025 08:09:05 GMT  
		Size: 66.5 MB (66493760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:84d7869326707918f8017660abb61e07bf85545665587c47c75212b024d84ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7655227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f78cd334f922550d198aaced125697fe79820aa0e68451dc3687844c137eff`

```dockerfile
```

-	Layers:
	-	`sha256:69854c67014a55e3cbc0388c744d9f3bdef6b499bc255551489ddc567868be30`  
		Last Modified: Tue, 04 Feb 2025 08:08:56 GMT  
		Size: 7.6 MB (7647898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e27ad8a4239ffd6edc6265d973c3ec43e3477ab76afac7cb1ee2b147937370`  
		Last Modified: Tue, 04 Feb 2025 08:08:55 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:24947995300edff9fe074d902dea0635e6d22ed2fd1937fa6508b0ec0c990968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144330742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcab1fa96a7252e1d34e96a40a4923670646b93a75fa50937e7e7cbd46fe398`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f48ea4a277664853f54eabe6340c7571241c845468906404bbb1efd60e69807`  
		Last Modified: Wed, 05 Feb 2025 12:01:49 GMT  
		Size: 48.6 MB (48560783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1f7d849459507f8a608795416d02b409e9f01c22159fa5acaf53ea0891b503`  
		Last Modified: Wed, 05 Feb 2025 08:49:47 GMT  
		Size: 27.2 MB (27214463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd8e9f79a90256c65272d5e3f7412b708597a6f16ea9693af76e4d17ce51d21`  
		Last Modified: Tue, 04 Feb 2025 11:36:07 GMT  
		Size: 68.6 MB (68555496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f2b1e81f1b440e5843aa24251b0b8923a99a1690c6dddfe027fb3ace5f939d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7672334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b609fc218e38ddd086dfc5bc64b9f12be4c636bbd78e05042313c048a7f24862`

```dockerfile
```

-	Layers:
	-	`sha256:e23016206115b86c9b36dd0ae2492aeb3ac7bef4a88beb722d8b794113fe07c3`  
		Last Modified: Tue, 04 Feb 2025 11:36:06 GMT  
		Size: 7.7 MB (7665038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b48b762e9223711dae7c7cdd1c675f03008477b830052c67c491f6c42f63dc4`  
		Last Modified: Tue, 04 Feb 2025 11:36:06 GMT  
		Size: 7.3 KB (7296 bytes)  
		MIME: application/vnd.in-toto+json

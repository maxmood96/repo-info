## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:adc1ff03d90d353ad1b1985fde434346d83fec519c8548e9e16b888e55a55051
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
$ docker pull buildpack-deps@sha256:800f02d4ad22de4be2ed9339b1a9cf66142bf9766b29732b624d907aa005520f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141838901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d39b5a7e77606f4befc02cd9f0634d596f4eba4fd272135fa6fdab5cb714ce`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2aa53e779a14a678b6be0553334055853528ebc9774eaa3e69e5fd71326114f8`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 49.0 MB (48967949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505e1c0337e142d28ab6c58fa7e5bf319287c629af695b520d6eb278c386eca`  
		Last Modified: Tue, 08 Apr 2025 01:24:25 GMT  
		Size: 25.3 MB (25273414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68956bba4f38c9a7df8163b678a6e5da9925d8244f2276ad427d279ae2fff2d5`  
		Last Modified: Tue, 08 Apr 2025 02:14:00 GMT  
		Size: 67.6 MB (67597538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:28a3ad8675d0bf30783caa5c32554824d4869e501d82d9fd408545590725bb50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7612107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61819005bc59a8b4ca1b5191ca817f02a5d9d5748d4a82028f0648938fe9222c`

```dockerfile
```

-	Layers:
	-	`sha256:dc079a9a58447f24122b33fd415df0e42c13e344f3ca3bfa7fedf507584e14a4`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 7.6 MB (7604810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b22e0d3124642b9ebd62ccfe785cde6be35dfddf6b375e1a2aa56e81479ed2`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:51a83913a3d1fb28eea1e17a8aac3a1d26fce1cd70d468e24c8a89359b859b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136406047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0199a72a714d847bc58b7145c181c598d2b394e04c3ec25bdf18f8b1c137b71f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7a67f90f752f0b4c3cbc55e5cc36457c9464d60f34b4c1a8cb2a06c06cfda363`  
		Last Modified: Tue, 08 Apr 2025 00:23:29 GMT  
		Size: 47.2 MB (47203396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5a07c09d53242d965ab755e1358498dc94eabdef8c99be65a21d5b9eea16d2`  
		Last Modified: Tue, 08 Apr 2025 05:12:45 GMT  
		Size: 24.0 MB (24031511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b89d4498cb31b4e330ac0bf8f8366b90ab05c82f7ed154f09e19faaaf575be5`  
		Last Modified: Tue, 08 Apr 2025 08:38:45 GMT  
		Size: 65.2 MB (65171140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5bf2334b66690915e97da36328409dbf6861ab69b3c7fd4018b14917c718ac91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7619120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb6c0481967776346d3241c3e9a4e5747d4492437f9630264214bf5f8163aa6`

```dockerfile
```

-	Layers:
	-	`sha256:0b0607048247000dc44f0e6a99aad6b058a648ab663600701ecb5cba57ff25f7`  
		Last Modified: Tue, 08 Apr 2025 08:38:43 GMT  
		Size: 7.6 MB (7611763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf38d62528c6518b4d12d781b51c59e21da77d285c0bc7708805be123175af35`  
		Last Modified: Tue, 08 Apr 2025 08:38:42 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c866d0af4edc016dabe48806c6290c893dcbde67aa39dee6ec05c25d5820801e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131448967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6452b92055810c27ee4d1bdc3543c1974a0bbc8e928f54ad88c12b4dfbdd97ef`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9e1d1d502e5470a18b1778621dae87bc08126015f4514c8d42f4923e5bbe3526`  
		Last Modified: Tue, 08 Apr 2025 00:24:51 GMT  
		Size: 45.5 MB (45459990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aef4244a5aaa0829da0ede8fd328ccc49be5178ede43a05010a5169a12ac0dc`  
		Last Modified: Tue, 08 Apr 2025 07:39:15 GMT  
		Size: 23.3 MB (23303278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f877aab82202905af0b48ebd21bac544815a1b4a8d0acbea3e524330c43db1`  
		Last Modified: Tue, 08 Apr 2025 17:31:40 GMT  
		Size: 62.7 MB (62685699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bf000902a4f0d9e28dde200a8cda562464f4fdbfaa7517517fdb1ca0daf4845b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7612666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e2ac1899251c7ba82e90ea872dd4c174dee62bcc284c7aec57f17c9897a93f`

```dockerfile
```

-	Layers:
	-	`sha256:a9fbbc95120cee49b6a6901ef927432a913f1ef856ba3ee28d27bcac0698ef9d`  
		Last Modified: Tue, 08 Apr 2025 17:31:38 GMT  
		Size: 7.6 MB (7605309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cad2ba1fbc0d47dadc84f2285a014929eb92004da895c7c442ed1b4d3452b631`  
		Last Modified: Tue, 08 Apr 2025 17:31:39 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e2fc2c3e226bfeb325b19fe6f060327c06241ae782d4907b3e0c6df5d962855b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141481557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811f47d93db9c7678056fa9009352ad6ca9be480bc9062d4c07319cf6429c26f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:09d775ffe2e3a261e25d75c66999fe50b8109b656ae312ea92d80a3277b69b88`  
		Last Modified: Tue, 08 Apr 2025 00:24:23 GMT  
		Size: 49.4 MB (49356840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd26d5bca0f15f13ec1e165536514cafcf57ff3d2c87ab2850f356915ddeb3aa`  
		Last Modified: Tue, 08 Apr 2025 06:04:11 GMT  
		Size: 24.7 MB (24668055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435258a53ca79e7f70aa94751fa20a91cc1653438c309c299182c4de6da3bdd2`  
		Last Modified: Tue, 08 Apr 2025 12:19:28 GMT  
		Size: 67.5 MB (67456662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3ee4c2725d5c2194ee9117784767ed0885e13a7d0cce89da56b6e380ebafc8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7619850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb898fee0aaba28e2e38dcbe7c8400549be386e57d2983d82edac912c97d8cba`

```dockerfile
```

-	Layers:
	-	`sha256:b0f3b3738874b491d2a28c3b7cc528215748cca26e71a91f72f26bd5b0788d1f`  
		Last Modified: Tue, 08 Apr 2025 12:19:27 GMT  
		Size: 7.6 MB (7612473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f3611f10a23bf2532d7ac3392efb92ab25334c2b1e72be3fd1f1cc691b2c9f`  
		Last Modified: Tue, 08 Apr 2025 12:19:26 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:56d91d6ead2cf54fad200da22908ec75998725d5e6713d2b9d1791eb91b76582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146381595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2eb6edb45a943b8bdabfa6d1bfc4a492fa5d2b8acf42d8be5d3b541721cf7f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a0f0bbaf0e5a890ab90a12e5df307c321a3344fa0accfb31dc895fe008c16f85`  
		Last Modified: Tue, 08 Apr 2025 00:23:19 GMT  
		Size: 50.5 MB (50476501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686927d82bc30ed67f20e1ddfb9d146b7acb12e90c947c73db07541c131a8cd5`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 26.3 MB (26298358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f78585b0ae6a95bc4b41ccaf9f3cb3acfdcca008d5b11330a5414a8ef1b7691`  
		Last Modified: Tue, 08 Apr 2025 02:13:58 GMT  
		Size: 69.6 MB (69606736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:685de755051800d7281f1b3d5486b6ea23ee60ee49cf0de65438969d6acf1964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7608154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e26fbc2312e6c210aae26d028c86782d35e412a9299390a47bd2485fead037`

```dockerfile
```

-	Layers:
	-	`sha256:a1e94ca1c35b7b11db21ddb7a22a29b752ca66a9d8ab61586c471bb246a85149`  
		Last Modified: Tue, 08 Apr 2025 02:13:56 GMT  
		Size: 7.6 MB (7600880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71d100c2597b82364be9c9b86f3c50ade3e6a50380c96a16a2b4f04d79bfd672`  
		Last Modified: Tue, 08 Apr 2025 02:13:56 GMT  
		Size: 7.3 KB (7274 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e825156523fb1083a70290fdff7870a525d7ca38831c8431414360b4fea7c81a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140567265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d620c37c43224ee032bcf67d4a24976bae2687580176f1d728b4c57f1f8449d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e12542a0a53bb97cc352ca7ce416a009a12137a70b8b9c3e736be4923c559ab0`  
		Last Modified: Mon, 17 Mar 2025 22:20:29 GMT  
		Size: 47.8 MB (47750847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e581beb347f24f554e5f2cf2d1525cb47adbd2ebd171f2c46bd47fada5257b`  
		Last Modified: Tue, 18 Mar 2025 16:30:23 GMT  
		Size: 26.3 MB (26282283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f3cc7353bb84ae34c688ff3596f801439d22635390e86e17ef4a03803ec818`  
		Last Modified: Wed, 19 Mar 2025 05:27:01 GMT  
		Size: 66.5 MB (66534135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f39960c4a777e5e9ef8ad79fea822b77aed8a0e3cffed5d79c111db746f782a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3c5d507434849ea49191e80ff85416e7d634f56bddf4d43481a6885d77c195`

```dockerfile
```

-	Layers:
	-	`sha256:ad5da8a3a38e5b37de2a54a8483f372dad8e5f36d9780e831e8063e2b265a275`  
		Last Modified: Wed, 19 Mar 2025 05:26:54 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:367f939991027b42a5009f021c517b683d364e771a4c1aab89bf38ab5a75ba89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152246469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686cc5d2862d37e1a77c3618b0cb468575540ecbb4ea2940c2aa06cd9d099abb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:24038d07494a40a6e0f9bb4cfa800b5c396d2199d38fdbd9a4d93a09f5534ac0`  
		Last Modified: Tue, 08 Apr 2025 00:24:22 GMT  
		Size: 52.8 MB (52784300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db81c823da47f6b320f39ca946071003941c644715aa03b5cfb4494f3617d2b`  
		Last Modified: Tue, 08 Apr 2025 04:31:07 GMT  
		Size: 26.6 MB (26637683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40825775c0fc5d49e80018df1342d3a42c3a0c76661dcf0b4bcd002c52dbd16`  
		Last Modified: Tue, 08 Apr 2025 08:39:20 GMT  
		Size: 72.8 MB (72824486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2a8a7de7a25dc7bb0a2ad6581f286978f18dc52bde33d8952700ef8841b3b7d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7625275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823fbf76b8bee27b33a47bcfaf954905198b2e94ccfb8719816112d5861755c8`

```dockerfile
```

-	Layers:
	-	`sha256:6e8beef348bec3a12fc55014baf3c4d760c06ada146675263a259b57df7d9642`  
		Last Modified: Tue, 08 Apr 2025 08:39:18 GMT  
		Size: 7.6 MB (7617946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:443d4e27d56cf92a980c1bf665f91a6fefa405201d862e884d506ec08ef0412d`  
		Last Modified: Tue, 08 Apr 2025 08:39:17 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d93e840deedb035dfb355ff7e290c5e8f0e9aaf4047732c73b193fd048e493e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138584538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c58088813a450129822a8cd9a3369cea3447e05ffd6091dd282d3b0e9aeb49`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9c53dca7ad1a1783f586e5e01ac8c6a23808333e74dea8e73cb813fed1a625b5`  
		Last Modified: Tue, 08 Apr 2025 00:25:11 GMT  
		Size: 47.5 MB (47479327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffe0734c1595d1fe0c36013a6078b10a14e39d1128a06575271e9a043d41f2a`  
		Last Modified: Tue, 08 Apr 2025 01:22:05 GMT  
		Size: 24.6 MB (24613675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6508389986649aabcea20a16ac597e9453899e4f0fcdc57dab93e6abf5afec42`  
		Last Modified: Tue, 08 Apr 2025 02:18:53 GMT  
		Size: 66.5 MB (66491536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c50f8b18b54a9971af2fbd56f3c88d462dfad3703573a42878e0187a5e60e2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84333dcfaf82005208c751114094b195a08635102681a9be89f3431b8244d36`

```dockerfile
```

-	Layers:
	-	`sha256:b47a3ab6ffcc4a5fb2009aa560fe32341dddf8f701c3926f0d1fc20e23f87c9c`  
		Last Modified: Tue, 08 Apr 2025 02:18:44 GMT  
		Size: 7.6 MB (7594732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c800b76168b9a798e494d5dd18238f02e205f0aa7fe5750ba9998ab7558e6617`  
		Last Modified: Tue, 08 Apr 2025 02:18:43 GMT  
		Size: 7.3 KB (7328 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a9ed0c43fa50349539ba692b68311e7612d1acb7d9f5a90e6e68aa407d327ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143721920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0820c7ef4f895df8a8dfe7aac1cbbfdb874941c10a8a684d76e8551238a09370`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4724dabe4aa05329c356a033beb752bf4d3d8e15762c4c9025e18f8b74f6a65`  
		Last Modified: Tue, 08 Apr 2025 00:24:40 GMT  
		Size: 49.0 MB (49047465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b70d32a5e527bdaaef0ef8d058290901aa64df97cc259e7f2fd2e845c51227b`  
		Last Modified: Tue, 08 Apr 2025 03:45:05 GMT  
		Size: 26.5 MB (26460166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d56a7d1628e664d6ddfb9ea04b13051b1461c586b96d98f706033c1d083c89e`  
		Last Modified: Tue, 08 Apr 2025 06:53:42 GMT  
		Size: 68.2 MB (68214289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cb80040911f979319ae8e4fe549675726f9e6375ebe31d322bd759f03d9ca132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7599543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27289725925469a872c1a4faecc190035613796bf915d35d54eb64c891130bdc`

```dockerfile
```

-	Layers:
	-	`sha256:f1ca06c151fc095028cbf0fe841b3eb7e1010402b147220bf8a103e721dd897e`  
		Last Modified: Tue, 08 Apr 2025 06:53:40 GMT  
		Size: 7.6 MB (7592246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24cbf7ad1a8a6714fb130c76dda5b087840fa92ef62a1ecbc747e87d5f457f7f`  
		Last Modified: Tue, 08 Apr 2025 06:53:40 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

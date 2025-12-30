## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:c08e6defb9f3ad3172dcec1cc58c58662510185349c99a46a98566315cb74ce9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f39e2c1a3383bfa072e9cc2adbe094313ddaf9c8371c6640f3ced4af911d4408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144438020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8517dc8d7972210960277f75b53801c7b63873cc87e3ae962e8052b903cef9f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1766966400'
# Mon, 29 Dec 2025 23:45:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e1869079ab5cc3b00301445717c112f3ddb9424b5d7b2a41713bc70d9482ee85`  
		Last Modified: Mon, 29 Dec 2025 22:28:05 GMT  
		Size: 48.8 MB (48830058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9becdec1844ece10920454e52e9f153d35fd872e9ffaceb5593016edc7486d22`  
		Last Modified: Mon, 29 Dec 2025 23:46:16 GMT  
		Size: 27.2 MB (27164425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c878fb0b7aa23d581ef5f8169f99d577505c3e94f8550d0f4a0f4615645735c9`  
		Last Modified: Tue, 30 Dec 2025 01:24:01 GMT  
		Size: 68.4 MB (68443537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ceb0cb701c019150c6a8c121e7b02a540f7adcc1b2efbdd333c661d1bcb95396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8fc7d918cfdbd247b3d64e19d1b6ed0f9daa080a1ce7c8215ef758aff568bea`

```dockerfile
```

-	Layers:
	-	`sha256:dbc143ec65c2ad05e27781ec6c7b6e8a9137b4617b1216b5b13f85649a924756`  
		Last Modified: Tue, 30 Dec 2025 05:21:39 GMT  
		Size: 7.8 MB (7769522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4987203c14bb66e72bd2c2e296042ef75c014ded13d88666352399bda23c6530`  
		Last Modified: Tue, 30 Dec 2025 05:21:40 GMT  
		Size: 7.3 KB (7266 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5b628a2090cf0d52a1a064253185dd5c41f3cfb6054e399c0b4c1250b7c44b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133359953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad02069c08c5357f382c140775d8ec1299f9b78b7f8dfa38247bb6997f089dc1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 00:34:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:07:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:241c7878eb5bbc21e3d5116dd5ea31832b2d3bc7489b0d564310ab3bd542adee`  
		Last Modified: Mon, 29 Dec 2025 22:25:59 GMT  
		Size: 45.1 MB (45129806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cfe0fcd77ad4f32a187bf7cc2a756d93850a1250b0bb64207ab8263c6fe614`  
		Last Modified: Tue, 30 Dec 2025 00:35:10 GMT  
		Size: 24.9 MB (24885689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d9e7eb1430fbc458f5de067624571165f4d9928add27333f54b491748689b6`  
		Last Modified: Tue, 30 Dec 2025 02:07:37 GMT  
		Size: 63.3 MB (63344458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bb5f06c3dbf1b66eccf136f7cb6ce808446d2a938f4967a9acc8168001d88f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173046714dd59d64f1777ebddb2a9fa93bb26392eaf16a3feff66cdc978303c4`

```dockerfile
```

-	Layers:
	-	`sha256:4c24fe21ce4c7b1fe932df87b6ac135f47233b92c509dd8735279f291cda3693`  
		Last Modified: Tue, 30 Dec 2025 05:21:46 GMT  
		Size: 7.8 MB (7770021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:119e89b98b68ea269ce5d8256c0e1420b7addb9d75f6e0ed33b39bea36563b0a`  
		Last Modified: Tue, 30 Dec 2025 05:21:47 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1b9a9f6fbdf707bbf265624a9970eac2f94c6896a85f84e7ca2115554ecc06d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143434201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a2bd853ce5943a1cff187bf2df27b3ab7fa94f82df683ea943abb1f18a6be4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1766966400'
# Mon, 29 Dec 2025 23:46:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d6ed83950a3f675536ad8634cde3cf4c241d5faea11ae3192ff5909f826256f2`  
		Last Modified: Mon, 29 Dec 2025 22:27:42 GMT  
		Size: 48.8 MB (48831993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf6ef9ff46c8cdd87f91591a96ba850200dfe34c376dffe91134bf667ddfa22`  
		Last Modified: Mon, 29 Dec 2025 23:46:56 GMT  
		Size: 26.5 MB (26460878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7c23095ce6398eaf80110721fa38c4bf3ba716dfc692946b69f2bf36a47248`  
		Last Modified: Tue, 30 Dec 2025 01:26:10 GMT  
		Size: 68.1 MB (68141330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:da1e5c25d3b4ff40386cbd2a01bef1e006f3447c489b4d37695a8b0f1d620fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc88bb178025d9960a378ace3d0dace390891058b0f59f7d130e69e2c19f5a79`

```dockerfile
```

-	Layers:
	-	`sha256:86f067988653e2278c93a5c0bd6459e449bacfd091e1e28624b446e48a1b4521`  
		Last Modified: Tue, 30 Dec 2025 05:21:53 GMT  
		Size: 7.8 MB (7776547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f14c4ebe6c23bdf84d8dc115a48240589907e2fd6428e791611d6a3ca9e70d84`  
		Last Modified: Tue, 30 Dec 2025 05:21:54 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f1a187c664fc82f4c38d660a4d676a432337562570b30201d14c67a1376d4b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148776146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caba1f9147702bdbd52108310209b2cc20195eb8ed2f52ceabd0de7f10797f86`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1766966400'
# Mon, 29 Dec 2025 23:47:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:33:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a557815b7e39210fb0b4048ae58b1ffddbc8cf0f656a5974b6c3b24f7bdafed8`  
		Last Modified: Mon, 29 Dec 2025 22:25:28 GMT  
		Size: 50.0 MB (49955836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a5e10cdcca6f1b0c95acb93ab2b6af2d31550b8756e6b5bae03f69991891b7`  
		Last Modified: Mon, 29 Dec 2025 23:47:37 GMT  
		Size: 28.4 MB (28412777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637f9908731534f4dd3db9b4b7e9719543000812fbb5ec06ac1443d1521a0d94`  
		Last Modified: Tue, 30 Dec 2025 00:33:31 GMT  
		Size: 70.4 MB (70407533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:24ac1fb9d6af9b7a0c4b731339283e1e4299abb2635080832719dc80f800aedd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d438cb16a887c7869496f664590d542de908c09f330cc70a425517275b7d11cc`

```dockerfile
```

-	Layers:
	-	`sha256:f34200ffb9d31406fdf03c408e78fa1032b31089591a6c8be417930658e6f150`  
		Last Modified: Tue, 30 Dec 2025 05:21:59 GMT  
		Size: 7.8 MB (7765655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bb2d4a0ab9ec735a9f61e3a0ac211b52ec718e88025fc6f1239c67423e8e059`  
		Last Modified: Tue, 30 Dec 2025 05:22:00 GMT  
		Size: 7.2 KB (7244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:282e63fa0ef5da7ac0336a93437451a0b06216d0bd5cca8ba9d07597813e32d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156197037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c177f70aaacf8396ef402cac82342ac97137157e15f575f77bfd1e755b21603`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:21:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:09:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ca6b6474de59c13edb40994c0579d1471aee6a7743baa1f84bd96cf0fbd414da`  
		Last Modified: Mon, 08 Dec 2025 22:50:05 GMT  
		Size: 53.4 MB (53413786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16460d60e48e0172db82e752033b5336b64df38a32ba4e288da4b3068cc402ff`  
		Last Modified: Mon, 08 Dec 2025 23:21:53 GMT  
		Size: 28.9 MB (28864526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff96e6fb6ec2cfd3a984712824e772995b886f15a30aa9cd1af807a917dc615`  
		Last Modified: Tue, 09 Dec 2025 02:10:10 GMT  
		Size: 73.9 MB (73918725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:159f320aa73917aba120433176afaa44ead95f3e2dd2a8cd38fd6451a925c54f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658063f4e7c5956ec12919c0cfb5929aae391913c5d09ca480380446322729f2`

```dockerfile
```

-	Layers:
	-	`sha256:53a3d31a9edb534ddd6b4e95caa61f733f33583707f57a2e2cf2d65b78b14c2a`  
		Last Modified: Tue, 09 Dec 2025 05:21:10 GMT  
		Size: 7.8 MB (7767389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:015886c42a59d014af6dd65751896787e6c30ba26d07ff58223ac5f9ae184646`  
		Last Modified: Tue, 09 Dec 2025 05:21:10 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:43c779b5e19e2fc1872e6d44b77a8a7ca207787393a18c308cb67b7272d0bdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145681327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3d278ef30351ec8f1edde90c5a2216d40ce4abcf9e3e1935ef13a0c65aec81`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1765152000'
# Thu, 11 Dec 2025 08:32:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Dec 2025 08:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:002664050c13ca9d4571d9c24b2cd8235785825417d0a59db3d16cec4b277530`  
		Last Modified: Tue, 09 Dec 2025 01:49:57 GMT  
		Size: 46.8 MB (46840355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79762d676bf44b71b19af2f5e9bf3520032115760ca18d18b1e487b509a74b9a`  
		Last Modified: Thu, 11 Dec 2025 08:33:56 GMT  
		Size: 26.4 MB (26411155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899e9bcb2a2f2dedd16603a638381275feefb5833c5f56fd53977194d927e781`  
		Last Modified: Sun, 14 Dec 2025 08:38:25 GMT  
		Size: 72.4 MB (72429817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fce42cd753f415ab35d6d0e0f69536e57104392da4128af610e1a691fae3e362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7760961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da71ac906f7cbed973832ddc433331b0b4bda21bd2c5569d5b1e3c9a7314df4`

```dockerfile
```

-	Layers:
	-	`sha256:df245a1316d4e860abfa8ca4e79c843583b6791da80af3566ba3c3430fd4ef53`  
		Last Modified: Sun, 14 Dec 2025 11:20:17 GMT  
		Size: 7.8 MB (7753663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb3716eef1a86b8ccefd3cc1d8ef579d9b6ee6b398b3cadc12ab89bacd2f9d83`  
		Last Modified: Sun, 14 Dec 2025 11:20:18 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4d4094a3611a94bb8619448009279917f6cf00bc3e8e68a7e85f3c3157aa2b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145836058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c2ced3056e700a658e138787992921a4f262a0848c57150192b43344420b70`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 03:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 04:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4ed754f864448d0e594994dc11148ccb02da6ea309851c997288e88ce4fa4e08`  
		Last Modified: Tue, 30 Dec 2025 02:08:24 GMT  
		Size: 48.4 MB (48397553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d28917da9bd93a97bef96b25f92932fe3babe10b8325e0cde3317e7a34eba7`  
		Last Modified: Tue, 30 Dec 2025 03:24:40 GMT  
		Size: 28.3 MB (28270771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0cf5f751d0c65a3f9d4bfed3f5391773af837d7f314dc3df35eca86c8c1ce0`  
		Last Modified: Tue, 30 Dec 2025 04:14:08 GMT  
		Size: 69.2 MB (69167734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3c1c4976bfc13a2df4ca70218dcfc2567be56494e6fc6319b6ce8d97db25b031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87616236032119fa636a8536b8757b683d5118e05adf36186ef53934a5ce4f89`

```dockerfile
```

-	Layers:
	-	`sha256:cc388f85c2472f18e055ae50d936b013e606445621e58856f552969219e2d7c9`  
		Last Modified: Tue, 30 Dec 2025 05:22:17 GMT  
		Size: 7.8 MB (7770435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0a3b5879a947a7fb770705e30b0c80ae27792994ad165e60f8b6022e824b27b`  
		Last Modified: Tue, 30 Dec 2025 05:22:18 GMT  
		Size: 7.3 KB (7266 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:aaf0cc2d977e284be70dfaf077100eb10869d82938de3ee69088b7ae19c72b0d
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
$ docker pull buildpack-deps@sha256:7a2986d2c6a94c366c047804e71e28754eb292ce0b610f87e820783b5726c3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143780596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ee080a6400c7e1219f4e1f88081a66d6d60eace580182d29e120e2dfaf4b4b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8d64c6c7c21822ac171c4c396d70161707401d6d50d133075d661956f08dc756`  
		Last Modified: Mon, 08 Sep 2025 21:13:08 GMT  
		Size: 49.7 MB (49657990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ef32ff63c929905defc6f655e25216327571899c86b682cf8814eb2c3a0a3`  
		Last Modified: Mon, 08 Sep 2025 21:55:00 GMT  
		Size: 25.8 MB (25793066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb01fb26197afce850c60aaec10a56aeebcb0718e65cd705a94bc39a9af78544`  
		Last Modified: Mon, 08 Sep 2025 22:13:45 GMT  
		Size: 68.3 MB (68329540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e86784ba253f8e402000b8d46c80cdf02fbb7a43bdcf4a6fa14eca5f1c965f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f271830c6791a4eda6c25d1fc2714de4ce0ac21187b68ecade928a6ff8f50d99`

```dockerfile
```

-	Layers:
	-	`sha256:18fa4d46a3f7e781b9ed5d63014a8898d57eae943f1d53e809f85e57abe70f3a`  
		Last Modified: Tue, 09 Sep 2025 01:21:35 GMT  
		Size: 7.8 MB (7770457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30f27461e4f0eccc18e6e19f743c1b3e562e2a72559aeece71b80300c088e39c`  
		Last Modified: Tue, 09 Sep 2025 01:21:36 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9fea55e604e5b3d9fc299f00cee74420981758f2986041185f23a41f7b08ce50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137988790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca3c79cd13e0f811e1d9bcb4b2c777da61ffb7a236d8bb92e75b710ea4ff65b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fbbf51ad93abaf2c32c0bd2c116235b9ebbdf46c27b1eb3a1de581d2505529d1`  
		Last Modified: Mon, 08 Sep 2025 21:15:28 GMT  
		Size: 47.7 MB (47745321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643a27ea3b595194ea4b57e98121e28094f76ae480ffaf98bb45b0ff375de320`  
		Last Modified: Tue, 09 Sep 2025 01:32:11 GMT  
		Size: 24.4 MB (24441403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066f85c5e5a320fa62ace82553ffa0f839dcb88ebbbf0a438e8427cf81a027e7`  
		Last Modified: Tue, 09 Sep 2025 05:05:25 GMT  
		Size: 65.8 MB (65802066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e7e08cfb84487657a4fbf43b13c318a1703fbbe5e325cc297f0a0351ea8bf16d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2a98a79efeca9efd865399391c1ebbef8cda5419cc352e6ebf32eba3ea8a65`

```dockerfile
```

-	Layers:
	-	`sha256:c1124bf51a1c51846e02fb949aad3671150dc4f097cc3815a4370318f641c99f`  
		Last Modified: Tue, 09 Sep 2025 04:21:48 GMT  
		Size: 7.8 MB (7771504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:515feec7528b340c836d0026455f78d2f160a8772f45f64304db33b6e295eb2f`  
		Last Modified: Tue, 09 Sep 2025 04:21:48 GMT  
		Size: 7.4 KB (7361 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0cdba8e04b14acaac47ff534c7fc5bdf2f60db8181911a5addbda35ceb620f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132930871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd76f4a3b8950686cbadd306d7aa8bd387f3f1b66ef8b1e6164bb02d37bfce6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d30a0c5c579644a88a894fd0b1f1db229651b30c974b07aef6ab9bcde5b64440`  
		Last Modified: Mon, 08 Sep 2025 21:15:47 GMT  
		Size: 46.0 MB (46006695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf528d0788e249a97adf6d73be0b9ae329c2651a09b55c47f7bfbe9fc96a9cd`  
		Last Modified: Mon, 08 Sep 2025 22:48:40 GMT  
		Size: 23.7 MB (23710180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717220db35946b78b9fb18d38321ad58f2681e6386e6e8368e047874b841311c`  
		Last Modified: Tue, 09 Sep 2025 06:19:30 GMT  
		Size: 63.2 MB (63213996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:386f46d7c22716e49960956217a5ff81ce502a865be4944e9474206c4eb5ba64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8267cbad4aef56b48cff3617497f6652caa7b36c58d5bc6e95cb92603b34ec6`

```dockerfile
```

-	Layers:
	-	`sha256:9bd83afcee8b648362142b9383fc6a6c69309b50d2272417494cc621d2d0842c`  
		Last Modified: Tue, 09 Sep 2025 04:21:54 GMT  
		Size: 7.8 MB (7770956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df4b72b54efd25fabc25ec283658012f24fe5378395e8e75e1ceaa05df06d89c`  
		Last Modified: Tue, 09 Sep 2025 04:21:56 GMT  
		Size: 7.4 KB (7361 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f1cbd3be9a0299892523e952c275f47854866747805ed285d5196f9ca815fbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143089501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06dad665a38d260897e967d3ae2b0fe03996404fc56b1e6dd12e08af9019e72f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:00e024daab2d43f36749bffb01f2b299b405cff0659a8e4f4f00bb468dd24c27`  
		Last Modified: Mon, 08 Sep 2025 21:14:58 GMT  
		Size: 49.9 MB (49934721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523fde0f8298499f83d08590922e2548966d7839a982d2f61f9bf20422631032`  
		Last Modified: Mon, 08 Sep 2025 22:30:33 GMT  
		Size: 25.1 MB (25121637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7a4b2e0bfb6f60fbd361b9831a03e03dd998e97fef4054fc95dce3d9157a05`  
		Last Modified: Tue, 09 Sep 2025 02:13:15 GMT  
		Size: 68.0 MB (68033143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a772084cf6bcde6c2f71688f86e27f07f50f1348bdc3b54ed212accdbcbce1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7785497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93596cd9d557961c5bf8aa4c0883f95065e3d2b0539aa273847976682ffbab15`

```dockerfile
```

-	Layers:
	-	`sha256:201d552895d621cee0fed5193b8efa99d9293d63f10aca845e24b496289d9565`  
		Last Modified: Tue, 09 Sep 2025 04:22:02 GMT  
		Size: 7.8 MB (7778120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b56d449b4e12495146198ce3570b444666d35b4cecf3ffb3de7d4cd2bfda86d7`  
		Last Modified: Tue, 09 Sep 2025 04:22:04 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5e1d45d3b8d9a9920694d77c2ca2b826928e1d02dff21d496751dfc04b97eda6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148340412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67af15af73f8f04c66b25daa3b7533dcd61ff4225eb974809e7f82391b5f08b8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:eb039ce3bcf3fbed73729096e510ae45e98c7db73d412a09aa57aaad6f2f6267`  
		Last Modified: Mon, 08 Sep 2025 21:12:53 GMT  
		Size: 51.1 MB (51113613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb4ce6e6dabdd026c92e91d6d35c69c5877c49180dfc2038eceb2d3a81ffb31`  
		Last Modified: Mon, 08 Sep 2025 21:55:10 GMT  
		Size: 26.9 MB (26880746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cf30a6a5b2b470e48344ea274a9e04bf7432fce9adcb8cb91cb62f15698361`  
		Last Modified: Mon, 08 Sep 2025 22:13:37 GMT  
		Size: 70.3 MB (70346053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:995022affd3d64847aca332ed6038e48810268933ef17421cf880199c7806d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfbac34947ea4514de252d657e20b57edd7060e05bb4a55a53b2987ac078e29`

```dockerfile
```

-	Layers:
	-	`sha256:e7cefc4132126157eb699994fe10b6be9319a2c17f300b8bac5f41b03e5cbac4`  
		Last Modified: Mon, 08 Sep 2025 22:21:51 GMT  
		Size: 7.8 MB (7766606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7a5d7f9d99fb77849cab1ab41fbdb3359ca855902e185729138214dec8ef729`  
		Last Modified: Mon, 08 Sep 2025 22:21:52 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d738329437502b669e772e7d295d2063b83f036fb2d371defe2a2603b7e09c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142883769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5db20af0230068e1698ac5589826ea5fc56b66186c1ac0cf1b5340bc7d459e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e92e35711c7a07432f12289818406bab4746919197592d38fb8632974832ff9a`  
		Last Modified: Mon, 08 Sep 2025 21:18:22 GMT  
		Size: 49.8 MB (49822261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5720cce3339585de6afad24f3a7efc526d8b9755873fbcf07a2420b66b3573ec`  
		Last Modified: Tue, 09 Sep 2025 04:23:26 GMT  
		Size: 25.8 MB (25756499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb4a8a71b5336697bb6c651f14886de4102aa103fde259ca53a8220e8dc6746`  
		Last Modified: Tue, 09 Sep 2025 17:48:41 GMT  
		Size: 67.3 MB (67305009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a8fd3a2b2fe3eb3d61c57cda8df34cd73aa5a955b06b2a904f73ffc46ffe0113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4988746c5974bea173a29e007f4c2f34595ddb50d951837a3d598849b1abbe63`

```dockerfile
```

-	Layers:
	-	`sha256:4d531b29ea61806a8ada6fdd1f8365af5c01e94a046ebdb5f2e1227a9b7d7a0f`  
		Last Modified: Tue, 09 Sep 2025 19:21:10 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b263e008b06055da328b1f498e32c20a82ba11dd27c59f5efd9c2b791225fd8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154175582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092c48609cf218774f42455413f255c0de2231bd13949ef2f749b69d79364525`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:772eb1186277ef333cc2188830519c27192dac48fb00016f4bed1d6fb65f0e2e`  
		Last Modified: Mon, 08 Sep 2025 22:22:18 GMT  
		Size: 53.5 MB (53458792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383909d767bd90933a41650a2f22af3654b67dad5eb9eb12c8f0c5d5619ec04b`  
		Last Modified: Tue, 09 Sep 2025 03:12:59 GMT  
		Size: 27.1 MB (27099124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21675bb5849f4e08ff04ccc490a1604dc152c26899ff15f1b7123fdb165262d2`  
		Last Modified: Tue, 09 Sep 2025 15:27:53 GMT  
		Size: 73.6 MB (73617666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db74429c766917a247241aae9981d553aaf26091010775f3d0700cc2883f0037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7784885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f81d5d78b677188ee7022dea0cafa367bc8e01da25fa7d482c64ecca781996e`

```dockerfile
```

-	Layers:
	-	`sha256:738b71b2be435cfad62a58b4a2a32c49e005bb8355e72496cd9342a9ad6324be`  
		Last Modified: Tue, 09 Sep 2025 16:20:58 GMT  
		Size: 7.8 MB (7777556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d5be2bd4149b6996278519f613b197c8112acd3bb66d76f1a26fa9f4090a20d`  
		Last Modified: Tue, 09 Sep 2025 16:20:59 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a60e44821ff1eac1493f1d9ce9b665bac47e8b9dea70412b701591c00ff67726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140344285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec57c9015beb0e5f4b82331fecb4a8fbfd8cd6678afffb6716ddd7f3d6e2664`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:347be58a551dcf8aa3dd300ae844cdfc6ff2cdec19870bd090fdef86fdd7d393`  
		Last Modified: Mon, 08 Sep 2025 21:38:55 GMT  
		Size: 48.1 MB (48052647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40a5a581d6d2c97cf774bc90f07071cf2fb0f1b3c0571346161822b7094bcd3`  
		Last Modified: Tue, 09 Sep 2025 09:13:34 GMT  
		Size: 25.1 MB (25071945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db66c5e84f1e64845f6aff4b1b0ac7d573e0b57248e1ca5ccfaf4eba4dd11ee2`  
		Last Modified: Thu, 11 Sep 2025 01:39:05 GMT  
		Size: 67.2 MB (67219693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f512908a634ee2b8150d4d21a87404b9121fceecf7d2c7bba09d419d00edfe20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7767588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316fc4649ad7916e9a29490161717e93fd80bf677e2158c2072affef480ebf3c`

```dockerfile
```

-	Layers:
	-	`sha256:2263506e812637cdf3cadbc5ff04087605f043c19f4a0ecaa01e4dd92e574990`  
		Last Modified: Thu, 11 Sep 2025 04:20:47 GMT  
		Size: 7.8 MB (7760259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e1626cedf6c825679b91cc3acc46d535f233694009452e817e2e0fc153025fb`  
		Last Modified: Thu, 11 Sep 2025 04:20:48 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:35919d1cfcf2bc87cc49636abdc5a135ab392ff5a55b51c35aae3eeb19855329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145714055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f779c84511a1aaf7fda5ed5c3aaec13a07430d575ba748214b45038feab8575c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:75e6f7d74f7a64a858e5c9cdecd19e5f33e99956d1f33d14985ac51b655eba01`  
		Last Modified: Mon, 08 Sep 2025 22:22:23 GMT  
		Size: 49.7 MB (49652038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f495f7a03a882cda8ba1cac3fcd8e67045987237ece386400cab302efabfe1`  
		Last Modified: Tue, 09 Sep 2025 10:20:34 GMT  
		Size: 26.9 MB (26893291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a29a0faa66c0d5bc6228e67d1d922c479797207d6a82c57cc284e6c444b5ac1`  
		Last Modified: Tue, 09 Sep 2025 17:57:25 GMT  
		Size: 69.2 MB (69168726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e4dfb0ec934ad3c1c3af17d5bb6ec7d404c96b0f74614fee9b30c3169c1bd245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399270849c32547bad7efd15345cb35a023ba7af3755164740c61bb65e669117`

```dockerfile
```

-	Layers:
	-	`sha256:262d3d3abcd873bd29005e1cf57a37df4622b86e7360df36aca2910c43e52f27`  
		Last Modified: Tue, 09 Sep 2025 13:20:53 GMT  
		Size: 7.8 MB (7771370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce6f47d8b471eaf0f99743dbeb9236862bb81f040386fa3d36e628eade19f89e`  
		Last Modified: Tue, 09 Sep 2025 13:20:54 GMT  
		Size: 7.3 KB (7296 bytes)  
		MIME: application/vnd.in-toto+json

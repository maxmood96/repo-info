## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:21f5f9e4c3e3b6aba3d5cbbf98eb833ff4be9b4907fa5e1b6c3e719677850092
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
$ docker pull buildpack-deps@sha256:57920e30e8e2a49e5614db78f182561763b0aa965b8cdfebaeeee2c2f0ffa34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145284256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d046964e84cc8b77c6ec59123a044bcaaa855d6a891f23fcbba44ac2157717`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5da413a3f50eb44f07bba0eecd786bf3efd93a4ca4c52ba8109a9b9ba14e688b`  
		Last Modified: Tue, 12 Aug 2025 21:13:15 GMT  
		Size: 49.6 MB (49562283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3d257b869b2a60078b7a65964ab94a9b367c5ab49593e2c17c1f7845cf6eb2`  
		Last Modified: Wed, 13 Aug 2025 06:40:49 GMT  
		Size: 28.5 MB (28535525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d86fe6006038239df0ed2d48c27073d2bc03b5547e42ef3e28ba6ae24c42e7f`  
		Last Modified: Wed, 13 Aug 2025 19:22:34 GMT  
		Size: 67.2 MB (67186448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6ce64799ddb2db2a8ab4c5c16618193be88e29cebedea7c1369482dae9dc7030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6451494ede8156481ae8b4dc7bc9e9ec7792ba0809daa55f2117f83ac8873dc0`

```dockerfile
```

-	Layers:
	-	`sha256:258b8e74cd89877502fa2c82355303b369e97095ef8f0afe8ae2f0b2e1bcd14f`  
		Last Modified: Wed, 13 Aug 2025 19:20:59 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3ef7ec47659e0026d73e81028a2a84898cb822913df884b2041701b19b203e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153724344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f51005a38b0516dd464221116f8a63756e873727a7498678d04c43f46cb74e6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ae7a451fcc7e9bebf7ef51b031f5ec2600e7c017efb66e1de76397538aff917`  
		Last Modified: Tue, 12 Aug 2025 23:09:05 GMT  
		Size: 53.1 MB (53147748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48ea27c6408465e04631c45f46084191d49262124cafc6550f5e911abd6374`  
		Last Modified: Wed, 13 Aug 2025 12:14:50 GMT  
		Size: 27.1 MB (27069254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca3385b479d65092a57bf9f294af41066b99dc31de27938a478b8d7dae4e82e`  
		Last Modified: Wed, 13 Aug 2025 21:22:30 GMT  
		Size: 73.5 MB (73507342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5fd5509dfba0fd4238f908b06f6b2001c0c87581e342b75d01beb79574934742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7793573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b4b0692f1da572640c2b3e5c7a01927c4af78b5cb8aac0c8b3983132acf882`

```dockerfile
```

-	Layers:
	-	`sha256:c0074d81b89cce6ba88a03eff5ea43547dae8bf4313966161b172e4d6f96f3fd`  
		Last Modified: Wed, 13 Aug 2025 22:21:46 GMT  
		Size: 7.8 MB (7786244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adb3071410bd40a9d534a82119f5afe987e2813e44ab56d324f173858b9e579f`  
		Last Modified: Wed, 13 Aug 2025 22:21:47 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9a984e3065d82cd534a7df44d5c55f68055509c51c3dbc901e27263b6effa08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139941891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fa80fa3b0ceed85fdbb84e2b85349b6bb6170291b2f5f4a2b8de5ecb59ab75`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a9e91ea2edc2d111f6a67eba934b0ebded0b74c51de6a807b73d07cbf965e132`  
		Last Modified: Wed, 13 Aug 2025 01:03:20 GMT  
		Size: 47.8 MB (47776559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64af9f489cd1777e5b300ee5ecaa1ee0eb257910fbeea3b4885aa18546f4677f`  
		Last Modified: Thu, 14 Aug 2025 14:45:40 GMT  
		Size: 25.0 MB (25043691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ca0dbc65f78a497c831d706ac3403d38aa6f98f2a4e700c685ca0e3cd72cd3`  
		Last Modified: Sun, 17 Aug 2025 07:42:58 GMT  
		Size: 67.1 MB (67121641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cb9940a110035883ae07b786aa7d37fd2ca69184d9198b029abaa1236572c19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2209a09910b21f2d95c9cb3acb799305eabb2a800e94c8b45c5a5fdbed22c21e`

```dockerfile
```

-	Layers:
	-	`sha256:e0db5cee89cd9e0e4d0931dc4c4a69eb258c3e8177a88dcd08b144b079617d45`  
		Last Modified: Sun, 17 Aug 2025 10:20:50 GMT  
		Size: 7.8 MB (7768899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3635fce3bc436748988d18d58000aaf8b56a04bc69d639690367bfe9dd858bc`  
		Last Modified: Sun, 17 Aug 2025 10:20:51 GMT  
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
		Last Modified: Tue, 09 Sep 2025 11:45:53 GMT  
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

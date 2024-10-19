## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:b7b31cf258096b5047be55aa30dad94e2ceb052c8c9e10c00d35725b10ec1bbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:stable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e413426d5ceb4bc8b8485584a2334f982af09c40a294c8bf8bf6cdaeeee9875a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137996104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6a3fd709dc98777b4ee2dac0d91e0d775c501c5f754c2721afda51367884fe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aadc5092c3b7a865666b14bef3d4d038282b19b124542f1a158c98ea8c1ed1b`  
		Last Modified: Sat, 19 Oct 2024 02:06:37 GMT  
		Size: 64.4 MB (64389695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:267daf9a035387db438e0e46fd4b93300a407ab8d2a8a08471e53480601da952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b34fb506a8ed23e1d427f349569ab9a18e6805d6de10ec99ed6a589dd583cc`

```dockerfile
```

-	Layers:
	-	`sha256:9f092bdcc560f05d219daef70c3dbe1cbf5beb875614df187738facf640574ae`  
		Last Modified: Sat, 19 Oct 2024 02:06:36 GMT  
		Size: 7.8 MB (7764370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:305b58c6aa4607a016c86411aaec62620a8480a7db911cf2b1b620bc59033585`  
		Last Modified: Sat, 19 Oct 2024 02:06:35 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:065821ca01f5b46e546b666ebc542baa9cadd26c83971d920f718a4d04641532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132056978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c329746ec886de5abee981e2a8dad46f0a25ec5606516321a628ea9cec7098a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:f8dacf0eafc6476110951ab49fd75768d4262a1b61984cf9b4625bdd369500eb in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:638c60a841003707ab5971d86e3c262372536df80608e7e3641e6ad7f5dff43e`  
		Last Modified: Thu, 17 Oct 2024 00:57:04 GMT  
		Size: 47.3 MB (47330521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74674b1e8da5cd0bdb2b88260b7dc90e413cff1e3bb65d3d272730dbf8690e00`  
		Last Modified: Sat, 19 Oct 2024 00:54:46 GMT  
		Size: 22.7 MB (22729575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2d8e5c6c3bd120c07665df831c223d98cd86db7ad072c55a7433e227d49b3d`  
		Last Modified: Sat, 19 Oct 2024 02:55:37 GMT  
		Size: 62.0 MB (61996882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:993bf84285db8ca4c11425d3a303adbe960660b326c4fe16d6692cff7d2cab22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7175b75d18a4b7c149ef131238c169805dae0110254e68d196b78cef76713d9a`

```dockerfile
```

-	Layers:
	-	`sha256:8b6c17ef335d13a13ac672b98127369486d26b77a478f85e6dda04d194d55425`  
		Last Modified: Sat, 19 Oct 2024 02:55:36 GMT  
		Size: 7.8 MB (7765924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1348c0de7b4712e505c350d0c2142d3801c2c26e7c23faa55c9ce197ddd624d2`  
		Last Modified: Sat, 19 Oct 2024 02:55:35 GMT  
		Size: 7.7 KB (7734 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:eccb934d63bac8c068380c9805d9b43b7f336b4c18f3240641a37e90dca17cf3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126744870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e0a5ed5211488d49c46201bd0003329cdeac002c563154869325cec7f1e5c0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:11 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Thu, 17 Oct 2024 03:03:11 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3332329de6b42a2c5f534a6f40381b05e4356eb62a42408f66b4d98e78cfee55`  
		Last Modified: Thu, 17 Oct 2024 03:36:59 GMT  
		Size: 22.0 MB (21957453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d531afa8550e37b4fb5ecf878018cd17fb79413ab81359496c3eedd8bb0abca2`  
		Last Modified: Thu, 17 Oct 2024 03:37:18 GMT  
		Size: 59.6 MB (59639477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:24ff51eac951beb8cae6eb10c9a6316b92ba535f6ce57b697816a2f90d9e35fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137528678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d53a93f46b21e92bf85f52aefd48305b7987e7037693f374d44cb5e8ce0324`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:49 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 17 Oct 2024 01:11:50 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:30:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:30:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437f71cf1903685ed3f6314161e121602758f809a760d2bd2293f7cd8ce1abe1`  
		Last Modified: Thu, 17 Oct 2024 04:36:08 GMT  
		Size: 23.6 MB (23594190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143d0f027108dead9d56047ebcddbf6b5ce9a7d51ab49ac1eeef8590e7bd9764`  
		Last Modified: Thu, 17 Oct 2024 04:36:24 GMT  
		Size: 64.3 MB (64349510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:273c4a697c5f46c260ff0dc5ce28da78d7895442714cfe2ae670c62596c94c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141680190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f891597f8aa0b920eab180791c23ad8f9ffc9da20a5a68b66b0c2a936320a4a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0968576d52726552d23c39a66f1a0ba3f2ca10d188a4fc6750691a97ed494efd`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 24.9 MB (24894938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118b4d3aa7d5b42c90f2dcf856bd26bfe40949f5a30646fbc676721418903875`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 66.2 MB (66208418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f7c27a970016230430108f980988c338d4d1137a98cd2b936476020943ea3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0fde0a53d069f07ff292e0334b827638c5a995a20f008cb02dca195cc9b24f`

```dockerfile
```

-	Layers:
	-	`sha256:e43a3a69d39b1261a900b087590ce28109339ec7b0fb043a670c0683b9cc0a50`  
		Last Modified: Sat, 19 Oct 2024 02:06:21 GMT  
		Size: 7.8 MB (7760446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f61feb336f32426818cb28c5c4aae9e6aeea748ea4612b3d85b14136f23d82a`  
		Last Modified: Sat, 19 Oct 2024 02:06:21 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cadf76ca0578af7d2c32dce3d1860f04b28959bb1cb0f27e982288bba02c972e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136494026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0434755538859a36858a1cf943ffb9a3464378e9371f90644cb583fdfeefe551`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba3cc6e574320e30c42f84b70c8e03fff0393ea65f20833b10b3a8aa1415e1`  
		Last Modified: Sat, 19 Oct 2024 00:56:12 GMT  
		Size: 23.6 MB (23648020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d702889c46052954a44f8b6ab39510d9b55acfe4a180194a7cb475c90b2b76e`  
		Last Modified: Sat, 19 Oct 2024 02:08:09 GMT  
		Size: 63.3 MB (63284387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:821b714bf8d6778d6d1b920a2baace275ae17c38d2e45770d4702d64b3d8634a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae759b8a8a22e7725a44091355ef141327e65f7a7442e018dfb5b90b94cf0cce`

```dockerfile
```

-	Layers:
	-	`sha256:7bab8cd7f7cc5b0a4b903dd7d23a799c7767e8dec89874cd1de2cc7ac2343c85`  
		Last Modified: Sat, 19 Oct 2024 02:08:03 GMT  
		Size: 7.5 KB (7509 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c927f08d08e798a2932be4e20dad881e66c13708cd3fd12432a15db03914f304
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149095404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a195c447ca2ab15bd44723fc52ceba6b8484d8f8e8b74bf23786dbff4233d1a9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:38 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
# Thu, 17 Oct 2024 01:18:40 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:42:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a4688a74de76e26de6977ef8438b7e0161edaee4d986ee61e62bc0b84b1163`  
		Last Modified: Thu, 17 Oct 2024 01:51:23 GMT  
		Size: 25.7 MB (25709972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8022c20c080be7d80dd6512a4c9fed59039e755de95495c76a32f7c2baebf1`  
		Last Modified: Thu, 17 Oct 2024 01:51:43 GMT  
		Size: 69.8 MB (69829835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:96caeb2a156ac3e5a114582e769104d80579b8f79601b73c7f453b4d8c947bc0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135485414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849e1c7b1cd0aa3c234e84d733980139487f92521f08631a58f63d02eb0e74d5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:45:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Thu, 17 Oct 2024 01:46:00 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:40:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:40:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba66dca1247069bbe2e2adfc1cbc055a99250a0e8c3ec2bfbbb419a1f58e5bb5`  
		Last Modified: Thu, 17 Oct 2024 03:48:39 GMT  
		Size: 24.1 MB (24051978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d236e9b4fd4c23047a10cb64d0cfc027a005094af65d82f927b8a39dfe85c14f`  
		Last Modified: Thu, 17 Oct 2024 03:48:53 GMT  
		Size: 63.5 MB (63494989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:aa1965cafb65cd1563aef360378821ad9464d3e4cd1845d6c45ebd2aa60421c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1cd481a380b6886c7c12738343b41c1ade28dd9c6a1c234de96a7589e732b5bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125525311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122e37db456fe0272fd5e6fffa8741d29df7a636e562ec6693030987d215d040`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:081f6e87de1740da2f39512936ee31f910545d1ca95c9229fb78554f5ca87186
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120421792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2645dd3716edb9848cc994161b027f182e7b8ec17552dc88ebfe4f04e339c4b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:19:10 GMT
ADD file:711abc0c0a502fe727f811a82e7e6175c753593bc9f6d477a47b889fc3fe8ff6 in / 
# Thu, 17 Mar 2022 05:19:11 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:15:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:15:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 19:16:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6db9b0909e16205c253a4a6e736ed382b68f85839d7822d22d5ddd35fd2fda4`  
		Last Modified: Thu, 17 Mar 2022 05:34:11 GMT  
		Size: 52.5 MB (52470250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd49582c7f6675ebcf6ce05a8c46ca03963dcb872a6609647908e9f3ec1bdab`  
		Last Modified: Thu, 17 Mar 2022 19:40:09 GMT  
		Size: 5.1 MB (5063869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5be2734ad2363ae06404b77e944bcdb8496677704f50b8b579838e015ab189`  
		Last Modified: Thu, 17 Mar 2022 19:40:11 GMT  
		Size: 10.6 MB (10570982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e806b3e4bd3a2bcc0347f8ed2951681ef09caa248f10c65740a1e875c73a0f`  
		Last Modified: Thu, 17 Mar 2022 19:40:52 GMT  
		Size: 52.3 MB (52316691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:35c32afc6ff86fbc3fb2cc18654ad77c8e4cee46e02a0210c20d30ef67dbb08a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115584420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53356b02ba0d76fb4d6b20cb3f6ee97f6b19aeb3128466428725882190885943`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:17 GMT
ADD file:b388eaef074fa7cc4e0f6f0b6a56e4be6c69489b63477ab4469ff5415074b0c7 in / 
# Tue, 01 Mar 2022 02:02:18 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:26:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 09:27:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:17a41fc762495ca54ac53f271889bdf4ac8bea7cedfa3b585e4e42ef106935f1`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 50.1 MB (50117069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9173ee01c42f46f1839650f0a56ee12ab74693f31dacccf586222ef98cb4ec19`  
		Last Modified: Tue, 01 Mar 2022 09:51:00 GMT  
		Size: 4.9 MB (4922642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f119f27841bdc8ee96fe83e4e2bb9b453db5a3a239036547b8e09c87f650befe`  
		Last Modified: Tue, 01 Mar 2022 09:51:01 GMT  
		Size: 10.2 MB (10216974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b827df064e12020cb42fda8ff122cbf83eda05e2c27240cc0dcb551be21b6ef`  
		Last Modified: Tue, 01 Mar 2022 09:51:51 GMT  
		Size: 50.3 MB (50327735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6754ae79da3a0a1282e7e6619f895746b32b83c93b468a40a9ab1a5a188b4646
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123881046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f63a7e09c5ad7ff69697a44dbc2ff8fc8220a45b2db417b5ffbe9bfbb15a0a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:41 GMT
ADD file:5effc7e0ab7312f14a7ee81c06c71400aae31219d477ebe1a4f7a9156797c42a in / 
# Thu, 17 Mar 2022 03:21:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:11:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 22:11:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:260ad8146ed2447d5587608b10fed4f80de80cdc559e619f3a235d3ba09eaf7b`  
		Last Modified: Thu, 17 Mar 2022 03:28:04 GMT  
		Size: 53.6 MB (53616308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1399f445da611be3789923cf26d158e3f4f80449b7295fa069a8eaecaaf137e6`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 4.9 MB (4937558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd9e43777fa6c09c341f3aa922f47b5b3ace26de1d779124afd2f1d435731d9`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 10.7 MB (10655858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f81267e40a2df9e572fe797e45dbc086008422eb2216df18b7a91f1cf13e22b`  
		Last Modified: Thu, 17 Mar 2022 22:21:21 GMT  
		Size: 54.7 MB (54671322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:77edc22f46a8aa89c71bfb503c225cad6cacace3bb3041af1ca453b59c33be81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128392018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ef4112402fea805eda2c430d8a56e451a7bc828da69c352ca78dfb994ba623`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:07:15 GMT
ADD file:4341f64e7f1accc7f9737a9896bf50c6ba8f51698e52c594d9421fe4f2374e2a in / 
# Tue, 01 Mar 2022 02:07:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:40:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:41:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 05:41:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5cf8159e9217c5f37fe58b260cacc1d132c2e21ca58c769d29c6eb720993a304`  
		Last Modified: Tue, 01 Mar 2022 02:15:15 GMT  
		Size: 55.9 MB (55938747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700db29f99e559f6f1909315637ddbda6667a35bd437b9e5d8c3beb373c6c1f`  
		Last Modified: Tue, 01 Mar 2022 05:51:55 GMT  
		Size: 5.3 MB (5283081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff041f2862924d1932eb1f5d7b01079bf8015dcc0dbb94a23d2475b8684d875a`  
		Last Modified: Tue, 01 Mar 2022 05:51:56 GMT  
		Size: 11.3 MB (11250640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ec658b51a80445b805d19e0462b4112f90132f61a78d8d7f5b29f6903e1e44`  
		Last Modified: Tue, 01 Mar 2022 05:52:25 GMT  
		Size: 55.9 MB (55919550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3554af0c6c98229922473d6ced6ad68ffbcb239b1b6f6f612dfe7ed4428c8f01
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122054452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50832c0d9e42109f1087a11d1286cd6bbebb5a28e888635a8a87a2de03069719`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:52:25 GMT
ADD file:f2f4496058901761fb8d3cc93b176b91332f07b531477abcf8b4e96df093d60a in / 
# Thu, 17 Mar 2022 08:52:29 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:21:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 19:23:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:73de72abc870c163c22dfe15cfe1ed937cb3f6a4bba21ece0d7fac49af0e3cc0`  
		Last Modified: Thu, 17 Mar 2022 10:42:38 GMT  
		Size: 53.2 MB (53187444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb7b2d10882abf71983dbea94cab908337239922a3f811e1a7bf38adea36a37`  
		Last Modified: Thu, 17 Mar 2022 19:50:49 GMT  
		Size: 4.9 MB (4910812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd267fe158b034479e5b906b37e6448e4abf719a073250d1670bc4859f1ea46`  
		Last Modified: Thu, 17 Mar 2022 19:50:52 GMT  
		Size: 10.7 MB (10658789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fd9f036e1e2b8bfe724c10bc3139cd9d66d005d798076c93e9d660332db9dd`  
		Last Modified: Thu, 17 Mar 2022 19:51:42 GMT  
		Size: 53.3 MB (53297407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8f1f3d437885dba6528db53b19c9b43fe4c8fff6f4a140fc6e4143ccc269e916
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134715847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dd9880c8ba2959f6888a9d7bdb0425038cd58f3237f278ddae37698bc1e527`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:04:22 GMT
ADD file:00554eaeb433a7cc43c22f2544d800896f451a2e5a7895863c4651ed425b8c36 in / 
# Tue, 01 Mar 2022 02:04:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 07:06:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 07:07:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 07:09:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9ff352265b4a055377b95db6dddea03717bbefbc7f30fbacf493764d617ae85e`  
		Last Modified: Tue, 01 Mar 2022 02:14:41 GMT  
		Size: 58.8 MB (58834115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6e10a400e162a4b996dd3e9c41cf812cfdb85d9830543b1c0b42305ab08b61`  
		Last Modified: Tue, 01 Mar 2022 07:42:05 GMT  
		Size: 5.4 MB (5401790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7ac604ebf8c0f6690f9477f7cba586130342d01fb167fc710f6621475e1786`  
		Last Modified: Tue, 01 Mar 2022 07:42:06 GMT  
		Size: 11.6 MB (11625870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20dd043e4a99bc0c4d1ed0c5ead9dcddb30bb43c85f40f573a87b12292f70b4`  
		Last Modified: Tue, 01 Mar 2022 07:42:32 GMT  
		Size: 58.9 MB (58854072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ad3263ff9c5ac4e4596271d8ad8f6d74cbcd9041b5f353ae4bbc7a4399b714c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123160906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d8d0507d7ab7edb93b6c2308ea8f0c981ed134368bef9cd8b7963a148b3d6b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:38 GMT
ADD file:75b45e65d2ec2c6822b1ddc46ff159dd10ac56bf9dff8b0996ac589a1ede22ff in / 
# Thu, 17 Mar 2022 03:06:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 18:20:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:20:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 18:21:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ae9f1a186a2633be1ad71c317c2f195b221cef89502f9edc510b3a2049723758`  
		Last Modified: Thu, 17 Mar 2022 03:12:26 GMT  
		Size: 53.2 MB (53217527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d6229369d1bac8aa97bfefe6dd7990a66c0a3e98f420c282a39a279df7c391`  
		Last Modified: Thu, 17 Mar 2022 18:29:06 GMT  
		Size: 5.1 MB (5137013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf171d8059efb2bc6c026904c68dddd3487a129cd53d33def9589665326d56f`  
		Last Modified: Thu, 17 Mar 2022 18:29:07 GMT  
		Size: 10.8 MB (10761392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cdad8e45654b094c248eb6bc86e3e0d8dda7b0e1df7c2792f2abb3a0d18cc8`  
		Last Modified: Thu, 17 Mar 2022 18:29:23 GMT  
		Size: 54.0 MB (54044974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

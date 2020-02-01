## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:de6028bd24d727f3ad9f37b7833b7835515e6592cb2bfdbe87fcd7274829051c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:79d7e913123ad5a395da423bb96db30af6211601608c7fca47c7baa04cd2a51f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124324923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ff35416fba9abaac38d418d80736ccf0beef7e0e2908b67f19ccca01192207`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:22:47 GMT
ADD file:68b1541306250f957e5f1035d80f5683c1ed22e73cf2f2b563adc52424897a09 in / 
# Sat, 28 Dec 2019 04:22:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:56:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:57:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 04:57:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d0b468739e287d7cd8fa8bcb34afb10216f12567d28caab345db8873c4246896`  
		Last Modified: Sat, 28 Dec 2019 04:27:19 GMT  
		Size: 51.5 MB (51479608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44261d6f427d89f764fcd9898d2845c7327812575dcc485436bb888b2ee1d0c7`  
		Last Modified: Sat, 28 Dec 2019 05:03:30 GMT  
		Size: 7.9 MB (7919965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd42132ce8afeea96ec992f4170f1b4fe9fa1a621a93dc2d236088351e29685`  
		Last Modified: Sat, 28 Dec 2019 05:03:30 GMT  
		Size: 10.2 MB (10183322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c16ba6f425320c83bd55536bb502f6e0b7064468bed05a5dcdbf0a13e9d892`  
		Last Modified: Sat, 28 Dec 2019 05:03:45 GMT  
		Size: 54.7 MB (54742028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6c4167c38ea49be53d627b1057f46e053088bb1e61578357c5ef364f3635b0b1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119604414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b0afa7f71c6f0cacf05178c853926efa760afe4888827a83e7b203db855f07`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:52:33 GMT
ADD file:e863dd2efdd5f4a6e29a4da391218d83cf13d07b263a55c438361d48079dd528 in / 
# Sat, 01 Feb 2020 16:52:35 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:34:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:35:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:35:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:25551be68c42d4da1cad9359e21cdc842a69363b035a77721ddf9ad7db276105`  
		Last Modified: Sat, 01 Feb 2020 16:59:21 GMT  
		Size: 49.5 MB (49540705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718af626bdc2f1b7d5facec6b5ba8016afa8bb5d691f4ead7274c55588a7bf48`  
		Last Modified: Sat, 01 Feb 2020 17:47:57 GMT  
		Size: 7.5 MB (7494164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19493feb9c608ccc1c197cb34c49c8902d9e560ef999db9500a91a6244e10e0d`  
		Last Modified: Sat, 01 Feb 2020 17:47:57 GMT  
		Size: 10.0 MB (9974015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9e0dd91a0c5d9c8d98b8511ad3af8cf0d03337280a36a0032e81abf0aaedfc`  
		Last Modified: Sat, 01 Feb 2020 17:48:25 GMT  
		Size: 52.6 MB (52595530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a268b21da5df37140958d0041c81a338f441d32c67fb7c6796dc012fca2bb2ef
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114167398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab25a969a5337470d1a9461b1a7679f1fef1e91e392dc29af844c0fd9a892bf8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:01:32 GMT
ADD file:b5c7da33763f5d6cace9605e53bf483375c1f792de0982f47885c85b47304392 in / 
# Sat, 28 Dec 2019 05:01:36 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:55:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:56:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 06:56:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9d5856d0eb425d736e9f4c60a79333c1933bada38a126c109eff8f1eb43a9c21`  
		Last Modified: Sat, 28 Dec 2019 05:09:48 GMT  
		Size: 47.2 MB (47210722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3768cabb2504bdc0d3bf15c2e022ab2e94f61e198eb24b077cb6c5e620d5ac`  
		Last Modified: Sat, 28 Dec 2019 07:09:45 GMT  
		Size: 7.2 MB (7234041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfad613eea011450300250c8f76f687229e6483a59e575849962e519e171c0b5`  
		Last Modified: Sat, 28 Dec 2019 07:09:45 GMT  
		Size: 9.5 MB (9529582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdba93dc41685dd6b3cc9be45d32c5995478ce980c4972401e0c1b17f7c5c70`  
		Last Modified: Sat, 28 Dec 2019 07:10:09 GMT  
		Size: 50.2 MB (50193053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2070060cb2ee835dcb802dba2fca6aab04e8da311fc33641af9addb30efeb5cd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123675555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66e710292cb076fa6bbf8256932e4ded0bd0de3255936a50bc14c3ab033f75d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:58 GMT
ADD file:636edb6845120aa418f3291c0858ab38c7d658cb2790c08b113e8068fe152a32 in / 
# Sat, 01 Feb 2020 16:42:00 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:26:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:26:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:27:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a3f06cbd9a524c44b9b8c92922dc9c06d87668d76af414bd34aeb7238502e475`  
		Last Modified: Sat, 01 Feb 2020 16:47:18 GMT  
		Size: 50.5 MB (50505966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66da598f357ac8ab4c813dc7a16cf57b1d0fdc7579b59a9a2cee24efb09f057d`  
		Last Modified: Sat, 01 Feb 2020 17:37:33 GMT  
		Size: 7.8 MB (7793001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a8f172b9e64796699f56dc5a838982165c0591f68740791b1d1e8971e09602`  
		Last Modified: Sat, 01 Feb 2020 17:37:50 GMT  
		Size: 10.3 MB (10252714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48a71f1808040c4e34e7856e42f28683335784039b75aa3cc9c48c178a2bced`  
		Last Modified: Sat, 01 Feb 2020 17:38:15 GMT  
		Size: 55.1 MB (55123874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:db91270a77daf6a2feadaa520afd5859c51c4e27f5788c4a0ba5c0a43c95fe98
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128154903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80c3f50d7a1cf44c1d004084cb29aefdc57b8607aa1b95c2ccd998ffa84340a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:00 GMT
ADD file:941e54a7461d61d84748dacc44e888cce50acfb10e34f38a7e4083e19f23b7ce in / 
# Sat, 01 Feb 2020 16:41:01 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:36:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:36:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:37:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8901e4e25f1677947cce32c9111e1a14e167a08c1c9b0f38aa3b62ad8dfa24aa`  
		Last Modified: Sat, 01 Feb 2020 16:46:18 GMT  
		Size: 52.7 MB (52679793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a37f13c8736e8d302836bf7f36d02b6d21c78ea34eaa0d441bfac8ab1e8c15`  
		Last Modified: Sat, 01 Feb 2020 17:44:29 GMT  
		Size: 8.1 MB (8093419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf161fe0fa72e46e5ea25da7008f0141c7c33bd269c543c8f95df1e56c25b90a`  
		Last Modified: Sat, 01 Feb 2020 17:44:29 GMT  
		Size: 10.6 MB (10622239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3013dd71e2203e20bbe8863f8023cad80c4bcc8e6c089ef172e39590a4d889ee`  
		Last Modified: Sat, 01 Feb 2020 17:44:48 GMT  
		Size: 56.8 MB (56759452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:835bba8392d7ae18ae9c353d0629eb80e5758cabf2fa8ed60527aef4fc17ab64
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134623764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c467d7c2fe1ff62c21d62ba23204e146a1278136c7a28ad5982c0199ea944a2d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:44 GMT
ADD file:d7ba1f92f51134645d0c28cccf74dc6cc9cff62c18d1e7ea24e9306b603cc4c6 in / 
# Sat, 28 Dec 2019 04:21:49 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:04:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:04:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 07:05:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a19f8e61b2d8b008c7115d66fcae892bce80e022931657219cecb2a15110c398`  
		Last Modified: Sat, 28 Dec 2019 04:29:56 GMT  
		Size: 55.3 MB (55284979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814b37b063181f0e69d2ffc211b88d130aa8935273a93f9155d2df7a1bf9c150`  
		Last Modified: Sat, 28 Dec 2019 07:23:51 GMT  
		Size: 8.4 MB (8352650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1122a79a4397f123afc0998256257fa3fcdfa99567d9a6e43d19cdaac02f9ee`  
		Last Modified: Sat, 28 Dec 2019 07:23:51 GMT  
		Size: 10.9 MB (10946018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5501c344b50ae868e0144d013d546e02a4c4033ebe9c8fc067ee90f568efc396`  
		Last Modified: Sat, 28 Dec 2019 07:24:22 GMT  
		Size: 60.0 MB (60040117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:39cb10631e1868c25c56cd9722ecfa6cc30b305739f7d25649754d5a2580fcec
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121778415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59f36874eb9b666eea6d246b673a952ec0cb2ad57ffaa2eee91aa1aa7a347d9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:32 GMT
ADD file:ebe1df568622bb8e8e8e3b2318d11550389d84f3196d3ade9aaa9ecfdecd1028 in / 
# Sat, 28 Dec 2019 04:42:32 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:47:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:47:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:48:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7d0208a582df93acf7a81d059abd969865a1e647765a53c87e2123fb6b283a34`  
		Last Modified: Sat, 28 Dec 2019 04:45:42 GMT  
		Size: 50.1 MB (50131585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46a42bc5c7805eb22e48c27565c0a108b60dd3c74386aea7cb2a2b367d00d07`  
		Last Modified: Sat, 28 Dec 2019 05:54:12 GMT  
		Size: 7.6 MB (7591630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77c311db77933f5cbc7d2dc6e649e1d95c34ce4c806932601722b88f9b28a61`  
		Last Modified: Sat, 28 Dec 2019 05:54:12 GMT  
		Size: 10.1 MB (10069342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc903c6290ae481b2ee639d7b0ce90ef144f5db8cf1c9f396e521df9b32214c8`  
		Last Modified: Sat, 28 Dec 2019 05:54:25 GMT  
		Size: 54.0 MB (53985858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

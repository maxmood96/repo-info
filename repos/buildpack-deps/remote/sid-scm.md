## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:4d5d589472865acaa45c1f7f25bb87f009ec6529fcaa5f46e0824ab4958915fb
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

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ad133adbe7e0146e99e98c5e4ab656e46458168ead4a0c028b982fe9b51124b7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140363730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2bc5255bd0ed2b35e7ca6ec06a8ee543bb36dc32e42e1701b67ef0bd335561`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:21:22 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Thu, 17 Oct 2024 00:21:23 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:06:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:06:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd12486823035917e2bdfef20e61a67c184360d98ed6ebd28bb57588bf93a8a`  
		Last Modified: Thu, 17 Oct 2024 01:11:46 GMT  
		Size: 20.6 MB (20559740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea70d03627f3e5c406d1ee5dff15665aec2cced533a490d601ee7442319226e`  
		Last Modified: Thu, 17 Oct 2024 01:12:02 GMT  
		Size: 66.5 MB (66532116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:01d2dd0dee2fd58f2253a6f26e754440b8c0515b6171462c890bfb5257a16def
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133319694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24d0b4c956ac03e07ee2103998239b5293708df10144188615f97ae3e5c8720`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:29 GMT
ADD file:4e733f6ab5ca47e96afa5484ac2356542259685b0f38d5370aaf3ff6efd60b52 in / 
# Fri, 27 Sep 2024 03:19:29 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:59:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2dab2d41b4d3c1013596d851ef68dd96a59ea71db4c50a8e9daec6977beb1e9a`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 50.1 MB (50141188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45409b0518e0782369823c9bfaead974fdd198f9b729525b7784d928cf3f7973`  
		Last Modified: Fri, 27 Sep 2024 04:04:32 GMT  
		Size: 19.4 MB (19423742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03463b6c07bccc1364fec128e533c62c4e2533ee53250fc1153a70167b6f44b`  
		Last Modified: Fri, 27 Sep 2024 04:04:50 GMT  
		Size: 63.8 MB (63754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:17cd05150504f279feed04079948b74f6e364d1682b04e9040e80caa426db01c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127662177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a55dab28cc2ae523f094e6efebc21ebe56b8b362c582c1c533e962dbed93e7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:14:39 GMT
ADD file:7c02e68cb0d4c1b545df6c3c1548fdfbb0b8728190927f1aa0a481628eb80842 in / 
# Fri, 27 Sep 2024 05:14:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:33:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:55055767cac3db3f353667eecf5967bd4d61aaf6f68b845d1c472311762c6497`  
		Last Modified: Fri, 27 Sep 2024 05:18:38 GMT  
		Size: 47.7 MB (47656889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe7ba8ffc1ff9cdaa583c4b78a356d900036e41391f4ad532ea17ef7226ff6`  
		Last Modified: Fri, 27 Sep 2024 07:40:59 GMT  
		Size: 18.8 MB (18770645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cad0c26ab0027c184690fde3603662a1fe5a37591c336a98696770ac66936e`  
		Last Modified: Fri, 27 Sep 2024 07:41:21 GMT  
		Size: 61.2 MB (61234643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5f513a1c5f215d83b71b8cbd64ca21887cb12f01b07695a7ffdf01a67e2b0fd2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140036229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36031ec48fc57c491b354b9d8b65ff95c5876b9efaab45a0c871a1ece21d7b30`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:54 GMT
ADD file:0530740e6d33fef9d1d8ba1df1cda3d2bbd45ee34654975f96a8cd318b315f82 in / 
# Fri, 27 Sep 2024 04:38:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:21:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99a192f51b57a678feb659bcbaa8cde28d31be7455d5517ca87c1d8fba2866f1`  
		Last Modified: Fri, 27 Sep 2024 04:42:11 GMT  
		Size: 53.6 MB (53594265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fc848450eda758c5f4c056230d289d3bacb82835760763661a9b5aebb3758a`  
		Last Modified: Fri, 27 Sep 2024 05:26:37 GMT  
		Size: 20.1 MB (20139073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd393ac9d5f3e6f4ef01c240e4ee33361f9163326dc4fe0c98ca544756cddc12`  
		Last Modified: Fri, 27 Sep 2024 05:26:51 GMT  
		Size: 66.3 MB (66302891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fa0b5613ee13ef0010892bf1f971c9d195718955a9180c5767d52a77495ccb7a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144136404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6cbe719c841d593cf0938b232d2f88c834542d6721dea9aef5aa775ebaaefb3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:39:51 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Thu, 17 Oct 2024 00:39:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:06:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15aaf6c71ee896572e8510fe4d438d0dbd76161c333521b2012d9264e2e14151`  
		Last Modified: Thu, 17 Oct 2024 01:12:12 GMT  
		Size: 21.7 MB (21665512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baf36563cbaa64d32ebee9da5e6774f7c3ec5c4ccdfca4ab2bd2c321a22c66f`  
		Last Modified: Thu, 17 Oct 2024 01:12:33 GMT  
		Size: 68.4 MB (68352915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:81b3eb351c29e1eee6d71447de5ff65324ab8ab5f47e41527137e7f86f17a573
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137919932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4aef28a5b9c90b1852dff723450b8f097427b7efea4336d6dc48df2542219a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:03:44 GMT
ADD file:7373f4e4970ea9ada45c8717ca5498ffa4ffd9d16a9261475e1291ae954742c7 in / 
# Fri, 27 Sep 2024 09:03:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:42:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 10:44:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b63745dc97c5bfb473a84b3b12d099f6a8a1ca3adb2bdb16407181689c5a9724`  
		Last Modified: Fri, 27 Sep 2024 09:12:19 GMT  
		Size: 52.1 MB (52125578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ffc0b3c363e12b941d7e80d3bb54718d788594c92b04828cf954025257521c`  
		Last Modified: Fri, 27 Sep 2024 11:04:48 GMT  
		Size: 20.7 MB (20727164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3d0102a70641af727b17e4dda29d3e752776fe5f927c48dc6ba42534da6baf`  
		Last Modified: Fri, 27 Sep 2024 11:05:38 GMT  
		Size: 65.1 MB (65067190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:41ea68f4856fcfc92d08450a4e126e0e2e50ddc67d7083e73f7989e8588b0c90
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151774909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ff9635ca0f0e2eb1753e1b9d77119fe5100e04cb5dfa6565bf38e395943cc8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:18 GMT
ADD file:61be8fbc8c48a038743e523ea5539b007c504e38025630b54f774464a5b21963 in / 
# Fri, 27 Sep 2024 05:33:21 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:58:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7d9882c6fe69b65aaa672267378b325d49eb761a1518c6646ba15eafea787b1f`  
		Last Modified: Fri, 27 Sep 2024 05:36:38 GMT  
		Size: 57.1 MB (57123161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5a7efb15e28989001836168c26f86cfa942d47c522ef07c07c02abbf8fb2a3`  
		Last Modified: Fri, 27 Sep 2024 06:05:40 GMT  
		Size: 23.0 MB (23025627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83256233144f0df0689578c0a89c181e74e6ea6cc435661a805b2a60809bd43d`  
		Last Modified: Fri, 27 Sep 2024 06:05:59 GMT  
		Size: 71.6 MB (71626121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0d34076051b03e658b59b9167c20d545d924469e7f2829509eceeb01e5b1f0c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (136960114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122d6b276a8d897277117783348c16c5fb72421b777ea13632a0d12e90f081be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 12:24:57 GMT
ADD file:60c08991ed6d648cb7220494e8e535efc29df9008317554c36bf5396cbdeafe4 in / 
# Fri, 27 Sep 2024 12:24:59 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 13:47:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 13:50:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5817b4e976e9e9f6db4fe62c9c9fe0f00a2b6fab03512e0faea17d129e7ef265`  
		Last Modified: Fri, 27 Sep 2024 12:30:30 GMT  
		Size: 51.5 MB (51526068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3ba3299436eec7913d1fba15e85531ef871a7696fe51c51a313fc9b814bc4e`  
		Last Modified: Fri, 27 Sep 2024 14:00:27 GMT  
		Size: 19.9 MB (19902277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9f4a99275f793e5c8e68b8d73f18d109d2b326d17fb8683a66ed765527984`  
		Last Modified: Fri, 27 Sep 2024 14:01:33 GMT  
		Size: 65.5 MB (65531769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b141a1e4d3e090f1289387b4f386a06ff9a10536d71467dacc45743ffc85c099
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141564885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f6067781a4b36d561c120b2a47b037fb544c7e50607d9658b7102c0a97c16f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:46 GMT
ADD file:5c5ad29b01b72e50aceb20af8172a88e23803553ed45c73a28a9a138856ba70d in / 
# Fri, 27 Sep 2024 02:43:51 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:15:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:17aa999733edd287bf5bd51ab2a58ef17211e311db82e8024e72304b5186e2aa`  
		Last Modified: Fri, 27 Sep 2024 02:47:37 GMT  
		Size: 52.8 MB (52808143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8d052710c80bb8f1ba5c4daebfc8ac149ed5b56a5185e5d6bd1a75f49bba31`  
		Last Modified: Fri, 27 Sep 2024 03:21:13 GMT  
		Size: 21.4 MB (21426030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cedf4fdb3f455010b1f7eeb3d9f24a25a7fd469356a31a9f5f4de26d8238f1b`  
		Last Modified: Fri, 27 Sep 2024 03:21:27 GMT  
		Size: 67.3 MB (67330712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

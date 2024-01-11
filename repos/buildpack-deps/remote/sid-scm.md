## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:eeb7cf04637637fcfde946b8182b244c21dcfb9efedf00f9899097698c40f431
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
$ docker pull buildpack-deps@sha256:360f365fd501976d00aec6605b48530cc151cfb3029b3c11281d9ccbc9755e41
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144827225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e752895bec72bee797d06eec6d32b01118e8195862f49de9698f6ee6d57906`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:39:34 GMT
ADD file:4c1ddd73138f061e46cb63a959e0b45e213bbe55a4e9859988b45cbe28c1939e in / 
# Thu, 11 Jan 2024 02:39:35 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:40:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:40:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f8012d8f125a645d98266e2a23733c0354f39eaae73d40ec23f48c12dac17e1`  
		Last Modified: Thu, 11 Jan 2024 02:45:14 GMT  
		Size: 52.3 MB (52267954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d4389e3b2cf1b1b5d2973b88c056f511579317121eba04eb993bb13d8092a5`  
		Last Modified: Thu, 11 Jan 2024 04:47:38 GMT  
		Size: 23.8 MB (23784573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb183d0010e4c134b94cbd70e63a2a8ec66d3c15e7101509e6f7f056182ff53`  
		Last Modified: Thu, 11 Jan 2024 04:47:56 GMT  
		Size: 68.8 MB (68774698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:eda7ad1c9adf08141546487b4ca131c7c951de47acff64152d95db04680b52af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135854704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd629151c9a68becd2cd8cecc176f909736db356d0d4889c5700cbd713dcf67d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:00 GMT
ADD file:cd6b2b4b3b0e27503b12f67c0901ed5145dc3891d490c198b6ea77c5429c7ad7 in / 
# Tue, 19 Dec 2023 01:56:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:26:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:26:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5110329ab47599ddb3bc004401c37c9cde68589c2b2734abaaef4fd51bb0f3c`  
		Last Modified: Tue, 19 Dec 2023 02:00:24 GMT  
		Size: 47.3 MB (47266091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4217a8fea4bbcabeb43f96e627c8788aed8b7f524c41838c7b4e9aeb229a6572`  
		Last Modified: Tue, 19 Dec 2023 05:33:42 GMT  
		Size: 24.9 MB (24911605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42019878fcdad4a69934727cbee368f7e012c1b035b52d0baa848cfaf64c288e`  
		Last Modified: Tue, 19 Dec 2023 05:34:01 GMT  
		Size: 63.7 MB (63677008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d56752c809164331b8edfcd3bf4cc490ba34c97361dd9078eefa0de8b2c60e16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132491403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf813306a55f53cb383196d4190f1ebeae347d6fec9220fe99123568328e5bc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:44:19 GMT
ADD file:8fdf812544a777aefa5a72371aaae01c05618dad10c40d3f4c4535ab61effa5e in / 
# Thu, 11 Jan 2024 02:44:20 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:21:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:22:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:738b42c6f08e0cf326b2758999daf25b796a2257c832077146951a1871b3fa48`  
		Last Modified: Thu, 11 Jan 2024 02:51:44 GMT  
		Size: 46.9 MB (46880379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e28248858523a50531a4a4ba3120a7a3bed7f5d8f5e1532dbf70fe0e4abdde7`  
		Last Modified: Thu, 11 Jan 2024 03:32:57 GMT  
		Size: 22.0 MB (22032903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262aeb61dcefe26c7a021c6cbff21437816af99da1c465425a42a57695535cb6`  
		Last Modified: Thu, 11 Jan 2024 03:33:23 GMT  
		Size: 63.6 MB (63578121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5a72b0d80e775202e4637daa12333eb46351c5a626aaa055df78bc26bec51c1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141823279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57b09fc98a3aa247da6b784c2e7d996c51a0bf6f7436d60367b9c2533fd1b1b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:13 GMT
ADD file:b95bf5556d43a8a1d79a2dbf26ab8a4a912869d65cc1b76a372ca80259a65b7b in / 
# Tue, 19 Dec 2023 01:42:14 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:38:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:38:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2f38ee39d2143cc6781c8d40b267519e59c558f7902df442f2e5ecfcefb01689`  
		Last Modified: Tue, 19 Dec 2023 01:47:24 GMT  
		Size: 49.7 MB (49689786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec939d1d3b6574ac3482db9be62850fd83b1612f01d44fb296af8ed464c33f1f`  
		Last Modified: Tue, 19 Dec 2023 11:44:56 GMT  
		Size: 26.0 MB (25983709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591136ec6e5960d51ec4ac04b638e9bb1afe645fd53be0f002e76e7d236d522b`  
		Last Modified: Tue, 19 Dec 2023 11:45:12 GMT  
		Size: 66.1 MB (66149784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:00f7b74544830d9d612b9e0b77992ddc94cab7f7339b9c237d08d35678fb65dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148666760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7f2525814d83a3d8d28dcfc3d1a917670cf907163da99a15fd60f7eee475c5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:20 GMT
ADD file:62936974dfc268ed9921277921d72e2fe4b8e316d02774bc95127ec6d56693e3 in / 
# Thu, 11 Jan 2024 02:40:21 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:36:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ed5772f4773b25b36078212363dc2fec6143ee364938f8da48464f4eec8f182a`  
		Last Modified: Thu, 11 Jan 2024 02:46:50 GMT  
		Size: 53.1 MB (53117689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2db4548d8325ba0eeaa2762072b818997f0ca88e46fd790e170e60a67b1eae`  
		Last Modified: Thu, 11 Jan 2024 04:45:49 GMT  
		Size: 24.9 MB (24852383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029a70e763831146af2e2372d63eaf8bea93c65c5584418f84d97b2c06bec0a7`  
		Last Modified: Thu, 11 Jan 2024 04:46:13 GMT  
		Size: 70.7 MB (70696688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:82307421f0a9d197a72659ef5362fdf66c1582b324176ee76abdaa253ef4c876
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143111557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835187fc40563e0dc55f9bd1c7a6d0323bdcb99771492296d72bcf1a47e94227`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:14:46 GMT
ADD file:5f44d39d860d41ee2d969347a8ee97117d8464c5ba5bb8a7f437e02e02bfcb33 in / 
# Thu, 11 Jan 2024 02:14:53 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:05:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:07:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:44d8b0d43d4e86510a6929ab344b91638efe7be700303879a57bc650fbd84861`  
		Last Modified: Thu, 11 Jan 2024 02:26:21 GMT  
		Size: 51.4 MB (51364371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc4cda8e31359619d6ac6175803cf81d221646100de8856ff3c129b6c42d76c`  
		Last Modified: Thu, 11 Jan 2024 03:30:44 GMT  
		Size: 24.2 MB (24168147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48efcd41b3712a829c2841895c2c38d12027581f76d5f0d986fd20cc2f608c3`  
		Last Modified: Thu, 11 Jan 2024 03:31:39 GMT  
		Size: 67.6 MB (67579039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4df51f25e0e066e317211b0c8f337d1595123b1695efa23d860d40760ad29520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154000490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9524f0ad342c674364fbd23da2814fe7a9512b65c6534904c954bb9a5b09dd3f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:00 GMT
ADD file:ebe2bb6638a51888bf27d1bb5ca609a91df94474b4abf70f874e60b653885a2e in / 
# Tue, 19 Dec 2023 01:23:03 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 12:01:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 12:02:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:97954753acf4d5cb589b2a49219ffbc5c86834cb864ed80f516370017ea3c569`  
		Last Modified: Tue, 19 Dec 2023 01:28:17 GMT  
		Size: 53.5 MB (53455717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf9bc2559c9bc0dde88b00d18449e9a40dea5919313c9dba6b3a432f24542e4`  
		Last Modified: Tue, 19 Dec 2023 12:25:16 GMT  
		Size: 29.0 MB (28960588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bcb9d372effc2b9eed2bc00b534deeaf705ecf5a3705a53bce008b65768d0a`  
		Last Modified: Tue, 19 Dec 2023 12:25:37 GMT  
		Size: 71.6 MB (71584185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:68532cbe11fcd817884f92d2414029986683278cefee0fc5db0aa359cf8155ec
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141939135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bb7c290da7a50388e4e3c310c7c99ccf13c36ff756a9ba1b5e392f65c3e31b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:08:57 GMT
ADD file:2425f95373d17e6fdcc9fa7f49bb6c7911f6b90dc27b013c125e09c38c1691de in / 
# Thu, 11 Jan 2024 02:08:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:31:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 02:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c4051c39033b0cb21a5a8e11e0cc7f40eaa9806ddc6699457c2f509128c3a492`  
		Last Modified: Thu, 11 Jan 2024 02:11:46 GMT  
		Size: 50.5 MB (50487871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680ecbf0470fdf287fdea90380971756e9423f13d45445f3c9b23000a0ace9db`  
		Last Modified: Thu, 11 Jan 2024 02:41:54 GMT  
		Size: 23.5 MB (23463389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be477d1b1316100dce4471ec2cd1633d4849b301db02472aa0f0b6afad63081d`  
		Last Modified: Thu, 11 Jan 2024 02:43:13 GMT  
		Size: 68.0 MB (67987875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ea27c289fb7caaada04fd9f044f49c4bf897322ac7a54c392945d108cbd29056
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.6 MB (146559528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17277d58179c3ddf94a071bb95809f56ab29c2426db21a0f2920964023436c6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:46:39 GMT
ADD file:8031754126dba92ceeddd0be53523bca85fa55f5859c83eaa57be2b0ba8f8046 in / 
# Thu, 11 Jan 2024 01:46:44 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:13:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 02:13:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ce6f2c0c05e382af54def5b355ea9bda0f36bd689f9f43fdcd74463778010bc5`  
		Last Modified: Thu, 11 Jan 2024 01:51:57 GMT  
		Size: 51.7 MB (51672176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccdf962076103e72329069bf48fa3112a100d8a6deee506176beb22e27789a0`  
		Last Modified: Thu, 11 Jan 2024 02:22:51 GMT  
		Size: 24.9 MB (24850534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b64ba60f98b957715429fcc464c59051f469caba372893e922d41e0cf32bad4`  
		Last Modified: Thu, 11 Jan 2024 02:23:07 GMT  
		Size: 70.0 MB (70036818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

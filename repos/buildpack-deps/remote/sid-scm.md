## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:204011ff07c91735d9fb8fef9ec2fa049ec6599f0c1223d62500bc2b163a6623
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
$ docker pull buildpack-deps@sha256:784bfb1c50638c37745084e218863fdf8d4823db8348b49d2e5a43164d9c39ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138487465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563f838340ede731235bd8b2fcf447ebdd93c299987b835930224303bbddf7a7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:50:13 GMT
ADD file:9151e08b2e412287dad7d69ba24534b298db5f003230d2502a6ba98cec1ebd47 in / 
# Thu, 11 Jan 2024 01:50:13 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:58:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:59:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b1b81c0298ff01b74292896351d56a8bab04cfea53060a06c7a5a819fcaccaed`  
		Last Modified: Thu, 11 Jan 2024 01:55:53 GMT  
		Size: 49.4 MB (49383131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d3596882ba4d789b2748d175d36c81d47be0b31bcd840be1acdcd1f4f8e0dd`  
		Last Modified: Thu, 11 Jan 2024 07:08:29 GMT  
		Size: 22.7 MB (22727696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9c40a74a9cdc4bcbf9e60c299bf24612ef99ae8a4e0ff4c0774d9fdae77a82`  
		Last Modified: Thu, 11 Jan 2024 07:08:52 GMT  
		Size: 66.4 MB (66376638 bytes)  
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
$ docker pull buildpack-deps@sha256:399e6cb30e7cc5e4f9532cbb4372c64218a951c53c13c6a8a403c08516a79804
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144519111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf46ff41e63c03c450672f6e0cf4d7983da4bfb702a0ef8af0b7a16c8beab4f6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:49 GMT
ADD file:41d0336f9211d4665c98a2ae6d92a97885617a6f3ef646ad5e96e1c505887f36 in / 
# Thu, 11 Jan 2024 02:41:50 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:29:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 09:30:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2a6d440355d1d93856497f93e287cec8381a68287949dd140442830cc02425a8`  
		Last Modified: Thu, 11 Jan 2024 02:47:08 GMT  
		Size: 52.1 MB (52148723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2daf712adc807f54f8b2b64a1df5a3955a5a93666ac193bb4074a1d18ee8d3`  
		Last Modified: Thu, 11 Jan 2024 09:36:43 GMT  
		Size: 23.5 MB (23530411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3fd6ed3f8d38e910bb159ceb062013c7c1ddba4294b092d803454c6df4d781`  
		Last Modified: Thu, 11 Jan 2024 09:36:59 GMT  
		Size: 68.8 MB (68839977 bytes)  
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
$ docker pull buildpack-deps@sha256:364aa26906ce0ca0dca15a60bd9d8b7b17d7f94bdfb587148cc66cd645005871
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156799453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ad282d024978e28923a9585d44fb0a5c5f68392459167812599f5c8c82482f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:35:47 GMT
ADD file:c2cc792d0e48795239ba8948f28a31a458128e8d2dade2ed88a7cc1830609097 in / 
# Thu, 11 Jan 2024 02:35:50 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:12:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 07:13:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a12077db2f3238d1c66f5358bd931ff537264797def7be2c14c9e9cd0ac05402`  
		Last Modified: Thu, 11 Jan 2024 02:41:17 GMT  
		Size: 56.2 MB (56185653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25800b978411714d00508bd5510f9f780d186fe5a4b83794204a9ad4f6eb6bbb`  
		Last Modified: Thu, 11 Jan 2024 07:25:41 GMT  
		Size: 26.2 MB (26179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5849bf0a86283edbb330815a50679f0e541585b82098279c61a8bedd8a86f8a`  
		Last Modified: Thu, 11 Jan 2024 07:26:04 GMT  
		Size: 74.4 MB (74434454 bytes)  
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

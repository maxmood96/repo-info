## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:5390a3f65952a8c25c5b8da9cd4c3e193e11fe221b22fa9710d107373d83c3e6
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
$ docker pull buildpack-deps@sha256:5a985f22812a6acd34f3a3d02f0a73e0a13a0efb88fcee7551f93beda69e901e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129372016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ae2daeef7f4b6500a4334a37ac3fccb9fbdb1a9e0aab726b7c5da605e11938`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:05:54 GMT
ADD file:20b1068c276c223839818edd0aca3981a1b8139130064d19f9ec38e26a94ff27 in / 
# Thu, 17 Mar 2022 04:05:54 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:33:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:33:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:34:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab40a96ab944197ee11d696f776db9c1130db9825e9996a5e8939611fcf5e470`  
		Last Modified: Thu, 17 Mar 2022 04:12:27 GMT  
		Size: 56.0 MB (55984715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214f624759443498bdf804a19e1294b81976d28ed00d521e85a6ef33658ab378`  
		Last Modified: Fri, 18 Mar 2022 07:05:57 GMT  
		Size: 5.3 MB (5269458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59203613ecfdfcaa48f715e4d48dfb31fde19bed9d8d6dd6886973ca3d859f7`  
		Last Modified: Fri, 18 Mar 2022 07:05:57 GMT  
		Size: 10.9 MB (10924378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a88b822c644e86ce744ca1d166b2e420d9afa87c5a9d8f72b763751621710e`  
		Last Modified: Fri, 18 Mar 2022 07:06:21 GMT  
		Size: 57.2 MB (57193465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c3a960565ecb75e2eb3393f24358b82acfaeee5a2447d2388d8eb9b13ecec210
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123961325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357d23666f500939df5aa5b58357dfce58f2867bfb2e4cac454d3bfb34d5f74a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:23:03 GMT
ADD file:a9d4a5aa739c9c980a2e0b3342f616a0ef24327457038a7d2d1f054b47bb869d in / 
# Thu, 17 Mar 2022 05:23:04 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:24:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 19:26:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1b1560f4e7f4d5dc335516eb5f16007a5ba8efcbedcc5584f361684738e508d`  
		Last Modified: Thu, 17 Mar 2022 05:39:40 GMT  
		Size: 53.4 MB (53393523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3688991f52d334055cd012a6287b39073e9b4ac6c7cd7012b2c8be6c4cf410`  
		Last Modified: Thu, 17 Mar 2022 19:44:30 GMT  
		Size: 5.2 MB (5164495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247526418f56b9d635ff39e99bd9d2058cdf75fa52ee8a6fb0e2a007868a5e12`  
		Last Modified: Thu, 17 Mar 2022 19:44:32 GMT  
		Size: 10.6 MB (10597460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b46eb17078ce0bb185a36f41062c74581f4ba10f530a5751c9f5b4a0565ef41`  
		Last Modified: Thu, 17 Mar 2022 19:45:08 GMT  
		Size: 54.8 MB (54805847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a25d04d841aedf31e05e016cd54bd4977b4a7ac91d3f6edb54b468f2e93ea694
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119111079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cf65ca29c3361e710e61f7d7e63c24f072f95b32c0e5182603ae9b1e76115e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:34:34 GMT
ADD file:9aa47fa903f49c3cddd2c04ea6dfc8adc7cb3e1b8f49392eb4ef30199e306b55 in / 
# Thu, 17 Mar 2022 09:34:36 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 02:59:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 02:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 03:00:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5abaa3393d9da88a4f8667cc7ed186e0fcf756926f31ba33f3b531a2db42031`  
		Last Modified: Thu, 17 Mar 2022 09:51:00 GMT  
		Size: 51.0 MB (51008095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a92e937e95ec8c4708c51bf5b42788af6dc7933017024adfe3755af9a222a4`  
		Last Modified: Sat, 19 Mar 2022 03:34:48 GMT  
		Size: 5.0 MB (5023856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f9c704ba15933d332549e911b8ecf5197b7956ef44f600fb06943964d50581`  
		Last Modified: Sat, 19 Mar 2022 03:34:50 GMT  
		Size: 10.2 MB (10244633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b84168887f66171a81e384a0ec065ccce1eed8938b60a25c845862b96da581`  
		Last Modified: Sat, 19 Mar 2022 03:35:37 GMT  
		Size: 52.8 MB (52834495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5104350a4b9e8c36160e7a8dff8213b970db7110daf0c7963d9258441c8e206d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128093327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab27685e35837628412ad93522e47a3c2156485e169faa12ac634349ecd5081`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:23:19 GMT
ADD file:1d38d88879da25d9a1bc7a4c5e36bc54d45209f4c931e6da3f7a5121498cecf5 in / 
# Thu, 17 Mar 2022 03:23:20 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:13:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:13:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 22:14:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1bb23fb7eb3b065e76a0f28cfe8d85ecc762b7cff467fdbcda2f70363c88087`  
		Last Modified: Thu, 17 Mar 2022 03:31:11 GMT  
		Size: 54.9 MB (54916866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c42e541f9a190ed5b1572f38d77d9a07c7899f7b9640e25460c12e849991f1`  
		Last Modified: Thu, 17 Mar 2022 22:23:20 GMT  
		Size: 5.3 MB (5255457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556c64db2922b5a87b5591ed9b67221014a21677b094903b77fc24099a5a1f3c`  
		Last Modified: Thu, 17 Mar 2022 22:23:21 GMT  
		Size: 10.7 MB (10693240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a84215e2a63ae365e4e0fa67da1b0c8f3b996b8f6f063442e4530fbcc3411e5`  
		Last Modified: Thu, 17 Mar 2022 22:23:40 GMT  
		Size: 57.2 MB (57227764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7af7f530a07b9fc3e069d8c2d7315b3911b7722c36d7220bd4159676ee93e6e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132364971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0326bb0bf6befcd22829ae1e530771cae65c8712aa7376965ec9d42e367cf03d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:17:34 GMT
ADD file:2cb9c8978846d8941a8213d064afc34b86f2f04e601b9ab365a29fff596c2aa5 in / 
# Thu, 17 Mar 2022 08:17:35 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 14:30:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 14:30:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 14:31:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23f252c494b0d56260da77f35c850c42d26d01946241721f649418fdd13ddb96`  
		Last Modified: Thu, 17 Mar 2022 08:26:58 GMT  
		Size: 57.0 MB (57031438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713c087b701c0e96ba52a634dca0b79b7bfc26336946b8ef9b7bb6deda31d1c1`  
		Last Modified: Fri, 18 Mar 2022 14:46:45 GMT  
		Size: 5.4 MB (5401519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c902ee6ab20573e3958bbd0b3e2ec3a189d08dc0fdac8987424bf548e32cde9`  
		Last Modified: Fri, 18 Mar 2022 14:46:45 GMT  
		Size: 11.3 MB (11322536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722bbd8ae920e50c9410f926a8e92f3781c08987e33e82b3fd5d3530ae5456bb`  
		Last Modified: Fri, 18 Mar 2022 14:47:11 GMT  
		Size: 58.6 MB (58609478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:bb31e32161757d98ea65cc9af7eb8b8267c83657d505ea76ba1e2e3007730128
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126483646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e44dbc7edfc589fb09f1d22b5fa64c59c00c91fafd1fbde16a1152b6b5b3d1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:55:47 GMT
ADD file:2015a98f802a1e28eca2c4eba0b574f58c2cd7844c0d94dbf0e29e8180aea210 in / 
# Thu, 17 Mar 2022 08:55:51 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:39:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 19:41:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d194d6caec7e92bc6e1448edd24c61790b7372a62bd6808d5cd0c5a6eda1736`  
		Last Modified: Thu, 17 Mar 2022 10:46:33 GMT  
		Size: 54.6 MB (54636832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6d8d6c495a88dc95c7cdb4d3ae2e01617fbe355ec506b682a16ac6bd71546a`  
		Last Modified: Thu, 17 Mar 2022 19:57:08 GMT  
		Size: 5.2 MB (5222583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91053236c731557db21c8cae8dadcde7f25967ff5d460c9f67f4789ecb8b3be7`  
		Last Modified: Thu, 17 Mar 2022 19:57:10 GMT  
		Size: 10.7 MB (10673017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c156ba31cbc1cdf259de80c19d95c4eaf735a0d8b5715a38c58be0755d068c4d`  
		Last Modified: Thu, 17 Mar 2022 19:57:58 GMT  
		Size: 56.0 MB (55951214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:613cad87dfea2deca46963e2d16f0c5b2f1111aa14332655709194c8585cfd92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139574782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec092c1bb5f999d55538748894dc28728d251e1cb39afcd931eb5e3704d27126`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 11:20:22 GMT
ADD file:52ac257bb3e9b43a436c32541c15e9c3a00323e3e1d0b20273b81a572fb8d66f in / 
# Thu, 17 Mar 2022 11:20:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 05:59:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 05:59:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 06:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d022277e505c1e9a57478a80b1b82e11b58551ebc0afcb5e723535b6ee105cc8`  
		Last Modified: Thu, 17 Mar 2022 11:30:38 GMT  
		Size: 60.4 MB (60406211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5191baf63a49f74aafee330281325a08a8d65451cc0ac632e8aa56129d9dca63`  
		Last Modified: Sat, 19 Mar 2022 06:45:43 GMT  
		Size: 5.5 MB (5543862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471dd71263fc10a8a1efc9a8fc7652bc8d0e227dafa1f6f9493a5a9779600d7a`  
		Last Modified: Sat, 19 Mar 2022 06:45:43 GMT  
		Size: 11.7 MB (11702261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b11bc794149909ceb1decbb8091901df40d21ad217894f0b435df98f07d5ec`  
		Last Modified: Sat, 19 Mar 2022 06:46:35 GMT  
		Size: 61.9 MB (61922448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:6b91da13d7013eab079224fbd7fa095000006ed0df6803da49afa74fde9ce696
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119768333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea75dc836ca3dcd73c98a3517af8d39cdd357c584e767e7f30a3882d930c52a1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:14:08 GMT
ADD file:1dc8a81ea9c954e594eb32623a82cdfb528586b569a915ba8f70a49f68a6f7fd in / 
# Tue, 21 Dec 2021 02:14:10 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:56:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:57:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 03:02:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6b741955e06623f1924320507da1630323c4cf1d6489febc99917464e765860`  
		Last Modified: Tue, 21 Dec 2021 02:30:31 GMT  
		Size: 51.5 MB (51541457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91689f9aadadd96fe4e4ad4ed92ff1cb6a48034aedc9f41e14d54cf85bcdd039`  
		Last Modified: Tue, 21 Dec 2021 03:34:04 GMT  
		Size: 5.1 MB (5089016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a290be0dbc2a1d1f5f12db96d9dc0949f33b55d33712a23f37c71cb89606a3`  
		Last Modified: Tue, 21 Dec 2021 03:34:07 GMT  
		Size: 10.3 MB (10320854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44222df82131b4d925c2f594e50c018b1fb6d67154b22de79d99eb4cd4a356c9`  
		Last Modified: Tue, 21 Dec 2021 03:36:17 GMT  
		Size: 52.8 MB (52817006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d9ef1f8c3ecc289a408855d3f676432b979c8f109765f74b00761e0f711426d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126874104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f9b612bce1263367229e755458dc743dc79412ebe6e29a4237e27be1757e43`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:08:11 GMT
ADD file:4a7b0c9e8bc60d35d06240af5417427853918fe6624688050d4aca10a22b433f in / 
# Thu, 17 Mar 2022 03:08:14 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 18:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:23:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 18:24:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e1d6cb1e553f745f248c4d7a409401acdb697f1bd597e8c1c08d6fcd5db0f2d`  
		Last Modified: Thu, 17 Mar 2022 03:13:59 GMT  
		Size: 54.2 MB (54246705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99267e3e8ccd599670f5059d59cf2f80cafc0773fc8b74ba953d5d5cb2189fed`  
		Last Modified: Thu, 17 Mar 2022 18:30:46 GMT  
		Size: 5.2 MB (5245707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3282440b854d7908290c041b1619604c86d6fb3ec5e2ed67356bbd4ef1847863`  
		Last Modified: Thu, 17 Mar 2022 18:30:47 GMT  
		Size: 10.8 MB (10819596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d19b2ec710aa05189651236530efc7d84062cf9d7d6fd4a3d22965342a45839`  
		Last Modified: Thu, 17 Mar 2022 18:31:01 GMT  
		Size: 56.6 MB (56562096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

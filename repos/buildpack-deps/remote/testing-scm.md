## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:8fd293790116fcf9fc8cd3f75adf8bc49e71b6e591e190fed8c67450ac490c66
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

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:22fee860c920c085bdf1c017d08341223e0de3ddb7a01f28506b74dce3ca992d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142439712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ce1fa3097146fbcda3525a43acf799c7de22027b13e1dac605ee96c438d19f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:37:59 GMT
ADD file:8ad3e26aeda90bbd087b64f3a0110c8f2e520a774d62a26d5aeb7c5006e472ca in / 
# Wed, 31 Jan 2024 22:38:00 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:29:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:29:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a946c083680d9a81b8eb8383bbc21cd34444b1c5f3212c5d3fc463e0220d7b73`  
		Last Modified: Wed, 31 Jan 2024 22:44:39 GMT  
		Size: 52.3 MB (52283197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aaa07716edd95aa6e78fbf886a2b62004144888c2eb3728580637af2de7642`  
		Last Modified: Wed, 31 Jan 2024 23:36:36 GMT  
		Size: 23.8 MB (23791920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a35bdadb6720cffb93809e51a48b4b14d7070d9f64b3ef4392e405586235968`  
		Last Modified: Wed, 31 Jan 2024 23:36:54 GMT  
		Size: 66.4 MB (66364595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:710883c1e02d1e75576cb77278f23db6bb3b44efde3a434e14a81402843e8973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136154643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf5d83ce7acff178d4680946367be523f6b57bc7421f58a7fb75633199996b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:08 GMT
ADD file:7144257253ce293f694d917fb06ea4d03cb3cffd94c432e47fa5a77e03a5a2f7 in / 
# Wed, 31 Jan 2024 22:46:09 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:20:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:20:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9be7d01dbe3e5ca74f21aad18f318e9da338902efa0bdf09221df8cf061d6b3a`  
		Last Modified: Wed, 31 Jan 2024 22:51:27 GMT  
		Size: 49.4 MB (49400791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a34997ca134aedbce87b0387fb6c33340c58bb878c2ee87be402220de4c0f68`  
		Last Modified: Wed, 31 Jan 2024 23:26:16 GMT  
		Size: 22.7 MB (22732709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c148329f0e03f45075be8f176dd6c41faba92fe9cbfd963747f61bf750551ca`  
		Last Modified: Wed, 31 Jan 2024 23:26:36 GMT  
		Size: 64.0 MB (64021143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5335ba0c761132f4afe2bbbf621f34de17de568535fb2f9944daf638f9f626a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130326549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6f5ac10ea7ef01945592c04df825275d96f7cf1b70058a1570285f8134b5cc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:47:01 GMT
ADD file:313528f956e019639cb41933c0f6d14e7dca01353fe4ca789d7ac69e4c131ccd in / 
# Wed, 31 Jan 2024 22:47:01 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:56:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:30dca4c17f72b09129956e26ae0841f8c684bf0810e63983ab453762044c668b`  
		Last Modified: Wed, 31 Jan 2024 22:53:21 GMT  
		Size: 46.9 MB (46892605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43baa7a4e2b9b0f5f9670286f20f999f396d37b58f26795cb62ee2e3cb4647d6`  
		Last Modified: Thu, 01 Feb 2024 03:02:59 GMT  
		Size: 22.1 MB (22050829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21488e6932eccaa048a628e2634682475e7967d8fbaf4684c255dbf1ad737c40`  
		Last Modified: Thu, 01 Feb 2024 03:03:18 GMT  
		Size: 61.4 MB (61383115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c9d77820522bcfff39018a04c31567e9de272deb8fb098e2e326eb11ba30b903
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142177552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8696f657ade23ff1fa207028cdf965cd35747c7ca5ea3b75cff23782d71fd549`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:18 GMT
ADD file:22615a550fb316cdf09ee3c185139fbdb9bf6b776c7f96bba26ba5cc5b14fbb4 in / 
# Wed, 31 Jan 2024 22:46:19 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:49:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:50:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b24f8e2b921fe314282df3bbfa20988c1046ee499441de80fd5229551987d1eb`  
		Last Modified: Wed, 31 Jan 2024 22:52:31 GMT  
		Size: 52.2 MB (52161387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3734a145b10aaff86d0b31ab8c862448f17bd19fd0bf41ea74f065b5217e8d0`  
		Last Modified: Wed, 31 Jan 2024 23:55:53 GMT  
		Size: 23.5 MB (23537259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7290694492bdb4e5b5951a97dc859b4a2a25c8bb16c78b5baf9a376c306ed4c`  
		Last Modified: Wed, 31 Jan 2024 23:56:09 GMT  
		Size: 66.5 MB (66478906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2fcc797d9ea21e3403b47876586a1cb5cb610345786fc405ca9e58042fc21b25
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146174826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559aad563eab98f8e4977932469307f3a47e5247f40b19e6475fcef35c7fa6aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:41:43 GMT
ADD file:443c10cf2bd14299f3b496a80df4429c5642d898fb2f3e8c184e8c4d58fb8cd2 in / 
# Wed, 31 Jan 2024 22:41:44 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:42:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c71e0026d29ede0429851d35323a9a769fb82ad7760740b559b172f3789ae3b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:09 GMT  
		Size: 53.1 MB (53140039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e20811788aefb929a0e339e49aea232089bba4dfdd96c9f7d13061e0608071c`  
		Last Modified: Wed, 31 Jan 2024 23:50:35 GMT  
		Size: 24.9 MB (24871659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad80f048e3484dcd9590861b0d67f2e85be42b1cde352abb5d6525a0c98e59dc`  
		Last Modified: Wed, 31 Jan 2024 23:51:00 GMT  
		Size: 68.2 MB (68163128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:289b64d2a4ecbe54944a5f8cdc6ad935d266fcdc62919a17bf67f15b0cffa705
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140788640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6dbedcc9010863b2dfe11ab088276267187e74392704d51f5d51565c11e6cb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:34:03 GMT
ADD file:534203d126346e48b8c0d0430dcecaa093294a7a3c98d571701aab3e6c36d391 in / 
# Wed, 31 Jan 2024 22:34:09 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:36:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:38:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b3d1be35073c977f0bb775d26df73db32aabd06a76b52f045f43c249f737a518`  
		Last Modified: Wed, 31 Jan 2024 22:45:28 GMT  
		Size: 51.4 MB (51373756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29775ff2e6dca77fd66e0ebc9778fa50a528946fea171a8991f404341704a4e`  
		Last Modified: Thu, 01 Feb 2024 07:55:48 GMT  
		Size: 24.2 MB (24179287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50d72572bd478bcb67e887b6c4a3b2bcaf9424f2e33029ebd8304a6acaa88ea`  
		Last Modified: Thu, 01 Feb 2024 07:56:41 GMT  
		Size: 65.2 MB (65235597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0008664126fc1a3ae57c7a7a80c719660f1bd9fb387124be4655690f1a859c3d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154267052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6de867ad361fa678d633a951a377a16516aed84d207f9c973497a5622536c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:32:14 GMT
ADD file:9862d7fda5f3fc5c48229d44a182f0619051f084c461b10ae5cd841f609dd876 in / 
# Wed, 31 Jan 2024 22:32:17 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:43:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fbf7f53bb9540a00260474ff7da2e470dc3eecfdc9849d2cfb73bb9e5f549622`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 56.2 MB (56198785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ba056f52a3a3f9fb8ddeab8c15f4923d3aee8ca28982082fee3b8e7078539e`  
		Last Modified: Wed, 31 Jan 2024 23:51:34 GMT  
		Size: 26.2 MB (26193139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b07f587272b481fb6b3580d1d5cf385bee054bd693b6629fb78936797172435`  
		Last Modified: Wed, 31 Jan 2024 23:51:55 GMT  
		Size: 71.9 MB (71875128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:82138dc991c1ab32ceb5d9daf1814dee7b763bc6407c2d0a432c5145478877ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144035477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d23756876688a4b80e5b5ad210e0ac8e4f6f1f94c8cd6eab8223db291cf1fc0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:18:29 GMT
ADD file:3b31c2bd33a3d7e6352823413292afa26a09dbcdbc56396202701f16e609204c in / 
# Wed, 31 Jan 2024 23:18:33 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:46:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:48:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:651c4bce8b545a7028c9eea81f8b25dae93c9bf0073fff7020f5784448310184`  
		Last Modified: Wed, 31 Jan 2024 23:31:42 GMT  
		Size: 51.7 MB (51697772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8bef819e59def6e5aacc1cfae21f5a548b594589a04dd83f55049c50ac9a9a`  
		Last Modified: Thu, 01 Feb 2024 08:22:11 GMT  
		Size: 24.9 MB (24864246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d30757e69c8b337cc88adc01ab0f95452ace75b76d316525fb8181f709ed9b4`  
		Last Modified: Thu, 01 Feb 2024 08:22:26 GMT  
		Size: 67.5 MB (67473459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

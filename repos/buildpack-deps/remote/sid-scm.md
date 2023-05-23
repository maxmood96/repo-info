## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:a7d164922b72957b9ada54a23865ad9499188a0a5fc432840533191aa79fc4e9
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
$ docker pull buildpack-deps@sha256:7c5933eed2248b68c715c96b72c91e0ccaa181eb231423fd1b6240d9a73a511a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138082358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1e6a03fcd1de6f186a845d3f6e4e140f416cdb243d7020bed9b8b9f81a4981`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:21:12 GMT
ADD file:3b942ada2dbba1c073e568411a383d6ab987c117af5bbb011afd46549d64c4dc in / 
# Tue, 23 May 2023 01:21:12 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:52:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:53:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8285c3e1284db51d7096ff9c9434e138a00153495c655a040787b10e562b7515`  
		Last Modified: Tue, 23 May 2023 01:25:36 GMT  
		Size: 49.3 MB (49289184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c93962a936c4e623abcd5c132acd83a550b41b475220f5ba03708dd030b1c0`  
		Last Modified: Tue, 23 May 2023 01:58:03 GMT  
		Size: 24.3 MB (24276999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f584564987f0be0d812aecff1df91b59183f5667eadff38eabade6484098b`  
		Last Modified: Tue, 23 May 2023 01:58:20 GMT  
		Size: 64.5 MB (64516175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ca0129c31bd738d32d309e899c2fb3935540fafc790eefb0cdb5fd67e815f3fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132250396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d394e34a03499c0b680e262586555cfdb14ad7c7dc1d5a5bf546b6d9144363a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:48:49 GMT
ADD file:bbdd13db0e090d7d928a2beba57e3c1340342d05e5c15f7b7377c9791a5cb4ba in / 
# Tue, 23 May 2023 00:48:50 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:18:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:19:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d14a321d144fc48aa438b2364b0f1a5667979322ef9cada9309bca48584a11a1`  
		Last Modified: Tue, 23 May 2023 00:51:36 GMT  
		Size: 47.2 MB (47154613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af911895fe3f6120ef979a3b5dbd9bac4de6b4d900e6ad8ddd6b28ccb19a7746`  
		Last Modified: Tue, 23 May 2023 01:22:48 GMT  
		Size: 23.0 MB (22951581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc480ad84aad81f48b8427943b9e4cb119ca2f0562152d578d98f45ff47a69b`  
		Last Modified: Tue, 23 May 2023 01:23:06 GMT  
		Size: 62.1 MB (62144202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ab0243a521c1c7f1594786e9740b3ea4af0957543c76a2154250e16896e0138d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127981149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93cb3edb35101b92d8d4bb39ff8037c1209fcdfba20441be54d9a44ded27bb7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:48:42 GMT
ADD file:17739fc730ad8febc64f53eec61cbf10f8d2c5184cfda5466e89ab423a88f9d6 in / 
# Tue, 02 May 2023 23:48:42 GMT
CMD ["bash"]
# Wed, 17 May 2023 00:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:02:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b827c534260a55126ac3b18c14ea9160a3a3a03448b5c2b4462f9f3f4cf0ab`  
		Last Modified: Tue, 02 May 2023 23:53:05 GMT  
		Size: 45.0 MB (44988077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858686fb647755cfaf9d97846212a8b1056f291d77f962bb8bf7be5d16a5ff60`  
		Last Modified: Wed, 17 May 2023 00:24:35 GMT  
		Size: 23.2 MB (23219225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16fdb017446b11706119bca2906a6b8fa79ccf636d08457981e54be450413bf`  
		Last Modified: Wed, 17 May 2023 00:24:55 GMT  
		Size: 59.8 MB (59773847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ac2df2125e5d39cc0c994d4510d58d81efc343dee4488bb06977f7e284821911
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137648677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b4d4d006f96805b2634f6427f048978da0f88aec79d2e9217118eb49d9ff0c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:48 GMT
ADD file:4608b82b211b6814e5bf372be706a6c01bd7a2a4841b59ac5430ec3a3f94468d in / 
# Tue, 23 May 2023 00:43:49 GMT
CMD ["bash"]
# Tue, 23 May 2023 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 05:59:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5842d200e3f7df637a96b64f14e82ccb2c66e201137165f2d91447fbd3248a8c`  
		Last Modified: Tue, 23 May 2023 00:47:31 GMT  
		Size: 49.3 MB (49336298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8c760dbeccae06cc6b46a82bd8c7d79890fb31a8237d0ba2b23c16b2b47fba`  
		Last Modified: Tue, 23 May 2023 06:04:42 GMT  
		Size: 23.8 MB (23813069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6085f2f6a378ccf03bc2e19864b5cb626f6bb97c0548e81dfe6c75f730b24245`  
		Last Modified: Tue, 23 May 2023 06:04:58 GMT  
		Size: 64.5 MB (64499310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:422d0aa6fff6fcb37cd178f841f4443fbb8e965f81a82e967c9594cac948b3db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141766746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5385cadb1e1cdf30b092f4e8fe2ca0e40a08e8704a2869b66a4f8380fba3c9d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:40:47 GMT
ADD file:33dd3eb2725f92170606ce015e99cc9496d244630b3f4844cb8f3f61b16e2eb0 in / 
# Tue, 23 May 2023 00:40:48 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:01:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:02:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1034171b4bde64cf8e4ff854704a3bf68000eddcceb63b481197082dced785ba`  
		Last Modified: Tue, 23 May 2023 00:46:09 GMT  
		Size: 50.3 MB (50311497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0773461f28d3828f3df4474bf07fd4bc2d3cdec7f41c65f1253678f4a5f861b9`  
		Last Modified: Tue, 23 May 2023 02:07:38 GMT  
		Size: 25.1 MB (25112113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f3b130ddfdd33ce29355bf1322b63f47960cc73b9e64789abc64c7954273d2`  
		Last Modified: Tue, 23 May 2023 02:07:59 GMT  
		Size: 66.3 MB (66343136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1b1edb40ca42a51b07f5bb498c7439c17e692ba56b3fea9752a17ca5bb082f3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136588935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3f823aefc280a80ebb4d6ebd8df0141176ba201aea05a25f28922abd20d2f0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:11:03 GMT
ADD file:4747b72418fe8be7c83a33927d22b74c9169c9f02959e41f61d71d739fd30ff8 in / 
# Tue, 23 May 2023 01:11:08 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:58:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:00:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0f1da758a33cea391a9b76cbdcea2cd41c87b5a2c179c4c1f3d65a456c65d8e1`  
		Last Modified: Tue, 23 May 2023 01:20:05 GMT  
		Size: 49.3 MB (49293333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebbc59228088cdeea0edefdf4596c78cc8f25b00177cd12202cf4a879b33945`  
		Last Modified: Tue, 23 May 2023 02:13:15 GMT  
		Size: 23.9 MB (23868941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2051f379a7704fbd90dac1820d91a3165e19ecd15d8720c7e0af0762d9ecd78`  
		Last Modified: Tue, 23 May 2023 02:14:04 GMT  
		Size: 63.4 MB (63426661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4e4e157c685485b0720b1004928b51fcb8cf204acb6f9feb071186aca3e6b53a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149190846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e84aced56271ea273dff3a077a1d6b1b1de944803da6e41e84ae238253cdc46`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:17:52 GMT
ADD file:cffada1d28fb1dc246127e193bd218b3c76450667fe4cd380f04a5caf5571be9 in / 
# Tue, 23 May 2023 01:17:55 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:55:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:55:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d914d1b8acfde6dc74b2fb48f95f7aedafbe4e4ad3b6ea21aa9db007eee47739`  
		Last Modified: Tue, 23 May 2023 01:22:29 GMT  
		Size: 53.3 MB (53302061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfd02567bd019328b094640438b56aa8ec096d625eb4dd7646bad29dc33d703`  
		Last Modified: Tue, 23 May 2023 02:02:41 GMT  
		Size: 25.9 MB (25928691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37bffe3818ac84f2da95782d45c9d0ec1ac2686d474eef4dd224cd8a76dca7a`  
		Last Modified: Tue, 23 May 2023 02:03:23 GMT  
		Size: 70.0 MB (69960094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0f3f24588a6e3e641f6ceaf5cac395c4327dce2cd21464e8098d2f6590e17e99
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127953533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23ba7ed8591cde0e9e2378b515b76628f77b9612c90c738b497144207f3e2e7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:09:11 GMT
ADD file:20221b6f94aa48c9890226bf3be037d4b2c2cb20a076225236ca9d2c09efcbd4 in / 
# Tue, 23 May 2023 01:09:13 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:31:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:34:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:04b827a08c39becba5f6c479b23a265f1f501c5d3aef76e037fa30157864daaf`  
		Last Modified: Tue, 23 May 2023 01:12:26 GMT  
		Size: 45.5 MB (45503414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efef68c40b0d23d116a73ed6b2156ae42fb93e63547bebff3d6febc2bbbea30`  
		Last Modified: Tue, 23 May 2023 01:42:27 GMT  
		Size: 22.5 MB (22487151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b058e1f937b69e6050ad30d3ef4e1094300d70d5175e07c16d50c7efd62c36c8`  
		Last Modified: Tue, 23 May 2023 01:43:46 GMT  
		Size: 60.0 MB (59962968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:70977233de40bbe9066fed257f97a82a95d317fa3b3470d5bff952b459efb022
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135549386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101796ab7a05306e9c9033c56ec329c3edd0dbdb5d7507a277383ee43815170f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:02 GMT
ADD file:7a71212c59dd3640d3ec2c6d4fd4df4a864f77e634571c1e200a6f7877a02cb2 in / 
# Tue, 23 May 2023 00:43:06 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:34:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:35:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:021a3707435b37ce556f1886fb9417a47cbfa836555f680d70cffb85f96a6eec`  
		Last Modified: Tue, 23 May 2023 00:45:58 GMT  
		Size: 47.7 MB (47664615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6242508e16648c81ff21ed8251d1dfbddaed438084bbcd6c7baf639349cf592b`  
		Last Modified: Tue, 23 May 2023 02:39:32 GMT  
		Size: 24.3 MB (24275724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081327490bfb5677aff76324903d283fb120712a9f911ed52f6d4be91df47e0d`  
		Last Modified: Tue, 23 May 2023 02:39:46 GMT  
		Size: 63.6 MB (63609047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

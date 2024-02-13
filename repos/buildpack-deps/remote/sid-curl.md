## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:8c74f4bb17335392329320c3e636203e880e20ad49656d32bdac0933452198bd
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d1c743af9b2f43730e2f8d2a90966952e1c05d7eba867f064b254d425e63f787
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76507372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7e3baed9409d7c78f0e08ccd5994257277c2e71b13f26b332343359456f03a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:01 GMT
ADD file:d669b75a7533bca38f2c301c256ebdfa35812b13652db86b8742a30e6856fd74 in / 
# Tue, 13 Feb 2024 00:39:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b49777280093cb58e1e93044ad56b006d1fb67107f14896ae3fd237faac8d485`  
		Last Modified: Tue, 13 Feb 2024 00:44:56 GMT  
		Size: 52.3 MB (52336486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0416ce76c708a01d23d622188ae0a4c0552e5a29d07378826ce051a51a2fc61d`  
		Last Modified: Tue, 13 Feb 2024 01:33:47 GMT  
		Size: 24.2 MB (24170886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b839041109743d570e5b781207c8b6dd0d83f7a02c1312c39b3abb5859206ead
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72475557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0f7d477c9f33dfcd2679ea280f5c1a52efe266dd8936b0206e4796fc5b1727`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:36 GMT
ADD file:624f450cf1c3fdf8774bf8313557baecef902871c3ad8dff4410f14122f8c507 in / 
# Tue, 13 Feb 2024 01:09:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:24aea175239943bb2adfa7be646a8e0c040383dec937faf220aee85a3f296298`  
		Last Modified: Tue, 13 Feb 2024 01:15:26 GMT  
		Size: 49.4 MB (49423639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c530646f760ee121e031a3cfc99e5f7b580df8596f51a1f5e30e10af689119c`  
		Last Modified: Tue, 13 Feb 2024 01:56:34 GMT  
		Size: 23.1 MB (23051918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d6b8be762fd7b820a830a3321642176df58972875bda564d8ab9992399b21a19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69289468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847f66994b4f16318f221a7a1e0bfc18624e296073c3f43d158ff2b83d9c8b0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:22:33 GMT
ADD file:fd66e10084783208c7cc3adad23d5c975d8f5be56c462c5a37d7a50fffacb677 in / 
# Tue, 13 Feb 2024 01:22:34 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:20:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a9ce49138215d345df26ba8499250bd7c71ec90f1afb15a8ac29dcd7248b188d`  
		Last Modified: Tue, 13 Feb 2024 01:29:59 GMT  
		Size: 46.9 MB (46928854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bed3d75f3913415a967fa0e909adbaf536b4d7ca377cf97730e2135c92b5c0f`  
		Last Modified: Tue, 13 Feb 2024 04:30:48 GMT  
		Size: 22.4 MB (22360614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:471947f5197058ebfb95666bd4796655232ffb21a10bbe66bfbf513c998d6c5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76081475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ed0f568e4e46400479da1e5ad8a697b7df7d49591b78efc93ef2fd2b0e9091`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:42:26 GMT
ADD file:88085ab115a08b9d412def1f9fea5d59c60a8e26965f72639d8199179230cb86 in / 
# Tue, 13 Feb 2024 00:42:26 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:84e6541c14eb2246826ed0d079d915b03d190721bc05675c66f459f0cc97e40b`  
		Last Modified: Tue, 13 Feb 2024 00:47:37 GMT  
		Size: 52.2 MB (52195661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb51a1adc81a562b48092b8b5446a6aea6604838e971db7945e6af747f8414c`  
		Last Modified: Tue, 13 Feb 2024 01:49:18 GMT  
		Size: 23.9 MB (23885814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5a308728d3b203f524e96e1e51691b47168168b7318136b03ff137e66eb6ee7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78457588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345b0696be583a4588b82ce28f76fa3e2241256e439d3cf9a96e63c5314f54a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:38 GMT
ADD file:4189b090bbf8678fcabd8dabb56450346892e68ce7343823f5a1de966a7cfba7 in / 
# Tue, 13 Feb 2024 00:40:38 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:986c70cdc0585f2b2041c18972cf24b00e1384bf0ae25efa4ed418df60c27f39`  
		Last Modified: Tue, 13 Feb 2024 00:47:09 GMT  
		Size: 53.2 MB (53166067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5992ae92ecc708d9f7dbc50c93a7a44033fbb23286817ad552428376a53b6b21`  
		Last Modified: Tue, 13 Feb 2024 01:33:35 GMT  
		Size: 25.3 MB (25291521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a4a8db675393ee92fe409ef196cc95ae2101616b16dcd567cbee927d7adacb37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76038798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9eca413a639eeb7f89bb3aba1e73462639a1e199d4687fb37ade8e121335cb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:07:17 GMT
ADD file:46b0dcd0e81e4f61221659b1260cc43869ec44a23c045f293f694b50a4ce89a8 in / 
# Tue, 13 Feb 2024 02:07:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:01:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ba59fa1171a061c2b49e9de14015f71d0e00ec2a17b49ddcdd453a663a922bf7`  
		Last Modified: Tue, 13 Feb 2024 02:18:44 GMT  
		Size: 51.4 MB (51411523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11595e21bfcc750f6639cddb481d3bae82b987766fc917da9fdbb55241005776`  
		Last Modified: Tue, 13 Feb 2024 04:27:08 GMT  
		Size: 24.6 MB (24627275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8ca8a63e9f98ec918b00dbfa0cbfb9e821cec7c7b9a7262e2ebfb57dbf86c5bb
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82497179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add37801d447fd77e633588185ca27ec48e8f097c48c4bfc36b48bec7ba57b3e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:17 GMT
ADD file:d19bcd45d866b0d48dac33521c067bfbc08e3a101f90daebd092f75f282f6aff in / 
# Tue, 13 Feb 2024 00:40:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:947f8d1be7548afd5382ff5b1b5c220ae7893fa7f2c8f135cf8967ae1d5d8b04`  
		Last Modified: Tue, 13 Feb 2024 00:45:58 GMT  
		Size: 56.2 MB (56237347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81019b4261c2b7655008e5d128bbae18fd5c794c1676de082ef06c6e9d52b2f8`  
		Last Modified: Tue, 13 Feb 2024 07:38:36 GMT  
		Size: 26.3 MB (26259832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:05da3f23abd0d4fdbfd32e5862e58f132da411fbe7b4892ceb60ffcfc563174f
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74357809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb3bebb24086f8a3702016ae8531035dfdc9bbc785d2b5466db4bcd57ca1d2b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:16 GMT
ADD file:b421fdf9092f4ec73d99564dd5502ef1d3668a7a691ba3bf1dbac96a04dc4a5e in / 
# Tue, 13 Feb 2024 01:09:18 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:31:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dd7397a9685010df855591550ae6ac222e43aafe4aa8f629b13f53ec98a94bff`  
		Last Modified: Tue, 13 Feb 2024 01:12:06 GMT  
		Size: 50.5 MB (50535650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37f9252bfe79456c9018c3962c3bb12a6b36262f5780411de6623ccf1a0df7a`  
		Last Modified: Tue, 13 Feb 2024 01:41:30 GMT  
		Size: 23.8 MB (23822159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3d8adea1bb07411818beb7059fe1c1f46540e6069549a17757b87bacba9eb7c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77049806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f73e082015284c35b32815c0f3361322c3f497023955778b8843b6cde5ef827`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:12 GMT
ADD file:4bc7c850cbec49616034f8ea4f54dd700feae8731e30f527142a4ae20f2089d9 in / 
# Tue, 13 Feb 2024 01:11:15 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:463755eaddfb5b742f8a2a82a7c2ebcfcdcdbcfcad5bc7a79a96f0c7ea3c590a`  
		Last Modified: Tue, 13 Feb 2024 01:31:31 GMT  
		Size: 51.7 MB (51742366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cc53fd314acb7fb481a8eae3a329f16695193f59a9f56c9e4806de6b5cf329`  
		Last Modified: Tue, 13 Feb 2024 02:59:42 GMT  
		Size: 25.3 MB (25307440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

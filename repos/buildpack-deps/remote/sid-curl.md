## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:badfc9481b53b7cd0c0d2313c5bec5216d698d986ff52b2ab3991f70f3f04a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c6d2cd2830f042eea0a99c94a96616c026156a171e89c69408f76f0dd416f6c0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70212108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4f434eb0f12cf8db178e6147602761dcf57523f25a544a6927fd645e714e2a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:21:58 GMT
ADD file:5d2d72d29ae1c01dc7f5bf337c78d40925a9843052910f79f066f681a2ec43e6 in / 
# Thu, 23 Apr 2020 00:21:58 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:58:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:58:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2bbc6b8c460d7ed40af9e8f69693608780022541107dbb47c4a717e0a15e84f4`  
		Last Modified: Thu, 23 Apr 2020 00:26:48 GMT  
		Size: 52.0 MB (51979787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af86ee5a9d864ef79346df3bd57faa5631e1b16cc83353b543768d6d306d88f3`  
		Last Modified: Thu, 23 Apr 2020 01:04:33 GMT  
		Size: 7.9 MB (7934538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb4c0ecf8059fde4ddfb61bd7bca435c46f56832aba0b7726caffbe9f0eb90c`  
		Last Modified: Thu, 23 Apr 2020 01:04:33 GMT  
		Size: 10.3 MB (10297783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f4b8db1e927c5c8e8f512fa3a28c30e02c3a81a309d191ff8e8a1b749532b317
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67454192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9183ed1358994c1f33af47e1a36789a7410f70145385a0a0514036849730bfab`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:52:56 GMT
ADD file:bd1d9af70dc12dc4f17f2b7768c241504faf686b41fc7a690e618f93048fde8e in / 
# Thu, 16 Apr 2020 00:53:01 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 07:53:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 07:54:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c1a8f9f50766a877cfcad4d61e0db97b4f5cc37823b5af730a9b1e2a867d6410`  
		Last Modified: Thu, 16 Apr 2020 01:00:47 GMT  
		Size: 49.9 MB (49930750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0560a304aa773636ff4d2d0b589147c30f28a9f3a9eb74d4cec04316bcddef9e`  
		Last Modified: Thu, 16 Apr 2020 08:08:19 GMT  
		Size: 7.5 MB (7514769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d0b1b12f45fe7e95157fac9261c9861a14d708d1a418158b4cf1e4707779d9`  
		Last Modified: Thu, 16 Apr 2020 08:08:19 GMT  
		Size: 10.0 MB (10008673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fe2aa7c2d350c24b2810713189ecc2a7dc4cf1446e9b572db4eb158cccb9916b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64584291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e042551de993ce1fa6414237932d14d1e732a2498ac3725cce7a9634eda5cf3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:02:49 GMT
ADD file:5de6dfe62ae35545ab2dc195cdc7ed6211867d4583f721d08acfff371bc7cecd in / 
# Thu, 16 Apr 2020 01:02:51 GMT
CMD ["bash"]
# Fri, 17 Apr 2020 02:09:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 02:09:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:9d58ce8574bee4c2429ae80f47b2650443254f3f9a0dd9fc1c8d64277895520c`  
		Last Modified: Thu, 16 Apr 2020 01:11:11 GMT  
		Size: 47.7 MB (47655417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49d113a28808faa8fe3cf110ffbf1d3f61e1734b4bf5bc389129f31b164756c`  
		Last Modified: Fri, 17 Apr 2020 02:13:40 GMT  
		Size: 7.3 MB (7255893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cdd02f3a35cf68582a2a9020525ec2a2db6792c7abd94d1eed23a0c585b6be`  
		Last Modified: Fri, 17 Apr 2020 02:13:40 GMT  
		Size: 9.7 MB (9672981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5301a8049500a33f64b1af5f6f239f3b8417f18403393f52e8ff74511832fb0c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69012440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a14928fbadd7e3cf8282e45396d5d37b41810b98e0e54d2f66bfa0dc151ff25`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:43:10 GMT
ADD file:ff8b5c2517d26b49a4c8114e515f5413a0c64b28ff1e5d3fa1bd70603aaadff6 in / 
# Thu, 16 Apr 2020 02:43:13 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:17:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:18:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2f361d4eae096128866baf55f9d19448df20331f319ad8df0f05397bfd2fe7fc`  
		Last Modified: Thu, 16 Apr 2020 02:49:55 GMT  
		Size: 50.9 MB (50910038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c3a136011851aa29f08165cf962f4b5df6865a2236b90a5fc6d0f1c01ded33`  
		Last Modified: Thu, 16 Apr 2020 03:29:25 GMT  
		Size: 7.8 MB (7808061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0d0c43c17c0157ca9f4cd6b676d7a8e76ef248c724901495c897b950e8ff1b`  
		Last Modified: Thu, 16 Apr 2020 03:29:25 GMT  
		Size: 10.3 MB (10294341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f8110b83bdef41a192e6686e465966a0c21a1140c566bd9f883eee54c0e8293c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71897387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4413622ed30ea988b9e0d8dc3a22941e23a1c0d4dbf5b311e4d2d3c7eabfadb5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:41:56 GMT
ADD file:af11f81927371cc0ed957aa36f4036c71c73a0b79ab27523cf0d49d8e0260041 in / 
# Thu, 16 Apr 2020 01:41:57 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:31:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:31:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1cf4ce40baf558f42709af03658907805f477c72b1b1a39869aef429cd35cd3c`  
		Last Modified: Thu, 16 Apr 2020 01:48:16 GMT  
		Size: 53.1 MB (53130042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dcc2dce5f80bcf713e09688ddce4e707509747c60ac5dcb21b50ba63fa26bf6`  
		Last Modified: Thu, 16 Apr 2020 02:39:42 GMT  
		Size: 8.1 MB (8110058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b96fa002b78190463928c6db889856164ede953e0bbc48a860d1856d448dd69`  
		Last Modified: Thu, 16 Apr 2020 02:39:43 GMT  
		Size: 10.7 MB (10657287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e9fa88f5acc98e2d6c94cf216e5582d2c661e9f1c57c3e94852919db29ef8110
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68481963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fcfde8c0c85be33261564e43540bfc3f3667b763f2aeda69a91bba55661f6e3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:11:00 GMT
ADD file:66d4b8806942796ca49e31a046824a633333dba393126281f5c12e26efea8e7f in / 
# Thu, 23 Apr 2020 00:11:01 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:56:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:56:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e50f308fab9e31aebf27548f07771af5a99a609ac88a60bbf74cd4f85125c24f`  
		Last Modified: Thu, 23 Apr 2020 00:19:59 GMT  
		Size: 50.7 MB (50696153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81374d42ab3f43b1e9a01bc0af60264f1036fe997a6abb2a98e309bef8774229`  
		Last Modified: Thu, 23 Apr 2020 01:13:33 GMT  
		Size: 7.5 MB (7461350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f82f88069fa53135d2819a8aa2d5e279767bf7aaf186c38c0b84e09717b63d7`  
		Last Modified: Thu, 23 Apr 2020 01:13:34 GMT  
		Size: 10.3 MB (10324460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3569597c98319860fe0753a053761266862f39bb85ff61408925cf767a0bf83d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75192686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7451b1810fab0d7de265face4d9302862cf00cd37446ea046c4c1df1f5c0209`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:40:28 GMT
ADD file:68afd6d0e23ee44127b8e1f922e1a6977efc12c46c7aa7afff807e146187d870 in / 
# Thu, 16 Apr 2020 01:40:38 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 05:51:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 05:51:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2b17b1afa1bd62e539e75bfdf0ac70297d76a76fc7df9fcbbc67ef6c31717636`  
		Last Modified: Thu, 16 Apr 2020 01:58:42 GMT  
		Size: 55.9 MB (55860496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f930d34b8f1d3792eb6eb828ce6a77754290b38b418d7578625e5b4eb10f66`  
		Last Modified: Thu, 16 Apr 2020 06:23:28 GMT  
		Size: 8.4 MB (8356254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d760269fe892aae3c468a162893981cdd2303cdef6cd9b9f91904b4af14ac395`  
		Last Modified: Thu, 16 Apr 2020 06:23:28 GMT  
		Size: 11.0 MB (10975936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5e595f2eec40e7c5ab239a1188c5951444d8cb25d62c95e2dc07ccfb3b373133
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68360471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e89fd7676aa827148252d683c047d6eececf1772de005775229c79f2ec56f3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:42:56 GMT
ADD file:1d96a73c9c03d31b0a60aa6b4e0215085afcdee6dc39954655798110c12c223f in / 
# Thu, 16 Apr 2020 00:42:59 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:01:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:01:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3633d30b569d7f8e4addec62b3bb5c460572eb82d6568a9bc40a9f189dc4bdcb`  
		Last Modified: Thu, 16 Apr 2020 00:47:02 GMT  
		Size: 50.6 MB (50576543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275dfe1709bf7bfd1a7e225a7b974994148dca503ef21f837a74970529f9eb01`  
		Last Modified: Thu, 16 Apr 2020 02:07:15 GMT  
		Size: 7.6 MB (7600071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae5ff7d1251f85fd4f476599f4408381f4e029ec36f4f1b66a96e89b921e7a0`  
		Last Modified: Thu, 16 Apr 2020 02:07:16 GMT  
		Size: 10.2 MB (10183857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

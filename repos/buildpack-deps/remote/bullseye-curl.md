## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:69f219c2f86fde044434c40828e039b1be893d0df31e44590b426fa72480be4b
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

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c8ed5dcbb233402307ab7db410d7900c38c2e2ed81e20439a57f3da8c76ca047
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70822150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350aa09d727859be6d025bc275a4b498d51a2d154d7571bc39d5317a676c6ff4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:54:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577ff23cfe55ac8872bc433ce99971a34011e7a15f7c8afa3d6492c78d6d23e5`  
		Last Modified: Tue, 21 Nov 2023 10:02:30 GMT  
		Size: 15.8 MB (15764247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c23abea3a5efc4debae1f1bec6e3158668a82b6c8df371a6e258a248c29b4777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67937675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55717d14d3b04b67807a055241a5179bd8e274e358f0d53f6e9a50525d39ddf1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:01:00 GMT
ADD file:a5c8bd4b0873bd9ad0402143df41b5fd89c50bd24bb071b7d010919e189d88f9 in / 
# Tue, 21 Nov 2023 05:01:00 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:16:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7378d71ea16926a061a2edbf0eb3dd13563fcb3ba9cf139c25e8334b36db1adf`  
		Last Modified: Tue, 21 Nov 2023 05:04:15 GMT  
		Size: 52.6 MB (52562921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaa95caafdd4a91609c9997495068a1afc54f385cc3d198e197fac2e00499aa`  
		Last Modified: Tue, 21 Nov 2023 06:25:36 GMT  
		Size: 15.4 MB (15374754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ad86b6a5c10024d3a342add15039ffb3ec622b8489665819e6526d6c20888992
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65095308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d2362666a519f1f8c5b6aa3419b0fa2db7e0e46f3aacf502ae06a7488ca50a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:54 GMT
ADD file:ed8d88d0476fad37879d872d61d05a8cffff35609566f080f78bb882d1bae26b in / 
# Tue, 21 Nov 2023 03:57:54 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1dac19092a737e476f9b096fe28463512ae21c4f596dd2f8b84d62530416dffe`  
		Last Modified: Tue, 21 Nov 2023 04:02:11 GMT  
		Size: 50.2 MB (50215653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98461d76c0d7c5e4d320986d659d56aba23d807280d398632ef50acd8a6e028d`  
		Last Modified: Tue, 21 Nov 2023 14:15:07 GMT  
		Size: 14.9 MB (14879655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2a66d27332240bff4f704ed98e6b0f9c76bcdb3f404159083b2146dbf53f1102
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69457985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d5417794b6f151c095aabdcfd742fd5c0c9d5ac6ddac5d0f5904fe51f6f65b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e860a4a6ca9e583881322c2e78baef1911e4d61bc607563e8ad9891e2d91f9`  
		Last Modified: Tue, 21 Nov 2023 08:07:01 GMT  
		Size: 15.8 MB (15750113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3031323302eaff84a691d3ee86f673dcf58faec6ca26af36306a26264bf3fc4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72314415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e808a609f652bd8bfd97a50be155e7b8cd8f48d49c5dcca1574139b8b52ebc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:06 GMT
ADD file:4095d27bc1a281dda044919be3bb570d581df169c01f22b0963b38e0dd6d9eff in / 
# Wed, 01 Nov 2023 00:39:07 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 13:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:95d6aa56ba74b8ed0a732c4676a2c45c84a18076696d466cd9bf0b459c600e02`  
		Last Modified: Wed, 01 Nov 2023 00:43:49 GMT  
		Size: 56.0 MB (56046261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a221a3957c157fc6091d669757aa644810547d3e3fcf1e1af9da5c23408ccfd`  
		Last Modified: Wed, 01 Nov 2023 13:57:18 GMT  
		Size: 16.3 MB (16268154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ee90e25e1f717ac8bc868652fef2f392e59b5b1cbf0d73906144ecf450288947
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68818920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25455f146cbb8cace4b715ae289e3c86a6698ba2c6b4dd2adcd10afa9213ba7e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:10:25 GMT
ADD file:dbfc3d226166089c4db0c154fdcea8049b8758c6812f1c397dec1444985e8557 in / 
# Tue, 21 Nov 2023 04:10:31 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca31218601e95f4aafae0dcadda7600aeb04db374e1e829d5c123f8033ba3472`  
		Last Modified: Tue, 21 Nov 2023 04:21:21 GMT  
		Size: 53.3 MB (53289162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4053cd5a6af26fb90d7c0467241aaec093f035fa809a6ca17aa5e69d24eebd58`  
		Last Modified: Tue, 21 Nov 2023 13:01:44 GMT  
		Size: 15.5 MB (15529758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:96b66b231fd64c79e68c691f1433a4bae3e42a85f281bae68f9d92ca74757725
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75695091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889c736f84811847c5c858939a4798aed2d8b76097caa4c6d78166be76e0a32`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:26 GMT
ADD file:c21c2b6cb3f9bdf6cc3641e9ebf810a461174480c6cd1c25515cf9fce4aa2143 in / 
# Tue, 21 Nov 2023 04:24:30 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:56:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23ebe74b854f8f6e2671f4c8cc147a6925fb7d929ce5898f7ca2af9781bf7d38`  
		Last Modified: Tue, 21 Nov 2023 04:29:21 GMT  
		Size: 58.9 MB (58929678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1736e334b1e250eaca590180779f3cbbdea68af8d960e1795174a8524fe6517`  
		Last Modified: Tue, 21 Nov 2023 07:08:03 GMT  
		Size: 16.8 MB (16765413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9e358f5a8c9afb1a2a92c448a0ead789ae73f7a3f08d60828c77a609488c14ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68936498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d58ad62e6f20633b36173add8ac4f67db4f318b98538e0af575671b1d23053f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:52 GMT
ADD file:b0a8fd50925b3555a0c10177e65551cae288917f9bad8fb4728ec83cc0765afe in / 
# Tue, 21 Nov 2023 05:05:01 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:08:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9488c1539560318cb45b39150f91e365b928c0a246788663f5c72d185864bd3e`  
		Last Modified: Tue, 21 Nov 2023 05:10:34 GMT  
		Size: 53.3 MB (53296396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c193fc0604e913e07c3d3f12254414b0f8e42234edfd55788c347f10cebf6ea`  
		Last Modified: Tue, 21 Nov 2023 06:17:13 GMT  
		Size: 15.6 MB (15640102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

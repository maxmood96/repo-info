## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:24f292b45ca540b2f6356802d5e5254a25ab72249cd82d65ffdc567c71de56a9
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:17d5f19cb2f75712e579d4bbaf4dd688d7f48d3174a26217533df8289934aad1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69795449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ef9136713b641beebf227dd0d1f6c4067ddb04b3877e71c275fb7c90d1c1bd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:31:25 GMT
ADD file:8efef3fd1e16c5994e0b27af5c19056cc369818d299aaf62b89b89ad82426fe3 in / 
# Thu, 23 Mar 2023 01:31:25 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:04:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:05:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ddb08f6d450933d22f98a93a56726ec0491dcd496caf4455cfe7066900409348`  
		Last Modified: Thu, 23 Mar 2023 01:35:52 GMT  
		Size: 49.3 MB (49291637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b67c216879c602a3357a3e051406068e953242d0d7b402dd7e6671d414199c7`  
		Last Modified: Thu, 23 Mar 2023 06:09:55 GMT  
		Size: 9.1 MB (9081298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184c8a28afd4da0484a1f9c3cc7e52748726daac5cac85bc0fc702f666f1939e`  
		Last Modified: Thu, 23 Mar 2023 06:09:56 GMT  
		Size: 11.4 MB (11422514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8b516bb4199218b93e0828691cca7924741a8012ef412cd89ec797180b9ad014
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67698334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9438faefdd9540401ef284f3ce81a1c9c2829d48e27358bfaecfb65aedfa6e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:48 GMT
ADD file:b02c911309a1b69d235b76dab369d523653c62374b0173ee9f1b65017607f9d6 in / 
# Wed, 12 Apr 2023 00:48:48 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:18:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8699c4859220eb7e4f2a5ae13e4dd5f9143cb7144e2a02a3eb381a79416524bf`  
		Last Modified: Wed, 12 Apr 2023 00:51:27 GMT  
		Size: 48.1 MB (48109671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b565bf44c40ab65f5193c4fbfd752809f50e95e2c4b2397728f42419979d7c`  
		Last Modified: Wed, 12 Apr 2023 01:22:25 GMT  
		Size: 8.5 MB (8522810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8db076a21199a98e758a14876a91c9a890bb606e6d9d483862bcb73bc5cfbb`  
		Last Modified: Wed, 12 Apr 2023 01:22:25 GMT  
		Size: 11.1 MB (11065853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f45638145f3049bdd8569f5e3e37f9012b169c009beecbf423abcfede1b90b6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64783911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfccb40ab0d880192527f3c9058b284e721f369d3a6a86d097ac545f40dc846c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:28:43 GMT
ADD file:628ac1300ca273dba23c7d617164bc6e664cdebb4106910020d7b3dcb39429c8 in / 
# Thu, 23 Mar 2023 01:28:43 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:42:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 12:42:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:53d7f1f008e91cd29c47c933b404c16fc1d4cf64b8699ad1269e882f53ca6e2d`  
		Last Modified: Thu, 23 Mar 2023 01:34:10 GMT  
		Size: 45.9 MB (45911196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61016f9e9c2f44cda61da9f54267fbafe7fef3695caec3c87c6d5ae9eb452ae4`  
		Last Modified: Thu, 23 Mar 2023 12:46:05 GMT  
		Size: 8.2 MB (8168245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4226b16c6b7093dc765001b6e5615e8150c8d19be6c96ea1171e1ad13654f5`  
		Last Modified: Thu, 23 Mar 2023 12:46:04 GMT  
		Size: 10.7 MB (10704470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c3e4535c3a32e860c9cdcb87e33d91d91a05de0caebac0e396b682b23449f890
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69632231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59a19733f90d03e40a3a26aa25904ff3dd15a57aa3bc07c4723ab3a166147dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:21 GMT
ADD file:2784bc6dba1e1dbea293e074ebf51fa7d89cb5545ea63ba2ed75b74d067387d4 in / 
# Wed, 12 Apr 2023 00:40:22 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:10:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:10:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:43d214f7ab3ca35a0c9ed4d8cdf62b36248aba2fa1bbac4ecd64e82ba2520b70`  
		Last Modified: Wed, 12 Apr 2023 00:43:58 GMT  
		Size: 49.3 MB (49327656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99d9e5d2b2df062d16ffea4a022a4c09ce904fb96ec3fa4712a1d936593ae2a`  
		Last Modified: Wed, 12 Apr 2023 01:15:01 GMT  
		Size: 8.9 MB (8915031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd2b1a4cab3b4ac2bb4a7e9aaaa60ce806e3c49a8726f7baf5a10ba5e0e89fb`  
		Last Modified: Wed, 12 Apr 2023 01:15:01 GMT  
		Size: 11.4 MB (11389544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7fd624c3066dfa1ca3da4f7665c730788104cdc2cb90f94fe839582a1a20bff9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71401769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d2d9289ea8eef61411b36e3c5358bc3e57f93d19422a12cdce3b5d7d7e922d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:51 GMT
ADD file:31710a830769b5e1f2612e1cd05380f677714bf52f61a54adbc7424087fd1378 in / 
# Wed, 12 Apr 2023 00:39:52 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:11:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:11:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:35e4af56b8bda58bf958814bc36c8e3a9a1d719c8582c0f33d7d69cc5b416211`  
		Last Modified: Wed, 12 Apr 2023 00:44:24 GMT  
		Size: 50.3 MB (50310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145bb18c860aae65312434f79bce9d784a4824ef455202efca0f687a388037fe`  
		Last Modified: Wed, 12 Apr 2023 01:17:27 GMT  
		Size: 9.3 MB (9263774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2063c41d1dff24f54b6a7d8edde21610fe37e02b35ed369be0ccf9f64cdc43fe`  
		Last Modified: Wed, 12 Apr 2023 01:17:27 GMT  
		Size: 11.8 MB (11827096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1cb13e8dab0a14d667e4d9b265c749ae59a611e6862763377f1c8e34e0112c01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68902391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54d7ab7b13f29c59bc95210628c83870c56bc3b074d787b15d305d64a13d17d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 05:18:32 GMT
ADD file:2d913f7b6c2e804834958b3d144bd7b5150a438e2aaa73cdf2f1be1c64d10100 in / 
# Thu, 23 Mar 2023 05:18:38 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:22:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:23:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:83c1a140184ad386a37a5446dba474a2a8498dff7ae8d2ccd2957aaf8dc1682e`  
		Last Modified: Thu, 23 Mar 2023 05:26:35 GMT  
		Size: 49.3 MB (49291603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaeb19ea7953e3c0a2cce0d76910d46a1fc5e289c90379ecb81b3e5ba2a0c16`  
		Last Modified: Thu, 23 Mar 2023 07:37:04 GMT  
		Size: 8.4 MB (8439874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecc4eca24f781c1e786d1fc88cb24202f1248f85adc06cf1b375f5607ec2d93`  
		Last Modified: Thu, 23 Mar 2023 07:37:04 GMT  
		Size: 11.2 MB (11170914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:85bf0cae57000ef766ea7ed7d8f16d94925cfc5dfe0ffdef79a82c81cfdb0bd8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75136981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f95dec386d645db16ef52d1d12753c4acc5e8cd37261e08c733828e13efe122`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:20:05 GMT
ADD file:3534cf3f10dae5b70c64865fd70cf5b9aa6ace6be9caa2d69518d6d59c4943fa in / 
# Thu, 23 Mar 2023 01:20:08 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 13:18:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:19:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8de2c12bac6cdfac096a845424e637222b157d221d8080dfc0e3cd14581716d5`  
		Last Modified: Thu, 23 Mar 2023 01:24:47 GMT  
		Size: 53.3 MB (53290173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ffcd14b130bc950e2e794bcf2e09ddffa8e18668803aa384fc8de743e9d8d2`  
		Last Modified: Thu, 23 Mar 2023 13:26:33 GMT  
		Size: 9.7 MB (9661589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecca2a654e1b66be833e49110ac475ae4995f36d83ba12ad0396e8f4cf953872`  
		Last Modified: Thu, 23 Mar 2023 13:26:33 GMT  
		Size: 12.2 MB (12185219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b6ecdf5c65f021e05c80106a2cc8a598f2fb062039c62b358a2a42fc40f3d4d8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64406378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc1ea8528f7edf3edcdff9fd62663fec45eaf492953562405ce7f8504695160`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:05 GMT
ADD file:b8c0cf42f791d92283c2c47cf2ed446fb98a7cde685c9b923c89cadb86ddad31 in / 
# Wed, 12 Apr 2023 00:09:07 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:32:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6178d7c3b8603b1579d72ad9f5bda8fd22627feccccd498dad946eddfe96d27a`  
		Last Modified: Wed, 12 Apr 2023 00:12:25 GMT  
		Size: 45.5 MB (45494949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd056fe810f7c94134b5c26af6939949c18bfa4868dbc9f81ea8d7a25a0daf4c`  
		Last Modified: Wed, 12 Apr 2023 00:44:01 GMT  
		Size: 8.1 MB (8117374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f8d5394c046224d62d5170fd151d4339e0f5131b1503bf3eafecefe1ec7a10`  
		Last Modified: Wed, 12 Apr 2023 00:44:01 GMT  
		Size: 10.8 MB (10794055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2a32ff0d5208b6ad040a9cb58b776824b3c95030e002745b9128549a0e88a98e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67666740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d98184dbb030d39270ec3b57dcd40af7dc1cb4c8755f6afe805779ab651c12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:01:19 GMT
ADD file:0593fbca11f3d4a9b2b916ee99bb70651af04ea1275262f12e9b0e5c07e81f0e in / 
# Wed, 12 Apr 2023 00:01:29 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:28:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1844a6b5cc32e25703d3a6ac2115866157b1f856d7463d0dca8443fea51061f1`  
		Last Modified: Wed, 12 Apr 2023 00:05:31 GMT  
		Size: 47.7 MB (47665068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f306dc6c45f3e2637390b46a2dce7fb061bb8be6ae7c72c47bba97d84b99d256`  
		Last Modified: Wed, 12 Apr 2023 00:33:37 GMT  
		Size: 8.7 MB (8713548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7676682574fe22f1cac8016a4f36ad54898c4313e0609a7e88e75e035e32444b`  
		Last Modified: Wed, 12 Apr 2023 00:33:36 GMT  
		Size: 11.3 MB (11288124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

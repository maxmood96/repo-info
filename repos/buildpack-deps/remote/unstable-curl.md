## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:030a9654d45dab965b321a7d5863b14ece9aec074613d9abae82bcdee1ab31cb
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
$ docker pull buildpack-deps@sha256:67ccfadba9024a28b93563f14db9944a2c649f233db3cfb90f155333678cf215
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69428500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42de8cdc96b8d839a3f771af32b8372411736863b8062700709298617a3b2ea6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:35:41 GMT
ADD file:3bae49887734af64f153e9e3668684efface6dd04ba31139b3d6b3aeb7589128 in / 
# Wed, 11 Jan 2023 02:35:41 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:07:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a0e522725e09a558b80e5d58e7b360150ad3fe901915db5358002bba7e461b9c`  
		Last Modified: Wed, 11 Jan 2023 02:40:40 GMT  
		Size: 49.0 MB (49040747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9982d6c78fdd2a5e480eda90cc33945a46c3a49f844c51993bdb61ea401c22`  
		Last Modified: Wed, 11 Jan 2023 03:14:08 GMT  
		Size: 9.0 MB (9034446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f912e649ff1b5f13cde3e28b1254be9cef3ad6b8f7e119be8bade6ad4a2c301`  
		Last Modified: Wed, 11 Jan 2023 03:14:08 GMT  
		Size: 11.4 MB (11353307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:dbf167c21240c1242196d8c90baff84fe0655902508a531fad9591f9d56fb1af
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68339179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d887ab2a1969db624022a02ccf6517953432d7e4b390d23ad1d6ad45d3a90d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 01:55:48 GMT
ADD file:c258ec7f780b3ff9c8cd584e0032e838b39a09afc46940f4ac745695130b67ed in / 
# Wed, 11 Jan 2023 01:55:50 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 02:28:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 02:28:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a63c02841fd8a16e36e06a2fa4539584c2578f39a3f7bd88934a6c67fc294d9e`  
		Last Modified: Wed, 11 Jan 2023 02:01:08 GMT  
		Size: 48.0 MB (48017943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e0852ac4954f884346a0ba77b1c72d65daf0148903acb9a35db7dfad06d432`  
		Last Modified: Wed, 11 Jan 2023 02:34:15 GMT  
		Size: 9.3 MB (9319858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ff229adae1feab6cbc20cbc1815df4cda72e4b5f1550cc783d1ac1878ee67d`  
		Last Modified: Wed, 11 Jan 2023 02:34:15 GMT  
		Size: 11.0 MB (11001378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:092b197e636deba8def98e1724d5a7ab1e397383c55ebfc1edeb257c6e65ddda
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64607073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbaff2f440b26a0f1b3d91996da0829e25f7f7ea94214b9aa098ec57d89743c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 04:01:58 GMT
ADD file:45e9dcffe5e042927af8c1ae4e6393b33fda2a9ad194140450689e4f039e0e20 in / 
# Wed, 11 Jan 2023 04:02:00 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 04:36:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 04:36:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b5f9150f24704ac05df76d4317fa7947141130d434993eb229642f2806e580c9`  
		Last Modified: Wed, 11 Jan 2023 04:09:46 GMT  
		Size: 45.8 MB (45836631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76dd86f667638a0d24fc7caca6a13df077a2ca83ca774f180a73ae3b21239d4`  
		Last Modified: Wed, 11 Jan 2023 04:46:26 GMT  
		Size: 8.1 MB (8136164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483384d04259c74f6b246f5f72d9b7808cb4db037464d9e35959767481be012a`  
		Last Modified: Wed, 11 Jan 2023 04:46:26 GMT  
		Size: 10.6 MB (10634278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8399dee50485a5b688ca4d79c96e8b593df4120d6951c1bb7c0d345d0b670242
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69270237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7feee35f59b4bcd8c8084ae00bb1bb439020c9af9f46d15495f0225e5a75a1d6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:58:15 GMT
ADD file:b780242785904e4fb27dec85c00f7e10bcc0dbb0d7006b133d9038c4328c7d83 in / 
# Wed, 11 Jan 2023 02:58:16 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:27:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:57ec0bfa7127b6c459b1b1f099459b850b4fa150e388b2c3ba10105c4a746caf`  
		Last Modified: Wed, 11 Jan 2023 03:02:47 GMT  
		Size: 49.1 MB (49084551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c81a30877f5e4b6157288cf3088552f011edc6c7b1f1ad0e931c54a99121d57`  
		Last Modified: Wed, 11 Jan 2023 03:33:22 GMT  
		Size: 8.9 MB (8866992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dbcce22354f1f070c2b60f5cdce7ed07210c870842c8951379f29693c8191b`  
		Last Modified: Wed, 11 Jan 2023 03:33:22 GMT  
		Size: 11.3 MB (11318694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7b5c2eb7be982db3bf03954b5d84617c97dc4bdd642e221c0c23ade293e6b022
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70852009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee10c339051eb198804bc1d1979160fdcefb2f00812bb18db29785cd3a97ada`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 03:17:15 GMT
ADD file:70daac43e15ae08f49ca2f191e46f20fb9df90f6fa25b199b61103e75ae43d16 in / 
# Wed, 11 Jan 2023 03:17:16 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:50:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:50:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:19edd03a92bb4010fb5a10c8cc739c02db9ae484e4e25247ce4b7e0977cf1e9d`  
		Last Modified: Wed, 11 Jan 2023 03:23:48 GMT  
		Size: 50.1 MB (50082487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cabc838a5a608c7c069930064fc921b2d9d4876490abf6fb0f2167b38bd8a8`  
		Last Modified: Wed, 11 Jan 2023 03:56:53 GMT  
		Size: 9.2 MB (9213611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdadd8b2dc92af1b4e9d2450c4417d3496f769af427b8ef28ebfa4ba33e8f68`  
		Last Modified: Wed, 11 Jan 2023 03:56:54 GMT  
		Size: 11.6 MB (11555911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:73d41217368bce50e169d9865daadd3d5485d5a756dc572306449a883b73ed4c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69788034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebb67403d4f8ef4a6649282a3df5aa669795e3ea2cbbf6e66b43ed1f670f677`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:11:07 GMT
ADD file:bc4f0f717f54bc1982dd6d104f684f180c7b8da660351e5be4853a56b38e374f in / 
# Wed, 21 Dec 2022 01:11:13 GMT
CMD ["bash"]
# Thu, 22 Dec 2022 00:03:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Dec 2022 00:03:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:22a773956e0933f1a01038ae977c7c99f46cd5ce02f672c66be9a1c837de4eac`  
		Last Modified: Wed, 21 Dec 2022 01:19:25 GMT  
		Size: 50.3 MB (50292945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189eef164aa69dcb61fb78c17df64c6779df804d82ba70a52d4e89d3b19eb0ad`  
		Last Modified: Thu, 22 Dec 2022 00:18:32 GMT  
		Size: 8.4 MB (8376404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1e283b7e05e1f80446c30786dca684e73248af2172c069b9d51b1bab48ee9c`  
		Last Modified: Thu, 22 Dec 2022 00:18:33 GMT  
		Size: 11.1 MB (11118685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e6516355d5355fca39c7b51b795bd1f6127d73e0123443df3c72bb27f6c2e1e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74808691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aaebe271226e56519ecb2868bad2010807fefd88187277321119b2e87f9229b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 03:49:50 GMT
ADD file:a8a466b916dd8b82163da9263cfb32eb757c2a0eb173228a5ac8ef05bdc55653 in / 
# Wed, 11 Jan 2023 03:49:53 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 07:17:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 07:18:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:35c8c29d2bf600cd3a311b3649ac4076a0670c35cc296f1f28d2622bb6dd54d4`  
		Last Modified: Wed, 11 Jan 2023 03:56:03 GMT  
		Size: 53.1 MB (53077709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab0d63135d44be3ecac38d5206687b79632de571e5c05f58c0a49d13d4dd332`  
		Last Modified: Wed, 11 Jan 2023 07:27:41 GMT  
		Size: 9.6 MB (9615481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b2df2d7c9512f9de0ee08a692413dcbdbf53d56bc49fda25fae6cba32ce022`  
		Last Modified: Wed, 11 Jan 2023 07:27:41 GMT  
		Size: 12.1 MB (12115501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:497cc8982890eab597c6d34bdad7c65b903ffb329fc1dd479748adab4dcd7558
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65240087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb5da4fd1d86a7ef3a37f0981a23b5ed7a1ac32ca8221d418dafceb3054feee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:10:21 GMT
ADD file:ce5483e7a7d6e8eae2ec1f1c22390523d24dd0e613a20f8d424c81a1e12240ab in / 
# Wed, 21 Dec 2022 01:10:24 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:05:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ec8e0a8db89be83ab5fa46e2a3ecb60ab7e5df3621c585c4ae748c563af17385`  
		Last Modified: Wed, 21 Dec 2022 01:26:34 GMT  
		Size: 46.5 MB (46453589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f8c6e126b4271f9c21a1890d7345d3a741f26baa2d58b1c871c87435c0d4b8`  
		Last Modified: Wed, 21 Dec 2022 02:33:08 GMT  
		Size: 8.1 MB (8052896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45d51aafdd462331d0b5b67c93150c348af9265261f8e51be63ebd57302f9d4`  
		Last Modified: Wed, 21 Dec 2022 02:33:09 GMT  
		Size: 10.7 MB (10733602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:501736616e0043817cc4266704e1b2ea46d71785a8fcc91c5cc9cad0daf2f524
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67315403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5deaf1b7f5262a80b1874b26dbc773337e201a6f1f0d4db98eecb9977d8a5f62`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:22:39 GMT
ADD file:603b8f38f314737d8b96d7fa7c31b4c6ede8fec5c46d30621085354a718b7cf6 in / 
# Wed, 11 Jan 2023 02:22:43 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 02:50:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 02:50:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:63d179f68a4d4f8c050f7c24ec5c73831d75b928d359ddbbf2e658360463fd13`  
		Last Modified: Wed, 11 Jan 2023 02:27:08 GMT  
		Size: 47.4 MB (47434084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8ad9595a7cc2a79974880bde3167e302536eaeca227adc959cfa976ef5c29a`  
		Last Modified: Wed, 11 Jan 2023 02:57:32 GMT  
		Size: 8.7 MB (8665726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53049c87c88bc24602f77d08379e056c3032ef773e4e1b619f0f1b543464ab90`  
		Last Modified: Wed, 11 Jan 2023 02:57:32 GMT  
		Size: 11.2 MB (11215593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

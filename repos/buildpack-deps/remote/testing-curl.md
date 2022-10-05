## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:229b5e94458367014fa96fab2f4ec17be4fc82596a3fc9b4d1a2ed8ddbf15570
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:65f4152e56d007d77c7d77e60f052056273d3a9ecd93ec0ee27f03e9d06c15a2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73642716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4264bd0b8285ea524f31b2355c6cd723c750a6c269a38987e6a7776185b1666`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:03 GMT
ADD file:ca5a5911d0951e5c75f1790eb644a6fd41dcb9712fa2af0fb6d3a537a72e6ad8 in / 
# Tue, 04 Oct 2022 23:26:04 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:52:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:52:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6674a3ae4f8f54c2f747bad2069e50ce00e352d650887729310d984cebecea22`  
		Last Modified: Tue, 04 Oct 2022 23:29:50 GMT  
		Size: 53.0 MB (52962415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e064222ce493e48ae4ceac8f18316e08d2afb963ad57bd63b8630a0ae009f8`  
		Last Modified: Wed, 05 Oct 2022 01:18:07 GMT  
		Size: 9.3 MB (9298646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab229472e3a483409ce2bbc4d461fc6512c03c687daf6546b52705bc7f18961`  
		Last Modified: Wed, 05 Oct 2022 01:18:08 GMT  
		Size: 11.4 MB (11381655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4c3fea69e1e4777e0477d2bd05fe0a928dac89285b2485e281c89d33f1116888
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71612761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159dda42248d4464a45912c2782dec3cd5c2cf073da7e38e5ab9a9ac80cde99a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:48:31 GMT
ADD file:2f3df348b6a9200fcbcfe13a10334cef72dca5f19d7ed73055f7a03ff08122f7 in / 
# Tue, 04 Oct 2022 23:48:31 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:12:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2843f1fd91937d710e0d158046e9c23fe034f11c8c934a478f443b561be758dc`  
		Last Modified: Tue, 04 Oct 2022 23:52:36 GMT  
		Size: 51.8 MB (51838659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0cbaeabf686852f0109b0402554bbb882e0b7f95b9befb62dcb2c9cf5334b69`  
		Last Modified: Wed, 05 Oct 2022 00:22:23 GMT  
		Size: 8.7 MB (8744107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01b61654d50a40ae8ba57e261eb049904e5e6879f2e9421bb37a8653997b3e6`  
		Last Modified: Wed, 05 Oct 2022 00:22:23 GMT  
		Size: 11.0 MB (11029995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5b0dee0e2cc0e1938cf13bff64e7e8012209764899a65e170b1d0ebc91e645e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68750987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d654a5ab6c7cd35f5bd3a5856e37d1f2b004dd7fd02791250fb62401d704090`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:57:54 GMT
ADD file:9f3a74b8856c0affe36dd4e0700a8a2686a9d2275934fd9af95135f13731d10e in / 
# Tue, 04 Oct 2022 23:57:54 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:29:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:29:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b2ee1685df1bf13149eece9e0085c6befe355f21deeea69484a3ab1fab51e40c`  
		Last Modified: Wed, 05 Oct 2022 00:03:53 GMT  
		Size: 49.7 MB (49692608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237b865ef48770b9d41964e18461ec2d393677f4fc653a0953e9f0b9773d47ac`  
		Last Modified: Wed, 05 Oct 2022 00:52:01 GMT  
		Size: 8.4 MB (8396889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902b8eea02f53006b302a3dbae787275ce520ccf78df670e0dcafbfd1c4e17cd`  
		Last Modified: Wed, 05 Oct 2022 00:52:01 GMT  
		Size: 10.7 MB (10661490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1481632890c7a3ff9c1451626fec55caae7629692e9bdd524847cd9761439cc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73242713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6b892888321feaf66863a61297f525763ba073853acb3ddda2197f0c5ee3e1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:00 GMT
ADD file:269c8bec4871d84b9133706a2f391209619d53c0bfa56121c740757cf5798fcb in / 
# Tue, 04 Oct 2022 23:44:02 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:21:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2debf9e7f23054c81a936da9b01c5db9f72a55d4810f7bf0e5641bd1748d90b7`  
		Last Modified: Tue, 04 Oct 2022 23:49:11 GMT  
		Size: 53.0 MB (52980389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a790615211c3ee762ced64a5b81859f93d76062f4cf9c83d396fb13c24f7cf`  
		Last Modified: Wed, 05 Oct 2022 00:36:13 GMT  
		Size: 9.1 MB (9128105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae70f6dfe035ba217dd9a40e630bb3cae03e8d9cef649641a8a502495edf00c0`  
		Last Modified: Wed, 05 Oct 2022 00:36:13 GMT  
		Size: 11.1 MB (11134219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2a81e9afd940a37049d2c75e3ea14fb2502ecf75afa4d6093ba9a4493bdb3ad7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74983577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b6146367530e5e957c510fc3932d48e1f1f9965b00c9a9a10d876920876532`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:38:57 GMT
ADD file:2a0c743e373aeed6462c2f3ae8a138fb0e240e935ad7ca5bf008aa3efd3673a0 in / 
# Tue, 04 Oct 2022 23:38:58 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:06:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:06:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c68776dad61a299b8e65d1a6a02e376b8ed2e9b241bd753bf6c35d497055ecdf`  
		Last Modified: Tue, 04 Oct 2022 23:44:23 GMT  
		Size: 53.9 MB (53932827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e1a78eaf50f3a9e7fd0eaec3d6abbc176033d6ca5108dafee5df9988d1427f`  
		Last Modified: Wed, 05 Oct 2022 00:20:44 GMT  
		Size: 9.5 MB (9473771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cc3926eab5aa6b28a396ddad5f657d4bd9890ed5be6836db7cb21429b7923c`  
		Last Modified: Wed, 05 Oct 2022 00:20:44 GMT  
		Size: 11.6 MB (11576979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e5058dddc52ad36c288407f5af719a4dc3aa74924aec66516c30dc751bdfa176
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73215183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5951df76190d6ae0ef0fa7a4d6820b112afae63e962209ec9582838531c05a6c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 01:09:11 GMT
ADD file:3491a858e0f5d7985f9d29ad3567a39b0271d5794db146892787053625c3b44c in / 
# Tue, 13 Sep 2022 01:09:16 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:40:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 01:41:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b94700b51ec501e09ccd1e3b3962175f6110497a6ce43a01932cb0ca2718f356`  
		Last Modified: Tue, 13 Sep 2022 01:16:48 GMT  
		Size: 53.4 MB (53424305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc07918d1372f974586c63d6aecbeb7a19896ffcd4f48df4b090b4bb8ec36db9`  
		Last Modified: Tue, 13 Sep 2022 02:02:34 GMT  
		Size: 8.7 MB (8657983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623176abb726f5305a72b42bb4719f479242a849cee500abc5f6ce16b8f94697`  
		Last Modified: Tue, 13 Sep 2022 02:02:34 GMT  
		Size: 11.1 MB (11132895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5ccbecabed537e9c487c2dc7ec503351ba0cb52a24238ea701d2f4e0307a0104
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79138638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d590241e6109dd3cf4991606afc14594fa1c6acf47ede90f6703f6b7948ca8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:16:56 GMT
ADD file:22dddefde9f3e8eff6049751a459a3c4fdade46622016ce6269b630157170962 in / 
# Tue, 04 Oct 2022 23:16:59 GMT
CMD ["bash"]
# Tue, 04 Oct 2022 23:47:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Oct 2022 23:47:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8fd653dd210d0ff49ceb9b32e662a564ab01445265e165edd4f963c3953f5b33`  
		Last Modified: Tue, 04 Oct 2022 23:22:42 GMT  
		Size: 57.1 MB (57111564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0f7f38b022f1a84d71f8e4124fe0133ced1b702ee627bff0eb3e756558fbdd`  
		Last Modified: Wed, 05 Oct 2022 00:02:33 GMT  
		Size: 9.9 MB (9883282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79064b2f900a5a0fc53fac8232b1268f1f2e3496cc5722826e03a2b768366be9`  
		Last Modified: Wed, 05 Oct 2022 00:02:33 GMT  
		Size: 12.1 MB (12143792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:159b89a17ab3b76bfb279482fb906e1cfdae0d2eb17e15ee717502f505f12606
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71456230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff8dc2fcfed184695d8f875639a4d5ea4a5d82c29580c26623fab8f0108d5cb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:41:48 GMT
ADD file:75b0ff403984b3c95919c781c632871090a7238d4c22c9c631160406de8309a4 in / 
# Tue, 04 Oct 2022 23:41:54 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:07:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:08:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b7893043d434a6c00815ae2e7de11adb8c1f06815bbea513110060ae94e8851b`  
		Last Modified: Tue, 04 Oct 2022 23:46:26 GMT  
		Size: 51.3 MB (51280212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ed7a0c18fee7ec61cc5b8d9ae520abe4b09aa014195c8b9481866aa0eff290`  
		Last Modified: Wed, 05 Oct 2022 00:31:29 GMT  
		Size: 8.9 MB (8935386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847d523eea662ddeeaa863120a2afe9127a5bb8c4a67ff524928ce23514e9469`  
		Last Modified: Wed, 05 Oct 2022 00:31:29 GMT  
		Size: 11.2 MB (11240632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

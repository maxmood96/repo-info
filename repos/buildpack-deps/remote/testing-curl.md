## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:bd09358a2cc9bf64a51e42d6f2d31ce0c8c60c5883b89d8262f9ae3df8cec080
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
$ docker pull buildpack-deps@sha256:0fb66f4c1df22615d652c3505e28c2962eedc85aa1b4b6d76c37edc447c1f4c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69765147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f4ce0a00ef02c3e42bca03233a31b33d0159c10ffa472b824ca96804d5f682`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:29:51 GMT
ADD file:98917c081507795b8ce084d09f5df75e959c5365882d73ca7a52da226c93fdcf in / 
# Thu, 23 Mar 2023 01:29:51 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 05:59:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 05:59:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c15c60aea1a8c926f00ec7713f9ae1fcd349591095bddcc01ee5a6027b8a3998`  
		Last Modified: Thu, 23 Mar 2023 01:33:26 GMT  
		Size: 49.3 MB (49278011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7a10c25fd2bd2e34fb5e4a59e626d6bbc6f8fda13a14dd73e631b3c91c2e3c`  
		Last Modified: Thu, 23 Mar 2023 06:07:02 GMT  
		Size: 9.1 MB (9081481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0d04ad2d6622983195ee4a7f6a29b48e631f0f4722d7d32ca1a3920924f91e`  
		Last Modified: Thu, 23 Mar 2023 06:07:02 GMT  
		Size: 11.4 MB (11405655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ab98c3b2a788f875511e5e9b0281839f15aa57a4991c4c689a1cd458544e3a44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67691031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640b162279ef98924d9653a829b3b12e5098b863374d465f06acfc6ffd2578ee`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:48:20 GMT
ADD file:db0e63af763d83bde06370ca01585b3ee9f44f7ed2882957bd550b09c5f1cbc2 in / 
# Thu, 23 Mar 2023 00:48:21 GMT
CMD ["bash"]
# Sat, 25 Mar 2023 02:36:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 25 Mar 2023 02:36:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:de716ea1518d1453b21c4aa4b1dd63157f88ebd2da72a9849cd248b6ba9dc14f`  
		Last Modified: Fri, 24 Mar 2023 23:21:59 GMT  
		Size: 48.1 MB (48116759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054e6ff49d1df0dc5ba1eccd502285b0020102b49e8796ba766a5d4b90767319`  
		Last Modified: Sat, 25 Mar 2023 02:45:23 GMT  
		Size: 8.5 MB (8522656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5753756896417526cd79400e7a964a0dae5572c6b09a63d6aec5a9543d4ef53b`  
		Last Modified: Sat, 25 Mar 2023 02:45:23 GMT  
		Size: 11.1 MB (11051616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1a5fd5565a96a28b5697fe91cee1bfa10686530f24736891bcc6aab90718b2ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64745350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320b1096c45b1588add1358fdcf606ea86168a27bfae2aea622165c45259f995`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:09:37 GMT
ADD file:084e44d77ffdb8aad1f856ec10db87922bdba3a90e06f9f1cafcb6e4284c8ff7 in / 
# Thu, 23 Mar 2023 01:09:37 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:37:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 12:37:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0b14dce67c2fdb37d2b0eacccff5119e226c45c2906f12d6ee93d8850400824b`  
		Last Modified: Thu, 23 Mar 2023 01:32:34 GMT  
		Size: 45.9 MB (45889194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395ab26b892c3659080680521b7e37b5cee24838f59696a77cfd944e93ccd158`  
		Last Modified: Thu, 23 Mar 2023 12:44:04 GMT  
		Size: 8.2 MB (8168514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07788f0ce3e6e5ae63843a828f2542045686f8131e60c22d54846351e88422de`  
		Last Modified: Thu, 23 Mar 2023 12:44:04 GMT  
		Size: 10.7 MB (10687642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2639bf0010ba07cb4d76830b164d3f00c49c2e591b4b7d33e3df33d8ffe01af2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69614525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1998bdcff0bfe38296102103f303c16098b207c1bfd10c87c0da1fa88b653ee`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:44:48 GMT
ADD file:fc54d0a42f70d91c654d7ac03aa3d437fad192d9f4fd701e214da74c18630636 in / 
# Thu, 23 Mar 2023 00:44:49 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:08:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:09:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b813e5ae6de73806a605f44184f1b7d14569e88447b46841154803d1dd1eb646`  
		Last Modified: Thu, 23 Mar 2023 00:47:13 GMT  
		Size: 49.3 MB (49328280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d2c7ce01662547528b6d61e036191dbfe660303bab6f430344734845b3291`  
		Last Modified: Thu, 23 Mar 2023 07:16:16 GMT  
		Size: 8.9 MB (8914423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f716da59b3846ca60aabeb709b6096ee3b11de955af29949f2e1ea56c6e43331`  
		Last Modified: Thu, 23 Mar 2023 07:16:16 GMT  
		Size: 11.4 MB (11371822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:623b046484b279e6f72cec0cec1f759a1b672c0ae14af515289c5cf64dcff156
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71394904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b7cdce9a98b4064762dfd0c76430eb016d92a7e15021c6bdf91d15f58d5dbc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:38:46 GMT
ADD file:a8b128db07f7f5c47ccd2afe2595fdf9b31844beff2d07ae2ea0e204e2aef4c9 in / 
# Thu, 23 Mar 2023 00:38:47 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 13:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:42:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4dc30e65d953c72fa1dd5a25980f7eeea620434c102211fdb72a04706c06dd96`  
		Last Modified: Thu, 23 Mar 2023 00:42:07 GMT  
		Size: 50.3 MB (50323933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4e857b25978a7d4a42bbc134bf1ee209791d8f3fff94cb3745d9753472886a`  
		Last Modified: Thu, 23 Mar 2023 13:51:54 GMT  
		Size: 9.3 MB (9261870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845682110df86e268754e9c3ecfa5297b566a487052aaf7766ae3e9bb0cfe5bb`  
		Last Modified: Thu, 23 Mar 2023 13:51:54 GMT  
		Size: 11.8 MB (11809101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cadf8f4e08099c01875c361dcd8fba3645b495aeecf0d53c2fd22a569372c184
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68885675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad6eff184509b73b66c889069c907dfd84004b8c2324f62ffbe80bc0453f87a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 05:15:54 GMT
ADD file:454bfcbdd9d738730885002e9124aea5e8eb4920ca5d3bf13bb9f4707023bd67 in / 
# Thu, 23 Mar 2023 05:15:59 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:03:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:04:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:70edc5cd98f5a2e589d309248c77122dabf95f437c0448b99513b15ef209f244`  
		Last Modified: Thu, 23 Mar 2023 05:23:55 GMT  
		Size: 49.3 MB (49291654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74250ff8fd2374ebbb2086f535377d5246a78ee51939da5984dc42e7afe6d2f5`  
		Last Modified: Thu, 23 Mar 2023 07:30:58 GMT  
		Size: 8.4 MB (8439840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649c3b2ae326a6eb2a81faaff9322b317ad4788f4c53f6c3b6721724ed9f3d04`  
		Last Modified: Thu, 23 Mar 2023 07:30:58 GMT  
		Size: 11.2 MB (11154181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b2e26276ba83c4b68ff602aaa743294d6f71c408e0912d7dd1a787da5bffc9c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75120105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6cc655a5db67e5cb97de4dfb139ff43049f64913c4d3b79788825fea30a1c9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:18:49 GMT
ADD file:5e17f6075630657b8465309f99ecbfc57e325d159b54f58181b974526f2314a5 in / 
# Thu, 23 Mar 2023 01:18:51 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 13:09:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:10:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:60e68956630003599038e3cfe86d6dd09ee874e8c30d9ea29b8350e0d3fa8497`  
		Last Modified: Thu, 23 Mar 2023 01:23:06 GMT  
		Size: 53.3 MB (53290316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bcdbd51144dbb4a208e40072c2caf491305afb997e9161481db00137eefec5e`  
		Last Modified: Thu, 23 Mar 2023 13:23:20 GMT  
		Size: 9.7 MB (9661293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bed649f1a85d37347952942e0ee256bdf515769a40a1c23cf02e65c6c90e6b1`  
		Last Modified: Thu, 23 Mar 2023 13:23:20 GMT  
		Size: 12.2 MB (12168496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:298db3ad581a56e2a70e82274c0e717ad5ab9d574a00299a643dafa4e680d559
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67653616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290be5986aa7b55668dbd44a9fbced7c69acb9e78a980a946a6ef4fd3bbd3eb6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:43:22 GMT
ADD file:2114d04d7187ee787a64bd515adc18fc532b91c0272b95492fd44714772b3eb4 in / 
# Thu, 23 Mar 2023 00:43:24 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:14:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:14:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:09c6f64f2013e0d0258d4e75a51c004bfcc5479af28502ec4cbf6e25f28ee505`  
		Last Modified: Thu, 23 Mar 2023 00:46:39 GMT  
		Size: 47.7 MB (47671033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e82f091e943de9ab4106fad4ac73a5dc36724b95a34f43ab7b13cc7bdaab83`  
		Last Modified: Thu, 23 Mar 2023 07:20:30 GMT  
		Size: 8.7 MB (8713238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de18cd0ea70f6df120e2f1d1378f749815fcc7ea8a2e507e53cb8197edf3a91`  
		Last Modified: Thu, 23 Mar 2023 07:20:30 GMT  
		Size: 11.3 MB (11269345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

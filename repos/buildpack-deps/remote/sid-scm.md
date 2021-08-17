## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:46fe4341dcb0c984a75bb31226a986514103472114a51f8641e0c3de2616ace0
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
$ docker pull buildpack-deps@sha256:fcd3b293743077761c86cb0727ecc37367cc990a22a49680aee847893bdaae64
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126213428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fafd28ad644ba9be4f74a5cdc1eb067dfc762badc0804578e2ce613f29d667b6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:46:20 GMT
ADD file:cac9ad9d988141c80929e8c31f4cb388618dac0bbc048d4c5e3b8029c85c576d in / 
# Thu, 22 Jul 2021 00:46:21 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:13:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:13:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 01:14:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:531fc43e70accbfd0e52721b79cfd564769d6f1b7e64a98e9f670327d4c4820e`  
		Last Modified: Thu, 22 Jul 2021 00:51:36 GMT  
		Size: 54.9 MB (54909299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f3334cfec756c2189b8a7cce5cd3ddf363b2acfc7b8a38f1ccf8cdbe4ef115`  
		Last Modified: Thu, 22 Jul 2021 01:21:10 GMT  
		Size: 5.2 MB (5171133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284c0769674315a1486ea9eee2a7dbe2a630850d90b8e445a2b8d7034528be1b`  
		Last Modified: Thu, 22 Jul 2021 01:21:10 GMT  
		Size: 10.9 MB (10872519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5845626ba0291c9852420419c76d5f8620b7801dc4b4420487f0119d42c59b6`  
		Last Modified: Thu, 22 Jul 2021 01:21:30 GMT  
		Size: 55.3 MB (55260477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fddc868bc480d8d9c096cedd279e44d56489226fe39c2a8ebd4b4128d19ffab8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121060861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35367af5334f37ce7b69443897d7ae4354af1708ba2d1483ff7a11ab46e7a8e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:51:25 GMT
ADD file:7b9b18b6a1a6deb81eb9bf8638d60de26198ba106aaa757dfb838b264fc90252 in / 
# Thu, 22 Jul 2021 00:51:26 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 02:07:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 02:07:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 02:08:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9de879dbb26d0cc624c499f5907a14117d0f357e4e39699d3208c57d5091b537`  
		Last Modified: Thu, 22 Jul 2021 01:04:16 GMT  
		Size: 52.4 MB (52445986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef97169c47ca52a8e66f6ef70d0a4d9e5cfae0f8b72d1937ac646b3bdf48d8a`  
		Last Modified: Thu, 22 Jul 2021 02:24:13 GMT  
		Size: 5.1 MB (5075544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e445910f582e1f6da040a3bdd8886f00fcc077bf63486317b6de7c17cf3ba01`  
		Last Modified: Thu, 22 Jul 2021 02:24:15 GMT  
		Size: 10.6 MB (10571845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d89631dabbc12408ce2f82d183513c97cde3d9b7ed0f3d4863be9777cbc50ed`  
		Last Modified: Thu, 22 Jul 2021 02:25:07 GMT  
		Size: 53.0 MB (52967486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e5b3206697bb0c0eb1cf9cfc0de827c58df2c947994bde46d403f1ced6336e05
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116192536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a002dc841a1b3a25165d14c2b6b12e95bdf8beac7616c7a3316e35a527f945`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 02:05:12 GMT
ADD file:dc3a5129f00ffe49d5f2b5c7472bb0e89235fc02cd3f1cc7d27243e371d4a8e9 in / 
# Thu, 22 Jul 2021 02:05:13 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:18:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 04:18:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 04:19:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d81caeed2081307865201ac11c62494bbd309b5efe940cf9cae7a6739c8ca2a0`  
		Last Modified: Thu, 22 Jul 2021 02:18:16 GMT  
		Size: 50.1 MB (50111961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab786a921ccb7c1afe30eca6993da354114a957337287d819030ab934e693711`  
		Last Modified: Thu, 22 Jul 2021 04:38:30 GMT  
		Size: 4.9 MB (4936974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d08ba7697666bbe33ab34e16c74f6a0e1e670f45c2a33f9f3205862bd88c74`  
		Last Modified: Thu, 22 Jul 2021 04:38:31 GMT  
		Size: 10.2 MB (10217393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d317888fa778790ee95eafb5aed1fdd97c57a5c4c046dca2a88c869fd8f2eb61`  
		Last Modified: Thu, 22 Jul 2021 04:39:19 GMT  
		Size: 50.9 MB (50926208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:13c60ada20f3435b18cafffed1bfa185e2b60cd75850edea8c525c6f86c91209
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (125032841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ce35a38432592dc56455e29db74e7845904d33c98fccebc18ad510afa2736e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:46 GMT
ADD file:a3549e948b3f56a447f7f9b8c10f86c1915a2f52c546e1e7891735ee86a647ee in / 
# Thu, 22 Jul 2021 00:40:47 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:17:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:17:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 01:17:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:62e8b52de22392fa7c459ae1bacaf43117fdae59adb2ad8b421412ace5a516b1`  
		Last Modified: Thu, 22 Jul 2021 00:47:01 GMT  
		Size: 53.6 MB (53593074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f26cc7a118272da0a6d22d8d2788a1a25d2f7e416cfda133a48219a5f1fced3`  
		Last Modified: Thu, 22 Jul 2021 01:26:21 GMT  
		Size: 5.2 MB (5159864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d208ca6539dbf6b41a01d767eb9b2904ee7a991935f60f061cd678987bc3b4d`  
		Last Modified: Thu, 22 Jul 2021 01:26:22 GMT  
		Size: 10.9 MB (10873259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8ab38b650bac84d69771a018e22df0bbc743711a43a0d444b551ac2aa10262`  
		Last Modified: Thu, 22 Jul 2021 01:26:46 GMT  
		Size: 55.4 MB (55406644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:04e0650bc727dd18f73c095ef5f35e238acfdbc963764c86f55dbd57a2817916
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129204520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3ac461708875960f1d5e7c484c1b60c5867b04bbdbb89494195e2999ae5c74`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:42:42 GMT
ADD file:8d9eb4b2afc4eb0058f4080c5f0eedf0ddef323f1cc5a0403658254d191f117e in / 
# Tue, 17 Aug 2021 01:42:42 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 02:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 02:02:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Aug 2021 02:02:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:79e62a40ce7bfbbe436e33c1da1c5661386b9674fe81402fdbfbb42a5b84998b`  
		Last Modified: Tue, 17 Aug 2021 01:52:55 GMT  
		Size: 56.0 MB (55967475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe3391f9add930caab1f7ad8d326db740aab914960a3522b2baea8f34b06d23`  
		Last Modified: Tue, 17 Aug 2021 02:11:30 GMT  
		Size: 5.3 MB (5301763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c1c03bbd7c2f8c23dd8b5a8bae89de98d00fe400f6f7c89140aed7a78c6aa7`  
		Last Modified: Tue, 17 Aug 2021 02:11:31 GMT  
		Size: 11.3 MB (11250490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71047ae47f0ad2d0279c1731200ffbae15c68839f662197eb53927e89f4a346a`  
		Last Modified: Tue, 17 Aug 2021 02:11:56 GMT  
		Size: 56.7 MB (56684792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:01dbe5850925eb9009c48ba896d743425d9eb54e88f88144a71fc452c7c68626
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123227419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107fda626c0b3057d97ce6567e702283ed54496419012afefbb061a4150505ee`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:10:12 GMT
ADD file:21823f99ac9631853baf61992ae48f9aaefd9aa14689bdad76945cbe790d4b23 in / 
# Thu, 22 Jul 2021 00:10:13 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 00:46:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 00:47:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 00:48:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b7674bbd759fec6741d7d94cfebb5e0cf54c599cb2a824313eb96b1d6622a44b`  
		Last Modified: Thu, 22 Jul 2021 00:16:59 GMT  
		Size: 53.2 MB (53162150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bbf92e62547174ba9022d0c0fe12fa84126289620f8148cf33269681b8273c`  
		Last Modified: Thu, 22 Jul 2021 00:57:29 GMT  
		Size: 5.1 MB (5130754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2614779dff3229eb62dc8a974d88a9bf60cfd085721871ad71d642e0517eb35`  
		Last Modified: Thu, 22 Jul 2021 00:57:31 GMT  
		Size: 10.9 MB (10873093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100254d07ca9795fcf9cb6c9e7d187591a97a9ac79c2b0c7c4351c8e7c1f30a8`  
		Last Modified: Thu, 22 Jul 2021 00:58:21 GMT  
		Size: 54.1 MB (54061422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3f8769eee4695a61ad3940a4c1a1333f1a953ad60dd3dc77428aa8a3e565cc43
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135526176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b610da6bb9e2031c67db7105a6676fd68e0690fc594a692cafd6625ad3b44a1e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:33 GMT
ADD file:d5172916465206276bfc66e1d963768fd3cda811ba961e86fdbc4b49f0a72dfc in / 
# Thu, 22 Jul 2021 00:19:40 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:19:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 04:20:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 04:22:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bb31d3e4dd3826fb7298bcca3375efce01b08c74be37a5494cb4eaccd247d8e9`  
		Last Modified: Thu, 22 Jul 2021 00:28:17 GMT  
		Size: 58.8 MB (58810717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6ede8e70912b2a939d88a27d547a381f612b6c792d57e726d55e899c3866ec`  
		Last Modified: Thu, 22 Jul 2021 05:18:34 GMT  
		Size: 5.4 MB (5421821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18b90280541d7eb6e7e1d27889a4b6e4dc571eb851a0b49f6da40e06522687e`  
		Last Modified: Thu, 22 Jul 2021 05:18:32 GMT  
		Size: 11.6 MB (11626277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96af94f2c600d7f45682dfda0d3faa954448e1b45034e2ccc980c66372c03c36`  
		Last Modified: Thu, 22 Jul 2021 05:19:52 GMT  
		Size: 59.7 MB (59667361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:166bf7d50f030e28673f716d264394736ae50f21f1fe8eae978b234f83533d64
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117045462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2201b968f83c8036d3d48fbd162d3df810afcef6b73112a781311ea8a4d046ca`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:15:18 GMT
ADD file:b4e98baa24988a55379e3fdf724731b1139785071c1e2ca5d8e5adb43be85150 in / 
# Thu, 22 Jul 2021 00:15:21 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:01:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:02:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 01:07:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f89739902ab20ca21252189bdcfa682d2d8fa5c61d2bb714fe2fa6f3a5c519eb`  
		Last Modified: Thu, 22 Jul 2021 00:34:31 GMT  
		Size: 50.4 MB (50397728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfc4d529e1e9e4423209e8cd25e27a2a6f2936444c4aefe731dff4f2182309a`  
		Last Modified: Thu, 22 Jul 2021 01:24:42 GMT  
		Size: 5.0 MB (4984778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31856dffc5e9c49615c1b03c06dd7711260172bc519c1d48536e27cbf15fadc3`  
		Last Modified: Thu, 22 Jul 2021 01:24:46 GMT  
		Size: 10.3 MB (10293785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a92ee8d3a71206345072e79dd2dbc21375b2232df7d85161732f650f4427f1f`  
		Last Modified: Thu, 22 Jul 2021 01:27:18 GMT  
		Size: 51.4 MB (51369171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:60b691392eb70c4585f3aa02bdcc5a3ad1f9286c0be43a17aa4dd396470e2de4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123819445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1947dfd41d6be6ee2b6088cdcf029beebd1f807533e35dd1eba6818b395fa21`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:43:01 GMT
ADD file:eb0fa0f991634817ac5af2d4e957d8d14c8fb5a8d501cfeb56949d715ca84f1c in / 
# Thu, 22 Jul 2021 00:43:08 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:16:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 01:18:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:730f0cea2dc4896e7a1a70e4e4e14165f66e42bcd880b7b7242a68c9d2ffa297`  
		Last Modified: Thu, 22 Jul 2021 00:48:31 GMT  
		Size: 53.2 MB (53187330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7d1fd11d3f6b43667d4ca70d209f8ae22c2e40a78c9c810ae7a0f944c04b98`  
		Last Modified: Thu, 22 Jul 2021 01:28:41 GMT  
		Size: 5.2 MB (5152875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082a8f611511094fa5cccaf153c7a6dd4dde6a330473614087e039fa44ca58fe`  
		Last Modified: Thu, 22 Jul 2021 01:28:42 GMT  
		Size: 10.8 MB (10763675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420f67b72350ece22438f02a25c08026b757f5fc506536df3d9d0b2b294c37a1`  
		Last Modified: Thu, 22 Jul 2021 01:29:02 GMT  
		Size: 54.7 MB (54715565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

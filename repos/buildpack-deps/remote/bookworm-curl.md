## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:077631be0fa5cd79a1da3c7e9c40798944d53d8cf5363c96059ca3082f367ad8
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

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6e933552414fa5eb22411f8158e2436a3c469b81e4f70ff61e62dbe3735a68fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72211131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116f59cf3a0529f2503e3c3c5f5497e47ce1d3f447f2d28b532bbdaa9ead3361`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:22 GMT
ADD file:2a92eda55857403475e71c7e72e14b8332b700683b753b80998c67de8059b01b in / 
# Thu, 17 Mar 2022 04:03:23 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:27:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:27:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:66fb1aabb4c03c1a8502c7ab4d442a4602f465cee7eccf27eb706178ce2859a6`  
		Last Modified: Thu, 17 Mar 2022 04:08:59 GMT  
		Size: 55.8 MB (55754297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeea17ea14a09712ca5b490a0c64f57af435ba10cdb9a1a7c56af17b85ac9361`  
		Last Modified: Fri, 18 Mar 2022 07:01:56 GMT  
		Size: 5.3 MB (5270513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72b20718d5e8e4adb64ab4e1a41c30a4e311400c1e600e19792c50c1522420f`  
		Last Modified: Fri, 18 Mar 2022 07:01:57 GMT  
		Size: 11.2 MB (11186321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:558bd2df00fefadc20c80b2c2eb8636b28d7b74a3bbf8801a6df8d444997a1c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68887503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7cddb5b60b02cc4c9dc64eba7422c3844ebe5abc88c9235019a4f00cb7b4ef`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:18:12 GMT
ADD file:990567084063731033d76e2ad1efcd558f47300ad1e9848197a4365f45d534b5 in / 
# Thu, 17 Mar 2022 05:18:13 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:11:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e5c18c3be596e08b764befc1ff336d017f3a31c10bf139ca155094240de76a8c`  
		Last Modified: Thu, 17 Mar 2022 05:32:53 GMT  
		Size: 53.1 MB (53139012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0040329b3b511cc0d15a0ae2eb2bbcd344c2c8291532ddd0f333b1e142b464`  
		Last Modified: Thu, 17 Mar 2022 19:37:02 GMT  
		Size: 5.2 MB (5169031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c800c571bbaa0a9c8eae64db9691f97d467f0bd06250b5da62e182b97753f497`  
		Last Modified: Thu, 17 Mar 2022 19:37:04 GMT  
		Size: 10.6 MB (10579460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:83d0e2b46c70a52e95a07c807f96a53d8dea413470b8b193cbced35050dd9f55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66064217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e3425ae1ece84a216e81a7922d8246d14921d90909616b7d4032a46730d888`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:01:09 GMT
ADD file:b4dba23a3881b51ce93a5fac275db003c57e88fc4534625e4c57917ee7d15dad in / 
# Tue, 01 Mar 2022 02:01:10 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:23:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:bac975da179fd2ec964b1f0a2374ae27456aefbe28014e1301872aaa7a545619`  
		Last Modified: Tue, 01 Mar 2022 02:17:11 GMT  
		Size: 50.8 MB (50787576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1c6337247740872b2c547fe2c235240cb511f34f377358193108cc09d66ea1`  
		Last Modified: Tue, 01 Mar 2022 09:48:05 GMT  
		Size: 5.0 MB (5035170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1747c607a3fe8511a51023b984fd817a06b714e0a09c5028257ed90eebc47b0f`  
		Last Modified: Tue, 01 Mar 2022 09:48:06 GMT  
		Size: 10.2 MB (10241471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:13403d3678b00575bc759149f4be7e073db208614846ce3c89476f3fed441b64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70601436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8c3eeb044bcfc63ccecb68626130cb108ca71731e3f231ca7f615652f3e62f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:18 GMT
ADD file:c8087b65b6b61e4854699fe41f5bd7f307c0e0710204b586e85fd8176523d9bb in / 
# Thu, 17 Mar 2022 03:21:19 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:08:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:08:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:906df7cbb9fee5eb5d79c51ae55b6a857335ddd1b44645e3a59b3a50862f4317`  
		Last Modified: Thu, 17 Mar 2022 03:27:23 GMT  
		Size: 54.7 MB (54668239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2bee854a2c1d4d436485263d8648a3eb5c0a4cdc26326102c680903b409889d`  
		Last Modified: Thu, 17 Mar 2022 22:19:48 GMT  
		Size: 5.3 MB (5256412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f88519bd8fe148fde1d5a9917fbea41afdd523e19fcecf2dc8f2f39c86cfbe`  
		Last Modified: Thu, 17 Mar 2022 22:19:49 GMT  
		Size: 10.7 MB (10676785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5017ad435aafdcf2ea872f2515fa180db4832f9e77dd4f8e5e5adbe1e2a99598
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73515014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845963f985308db7a4d7847da6d5da11fdecc643b2a303d445c0d258afc60a2d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:06:44 GMT
ADD file:2e2ec9677737b8bd29e3af438e4f72a00e4024d7771df47c835bc532f3955901 in / 
# Tue, 01 Mar 2022 02:06:44 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:39:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:39:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:86f9569b4496bcb71f9a06eca983db008f228f89df9115b51deb7ba67bce86ba`  
		Last Modified: Tue, 01 Mar 2022 02:14:26 GMT  
		Size: 56.8 MB (56800248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc642b9c58ccfd6d24ba39de754790979cb5f4259049a1024063ce9ecd8048b3`  
		Last Modified: Tue, 01 Mar 2022 05:50:18 GMT  
		Size: 5.4 MB (5407350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03eabfe59d42c8a3ee934b6d80db7f1185e56951d5ec5a9561133731b6ff2d`  
		Last Modified: Tue, 01 Mar 2022 05:50:19 GMT  
		Size: 11.3 MB (11307416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6c26b63853717627ee2afe3c6fd3ca33f6f613b6fbd08d35bbece743caf1e828
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70219099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e392fa48047c7641d289f83d6ff6f2d4fadcb59b0dd64ae09808891888402f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:51:08 GMT
ADD file:550d1d8a058f07f217e9d0ec1e582f897b1cd24ad6c6c3697d5c89039c5ae265 in / 
# Thu, 17 Mar 2022 08:51:13 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:10:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:11:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f4e5d74924161483e853a5bf08fcf297bf47b3124d7d1840e280c5f487a8750d`  
		Last Modified: Thu, 17 Mar 2022 10:41:21 GMT  
		Size: 54.3 MB (54339160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88c2306400a47802f9098940358dd510c9d432998ff5d8b9ef4eb54da37c1b1`  
		Last Modified: Thu, 17 Mar 2022 19:47:35 GMT  
		Size: 5.2 MB (5225142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894a35eaaf609861da62a9d25299ce8269925d4e205b08c5c62d7e99d19b7d6f`  
		Last Modified: Thu, 17 Mar 2022 19:47:38 GMT  
		Size: 10.7 MB (10654797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:da70962bf15d882b191030ec80881350c1da32d06e1d77f2cbf4a370ab1762eb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77403099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ede6fa2ede1b0333e211d7142ad3fb81a01a889860679f4bf08bd27b189e43`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:03:22 GMT
ADD file:08a06b615cc3142b45e95ffc03be0940c1aed49581fdb5c3a45d69c9ba65fcdf in / 
# Tue, 01 Mar 2022 02:03:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:54:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:55:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e0578def7e304114d931a4e4be85f40364b30cf0228e8360d7ec9d82b30f2519`  
		Last Modified: Tue, 01 Mar 2022 02:13:53 GMT  
		Size: 60.2 MB (60166365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb379d336c1a24b02d5693d3a19fe1017d67c67f734a56c109c876bcf8547f99`  
		Last Modified: Tue, 01 Mar 2022 07:40:40 GMT  
		Size: 5.5 MB (5543531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a933c5a043de953ab3d5444edf590034fecf2a41084159c2ff91dcb57e349a89`  
		Last Modified: Tue, 01 Mar 2022 07:40:41 GMT  
		Size: 11.7 MB (11693203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:921e730e8c3a0d9d32ab4dfc25e429dbda5edc93aa022224097b3a2bc7d3a3a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70054989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6b42801d69d07fdb4e1459d7e8891ac86f73b75630edd74959132a017ac1e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:02 GMT
ADD file:82d5e48a017e9f867dce69500059071538b25dc5395a355bb79bfed992fb8cab in / 
# Thu, 17 Mar 2022 03:06:09 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 18:19:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:19:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:91cc6fa8b00e7facc9855a15de9dbb6211a8692978d893a028e487ca7988379b`  
		Last Modified: Thu, 17 Mar 2022 03:11:59 GMT  
		Size: 54.0 MB (54000921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2c6272c85978c4b20b105a7a33a11881628bc38840c72128a526cdc6b709ab`  
		Last Modified: Thu, 17 Mar 2022 18:28:20 GMT  
		Size: 5.3 MB (5250449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900da87743fe44ae1fee0a700fae42c07e9ade18d95f98fbace40ab318fb4846`  
		Last Modified: Thu, 17 Mar 2022 18:28:20 GMT  
		Size: 10.8 MB (10803619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

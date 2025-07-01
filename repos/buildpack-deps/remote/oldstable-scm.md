## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:5ec85029bd4fe5ef5489066f76682645ec80f5328246b7042cd414853af1bf5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:157a5c2b2c27a9943044a8d1fe723e84b565aee19d031cc9cecc40d1ccd22021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124277284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2833c60b2946c87a62bf2138b86b2ec9f5c62f451c53280cbac15703f0c8c42b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8156a957a8b63a670ed89130a2e1eedf5c1b2a939f33a952c4159b4ebcb0a`  
		Last Modified: Tue, 10 Jun 2025 23:36:44 GMT  
		Size: 15.8 MB (15765139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2678613884c2f141cc551880b1a1587f0c890606a900bbac5a1ace2645be657`  
		Last Modified: Wed, 11 Jun 2025 00:02:35 GMT  
		Size: 54.8 MB (54757363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:706fdd672b6cb999ec92a12f25cb3114866c9b870078fe40e9676a8cac0766ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7919507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbdd539318f99cb048f9e98b1cde3e1b06fbefc4a72861a36cee2f6cdc32480`

```dockerfile
```

-	Layers:
	-	`sha256:3253d0380a032a91694936873111d677837ae54c3e17b2fe6755866d3519c9b4`  
		Last Modified: Wed, 11 Jun 2025 02:24:07 GMT  
		Size: 7.9 MB (7912154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6765477cfae51e013d272da62e4b6fad14fe476118d2739be53c2dc3ad045f9`  
		Last Modified: Wed, 11 Jun 2025 02:24:09 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c0f8634c933cc6878adf71bd775d7530be333997e6f50fadc713f71a8de04a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114555450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d2cb0e000ae8cc2ea5a3d2fcac740e1e1db33fcaf3557ed51f29ad1afe2c1f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c43258def9bd93af20e1c5bd4e42a71d9db281a9fc468bbb5eb78d7a51c6472a`  
		Last Modified: Tue, 10 Jun 2025 22:47:56 GMT  
		Size: 49.0 MB (49043954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319bc9ba38020b34f4e3f562e110c9ab25e658493eaf95bfc783a633f2d4b036`  
		Last Modified: Wed, 11 Jun 2025 20:11:47 GMT  
		Size: 14.9 MB (14880672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc07acb5bb3458d1880be716fdb2bcc90e78327b21f1c1531b5e4bd0941213a8`  
		Last Modified: Wed, 11 Jun 2025 13:12:55 GMT  
		Size: 50.6 MB (50630824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:975b5dc0f313db78b4700c125c0bc5031070ed7046824deb20c4e50fba9468b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7922761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b611eadac0e6390cf7b0fb58d2c9337d65fb482ad525ae9ee75e94412490909f`

```dockerfile
```

-	Layers:
	-	`sha256:6e8e888e3970493013233cc25ad2c1143751409c73be13388f67386f1a3b8c73`  
		Last Modified: Wed, 11 Jun 2025 16:19:59 GMT  
		Size: 7.9 MB (7915348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f665dab8bb1ebdcdd1800e92d1cccff808d17441fdd68ab869b7420b1528b24`  
		Last Modified: Wed, 11 Jun 2025 16:20:00 GMT  
		Size: 7.4 KB (7413 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:daac85694546dab3d4080c79bf955e579a18c88bc91fa83c961b02564232d54d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122855949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be572007a58aa22332ec3de721781bd0a28004e84d5a0911508dbba7f6ee769b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6f3b6fbce84c42871ea80f05b2c61e622e08647f7164e9a95a391926c1f714`  
		Last Modified: Wed, 11 Jun 2025 02:56:50 GMT  
		Size: 15.8 MB (15750566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7850095446c84fa9107622e378378aa7daf4b928caeecbc1149118900d32f7`  
		Last Modified: Wed, 11 Jun 2025 10:33:17 GMT  
		Size: 54.9 MB (54853082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8260c4cfb4f8e8bc29fddedac2ac08dc929808d81f6298be2fc35ad2b00ab0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7925321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ca814aee9b0859b92a60bd0a408b83c3f68289ed31ede7cde41dee851af995`

```dockerfile
```

-	Layers:
	-	`sha256:99380feed88f956fd4322ad73b31a7332383eb0e8201dbd0560a856ee47b7eba`  
		Last Modified: Wed, 11 Jun 2025 13:20:02 GMT  
		Size: 7.9 MB (7917888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b62e70a2d103944dfd8b7a67087ac8d32e7eeca303570c7850bfed1e6e7b7e50`  
		Last Modified: Wed, 11 Jun 2025 13:20:03 GMT  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fdba36a14921d17a845cfec8cfcf5c82b994fae5f1a24834a371176e4dd0cfe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127008778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bc9481776b6063f6cfde157fe7d571ba1121034d475dc45de748d219d81393`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113be81052ec8e8323c4db158dc9c99295355934e950a6367e5c27038fd1e04c`  
		Last Modified: Tue, 01 Jul 2025 02:24:43 GMT  
		Size: 16.3 MB (16268907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05b439f6df174e28bd21dc59eead603def3bcbd47ec6462f86b7758c4db6ef`  
		Last Modified: Tue, 01 Jul 2025 03:19:57 GMT  
		Size: 56.0 MB (56049937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d006d5e7d71524b98b0c95b15930436f551b2be990b9a7bfc0f38b0557ba7d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe60979650c1cddf1356d6ce18c2786636be1316d989dc23e5cb87fd8a5c45cb`

```dockerfile
```

-	Layers:
	-	`sha256:a7bc53c81442fdb75119ba97e93d5ae4028d8a5162adb5864344f5c725ae5451`  
		Last Modified: Tue, 01 Jul 2025 04:20:26 GMT  
		Size: 7.9 MB (7907724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33cce3240cb0fb879e74ab783416e16790d07f344d8061f791abc1de4bd88bbc`  
		Last Modified: Tue, 01 Jul 2025 04:20:27 GMT  
		Size: 7.3 KB (7331 bytes)  
		MIME: application/vnd.in-toto+json

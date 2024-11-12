## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:234ad1de0c6bd8ae1024516f64646becce5040299546d61dce815cb7ec74454d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6fbde97d2c5f38678ecc77dba69ae37004e01c5fe1060195a6fa0a03a166b6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138025417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408d444d56480b9093884d1bd6088cbd039fc990d5bf1507bd57a0e13bdd3a33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d933d77fc474f2f63922bf70e05b7ea0af809991a3e5cb05967accda9f937dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5efb1b53407bad0cf8f47b0a1d54a6a9e90a27ae1c86a6a6de8f9bb3c8cc85c3`

```dockerfile
```

-	Layers:
	-	`sha256:b6f4689c52467b37f8370b7c0f6ac7fb405ab637e983b4ad7353590dd0a8a2cc`  
		Last Modified: Tue, 12 Nov 2024 03:58:27 GMT  
		Size: 7.8 MB (7764442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91abd18c81a94564d4a7151834429ae9fbf19f28c3a4e2937046f1a765ce3039`  
		Last Modified: Tue, 12 Nov 2024 03:58:27 GMT  
		Size: 7.7 KB (7654 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9a1f00aee35fdbfc3bbef35f7b430afe4b7d61335911b8ca883d4ee277540158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132068934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28e47e232c9eb35167cfd394f5c0f26dd9550bca5ee8ac3a7fb762992cd8e96`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:895d07844c9c09054971f530ffd0794c329a785344079a01ce24e3d51727407e`  
		Last Modified: Tue, 12 Nov 2024 00:54:43 GMT  
		Size: 47.3 MB (47338750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efb128382700f7090be7bec74d12308eb11ced11717aae4403b7bccde20f24`  
		Last Modified: Tue, 12 Nov 2024 06:28:08 GMT  
		Size: 22.7 MB (22733304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5d34c31582cec80127fc538f65a56104fac2a20c87dbcaafc70b88f7a0a8b7`  
		Last Modified: Tue, 12 Nov 2024 11:29:42 GMT  
		Size: 62.0 MB (61996880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:146afff14da66d2415f7e870a0b5475327d3b8c5c3012e0e73e9929ce55432aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1139b21f47128807aca40d8f91d82ce8acf1684a9f67bba7bd10747e93444a31`

```dockerfile
```

-	Layers:
	-	`sha256:e5dc3d0311f5fe151c6c570f37bed7153cdc58ca55dc3f8244a7b0463ad6f4b5`  
		Last Modified: Tue, 12 Nov 2024 11:29:41 GMT  
		Size: 7.8 MB (7765996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3878cd87f19cd6baf6f4baacf94bb729da9783cc7ba94a83e2575efb914f143`  
		Last Modified: Tue, 12 Nov 2024 11:29:40 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d8da1a84da0bff207409bbac38dd1a02df0945b14ffd1fa2e34036a968789458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126740448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11391af0d1d3a25dfc5836b449c838b6faf132d3b8f3207da24d749b265ef353`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f68420f2ab6efd74aba4b4ff72fe115144308ecea01703acfd9de4db386df`  
		Last Modified: Sat, 19 Oct 2024 06:36:59 GMT  
		Size: 59.6 MB (59635104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:82abbe189e4134358a35de062d14a33ab4ef2350f5335ed22d488f490c39e3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a185c3d89851dea1a6599e78d946fb300c3e2ee6fe011b211285a182fc5e834`

```dockerfile
```

-	Layers:
	-	`sha256:f581eedd8301e57f012174ed44c98b695ef71465963ae45671ac92102a1eaafe`  
		Last Modified: Sat, 19 Oct 2024 06:36:58 GMT  
		Size: 7.8 MB (7765651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcf5b6a5be36ea85b8ff05143189e2f676d385b38504343c20e9f59dc37a002e`  
		Last Modified: Sat, 19 Oct 2024 06:36:57 GMT  
		Size: 7.7 KB (7735 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1b238ddfffd81f1788a7575612d8a052bad65a59129adf13b225091a1f798575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137528856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89ba4d07f4ae3ae3debaa56c19ea06e7c0b9d2773c56679e3399263fadd9488`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4ae890e89350690ad59722f03f334f49def59e9a7a1b4eb60f59e60964f978fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ce0978485db8f8cd9635afd0ac7fc48b931593fe09f24a19d60b0d76c4e639`

```dockerfile
```

-	Layers:
	-	`sha256:5be58f0330ad5ad6c6e1439539fff91b3e586695d4806db0cf17398a4ea80ff7`  
		Last Modified: Sat, 19 Oct 2024 05:17:14 GMT  
		Size: 7.8 MB (7770781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd7d4cdd0c303535f95e2806de4f42d422c025d70f90f72882a1301f380aa64`  
		Last Modified: Sat, 19 Oct 2024 05:17:13 GMT  
		Size: 7.8 KB (7759 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3a9a1cd1d4fc50ae45994fcf166dd95bd945fddb91781ffb82b09f84b8d70daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141687762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de9bf2a38fcbf043555508c597839677889c027dfa88e84f35a66f1493b14a2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46592415d8ae65247d6cff038217c0ae0c38f5f2fee88eaa3f5ae09743a290`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 66.2 MB (66211304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d29c3a56480553061917153ef4826fea0ff6b84616cfc7a020c1682e578f5c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a9925b36e8fa4b0eddfc89cf9f299ae4e6da2ab487e270d5483829a67266f7`

```dockerfile
```

-	Layers:
	-	`sha256:21211546a412a59b68e54a0883d6e64098cc26325b2fac0f05cf5b94ab27c266`  
		Last Modified: Tue, 12 Nov 2024 03:14:22 GMT  
		Size: 7.8 MB (7760518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac6f9f590da617c7f5124adbdf5cc841c3d0456606c3d5617a33a51ecf792f53`  
		Last Modified: Tue, 12 Nov 2024 03:14:21 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cadf76ca0578af7d2c32dce3d1860f04b28959bb1cb0f27e982288bba02c972e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136494026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0434755538859a36858a1cf943ffb9a3464378e9371f90644cb583fdfeefe551`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba3cc6e574320e30c42f84b70c8e03fff0393ea65f20833b10b3a8aa1415e1`  
		Last Modified: Sat, 19 Oct 2024 00:56:12 GMT  
		Size: 23.6 MB (23648020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d702889c46052954a44f8b6ab39510d9b55acfe4a180194a7cb475c90b2b76e`  
		Last Modified: Sat, 19 Oct 2024 02:08:09 GMT  
		Size: 63.3 MB (63284387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:821b714bf8d6778d6d1b920a2baace275ae17c38d2e45770d4702d64b3d8634a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae759b8a8a22e7725a44091355ef141327e65f7a7442e018dfb5b90b94cf0cce`

```dockerfile
```

-	Layers:
	-	`sha256:7bab8cd7f7cc5b0a4b903dd7d23a799c7767e8dec89874cd1de2cc7ac2343c85`  
		Last Modified: Sat, 19 Oct 2024 02:08:03 GMT  
		Size: 7.5 KB (7509 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4a4289d5bc6db05198984f4e81697f55cc0d7ac6720bdcbdb13af2b5b385c231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149085096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3875cb156e725ad37ee97b98abf0f972f2ac10c4ff305204b30071a468158a4f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913acd64029d37b20e9e161bb8659516cb78a99cfd56eb921fc4ccd76ae7c0c7`  
		Last Modified: Tue, 12 Nov 2024 16:09:31 GMT  
		Size: 69.8 MB (69812283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c21374c30e5f547aa9e66b04b1997909f699921da61d213ed3fb3d2a7de64c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7779842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a315c2156e595de5e483e597dd3ea85ea0533d0e98f410011d7326f27679968f`

```dockerfile
```

-	Layers:
	-	`sha256:d9c5acd4f7b46ec0c9c2839752d6be8030b1bcc4d58b67483ad71a717d9899cb`  
		Last Modified: Tue, 12 Nov 2024 16:09:28 GMT  
		Size: 7.8 MB (7772149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1014f338054fa217964a7cd584f29304bb70ac47f3c759f554c010e2b966ee4`  
		Last Modified: Tue, 12 Nov 2024 16:09:27 GMT  
		Size: 7.7 KB (7693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:029bcbdc4d92b810548bb6fe4d4a5d4fed99197e43c6a7cf1366a8d78db2c8fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135483424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ab4b43343266a1cc583fb48be5a34866624b123c7e48c1a091011da24be0f2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a99db1e4eb0a57b7be4b1376a7fdf886d4118a6263595ad414d052eb69ee9b4`  
		Last Modified: Sat, 19 Oct 2024 03:46:26 GMT  
		Size: 63.5 MB (63494580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ecf9164fa7d6fe0f7178e89f1831c99d40d886c359e875262bf5d2f7fedb45bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8b973ea0fea3dbb11fa12a9b53632b91fca04c49806d2caf99693e37c78d69`

```dockerfile
```

-	Layers:
	-	`sha256:6e7b6cf839452bb8901601f821aa42480d98fc226c60373c907ff55920f3d325`  
		Last Modified: Sat, 19 Oct 2024 03:46:25 GMT  
		Size: 7.8 MB (7763576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ad6de2140fc403088cce711e23a06bd50be647583ddfcdda8b53b2134309157`  
		Last Modified: Sat, 19 Oct 2024 03:46:25 GMT  
		Size: 7.7 KB (7667 bytes)  
		MIME: application/vnd.in-toto+json

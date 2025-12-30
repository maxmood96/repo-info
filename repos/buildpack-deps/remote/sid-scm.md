## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:355856339714c6fd1d0b8926a1cde3d8c033fa3558eb04a98eaf63fb2c697e04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9a6c04c7e2e559dc70d9e7560f543adc612ac608c7438207ead16b7d78f43bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144419242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3adddaedaebb2ea520ddcca42322e544825123aea041e41256fdfb258904755`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1766966400'
# Mon, 29 Dec 2025 23:46:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:36a4985327850927961426bc6fcb1fb8dc1f9b5e7f69f8061c7daf2f4aee58a7`  
		Last Modified: Mon, 29 Dec 2025 22:29:41 GMT  
		Size: 48.8 MB (48821118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff00e9a4f0fade15b203525aaff92a3d5f8f8fc08fd83188ea3896aee735cf9`  
		Last Modified: Mon, 29 Dec 2025 23:46:39 GMT  
		Size: 27.2 MB (27163941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65cc8637f491021b1a5b654de24c9952c1a34d6f439d5276b217858ffb0cbedd`  
		Last Modified: Tue, 30 Dec 2025 01:24:03 GMT  
		Size: 68.4 MB (68434183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cf412ae0ecad64d0ea78f1c35c88878324a197132f3546ab9386e8c8fb2c1c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56adae585526f9d9fc90e8693340e680b8c614aa6b3ac5a6b74d9df6730b1c63`

```dockerfile
```

-	Layers:
	-	`sha256:cc3f6c195d49296950abdb39143c776d8ef814a3bb852b864f9a19b6aeded14c`  
		Last Modified: Tue, 30 Dec 2025 05:23:16 GMT  
		Size: 7.8 MB (7764995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd5c5e6680913b3918bbe626d96bfebc20bdf7ec29eb84ae78eef9b03458b321`  
		Last Modified: Tue, 30 Dec 2025 05:23:16 GMT  
		Size: 7.3 KB (7254 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6f89cdfb4b2a6ca3ed1fcc3c486c87483eac3b363529b829682262ff86f29a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133324475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece683554b52228353b782d0d9dd39befc0b30f3bba79b00e54c46461a95c1f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 00:35:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:07:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fa37dcda97874915e8cdcc90ad670632c868d75ea88f3d100f667fda60d8b657`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 45.1 MB (45112498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4476f3007fecd22f80f4b20b480cc2969ce90429f8c85967f8e864a1ea4ea7`  
		Last Modified: Tue, 30 Dec 2025 00:35:29 GMT  
		Size: 24.9 MB (24876058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e43ff0df27ddbb7e584554f19ccd47c0d42c490cd66902adb1e4ef8c438b50`  
		Last Modified: Tue, 30 Dec 2025 02:07:49 GMT  
		Size: 63.3 MB (63335919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b2f9ec8a478e275b47ee7dc14695b06221a7ce4ae6d6a2f1bf00d146b3207126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7617a53d50d9b688d91f32b10d336e2c140915abae4a4bc6c86d7db7f443047c`

```dockerfile
```

-	Layers:
	-	`sha256:deb631f809ca092d3e2929e0ed72b3576c533be56dea52726cbca833c4f69251`  
		Last Modified: Tue, 30 Dec 2025 05:23:23 GMT  
		Size: 7.8 MB (7765494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:016094b9628ed0cb91b5a06a27c556d9bd31bde6cd61cc7a81b3deea5b7fbf94`  
		Last Modified: Tue, 30 Dec 2025 05:23:24 GMT  
		Size: 7.3 KB (7318 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:291c7d216675b8e6078e6fd1f9d59f8cb4ba65490f06b187d9f3f27ccccde14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143397193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e90fa28671be68d88fd55e2fc043b5fa2f1be927014a90db590c27a4d04142`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e81a19d37d9900498b0ca8a841e2e3fe3dfde06146f7d10d1e71e1df7a8ae8ab`  
		Last Modified: Mon, 29 Dec 2025 22:29:24 GMT  
		Size: 48.8 MB (48801029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ee77a5614dc66e1139efb80cfe733dbde2b288b1202ba35c49e9a008fab1f1`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 26.5 MB (26450657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fd72cff7703be5b505c0f450c68a28d0e97b7ea4b0af0d5b1b9aa834492080`  
		Last Modified: Tue, 30 Dec 2025 01:26:07 GMT  
		Size: 68.1 MB (68145507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c2df92adf9fb3e9cb175f891be88c6b2af815e1c710b70cecf7ac3c8374d975f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7779354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10b7688d2b065002cd2b579e90b2730cce38bdaa005a2aebc3a3a74cc9e345b`

```dockerfile
```

-	Layers:
	-	`sha256:c786b15e0d835f7954cbb24756c309acb3be6e9c54ce288f6fda266ffc9e1ae4`  
		Last Modified: Tue, 30 Dec 2025 05:23:31 GMT  
		Size: 7.8 MB (7772020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b42fd79ad472b7c4ef83315ed15f52147ff157edeb08be46de97e81441f6b52`  
		Last Modified: Tue, 30 Dec 2025 05:23:32 GMT  
		Size: 7.3 KB (7334 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e4fea4d6acb52667f7ab5a1995e5eb87f7867a0f1078b3e6a66e3c64fda120d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148755025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a3d18f37951f4fa8b5826c9165415777acd4fc890d6f2f70eed90965ffd6a8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1766966400'
# Mon, 29 Dec 2025 23:47:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:33:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f17a69092f61f8d721afcb2893fe3fd9f89bff73ba6442fc317604ef6ed50dce`  
		Last Modified: Mon, 29 Dec 2025 22:26:26 GMT  
		Size: 49.9 MB (49939146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217ad4932c84f70ed9491cf091cd8265fbcd5562d33475dc1380251ed82c8c60`  
		Last Modified: Mon, 29 Dec 2025 23:47:38 GMT  
		Size: 28.4 MB (28407813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4886d5c61711ec5b4b405d5f907882fc1f09575f0c9a0648a6cd1812bdd985f1`  
		Last Modified: Tue, 30 Dec 2025 00:34:24 GMT  
		Size: 70.4 MB (70408066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:405b8c94602678d8f3b57128597fe15c714a82748dac48bc9677250b8ce32f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9386cf7e06ed1ee71803454b2ec9c7e84355d257133fe512a03c9bdafb90003f`

```dockerfile
```

-	Layers:
	-	`sha256:487691bba939af5c8238c6f5a75a2dca830626506fb2640de0fcbc142ec65896`  
		Last Modified: Tue, 30 Dec 2025 05:23:39 GMT  
		Size: 7.8 MB (7761136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01a581a25b34bccb9c38c6a82b2983c4ff2edbb1d5986102b4e1ab25e0274b0b`  
		Last Modified: Tue, 30 Dec 2025 05:23:40 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e0ff53c3f807889b5a28e9ae65c38fb7b4dda955e797971d74e7232592132911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156300372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133d0da785a92a06bde6cec06816ef1e95f9b320dfa81d9f81a85395bb7fa286`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:22:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:91f19749139bb2193587558635e0a320b0f29835fa1325bcb8c73b48ad8b72df`  
		Last Modified: Mon, 08 Dec 2025 22:50:49 GMT  
		Size: 53.5 MB (53494424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a82bf53318ee9ff50934cd5a455b97b8549b92db55df72cf410249ca6112c7`  
		Last Modified: Mon, 08 Dec 2025 23:23:07 GMT  
		Size: 28.9 MB (28884607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03e0f90ac822b83290c4938a8d44e3bfd579a2891eac5e11b8dec4f3a80cf68`  
		Last Modified: Tue, 09 Dec 2025 02:11:35 GMT  
		Size: 73.9 MB (73921341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:da8eaecb02afb86ed4776ac879c2afdc4d0d5e7ac54a0e211f5255cbb570cb1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7781482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf2b2813fd2508cee53489d7c5150dd30f629d7a61d2460b520818e6bb8a133`

```dockerfile
```

-	Layers:
	-	`sha256:05ff2f047cffa4b6ce0b062d3fb5b3b640783d4c60b453636674b0145c3ec6e9`  
		Last Modified: Tue, 09 Dec 2025 05:22:28 GMT  
		Size: 7.8 MB (7774196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58cf7ba0c983a220bcc3ff6620e342bc4bbad99c28791ab40942955ba05907a4`  
		Last Modified: Tue, 09 Dec 2025 05:22:29 GMT  
		Size: 7.3 KB (7286 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:053b1dfc126481e5d725d600168c18abc0a939baffab6aee3edbee52dd5e771e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140564449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114580fc7d172397f566cf45872f1b986da29c7f523350051b7a98b2f15982fd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1765152000'
# Thu, 11 Dec 2025 08:35:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Dec 2025 08:40:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:109a9388fb2c93203e12f30aeaef237cc88f26bdfe719e6c75ba4b856571d621`  
		Last Modified: Tue, 09 Dec 2025 01:53:48 GMT  
		Size: 46.9 MB (46917024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c6713d289f87fadfcb1cc49dc5c1255a2e68dec8f35d177d80c213c8c3d375`  
		Last Modified: Thu, 11 Dec 2025 08:37:29 GMT  
		Size: 26.4 MB (26413809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3a6f1c36dc6239a02beb52306b77dfb11edb7a5a71763ffc22541d84875bb0`  
		Last Modified: Sun, 14 Dec 2025 08:44:39 GMT  
		Size: 67.2 MB (67233616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:901c5110763d511343a8b974ee06e4a2b9eb265733ad651c2a4eb90c81dc9f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7758496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002dbde31a99e8f49c3416b0527616e4a69537c884d643b232709f127dd4cb83`

```dockerfile
```

-	Layers:
	-	`sha256:3af57aada69d51dc50f1466a7640291a87e2ff2dd97821c37b95fe90488a6bdb`  
		Last Modified: Sun, 14 Dec 2025 11:20:45 GMT  
		Size: 7.8 MB (7751210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7acb74a6b8325e38c2383603fa35e82ef5b3ee052c3f53e8e6231d760b0163`  
		Last Modified: Sun, 14 Dec 2025 11:20:46 GMT  
		Size: 7.3 KB (7286 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fe89b0da8067110ebeb9583ba3aedef86bc266da03b31cbbf614dc76bb9da79c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145876222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd84db59840a707cca4c74df95cc1e80071ca306de057317dbb0e91128368bbf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1765152000'
# Tue, 09 Dec 2025 00:11:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:47:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9a7cba59687143fa1a3bde49b08caedd4592355c94693db34a36ceebea332a04`  
		Last Modified: Mon, 08 Dec 2025 22:15:38 GMT  
		Size: 48.4 MB (48404077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c41c2bc13ca9c32fc8ea3b0ee8862d2350cf32202664571fd15af30f5ab552`  
		Last Modified: Tue, 09 Dec 2025 00:11:46 GMT  
		Size: 28.3 MB (28311739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5116962aaf70b7ed1f02f2ccd4dc554c6270985ceaf307b1f7833ab499653777`  
		Last Modified: Tue, 09 Dec 2025 01:47:51 GMT  
		Size: 69.2 MB (69160406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b458f6fceb79597a2cd0824315ab538af23b19ad14a90f3e583e63ab61b889ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f360123860a5b31d4db24693cdebceaf01ec3b10b396f2b6c5705c7e28935914`

```dockerfile
```

-	Layers:
	-	`sha256:fe5063963fcd36c834f105ebcf8e36e11f7001ef1e13dfec28d9d60b4a3537a4`  
		Last Modified: Tue, 09 Dec 2025 02:24:09 GMT  
		Size: 7.8 MB (7767980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1fa8fff0c1eaad63a93aeb7d42b4ef63090b82c925487879a794b8b44f8ce20`  
		Last Modified: Tue, 09 Dec 2025 02:24:10 GMT  
		Size: 7.3 KB (7254 bytes)  
		MIME: application/vnd.in-toto+json

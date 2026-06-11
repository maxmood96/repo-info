## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:7219ab7ba780766ac61d27d70b638625617d93610e0de5a7666dc473b63f3a42
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b6fe41c8e3ed9700f7b2dacdc856203673d5ec24fd30f59d737e7f6c3d2038c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142737039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee7542fa6d466fff32d75e9d6f6cc990a83afd9dbc72a5487480f36fdb503f2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b365b6ff7b7e310e1b9a88f996e65b89969c7fa450492b68249d1d1c38e0676`  
		Last Modified: Thu, 11 Jun 2026 00:42:51 GMT  
		Size: 25.6 MB (25635173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca884014342f240be01d391b498c3ec61b2f4af2c205e7e9a0b5ac2cb2f24c4`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 67.8 MB (67784745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2a84352ada511f2b6fe43e679ee074a9c1a213808abd60fb10e784f3a21286ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e1851ce9dc1c8858602acc0d3dede07ff97787dc289751a3c34229c02108a1`

```dockerfile
```

-	Layers:
	-	`sha256:cfd98ec8beeda790e4f5502ad80f4049edb0457341d09e575525e23098b559e7`  
		Last Modified: Thu, 11 Jun 2026 02:24:59 GMT  
		Size: 7.8 MB (7768523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36130275a870f5a12d0798e2f4cef50723de036d4b697e059d27c0395784318a`  
		Last Modified: Thu, 11 Jun 2026 02:24:59 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d5c9ac0c2fd5a0421f714bc3adc4a1352e9267d11ee2e62c2f0103da731234df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137202459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1601c0404fe46aecc9efccc9a027725d09ffd705a7e13fb2570565fc40e4592`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:21:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:46:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f4fdc449648c31ec97234c27647662108b2d6bce3fe83032a1af88265bf2ff35`  
		Last Modified: Wed, 10 Jun 2026 23:40:32 GMT  
		Size: 47.5 MB (47494811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3be6b9d9888f84dbe643ff398f469da8712a1ac207b5975f98e812dad9062c`  
		Last Modified: Thu, 11 Jun 2026 01:21:44 GMT  
		Size: 24.4 MB (24364313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8792c8246eb40706682474cfe0f7440cebb3cc0986b9ca229c49e962ffcf1a6`  
		Last Modified: Thu, 11 Jun 2026 02:47:03 GMT  
		Size: 65.3 MB (65343335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:15ba2103e62024a2da4561c161e4da830639db37ed6bd1d18feb0b61c46b389c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3486bde47b748c981bf3e158214f16269fe4ba8cffc01961bf8866a7ccf33d8e`

```dockerfile
```

-	Layers:
	-	`sha256:5c17cfc0c06677efaa147c8ca47ce4744cbea4460ffafae03d73259b453f080d`  
		Last Modified: Thu, 11 Jun 2026 02:47:01 GMT  
		Size: 7.8 MB (7769561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d62ac269d23ada8f9e50cb7779625c4b32543e462c161381ff9569254cf596`  
		Last Modified: Thu, 11 Jun 2026 02:47:01 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e0414039d8a4a188bc896a3acb75df62ce0ef14f269401608e9a2435cf543e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132131166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c5f74a07327ecdc613a87019c1aa3b649de396ba434381e8eef7fc9cf75166`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:27:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:45:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:df041f2d52cc5410fddc569f8ab35cdfdd35a38e037f7aab971e409724bfd203`  
		Last Modified: Wed, 10 Jun 2026 23:42:20 GMT  
		Size: 45.7 MB (45748641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04879054973f6f0ae366a776f1ee6e23a5ae9b6072a5861ec514fdf29f7dbd68`  
		Last Modified: Thu, 11 Jun 2026 01:27:20 GMT  
		Size: 23.6 MB (23635995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e960af1a374080feee4d695210e1cc29cde28cd70c56fad7cb555534519a7e`  
		Last Modified: Thu, 11 Jun 2026 02:45:25 GMT  
		Size: 62.7 MB (62746530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:64428292fce48880e567dd8400af2cc77fd96fe85fa2be3f83215ad0ffefad6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1369da63da4837e1d85ea9a4d2f0c84aaae73dd376da650213ac900c9dbcf737`

```dockerfile
```

-	Layers:
	-	`sha256:f5137b7e9b31890072be4721f3777d7bd5a56b21fa5933f97b33d0749abf7ac4`  
		Last Modified: Thu, 11 Jun 2026 02:45:23 GMT  
		Size: 7.8 MB (7769030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a5f7a4309a96bdee449b50ba36141dffa843e3fbb631ab47c64bca8927825e`  
		Last Modified: Thu, 11 Jun 2026 02:45:23 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b6cdc8b43c89fccd675edcb2dcc9130b0abce31e3e1aacc1f295b079adbbf13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142305014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0715e95c42915f8a52b311a668553340b43a5b015d8b93b97c737d167ac922b7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2ab02859108b91c1c26f2badd015b5215eb066b7ef4f3a22bd1536a8debe96`  
		Last Modified: Thu, 11 Jun 2026 00:44:32 GMT  
		Size: 25.0 MB (25026911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2e427d8856f71d8d3667d1c4d9274b8aca2bd9d228387c51c211909e51263f`  
		Last Modified: Thu, 11 Jun 2026 02:22:21 GMT  
		Size: 67.6 MB (67599934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c5a3b4e297856cdfe57fabb2f4f2998eff4a2325fd38023486c0a79745869a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef45d04ad2d1db089765f1d1113b0fef1910e2aacbac024e302ccd968d0461e`

```dockerfile
```

-	Layers:
	-	`sha256:41faaac3d7e4bc729674e6cb6e933145964a69ca4a015bb2ef32be82ea5d599c`  
		Last Modified: Thu, 11 Jun 2026 02:22:19 GMT  
		Size: 7.8 MB (7775561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:161bbcc5be5fbb5f69abb244f0c43263587559bde20ec3db2b5503a03bec4ab4`  
		Last Modified: Thu, 11 Jun 2026 02:22:18 GMT  
		Size: 7.7 KB (7669 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4422f366fd4a7c0d27bf02c4fea56bc01dc4d63712e314ca7d10ec432941acd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147456764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc14dc0f98eb6cbd85fbaaef34d31a175e51ce7fed047ba4d088e6198368634`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:45:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54ac1ec51d3293c1ade0065529ca23d5fc365d00997ff4e5a290cef3692dc04`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 26.8 MB (26797651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e0028665ad759d9a734f0342c043d69fa3d024141c3329c900f163c639953f`  
		Last Modified: Thu, 11 Jun 2026 02:25:16 GMT  
		Size: 69.8 MB (69823550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:28f691fbff76b49c2a1f5d7c889adc326ae6ddacc30cbbe3d2a39fa8b22f9800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c66da807796f3ca1f4fbb29f8d3ce50ac0a5e47f6d5494663d8a20c3b02f403`

```dockerfile
```

-	Layers:
	-	`sha256:14dad126a428a8686e85f88154c233a4cb7f1d8db69f25e8ca4892dc33fc7ace`  
		Last Modified: Thu, 11 Jun 2026 02:25:14 GMT  
		Size: 7.8 MB (7764657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daa1fd6b16dfe312e5275842c5b380159362ea4fe0d5543f81cd8bb762e0d912`  
		Last Modified: Thu, 11 Jun 2026 02:25:14 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:239e24bb51b1eb08ec856933ce152e61dfe16e7f849fe1edf6791f172877dd32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153195790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732df47f3d00760e12fb53fc4edeec3f6007cfec408ad244ffcb248636f53f8f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:14:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 06:52:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743dcca676e80d0b7074d4f03820f8068053078d4942f2a921fdf172c62897ae`  
		Last Modified: Wed, 20 May 2026 01:14:53 GMT  
		Size: 27.0 MB (27021149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7396fcf223bd659e5dda1b961ab403e3df6f9d118708751addc02badc2015799`  
		Last Modified: Wed, 20 May 2026 06:53:00 GMT  
		Size: 73.0 MB (73042459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:41b7b50813e78495182edbad237a2edb0bd837bc5239b5198a27eba010f7204e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b82db0a52ab76288a5ff0f55d4470a801d8ee5303900eaf722ec8bcd724d89`

```dockerfile
```

-	Layers:
	-	`sha256:0c114ed434398aa1abb7607c30087fdeb336061b0a040866b6370204950b2bc5`  
		Last Modified: Wed, 20 May 2026 06:52:58 GMT  
		Size: 7.8 MB (7775540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dede141388dc4306139ead9d2d907f1b911bfcb92f63caed66a3d3067743a8e`  
		Last Modified: Wed, 20 May 2026 06:52:57 GMT  
		Size: 7.6 KB (7613 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c2550ac47b21d6e3e57ed8e88df3918a1b3b2b979315cce4e0c0cad421b5c2e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139435858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabe29e6cb44f1ed7ca28fbb1cd004dcfb1fd600e8e6b17c692a2704819220e3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 14:01:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 23 May 2026 06:47:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e6afb0d9fe2fdfebacf2ccb9782fd129d9e416f637c13f72c2f0427e69c04c88`  
		Last Modified: Tue, 19 May 2026 23:49:54 GMT  
		Size: 47.8 MB (47796268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db76586e2d1a29e7feb120e0fcc7fa49e8df54823efd2e1b4e13ca0fe4ab60d`  
		Last Modified: Thu, 21 May 2026 14:02:51 GMT  
		Size: 25.0 MB (24966381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244bfe91065712f707f8614b6bb5478bb453a0332b440e47735c29ab8e1ac33e`  
		Last Modified: Sat, 23 May 2026 06:51:24 GMT  
		Size: 66.7 MB (66673209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b0c9e0839c1a88116ec96b8780cec98f7fcbee3100ba7e6f32f8cda529d9a369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7765867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33889134f8b7c5c78a23b98c11bf45de4dfabff6ab4b81719111bbae65e22cd9`

```dockerfile
```

-	Layers:
	-	`sha256:cc96d340b7e9a19815b8ff640a5f1b97aac2ec84a156ffcf481935edfe6877c8`  
		Last Modified: Sat, 23 May 2026 06:51:15 GMT  
		Size: 7.8 MB (7758253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ab1aa400b9ef5bf09c12e4b72288cbdc6797db05fa6dfa56bd381e496fda95a`  
		Last Modified: Sat, 23 May 2026 06:51:13 GMT  
		Size: 7.6 KB (7614 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7be60f9372bb12a2dda8515ff36646686f24a22d7f874415ddc9af420591703b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144843163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0da4e2355435862ac8d1cf1aabced98cde1cbf607903f5cd0e1589e3e1f7815`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:26:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b58925113278ed74d68122ff77b22976b064cb872b273063a3ab182209055ee`  
		Last Modified: Thu, 11 Jun 2026 01:44:45 GMT  
		Size: 26.8 MB (26803918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c67e4e83aa860c5b719a4e0cc01db908ae525049821b3c459f866ed434f070e`  
		Last Modified: Thu, 11 Jun 2026 03:27:03 GMT  
		Size: 68.7 MB (68653348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f9309cc2793723b52685ae0f66a4c08a6f1643f1246930618d09846354fb85af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fcf6cd1aa69354d725962b936960a7955e664978c2df7502f3425071159b5a`

```dockerfile
```

-	Layers:
	-	`sha256:5e156a9c1798d537f120a69f6e7edce33c05ab754ea2bf5f5363a66df08acaad`  
		Last Modified: Thu, 11 Jun 2026 03:27:01 GMT  
		Size: 7.8 MB (7769436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94461a9bf0d6c01685e5efb3905095506a4df1c41257f01f8008f9712fa681f1`  
		Last Modified: Thu, 11 Jun 2026 03:27:01 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json

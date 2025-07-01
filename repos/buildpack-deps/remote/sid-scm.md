## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:0c535bff596520c503e34170d71231ae071753978e211ed12ce5cdd3c31ebb4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:341a0b57d2b16179f0dd59ae8b0fd66545a0766d6435bade43642063df056ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143095957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234e297b09eb1b7340d85e8ad8cf502b18e8c565140478ebad7defafeecb32fe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:603de70df79137e44ed9b8e9d2eec3a1b8eb889b8a8650df1a6bfc2ba9798f72`  
		Last Modified: Tue, 01 Jul 2025 01:14:45 GMT  
		Size: 49.3 MB (49267699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b752883ea09044589f48c52df49289712f416806e7b67e6d3b283e6c96ac266`  
		Last Modified: Tue, 01 Jul 2025 02:25:34 GMT  
		Size: 25.6 MB (25619155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb14a16253ea0df4ebeb77b1db25ac37e73812925ccf4de831d1f7bc411f2c38`  
		Last Modified: Tue, 01 Jul 2025 04:11:59 GMT  
		Size: 68.2 MB (68209103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9f33435c6ebce0f65890ce6e2c0cd5afabf06db7f0792bcf0df87801373fd678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7785960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a296c583045141ecf21098993f50a2d21de384a36f7a83ab0429f9c41ea78c1`

```dockerfile
```

-	Layers:
	-	`sha256:f905e0475b1abdfbb452be9d28bc18875a564d7d54439a1393fc224120d8ce21`  
		Last Modified: Tue, 01 Jul 2025 04:20:59 GMT  
		Size: 7.8 MB (7778664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b04e3e8108bf5c459285697f1c4c21463bced81f3f67c073d47063bac5e950b4`  
		Last Modified: Tue, 01 Jul 2025 04:21:00 GMT  
		Size: 7.3 KB (7296 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7e76a2ab3e9adb7c843aac72b39c46589fbef7b2a760689e003fd3e072100446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137404579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3332a4cd116ba5cf9cb8f699248025d6b805df274fb912d5bf77b66d2f9401f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8344b2028cc05a08f8b0b577cc9430fd30421d98f7302a20cc79a7392635ca51`  
		Last Modified: Tue, 10 Jun 2025 22:47:59 GMT  
		Size: 47.4 MB (47435203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e8ec6927bc0cb7d56e990391b853ec23d7d3eb74a5f1f9500df8d5cf23ea4d`  
		Last Modified: Wed, 11 Jun 2025 03:13:46 GMT  
		Size: 24.3 MB (24328621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2085f136199cc5a804201375aeae18b933264b5486014fd2d2c46cfb68e131fc`  
		Last Modified: Wed, 11 Jun 2025 12:21:44 GMT  
		Size: 65.6 MB (65640755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:625a2db157df82c398b21c4202a1e0f9d6c8b6d6be358b3c4ac1c84f4ae6e460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7793883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0488e13d788ff8807b78f4ed2b0f945d1d2e9915636ad250937c9eec4cfdb84f`

```dockerfile
```

-	Layers:
	-	`sha256:174cf164fd718ed3d05dd43f5796b35ba27ece82e631b087165cfef849a97459`  
		Last Modified: Wed, 11 Jun 2025 07:20:30 GMT  
		Size: 7.8 MB (7786526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71a731a60015a8e89e7008471aef30701ee6676227e23b2ef5f6b5b0fd36ff2f`  
		Last Modified: Wed, 11 Jun 2025 07:20:31 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e9dfd2f4319778c21493617a5dfa6ba56dcb68acffaf1731119b0de0217f808c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132324837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7072d59072931ff876cf93d699a2ea2e86ee5c94b6fae1cbb1e5639103a45105`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0ceacdda8a07413d9c26c141b0f4894fae020e6ab65ff0188cce0bfe5e0c66eb`  
		Last Modified: Wed, 11 Jun 2025 01:10:03 GMT  
		Size: 45.7 MB (45707825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b841f0ab46f7d7bc86d75d499d470af27c2315d80feaa41746c1f9e6d995ef`  
		Last Modified: Fri, 13 Jun 2025 17:03:18 GMT  
		Size: 23.6 MB (23601456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b703c4341425792b641192b1633584b31d3164c5bde6219fcbd37175e45bb2`  
		Last Modified: Wed, 11 Jun 2025 13:14:31 GMT  
		Size: 63.0 MB (63015556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:be2f4b723c24be443e14570888b1798b2f0bc84be10c1e3cc58fe81c320c8e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7784099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabe07e801f2691e08df429cb0df6532e0d647605799cd2473a4483e0a51d292`

```dockerfile
```

-	Layers:
	-	`sha256:0c8712b91f1d52e08b2c5fc2859eb834187fcc78de07d56202aec9ddaa562b0b`  
		Last Modified: Wed, 11 Jun 2025 16:20:43 GMT  
		Size: 7.8 MB (7776742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f2e5e6ff4158493e4d7a9d516b7c98a242c2cf760c7424daa1d1fc7210b1cb`  
		Last Modified: Wed, 11 Jun 2025 16:20:44 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a44bbf6f4bb8806f5610051741889d42146f684cade400c38a2b064c2d1b3809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142529431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d666e1a29145575caaa4bb5d7a5e9ff8a6a11cac3c46d92415cbbd156474d16`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4b10e85b1b46df396d3cb4118de7b2483607b89bcd163318c9756c711f9a3ef9`  
		Last Modified: Wed, 11 Jun 2025 00:37:10 GMT  
		Size: 49.6 MB (49629348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae44e59140036c47291ca98d6f5cbe09bbc2c6ff2f7067e6ed8f93f2a9ed0b71`  
		Last Modified: Wed, 11 Jun 2025 08:13:09 GMT  
		Size: 25.0 MB (24998868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1842d0d17df930326b268986cae23d9f266eff7b38d9a7a69d040cf74bd3fa`  
		Last Modified: Wed, 11 Jun 2025 15:10:50 GMT  
		Size: 67.9 MB (67901215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a2577f69e3097f2d61bcf1b891a3e4915a8d4cfd88171fbddd30291e78f82f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a783af888eff79475ce1bf89a35c6dab1d185403a33d0f358048ad8931bfd28`

```dockerfile
```

-	Layers:
	-	`sha256:f49d547905e27f661fcb0be6b5c599bc00747b673ac96448ad0ba88bfafbb8e3`  
		Last Modified: Wed, 11 Jun 2025 16:20:50 GMT  
		Size: 7.8 MB (7783906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b702b7e83b70bd6197639f40a287179ab9bbac633fa5bbb9bf800c2fd2bd4dcf`  
		Last Modified: Wed, 11 Jun 2025 16:20:51 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:12a8b731a15ac989d4c0ecf58c8cf4b2ca697328589ecc69e4d8c96899101b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147850682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda7f13a0d9e866ae46b8c46d1bda7606e312ab066fdf3f1cca24606d24ac45b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:41ea081e29dc4034ec31a49ac48ddbf738b840fd4d226f5678cb63f00b10ab33`  
		Last Modified: Tue, 01 Jul 2025 01:15:01 GMT  
		Size: 50.8 MB (50790707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d224078a83c5498b9115edbeec34eecaddc04a9e2e47f0e71d34a7e780a2059`  
		Last Modified: Tue, 01 Jul 2025 02:24:36 GMT  
		Size: 26.8 MB (26773974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6014d1af113edbca3a63a8a8aff65bf03bbb831dcab023e346303a638c1250`  
		Last Modified: Tue, 01 Jul 2025 03:19:59 GMT  
		Size: 70.3 MB (70286001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:14b6a8a1fae7a389dbdd32b73a894bb37ea966361e77e6f44cba3331598a882a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:864bcd851bf1d378f5d1ff51f1ef08c35a956f5f5e5bcc43828fd3f3a0cb8d98`

```dockerfile
```

-	Layers:
	-	`sha256:b0e58f4e950070edd432fd0116f2c307f5f9e9e15321ba71b4c276cae598c7b1`  
		Last Modified: Tue, 01 Jul 2025 04:21:27 GMT  
		Size: 7.8 MB (7774805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ef0e6d7e7f58f927fcd2f1851077fd2e32f8b35023908f287dde95946d1463b`  
		Last Modified: Tue, 01 Jul 2025 04:21:28 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:29dfa45bf59b94c4881fdbebde030ac5ea9b185b54e1ee45d1ff9ca7c28ec0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142277934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e04d308b1948df8c5fd40de1f63e79ea3b7fdc08f312fbffb4c2c7303f91492`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:54a8735d26fa76df64dcf3824b7f78b58d44ea01ab0788f2fc33afa2bac4f1ad`  
		Last Modified: Tue, 10 Jun 2025 22:48:52 GMT  
		Size: 49.6 MB (49553255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06ee97fbcbae75cf1777c40791b1a1c25100c4b6ad8a9ed9323cceb66a38ba5`  
		Last Modified: Wed, 11 Jun 2025 13:02:36 GMT  
		Size: 25.7 MB (25652069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bd97199828602994822322c66b6b3a65083d16ea25127f0a48c6b159108cd4`  
		Last Modified: Wed, 11 Jun 2025 22:23:25 GMT  
		Size: 67.1 MB (67072610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ebaa1066d786af0d05652d516a8ab35a85653477db71b7384913d74f4ca664bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902b9567fadf08dd26449a8656158664f54feaa3a729921bb57c40ab328f969e`

```dockerfile
```

-	Layers:
	-	`sha256:9941c0a019a81251a96cd85006c855582f4c4a4e5cd9b033d8a5a1e10ef7715a`  
		Last Modified: Wed, 11 Jun 2025 22:20:49 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:464923e5be1e684c93ef53ad158009c711c96d8c9bc89a96e06104e687eee505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153424114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:330fa7c18fb773f4466b3f1c10bc32bdf6b037affe3fc2abdc992cb4ec220714`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f34e3f5941a9b9d7f66cc62bea1f477c727df8c87b640bd63d443c8cb4c08203`  
		Last Modified: Wed, 11 Jun 2025 00:27:42 GMT  
		Size: 53.1 MB (53098680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f227a2066e39def58b490c6183c1c743b3db44ed881ae2f1d7f6c8febfbc6b1`  
		Last Modified: Wed, 11 Jun 2025 17:42:13 GMT  
		Size: 27.0 MB (26983625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fa176b0ee9b3a9a511ef65649d379d0d0d4e1a342fc2d3e54b6d5e65171edc`  
		Last Modified: Wed, 11 Jun 2025 19:14:57 GMT  
		Size: 73.3 MB (73341809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:39fb1501f14a4eadb0905a4a1f7fb15594eeb5acf678b32f54c6a986bbf7fc6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7799928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ea03e798da2635abd93ae5536646bfa8ec864fd38db38fb4c076447e59e6e7`

```dockerfile
```

-	Layers:
	-	`sha256:c44f47677ce1390cf497df8d0457f1c7b168a0d6206506e79970ea026be61082`  
		Last Modified: Wed, 11 Jun 2025 22:20:53 GMT  
		Size: 7.8 MB (7792599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8664649252eadf95e223b2695dd75fd77d68ac8f40ce31ef54c6dbfbd53c56cb`  
		Last Modified: Wed, 11 Jun 2025 22:20:54 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c943f0df1229a3e28ac477d138c40fd08872d11f7de222ad53ddaa72e6f05986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139802594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce16ffb167865e6220ea2272051deb55f210901f0990bc336d1b99fa5adc706c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:42f7c08d656e09c01f14d35a847143f84e881d1ac3f16f3ba511348bbbaa7d82`  
		Last Modified: Tue, 01 Jul 2025 03:27:03 GMT  
		Size: 47.8 MB (47756066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a4ef3bea202b6f661456b37f5106a6a6e0acda6439394bd6618c6150a35c24`  
		Last Modified: Tue, 01 Jul 2025 02:22:42 GMT  
		Size: 25.0 MB (24954336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f59f94fee11898b889be78db1b26357b77690be8753df91b533098e18b75eb`  
		Last Modified: Tue, 01 Jul 2025 03:58:27 GMT  
		Size: 67.1 MB (67092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:65c3595b06707ef5426bca16f71cb4f66d35ec7e0ae4f3907b151a328ffa218a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b53efe2f6dfcc9c74753e064965dd8b027f962c71270fd3457baea55453523`

```dockerfile
```

-	Layers:
	-	`sha256:9dd4435e2ee2298f9a1bc1df11cc151392ee318da2a40204a523df4a3283f0fe`  
		Last Modified: Tue, 01 Jul 2025 04:21:47 GMT  
		Size: 7.8 MB (7768492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:520805d6dc202af83c93803382120eb09227a998e179b4c9256ddfe72c8a9017`  
		Last Modified: Tue, 01 Jul 2025 04:21:48 GMT  
		Size: 7.3 KB (7328 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f6304f4124c45e010879ecc9dbe6745152bbd2d30b3f0a56aa9183e0cb811fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145183359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d20c38b07b996dfbc65590d82786b74de9bafd981262350948cfedbf84677c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4acd445fdd6fc8a863e2e2fbc1f6d0dd614a42ad5a89118b6cd287f18c027f79`  
		Last Modified: Tue, 01 Jul 2025 01:16:17 GMT  
		Size: 49.3 MB (49346648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d516536545f6fd66256972b93b51614ab1c9f96883e1f5c8990597ce59c040`  
		Last Modified: Tue, 01 Jul 2025 05:31:15 GMT  
		Size: 26.8 MB (26786410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca1529b246d5d5bf9d3254f1e2eb47235c74e91731ad440f78e506bbce83b45`  
		Last Modified: Tue, 01 Jul 2025 08:57:01 GMT  
		Size: 69.1 MB (69050301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7cb229de4961437de09372793647efe225f49ff689b3b532cc3079ed1aec7c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7796127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e031870ba8ee01ee180569687a2289a1adbcd3bfed2c1cd756fef7ee6017c75a`

```dockerfile
```

-	Layers:
	-	`sha256:02cf29dfba17a257dac937ad808c8f9f80df511c58940f19df57322de5643daa`  
		Last Modified: Tue, 01 Jul 2025 10:21:04 GMT  
		Size: 7.8 MB (7788830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a39d99a1b7c617975bea309d04115a94e9519bd2ff331eaf55bd4287987839d`  
		Last Modified: Tue, 01 Jul 2025 10:21:05 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

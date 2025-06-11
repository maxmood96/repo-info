## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:bdff47e527316d02afa2ebd715b477970f1d1a179d574263ab14245c8f8fd604
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

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:af6a50941cfc5c1606c3d105484f8a10b89c11e5395ec997dcd1c1fc03dd0b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142909972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588cb5fdac5c0ce11ce4ee586bd7ec6af5c2d97b37a09e153d6123003b08339c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6b1598688dd5948f64dc955f58b0dcf5627fc6bbc5754f5ea08612c6d3bace8b`  
		Last Modified: Tue, 10 Jun 2025 23:26:12 GMT  
		Size: 49.3 MB (49263317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cec2bdcd950987565d27e6bef170159a9fdde6f46531b0889933354046db48`  
		Last Modified: Wed, 11 Jun 2025 00:01:47 GMT  
		Size: 25.6 MB (25603931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbea8bacad06666c3210aff4437aaea1773f797c5f0e58c28f9f9d0f3ca5ec62`  
		Last Modified: Wed, 11 Jun 2025 00:02:53 GMT  
		Size: 68.0 MB (68042724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1aa4910882821580cca174be29b22c1c4f7a26dc99a64cbedc54e4eca50ba047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67ffa512f71cc660de1674877fe436b3fb2970312602c45a3442cba16501873`

```dockerfile
```

-	Layers:
	-	`sha256:627fba575cdebcc4ce0639ca315b43d5577658b643821b739c625f54e9e403b5`  
		Last Modified: Wed, 11 Jun 2025 04:20:59 GMT  
		Size: 7.8 MB (7776243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ace33d7b9dfbc1b9df233a4f0b5f0ace0b0679e0eb2926aa8fad14bdaeeb671f`  
		Last Modified: Wed, 11 Jun 2025 04:21:00 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v5

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

### `buildpack-deps:unstable-scm` - unknown; unknown

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

### `buildpack-deps:unstable-scm` - linux; arm variant v7

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
		Last Modified: Wed, 11 Jun 2025 04:58:57 GMT  
		Size: 23.6 MB (23601456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b703c4341425792b641192b1633584b31d3164c5bde6219fcbd37175e45bb2`  
		Last Modified: Wed, 11 Jun 2025 13:14:31 GMT  
		Size: 63.0 MB (63015556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

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

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

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

### `buildpack-deps:unstable-scm` - unknown; unknown

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

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4da97911ba7d4e39aaa9ac5e5efc03e6de300e12a5482654ec8b071378628292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147680199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7822ec7444554aed38f213ccb2e82388be6ace88a3102de9c407759ef93a125a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1a1a02b91b1c2266da4734f34b831bb020d740f7bfd0647d1828242b377de717`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 50.8 MB (50786017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13c1899ec001f75529ee8cd455eb4a23c4b9c5414c63db7730474213c55437b`  
		Last Modified: Tue, 10 Jun 2025 23:36:16 GMT  
		Size: 26.8 MB (26759161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521cd224c201b94f36b1b9e6ba5db4b89c6a8f696946eeacb5bc6b1ac6ed6f5a`  
		Last Modified: Wed, 11 Jun 2025 01:13:31 GMT  
		Size: 70.1 MB (70135021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:73be5d884aaa2959427a7e1072b12a78becbbdbe0d0cbe4944c73094a7fe1ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7779665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7a5eed419dbd2d3ef98df812d9b24c913d5954f120cd5739b6edb3fec772dc`

```dockerfile
```

-	Layers:
	-	`sha256:770fa87e6b934d3398496d1de1c914944905391583fc6e4b68c049b055f8780c`  
		Last Modified: Wed, 11 Jun 2025 01:21:22 GMT  
		Size: 7.8 MB (7772390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91cab14eb66433755b8897dfbc7a585872e4e3082eae6459a8930aeeffa701bb`  
		Last Modified: Wed, 11 Jun 2025 01:21:23 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; mips64le

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

### `buildpack-deps:unstable-scm` - unknown; unknown

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

### `buildpack-deps:unstable-scm` - linux; ppc64le

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

### `buildpack-deps:unstable-scm` - unknown; unknown

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

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b3df35c212eb327805801f1cb5fbb0583a28b36fbc27cb48022a17955cf0f931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139675924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38df2eb066c6eabfd808fcae02b5a5dd60214b63d70e236191512be0f93aff23`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0009e91f3f8c4153a02b39dc6e9b3c5a36cc3c8e1a157d73e8f9e91097515059`  
		Last Modified: Wed, 11 Jun 2025 02:03:30 GMT  
		Size: 47.7 MB (47749671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df49454d4e709bab7fd6d2461b736d24ce3db865904adb84e1af7a3e0716ace`  
		Last Modified: Tue, 10 Jun 2025 23:34:49 GMT  
		Size: 24.9 MB (24939799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d5419b50e53679e06a4b73e768cb2cd1c6fce73cac408ba77b0431e99651ce`  
		Last Modified: Wed, 11 Jun 2025 11:59:20 GMT  
		Size: 67.0 MB (66986454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:13152d5e9f5b06e7cbf399aca691342ac96aab2f2762cce84dc2c6f6771df1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891c1b4d6ab7c75892f8c0a954fa53dbb2e79ccfa630418565b6efbc15f62e01`

```dockerfile
```

-	Layers:
	-	`sha256:869bf10b7b7bb91caa75f268c11308a51d4ae46dda938da8f513a8ac7ecf2675`  
		Last Modified: Wed, 11 Jun 2025 13:21:11 GMT  
		Size: 7.8 MB (7766059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d2fb699ad45851b0fc32af2e6778cb5768d8f0a1e094d0dfbc8e31905108566`  
		Last Modified: Wed, 11 Jun 2025 13:21:12 GMT  
		Size: 7.3 KB (7328 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c293ffb9b5b24aef4938abd4885ba2ba9e2f6da430c5814905c41195205aa15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144801421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8e8179fdc2fd23d77f50bc13033a5be291ee18a60712acf385c1258dec97d4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a52b4c8ce9959e1107790b0cf878188904eecb5b1ccf411d93d6ab16036dc160`  
		Last Modified: Wed, 11 Jun 2025 02:03:33 GMT  
		Size: 49.3 MB (49343092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf0965e23eb9d70e72f15582a2cb686bcf1857eb924b4d704542fc37d206146`  
		Last Modified: Wed, 11 Jun 2025 02:51:24 GMT  
		Size: 26.8 MB (26769281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc44cd2b9aa97b3fbb56995ed62a657167162e1278b818c7bc6bd60f13d1e12`  
		Last Modified: Wed, 11 Jun 2025 07:20:39 GMT  
		Size: 68.7 MB (68689048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:52b93c5ebe2451a2cc87dff75a7cef376de6933d492208b7a6700656686611bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb2182c6381249391b53a79cc33c435907a5c53171561f8c71a595990551337`

```dockerfile
```

-	Layers:
	-	`sha256:420baad8ae06e11a3b53d019d6555225c352251ccf0cb6ba267eb8a9ae0fb4fd`  
		Last Modified: Wed, 11 Jun 2025 10:20:47 GMT  
		Size: 7.8 MB (7767538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86234c91b0e0ca8f244dbaa838cb2bf82282a4a04bc299e3d47ebd138f37a9d1`  
		Last Modified: Wed, 11 Jun 2025 10:20:48 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

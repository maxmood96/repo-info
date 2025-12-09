## `debian:testing-backports`

```console
$ docker pull debian@sha256:f76061dfb180bdcb85174819247432dd04e9888c589b5d1128d25bba372c989d
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:e033aeb3bec2ef70afcd2f9a41e41cc6c8b7ad0e53fcaaaa832af62ad2cdf273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48512735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce35606212ec50cbabbab718a99b619df079d267da66a584339ab20d7c23974`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1765152000'
# Mon, 08 Dec 2025 22:29:42 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d07e7493d30660e90d785732f6efa7dbc2cb9ffe13064e2383c3338b574466d9`  
		Last Modified: Mon, 08 Dec 2025 22:16:56 GMT  
		Size: 48.5 MB (48512513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eace65448f51a7986120eac444b1d6abc73ed206877cde6f11f831c7fd238a`  
		Last Modified: Mon, 08 Dec 2025 22:29:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:636f5794fffb4c3c3afdd2adc577fb509544cc7201bd790fa15f0e85b66313f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3139399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c85138143947fad6cbf8f461c28a54bc29bd67d1a361acbe7aadc34d6e3210`

```dockerfile
```

-	Layers:
	-	`sha256:2291711230ef809336e68db2cfa4e2274ef720b759b76dd95ddc5f461ef6abff`  
		Last Modified: Tue, 09 Dec 2025 01:31:25 GMT  
		Size: 3.1 MB (3133605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8a0e2c163b8a55a23bdb09fd482931bac8d251f013c2442195ba1a912736735`  
		Last Modified: Tue, 09 Dec 2025 01:31:26 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:17448dd056f9f810fa5765d1fc3f0cd6a1754b8514cdcc6ef02978d3cb879803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45048266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577a7de4db214b76c31e716f6e096fe687067ba57991ed44805d5b5e09efc4ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1765152000'
# Mon, 08 Dec 2025 22:32:45 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:91b533abf4656d434dc53008257ce01cf32442eea1b3e818bc77f00130717fb9`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 45.0 MB (45048043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42fd7a3c6696d9c9e82a1388189ef6dac5400e0950d8c262f11b20f6ab19357`  
		Last Modified: Mon, 08 Dec 2025 22:32:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3e26936b0e5fc5bad5a0bb1e68f13d6eee69f0e6157f9cff0742206351db331e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3140823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f213da437599fb6cc0cffe5f8eda339fa121d675bea8162d8f4424c17ea3338`

```dockerfile
```

-	Layers:
	-	`sha256:842e0ae42b06e606e730dfc894527cf8e7afa8401a732bdd1d9a26e547339a2d`  
		Last Modified: Tue, 09 Dec 2025 01:31:30 GMT  
		Size: 3.1 MB (3134973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ed47b5bb489388758aed7050e949da5f82128c196c23008481e984529fd465`  
		Last Modified: Tue, 09 Dec 2025 01:31:31 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3492e5696c3231ae33f5937caa4eb3eee728e25c01de892ecaf02aac20aaa0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48599561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26f9745ad2ed1cbd482f9fa6431360e9dfca16913b1e88844cf7bfd6dfa01e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1765152000'
# Mon, 08 Dec 2025 22:32:42 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:980892eaed7a52ea486458964bd611659e21bc061abbc845e2c0e0044e32f492`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 48.6 MB (48599339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053f741c3f007f59d8fde0b4ae5d66e4bd6eecc592c4f91e0805b0a78da84792`  
		Last Modified: Mon, 08 Dec 2025 22:32:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:aa4a299f9e05ded3e884cbd830b486839b2a0ebe3ee301c52b9a06faa69131e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3140308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7baef659f695bc41e1e7ebee359d61024ba58179871038f5bacef1724f3546d7`

```dockerfile
```

-	Layers:
	-	`sha256:2803bcadbdf95fc150c6c61c3dc8e6f3fa03e4103d3c893917c523498cedde0c`  
		Last Modified: Tue, 09 Dec 2025 01:31:36 GMT  
		Size: 3.1 MB (3134446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c341b07ea6333ecb6a8006feffdb5612f3a3f628c1016951d458fdde71f5a590`  
		Last Modified: Tue, 09 Dec 2025 01:31:37 GMT  
		Size: 5.9 KB (5862 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:781ed69f704a870f56f36a63c58caffa59442ab079c22dae148df9d75764fb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49874804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4cfd64a03f58d325314d2b49d736144feec4c40923eea3ecdf574aa2a8974d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1765152000'
# Mon, 08 Dec 2025 22:30:43 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c493222762af604803548557b7f7446193795c2901c28794f84318d3e7ad41e1`  
		Last Modified: Mon, 08 Dec 2025 22:17:00 GMT  
		Size: 49.9 MB (49874582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d659e7e81dfd24736662c7efc83a890bc17e317b1833fc5c10bb9d504fc8fdb4`  
		Last Modified: Mon, 08 Dec 2025 22:30:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ad640dcdc6eb18566ca6b00376c3064dd9443bcd10c0a79f018bfac49a82d402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f6ee7ef8f7253d162d22132ba3ee9c238f9c79d5286bdca52510d415e4bc9d`

```dockerfile
```

-	Layers:
	-	`sha256:88ab5b93a72733f165f7d5de46ddafb520d886d207069589d744b4c3a6c35c15`  
		Last Modified: Tue, 09 Dec 2025 01:31:41 GMT  
		Size: 3.1 MB (3130809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa24ce28be640de9e0f42860f582371548d396b159885a16cbc94dba0e6d1f7`  
		Last Modified: Tue, 09 Dec 2025 01:31:42 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:295be79e3092feeeab461db25d78aef96d05cfe4dd003c9a94deeeb913d5d95e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53334856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89f37edc759c065cc1dd9d7c0b6ba12ebbd8b7aeb79733f8448259cba2210a5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1763337600'
# Wed, 19 Nov 2025 08:09:40 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3415dbe8c9fa5c426374b6be2cb753ee1cd73c4fc4d9120de95ac3d35fa936f1`  
		Last Modified: Wed, 19 Nov 2025 07:09:23 GMT  
		Size: 53.3 MB (53334633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85d4c881c65aa04f06c620630f6c099db2a51bd358dd9ada781e88197e6d026`  
		Last Modified: Wed, 19 Nov 2025 08:10:16 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ef3d0e0932538306298b171388221b2d465908929a0d091828c351f31849054a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b14d083166d695413852457d402c5a248b3396bf9a3cc2bb3b5b91b4e3077b`

```dockerfile
```

-	Layers:
	-	`sha256:a3773fc524abe8e0d7188668b80e3865eafbd72f5705f8cfa397faf08006c2c5`  
		Last Modified: Thu, 20 Nov 2025 00:02:08 GMT  
		Size: 3.1 MB (3133026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b54694d9946b7e0e6668045be46aa8809a6fc98583f613048485ef5fb6c8c0cb`  
		Last Modified: Thu, 20 Nov 2025 00:02:08 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:1f55c36b71e141ac8bb3de7b6b3edf0e546399731eadf4f200f2729dbaf324ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46806558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9448999da3259639bb002fc304b133cf1b9562574ccc54da22a76732d4fe2ff5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 07:58:27 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:57bd4f7d65060f5143ea57714f6e69a3a375d12220b4dc8eeb59fabbd8adf6b4`  
		Last Modified: Tue, 18 Nov 2025 01:41:39 GMT  
		Size: 46.8 MB (46806334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f77aba92446c6925147878b80c551cf5200ba268d8f65926abf20d1de006737`  
		Last Modified: Tue, 18 Nov 2025 07:59:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5e901a2c52b8d98454eff20a6dc1163daeceed564a675a8d7f125a3c265a7dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32af2e04b2ff66e7a321a20d1917720c1b15bf8491a95d3a4467ad04d913bcbb`

```dockerfile
```

-	Layers:
	-	`sha256:cad6781940f210967a7aaf44f5ac0a131f1c8767ecf560019933e4f47b9d522e`  
		Last Modified: Tue, 18 Nov 2025 10:26:40 GMT  
		Size: 3.1 MB (3121836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24894d17fd589e0c6e842c478f9ecedc0c7e823f0ab339ace60e255b15d8179e`  
		Last Modified: Tue, 18 Nov 2025 10:26:41 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:ad296c806592971f4ea15861e245699a087bd1f24bbad1f4d2a4c7f2fa0ec93b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48371154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad89214ad53d60a89f7be873f8deb3133d75a17bccce7368de822715ca05b659`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 17:12:47 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:963b067f9eecc96262cd77759b1e1e10770c29e86028729532e1addf32185ef1`  
		Last Modified: Tue, 18 Nov 2025 16:21:20 GMT  
		Size: 48.4 MB (48370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725624363fc75d05347d2cff8f50eb0a33274b698d84ca7a925a78a089545e1d`  
		Last Modified: Tue, 18 Nov 2025 17:13:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e690c7667f3a0316deb777f4df690e9fd734740ecb07a4531715a72fbcd7cd10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93dc4d8921ea4ce411e46dc02866ef42b263be12fdab23cfa0580db8c68bad9`

```dockerfile
```

-	Layers:
	-	`sha256:64af50c72e111c473b7b166565f873f63b7c6a0ebcf68188c906bf07e2511b8f`  
		Last Modified: Tue, 18 Nov 2025 19:25:16 GMT  
		Size: 3.1 MB (3130986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb05a514c43f1a758b1f9475f30ce0589f11da60ae73d5f9cbefd63e072f44db`  
		Last Modified: Tue, 18 Nov 2025 19:25:17 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json

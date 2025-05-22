## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:7ae886a2bb575ff8729d0f5e239539423710e6b4c65c0fd263ec16f4537650c9
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7068a13c401f297719a4c15b8bc738c13a16505f90d3e4cee3cccb491c095a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74830659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83644fa2676c0f077a7f4b2854fc68303a8932ef031bba8c91f818a9a5fa66ae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073c3e094f775042a2296ed99ca159904c7ae19127cddd6dc0e02dfeff3ac66b`  
		Last Modified: Wed, 21 May 2025 23:20:52 GMT  
		Size: 25.6 MB (25583751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:30dce5b86276ea1ab5a19122afb9965a92bb003e8a6663e32bce716ada2de982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc63778a9addc9223df451d73e626c40d5d433c7fe93fb8147a7adc496e8483`

```dockerfile
```

-	Layers:
	-	`sha256:127f75efa84446233bf62d055f1a5ef2c037fc1d489ef29ca240502a2cbd59db`  
		Last Modified: Wed, 21 May 2025 23:20:51 GMT  
		Size: 4.0 MB (3996441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd056a7aa68ae459a1319b4aaf16f5c0dcecec2360a0ee6e62da52ac4c9da77a`  
		Last Modified: Wed, 21 May 2025 23:20:51 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8960c0f06be814ca30bf209481d443b22a3cdf78dfe0ed92f4a75faec94d7193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71903058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cd09141dbce9640390f777b90f7604b24d90c47e6945081ee2ca3ece0b59d5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:15a0811b2608aa97b4e0811060ffea557de20e605122f0c38825f47469947704`  
		Last Modified: Mon, 28 Apr 2025 21:10:19 GMT  
		Size: 47.4 MB (47428611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b453de73db44edcda29182f13881db794c74b0f335096c735f5f88ffb61b994b`  
		Last Modified: Tue, 29 Apr 2025 06:01:51 GMT  
		Size: 24.5 MB (24474447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d92826e7ca33d9783680b60f07cd8a3d048e3c5d49d3b08b4fb2c8d8f98a675c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3999534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad4354b6fe53b29d5f1ed02bc6d1ffdc3d9437842a9decdd0d41dd263a76c0c`

```dockerfile
```

-	Layers:
	-	`sha256:d7f3a7f9244ef309ac89251fdeaaf694e68f2fa0597bf5ebd0c7ee76ebce05ae`  
		Last Modified: Tue, 29 Apr 2025 06:01:51 GMT  
		Size: 4.0 MB (3992655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:443dbd55c7b01b5a59785c65a175ffeac150c102421426802730040e70380fb8`  
		Last Modified: Tue, 29 Apr 2025 06:01:50 GMT  
		Size: 6.9 KB (6879 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1a5ffa9b745ddb1d6bcd09c6ae59256668d44a08b2e7a7820979c9157d6c1fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69422195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471eae3a39a8277efa0354b33ff1f02a006719efe607952a3306797b1a7efd10`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d877c043ab6ec52d6d4eaeab7dea355ef83893e584af00854b55ca611a3bcd99`  
		Last Modified: Mon, 28 Apr 2025 21:19:08 GMT  
		Size: 45.7 MB (45683821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785865296d03ccb31a01d56e5adab53e0c986bcfdc0c9920d48d9b1d2d93eda8`  
		Last Modified: Tue, 29 Apr 2025 03:39:17 GMT  
		Size: 23.7 MB (23738374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e32f482c1e7ddda785eb21e00672991a91f24fa6b40840f6a5d0a5fecec7c602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c88f6d685463df5d4702ed0131cb5e440a8a1ca41ea2979bdd646a7b485af7d`

```dockerfile
```

-	Layers:
	-	`sha256:580b68f14d149fb86296e5923407fe32efa5ed0349d6bbdcc273a0741f769a99`  
		Last Modified: Tue, 29 Apr 2025 03:39:16 GMT  
		Size: 4.0 MB (3985247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b9b708cfc28c5ed42f414d8d9d6e4dc15f3af639bba424d5ccb02bc32ed42e9`  
		Last Modified: Tue, 29 Apr 2025 03:39:16 GMT  
		Size: 6.9 KB (6880 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3f2fe02448f330b74da14b4c094bfc7e92e087bdc753fbe07d1e41b689307aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74741086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a059c5a9f9b224518e93cffe75d6d5e9592876e9fd09319ed2c54177d3eb0e05`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:288a1cecb0ea762427d39b072c1ca965d193e927e04da652f7b21eb12e9b2acd`  
		Last Modified: Mon, 28 Apr 2025 21:23:23 GMT  
		Size: 49.6 MB (49624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6faa4d9377738e3cc52e5d3cadb55bd77d367fb6439d9d14741079130dc9e4e`  
		Last Modified: Tue, 29 Apr 2025 01:48:13 GMT  
		Size: 25.1 MB (25116968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5452c96a4e99b734ebb51a784d38378a97839d67e8390f0ef4ff4a82682b0102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6506ac17edf4d0d4371021db856acbff14b4f54fe6c07d92cd543d5050ebc5c3`

```dockerfile
```

-	Layers:
	-	`sha256:b22328473e8a24afb96ea50af42494dbb5f4c96c3297da3b6c6ccbdfec89f7fd`  
		Last Modified: Tue, 29 Apr 2025 01:48:13 GMT  
		Size: 4.0 MB (3985280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8ad75105e0a5aedec033bc639fef39a7f18c7890a2b757153623f80874d1f55`  
		Last Modified: Tue, 29 Apr 2025 01:48:12 GMT  
		Size: 6.9 KB (6901 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:08e20e1b6588b122c336608d933dc24ea4ced2196252f951a6e7483d186814f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77507096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10e4bc89d31ad4149e68349c67fc4f470f8b8a8968f5b0d125510f8aefdd47c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7e1acd19dab9f7ab62b7570b85e71035e78cd9d9b9bff975df4b0a635578c7be`  
		Last Modified: Wed, 21 May 2025 22:28:11 GMT  
		Size: 50.8 MB (50761280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24ada90c6b3f67e8ac11f8d9700e1fbeb5f64ed848c2ef5d89e89c3d1161d7e`  
		Last Modified: Wed, 21 May 2025 23:19:58 GMT  
		Size: 26.7 MB (26745816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f994515d62f455ad16004599055fea85c1f2770a865b115ed127f4223e8c3946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1825fbe5843560a58ffa256a21502d84e39f841c9210dec5d074591cb746f761`

```dockerfile
```

-	Layers:
	-	`sha256:528b64fdacca13a43986cd6a12b8350a7c594980265fbc2c6da4314dd6e78380`  
		Last Modified: Wed, 21 May 2025 23:19:57 GMT  
		Size: 4.0 MB (3993560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9191f35729fd8c05e8ed6adadd9d57acd0b16adb56917cd1175ac13468b4f462`  
		Last Modified: Wed, 21 May 2025 23:19:57 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:99c920ed3667ad19ce9dc6ac05ada03cf590245fe6904488767732f2fe270ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80216129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c643720b45d30c7f78fe7a4ff36e10416b3c9451543049529d38b664272a172`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:03ebb30bb37cd398ea8ab1a268c301664089cf5a54d23466e4338782afb5f9cf`  
		Last Modified: Mon, 28 Apr 2025 21:25:28 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed88abda34c2c7766794d61fd8b43cac1ab4eeadc9f85398417820583a09e36d`  
		Last Modified: Tue, 29 Apr 2025 07:48:18 GMT  
		Size: 27.1 MB (27143577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:85932e4f10825d37ae274cfad3afceca00b017aca41b71275643c5d8109dcbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314a19d49ef6458643de65026856a1737810f9fe505d64791db36f84db0d6856`

```dockerfile
```

-	Layers:
	-	`sha256:dff5d12bcbabbaa3dc2e00e2b759be583d6703021b58fd1a6cd7d3d6a1f3f93a`  
		Last Modified: Tue, 29 Apr 2025 07:48:17 GMT  
		Size: 4.0 MB (3993659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:464151fc98e170a8303bb29d01aa714ae6a4895f6f15002e30d4fc88bae7724c`  
		Last Modified: Tue, 29 Apr 2025 07:48:16 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:5e8a6323c6da70a665a0c5413e28153899e4eccb896a92780e805a909a31b8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72649005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f38352c775944087262b83841025b54d353ec9df223192ad78af9a2823a9a9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Wed, 21 May 2025 22:36:51 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bd8670e232ca11355ffc7ddcb280e00c712f98c6d6ef1c601d041012816cfa`  
		Last Modified: Wed, 21 May 2025 23:26:24 GMT  
		Size: 24.9 MB (24917594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5487b90124b64172b4b3d78de8b5dcfb51550c1f4b37ed19ae645c9944640e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3995786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db71767e7116d80a232e4589f034c8fb7cc0c683632bd7e748dcb1ff2d4bb730`

```dockerfile
```

-	Layers:
	-	`sha256:e2303bcdbed8af296176ca76f8b7599e01489b002661f6f2609b5d1b2b3cefcb`  
		Last Modified: Wed, 21 May 2025 23:26:21 GMT  
		Size: 4.0 MB (3988933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29bd6042780dbc076d553ea25fac1ab9123c28b90ba1e9e716e1787509280f7c`  
		Last Modified: Wed, 21 May 2025 23:26:20 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c66a6d2cb9e68f7743bd7e1da2ef77c7db87a118095fbd97745f32fe93bd1eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76080001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b4691d06221580f5c9c32e241d67816f5d76f5408e4c7ba86299c8d4f268dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Wed, 21 May 2025 22:31:46 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8645228c4b06e89bef4ee7caae64a6417dc0f102985c8d7902876a160465531e`  
		Last Modified: Thu, 22 May 2025 01:03:11 GMT  
		Size: 26.8 MB (26757774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:36255b67745ead1c05946b6042f04c536df6efbd23e60ebb3c83c2efc06a480c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4011044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834bbb46505a035638d988c7819373ca265e810e1312b46cdf5a63d1bef69db8`

```dockerfile
```

-	Layers:
	-	`sha256:762de580b6a9b2edb3a75913673b034bd358822166034a7291b84d3c76880b80`  
		Last Modified: Thu, 22 May 2025 01:03:11 GMT  
		Size: 4.0 MB (4004223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2117ab1c8672cbd22c49e401d4a08c4185fa2a670856291dd82a15b5024cca88`  
		Last Modified: Thu, 22 May 2025 01:03:10 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

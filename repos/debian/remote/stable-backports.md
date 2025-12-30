## `debian:stable-backports`

```console
$ docker pull debian@sha256:71801731ccf8468a7625c54c9b27a6ff1d8b1f7fdd652fe1110781d49b256ec3
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:c283f2ce9890c4fd206c768b421824783b7235609b4d1bdab3f989927e9802a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49289806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472a964c4bbe25728fe3fea54ec2696ac5c7e6b7722108b55d3c7252615a1fdb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1766966400'
# Mon, 29 Dec 2025 23:15:43 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e4daac3383367c8556472a0b667e1eb04473733378be1e542899b71856af39d2`  
		Last Modified: Mon, 29 Dec 2025 22:30:08 GMT  
		Size: 49.3 MB (49289586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f866b90d840e4221613792a30ce071bb18e43760bec0e19ec6d75b4fd31edb`  
		Last Modified: Mon, 29 Dec 2025 23:15:55 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c9307ff18c2d97ca87a2d928af8318e3fb86ec9eadb2d5c18c2ddd4b13fff9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8506aef2c844f6a591de75e52ba02da643248ae919befd8e47ba886e873fba6c`

```dockerfile
```

-	Layers:
	-	`sha256:7ca74e9e50c84c4b3966f3413d7e1c4c1ce4c58b6265781d7b4a1b20c8a6c14f`  
		Last Modified: Tue, 30 Dec 2025 04:27:19 GMT  
		Size: 3.2 MB (3170018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:249687b300aa5ca4373d8c76d91d7cfd6f5bdc8efe788adb5aa50b5a627d8ded`  
		Last Modified: Tue, 30 Dec 2025 04:27:20 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4517baabd39c3eb1e5d50b6d1ddbb5bf9ba5d347ec9112a996cf7c4f86735fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47448993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f697ca21f93fb569559b013f8c693d461d8bffd7fe025d4daf8d1c550f6c132b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1766966400'
# Mon, 29 Dec 2025 23:13:51 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:14a0158279aa09e13720e6f5c049e063876176ea025ff723ec55fea8391c04a5`  
		Last Modified: Mon, 29 Dec 2025 22:26:25 GMT  
		Size: 47.4 MB (47448770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc59db220d6a1759ba61970b663f7e29821ec55a795869ed54077d12e581c1a5`  
		Last Modified: Mon, 29 Dec 2025 23:14:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c33013232818b16d3ebf6fa587a2c73bd6c15dfdb636f32bbfa9bbfdca625da4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01df4ad385e201e8a7fdff214f52cee089ad9374cd85df2e68f776c9db63c1b0`

```dockerfile
```

-	Layers:
	-	`sha256:e5fed7a7363cc5b40a41d4b54028711ad599851d39f35290d1cf69d68b4d91ec`  
		Last Modified: Tue, 30 Dec 2025 01:30:00 GMT  
		Size: 3.2 MB (3172955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc18de95d65c500ca1cda9f02f60964ba0eed8751861f6b642d70a64074d939f`  
		Last Modified: Tue, 30 Dec 2025 01:30:00 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:d7669256cd5a4445658106833e274a0abb6dcf27c0a032d38252b707c6acd49c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45718538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545afb7d576559cd8095525fffc075ac930f189e08aadbaf9e48322da6453124`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1766966400'
# Mon, 29 Dec 2025 23:15:12 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ac6fc173bd815aebc04ff02811f8490649995d7ca7ca3cbfa02d45a5033c2455`  
		Last Modified: Mon, 29 Dec 2025 22:27:34 GMT  
		Size: 45.7 MB (45718318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b16321e020e617aef894e6c6c827dfb037a64c246274834c99c82ba9e8485a3`  
		Last Modified: Mon, 29 Dec 2025 23:15:25 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e93010f6d7ad3c426062f2515dca742a8ae773e86cf55241e90d5a035db6a7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ad22e377ab893926ae7167b751c1a23d456556698fd12b1451b0b54730ad8f`

```dockerfile
```

-	Layers:
	-	`sha256:72e18965b5d7d9b6f86c66958a3a774845974fa466034972cb8579b763717ea5`  
		Last Modified: Tue, 30 Dec 2025 04:27:29 GMT  
		Size: 3.2 MB (3171392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d674d49cd4488391ce51ebead6b18b268acd746f13344c4cbd6e7cb0fa2afd9c`  
		Last Modified: Tue, 30 Dec 2025 04:27:30 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6fd46d5fabb261c3c72df7937fcbb39d02512cc89f23ff433ad64cb74bae84c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49650415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4777d06bb0276df9b88789eab25c85c615b75a345ad98287ff3c3e39fc83bc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1766966400'
# Mon, 29 Dec 2025 23:14:57 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3830c935b975f11e7dbe9bf4831df0b504b708ff46e43f0cb2a8e6c15c3c37b5`  
		Last Modified: Mon, 29 Dec 2025 22:29:54 GMT  
		Size: 49.7 MB (49650194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17286c39e18c5ff90ab103450b3aba1ea8aa6038c3a539903e757abea98ada0`  
		Last Modified: Mon, 29 Dec 2025 23:44:40 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7d68b002d8ae31e0047248f4a8adc02dd3eccf26f8d8dc49843b7c2c9d361776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d47928ec01098e9ed50429bcc1cda282652f0e69425285ff8c9c0237dc04dcb`

```dockerfile
```

-	Layers:
	-	`sha256:2da97af1ba07f348f605d66b458a77b4ef70f815cba8c363fb5713459c0b9e79`  
		Last Modified: Tue, 30 Dec 2025 04:27:33 GMT  
		Size: 3.2 MB (3171499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b0995bdbc78514a4a47122f194c838e830df339c02d4f8c8284b15d319eb3cf`  
		Last Modified: Tue, 30 Dec 2025 04:27:34 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:5963327e8534e3b536d54bec76c8bc04cb88d2a5c89ffddc8a4b9e75cd62f69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50801906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79646e07830b6d4a7b0f72c42d4fd9bb2e843c53f9d2fed2b016049c8238fa7c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1766966400'
# Mon, 29 Dec 2025 23:14:19 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ef70f0fa0a00f24b708c246b0fee5d6c24a59388d7d44bcaace26ae3346ff1f8`  
		Last Modified: Mon, 29 Dec 2025 22:26:51 GMT  
		Size: 50.8 MB (50801684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd5d1d052aaeca0e3fb40b04e0369aef34e0eb357b480dee7742163e9fe6abb`  
		Last Modified: Mon, 29 Dec 2025 23:14:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8ba5432456e5f9652a5e96879223f35c1f6811b304db31e5f1a5a63d73da68c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb226a0c745e64c8310a9a07200d204cab22a671a0b27d940a2bd62ef1dc826`

```dockerfile
```

-	Layers:
	-	`sha256:c322178b74ff640b22d735862f0c386a988d365c0543b98ba2acdedffb61de37`  
		Last Modified: Tue, 30 Dec 2025 04:27:44 GMT  
		Size: 3.2 MB (3167221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4dc29a9806ed9ba07f94e67311447a0ffc6322515f4dea4c50f20251dff3444`  
		Last Modified: Tue, 30 Dec 2025 04:27:45 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ea934aba171c0d5bc16131606eb04fe8a2551edaed119cae5ce17be88753db2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53108700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbaf5319ebe924d11a3704ddd2a10a06424adda06ede07789a6e3a1eabfabd8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1766966400'
# Tue, 30 Dec 2025 02:14:30 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:960dc7bb8ceb27f27553047d66d7add93947a0937e405f331adcb5af73395bbb`  
		Last Modified: Tue, 30 Dec 2025 01:50:17 GMT  
		Size: 53.1 MB (53108480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc540047c7d13e67003d1bb67887d8dc350491a25e61a87d0a31def4fda82da`  
		Last Modified: Tue, 30 Dec 2025 02:14:52 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fcdc37e226d749e73208896d97729f1e424be0ce479f82827024151f576a1f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b651db886b255593f316b4676789993465791bb3aad51ea185e57a8ceff352`

```dockerfile
```

-	Layers:
	-	`sha256:9a060590a04cd7bc245cc2d229508838f867fbc57675260f6c63a5891dee9cf1`  
		Last Modified: Tue, 30 Dec 2025 04:27:52 GMT  
		Size: 3.2 MB (3173529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9164f516f90b781bf478c7f07ea51819848ee3316816177900037ee653afb00`  
		Last Modified: Tue, 30 Dec 2025 04:27:53 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; riscv64

```console
$ docker pull debian@sha256:a1bcc75e79900893cb1ae9d70fed42383336c76141bc83c17e3b297c2b4fb6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24706a0c930c2b25d69a9e6dd889a0c0befc88814895ad305dc496d6dd1e2268`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'stable' '@1766966400'
# Tue, 30 Dec 2025 01:19:31 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e8f5423829dfc46d3b7886412fb3a4c23288027628a109e7a3c0a6b968656802`  
		Last Modified: Tue, 30 Dec 2025 00:41:52 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4936bb5144a4984da47e498a13f04f5870d6e898edadaef2dc49d658f8c0e80c`  
		Last Modified: Tue, 30 Dec 2025 01:20:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9903bb4d77c5ce897e84fe23be5e4fb1d2582a62a2e7acf22ed4a826fb9fee9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3168150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2e7a938bf099fc74ac54622d707db21ac252a6144c92cb22657ee7f4b7f1d2`

```dockerfile
```

-	Layers:
	-	`sha256:cb1a69559ef729af85ffdee129d6160de185f95befdbc1af22667dcbf662aa5c`  
		Last Modified: Tue, 30 Dec 2025 04:28:00 GMT  
		Size: 3.2 MB (3162341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a6304379357df8e69985a8b71d8b7dcb24c93be1f9d16733c654d6640185706`  
		Last Modified: Tue, 30 Dec 2025 04:28:01 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:434e2138257e8785b6b81cf22691cd0398f9adcafec736f259be6c46199fb534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49346179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959dce60417e0cdfb10d91afe7c6c58d45c365b388cabe1039b9989a9053aab4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1766966400'
# Tue, 30 Dec 2025 11:10:27 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:41d2df2988ee4221c09132a380e8ebf7c23da965c82008aae674cc62490fd4d4`  
		Last Modified: Tue, 30 Dec 2025 10:20:14 GMT  
		Size: 49.3 MB (49345957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b07a8276dcb8da5939504f23fa59c9446a6a4bbd317e314c9e44528a9328c03`  
		Last Modified: Tue, 30 Dec 2025 11:10:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:da8fd83656d2af80e39320be9abe29f36c246dfeed027d555e8d336f9b052668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c13a186bbd6db426b90c06f6d5a3b314af858be07d347df40bfeb75b4ead96`

```dockerfile
```

-	Layers:
	-	`sha256:e2312e686fc0db10b1f75d367f046851e499054c93484d9c07716523a77a12b4`  
		Last Modified: Tue, 30 Dec 2025 13:24:47 GMT  
		Size: 3.2 MB (3171465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86c6ffdb200df6a550ce61414cec27d4591352d6f7fcff5721e2753106c85eeb`  
		Last Modified: Tue, 30 Dec 2025 13:24:48 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

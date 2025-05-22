## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:f10eeed876cc0a28e3e4ab0262dbb8f1f69f39dc8ba6f79c6edc2297dda81b7a
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b8b9970d89200157edb39bd6d16ed62e41e1c351aeea0914c94c5ef0b7d4180a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74835699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3409c7c62a109f335a284c60fbe00408be41e2988cfb248ccdc66c5a7b794e8d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:21c8f2db1ca60de292da0e982c4bd4b81bfe468b8d652fac5b9003ceedf12013`  
		Last Modified: Wed, 21 May 2025 22:28:04 GMT  
		Size: 49.3 MB (49250549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734d79457730a0db09039cff8714fa8c41f073c5bed3529b5417fcd2b8736c7b`  
		Last Modified: Wed, 21 May 2025 23:20:43 GMT  
		Size: 25.6 MB (25585150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:096bb313932620853cef377305b18e3d31666176400c07ceaef78a5e5d0c86e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bcd3a78a82125e7b89aacf64cadc946e8447c5c8b3445fef7267e2798f12b2`

```dockerfile
```

-	Layers:
	-	`sha256:d7575a5c3eee0480e15a479850c98547355e53a193e83e49b398098946e4c1ad`  
		Last Modified: Wed, 21 May 2025 23:20:42 GMT  
		Size: 4.0 MB (3996437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dba97c1dca66e3650e9ce6956c2e81214a2fd305a21de27f7a0dc02250f69fa3`  
		Last Modified: Wed, 21 May 2025 23:20:42 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4efc4a237ad35b80ff91ca56dd86ed360edf3ee8b60c4101a23a26e9c5f94298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71766422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ba10f3f35c0fc72e22c3c4060bf011cbf9b61d0697220d456362851deb11aa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0f211461130ff11866a85e649352ceeb2f6ebc110118114f92b30349c5de358f`  
		Last Modified: Wed, 21 May 2025 22:28:23 GMT  
		Size: 47.4 MB (47442893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390184f3e2aece3a9d3a8380bf315948d0d62ca40bd766f23543d583f330b82a`  
		Last Modified: Thu, 22 May 2025 01:14:31 GMT  
		Size: 24.3 MB (24323529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e103a1b526f1ddacb17397861519a211c067be4a6508b584541dc6bd17b46706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4012652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97830a1ec193c120aef8cfca76a16927e94824d95719ccc91931215717a3c1de`

```dockerfile
```

-	Layers:
	-	`sha256:8891b0c5fdc075bf6d4f47b9fd6fac876e210556d79a8c2c324967a3531724da`  
		Last Modified: Thu, 22 May 2025 01:14:30 GMT  
		Size: 4.0 MB (4005791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40477a362eca4d8c357b3dee9697057c200b896854de22a22f83dd6127d3d452`  
		Last Modified: Thu, 22 May 2025 01:14:28 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1462ecdaf1f80ea6299f72b7f24cd2fc1085e5d135d00bb1c15117c8c48ace8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69288386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de4038123052ff39549b1543dfc64d086b9d53352dafa99d5a88ec546c7ba6f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:766cbe9ca16b5ae7e32cf18657be459754ce87056cceebf6831ed9c18fd8a62b`  
		Last Modified: Wed, 21 May 2025 22:29:51 GMT  
		Size: 45.7 MB (45698630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b248e723f972fd882067b040659dac6bf0007c9489588821ca8240ce91487131`  
		Last Modified: Thu, 22 May 2025 02:29:17 GMT  
		Size: 23.6 MB (23589756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:60c3615fc6e9125883b8253f01f9e9c828e161b7e02fd4933ea45565c243e7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c1091361550cb9b2cb26f5ab0103db43da4a5451786321fe56e4246519f421`

```dockerfile
```

-	Layers:
	-	`sha256:2bfbcd98e5cbf3590285398178b2b73851bc0ca462fc18ec506cc7e95b95f408`  
		Last Modified: Thu, 22 May 2025 02:29:17 GMT  
		Size: 4.0 MB (3997930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477b78f74185b49abaf38c673e5adbbe94ac5ac0b0ecc31366570aca1b2c3547`  
		Last Modified: Thu, 22 May 2025 02:29:16 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b78f989028c2c93ea81827a11563c39121dbd4583eb4eec119c095cd90def747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74593899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4494982ae30620e19904cabe26b1f716f940f723c3b746851aa9fb46b1d8b0cf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4d7c750dee99fc4f87ba2d4a7a97efd437e614ec9079e7fbf547ab9ce640bc68`  
		Last Modified: Wed, 21 May 2025 22:29:21 GMT  
		Size: 49.6 MB (49617866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945b158d051d6fdc917c4a2f2c9c640867150d5c68a1439dd536c0ff065f9eab`  
		Last Modified: Thu, 22 May 2025 02:48:22 GMT  
		Size: 25.0 MB (24976033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4903b50d39e515af980eeab4a89cdc0212cb25030a0f00bb08b0de6502574634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8437dfda8103c0cd47f7e8827d9cf524d6ba1f7876a3c530e01d547419267dc`

```dockerfile
```

-	Layers:
	-	`sha256:f810e6056517c438079de557d26fd0dbe0f4a6dfc75638e8777585cf46239692`  
		Last Modified: Thu, 22 May 2025 02:48:22 GMT  
		Size: 4.0 MB (3997967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1d0337d2cf128132d6c0d9af576ac7ec4e5a16564645bcc6382a6295925fe4`  
		Last Modified: Thu, 22 May 2025 02:48:22 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a1be225f919f1dc68ed61d20fb7b684b612313c662d09e5ade30a7c6422dae62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77505847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740557c799cb9fb37dfd29ada9533e561e19adac5eef78d763323c2483154b17`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5c296d6dda96e0fb26dc4760b3366cec8a0723558334f5c902e1c373d0e43ab6`  
		Last Modified: Wed, 21 May 2025 22:28:10 GMT  
		Size: 50.8 MB (50760379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a77ccac61e5d039233fd2cf7db2ad5fed48827a001629e91bc009eff166aeb4`  
		Last Modified: Wed, 21 May 2025 23:19:45 GMT  
		Size: 26.7 MB (26745468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e80c94113406fa485bb1ea6f242454470d1320013131df4995c5d0e59ca1ceef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea4b98ad30680179e06c9e7c60ce3f551ecb310f50d627817c862c2050135c7`

```dockerfile
```

-	Layers:
	-	`sha256:cdc7947e2510dd2792e4a13399f8e26cfd8a15eef16923c2e806b2956d62d3e7`  
		Last Modified: Wed, 21 May 2025 23:19:45 GMT  
		Size: 4.0 MB (3993556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2037a1ffec1894a6074050befbe29a6425685ce2c71a66ed6f984f4e2068f8fc`  
		Last Modified: Wed, 21 May 2025 23:19:45 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4f63631b8122a3c491e666a920312be76cbc4a816fe371b0a14223ef1e010f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75153216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5252bc5c4e2e64ed4ac1b4c6208c215958b8bad10cad810ed68ae21f22e011b5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5d206785716d2e915433eb85845aaf9607094981ed3c32854f9401982e23a7af`  
		Last Modified: Mon, 28 Apr 2025 21:11:40 GMT  
		Size: 49.5 MB (49535121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d46b0656b2eaf48d740fb0cc28ea93ea835c76c41dc63d12f18a3fd227d3d57`  
		Last Modified: Tue, 29 Apr 2025 12:45:17 GMT  
		Size: 25.6 MB (25618095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1eb22788df5278714410643bcde5c5b8a8a33b2596944feed9a61121a5b12e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8e5ebb05edc6d9e8b9d4d6c47cace35c0362a0925204e3ef15a98d47a75bce`

```dockerfile
```

-	Layers:
	-	`sha256:56a384a3fa31022d2b3ee7cc45e0d48ccb71e0b3e093d0cac7cd2c94fc230ae5`  
		Last Modified: Tue, 29 Apr 2025 12:45:14 GMT  
		Size: 6.6 KB (6637 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d916505fd9629d53a5ba338e57ce1e055dc1310f11dc3d1ef85701b0465f9473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80038340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26813e88aae6e4da01a654c1721071112914a981436bf000496d3f48cf48e64c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d320c0b02fe20eeef6a5432aed2b294506f621139378d9f899d155d81d1080d`  
		Last Modified: Mon, 28 Apr 2025 21:22:39 GMT  
		Size: 53.1 MB (53078100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e713da9ea3255a6f791030cf59cd9bdead64cd96fffafbed2a4a6fe1aaeb2b4`  
		Last Modified: Tue, 29 Apr 2025 00:38:55 GMT  
		Size: 27.0 MB (26960240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0431bc5585e61cb1d616cf16e59e5c6fffa7fccc7f288e7dceae03311274214d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722c3b01fd5a7b5d42090f25c172ef052d954180666f8924ddaac8fbf4f9289c`

```dockerfile
```

-	Layers:
	-	`sha256:242bb3225b254c8fdf84a87808bbbfa902a63706f72753abdc42c0faa8bfe3f9`  
		Last Modified: Tue, 29 Apr 2025 00:38:55 GMT  
		Size: 4.0 MB (3978746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8b2ec3b7d59cab72f07531f7e988a96cec555f4c2313880c70c572c566ee315`  
		Last Modified: Tue, 29 Apr 2025 00:38:54 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9c9ecde103db515563a684e0d8379b58a1fe32d3cb98a32c84e3b397ba47dd5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72652952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3650f9f2fb2509b9bee7771faa3dc5292a00330a7b4719653e14500b82424f00`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:70274c6f176412a652733a045be62228bfceb31afa5c428bc73eb440514be7e5`  
		Last Modified: Wed, 21 May 2025 22:29:51 GMT  
		Size: 47.7 MB (47737557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db4d1c372b0a8bcc5558ebc33a0807a079cce1bf7f64840912ce33adbe79d6f`  
		Last Modified: Wed, 21 May 2025 23:22:57 GMT  
		Size: 24.9 MB (24915395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dcfdae090ceacc8bd43f613448238c3d1f073c56cb3b5c4edf8d796250d94d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3995765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df61acedb89450f8e7019da3954eeb01eae0fd02060724ca86b0b9553ceff0be`

```dockerfile
```

-	Layers:
	-	`sha256:7f20a9ca225f6318e0f3e7240126f72ba91349080314165ef7be99be5bad3bc8`  
		Last Modified: Wed, 21 May 2025 23:22:55 GMT  
		Size: 4.0 MB (3988929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6d2b740cc5348b566b212a5e9a17917a30c0394bffd2cb451d17fefbfadf483`  
		Last Modified: Wed, 21 May 2025 23:22:54 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8bd6a909695a017cc5b20588c373fedf24a6fafb80eb01ba53426e35dd03fb79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76079055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfdd5e3ca77617c4f0cd24f47a87ebdb462ebc1f50ce53c1302842caea9c844`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:719077674b144dec5ce39e78bd5eb75fa6363d159411371db443b10356484cce`  
		Last Modified: Wed, 21 May 2025 22:29:06 GMT  
		Size: 49.3 MB (49325662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f279b96ed4b6a4d60a4f4cae771f06c0b94acf2fcdaafdb528c367ec96583697`  
		Last Modified: Thu, 22 May 2025 01:02:36 GMT  
		Size: 26.8 MB (26753393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:52abd8c490412eaab95b37d35751a649e7ae83031b58c02a8b10c1004f2387e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4011023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2817033355e96fa1eb66e79a00ce11a46852bd5c2630aecbc414adc460a185`

```dockerfile
```

-	Layers:
	-	`sha256:2587dcaa707777996e437a4ba76dac01cb03c0fb8e6db5cae182845dfbbc79d8`  
		Last Modified: Thu, 22 May 2025 01:02:36 GMT  
		Size: 4.0 MB (4004219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8605d5642214152ced1b4c192e7a31de9718acbf6d057b2c357d9cb56db9722`  
		Last Modified: Thu, 22 May 2025 01:02:36 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

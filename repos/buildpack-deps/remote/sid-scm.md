## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:bdf7d793b6acec846a1f92795340827a0eef3297904e5a7eee23861a927c27f8
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
$ docker pull buildpack-deps@sha256:c81ea13513283228c5f96f4f3bb7e0608b3d5bd66d89ab64bea218f21e86c846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152504712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35476300a133160beb3b92df9403b33d8265c0968ef2327e4ce6dd17363e96c4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:02991db6507c0026c404c68dc35ba4f9c80895d9d7fc4576cc1507337d1b4eb7`  
		Last Modified: Tue, 19 May 2026 22:36:41 GMT  
		Size: 48.7 MB (48712012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaab406cee21a5226773a482e38ac91869a010b6b5a398856bb12cca4e8f5c66`  
		Last Modified: Tue, 19 May 2026 23:23:35 GMT  
		Size: 26.9 MB (26893097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751e3a290aac34d6c988f9b5828c1d5f042f85c5e0d94ffdd846e594866d4adb`  
		Last Modified: Wed, 20 May 2026 00:26:49 GMT  
		Size: 76.9 MB (76899603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b6c34d895e11c205b3e9a38693cdf2718828ace1d6112f7a4ff91943bdba4f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8271449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e329485a28f75c6d66b169ff5e08d9eeae2ce0371dd68f474a45e4c3822b146f`

```dockerfile
```

-	Layers:
	-	`sha256:3aae0a2a342ed7fe7dae521409bcbdbca2697ec24c85a9f30910d7943e3798cd`  
		Last Modified: Wed, 20 May 2026 00:26:47 GMT  
		Size: 8.3 MB (8264195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e61b23d585bb15d2b22a08255eccf7844a94dbacd976d2008991b91edd31206`  
		Last Modified: Wed, 20 May 2026 00:26:47 GMT  
		Size: 7.3 KB (7254 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:18a99427b5c57fccf0184ba5edff4085d61ba3179303c8d67bff0cce228ba4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141641400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f14065b0dfdb3ccbacb03ae5cab045aaa7a2da9d06cea29b719b615ebea777`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1779062400'
# Wed, 20 May 2026 00:04:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:34:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1c98d9ac4796e25c1d81c99407f882de7bda76effb4d3c6a5d937bf755cc2313`  
		Last Modified: Tue, 19 May 2026 22:36:23 GMT  
		Size: 45.6 MB (45618956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1515c975babc2c0d71d5cf9a3ec0808ae1a576e22e50913d437d07a60ef65f`  
		Last Modified: Wed, 20 May 2026 00:04:13 GMT  
		Size: 24.6 MB (24603114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5553a007241b1597e7b47e09586bcab8915ab176f1b18c717170ca0fcf73910`  
		Last Modified: Wed, 20 May 2026 01:34:41 GMT  
		Size: 71.4 MB (71419330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6da84a5da78f1d2f2240767d627ce86faa434722928d0512b9da544c9564b795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8271417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537874cf08efa65b9fc07cb5a869d02de8d36267709a4cca5f2a3cdd1dfda66e`

```dockerfile
```

-	Layers:
	-	`sha256:f93a9a9f6846985fb3ec8e109a2dba06e965187f9455ce87ac8786aec3249ac3`  
		Last Modified: Wed, 20 May 2026 01:34:39 GMT  
		Size: 8.3 MB (8264100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b9423b81a9bb8eb64ef96e070fa2004badf0baf95a09b32578e9387a60d47e`  
		Last Modified: Wed, 20 May 2026 01:34:39 GMT  
		Size: 7.3 KB (7317 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4e6fcbf07ec6e6d0a9c16725ee106a2a111512f3bc34b23dec2a17dbbe4a3d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150974612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ec67bc82e8859d8f57880ad08f88cc68f2e803341a5384c644660d38de9171`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:26:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c2bc0682b6790aa6b6a3a5a7933e32ea4a35d72d531a3c53509cd76aae83fc88`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48737609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab26ead8a9a9779bd1e4fbb72a954ed83ffbb2d9d0e5d585eb545c5b6270c442`  
		Last Modified: Tue, 19 May 2026 23:27:06 GMT  
		Size: 26.2 MB (26170738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4f42b49afc591850a47b31466ec9e30deb1aa59f61962edaa6feaffb6924ef`  
		Last Modified: Wed, 20 May 2026 00:27:51 GMT  
		Size: 76.1 MB (76066265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b61ae354d08eb161826369abaa9e9c2059499673a851aff1b8b932c808cc8cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8283031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e550ddb7715df894773c6888e56d9d64679f42347796c08e4d892debf9cd8b82`

```dockerfile
```

-	Layers:
	-	`sha256:dbcaf350fb7b077583bc1cdc96fc2f16c39fb584b33daad4b051f2815cb28694`  
		Last Modified: Wed, 20 May 2026 00:27:49 GMT  
		Size: 8.3 MB (8275697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3f11e1e622d372186fe253869d86810e5fc2da709ca06cc99f1cd7ba528aef1`  
		Last Modified: Wed, 20 May 2026 00:27:49 GMT  
		Size: 7.3 KB (7334 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:bcd2fe77e8362883dbe7939c058d62984731f700d46f8fa2a47f00fe0305f62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157353613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3048bb1403264e06cd5d19b2fca14d2c43c0187f2653fb64f1c3537b9be4902`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:45:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:506409f9b5466021b987fde6d84a8bc529520e50798929836cef94e3223d354c`  
		Last Modified: Tue, 19 May 2026 22:37:32 GMT  
		Size: 50.0 MB (50016004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1f3d5431169cdd29adb39f5cf26f13e071f7217f28223b49e250857b02be6d`  
		Last Modified: Tue, 19 May 2026 23:25:28 GMT  
		Size: 28.2 MB (28209479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62d0bd46ff0533780d2f77ff103a5c122ca383e8dd50cef1106912fc2d9dea7`  
		Last Modified: Wed, 20 May 2026 02:45:54 GMT  
		Size: 79.1 MB (79128130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c73b55c7e30f9bf159a98549b2c24e0c269952e402f3eb40f062bdad2a99f2e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8266917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9728a36f7accf8708f8c788d0c47d6f30d3cd041ed7ad46c871f2d34a7d5511`

```dockerfile
```

-	Layers:
	-	`sha256:140cbaeea0fecedc4757cfa8920adef0fc4ea6c0491cb45f336a4343bd49ceb2`  
		Last Modified: Wed, 20 May 2026 02:45:52 GMT  
		Size: 8.3 MB (8259685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ea646de6a5690a95a93e39226a9baf3bc73639dd2beda2f9a207d47d40edd9`  
		Last Modified: Wed, 20 May 2026 02:45:51 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7b89c0c33bfd5abc98ad23ec1ba8b9b9f5ba109c9d3615ebfe69c423b63d1c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166772073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3048b6f7a3ca55eab3398364a012d0a5c3e4ea44505baf5c7e4eaf9f548640c0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1779062400'
# Wed, 20 May 2026 01:14:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 06:52:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0bda88a8fa865607f7a3bfe01b25fa99681c2572077bbfaf6b7e16e1f51b5b50`  
		Last Modified: Tue, 19 May 2026 22:36:39 GMT  
		Size: 54.0 MB (54046122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ac92e3c123ea205d76f5d82b79747aea7ae5197399f942393a1c3ea0ec0034`  
		Last Modified: Wed, 20 May 2026 01:14:34 GMT  
		Size: 29.3 MB (29285530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748f4090d3ef4e4805f871375fca40276f6e550a6f99e7794ca38dfdacbc423a`  
		Last Modified: Wed, 20 May 2026 06:52:52 GMT  
		Size: 83.4 MB (83440421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dc6263c24c1343a3f2d35339f4a7ef7e27b4a9860445d174e79a9b50d445faa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8256425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ff1aea8dd34cefbaedcdd10d503dc34bcb1dbccdca8957c56cae6d80d38c64`

```dockerfile
```

-	Layers:
	-	`sha256:4de777861e8757b6b605ff086f8ee28bb3b55e44d1c8b6f7bad16327d4ac7f3d`  
		Last Modified: Wed, 20 May 2026 06:52:49 GMT  
		Size: 8.2 MB (8249139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa2d1956218682a8c7c4ff7747fbe0616bc8526f117a4c9bcfb74208ac43549e`  
		Last Modified: Wed, 20 May 2026 06:52:49 GMT  
		Size: 7.3 KB (7286 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:92a08c10eeeb210a05561cec750849521999a13293f0ee2d36d050de11e51a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148605270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60a5978fccc8fa704dc1da9d5955722be336010632c3f58c825321719c1b42e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1777939200'
# Mon, 11 May 2026 00:52:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 May 2026 00:41:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:291921d355da34dfbce324263312328392c6a6c78ee971f9b4d7d37f1527cd2e`  
		Last Modified: Fri, 08 May 2026 20:26:01 GMT  
		Size: 46.8 MB (46838649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340855859b1344ded89a6e027caa6be811a60e26a4f08013b27235c463879b0e`  
		Last Modified: Mon, 11 May 2026 00:53:36 GMT  
		Size: 26.5 MB (26453358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5edc8a79553eb62a40d99b38aaa32211fc341a1f9cbd23a6cfe2581ef0fd704`  
		Last Modified: Tue, 12 May 2026 00:45:17 GMT  
		Size: 75.3 MB (75313263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d5c6f7b824d880e3a468dc7a1947b4a90dea4fb0f7eb4a4ad16d79da03e5b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8266649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c8c871ff831a14d6dcae5404d23df702d19579d2379ff88a5e2b88e3908140`

```dockerfile
```

-	Layers:
	-	`sha256:5a99e4460f43613856645494c5602ee26e5458ff787f391170bb050985336be8`  
		Last Modified: Tue, 12 May 2026 00:45:08 GMT  
		Size: 8.3 MB (8259364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfe195eaa633b634643a6b7e6aa3d6b8915f76c91cff1cc239c647ae5d81ee52`  
		Last Modified: Tue, 12 May 2026 00:45:06 GMT  
		Size: 7.3 KB (7285 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:050a16303247a37c197a460d46e43ec07688c98b2ded6561379b75a57ce31121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152570633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d624d05620c77aba6acf4e9b1fdc09b628ab7f6e262afed97bc73fce54bcc07`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1779062400'
# Wed, 20 May 2026 00:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:05:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b2de0004fb71a1e4abdd27d0619b3567a865a43b4039f4f3ca7e11b6e7bf8ca5`  
		Last Modified: Tue, 19 May 2026 22:36:09 GMT  
		Size: 48.5 MB (48454253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558e98e58fdd0e7e9d312d1df7e45d14fcbde914744efb8b87cc091a75f459ef`  
		Last Modified: Wed, 20 May 2026 00:18:56 GMT  
		Size: 26.7 MB (26690815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bb487184dd43970e32613d936ce72502fa8f8c5f662aad3fc0ef56ac0b146e`  
		Last Modified: Wed, 20 May 2026 02:06:15 GMT  
		Size: 77.4 MB (77425565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4b35a8aa98de2be3faf3560b24b90ebeb2d6a202935150723dc24cb337f16c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8249302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df912163ece63088ce5bd696ea2875850527d6383db585afb1045ae978fe1997`

```dockerfile
```

-	Layers:
	-	`sha256:90b6ba49fb2026db24d59826861ce94322ac35652f7056c33c7697178b383d32`  
		Last Modified: Wed, 20 May 2026 02:06:14 GMT  
		Size: 8.2 MB (8242049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbbb2ad03a992164325b60809a5c0d9006cf2865c1f2b89c997c1e48bbffef65`  
		Last Modified: Wed, 20 May 2026 02:06:13 GMT  
		Size: 7.3 KB (7253 bytes)  
		MIME: application/vnd.in-toto+json

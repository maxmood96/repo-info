## `buildpack-deps:oracular-scm`

```console
$ docker pull buildpack-deps@sha256:06dc9bdc1ea4cdba063beb10ef1469f746aa67ccc9f8f0c145cbd2d16b02c7dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:oracular-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8a361675fd8b874cdd20671feb035f1f3ce52c1891cf7d9b690ed1f32db73182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92810891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea18b3deebfc59d5c0571e1615391a656c1d8c0c5858d56250747d08d119d21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:73f6e57f4af4f06e7be06f1e898a5b2b2404356c0a780d312160801798914622 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ddbef59e0ea0a03a6305017a7cbc1c5aa0887589d1467bbdd2988076e0a71f65`  
		Last Modified: Fri, 27 Jun 2025 02:02:31 GMT  
		Size: 30.7 MB (30679690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfe4dee91a3a393d84f459d4b964780cabe6e6839eeba3094a6e433668d3119`  
		Last Modified: Wed, 02 Jul 2025 03:10:01 GMT  
		Size: 15.4 MB (15395530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49adfd89742ab9a90cedcaadb3b1bf234e2908e4289d1fdfe1e028104ad1ed`  
		Last Modified: Wed, 02 Jul 2025 04:11:47 GMT  
		Size: 46.7 MB (46735671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6cf3d689188d84460786dfa7a15c7dca61b94a700efd759a2f96c127e4ca0e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5295851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d77601fcc52f8f2cbabd39aa186b20122ce9c570098b91cee5baa5538806e2`

```dockerfile
```

-	Layers:
	-	`sha256:44efd7d368218dd3d5943a784950948980897d6c96f3017ff1ff45e4b202fb83`  
		Last Modified: Wed, 02 Jul 2025 07:20:20 GMT  
		Size: 5.3 MB (5288527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e2b7340b1c749ef84fe5ccc25e7e0a31bb2f202e4ceb58273ffb54dd4455216`  
		Last Modified: Wed, 02 Jul 2025 07:20:21 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b9e79e4878422b6bd6d6d33648c40f3aab82d7f7b7bb709ae3855163974e601d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91111762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe45fc8ffc800fa59e5b259f28d4258439654a5c79976d46b10d7085560bba9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:d7cd86da978be9344bc3884949ae28fb5a1546ef9ddefbbffee312a459a6c663 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2eabd78563fdf870a2778760b77a21198d44cc94c7327710db3d781fc126036e`  
		Last Modified: Wed, 02 Jul 2025 09:17:24 GMT  
		Size: 27.6 MB (27571857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b62f06ca381285e9e2a855fe4f33e4ebbb2d9001384c835fcf1c4b47adc496`  
		Last Modified: Wed, 02 Jul 2025 10:22:18 GMT  
		Size: 14.1 MB (14061913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d47500d69eeba4c28901c9ee3223bf9a9caa587a053919ee5599db65684b5f`  
		Last Modified: Wed, 02 Jul 2025 11:12:13 GMT  
		Size: 49.5 MB (49477992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b1aba739c5c4fff25683cf1a36faf68b95b2a7a29e5513bd3cbc78cfb60424ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaff298b12778ce85e14d62bc84b59387be335d98fb222b6bd4eaa0bdcfe74cc`

```dockerfile
```

-	Layers:
	-	`sha256:cfb64978b2f895a15c31c649769b9c83e05a8510e00fb64f3bc87c117f84c24e`  
		Last Modified: Wed, 02 Jul 2025 13:20:05 GMT  
		Size: 5.3 MB (5289831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581386fbc42bfb82325addd73a468527c8dbebfa00dd2261bd830fa7f2885421`  
		Last Modified: Wed, 02 Jul 2025 13:20:06 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a4b8220f55364f75e9bae2d5a6b885ccc93276824599919a2716ba94154aae53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92119363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f32978a4ae8d2f601229b9ea86bff3948f21200eab8305f22bcae4cbf8f479`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:141cc31a669b0cb379998fadb16bec2f2802a6b1d7f5b2451953d017f58564e5 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c622f78cc3b59916d6c50ebd4442e404ba82d4225c20c035e8c73a19a54ff060`  
		Last Modified: Fri, 27 Jun 2025 02:02:32 GMT  
		Size: 30.4 MB (30352874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e78288abc89f5c7b878d2a70a18e38384119da1408d98a3c1b9df9fdf911978`  
		Last Modified: Wed, 02 Jul 2025 04:20:17 GMT  
		Size: 15.2 MB (15166982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b3866d50f29eaef435b63dd8b6c58db79f4b5dfc3d20a0fce1f905cd424042`  
		Last Modified: Wed, 02 Jul 2025 07:38:19 GMT  
		Size: 46.6 MB (46599507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:204c9c93749ce71c0da18dd1a6fdc4f6f4d7a3391b78f0057d54e4ad26a7b0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:203c786c455813ae4dba1bfcd745e6e414e902371d74c2da271aefcc64d79e22`

```dockerfile
```

-	Layers:
	-	`sha256:f101441ce0a7899e12503a8ab28f21b32b1e5f43a384e2c86985c26492c315c8`  
		Last Modified: Wed, 02 Jul 2025 10:20:01 GMT  
		Size: 5.3 MB (5295716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8c516b70e28334aacc80d8332cf390f11fbac677c4429f15c0417918763d43a`  
		Last Modified: Wed, 02 Jul 2025 10:20:02 GMT  
		Size: 7.4 KB (7404 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0f58ae71fa2899b57d7a176bbddd08150dedee35144f2178d09ece51f3495522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104299144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09031a0177835310829dbfb05984e0a294de634bbe111ac25098e342eb08cc0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:176c756672705e33e9bc6ceb5378185488062110b00b19ff96c5ddf8406b5c0f in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:989df74a5080626482e46999f13d3a2afbc98992fcb052f143d4de56a113c188`  
		Last Modified: Wed, 02 Jul 2025 01:15:14 GMT  
		Size: 35.1 MB (35136598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534482ca78648ccb3717c86cd7f8ab1fffce2b34509ff35e4d179366cb99d953`  
		Last Modified: Wed, 02 Jul 2025 03:11:59 GMT  
		Size: 17.3 MB (17269959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05b8d99e376e3f1e08ec554cae1483abb78ad6bb933e78b5a8d14683f74e781`  
		Last Modified: Wed, 02 Jul 2025 05:12:29 GMT  
		Size: 51.9 MB (51892587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:997c0e02f79a8890e3c85e69932d2a3e8a57580706dbca8d426e134472f1e664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e62238786846448988276e652fdc63fe33fd3f8bf58f24df1a82eea105f9117`

```dockerfile
```

-	Layers:
	-	`sha256:8b54b3c4b6f8a5de0df130947e9cd3be87cdc348df422cb13ec8ef8b45bb3443`  
		Last Modified: Wed, 02 Jul 2025 07:20:40 GMT  
		Size: 5.3 MB (5296399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a10c40004e0c6f64ea7ca3ff59b27974d6ac6a47e75fb46a84f78e51008e527`  
		Last Modified: Wed, 02 Jul 2025 07:20:41 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:72d7b0179a1a4286e7e3d4e1dab3fb9be18b6fd24e1f2d5d72419162dec9a468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102366936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9f2eebcb5a2b1fc85461c26371b7587ce077e1e1f30f1b04cd1364cb5b4e4a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:f50c324800ca2fd46eb5fa6a9241f99c4a240e761a0db286d0056f34986108ea in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c47eac20838722cbb54e617e73f13e22ae46725099dd62b266ecb203f5d58d2e`  
		Last Modified: Wed, 02 Jul 2025 01:19:20 GMT  
		Size: 31.8 MB (31817194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db293af67a6fc7562117a76fb78b63def10d91907bc0b40f15a3c8018f150723`  
		Last Modified: Wed, 02 Jul 2025 13:31:23 GMT  
		Size: 15.9 MB (15890507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439ea827b0c9b72319966f83ccbc38c55ceb90dbe2dc7d9aab705310f74ef38b`  
		Last Modified: Wed, 02 Jul 2025 06:33:52 GMT  
		Size: 54.7 MB (54659235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c848635fd2d075a929dcdb5f54f379c7093030f522457df178fde0d2bb04543d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5287094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52855a0bf5aa5cfa8a49a06c89755175f54f6574ee5f8dc30fa37f916c016f75`

```dockerfile
```

-	Layers:
	-	`sha256:7c568d28e6a5b3414b10ae38d3877e70d25ba2bf7160b0618e67b34fea49e3b0`  
		Last Modified: Wed, 02 Jul 2025 07:20:45 GMT  
		Size: 5.3 MB (5279738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8304c87c44972874d224bd1fdaa26750035f58a3cbfe53620172641c2ea16a3`  
		Last Modified: Wed, 02 Jul 2025 07:20:46 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:892f5b9135692d09774926582454dbfe566845619dbb8d5d7c51f5af60184a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95958438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233d6e366bd644504a9ea116c6873a8bccdab215ceec3fafac5b1abed371daf4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:eaa386b9e68958f8ab5d8a86b7cf97bf8b861ca9a5b5e3bb944b7ba3a2c0eb47 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:17291234c83d72533c1476784cc72e487b936acde473238d2149baa0d74047f9`  
		Last Modified: Wed, 02 Jul 2025 03:45:00 GMT  
		Size: 30.8 MB (30836304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e2454b555b91662f9d3218b59309a2a774a85aa187dd4d9357917326fae122`  
		Last Modified: Wed, 02 Jul 2025 04:13:59 GMT  
		Size: 17.0 MB (16958553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5aac16fc5f9e7e300d8eda560398cde7c04b2852ef41e0e944619d0fea2613f`  
		Last Modified: Wed, 02 Jul 2025 05:18:52 GMT  
		Size: 48.2 MB (48163581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:768ba02d4146360a2cd520c695b72c1a98845d5767fee809386faa94a96b3a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5298180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8975555734cf8fc850440537280a47d47248850b0c49a6b9bb170feaf416b1`

```dockerfile
```

-	Layers:
	-	`sha256:8369daae4dc7c2d9491a7876c56600e2603fb5569148868e5e32f8c755281e34`  
		Last Modified: Wed, 02 Jul 2025 07:20:51 GMT  
		Size: 5.3 MB (5290857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd194da67f965299846d4802433aca211f3f704d2acb2e6cd6beea9ce45c079a`  
		Last Modified: Wed, 02 Jul 2025 07:20:51 GMT  
		Size: 7.3 KB (7323 bytes)  
		MIME: application/vnd.in-toto+json

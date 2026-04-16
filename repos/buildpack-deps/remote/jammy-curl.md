## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:ebe99874b14af7441e823710ae9a8fc303a56d37c28680134197bbc9701c8710
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

### `buildpack-deps:jammy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e034890b8927a806017ee40941ab2c42483aa191d21f19bb803652d8e6fae2e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36842888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7992864134b7027d69ad5661a14965873bcfb053f03e17b88ea084737bd9a384`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ecec50759c3bd60116bddbffcebabb3dcd76303cf36ce83784b5ba0cf93040`  
		Last Modified: Wed, 15 Apr 2026 20:24:53 GMT  
		Size: 7.1 MB (7106390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d12fef80439f89c1101b94c03c5242772e05c52340b221cadf32f0432be50772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3212096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c42f9e9a09aa4fbcd395bbc4c5d773156c111324cd0f4b7c66755f2521c6ed`

```dockerfile
```

-	Layers:
	-	`sha256:22d9cd72cbc6d7eaaf3a1aebefba370855a7d674c98f395039b4a1d6abd4555e`  
		Last Modified: Wed, 15 Apr 2026 20:24:53 GMT  
		Size: 3.2 MB (3205215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c41020868d7ffc8c12709f3a19a953bfd0a2cd72a0e404e5c7caa73f38939986`  
		Last Modified: Wed, 15 Apr 2026 20:24:53 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:65c7fd00fa8223685c8ebd7774b443ed7705c935f44c8b32b38ff3f663155e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33852236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b044bc8c992b3ef8ae5e082e958df7baaab5d1e8ab57825def2a212bdc1b14b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:44:44 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:44:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:44:44 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:44:47 GMT
ADD file:cf79b3b81bc9aa60d93ec4cfb803894aca6ed3d1e7c9ed02435158c6c0de400b in / 
# Fri, 10 Apr 2026 09:44:47 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:31:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f1c61368409f262f2b51173bb83056489f63f356da65ec1d7227c4451afc7ff0`  
		Last Modified: Fri, 10 Apr 2026 11:01:03 GMT  
		Size: 26.8 MB (26841687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ea175a59e4f7f510d8b43574403d0483cfe07a859f9c54ff97760dc3b0b09e`  
		Last Modified: Wed, 15 Apr 2026 20:31:20 GMT  
		Size: 7.0 MB (7010549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:039896faefc2f2a40386035144363c9ca563fe8e79d266f7291b4d0c02a7a959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3214467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f4bc3f759fe410b880b1a2628c68cb130ca49282e93f2fc8a0eac4fac143f5`

```dockerfile
```

-	Layers:
	-	`sha256:b4907caf1abbe72cf11eabe8f8c6e513bc7a596354d95be37dd5b364798ea5ae`  
		Last Modified: Wed, 15 Apr 2026 20:31:20 GMT  
		Size: 3.2 MB (3207522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1cead1c7a94be3013102864eddec2319d3dc1b20f9f6bd7ec365d0ac3753ea`  
		Last Modified: Wed, 15 Apr 2026 20:31:20 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:20ae035ec13f05d715f762b656ab4385ea11b8ff4343cf1807d2e7f41d1b455a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34667670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856122bb5f7acabf37eb73434ac6cb7821c7f8b23fb9aab8b87b9a58c9402ef3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a5bc53c1a6e7cc1735f8944574d4921d9d23f26d4b1025adf1c324ad2b07b6`  
		Last Modified: Wed, 15 Apr 2026 20:24:21 GMT  
		Size: 7.1 MB (7061127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:257c39f2c14e08ff0fea7b13a9adeb44f4b5c5b9b80d7786712377c681e48534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3212443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6cb243a35e3f5c616fac508c077156e132f5ed736f9583f5e6033f5846d6d8`

```dockerfile
```

-	Layers:
	-	`sha256:777cc81d3bcd635f6f709b6b81aca38fab76e45332de6c087306679bba3314bb`  
		Last Modified: Wed, 15 Apr 2026 20:24:20 GMT  
		Size: 3.2 MB (3205482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:253e50a01807fd1e0e5cc944d6c7ab10b25c4ccb50086c3c96e969eef048feb7`  
		Last Modified: Wed, 15 Apr 2026 20:24:20 GMT  
		Size: 7.0 KB (6961 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4e18d21fc8becaab29dea999c5bd0277ea59edbd3b3c1d892d1fddf8de54d15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42834612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf5a7d7d4cc74342539cf336fe4f8f47293f62ab46e906135228b55ec095015`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5934dcd0d71e03d90a927f281153e6d3ea266863de69f95adc0ac8dc3ddc9e4e`  
		Last Modified: Wed, 15 Apr 2026 21:11:30 GMT  
		Size: 8.2 MB (8186214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bfd60ad591d1e42ce3e899aa885b639cd063c2cd08a73f02803479890a74c90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3216764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26dbc957bd511fbf022fc9aaf33f4a1d6325d49643eccc4232778ba5a4d6b712`

```dockerfile
```

-	Layers:
	-	`sha256:2dbdf8e67dbea58a0a5fb70ac340577f92ad93721f8e7e583f8d4942661f48c2`  
		Last Modified: Wed, 15 Apr 2026 21:11:29 GMT  
		Size: 3.2 MB (3209851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55430ea8f8dbcba20dd076009e4c1473f9227ee36b261013c7a2f3727371019a`  
		Last Modified: Wed, 15 Apr 2026 21:11:29 GMT  
		Size: 6.9 KB (6913 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:2b02701283d6934414af141d20c4ac7b61e796c1b3da4cd9e4f2dd86ed4725f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34359710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b34a4c4ae3766fdd396225c82f11ecfcd6a3f46193551d5194721882ea271d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:32:30 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:32:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:32:31 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:33:10 GMT
ADD file:cef4de62251709bb7b835e063bc33adeb6a0fff04ccc75dc4822972fe4b3c892 in / 
# Sun, 22 Mar 2026 18:33:14 GMT
CMD ["/bin/bash"]
# Thu, 02 Apr 2026 16:14:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8b5ae14641591653bb3f51ef85e2794ecf70f68429e0388fc2292269c97d806c`  
		Last Modified: Sun, 22 Mar 2026 18:43:53 GMT  
		Size: 27.2 MB (27241072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b600eb68ff8d6a9d6795092227c9b7a3b32cfbe3f5f5592dbec2c7605106cabf`  
		Last Modified: Thu, 02 Apr 2026 16:15:16 GMT  
		Size: 7.1 MB (7118638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c5c19b0e5899d87701aa96836a04812547b01506eb0bafcb94154ccc69b5f76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3206016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26fd38e6330023b1149776048a09dee09e54445031096d3eb5b6a63d8625e13b`

```dockerfile
```

-	Layers:
	-	`sha256:cec623bc70477f40f12209d85a238fb45023276aef7dc0ca7aa3493589906b2f`  
		Last Modified: Thu, 02 Apr 2026 16:15:15 GMT  
		Size: 3.2 MB (3199103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cc8e06351a59be031dbaeb7ad1343c92511f198bbe92f1b9d38d0c79b96f6fe`  
		Last Modified: Thu, 02 Apr 2026 16:15:14 GMT  
		Size: 6.9 KB (6913 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:adb9c815661cd4a92088e44a8a9138fb94b1e7187cac30857ca3a84620febf03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35221434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ad8417de980b3b43f8fb01583287a4b34e12338c110ec9bc9eb1c5e64d4c27`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcb2def34f87e70db8ee4787df628a5479c6cdb42d140cd23cb1cfc202317d9`  
		Last Modified: Wed, 15 Apr 2026 20:43:23 GMT  
		Size: 7.0 MB (7019135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ce77b001739922b85e9c0320e23a5fa03f5662ba60d107deda3ed7d57cbe0961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3214313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d04f148cf262848d05b2feef1e50224fa4cb38d3cced53f9f7907ca158f9925`

```dockerfile
```

-	Layers:
	-	`sha256:5b86dad3b3b9a5395d2f4ae00b8ec2d2b5927dea59e0e2523a54f4ef7e137f5a`  
		Last Modified: Wed, 15 Apr 2026 20:43:23 GMT  
		Size: 3.2 MB (3207432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65327e31be22773519c3f0e0835a182e75bd9ca94fd4caeef7dde59e7150b872`  
		Last Modified: Wed, 15 Apr 2026 20:43:23 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

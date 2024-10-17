## `debian:testing-backports`

```console
$ docker pull debian@sha256:55b8023617cffe1cae3009872bfc77aefff4bd9a13ce271f547d6eca8a2071ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:15d1ad0b202e3302bf30217df612bac4b6d9991851f98dcbc3299a2c40bcd580
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53238944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a2f961482705e8a75f4398d7926311688ff2a0d11a29de6b2b797ca1ae4ebf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:22:01 GMT
ADD file:7cd25c47cea2c8bd0960e59bbb70e07523a0cf45c77c330ba29dd0040fd2ae3a in / 
# Thu, 17 Oct 2024 00:22:01 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:22:06 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bfa02bb5331e16713de983c8b0601bfcd284f32c36808d948bf38003dcc2a65a`  
		Last Modified: Thu, 17 Oct 2024 00:26:18 GMT  
		Size: 53.2 MB (53238722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b4b2345b023d4da3abd49e93a8beb6e7029b7e4515a80dde33c1697defce13`  
		Last Modified: Thu, 17 Oct 2024 00:26:25 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:edf42196519a3509cc5125753d4f40d2db6af8ccb63c5f27e9c9753d59322c97
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50146320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc53ac3c947c4a197c3a1a91fe0db961a4afa79c37d8640c235fbbc79a5c4a50`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:55:26 GMT
ADD file:8ca508f4aa10fbbd4763585ad66153e001d58d356c8d78804db912ec3b2c26cf in / 
# Thu, 17 Oct 2024 00:55:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:55:29 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:92fc55f27ee43568f631f9e9bf8b96fc9cc011f9dd8f77d49e2f8f720ac28722`  
		Last Modified: Thu, 17 Oct 2024 00:58:45 GMT  
		Size: 50.1 MB (50146097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68dc5efe0609cceb5e9cca62079f87a7412d1880e78c3c03b3557c61a6e4bb0`  
		Last Modified: Thu, 17 Oct 2024 00:58:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:35bc2f5fc9349a2118e511bf6e683375c542d102d4f5131a5559646983a87fb2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47634156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95dfc69e370c0533767262e4da0013792647db83355fa1c793054cac0b31660`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:15:21 GMT
ADD file:fb5e39f7f5bcfbaa21f64fd97ca1564921b5d0673fe330a8834c706152a09859 in / 
# Fri, 27 Sep 2024 05:15:22 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:15:26 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e46465b055aa50600d1bdffbdb586bb40e82873206be9d67794a93d24d546e91`  
		Last Modified: Fri, 27 Sep 2024 05:19:34 GMT  
		Size: 47.6 MB (47633937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1bfd82f21bd8b8e3075adbbcb04fc275f8385136674ed2cd965a7a81f5c853`  
		Last Modified: Fri, 27 Sep 2024 05:19:42 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:66d37c7ac51aabb793d91b58f502102244e76b411ddeb2f0ca1047bd4d7ea172
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53616810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d31adecd0c1a4c1104cb37fa19adf1409e2fa357c374701b15e0009d0adc91`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:39:21 GMT
ADD file:dfa41c5a8e1c4511359423b532cb30507d2ec0cb9ef2412143a4d4a2752d2d0a in / 
# Fri, 27 Sep 2024 04:39:22 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:39:24 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:be8a7f4a2cec45419ae4d29243820f77c134b84630752f45d42a7725f62db14f`  
		Last Modified: Fri, 27 Sep 2024 04:43:03 GMT  
		Size: 53.6 MB (53616589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756750d78fcb3a79314c4780c39070bf6456c97cb5130a432771413f3e72e65b`  
		Last Modified: Fri, 27 Sep 2024 04:43:11 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:148648a084ee2265b4bf01dbdfad9f628bc680867fa696c9633d18a544874b2c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54077656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259c9f7f76997f3f10c84928b146844d4acf2e89fb066aac1c96d8508a0ba1e6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:40:33 GMT
ADD file:a7ecd48c19b46d7a871710ed2d610975d1c54151fa41fbce20c1568c6aa36e82 in / 
# Thu, 17 Oct 2024 00:40:34 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:40:38 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ef528d0513269e1e9a57e7933e2f31b93816b991227b43f1d3e56d437c4f3370`  
		Last Modified: Thu, 17 Oct 2024 00:45:18 GMT  
		Size: 54.1 MB (54077433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f9fe0bfda6feba64e4b1c72beb28f9d75b8d633bd0c1f7ea3949a2dbc4c19a`  
		Last Modified: Thu, 17 Oct 2024 00:45:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:13cdcf7e491b30a50058c4fcf550c15a67e2850d752efff9939a0547a0d0ccca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52096617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cebf04beef5d1349c4331292d535aa353f13e94d9b4c3add9dd768284af7a5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:06:11 GMT
ADD file:7a78a5938833234acfd335f8c9f0fee0472ad7618492e6ebf2b52e0031f2de4e in / 
# Fri, 27 Sep 2024 09:06:17 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 09:06:34 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a03865fda81585be80749d484803fe2bec42c5d5eb183671791eccec1893d3ba`  
		Last Modified: Fri, 27 Sep 2024 09:14:40 GMT  
		Size: 52.1 MB (52096392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b38e529c944e36bd4b0456576d1d4623eb55b21dd8203ae08dc3f08c7e34240`  
		Last Modified: Fri, 27 Sep 2024 09:14:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:9fa1498dfa020fd692f0a64918afd155409ffd79b3b77b90130e6b9636769922
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57100602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db8ffd50454b812c89e7967f9ffd6972a165ada878ee0783bd4911766448b45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:34:08 GMT
ADD file:1cabb289a72ffeb44fe38a5ebdb31c8f6a7bb3e5fd5c46b1b4132b34443c5811 in / 
# Fri, 27 Sep 2024 05:34:11 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:34:15 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4fe1b2916866944b77c438d068d2b8fa4c195832fc93b9c0068bfa8310f21499`  
		Last Modified: Fri, 27 Sep 2024 05:37:42 GMT  
		Size: 57.1 MB (57100382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91188ac5324eccf5442409c38a65cb46bdb9195da0420988aa015240a3ecdaa8`  
		Last Modified: Fri, 27 Sep 2024 05:37:55 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:11e34b42d51eacab3993b15fc4407aef6fcaf017faab042053521cc82779024b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51492971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8268bbcaa11d014bf2b96898e0446f553a13ea8fde4ab3bd26a41ef1665db3ed`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 12:26:02 GMT
ADD file:ba946654bb1b3cc05385513ea44d575e3d17bf03278c865ad9076b1885d17ac3 in / 
# Fri, 27 Sep 2024 12:26:04 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 12:26:17 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b982516df848bcd6f1ebe3e5d6de5f3d847a1d88bf1de3c2aa932efda9534c2f`  
		Last Modified: Fri, 27 Sep 2024 12:31:51 GMT  
		Size: 51.5 MB (51492747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d4de266d66f888be02025c63dd20f9f0f2876774c14c07a237e75ee4ea96b9`  
		Last Modified: Fri, 27 Sep 2024 12:32:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:8331483eca7de5fd6d73794602c09fbdcfefe0af5a1226580dcc5b04168fe52a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52771292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0beecb6c10dd580d8ac05abe754c4a4ecd9b2c759049adcad5b325cabbb03503`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:44:52 GMT
ADD file:3e39c625eaf60953d8cee79d51e2111b241d054227598d815a080b9fe676b690 in / 
# Fri, 27 Sep 2024 02:44:54 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 02:45:01 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6254903b6edc85d1dc106a3e9025a77bf951ee477df6401427b61d5e2f6ccc3a`  
		Last Modified: Fri, 27 Sep 2024 02:48:24 GMT  
		Size: 52.8 MB (52771071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab3693a9ca66aca483f81143a7c9138f7ae1dcfa75396ab3391aa67796da15a`  
		Last Modified: Fri, 27 Sep 2024 02:48:30 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

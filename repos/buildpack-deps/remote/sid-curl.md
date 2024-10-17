## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:2ae16178dc58c8343918628bba7275969841d87d8f0986964953cd51d4aa19c6
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:aafb1e03b859e522189ca725aafeb07e85f01422fe7e527b4c0c2e1d93608d80
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73831614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999051386cb7de9c2fd43d1b9ef3c5a7cee281c5f450630bd090bb0925213cf3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:21:22 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Thu, 17 Oct 2024 00:21:23 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:06:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd12486823035917e2bdfef20e61a67c184360d98ed6ebd28bb57588bf93a8a`  
		Last Modified: Thu, 17 Oct 2024 01:11:46 GMT  
		Size: 20.6 MB (20559740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:30933517776b76905a907aa358c2fb68bb1dd1bdf746c085acf787711981d99f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69716520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765641333392e957060ccab7afe0208a8588b3c93fed80b1ed7c83f4f93b7ebe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:41 GMT
ADD file:60f06c5e1590158022d322cc41b07cc01fa17e02a84be35114e99f05ec411c78 in / 
# Thu, 17 Oct 2024 00:54:42 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:27:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cdb5fb3064b38bc0e5b5aae72dad6be74503e4faee528b87f7073a8a6ce9adfd`  
		Last Modified: Thu, 17 Oct 2024 00:57:47 GMT  
		Size: 50.1 MB (50147588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b51e9513f401d905da66d3e959803693c1c78e3059a3fd54de6ad45f59179fa`  
		Last Modified: Thu, 17 Oct 2024 01:36:39 GMT  
		Size: 19.6 MB (19568932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c780efb80814d59b9b22eda9132f837a432f5408e965f9997e2370cdd42e43a9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66588320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1c8c22827f91e2c6300c81d70e34a22ab986b233a794d09a4694ee6e20d608`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:04:18 GMT
ADD file:bf9375f2b0e5c66c0a1840e13cfa8b3f0aa55934d9c92c13e479c8cf7909e923 in / 
# Thu, 17 Oct 2024 03:04:19 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:31:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cf1d8a933c6efa9a7129c6faf202eeab8feff677f32fbc0037a3ab76003edcf8`  
		Last Modified: Thu, 17 Oct 2024 03:09:00 GMT  
		Size: 47.7 MB (47691399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbd60cc121d929130eeee92fc8225e4ed5482cd36b62a951095ebafb943c0a1`  
		Last Modified: Thu, 17 Oct 2024 03:38:59 GMT  
		Size: 18.9 MB (18896921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:39a72e54041e914f8d292a8fa66bef1d0fd12c2a538f9e6286e065bd58a7ebaa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73829093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0fe48f5cfa07b62758890a51ce5de365b75cd7ad632d8bb825a9982ff7670f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:35 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Thu, 17 Oct 2024 01:12:36 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:32:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd949d90425f27d9499ed62d5edc09c30effb2a25cacc5cdbcec475f72c714b`  
		Last Modified: Thu, 17 Oct 2024 04:37:48 GMT  
		Size: 20.2 MB (20199608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:732baf4782fc85fa8cfd31ad662e892afc0d4db53d1c5cefe7a12d67967e73d0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75783489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9d751c252d9a73cbaae351ea015b6372837abdede0240d07b5f1a7dd70f6f8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:39:51 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Thu, 17 Oct 2024 00:39:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15aaf6c71ee896572e8510fe4d438d0dbd76161c333521b2012d9264e2e14151`  
		Last Modified: Thu, 17 Oct 2024 01:12:12 GMT  
		Size: 21.7 MB (21665512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b3e43eaf1da53ac548a81eba71804f3eb7e037133540d7c3d03f873d4dfccde1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73044390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edcb217fdfada19176a3a00824c022eea204d2bb208bcdde5720e6acca9789e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:10:11 GMT
ADD file:8ffd9575546e69884562db46178b841df2ba1ed04549599485b7c502f81ac4cc in / 
# Thu, 17 Oct 2024 01:10:17 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e3c6aca2e6ea9e1b19b3c46a60581e28de71137e5bd8fe9c8ea62365a8e75d74`  
		Last Modified: Thu, 17 Oct 2024 01:18:46 GMT  
		Size: 52.2 MB (52157899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8caa54e7215b92f68792f1b978dc23df0d8344fea83727a4b5758d7a94f9713e`  
		Last Modified: Thu, 17 Oct 2024 02:11:58 GMT  
		Size: 20.9 MB (20886491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1aa6a324bf194794cae8e50a0b5f82e7dcb420da4e2a8e96fe2b7e0d1d67ae50
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79121860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5df0b8fb1a4183a5822529e9f0b646a72cf005397e0551f610a10817ac3096`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:19:05 GMT
ADD file:3f30d2b91e08061eb3185f2f9c67756024dc8f3e6cda74d75d6ae54a603cdd2b in / 
# Thu, 17 Oct 2024 01:19:08 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:45:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:df36361b5ac72face21de9a14adcec98ba3abb2261a8339bf516725d8753f43e`  
		Last Modified: Thu, 17 Oct 2024 01:22:16 GMT  
		Size: 57.2 MB (57176824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d6fbbdfd760d192f962f091ac6ac50b83943b30afeeef05cb2189597ca0d4c`  
		Last Modified: Thu, 17 Oct 2024 01:52:34 GMT  
		Size: 21.9 MB (21945036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ec5902acf9ad0c94a3b766784a4f643ba4d2ce81e8e4cc00c5630f9835e0bc84
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71587966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc2f4280729a6d4e7ed21cd4f0b7ee24e080d628a28e79cd5db588b28b5cb7b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:09:12 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Thu, 17 Oct 2024 01:09:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:41:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29cf887cb660615390407db841ad4c44be2414b9bf999ba668d93a8305675c7e`  
		Last Modified: Thu, 17 Oct 2024 01:14:47 GMT  
		Size: 51.6 MB (51562685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cffe06738a4c488c5af7baf511864fe81ba7e38149f28d93443e35a8d7d414`  
		Last Modified: Thu, 17 Oct 2024 01:54:09 GMT  
		Size: 20.0 MB (20025281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3feb2bc94e8b438f04b46cf2134a1b28917f064e50af7bda8fef163072c8b3f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74491345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e16c92f642c5eba205fb0cf20718be087eb78bec76c62b71f8d9a58a0479657`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:33 GMT
ADD file:2f1a819570e851a9bce2342f32c7927abdb02af08d5e469e6f5d41a193235bb2 in / 
# Thu, 17 Oct 2024 01:46:35 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:42:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:79590eb16acf1f35f7a00e8c30e7daf7ed5d8bc9d65ff782665704f532af0ac0`  
		Last Modified: Thu, 17 Oct 2024 01:50:44 GMT  
		Size: 52.9 MB (52851981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72407aa6b20ec8dd251f8d046dc6a90dc4762b5a40f3de1875d57e9707b2249`  
		Last Modified: Thu, 17 Oct 2024 03:49:29 GMT  
		Size: 21.6 MB (21639364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

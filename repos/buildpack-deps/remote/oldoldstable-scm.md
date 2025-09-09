## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:ee5b441932674423312b9844934f615634a608be4a2c14e8dc758b2b97c02d60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5f9005ddc6d5f40aaf6a31c3cdce0eb7dad6abea0839caad423482b3c6e9baba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124277987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852dd576f8134b9381422ffa6c72455ea68c19da1a63dedf1401155d7b28b2bf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebbe40dd6978ce6b51e9d84d91a658eb2959635aec29cb2475587fda81e28d1`  
		Last Modified: Mon, 08 Sep 2025 21:54:22 GMT  
		Size: 15.8 MB (15765345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b969d43370836ef53860df2c53e721ccfdd06653f3db3f7100570314bf509d12`  
		Last Modified: Mon, 08 Sep 2025 22:13:40 GMT  
		Size: 54.8 MB (54757246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aeaa53af562f653411c81339d4a733e3a23b68865c03bdcd17946b11ab5034cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7919519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e6d8110a42ed7427ad0419c734ce6dee3ddfd95529d21150fb2c845e7824fd`

```dockerfile
```

-	Layers:
	-	`sha256:ff733dac133c4ccf99ba28e899817bdd8f2e62745bd81062c72f4064a374d02c`  
		Last Modified: Tue, 09 Sep 2025 01:20:02 GMT  
		Size: 7.9 MB (7912160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f720e998dfc5d6c34fed8d44c3310b304c0e7437b685a072df15ff26ab1781ff`  
		Last Modified: Tue, 09 Sep 2025 01:20:03 GMT  
		Size: 7.4 KB (7359 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f9fbe19eae002e2d74ea1c47b92a51d60cf683c03b373f9fef27ff35a03fee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114557856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495105e91f6818415f88415923728c98a1c4327f0cba59b2e05519f1cc0737f1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8274f5d2891e4b4a199e88ea54bf64be2b431cff01268ebaebfacd12519d655d`  
		Last Modified: Mon, 08 Sep 2025 21:14:50 GMT  
		Size: 49.0 MB (49044356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7f7d1af869adfa648959578fb79545e78d3ad3763e029dfc7f93e144fcbcf1`  
		Last Modified: Tue, 09 Sep 2025 00:01:03 GMT  
		Size: 14.9 MB (14880715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ecf2b4d23f0a78cb60113427441ac697a546595e8f7673028790822ce75517`  
		Last Modified: Tue, 09 Sep 2025 06:18:47 GMT  
		Size: 50.6 MB (50632785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:738040c96024651bc63346e82d0cbb9c0385456af0e4e448e01e37349155afc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7920983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d5072c2b4d26fae4db32e24420daf5b5ed4db6525d0df2dfdded8a0971cb4d`

```dockerfile
```

-	Layers:
	-	`sha256:7ca8dc0c4be49a4377a4344974556aa5485c7cbe8d49295b3fe3a25c0f648632`  
		Last Modified: Tue, 09 Sep 2025 04:20:13 GMT  
		Size: 7.9 MB (7913562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e4f675646f09b73564c098f968294c644a52b0d350727dadc511298ce9f8979`  
		Last Modified: Tue, 09 Sep 2025 04:20:14 GMT  
		Size: 7.4 KB (7421 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2e29c80e6cea16c1b2958f17fb062e2238122226820ff7144c8e1a11a78ebf04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122854985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1922719ad5689353ac6886e441fa7262270b1f31f04fff21f177ae740de3000b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c26dea2f52a9cb0633591a828e9fd53a32d89290a8c2b4b5d5286f76f5332d`  
		Last Modified: Mon, 08 Sep 2025 22:20:05 GMT  
		Size: 15.8 MB (15750666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b8f2ae237d2864fee9f12b950708d56b6e76bc6595e309bb307eade128f989`  
		Last Modified: Tue, 09 Sep 2025 02:13:06 GMT  
		Size: 54.9 MB (54855949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4988d25af8fffc1d515cc5e0c7f8b3c4d1242fb4c8641ad572cacbcdeab946f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7925331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2921327097c576d6ca3c5c64a9c9382e9685455def8e626152196e6e9545dc9a`

```dockerfile
```

-	Layers:
	-	`sha256:747b6391bfb701e7411b72e15f80038d0236d37e3f84c0021ff48c9e54afc3ca`  
		Last Modified: Tue, 09 Sep 2025 04:20:24 GMT  
		Size: 7.9 MB (7917894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9ed60bf54836bebbbdb1818354f03cd59c3ade6d79aa4282abcd781b9e51c42`  
		Last Modified: Tue, 09 Sep 2025 04:20:25 GMT  
		Size: 7.4 KB (7437 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:878467f4323a7db542d5fa9e6ac15e489508663b2b075f81d6c2ca2268ab4378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127009493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb4b9dab7a641a9cdba49ca74a7bcbf3a27bba333676840bfcdcd0a6c4685f7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:21d761bd0e7544a956d2e6eb27c7a89e081fa93136574d1836ddae535c60eb08`  
		Last Modified: Mon, 08 Sep 2025 21:20:56 GMT  
		Size: 54.7 MB (54690513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0956db1fbb0de06709cacad88eee1a92edcd3eb326031290d4f6e321e68d7c6d`  
		Last Modified: Mon, 08 Sep 2025 21:55:16 GMT  
		Size: 16.3 MB (16268970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8151bbc2095026ddf31b19dbad5daa6653efd5a630af32432a4736a4ce7bc56`  
		Last Modified: Mon, 08 Sep 2025 22:13:43 GMT  
		Size: 56.1 MB (56050010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a17f0c7337a5eab9cd77a7a4da379bc92ff57b4fa143868a7308f56fd816cdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55de13e7fe329b6d5dcba26e487e6c4916843df3b1bf31aa82f33f75ff463ef`

```dockerfile
```

-	Layers:
	-	`sha256:ecd5c1894f051793e6c86780cfc07e9fe465cdfaf43866a4da3e49f31e95d3f0`  
		Last Modified: Mon, 08 Sep 2025 22:20:17 GMT  
		Size: 7.9 MB (7907730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff0c3f0eed592caba543ac00d1488d0c316f843f08c015c82955d6b30c876ee6`  
		Last Modified: Mon, 08 Sep 2025 22:20:18 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:fabb3c738748e591cf514e46ad72ce6d2f6a23a445d2e2933d3f278d885fe6fd
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d4b743d71913939a489c8d0fb16d9b34c973af345fed8559d844c36333044415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75451056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca2b857f00f27d13ade114bcbbfc2bf8fca40de0bc63b6c858eb500b7098ab`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8d64c6c7c21822ac171c4c396d70161707401d6d50d133075d661956f08dc756`  
		Last Modified: Mon, 08 Sep 2025 21:13:08 GMT  
		Size: 49.7 MB (49657990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ef32ff63c929905defc6f655e25216327571899c86b682cf8814eb2c3a0a3`  
		Last Modified: Mon, 08 Sep 2025 21:55:00 GMT  
		Size: 25.8 MB (25793066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:35e6c218690835dc9d1430e16de96f71309d1a283973487d3e7508fd286985d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4122861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d83dfa9d52c27ef42049380cabf23775e7730defce5d5cc5080be4153838fc3`

```dockerfile
```

-	Layers:
	-	`sha256:42b2cdac80b3a4f75731e336fae8cc46f410f5d7831c97f997817671f8fbc4ae`  
		Last Modified: Mon, 08 Sep 2025 22:21:21 GMT  
		Size: 4.1 MB (4116057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fcbb46030688f391d4f0b73ef0c2bc744f34ad53c7afae44341bc44347ff966`  
		Last Modified: Mon, 08 Sep 2025 22:21:22 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:0865b9757e3b5b0639b18f8bf16c1031a65adeeff1bb2a1efc3067a1e59e8004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72186724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86840c92bcc05788ce722167d7359b0e1995e97d9e4ce786b786e2756248ca92`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fbbf51ad93abaf2c32c0bd2c116235b9ebbdf46c27b1eb3a1de581d2505529d1`  
		Last Modified: Mon, 08 Sep 2025 21:15:28 GMT  
		Size: 47.7 MB (47745321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643a27ea3b595194ea4b57e98121e28094f76ae480ffaf98bb45b0ff375de320`  
		Last Modified: Tue, 09 Sep 2025 01:32:11 GMT  
		Size: 24.4 MB (24441403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a80203fec62802c035f800bdc5c619ee81a0290412d8c410e1eddae7d6494184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad9b8865b795a9d1025980ff3c80adc821b9681e34fa8b4d3e3d78e587d059a`

```dockerfile
```

-	Layers:
	-	`sha256:5393bdb30c4e8c2717377410e520e80e86da8b5b0993a0b644c3d8d9045c9631`  
		Last Modified: Mon, 08 Sep 2025 22:21:28 GMT  
		Size: 4.1 MB (4119056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:946eb848acf1c63fbcf11d686de017f36756339ddca09cb4abd90c64f7ba9f45`  
		Last Modified: Mon, 08 Sep 2025 22:21:29 GMT  
		Size: 6.9 KB (6868 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9fe1826bd38353d4a1541452b7d3e75f09432f16f46368c54d2bed0d4d4977f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69716875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ee02187bdfcef215a78a59a30319dc198e4b360e777d98a036b0c9219f5999`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d30a0c5c579644a88a894fd0b1f1db229651b30c974b07aef6ab9bcde5b64440`  
		Last Modified: Mon, 08 Sep 2025 21:15:47 GMT  
		Size: 46.0 MB (46006695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf528d0788e249a97adf6d73be0b9ae329c2651a09b55c47f7bfbe9fc96a9cd`  
		Last Modified: Mon, 08 Sep 2025 22:48:40 GMT  
		Size: 23.7 MB (23710180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f6d360b51c498125124f7aeb15162a9461f1b47cb612165df296d3eb0d24b8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef911a531a6e1ae293f39a421e0611c48b4b32ddba6353771f6751dd53ecec3`

```dockerfile
```

-	Layers:
	-	`sha256:5901ba408c866a6db2853350b3ef1243d8b9ec24d42b3e69fb7440ec72944559`  
		Last Modified: Mon, 08 Sep 2025 22:21:34 GMT  
		Size: 4.1 MB (4117550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a787ff616a6aa1054f55df02931dd6d7e90b37384e55a39ffcce03a9b65f941c`  
		Last Modified: Mon, 08 Sep 2025 22:21:35 GMT  
		Size: 6.9 KB (6868 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:079596f43ceccfdf4d56f35795c434cb67f828a4636e8eda5aa629e70a0435bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75056358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9134839a934ac65fec098e08afd9029d836c9149fb558eed80b9d48b720dfd5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:00e024daab2d43f36749bffb01f2b299b405cff0659a8e4f4f00bb468dd24c27`  
		Last Modified: Mon, 08 Sep 2025 21:14:58 GMT  
		Size: 49.9 MB (49934721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523fde0f8298499f83d08590922e2548966d7839a982d2f61f9bf20422631032`  
		Last Modified: Mon, 08 Sep 2025 22:30:33 GMT  
		Size: 25.1 MB (25121637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:65f7bb8f6d6963f4968b2edbf47a5a853c634ecb6496da63756119ffa224850b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2747ea7f5f25a73dd1d1ae759f44a83a96c4c40d4a72c9f46c86eb5f9ebdbb96`

```dockerfile
```

-	Layers:
	-	`sha256:38f2aa730ed8ce1e29d117ebc85dedca6f7b00ac299c925c20f8e29e6955895e`  
		Last Modified: Mon, 08 Sep 2025 22:21:40 GMT  
		Size: 4.1 MB (4117587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93991f9078b34da1dd4243dc9b91e379b9d342b2800870c1df2f70454c0c13ff`  
		Last Modified: Mon, 08 Sep 2025 22:21:41 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cc1f76a3efa7c44f78446b0f4fa010ca8f4d84388c187bbe2ec6d2d349afa846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77994359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169b166bde99a59b12749381c04761c7cbf3b4765b5827c6408c4de35292c8b7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:eb039ce3bcf3fbed73729096e510ae45e98c7db73d412a09aa57aaad6f2f6267`  
		Last Modified: Mon, 08 Sep 2025 21:12:53 GMT  
		Size: 51.1 MB (51113613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb4ce6e6dabdd026c92e91d6d35c69c5877c49180dfc2038eceb2d3a81ffb31`  
		Last Modified: Mon, 08 Sep 2025 21:55:10 GMT  
		Size: 26.9 MB (26880746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dfd1e5d686f726a2d27f3d0e56c9b29e36573847b645fcc35e903c8b3959d929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645baa72547dd70f81718392ac3a634ebdfeee9d0a51d4d3a09b6bfdbabeb016`

```dockerfile
```

-	Layers:
	-	`sha256:e9cc3a436830a1132a17ef4a022c453af65d38faf7fcf469a8f8ca1dfe0700fb`  
		Last Modified: Mon, 08 Sep 2025 22:21:52 GMT  
		Size: 4.1 MB (4113177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae5e23ddb207545dcd3b56d9e43e5a097a250a3f49e1257fa7535941227805c5`  
		Last Modified: Mon, 08 Sep 2025 22:21:53 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e42ae1b823a3d05aafb9e3b7d680368cee03e3f0fd696c9a41e4c21647d588ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75578760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f6df2349a8e170b8a6e5e2c6a49ec95b948cc003156b187385472cec298821`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e92e35711c7a07432f12289818406bab4746919197592d38fb8632974832ff9a`  
		Last Modified: Mon, 08 Sep 2025 21:18:22 GMT  
		Size: 49.8 MB (49822261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5720cce3339585de6afad24f3a7efc526d8b9755873fbcf07a2420b66b3573ec`  
		Last Modified: Tue, 09 Sep 2025 04:23:26 GMT  
		Size: 25.8 MB (25756499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8df696c41fccd79e10936b75d059ce0b29d77afa7d75f8cc489670acc8f1814e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e88a210b2f6f4edb996dee924d94b62b4ca03d878f222d209d61de3614b385b0`

```dockerfile
```

-	Layers:
	-	`sha256:ad71fb48a81765d8ac55559c8c367b4fed708f27a9e207d472ce55cc7f99d7af`  
		Last Modified: Tue, 09 Sep 2025 04:21:48 GMT  
		Size: 6.6 KB (6637 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:89dfb7b3873ac82cbc1d13dcb650c46d0672eed38d9cd55fec3ed7605d0c7315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80557916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec93edc47036590e8e52a74bfe741dacfefe2881af844428c969edbbf67acbe5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:772eb1186277ef333cc2188830519c27192dac48fb00016f4bed1d6fb65f0e2e`  
		Last Modified: Mon, 08 Sep 2025 22:22:18 GMT  
		Size: 53.5 MB (53458792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383909d767bd90933a41650a2f22af3654b67dad5eb9eb12c8f0c5d5619ec04b`  
		Last Modified: Tue, 09 Sep 2025 03:12:59 GMT  
		Size: 27.1 MB (27099124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:94f6aefb1e7015ad53ef8bc4030573d8acf3e0568ac6af6132902e023b3f22ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3f80c4ce5ee7fafb73b0bca2141a776d6e763f018a2bff97f56840a2f4ec4e`

```dockerfile
```

-	Layers:
	-	`sha256:14ecf6714e2ab8f30e3be7d5e0e42e5e027c733a93b69789f818a59c82a4df20`  
		Last Modified: Tue, 09 Sep 2025 04:21:51 GMT  
		Size: 4.1 MB (4119883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb50c3322774b03868d21b6c95c4da2bb60b909b738503a49e5b2e7f7cbf55a6`  
		Last Modified: Tue, 09 Sep 2025 04:21:52 GMT  
		Size: 6.8 KB (6835 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:79ce8dd7af6cc245f5550228781b4ffa37d4220f2207c655a047047cd10ed205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73124592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289476c5c996125c4efcbe34436c04d94929d42565a34a9b6a4f914f9239ddb5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:347be58a551dcf8aa3dd300ae844cdfc6ff2cdec19870bd090fdef86fdd7d393`  
		Last Modified: Mon, 08 Sep 2025 21:38:55 GMT  
		Size: 48.1 MB (48052647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40a5a581d6d2c97cf774bc90f07071cf2fb0f1b3c0571346161822b7094bcd3`  
		Last Modified: Tue, 09 Sep 2025 09:13:34 GMT  
		Size: 25.1 MB (25071945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:45216817ef0c5365a8ec976c452f520737479431e5c6908a9fb176aebde358e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4115373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6563d9a3599932ceb4b49e522cb236be5848f1cbaadfdf8e1aa5f54c4371b5b0`

```dockerfile
```

-	Layers:
	-	`sha256:a4cfc076d75abe85bf2b7b51a63f93aac9409b14edac165609e1fe07d0c81f6a`  
		Last Modified: Tue, 09 Sep 2025 10:20:29 GMT  
		Size: 4.1 MB (4108537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d12704a058791f95dfe5beb2898534d8c23cf98cf4cacb4d8bc5dbe25e18e8a`  
		Last Modified: Tue, 09 Sep 2025 10:20:30 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e3adcf64d80c67a7b0fc88cfaa31fa9bf6ab4be2763fdfa91600b4443cc930ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76545329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916ce5db17003e0f25012aadf6875a8ee1530868ff0124ddb1ee0e2fb84d4aec`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:75e6f7d74f7a64a858e5c9cdecd19e5f33e99956d1f33d14985ac51b655eba01`  
		Last Modified: Mon, 08 Sep 2025 22:22:23 GMT  
		Size: 49.7 MB (49652038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f495f7a03a882cda8ba1cac3fcd8e67045987237ece386400cab302efabfe1`  
		Last Modified: Tue, 09 Sep 2025 10:20:34 GMT  
		Size: 26.9 MB (26893291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e80378e0c24d4685f87691eefc4928f20246266c46d1e09c0673786b2f0e3d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1663506d1e87fc2f19c79887ab7ee4c78f4eee3256fe4dcd3aa51a58a7b7f0b4`

```dockerfile
```

-	Layers:
	-	`sha256:546c6729dbd7ff51527514f7593bc5281adb07976cb437deed2d6ad08c1f0aae`  
		Last Modified: Tue, 09 Sep 2025 01:21:46 GMT  
		Size: 4.1 MB (4117467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:076da61a23dcd01f7aa77a89fd5016641e95159fb8d9dae14699f9d10edaaa3d`  
		Last Modified: Tue, 09 Sep 2025 01:21:47 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

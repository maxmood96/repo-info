## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:7480c0e410a1862bf4427a0e35b9edb93c3ea6744237ec98c6fa85677b6af217
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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; arm variant v5

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
		Last Modified: Mon, 08 Sep 2025 21:50:10 GMT  
		Size: 24.4 MB (24441403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; arm variant v7

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; 386

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:792c658776779e639c8c5d2e759f62bfc2f116241832afe4f1b78217aa3fd7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78097808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0ed6a3a23fd00a8c203b6f9316d382d5bb3b1319738f9a099b3df8f44a9df6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5da413a3f50eb44f07bba0eecd786bf3efd93a4ca4c52ba8109a9b9ba14e688b`  
		Last Modified: Tue, 12 Aug 2025 21:13:15 GMT  
		Size: 49.6 MB (49562283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3d257b869b2a60078b7a65964ab94a9b367c5ab49593e2c17c1f7845cf6eb2`  
		Last Modified: Wed, 13 Aug 2025 06:40:49 GMT  
		Size: 28.5 MB (28535525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5f8ece5fb0bc4cc7553ad04de6288f130827d4954508a01a0f6f077057db9e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c64783547b54a226b1d912e712c6ee812c6fb184235a2939e8788a6372d263`

```dockerfile
```

-	Layers:
	-	`sha256:ecd03ea8089aa9dc7ca02b304c16da4bd884f6a16b75e6a15aa216e7c347a9e8`  
		Last Modified: Wed, 13 Aug 2025 07:21:24 GMT  
		Size: 6.6 KB (6637 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3d8b97ffd3f4c22a63f6ea98f3b5607e6eea9993815b25a89450339a5fa25e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80217002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ae0a4039f8a43ca2a83956e13a7aaff098c65c3b3841082164b28d86dd6657`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ae7a451fcc7e9bebf7ef51b031f5ec2600e7c017efb66e1de76397538aff917`  
		Last Modified: Tue, 12 Aug 2025 23:09:05 GMT  
		Size: 53.1 MB (53147748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48ea27c6408465e04631c45f46084191d49262124cafc6550f5e911abd6374`  
		Last Modified: Wed, 13 Aug 2025 12:14:50 GMT  
		Size: 27.1 MB (27069254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:64e15c05acbe1de51039a5bfcb25ac72a1f7a0b179790765258fe19353ec70d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a134817a688da9db48ba038230fa67bc0c78990f69db802329714a201cd186`

```dockerfile
```

-	Layers:
	-	`sha256:6e2411b3ee2bf110bed1660766deab484d3fbcbf9974a5460a284cd03e8fca09`  
		Last Modified: Wed, 13 Aug 2025 13:21:36 GMT  
		Size: 4.1 MB (4116220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:359c1fe635be880d9f83899169ac8a8ff09117cf48a18fc0dc22c94887d01c78`  
		Last Modified: Wed, 13 Aug 2025 13:21:37 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:447940fa7bbf5230bc339aae8a40c39838ae959d7852061b8d2c4e2d9a6a0ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72820250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536d174447e56f3b2f8485a454e6937a772886d8fc9e46eb370e4b30450ccfb9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a9e91ea2edc2d111f6a67eba934b0ebded0b74c51de6a807b73d07cbf965e132`  
		Last Modified: Wed, 13 Aug 2025 01:03:20 GMT  
		Size: 47.8 MB (47776559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64af9f489cd1777e5b300ee5ecaa1ee0eb257910fbeea3b4885aa18546f4677f`  
		Last Modified: Thu, 14 Aug 2025 14:45:40 GMT  
		Size: 25.0 MB (25043691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6d4b677973b25f866ca40a16b3a098d7534dee03b9eb3b4df07b596347e14d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261608d6844cf4ea00520a67550d368943904d343b091a4ff7929221ef96e84a`

```dockerfile
```

-	Layers:
	-	`sha256:5888bb9986b42b8e73e10f191990d251a0014c33e068eb6552e09fa48e3ae50a`  
		Last Modified: Thu, 14 Aug 2025 16:20:46 GMT  
		Size: 4.1 MB (4104826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c76f90bec4cb9cc774b5e07ca51dda6877899e45683fd5addaf57ef9a94f85c1`  
		Last Modified: Thu, 14 Aug 2025 16:20:47 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8c383f2e609956c30ee4ea0368a9de9f2a250ada914fef4f4052c3ffd53a31ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79373991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3029bcb85bd540a7de08375df7608f36422a0fca850b9497b3246a717b239a86`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4959d43b6e4e3bb883ad4324fbf3d2d46fc88486af520d990c753fc3a7ba0062`  
		Last Modified: Tue, 12 Aug 2025 20:56:23 GMT  
		Size: 49.4 MB (49380676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e9f068820d21f743fb7a4899ffdac4cbb3c9018377c7ccd9ea60dfaa661d90`  
		Last Modified: Wed, 13 Aug 2025 11:02:14 GMT  
		Size: 30.0 MB (29993315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:239cef95408a40994d1d96b1a486418f5b23148ebf9fa19178d0c9053d9292e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d481c5b84fb79e4f4a64c902e5a650ae70b47fb89804a0f609a9cb8bebae777b`

```dockerfile
```

-	Layers:
	-	`sha256:a13aa6a6930536cd344c49672b2092a5fc7c43568815ea82ed859223f578ea24`  
		Last Modified: Wed, 13 Aug 2025 10:20:48 GMT  
		Size: 4.1 MB (4113802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2ea1577d7c6eada5d4b7fe9f05a719b7d76f24569443ac2e3359c4ddc6d8059`  
		Last Modified: Wed, 13 Aug 2025 10:20:48 GMT  
		Size: 6.8 KB (6803 bytes)  
		MIME: application/vnd.in-toto+json

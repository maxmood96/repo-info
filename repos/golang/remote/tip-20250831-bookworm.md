## `golang:tip-20250831-bookworm`

```console
$ docker pull golang@sha256:b147e04579218b763ff62392c186d4c0f2ec7d12a9e11511877036407db78cce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
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

### `golang:tip-20250831-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:0c7234493ecbf76f527650f4232a412cac9280e3c3d4659739d99120c7dac7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312748463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de1454d9f3ea07bedb22f897a9f0f9184f2e07f797effef7efb8a034a82487b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffef7dc6f99e0837fd18f5ab2b363aff8d1c12ed377199f6d6478f80b458c05`  
		Last Modified: Tue, 12 Aug 2025 22:14:50 GMT  
		Size: 64.4 MB (64400050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e3c77927caae28a413fec4c284bbdd761850550b747f70a79511bdd77ff72`  
		Last Modified: Wed, 03 Sep 2025 20:48:22 GMT  
		Size: 92.4 MB (92378559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3dff0c88890d852f1b6000c60fab1e5090230eba3301a46159a26dd4149cf4`  
		Last Modified: Tue, 02 Sep 2025 17:26:01 GMT  
		Size: 83.5 MB (83454344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85fbc69ea3f6734cfd2826a73529cb38d2491c084e2e64388b444534490be7e`  
		Last Modified: Wed, 03 Sep 2025 19:59:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250831-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2f8dbbb53fa9c98e0c2af676beeec8fd5ba8a0db3019eb134400ded4a57f785a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10516572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224ced43d195810c3bb0e3128aca88c3652092c8df70daf128f44bc99087dfae`

```dockerfile
```

-	Layers:
	-	`sha256:71027d8f6d729eb3ef671654d900cf58d0210678c5e2c57813f22a5869715372`  
		Last Modified: Wed, 03 Sep 2025 20:24:27 GMT  
		Size: 10.5 MB (10488143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce9d84333ed4b61344b4457d75ce6e19ef018331487572632cf97f82870cdfea`  
		Last Modified: Wed, 03 Sep 2025 20:24:28 GMT  
		Size: 28.4 KB (28429 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250831-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:242d4aaf0156baed82152a27e3b05f2a9ee4f980d0c208ccafa3992be66f0252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272551509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad660e17ac737707ab7a01ca58839647eca308d75b561dc8e123c79bff4620e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a06e9cd35e09740ec78f63d1179c1e1528d9cfd9686a0094a4655ebe70922c99`  
		Last Modified: Tue, 12 Aug 2025 20:46:18 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4756b55428372e77ee6ab2b6c5a35bda8bf113537f0ebde9510c43737f4249c`  
		Last Modified: Wed, 13 Aug 2025 00:15:08 GMT  
		Size: 21.9 MB (21929365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897d6edccc28c5bb741d67021941e03742df0d455c33993ccd0aa632e1cd6d24`  
		Last Modified: Wed, 13 Aug 2025 06:46:44 GMT  
		Size: 59.7 MB (59656741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646a036d17dea963a87e5b5f829c9131c3947ef44cfc0b2795f389524f661ee`  
		Last Modified: Fri, 22 Aug 2025 17:34:29 GMT  
		Size: 66.2 MB (66243912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8183d7d02c47a9b085b3d0bc6d67309b7fa4b7ef97cac1694dc0b5ea8b6ce9c`  
		Last Modified: Tue, 02 Sep 2025 17:26:14 GMT  
		Size: 80.5 MB (80512289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f74ca79090011b11bf9f33e96fe7355cc8051e41d7e1ea214dfd5a621265c0`  
		Last Modified: Tue, 02 Sep 2025 17:29:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250831-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:fd24b5486a386616818b8b021a679d65a440f7c5fe35c77f82bb83daaf81373a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10323378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4eab42001f7deaa8d8388865062c78405d3997ad9a96d5c0f8401f9ecdb78b`

```dockerfile
```

-	Layers:
	-	`sha256:025b7b640cb2d6400862cf0e5ce3a5c1e723a88e188767398907c8142fac36b4`  
		Last Modified: Wed, 03 Sep 2025 20:24:36 GMT  
		Size: 10.3 MB (10294841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d375aea5bb24c71b068ac4189c63585643d1c438a53c939282592a4067e97d4b`  
		Last Modified: Wed, 03 Sep 2025 20:24:37 GMT  
		Size: 28.5 KB (28537 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250831-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:9ee9f635dc56f5b6c59fdc1ad431e2cd8cb8f6f072d0d126aa081482bec72c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302184679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ca3fd3b49de4bad617b9133a83c9213109314f0515be1c5c6645fdff3ed740`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4910ed05e8b3022bc1c6adfffae5e35b0d2b4c6d756ee21311b48b509147a1a`  
		Last Modified: Wed, 13 Aug 2025 16:31:39 GMT  
		Size: 64.4 MB (64367003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022e19889d5b43d1bba827a7f5dfb329b722fbf9878dea6ccf631c82db2efc8a`  
		Last Modified: Tue, 02 Sep 2025 21:42:11 GMT  
		Size: 86.4 MB (86441757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948ccd09d5c498d3bdd3015babafec64e8e01106fe6a739f268b131403fa7cbb`  
		Last Modified: Tue, 02 Sep 2025 17:24:20 GMT  
		Size: 79.5 MB (79463464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7257350adf382505dcbaf6a0abcb37eca1057f23a429edd55e7368867683208`  
		Last Modified: Tue, 02 Sep 2025 18:07:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250831-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ac16a305943135e5738c145a14ed41fb739835fd0a630d642fecb2a16d94c99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10544532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185c5d60ab37421703d41d6b2ff093113a639da29749afab1054f8eab10c8364`

```dockerfile
```

-	Layers:
	-	`sha256:5092f1890f809c96c2363e9e7b4222caeed57c87b8639d2935ccf90f11e722c6`  
		Last Modified: Wed, 03 Sep 2025 20:24:46 GMT  
		Size: 10.5 MB (10515967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff752b0722850631ddf9ebc466c656e558477ebd32ab61df40c31d86fcfb5f5c`  
		Last Modified: Wed, 03 Sep 2025 20:24:47 GMT  
		Size: 28.6 KB (28565 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250831-bookworm` - linux; 386

```console
$ docker pull golang@sha256:36c7241f03e0d2a759db39dff060040bf308ce4cd519c1098cdc2981fc73ed61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 MB (312506953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ce172b08a126fa96b8003854c3e98c577462439de67ca41fec1c671297ba82`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:73488b414dce83adc963656678257daf6a25aaa9e6d76928aee03f81611c17ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 49.5 MB (49478115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874646e2459984b117c58d731a64ebcb9d23f76cf755c68e1ddb30317e57abc0`  
		Last Modified: Tue, 12 Aug 2025 22:13:36 GMT  
		Size: 24.9 MB (24861125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c25d261fc893dbf63d447e191cad0237f37f95f01960ee9b9026b75ab3a74`  
		Last Modified: Tue, 12 Aug 2025 22:14:47 GMT  
		Size: 66.2 MB (66226107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf3a0a4e67de53991eae294b658a0f8db17a343171288b0c4f2665bea2f23e8`  
		Last Modified: Wed, 03 Sep 2025 19:08:04 GMT  
		Size: 89.8 MB (89808683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc969e7a30537f064821c7c82ed2000b4f696dfb82f12bececa0caf74f9469a`  
		Last Modified: Tue, 02 Sep 2025 17:27:09 GMT  
		Size: 82.1 MB (82132767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66591cfddf70274ea2b7db2027b7b2f852b1896984ee40cf79bdae0112dfaf`  
		Last Modified: Wed, 03 Sep 2025 19:12:43 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250831-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:9adce45d8693217f20a1797100744243515bed64383168b545bfedd7a8842c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10496127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85b87c7f64b73a3ffae53815e4b55a6bff6f8b9aef7fec3e9f58357da07ef31`

```dockerfile
```

-	Layers:
	-	`sha256:c3c003a2eee50c8571440ce4857b3c864167e4b95f9c39c45f68bad09d640151`  
		Last Modified: Wed, 03 Sep 2025 20:24:56 GMT  
		Size: 10.5 MB (10467731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2200a2ac6422261cf302a65dd4f6c0bc63dbd2f8b689af7bdd9fdab0da83d982`  
		Last Modified: Wed, 03 Sep 2025 20:24:57 GMT  
		Size: 28.4 KB (28396 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250831-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:ed59323e9b96ab982865e8038ed5fb7c1ea35f6bb84b79ca80627a97a3516d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283851964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239f941700c9f76163b9ffbefdb02b0ef32ff6e35f1e42cf41e78cea6fa3ed98`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:39ab9a968f454fda0ebffae415d31434cb4c4b3f4bb9da0e89f360bd60fa3275`  
		Last Modified: Tue, 12 Aug 2025 21:09:50 GMT  
		Size: 48.8 MB (48776657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5bf976bc5466a2e4cdc6d87c28337bf663ea094da7d169694d61961d11248d`  
		Last Modified: Wed, 13 Aug 2025 06:38:46 GMT  
		Size: 23.6 MB (23603659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e53fb77ec58b351a832fef6343e52e81f478bfac5e6664210978fbb38a2cddf`  
		Last Modified: Wed, 13 Aug 2025 19:21:03 GMT  
		Size: 63.3 MB (63308715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b41136c2f291bd13099a18611b2b7518da292943df8ae3469285b2a82ab662d`  
		Last Modified: Fri, 22 Aug 2025 17:35:21 GMT  
		Size: 70.0 MB (69983468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e1a64dc9f254709b5921f017a1d258d813c7c1d0320d978d07191f6a230bde`  
		Last Modified: Tue, 02 Sep 2025 17:43:02 GMT  
		Size: 78.2 MB (78179307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b802fe470ec522be8462d34ee0fa329925676f4c49c77565627056a0f9697893`  
		Last Modified: Tue, 02 Sep 2025 17:42:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250831-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:49e539e7d81e901e185331b364c8f4d28814fefdc864bc9b3016777e6a9dd075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 KB (28283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0cf80f89e72edc7735f365dbc36300d0e36be3a1bebdfbd09ef7e3a02572e3`

```dockerfile
```

-	Layers:
	-	`sha256:ba5bc1f12a45af2edcac9edc7c12d9adf068977ae90b107038a807f411bc153e`  
		Last Modified: Wed, 03 Sep 2025 20:25:04 GMT  
		Size: 28.3 KB (28283 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250831-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:320c00315cd22f3ed271120b8e6328412dbc30c1df14299d7be85604a1ded507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (319046042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa30a37068cc49398f5870627c3cfe6fb622c6078527d7accb476b5f31a91aa6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f87ea767eb09118b3668a0dc44ddf5bf258db4f1bebc7989803cb1b75a66c9`  
		Last Modified: Wed, 13 Aug 2025 14:33:16 GMT  
		Size: 25.7 MB (25666039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb09aa58684adf8f458ec24cfe46bcd658b8344a3c5c5ec70c88bbe9010b255`  
		Last Modified: Wed, 13 Aug 2025 22:43:40 GMT  
		Size: 69.8 MB (69839966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a90f33dee95b0cc1cac58b7d8f984ddb9d36a6f3d6f293da1b4570532671ca`  
		Last Modified: Tue, 02 Sep 2025 17:33:11 GMT  
		Size: 90.4 MB (90385885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65adef97a585f4d6f34375efc6b453ef50bc737c051ef6eb9403cedd2e831eb9`  
		Last Modified: Tue, 02 Sep 2025 17:28:09 GMT  
		Size: 80.8 MB (80815917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d435cf60e9a6f0650abc015c5353045d197534f2f1e5511afd6d1e19e28cd439`  
		Last Modified: Tue, 02 Sep 2025 17:33:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250831-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:32b5c154c67b7d1ccf9db1fdf131227361955b4f919cb401af49c6460631c5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10489089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d708da70579cb95efe0be7f9af30f81917dd8971e0e876d08dede5d64aa751a4`

```dockerfile
```

-	Layers:
	-	`sha256:290f4db1d52a5572cbfcf6b81c2d41cd97646cad0a8c021ab72c0a01cfef0dc2`  
		Last Modified: Wed, 03 Sep 2025 20:25:08 GMT  
		Size: 10.5 MB (10460614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f03923f067129c8e01b58a9790e1d0d4e0eb519c452b0d8f82b9def107ed5df`  
		Last Modified: Wed, 03 Sep 2025 20:25:09 GMT  
		Size: 28.5 KB (28475 bytes)  
		MIME: application/vnd.in-toto+json

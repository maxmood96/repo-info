## `golang:tip-20250815-bookworm`

```console
$ docker pull golang@sha256:368d3239cb0f446b5322710b2aaedd89797f89c41e3eb886d58ac4841d9fb552
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20250815-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:50b686e3379bf5e1c8d756e5dc2ab9c99586634a1143a9cb165986dbc5e1090c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 MB (312428515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1afba38f03d3a52183149ec9dba5b9982498bbf7e380036b4c628346aa1f471`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOTOOLCHAIN=local
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOPATH=/go
# Thu, 21 Aug 2025 20:07:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Aug 2025 20:07:19 GMT
COPY /target/ / # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
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
	-	`sha256:65c27e52251188baae6362a00c6b50c016e4476775d19f64846eca2b887fefa4`  
		Last Modified: Fri, 22 Aug 2025 18:11:55 GMT  
		Size: 92.4 MB (92378727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c981e030468965854d1b7da64b902a546cf410e421543877a0dbcd1eb3b5506d`  
		Last Modified: Mon, 18 Aug 2025 19:09:02 GMT  
		Size: 83.1 MB (83134228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18026f25098f38a19409e8e20f3bd8b565466ff39a12911b43be3ed06d10c592`  
		Last Modified: Fri, 22 Aug 2025 18:11:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250815-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:69425699e670c50335fce41a3ff3a7b0f90f866344bb060be4978df9555f7d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10516571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b668033656e46c9e3df68218f76a78af92ba340f091a80ca99bdddb816ccd14e`

```dockerfile
```

-	Layers:
	-	`sha256:e476a4e3fde8d8f64dd23e0896f790a97ccc199a0527ac98452324669e4d2cf9`  
		Last Modified: Fri, 22 Aug 2025 20:25:37 GMT  
		Size: 10.5 MB (10488143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e80750fba69b77348db1bed20e5a56232a74105c0fb4ec6b1ce070f60e166585`  
		Last Modified: Fri, 22 Aug 2025 20:25:39 GMT  
		Size: 28.4 KB (28428 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250815-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:ac32d51cf9b0fa1088d502b1c628b9b25844793c0dfe8a881b181c7da9d3703d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272197997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ee7ed21dad345f5e0484b85d0c591be8334fce6ed9a5ca9e294699fd5328f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOTOOLCHAIN=local
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOPATH=/go
# Thu, 21 Aug 2025 20:07:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Aug 2025 20:07:19 GMT
COPY /target/ / # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
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
	-	`sha256:65db35adfd1c26b9fd865e957c7ac16cfbd5d2925f26a2f01840bdbea9cb3b72`  
		Last Modified: Mon, 18 Aug 2025 23:18:49 GMT  
		Size: 80.2 MB (80158777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942c3b32ac83105df39ed8873ab885be1707fe38391d8a389a1770e644286ded`  
		Last Modified: Fri, 22 Aug 2025 18:14:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250815-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:04dddb8b466d73d6d30dccae5cebd68efec81b71aca6e339d65337d517a440e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10323378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34bdb07c5ffaebefac77d60f4abe72035adcf44279defd97535696cd3f31ed2`

```dockerfile
```

-	Layers:
	-	`sha256:0f7491c46acf7d4b469a398a95cebfbc9240a5d325a1347c7ef8b9ae41a47b1c`  
		Last Modified: Fri, 22 Aug 2025 20:25:49 GMT  
		Size: 10.3 MB (10294841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24619fe38e6f3b1b0cf36a63c8a79acdde3b790521b8869164db201a7a5ec208`  
		Last Modified: Fri, 22 Aug 2025 20:25:50 GMT  
		Size: 28.5 KB (28537 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250815-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:bc75f82cc8bdf6d040c4bdcb224a696dc79336cec575b72d48c1d312f0a9d1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 MB (301853896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc0e31de79445f5567e1532f78962f440d29ad6dcacefe2cf550266d36431b39`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOTOOLCHAIN=local
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOPATH=/go
# Thu, 21 Aug 2025 20:07:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Aug 2025 20:07:19 GMT
COPY /target/ / # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
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
	-	`sha256:902cf5756952fa0a8278b2b2f1c58b4fa5fa5312cf0afd939cf91a357efac9e7`  
		Last Modified: Fri, 22 Aug 2025 17:34:16 GMT  
		Size: 86.4 MB (86441815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9a962081772d9ddd06f0164791e2d37e59bd0091e1d2b79d410ab8b218794c`  
		Last Modified: Mon, 18 Aug 2025 22:12:08 GMT  
		Size: 79.1 MB (79132623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77875fedc3047b743cda9e42de7843ac65b81047e249b116ba381917dd1fea4`  
		Last Modified: Fri, 22 Aug 2025 18:11:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250815-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ac0738440b5f5d1c3c053d77de80bc0c9861d96df56dbf37f16da285dbe6855f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10544532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c04d360c0adf6a55a9f98fd2d686e261fa44fc88da888feca8c58dcd46fbcb`

```dockerfile
```

-	Layers:
	-	`sha256:bb9e6b381f7590072013fbbb6f00851f53735d12cd1272c6b4c125c40c19589b`  
		Last Modified: Fri, 22 Aug 2025 20:25:58 GMT  
		Size: 10.5 MB (10515967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a313bb675f3c89503cce112f89ba3576a13d7454417b8179431e13377d154434`  
		Last Modified: Fri, 22 Aug 2025 20:25:59 GMT  
		Size: 28.6 KB (28565 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250815-bookworm` - linux; 386

```console
$ docker pull golang@sha256:016c245042fb058954987af651aa668eafb65818f7bbe43c69a70d4743e5c34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312132813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e3f6db55db079876e2c16a5d1eb33edbca5edc076d13983f440412e1bc1e29`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOTOOLCHAIN=local
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOPATH=/go
# Thu, 21 Aug 2025 20:07:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Aug 2025 20:07:19 GMT
COPY /target/ / # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
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
	-	`sha256:de27ee0ece41e7c262371b2969fcb88fbffca5d4e99abedcabde7ab45f6326dc`  
		Last Modified: Fri, 22 Aug 2025 18:12:14 GMT  
		Size: 89.8 MB (89808214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82670d3acf9adce43c089b894a11312540a785c816af45b90edbb17d606892e6`  
		Last Modified: Mon, 18 Aug 2025 19:08:00 GMT  
		Size: 81.8 MB (81759095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c68c87db0fad7f2549c1be40efa649d971c47f8d58927a833cdd6ce7098f03`  
		Last Modified: Fri, 22 Aug 2025 18:11:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250815-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:db9ac60ea109caccaa50cb3170e5dac7314d5467db186f3b1a3a21c43025d1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10496127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174bba10839a52372aea539e10ed5ac933b388297c25619327d6b669d2555f5a`

```dockerfile
```

-	Layers:
	-	`sha256:17e40599038f8a4ef57bd7c2f4ab5ba7522d4f87ef81d8e4776e638fc07074a9`  
		Last Modified: Fri, 22 Aug 2025 20:26:06 GMT  
		Size: 10.5 MB (10467731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34b2bcfd6c9d45c416d930ad4d3cd4021a9bf3770f7d3ed15d8fab5293682232`  
		Last Modified: Fri, 22 Aug 2025 20:26:07 GMT  
		Size: 28.4 KB (28396 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250815-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:96c46912c1a43ccff10ea9f61525826e203f607bfb8310a51c84e32b6a80be0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 MB (283516471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a469a872079ff7095c87506005c463ba5adcb56c8b808acd5ca0c9b80d1de90a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOTOOLCHAIN=local
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOPATH=/go
# Thu, 21 Aug 2025 20:07:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Aug 2025 20:07:19 GMT
COPY /target/ / # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
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
	-	`sha256:b3ec77bb9bbf3ecaf50f6fb0ad26063c518f62818e4278abb1f247effab4fb97`  
		Last Modified: Tue, 19 Aug 2025 00:21:01 GMT  
		Size: 77.8 MB (77843814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bf0e29ca5b885036abd76a0bd2fe04617eb2ab4d248c5852b6da0d1134a763`  
		Last Modified: Fri, 22 Aug 2025 18:09:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250815-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7c968b01ec52abeb732cebe7a1135479474bf1525624658be946b0677ca5cb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 KB (28283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f98a3a0d8b579cdf3a790b76f2f155aecf5f383fa09e669fef75f9cd2883df`

```dockerfile
```

-	Layers:
	-	`sha256:c7c0f3a41b70df3fe1a8a45ae5d724d10bca797dd6a3479017c97aa48bcb388f`  
		Last Modified: Fri, 22 Aug 2025 20:26:14 GMT  
		Size: 28.3 KB (28283 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250815-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:48bf00100680b088dcf41dd4e677466df8a37a611e88af2149f17857a4d80f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.7 MB (318711663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471155e29ede7b9e44eaeb393b603c7714906366ee967ff62b961d5cdf12b8b1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOTOOLCHAIN=local
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOPATH=/go
# Thu, 21 Aug 2025 20:07:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Aug 2025 20:07:19 GMT
COPY /target/ / # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
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
	-	`sha256:48148385706fd854d274316750eae3ff7a535186201d6b3915d4f78273cb3691`  
		Last Modified: Fri, 22 Aug 2025 17:36:55 GMT  
		Size: 90.4 MB (90385992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d39b86dffb1db621a8fcea400d6f61123247f5d28fb771a6f68ef42e85a595f`  
		Last Modified: Mon, 18 Aug 2025 21:57:49 GMT  
		Size: 80.5 MB (80481431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626b1eea05ab91d4e0cc1f28edc64a1232b90a5cabddcce5fd3e39e7703a38d2`  
		Last Modified: Fri, 22 Aug 2025 18:15:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250815-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c147c8799e5796a94105253e57b01d727ecde340a875d0f7ccf8c50d628be9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10489089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46039e3071212e775c39de19991bb953c9c0828b4f63ad8ba9f8de3ed18cb3a`

```dockerfile
```

-	Layers:
	-	`sha256:5ce86537f5aa4e0562825bca55725f4f08d87bf54452ee675c59555aa18e15b8`  
		Last Modified: Fri, 22 Aug 2025 20:26:18 GMT  
		Size: 10.5 MB (10460614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dcf2058ee05f05b66f17d132b9b9d96648eea25beae41f68a66395fd6f32ff9`  
		Last Modified: Fri, 22 Aug 2025 20:26:19 GMT  
		Size: 28.5 KB (28475 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250815-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:07ff94003fdcdb8ccb4cf43dcbc9f88f2bb3ccb244a4fbab8b85e39b59085aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285340409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f851a6aa7b9bd798cd20ae918e8f170098b3705877b148ac98eaf5033ffa44`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOTOOLCHAIN=local
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOPATH=/go
# Thu, 21 Aug 2025 20:07:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Aug 2025 20:07:19 GMT
COPY /target/ / # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af75c300f83884b3a2b4352096299334113ee00d6718ab116cdad0fd28ea4064`  
		Last Modified: Wed, 13 Aug 2025 03:14:49 GMT  
		Size: 24.0 MB (24020172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd6f1f2a58fa1289478b7c4157102354638b354f847958c5d7c5b4449c508e`  
		Last Modified: Wed, 13 Aug 2025 08:03:43 GMT  
		Size: 63.5 MB (63497769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46ddef82679eb8cfd4c812771b109c61028186c876518a5ed5996cecaff887f`  
		Last Modified: Fri, 22 Aug 2025 17:37:49 GMT  
		Size: 69.0 MB (68975042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3316bff964f9f759871a9216a703323b51e64d4b58eb53b6a858e7831c8cd357`  
		Last Modified: Mon, 18 Aug 2025 18:40:20 GMT  
		Size: 81.7 MB (81697402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b1a5cd92e71bdf42ff53a26578ed1ed30443dba8964a32d8ec337ce3c08766`  
		Last Modified: Fri, 22 Aug 2025 18:14:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250815-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:62877bd47e9393138791b2c08e17633f3bb86ccd27904f5f76594bf70c91686a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10348330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc0f8bc987f273076eb3ff538dc9a05a59d5f673f215d3ace29f66d015a02c2`

```dockerfile
```

-	Layers:
	-	`sha256:30b2f8b8d10c7d020609d88c6d2d1fa1d92c63934bc986ebf65006243e3fc101`  
		Last Modified: Fri, 22 Aug 2025 20:26:27 GMT  
		Size: 10.3 MB (10319901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:087bc6405c9674c13586c71e88bb316953d2e2d672cb700a98233e462154990a`  
		Last Modified: Fri, 22 Aug 2025 20:26:29 GMT  
		Size: 28.4 KB (28429 bytes)  
		MIME: application/vnd.in-toto+json

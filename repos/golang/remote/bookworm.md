## `golang:bookworm`

```console
$ docker pull golang@sha256:c4bc0741e3c79c0e2d47ca2505a06f5f2a44682ada94e1dba251a3854e60c2bd
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

### `golang:bookworm` - linux; amd64

```console
$ docker pull golang@sha256:c3dedc45bf4e47a3d94eeb6aa65a1f085e3810c6cc54a33633cd050e03ed2a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289335459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93df0ec14a0a2cbbedb5a7ddf4775345dae08d77414b9d427555ad43b1832146`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5073558d5a5274440fddfe987f56645dc90b8b84481e9e3dc858ac3311e33e`  
		Last Modified: Mon, 08 Sep 2025 22:13:51 GMT  
		Size: 64.4 MB (64396915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f695821d000cee45afdfe19101f31baa43771c64924d903cf125d742a77485`  
		Last Modified: Mon, 08 Sep 2025 22:39:15 GMT  
		Size: 92.4 MB (92386171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330457f0054be4c07fbaeac90483ac4f534113ccd944fe16beb9e079a3ab3a36`  
		Last Modified: Wed, 03 Sep 2025 18:49:05 GMT  
		Size: 60.0 MB (60045609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b224783a0fbe96c1da9149c6063c20a22f1c2569482bd0d0bde36f2e1caf2f8`  
		Last Modified: Mon, 08 Sep 2025 22:39:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:47c7d39aaf7913d452c2ac64546150951bbefb23d107a6f35ef79a3df6e14ffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10523579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c0d4f06316609c9e36e5af9d7cf0325d637e65f5455df469b31e31a39770b1`

```dockerfile
```

-	Layers:
	-	`sha256:1fdeda19396093f6519f6a63484607ef167642b50319d18c12eaaf833d8d4f8a`  
		Last Modified: Mon, 08 Sep 2025 23:22:42 GMT  
		Size: 10.5 MB (10495740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fd69c111f78d0d8e2c818b9f067feca8afd66c9d21a658c8f760cfd8407d9a4`  
		Last Modified: Mon, 08 Sep 2025 23:22:43 GMT  
		Size: 27.8 KB (27839 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:ecfc5e529b88f5a8e8bbd93a68f2219355dbe7c762d0949af5eca2b6880552dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (250997364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70fce85884e32bfebffdf0b3ba66517cbc8b76885b646dacbf58faf0d023fd5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ad8fb006981127731180a5d548f700fd609cacd7e365cb66fbcaf2fd1e979c`  
		Last Modified: Tue, 09 Sep 2025 06:17:59 GMT  
		Size: 59.7 MB (59652826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3992a4a78ea6ad3253d43b3d0d5184a728909de1c589e7792ee077bf0db5345c`  
		Last Modified: Tue, 09 Sep 2025 07:10:11 GMT  
		Size: 66.2 MB (66239127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec999c8e928607a0bc4da54080226a6c247c744815a64f6c10bf38b015958ebf`  
		Last Modified: Wed, 03 Sep 2025 19:08:36 GMT  
		Size: 59.0 MB (58978176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44979a3987a2d5fe772016be9438768a8dd1eba1b7d42a5138174109cae135c2`  
		Last Modified: Tue, 09 Sep 2025 07:10:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:581e7a48842c5514f3259e6904441b98a60fa4c190d4559e617c5f4098d7ec56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b0e96e9950d98197dfdf2df4cb557c0b659cbc3d2835945473c0f3b1eb9b3e`

```dockerfile
```

-	Layers:
	-	`sha256:0680fcb05fc7cf9abd236a39a314ed56491265889965f40c8bd353806c0608b3`  
		Last Modified: Tue, 09 Sep 2025 08:22:38 GMT  
		Size: 10.3 MB (10302454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7346d39b7732223519fbc1d2a9c80e98d80a1edd0e8b07cd8c2ada86ccf4e34b`  
		Last Modified: Tue, 09 Sep 2025 08:22:39 GMT  
		Size: 27.9 KB (27946 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5b750ccedb9945199e8cea0fff0ffdf0d190353ed835930c680e1286a56e0330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280337032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940eafe910b9988d43f46247f3f99bf986bb34e050b25d64d7d9a31f9e4a16ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133142790bc081eb3e5455996df5c3f98df543c5a224c3643437a19d4d6a7d93`  
		Last Modified: Tue, 09 Sep 2025 02:12:12 GMT  
		Size: 64.4 MB (64371181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1047a9797249ed6c1a3f00080eb5dfdcf976f837263a3cf4e620ac922e85c55`  
		Last Modified: Tue, 09 Sep 2025 03:13:17 GMT  
		Size: 86.5 MB (86456406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4681030a890db37290ab2fddf45adb75dbd1fbf983ba1b16efefb7221b97b1ec`  
		Last Modified: Wed, 03 Sep 2025 18:48:35 GMT  
		Size: 57.6 MB (57555480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9e12c6a2278980d5b40259f18b7c105a69488f2d859dba3296625566b3dec3`  
		Last Modified: Tue, 09 Sep 2025 02:48:48 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c4217feca93507c6a5e5cbf221fe7f8e363d9a040140805e5afae4cf058139bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10551561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68bc387bfd72cc4caafc419afca48c69e01fa867383287cb31e318f5492f5759`

```dockerfile
```

-	Layers:
	-	`sha256:c7eec0d30d6236172c23f6f5faa03eae58c19188d9af640333bbc016a0ee82d2`  
		Last Modified: Tue, 09 Sep 2025 05:22:48 GMT  
		Size: 10.5 MB (10523588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:715765b4ae4f46f0eac74c907fd485e520738ef7e61d3b43902f7990233446af`  
		Last Modified: Tue, 09 Sep 2025 05:22:49 GMT  
		Size: 28.0 KB (27973 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; 386

```console
$ docker pull golang@sha256:13c97c7426c9310c604cec10f18b29c74f975584ad249f73f6ed5289b274f7bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289131833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af91cb2f1afd9c597b4e225488c1ce5abf5aeab697689934694683459ba34b75`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5538e96bb7df1a7ef01bd7fcbf51f4cbc041246109c06cf661f7058c203851af`  
		Last Modified: Mon, 08 Sep 2025 21:12:26 GMT  
		Size: 49.5 MB (49466684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822d7073f1bfbc05d754234ff0c82bf81a44dcb6b19979f28688d3054a71fa6a`  
		Last Modified: Mon, 08 Sep 2025 22:07:56 GMT  
		Size: 24.9 MB (24860658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2248c0dfdaafb69ef95f2c3162eb9698e04d446b6646131ff2e543b79a6f79f`  
		Last Modified: Mon, 08 Sep 2025 22:39:17 GMT  
		Size: 66.2 MB (66233051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4132978c8205198916a37f06105ad2fd07fb631e0ffeecb14abdb9f5b3fabdf3`  
		Last Modified: Mon, 08 Sep 2025 23:12:30 GMT  
		Size: 89.8 MB (89807234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8134730600d4cfc74c5293aacb74478de1de4810632b08ac46dafe23f69bbce`  
		Last Modified: Wed, 03 Sep 2025 19:04:05 GMT  
		Size: 58.8 MB (58764049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8147ed5ddd3652b53f88b5edb8cd104c8af7e41f5c3ea6d269a30e0c7cd99970`  
		Last Modified: Mon, 08 Sep 2025 23:12:06 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6194f2a63b7294e5f32f2ea93f8dc84eb78f22664e435fefcb42299424da88f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10503117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a8e7a39ca84bf2661d2611073b9b73e658034f0306a37d349c8fe1fc0aac8f`

```dockerfile
```

-	Layers:
	-	`sha256:de37e22a6913dcdce86f3f5980f1fcad17b651ce635d28e827c15923c276c8d3`  
		Last Modified: Mon, 08 Sep 2025 23:23:05 GMT  
		Size: 10.5 MB (10475313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4680b631ce7fcdafc507c2f8dfef2161400cdaf25236eadb32a3e6f036fe8e89`  
		Last Modified: Mon, 08 Sep 2025 23:23:06 GMT  
		Size: 27.8 KB (27804 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:9c4d35347dd0e21d78441948b20011503934d336d8404835cb498b317ea89cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262140189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cc50e13e2eb14450e4aac377fc9e68f0f5f5a3f1f131106e76be413e749261`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:32b0a76df497911c1adc85f7748d78b916d66733f6d0c87cdc6e9eb06317a625`  
		Last Modified: Mon, 08 Sep 2025 21:14:25 GMT  
		Size: 48.8 MB (48760780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4b1410ff953e9baafd271cda9e27ee11dab33c7404024b5d7f0a941e7606c4`  
		Last Modified: Tue, 09 Sep 2025 04:22:26 GMT  
		Size: 23.6 MB (23611387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee49a4f2d47eca9eb39dcaf1cce76f6da099edc10cb571b790f8588eb5731614`  
		Last Modified: Tue, 09 Sep 2025 17:57:06 GMT  
		Size: 63.3 MB (63309380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2399203c3f138949b9c739767b010496dee12253a25cf54ee57e03160f9ff7d2`  
		Last Modified: Tue, 09 Sep 2025 19:26:08 GMT  
		Size: 70.0 MB (69979855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d29a42ef2530f05f5cf537801a54b97139f5ccd83724c719331ac0f6142402`  
		Last Modified: Wed, 03 Sep 2025 18:52:00 GMT  
		Size: 56.5 MB (56478629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577eefe914dce9189220ef96a6b649d94ace0f5cba9fdac1cffbf15363dbe1b4`  
		Last Modified: Tue, 09 Sep 2025 19:26:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b4dc6868dcacd1b39fc1bee569dded8cd4bd584d657c55ce4918b91a32a7efed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 KB (27697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bf406102103cc4fbbe658591f242a52f08212f8500aa36536c23be910e3722`

```dockerfile
```

-	Layers:
	-	`sha256:875dfada0c616096a739cc19bb659e7a3eec67d7af6511e2f544bccdaa30b3df`  
		Last Modified: Tue, 09 Sep 2025 20:23:08 GMT  
		Size: 27.7 KB (27697 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:f1d041f986c73b3b52728e4f51c470d769180c2932c217aee5599330c42e7861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296280121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38deee867ecd83322023453e5563e2763ce86c233e4274d5e09a211d3f3dd701`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b92467bcafecf194d3c4efbee466dcb9b2010a0899f7d2b928f9afed69de0`  
		Last Modified: Tue, 09 Sep 2025 04:47:21 GMT  
		Size: 25.7 MB (25668980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aad37d5c4461745e898b391fa21157366a7f13cf28ff4bbb1e1434d87664d3`  
		Last Modified: Tue, 09 Sep 2025 15:23:55 GMT  
		Size: 69.8 MB (69845800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65970e4339f44b2e14d292b7e7a36e775e579313b1e90a476ecebb14d3b3d8a2`  
		Last Modified: Tue, 09 Sep 2025 21:55:53 GMT  
		Size: 90.4 MB (90402199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9295eaa21ceb778d7859c40f41ccdf7cdeffaaa99a56ac388f747e3eb72308f3`  
		Last Modified: Wed, 03 Sep 2025 18:50:02 GMT  
		Size: 58.0 MB (58036165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289250ee5eed4c55189b0079f20f7ce7afa3472535de48422e98e0cd35bd9b81`  
		Last Modified: Tue, 09 Sep 2025 21:55:33 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5d0667ab4264bf15e16844254616a433e6ac8014bde26d5008e905e7e073e4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10496119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d753dd17f9e19931c68731c00af611ce9116ac3542000af9eecc8189ca48618`

```dockerfile
```

-	Layers:
	-	`sha256:0858efaf11c93cf58afc98198eafea1fddca7c0b19c31d9c5e925c52cd5939a1`  
		Last Modified: Tue, 09 Sep 2025 23:23:12 GMT  
		Size: 10.5 MB (10468233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40786cacac4fd434de1d6b92cad520e84cf691939907347e1c586e58e5510fe3`  
		Last Modified: Tue, 09 Sep 2025 23:23:14 GMT  
		Size: 27.9 KB (27886 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; s390x

```console
$ docker pull golang@sha256:49ce5833f7e725053fa37ef0e24676376dadb08101470004d377015fa760a791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263031185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f7fcc655bbadd55137f0f5d1cea16aa50280c41c6871f3b69b1fceff81760a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f0c679ec7b70d7fa5065a6e28276437547a7d43502b4e016c2e85aed8c84c`  
		Last Modified: Tue, 09 Sep 2025 01:20:52 GMT  
		Size: 24.0 MB (24023865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed122f74eb7bf77b1109cb95e13be357040ccb22119f5f02e566a491bcc45e`  
		Last Modified: Tue, 09 Sep 2025 17:52:15 GMT  
		Size: 63.5 MB (63501842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ddfb71300e1d87b007880baa135308d1daa68b727cd83e228a0277cb0e12a2`  
		Last Modified: Tue, 09 Sep 2025 19:10:46 GMT  
		Size: 69.0 MB (68989593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af48389d563ccb39441056114ee8bb4fefdded621ed594eb028cdf9787ad997`  
		Last Modified: Wed, 03 Sep 2025 20:23:25 GMT  
		Size: 59.4 MB (59378188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2fb993de4e894093c708bf212413f571b2125fc1c827f303098ee24100fe51`  
		Last Modified: Tue, 09 Sep 2025 19:10:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:26dcd18495035e16f44fc90fccb515fe3b627da5d98c9c67589d48b9c6eb7fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10355338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28942c03d2d90fe6246eea33e27e054b56e1b808e56dd89f7e547c1e8b559aa9`

```dockerfile
```

-	Layers:
	-	`sha256:943763128e764ed33dd9911ca12c042d3634db0cd96231e6f4257d723c6fd4b2`  
		Last Modified: Tue, 09 Sep 2025 20:23:22 GMT  
		Size: 10.3 MB (10327498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b12695fe30222b9839622bfc0bcf95487dedafcd8e2100c40b1609c4f18d70`  
		Last Modified: Tue, 09 Sep 2025 20:23:24 GMT  
		Size: 27.8 KB (27840 bytes)  
		MIME: application/vnd.in-toto+json

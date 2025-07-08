## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:dea5284ad9624a9cf9bb687e0506f7d9c694cb4283e0fb854b24bbcd3d66d788
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

### `golang:tip-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:303cd441a1eef717dc555d5ed7ec2662ed3649b0874f22fc52711d56340449f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 MB (312356393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b2e6592693c2a366875bf2d49a7b2d2f0a44c646265e56cb48b1fac0a8e840`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70151763f23e129416a9ace117a26a1a30f7614b0aa83aa871c9406f671a2cea`  
		Last Modified: Tue, 08 Jul 2025 20:42:41 GMT  
		Size: 92.4 MB (92355253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9b1bf1df4ddb6cd2f3ba43fc263309f8c370fe86f15d3de62305a26c4885e3`  
		Last Modified: Mon, 07 Jul 2025 21:08:01 GMT  
		Size: 83.1 MB (83086126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05089c7cddd5bb06052a74f3ab71e56846ae96036b2a2fed0341630cb0c454e`  
		Last Modified: Tue, 08 Jul 2025 20:42:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e36d1b66ff6b142090f851506dd0e9fcec9ce9b053fceaf48e33e893e4dc583b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10516404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140776c1aa3b11ff48fb1c98ceae233e675c8a64a898e037c9ec046bedd4c7b0`

```dockerfile
```

-	Layers:
	-	`sha256:3ba827092ebf6c7e6c1cf5f8380fe83eee40d996f4a5b9e858ba89f96f4d866b`  
		Last Modified: Tue, 08 Jul 2025 20:29:45 GMT  
		Size: 10.5 MB (10488745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3189e23993b98ea0e1b26d8bf46f65bb5b704190309d8812fc70ddcdb8392c00`  
		Last Modified: Tue, 08 Jul 2025 20:29:46 GMT  
		Size: 27.7 KB (27659 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:e9108b063a022cd708dfd72c4635de4e3ee463bb9e0ebb4a3295a3f317171a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272182687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e99b164a1dff39f502707a59b6f7f61bb4c3c6d421418b89d3cda176754b7c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bc2e28ca8cdb751a10e1e014b374d783cdfa924e032e1f9eb674e7fae1220927`  
		Last Modified: Tue, 01 Jul 2025 01:14:29 GMT  
		Size: 44.2 MB (44208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcc606b1195a348c6a47399c1a54ab936d4477a526d62306ddce89fe76a2d22`  
		Last Modified: Tue, 01 Jul 2025 08:59:56 GMT  
		Size: 21.9 MB (21928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f4c85f426e2c955b1dac4fa88bc182d725644c23ad01bdcbf64d9664e34a8`  
		Last Modified: Tue, 01 Jul 2025 18:28:59 GMT  
		Size: 59.7 MB (59656492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01db66a5672ae3586307aae98741965819f3d140302c02b7d781087e66393285`  
		Last Modified: Tue, 01 Jul 2025 21:45:51 GMT  
		Size: 66.2 MB (66208443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69fdb869efc0a02a2300329eae27592000268e157c8997d8c67d1e2518080e9`  
		Last Modified: Mon, 07 Jul 2025 22:02:14 GMT  
		Size: 80.2 MB (80181079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14aaad51db2df7b07ff5fa6b4966ca73704e7a5fb726b5d5bac12085fedd7603`  
		Last Modified: Mon, 07 Jul 2025 22:02:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:aee1fcc7d6e223393e93fd2ad25b797b2e8792aec9bab4855c211f1c575c86e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10323242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57dabc24830ca3ee4ee751274523caf23c55a279802c8fe3a26a6683275bdbc`

```dockerfile
```

-	Layers:
	-	`sha256:535690ffe6f0596567fa2cd98cf875a8868ceb893cd16999e09e8030a1fb7a62`  
		Last Modified: Tue, 08 Jul 2025 20:29:54 GMT  
		Size: 10.3 MB (10295459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a4727ec26dc59e29c82798641b2d4836cb9b3b390e0cc6f18dba1a216ed8afc`  
		Last Modified: Tue, 08 Jul 2025 20:29:54 GMT  
		Size: 27.8 KB (27783 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:74d3c79d718a4d232470fe89248240661f6832f27c330452495a5250591f21e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301736865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a0297477e79f1d509bcb6d2492e2806ca853dc07cc39324329e397e09226c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9cdd730a2c32e544c8de28ddcb3800bc8b143e551c286d3ccb2704444d69f`  
		Last Modified: Tue, 01 Jul 2025 13:28:57 GMT  
		Size: 64.4 MB (64363294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600757b9c81e03e94454dc99e102eadb0af5caceda3e8c19007feb5ecae82656`  
		Last Modified: Tue, 08 Jul 2025 05:44:43 GMT  
		Size: 86.4 MB (86425424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93fe74c58f17b8638ab4c828f8d4b865821c43447e64c8cd4bfbde5a810c7b1`  
		Last Modified: Tue, 08 Jul 2025 05:43:08 GMT  
		Size: 79.1 MB (79051196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d100e50aeb7f571e7876199c2b01ed47aac5b8f1b65e84d6d897108299fe22cb`  
		Last Modified: Tue, 08 Jul 2025 04:42:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:9287ae0b6524dad97e4084bc7870a688fc4369ce2f8989cc4acf37c13de3aff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10543296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c60ec9992ecea189141a3e8acafc6a942bb9d2748402fd8c76ac6a9b29ad6d9`

```dockerfile
```

-	Layers:
	-	`sha256:0fa249f8d32e3e640ef1257b32ac8c4b8b2239ff24b6f801745092173aa766e8`  
		Last Modified: Tue, 08 Jul 2025 20:30:03 GMT  
		Size: 10.5 MB (10516593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56a84f0b73518321c022662eeefd0d74aa7d77174c52cca6de900b294f5a92b2`  
		Last Modified: Tue, 08 Jul 2025 20:30:04 GMT  
		Size: 26.7 KB (26703 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:eefc8661d5cb1ac20340dd1e9f49a0a9f2566a5b7927fb7a69283f04e6705b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 MB (312154790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3710d5606cf68f71e2edafa5fc5b373d6b801bc3a8d8add311e04f3404aa9c5e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8f46577375004356dcdcda0b1eb9cdda01e0943d00443270daca69a2ba1d0`  
		Last Modified: Tue, 01 Jul 2025 02:24:27 GMT  
		Size: 24.9 MB (24856933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952009550cca50c5a8b42bdeb6e9116dacc2baceb5799f97bf16934eed752ae`  
		Last Modified: Tue, 01 Jul 2025 03:20:00 GMT  
		Size: 66.2 MB (66225317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7634121e6b6d081a818c420b64c141cc40e2b79b6d992445a10c5f52e20a41ab`  
		Last Modified: Tue, 08 Jul 2025 18:11:45 GMT  
		Size: 89.8 MB (89774582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9fd65ade23887bad8cc24159556378a6549464832612b1c87e5e65754cc9685`  
		Last Modified: Mon, 07 Jul 2025 21:08:46 GMT  
		Size: 81.8 MB (81820379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f15e93ce1fceedcdd6dace103307bc97f5e6711c846678a1ab9b4838f6927b`  
		Last Modified: Tue, 08 Jul 2025 18:11:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:945d563793130d084accdacbd0d2c510b0fdf1ded9278099d73175596a296b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10495939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e9e2e81ca91a4ffa63c90274785ae0438eaa498faca3ffce4ac07da14ed00d`

```dockerfile
```

-	Layers:
	-	`sha256:cda21092f0d66431424d5967b30d0f297033f40d373979ac902df65d9460c40f`  
		Last Modified: Tue, 08 Jul 2025 20:30:12 GMT  
		Size: 10.5 MB (10468323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3288bd0ac81a4627e821b0dbe80d8ba54f4e7f7fe12ebf6913c1b1e51595276f`  
		Last Modified: Tue, 08 Jul 2025 20:30:12 GMT  
		Size: 27.6 KB (27616 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:a3c09b820b834543ad816c80ef7f022109fac65d5af56094bba5bef96d275851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283448616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0c56f8375fe97412662b4b297e2d43add6ed42dc05e7dc666846eb526076a2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:99debc858569995ebc7f6d9290cbc19f540a471b716e06514603892b92705c6c`  
		Last Modified: Tue, 01 Jul 2025 01:14:35 GMT  
		Size: 48.8 MB (48775546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1158647b6db84897a383ed457f276b7c4d602a99d74b1c159bd2c138fd994fd1`  
		Last Modified: Tue, 01 Jul 2025 18:49:08 GMT  
		Size: 23.6 MB (23598851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3ea11d1e2f3faf8589ad741098f10976c65ebbdefe26521e25ec1f6abde856`  
		Last Modified: Wed, 02 Jul 2025 03:03:00 GMT  
		Size: 63.3 MB (63308526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490218841cb4006ccea3788c2da907c733bc1f20eaff61ff40fda60e6510af0a`  
		Last Modified: Mon, 07 Jul 2025 22:51:57 GMT  
		Size: 69.9 MB (69945605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd583f32ad8ca5ce8f1af178a35eaaa1ac5bb073d6c7ffcf91876ea3497aa673`  
		Last Modified: Mon, 07 Jul 2025 22:51:56 GMT  
		Size: 77.8 MB (77819930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93524b60d8f8f3eb2b058dfc0594d0729b8a88947ce54bebff0b2177ce067d0`  
		Last Modified: Mon, 07 Jul 2025 22:51:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b1549f1cc540e34919efbaeda2ed7f86e5c597d254d4712d963c45f25217e387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbcdc00f61d52241525386df33c8c4c574a16835e92d0deaf36fbb9f2714f51`

```dockerfile
```

-	Layers:
	-	`sha256:64e6639d11f9a7e2e8caa5403d09c17586651845e214732c0e05aa53b8b96e9d`  
		Last Modified: Tue, 08 Jul 2025 20:30:18 GMT  
		Size: 27.5 KB (27531 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:1c4d90f4f63ad1187a609276dbbf49c13f0879493d54ba69db76f79b0f3ae3b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318569515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36027028c1b8438d14d731324981f3166ba8282b5f70520e14196ba9d23feab4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7082fff0db11ec79e9a3c8fc9c05691e086d30ca51023010805fccbeac2b8dad`  
		Last Modified: Tue, 01 Jul 2025 05:07:55 GMT  
		Size: 25.7 MB (25663667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e6cd79d875ce6ba17d2080d5bd4d0d55f7eec0f6bb923ae0b53e5bec14ef9b`  
		Last Modified: Tue, 01 Jul 2025 10:09:38 GMT  
		Size: 69.8 MB (69840014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57d9349410a306544d8415703fe52cf359c3239d46bb47a0ff96b2173c5c707`  
		Last Modified: Tue, 08 Jul 2025 00:33:30 GMT  
		Size: 90.4 MB (90369347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22b55aa5c49337c93ecd39f723f408177c4f428404ab6858571184b51126cd1`  
		Last Modified: Tue, 08 Jul 2025 00:16:14 GMT  
		Size: 80.4 MB (80359086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54eb7d45cbb167d99a9f75c90fbfeb3c8cc33e3b7f605f80880b4828c057841`  
		Last Modified: Mon, 07 Jul 2025 23:03:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:884b36eab5a4a6271d7cd83667840803dbb940563f56a078cc0515c76ee4f1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10488945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcbfdcc512b89e3313aec9dfffeaddf91dcf9e9d31d55d0ddb66c35a49d8b50`

```dockerfile
```

-	Layers:
	-	`sha256:426d1451ea4b5c49ac5c1a787612c17fbff7fe2a55005da01f200f78d7cbcadb`  
		Last Modified: Tue, 08 Jul 2025 20:30:22 GMT  
		Size: 10.5 MB (10461228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d9f7b9f58125ddb11f72db14203a49bc9c11e0d9286fe7827daacb518a0dd1`  
		Last Modified: Tue, 08 Jul 2025 20:30:22 GMT  
		Size: 27.7 KB (27717 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:be9439aef32b84c67f51a9a5cc220b46ad2e8e007beb5e9d7f67a250bcf7fbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285223852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49137d93405d2ffeacd84ae881007a5171ea621c07402ab08e5a234e05db42c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dca9cef3741351ad228dc4986e66f3e324bfb88d5cc9e2b190dd3a3abf7dcf`  
		Last Modified: Tue, 01 Jul 2025 05:30:26 GMT  
		Size: 24.0 MB (24020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff1e32b479a11528098c70ba4af6292099abafcb29e0823d2861c86032c9b0b`  
		Last Modified: Tue, 01 Jul 2025 13:41:28 GMT  
		Size: 63.5 MB (63497964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c580e287c9c366a32f1f5f19f852bd00d4ee67c95b7a4b3e443b2e65c5cccd97`  
		Last Modified: Mon, 07 Jul 2025 21:28:53 GMT  
		Size: 69.0 MB (68957938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff319e613d7718d33c97b2a4d68807464c2ed71607411d5eaa89b10ec085d5d5`  
		Last Modified: Mon, 07 Jul 2025 21:28:58 GMT  
		Size: 81.6 MB (81597964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1668e195dc57bea76e011a3a6b8ab02b1814c7703831647ec5fa3c3b5e6b6d`  
		Last Modified: Mon, 07 Jul 2025 21:28:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ddf0e2faec5fdeef662737c4044990b45ade3e4a9df6f2558f0328bb8ff97d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10348162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c34698dc7a668b50875054dab7760e959f75ba9a26b74b1440843647e1a61c1`

```dockerfile
```

-	Layers:
	-	`sha256:e2958a3f09e33c1a31d9bb04e5e1f663273f5f1a579f7785017452574df31879`  
		Last Modified: Tue, 08 Jul 2025 20:30:29 GMT  
		Size: 10.3 MB (10320503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6602f4ef1b533feb8a51d1c3f54d5c0b3e8a435afb433ad287d4d02f44e20895`  
		Last Modified: Tue, 08 Jul 2025 20:30:30 GMT  
		Size: 27.7 KB (27659 bytes)  
		MIME: application/vnd.in-toto+json

## `golang:bookworm`

```console
$ docker pull golang@sha256:88cce69058466d1e99c5b46bdf4aacd0814278492f9fd30eb0b311212a2d023b
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
$ docker pull golang@sha256:414a753c2f67d0efccb01b5f58b3d3a8a2cbb7c012ce9e535418b5b3492b2c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289459115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbfc044b250369472b7482dc5150a1fff98d095c25d494d4a23b3d1511be210`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 07:44:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 07:44:27 GMT
ENV GOLANG_VERSION=1.25.3
# Tue, 04 Nov 2025 07:44:27 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Nov 2025 07:44:27 GMT
ENV GOPATH=/go
# Tue, 04 Nov 2025 07:44:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 07:44:27 GMT
COPY /target/ / # buildkit
# Tue, 04 Nov 2025 07:44:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Nov 2025 07:44:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb445e472b1bad54f5a28edd51b11aec79eca8513394866a261891be9da6a343`  
		Last Modified: Tue, 04 Nov 2025 00:28:00 GMT  
		Size: 24.0 MB (24029301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2123190679e81d983648da92f1bb9ddc74383512edb00ad64f93d24d00d8807a`  
		Last Modified: Tue, 04 Nov 2025 04:14:49 GMT  
		Size: 64.4 MB (64396145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a0646cf7f3883f5b009a5b8b6b36882473e2914632d6afe1a30a693e4e3f36`  
		Last Modified: Tue, 04 Nov 2025 07:45:13 GMT  
		Size: 92.4 MB (92402102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91631faa732ae651543f888b70295cbfe29a433d3c8da02b9966f67f238d3603`  
		Last Modified: Mon, 13 Oct 2025 22:32:32 GMT  
		Size: 60.2 MB (60150352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fd8b62e9efea39067bb86ecf3309d1f4b119d829fb4d96a2eab004d43959c5`  
		Last Modified: Tue, 04 Nov 2025 07:44:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f42a1da81a7efcd919d09a6c52949f199ffe95cd66bbf1e4424f862c84967728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10523537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f55d6f66a8c4c14fc959ec28c7a28d7becdff9f2eb9322f542aad2d9ea99ba9`

```dockerfile
```

-	Layers:
	-	`sha256:cac7b54629e0da28d0ae30cbb6c566abf4df128c33e7da41f93422392ebf6e03`  
		Last Modified: Tue, 04 Nov 2025 09:22:39 GMT  
		Size: 10.5 MB (10495740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4dd97c2bb655c75e00051a4f0f66249c46152422932b4e99154529ca0f4d5e5`  
		Last Modified: Tue, 04 Nov 2025 09:22:40 GMT  
		Size: 27.8 KB (27797 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:84b002e3f969e69f3b970442f988590cf38b3d8114e806d5aabb346917d924e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251111610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ec47e7890a1e776ff1ae37e0cc263a9ab004690db7b0dc830c7a3ba3ba1690`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:17:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:23:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:23:51 GMT
ENV GOLANG_VERSION=1.25.3
# Tue, 04 Nov 2025 03:23:51 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Nov 2025 03:23:51 GMT
ENV GOPATH=/go
# Tue, 04 Nov 2025 03:23:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 03:23:51 GMT
COPY /target/ / # buildkit
# Tue, 04 Nov 2025 03:23:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Nov 2025 03:23:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:461f215c759f019a0fb4d33c976a91c4c2e4b033762b07a2f81bac66dee9e613`  
		Last Modified: Tue, 04 Nov 2025 00:12:30 GMT  
		Size: 44.2 MB (44196437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad602f359c1ad647108cc57270e592fc1f62f8ffd947a100fecee62a4a0d017`  
		Last Modified: Tue, 04 Nov 2025 00:39:15 GMT  
		Size: 21.9 MB (21934879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4c6c96cff86026dfac835fc2d229a348ec06ff2d2c520014ac2aeb4555bd9e`  
		Last Modified: Tue, 04 Nov 2025 02:18:15 GMT  
		Size: 59.7 MB (59652141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b08a78287cb90cf6e81465571017cae4b67f872276579792b733829fa0a1c3`  
		Last Modified: Tue, 04 Nov 2025 03:24:36 GMT  
		Size: 66.3 MB (66255045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af0985c887920d8ad25f36932e706271ae84032a3ae370b1f5325188b8578bd`  
		Last Modified: Mon, 13 Oct 2025 22:33:14 GMT  
		Size: 59.1 MB (59072951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96129a9961b6d334982753f185cc16f40dbe16578fafbf2f0420620d76fa96f`  
		Last Modified: Tue, 04 Nov 2025 03:24:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:80f3cea34e65362cba33d0248c61863e87d972ffb7d6bc6d0d8a29b7639d07b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bf167ca9df0ce5087cdfa6153d2983cf55874112dd8d78860b9f5e4bc46746`

```dockerfile
```

-	Layers:
	-	`sha256:13a736d07a587ee4b9b9d6d04fc7c4234ffdb570614c7845376479f7235da14e`  
		Last Modified: Tue, 04 Nov 2025 12:22:47 GMT  
		Size: 10.3 MB (10302454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42331d27a7fca1c74cbed696cb9d20f92ab8b30f11abec2ad013763503a8faa9`  
		Last Modified: Tue, 04 Nov 2025 12:22:50 GMT  
		Size: 27.9 KB (27903 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:8b7ce5461b6624171a9a9d1f4fca3f9c42d840d3b0ae22f4ff254a876f92ef11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280451951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb5c24705a64403151cdacfe1a60d61bb8b2beb50f99cba72ef2f24cc7c7adc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:29:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:22:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:22:36 GMT
ENV GOLANG_VERSION=1.25.3
# Tue, 04 Nov 2025 02:22:36 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Nov 2025 02:22:36 GMT
ENV GOPATH=/go
# Tue, 04 Nov 2025 02:22:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:22:36 GMT
COPY /target/ / # buildkit
# Tue, 04 Nov 2025 02:22:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Nov 2025 02:22:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463896571d3ff5317461a64229e9e4cb27d6d877114079419cf8b4fc96b0c02`  
		Last Modified: Tue, 04 Nov 2025 00:30:33 GMT  
		Size: 23.6 MB (23598514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020f0f7f102dcd1ca7603a86d7398adbe5369a820cc6f32954c0b3b5e2ac7403`  
		Last Modified: Tue, 04 Nov 2025 01:30:05 GMT  
		Size: 64.4 MB (64371335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd40c9b1ae005a04f7165c99ce2ae27c4e772cbf0c186575573da6f6ddc4dd0`  
		Last Modified: Tue, 04 Nov 2025 02:23:15 GMT  
		Size: 86.5 MB (86472305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dab1238d3d9c3bd1753609badeac4c19b7239aef9927c6dc13db4335a66b568`  
		Last Modified: Mon, 13 Oct 2025 22:33:13 GMT  
		Size: 57.7 MB (57650163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bef84de6e1d62363c78f78412f151e7e61ae4a4e12545bed0d62eb79ccf93e`  
		Last Modified: Tue, 04 Nov 2025 02:23:09 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:81c71d5ad1df48e189a9261c3b1801c0ac9e65f08aaf52708058875978d15721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10551519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1607868c7f4065a4ceb3ed61b75ff43965516237b8cc48ee2bd2998222f36c0`

```dockerfile
```

-	Layers:
	-	`sha256:8557e1bdf1bb8b0ebad7dc6e697e53e59e182e529c09d3814b87d7c6bee071f0`  
		Last Modified: Tue, 04 Nov 2025 12:22:57 GMT  
		Size: 10.5 MB (10523588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea61fe493de973830982ff1bca51810946422a8323f5059f7b9677069051b8`  
		Last Modified: Tue, 04 Nov 2025 12:22:58 GMT  
		Size: 27.9 KB (27931 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; 386

```console
$ docker pull golang@sha256:cd21745063807bd350277f8773d956b4b4b5c703c0015a5a03daf593d87bc424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289259728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db8a326fbcca6842606803dd334ca36a80af83711b1baa0cb51f174a0d475cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:31:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:22:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:22:15 GMT
ENV GOLANG_VERSION=1.25.3
# Tue, 04 Nov 2025 02:22:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Nov 2025 02:22:15 GMT
ENV GOPATH=/go
# Tue, 04 Nov 2025 02:22:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:22:15 GMT
COPY /target/ / # buildkit
# Tue, 04 Nov 2025 02:22:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Nov 2025 02:22:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3a9907ae02a89d2535bb875a11c05038e0be4fa333c35747cd42f6f7b49e018d`  
		Last Modified: Tue, 04 Nov 2025 00:12:58 GMT  
		Size: 49.5 MB (49467114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce6be8e6c76b859a7e1808f7c9de22684a829f5386b5bf2011b85482d4d192f`  
		Last Modified: Tue, 04 Nov 2025 00:26:27 GMT  
		Size: 24.9 MB (24864369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b596182a9b4836dc17a3bc5eadc1e2798b0aa5aa0c8f50fec56b60d802ddb375`  
		Last Modified: Tue, 04 Nov 2025 01:32:07 GMT  
		Size: 66.2 MB (66233815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f08f07732287268052dfbade49bb6f6e96d9dc3d4d5c7a55c9861bf0431512`  
		Last Modified: Tue, 04 Nov 2025 02:22:53 GMT  
		Size: 89.8 MB (89823371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95a97777f39c24f1a92cb9717c8fb60aaa699bf624bf9ea8e2cf61d0d8d4abe`  
		Last Modified: Mon, 13 Oct 2025 22:32:51 GMT  
		Size: 58.9 MB (58870901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7db8f11c08d76587bbcbdf7555caaca7ee2f8703ef93dddfbe68f96e671c42`  
		Last Modified: Tue, 04 Nov 2025 02:22:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4c1de199108b718e24c764a0b50243054da7e1f9d2fda9b4d1c139c06520824e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10503074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046db89451636743fb15b6029d2a7e30d22d79ab9aa7019f7adde8472df9e574`

```dockerfile
```

-	Layers:
	-	`sha256:1cebacf2a5e4786b937eef635ddc36a6ce9336c7e25c98c430267e8e9556e451`  
		Last Modified: Tue, 04 Nov 2025 09:23:03 GMT  
		Size: 10.5 MB (10475313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:343301915fc95d79b7391437a4e2da692ae71beb8f8032cca02d70057f0fd550`  
		Last Modified: Tue, 04 Nov 2025 09:23:04 GMT  
		Size: 27.8 KB (27761 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:5c6a855e44ae1a01f9601f6d797892730bf1292146627bac0ab7581f21d2f7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262254983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96661fa629c65faaa4246517c3245aead234130183edef23f2aefb1d20804e1f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4ff7a7a0be4afa0c088333063434d872e5a67b49bc2165e0d5f1c8b45e31c387`  
		Last Modified: Tue, 21 Oct 2025 00:19:28 GMT  
		Size: 48.8 MB (48760743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ada83e05f36ace3b39ede326eee5e8c640f47f0d217601cc47ce49334a0f7e2`  
		Last Modified: Tue, 21 Oct 2025 17:26:33 GMT  
		Size: 23.6 MB (23613801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20eca72dd31bb50cadfd79b7ad12f89f5688c744f6a098004e516ee38f52407c`  
		Last Modified: Tue, 21 Oct 2025 23:43:20 GMT  
		Size: 63.3 MB (63309417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b8b987535d1ca746e1df1d7a5e1bbbe17811a45d2a394c4b90bfa962bb4cb`  
		Last Modified: Wed, 22 Oct 2025 01:07:48 GMT  
		Size: 70.0 MB (69997127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dd8206818bd27a5e75e0dc8f188f71d95a622e6e1f691d7856fde2440fc249`  
		Last Modified: Mon, 13 Oct 2025 22:33:13 GMT  
		Size: 56.6 MB (56573738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239cf4805b7095ff09ba201749cd1f9979d7287fd0223e6286020ac09529c53f`  
		Last Modified: Wed, 22 Oct 2025 01:07:36 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8837b5a56c2ed99c2c404499f712c03eafd16a54097b238f959285ccacd5ecd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 KB (27697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7c75da0d2916e4ad24bb83eb34f2b03694397299ed7616f6f70c08b72c696b`

```dockerfile
```

-	Layers:
	-	`sha256:c3bcfa9022ba4e4d461deae2af2cd4267445575f0d453c013be61e7aa722892e`  
		Last Modified: Wed, 22 Oct 2025 02:22:59 GMT  
		Size: 27.7 KB (27697 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:4c872de3d8926eecb0b7b31ce5a0443263daa3206739ca61282e27346628b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296397016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b0ce9661a3224751151f01ae8cd3214d1e489cc52b63b4b410c004ff033ebc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:297b234228c60cb6a9bc0156bdf582119f3c4f22112d7d2e8128e4d1403158cb`  
		Last Modified: Tue, 21 Oct 2025 00:19:36 GMT  
		Size: 52.3 MB (52326787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665a6d4e6976a738d68a77f188daf2501160c6ad54e4788282d2395e926b5e6`  
		Last Modified: Tue, 21 Oct 2025 07:42:57 GMT  
		Size: 25.7 MB (25672119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9014e4879ede8e5983b7a1a0f265054143b5d897d5a848c01fe4c938fdaa27`  
		Last Modified: Tue, 21 Oct 2025 17:30:59 GMT  
		Size: 69.8 MB (69845634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bdacc7744170991b6e3ec786cf581f2480e153c22dfc33bb6dd0e55bd8cf4a`  
		Last Modified: Tue, 21 Oct 2025 23:18:18 GMT  
		Size: 90.4 MB (90417857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd79e032fd555b767c904ba3576a69bc211a15c564010ebf1a3788cd00df21d`  
		Last Modified: Mon, 13 Oct 2025 22:32:24 GMT  
		Size: 58.1 MB (58134461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa0a4dd9299f1aa6f6ee2390e1348ad92f07397739e21af8da1a55dbe3698d6`  
		Last Modified: Tue, 21 Oct 2025 23:18:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3fcea4d09394b3dad6ead6b31408196ffd85a7add1029af7cbdd007ac91da317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10496120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e544f9b2ccc995e4b2beb970977866ed485d2bf7e08a57f989c1ec8983ba7a9`

```dockerfile
```

-	Layers:
	-	`sha256:74888dd425ff321660c30cb686ac889c0bbf9cc18fe2d4fde461e63d4482de70`  
		Last Modified: Wed, 22 Oct 2025 02:23:03 GMT  
		Size: 10.5 MB (10468233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5f1c348ecd4a1db44f3c04fcebe2ba5712154cbfa5ea7b82dde62c6ff5c8b86`  
		Last Modified: Wed, 22 Oct 2025 02:23:04 GMT  
		Size: 27.9 KB (27887 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; s390x

```console
$ docker pull golang@sha256:124fb4b31ceee79191680bc90769d816043584c5248d89ca7441c5cf19347274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263156340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbdca24a2aafd333f052150bb69234ce433d3edd98e22423f8f346f11c95852b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:769a86a44e9ad2fad1b0132047fcc9c080f859777f09d3856b818bc85f1c5895`  
		Last Modified: Tue, 21 Oct 2025 01:19:50 GMT  
		Size: 47.1 MB (47137521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ca271e8b0e27269a77c65ea555986eaaadf5db02b1ac24f66f8ce2e45a475b`  
		Last Modified: Tue, 21 Oct 2025 22:50:23 GMT  
		Size: 24.0 MB (24027291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944e6bdda425b877e973cde5b6c8eeabf7eed45bfaba0fd705b4f180a07f001f`  
		Last Modified: Wed, 22 Oct 2025 06:00:23 GMT  
		Size: 63.5 MB (63501423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e5329ef731e263d1c6b30e55e66153c9c0292e1db1f30d716baf43f0fd397d`  
		Last Modified: Wed, 22 Oct 2025 10:22:25 GMT  
		Size: 69.0 MB (69006838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cce485d826b4034b25b00ba2ffd0ae02402af07840c83aa561b76bede0f4bb`  
		Last Modified: Mon, 13 Oct 2025 23:28:51 GMT  
		Size: 59.5 MB (59483110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce790783db86bd19f94424a71242e4641216ba02fe2a0210cfaa9d958ad2b65e`  
		Last Modified: Wed, 22 Oct 2025 10:22:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5bb6302794c8f3ba32603d983c3aee959e96d3d2bb269a35b933185f5eedf587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10355338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4f2f783f6ffa4cf7586a99550f6a10263b553675221181b2441510dcb901f7`

```dockerfile
```

-	Layers:
	-	`sha256:7d7d74391414114a1ed87e92ba33b4debd2e748b06dc829b94fdd0d396ccb6e0`  
		Last Modified: Wed, 22 Oct 2025 11:22:54 GMT  
		Size: 10.3 MB (10327498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd92075db312b701f3e635cea74600fbda7794852a60ae5691a1e6660c4fc85e`  
		Last Modified: Wed, 22 Oct 2025 11:22:55 GMT  
		Size: 27.8 KB (27840 bytes)  
		MIME: application/vnd.in-toto+json

## `golang:tip-20250823-bookworm`

```console
$ docker pull golang@sha256:acf211daaa588f25b7001f056aaa51a1f37f37bf6715c081967b4e22c18ebdeb
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

### `golang:tip-20250823-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:760d01c93ba7dc47e76678c936c78c1dcd57c0431551b1cb37f01dc910b813cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 MB (312417563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72598a30d42d1f8a497ed786f5869c363f4f0e99d06833bd4849ecb493b720ab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 25 Aug 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Aug 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
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
	-	`sha256:847875f8ef06b1d4c3eb981d64107a2085b7b678bb9fcb40571c18e2598af6a8`  
		Last Modified: Mon, 25 Aug 2025 21:10:36 GMT  
		Size: 92.4 MB (92378414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d550b0c36e09ff5790a4933d03a35b9476508e0154ee793c00f79de3ac387e9f`  
		Last Modified: Mon, 25 Aug 2025 21:00:15 GMT  
		Size: 83.1 MB (83123589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b47cefecdd08daf6e8bcb4bc6a7eaafb1ff995ab96ea5f0765d811f9e081eda`  
		Last Modified: Mon, 25 Aug 2025 21:10:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250823-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8dfb38130a4da11277b6e74d5ae03576db88a886f714445b3ee85a6a35babb1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10516572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1158d31ef5dd03424717612eb298affbc9f3391f1c761a769ec8ee4b903e0bbd`

```dockerfile
```

-	Layers:
	-	`sha256:7c725dcbd2548905c018f300df59f58dbbf9de02596929ecf6386f6deb4a95fc`  
		Last Modified: Mon, 25 Aug 2025 23:24:35 GMT  
		Size: 10.5 MB (10488143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65c3a59d845ca223c0e417588307b08a52fcc6b568172692f261d405d62328de`  
		Last Modified: Mon, 25 Aug 2025 23:24:36 GMT  
		Size: 28.4 KB (28429 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250823-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:1239f698b6dd02d7b6615d8e4c9a2217ff7bd028664f1a6dacb42d8cec402a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272197371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086f3f40209972c71d42fc26d8e2e92997f73d97ca16e224fd5fad238698a4f2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 25 Aug 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Aug 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
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
	-	`sha256:9b7bbceab697cd612c9df9f47bcc80c06c8d22159be94df3795ecdee732a36e0`  
		Last Modified: Mon, 25 Aug 2025 21:33:11 GMT  
		Size: 80.2 MB (80158151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e732dee48153f5bb837aa91c9075a52b3083299e4d4b0cc230ba2705cd32438b`  
		Last Modified: Mon, 25 Aug 2025 21:36:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250823-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f2dc098404f35df7f60ba1057d13a904d78219e20e80bb08d2e4bf2991620853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10323378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f17200822919b71645837065a07be75789105e4783852b68c919cf523b53983`

```dockerfile
```

-	Layers:
	-	`sha256:4fd856d7873a2eee15d96f3dc4e6502e208b5dcfc471e17cd363910e8bb56176`  
		Last Modified: Mon, 25 Aug 2025 23:24:45 GMT  
		Size: 10.3 MB (10294841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c6c8bc9058b8aaf930d086569bd6d7d0f8353aa211df25279897be9c38696bb`  
		Last Modified: Mon, 25 Aug 2025 23:24:46 GMT  
		Size: 28.5 KB (28537 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250823-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f2e1ca1621aecb9d1bb59873c2053dabc15090514ec06057662d2b1d8fea67cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301839642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de2a8aed8797b868f8da8a4cc612c0cc6505975bdf87b09edc272ba3b660191`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 25 Aug 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Aug 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
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
	-	`sha256:9eee5969e4377d6381f91daec759a184ca62e8181048bb70f3b9df717a06ab4a`  
		Last Modified: Mon, 25 Aug 2025 21:23:21 GMT  
		Size: 79.1 MB (79118369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c333c8c7b6dd084f2edd5784d6a59d15592849f1fdc21559c3c07ec58dfad802`  
		Last Modified: Mon, 25 Aug 2025 21:25:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250823-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e0152759dfcd454b97103ca856f8a6183193901875bcded26aca2d6b9f5125db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10544532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a0980ffa1475969b1e65cbc216102778d06cb5fa94c45a46fe1958758f2b04`

```dockerfile
```

-	Layers:
	-	`sha256:28320d96dae751a489d98ae5c8631dbba5bb28768b8a635d70bb51e23a973d50`  
		Last Modified: Mon, 25 Aug 2025 23:24:56 GMT  
		Size: 10.5 MB (10515967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fc9531ce0b1a7d04c931d73e48837a1b0ea7fc7aa601d9466d7fbf6230e6f7c`  
		Last Modified: Mon, 25 Aug 2025 23:24:57 GMT  
		Size: 28.6 KB (28565 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250823-bookworm` - linux; 386

```console
$ docker pull golang@sha256:ff7dab141f76f06e9e790def4ba8e1f540888e1663bbed0c35652baa84fb7dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312135423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ae7503599c09588c05003aa01e3b29baf92ef7fab77062a3336c63c149dc9a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 25 Aug 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Aug 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
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
	-	`sha256:8d42e4509bc10c32a44078dfa72eb052d77fd115b17753c9b422d9c9b8193257`  
		Last Modified: Mon, 25 Aug 2025 21:00:06 GMT  
		Size: 89.8 MB (89808694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed00e4afa60c0f083e905e3cb9e3fb29568be047d47ced8ca60d1231e5101266`  
		Last Modified: Mon, 25 Aug 2025 21:00:07 GMT  
		Size: 81.8 MB (81761224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eb815a2f18afcb2d2aac7b77d243d71b6ebc811666a1450b5b2d920062195d`  
		Last Modified: Mon, 25 Aug 2025 20:59:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250823-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ae28afbf3d55478701bbe3f82a7e4e05da186fe393e7bbc9b023c9ef39ca51b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10496127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c22204e9d946c47843464b608c488360d459bf34c4a64b1bede2744d63b385`

```dockerfile
```

-	Layers:
	-	`sha256:6cc43bb2cae313d13721671d756d798e5c18fa33389d5ffba28e194ec960b3f4`  
		Last Modified: Mon, 25 Aug 2025 23:25:05 GMT  
		Size: 10.5 MB (10467731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3366f584afdd7f03ac0e02e59132176f15682b778351794fc28967f0956311b5`  
		Last Modified: Mon, 25 Aug 2025 23:25:06 GMT  
		Size: 28.4 KB (28396 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250823-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:a8a66de5cc61e93396b601e60e12b0dbe71e48c3b3f177bc07b37c0995dac9c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 MB (283503521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a042b071afddfd6f10b8052cbf73b4a8885328de7ba811b4b58cfcd35a346e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 25 Aug 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Aug 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
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
	-	`sha256:06540d0c74ebff0570e1821aeb0db2f1803c6997f1fc9638a9e7c25f0f2c1660`  
		Last Modified: Mon, 25 Aug 2025 22:19:05 GMT  
		Size: 77.8 MB (77830864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438043a26f5a3cb65ac9caed8163fc3a97242c566e8ae7c9bc46f239c50c14e`  
		Last Modified: Mon, 25 Aug 2025 22:18:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250823-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:56db07005873fdd2a120481e9ff61ea5f6565776373c2c41d830bb344eef4264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 KB (28283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc46a52fdc2dd6f781df362927070c0464c88ab39596e7ab84b6d1401d48e4f`

```dockerfile
```

-	Layers:
	-	`sha256:bdca1767b833532ea483a360125d524c4a30f9a44a757cfc5b859bef8ea167b8`  
		Last Modified: Mon, 25 Aug 2025 23:25:14 GMT  
		Size: 28.3 KB (28283 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250823-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:f0b364b2e0c0c76eb23347775e7c6e8cc645f1ed14fdcf269f9f378d2114b931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.7 MB (318707081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b25b4cac7560be85245bd6de61b2b29feb8d649bcf4fa9158ce8b3d2c04dc92`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 25 Aug 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Aug 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
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
	-	`sha256:2f497bb9c72f47bbbcc0dbb56c1882627096799f2972f4f6a666d6c33790ad02`  
		Last Modified: Mon, 25 Aug 2025 21:29:02 GMT  
		Size: 80.5 MB (80476849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f4e32b5c90e8b063b93d56c09e13166260b07b43423aa0bd81576c5590d81`  
		Last Modified: Mon, 25 Aug 2025 21:32:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250823-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:43dea425ccc67b58bf5f9b406653e235eb6fa368f411a8d50c8c569cf6a63ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10489089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8286b21bf4295a51997ea6c1b95769e37023281f36526db1c9e115f0ff9dd0b`

```dockerfile
```

-	Layers:
	-	`sha256:e21c854f5c35540bd311546633519914687e4773482845c3bb67582dbd031d27`  
		Last Modified: Mon, 25 Aug 2025 23:25:20 GMT  
		Size: 10.5 MB (10460614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f15125b5b78f1b053ca528bee7136e3aecd15fff17bd4f5adc44ccfaf313f56`  
		Last Modified: Mon, 25 Aug 2025 23:25:21 GMT  
		Size: 28.5 KB (28475 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250823-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:7316d384ede933ac43d074b8180a1c04db8c789bf536d6e0f03ea562afa0979d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285328331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49dd0173a012b8e6d5f9b606c0aacdd35f98746c746f03f82dcdf85493ceb8e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 25 Aug 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Aug 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
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
	-	`sha256:c4bb0635d2e248956f88a4462ee973445c0bd3979670795027980550063343c5`  
		Last Modified: Mon, 25 Aug 2025 21:46:03 GMT  
		Size: 81.7 MB (81685324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc8524f69bbc7f9ba047c538d1c580035eecbd714f487db781f1b4cff25bf24`  
		Last Modified: Mon, 25 Aug 2025 22:15:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250823-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:76d3cbb14ced567dda6a3594d906b1d164a0ab533ca991410e03c533d1626b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10348330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4855d75759dd4bda861adab52acfb5917363e41361111d195f86cd8fe65ad830`

```dockerfile
```

-	Layers:
	-	`sha256:e6d58c3c98d006d683a0af9803541aa8a55d743d3acdcd15a7c61d189ca44a44`  
		Last Modified: Mon, 25 Aug 2025 23:25:31 GMT  
		Size: 10.3 MB (10319901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caad620e286c74efee1be50217416ac0f3283fb353bda270706759dd19d10207`  
		Last Modified: Mon, 25 Aug 2025 23:25:32 GMT  
		Size: 28.4 KB (28429 bytes)  
		MIME: application/vnd.in-toto+json

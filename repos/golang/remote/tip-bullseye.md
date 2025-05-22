## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:369c58f4675233479e86ea198608fb7347ec16d304089027561e919f1f15a18d
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

### `golang:tip-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:dabd6c0c4009a614405105de174e9ad2b37f2201186b61d4ce3dd653b3791e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337908549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0669333d5a8d03bd34255abb8b528c4e7d35d3a810cf06405aac529b0d25be8c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Wed, 21 May 2025 23:20:29 GMT  
		Size: 15.8 MB (15764874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a69a02035012d2783a66ac7ecc549af09c1718d81affa5f9c39abcf969da971`  
		Last Modified: Wed, 21 May 2025 23:37:39 GMT  
		Size: 54.8 MB (54757308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d0ce73e418b68d83220613f18f86e98ad322d7ef5b6ea63f944c861dc1f582`  
		Last Modified: Thu, 22 May 2025 01:14:19 GMT  
		Size: 86.0 MB (86021885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3152514912bccc29796b149fde0366f2c5aabf882d40321f8719bdbe9b9c2cb5`  
		Last Modified: Mon, 19 May 2025 23:28:50 GMT  
		Size: 127.6 MB (127614129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ba156ac94734850c6309b755352698b359d9adec59e9f0c07e8456aecaaaf0`  
		Last Modified: Thu, 22 May 2025 01:14:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:c5a1b2b7924698ee497964601e71375d85b83293d399afc9d26552d8745d74f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10340879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba125264adb514c1580f6071e90f15caecd03f796d302700c3ba08cce95518be`

```dockerfile
```

-	Layers:
	-	`sha256:f5e0818dfb96711016d635a12820a86dad596912172a1185fd0e635171286719`  
		Last Modified: Thu, 22 May 2025 01:14:18 GMT  
		Size: 10.3 MB (10313818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97fd7a7ac5eaf240ca32731373f7c6337c474711f8b4ade4d08d272f100f1fd5`  
		Last Modified: Thu, 22 May 2025 01:14:18 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:2b30fbebb4111d80dd597d594f6878a4ad6c6e7f9b022bdbe9b030d63cd00178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301975039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29e24323ddf5a68ad884e4f67c2ed888064749600a9edc453de55be1cb2e0d9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:72fa46f1d669ee2de1ffbc36b654bfe8dd0aad49156f4143a5d9edd3a5c3d559`  
		Last Modified: Mon, 28 Apr 2025 21:16:06 GMT  
		Size: 49.0 MB (49040048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de64850f276e76efd1e91be51cb4b2577218e49bf52707b1bf6de3be76028cd8`  
		Last Modified: Tue, 29 Apr 2025 03:37:44 GMT  
		Size: 14.9 MB (14879026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4cecedb434598f97e33a3320b6af6e1676388e6c13b31f0aab4b7c9372012`  
		Last Modified: Tue, 29 Apr 2025 13:23:50 GMT  
		Size: 50.6 MB (50625161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dc7e83fbdf292bf0238a22da7ed8a7b954d4a791ff1772973394bf28d278ed`  
		Last Modified: Tue, 29 Apr 2025 17:00:23 GMT  
		Size: 64.9 MB (64922699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa57e96661f23b74a5007ca5b539e5d28d960192676ad8b6b38063081e7fce05`  
		Last Modified: Mon, 19 May 2025 23:31:19 GMT  
		Size: 122.5 MB (122507949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53021caa77e8d08a82b32675a78bd202238304d118ac9ec4988bf29897a34997`  
		Last Modified: Mon, 19 May 2025 23:34:44 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:1242197fb8961ab123cdfa9dbfe21d8f8d702495701d9b626d2c2776631037cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10146167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18aa9e461823e9e98ce63e17fab4c60653cf4efa7b9b7b19425d99d331baff9`

```dockerfile
```

-	Layers:
	-	`sha256:d4bb2f0dcb9766a8eeeb977c50cc83fcd44cdf8fa1ed26ba4f0af4e1bbc5a364`  
		Last Modified: Mon, 19 May 2025 23:34:44 GMT  
		Size: 10.1 MB (10118998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fe4fc15f9fa6327855648ec0b2fccc97028c4f0d20ab531d0b8a9cafccedc2`  
		Last Modified: Mon, 19 May 2025 23:34:44 GMT  
		Size: 27.2 KB (27169 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:a560a2adec2884b207d4ea2330d15d3adc9ab20e8becdd719e1f41b454ef6f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324525523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3cd2d3b1ee00ad23f32144c3c18fd10a3ac1501dcf9f27f1448f262773be95`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Tue, 29 Apr 2025 01:47:13 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b30b3b7ef57604d52a4f287f3a1202fa7094c2c34ba89e66f13f2ef75a47ae`  
		Last Modified: Tue, 29 Apr 2025 18:37:49 GMT  
		Size: 54.9 MB (54850001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8c6322f6933d3c7c501627d667e914654793c3d67e2daa5122b6519e08d8af`  
		Last Modified: Wed, 30 Apr 2025 02:35:23 GMT  
		Size: 81.4 MB (81414127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583af8027226f07cd540ce15387789410501e4b5b5d00ffa1a05fcb1dc81e7e9`  
		Last Modified: Mon, 19 May 2025 23:28:57 GMT  
		Size: 120.3 MB (120266151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd26f44229d4b8a1cb708cbc7e648b04279d22ba7ae00321e28d6e33058d7acb`  
		Last Modified: Mon, 19 May 2025 23:31:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:df4f1b14a68fc972abde34deef24a6dac6a4e488f47dc6b356b613b752625dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10342297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56b851dc28d0c8b0ebc40249082b44e38ba90db7a6d6996f15519e7a3b60343`

```dockerfile
```

-	Layers:
	-	`sha256:271e1bb9deeb8fa4aa293cdc2f5d9c4f454439c6d7390d74ce44e7440cbf383d`  
		Last Modified: Mon, 19 May 2025 23:31:13 GMT  
		Size: 10.3 MB (10315100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:617c4046253823c542f038acc456d211c388b5acab34828e6dd81cf273c3123a`  
		Last Modified: Mon, 19 May 2025 23:31:13 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:6d4567374708ffe2764668ba993f146a12e66709d0f0f1b2906d12b0effc486d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.1 MB (340149560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29129f95d699ee70ea2349c9ca133faa77cc717f155dd0d4bc0a1fb1f5b7530b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6c1a0525f904d970c0719d0ae307af1606eed8214108a47c9374eaffab5c71ae`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde5c2ebb13d7ca154f5cc8b4e26e7e3a669b8bac689ec15851b65e299a0fd6`  
		Last Modified: Wed, 21 May 2025 23:19:38 GMT  
		Size: 16.3 MB (16268487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e052669a7dd77fed659f1b6d3fcf5171929214e8821aaf28744160fb71f4f1`  
		Last Modified: Wed, 21 May 2025 23:37:26 GMT  
		Size: 56.0 MB (56049779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ad55923276be377afb8ed348ba98ddc03f09ca4576d59c12bde0f1a7e52f6d`  
		Last Modified: Thu, 22 May 2025 01:14:55 GMT  
		Size: 87.4 MB (87447914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24d8be6f5d36fbc3aec81708ca11efa4fc67dbd10e5ba59a5e7c3fa29e59478`  
		Last Modified: Mon, 19 May 2025 23:29:26 GMT  
		Size: 125.7 MB (125697440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5961f310382d04dac0e9383e5ddfa6fd9bb9cb6d3966ab4fb17adb112208bf0`  
		Last Modified: Thu, 22 May 2025 01:14:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:c2022e5d5886b57a08bef9c98e089f4df57601618bd366f1c7ae34281fe78089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48ff00b01bf960c87ce0898114c7b82524e3e5ce0dc0e54fe61bb225e59b04e`

```dockerfile
```

-	Layers:
	-	`sha256:484215e9a041f09e6ec3d894dfd2481e17e2a696c73d16d3c5a427fef9386da0`  
		Last Modified: Thu, 22 May 2025 01:14:53 GMT  
		Size: 10.3 MB (10303131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c9373f30068021494088c4150eb40a14695ce390d1c81fef57379a2c79dcbde`  
		Last Modified: Thu, 22 May 2025 01:14:52 GMT  
		Size: 27.0 KB (27027 bytes)  
		MIME: application/vnd.in-toto+json

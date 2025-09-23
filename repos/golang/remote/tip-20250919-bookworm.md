## `golang:tip-20250919-bookworm`

```console
$ docker pull golang@sha256:277cfa6102e229fc94071ef4a61c5bc60a9ff8605264ce39a3e4b2d1094db9d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `golang:tip-20250919-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:515b80bf623c8b68a4f14e7880e3a33589e91473b388a7ef2c21867fe2f88b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 MB (272889190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc893d56a91c1a0c36deba7e823672b4e1f052848baa085be3336e098d8c916b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
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
	-	`sha256:853462faf22c513f9312ba74d425f3dde3205d6bef10aef89077e0e6c545670b`  
		Last Modified: Mon, 22 Sep 2025 22:16:58 GMT  
		Size: 66.3 MB (66254317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b53903587a634418235ca9a2a24afbf265d09dc392f55b668e6b9d3c5f19d2`  
		Last Modified: Mon, 22 Sep 2025 22:17:28 GMT  
		Size: 80.9 MB (80854813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b427205274bdbccdcad0efccc264cd5d4a970867d7a21b51b2ae5989ee124c6d`  
		Last Modified: Mon, 22 Sep 2025 22:17:21 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250919-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:95297de0691a51b82845753725693c0409f5b56e943ed1eb34e2b38070276b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a0917400340bc8b4ead8f8ea3e2c2fb05b90782303e617c94620e54e6d53b7`

```dockerfile
```

-	Layers:
	-	`sha256:9b4e0868a15bcd1d25f27c8b2428f57995b2168a18e0f39f0e2c989ea4c88909`  
		Last Modified: Mon, 22 Sep 2025 23:24:34 GMT  
		Size: 10.3 MB (10301614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce1d80a43327ee09177fc79a269a242ea9996820770354acd81a5cb7a827775`  
		Last Modified: Mon, 22 Sep 2025 23:24:35 GMT  
		Size: 28.5 KB (28541 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250919-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d68f4d72428cb372af4859bde43f3aeb2ad5215aeb7524002d9a29d9b5596974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302564143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7b693ed244692b593cebc210676a1bd2990c16a0e2688437a91f34fc539770`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
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
	-	`sha256:2d42df5273ec61734ac6393c43b7e3093fe8c71d888e5e491814c782937992e9`  
		Last Modified: Mon, 22 Sep 2025 22:16:04 GMT  
		Size: 86.5 MB (86471721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3b299721a40c4d6ce1f1cb5eea411e8ebfdde21f8badd13b95f602420e920d`  
		Last Modified: Mon, 22 Sep 2025 22:16:02 GMT  
		Size: 79.8 MB (79767276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7b3883cf3699d703720d05752ce60b55a79cdb31272d55460ff3aad9a700ec`  
		Last Modified: Mon, 22 Sep 2025 22:15:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250919-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:59f85eb3319e37253546cf16b2d2636c584403d217167d1a048787f6e7f1d412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10551305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd72928e9896e9f66b038391d87f30c00a76ba0eca9edd466952d7b0b675b502`

```dockerfile
```

-	Layers:
	-	`sha256:df9141d21cef96e0975bf0f57cddb73064394137c416e6e4bb045e0820fe697a`  
		Last Modified: Mon, 22 Sep 2025 23:24:46 GMT  
		Size: 10.5 MB (10522740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f39a542adedbe2c1d0975e1c9ff51af6e74c7514b41ac78bc2b644dd214bcfc`  
		Last Modified: Mon, 22 Sep 2025 23:24:47 GMT  
		Size: 28.6 KB (28565 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250919-bookworm` - linux; 386

```console
$ docker pull golang@sha256:18cbc7ae2f7d9f6017ac054c33a56a9849ebc246011b1e3a58f3c2b189abcc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312857457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb280e87e0256b4a09c4e97ede139c4ee19a4a3b58b471bca24c6fba9f23074`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
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
	-	`sha256:17b0e23e2b814ef97970340baa616cfbe6ef37a95eeedfc94bedebd8b5b44c4f`  
		Last Modified: Mon, 22 Sep 2025 22:14:34 GMT  
		Size: 89.8 MB (89823455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3896767490999bcc9dd9f56984e3a495c1802d5f9283b126ed682e5e7c6e34ea`  
		Last Modified: Mon, 22 Sep 2025 22:14:34 GMT  
		Size: 82.5 MB (82473451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed75abbe364c720ad57f1a758a01b2d21f828b25de38ec435a01ab2414e224c9`  
		Last Modified: Mon, 22 Sep 2025 22:14:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250919-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:69bb6d425e5dbeb401bbf496bdd5205379c2731ab715d4c4c2d313d3a1665e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10502895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d109ca1abdb4394711b1735a5cc1391580962e47e713975c289d30f91acc20b`

```dockerfile
```

-	Layers:
	-	`sha256:58bd5e5597270dadc07120fd829ed75a49987d987e232a0a358204472901e40e`  
		Last Modified: Mon, 22 Sep 2025 23:24:56 GMT  
		Size: 10.5 MB (10474499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51ce673c2985a9955c54e4794b35d6e1e0adf4f2f14f9fd697d5312ebbe8e6e`  
		Last Modified: Mon, 22 Sep 2025 23:24:57 GMT  
		Size: 28.4 KB (28396 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250919-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:f37178a4bc2dfbba96ed6b22ca338fd51aa9d5f2bfaa9dafc81cdb3543b2ae44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284349191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2bbe96269262d9b92ebccf3a8b6734e0cad2945f478d874f65584bea2fb0d5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
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
	-	`sha256:4de4e3e28725018dbaaa156ab7ded1b01b9349de10f14893745191d31d2566ac`  
		Last Modified: Mon, 22 Sep 2025 22:31:16 GMT  
		Size: 78.7 MB (78687631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecd2d8e076a3499377eabca7eddd178e5a522cf4612cefea6a5223740bb8c5d`  
		Last Modified: Mon, 22 Sep 2025 22:31:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250919-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:92d01368d9df2fd82e685a16c235c8da11040290d4cd0294ae3d06c46d5f72b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 KB (27167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc9c68fc0868d04149698dcca11e8002ec916b0c4d3ebd52144e471f53d0169`

```dockerfile
```

-	Layers:
	-	`sha256:48f70d689ca99c1f0b48f56b963cd1d6f6db3ea3c4dc645df6dbcdb50e34adad`  
		Last Modified: Mon, 22 Sep 2025 23:25:04 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250919-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:85b9543c0babd031895e7acae5cae939133770cf617a7fd40f74f2a73e7e818d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.4 MB (319400203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d79dff3c2de6ae2ca2abc4d2fc28b360e10ac69122b463020b0c4beb493283`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
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
	-	`sha256:89d108a2cd33a563c43774575918efeee76a04312bcb280885b5be517d0a8962`  
		Last Modified: Mon, 15 Sep 2025 21:19:47 GMT  
		Size: 90.4 MB (90402577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cde134c38211f8221348f6d1f1e1ad94732dd62caecb5c0a2623dc2674afdd`  
		Last Modified: Mon, 22 Sep 2025 22:19:09 GMT  
		Size: 81.2 MB (81155866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499b2aa537856326c5ff8e5b9556a7e75f758e19a277036e7c9a8d04827328d2`  
		Last Modified: Mon, 22 Sep 2025 23:11:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250919-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:48599b42caf41971b88da648c6493de5afbf1dcc385f98ff07967c6ad72db0a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10495872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ab1cd011973aa1283208b57b409bdbbda738f613598e44c0a59153f05eddca`

```dockerfile
```

-	Layers:
	-	`sha256:ed4605ec1d13094d54273ff379a32b831164d91ba1567fc6f85b3e8f9f332480`  
		Last Modified: Mon, 22 Sep 2025 23:25:08 GMT  
		Size: 10.5 MB (10467397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:520d56a5f2df80b4d11b3620b317e03e5259f42a4c04dd30e89c2b0009551037`  
		Last Modified: Mon, 22 Sep 2025 23:25:09 GMT  
		Size: 28.5 KB (28475 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250919-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:e8c97ddf459bb84576d42acae9ce52eb8e3972b7366842763a57bf3fad3922b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286031697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76cc89cbe3be59290330b882b199b6ece55e438552812b6a3f46a2c4bab4476a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
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
	-	`sha256:57f98ca119e81becfa4215c8c39f78dabe31b2392456cc31059e7ae845d41125`  
		Last Modified: Mon, 15 Sep 2025 21:26:07 GMT  
		Size: 69.0 MB (68990087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378803bc6cc1e0c01f411ee825bdc456b59e4a7d5184c546614a84a4ce15dd67`  
		Last Modified: Mon, 22 Sep 2025 22:15:10 GMT  
		Size: 82.4 MB (82378206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3a64c0a6ae4011ee285c91eeaea0b47f0a7d3be409fb3143da4b484767ab99`  
		Last Modified: Mon, 22 Sep 2025 22:18:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250919-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e5899193e3ff76b3d64c35335c1e9abf8dc9b13529f0717e410874eb7b875224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10355103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e22367e11ef663fe0cc93d9b32afa4001ebe669024ef4505109be74fe653650`

```dockerfile
```

-	Layers:
	-	`sha256:96fe888ac11b450eab1e49ef8bf042793fbce7fff154c321093c693572ad58a4`  
		Last Modified: Mon, 22 Sep 2025 23:25:18 GMT  
		Size: 10.3 MB (10326674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47129f3acbdcbdbcfbf66981cc2dc9dadf8499b5dd2d34bc42f692e99e482c01`  
		Last Modified: Mon, 22 Sep 2025 23:25:19 GMT  
		Size: 28.4 KB (28429 bytes)  
		MIME: application/vnd.in-toto+json

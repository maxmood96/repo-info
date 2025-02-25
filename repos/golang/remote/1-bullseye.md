## `golang:1-bullseye`

```console
$ docker pull golang@sha256:1f65e1176d093a62216bf1147a4a750bf81ced7c5e05c204e55f1f4fed2f5eea
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

### `golang:1-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:705390e58d888ec803656145049d6b671ece7242e436dd58fe1b39b998a09135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288829120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c70b06cbb7fac971543fd829e7463cb9f7687a3dcf53792a024fe8b116393c9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bcbc2151ce4be9aa40b26468719dafd6528d7d11d6f6cb60e3a58a3447305`  
		Last Modified: Tue, 25 Feb 2025 02:12:52 GMT  
		Size: 15.6 MB (15558424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36295709cc3855d0f98f8a6b939053cc43efcf3092756703c1fc518d73fe77`  
		Last Modified: Tue, 25 Feb 2025 03:13:48 GMT  
		Size: 54.8 MB (54752085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a42579592c327b092b56fb96fd38798fd3b7be90d94c0473dc2b3d8d3b54f25`  
		Last Modified: Tue, 25 Feb 2025 04:17:46 GMT  
		Size: 86.0 MB (85971567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a60326dddc23e8774b39171d6496c16678bd44e52909e9a94763d62f3cbf89`  
		Last Modified: Wed, 12 Feb 2025 10:27:40 GMT  
		Size: 78.8 MB (78805485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab6d738e883a57a47b3430f2fe4b0288309b1542ca9f3e00bbdb2e3751cac9b`  
		Last Modified: Tue, 25 Feb 2025 04:17:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:474d69931d19096b06c3b06288b6982fe4dd0fd0f936f1dc07ba60b1b1637505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10298228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350aede5ba61effa918a3115011b2d3867a4749668d2631c64241912db7abdab`

```dockerfile
```

-	Layers:
	-	`sha256:e9397dbd1faa72c180f083556b33849b35b4c9b237c061b4dd5c23f0a6746c20`  
		Last Modified: Tue, 25 Feb 2025 04:17:45 GMT  
		Size: 10.3 MB (10271760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01744ae7c7dc22d99a866329c116f3ff6ba8cf967fca59e820f0c5dd68ba3057`  
		Last Modified: Tue, 25 Feb 2025 04:17:44 GMT  
		Size: 26.5 KB (26468 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:f104c6b9406d1a9a992e20418c5dee9664a3e7f7f8ca3d36cff016436beb15e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256199781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f6ddf02ca6866fc9cbc6777e2bf396f347831be35125bdb2d32c1e27971829`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7dafa8b67e9b20318af5959237616a556f517d3359b4cec5bc2b6899a7c8336b`  
		Last Modified: Tue, 04 Feb 2025 01:37:44 GMT  
		Size: 49.0 MB (49024794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfe1cf520a5741b594ed015a44e9386892026b5310b613c2207dbb1073919e7`  
		Last Modified: Tue, 04 Feb 2025 10:42:22 GMT  
		Size: 14.7 MB (14673818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed7c48b43b3adcfcfb794cc307d61fbdfd95ebf9cf80b1a014e90a497356d90`  
		Last Modified: Tue, 04 Feb 2025 16:21:50 GMT  
		Size: 50.6 MB (50640069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939d641c4fb5f7d6edca115cf3c6db8bc11e32ec83c49422dab7839f4914e1a2`  
		Last Modified: Wed, 05 Feb 2025 00:36:13 GMT  
		Size: 64.9 MB (64892491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ff7ce8adbb73c193102166498a2962195641bfa6bbc14e5dfa44f02e4d7d0f`  
		Last Modified: Wed, 12 Feb 2025 17:45:53 GMT  
		Size: 77.0 MB (76968450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd24fa4f3f91ba9a82542866d5b47b49e4c06a8a39ea189a296e687fb2d5206f`  
		Last Modified: Wed, 12 Feb 2025 17:46:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:dab90df725fb11504eac910a0c7ccbd5b782890161f7fd60e97df0ef318445ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10104690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b332e058a34f4abc3ab663216ccea1ec62e45b70d53dada51d5b425dbc0806b`

```dockerfile
```

-	Layers:
	-	`sha256:92b583d0df52aa3c51d13a22c3173feded4f3abfeeb9b6cf47289d2f2edaee32`  
		Last Modified: Wed, 12 Feb 2025 17:46:53 GMT  
		Size: 10.1 MB (10078120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4f18009e887412f5fcbb2c89cc19266c5e983c2355c8389657f4123ff4ecb7f`  
		Last Modified: Wed, 12 Feb 2025 17:46:52 GMT  
		Size: 26.6 KB (26570 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:a692552f6607c29c8bfaccc327b4d11d0ec0efcc4147c5f4f3692515e0a55fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.1 MB (279085052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa8b8b96151eb33ea94b1029eac5d4ff89dd39771f582494facf81610674ea8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c7afb1aa0f9672a06c4c7eaa6b7c7e111a91a8d45272dce1e361ac0b0ed79a`  
		Last Modified: Tue, 04 Feb 2025 09:00:33 GMT  
		Size: 15.5 MB (15544055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e2f45c7ddf8cc116eeb2ac1ef8be70e3639a883c6d9e5eaf1f2dd702dbf92`  
		Last Modified: Tue, 04 Feb 2025 19:02:31 GMT  
		Size: 54.9 MB (54852696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645f8f0990a7270606266e36ae54950c498997c10e31242c830d3106f5fd7ed4`  
		Last Modified: Wed, 05 Feb 2025 02:02:38 GMT  
		Size: 81.4 MB (81382226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18364ce0d2587c74fc30d8602f743c52178d9e6408c64d9091baffbff467af7`  
		Last Modified: Wed, 12 Feb 2025 09:53:13 GMT  
		Size: 75.1 MB (75060222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e03cd62280c6dfb169bc07d29507c76d88cffa0e95c43f23928425e0aa97d79`  
		Last Modified: Wed, 12 Feb 2025 17:43:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:8a2dbcc93d143ae1a2f718121a7f33d333011a0b4d460f61c4ee95fc41373c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10299958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368c4ef9110e3ce30d400ec8c78a0371dd2957130bae7d754aaaa6f7ecb29ddd`

```dockerfile
```

-	Layers:
	-	`sha256:1fe63bf355ff11350394da5c7b2bc785272b96d7aca28a06db023719eaaa648b`  
		Last Modified: Wed, 12 Feb 2025 17:43:37 GMT  
		Size: 10.3 MB (10273356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60efb9615aa7c8b7822adbdd208c5af6101ebdb1c359bd6ffca302027213f21`  
		Last Modified: Wed, 12 Feb 2025 17:43:37 GMT  
		Size: 26.6 KB (26602 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; 386

```console
$ docker pull golang@sha256:1bd195df8df787fe73331d0739d45d567c124ae93ed3bb0f988b749568751bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290899229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755a5beb21c552b7ccfcfa9043ed7e3d4802c14d798ed2a1cd7da6b2d96c8eb4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1763bdfcd7e692c8f35c71602a5206ff9e4716856edf6ae712febb4cc579d3`  
		Last Modified: Tue, 25 Feb 2025 02:24:11 GMT  
		Size: 16.1 MB (16062177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820de11811e966e41fc39b6790cf28a33ce0645127033d9f041fa3707235430e`  
		Last Modified: Tue, 25 Feb 2025 03:13:43 GMT  
		Size: 56.0 MB (56030023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b285199cadaf71624a008570db11f3fd44b62c1453f2926119cbc84f7c1c0`  
		Last Modified: Tue, 25 Feb 2025 05:12:13 GMT  
		Size: 87.4 MB (87397930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366fc1b7517b38e35749547747afd275840849b03e59ce7bdb829acdcf634998`  
		Last Modified: Wed, 12 Feb 2025 17:30:21 GMT  
		Size: 76.7 MB (76730079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39588322a7f2570c915376b53d344bc9238a7a42a34796cb38781fc63c2654d2`  
		Last Modified: Tue, 25 Feb 2025 05:12:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:5138f78cd6c21ebcd61ce53cf06c27fb4a9d28542e54c48b80374ad5e066337f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10287977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9e42766156afc1df98e184e7b83946e56772f0cae90e58da8247f31ffc583d`

```dockerfile
```

-	Layers:
	-	`sha256:dca1435a8730590e2cedd035cd24102edc9cdd6f480efddc4e49de547bfea170`  
		Last Modified: Tue, 25 Feb 2025 05:12:11 GMT  
		Size: 10.3 MB (10261545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c5e052778c366d1d1e7a2b3feba61242fb2906db13d3d909aade37f6d0e11f`  
		Last Modified: Tue, 25 Feb 2025 05:12:11 GMT  
		Size: 26.4 KB (26432 bytes)  
		MIME: application/vnd.in-toto+json

## `golang:tip-20260626-bookworm`

```console
$ docker pull golang@sha256:9fa340fdf90257ed54057eb4098dbb77b482e9a5e7309be21f65fbc8276fe823
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

### `golang:tip-20260626-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:e8c01b000f16b9fa75d050b00f30f421568630e41cc1b4f7df1da8bd87256d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.0 MB (332040200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0982bda8bb9a3ac77f48ad7b473b39c40025c6549a16ce5676b275734d28bcf0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:41:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 00:03:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 00:05:05 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:05:05 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:05:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:05:05 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:05:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:05:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd7bf6f6036613e20f62549df75ed694b99118002358bea5a81baf3929d1ff`  
		Last Modified: Wed, 24 Jun 2026 01:41:33 GMT  
		Size: 24.0 MB (24044046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791c68bc2063683c3d15907b8ed1b777cf14ca153c6f8e5b12db0868dfa7e38a`  
		Last Modified: Wed, 24 Jun 2026 02:28:33 GMT  
		Size: 64.4 MB (64404017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844dcda27815e14e3dd306d3fed597541d7315cff3b47a56a6cc7fabee195110`  
		Last Modified: Tue, 30 Jun 2026 00:05:34 GMT  
		Size: 92.5 MB (92481844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96112613ca74dcaf72b29b75f1686921a6f92c1d50000e911abd31cedae3173d`  
		Last Modified: Tue, 30 Jun 2026 00:04:41 GMT  
		Size: 102.6 MB (102607925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cd229b506506e480732f0dd29463afd2e807149958923cebffc23627f98349`  
		Last Modified: Tue, 30 Jun 2026 00:05:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260626-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:fdfc27f701614876203134fbb814f9e55407ceb2f7ac7bf88cc35443d378f87c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c8a0d9def057d934180111d71c6c671915191b36b95025ca666eb2c7c69763`

```dockerfile
```

-	Layers:
	-	`sha256:c6df4fef62ba3e084802e2d351e3a1fe9fb57e183e60ada8802057b8c3295d50`  
		Last Modified: Tue, 30 Jun 2026 00:05:32 GMT  
		Size: 10.5 MB (10497073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744d17d09fe196c10a7ed7b73e3515db8bb44a75d9b26f00dbd4ade78bb63f81`  
		Last Modified: Tue, 30 Jun 2026 00:05:32 GMT  
		Size: 28.4 KB (28390 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260626-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:07a066e685fac7c682aca2d8d4cf0ec0c775038c749bd7d77f6752bb882c5bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290473874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a448976b80d25daa976dbe996ea34e4a0f9a21c4fc9dff76e7273e1c782d6b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:22:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:54:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 00:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 00:05:47 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:05:47 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:05:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:05:47 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:05:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:05:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3622debffba3838b917703fb6dd9c161a4d93d9fd97c61d3e8400a2245f93c67`  
		Last Modified: Wed, 24 Jun 2026 00:27:30 GMT  
		Size: 44.2 MB (44208145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0df8de55f365d832099cabf27409104999d59b26292d91202ca6e160c4b513`  
		Last Modified: Wed, 24 Jun 2026 02:22:52 GMT  
		Size: 21.9 MB (21949935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16c85bf5ff1b42ae66f83fdb64a6cd05a854ea2289dfe1b0ae9e4ee6a806d0a`  
		Last Modified: Wed, 24 Jun 2026 03:54:41 GMT  
		Size: 59.7 MB (59661949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c412b3026eb5ed5326d37e4ce28233451354482dee5f3fa4cf4bdeefb1ed444e`  
		Last Modified: Tue, 30 Jun 2026 00:06:17 GMT  
		Size: 66.3 MB (66339325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea34c6465040d9a03784c749dc96fc02b642a3007f305eb3e72609624011a8c`  
		Last Modified: Tue, 30 Jun 2026 00:06:17 GMT  
		Size: 98.3 MB (98314363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8d317bb63ed6d01fa732ed244030d2a50688f02a213e85fd0722c5838366c`  
		Last Modified: Tue, 30 Jun 2026 00:06:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260626-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8ed37914bfc84e251cb5fcc94c594342c5bedc8fc406d79072f5b231b0388fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c164039061903092a2257660df4812e319144cb5a9ad72420cded8d70ac63a`

```dockerfile
```

-	Layers:
	-	`sha256:3190f3c331e2ee6c927f46db5ab1d1a0ca50e7bd441e33ce2c529b80e4ae3651`  
		Last Modified: Tue, 30 Jun 2026 00:06:14 GMT  
		Size: 10.3 MB (10303769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2595ecc8180e7f61a2ec411034f5d8a52f5841315845555f0eaca227a81aee64`  
		Last Modified: Tue, 30 Jun 2026 00:06:13 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260626-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:42358ac8ad6fcde63925c0017bbc864b5d99befe867f199688711da924715416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (320030797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce57b9133739bc62b41c19e300ab7598d26650bfaa747578014203e70b2f940f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:44:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 00:02:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 00:04:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:04:15 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:04:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:04:15 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:04:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:04:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ebca214f1a4b66acfdb0bd20aa3ee139d1747885ef4b0f3d07aa2a68459230`  
		Last Modified: Wed, 24 Jun 2026 01:44:48 GMT  
		Size: 23.6 MB (23613316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533bb0e918720911be6cb7a1a5ba9ad0e1a308fcbf24961a23aba0cd220df6cf`  
		Last Modified: Wed, 24 Jun 2026 02:35:28 GMT  
		Size: 64.5 MB (64487706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a370b0060c4dd8c0fd31022de7135bd81f6932df3fce7b33cb142cec44ff15`  
		Last Modified: Tue, 30 Jun 2026 00:04:44 GMT  
		Size: 86.6 MB (86554483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc19bf506b072ad4aafc8fd4d3064dd82a2aad3673c0290669bfd12b0d5429a8`  
		Last Modified: Tue, 30 Jun 2026 00:03:59 GMT  
		Size: 97.0 MB (96985935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f1c3bd8fe5795f6f98d119f7e16d9823f23025ed53137dc2f34f431dc47909`  
		Last Modified: Tue, 30 Jun 2026 00:04:41 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260626-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5357a2d753906beb8e36106f73b3811628eecf7d29c9b4d9ee43edecaf669d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8c7c7678c450c4f5367def4af1ce09d12445c5d2e070e80586db1e48583e25`

```dockerfile
```

-	Layers:
	-	`sha256:1ac5ad21e47b9831d976a40f4a1a62a97f9419c5dc2bd83c0a939c15c6f899e4`  
		Last Modified: Tue, 30 Jun 2026 00:04:41 GMT  
		Size: 10.5 MB (10524897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4b784c9703dd7dffabace29d544a7f484000b06684bf19ece150f605a399a18`  
		Last Modified: Tue, 30 Jun 2026 00:04:41 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260626-bookworm` - linux; 386

```console
$ docker pull golang@sha256:da85ebd50cf7341d30c07959b640e1922791812fe3c62e052369473bc4086760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330913090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f744c2d61557d4ac28fc8ae6aa597f9cad1ff191e651ce8f65c0fb02d5dfaa6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:43:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:34:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 00:02:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 00:04:47 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:04:47 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:04:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:04:47 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:04:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:04:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:96cbacad9c1883b9ae87f68a0550ac0bd7e0b7ba2b15b142a793b89b5a5f36ad`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 49.5 MB (49491378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b45c9ce5ae5ea6ab37787312be8b0a9732642c1221f97d5689baacac874b4cd`  
		Last Modified: Wed, 24 Jun 2026 01:43:48 GMT  
		Size: 24.9 MB (24879740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db0110899c29fd647e62f912bfb740fc8af5310cdc227454d8f086f16cba33e`  
		Last Modified: Wed, 24 Jun 2026 02:35:05 GMT  
		Size: 66.2 MB (66244204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2662ea5985807e4495e170f8844f3104b85ef94d7754ff14bbc705fab07e983b`  
		Last Modified: Tue, 30 Jun 2026 00:05:14 GMT  
		Size: 89.9 MB (89903918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfe287f4fcc073ba1e90b598305ae90f45e8a3339ed6d99366e8996528c1a25`  
		Last Modified: Tue, 30 Jun 2026 00:04:49 GMT  
		Size: 100.4 MB (100393692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ab897151f9f456f60ea9f0424cec2304e8c412cd2067940350489d515500a9`  
		Last Modified: Tue, 30 Jun 2026 00:05:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260626-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:48fd1c072de40840402373fb63db5b485a8d5f4f7287f3d88eed1de04e10830f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10505010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9ee79a84bdfd1ae0a4566433b5cd8da52036f349cad82e8a0d82a3a6d69812`

```dockerfile
```

-	Layers:
	-	`sha256:93403384d49c45c8348e537644106df984e77853ad6e804dcc1f0bb7344267f3`  
		Last Modified: Tue, 30 Jun 2026 00:05:12 GMT  
		Size: 10.5 MB (10476653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:902755bfc18ac2a89dd1046da5ee00d6cf7338566a2d98a50b73333f22365e4e`  
		Last Modified: Tue, 30 Jun 2026 00:05:12 GMT  
		Size: 28.4 KB (28357 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260626-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:a12bcc8505d9065e9d0a0b21b6a7ccbcdb13e988b7ab7e8d8a172b3fe58a7883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301764162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60152f36ea7df9b327ac0312451021db6f4345c57a18948570626c3719b0e6f2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 14:04:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 19:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 20:18:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 00:29:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:29:22 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:29:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:29:22 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:29:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:29:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d06e8744a62761c63cdcacfb2a61022e2f4c0aa854b6cede18fced28342dc1b2`  
		Last Modified: Wed, 24 Jun 2026 00:26:53 GMT  
		Size: 48.8 MB (48792819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a2f466b887b6a2a52424171128948207dccef13979fc60f50cb7beb67f123f`  
		Last Modified: Wed, 24 Jun 2026 14:05:16 GMT  
		Size: 23.6 MB (23623971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911f76b03057793439aa57a4c1f92b3f5d8467508369f84d1b616a44d437f66f`  
		Last Modified: Wed, 24 Jun 2026 19:28:16 GMT  
		Size: 63.3 MB (63315803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654b25dab3b07b2704810e9680f6eed67322c4a7200f8be9169d2bc4b30b592c`  
		Last Modified: Wed, 24 Jun 2026 20:21:00 GMT  
		Size: 70.1 MB (70084425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b77e00ba245327cc756abb2cd21e13969e6a7643574050f352d37c5008ccb6`  
		Last Modified: Tue, 30 Jun 2026 00:31:43 GMT  
		Size: 95.9 MB (95946986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5cde859635224cbcd0e76a11c0f9fae8316e096af2d7d1979dfb5c09173a35`  
		Last Modified: Tue, 30 Jun 2026 00:31:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260626-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:9beec23233149a1f44015ffa48a8f6188dd063a901b2097d4014626d16dc80bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76729cb64ba9c5c6c675e2bfff3d55c8744ab3f726804537e6fbf8c9a432cdad`

```dockerfile
```

-	Layers:
	-	`sha256:1be3b548fa5aea962a959ebe0a6dc92df87e587c785060e651b0c752692cb151`  
		Last Modified: Tue, 30 Jun 2026 00:31:33 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260626-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:568dc569578a3fad743958cfc8430efc23ff01c559542ff17671024464de6ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.4 MB (337353012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d1fd9fb4d75f015ce4037957a40c2622593ab16d7a3a4f2b3590a89172fe03`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 09:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 11:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 00:04:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:04:54 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:04:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:04:54 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:05:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:05:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:55b0e891f4e8dc14bf4bc7e853254fcf1f3ba5a8e8e3c07c21e7dd5bd6d87882`  
		Last Modified: Wed, 24 Jun 2026 00:27:34 GMT  
		Size: 52.3 MB (52346847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a217268ac6656bd05839d5770fe7b3c0c976d29750b0c5635d099e473a789a10`  
		Last Modified: Wed, 24 Jun 2026 03:25:44 GMT  
		Size: 25.7 MB (25687048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6542f967f29885e49bf508e83dceee1eda4fdb044dcd68c1237588f15b795e2b`  
		Last Modified: Wed, 24 Jun 2026 09:10:08 GMT  
		Size: 69.9 MB (69853519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9034cb40d1ddee03957e235882d85c3935748284d5ce7d9e3b1fb946a360d593`  
		Last Modified: Wed, 24 Jun 2026 11:45:03 GMT  
		Size: 90.5 MB (90495696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ea8767a8a0a93030114399f1f19e8f448718e14ab3c948bcc8dac1be9cf2f8`  
		Last Modified: Tue, 30 Jun 2026 00:06:26 GMT  
		Size: 99.0 MB (98969745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de5bc52c85d076e1635325340f506ed4b8ae59b7a789d97dee9715bb875b20c`  
		Last Modified: Tue, 30 Jun 2026 00:06:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260626-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e9533ebad23fe1e3093018be1256ce2a9d857659c2c45b47b14d80868c68506a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d365193e9571d0d9b29e1b574f17d02c95356dce1c9658e101c20ebe3995cf`

```dockerfile
```

-	Layers:
	-	`sha256:6636a44deb02920eb46fd341933574453a862d3467d50195364768d6ded43ce4`  
		Last Modified: Tue, 30 Jun 2026 00:06:23 GMT  
		Size: 10.5 MB (10469558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:468b8ae0113b5c41483549533a2c4d799ab12db5e5d585f76b8aded679f1c01f`  
		Last Modified: Tue, 30 Jun 2026 00:06:23 GMT  
		Size: 28.3 KB (28258 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260626-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:dce79c51072726a6b9fa6c377cb9793030b32e48bb571752e2b9a7eea8281b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304830917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1bc25fc56f0d06481580e1f33fc2681d6d65ed5b71250975c9d42ed7341316`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:45:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 00:04:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 00:04:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:04:42 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:04:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:04:42 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:04:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:04:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bdd2e9d83d68023204331dd445067114dbd3500d2d496368624fa7ef81743d4a`  
		Last Modified: Wed, 24 Jun 2026 00:27:09 GMT  
		Size: 47.2 MB (47161675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075239c7f31ef6bc9923503289fbabd4a216a0cc1314ab546cdb22b3aa178273`  
		Last Modified: Wed, 24 Jun 2026 02:46:07 GMT  
		Size: 24.0 MB (24038997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98bfd0e5e3c41d5610549c351f2a214a1057c70f21ae763c153398d8481275e`  
		Last Modified: Wed, 24 Jun 2026 04:29:51 GMT  
		Size: 63.5 MB (63498267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f479bd9436c8612b91c321c7cd06b62747bf0557be0ef448a25fa40836c962`  
		Last Modified: Tue, 30 Jun 2026 00:05:27 GMT  
		Size: 69.1 MB (69087680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdf657db5fc71df443dbbc81704a25107962ecb9a4a8f16c3715658947e80b9`  
		Last Modified: Tue, 30 Jun 2026 00:05:12 GMT  
		Size: 101.0 MB (101044140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c13ee47b55240ecb6108855ca6ed14271a056f35f7acfdaa8d567305d043b79`  
		Last Modified: Tue, 30 Jun 2026 00:05:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260626-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b3ff0e3d046ccba5392cc1181b378a60bd238f015b1fbc2b1f68e8b305e0a63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de404981d4d24b390882078f378c47f60eaf1b248f2e10883034ad0ec41caf59`

```dockerfile
```

-	Layers:
	-	`sha256:5ddf43c91430bda4d5802e894b6957788f435d901d5f1c4a8e21e3da63f17f4b`  
		Last Modified: Tue, 30 Jun 2026 00:05:25 GMT  
		Size: 10.3 MB (10329579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf27017028ad56f1988a4e7a681c0548709364bb481896c7efb25d75353e3968`  
		Last Modified: Tue, 30 Jun 2026 00:05:25 GMT  
		Size: 28.4 KB (28390 bytes)  
		MIME: application/vnd.in-toto+json

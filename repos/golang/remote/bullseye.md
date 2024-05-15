## `golang:bullseye`

```console
$ docker pull golang@sha256:78b171fe51f25b8c3197710f281dacae94759a254e9a486576005f9dadba9e7d
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

### `golang:bullseye` - linux; amd64

```console
$ docker pull golang@sha256:af977b340fde3237836d4ce21ebdb9164c681a9bed74ae07c29c16247bb31f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280723025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc950eec2dbd891006be5c8f8dbc4dd1f0a05a37a18dfe224018313821987b3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 May 2024 16:32:49 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 07 May 2024 16:32:49 GMT
CMD ["bash"]
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b037c2b46ab4e54a261a0ca65b12b93e00ca052e72765c9cc4caf1262a2b86c`  
		Last Modified: Tue, 14 May 2024 03:05:30 GMT  
		Size: 54.6 MB (54589605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9a38a665687defe9b9094f70d5518fdfb5aa775fe284087343a9d3089ab672`  
		Last Modified: Tue, 14 May 2024 22:58:58 GMT  
		Size: 85.9 MB (85926301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2803732098de4a81fcaccbd29b7b3515e158831607b36ebc68de2a7442ad067c`  
		Last Modified: Tue, 14 May 2024 22:58:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760c6cbe8f6eeb7ed10691de63790102d74dc5908b85ce0decd4910dfe8d1b5a`  
		Last Modified: Tue, 14 May 2024 22:58:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:a49c5886fc76611c8bdd3405b2780c5ee7880bd06364b6b3d9487659b88fa4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10237300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b454910fa6440c871f7afc5f96622514443cfb00ffdfbc79593f05c1f3919c6a`

```dockerfile
```

-	Layers:
	-	`sha256:85ef02a2a12b2281ae574869cd0fe5575e94322ec1b7c0c576c09e2a779ddf87`  
		Last Modified: Tue, 14 May 2024 22:58:55 GMT  
		Size: 10.2 MB (10212391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c1a0b2b739e159e623f97e04543287e4c717928df1708ae6ab30a972171a7ba`  
		Last Modified: Tue, 14 May 2024 22:58:54 GMT  
		Size: 24.9 KB (24909 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:b61156e2197553fdc9cc45ab5f6de9fdd982a008eda1617b49024911df848d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248054307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e820114ae55728cff9041aa65db33dd91bb142b5b966ca2d123180734091990b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 May 2024 16:32:49 GMT
ADD file:e0e66bc918a84b9ec6caaae1380270276be179a5864b6234a18c001b3e94f855 in / 
# Tue, 07 May 2024 16:32:49 GMT
CMD ["bash"]
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ebc97a184476667a6a83dfc0759e34e05bc66d258ece39a010b6273982b4dc57`  
		Last Modified: Tue, 14 May 2024 01:13:05 GMT  
		Size: 50.3 MB (50256445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f46483bc34de5be97fb9e8af88e9cf41c36db4eecccc529cc7904ee92a32f72`  
		Last Modified: Tue, 14 May 2024 01:48:02 GMT  
		Size: 14.9 MB (14880295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d6f4b9983a8ee98e2432d49e727c6278cadb8efecf5ab79268999b8d08c984`  
		Last Modified: Tue, 14 May 2024 01:48:20 GMT  
		Size: 50.4 MB (50359447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3cea1fa2efbb359a15b4c5c118221035974971de6c6ba65c090f6b68ad68cf`  
		Last Modified: Wed, 15 May 2024 08:38:09 GMT  
		Size: 64.8 MB (64842749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd578652b0fd72238bc2565adcc2bf2716995c086d72609492506b36ddec660`  
		Last Modified: Wed, 15 May 2024 08:36:50 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f55a84facd68d5a684a4cb8c1e2a59fdce9c92702fbe2bc2eb824d89a3f77fb`  
		Last Modified: Wed, 15 May 2024 08:38:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:c4df93d469171da8e8ba8ca77f161e9ae0ea88d28962d586f8be50067a18cf36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10044519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82aee2f3fc359802c7b979121aecd8af31c3d47a41a45991660936b416c40686`

```dockerfile
```

-	Layers:
	-	`sha256:8e941f00ce8a60d7b3bb4cd7353a5d68e213edede565bd0f27e9d38b3c765dc5`  
		Last Modified: Wed, 15 May 2024 08:38:08 GMT  
		Size: 10.0 MB (10019515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f240822d31caa02b1c2d70de9b9456fef82e0e76e93475419f0021f1cb93f35`  
		Last Modified: Wed, 15 May 2024 08:38:07 GMT  
		Size: 25.0 KB (25004 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d64269a55ff38c4ba6519ac568d2d3caf38a11a5cef691b33506e19c6cdc2839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271794120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee362586133df9dca1a7beeade8824a0bec060ca877968dc687765e054d6f52`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 May 2024 16:32:49 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 07 May 2024 16:32:49 GMT
CMD ["bash"]
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691cb555e773cb93573d3bc043d7cf17af1d4819163089dfddab3f4cc971718e`  
		Last Modified: Tue, 14 May 2024 01:53:53 GMT  
		Size: 15.8 MB (15750525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dce352085291a4828eefe3a8fe5557c610cb7e308cbe4a56a62e0922171dc1c`  
		Last Modified: Tue, 14 May 2024 01:54:08 GMT  
		Size: 54.7 MB (54696093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388cf2a5682d0b9f615e4a3a91f621f1e362fa0fefd058e87bf8aeb1b1d2c1a8`  
		Last Modified: Wed, 15 May 2024 09:26:55 GMT  
		Size: 81.3 MB (81336316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d540c1f502e66badd39f9acbd5037011b4a4a15454c8fb22de7aa4378ae97`  
		Last Modified: Wed, 15 May 2024 09:08:33 GMT  
		Size: 66.3 MB (66272038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57df3033110cfe5e2b581f253c669df8fcf0da5557da17d89ec043f5c44e4bf3`  
		Last Modified: Wed, 15 May 2024 09:26:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:5d4729b2ec1e031f9700b6e9c6704d7bd01b8fd8b5e51d01d3a687e085599be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10239112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e6b162c2a43413e228c9d5e79253fb6fdc9807ba7c0213c7a6c2ea4e775c96`

```dockerfile
```

-	Layers:
	-	`sha256:01d7615b4351fdb0667806162362886ce65f7b784423995bc6589fceb40fa5e2`  
		Last Modified: Wed, 15 May 2024 09:26:53 GMT  
		Size: 10.2 MB (10214193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bc68225dc0d6030a53ba812b99c3aa96190ebc5dad469546c1e1c19cd5b5a6e`  
		Last Modified: Wed, 15 May 2024 09:26:53 GMT  
		Size: 24.9 KB (24919 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; 386

```console
$ docker pull golang@sha256:77840fdf9e7cafe8a8c34a9973a7c8dff22ef47092bb06276a0b5810c7fbde5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282968183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659d2a11e0dcf0d426c2273990e86818a6b1b4351ca1efa0f58699609f33f13a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 May 2024 16:32:49 GMT
ADD file:052f086288480e72435d634b2bf07198eb86bd50d8625c576e50f1c86e39f537 in / 
# Tue, 07 May 2024 16:32:49 GMT
CMD ["bash"]
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e2ec811b59a6f77ebbb7b1faa7ee83a70e39a8f7628970c01799c727a412a1ca`  
		Last Modified: Tue, 14 May 2024 00:52:20 GMT  
		Size: 56.1 MB (56076057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182e16878498082da3be413141adb855109c55626d0485b6aafb79e1cbdc5474`  
		Last Modified: Tue, 14 May 2024 09:14:33 GMT  
		Size: 16.3 MB (16268989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45622f6623917a1133bbaccf5f0fa4ae87c3ed7e9cbdcb259e65485804757c02`  
		Last Modified: Tue, 14 May 2024 09:14:54 GMT  
		Size: 55.9 MB (55929438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb242ae8460adcf6e90ee8bbbfa1d968364e5be6c9df1fb1492e922431bc0435`  
		Last Modified: Tue, 14 May 2024 22:57:35 GMT  
		Size: 87.4 MB (87350227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d70c2e11293b260deeea31f3e83c3b7328192065df7c31df5f7c5aecfa7c0`  
		Last Modified: Tue, 14 May 2024 22:57:35 GMT  
		Size: 67.3 MB (67343315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca1943c0c0fa5c57f028e9f4d62ccac1294def5e412f457069f4879ca620420`  
		Last Modified: Tue, 14 May 2024 22:57:32 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:84d565fbb6e0b66a9c57736d742e48a1c028cca263616b2643df3d0f60ba01e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10227551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d5f7006334f820164d84cdaab0c77ceee713c8eccfe047347cdbbfa4a62361`

```dockerfile
```

-	Layers:
	-	`sha256:6c998aaefedeb2256a462d558573353e19f059d3927105f192a3f39c107c7136`  
		Last Modified: Tue, 14 May 2024 22:57:33 GMT  
		Size: 10.2 MB (10202677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f29b72e82816a03766ffd21467d05843e4b126a49b351063a76ec73e1aefd231`  
		Last Modified: Tue, 14 May 2024 22:57:32 GMT  
		Size: 24.9 KB (24874 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; mips64le

```console
$ docker pull golang@sha256:6fde08671084ad0d77f5bc3f49b1cdc427138da1d2528e00a1131676c5b03d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.3 MB (253304105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5be63bee80c927e0d7e8e4edebe07fc09de161008c6313a5544af4cb23e52f4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 May 2024 16:32:49 GMT
ADD file:21c5796082f318cf57901c774792fb836e16ed2e984bfd93de345b83005884b5 in / 
# Tue, 07 May 2024 16:32:49 GMT
CMD ["bash"]
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fc8239cb1934c4e9e9368d2009f62f73698f5ad0167ec8a7f5128c5b24848b49`  
		Last Modified: Tue, 14 May 2024 01:23:03 GMT  
		Size: 53.3 MB (53322052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae485d7e63e18bea6220a5c2d4a706379e1cf701af08f3d2bc40119bd3dd7ae5`  
		Last Modified: Tue, 14 May 2024 11:40:25 GMT  
		Size: 15.5 MB (15530346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b7741bff2a58b71ac6371e1fbf6f9dcb366c82fb6243829c330c2a13b5037`  
		Last Modified: Tue, 14 May 2024 11:41:09 GMT  
		Size: 53.3 MB (53312597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c1db3d8544cf27da7715568f3ed45a88483687cc1a80dd03818db7ec4d0b87`  
		Last Modified: Wed, 15 May 2024 19:08:26 GMT  
		Size: 67.0 MB (67023003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd24f52d83e351fc6c8a79cd9b7021f852d722e6f4914f2e51b03ad27dc8605`  
		Last Modified: Wed, 15 May 2024 19:04:54 GMT  
		Size: 64.1 MB (64115949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1df24f30df45db215317c84310f1dd24ec03339c103a6075f61ff743f40163`  
		Last Modified: Wed, 15 May 2024 19:08:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:17676c9b4510b42d4f82629585c7c7e57e0f69b20a701edd87c474017f44bca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 KB (24753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e26c51cf4b7f1d478eed2d2444ca34781df0a2a798cf15731d354d27c825c36`

```dockerfile
```

-	Layers:
	-	`sha256:982409582a807c2c9278260e61df4747bee768697a515f03613c123b46388ea6`  
		Last Modified: Wed, 15 May 2024 19:08:19 GMT  
		Size: 24.8 KB (24753 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; ppc64le

```console
$ docker pull golang@sha256:fd56e6fdeb589fc1c0741bb9202b9e36cad98a3664337202afa3465941141e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281413106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ca2ab6aaaf2ead7cc34dc97fd3f81e65710256bc5cbe5d6bbfecc589a3ca91`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 May 2024 16:32:49 GMT
ADD file:4b54ed39e81b5ea585c47d145304cf7a54b08e7b1ac284a533f59d1a4768da9b in / 
# Tue, 07 May 2024 16:32:49 GMT
CMD ["bash"]
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d13e42d2790e01b63e6e5f051b276a525e360366071e8144b80a7a814c950f7a`  
		Last Modified: Tue, 14 May 2024 01:24:27 GMT  
		Size: 59.0 MB (58969434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fe3151b57b060a2fe0ca52c8936b461c9e0545bc85c0c2eb5f57ea98c7a94a`  
		Last Modified: Tue, 14 May 2024 07:11:41 GMT  
		Size: 16.8 MB (16766925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435512f1cbc8e07bb0a635d32fa068bcf448922bef667d36de93d14ae1a1efaf`  
		Last Modified: Tue, 14 May 2024 07:12:00 GMT  
		Size: 58.9 MB (58873785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d411219e2c32387f746f96d674e9586c620030d01db21840078e47aab2b8d19`  
		Last Modified: Wed, 15 May 2024 04:45:41 GMT  
		Size: 80.4 MB (80372748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a09e6cada02540e54f2e6e8c59f80c9960dc5c4559a3d96a1cc4bcca469ff9e`  
		Last Modified: Wed, 15 May 2024 04:44:01 GMT  
		Size: 66.4 MB (66430056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a4cbc765e9a552c1ee367f3d33284cb599f559d690f0b6d30b9d7bfd1c850c`  
		Last Modified: Wed, 15 May 2024 04:45:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:d19566ed3ab0825e3a89e68d24445e1988e0454bc1d7885d84273e4555c6df2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10203039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a279f962c8ee0d6eec6e81e4bac362f3b9badeb72b7056f88cef0d9965d9fe9b`

```dockerfile
```

-	Layers:
	-	`sha256:b581e8aff8c9e548dbd77df0a1e1721e2fc34ee67197d675cfcca6fdda634f39`  
		Last Modified: Wed, 15 May 2024 04:45:39 GMT  
		Size: 10.2 MB (10178088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967eaacdc64f27a4ff3130268015b31cedc9ab1a4c3c9cba5085b159bc343571`  
		Last Modified: Wed, 15 May 2024 04:45:39 GMT  
		Size: 25.0 KB (24951 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; s390x

```console
$ docker pull golang@sha256:b50a3ceb0251440a5942b50d8d8d8eb6f45d54fefabaf10c3eb991525ad55c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257081638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98a47ecb93cbc785649f572345a1ebad530df71c555d361b7cee988a028b1d6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 May 2024 16:32:49 GMT
ADD file:a0baaba4b04b93c49efe9fdafcb2308d4f775370b8e2a926df265487484d9788 in / 
# Tue, 07 May 2024 16:32:49 GMT
CMD ["bash"]
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:43f368780ca3724d6cdfa64641264541097ebb1b158cd3e0439fbf1846f179e9`  
		Last Modified: Tue, 14 May 2024 00:47:50 GMT  
		Size: 53.3 MB (53337573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a81dfed6865ecaa40f3f43b4bd4c389449dd3e0fcdc04d95ffd4c8e09fa9cd`  
		Last Modified: Tue, 14 May 2024 01:30:16 GMT  
		Size: 15.6 MB (15642393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0bebc382626195b064b7bc5d045ae9224b0d8f3c00157347449a593b555471`  
		Last Modified: Tue, 14 May 2024 01:30:30 GMT  
		Size: 54.1 MB (54076843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37842ed5856e4a7d59352985e1785f51b4b3ba0b2fc065f293f4e7cb0a81e2ee`  
		Last Modified: Wed, 15 May 2024 02:45:55 GMT  
		Size: 65.6 MB (65625594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b913ee17a483cc427f632db9240a13b45ee66ca5d56d622dcfedef41eaa6cd`  
		Last Modified: Wed, 15 May 2024 02:44:08 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fee3b7096e1e9844d71a99dfa9bf361a37455075f1fcbf8db27b138bc6d1306`  
		Last Modified: Wed, 15 May 2024 02:45:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:d7b30b9ff1305692c865460baf76ceefe6bbe335edc25d682cc4ef13974ed482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10066881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31db85a586a842e92e7c36a5af9fb8fdff9264ceb1920938f6c2c742733a0d63`

```dockerfile
```

-	Layers:
	-	`sha256:55670bcf1e586c8704af98615e9b36e5f214ab5b9a40265444166b10a85f16f9`  
		Last Modified: Wed, 15 May 2024 02:45:55 GMT  
		Size: 10.0 MB (10041972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5edb6c21aab4b4cd6370d9be3471bb8c3d3115c6098a3437f3e3461ee5df97f8`  
		Last Modified: Wed, 15 May 2024 02:45:54 GMT  
		Size: 24.9 KB (24909 bytes)  
		MIME: application/vnd.in-toto+json

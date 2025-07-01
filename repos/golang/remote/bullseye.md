## `golang:bullseye`

```console
$ docker pull golang@sha256:92523b060a66e941a0c0a20afb7895e9bdf80748741ec12c29d5859f213968f1
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

### `golang:bullseye` - linux; amd64

```console
$ docker pull golang@sha256:25213d49c32e4a877ffa6dd10f9309c5965fe53988d968197464a37a939de6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289281563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d582c6a625957d87bbee9bcb38af664e0768739efbf525858c07bfb48ffb4d9a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408a499c9b569e198473b636afa8c383e459ee6fe76ba4159b758c84e68f10`  
		Last Modified: Tue, 01 Jul 2025 02:25:30 GMT  
		Size: 15.8 MB (15765336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06772a4eff3df697497bb68b4dcdeb97fdb9338b5e7dde7d1a53579c3203c9ba`  
		Last Modified: Tue, 01 Jul 2025 03:20:06 GMT  
		Size: 54.8 MB (54757481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf79c8cc38009862a24d343b55a2227f7c333f0866e45246104708110e9a9663`  
		Last Modified: Tue, 01 Jul 2025 04:13:12 GMT  
		Size: 86.0 MB (86021956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f67fead7e33763b5fa924cb2e4644bbf5332ed056eb32ba0bcd3bdb68eea3b`  
		Last Modified: Thu, 05 Jun 2025 19:27:55 GMT  
		Size: 79.0 MB (78981811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620308340857488dc978c3b079eb875363beb4021aada8325579e796ee50d13`  
		Last Modified: Tue, 01 Jul 2025 04:13:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:e520cfd8159b0576e96b2b9181398d6185ca4e02ba4d4b58e5ea5f1b5d67683c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1f6677f6d1fccb287f5db9dedbfc2b341c035cdc386e0fd645180f78c73419`

```dockerfile
```

-	Layers:
	-	`sha256:45e2636745f217ae47d73e6c1cb4f60161bf41fc72fba52f23a6da8e89bb8f37`  
		Last Modified: Tue, 01 Jul 2025 05:22:41 GMT  
		Size: 10.5 MB (10499264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a00180ec8595a5196a08bfb9de4c760375e659847c41636bf6830eef22774764`  
		Last Modified: Tue, 01 Jul 2025 05:22:42 GMT  
		Size: 26.5 KB (26467 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:dc2f04316addaab11b1582b5eff8dd38d70f3852bce08874d1b9c0c936822223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.6 MB (256642300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff470d2b137c58a259cde050bf662daa93d32fe403e29a47afff2446d039022e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c43258def9bd93af20e1c5bd4e42a71d9db281a9fc468bbb5eb78d7a51c6472a`  
		Last Modified: Tue, 10 Jun 2025 22:47:56 GMT  
		Size: 49.0 MB (49043954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319bc9ba38020b34f4e3f562e110c9ab25e658493eaf95bfc783a633f2d4b036`  
		Last Modified: Wed, 11 Jun 2025 20:11:47 GMT  
		Size: 14.9 MB (14880672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc07acb5bb3458d1880be716fdb2bcc90e78327b21f1c1531b5e4bd0941213a8`  
		Last Modified: Wed, 11 Jun 2025 13:12:55 GMT  
		Size: 50.6 MB (50630824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f7feeb0b6a1c7b2f8058fc4bcf8523950540bd39c01231df0b01c7791add68`  
		Last Modified: Wed, 11 Jun 2025 18:28:34 GMT  
		Size: 64.9 MB (64942390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ca4d2f2221547bbb6d011d5b305d7607f58d76e99b3112e811b1627f40e830`  
		Last Modified: Thu, 05 Jun 2025 19:28:26 GMT  
		Size: 77.1 MB (77144302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c99372cb8f00ea0f6864703347d3b1999882fdec46f5abd7caafc1f6882a6e`  
		Last Modified: Wed, 11 Jun 2025 18:28:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:ed9191d3317010580f1be2b925e091295a21b601312e97200a314f0f06ee79eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da750e2ec4ba3a1e77167b54a902f0e5a3b5fb32661f657da28c2c658cf470e5`

```dockerfile
```

-	Layers:
	-	`sha256:bca2611b435bec19f2019324c7c6273685b50e86f5ca310f9c1909213cc9d578`  
		Last Modified: Wed, 11 Jun 2025 20:22:44 GMT  
		Size: 10.3 MB (10306259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd1558ef0cc1b64ea1d15851cef41591ba9808b6d4f7f4c1ca28710a4279d911`  
		Last Modified: Wed, 11 Jun 2025 20:22:45 GMT  
		Size: 26.6 KB (26570 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:adab0729c01346f04209d2ea5fb42d1730170d4f4a22277379311902f26b3a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279522730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4189202f27d1c7235c3f3edd89bd5af7c0d118f86dbd103b53d36dac1015051`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5424250d141bf5f4ec62e698bba9b5695482a3015186d3b14a633da8916bf7dd`  
		Last Modified: Tue, 01 Jul 2025 06:52:24 GMT  
		Size: 15.8 MB (15750716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7766ba090abb327ecb7e9e14ac90bbcc45c5ba6bb8a568ae531c960ff1acad55`  
		Last Modified: Tue, 01 Jul 2025 13:29:45 GMT  
		Size: 54.9 MB (54855722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98572dd73a5c059785d6a372d5be31fb37c7a7723e69652d697c7309a4cbe212`  
		Last Modified: Tue, 01 Jul 2025 17:19:15 GMT  
		Size: 81.4 MB (81432336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f244882bda0eb70b1153262e9054d1f8801651888a3a6fc5a828db420391040e`  
		Last Modified: Thu, 05 Jun 2025 19:28:02 GMT  
		Size: 75.2 MB (75231544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3ca82295f5cef6eb62690d1ac80593e0f5feee0ccd032fe44baf7ee4980ed0`  
		Last Modified: Tue, 01 Jul 2025 17:19:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:5d872983decbee9a231c89770ba49b3bd269aeca7ca142403b2b03a86efa606e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10527173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6fe9767ebb15463230b7f61e7d803ae3f2d596760a70361eb4a372f4ebe1b5`

```dockerfile
```

-	Layers:
	-	`sha256:c616f43a1b1661797293d3c4ddf836b9339eef891c2e493da228e6f00baa683f`  
		Last Modified: Tue, 01 Jul 2025 20:22:46 GMT  
		Size: 10.5 MB (10500571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d75faa4b11a6886e20949995d47e0f5a3f7b73e6d6d2a4748b06f765368177e`  
		Last Modified: Tue, 01 Jul 2025 20:22:47 GMT  
		Size: 26.6 KB (26602 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; 386

```console
$ docker pull golang@sha256:29116c31e2f8c07733dbc861187ed6bbec305983e602e324794f25ef5f87cb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.4 MB (291357532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edaf482f5de20b7ed289ca9067add88911a5c581b5bf576bd38fcb2fbcc5ad31`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113be81052ec8e8323c4db158dc9c99295355934e950a6367e5c27038fd1e04c`  
		Last Modified: Tue, 01 Jul 2025 02:24:43 GMT  
		Size: 16.3 MB (16268907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05b439f6df174e28bd21dc59eead603def3bcbd47ec6462f86b7758c4db6ef`  
		Last Modified: Tue, 01 Jul 2025 03:19:57 GMT  
		Size: 56.0 MB (56049937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24409f6f24831cdf9a206d20c11693816722d7fdbacc221aa1db1fc877179f6a`  
		Last Modified: Tue, 01 Jul 2025 04:13:31 GMT  
		Size: 87.4 MB (87448017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae592fba0490bc253690fa17e5004b2923bab9e7f9c8d6e116245da17997d7d0`  
		Last Modified: Thu, 05 Jun 2025 19:28:06 GMT  
		Size: 76.9 MB (76900579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ed870cca4505cd89075298281a841f9b36761d2f91aedd17c935f82d48d5f6`  
		Last Modified: Tue, 01 Jul 2025 04:13:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:7a4a4be1d213f9e11da0bff9bcadaac63a78cb93584ec3a1280b768ee6c52956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10515001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c813067c29b46adf18032251b221d78f18e5537069eaffb8c3bd99aed4f6b1b1`

```dockerfile
```

-	Layers:
	-	`sha256:737ecd8ba4ea11210a8c94bdfffcc46cf8a246e67556c4d9995fa4a113df8704`  
		Last Modified: Tue, 01 Jul 2025 05:23:04 GMT  
		Size: 10.5 MB (10488569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fd48e50d3263eea07afc169b792995eca20ba55baf6624cafbea27edb9aa8d5`  
		Last Modified: Tue, 01 Jul 2025 05:23:05 GMT  
		Size: 26.4 KB (26432 bytes)  
		MIME: application/vnd.in-toto+json

## `golang:bullseye`

```console
$ docker pull golang@sha256:ce51c709f86b89febb2b0bc03b33a978c0b52293b43fb18ac93e647aea8c51a6
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
$ docker pull golang@sha256:6f73dc550599a3d346b55a2c7f9578d5dd68a3c26d8ec038114a72c69a095505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284066641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579d365201685247ce1a6677ff9d9654e50ef608456b6f08e82ae61e21de9331`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOPATH=/go
# Tue, 04 Feb 2025 18:26:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 18:26:14 GMT
COPY /target/ / # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0388f0d5bf1adc15e551cceee5a85f21b1ebf5b13c380ee0e941c5d55013598`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 15.6 MB (15558271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d473f760e53d3d50afd1cebc7113387023a04ff8ec34073c4412b465ccc2fc5`  
		Last Modified: Tue, 04 Feb 2025 05:19:08 GMT  
		Size: 54.8 MB (54751917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4964402c92ec3884f54a18573b81ea733af145cb379e3545ebc13c6fc654c6bb`  
		Last Modified: Tue, 04 Feb 2025 19:33:16 GMT  
		Size: 86.0 MB (85971567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd968b00abc2f44f5d74b014d2b833a05dd020b5f534f19dca853c409df33466`  
		Last Modified: Tue, 04 Feb 2025 19:32:46 GMT  
		Size: 74.0 MB (74045855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce186e0ce44cdc6d047f69a781db76161d0f7c9bddcbd2fcd543a28b055b7bf`  
		Last Modified: Tue, 04 Feb 2025 19:33:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:06d81ce096f016a44c492ee2c432828aa03cf48eaaeb35ce709c1f0c21a8a5e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:240664f8f46989476e6e0d0af3ee9d7f956d22f3e9a3a54589128655c3b1c773`

```dockerfile
```

-	Layers:
	-	`sha256:121eede20b261520cbf35bf8bc437eebd4d1cc28b72396c714b956654d366b85`  
		Last Modified: Tue, 04 Feb 2025 19:33:14 GMT  
		Size: 10.3 MB (10268959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c80de66ea25aced27d81252b1ceded1f341dedefbfb12e3bd948e9cb0728f346`  
		Last Modified: Tue, 04 Feb 2025 19:33:13 GMT  
		Size: 26.5 KB (26468 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:13aa3f84b620ec89db2ebe6cbe9b3efa6e1fd9b57cd4c9c911454f6d8d860306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251426404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525deb4efb79a0217693a86c0a5b55bc92041168d30846a704bc280314910d97`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOPATH=/go
# Thu, 16 Jan 2025 21:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 21:14:07 GMT
COPY /target/ / # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055bc7f040fce3e9b8f05fd7f56b8a568950e082ea8ea3aa96cf99f49523ca5`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 14.7 MB (14673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681398f28ce19a7af317e3774529df465ed1770ca10164fdba3b20f23a5d8026`  
		Last Modified: Tue, 14 Jan 2025 16:16:27 GMT  
		Size: 50.6 MB (50640646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805d177a7a386c16ebe8d12f47c059e2765669213f25366ab009643e7e84dab2`  
		Last Modified: Tue, 14 Jan 2025 22:04:03 GMT  
		Size: 64.9 MB (64892787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71181da0f46bebe3348744084ada18c7bb3fc1a115b2faa229669f2846f8a617`  
		Last Modified: Thu, 16 Jan 2025 22:10:17 GMT  
		Size: 72.2 MB (72193920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bde5b79bfa9472d8b829dbaab8c66a1637aa674d4d8981f9e54c821a049d2af`  
		Last Modified: Thu, 16 Jan 2025 22:11:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:27ae3b72706459037a63c2cc69f781b3f180aa9fb52e51e8c60ae381f26a2065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10101871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220cba373f8682b8bf3a00b4b1415106cce62823e725ae973069d7850103faf5`

```dockerfile
```

-	Layers:
	-	`sha256:1151d72ea695893997db5d50ebbead53daf0e1dda3c19f00638de32d45a50f98`  
		Last Modified: Thu, 16 Jan 2025 22:11:07 GMT  
		Size: 10.1 MB (10075301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e748bad19f263b26bbe7afcc2976280e9b91e2798f8761a2b79ba543cfb9b33`  
		Last Modified: Thu, 16 Jan 2025 22:11:06 GMT  
		Size: 26.6 KB (26570 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f051a5c8f2bb77a48cdbf075cf251430b8574fd6591bf2e2eda8b5f97c7d2735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274701766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30eea79f1b72cf345fb27711f46623df596652e057720f8958625d4a928ce7f3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOPATH=/go
# Thu, 16 Jan 2025 21:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 21:14:07 GMT
COPY /target/ / # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfd6b176342cb480b79cef9a7188364b0f5702ccc77422fcdb5d7d8f3f42c8`  
		Last Modified: Tue, 14 Jan 2025 07:00:18 GMT  
		Size: 15.5 MB (15544093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23ac0e9b25076f1cc90469f31bffaae783c6a3a88272620af5e7dcbe0b8202`  
		Last Modified: Tue, 14 Jan 2025 13:31:46 GMT  
		Size: 54.9 MB (54852602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01465e7bfd0860e22fcea8887f9fed9a79cf8b30c3d7d1f26f90f5947268c69d`  
		Last Modified: Thu, 16 Jan 2025 22:06:51 GMT  
		Size: 81.4 MB (81382578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9d514b7aa85ba6aa1665a90e4a24f9a4312a9ae69f1e26235cf49d08b80c7b`  
		Last Modified: Thu, 16 Jan 2025 22:08:29 GMT  
		Size: 70.7 MB (70676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2b0b8741b504b9c72bb6bbf5fcebb3214956dba0f34013c09561abd77c0911`  
		Last Modified: Thu, 16 Jan 2025 22:09:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:9e94eb519c95edd1d4400f5de453382bd8e01d2f73bb9d74e395f4b1facf561e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10297139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485c87f8144d3693c0decf6097c1336bd431fbaf2904c330c225566cc92558c5`

```dockerfile
```

-	Layers:
	-	`sha256:15544c572b1f34e81c0c455981a0bfb72f7d55d2182f08c882c81650bae0c321`  
		Last Modified: Thu, 16 Jan 2025 22:09:02 GMT  
		Size: 10.3 MB (10270537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86582b77e5e3f10cdefe0c89a8714942de8c546f15f575b7a7ec323a0358ce50`  
		Last Modified: Thu, 16 Jan 2025 22:09:01 GMT  
		Size: 26.6 KB (26602 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; 386

```console
$ docker pull golang@sha256:2b53976283523a41694dc43a3c48d3acd31d09f1b3c1e76c3bfbe57b09e41b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286086036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a4fcd2edbe6c36bb3a7479b571ab46cd15097fcf749d3adc77911600435b31`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOPATH=/go
# Tue, 04 Feb 2025 18:26:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 18:26:14 GMT
COPY /target/ / # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c2b5327eac1fcd49233dc8f6e5417e7e2efeea16edfcbff9dd025f389e15b11e`  
		Last Modified: Tue, 04 Feb 2025 01:36:38 GMT  
		Size: 54.7 MB (54675956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d372eab1872f98afed1da2c899af883a0b3a6e52e25e2690ed35b3d6f859e5`  
		Last Modified: Tue, 04 Feb 2025 04:23:38 GMT  
		Size: 16.1 MB (16062054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4520e7fd9b17628990db3e961c2d7570421849af1fe255937c0a9e48cf49a48f`  
		Last Modified: Tue, 04 Feb 2025 05:15:33 GMT  
		Size: 56.0 MB (56029876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11861e3f148bc95dfd80370398e10e3d33ae3752c3e156597e36693b2cea921`  
		Last Modified: Tue, 04 Feb 2025 19:33:01 GMT  
		Size: 87.4 MB (87398180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b77728945927969d0c8ded023b60910b4b7d2a79c658271ebe4948de9a6d578`  
		Last Modified: Tue, 04 Feb 2025 19:32:35 GMT  
		Size: 71.9 MB (71919814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4331307f3dd3a2b0bc0e07d8d6ab4daaf16d289380436289ad673e32d5cd24`  
		Last Modified: Tue, 04 Feb 2025 19:32:59 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:d9480ffa8b1dcd2b0fdc56e78cdad706f16019a27dcbadc638c3ed9d8164e238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10285176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d016456cb0fd6327ecd68be98357ce342338e79820a480912ed4f3b5e1d3a8`

```dockerfile
```

-	Layers:
	-	`sha256:08a23e53380b54a727eee432f6da4a840290b10eda5223bd594e3f5f944814b0`  
		Last Modified: Tue, 04 Feb 2025 19:32:59 GMT  
		Size: 10.3 MB (10258744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7462837737eed41511da64fac3293967e8b9b28751329e6451457228c180abba`  
		Last Modified: Tue, 04 Feb 2025 19:32:59 GMT  
		Size: 26.4 KB (26432 bytes)  
		MIME: application/vnd.in-toto+json

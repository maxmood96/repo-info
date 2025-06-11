## `golang:bullseye`

```console
$ docker pull golang@sha256:008af92ebdd6e450d813e973de35a346c2a77181a0a0f6cbed8878dacef2bc79
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
$ docker pull golang@sha256:9152d4f2dc383fadb85c66a8910e9af0cbfdeed913fa11d1b3503d8a2b5ef2c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289281256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6f1fe89584994285c8331ccd40f0aa7106fea4836ba0d4b461e2674fb6641a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8156a957a8b63a670ed89130a2e1eedf5c1b2a939f33a952c4159b4ebcb0a`  
		Last Modified: Tue, 10 Jun 2025 23:36:44 GMT  
		Size: 15.8 MB (15765139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2678613884c2f141cc551880b1a1587f0c890606a900bbac5a1ace2645be657`  
		Last Modified: Wed, 11 Jun 2025 00:02:35 GMT  
		Size: 54.8 MB (54757363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88df5d87501d36d778326a0aac9b82eed594c7b1482f9525ed45c1c8a21552a`  
		Last Modified: Wed, 11 Jun 2025 01:14:49 GMT  
		Size: 86.0 MB (86022003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f67fead7e33763b5fa924cb2e4644bbf5332ed056eb32ba0bcd3bdb68eea3b`  
		Last Modified: Thu, 05 Jun 2025 19:27:55 GMT  
		Size: 79.0 MB (78981811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e983c59284a4d6ea90caab11c4d9fb40b663ee18a6dbb8d6fc0e8225070706`  
		Last Modified: Wed, 11 Jun 2025 01:14:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:8d4b83f3f79488bce6b77f5412b5254215676e9651cf0df24b3165a5bea2bb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c22b1cbd8cc9911b5c16a2ae8f1282de1094d150832f44e607b50da9172e644`

```dockerfile
```

-	Layers:
	-	`sha256:1814b6367f329c3a2eccad9cfa48b298821fb527a59b20f5b50144f0556d6f4a`  
		Last Modified: Wed, 11 Jun 2025 02:22:40 GMT  
		Size: 10.5 MB (10499264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48f717b1a433cd0250082f0bbcf3f1c97c6ed0577a772adc703cc967fe877bba`  
		Last Modified: Wed, 11 Jun 2025 02:22:41 GMT  
		Size: 26.5 KB (26468 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:09b38cdfe714b2ab968471dcf5d69bcb88a9d526760e08ddabb6ad10d8c44a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.6 MB (256640743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2160cebbff34e08319ad536ff1dcaa24c2f86895a29f8c66bf99b50b36eda3d8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
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
	-	`sha256:2bf062f1f44f96722293994387f4b88016e2f0a9f49c7f09b2ceffefc7717199`  
		Last Modified: Tue, 03 Jun 2025 13:43:06 GMT  
		Size: 49.0 MB (49041988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933c7aef3dae867caad0cbafef5672fb39317c04b3bf8bff0868bf265098c4de`  
		Last Modified: Tue, 03 Jun 2025 14:32:56 GMT  
		Size: 14.9 MB (14880519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0144e65734487c61a592b9ecd7d576c77bc270bd5d65049de36718f77416c6`  
		Last Modified: Tue, 03 Jun 2025 14:32:58 GMT  
		Size: 50.6 MB (50631322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd4739ceb6e38b56a017a3579cc385de56e1cf7fc98c2c4b4dabd966a9c123d`  
		Last Modified: Tue, 03 Jun 2025 20:02:27 GMT  
		Size: 64.9 MB (64942454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ca4d2f2221547bbb6d011d5b305d7607f58d76e99b3112e811b1627f40e830`  
		Last Modified: Thu, 05 Jun 2025 19:28:26 GMT  
		Size: 77.1 MB (77144302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcf921c0fdf08bf437091e97743106903a1d620e63829a373fadc9a24227770`  
		Last Modified: Thu, 05 Jun 2025 19:28:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:be74cc0507f876206fa214289fc79a84b55a2940c9ae1d8ae4738446e9eb92dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10144636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20dd20d07e8846ae7545727288c2b915042db9acac02428aa2a7c9ff490bcefe`

```dockerfile
```

-	Layers:
	-	`sha256:2e03b69939dbbf2b43368c4fbe100575e63eef10a6634165313103b92ded5f7a`  
		Last Modified: Thu, 05 Jun 2025 20:23:56 GMT  
		Size: 10.1 MB (10118066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8bc4012b47d0ee3a2d42575a891309aaa3165f5ce4b21241498036ed471dece`  
		Last Modified: Thu, 05 Jun 2025 20:23:57 GMT  
		Size: 26.6 KB (26570 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:8addc1b6b03b52ab62e2fb01a29976520213d4d9d3e20bf187f22178bf3d6434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279520136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45caee9df7837c8144c88a65fe864c7f073c8d00f87bcc482297ecf964f37c8c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6f3b6fbce84c42871ea80f05b2c61e622e08647f7164e9a95a391926c1f714`  
		Last Modified: Wed, 11 Jun 2025 02:56:50 GMT  
		Size: 15.8 MB (15750566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7850095446c84fa9107622e378378aa7daf4b928caeecbc1149118900d32f7`  
		Last Modified: Wed, 11 Jun 2025 10:33:17 GMT  
		Size: 54.9 MB (54853082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce21d4bbe9184212fde8adefbfc030f40411c90d06a55c1e3138b2484c5ef9a2`  
		Last Modified: Wed, 11 Jun 2025 15:25:23 GMT  
		Size: 81.4 MB (81432485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f244882bda0eb70b1153262e9054d1f8801651888a3a6fc5a828db420391040e`  
		Last Modified: Thu, 05 Jun 2025 19:28:02 GMT  
		Size: 75.2 MB (75231544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976b6d321be39c3167558551bc6c286bd6f7d69d0eaa1602ef84f953d38c0e99`  
		Last Modified: Wed, 11 Jun 2025 15:25:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:e4c85edab32eaa6873d3c6956f729f7b1f346fb7b8ba9fc401a80eb2dba0e3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10527173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab0a38b9faa7d9a3cd44f722c8ec4382cf444a5afb32c743b0463a0accf28cd`

```dockerfile
```

-	Layers:
	-	`sha256:081c886d82fbea5b0d2dfd883f259837897e24e5a20f55b94354011ee80426db`  
		Last Modified: Wed, 11 Jun 2025 17:22:44 GMT  
		Size: 10.5 MB (10500571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f37d34f50ac1c895445bc1db0084300d47239ef6ec7ba48b536edf19d351141f`  
		Last Modified: Wed, 11 Jun 2025 17:22:45 GMT  
		Size: 26.6 KB (26602 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; 386

```console
$ docker pull golang@sha256:a78fd72124c4d3f57334931ece5331f2d560963305903add5c45ba6e5d1f911f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.4 MB (291357337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd09de5a9d01a7e95fa0507cea89db5171ef5b97c85932a4cb1d6bab0e748fb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
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
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e7c1ed34c380b4c9e9f08e94b0f7b9bf90a0e8c42de246cb4b2159e2126fef`  
		Last Modified: Wed, 11 Jun 2025 00:00:47 GMT  
		Size: 16.3 MB (16268617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3a34392e433938214bbf2cba34365a474d819c470686803059c6d8390cf680`  
		Last Modified: Wed, 11 Jun 2025 01:13:31 GMT  
		Size: 56.0 MB (56049939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8aa7b664fdaf3297d83a495d4d0321b254c2ff2cd304a1e4b4bdfd40e272d3`  
		Last Modified: Wed, 11 Jun 2025 01:14:56 GMT  
		Size: 87.4 MB (87448033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae592fba0490bc253690fa17e5004b2923bab9e7f9c8d6e116245da17997d7d0`  
		Last Modified: Thu, 05 Jun 2025 19:28:06 GMT  
		Size: 76.9 MB (76900579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddd7c91a5e5f16430a656e058ef645e83309635cba53d2ade4450d181b08a2a`  
		Last Modified: Wed, 11 Jun 2025 02:16:10 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:ec7887f41337ad7ef1b66a1533f78e1d1dfd15c19cb6eb3aff638dc45b940f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10515000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17a3f05c31ea04df38cc0d141e1ec66ba5fceb2fced4b7b3c1e396a3ef7d995`

```dockerfile
```

-	Layers:
	-	`sha256:f166a85d4af436e05e026247e90cf24e17ef52d2464401122423081684abdaed`  
		Last Modified: Wed, 11 Jun 2025 02:23:05 GMT  
		Size: 10.5 MB (10488569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39b77bc5412799ed407432d4a16415281d168b280f5081f0042bc6a483ebf437`  
		Last Modified: Wed, 11 Jun 2025 02:23:06 GMT  
		Size: 26.4 KB (26431 bytes)  
		MIME: application/vnd.in-toto+json

## `golang:1-bullseye`

```console
$ docker pull golang@sha256:9e53abacfc22cd3df3e4ebcc04ac64951b71d2a38c52b690f3807af6a2000ed2
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
$ docker pull golang@sha256:881b57c7365868a3bf7fa9488e52ef554107db5d93c1831fd46e0f6d31512800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284062222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28f3955445e745a5a23b49c4fe13c9806a89d05ea5bef1072064290def3a452`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925257a7168ed219a5d7c2a69af3245ca4cd9e376424f7f006535d9714437bd4`  
		Last Modified: Tue, 03 Dec 2024 02:15:41 GMT  
		Size: 15.6 MB (15558387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb34ce34679cf6bc8738a0166300fb0af605abff20bb9c1c8008dbc48722061`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 54.8 MB (54753972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df8aac0343541eb0c97272f251d6ef9eb7bdb2dcc4dfae955e213af1571b8ed`  
		Last Modified: Tue, 03 Dec 2024 04:31:49 GMT  
		Size: 86.0 MB (85971558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79bddf330f7de2b96b69740174bc7152350ef81439db2dfa776fc3a9365dc80`  
		Last Modified: Thu, 07 Nov 2024 02:59:16 GMT  
		Size: 74.0 MB (74038999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6164018c014e434f7140750d2009e0be5da6cb17159f34c8181372c9071548`  
		Last Modified: Tue, 03 Dec 2024 04:31:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:e0c92a9221fcb46669699846f610885c578c0c25adb0ca8c99d9a896124ea448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10308538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b194d97959c174ed38439be2cde08421b84ab044c9c2e6807abcb0b65af9a307`

```dockerfile
```

-	Layers:
	-	`sha256:60a0258bd022994f6d72216ef6a2baedcc3b8390c28bea5fb376d926383eef2d`  
		Last Modified: Tue, 03 Dec 2024 04:31:48 GMT  
		Size: 10.3 MB (10282070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1c552e4dd8fc21afce69180d64b2a0b98d176e93b49363e1d56400aa2d2106b`  
		Last Modified: Tue, 03 Dec 2024 04:31:48 GMT  
		Size: 26.5 KB (26468 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:c1b61434033d78804b7e7a66efd3209c150311267ad1cacc5cc977ccd39c4c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251416066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffbd635938c5fcf3c8df0daade4ff954e8cf882b8e11ddb5c50e605e7a21d26`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69dbedc8019388fd330866fcfa04c35d28f86d1ef986691ee290054433639992`  
		Last Modified: Tue, 03 Dec 2024 01:28:37 GMT  
		Size: 49.0 MB (49025021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370e6aa30e16daf07d99e3fb5cd8610cda77f49507a7b2ba76a646359cf7db6b`  
		Last Modified: Tue, 03 Dec 2024 07:36:42 GMT  
		Size: 14.7 MB (14673759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54bf5af43178bf200a2aed84d9a42570d6bde94092c2ac746652561137c9a86`  
		Last Modified: Tue, 03 Dec 2024 17:16:41 GMT  
		Size: 50.6 MB (50640414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237566a0c373b0ea5bb6b5e06c163480b2bd251ba16e744e051a9b21e15496e9`  
		Last Modified: Tue, 03 Dec 2024 20:23:09 GMT  
		Size: 64.9 MB (64892629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e990400f8c0342109351b2ea2dff891387190e755f29d02b0f474578fc3d222`  
		Last Modified: Thu, 07 Nov 2024 02:59:45 GMT  
		Size: 72.2 MB (72184086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dea69b0b68146dea3238a614ac1aef81862546c6a33a3b9128587c841e0b9c`  
		Last Modified: Tue, 03 Dec 2024 20:23:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:efc35bafd08b8452ef30b932c3e48de5c3e74193375d4f15ebd41a8e75e77cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10114766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e05d0ecf850034f7b576c320ed929a27eb2034819c6f7e75f756e6ed332b9b`

```dockerfile
```

-	Layers:
	-	`sha256:c59deaedbb0a3d812fe22f791da6432491beee1a329be13d6ccb3538df5471d7`  
		Last Modified: Tue, 03 Dec 2024 20:23:08 GMT  
		Size: 10.1 MB (10088196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cef1934ccad219b60ff10153e8e0363b37d5239ec69eaec83d2193f23f2dfe1f`  
		Last Modified: Tue, 03 Dec 2024 20:23:07 GMT  
		Size: 26.6 KB (26570 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:a176dc902a0dfd587432779c7217ff6a8a6882173f0fe53bd94a3d65d58c70db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274693882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaec2f68d982b928e9b740030a6a1dc2bce2f4590a4600c0255a29e5c8181a7a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b2279cee7374c65ae079e8ccdceeeb8b20c07ffc727e5b7cd595285b44a3a0`  
		Last Modified: Tue, 03 Dec 2024 05:39:10 GMT  
		Size: 15.5 MB (15544048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2749caeb5baae1b5e6316a6f02e57835aa548497fba6792be844c743a57c72a2`  
		Last Modified: Tue, 03 Dec 2024 11:51:00 GMT  
		Size: 54.9 MB (54852316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3ed926cdc291e41b6035844915bf308860cedf34c967373d903b8649317619`  
		Last Modified: Tue, 03 Dec 2024 16:35:27 GMT  
		Size: 81.4 MB (81382418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323003b0d8ad8001283c9881b96c87e9fa38fb378aa4de93c4defd3899f30d2a`  
		Last Modified: Thu, 07 Nov 2024 02:59:17 GMT  
		Size: 70.7 MB (70668948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c758b7f653ce80bfa0ab26fc744296079e397faefe9d7e56a382a1b312b900ba`  
		Last Modified: Tue, 03 Dec 2024 16:35:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:388d14751a3604abd2248863cfb26d06adfc578700bccd9d037ce23ba42b3dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10310270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b4e2ec9655be6e50720bb0953ffcb0b540148bbc3a6243359478cb16201f12`

```dockerfile
```

-	Layers:
	-	`sha256:b308592badca4264886c2256eef79d28da97b791cc3dc18117fab43b72fcf8a4`  
		Last Modified: Tue, 03 Dec 2024 16:35:26 GMT  
		Size: 10.3 MB (10283668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8df779384a54d249c1bc5866fe86fc1d1741395c07e6a73b17fb9e88328ffd52`  
		Last Modified: Tue, 03 Dec 2024 16:35:25 GMT  
		Size: 26.6 KB (26602 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; 386

```console
$ docker pull golang@sha256:1fde569629aa2b7db8cfbc8b14a758aee8633b84296ba1868474726e2c2f229d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286071608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96150877595b87aff96fa1c9854a992b3a404a00f545638d7b6aea08b939088`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:862f429b4105c1e5714d48631896837c3ca6f797479296293b7c33c6699eae95`  
		Last Modified: Tue, 03 Dec 2024 01:27:25 GMT  
		Size: 54.7 MB (54676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ac5b88f14d979c6f071eb85aa8a772f827338af23171657add5b5e4fc91e2e`  
		Last Modified: Tue, 03 Dec 2024 02:14:36 GMT  
		Size: 16.1 MB (16062064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc99b34aeb38c1b23bfa1cbb2b4b9d6e5a643b78e7b238368942282890609c8`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 56.0 MB (56027112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b9f6a140887d6035382252c80f84f550f77925353c17be12b711c9047aac91`  
		Last Modified: Tue, 03 Dec 2024 04:31:33 GMT  
		Size: 87.4 MB (87397982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d309da02a5efef0a1926ae8de3247932524a303115a90abb23504c4cffb291`  
		Last Modified: Thu, 07 Nov 2024 02:59:09 GMT  
		Size: 71.9 MB (71908016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f4ab74d30ddc19d6fb9385e84d46171a38a69356a84ed6365d13b223fc4f47`  
		Last Modified: Tue, 03 Dec 2024 04:31:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:92650b0353b1e0efc8a2f3e1cb5c47d1ba06ff6edde941db31d6c2537f57e249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10298288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30379205bc940d32dcde8ceb693398f3f63c0d6aaec80412e3814b13ffcdd304`

```dockerfile
```

-	Layers:
	-	`sha256:8a1f36f81a9fa452583e2d4c7a4dcdf9b3def81c64dee95162a3f71889700c0e`  
		Last Modified: Tue, 03 Dec 2024 04:31:32 GMT  
		Size: 10.3 MB (10271856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4adec82dc5479260cab12788b729aad1d6b3cb82b670d231c150918c02934047`  
		Last Modified: Tue, 03 Dec 2024 04:31:31 GMT  
		Size: 26.4 KB (26432 bytes)  
		MIME: application/vnd.in-toto+json

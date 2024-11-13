## `golang:1-bookworm`

```console
$ docker pull golang@sha256:11bdd4a00d041f6a5818e9b49a321c81394e44b54a3f13665a9891bf4c749745
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

### `golang:1-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:f61a48f4e7063c15eb9abf8cdd8077aab743fbe0d933f40c1b42d7868afe855d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304357055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0457bb691895d9d1b47fd0d8c5328b697ad2a121234dda0f232409951232930d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59585393ce674fb64fcaaae0b8dada910951ec63eeef2f343edf54de73e0517`  
		Last Modified: Tue, 12 Nov 2024 04:54:46 GMT  
		Size: 92.3 MB (92292483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79bddf330f7de2b96b69740174bc7152350ef81439db2dfa776fc3a9365dc80`  
		Last Modified: Thu, 07 Nov 2024 02:59:16 GMT  
		Size: 74.0 MB (74038999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe407d04300b5198977867256845f5ae071d6b80fb3c877626947b71794759ea`  
		Last Modified: Tue, 12 Nov 2024 04:54:45 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3012b9669ff72b1da3e99b2d3a335f6d2527d6fbe11d489e1b1ebf16a9eb7db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5714c789aed824c3f44bcb5b224d41c938abb6bd5115d09aa7403d2a65c6c60f`

```dockerfile
```

-	Layers:
	-	`sha256:797657de01809641b388b03ebc9fe0ffe50730ab4c85f61baca5e4ded4ba1224`  
		Last Modified: Tue, 12 Nov 2024 04:54:45 GMT  
		Size: 10.3 MB (10294140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:919ef47f131c1a9b3c0cab4235f97296dc8be005e891941c0792eed6474bb0f5`  
		Last Modified: Tue, 12 Nov 2024 04:54:44 GMT  
		Size: 27.6 KB (27646 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:de503d2bc5abb47cf217ff55c9323e4b41019c16a44b6f453a7cb36241c5118a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.1 MB (265061470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b354d1895df6f21b1f8fc27cfff4c26e6cbad72e2274053cb5700cc65de220f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f68420f2ab6efd74aba4b4ff72fe115144308ecea01703acfd9de4db386df`  
		Last Modified: Sat, 19 Oct 2024 06:36:59 GMT  
		Size: 59.6 MB (59635104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59eda5fd5a6cdc7a116d09dbe0229c33b61199eda59e6ccec36e3c02d7c68fd`  
		Last Modified: Thu, 07 Nov 2024 02:59:45 GMT  
		Size: 66.1 MB (66136779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e990400f8c0342109351b2ea2dff891387190e755f29d02b0f474578fc3d222`  
		Last Modified: Thu, 07 Nov 2024 02:59:45 GMT  
		Size: 72.2 MB (72184086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2f2f7ea5e11dda4fc10813439fb2e28c2810a9b0ec3f3f62a37bedbc0b48ed`  
		Last Modified: Thu, 07 Nov 2024 02:59:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5850b06e5f9a285568ef97bb856691ec8978854b2e1041d00d8dfe35ed3e8456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10129977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4ce7c8f9017bf85257bf60fb50d8688dd0c0e2ed6f3685bc8194a33489afe4`

```dockerfile
```

-	Layers:
	-	`sha256:211c699d050c5265d8520c8fdc4cfc5ffbdef44ce2cd7f7b7fadecff16e6c30c`  
		Last Modified: Thu, 07 Nov 2024 02:59:43 GMT  
		Size: 10.1 MB (10102167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d01fdffb591110d98475c84e0b0edb4e2cb07704d94dc0d6d96405d77e57b1d`  
		Last Modified: Thu, 07 Nov 2024 02:59:42 GMT  
		Size: 27.8 KB (27810 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:15b0073131e5f3dc0cb9e94007709581e991ca21cd4b2471c5a756012f8ec98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294549249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab7f4b02fabe5c32fda4dd449cc7a34689f5d257b5ac880831b9ace94d169cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc6ea9985d6735252067a2041e797c0dedef261a9695671fa4ef7891a96e4b5`  
		Last Modified: Wed, 13 Nov 2024 02:41:57 GMT  
		Size: 64.3 MB (64347700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f961eceeef94381b62a005e74a14d6b8d71034685e61a1e8643e3386dc5a1c`  
		Last Modified: Wed, 13 Nov 2024 08:09:34 GMT  
		Size: 86.3 MB (86346989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323003b0d8ad8001283c9881b96c87e9fa38fb378aa4de93c4defd3899f30d2a`  
		Last Modified: Thu, 07 Nov 2024 02:59:17 GMT  
		Size: 70.7 MB (70668948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e25fa04684316ad6b15c4625dc07c6ef110f97f1e63d30b8769652e097b3f60`  
		Last Modified: Wed, 13 Nov 2024 08:09:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b6700552ee4529cc3280b571b0741c88d8981b4f560dc2fd9763238d663ef6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10349894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9301401158db5ec8aea4e702d73235486eb5ca17a151986a9d76e009feff654`

```dockerfile
```

-	Layers:
	-	`sha256:596c4a0aa474bf73bed0811bfdd28cafe7389f7483a48d2a4429ee18fa2cde43`  
		Last Modified: Wed, 13 Nov 2024 08:09:30 GMT  
		Size: 10.3 MB (10322066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193b1b589fc632107b203e039161a85567bf74b8c77a2e015241ed720b1f4d5d`  
		Last Modified: Wed, 13 Nov 2024 08:09:30 GMT  
		Size: 27.8 KB (27828 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:4e00ae6cc6f1798921aeb99f9c606e7abe42b394b84c4e07c0313bce43778826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303297132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b48cd8805324fd3d21b3bc79b844eac4ecc486e5758b3c226b54cc3c0d5ab5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46592415d8ae65247d6cff038217c0ae0c38f5f2fee88eaa3f5ae09743a290`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 66.2 MB (66211304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc46def7e41a68765013b503fca1514029139dd6e3f3cf6bec6f7f406a741a86`  
		Last Modified: Tue, 12 Nov 2024 03:59:02 GMT  
		Size: 89.7 MB (89701195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d309da02a5efef0a1926ae8de3247932524a303115a90abb23504c4cffb291`  
		Last Modified: Thu, 07 Nov 2024 02:59:09 GMT  
		Size: 71.9 MB (71908016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097d855e0fbac241470ddc47dcf611ceef432eec9a6a61d20c4889c3e8bfbfea`  
		Last Modified: Tue, 12 Nov 2024 03:59:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7b989b15a294bd4b75368656a325e0efd24b0ec925aa444b9525db4f1a574e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10301774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20657058410c28a57f62ab97022994271a2b0802966fbb1ccd9929784755b0c8`

```dockerfile
```

-	Layers:
	-	`sha256:e69b57ec013f78d91dc0ae6e9e5c45da34a475b2ca7d87cfbd1f344e29d3aa6d`  
		Last Modified: Tue, 12 Nov 2024 03:59:00 GMT  
		Size: 10.3 MB (10274184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e686e10719d590a1d57fbf109d13c5a90a5a9aa5ba53aefea958201e6076365d`  
		Last Modified: Tue, 12 Nov 2024 03:59:00 GMT  
		Size: 27.6 KB (27590 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:59b77b35a3d6c3a4c295d6d5df69149b221a3e5ba41b7bb00c3a24c74609f3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274672531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde1e77d951a4386dc56391ef48dae68cc4b6f1821e152e30d528808c6779fd6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:17191dc8a469e4ef93330c5c8402fa0c0761218a5fa02ad2db7b34508d0e995c`  
		Last Modified: Tue, 12 Nov 2024 00:57:16 GMT  
		Size: 49.6 MB (49559181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf888157372a89189e8193ccb502b1003341993a439a6f526f90dc05a6100692`  
		Last Modified: Tue, 12 Nov 2024 18:00:45 GMT  
		Size: 23.7 MB (23652171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aa8c732dc480c917c006c596db2d04829d92a5899b87a988672ce7b03cfd6e`  
		Last Modified: Wed, 13 Nov 2024 02:02:53 GMT  
		Size: 63.3 MB (63281490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d1f6f25ee4e0c7b1ec6d148ab77c50136bdbef9e338e495fc099aa79871dfa`  
		Last Modified: Wed, 13 Nov 2024 07:25:48 GMT  
		Size: 69.9 MB (69865831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f81694bc2d6f633d7ccbad361e1e6ae621631bf889fc11bc127c432c7d8965`  
		Last Modified: Thu, 07 Nov 2024 03:03:54 GMT  
		Size: 68.3 MB (68313700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efa916d122a23b333bd99f4522bc6a29220a831b64100cd1fc564826210d04c`  
		Last Modified: Wed, 13 Nov 2024 07:25:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b9eba0ee8dcbd968db6b4b24790668000936a7e5751533631bdf084421f24f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969f51434f02e0bf745cf19c01c60cb87eff4d1ff7711cd140754b8cf1204370`

```dockerfile
```

-	Layers:
	-	`sha256:917a57fe7bca9e2a2a5df27049ccaf50be13a09344916c5eb268631a0e72fc29`  
		Last Modified: Wed, 13 Nov 2024 07:25:40 GMT  
		Size: 27.5 KB (27539 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:42ed77f9e51736d5aef9adad5918e211277c14435384f9ece1f393ed83227fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310200411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4ee1962cef060d31ad2b46579cf0a494c62a5f35d62684940f159109c4a268`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913acd64029d37b20e9e161bb8659516cb78a99cfd56eb921fc4ccd76ae7c0c7`  
		Last Modified: Tue, 12 Nov 2024 16:09:31 GMT  
		Size: 69.8 MB (69812283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54925cdc31efe4d5e1af121f44cdcb59b0fbc2cf1ca33497a1e46997a98c01`  
		Last Modified: Wed, 13 Nov 2024 00:23:04 GMT  
		Size: 90.3 MB (90286679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d45dcd888e3183671630e662953341e3111584ee0e6ca4f0d40e50580ea2de`  
		Last Modified: Thu, 07 Nov 2024 03:00:09 GMT  
		Size: 70.8 MB (70828478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8940e8c79a95f34e24b46e26cff3ef70fb33ea7e0d211cb6260a51efa979956f`  
		Last Modified: Wed, 13 Nov 2024 00:22:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8dcb17c47bb904ad9037fb2888f6ce033b57e59eebedd0559205878edd5a4af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10294501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5322b14e74827045caf1afc1a60189e92b09e08f53ff70e449716db1ddc93093`

```dockerfile
```

-	Layers:
	-	`sha256:f52ee5139dda3f49379b1df430aa5e6797a02aac8a956ea8c7703efd1a6013bd`  
		Last Modified: Wed, 13 Nov 2024 00:22:59 GMT  
		Size: 10.3 MB (10266783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ad52ae415a323ca8b9952b002341aa5767b09ca39369644b73c7f9ea1996a37`  
		Last Modified: Wed, 13 Nov 2024 00:22:59 GMT  
		Size: 27.7 KB (27718 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:64c2158e5220e9258651d1956d89487c2e8299d50f3a6a04ad47ae0d1bbdfdda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277294647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc35cc917ebe1aa89d007796b97e0ffead87f1f53bbf44558b4667bef89f889`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:9f9f8fa8b12064144bd5037b70d4d9ac4fcbcd94f2921feb1e017764a273f798`  
		Last Modified: Tue, 12 Nov 2024 00:58:23 GMT  
		Size: 47.9 MB (47938688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b034664a3d7aeeede4479f8aebfb2fff094119ae93ccf99e62d557e92b31f`  
		Last Modified: Tue, 12 Nov 2024 09:01:46 GMT  
		Size: 24.1 MB (24057883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404d777567f321c549501c18afd08de2ba33359f57a5f517f6d5cc81747dbfa`  
		Last Modified: Tue, 12 Nov 2024 23:32:38 GMT  
		Size: 63.5 MB (63473961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745112af4469f10811307e8f23c3f629471d32ec85be7f2aebfec0a1f84c067f`  
		Last Modified: Wed, 13 Nov 2024 03:31:04 GMT  
		Size: 68.9 MB (68874065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899e076c675a549e2d1bc5d05ac9fc56f919b55bb9ec6d441d414eb5acb3e0b`  
		Last Modified: Thu, 07 Nov 2024 03:03:52 GMT  
		Size: 72.9 MB (72949892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270a7782f4b7b26afb09051144d1ef582f5746f5b6d85338e2f65dc877d347dc`  
		Last Modified: Wed, 13 Nov 2024 03:31:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:18e14532eacd8828da2c5b6ee023b56963865bb67a92555376b244aa6deb626e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10157549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6c850a019f468d04e4885534f3b78741210ea3adf6a359ae133fda670c557f`

```dockerfile
```

-	Layers:
	-	`sha256:33ee560149d628705b95b74d4849114e04adcf8bac8d597ea3fa184abb9b6dfb`  
		Last Modified: Wed, 13 Nov 2024 03:31:03 GMT  
		Size: 10.1 MB (10129903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6721959a342dfbfd3b1f08225850079e8725d74990db2a872480d214273dedcd`  
		Last Modified: Wed, 13 Nov 2024 03:31:03 GMT  
		Size: 27.6 KB (27646 bytes)  
		MIME: application/vnd.in-toto+json

## `golang:1-bookworm`

```console
$ docker pull golang@sha256:1f001ad8c8d90281cd9d6e0ae4a40363039c148c503bcd483ff38c946b3d4f6d
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
$ docker pull golang@sha256:a92a5043f077814bc5a32f5c5e161c5bda773eab3b3b4c9484e5b47789445bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294509322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986f7450c3fab33798ea6f7d6b8d6e4d652e667eeb3b04aca92a927ffe0682a3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350fba2a5c2e7c67ddb0ca3e76d120485cda7acb86a84c32dc9f8dc53a65724f`  
		Last Modified: Thu, 07 Nov 2024 02:59:18 GMT  
		Size: 86.3 MB (86311360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323003b0d8ad8001283c9881b96c87e9fa38fb378aa4de93c4defd3899f30d2a`  
		Last Modified: Thu, 07 Nov 2024 02:59:17 GMT  
		Size: 70.7 MB (70668948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea7accc04c864a08b1ff8914425297da0a6b94ee05e2e8961f1d88dc86d2d82`  
		Last Modified: Thu, 07 Nov 2024 02:59:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4c017bad8658f1d638572a34bedfce3b11f03263bdc1e17c7170442663c78b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10349852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c0993f821452a6dda7a44b2f03a9b2c17ffcafbdd9594647e1d00b1203edba`

```dockerfile
```

-	Layers:
	-	`sha256:5c992632455b1e6657c546814c7d2d5a524006435c1d7a1b4fdd22bb0cd37020`  
		Last Modified: Thu, 07 Nov 2024 02:59:16 GMT  
		Size: 10.3 MB (10321994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:161dc14c5a2c002886c8d74de15c8b2a6b907ee5563cda4e52e428feff2f2ad5`  
		Last Modified: Thu, 07 Nov 2024 02:59:15 GMT  
		Size: 27.9 KB (27858 bytes)  
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
$ docker pull golang@sha256:9919051f194ee3ad085796904b416e6e41b887b62a478a67c5c779033e9b343b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274657835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2152a7e57a02708d70f493d88d4b4dd5e6b5b82d6466b5456346e297aa8105f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
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
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba3cc6e574320e30c42f84b70c8e03fff0393ea65f20833b10b3a8aa1415e1`  
		Last Modified: Sat, 19 Oct 2024 00:56:12 GMT  
		Size: 23.6 MB (23648020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d702889c46052954a44f8b6ab39510d9b55acfe4a180194a7cb475c90b2b76e`  
		Last Modified: Sat, 19 Oct 2024 02:08:09 GMT  
		Size: 63.3 MB (63284387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a36a8c8304278444a69b45df3237dd325d03c14c930d7ebbb98b5b9bb4f45a`  
		Last Modified: Sat, 19 Oct 2024 03:21:49 GMT  
		Size: 69.8 MB (69849953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f81694bc2d6f633d7ccbad361e1e6ae621631bf889fc11bc127c432c7d8965`  
		Last Modified: Thu, 07 Nov 2024 03:03:54 GMT  
		Size: 68.3 MB (68313700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265faaccb2573fb36bb2c9b2edbc85c31d9d6794b669f2c1c25c6dc27d8ed9ae`  
		Last Modified: Thu, 07 Nov 2024 03:03:46 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4badbcaf0c624c1598b3b5fb3683a299575b0eebe74bea325d29e3a34d514054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 KB (27569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989dcb9558cc066a66109cd070d684eea3dc5cf3cb2b749c6cdb49d3abb17797`

```dockerfile
```

-	Layers:
	-	`sha256:834cc1e133864e2fa068c0f0420af4c69220f80e84cd8dd2c76c0a237c06d2f9`  
		Last Modified: Thu, 07 Nov 2024 03:03:46 GMT  
		Size: 27.6 KB (27569 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:7a8d16d90b3c62575af4567a4a3173785bee0002ac9da041470376741d224129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310173087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df664674c0784cc561d7d39265ba05a185120b8ce7184d4082ba62ad2d89399b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
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
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823a3ab0dcc6f88db2bc0c18d80304ad0e6a3cad08984b6ce0a7abefd371d55`  
		Last Modified: Sat, 19 Oct 2024 00:56:54 GMT  
		Size: 25.7 MB (25705977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3666a280304f3727f745e818ab5e252dd98676495517a360e23f821dee0fa6`  
		Last Modified: Sat, 19 Oct 2024 04:07:03 GMT  
		Size: 69.8 MB (69825530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a384557667db09914e29d61cab511b9f6693736f0ea15422c1ec112462ab0eea`  
		Last Modified: Thu, 07 Nov 2024 03:00:09 GMT  
		Size: 90.3 MB (90257347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d45dcd888e3183671630e662953341e3111584ee0e6ca4f0d40e50580ea2de`  
		Last Modified: Thu, 07 Nov 2024 03:00:09 GMT  
		Size: 70.8 MB (70828478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5b5498e250bdc83df3436aef926945c06c948e950b8d1b6250c8acd4cb27af`  
		Last Modified: Thu, 07 Nov 2024 02:59:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:744a8104f8c175af265795efc18aa7dc0232599f4d6d2e805ecd5c166abe948a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10294459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3fb2c8a9496492cb462e48e8c462d3c9e7c1a039a79c2d68aa60b6db557e60`

```dockerfile
```

-	Layers:
	-	`sha256:c36cab9cc195149dec1ac0a26ff92ad4f3d6efa883617d20458e4f13e525ec79`  
		Last Modified: Thu, 07 Nov 2024 03:00:07 GMT  
		Size: 10.3 MB (10266711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e33614cd3a2570ed23c95604cc595d4407f2e172a6194453a8e9f0144d9ca978`  
		Last Modified: Thu, 07 Nov 2024 03:00:06 GMT  
		Size: 27.7 KB (27748 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:c9f730166fcb06321dd402805bdac958ff5f52801dab389d966ae01b56855a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277279420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c1569846971f4e3b7c9c3ea2a086bcdef236f0be9abd20ae9f0d0d78f91595`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
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
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a99db1e4eb0a57b7be4b1376a7fdf886d4118a6263595ad414d052eb69ee9b4`  
		Last Modified: Sat, 19 Oct 2024 03:46:26 GMT  
		Size: 63.5 MB (63494580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d172550621422ed97b2a593473b9a3a5fca6ccbc36c78ad400474bfe8c3ea4`  
		Last Modified: Thu, 07 Nov 2024 03:03:52 GMT  
		Size: 68.8 MB (68845945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899e076c675a549e2d1bc5d05ac9fc56f919b55bb9ec6d441d414eb5acb3e0b`  
		Last Modified: Thu, 07 Nov 2024 03:03:52 GMT  
		Size: 72.9 MB (72949892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b7326268d798cd34f6aea59a309e8315e60997c7095cd2b016c718144f266b`  
		Last Modified: Thu, 07 Nov 2024 03:03:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6e7c6e606e3a397cee2d0421c071a45bebd25378d622ec1f3dfdc28309ed6c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10157507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd60ba747a83497c47ee12592def4adb29d60febea4171d74ee2bc8f975f70f`

```dockerfile
```

-	Layers:
	-	`sha256:44454fb296ffb2290553e1fd2016747fc4a8e9bf2b53ccbff56abf49807ac384`  
		Last Modified: Thu, 07 Nov 2024 03:03:50 GMT  
		Size: 10.1 MB (10129831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82037daa83ae5926d2526007b1619ca42579fe20df9da2fa2072930353cb2dac`  
		Last Modified: Thu, 07 Nov 2024 03:03:49 GMT  
		Size: 27.7 KB (27676 bytes)  
		MIME: application/vnd.in-toto+json

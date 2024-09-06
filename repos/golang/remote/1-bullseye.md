## `golang:1-bullseye`

```console
$ docker pull golang@sha256:c6ed81d55e2a0d171bd483f89fb1cfd593f21092b2045e4698b7608d9e30e185
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

### `golang:1-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:e656c16bbd3beddfe901a478e44e6bc0fec632a0ef2f489e5b6fa0474dbc42e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285533348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ea70b079e76c9efa49930317e93b090c22bfa1928dcebc7683cc515c6e5a6b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:56 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 04 Sep 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:56:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d691dff6d17d00b0cbbc4772eb805d97e02504d89ea3e5857cb97c943b74462`  
		Last Modified: Wed, 04 Sep 2024 23:02:33 GMT  
		Size: 54.7 MB (54726023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59c79e79e165e729f8f8b749b6f9ef266e46e2eba378228d8de594d5c102320`  
		Last Modified: Thu, 05 Sep 2024 22:03:12 GMT  
		Size: 86.0 MB (85958156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bff916ab0c126c9d943f0c481a905f402e00f206a89248f257ef90beaabbd8`  
		Last Modified: Thu, 05 Sep 2024 22:02:55 GMT  
		Size: 74.0 MB (74003284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284aed4a7e09ad38f390ffb7487982766849ee04bbda3224d2fa3eca30e8a4d2`  
		Last Modified: Thu, 05 Sep 2024 22:03:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:75faf00d91b1ee641ec22e2bd3aaa7be26cfb604d5bad04664608dedd026567c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10281382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c306ce2e86e59cd767a69ffe11496c6102fc680631eadb0460274c794a07c8`

```dockerfile
```

-	Layers:
	-	`sha256:e9228afc17dc9ce6d0429383f6516023ec6f6f98a115250d209701d79dbeb776`  
		Last Modified: Thu, 05 Sep 2024 22:03:10 GMT  
		Size: 10.3 MB (10255034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca15eb0387a78521e7081498fdd23bc050227abc56881ec8c610cc9e34b55213`  
		Last Modified: Thu, 05 Sep 2024 22:03:10 GMT  
		Size: 26.3 KB (26348 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:6951a314f8134f3de569728bcb92d8717a79317e75f0e20486e1d8a120b1589b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252485569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8e9b30f54f7465a15929ed39f96c110452631d17aa2a7cef9864a43fade27c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:45 GMT
ADD file:7674761630f1c6dfdf95da576bd19dbfe7bc4d942d11d31eff2012ec8b2c7ff1 in / 
# Tue, 13 Aug 2024 00:57:45 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:25:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:26:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 17:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOLANG_VERSION=1.23.0
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOPATH=/go
# Tue, 13 Aug 2024 17:10:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 17:10:31 GMT
COPY /target/ / # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a986643b6b9d356e3c44ee35fdd352a1064e1fb2a1524c0627e84ba34207b8e2`  
		Last Modified: Tue, 13 Aug 2024 01:01:15 GMT  
		Size: 50.2 MB (50242333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8868560f8e978ee832f67027b7330376be350ffacd30a199b730c72d9550757`  
		Last Modified: Tue, 13 Aug 2024 01:33:28 GMT  
		Size: 14.9 MB (14879497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7deb3ed53b620f0871f5051050fe0d850fd52da94803425820e75bb7b8d4e2e`  
		Last Modified: Tue, 13 Aug 2024 01:33:45 GMT  
		Size: 50.4 MB (50357748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1643dd34ded149a805ac35a064b9b839f8d6c57bbd3669535881a455fcb86305`  
		Last Modified: Tue, 13 Aug 2024 11:31:56 GMT  
		Size: 64.9 MB (64878285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6363114f7204e8b9cd3cb47febe5a3082ffb85a82d8c47efb0021f3f9323f`  
		Last Modified: Wed, 14 Aug 2024 01:59:55 GMT  
		Size: 72.1 MB (72127549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fcc933875f5060f89baeae5b1b5c6954bbd9741d38d62160d6872f0494e5f53`  
		Last Modified: Wed, 14 Aug 2024 02:00:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:92d098e1fa4ad31f88bb74daa1f47777769cc63e759a8943bfd8ef73e7fbc4e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10088028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818e85a236e43efe77d115d88f63c7e4782f94590a9fdbda904e527a8c9ab9ca`

```dockerfile
```

-	Layers:
	-	`sha256:fb300a5eee3be36d736e405b680c9972932cf05e21a5878654dd502420a6e6a0`  
		Last Modified: Wed, 14 Aug 2024 02:00:50 GMT  
		Size: 10.1 MB (10061584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b44e2b0cb14c3663c8dda6e4596d82d4ef68cf3198eeeda36e22ac402ee094eb`  
		Last Modified: Wed, 14 Aug 2024 02:00:49 GMT  
		Size: 26.4 KB (26444 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:661020bd455033c8efbd31b18d91caf89eda92a1b4903833294b7579f2351a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276306080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee23abead1c0249335f60ec1cd515d67041e5422a1d8e1a6f3a07744824a624`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:59 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 04 Sep 2024 21:40:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:03:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf248fd698830ce7c74f07fb7ca6adac7bea55a16521e9e1f2afe06219e00f6`  
		Last Modified: Wed, 04 Sep 2024 22:08:56 GMT  
		Size: 15.7 MB (15749712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b216df41d3eb392b55b4bb8c654fe024d7c3d00404a7e105f494ef43990fad`  
		Last Modified: Wed, 04 Sep 2024 22:09:10 GMT  
		Size: 54.8 MB (54833449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6321cc2f68c817a276b509dea0b6abbcca8b3bfcab0c79b3d01cada5b1b80b5`  
		Last Modified: Thu, 05 Sep 2024 12:05:56 GMT  
		Size: 81.4 MB (81366514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a355a3cac949bed5cda9c62103ceb0f004727cedcd2a17d7c9836aea1a452fda`  
		Last Modified: Thu, 05 Sep 2024 22:09:14 GMT  
		Size: 70.6 MB (70624628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed4976d02ca444f35b6403a903999427f424aa36444e5603c1ff1bc22af6700`  
		Last Modified: Thu, 05 Sep 2024 22:10:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:4f6d506c8a682d6051756442bf313292ec96d860cd60facb25362e38ea3f947f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10283403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c60777c353c65da98e2f8a796b2d85b74c3a1e56f5310e4ff6bed1b25858e22`

```dockerfile
```

-	Layers:
	-	`sha256:c3806def360e481f3b13c6e489541c90716f26be4950696bc4dd0e18ad02702b`  
		Last Modified: Thu, 05 Sep 2024 22:10:02 GMT  
		Size: 10.3 MB (10256738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29f340f9885135bec417b8dcd5403898481a03fd7cbc901d2e01a8d813d59313`  
		Last Modified: Thu, 05 Sep 2024 22:10:02 GMT  
		Size: 26.7 KB (26665 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; 386

```console
$ docker pull golang@sha256:bdf984d9c3c96dc60d38fe619064ee290197a8f5c8b754c1abdd5737a1c80e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.6 MB (287613892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f7b716b82dfb5382698c6e433961f323d4a6feebac53f7d77d9597408bb0c1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:44 GMT
ADD file:1d8ae4e7067486ce0279b3d90aaecbc5973872ad64266d252bfa3fd5e4fc2e5f in / 
# Wed, 04 Sep 2024 22:44:45 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:14:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4533261556c046eefdf517bc6e06bc455b876caf2226aa504a13b5d66d250281`  
		Last Modified: Wed, 04 Sep 2024 23:21:18 GMT  
		Size: 16.3 MB (16268301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341d50e4bbed9704aae2147f28b4a07fc71b73539d282c37f60e183d38865daf`  
		Last Modified: Wed, 04 Sep 2024 23:21:37 GMT  
		Size: 56.0 MB (56030074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb19bd22eb032236bc88059ce72cf292a404816fed88728ea4d0070b90bd8146`  
		Last Modified: Thu, 05 Sep 2024 22:03:11 GMT  
		Size: 87.4 MB (87383008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead5944571d35e19fa81ca655e6b7753cdb3e37418aa683e0c2a9c169e5d7256`  
		Last Modified: Thu, 05 Sep 2024 22:02:55 GMT  
		Size: 71.9 MB (71856183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a080f9c22972c331e5b0c34f2a64de5c7be8cc89ac39b2fc7ac5f7a0bb162ac6`  
		Last Modified: Thu, 05 Sep 2024 22:03:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:b22f044df32bc4ff8c0fd6e87eb062812cff5edd8fddc2bea852e12bca1ad90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10271348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3242127ed9dd66eea14b945390a10d40072a5ebd10f46696bab3373304c6a`

```dockerfile
```

-	Layers:
	-	`sha256:9a8d29666a7080b7c6045c137336a7b834b35aa1a3eb323a1fab434d8ee50eea`  
		Last Modified: Thu, 05 Sep 2024 22:03:08 GMT  
		Size: 10.2 MB (10245032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f20a3f0cc11c6a8b31ec986e819f417f4950cb7264a3d12adee3c4426b03af21`  
		Last Modified: Thu, 05 Sep 2024 22:03:08 GMT  
		Size: 26.3 KB (26316 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; mips64le

```console
$ docker pull golang@sha256:1468af096d91b3dafb749a3c10ef72b83046e74a68d004199ef54ab76c200bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257690624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0741b846e48be2a654a2ba3cfcd1451c1c6a7fcbb63279a27f35243ba650a49a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:45 GMT
ADD file:6c103cf641951f38237d461bf13e5ba7a8b38776409e4443857a95928d972a64 in / 
# Tue, 13 Aug 2024 00:11:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:03:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fbfd53ead15e1f39becdee0e90a399fced0550dcbe1c27017a0256c390b08747`  
		Last Modified: Tue, 13 Aug 2024 00:23:13 GMT  
		Size: 53.3 MB (53310557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975486c9b8367654ca68daf3f98e4da57b660b9ac9788562fa218a38d9db4e6e`  
		Last Modified: Tue, 13 Aug 2024 01:34:35 GMT  
		Size: 15.7 MB (15734788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3b3474926636ee8b68ffaabc4b0327c4331cc3894af8f568c64d5f6f1d8594`  
		Last Modified: Tue, 13 Aug 2024 01:35:20 GMT  
		Size: 53.3 MB (53310999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8fde75c3c00cb4e30c6717cc43ea32f4e490fe7e8c4ace04e6c4ec24965684`  
		Last Modified: Thu, 15 Aug 2024 02:15:55 GMT  
		Size: 67.1 MB (67056360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f92ff5c1684aca058ae9537bdbaf5bafd344391c0d79677375775ca94fc2195`  
		Last Modified: Fri, 06 Sep 2024 01:28:00 GMT  
		Size: 68.3 MB (68277762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb403e658f936bbd581f42ea7c05cd17dc93167100c1f94b2346e121161efa7`  
		Last Modified: Fri, 06 Sep 2024 01:29:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:e2b99265f7cbd046dcd78ec2c25b04e32ea41398ad3ced39be177caca3c358b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fabfbeec41e42fce3a9ce52e978b1815623061d328ca2420a458cd13928eb1b7`

```dockerfile
```

-	Layers:
	-	`sha256:7d13c29a40fde5d47cf23733778be06c09419477648b1744332f076ecb6ac15e`  
		Last Modified: Fri, 06 Sep 2024 01:29:57 GMT  
		Size: 26.2 KB (26193 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; ppc64le

```console
$ docker pull golang@sha256:1b7850f98a494800879b29f08dd195bf63290369c3c07db8177b66019a78bb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285790620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49bde19d5a474bd487785e517f1b147f28086289d24f67908bf16a3cc2d10c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:03 GMT
ADD file:af2c25052aab46bab5ee70bf1b7f7c8d0339d147a2bd4daeb04ec25bd34e4799 in / 
# Wed, 04 Sep 2024 22:26:06 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:04:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a8e5e0425eb7845f41056f6e5fe36c228a23a602de31f39d88868def2b2bf980`  
		Last Modified: Wed, 04 Sep 2024 22:30:31 GMT  
		Size: 59.0 MB (58950090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e76b45808a7b15592738cc59f261bb4109d1d280c5fa410f157dd270ddbf8c9`  
		Last Modified: Wed, 04 Sep 2024 23:14:50 GMT  
		Size: 16.8 MB (16766250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb7a5e65d3cbab78e31accfce79b09855b78c5b547ef6a738d98e4678a2af87`  
		Last Modified: Wed, 04 Sep 2024 23:15:06 GMT  
		Size: 58.9 MB (58872541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6aeade1357aea929a692ab613b33965bc86d3534862ee5bcf5f1662f2cd9c42`  
		Last Modified: Thu, 05 Sep 2024 17:37:55 GMT  
		Size: 80.4 MB (80402602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e5b8a4bec9158fc0bc52aa7bb2055ac421fd36de9ea98898a7188751ff7da1`  
		Last Modified: Thu, 05 Sep 2024 23:28:18 GMT  
		Size: 70.8 MB (70798979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3ff45270fc9d9e2de4b6a32565322018ad40906f616d7b58e8ff675b83c7aa`  
		Last Modified: Thu, 05 Sep 2024 23:29:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:61313986069143f27bd85643a00bfa2a0a9df762c990ce66ec0c1699f90a90d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10247124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77809d65b11e2b1180ea4b5f712d434c5c5e1131a8b466551bd9af5c535efe8e`

```dockerfile
```

-	Layers:
	-	`sha256:ef499a2c3c83c19c5276b2a002c756242e14f1cd07d3b063272f2a7538217cc6`  
		Last Modified: Thu, 05 Sep 2024 23:29:40 GMT  
		Size: 10.2 MB (10220733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:631d8557a367fc14099a3d605bc990812477957adc13ad26c401177ed99e3c07`  
		Last Modified: Thu, 05 Sep 2024 23:29:39 GMT  
		Size: 26.4 KB (26391 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; s390x

```console
$ docker pull golang@sha256:d323eed8edfc8ae9ef2aa723913c926497bb627cc2d123489608ef094ab7fa35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261597301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319b9e050d33ad6fb9486ef032599e61728ba907964ccf8f0f6cf91ee1c7c05a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:51 GMT
ADD file:993091e64467ec0ea9bcecdd744da64284d459b933863322bd011dd2111f47c1 in / 
# Tue, 13 Aug 2024 00:42:53 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:17:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 17:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOLANG_VERSION=1.23.0
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOPATH=/go
# Tue, 13 Aug 2024 17:10:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 17:10:31 GMT
COPY /target/ / # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9c1a2da0ad07de8657187bee6e4fad1ff817bafdbac14fb77a3953cd7f50038c`  
		Last Modified: Tue, 13 Aug 2024 00:47:43 GMT  
		Size: 53.3 MB (53324089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c695efccb58000e04eb154deca02ce22ea52fd05ee4246281c66bb7a42d20a96`  
		Last Modified: Tue, 13 Aug 2024 01:25:32 GMT  
		Size: 15.6 MB (15641934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3f87ffa253b4cb357637ad56494facf5bf533f6fd3bdf78f1066c6fb0fb23`  
		Last Modified: Tue, 13 Aug 2024 01:25:44 GMT  
		Size: 54.1 MB (54075217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b221ab5055e6a918a4e1c366fec50c506c9321c39753b3200e0078544b9667`  
		Last Modified: Tue, 13 Aug 2024 23:09:43 GMT  
		Size: 65.7 MB (65656693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d766dfa346f9569deddaa862bfcc6c453c61295fa0688cff4cf096f917447678`  
		Last Modified: Tue, 13 Aug 2024 23:07:38 GMT  
		Size: 72.9 MB (72899210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0793901093e9e38c2f74f79a13b9277ce352968977f2131779837101cc21045f`  
		Last Modified: Tue, 13 Aug 2024 23:09:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:b48ac46c888809fe774f709b8bb05c3abc1c8d05a4fd676dc773993073740e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10110537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a471a3079c91aafd5c438a1e628106f1d07881794efe7767573f0b8b6ccff74`

```dockerfile
```

-	Layers:
	-	`sha256:2928b9b860349f01f75cc72e000fbc931bb17965eefcc42350bd78992f6da559`  
		Last Modified: Tue, 13 Aug 2024 23:09:42 GMT  
		Size: 10.1 MB (10084188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd6ea58e109686b37ad1a4e2acadb47dbcc62fb8622918d75f5eac7c78606b91`  
		Last Modified: Tue, 13 Aug 2024 23:09:42 GMT  
		Size: 26.3 KB (26349 bytes)  
		MIME: application/vnd.in-toto+json

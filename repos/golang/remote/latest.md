## `golang:latest`

```console
$ docker pull golang@sha256:75b7aad2425f1426d09326c4cd99e8fa93e0e08c8aec669213a51e511cacb38d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `golang:latest` - linux; amd64

```console
$ docker pull golang@sha256:4304d944c421bb279ad1faada14d03ac7e7edca61793d2f6a7ad94681c457887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 MB (299313703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5905f95343e84d1f8f14aff8f8b83747fb39ea0e0fad52a9d14cf41860295fff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 May 2024 16:32:49 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 07 May 2024 16:32:49 GMT
CMD ["bash"]
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6582c62583ef22717db8d306b1d6a0c288089ff607d9c0d2d81c4f8973cbfee3`  
		Last Modified: Tue, 14 May 2024 03:04:25 GMT  
		Size: 64.1 MB (64142371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d74711819e4c0c72946b3c61acc621af6c65bcb4a17d8730c0eee81f0190fc8`  
		Last Modified: Tue, 14 May 2024 22:58:08 GMT  
		Size: 92.2 MB (92201989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca4369267475245bb0e6217f0fdba040890f26fdef9b65cac11a545ab2db160`  
		Last Modified: Tue, 14 May 2024 22:58:08 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a583c4d6eaf816b7019318d9d5dc7917a08d1e10ba961226c2e9a90bc7aff277`  
		Last Modified: Tue, 14 May 2024 22:58:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:7180d60eb15287c8a73a34470f9def2ff8439704c06a911ce08f76257cb92a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10240931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f3bd98ae8299b720f8076f4211788ca48b1ed1185ef0b5f44a41c6b6f244fd`

```dockerfile
```

-	Layers:
	-	`sha256:e9ad3320397630e57235d2adad02378c7ec5ae43f0aed913053b0ad783bff317`  
		Last Modified: Tue, 14 May 2024 22:58:06 GMT  
		Size: 10.2 MB (10214844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcbae46239b810e009f64e64d0d628f6fa14cb7548f9b49d310b08cf2469880b`  
		Last Modified: Tue, 14 May 2024 22:58:06 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm variant v7

```console
$ docker pull golang@sha256:720d505001a7e0191a7655319f71ebba9b35a7986672a1e88b2ea0af3f06e1f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260335800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132c8d0370ebb7aa71a0915997e6dfa7a195cd93806797fcbdc2126522b93264`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:08:35 GMT
ADD file:1e106a38a0e44ca74d4d29c6d797780e7a29ffe249e473c48ee2aea553fc013b in / 
# Tue, 14 May 2024 01:08:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:35:47 GMT
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
	-	`sha256:dfc3b4ca62816a9cbf2bdfbdd78bf692a522e7f48a280492b9f87d55b2f4aa2e`  
		Last Modified: Tue, 14 May 2024 01:12:21 GMT  
		Size: 45.2 MB (45174745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641d6443415d538c3bf0e0d6ecc0f6b7603b4caf6c79708d0670bc082e9721c5`  
		Last Modified: Tue, 14 May 2024 01:46:47 GMT  
		Size: 22.0 MB (21953893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94dd085f2eef9c35615ce8d6f2e7b6340a6bcadb37fe8fd6698911eab87e371c`  
		Last Modified: Tue, 14 May 2024 01:47:09 GMT  
		Size: 59.2 MB (59217124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e6c13ed95293dfbc4fed7d4ddc34c72dc89e1934b798a96c4f0d2e90f3dddf`  
		Last Modified: Tue, 14 May 2024 10:27:20 GMT  
		Size: 66.3 MB (66274794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1603d52c48bdbe91aadcd6caa0a4004a094ebcedc5c97b4261c71d11453b37a`  
		Last Modified: Tue, 14 May 2024 10:27:25 GMT  
		Size: 67.7 MB (67715037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c7956b2fe2ece0221430cb3e28e64540d134c668ec168fa950d3410ad03d71`  
		Last Modified: Tue, 14 May 2024 10:27:12 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:1a50c4741a9b2a90f6951ed95c4b10383dee03b283419a6916e6af28194e719b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289927744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c4ada891c275bb2e6a642182af6416a46f5de81d01e2e7f09e07f1088c1074`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:44:43 GMT
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
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15856ca26414127b85cee6d10acbc4cee6eba9070f3f5a04b9cc72ce95abfa7f`  
		Last Modified: Tue, 14 May 2024 01:52:50 GMT  
		Size: 23.6 MB (23586610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ed4c12791345d3f20f66024e1f22275ce507868c508509b83dcf231b1c9adc`  
		Last Modified: Tue, 14 May 2024 01:53:09 GMT  
		Size: 64.0 MB (63994370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127d8270fe84eb58853be2e1c5cfab3174223af6218d6a6db28d334d571268bd`  
		Last Modified: Tue, 14 May 2024 13:50:21 GMT  
		Size: 86.5 MB (86461081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2ec01a76913a047201f0ffa809612c4a8c1ee07ac42e04d3cc65d835a13f5f`  
		Last Modified: Tue, 14 May 2024 13:50:20 GMT  
		Size: 66.3 MB (66272089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d44db2fe8e5e6995cf822eed9f11008b18e82189910c164ecaff18c2255466`  
		Last Modified: Tue, 14 May 2024 13:50:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; 386

```console
$ docker pull golang@sha256:1535d733254ef88f69a207fffa11a2c776fa3ca3a529413e4d794fe4e67ef80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298434474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39759c2c56af9b5a04f8a5e8fc748a02a478dd67c16b8d49a7aa24b06ccc4336`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 May 2024 16:32:49 GMT
ADD file:35709674a3b845511a896af16ea37a6022e7d48992d3198d0760c0c3208fe4ed in / 
# Tue, 07 May 2024 16:32:49 GMT
CMD ["bash"]
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:4f2f2f6205661e555e772749ae7fd294fb04fc0d06cbc67a50a11fbb4ef44242`  
		Last Modified: Tue, 14 May 2024 00:51:31 GMT  
		Size: 50.6 MB (50602424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d849fa81a6965e2bbc8dd9af462f55a46b59aeb701fb0a26992522fd43ce5c03`  
		Last Modified: Tue, 14 May 2024 09:13:04 GMT  
		Size: 24.9 MB (24888551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6250e2e75fd4f1cdc533096df2c601817950e8c3f1096f46dfeea2b609cee`  
		Last Modified: Tue, 14 May 2024 09:13:29 GMT  
		Size: 66.0 MB (65988940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50024ded5f9971d17cf21176d8b557107193cdeed0358bf8ac3f71a87d8542db`  
		Last Modified: Tue, 14 May 2024 22:57:31 GMT  
		Size: 89.6 MB (89611084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6fea609dd954ccc4782268fc1d98a32902bab08a8f911773fad5247659a41d`  
		Last Modified: Tue, 14 May 2024 22:57:31 GMT  
		Size: 67.3 MB (67343318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b48a043c8955b2ddf24e0856c3b40103897ae67a1a40b934b8f22f51a8983a3`  
		Last Modified: Tue, 14 May 2024 22:57:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:c0fea66d4acd827e9a81de8996b4ef5f06381ba68ad24e6dd2cee528d45ba9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10221421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bfee17ce1816d53e465c37e36f544eb8da42e81b84be8989bc03688e51d71f7`

```dockerfile
```

-	Layers:
	-	`sha256:30110a83d280f3de89b355f74d7c9fd92f652b2ce7df0a0cd1eef977fd8ff438`  
		Last Modified: Tue, 14 May 2024 22:57:29 GMT  
		Size: 10.2 MB (10195387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:793af388b1a0609d49b6fbb60092f60b597e72bdabc828ebe2f464d9f322e0ca`  
		Last Modified: Tue, 14 May 2024 22:57:29 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; mips64le

```console
$ docker pull golang@sha256:80b202183c3d4de4d1e3c1c94ec95b67740ccbf15345438a3ac73bad4ffa1c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269881962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb3fb827650a4e362ce26b5d7bc9cd0c5f33e2776549431087be9f0771aeda7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:10:23 GMT
ADD file:95717416297a85e0b38d171b3bf8d2b48e941bd725e476ee4f88033fed4ffee2 in / 
# Tue, 14 May 2024 01:10:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 10:59:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:01:40 GMT
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
	-	`sha256:0fd7e383bbed45ca14b36b1e22f1591a0b2bddc34b2b6e2b34d4cd54b528e75f`  
		Last Modified: Tue, 14 May 2024 01:21:36 GMT  
		Size: 49.6 MB (49582338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ce1d8a69726b5d3330ae01a246efbb18fb60d54fb0d08b741a960e37d8b115`  
		Last Modified: Tue, 14 May 2024 11:37:05 GMT  
		Size: 23.4 MB (23438164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3667485c8dcf18ff23740eff9103874ec0aba9a4d45bade2f98f9f85fe0f63`  
		Last Modified: Tue, 14 May 2024 11:37:57 GMT  
		Size: 63.0 MB (62968511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95cd4a21351ea2bddc747eb17e023a8f507d549a7dfcf8656edd9766897ac1fc`  
		Last Modified: Tue, 14 May 2024 17:26:33 GMT  
		Size: 69.8 MB (69779283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0571a9b674b272a4406b310dfe31520bee98346ec3ec27c000ab2edfd58e1d`  
		Last Modified: Tue, 14 May 2024 17:26:39 GMT  
		Size: 64.1 MB (64113508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961975b8ca6d7ccfedc6eca9238b64f8a0d8fc1e2af6f10f673b5954fcdba889`  
		Last Modified: Tue, 14 May 2024 17:25:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:9133d33f5a9b4fd41768df6ae0add2e5646af87ea4ea2838248075efca5b9998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305480869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f48e9277a6c18334bf569d9465a2284e4b4abbaf57b91d71a24fd7e4efdf78`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 May 2024 16:32:49 GMT
ADD file:fdb5c89e2970bd3b21a7b4e39491c1719b957f54babefd52ad455ea72a77bd3f in / 
# Tue, 07 May 2024 16:32:49 GMT
CMD ["bash"]
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:9027b64136d8b1ece1ad24cca3199e496689a33f47b8d112dbdd112c682e665f`  
		Last Modified: Tue, 14 May 2024 01:23:40 GMT  
		Size: 53.6 MB (53579748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e147daa0a988c77940b565d177a661a73270a0e821c65283b9e531ae38ebc4`  
		Last Modified: Tue, 14 May 2024 07:10:25 GMT  
		Size: 25.7 MB (25699676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88d9ff0405bb000dedfa15a3a34739370c3daa10367599bff02a57fd19a3564`  
		Last Modified: Tue, 14 May 2024 07:10:47 GMT  
		Size: 69.6 MB (69584088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5afd4d08d4f3ef4aa04e2f23a8cff9d41f980dbbf80bda32d92064a3694ca84`  
		Last Modified: Wed, 15 May 2024 04:44:02 GMT  
		Size: 90.2 MB (90187142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a09e6cada02540e54f2e6e8c59f80c9960dc5c4559a3d96a1cc4bcca469ff9e`  
		Last Modified: Wed, 15 May 2024 04:44:01 GMT  
		Size: 66.4 MB (66430056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a32bbb4304057158e827e6ab9b536bc5a3361ae020d62ed3ca270dc1c63219`  
		Last Modified: Wed, 15 May 2024 04:43:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:6a90b350f6bf898069c361709fe98216212a5642ead00fc7d8c9ff24cb07a9ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10213995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04293d05e7a6ee1e706ba51f09a832c46c7e156a9766912884a31ddf43a0bd8e`

```dockerfile
```

-	Layers:
	-	`sha256:f80b4f3ab9f9f40399955a13690ac76b2b710c57e3a83704126b3d7d4dc908a2`  
		Last Modified: Wed, 15 May 2024 04:43:59 GMT  
		Size: 10.2 MB (10187842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e000c1e93343d7ba6283a705891277a536d702039ef2bb6619a206c5e2ae1641`  
		Last Modified: Wed, 15 May 2024 04:43:58 GMT  
		Size: 26.2 KB (26153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; s390x

```console
$ docker pull golang@sha256:4a2cdadb093177bbfb267b6531c755d00c7c0eb20d7fc1e37260752b74026e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272293736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62096b589bdf12ab93d72441b78ddaaeb3417b8954910d16fe0a76cca5c56ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 May 2024 16:32:49 GMT
ADD file:d24c16f113416f94273813df324360fe934245f0f7f2973b6def2799e5605f1f in / 
# Tue, 07 May 2024 16:32:49 GMT
CMD ["bash"]
# Tue, 07 May 2024 16:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:b9285660d64168cd1c05bdfee5186da3634a289a06300d8ea12e57df80e4648b`  
		Last Modified: Tue, 14 May 2024 00:47:17 GMT  
		Size: 47.9 MB (47942190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c304d55d9ae47fcef54a6044634995ffbdbd5e4d3e409198127615b4043fa8b`  
		Last Modified: Tue, 14 May 2024 01:29:23 GMT  
		Size: 24.0 MB (24046857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943219d44d0b66fa3c53413ccd4b689951925725722eba1e47eec984778d3640`  
		Last Modified: Tue, 14 May 2024 01:29:39 GMT  
		Size: 63.1 MB (63130182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131cd7d70adad6cd0f95fe77b15ff99bb76dee88efb21b7fe02b23a466d7bbb2`  
		Last Modified: Wed, 15 May 2024 02:44:07 GMT  
		Size: 68.8 MB (68775272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b913ee17a483cc427f632db9240a13b45ee66ca5d56d622dcfedef41eaa6cd`  
		Last Modified: Wed, 15 May 2024 02:44:08 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0814680be42cb8e2614113b11c38aff02993494383e485194506a95737798d9`  
		Last Modified: Wed, 15 May 2024 02:44:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:5f7307815a43a2cebbb9989b4b60deea77bc4c596246ed5787b1ce21548693b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10077899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ace4f979b6706d0819c0455f0de92e6a81bb176c4519c684a34dd91e05b7b3`

```dockerfile
```

-	Layers:
	-	`sha256:1257b995bd16b209012474fc06afa0be7b70ad1a87b138a9d00fafed9d6f075d`  
		Last Modified: Wed, 15 May 2024 02:44:06 GMT  
		Size: 10.1 MB (10051813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:722ac55233e319430c01c73fac4beb87fca2e6108c8e39266ed7b578af1f21e9`  
		Last Modified: Wed, 15 May 2024 02:44:06 GMT  
		Size: 26.1 KB (26086 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - windows version 10.0.20348.2402; amd64

```console
$ docker pull golang@sha256:a3d3d5e7141926f91d103d008d92a93c0f320c25842f9c37e04fb12d3ec20bb5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2097003327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13264e3b904e30ac81957f961fd0122e92afbd01f659e78eddf1e5b5be79850`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 14 May 2024 22:57:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 May 2024 22:57:33 GMT
ENV GIT_VERSION=2.23.0
# Tue, 14 May 2024 22:57:34 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 14 May 2024 22:57:34 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 14 May 2024 22:57:35 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 14 May 2024 22:58:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 14 May 2024 22:58:56 GMT
ENV GOPATH=C:\go
# Tue, 14 May 2024 22:59:02 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 May 2024 22:59:02 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 14 May 2024 23:01:07 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 May 2024 23:01:08 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add3ab9f691bcf2bbfcbe5e76392dc02ab6de944e5bc7830e0f8242960100b09`  
		Last Modified: Tue, 14 May 2024 23:01:15 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2465ac2fc7eb2599c3725a241376beccc3177f7d3711da533bd21ec9953f77b`  
		Last Modified: Tue, 14 May 2024 23:01:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e887c31edba2a499abd1603a206983dd757500807ec60647403046c8103cba5`  
		Last Modified: Tue, 14 May 2024 23:01:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad955bd31bac9f3b32b74e139c1bef15bf34fe4a1f818a3070ede0077197872e`  
		Last Modified: Tue, 14 May 2024 23:01:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0448fa2ab6dc2a8d2b5279b5cc93d87ccb671cec27fe62ac3fdc3673bdea1d`  
		Last Modified: Tue, 14 May 2024 23:01:12 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a253e9ffea11b0c9dc0f74a8a2af6cd761cb9429f9b5fba0d09f3adccce640`  
		Last Modified: Tue, 14 May 2024 23:01:15 GMT  
		Size: 25.6 MB (25585759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3bf77e7b98f60483e7faf2d63af0249ee633a8ea9ca74d1ec1d8ecc5262677`  
		Last Modified: Tue, 14 May 2024 23:01:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e57062ceb81f22a01ac093d7dd60cfeaa7ae3d018dbd89f8439dacb243bb21`  
		Last Modified: Tue, 14 May 2024 23:01:11 GMT  
		Size: 314.2 KB (314187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafa7ab5d96fd306848bc6649eb24d761b01a41ed4916a73ca2f22a2e5b47923`  
		Last Modified: Tue, 14 May 2024 23:01:11 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7f41ef29929b59d9abf24c5b147aaa4f13bf7172f13cc008ec97478dbfe99c`  
		Last Modified: Tue, 14 May 2024 23:01:21 GMT  
		Size: 71.7 MB (71719233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163640c2ccb590698fd28cd0f260099b374e5a618d9a7a0f6719e4b73cd0f62c`  
		Last Modified: Tue, 14 May 2024 23:01:11 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.17763.5696; amd64

```console
$ docker pull golang@sha256:e6417857a0a8bd37d7c2ee9312872dd4c8e04970a9cbfed5b4cfc9dbe2fb1d4d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262241679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb286806701fdeaffe44e139681aeded790307f9a464257977fcc4167cdc0be2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 14 May 2024 22:57:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 May 2024 22:57:12 GMT
ENV GIT_VERSION=2.23.0
# Tue, 14 May 2024 22:57:13 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 14 May 2024 22:57:13 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 14 May 2024 22:57:14 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 14 May 2024 22:59:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 14 May 2024 22:59:29 GMT
ENV GOPATH=C:\go
# Tue, 14 May 2024 22:59:51 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 May 2024 22:59:52 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 14 May 2024 23:01:49 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 May 2024 23:01:50 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae1e8d4045a7fe8848974080a09ad979a6af938d1ffce3a9ad7a9e0dce68d99`  
		Last Modified: Tue, 14 May 2024 23:01:59 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644b4499052e4ac1dd0778e508c76735c13d2e76ec3bf63c02cfe5c363fa80e5`  
		Last Modified: Tue, 14 May 2024 23:01:59 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6369e7ac02ad31dba4be695e60103912c2975d0f103439bbaca973a10affc1e`  
		Last Modified: Tue, 14 May 2024 23:01:57 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc36279f867940e9e6ce2bfe94f5ac048481e350091b3ea09c05b10b114d1ae7`  
		Last Modified: Tue, 14 May 2024 23:01:57 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a325da50d8ba6f4dc9934b7ffa1b56e9a94025314510a2510f720cb9f36d0cbb`  
		Last Modified: Tue, 14 May 2024 23:01:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c053f486a18509fc34b5ba760d6818d9ca0eb05285382d296179ba4cfa897d1`  
		Last Modified: Tue, 14 May 2024 23:01:59 GMT  
		Size: 25.6 MB (25595570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b261082871772fc2120d1f1da8b6e86fd7ab4d37337ffc57c9794a23e97c1ae7`  
		Last Modified: Tue, 14 May 2024 23:01:55 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2235757b95f4d8041e30c3ad7b1d348c899ac633ae8ec4742ad5f01d788cdb`  
		Last Modified: Tue, 14 May 2024 23:01:55 GMT  
		Size: 354.9 KB (354940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e22d5cfec34a42f9608ad159f489cc8de9a70ad69fb80ede57e796d5118569`  
		Last Modified: Tue, 14 May 2024 23:01:55 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6703351aa9c36d4ba8505665bfa059c6bd9210320dbf594a7f9fdb5b14b30a1`  
		Last Modified: Tue, 14 May 2024 23:02:06 GMT  
		Size: 71.9 MB (71852576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c685a97ec0079874c98d9b58a56fdbed5d829607efb3518675ec748275ea80`  
		Last Modified: Tue, 14 May 2024 23:01:55 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

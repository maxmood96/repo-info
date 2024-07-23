## `golang:bullseye`

```console
$ docker pull golang@sha256:afd20a4454c06215a7692f856c2891ded914684091fdcd207040bcef91ece169
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
$ docker pull golang@sha256:fac64f60c927f6546042f673ffafdbf3fd6fbaf6a675815049c33aa77fc5cc3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280741780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba1b93ce143a994b265698647c3b8223774c6b02f25f98cb63182d55cf7b040`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 19:33:45 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Tue, 02 Jul 2024 19:33:45 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8ed7043ae24342affc9e27ba2f362a3d02c164d6f2cc7b837f33b475f4ef54`  
		Last Modified: Tue, 23 Jul 2024 06:14:32 GMT  
		Size: 54.6 MB (54588538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a97df9b72d4e3166a839a6881c38b6901f1dc07739c91d175e657f32d85ec05`  
		Last Modified: Tue, 23 Jul 2024 07:20:16 GMT  
		Size: 86.0 MB (85952127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a2f51ff3dde07bfa1ce35b5597b2d97295e64a461d98e696feda7b25a6dc5f`  
		Last Modified: Tue, 02 Jul 2024 22:06:15 GMT  
		Size: 69.4 MB (69352095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e10701146c7a1534ffadb6fd6d0d4ac3a9af23b7ddd287537668b1284701a1a`  
		Last Modified: Tue, 23 Jul 2024 07:20:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:8616fc5635d6cf3ca2f0c7937994e7a69edf71bb242c02e44357eab3396f80e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940d05495db1ed9cc5f986ab782df29e853728619acd7c236eabcbac8a51f074`

```dockerfile
```

-	Layers:
	-	`sha256:8f15e1c9deeb34ea0f43a9308f40ecd705f991f3e189179d379889e3a6a41a86`  
		Last Modified: Tue, 23 Jul 2024 07:20:13 GMT  
		Size: 26.1 KB (26130 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:97b06871feaa8b945b71ba1cacfe0bcbdd9490d6696f0c24da1e0fe7424f7a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248071083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d23779475460609a4103fdcba8c4d388e0c6d9a53a13fb5a9431e4af4c0a009`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 19:33:45 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 02 Jul 2024 19:33:45 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a61d577d5393ca0b5e52e6cbd75569b7d9e9b50cb27f783d5482f5f97240ba0`  
		Last Modified: Tue, 23 Jul 2024 03:48:23 GMT  
		Size: 14.9 MB (14879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6354534da26fdc193140968c5b8a059bd98e1fc05e33deacad3b97f257fd35f`  
		Last Modified: Tue, 23 Jul 2024 03:48:44 GMT  
		Size: 50.4 MB (50357798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a326ae1bc806aa8e48551aab4b30e38feaa815656801113a43931288c52965`  
		Last Modified: Tue, 23 Jul 2024 17:14:10 GMT  
		Size: 64.9 MB (64874215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1377363fadc0bb3eb9a3cd846c096d02c646b0f4af9bef4893106284c049e37`  
		Last Modified: Wed, 03 Jul 2024 02:23:25 GMT  
		Size: 67.7 MB (67716891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7244f814405a2008d3437473af9127afc5ea0c6ba3bac175ec4c4ffcbd18d8`  
		Last Modified: Tue, 23 Jul 2024 17:14:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:f5d72578d5dfc3d67035e9f1c2e9b256be885d3115bd929bd31892a14678d4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788a3655c168d2ce32455878ca988c1c6f3e87ddad7fd0a737725727b152b650`

```dockerfile
```

-	Layers:
	-	`sha256:ddd2d96f9eae5fcebf2b5c6bc793831e9fa7700a462c6a0ae10e4938076769b0`  
		Last Modified: Tue, 23 Jul 2024 17:14:08 GMT  
		Size: 26.2 KB (26226 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:2adec72cd75cedccd16c83e6949615067ea5a3e2da918d8ae61b71331609a16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271811970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6513cf712d4b0ca60d0a7143e95b14af3c8002ef747fd0e9c7a2a8c657901023`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 19:33:45 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 02 Jul 2024 19:33:45 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c27a83c76abd51a72277b6a74eb7f88e560054e0d04383f64e2886877a20dd5`  
		Last Modified: Tue, 23 Jul 2024 08:11:04 GMT  
		Size: 15.7 MB (15749501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac540a55631c4cba93c7e4e4bf634300076d45e71db5f34f3c0d770eb826303`  
		Last Modified: Tue, 23 Jul 2024 08:11:17 GMT  
		Size: 54.7 MB (54694822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f20208c04818358748e86aa3eeaa63ebae96d2d61835170ecabd8216d348f2`  
		Last Modified: Tue, 23 Jul 2024 17:33:42 GMT  
		Size: 81.4 MB (81365278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad54470edeaca3376e9010d6ee8ae76847ce9900d3bfcdf32fc98cfd6fc2fa26`  
		Last Modified: Wed, 03 Jul 2024 01:41:58 GMT  
		Size: 66.3 MB (66272226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3660b7e32c101717a5523f3f715109a81cae5de0d7527c37b70f95b4b01a1b`  
		Last Modified: Tue, 23 Jul 2024 17:33:40 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:b7068bfad71c4b34aee699996990447fd65967dea8e4a1d0f1a4829cdbfa826e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5cea4ab7a24bc0edd4fd974b42592049b740254816a936526be9aa6f3745e08`

```dockerfile
```

-	Layers:
	-	`sha256:b43623a7ba7c6a443ec4849a26701ed270d73b8c72fa7cad65240bee7d884a7d`  
		Last Modified: Tue, 23 Jul 2024 17:33:40 GMT  
		Size: 26.4 KB (26445 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; 386

```console
$ docker pull golang@sha256:7e985446939a061ee6f88c35deabc852b2bc89d88e1aeb6958394f7b02c7474a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282987878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1917a861042f799078f2aff025daa742f830aae03ff8e85e05cd19c8e001347a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 19:33:45 GMT
ADD file:d1f79afb47e16fbf87d0a90342c567c752e14b1bf325fa45d6de69ea871b26df in / 
# Tue, 02 Jul 2024 19:33:45 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:35a8dcedb97fd8133fbcd18694f30c60eebc7e4f268630ab7b35eefe40254457`  
		Last Modified: Tue, 23 Jul 2024 03:58:11 GMT  
		Size: 56.1 MB (56074170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4dc1000d9e0251c16eaa821d62c15a6b192ccf2a5a7ca1f418356c9510042e`  
		Last Modified: Tue, 23 Jul 2024 04:50:03 GMT  
		Size: 16.3 MB (16267809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb2358914d635fc6784c6b2db8c1b20149653f26b9311bf6d676476a452297f`  
		Last Modified: Tue, 23 Jul 2024 04:50:23 GMT  
		Size: 55.9 MB (55927780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a459c7e2b10a3812b09f7d96961efb25eac6444c69bba1635c83f0dcef0019a`  
		Last Modified: Tue, 23 Jul 2024 06:14:45 GMT  
		Size: 87.4 MB (87376605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b75921c461b2ae6d1ff16df768b5e8ff34e9b73cf9704174903aa4e8c76f79`  
		Last Modified: Tue, 02 Jul 2024 22:06:19 GMT  
		Size: 67.3 MB (67341356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a920d68db5a6325a82fd4a6a19e8f7752f302ec66c6c3dae14549069e01fbf28`  
		Last Modified: Tue, 23 Jul 2024 06:14:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:0a12c36188ace7be50b7f14b59ee3a0d5430240855fe2369a5e7279fc7e35699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523fcf1c0890bdcf7c52110093f568538312664c11aac9f02c471a2ad435ba99`

```dockerfile
```

-	Layers:
	-	`sha256:f8e50d7835415d99092157f8fd557347cd120e919d3f9bee6b6e3646e525ee0c`  
		Last Modified: Tue, 23 Jul 2024 06:14:43 GMT  
		Size: 26.1 KB (26097 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; mips64le

```console
$ docker pull golang@sha256:d46cb99a7832e2ac478cf38f9c6e0844e615b0befb650ea18cddfa57f254e658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253501580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee80ff34e250d3cd96e7bcd8ec3f4028b66be2936e7fa63d651c86b1cecf6329`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:58 GMT
ADD file:c27c9e3b89ea2f05df44728fc1fc46f994aa335600846cab7240fdd415afec7a in / 
# Tue, 02 Jul 2024 01:19:04 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:03:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:05:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47b1b1e48b458e7bb52034561a02c3a9df945540ee55d2b8112f6501aaad6d66`  
		Last Modified: Tue, 02 Jul 2024 01:30:13 GMT  
		Size: 53.3 MB (53306204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca902fb3ff705493024175dfa7b750ecd6b69939807e1032182d84553f4e2b8e`  
		Last Modified: Tue, 02 Jul 2024 02:32:52 GMT  
		Size: 15.7 MB (15734714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b25e341950d66380e7def2b99a1ad6804e2693911e88a6f3fb36c897514564`  
		Last Modified: Tue, 02 Jul 2024 02:33:35 GMT  
		Size: 53.3 MB (53311036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd721a610e0b2f3450f36a27af20a3f0098e5f37a824bc51f2ee49add82dba71`  
		Last Modified: Wed, 03 Jul 2024 23:29:18 GMT  
		Size: 67.0 MB (67026355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fcaebbd35ab2c899d9cd314218438d9bc23d7a6b5309c43bb0d51d8902f10a`  
		Last Modified: Wed, 03 Jul 2024 23:32:17 GMT  
		Size: 64.1 MB (64123113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44676aa02326835e5e95216cf936db25172e3bdd1d5e9f061c8a2204267b1917`  
		Last Modified: Wed, 03 Jul 2024 23:34:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:f13668ec56314910d4fc748134a3768aaadb678a60eacbe63401f5ba77d5faf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5f4e11925008fe043f42eb16a390c6b0c8b6313bf8fed5a143a62f3b5b9cdb`

```dockerfile
```

-	Layers:
	-	`sha256:570bc9af21f52792d03d34ad4d121823ba3fa1779a09ac2a0dc95fe9422b8a52`  
		Last Modified: Wed, 03 Jul 2024 23:34:05 GMT  
		Size: 26.2 KB (26192 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; ppc64le

```console
$ docker pull golang@sha256:1fad21613b2565b74593ec164f7f514f725299217e0a359f9b399b1f8fbf614c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281442716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a04b805ced0e5d53ea3046444cdb79ab44bb5622dd67148dd73e5a7e368c8e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 19:33:45 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 02 Jul 2024 19:33:45 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89f3ec0749e802be2768d4d8d990f300a55cd418831db42ee374e4bb81ab0a3`  
		Last Modified: Tue, 23 Jul 2024 02:43:09 GMT  
		Size: 16.8 MB (16765814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3543cad9c41f9c9127d1adde535bc13ac5b446330727c5083aafa4b8d005c62`  
		Last Modified: Tue, 23 Jul 2024 02:43:26 GMT  
		Size: 58.9 MB (58872667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbc79dccac4cda5ab4a5e54de747c10a433f7b25e8b9ef9221a0808ea15fad0`  
		Last Modified: Tue, 23 Jul 2024 16:34:40 GMT  
		Size: 80.4 MB (80399956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5442a44a1d407a5a3d1cba7a7a9b8820f3afe463e19c35ae36202ab5abc57af4`  
		Last Modified: Wed, 03 Jul 2024 09:51:53 GMT  
		Size: 66.4 MB (66449434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efd00e6f670bb4f7c52a202f86e7b1bcb1b76ab48aaa4d8e3f3798a3559b9bf`  
		Last Modified: Tue, 23 Jul 2024 16:34:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:434c743957e7defac67a823a26e2b8ce485079a0adb93081841217c0306d0972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ded28b0519808938799a982f11d1638e9e49e790cdc1a92ac48235ed6283e7`

```dockerfile
```

-	Layers:
	-	`sha256:fa4bccbef925ecde1f565d6689b79e8c76e08aafa7ed2cb8eee64686517764bd`  
		Last Modified: Tue, 23 Jul 2024 16:34:38 GMT  
		Size: 26.2 KB (26172 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; s390x

```console
$ docker pull golang@sha256:8f5ce263ec66952e0b002255099d83d528bf05168d63edc5684161e4f92acf47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257103269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfead80ebf7f751e70a1dde61f2c5b9abaee5d183a9da50c59bbbe2e2392bc2d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 19:33:45 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 02 Jul 2024 19:33:45 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e924418f310f18ad368886d6df84cac76659f51225b0784a1e53ff07318533`  
		Last Modified: Tue, 23 Jul 2024 03:15:16 GMT  
		Size: 15.6 MB (15641720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af67dae0133d3a5f116411c20eed624558ce4a187db4fd8eb9a8d622a827e5f`  
		Last Modified: Tue, 23 Jul 2024 03:15:29 GMT  
		Size: 54.1 MB (54075295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6943ee9ae2f23e3e2ab6c096bebdc78d9f7497a9fcb769dfaff643fb17f456`  
		Last Modified: Tue, 23 Jul 2024 15:53:46 GMT  
		Size: 65.7 MB (65650433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36325bf1498477d36098ce5907eb7a794a2e7eb1ff088a91163f8cf4d9ca6b9`  
		Last Modified: Wed, 03 Jul 2024 01:08:00 GMT  
		Size: 68.4 MB (68411572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20ce07dabf60db34eb42f011f0e08b8fc6b1a331aeecb32c6a9673118826758`  
		Last Modified: Tue, 23 Jul 2024 15:53:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:ca2b47daa0d2f255821fa40d5f3ff326b604710137dd6912918facb0bbe27169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb07baf91bd3a7cb5530de90b4d842093863a17e6109058520fdfc74aa91778d`

```dockerfile
```

-	Layers:
	-	`sha256:4dffbe072aaf752f65f7b276226fe2bffe2e2c651ee68e97ccc63e9403ee50e2`  
		Last Modified: Tue, 23 Jul 2024 15:53:45 GMT  
		Size: 26.1 KB (26130 bytes)  
		MIME: application/vnd.in-toto+json

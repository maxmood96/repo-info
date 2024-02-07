## `golang:1-bookworm`

```console
$ docker pull golang@sha256:83fa581965b1f512ac688445ba50be306c935520c67e0ed1332ff3ef54d9a5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `golang:1-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:ecde762a70025518c23ca1564441dc2ae2dc7af7254392e5d48c7918b156a163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297152912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c541743933a7d840c5923d7793a4417f92729d9b7115e8a5cef5deeb11eaf6b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 18:23:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08e8703b2fb5e50153f792f3192087d26970d262806b397049d61b9a14b3af5`  
		Last Modified: Wed, 31 Jan 2024 23:32:17 GMT  
		Size: 24.1 MB (24050083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e92d11b04ec0fe48e60d59964704aca234084f87af5d1a068c49456b37fe3d`  
		Last Modified: Wed, 31 Jan 2024 23:32:37 GMT  
		Size: 64.1 MB (64142328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4105062d1ee61f98bb0f7f6c0ac998caf55ff9a0e0fda9aa1fddbecc1f591687`  
		Last Modified: Thu, 01 Feb 2024 12:58:13 GMT  
		Size: 92.4 MB (92366895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848a732639f4ba926051511178f320171f919f2f157951958525c0773d8bc58c`  
		Last Modified: Tue, 06 Feb 2024 23:55:39 GMT  
		Size: 67.0 MB (67009646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6f762ff10f6812e1b6063bc2a1c85f2119b2b05906377991c98ee06a4160b9`  
		Last Modified: Tue, 06 Feb 2024 23:55:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:af24f004447402f53ec785fdf82b5a165a619d87b103e73bbd042314cdeb24d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258338172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941be54992b0c78e2cbcaa6f170976a3cacd29106a6fc836749c2b62a0d7c07d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:09 GMT
ADD file:24186d75daba80fe802230517bbb6b4e9d6c695398d1db98108b4487d27ebb43 in / 
# Wed, 31 Jan 2024 22:44:09 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 18:23:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:af02191d26cb0ab470ac42e81c677a72e87ee39e67a36576e102fffc8b1de4a7`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 45.2 MB (45177992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5dbfdb18fe3f9c4fd9d347eb380df7b3080c079f6bffef53d6d588fa3b49bf`  
		Last Modified: Thu, 01 Feb 2024 02:58:27 GMT  
		Size: 22.0 MB (21953682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2114ad3bcb8a20c51922836cabcbf31c1cc36bf285577a204f4dac5b756e1cc`  
		Last Modified: Thu, 01 Feb 2024 02:58:49 GMT  
		Size: 59.2 MB (59216669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca9b1f8d7860a719d7975578d676d9027aa7b6bbfaeccea30b3c58c1a727ba8`  
		Last Modified: Thu, 01 Feb 2024 05:44:18 GMT  
		Size: 66.2 MB (66222162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c045d43346367bebb622f20fa6d7f79c419dbbb6f2aacab90ec54d12d07f9eac`  
		Last Modified: Tue, 06 Feb 2024 21:28:00 GMT  
		Size: 65.8 MB (65767462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e54f788b49d7dfcd806154544bcaf20318d2907cdcabd8f42c7adc4705a5f7`  
		Last Modified: Tue, 06 Feb 2024 21:27:38 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:dfbb17c77d59e4e57bd67ab6e17a268b033680c4f8505c9d5e211f21864a4901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.7 MB (287700373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba3946f3ea9a4bbe3d39dad7eb7685bc2aeab5f5a1b19df791eac471d6c73d7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 18:23:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa7e263db1a3a05a9f31906dee83c0ef41151669759a3362e724b2765fd66f`  
		Last Modified: Wed, 31 Jan 2024 23:52:05 GMT  
		Size: 23.6 MB (23586448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c812910e5e62436c8483e793d1956d1c70bcf42d20d5f0885ddafbe0ba124459`  
		Last Modified: Wed, 31 Jan 2024 23:52:23 GMT  
		Size: 64.0 MB (63994808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0415bb1783d1a348827b100b0e918648a16b9be64e3af2d45b75d4996ff5b8c`  
		Last Modified: Thu, 01 Feb 2024 08:13:22 GMT  
		Size: 86.4 MB (86394350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0fd82be4907d6f953b1ba462fdbb656a0fe6262810e89b8a01112e709dbd38f`  
		Last Modified: Tue, 06 Feb 2024 20:48:44 GMT  
		Size: 64.1 MB (64109266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4912bc7d1a618e3caefaec76fdc8c9cfa294d1851caa729310ffb3e1267e7d`  
		Last Modified: Tue, 06 Feb 2024 20:48:29 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:4d84ef6fe17a3fbe598dd7d5f38281b220c3301b4a408aef395a41bb7a9c0e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296716326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830239886919a2e76b98ff9362a33c0f6381871ddc4c1e4d1133ff4747764c8c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:38:50 GMT
ADD file:185b752162445ab4f6f919d4279c3e0631e6ee605698ec61317458546cb121f3 in / 
# Wed, 31 Jan 2024 22:38:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:32:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 18:23:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4ea3f2a7e82bec0cc3c3005b69be76f8931170968478e9b540091cde5dbdf791`  
		Last Modified: Wed, 31 Jan 2024 22:43:19 GMT  
		Size: 50.6 MB (50603415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee967c27b9c941dceae087384959ba6b8e9de11c54505fd91905d98eea18baf`  
		Last Modified: Wed, 31 Jan 2024 23:44:47 GMT  
		Size: 24.9 MB (24888772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342d8ebbc02bcb8071e4594b56892d4ec04d2bdcf0ee0283d75d845023c1c9fa`  
		Last Modified: Wed, 31 Jan 2024 23:45:13 GMT  
		Size: 66.0 MB (65989049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7398ef24c7b6cb275d0a6291e39cd3a4d9418dc42f62313f52b0fab8952c51`  
		Last Modified: Thu, 01 Feb 2024 12:03:30 GMT  
		Size: 89.8 MB (89774019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1bcc438bdcf603a7092aadc2f33a27b18ad77e263040a640af0d6205b19302`  
		Last Modified: Tue, 06 Feb 2024 20:48:37 GMT  
		Size: 65.5 MB (65460864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea680941cd6e21d74423d15b6b9dd70222d0b6304652f86510aacc7b71ce658`  
		Last Modified: Tue, 06 Feb 2024 20:48:15 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:988e5189eb2541e109e359fd3b9677a49f71fe24dbb73b0f6ba71ddbb1f9df1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267837850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2077ed641abcfed2b05b0debd7874a24a2da2b925c01470f14322ae12f54436d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:26:24 GMT
ADD file:eee6c048a0eb51959b7cb7d3c4efc6652decf19517bcb25076f8ef9fc376ce48 in / 
# Wed, 31 Jan 2024 22:26:30 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:10:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 18:23:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:07a56ca79640510bd74a49ee96c70117fcef80d3a54a0b75ab30e3c06c58abff`  
		Last Modified: Wed, 31 Jan 2024 22:37:38 GMT  
		Size: 49.6 MB (49574061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9396b75608be0bb38ec0e5812806b60c77abc5f3118ac99b6d0696cfb6d142d`  
		Last Modified: Thu, 01 Feb 2024 07:45:23 GMT  
		Size: 23.4 MB (23438036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ca92fd224410a9f84732731a0d2db9a52407b7ca33a418dd08d3d679826a0a`  
		Last Modified: Thu, 01 Feb 2024 07:46:21 GMT  
		Size: 63.0 MB (62968385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e431e01413a84471a93d2d059b9d19171a00242a961633015b2944357153529`  
		Last Modified: Thu, 01 Feb 2024 18:40:32 GMT  
		Size: 69.7 MB (69722860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887a8378563a08d7e7defbe50a55d44ea28ab1b37a11099b03c21b465a9a8e24`  
		Last Modified: Tue, 06 Feb 2024 20:52:02 GMT  
		Size: 62.1 MB (62134350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9f0306f4230befcc66c70cf0a8d76411491224971dfd7222920a73142f22dc`  
		Last Modified: Tue, 06 Feb 2024 20:51:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:882643a9ec375b5fa1d2381207149e529ffd499d6467d2aecf7672b5dcc11f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303336567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9e8b316b44cda092010b03597cd4cbe95ff4bd6c5fcc45f5ad50fcd7d33719`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:20 GMT
ADD file:e856dcd026d65beec0f1b0cf2e26a377ae06e730603870e5f78290fc8c78c3fd in / 
# Wed, 31 Jan 2024 22:29:23 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:27:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 18:23:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7579f5ed16e0992350eed26d915c99451987a3b2cfb96fee25d4b65b8d8c2aac`  
		Last Modified: Wed, 31 Jan 2024 22:33:56 GMT  
		Size: 53.6 MB (53578470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ec8e5c0fa7f8ec08ca2f938f40e14f359ca71996729690f50368e0ff622ad3`  
		Last Modified: Wed, 31 Jan 2024 23:47:36 GMT  
		Size: 25.7 MB (25699520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa97c27b10146b73ca93631d629172e2bb41f6535ff6306e0fb5b0c9b4a71263`  
		Last Modified: Wed, 31 Jan 2024 23:48:00 GMT  
		Size: 69.6 MB (69584038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d27c0ce817cf45ea009954445cec293495b0bb8726b147c6d45499b9fdab8a1`  
		Last Modified: Thu, 01 Feb 2024 08:53:41 GMT  
		Size: 90.4 MB (90353903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a426dc58ed9e424530d062d0317e10e9274458515ffedf9891d5e6098fc4d92`  
		Last Modified: Tue, 06 Feb 2024 20:37:36 GMT  
		Size: 64.1 MB (64120430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb1661ffb9446601f46998198e66c9f68984408d88b83e891c3dec0c462670e`  
		Last Modified: Tue, 06 Feb 2024 20:37:14 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:ecf6bfe0d06e34450f50823ec4c53ddb87412dba0c866ba8463004fe10f3a6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 MB (270267421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baad39f0ab0db9f29bb63059b1446089deb55054cb848a4eaae34953356bbb7e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:56:21 GMT
ADD file:b1c0200d0f8b6070dfcbbadb831cbd04bd8d1b15c3c1f8e6e13c467f6c3f2879 in / 
# Wed, 31 Jan 2024 22:56:23 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 18:23:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0241650ae38ec8570f9718818b3b516c90697c5cd5686d5dd89306ae5f8e4657`  
		Last Modified: Wed, 31 Jan 2024 23:28:45 GMT  
		Size: 47.9 MB (47940767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1461a92bfa612443d019b6fc535db5abfd3639e66c1c5f41a511bdb1a782f00`  
		Last Modified: Thu, 01 Feb 2024 08:18:52 GMT  
		Size: 24.0 MB (24046914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bc22d156c3113277b2a400b2b60e0ea00f6f62f339de493144008d5cc58796`  
		Last Modified: Thu, 01 Feb 2024 08:19:08 GMT  
		Size: 63.1 MB (63130267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f6703bd26ac194942bbcf09cedd3348533b217534135725364c28e812693bd`  
		Last Modified: Thu, 01 Feb 2024 13:19:02 GMT  
		Size: 68.9 MB (68931524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab9bf3c7ed02fb6cb6ccedfbf53f2ae7421386d79d6662a044b6e6620564f16`  
		Last Modified: Tue, 06 Feb 2024 22:14:01 GMT  
		Size: 66.2 MB (66217742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41afabfa27de74c561395c5b4034b465074b296351e8b47c5acf61f534695cd`  
		Last Modified: Tue, 06 Feb 2024 22:13:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

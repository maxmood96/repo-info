## `golang:1-bookworm`

```console
$ docker pull golang@sha256:ed2fef39f056db960f0b844fa9f0590956c641982706ba30bec2839605cc6c5d
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
$ docker pull golang@sha256:89a1b98608f91fe47734cac497c0d7bd0c88239f90cccd00ea47057eb09604e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303944376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909878790629eec22929507a6ab7496b0e315168dfd9a01dbc0fd3d318d7d96c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:09 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Tue, 13 Aug 2024 00:20:09 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:43:37 GMT
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
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed93aa58a52c9abc1ee472f1ac74b73d3adcccc2c30744498fd5f14f3f5d22c`  
		Last Modified: Tue, 13 Aug 2024 00:50:05 GMT  
		Size: 64.1 MB (64143347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaef56be71e0dbfd65cfce30067669cf416cd6a54a17fc51a7fd11f4029b8fb`  
		Last Modified: Tue, 13 Aug 2024 20:02:48 GMT  
		Size: 92.2 MB (92230777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b14fb4020d7e427735797bf663a02a5a028e40fae0f8993ed5dfe75f15417a`  
		Last Modified: Tue, 13 Aug 2024 20:02:18 GMT  
		Size: 74.0 MB (73965318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d1f4306f6d717f726b1465661751fa6bad7f45a14c6f0133c41d377a0d775b`  
		Last Modified: Tue, 13 Aug 2024 20:02:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b0f755e160fa2c1a363f431851b058728aa9a06936a7b1035c403dc0026b0ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10285341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9126f99632d8f70571f93c43e7dbe6a30b861cd9cc207d8fd4a36574d930df0b`

```dockerfile
```

-	Layers:
	-	`sha256:4050fa6b2f3e67b08de0480a97f8e01c417960c663938eeae5597cbbb12bd3c8`  
		Last Modified: Tue, 13 Aug 2024 20:02:46 GMT  
		Size: 10.3 MB (10257814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ce16cf21bb77265ab875aa5141c16ab46e4c6610564f33f128758ee18cf860`  
		Last Modified: Tue, 13 Aug 2024 20:02:45 GMT  
		Size: 27.5 KB (27527 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:e3e4449f4e4e7f740122cd1d6c63fe1fb8cd16d526f6c68fc90773111f5b89b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264541612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a5841f7b583c0acb97645976c686f7192deaddbf3e8f50842d98fca0122149`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:26 GMT
ADD file:e3c71ceb3b7032e8a78ea70e306ec97b152570eeaae849a0c97bb61b2b12287f in / 
# Tue, 13 Aug 2024 00:57:26 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:24:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:24:21 GMT
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
	-	`sha256:fe61db625a1b529903f1126ded0caa9e4e1c247503d524cd43bc15454b6bcc2f`  
		Last Modified: Tue, 13 Aug 2024 01:00:32 GMT  
		Size: 45.1 MB (45148160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06599d70e5763853acd56f8e4938729e068e7942382f335f96ce0ae3bc5a63a`  
		Last Modified: Tue, 13 Aug 2024 01:32:20 GMT  
		Size: 22.0 MB (21954622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3af44a3c0ce16617696528373b53738420f91f3383cda1666cc673cbf6fe50`  
		Last Modified: Tue, 13 Aug 2024 01:32:41 GMT  
		Size: 59.2 MB (59221928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bc24d45690a515d5d64aeaa7be5994f7db1e902b9e4dadf7bbc9b27214008d`  
		Last Modified: Tue, 13 Aug 2024 11:29:59 GMT  
		Size: 66.1 MB (66089195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6363114f7204e8b9cd3cb47febe5a3082ffb85a82d8c47efb0021f3f9323f`  
		Last Modified: Wed, 14 Aug 2024 01:59:55 GMT  
		Size: 72.1 MB (72127549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794e0e6bfe8897aa8d2badc883a93aacac284e36a2385b6f0880852f4a4296cc`  
		Last Modified: Wed, 14 Aug 2024 01:59:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f1245c4cae3a035d3b1881a66750e9a0bf7676ccad761e5cb01a4fd44c8faf0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10094203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f643c0307132ced133d3d5005838cbaf8efd4fdf6cb38e31da89d30dc3a11b82`

```dockerfile
```

-	Layers:
	-	`sha256:fa2b41aa169a4e07c7c4a3b02601d5d484457d94acd84e31649659a6fbcf52c0`  
		Last Modified: Wed, 14 Aug 2024 01:59:53 GMT  
		Size: 10.1 MB (10066549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1034f1ff9e7f98441fb650bf30a31f3b719c0df3467fe7d68c2ad051046a0afb`  
		Last Modified: Wed, 14 Aug 2024 01:59:52 GMT  
		Size: 27.7 KB (27654 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:2ce9dbaf7f2890fcb424e35e9abb8bc7263e40dd54291f3325482c6b5ccba403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294066879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f37d53a950e26c37b64a6d2ebd572313afc1e6d9598c4e561c0b7d5cb30cac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:42 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Tue, 13 Aug 2024 00:39:43 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:02:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:02:39 GMT
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
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275677961327bd0cf394699228e29d7caf27f171c627899a20ebc9eeb550e209`  
		Last Modified: Tue, 13 Aug 2024 01:09:34 GMT  
		Size: 64.0 MB (63994880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba10d98c12a2ca1218e523a3acef29a20936647fc1dfa2c0efdf51ba7b784258`  
		Last Modified: Tue, 13 Aug 2024 21:36:26 GMT  
		Size: 86.3 MB (86282906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f9ed64c24993ada6c5d1b00ea7fbf5720c6cc30c9ae14d18134989fa7a08a7`  
		Last Modified: Tue, 13 Aug 2024 21:36:27 GMT  
		Size: 70.6 MB (70607916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e926ff100441db37fd809e84a1b238a7facaf8f44aa8da2c62d5c6b75fb4c5`  
		Last Modified: Tue, 13 Aug 2024 21:36:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1ec7ecd923dd5101afae65d2271b95b308dbf14d142e7bd416cc1833909464b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10313631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffc3d42ba19593cca96c3a8ae3213e22829f52420fa0850722fc00bc950acee`

```dockerfile
```

-	Layers:
	-	`sha256:35365cb61b7bec23c48652e6e7dab725b6b37dd17375c1e7e2a92a30a4966f04`  
		Last Modified: Tue, 13 Aug 2024 21:36:25 GMT  
		Size: 10.3 MB (10285740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2030f6b961a4a7e34243e07e72de469d5ba06d75d8d8d75602029fa9dfc47fb`  
		Last Modified: Tue, 13 Aug 2024 21:36:24 GMT  
		Size: 27.9 KB (27891 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:f8ddc4ae1e9feef1a8ffa360b65c41c62b2afe0a90ab3c6f3fcee20fcd47fad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (302961252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e9bc7eed7d07a1c541a834200499975ce741e879f928c16af02822e39f9e45`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:38:44 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Tue, 13 Aug 2024 00:38:46 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:05:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:05:47 GMT
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
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce3393c41a8406d190eb7fe061fde8daaa2b0fa20c672505d04631bd52a1325`  
		Last Modified: Tue, 13 Aug 2024 01:14:02 GMT  
		Size: 66.0 MB (65988846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cec92e743a48bc3c6c99c2090e6b215ea32ad087a4642a01e8970b2cac2b16c`  
		Last Modified: Tue, 13 Aug 2024 20:02:43 GMT  
		Size: 89.6 MB (89644687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948a02128519d4902024135fc03b12145f389fd4b2b393eb6499f6f10486bc83`  
		Last Modified: Tue, 13 Aug 2024 20:02:22 GMT  
		Size: 71.9 MB (71856633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e43db2d38a03d721cad4ad8bb32bb71569cb97f8d6a8d74d26122c86a35861`  
		Last Modified: Tue, 13 Aug 2024 20:02:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0e190b10828b5d06d1161d92d24295d3f30d89f742bccaf551b471f7c53fc7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10265544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dce9acb77734f051058fed9908b528e3916e3271438762a23016a1ff638f370`

```dockerfile
```

-	Layers:
	-	`sha256:27fccc4b485ee131c9d5fc2a359665d27de70058186eddc269712274c253d7c6`  
		Last Modified: Tue, 13 Aug 2024 20:02:41 GMT  
		Size: 10.2 MB (10238070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fd77db812a6c895cccf18fa3553d21409541712b6c40ff4b1f5dd62fca220d6`  
		Last Modified: Tue, 13 Aug 2024 20:02:40 GMT  
		Size: 27.5 KB (27474 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:b049b6223a09cc520d0306f25608b8a5d0b8bf92f0991d4e9a40e0cd7962e313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.1 MB (270095661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af592bd4eaf4633ff36c54afbb023e6ec8a4a3c292c66c4324312ab1ed723da9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:36:56 GMT
ADD file:bc2014dd4183b8b941ef345add7dfa4a5b389afd70c64828331a9e51522a8c03 in / 
# Tue, 23 Jul 2024 00:37:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:26:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:05c2d132d3391d998ebae95f3de018ca09dc34d9bfbb160a1b6d662ebfe22612`  
		Last Modified: Tue, 23 Jul 2024 00:48:21 GMT  
		Size: 49.6 MB (49563161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b431e247f5dc02821a251567e4e81f86ada15613f56a6428e9d515728a3248cc`  
		Last Modified: Tue, 23 Jul 2024 01:58:32 GMT  
		Size: 23.6 MB (23636541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b6025db3aeb726503a6d775307c4881743edbf88fbefd8a997f66bb236e568`  
		Last Modified: Tue, 23 Jul 2024 01:59:26 GMT  
		Size: 63.0 MB (62965755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384a4864817e575bb9be405b8211a736dc0d9f4c7a7a3f3a69362908649b06f1`  
		Last Modified: Tue, 06 Aug 2024 23:00:16 GMT  
		Size: 69.8 MB (69804406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ec510b2b8fe8d60e2b414c455523b255d2db4e07537481fb550635278f8c2a`  
		Last Modified: Tue, 06 Aug 2024 23:00:16 GMT  
		Size: 64.1 MB (64125639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677390295ff7019b7fabc9ca6abd29b1c6fe12e2b57476435284656da6bd16b7`  
		Last Modified: Tue, 06 Aug 2024 23:00:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2feb75c909ebf27c1de5ac46c68fa91d3bb79bfa2168602f03babe51a3c75e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b0e1f94cdd94e91d19ac71efbb35d1462c4ca885e11e767abee31600a762f0`

```dockerfile
```

-	Layers:
	-	`sha256:9c9d6c07df9800db780266279e283eb439bbf9f1148b285bb4417222353c4271`  
		Last Modified: Tue, 06 Aug 2024 23:00:09 GMT  
		Size: 27.4 KB (27407 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:fefcc2247180431fd3a7c8b9a1cb33144f602458fd53dc6886de7738b517194a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.8 MB (309825219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e87e7746d909ddbd2aa72f05d76a09e0b5a7fb977f3b57b67335e10f13dd079`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:45 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Tue, 13 Aug 2024 00:21:48 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:20:05 GMT
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
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eed7e3592a50ab5e7544963d89fc48e8c78210f32cca0a16ecb3266ccbcc73`  
		Last Modified: Tue, 13 Aug 2024 01:35:09 GMT  
		Size: 69.6 MB (69581670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f201d1082476b8e5828b878569001b67f05ef97d6646697cfa608d73a62eb283`  
		Last Modified: Tue, 13 Aug 2024 16:55:09 GMT  
		Size: 90.2 MB (90217892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00804d58ee01dde250ba214452343e0ba5cd0f3e98c64328395648d07b4df92`  
		Last Modified: Wed, 14 Aug 2024 00:13:23 GMT  
		Size: 70.8 MB (70772941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8bee01a0aeacb77a6205577c12238d71af4256278acf05020e598aebf58e73`  
		Last Modified: Wed, 14 Aug 2024 00:13:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2e824d1211b4030d04137351ddd7be5ca8740f5e5abfc1d27b457ebb1b6eda29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10258262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c377419f1318be57a357eefd6a071a50a08b039db06ecb7a254eb40c94418d6`

```dockerfile
```

-	Layers:
	-	`sha256:529f952b42d3e4a665d3c8c25b955691a54e0c837694736ca47eec0432466568`  
		Last Modified: Wed, 14 Aug 2024 00:13:20 GMT  
		Size: 10.2 MB (10230669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60f7ec7f59b2972c41378c882a0def1bd07a988e7d5287355d80249504fd4376`  
		Last Modified: Wed, 14 Aug 2024 00:13:19 GMT  
		Size: 27.6 KB (27593 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:3fe7af19aaf1ea1304e8ed10b83342240e9bf3ca0210536168a4289591b9d494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.8 MB (276808616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3e7b9c7f2fd198e4530349d3f1b2ff53b364c02fd52811fa1af2af797fe3ba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:19 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Tue, 13 Aug 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:16:38 GMT
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
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5671dc1d98954f99af5dadd617a0aa8b53840b28295900cb7cdd39eb592946`  
		Last Modified: Tue, 13 Aug 2024 01:24:58 GMT  
		Size: 63.1 MB (63125064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb724644bd76f1a0ff54c043dd51ad35a7b4ac4ae889cf9d65db267bdab2ddf`  
		Last Modified: Tue, 13 Aug 2024 23:07:37 GMT  
		Size: 68.8 MB (68804026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d766dfa346f9569deddaa862bfcc6c453c61295fa0688cff4cf096f917447678`  
		Last Modified: Tue, 13 Aug 2024 23:07:38 GMT  
		Size: 72.9 MB (72899210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb3533a7f134ba9070e272b22385b2101c1314d98ea5341a1eef2c75da2270f`  
		Last Modified: Tue, 13 Aug 2024 23:07:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ef01b3291087d0d26345dcb2967f740188e19311e4aff4978422df4b96dace2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10121740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9db1b7342a289681cd4b098771c6efacb676f89c7454f3c972aeab705ae3de`

```dockerfile
```

-	Layers:
	-	`sha256:59950e2ac15ab44459da053ebd57341da30561f4b5160b34c822237d28604908`  
		Last Modified: Tue, 13 Aug 2024 23:07:35 GMT  
		Size: 10.1 MB (10094213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f90a3137578e3c461351d1a0c9b730c7d45bf984fafc5ba56d2eb3ea7659e3d`  
		Last Modified: Tue, 13 Aug 2024 23:07:35 GMT  
		Size: 27.5 KB (27527 bytes)  
		MIME: application/vnd.in-toto+json

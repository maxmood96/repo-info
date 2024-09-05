## `golang:bookworm`

```console
$ docker pull golang@sha256:88d9a5d3de220869be9c59a417b260623a0251ed727195857d740ea64ed71c51
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

### `golang:bookworm` - linux; amd64

```console
$ docker pull golang@sha256:ff787165114376423b784ea19442b4a7988c58789f3aa97560f57f0aea87460e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303984084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5318a98101909c21a623950e8c9176f9888735772bffa73c524510b13981fff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:10:31 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Tue, 13 Aug 2024 17:10:31 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 17:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 17:10:31 GMT
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20663332bcc9b53cdcb67c88a48326dc358db93b72dc2032af41c46239a3574c`  
		Last Modified: Thu, 05 Sep 2024 00:07:39 GMT  
		Size: 92.3 MB (92260735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b14fb4020d7e427735797bf663a02a5a028e40fae0f8993ed5dfe75f15417a`  
		Last Modified: Tue, 13 Aug 2024 20:02:18 GMT  
		Size: 74.0 MB (73965318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c85014d0d1b661aa84465b70040e742ef94cbf936533fb4bc455bd11c715e8`  
		Last Modified: Thu, 05 Sep 2024 00:07:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6815c76de544a75fa610bc9153e59ab3433e4ef5ed20fdedaf3fd87ee413d3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10284730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dfda8d8265d1230177b968b9a37ca781e389012825ec773444e815f57e64f0`

```dockerfile
```

-	Layers:
	-	`sha256:27da37896fee8e010e90cb8345cce21a2a049d1a8b4af8deb597dfe9b6c2f7c4`  
		Last Modified: Thu, 05 Sep 2024 00:07:38 GMT  
		Size: 10.3 MB (10257203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:368418f204e8040d036229574e9a6470a7dc5c3432aba9b9145d108c0f54893f`  
		Last Modified: Thu, 05 Sep 2024 00:07:37 GMT  
		Size: 27.5 KB (27527 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm variant v7

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

### `golang:bookworm` - unknown; unknown

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

### `golang:bookworm` - linux; arm64 variant v8

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

### `golang:bookworm` - unknown; unknown

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

### `golang:bookworm` - linux; 386

```console
$ docker pull golang@sha256:b8dbe9f470038270fe8706bb24cd993082dcac4678ab2045e0bdd1d78006d128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (302975664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e6851ffac3d56106c36639762ae7fabce07dd3b6eb5736992d85004cb0e986`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:10:31 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Tue, 13 Aug 2024 17:10:31 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 17:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 17:10:31 GMT
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
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f610692db1620f4afe803908f30b5f7f161eb86c70e8b03501ba42c1b26b7ec`  
		Last Modified: Wed, 04 Sep 2024 23:20:20 GMT  
		Size: 66.0 MB (65990847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb385928d50e6ce8b5c5f6fbb07cf7544d5f4ce3e3b56cbff70182bf9dfea360`  
		Last Modified: Thu, 05 Sep 2024 00:07:39 GMT  
		Size: 89.7 MB (89657920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948a02128519d4902024135fc03b12145f389fd4b2b393eb6499f6f10486bc83`  
		Last Modified: Tue, 13 Aug 2024 20:02:22 GMT  
		Size: 71.9 MB (71856633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c85014d0d1b661aa84465b70040e742ef94cbf936533fb4bc455bd11c715e8`  
		Last Modified: Thu, 05 Sep 2024 00:07:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7891be383f233a68666f69f7c471360d161a659f4cf89dd20423518c5d156a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10264933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103f6cd9804fbb4b7924f1e6db3b809096ffe81f04f51a21a24db7dd66bfc0b7`

```dockerfile
```

-	Layers:
	-	`sha256:a5ad18e57d8ffa69c227a5d2c5cde9646af2e3c24d93fcf964a4331657a5650a`  
		Last Modified: Thu, 05 Sep 2024 00:07:37 GMT  
		Size: 10.2 MB (10237459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e94b404cfbad52b578f18c97a85a1254e9df1fe6f521e418b626966eb65ebc`  
		Last Modified: Thu, 05 Sep 2024 00:07:36 GMT  
		Size: 27.5 KB (27474 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:fd33373ff69e435af15291e9a0d27ef28c4b3557ee85ea16de54552155178819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274223970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c5450b1b3099c6f03a4d693d78739bb1359203bcfbdc55970e6ce824ae9d40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:10:27 GMT
ADD file:42b5546fc536a0937c9332001326b56edcfad5a5db46bb873f84f73c3bda9b67 in / 
# Tue, 13 Aug 2024 00:10:33 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:56:27 GMT
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
	-	`sha256:192d8664ef287a4c7c8030bb7f9fd54f06a0ee665114437e01bd957247249b59`  
		Last Modified: Tue, 13 Aug 2024 00:21:46 GMT  
		Size: 49.6 MB (49563201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f290e8d96661528fcabadb467014984544fb262f562d178e8eacd4c2b72d7bdf`  
		Last Modified: Tue, 13 Aug 2024 01:31:16 GMT  
		Size: 23.6 MB (23636644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada0a2437b401a0a19336dc670ab8d52dc4c37912787524de56c1c95a6bde7cf`  
		Last Modified: Tue, 13 Aug 2024 01:32:08 GMT  
		Size: 63.0 MB (62966082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e4347b91fe5fb291481abf0a60986f431eac5935ca32fd5709f207f8f9550d`  
		Last Modified: Thu, 15 Aug 2024 02:12:55 GMT  
		Size: 69.8 MB (69804132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27db76523907baf3cbb675048e8757c9a576f2d66aeec462441052ee2868acf1`  
		Last Modified: Thu, 15 Aug 2024 02:12:55 GMT  
		Size: 68.3 MB (68253753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5055010fc09181f3ad2b5be7871c2d7721a38fb098d895e51d52e3942bc52b85`  
		Last Modified: Thu, 15 Aug 2024 02:12:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d222c43570372c9571b6afe6f2113704caddf71a063b49e7a2c9438277d4283e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e82cd8ae05aa2789d521ed822c9e2bb81c51871909aa1e7590f1d6ff695a33`

```dockerfile
```

-	Layers:
	-	`sha256:566021b1c9faab5eb32f6dffd23f93a6be18241cc45ae0cf8e227436dcc7149a`  
		Last Modified: Thu, 15 Aug 2024 02:12:48 GMT  
		Size: 27.4 KB (27407 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; ppc64le

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

### `golang:bookworm` - unknown; unknown

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

### `golang:bookworm` - linux; s390x

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

### `golang:bookworm` - unknown; unknown

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

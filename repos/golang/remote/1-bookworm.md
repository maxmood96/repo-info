## `golang:1-bookworm`

```console
$ docker pull golang@sha256:b300c88a7579d9648b967b96c25a47480bde031165f765a4cd89dc0867ef13a3
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
$ docker pull golang@sha256:46a86b411554728154e56f9719426a47e5ded3cab7adb1ecb22a988f486e99ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299461168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a84586274428d0a1b9784f47c0f7893568c12b133b608aee859848d04c2ddf7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:21:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Mar 2024 18:08:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOLANG_VERSION=1.22.1
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:08:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:08:28 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b40be4436eff6fe463f6977159dc727df37cabe65ade75c75c1caa3cb0a234`  
		Last Modified: Tue, 13 Feb 2024 01:30:58 GMT  
		Size: 64.1 MB (64140328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85d001093ea5a15e173ede0aed3f6eea120f590af073ccfabe1a321ebb1569b`  
		Last Modified: Tue, 13 Feb 2024 13:08:38 GMT  
		Size: 92.4 MB (92373772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ef1a2d00d69c8dcace4d9369e061eb30f1cab4ec9321bf0f935d385831c223`  
		Last Modified: Tue, 05 Mar 2024 19:22:58 GMT  
		Size: 69.3 MB (69347681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7cd42926dc1daa1efa647b57e062cf826fc814adacc3eaccb0b508af21f18e`  
		Last Modified: Tue, 05 Mar 2024 19:22:46 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:89a01816d9753410e3b9385665b5d59b9637fc2ed526415a5df6d4da863d0dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260263884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae6cd6909c24bed9ce6ec19039a7cf2b1c4925f3ac08e9bac73a3437213cceb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:10:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Mar 2024 18:08:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOLANG_VERSION=1.22.1
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:08:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:08:28 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c41c61f6174f60169420d32957e496b1d382932c8ceb86da9fd7484a7210398`  
		Last Modified: Tue, 12 Mar 2024 02:19:27 GMT  
		Size: 59.2 MB (59213166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5b34e3f705b111457cbf72641e1932a528226beb14541a24bda91367db3f35`  
		Last Modified: Tue, 12 Mar 2024 10:41:24 GMT  
		Size: 66.2 MB (66233612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc98e10d1de92f4c4636f75b718b784a1feebc94a5853dc9b210b61faffbe0c`  
		Last Modified: Tue, 12 Mar 2024 10:41:29 GMT  
		Size: 67.7 MB (67712778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bcf2fd3bfcee7ca81a5af6a551efe21b63a478510bb8b8dfa2621fab997103`  
		Last Modified: Tue, 12 Mar 2024 10:41:11 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:3b3fecb519465a8c385efb1db645dec61b04e8520a2ab018878688f07c153828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289820542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e9f02e714944640a9f56cea3c4641959d56c3520b043d9c3425ff6bef78222`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Mar 2024 18:08:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOLANG_VERSION=1.22.1
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:08:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:08:28 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3861a6536e4e911503e7d2fc8f93228491ba45d1e5def0d2f3723e32e03d7466`  
		Last Modified: Tue, 12 Mar 2024 01:34:50 GMT  
		Size: 64.0 MB (63990914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc7e462754aa407ba73b5f3e308e2dd9f24ad9d6692a741f7864bbd27e67eb5`  
		Last Modified: Tue, 12 Mar 2024 10:18:59 GMT  
		Size: 86.4 MB (86408889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c6f29f6556ff45268a4fb5ba395c214cac9f4f9a57f55d27fc7ca44d1c5b4d`  
		Last Modified: Tue, 12 Mar 2024 10:18:58 GMT  
		Size: 66.2 MB (66246673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a240b3b808d917b5d8f2b7c06dc7ebd0517be84e95e48cbb79f15df84b7f5015`  
		Last Modified: Tue, 12 Mar 2024 10:18:49 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:1ad9bef4f2aba1831a12dcd726083453f638bc5e05341207e6c02a734724e843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298565501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3595faf3ab0e8db2948f7885389dbb6ec4cda98f7d0e0c116d4ffa07697769`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:44 GMT
ADD file:e12b4798eb856f517a57dfe550811e57903589ffa74a09d47f7c0261e23ca645 in / 
# Tue, 13 Feb 2024 00:38:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:17:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Mar 2024 18:08:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOLANG_VERSION=1.22.1
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:08:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:08:28 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:911275c2fc723590176bf48d32222d2b1299cd1a17294bdc4cebd96e25742b27`  
		Last Modified: Tue, 13 Feb 2024 00:43:21 GMT  
		Size: 50.6 MB (50581925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04ecbcf46d4507b6a8970b941f809a05d49cd1ac9402f7495e0cfbeac9fd1c9`  
		Last Modified: Tue, 13 Feb 2024 01:29:22 GMT  
		Size: 24.9 MB (24884414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d2a319089434096accd3face0ee4bb9f2e02eb5571f7d983c3c48579df902f`  
		Last Modified: Tue, 13 Feb 2024 01:29:47 GMT  
		Size: 66.0 MB (65986836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae1c0332765d563222c0047e69c57ef3a49395a851c283d7db6c54fda0adfbc`  
		Last Modified: Tue, 13 Feb 2024 15:12:48 GMT  
		Size: 89.8 MB (89769305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a38d9d3e8cac7068101167737f58c6f0f0871552769118843bf99bc9b8b59b9`  
		Last Modified: Tue, 05 Mar 2024 20:02:58 GMT  
		Size: 67.3 MB (67342816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fe0bd372be148f5f359e1bc70a45562d358d3124fca174b7df561fb4fb42f6`  
		Last Modified: Tue, 05 Mar 2024 20:02:40 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:c73adf8d3d4f7b932f45718657f0a4a06ee1307b50cc49408125ea8fbb8e8de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (269997256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3825a20eb05b96dabf7a40d03938c3da35a52ac0e2ace02a95b4e2941ebdb6a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:03:34 GMT
ADD file:fb8895339019f207ef48174cf1263bc0d0c200e8ff5100bd033fa9f04719a0ab in / 
# Tue, 13 Feb 2024 02:03:40 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:46:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Mar 2024 18:08:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOLANG_VERSION=1.22.1
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:08:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:08:28 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e79c0a3a7155a4df44e64f72b3886978fe62771937c5515432ff2dbd7eb44ae2`  
		Last Modified: Tue, 13 Feb 2024 02:14:26 GMT  
		Size: 49.6 MB (49563166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c104a14c05b649f6cf44b231609cb7fd64237e83ca7b8eb07b2a5029fb7481`  
		Last Modified: Tue, 13 Feb 2024 04:20:33 GMT  
		Size: 23.6 MB (23630739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b7aae7f397e2eb111826952978a14b68b4e05e905f004686ce9a46b279ffd8`  
		Last Modified: Tue, 13 Feb 2024 04:21:26 GMT  
		Size: 63.0 MB (62965953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf89a9dbced71c6f391f3cedb431df5f33fea7fa4e49184edea117162b3b4cd`  
		Last Modified: Tue, 13 Feb 2024 20:36:23 GMT  
		Size: 69.7 MB (69732852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54624227d01c2a00dd65e7f397b581e49c079e016f2d7d1d19fef24882ba9562`  
		Last Modified: Tue, 05 Mar 2024 20:23:13 GMT  
		Size: 64.1 MB (64104388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364d2797f34bc59648e4ca973e55cf4cddf36c87b259272f075ac749cae78cae`  
		Last Modified: Tue, 05 Mar 2024 20:22:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:3d78a732cb4fdec6850a1be80fdfbbe9acf3a36ed92d95d344c6c2089e4703e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305620578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4207d256b756334a7e9975ba910f7d7dd2d4144c685b432270f303baa83f77c9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:43 GMT
ADD file:83b2c138b49e79b23d3462cb4b39f3f6f151b690a83c7b1ff169ae4590fa0b43 in / 
# Tue, 13 Feb 2024 00:38:45 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:19:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Mar 2024 18:08:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOLANG_VERSION=1.22.1
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:08:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:08:28 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:79696cca44e9751723104a8e361568bddd373ed772da9f88250ba2947fbc6043`  
		Last Modified: Tue, 13 Feb 2024 00:43:22 GMT  
		Size: 53.6 MB (53556530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e1eedad062cc55ed99a98d52f8d5ad41e90a0d0e6e0f6d078e28affbcc296f`  
		Last Modified: Tue, 13 Feb 2024 07:36:09 GMT  
		Size: 25.7 MB (25696437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa5d5534722f047808ec018306e8774ac9f7fe290d7e48b9d2979085bbfd0bb`  
		Last Modified: Tue, 13 Feb 2024 07:36:31 GMT  
		Size: 69.6 MB (69581064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652dec73edb2a6f2a8bc3de25a8c663d0474ac8bb34da57a6336cc0a665670ea`  
		Last Modified: Tue, 13 Feb 2024 11:29:16 GMT  
		Size: 90.4 MB (90359417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4731839f8e1fc44aa25c431be93230683560659198cbc0ca3f1d32a2b27aaf02`  
		Last Modified: Tue, 05 Mar 2024 19:21:52 GMT  
		Size: 66.4 MB (66426925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30a08a7e3f9719e6e98b86c49ae12c9a8971ac428f8306370ab89c55ac40bbd`  
		Last Modified: Tue, 05 Mar 2024 19:21:40 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:3125d1d51823e0b9af0077d9afd0db45225e619461a74eb63bf5e7fc3d9ad1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272415925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38872e9bad247a0f624d57ab52b3025b8fd4460c86322c0f070b2aab4b7f7618`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:51:23 GMT
ADD file:78d8ac80b1cc0c1fee1055005d9481e7bfa64e2586e84feeda25de7413892506 in / 
# Tue, 12 Mar 2024 00:51:25 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Mar 2024 18:08:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOLANG_VERSION=1.22.1
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:08:28 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:08:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:08:28 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:08:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:46730624c51b83b2a39f8e8dd2b4f779e9de6d2947a869347d866c219bf64034`  
		Last Modified: Tue, 12 Mar 2024 01:20:56 GMT  
		Size: 47.9 MB (47916698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddd8fd5b149ee7af1c46d50fe003e26464d37986964f535f7974aa281f5e5db`  
		Last Modified: Tue, 12 Mar 2024 02:47:27 GMT  
		Size: 24.0 MB (24043467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e216ccb0e83eab691c529b6b3db381ade89246b00d45b49aa74a6de8d55709`  
		Last Modified: Tue, 12 Mar 2024 02:47:43 GMT  
		Size: 63.1 MB (63126659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376d9b1f95da7a0dddc8a2eb769d45ebe107f4697f73aa5ca32d47ef98da5f9a`  
		Last Modified: Tue, 12 Mar 2024 13:00:07 GMT  
		Size: 68.9 MB (68941641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866180a44f3b35cefae57b78e94e3871272cd41db4c5c737ca4427cf3be0cc9c`  
		Last Modified: Tue, 12 Mar 2024 13:00:09 GMT  
		Size: 68.4 MB (68387253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69243421c6084b67b56c9849c01faf7731d2531b77aaa8cb49d3e1cf2e2bc20`  
		Last Modified: Tue, 12 Mar 2024 12:59:58 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

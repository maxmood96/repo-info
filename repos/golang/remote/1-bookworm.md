## `golang:1-bookworm`

```console
$ docker pull golang@sha256:925fe3fa28ba428cf67a7947ae838f8a1523117b40e3e6b5106c378e3f97fa29
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
$ docker pull golang@sha256:03082deb6ae090a0caa4e4a8f666bc59715bc6fa67f5fd109f823a0c4e1efc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299474573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4ed86491a49bc887be0382d454058ab30887445728dd1fdb346ebc69395fe9`
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
# Tue, 06 Feb 2024 23:26:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.22.0
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
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
	-	`sha256:07ba5748a60099d68b45e3e85013323e77199959a82e59e519161be344cd7009`  
		Last Modified: Tue, 13 Feb 2024 13:08:36 GMT  
		Size: 69.4 MB (69361086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef5d6b83255c5dc7d0be6f555197ec958db9975e47cfa992e6e858ff2485bd4`  
		Last Modified: Tue, 13 Feb 2024 13:08:24 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:a7bacc8536138031835c896949a4e7b850fe551c02c714f4937e32a347938006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260259374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953b5bf75e51ea430d0922d3810f1ef9ee8927b4c988c2be03c36ff66e94df3f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:19:48 GMT
ADD file:9b07e306d84beed6568160f3e02cfd7537add7bed5debf00f251fee99a50ee80 in / 
# Tue, 13 Feb 2024 01:19:49 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:14:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 23:26:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.22.0
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:84ee7bddcb1a35ae933efe6113f47b4047fb90d2a626c4a8a93e3548fa8b61d5`  
		Last Modified: Tue, 13 Feb 2024 01:26:22 GMT  
		Size: 45.2 MB (45153612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e6fa0e83f7c31cdfb8e77c4a8229243dc182cac7b985200c404bddc6e2bc9d`  
		Last Modified: Tue, 13 Feb 2024 04:26:58 GMT  
		Size: 22.0 MB (21950325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc5ce3fd388c71fe9b8c5fd1ab13a73a9257e22d4d7127d4bb59672159f2c27`  
		Last Modified: Tue, 13 Feb 2024 04:27:23 GMT  
		Size: 59.2 MB (59212948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005a7bfe39765f8d5e4217de773710199ce7e0e67508956a9f89f4e44fd315c5`  
		Last Modified: Tue, 13 Feb 2024 17:19:58 GMT  
		Size: 66.2 MB (66233573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e78b7906fbe5615fd0dd019b95657e06629e30bbd461bdba271a6c59d69b03b`  
		Last Modified: Tue, 13 Feb 2024 17:20:03 GMT  
		Size: 67.7 MB (67708709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95120591d0a90c9ab5f521eaa9ea1b3b79887a8088641e5f76051389a21a299c`  
		Last Modified: Tue, 13 Feb 2024 17:19:49 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:bcd9afabb11afca65005f10dcee5c818162b1a0ee3c0d55fe2426abd1f8e2a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289839448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbeef2f2690917b347a6bc06aef96b4480907e55a2f079a207066c305cf92a0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:37:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 23:26:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.22.0
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603ae72c83b17aae41ce6857f0063bfd35b5f00dc5d7e1ad47fa18debb28b2c7`  
		Last Modified: Tue, 13 Feb 2024 01:46:49 GMT  
		Size: 64.0 MB (63990920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23d83702b673f096f3ad08d6fd0e17210ca2820cc17e8200245f59d0673551f`  
		Last Modified: Tue, 13 Feb 2024 10:37:03 GMT  
		Size: 86.4 MB (86408876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64f8be2f5605845877a9fa07d02f4e446d47bf5eacd419b6f8c50dcfa51cf85`  
		Last Modified: Tue, 13 Feb 2024 10:37:02 GMT  
		Size: 66.3 MB (66265714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056502cbc32b718fd7404acbc281be34cf53ab4f8088a500577ad81b17155f87`  
		Last Modified: Tue, 13 Feb 2024 10:36:53 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:eb365ffb1fb05e1072391f90ef00cfebfc93662165216593ccc76ffdf8ed9170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298567738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039ff5142ded71424558ac108810943145a790e8dce4222a2312541a0af1f201`
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
# Tue, 06 Feb 2024 23:26:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.22.0
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
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
	-	`sha256:e457d5a1694ef74e23acfb908c7f6ed2879f6fc2252225f40f68881cb63074c4`  
		Last Modified: Tue, 13 Feb 2024 15:12:46 GMT  
		Size: 67.3 MB (67345051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e9d05783d207c08ff58895bcb1d908dc705710c25425ebd24f22ad9bbc4076`  
		Last Modified: Tue, 13 Feb 2024 15:12:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:15c0c00c2e4650e553d0e9978a6b0ebb4057f0a8a760aeddfea96653e4175869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (269996621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8b86896e998ea6c7aadf49f942430cfe134572cfdb9e6c5cb4e53ad7a37070`
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
# Tue, 06 Feb 2024 23:26:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.22.0
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
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
	-	`sha256:dbb8a37f0dd64c872361af828007812be328d55fbc38b610836dea54233375bd`  
		Last Modified: Tue, 13 Feb 2024 20:36:28 GMT  
		Size: 64.1 MB (64103754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bdb1e2e3206ff0b74923f3981242e1629b31b2e06f33f252ff0ddb703a8083`  
		Last Modified: Tue, 13 Feb 2024 20:35:36 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:518871c2ccfc75e32cdc3a792e5398e5deea2c58d5b54d64f8b6bb4a9772d57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305616510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768e4bd7007267afc2a3809a041a0a51196e3d3e18320bdefa676cb8bf11c08c`
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
# Tue, 06 Feb 2024 23:26:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.22.0
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
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
	-	`sha256:17dcaee1446b6f3d94394f77291865bb4c63aeaf6a4ff63639cedd08cee035c3`  
		Last Modified: Tue, 13 Feb 2024 11:29:13 GMT  
		Size: 66.4 MB (66422855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a268a9d2ea39a1c2800ad37f4c7900f4fd17382bd02717d5a4bea9323e536c15`  
		Last Modified: Tue, 13 Feb 2024 11:29:01 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:822fe7acfebbbc595187c00868778e5cb76568847eea47165500f1bf3fbaa536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272414468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3faca9a214342e84adea7b683dff3c5b4d0bba452ebe014bc7ea54029a81f3e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:00:04 GMT
ADD file:1d9e47125f6551ab7fe22f20edbc4adcadd5218dbdfb7a047c97e717d6324a3b in / 
# Tue, 13 Feb 2024 01:00:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:22:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:23:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 23:26:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.22.0
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:da89920af3bd14aecc5a727fd1657da55be3de461026b5a06f2322c69a889fe3`  
		Last Modified: Tue, 13 Feb 2024 01:30:04 GMT  
		Size: 47.9 MB (47916307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a7259cfb8e3f88b1fd49291d1b3b2ce3eb21ddd5e75fbca62acb55fc9a57a6`  
		Last Modified: Tue, 13 Feb 2024 02:58:04 GMT  
		Size: 24.0 MB (24043419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1569134e3a5ad21d93140cc90cb238f68c3103130b0189522d194e045a7fa520`  
		Last Modified: Tue, 13 Feb 2024 02:58:19 GMT  
		Size: 63.1 MB (63126343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de86f4bf40069bdd2e03b6e2feb5e9c2036eb029bf850ac80182793a34b32a8`  
		Last Modified: Tue, 13 Feb 2024 12:02:42 GMT  
		Size: 68.9 MB (68941784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f50d95e6fcd7058ff0d9b853a27c6fcf90b6d537864f58aadd21fb95c7307dd`  
		Last Modified: Tue, 13 Feb 2024 12:02:44 GMT  
		Size: 68.4 MB (68386408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f877a07461d7dd375147d680cc8548fd3ecb0a55f30ffeca71d2cf7b44bdf9a`  
		Last Modified: Tue, 13 Feb 2024 12:02:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

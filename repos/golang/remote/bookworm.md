## `golang:bookworm`

```console
$ docker pull golang@sha256:52b1be543b70d020a1d6d63ccf81f40fdcb016e064efb807085d8e87b252534d
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

### `golang:bookworm` - linux; amd64

```console
$ docker pull golang@sha256:3db3999ce82f443c0aa6b8da50d8ecea2df945dcf2a78101aff57d2f61f83969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299448257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099c470ec840e8887d76f4c15e87efe549189a6bc94484f64d0bc861c8401c96`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:53:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Apr 2024 16:03:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 16:03:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 16:03:48 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f899db30843f8330d5a40d1acb26bb00e93a9f21bff253f31c20562fa264767`  
		Last Modified: Tue, 12 Mar 2024 06:02:43 GMT  
		Size: 64.1 MB (64140360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29f45468664d54091f4fe86895cf8a9ab9ca18dbd217ae87f4666b09f942fa1`  
		Last Modified: Tue, 12 Mar 2024 16:04:46 GMT  
		Size: 92.4 MB (92374620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1c83bd2b9a89bc4c863400c5520c7d7f498489844d55b771e6dbc175553d8a`  
		Last Modified: Wed, 03 Apr 2024 16:59:26 GMT  
		Size: 69.3 MB (69334141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f093284a449ae97444b9d4472d556d53ea4b765a83a94c5edbfe66278496d9e0`  
		Last Modified: Wed, 03 Apr 2024 16:59:15 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:012f88e72e9e7f53db3b641b254a8240b8841ec480fb6febf6c77f6321e72a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260265490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066026d8d672cfa1692ed81a9edcf0d846a8c28489e88e63999d78437f9df46d`
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
# Wed, 03 Apr 2024 16:03:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 16:03:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 16:03:48 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
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
	-	`sha256:dce1c7f2b71827cde6f4900b2108a560363903f2b8a5716525b621c0a64afb45`  
		Last Modified: Wed, 03 Apr 2024 17:00:40 GMT  
		Size: 67.7 MB (67714383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f093284a449ae97444b9d4472d556d53ea4b765a83a94c5edbfe66278496d9e0`  
		Last Modified: Wed, 03 Apr 2024 16:59:15 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:85e4d8edfff508cc62dc53196303e2ad5e2f28d51b9a5d7691e4362837704734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289848927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824aa3c1d42cdad43ab6513830466315ccf281e8e1ca3f7a4af1c38585712734`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:22:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:22:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Apr 2024 16:03:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 16:03:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 16:03:48 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421c44fab18bc9f4c62ca481e074d50b3a036e7c95c7607b6d036c34d67c5264`  
		Last Modified: Wed, 10 Apr 2024 04:32:17 GMT  
		Size: 64.0 MB (63990996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbe4bb4a0d8b43491c9cd09a1939fa98f6e0c6bb41b83b515758995342fc910`  
		Last Modified: Wed, 10 Apr 2024 13:33:59 GMT  
		Size: 86.4 MB (86408724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7b295dfee595cac7b77431a3c81dba172a0582f59e4603fcfaf178f88ac260`  
		Last Modified: Wed, 10 Apr 2024 13:33:59 GMT  
		Size: 66.3 MB (66269867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7318f984ad5d530058907ecd2f58af8f0b40ab4d227184a84491c13581155285`  
		Last Modified: Wed, 10 Apr 2024 13:33:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bookworm` - linux; 386

```console
$ docker pull golang@sha256:a7d9a11c284261aee84988c97d73ed23906ce270bf99ce1d1450838486169115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298567028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a583ae4f2c67caee0e7775e6c837d576bb7b557f4887e55fa15a82a2ef45fb94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:47 GMT
ADD file:4cc8d7cc52399e70fff26562034447d71192cc79b9dac9551bce3f3046ba905a in / 
# Tue, 12 Mar 2024 00:57:48 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:40:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Apr 2024 16:03:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 16:03:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 16:03:48 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:76c347d52f9093273e46a420ef3def7fbe603accb8533dbef53629d661d7d464`  
		Last Modified: Tue, 12 Mar 2024 01:02:18 GMT  
		Size: 50.6 MB (50581859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58451b255cbefff55ab1d06e4d8396e373e8deb00528e5b8f44a5575cb35e8a7`  
		Last Modified: Tue, 12 Mar 2024 07:53:20 GMT  
		Size: 24.9 MB (24884854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b4d1d8db8595667983f0b51d60745145d3d1fcfc8619838a6c2544bf9e75fb`  
		Last Modified: Tue, 12 Mar 2024 07:53:44 GMT  
		Size: 66.0 MB (65986890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff171e64afcdf8f68b17c2d8a965f18a01f01681901e6cc99c65ab1261cad0ab`  
		Last Modified: Tue, 12 Mar 2024 18:21:42 GMT  
		Size: 89.8 MB (89769193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bcae051efc415516d5c641a069c3a4f8446914746258fd4153c069a51b59f20`  
		Last Modified: Wed, 03 Apr 2024 17:00:17 GMT  
		Size: 67.3 MB (67344025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b44305ce8be245e5f37f094e633c311755eb6296c802d724288e7de2e66c31`  
		Last Modified: Wed, 03 Apr 2024 16:59:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:658fc239e9eec839fa1b5ef05c646337822501c641343dcb31ced0fbef0382d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (270002546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166b1f7d636022915f104858f7501423fe1a7b8a7eaa70811d4e3739bf2e4e1a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:05:38 GMT
ADD file:4d32a17a925fe03541568abf911d846953d3660b326987a74427b0262134b3c6 in / 
# Tue, 12 Mar 2024 01:05:41 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:05:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Apr 2024 16:03:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 16:03:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 16:03:48 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a1888556fef8803d385bcda912bec552fdbf67dbab0adac6cadf266d746cca55`  
		Last Modified: Tue, 12 Mar 2024 01:16:25 GMT  
		Size: 49.6 MB (49563114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f64944212b4456db3039905773dd6dea4c4590560c38ae7716d5dfa12559e8`  
		Last Modified: Tue, 12 Mar 2024 02:41:43 GMT  
		Size: 23.6 MB (23630647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638fdd2230a0e3b195fa0e78e24eb4739e6c5ad8a94c3bb93aedbaf4fad008ca`  
		Last Modified: Tue, 12 Mar 2024 02:42:36 GMT  
		Size: 63.0 MB (62965889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365bc8351f6d18343711b7f0dbd1f883316f793a25f384be825519cefa76848e`  
		Last Modified: Tue, 12 Mar 2024 19:46:20 GMT  
		Size: 69.7 MB (69732738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d257ced73e7c6a3822c88aa6ee95d640c9c76b0bebd8965fb63bdca6aacbb59`  
		Last Modified: Wed, 03 Apr 2024 17:04:10 GMT  
		Size: 64.1 MB (64110000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf50e09713fbec9736e987f41a4458de0a72d4d0793cc9f2c380e6f68daeb4da`  
		Last Modified: Wed, 03 Apr 2024 17:03:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:ebe06dd6251892d739a25ad292290fbee191d75177dc397a24c0a2df32b33099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305623207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5b872daadf06afd000258369b46c81294d37bd4a725f1a3e3f9ac858ce87ea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:29:51 GMT
ADD file:c5929f4b94168a6c2b67522cc5aea49aef7e290fc5c328f387523a3d16154100 in / 
# Tue, 12 Mar 2024 00:29:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Apr 2024 16:03:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 16:03:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 16:03:48 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ace76237e931cd48dae2ec361ac06fa249ce4c2877f599ed74f188ca39974407`  
		Last Modified: Tue, 12 Mar 2024 00:37:38 GMT  
		Size: 53.6 MB (53556955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30711853e1103e2a5ce889e2b171af6e0587cbe00d19b777a831e8e78143df`  
		Last Modified: Tue, 12 Mar 2024 02:19:58 GMT  
		Size: 25.7 MB (25696864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7f6b2d513138ada95189d6b9402e50953a70524968e742ada51774c5f48fd0`  
		Last Modified: Tue, 12 Mar 2024 02:20:20 GMT  
		Size: 69.6 MB (69581899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bca79b8df9f4b69785a12d3b8445b65a0986bb752052ca3a56eb1984046b70`  
		Last Modified: Tue, 12 Mar 2024 15:23:02 GMT  
		Size: 90.4 MB (90360116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b5a2f8425fdfa08985c31d89abe77cd8c3d333bc0b952fe90788bed7131491`  
		Last Modified: Wed, 03 Apr 2024 17:03:17 GMT  
		Size: 66.4 MB (66427166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498f9c83fcce7fe9d0d2aa169c3b8229583ad1361d80d8315e25ac1584355758`  
		Last Modified: Wed, 03 Apr 2024 17:02:55 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bookworm` - linux; s390x

```console
$ docker pull golang@sha256:1271148707ac00508b2e4ba492e6d782218bbc86bf87da61d350e9036cbb724c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272420353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b053edfdaff79b38a1a227e2172cc89d020c3eb1d23b2d352c296f87304426`
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
# Wed, 03 Apr 2024 16:03:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 16:03:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 16:03:48 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
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
	-	`sha256:fb7da68500ad669e4068696f2df549edeb5e51ddb98a8822b6d6f6e33aa70ddc`  
		Last Modified: Wed, 03 Apr 2024 17:27:57 GMT  
		Size: 68.4 MB (68391679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480b64f8bb19fae105679fa88a0320b6083953166ac53e727804ddfb5a256508`  
		Last Modified: Wed, 03 Apr 2024 17:27:44 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `golang:1-bullseye`

```console
$ docker pull golang@sha256:d737c922b6c45c66e5b25dafff3b867870eb8f423bfa85e3c7b79aafc7d6ce9d
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

### `golang:1-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:4ff32e92534a75df6b47bce4e5a4678bcd8fbb76805c647e0e855c60f0ce9641
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278592289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380c110c562bc167e57135ce31b07610f161592626095aa0d53c8b3c3b062ff2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:37:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:28:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:28:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 15:29:32 GMT
ENV GOLANG_VERSION=1.21.6
# Thu, 11 Jan 2024 15:29:41 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.6.linux-mips64le.tar.gz'; 			sha256='eb309a611dfec52b98805e05bafbe769d3d5966aef05f17ec617c89ee5a9e484'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		go version
# Thu, 11 Jan 2024 15:29:42 GMT
ENV GOTOOLCHAIN=local
# Thu, 11 Jan 2024 15:29:42 GMT
ENV GOPATH=/go
# Thu, 11 Jan 2024 15:29:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 15:29:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 11 Jan 2024 15:29:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c23b7d6528239a16f11d6e650e9a9fdb7039721df42b6ca01777fe34c2b116`  
		Last Modified: Thu, 11 Jan 2024 04:45:57 GMT  
		Size: 54.6 MB (54601205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de87067350268be51f2c816aad697b479a7e9d2499dedbfaa1c8ed04fa48a774`  
		Last Modified: Thu, 11 Jan 2024 15:31:22 GMT  
		Size: 86.1 MB (86106422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2de350d87eb8d7cca4b0b4e817b34fdb90591d36d4e9588441f83c3b85c767`  
		Last Modified: Thu, 11 Jan 2024 15:32:09 GMT  
		Size: 67.1 MB (67061671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4c2ddd1854e7382192afeced7b3fe732a9e370e2dc40b041e3af54c8ad817e`  
		Last Modified: Thu, 11 Jan 2024 15:31:58 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:5b887e8f14137fd9c5107a2cec8c6d7b8a9af5e1f41028ed25a5e259f9a5f2cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246288256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cce0db7b0eec400b2a4767d1a91bffab572ac8d58b6befdf1b7fb84f6360e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:07:59 GMT
ADD file:3b623bed8ec2536cb513edda1de6f79d2c8e06d6f82df2543202544dbba3ae3e in / 
# Tue, 19 Dec 2023 02:08:00 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:57:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:57:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 16:42:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 16:42:45 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:58:05 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:58:23 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.6.linux-mips64le.tar.gz'; 			sha256='eb309a611dfec52b98805e05bafbe769d3d5966aef05f17ec617c89ee5a9e484'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		go version
# Tue, 09 Jan 2024 22:58:25 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:58:25 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:58:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:58:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:58:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1b42212018867046767b36eb95cf15c4b66bbb7b4fb552aab446d9822de5765c`  
		Last Modified: Tue, 19 Dec 2023 02:12:11 GMT  
		Size: 50.2 MB (50215775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344f6b88eeb188b9948991d7a318480a17a477fd684c6fbdc230ad9a217fed92`  
		Last Modified: Tue, 19 Dec 2023 08:07:28 GMT  
		Size: 14.9 MB (14880518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36372cf5bdff61f93cd6e14b66d2512eebf0c58b08179f661fbb89bdd34a5ca`  
		Last Modified: Tue, 19 Dec 2023 08:07:48 GMT  
		Size: 50.4 MB (50353358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605ee73edc21a02eeb84ffd3f8ab8d544abd3edff6418e3a189407a9e58862e5`  
		Last Modified: Tue, 19 Dec 2023 16:44:45 GMT  
		Size: 65.0 MB (65006369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50377c3730f0369ccfa5966dcf60247bfd01d80c7b02b67d24840fb4d346998`  
		Last Modified: Tue, 09 Jan 2024 23:09:09 GMT  
		Size: 65.8 MB (65832080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22ef9a8d91e3682685dbea13168fb1ea447ee0caf8198719fe08f045cd6dc64`  
		Last Modified: Tue, 09 Jan 2024 23:08:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:741756d6aa27527344aff1c7fa2c4d0b82592ef5ca596c77bcf8a533b192415d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269832452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d197c85b9867da5ce04af3813ee567d7f072ad43b42ab607e2d55701615bf24`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:26:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 09:26:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 11:59:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 11:59:14 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 11:59:40 GMT
ENV GOLANG_VERSION=1.21.6
# Thu, 11 Jan 2024 11:59:48 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.6.linux-mips64le.tar.gz'; 			sha256='eb309a611dfec52b98805e05bafbe769d3d5966aef05f17ec617c89ee5a9e484'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		go version
# Thu, 11 Jan 2024 11:59:49 GMT
ENV GOTOOLCHAIN=local
# Thu, 11 Jan 2024 11:59:49 GMT
ENV GOPATH=/go
# Thu, 11 Jan 2024 11:59:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 11:59:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 11 Jan 2024 11:59:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebf2a961043d6b9dd703d0a485e216a2e302edf2e2525f7f410987d26905e71`  
		Last Modified: Thu, 11 Jan 2024 09:35:03 GMT  
		Size: 15.8 MB (15750711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826044e8ec1545c4af5dfe71ab63bce600198330f150aa968074bb86e78cd154`  
		Last Modified: Thu, 11 Jan 2024 09:35:17 GMT  
		Size: 54.7 MB (54699869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0fb7ee31baa7e44957ea0303c1098b92a53f16194573919483f3e2c29d2cde`  
		Last Modified: Thu, 11 Jan 2024 12:01:15 GMT  
		Size: 81.5 MB (81512680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88557adeebaeeb0d637fb048148b6fccd70d23d11ca7f285ac7df417335f5125`  
		Last Modified: Thu, 11 Jan 2024 12:02:13 GMT  
		Size: 64.2 MB (64161189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00968e69b0994e46f6e3c0497be2bffbed6046f22bc930ff3b91c2ef88fcd719`  
		Last Modified: Thu, 11 Jan 2024 12:02:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; 386

```console
$ docker pull golang@sha256:811f79bc90adbb328f3fcd64d3cfe2dec2c29170a316ae67b2ddd618e438b354
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281276930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bc3c6ccd7f8900a1fb3b86b40c13acb2905b31cc09807805d393f66d7a50a1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:19 GMT
ADD file:8a328fced7ae3a6fc868bbb95c23191103e595c9d22b2626c16f155bc48b51a8 in / 
# Tue, 19 Dec 2023 01:39:20 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:26:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:27:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Dec 2023 00:49:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Dec 2023 00:49:01 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:38:50 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:39:02 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.6.linux-mips64le.tar.gz'; 			sha256='eb309a611dfec52b98805e05bafbe769d3d5966aef05f17ec617c89ee5a9e484'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		go version
# Tue, 09 Jan 2024 22:39:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:39:03 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:39:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:39:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:39:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a789657fd5416b1ccfd519597a8f5e57bd5a80d04d1b1b7b2770df4469f4dd44`  
		Last Modified: Tue, 19 Dec 2023 01:44:07 GMT  
		Size: 56.0 MB (56046336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0386e6c873ad0aec679cfb967e1449dc2223a2543dd9923e9491c8d4dfe25ff9`  
		Last Modified: Tue, 19 Dec 2023 03:37:37 GMT  
		Size: 16.3 MB (16268921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a344c33a496f0c80e861246ac1b15db106b888d28c7bb89d17b87d06a5f1abc`  
		Last Modified: Tue, 19 Dec 2023 03:37:57 GMT  
		Size: 55.9 MB (55937182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842f62680c57f4b8e2f610fd0370db6f3356b5b4f5f03631850e68dc87cf1e8d`  
		Last Modified: Wed, 20 Dec 2023 00:51:24 GMT  
		Size: 87.5 MB (87502903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c971a57a0c1e536f5ed9f7cddf4b55b72dc5e34123becfbad819bf6060e4e93b`  
		Last Modified: Tue, 09 Jan 2024 22:48:02 GMT  
		Size: 65.5 MB (65521433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a428451fa05e9ff07f44d1e8cddc769ef8b900b81eddc975f6a88f0918f519d`  
		Last Modified: Tue, 09 Jan 2024 22:47:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; mips64le

```console
$ docker pull golang@sha256:2448aea83fd9a22dc5e6301ab4f7831a8b0eeeb463ebacf0e232f122966a6cb3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251277715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3148660433e1d72dc51c32bd3abccd17d3decbebc1abdd913d0258b40dd0c8c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:14:09 GMT
ADD file:95472c5be6ea30c4b6d715a3000e1bafb8e371897a96c9115040c4a7d2bb2c80 in / 
# Tue, 19 Dec 2023 02:14:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:59:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Dec 2023 13:44:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Dec 2023 13:44:38 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:09:32 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:10:21 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.6.linux-mips64le.tar.gz'; 			sha256='eb309a611dfec52b98805e05bafbe769d3d5966aef05f17ec617c89ee5a9e484'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		go version
# Tue, 09 Jan 2024 22:10:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:10:35 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:10:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:10:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:10:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4d8f97806f78898e256ac429d0634dfcccbd6f6e81547afde1469a5968e33b18`  
		Last Modified: Tue, 19 Dec 2023 02:25:21 GMT  
		Size: 53.3 MB (53289008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6729089c3e56fc6fa74aeb41283960af5e717a1e32232fb0de332e8b8393fc37`  
		Last Modified: Tue, 19 Dec 2023 03:22:13 GMT  
		Size: 15.5 MB (15530289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e24f65044fa0f3a3c6a2bf5c15dd5d639173537bdcd52919cfc676d1bbd685`  
		Last Modified: Tue, 19 Dec 2023 03:22:58 GMT  
		Size: 53.3 MB (53302689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30693ee91c40eb677431969f49a13f47517ab110d1fe43e7de5656e08f70d9ae`  
		Last Modified: Wed, 20 Dec 2023 14:14:01 GMT  
		Size: 67.0 MB (66953727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d320799bbe04fa829b1f649663db293f847f804ab0119911c1d02a32fb4e71`  
		Last Modified: Tue, 09 Jan 2024 22:39:08 GMT  
		Size: 62.2 MB (62201876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073b33903a48a3aeb8c27cb297ee576bc26b46fec8a463ecd57287e5887c5afe`  
		Last Modified: Tue, 09 Jan 2024 22:38:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; ppc64le

```console
$ docker pull golang@sha256:a3ba9149b8c21a927c17225bcbb77dda0e6f961bf53c0ea799a7cb128a52441d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279325399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968a817b03e52f9c0d49117bbd89be212c65d3d9796a6e2a9f8b69f98e7207bd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:41 GMT
ADD file:cb900134161e1d051fb57c4a488efa9478959953f2773baa8a90b13198589a81 in / 
# Thu, 11 Jan 2024 02:34:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 07:08:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:53:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 15:54:22 GMT
ENV GOLANG_VERSION=1.21.6
# Thu, 11 Jan 2024 15:54:42 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.6.linux-mips64le.tar.gz'; 			sha256='eb309a611dfec52b98805e05bafbe769d3d5966aef05f17ec617c89ee5a9e484'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		go version
# Thu, 11 Jan 2024 15:54:46 GMT
ENV GOTOOLCHAIN=local
# Thu, 11 Jan 2024 15:54:47 GMT
ENV GOPATH=/go
# Thu, 11 Jan 2024 15:54:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 15:54:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 11 Jan 2024 15:54:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1b9340c192fedc0211d4cda28f7a01e9ff3be108c42783e576f4a366c373f30b`  
		Last Modified: Thu, 11 Jan 2024 02:39:48 GMT  
		Size: 58.9 MB (58929662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764e705cb61758280364899cd162b2510b2a119833c02f501318b83950af12d2`  
		Last Modified: Thu, 11 Jan 2024 07:24:33 GMT  
		Size: 16.8 MB (16767158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1974dca40db9a6f34527c91c9763d250d18f0d45ff29c835a706bf5dab4025b`  
		Last Modified: Thu, 11 Jan 2024 07:24:52 GMT  
		Size: 58.9 MB (58874114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b205d4d389844f9a5f21d6bf7745ffefe4d9e73fd815b67671bc9b239b7dddc2`  
		Last Modified: Thu, 11 Jan 2024 15:57:17 GMT  
		Size: 80.6 MB (80564572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f62575163a0f657f3f4ff54291f3653ca0e5d0589506f4d79d01212df849f7e`  
		Last Modified: Thu, 11 Jan 2024 15:58:08 GMT  
		Size: 64.2 MB (64189738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4b5a19d723fa8d80970678d1013dd59aee0c28006dcf24378e509a808bd175`  
		Last Modified: Thu, 11 Jan 2024 15:57:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; s390x

```console
$ docker pull golang@sha256:bcb3c575834605bc227cd4622dcc6684afcf1f103c37a57af4dc57a1e0a03244
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255100935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1213f4cd01616d99431cf9e4c3569d12e4a830421ab4c1c3d34d89a4b3ef5076`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:45:23 GMT
ADD file:9ddcb5238e539e3b1fd8032aecf5e40f0b8b8162e6d045fcd58520db01e93296 in / 
# Thu, 11 Jan 2024 01:45:28 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:11:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 02:11:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:37:07 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 08:38:18 GMT
ENV GOLANG_VERSION=1.21.6
# Thu, 11 Jan 2024 08:38:32 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.6.linux-mips64le.tar.gz'; 			sha256='eb309a611dfec52b98805e05bafbe769d3d5966aef05f17ec617c89ee5a9e484'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		go version
# Thu, 11 Jan 2024 08:38:39 GMT
ENV GOTOOLCHAIN=local
# Thu, 11 Jan 2024 08:38:39 GMT
ENV GOPATH=/go
# Thu, 11 Jan 2024 08:38:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 08:38:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 11 Jan 2024 08:38:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a1442bb0c8abfd050e8bdb2270126c2f24402a8c57a00f8229c40c2a35253665`  
		Last Modified: Thu, 11 Jan 2024 01:51:04 GMT  
		Size: 53.3 MB (53296125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d30f97393df8af87413ca6aa015986e13ab489522ffe9a065961b2ed0f9352`  
		Last Modified: Thu, 11 Jan 2024 02:22:01 GMT  
		Size: 15.6 MB (15642723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb0e4599f9ae7a417945830efb8a901aff78d46ca9cfb95700e3b83352b2211`  
		Last Modified: Thu, 11 Jan 2024 02:22:15 GMT  
		Size: 54.1 MB (54070654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa180744e3589670af7d644ed8f5355f61aaf6729e5e452a268472fb2f9e582`  
		Last Modified: Thu, 11 Jan 2024 08:41:08 GMT  
		Size: 65.8 MB (65806738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23040f14f7214b982f0fd183fc6a5d5e569637ecbc0aba1f31a46c3ae308047f`  
		Last Modified: Thu, 11 Jan 2024 08:41:49 GMT  
		Size: 66.3 MB (66284539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ef85f1b1290a4e7a9fd7bcec186acc2281052d44885123b3b96ab98b24e611`  
		Last Modified: Thu, 11 Jan 2024 08:41:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

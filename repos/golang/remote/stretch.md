## `golang:stretch`

```console
$ docker pull golang@sha256:4d5642e6a51404768ca4d91bd5028e7e8ac2611861c011a48baa77257cf51651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `golang:stretch` - linux; amd64

```console
$ docker pull golang@sha256:8b6b86e45c7847fea9cf401da52e41747cfb18bbfb4aebe924b4ef13a3366521
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (292033335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e9f45ffc3ed969832431f2d5bfc29fdc3e69d9a303ad363cfbfe5b1c551128`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 06:33:25 GMT
ADD file:13031623172f5c5857e27de93553adedf17d955fa370882f850bb6ed6fb8cee7 in / 
# Fri, 15 May 2020 06:33:25 GMT
CMD ["bash"]
# Fri, 15 May 2020 17:43:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 17:43:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 May 2020 17:44:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 May 2020 08:15:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Jun 2020 01:30:00 GMT
ENV GOLANG_VERSION=1.14.4
# Tue, 02 Jun 2020 01:30:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='aed845e4185a0b2a3c3d5e1d0a35491702c55889192bb9c30e67a3de6849c067' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='e20211425b3f797ca6cd5e9a99ab6d5eaf1b009d08d19fc8a7835544fa58c703' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='05dc46ada4e23a1f58e72349f7c366aae2e9c7a7f1e7653095538bc5bba5e077' ;; 		i386) goRelArch='linux-386'; goRelSha256='4179f406ea0efd455a8071eaaaf1dea92cac5c17aab89fbad18ea2a37623c810' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='b335f85bc935ca3f553ad1bac37da311aaec887ffd8a48cb58a0abb0d8adf324' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='17f2ae0bae968b3d909daabc5cc4a37471ddb70ec49076b78702291e6772d71a' ;; 		*) goRelArch='src'; goRelSha256='7011af3bbc2ac108d1b82ea8abb87b2e63f78844f0259be20cde4d42c5c40584'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 02 Jun 2020 01:30:12 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2020 01:30:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2020 01:30:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 02 Jun 2020 01:30:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1c6172af85ee14a8db5a3a51d406b768dfa94d196c06d0d06d591507cf8199f0`  
		Last Modified: Fri, 15 May 2020 06:40:31 GMT  
		Size: 45.4 MB (45375207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b194b0e3c928807cfabf081055a117585ba5bf6697f65b2fede02225a5d73ad2`  
		Last Modified: Fri, 15 May 2020 17:55:27 GMT  
		Size: 10.8 MB (10797475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ec00f35d5b2d1db6b8e925a3005c1a285365775028db0339903ddaeec4763`  
		Last Modified: Fri, 15 May 2020 17:55:29 GMT  
		Size: 4.3 MB (4340139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b1353672b6861da5f1b58b0eca02ec10373a25d2898bddafa1b4bae2271c55`  
		Last Modified: Fri, 15 May 2020 17:55:45 GMT  
		Size: 50.1 MB (50084198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9691b96ca72553a20f0ad56fa9f01e53041b4327bc0c34840f3e562d2883ce`  
		Last Modified: Sat, 16 May 2020 08:24:50 GMT  
		Size: 57.7 MB (57723884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b7c4d1a3018e09dc2b605343964d589cb412f377e073a315f4dc179670c4ed`  
		Last Modified: Tue, 02 Jun 2020 01:44:06 GMT  
		Size: 123.7 MB (123712306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a901fc86043a10139c390ba0a58f8af387feb7b663cea73e06fd38d2f57619`  
		Last Modified: Tue, 02 Jun 2020 01:43:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:stretch` - linux; arm variant v7

```console
$ docker pull golang@sha256:0381e235a8e1915f4b78f41679e4727d1aaa6ecbe40093516343ae6e94ff74ff
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249784858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdb413791e2cc697dd4826a02961b5f91680035474447d7eb30e59045bdbe11`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 01:06:22 GMT
ADD file:89db8453485648b09e63411b6e2ad84f08844ee55cb115e59cdc8c8cb1c29a1f in / 
# Fri, 15 May 2020 01:06:23 GMT
CMD ["bash"]
# Fri, 15 May 2020 10:48:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 10:49:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 May 2020 10:49:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 May 2020 00:46:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 May 2020 00:46:56 GMT
ENV GOLANG_VERSION=1.14.3
# Sat, 16 May 2020 00:47:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='1c39eac4ae95781b066c144c58e45d6859652247f7515f0d2cba7be7d57d2226' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='b1c3a648c3c8877b98dfba1996dec604c8fb8899db07994b2dfd47b0063367c8' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='a7a593e2ee079d83a1943edcd1c9ed2dae7529666fce04de8c142fb61c7cdd3e' ;; 		i386) goRelArch='linux-386'; goRelSha256='46f8c744788103e8aeceb12c7d71eb16a58fe43e7e4711055fa9ef4bae50bff7' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='329359e2b72839696e78b6c0a96fd939e28e7435d852f31107f68037dd5f7442' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='1aad312fc7fa85d663e8226237cc7519b2599b88a213098abc10de8e84d6cfab' ;; 		*) goRelArch='src'; goRelSha256='93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sat, 16 May 2020 00:47:21 GMT
ENV GOPATH=/go
# Sat, 16 May 2020 00:47:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 May 2020 00:47:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 16 May 2020 00:47:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:11acdea2de14253903f5970d63a2076ff08912929430d1c33afe617c9fa6bf8f`  
		Last Modified: Fri, 15 May 2020 01:14:46 GMT  
		Size: 42.1 MB (42104346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99452f66748f5df5d89d2287e42b5c3d87c9d5e1e20c16ef729e87d463840cf7`  
		Last Modified: Fri, 15 May 2020 11:01:44 GMT  
		Size: 9.5 MB (9498344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cef06b7abe4487657829b47c97bd2992f14a34349e0bcf60a47de9c647bd3fb`  
		Last Modified: Fri, 15 May 2020 11:01:43 GMT  
		Size: 3.9 MB (3918713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c542e1b5d6ef8c44b0708c5d2d73da1f5269186501aaee2b172d32a8b50d86c1`  
		Last Modified: Fri, 15 May 2020 11:02:04 GMT  
		Size: 46.4 MB (46413310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e0669792f2bafc58162fb1fe98159b1566e12b5f32e9b9a9e58c6ddb814096`  
		Last Modified: Sat, 16 May 2020 01:56:49 GMT  
		Size: 46.1 MB (46059889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b432308bb3bd9576cd1e4c54e6a455bbc2f182b95efa3e3a3f1a6fb288d8f3`  
		Last Modified: Sat, 16 May 2020 01:57:07 GMT  
		Size: 101.8 MB (101790100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5563b4a627ae7a541afa86ca4ddd2836f1eb7d0c47d7613699e986f50fc6f4`  
		Last Modified: Sat, 16 May 2020 01:56:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:stretch` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:797628071b8979b3b5dcb8e6e506b116b78ea3f24b0e189fb9a213cf3d80ba5f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 MB (255219942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94525dd5594a7d64075ab2c7bbccb6b3edda37cc914badfc6742fd64ad9164b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 12:48:07 GMT
ADD file:251053dbd1ce0b3744de3eecf53a3ef8ccf92ea509678e59800952c3dbd1b32c in / 
# Fri, 15 May 2020 12:48:09 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:13:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:13:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 May 2020 20:13:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 May 2020 11:37:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Jun 2020 01:53:50 GMT
ENV GOLANG_VERSION=1.14.4
# Tue, 02 Jun 2020 01:54:32 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='aed845e4185a0b2a3c3d5e1d0a35491702c55889192bb9c30e67a3de6849c067' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='e20211425b3f797ca6cd5e9a99ab6d5eaf1b009d08d19fc8a7835544fa58c703' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='05dc46ada4e23a1f58e72349f7c366aae2e9c7a7f1e7653095538bc5bba5e077' ;; 		i386) goRelArch='linux-386'; goRelSha256='4179f406ea0efd455a8071eaaaf1dea92cac5c17aab89fbad18ea2a37623c810' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='b335f85bc935ca3f553ad1bac37da311aaec887ffd8a48cb58a0abb0d8adf324' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='17f2ae0bae968b3d909daabc5cc4a37471ddb70ec49076b78702291e6772d71a' ;; 		*) goRelArch='src'; goRelSha256='7011af3bbc2ac108d1b82ea8abb87b2e63f78844f0259be20cde4d42c5c40584'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 02 Jun 2020 01:54:50 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2020 01:55:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2020 01:56:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 02 Jun 2020 01:56:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8e144e997aec62ed9c3bb1ff83ae2a62cbea252858abfb48ac60bb2078817a6c`  
		Last Modified: Fri, 15 May 2020 12:55:43 GMT  
		Size: 43.2 MB (43163052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163052fbe4313f145cec99e4a4a1a7cc17d923a69c5354de191ecb396ef2a210`  
		Last Modified: Fri, 15 May 2020 20:22:01 GMT  
		Size: 9.7 MB (9748415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1173269921f10e4e86f34bf51752d9013d60db88a02c2dd476d5b8116e417476`  
		Last Modified: Fri, 15 May 2020 20:22:00 GMT  
		Size: 4.1 MB (4094349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693886e01d5a56a275694733a4d7bcf3854ae8ad4f5f789561237999e3e58498`  
		Last Modified: Fri, 15 May 2020 20:22:23 GMT  
		Size: 48.0 MB (48035115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfcefd990ff900eee4dd762dd6eb4697562d193c1d943abcfc1dbb67a15ecc9`  
		Last Modified: Sat, 16 May 2020 11:50:53 GMT  
		Size: 49.1 MB (49131448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7142b61a2413ef13e9f6708a9d26a4221916be8e41892398dffe2a6f13d9d19`  
		Last Modified: Tue, 02 Jun 2020 02:29:14 GMT  
		Size: 101.0 MB (101047408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fe1ede4bc52e811bc056d736cdf7a4d065e6f77b1a1959bc7480d51caebf3f`  
		Last Modified: Tue, 02 Jun 2020 02:28:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:stretch` - linux; 386

```console
$ docker pull golang@sha256:3c42df066d94563a4c4820002d4c41ae3b8d35839a0ab0341542bf888d8f3b22
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280209508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092da0a2e3c176da5032ae35c6d953d01e955ad9163156c324ca5e91dbddc351`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 07:12:19 GMT
ADD file:22284e8c6e684308a95b18c7ed63ef235582dbb1890d1d02c22213e41ae47192 in / 
# Fri, 15 May 2020 07:12:19 GMT
CMD ["bash"]
# Fri, 15 May 2020 17:22:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 17:22:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 May 2020 17:22:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 May 2020 05:41:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Jun 2020 01:50:43 GMT
ENV GOLANG_VERSION=1.14.4
# Tue, 02 Jun 2020 01:51:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='aed845e4185a0b2a3c3d5e1d0a35491702c55889192bb9c30e67a3de6849c067' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='e20211425b3f797ca6cd5e9a99ab6d5eaf1b009d08d19fc8a7835544fa58c703' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='05dc46ada4e23a1f58e72349f7c366aae2e9c7a7f1e7653095538bc5bba5e077' ;; 		i386) goRelArch='linux-386'; goRelSha256='4179f406ea0efd455a8071eaaaf1dea92cac5c17aab89fbad18ea2a37623c810' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='b335f85bc935ca3f553ad1bac37da311aaec887ffd8a48cb58a0abb0d8adf324' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='17f2ae0bae968b3d909daabc5cc4a37471ddb70ec49076b78702291e6772d71a' ;; 		*) goRelArch='src'; goRelSha256='7011af3bbc2ac108d1b82ea8abb87b2e63f78844f0259be20cde4d42c5c40584'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 02 Jun 2020 01:51:03 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2020 01:51:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2020 01:51:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 02 Jun 2020 01:51:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ddf311fc69760572da5334a35e5a0e9fa15690ee1e40ed4b06e9a65213bc7223`  
		Last Modified: Fri, 15 May 2020 07:22:51 GMT  
		Size: 46.1 MB (46094205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b241dd4b1f1a808fb80049baea941ffeb595af14983b6e48560fc4d07b66cf54`  
		Last Modified: Fri, 15 May 2020 17:32:39 GMT  
		Size: 10.8 MB (10818399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a58f9666641b58144531065f83cb2bf8ae4fc7968332d0563612de804752c0`  
		Last Modified: Fri, 15 May 2020 17:32:36 GMT  
		Size: 4.6 MB (4561476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a5af2e44b2e93a8556c765c57f7a929c2e24ace22880ce91c76ebbdee145d4`  
		Last Modified: Fri, 15 May 2020 17:33:00 GMT  
		Size: 51.6 MB (51616873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7ce904eab5ddb7909f1286377aecb94fc955b337654d55d74c28976e0b21f4`  
		Last Modified: Sat, 16 May 2020 05:58:17 GMT  
		Size: 62.3 MB (62252528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d5c15cfa1d686651d3c5b2d4cbc8c3c19fc411f523b82e183b3e3369aa852b`  
		Last Modified: Tue, 02 Jun 2020 02:07:06 GMT  
		Size: 104.9 MB (104865901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b89583bf8841b27f8384d4d7c4891fc4973b7cd1a8450a7407f28c17e04c60e`  
		Last Modified: Tue, 02 Jun 2020 02:06:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:stretch` - linux; ppc64le

```console
$ docker pull golang@sha256:4055b5341ab97eb49f279cef220525648cada6b46f41b30d1aa8e670e3ae6e5e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262830333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c027c41db9f556d37411b3a5acb223ccae0b5744e4354a186860774c080f3451`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 22:39:29 GMT
ADD file:fa4c7e3ca04f092e53cc791a32c929663412df3f68de2733bb867053577bf1d1 in / 
# Wed, 13 May 2020 22:39:34 GMT
CMD ["bash"]
# Thu, 14 May 2020 00:08:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 00:08:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 00:10:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 18 May 2020 14:01:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Jun 2020 01:28:13 GMT
ENV GOLANG_VERSION=1.14.4
# Tue, 02 Jun 2020 01:28:42 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='aed845e4185a0b2a3c3d5e1d0a35491702c55889192bb9c30e67a3de6849c067' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='e20211425b3f797ca6cd5e9a99ab6d5eaf1b009d08d19fc8a7835544fa58c703' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='05dc46ada4e23a1f58e72349f7c366aae2e9c7a7f1e7653095538bc5bba5e077' ;; 		i386) goRelArch='linux-386'; goRelSha256='4179f406ea0efd455a8071eaaaf1dea92cac5c17aab89fbad18ea2a37623c810' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='b335f85bc935ca3f553ad1bac37da311aaec887ffd8a48cb58a0abb0d8adf324' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='17f2ae0bae968b3d909daabc5cc4a37471ddb70ec49076b78702291e6772d71a' ;; 		*) goRelArch='src'; goRelSha256='7011af3bbc2ac108d1b82ea8abb87b2e63f78844f0259be20cde4d42c5c40584'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 02 Jun 2020 01:28:50 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2020 01:28:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2020 01:29:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 02 Jun 2020 01:29:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7732483b686efe14a1cf8add89a1568b83892e243798fba30808f1fc6287210b`  
		Last Modified: Wed, 13 May 2020 23:02:10 GMT  
		Size: 45.6 MB (45646193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df33ef5c6dd4781defd528815174987b67a617a4fbddd5e5241a2f67a34098cb`  
		Last Modified: Thu, 14 May 2020 00:37:47 GMT  
		Size: 10.0 MB (10002565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02507bd450f72bbb529f56f9579bb7169fc9be7900bc5b9b0587e4855e51ad8d`  
		Last Modified: Thu, 14 May 2020 00:37:41 GMT  
		Size: 4.3 MB (4296673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a5abe5a03ebb35ed027af57237427bf1650677f1d4c6a907f88cf889b5e403`  
		Last Modified: Thu, 14 May 2020 00:39:16 GMT  
		Size: 50.1 MB (50081278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e35845be2adbaca215afc318bca5cf1b474868bed30baed157c6ca94ae0bd4a`  
		Last Modified: Mon, 18 May 2020 14:20:29 GMT  
		Size: 52.9 MB (52901557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93aa6f2108d06ceab917e77b8d9ba44fa8e8e6752d56e89544b710755bc4e27`  
		Last Modified: Tue, 02 Jun 2020 01:48:05 GMT  
		Size: 99.9 MB (99901911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52aca7e81fd0402d27377b82929d28d45cda8318ba303d26de8e8ca415b2f2ff`  
		Last Modified: Tue, 02 Jun 2020 01:47:21 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:stretch` - linux; s390x

```console
$ docker pull golang@sha256:f697678f142e0fd1df6ad0d167bdae97b8811dda478970ad5be2e031797e58ce
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261787493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5315cfd4892ea8091b3ed5363a25994ce4655116b702378713b00e0e25519249`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 14 May 2020 23:08:23 GMT
ADD file:32ad2f356c0ec407aa31085089417aaa9f72a5dc2757ed68a0adf7a432e4bdaa in / 
# Thu, 14 May 2020 23:08:26 GMT
CMD ["bash"]
# Fri, 15 May 2020 05:03:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 05:04:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 May 2020 05:04:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 11:29:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Jun 2020 01:52:43 GMT
ENV GOLANG_VERSION=1.14.4
# Tue, 02 Jun 2020 01:53:02 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='aed845e4185a0b2a3c3d5e1d0a35491702c55889192bb9c30e67a3de6849c067' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='e20211425b3f797ca6cd5e9a99ab6d5eaf1b009d08d19fc8a7835544fa58c703' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='05dc46ada4e23a1f58e72349f7c366aae2e9c7a7f1e7653095538bc5bba5e077' ;; 		i386) goRelArch='linux-386'; goRelSha256='4179f406ea0efd455a8071eaaaf1dea92cac5c17aab89fbad18ea2a37623c810' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='b335f85bc935ca3f553ad1bac37da311aaec887ffd8a48cb58a0abb0d8adf324' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='17f2ae0bae968b3d909daabc5cc4a37471ddb70ec49076b78702291e6772d71a' ;; 		*) goRelArch='src'; goRelSha256='7011af3bbc2ac108d1b82ea8abb87b2e63f78844f0259be20cde4d42c5c40584'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 02 Jun 2020 01:53:06 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2020 01:53:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2020 01:53:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 02 Jun 2020 01:53:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dc69489da20ae5bdf6cefc772e7ff8420ffbd2c920a57165de6ead66d1a997e4`  
		Last Modified: Thu, 14 May 2020 23:12:48 GMT  
		Size: 45.2 MB (45232081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fe5c3a82fe7eb310483d893dd90a653f2b29688e70bb3a0000e8c208de755b`  
		Last Modified: Fri, 15 May 2020 05:10:26 GMT  
		Size: 10.3 MB (10325875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4757a1c09293f132a58fe2f774191e2545fd945ba597ec8d9a399751180aeeb2`  
		Last Modified: Fri, 15 May 2020 05:10:25 GMT  
		Size: 4.4 MB (4372587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba95febc21c79324c26de8b0b5fd907b89a7799fd541030a61348f0fd2caf6f`  
		Last Modified: Fri, 15 May 2020 05:10:41 GMT  
		Size: 50.5 MB (50511235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9ea9a105379dcd08f8411ba786e6bd96d5230823b7a860a5953f6adbc335d4`  
		Last Modified: Fri, 15 May 2020 11:32:13 GMT  
		Size: 46.0 MB (46015657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e8d7a5fd210030a0db8abbbfa1f388a90ad21efb0091c79f8366505d5e5144`  
		Last Modified: Tue, 02 Jun 2020 02:00:57 GMT  
		Size: 105.3 MB (105329903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de349c95e56c34930ad42b81dc50de0e6a12717ad50f630fd32db7b01248332`  
		Last Modified: Tue, 02 Jun 2020 02:00:43 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

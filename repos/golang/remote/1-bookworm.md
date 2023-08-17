## `golang:1-bookworm`

```console
$ docker pull golang@sha256:640f192f24852cd875514e18a01977ae87692dca466abed7705ad3c4670b6993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `golang:1-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:12359f96c43077803959dab88ce60c87cd2543f3b907bf54a34a5104270f404f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.8 MB (296836889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434a1905832963ddddafdfb5a8f329a0c0b78a3529c99d57259f0888e0feb973`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:30 GMT
ADD file:3a6d159d80cb8abfacda5873c243a6ae635ff603708febc4df51f8eec26d3de7 in / 
# Wed, 16 Aug 2023 00:59:31 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 06:57:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 06:58:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 00:50:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 00:50:03 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 00:50:03 GMT
ENV GOLANG_VERSION=1.21.0
# Thu, 17 Aug 2023 00:50:11 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz'; 			sha256='d0398903a16ba2232b389fb31032ddf57cac34efda306a0eebac34f0965a0742'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.0.linux-armv6l.tar.gz'; 			sha256='e377a0004957c8c560a3ff99601bce612330a3d95ba3b0a2ae144165fc87deb1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.0.linux-arm64.tar.gz'; 			sha256='f3d4548edf9b22f26bbd49720350bbfe59d75b7090a1a2bff1afad8214febaf3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.0.linux-386.tar.gz'; 			sha256='0e6f378d9b072fab0a3d9ff4d5e990d98487d47252dba8160015a61e6bd0bcba'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.0.linux-mips64le.tar.gz'; 			sha256='92f7933d997c589b4f506c6b3cc5b27ff43b294c3a2d40bf4d7eeaf375f92afb'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.0.linux-ppc64le.tar.gz'; 			sha256='e938ffc81d8ebe5efc179240960ba22da6a841ff05d5cab7ce2547112b14a47f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.0.linux-riscv64.tar.gz'; 			sha256='87b21c06573617842ca9e00b954bc9f534066736a0778eae594ac54b45a9e8b7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.0.linux-s390x.tar.gz'; 			sha256='be7338df8e5d5472dfa307b0df2b446d85d001b0a2a3cdb1a14048d751b70481'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.0.src.tar.gz'; 		sha256='818d46ede85682dd551ad378ef37a4d247006f12ec59b5b755601d2ce114369a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Thu, 17 Aug 2023 00:50:11 GMT
ENV GOPATH=/go
# Thu, 17 Aug 2023 00:50:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 00:50:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 17 Aug 2023 00:50:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:de4cac68b6165c40cf6f8b30417948c31be03a968e233e55ee40221553a5e570`  
		Last Modified: Wed, 16 Aug 2023 01:04:06 GMT  
		Size: 49.6 MB (49557399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31b0195ec5f04dfc78eca9d73b5d223fc36a29f54ee888bc4e0615b5839e692`  
		Last Modified: Wed, 16 Aug 2023 07:12:39 GMT  
		Size: 24.0 MB (24030511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1fd34c30b75e7edb20c2fd09a9862697f302ef9ae357e521ef3c84d5534e3f`  
		Last Modified: Wed, 16 Aug 2023 07:12:59 GMT  
		Size: 64.1 MB (64112171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f744fb50e06fe7e56d42f6f0776b4b6041b65ef9435c1982e66d5a477047682`  
		Last Modified: Thu, 17 Aug 2023 00:51:57 GMT  
		Size: 92.3 MB (92267457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661ee9827c7b967875eb48447f68fc66ca426a6067f385d1ce553a927a20c8ff`  
		Last Modified: Thu, 17 Aug 2023 00:51:55 GMT  
		Size: 66.9 MB (66869196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5c1764d69475fa335ef99e53c3a89552eabb243701101eed02eb42d90220df`  
		Last Modified: Thu, 17 Aug 2023 00:51:44 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm variant v5

```console
$ docker pull golang@sha256:438dc2ecf4dc2dee0404ff9a98e36f0d075b8dfd1e1ab1f5fa02db732c64279e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.1 MB (271122955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428cc3ae3cec356e7227d9479d4f57c0b307ed3cf9c93cb43767eeedf2543c9c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:48:23 GMT
ADD file:f079a473284b30bb99c4a21c61719c499c0a305c49fedaa717bbfefef021b7fe in / 
# Tue, 15 Aug 2023 23:48:24 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:40:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 00:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 12:12:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 12:12:05 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 12:12:05 GMT
ENV GOLANG_VERSION=1.21.0
# Wed, 16 Aug 2023 12:14:15 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz'; 			sha256='d0398903a16ba2232b389fb31032ddf57cac34efda306a0eebac34f0965a0742'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.0.linux-armv6l.tar.gz'; 			sha256='e377a0004957c8c560a3ff99601bce612330a3d95ba3b0a2ae144165fc87deb1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.0.linux-arm64.tar.gz'; 			sha256='f3d4548edf9b22f26bbd49720350bbfe59d75b7090a1a2bff1afad8214febaf3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.0.linux-386.tar.gz'; 			sha256='0e6f378d9b072fab0a3d9ff4d5e990d98487d47252dba8160015a61e6bd0bcba'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.0.linux-mips64le.tar.gz'; 			sha256='92f7933d997c589b4f506c6b3cc5b27ff43b294c3a2d40bf4d7eeaf375f92afb'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.0.linux-ppc64le.tar.gz'; 			sha256='e938ffc81d8ebe5efc179240960ba22da6a841ff05d5cab7ce2547112b14a47f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.0.linux-riscv64.tar.gz'; 			sha256='87b21c06573617842ca9e00b954bc9f534066736a0778eae594ac54b45a9e8b7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.0.linux-s390x.tar.gz'; 			sha256='be7338df8e5d5472dfa307b0df2b446d85d001b0a2a3cdb1a14048d751b70481'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.0.src.tar.gz'; 		sha256='818d46ede85682dd551ad378ef37a4d247006f12ec59b5b755601d2ce114369a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 16 Aug 2023 12:14:16 GMT
ENV GOPATH=/go
# Wed, 16 Aug 2023 12:14:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 12:14:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 16 Aug 2023 12:14:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1efc9639d902ebaa56d5e963066d5ab28cdf0e5fac5aa967c72326db76357b0e`  
		Last Modified: Tue, 15 Aug 2023 23:51:10 GMT  
		Size: 47.4 MB (47415020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34e7b4c1a2c0700b8db12eb4cb9569ce104cda1989e5b4a480e35dd71690d33`  
		Last Modified: Wed, 16 Aug 2023 00:47:01 GMT  
		Size: 22.7 MB (22709644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77d20c8ff916e804bfb695aec7b06de85d30fe17cb0e067d2cfc9f75356d56b`  
		Last Modified: Wed, 16 Aug 2023 00:47:21 GMT  
		Size: 61.6 MB (61554098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d444d29b2a5c45f2f1dfce9a46ad1ba4d4d4721d08a32731f36031b71930086`  
		Last Modified: Wed, 16 Aug 2023 12:21:48 GMT  
		Size: 71.3 MB (71279360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093b5064afbe9593ca433dbab93b8e2f836bbbf80ac60015ce4fea08f97eb129`  
		Last Modified: Wed, 16 Aug 2023 12:21:51 GMT  
		Size: 68.2 MB (68164679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efeaf2cc110f68aadefcbc87c339f65f9f5f3584951f3e7d0fd51d0754968296`  
		Last Modified: Wed, 16 Aug 2023 12:21:36 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:fd20e4647d8699360007454fe4faaee2119bbb1a50c23c1521e3cba681528d75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (257988552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b949fcfaa07dbdd167b3b1c234af63f00e0b7f766c39e91d180635adde31b362`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:16:59 GMT
ADD file:03964ab92340a6f07fac7e332ca5f5401b3a35aa1e4a5c0b2484a71ff345bc29 in / 
# Wed, 16 Aug 2023 00:16:59 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 05:28:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 05:28:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 23:54:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 23:54:19 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 23:54:19 GMT
ENV GOLANG_VERSION=1.21.0
# Wed, 16 Aug 2023 23:54:30 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz'; 			sha256='d0398903a16ba2232b389fb31032ddf57cac34efda306a0eebac34f0965a0742'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.0.linux-armv6l.tar.gz'; 			sha256='e377a0004957c8c560a3ff99601bce612330a3d95ba3b0a2ae144165fc87deb1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.0.linux-arm64.tar.gz'; 			sha256='f3d4548edf9b22f26bbd49720350bbfe59d75b7090a1a2bff1afad8214febaf3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.0.linux-386.tar.gz'; 			sha256='0e6f378d9b072fab0a3d9ff4d5e990d98487d47252dba8160015a61e6bd0bcba'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.0.linux-mips64le.tar.gz'; 			sha256='92f7933d997c589b4f506c6b3cc5b27ff43b294c3a2d40bf4d7eeaf375f92afb'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.0.linux-ppc64le.tar.gz'; 			sha256='e938ffc81d8ebe5efc179240960ba22da6a841ff05d5cab7ce2547112b14a47f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.0.linux-riscv64.tar.gz'; 			sha256='87b21c06573617842ca9e00b954bc9f534066736a0778eae594ac54b45a9e8b7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.0.linux-s390x.tar.gz'; 			sha256='be7338df8e5d5472dfa307b0df2b446d85d001b0a2a3cdb1a14048d751b70481'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.0.src.tar.gz'; 		sha256='818d46ede85682dd551ad378ef37a4d247006f12ec59b5b755601d2ce114369a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 16 Aug 2023 23:54:31 GMT
ENV GOPATH=/go
# Wed, 16 Aug 2023 23:54:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 23:54:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 16 Aug 2023 23:54:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:22c91d9cbb3cbc0e4a05c1bfc86da0b5a439ded4f68eb2fbc055ba6b85ca1d90`  
		Last Modified: Wed, 16 Aug 2023 00:21:04 GMT  
		Size: 45.2 MB (45232937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24238a7fc18d7c6089f4f19e3e3d866f42674716043768c48cf6cabb7c8855b0`  
		Last Modified: Wed, 16 Aug 2023 05:47:31 GMT  
		Size: 21.9 MB (21936925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3696afa3824e29b9ed0a2d2d4938069d1122051fc3db7a03f0ba2a9271d6ba10`  
		Last Modified: Wed, 16 Aug 2023 05:47:52 GMT  
		Size: 59.3 MB (59261852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8b0ca47464596430f1b7448e7e05a93b1212ffec63a019b5cb51f1801b8f0e`  
		Last Modified: Wed, 16 Aug 2023 23:56:22 GMT  
		Size: 66.1 MB (66119355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee365f01de296552390ca00d5dd8c25ffe2141a1f4faec23ef95677790b6fe2`  
		Last Modified: Wed, 16 Aug 2023 23:56:26 GMT  
		Size: 65.4 MB (65437327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793017e251d5b184049e698fb4f9a721acccfd22c7e35f736f6cc0e6d750462a`  
		Last Modified: Wed, 16 Aug 2023 23:56:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e0fcf8ccf6d5b18ab60e417a0a9f4838d8dc561b51759de06ed50a12067c9432
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287423089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c406e816b2dffc2f7f85775cf22335cca945664df36133eb3b91d0df0491c7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:49 GMT
ADD file:ca43018e3d97d44b49e60fe002bb20834a74cc1163d7e95ad50d549f072de158 in / 
# Tue, 15 Aug 2023 23:39:49 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 01:21:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 23:59:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 23:59:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 23:59:47 GMT
ENV GOLANG_VERSION=1.21.0
# Wed, 16 Aug 2023 23:59:54 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz'; 			sha256='d0398903a16ba2232b389fb31032ddf57cac34efda306a0eebac34f0965a0742'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.0.linux-armv6l.tar.gz'; 			sha256='e377a0004957c8c560a3ff99601bce612330a3d95ba3b0a2ae144165fc87deb1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.0.linux-arm64.tar.gz'; 			sha256='f3d4548edf9b22f26bbd49720350bbfe59d75b7090a1a2bff1afad8214febaf3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.0.linux-386.tar.gz'; 			sha256='0e6f378d9b072fab0a3d9ff4d5e990d98487d47252dba8160015a61e6bd0bcba'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.0.linux-mips64le.tar.gz'; 			sha256='92f7933d997c589b4f506c6b3cc5b27ff43b294c3a2d40bf4d7eeaf375f92afb'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.0.linux-ppc64le.tar.gz'; 			sha256='e938ffc81d8ebe5efc179240960ba22da6a841ff05d5cab7ce2547112b14a47f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.0.linux-riscv64.tar.gz'; 			sha256='87b21c06573617842ca9e00b954bc9f534066736a0778eae594ac54b45a9e8b7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.0.linux-s390x.tar.gz'; 			sha256='be7338df8e5d5472dfa307b0df2b446d85d001b0a2a3cdb1a14048d751b70481'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.0.src.tar.gz'; 		sha256='818d46ede85682dd551ad378ef37a4d247006f12ec59b5b755601d2ce114369a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 16 Aug 2023 23:59:56 GMT
ENV GOPATH=/go
# Wed, 16 Aug 2023 23:59:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 23:59:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 16 Aug 2023 23:59:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a014e5e7d08c37cf1703b97e701ccdc850e4a18d0ee679f03aa875dcd520aa85`  
		Last Modified: Tue, 15 Aug 2023 23:42:59 GMT  
		Size: 49.6 MB (49591310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715cea74ecbb15cb82efef1e77dd60c31d90b01d1286d6f39b4562afaebe75f3`  
		Last Modified: Wed, 16 Aug 2023 01:38:30 GMT  
		Size: 23.6 MB (23570046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003f1109a21287fa17dc866e87e8c6685113960cbb0379fee8f42b83de63c647`  
		Last Modified: Wed, 16 Aug 2023 01:38:47 GMT  
		Size: 64.0 MB (63988473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6529d3f2eda2bb51de0720b46e2e8359ed7a45efa1298a067b519e1cf2c094c0`  
		Last Modified: Thu, 17 Aug 2023 00:01:28 GMT  
		Size: 86.3 MB (86295615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f522442f73454806b6fdd7e17e615fe193aa0373d241d53304e395c3648e5aa`  
		Last Modified: Thu, 17 Aug 2023 00:01:27 GMT  
		Size: 64.0 MB (63977490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478ffd6b0eada993fc1f4690d2ef4183b6b53ae441ab0a8406afbfe68f903167`  
		Last Modified: Thu, 17 Aug 2023 00:01:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:216bafc1abcd9ef915089ef439632e309c1c22052db8c18b1f121b08a3aca27e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296419099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e58fb07dc19986c762a452e742e0941216b35f0a0358a161fea45196f063f1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:38:49 GMT
ADD file:3f0a4d6b18b22088d0785bc2e351d829ad1ed6f154058017035842bdbe2a8d1e in / 
# Tue, 15 Aug 2023 23:38:51 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:25:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 00:26:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 20:34:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 20:34:45 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 20:34:45 GMT
ENV GOLANG_VERSION=1.21.0
# Wed, 16 Aug 2023 20:34:59 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz'; 			sha256='d0398903a16ba2232b389fb31032ddf57cac34efda306a0eebac34f0965a0742'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.0.linux-armv6l.tar.gz'; 			sha256='e377a0004957c8c560a3ff99601bce612330a3d95ba3b0a2ae144165fc87deb1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.0.linux-arm64.tar.gz'; 			sha256='f3d4548edf9b22f26bbd49720350bbfe59d75b7090a1a2bff1afad8214febaf3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.0.linux-386.tar.gz'; 			sha256='0e6f378d9b072fab0a3d9ff4d5e990d98487d47252dba8160015a61e6bd0bcba'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.0.linux-mips64le.tar.gz'; 			sha256='92f7933d997c589b4f506c6b3cc5b27ff43b294c3a2d40bf4d7eeaf375f92afb'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.0.linux-ppc64le.tar.gz'; 			sha256='e938ffc81d8ebe5efc179240960ba22da6a841ff05d5cab7ce2547112b14a47f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.0.linux-riscv64.tar.gz'; 			sha256='87b21c06573617842ca9e00b954bc9f534066736a0778eae594ac54b45a9e8b7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.0.linux-s390x.tar.gz'; 			sha256='be7338df8e5d5472dfa307b0df2b446d85d001b0a2a3cdb1a14048d751b70481'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.0.src.tar.gz'; 		sha256='818d46ede85682dd551ad378ef37a4d247006f12ec59b5b755601d2ce114369a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 16 Aug 2023 20:35:00 GMT
ENV GOPATH=/go
# Wed, 16 Aug 2023 20:35:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 20:35:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 16 Aug 2023 20:35:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1dc6cc826af02d533745c4612f635e028f3471e46f50422fd20a6dc913b60574`  
		Last Modified: Tue, 15 Aug 2023 23:43:02 GMT  
		Size: 50.6 MB (50568054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca8436c5a9dc8b9ea408612ff7210bcceebd896671ed3e31c61f398f9a00f25`  
		Last Modified: Wed, 16 Aug 2023 00:34:36 GMT  
		Size: 24.9 MB (24869754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4ec215b1e0b3f7f5034048ddb02b52122b17ef3885d242da7fca37250884e3`  
		Last Modified: Wed, 16 Aug 2023 00:35:00 GMT  
		Size: 66.0 MB (65972400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3534d5cc9b58d68e1ac673d9b3a51a0e865066cefa3841839d934b5576f2f3cc`  
		Last Modified: Wed, 16 Aug 2023 20:37:11 GMT  
		Size: 89.7 MB (89672339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b6cb3a9564fd1e9fd19cdaf3f46dc406670f428924bc3348f0d5abddccc1f`  
		Last Modified: Wed, 16 Aug 2023 20:37:09 GMT  
		Size: 65.3 MB (65336397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0715ddebaaa77f04fcdd35081dbd9031e70e377f7a8ae58aa0f3b4eb2bfa1eed`  
		Last Modified: Wed, 16 Aug 2023 20:36:50 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:ba249beebbf466cee5eb46498baa93f06c6981cd08f69c6bdef86cf66aa05c77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267755419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fc738fadc9b9afb2901c5b88b8a95789d7581d347dc52e25e424c632b2afa0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:08:02 GMT
ADD file:359d49b8d6eb4185590cb5da2825a99e2b2d4b4d81519b9283794e64261eec2c in / 
# Wed, 16 Aug 2023 00:08:08 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 14:33:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 14:35:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 16:15:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 16:15:36 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 16:15:42 GMT
ENV GOLANG_VERSION=1.21.0
# Wed, 16 Aug 2023 16:16:31 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz'; 			sha256='d0398903a16ba2232b389fb31032ddf57cac34efda306a0eebac34f0965a0742'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.0.linux-armv6l.tar.gz'; 			sha256='e377a0004957c8c560a3ff99601bce612330a3d95ba3b0a2ae144165fc87deb1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.0.linux-arm64.tar.gz'; 			sha256='f3d4548edf9b22f26bbd49720350bbfe59d75b7090a1a2bff1afad8214febaf3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.0.linux-386.tar.gz'; 			sha256='0e6f378d9b072fab0a3d9ff4d5e990d98487d47252dba8160015a61e6bd0bcba'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.0.linux-mips64le.tar.gz'; 			sha256='92f7933d997c589b4f506c6b3cc5b27ff43b294c3a2d40bf4d7eeaf375f92afb'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.0.linux-ppc64le.tar.gz'; 			sha256='e938ffc81d8ebe5efc179240960ba22da6a841ff05d5cab7ce2547112b14a47f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.0.linux-riscv64.tar.gz'; 			sha256='87b21c06573617842ca9e00b954bc9f534066736a0778eae594ac54b45a9e8b7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.0.linux-s390x.tar.gz'; 			sha256='be7338df8e5d5472dfa307b0df2b446d85d001b0a2a3cdb1a14048d751b70481'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.0.src.tar.gz'; 		sha256='818d46ede85682dd551ad378ef37a4d247006f12ec59b5b755601d2ce114369a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 16 Aug 2023 16:16:39 GMT
ENV GOPATH=/go
# Wed, 16 Aug 2023 16:16:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 16:16:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 16 Aug 2023 16:17:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:96b8a462ea6d525b430e77289e7ae92006277c062da33a8446fd1e664d41600b`  
		Last Modified: Wed, 16 Aug 2023 00:18:49 GMT  
		Size: 49.5 MB (49542000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8a8c9ea13a792b89577cb50edc4ddd2f4e3530348051c8c3a6d83065301bca`  
		Last Modified: Wed, 16 Aug 2023 15:00:21 GMT  
		Size: 23.6 MB (23612660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b30253a84fcbbec4217a75f594587c3eda3f23774859a9d945f37da28e1dad`  
		Last Modified: Wed, 16 Aug 2023 15:01:15 GMT  
		Size: 63.0 MB (62950874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613fc4a15979681f5cc1c82a9dca28e9cf59ef5f7939591ced99533f2f94f85f`  
		Last Modified: Wed, 16 Aug 2023 16:46:40 GMT  
		Size: 69.6 MB (69624276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f76181e50936e0ff9f7f06e2d061256e885124ae31ca986783e96087d195f4`  
		Last Modified: Wed, 16 Aug 2023 16:46:44 GMT  
		Size: 62.0 MB (62025483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9a6c882a28443ebaf4fe238d7dd21c4351dbc45cc9bef24330179b599da964`  
		Last Modified: Wed, 16 Aug 2023 16:45:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:92985a2e3874c54a95113b16f64ddbe5cffddfdafce5d873f432f960d1a515e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (303044646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebe8c03c2e328fff07c497de157e1a0896045f7cca3db2d509a90b9a45a9137`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:09:14 GMT
ADD file:8397677919f9bbf5273ddf61e008bcaace9195b46bcb2c31aff4f0a88617f12e in / 
# Wed, 16 Aug 2023 01:09:17 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:38:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 01:39:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:05:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:05:27 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 07:05:28 GMT
ENV GOLANG_VERSION=1.21.0
# Thu, 17 Aug 2023 07:05:49 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz'; 			sha256='d0398903a16ba2232b389fb31032ddf57cac34efda306a0eebac34f0965a0742'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.0.linux-armv6l.tar.gz'; 			sha256='e377a0004957c8c560a3ff99601bce612330a3d95ba3b0a2ae144165fc87deb1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.0.linux-arm64.tar.gz'; 			sha256='f3d4548edf9b22f26bbd49720350bbfe59d75b7090a1a2bff1afad8214febaf3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.0.linux-386.tar.gz'; 			sha256='0e6f378d9b072fab0a3d9ff4d5e990d98487d47252dba8160015a61e6bd0bcba'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.0.linux-mips64le.tar.gz'; 			sha256='92f7933d997c589b4f506c6b3cc5b27ff43b294c3a2d40bf4d7eeaf375f92afb'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.0.linux-ppc64le.tar.gz'; 			sha256='e938ffc81d8ebe5efc179240960ba22da6a841ff05d5cab7ce2547112b14a47f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.0.linux-riscv64.tar.gz'; 			sha256='87b21c06573617842ca9e00b954bc9f534066736a0778eae594ac54b45a9e8b7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.0.linux-s390x.tar.gz'; 			sha256='be7338df8e5d5472dfa307b0df2b446d85d001b0a2a3cdb1a14048d751b70481'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.0.src.tar.gz'; 		sha256='818d46ede85682dd551ad378ef37a4d247006f12ec59b5b755601d2ce114369a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Thu, 17 Aug 2023 07:05:53 GMT
ENV GOPATH=/go
# Thu, 17 Aug 2023 07:05:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 07:05:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 17 Aug 2023 07:05:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c59f7b2759f74830e13fa72caeaf898f560f72787aa9d5aec28bcf8585f2f066`  
		Last Modified: Wed, 16 Aug 2023 01:15:22 GMT  
		Size: 53.5 MB (53543761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cce374dd487e4d067dd2727a6401d31bd379da6e10a83e5a902a80be18aabaf`  
		Last Modified: Wed, 16 Aug 2023 02:09:27 GMT  
		Size: 25.7 MB (25681124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acab4f12553730c8f77e5e6b7ef103cdaf3f7db095c145c4b58ec1da135086b1`  
		Last Modified: Wed, 16 Aug 2023 02:09:59 GMT  
		Size: 69.6 MB (69570024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4dd17847b9fbcafa06a2a520f1b6b4bac508660bb01ca6cb921fe0914fa12d`  
		Last Modified: Thu, 17 Aug 2023 07:10:34 GMT  
		Size: 90.3 MB (90251857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af23bb179d263e57e1463c2548f65f80570515588ebf41884731eb8d5bf8413e`  
		Last Modified: Thu, 17 Aug 2023 07:10:30 GMT  
		Size: 64.0 MB (63997724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15451f978b91a16b89674ff800c75830ed604b23237906020091524622169481`  
		Last Modified: Thu, 17 Aug 2023 07:10:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:8beb7f6648adfc35bce77e6b475ff1ae01cffa7a589539eaeb3b0a2af2be3bdb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (269978349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9504ae1a7a6c0efbf92055df81a0214cdb4738db6d1ebab822a7aa341643f532`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:42:11 GMT
ADD file:eeb165e8fcc9b8f3a9e8f10fdbd507a91bc934046a4f23f2d636ca4b1796d1e3 in / 
# Tue, 15 Aug 2023 23:42:17 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 04:20:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 04:20:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 11:47:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 11:47:59 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 11:47:59 GMT
ENV GOLANG_VERSION=1.21.0
# Wed, 16 Aug 2023 11:48:19 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz'; 			sha256='d0398903a16ba2232b389fb31032ddf57cac34efda306a0eebac34f0965a0742'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.0.linux-armv6l.tar.gz'; 			sha256='e377a0004957c8c560a3ff99601bce612330a3d95ba3b0a2ae144165fc87deb1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.0.linux-arm64.tar.gz'; 			sha256='f3d4548edf9b22f26bbd49720350bbfe59d75b7090a1a2bff1afad8214febaf3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.0.linux-386.tar.gz'; 			sha256='0e6f378d9b072fab0a3d9ff4d5e990d98487d47252dba8160015a61e6bd0bcba'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.0.linux-mips64le.tar.gz'; 			sha256='92f7933d997c589b4f506c6b3cc5b27ff43b294c3a2d40bf4d7eeaf375f92afb'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.0.linux-ppc64le.tar.gz'; 			sha256='e938ffc81d8ebe5efc179240960ba22da6a841ff05d5cab7ce2547112b14a47f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.0.linux-riscv64.tar.gz'; 			sha256='87b21c06573617842ca9e00b954bc9f534066736a0778eae594ac54b45a9e8b7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.0.linux-s390x.tar.gz'; 			sha256='be7338df8e5d5472dfa307b0df2b446d85d001b0a2a3cdb1a14048d751b70481'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.0.src.tar.gz'; 		sha256='818d46ede85682dd551ad378ef37a4d247006f12ec59b5b755601d2ce114369a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 16 Aug 2023 11:48:25 GMT
ENV GOPATH=/go
# Wed, 16 Aug 2023 11:48:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 11:48:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 16 Aug 2023 11:48:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2bf08d586558a71fd0c5172579e7c378968a16f427fb3af772e4aa11c6b0a7af`  
		Last Modified: Tue, 15 Aug 2023 23:47:38 GMT  
		Size: 47.9 MB (47922016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afba98ba5dea198ec27ff40c833c54ce73ca11dccc94b59611cb506b44fa422`  
		Last Modified: Wed, 16 Aug 2023 04:36:16 GMT  
		Size: 24.0 MB (24028770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc50673f1af082588bca57ac1eaff982b89ce5badbe6d6b389ad96961fe54a81`  
		Last Modified: Wed, 16 Aug 2023 04:36:31 GMT  
		Size: 63.1 MB (63113641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fce761814670516cbaa641efff78723f5770da721461f0f5915a14c68ad49a7`  
		Last Modified: Wed, 16 Aug 2023 11:51:24 GMT  
		Size: 68.8 MB (68826812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48625840d728dfb96322d9c51dc1c8f02f9a705aed84424d736d0a22d7c925c5`  
		Last Modified: Wed, 16 Aug 2023 11:51:25 GMT  
		Size: 66.1 MB (66086953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cafe45aea312c942c9a81e79c613dd8fc7a6e674be7eaee5e4322eef321e528`  
		Last Modified: Wed, 16 Aug 2023 11:51:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

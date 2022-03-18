## `golang:bullseye`

```console
$ docker pull golang@sha256:7ee35628084eb61d9b002d9e9e5c385a931e76338d3b072740398458ae03fe7c
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

### `golang:bullseye` - linux; amd64

```console
$ docker pull golang@sha256:414276ae7b98fdcc08d6885d2b128e822117d1a2d4ec1b8c475060c9c1b7226c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.0 MB (353032171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76246e054d050c226f0daacd03d86f1c3176a464821d21fca908bb911b5b094`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:15 GMT
ADD file:9c4db2a9644ee3029a8e9cca58350efef660c3167e59b91f2bee9c303e592664 in / 
# Tue, 01 Mar 2022 02:13:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:26:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 06:26:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 17:51:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 17:51:28 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Mar 2022 00:28:13 GMT
ENV GOLANG_VERSION=1.18
# Wed, 16 Mar 2022 00:29:28 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.linux-amd64.tar.gz'; 			sha256='e85278e98f57cdb150fe8409e6e5df5343ecb13cebf03a5d5ff12bd55a80264f'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.linux-armv6l.tar.gz'; 			sha256='a80fa43d1f4575fb030adbfbaa94acd860c6847820764eecb06c63b7c103612b'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.linux-arm64.tar.gz'; 			sha256='7ac7b396a691e588c5fb57687759e6c4db84a2a3bbebb0765f4b38e5b1c5b00e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.linux-386.tar.gz'; 			sha256='1c04cf4440b323a66328e0df95d409f955b9b475e58eae235fdd3d1f1cf02f4f'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.linux-ppc64le.tar.gz'; 			sha256='070351edac192483c074b38d08ec19251a83f8210765a532a84c3dcf8aec04d8'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.linux-s390x.tar.gz'; 			sha256='ea265f5e62fcaf941d53f0cdb81222d9668e1672a0d39d992f16ff0e87c0ee6b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.src.tar.gz'; 		sha256='38f423db4cc834883f2b52344282fa7a39fbb93650dc62a11fdf0be6409bdad6'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 16 Mar 2022 00:29:30 GMT
ENV GOPATH=/go
# Wed, 16 Mar 2022 00:29:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Mar 2022 00:29:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 16 Mar 2022 00:29:30 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e4d61adff2077d048c6372d73c41b0bd68f525ad41f5530af05098a876683055`  
		Last Modified: Tue, 01 Mar 2022 02:18:55 GMT  
		Size: 54.9 MB (54917063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff1945c672b08a1791df62afaaf8aff14d3047155365f9c3646902937f7ffe6`  
		Last Modified: Tue, 01 Mar 2022 06:36:13 GMT  
		Size: 5.2 MB (5153034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5b10aec998344606441aec43a335ab6326f32aae331aab27da16a6bb4ec2be`  
		Last Modified: Tue, 01 Mar 2022 06:36:14 GMT  
		Size: 10.9 MB (10871885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12de8c754e45686ace9e25d11bee372b070eed5b5ab20aa3b4fab8c936496d02`  
		Last Modified: Tue, 01 Mar 2022 06:36:38 GMT  
		Size: 54.6 MB (54575903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c86ff77a3175ed4d7958578d141a96b5da005855d60ea24067de33cd62e4c36`  
		Last Modified: Wed, 02 Mar 2022 18:06:15 GMT  
		Size: 85.8 MB (85811039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81903f94b12515e161bc8e14c9996086c565771055dc17545dc83e8b653495b`  
		Last Modified: Wed, 16 Mar 2022 00:40:29 GMT  
		Size: 141.7 MB (141703091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5cad44dc3750e69fd7b7b295baaae5f8a6c9aa8e07e87995a2c940bc1c7871`  
		Last Modified: Wed, 16 Mar 2022 00:40:07 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; arm variant v5

```console
$ docker pull golang@sha256:2163a6f970e1e150c289b4a3a3f453e2799f0eeab8519da0c178c8962a185371
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301628416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75669dfe89fe5aa483e6a2634704f7707291355033ca878b3f382ebcaa05411`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:19:10 GMT
ADD file:711abc0c0a502fe727f811a82e7e6175c753593bc9f6d477a47b889fc3fe8ff6 in / 
# Thu, 17 Mar 2022 05:19:11 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:15:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:15:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 19:16:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:50:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:50:09 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 06:50:10 GMT
ENV GOLANG_VERSION=1.18
# Fri, 18 Mar 2022 06:54:40 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.linux-amd64.tar.gz'; 			sha256='e85278e98f57cdb150fe8409e6e5df5343ecb13cebf03a5d5ff12bd55a80264f'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.linux-armv6l.tar.gz'; 			sha256='a80fa43d1f4575fb030adbfbaa94acd860c6847820764eecb06c63b7c103612b'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.linux-arm64.tar.gz'; 			sha256='7ac7b396a691e588c5fb57687759e6c4db84a2a3bbebb0765f4b38e5b1c5b00e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.linux-386.tar.gz'; 			sha256='1c04cf4440b323a66328e0df95d409f955b9b475e58eae235fdd3d1f1cf02f4f'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.linux-ppc64le.tar.gz'; 			sha256='070351edac192483c074b38d08ec19251a83f8210765a532a84c3dcf8aec04d8'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.linux-s390x.tar.gz'; 			sha256='ea265f5e62fcaf941d53f0cdb81222d9668e1672a0d39d992f16ff0e87c0ee6b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.src.tar.gz'; 		sha256='38f423db4cc834883f2b52344282fa7a39fbb93650dc62a11fdf0be6409bdad6'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 18 Mar 2022 06:54:42 GMT
ENV GOPATH=/go
# Fri, 18 Mar 2022 06:54:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 06:54:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 18 Mar 2022 06:54:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f6db9b0909e16205c253a4a6e736ed382b68f85839d7822d22d5ddd35fd2fda4`  
		Last Modified: Thu, 17 Mar 2022 05:34:11 GMT  
		Size: 52.5 MB (52470250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd49582c7f6675ebcf6ce05a8c46ca03963dcb872a6609647908e9f3ec1bdab`  
		Last Modified: Thu, 17 Mar 2022 19:40:09 GMT  
		Size: 5.1 MB (5063869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5be2734ad2363ae06404b77e944bcdb8496677704f50b8b579838e015ab189`  
		Last Modified: Thu, 17 Mar 2022 19:40:11 GMT  
		Size: 10.6 MB (10570982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e806b3e4bd3a2bcc0347f8ed2951681ef09caa248f10c65740a1e875c73a0f`  
		Last Modified: Thu, 17 Mar 2022 19:40:52 GMT  
		Size: 52.3 MB (52316691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9a11761f0937f4e7c54fe381fc52c77495582f6f17e654d7c16c4ef5cb058e`  
		Last Modified: Fri, 18 Mar 2022 07:10:30 GMT  
		Size: 68.8 MB (68756279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650e4625081c41323e504f368d049315b59e52fe335b0a16e3e69cb9c7b2c051`  
		Last Modified: Fri, 18 Mar 2022 07:11:02 GMT  
		Size: 112.5 MB (112450189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4f405eb19d0a27371fe82c03ff1df6f3deb8cfed47a1bf68418d5053e28134`  
		Last Modified: Fri, 18 Mar 2022 07:09:48 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:343fede0e567092b3e627226273bf51c733ae553bf047509ebcc1d04ed142c01
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290355471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51494bad127280ecff183b1b17fa6bda9e2deaac7e953975f16b8b207b8debef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:17 GMT
ADD file:b388eaef074fa7cc4e0f6f0b6a56e4be6c69489b63477ab4469ff5415074b0c7 in / 
# Tue, 01 Mar 2022 02:02:18 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:26:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 09:27:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 21:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 21:58:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Mar 2022 01:07:48 GMT
ENV GOLANG_VERSION=1.18
# Wed, 16 Mar 2022 01:08:38 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.linux-amd64.tar.gz'; 			sha256='e85278e98f57cdb150fe8409e6e5df5343ecb13cebf03a5d5ff12bd55a80264f'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.linux-armv6l.tar.gz'; 			sha256='a80fa43d1f4575fb030adbfbaa94acd860c6847820764eecb06c63b7c103612b'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.linux-arm64.tar.gz'; 			sha256='7ac7b396a691e588c5fb57687759e6c4db84a2a3bbebb0765f4b38e5b1c5b00e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.linux-386.tar.gz'; 			sha256='1c04cf4440b323a66328e0df95d409f955b9b475e58eae235fdd3d1f1cf02f4f'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.linux-ppc64le.tar.gz'; 			sha256='070351edac192483c074b38d08ec19251a83f8210765a532a84c3dcf8aec04d8'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.linux-s390x.tar.gz'; 			sha256='ea265f5e62fcaf941d53f0cdb81222d9668e1672a0d39d992f16ff0e87c0ee6b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.src.tar.gz'; 		sha256='38f423db4cc834883f2b52344282fa7a39fbb93650dc62a11fdf0be6409bdad6'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 16 Mar 2022 01:08:40 GMT
ENV GOPATH=/go
# Wed, 16 Mar 2022 01:08:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Mar 2022 01:08:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 16 Mar 2022 01:08:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:17a41fc762495ca54ac53f271889bdf4ac8bea7cedfa3b585e4e42ef106935f1`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 50.1 MB (50117069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9173ee01c42f46f1839650f0a56ee12ab74693f31dacccf586222ef98cb4ec19`  
		Last Modified: Tue, 01 Mar 2022 09:51:00 GMT  
		Size: 4.9 MB (4922642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f119f27841bdc8ee96fe83e4e2bb9b453db5a3a239036547b8e09c87f650befe`  
		Last Modified: Tue, 01 Mar 2022 09:51:01 GMT  
		Size: 10.2 MB (10216974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b827df064e12020cb42fda8ff122cbf83eda05e2c27240cc0dcb551be21b6ef`  
		Last Modified: Tue, 01 Mar 2022 09:51:51 GMT  
		Size: 50.3 MB (50327735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5088931f24458b9899c21494d859666033e8adcd14e9cc0cb3e5d02282c50b`  
		Last Modified: Wed, 02 Mar 2022 22:22:23 GMT  
		Size: 64.8 MB (64762177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6033d6c8d7cad4c5954b4b0f328c9cecd50c6dd209fc5f310e97d4ef1fc910`  
		Last Modified: Wed, 16 Mar 2022 01:24:53 GMT  
		Size: 110.0 MB (110008718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cc881805f297b9101d9de0363dbbb6c1be8791432119d6a3d26f3aaa95c29f`  
		Last Modified: Wed, 16 Mar 2022 01:23:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:9b8a5ea3de2895a1f34beb6f121b658c67ad87b4cc7dc957608331271a20bf8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313581830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c476985b1ca4531da152776161643f994b5d57593f7ae0800e6efba56c7702e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:41 GMT
ADD file:5effc7e0ab7312f14a7ee81c06c71400aae31219d477ebe1a4f7a9156797c42a in / 
# Thu, 17 Mar 2022 03:21:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:11:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 22:11:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 16:24:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 16:24:11 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 16:24:11 GMT
ENV GOLANG_VERSION=1.18
# Fri, 18 Mar 2022 16:25:21 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.linux-amd64.tar.gz'; 			sha256='e85278e98f57cdb150fe8409e6e5df5343ecb13cebf03a5d5ff12bd55a80264f'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.linux-armv6l.tar.gz'; 			sha256='a80fa43d1f4575fb030adbfbaa94acd860c6847820764eecb06c63b7c103612b'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.linux-arm64.tar.gz'; 			sha256='7ac7b396a691e588c5fb57687759e6c4db84a2a3bbebb0765f4b38e5b1c5b00e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.linux-386.tar.gz'; 			sha256='1c04cf4440b323a66328e0df95d409f955b9b475e58eae235fdd3d1f1cf02f4f'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.linux-ppc64le.tar.gz'; 			sha256='070351edac192483c074b38d08ec19251a83f8210765a532a84c3dcf8aec04d8'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.linux-s390x.tar.gz'; 			sha256='ea265f5e62fcaf941d53f0cdb81222d9668e1672a0d39d992f16ff0e87c0ee6b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.src.tar.gz'; 		sha256='38f423db4cc834883f2b52344282fa7a39fbb93650dc62a11fdf0be6409bdad6'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 18 Mar 2022 16:25:22 GMT
ENV GOPATH=/go
# Fri, 18 Mar 2022 16:25:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 16:25:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 18 Mar 2022 16:25:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:260ad8146ed2447d5587608b10fed4f80de80cdc559e619f3a235d3ba09eaf7b`  
		Last Modified: Thu, 17 Mar 2022 03:28:04 GMT  
		Size: 53.6 MB (53616308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1399f445da611be3789923cf26d158e3f4f80449b7295fa069a8eaecaaf137e6`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 4.9 MB (4937558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd9e43777fa6c09c341f3aa922f47b5b3ace26de1d779124afd2f1d435731d9`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 10.7 MB (10655858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f81267e40a2df9e572fe797e45dbc086008422eb2216df18b7a91f1cf13e22b`  
		Last Modified: Thu, 17 Mar 2022 22:21:21 GMT  
		Size: 54.7 MB (54671322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd71068207c873c7c4ce28b907cc067b45fa1501129ba0f50a9f34bee37df9d`  
		Last Modified: Fri, 18 Mar 2022 16:37:29 GMT  
		Size: 81.0 MB (81037784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9377fa436af8eb1e6f4ed5d9b7141e12da234c24177c517a326b9f70d77b1a32`  
		Last Modified: Fri, 18 Mar 2022 16:37:33 GMT  
		Size: 108.7 MB (108662874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598f1c03672dd2e858acd90f804b54df2fc466d2d81baf8c13bc3d73098b1fdf`  
		Last Modified: Fri, 18 Mar 2022 16:37:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; 386

```console
$ docker pull golang@sha256:a5aaca0005efbfb99e1984b5539a6b1006c19d37db0368cc4ae12a264cfa0899
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.5 MB (328488718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ccffa1d0ae18ceece93bd1c48ffdf934b755e2f66861bc45c3fd18e70238c2f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:07:15 GMT
ADD file:4341f64e7f1accc7f9737a9896bf50c6ba8f51698e52c594d9421fe4f2374e2a in / 
# Tue, 01 Mar 2022 02:07:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:40:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:41:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 05:41:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 04:37:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 04:37:26 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Mar 2022 00:45:03 GMT
ENV GOLANG_VERSION=1.18
# Wed, 16 Mar 2022 00:46:08 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.linux-amd64.tar.gz'; 			sha256='e85278e98f57cdb150fe8409e6e5df5343ecb13cebf03a5d5ff12bd55a80264f'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.linux-armv6l.tar.gz'; 			sha256='a80fa43d1f4575fb030adbfbaa94acd860c6847820764eecb06c63b7c103612b'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.linux-arm64.tar.gz'; 			sha256='7ac7b396a691e588c5fb57687759e6c4db84a2a3bbebb0765f4b38e5b1c5b00e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.linux-386.tar.gz'; 			sha256='1c04cf4440b323a66328e0df95d409f955b9b475e58eae235fdd3d1f1cf02f4f'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.linux-ppc64le.tar.gz'; 			sha256='070351edac192483c074b38d08ec19251a83f8210765a532a84c3dcf8aec04d8'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.linux-s390x.tar.gz'; 			sha256='ea265f5e62fcaf941d53f0cdb81222d9668e1672a0d39d992f16ff0e87c0ee6b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.src.tar.gz'; 		sha256='38f423db4cc834883f2b52344282fa7a39fbb93650dc62a11fdf0be6409bdad6'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 16 Mar 2022 00:46:09 GMT
ENV GOPATH=/go
# Wed, 16 Mar 2022 00:46:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Mar 2022 00:46:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 16 Mar 2022 00:46:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5cf8159e9217c5f37fe58b260cacc1d132c2e21ca58c769d29c6eb720993a304`  
		Last Modified: Tue, 01 Mar 2022 02:15:15 GMT  
		Size: 55.9 MB (55938747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700db29f99e559f6f1909315637ddbda6667a35bd437b9e5d8c3beb373c6c1f`  
		Last Modified: Tue, 01 Mar 2022 05:51:55 GMT  
		Size: 5.3 MB (5283081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff041f2862924d1932eb1f5d7b01079bf8015dcc0dbb94a23d2475b8684d875a`  
		Last Modified: Tue, 01 Mar 2022 05:51:56 GMT  
		Size: 11.3 MB (11250640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ec658b51a80445b805d19e0462b4112f90132f61a78d8d7f5b29f6903e1e44`  
		Last Modified: Tue, 01 Mar 2022 05:52:25 GMT  
		Size: 55.9 MB (55919550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4c03e566323e31b26438b87170c8b4fc3017bc855f2fbe0ebc948948e32e8a`  
		Last Modified: Wed, 02 Mar 2022 04:54:47 GMT  
		Size: 87.3 MB (87256982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a906e7e94af1beae985f125a159c22ea90d62cb953e84686b2278ae6ec224d7`  
		Last Modified: Wed, 16 Mar 2022 01:01:06 GMT  
		Size: 112.8 MB (112839563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b97ca95fd05243888b455fb0e2ca8d98abf126da1247c761e77c00e11dd4857`  
		Last Modified: Wed, 16 Mar 2022 01:00:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; mips64le

```console
$ docker pull golang@sha256:61e1b6acfa8d2c8e73279c5bc02cff1d6bd1bd84ba5ca84b2c6b894a50e90eba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297832162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ffe2a821164a9514666514319dc788bd40d219453747935a6c557ea5e68c9c7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:18 GMT
ADD file:5beac822d8ef6913f5cda32d2e19a31978679cd0a8f51793343f0616de081608 in / 
# Tue, 01 Mar 2022 02:02:19 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 03:04:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 03:04:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 03:05:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 05 Mar 2022 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Mar 2022 07:54:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Mar 2022 01:07:50 GMT
ENV GOLANG_VERSION=1.18
# Wed, 16 Mar 2022 01:19:32 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.linux-amd64.tar.gz'; 			sha256='e85278e98f57cdb150fe8409e6e5df5343ecb13cebf03a5d5ff12bd55a80264f'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.linux-armv6l.tar.gz'; 			sha256='a80fa43d1f4575fb030adbfbaa94acd860c6847820764eecb06c63b7c103612b'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.linux-arm64.tar.gz'; 			sha256='7ac7b396a691e588c5fb57687759e6c4db84a2a3bbebb0765f4b38e5b1c5b00e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.linux-386.tar.gz'; 			sha256='1c04cf4440b323a66328e0df95d409f955b9b475e58eae235fdd3d1f1cf02f4f'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.linux-ppc64le.tar.gz'; 			sha256='070351edac192483c074b38d08ec19251a83f8210765a532a84c3dcf8aec04d8'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.linux-s390x.tar.gz'; 			sha256='ea265f5e62fcaf941d53f0cdb81222d9668e1672a0d39d992f16ff0e87c0ee6b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.src.tar.gz'; 		sha256='38f423db4cc834883f2b52344282fa7a39fbb93650dc62a11fdf0be6409bdad6'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 16 Mar 2022 01:19:40 GMT
ENV GOPATH=/go
# Wed, 16 Mar 2022 01:19:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Mar 2022 01:19:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 16 Mar 2022 01:20:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b9a7ad0f3cddab5c27fc342066cc786b37353dfb853deb360bb79e8256fffac3`  
		Last Modified: Tue, 01 Mar 2022 02:11:43 GMT  
		Size: 53.2 MB (53179977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0268bbc6c02a19015d432ff84a4a52a697c1c6500f7132a064c4a521c7ec05e`  
		Last Modified: Tue, 01 Mar 2022 03:21:17 GMT  
		Size: 5.1 MB (5114689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:967051666d5d4fa8df0e21cfbe2760f27b7349a5dc9d005edb8a27a311e80759`  
		Last Modified: Tue, 01 Mar 2022 03:21:19 GMT  
		Size: 10.9 MB (10873370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c40ca208672a1f0a2cdc3c2d7366c218b35a36520cf3a81b95be586a9a3fee9`  
		Last Modified: Tue, 01 Mar 2022 03:22:07 GMT  
		Size: 53.3 MB (53297983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7a676eef3cb855e90070b3bb1db337b456b72252706cf99b691444dad2a6dc`  
		Last Modified: Sat, 05 Mar 2022 09:01:43 GMT  
		Size: 66.7 MB (66708442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603d7140be36d13778a1a185bca7be9bab514ddaee673cfbd9049311978406b0`  
		Last Modified: Wed, 16 Mar 2022 01:34:04 GMT  
		Size: 108.7 MB (108657575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ce106dd081182a42cfc9e1c7dbf2f169cf506b418d7c9f7e6df0210492e9c9`  
		Last Modified: Wed, 16 Mar 2022 01:32:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; ppc64le

```console
$ docker pull golang@sha256:649ba39215a81c82f25604635c73ad8d4477a32d3d8d7a591eff6bc012f3690a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 MB (323862423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f38abebc9865f2164967fdff715e0755228f45c891b43dd6f4f978ee0e44f9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:04:22 GMT
ADD file:00554eaeb433a7cc43c22f2544d800896f451a2e5a7895863c4651ed425b8c36 in / 
# Tue, 01 Mar 2022 02:04:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 07:06:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 07:07:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 07:09:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 17:00:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 17:00:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Mar 2022 02:34:55 GMT
ENV GOLANG_VERSION=1.18
# Wed, 16 Mar 2022 02:36:51 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.linux-amd64.tar.gz'; 			sha256='e85278e98f57cdb150fe8409e6e5df5343ecb13cebf03a5d5ff12bd55a80264f'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.linux-armv6l.tar.gz'; 			sha256='a80fa43d1f4575fb030adbfbaa94acd860c6847820764eecb06c63b7c103612b'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.linux-arm64.tar.gz'; 			sha256='7ac7b396a691e588c5fb57687759e6c4db84a2a3bbebb0765f4b38e5b1c5b00e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.linux-386.tar.gz'; 			sha256='1c04cf4440b323a66328e0df95d409f955b9b475e58eae235fdd3d1f1cf02f4f'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.linux-ppc64le.tar.gz'; 			sha256='070351edac192483c074b38d08ec19251a83f8210765a532a84c3dcf8aec04d8'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.linux-s390x.tar.gz'; 			sha256='ea265f5e62fcaf941d53f0cdb81222d9668e1672a0d39d992f16ff0e87c0ee6b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.src.tar.gz'; 		sha256='38f423db4cc834883f2b52344282fa7a39fbb93650dc62a11fdf0be6409bdad6'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 16 Mar 2022 02:37:03 GMT
ENV GOPATH=/go
# Wed, 16 Mar 2022 02:37:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Mar 2022 02:37:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 16 Mar 2022 02:37:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9ff352265b4a055377b95db6dddea03717bbefbc7f30fbacf493764d617ae85e`  
		Last Modified: Tue, 01 Mar 2022 02:14:41 GMT  
		Size: 58.8 MB (58834115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6e10a400e162a4b996dd3e9c41cf812cfdb85d9830543b1c0b42305ab08b61`  
		Last Modified: Tue, 01 Mar 2022 07:42:05 GMT  
		Size: 5.4 MB (5401790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7ac604ebf8c0f6690f9477f7cba586130342d01fb167fc710f6621475e1786`  
		Last Modified: Tue, 01 Mar 2022 07:42:06 GMT  
		Size: 11.6 MB (11625870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20dd043e4a99bc0c4d1ed0c5ead9dcddb30bb43c85f40f573a87b12292f70b4`  
		Last Modified: Tue, 01 Mar 2022 07:42:32 GMT  
		Size: 58.9 MB (58854072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9e7f99efef65249e101d28baa4f3b95cebd217c0146ca2b143e2640b9549e1`  
		Last Modified: Tue, 01 Mar 2022 17:34:19 GMT  
		Size: 80.3 MB (80288088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4ffc6f26c3d20a8c6b29f8452303bc06e7e6f87ed79cdbff9d58e51778c724`  
		Last Modified: Wed, 16 Mar 2022 03:02:32 GMT  
		Size: 108.9 MB (108858332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a64f060e5f8f1e55dfb479f8db690757fef1df178c8c23218cc45116204474`  
		Last Modified: Wed, 16 Mar 2022 03:02:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; s390x

```console
$ docker pull golang@sha256:2702929a87bf96e294a34ee64437abf5ba816c5fd2a0ef8247acf6764c211279
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300298299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0b33668a2452596846d5e06d8b39f3f42c633c76fd41405bd0d0ebd7f57db3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:38 GMT
ADD file:75b45e65d2ec2c6822b1ddc46ff159dd10ac56bf9dff8b0996ac589a1ede22ff in / 
# Thu, 17 Mar 2022 03:06:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 18:20:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:20:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 18:21:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 00:39:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 00:39:53 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 00:39:53 GMT
ENV GOLANG_VERSION=1.18
# Fri, 18 Mar 2022 00:41:20 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.linux-amd64.tar.gz'; 			sha256='e85278e98f57cdb150fe8409e6e5df5343ecb13cebf03a5d5ff12bd55a80264f'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.linux-armv6l.tar.gz'; 			sha256='a80fa43d1f4575fb030adbfbaa94acd860c6847820764eecb06c63b7c103612b'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.linux-arm64.tar.gz'; 			sha256='7ac7b396a691e588c5fb57687759e6c4db84a2a3bbebb0765f4b38e5b1c5b00e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.linux-386.tar.gz'; 			sha256='1c04cf4440b323a66328e0df95d409f955b9b475e58eae235fdd3d1f1cf02f4f'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.linux-ppc64le.tar.gz'; 			sha256='070351edac192483c074b38d08ec19251a83f8210765a532a84c3dcf8aec04d8'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.linux-s390x.tar.gz'; 			sha256='ea265f5e62fcaf941d53f0cdb81222d9668e1672a0d39d992f16ff0e87c0ee6b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.src.tar.gz'; 		sha256='38f423db4cc834883f2b52344282fa7a39fbb93650dc62a11fdf0be6409bdad6'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 18 Mar 2022 00:41:26 GMT
ENV GOPATH=/go
# Fri, 18 Mar 2022 00:41:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 00:41:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 18 Mar 2022 00:41:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ae9f1a186a2633be1ad71c317c2f195b221cef89502f9edc510b3a2049723758`  
		Last Modified: Thu, 17 Mar 2022 03:12:26 GMT  
		Size: 53.2 MB (53217527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d6229369d1bac8aa97bfefe6dd7990a66c0a3e98f420c282a39a279df7c391`  
		Last Modified: Thu, 17 Mar 2022 18:29:06 GMT  
		Size: 5.1 MB (5137013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf171d8059efb2bc6c026904c68dddd3487a129cd53d33def9589665326d56f`  
		Last Modified: Thu, 17 Mar 2022 18:29:07 GMT  
		Size: 10.8 MB (10761392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cdad8e45654b094c248eb6bc86e3e0d8dda7b0e1df7c2792f2abb3a0d18cc8`  
		Last Modified: Thu, 17 Mar 2022 18:29:23 GMT  
		Size: 54.0 MB (54044974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c31fef30b7389a7896fd11cc8439b889620677730ddc4b51fab0b295648f657`  
		Last Modified: Fri, 18 Mar 2022 00:53:27 GMT  
		Size: 65.6 MB (65559656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f22f8f65c926cb64a48e5cdd910ea71d97336203f1a8ccbd1a0eada5412fd9`  
		Last Modified: Fri, 18 Mar 2022 00:53:32 GMT  
		Size: 111.6 MB (111577580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0d8d6f7c6e59d73f1a2c1ccc0a56892ad2871007c7aca703c1bed589a8a708`  
		Last Modified: Fri, 18 Mar 2022 00:53:19 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

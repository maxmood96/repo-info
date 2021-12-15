## `golang:latest`

```console
$ docker pull golang@sha256:eb61213fe612b6af346cab13c2b81f1b8113f9ccf23a5ca6b54fede8ffd63bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 11
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.405; amd64
	-	windows version 10.0.17763.2366; amd64
	-	windows version 10.0.14393.4825; amd64

### `golang:latest` - linux; amd64

```console
$ docker pull golang@sha256:d860e175278037ee2429fecb1150bf10635ff4488c5a6faf695b169bf2c0868f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346105082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37eabbc422cd87d1d6f7d02fc132605c22a5ef03ca0ec8c83f3dc51101dbbdb9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 10:58:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 10:58:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Dec 2021 16:19:33 GMT
ENV GOLANG_VERSION=1.17.5
# Thu, 09 Dec 2021 16:19:57 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.5.linux-amd64.tar.gz'; 			sha256='bd78114b0d441b029c8fe0341f4910370925a4d270a6a590668840675b0c653e'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.5.linux-armv6l.tar.gz'; 			sha256='aa1fb6c53b4fe72f159333362a10aca37ae938bde8adc9c6eaf2a8e87d1e47de'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.5.linux-arm64.tar.gz'; 			sha256='6f95ce3da40d9ce1355e48f31f4eb6508382415ca4d7413b1e7a3314e6430e7e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.5.linux-386.tar.gz'; 			sha256='4f4914303bc18f24fd137a97e595735308f5ce81323c7224c12466fd763fc59f'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.5.linux-ppc64le.tar.gz'; 			sha256='3d4be616e568f0a02cb7f7769bcaafda4b0969ed0f9bb4277619930b96847e70'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.5.linux-s390x.tar.gz'; 			sha256='8087d4fe991e82804e6485c26568c2e0ee0bfde00ceb9015dc86cb6bf84ef40b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.5.src.tar.gz'; 		sha256='3defb9a09bed042403195e872dcbc8c6fae1485963332279668ec52e80a95a2d'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 09 Dec 2021 16:19:59 GMT
ENV GOPATH=/go
# Thu, 09 Dec 2021 16:19:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Dec 2021 16:20:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 09 Dec 2021 16:20:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9442ff4ff8634f5d742369e4ad1d6fea20a21a71807d249f6b28954a515760`  
		Last Modified: Fri, 03 Dec 2021 11:02:37 GMT  
		Size: 85.8 MB (85771394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba1e4e2904e6f722f1f8292e68ccdd20fed7fa2cc36bf6cef5ec212f3c44b17`  
		Last Modified: Thu, 09 Dec 2021 16:31:49 GMT  
		Size: 134.8 MB (134807391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc73180a07b32d19a6e968d749075d14466adf6cc4cc34736c39fa9fa1b4ae0`  
		Last Modified: Thu, 09 Dec 2021 16:31:30 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; arm variant v5

```console
$ docker pull golang@sha256:0e83dcf9bdcab9fd8a5d9f0064d059321b6e3264608e0f133cbad1ef6461e45a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294530190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15600798afd64ffd7dc3fd75f11222cc61769d1662d7873a82b21f3c71aeb2e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:49:59 GMT
ADD file:7db27b7237be13d28b7ac71f50b332fc30b9988ea3b9a25dbf567e66ae9f3733 in / 
# Thu, 02 Dec 2021 02:50:00 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:34:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:35:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 09:50:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 09:50:10 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Dec 2021 16:48:38 GMT
ENV GOLANG_VERSION=1.17.5
# Thu, 09 Dec 2021 16:52:45 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.5.linux-amd64.tar.gz'; 			sha256='bd78114b0d441b029c8fe0341f4910370925a4d270a6a590668840675b0c653e'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.5.linux-armv6l.tar.gz'; 			sha256='aa1fb6c53b4fe72f159333362a10aca37ae938bde8adc9c6eaf2a8e87d1e47de'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.5.linux-arm64.tar.gz'; 			sha256='6f95ce3da40d9ce1355e48f31f4eb6508382415ca4d7413b1e7a3314e6430e7e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.5.linux-386.tar.gz'; 			sha256='4f4914303bc18f24fd137a97e595735308f5ce81323c7224c12466fd763fc59f'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.5.linux-ppc64le.tar.gz'; 			sha256='3d4be616e568f0a02cb7f7769bcaafda4b0969ed0f9bb4277619930b96847e70'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.5.linux-s390x.tar.gz'; 			sha256='8087d4fe991e82804e6485c26568c2e0ee0bfde00ceb9015dc86cb6bf84ef40b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.5.src.tar.gz'; 		sha256='3defb9a09bed042403195e872dcbc8c6fae1485963332279668ec52e80a95a2d'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 09 Dec 2021 16:52:48 GMT
ENV GOPATH=/go
# Thu, 09 Dec 2021 16:52:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Dec 2021 16:52:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 09 Dec 2021 16:52:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7243911d8825e14c0a343985557fbeb75da8a3a059c3f67c83036cc217dac188`  
		Last Modified: Thu, 02 Dec 2021 03:08:41 GMT  
		Size: 52.5 MB (52467922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f91846e63508bbda03b74c487feabb599525b1c20c5b0e35d3ecb68b0791963`  
		Last Modified: Thu, 02 Dec 2021 04:00:12 GMT  
		Size: 5.1 MB (5063907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d446dad57642eb79a9cc56005f2d0bd04022a419a03076ed09503002b5f18f0`  
		Last Modified: Thu, 02 Dec 2021 04:00:13 GMT  
		Size: 10.6 MB (10571199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01c3e4ea3de2890a431db84174f2d19f5b0137f1d3ffa29e4afb1b24ca6404a`  
		Last Modified: Thu, 02 Dec 2021 04:00:51 GMT  
		Size: 52.3 MB (52323416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503f19fa8f1586edeb0952b57fc2b8fd3a3aef45c996bc3fe8f6b4f8ac1ed16a`  
		Last Modified: Fri, 03 Dec 2021 10:08:28 GMT  
		Size: 68.7 MB (68705359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d51f52e13302a293abdb640cb96a8110513c603882cbe056afc9f4691bbbec8`  
		Last Modified: Thu, 09 Dec 2021 17:06:47 GMT  
		Size: 105.4 MB (105398232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1214f8c7a4d351783d4e7b604373cda3c6f0ee9d89a99c2dfa45565653e795d`  
		Last Modified: Thu, 09 Dec 2021 17:05:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; arm variant v7

```console
$ docker pull golang@sha256:431794fb25d9777875688025f188fcb5f186ab320b981f7b1de8b3f6627648f2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283413106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4adde45590008de15f2f96989a740586e00d1a9edcdba39c9955764afbfc9f32`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:04:39 GMT
ADD file:f0d0256a657fcc82cba38ec9fe377ae4d30125de11e0003de81177370592b440 in / 
# Thu, 02 Dec 2021 09:04:40 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:38:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 11:39:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Dec 2021 02:36:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Dec 2021 02:36:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Dec 2021 16:58:00 GMT
ENV GOLANG_VERSION=1.17.5
# Thu, 09 Dec 2021 16:58:35 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.5.linux-amd64.tar.gz'; 			sha256='bd78114b0d441b029c8fe0341f4910370925a4d270a6a590668840675b0c653e'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.5.linux-armv6l.tar.gz'; 			sha256='aa1fb6c53b4fe72f159333362a10aca37ae938bde8adc9c6eaf2a8e87d1e47de'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.5.linux-arm64.tar.gz'; 			sha256='6f95ce3da40d9ce1355e48f31f4eb6508382415ca4d7413b1e7a3314e6430e7e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.5.linux-386.tar.gz'; 			sha256='4f4914303bc18f24fd137a97e595735308f5ce81323c7224c12466fd763fc59f'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.5.linux-ppc64le.tar.gz'; 			sha256='3d4be616e568f0a02cb7f7769bcaafda4b0969ed0f9bb4277619930b96847e70'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.5.linux-s390x.tar.gz'; 			sha256='8087d4fe991e82804e6485c26568c2e0ee0bfde00ceb9015dc86cb6bf84ef40b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.5.src.tar.gz'; 		sha256='3defb9a09bed042403195e872dcbc8c6fae1485963332279668ec52e80a95a2d'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 09 Dec 2021 16:58:37 GMT
ENV GOPATH=/go
# Thu, 09 Dec 2021 16:58:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Dec 2021 16:58:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 09 Dec 2021 16:58:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e704987a22630df63d8518dd22b13ec2a4f460fd492ab42b97cdc6f971e7be31`  
		Last Modified: Thu, 02 Dec 2021 09:20:17 GMT  
		Size: 50.1 MB (50134315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfec4d15f2394da70fac9265e0e06909f3fc78eb919976d21b07ba0ba5214dba`  
		Last Modified: Thu, 02 Dec 2021 12:00:15 GMT  
		Size: 4.9 MB (4922713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5168f89db31fd7437013ced429c3e2fb7ef1d0e51dbd25bc65fdfde5ab4d5ca1`  
		Last Modified: Thu, 02 Dec 2021 12:00:17 GMT  
		Size: 10.2 MB (10216972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a2d12df86190bd722a8220fd21e6b8978e175668c93e7678e898b6d6100e76`  
		Last Modified: Thu, 02 Dec 2021 12:01:06 GMT  
		Size: 50.3 MB (50327911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76e285909a437357e69881e130a03a43b934aec7f4898c352bff9dca73ff719`  
		Last Modified: Sat, 04 Dec 2021 02:59:59 GMT  
		Size: 64.7 MB (64727806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f89723ae6f3ef163922010cbc705bf1041c49bb8632566a566823a743b1eaf8`  
		Last Modified: Thu, 09 Dec 2021 17:20:30 GMT  
		Size: 103.1 MB (103083234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d217e816022fc4393982b1d04d3641e23ebed566571397ea0b8eae16592445`  
		Last Modified: Thu, 09 Dec 2021 17:19:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:6245b2bee36df7a76a983b7213af5765d6b61fda5a44fbaf95716135af152dac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.5 MB (307497052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c09c3892998e6d205df67677ce58226693649c6629b976988a8cba66bca9e5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:07:54 GMT
ADD file:998dc1c35eeeed1ddf46156aeb337fb9b8cbb4855caf994201167a1061f4ecbf in / 
# Thu, 02 Dec 2021 08:07:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:53:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:53:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 09:53:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 05:06:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 05:06:26 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Dec 2021 16:39:51 GMT
ENV GOLANG_VERSION=1.17.5
# Thu, 09 Dec 2021 16:40:06 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.5.linux-amd64.tar.gz'; 			sha256='bd78114b0d441b029c8fe0341f4910370925a4d270a6a590668840675b0c653e'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.5.linux-armv6l.tar.gz'; 			sha256='aa1fb6c53b4fe72f159333362a10aca37ae938bde8adc9c6eaf2a8e87d1e47de'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.5.linux-arm64.tar.gz'; 			sha256='6f95ce3da40d9ce1355e48f31f4eb6508382415ca4d7413b1e7a3314e6430e7e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.5.linux-386.tar.gz'; 			sha256='4f4914303bc18f24fd137a97e595735308f5ce81323c7224c12466fd763fc59f'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.5.linux-ppc64le.tar.gz'; 			sha256='3d4be616e568f0a02cb7f7769bcaafda4b0969ed0f9bb4277619930b96847e70'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.5.linux-s390x.tar.gz'; 			sha256='8087d4fe991e82804e6485c26568c2e0ee0bfde00ceb9015dc86cb6bf84ef40b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.5.src.tar.gz'; 		sha256='3defb9a09bed042403195e872dcbc8c6fae1485963332279668ec52e80a95a2d'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 09 Dec 2021 16:40:07 GMT
ENV GOPATH=/go
# Thu, 09 Dec 2021 16:40:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Dec 2021 16:40:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 09 Dec 2021 16:40:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6476cb406b24c94f24348db05d154b814b14ee38860dea1625080e7e08295a80`  
		Last Modified: Thu, 02 Dec 2021 08:40:14 GMT  
		Size: 53.6 MB (53619027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96565d527970b1cc982493f96d6b317b1fbfdd7bf0ea6fd58d44942bb4f597c5`  
		Last Modified: Thu, 02 Dec 2021 10:02:24 GMT  
		Size: 4.9 MB (4937631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8c15f93136056df893ba8088992a38e90dc37210fd6ebb712413fd045c58de`  
		Last Modified: Thu, 02 Dec 2021 10:02:25 GMT  
		Size: 10.7 MB (10655914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee42e24e52cb2f9b50ab14328865298f5ae6ac159219db890afc6366ec641a46`  
		Last Modified: Thu, 02 Dec 2021 10:02:46 GMT  
		Size: 54.7 MB (54669690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387334821c5766fe1e51787a0e39fabd91c968e763b23a2444bb011742679aa3`  
		Last Modified: Fri, 03 Dec 2021 05:11:09 GMT  
		Size: 81.0 MB (80986913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df682714696dcda51e3d1450e19e12e91596cb835720e25c9c4b9e1c4bf4c16`  
		Last Modified: Thu, 09 Dec 2021 16:50:23 GMT  
		Size: 102.6 MB (102627751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19c6eaaced152f2555856673c7fddada222c210af0071877297faa8944a5ebf`  
		Last Modified: Thu, 09 Dec 2021 16:50:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; 386

```console
$ docker pull golang@sha256:a7a008a5d05707d8f90fdac0d02b9d973b4a8111ffc81194d913d95dd30679f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.2 MB (321229174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3254e59dbb19fb4af9877edfd6e0a8a00d06aaea965dffd98e427af0f35b03b7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:37 GMT
ADD file:0fd00a1dc1745744d1e95964f1f6fc73e016055aeec062f1946440b6ba68411d in / 
# Thu, 02 Dec 2021 02:39:37 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:10:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:10:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:11:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 04:42:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 04:42:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Dec 2021 16:38:36 GMT
ENV GOLANG_VERSION=1.17.5
# Thu, 09 Dec 2021 16:39:01 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.5.linux-amd64.tar.gz'; 			sha256='bd78114b0d441b029c8fe0341f4910370925a4d270a6a590668840675b0c653e'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.5.linux-armv6l.tar.gz'; 			sha256='aa1fb6c53b4fe72f159333362a10aca37ae938bde8adc9c6eaf2a8e87d1e47de'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.5.linux-arm64.tar.gz'; 			sha256='6f95ce3da40d9ce1355e48f31f4eb6508382415ca4d7413b1e7a3314e6430e7e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.5.linux-386.tar.gz'; 			sha256='4f4914303bc18f24fd137a97e595735308f5ce81323c7224c12466fd763fc59f'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.5.linux-ppc64le.tar.gz'; 			sha256='3d4be616e568f0a02cb7f7769bcaafda4b0969ed0f9bb4277619930b96847e70'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.5.linux-s390x.tar.gz'; 			sha256='8087d4fe991e82804e6485c26568c2e0ee0bfde00ceb9015dc86cb6bf84ef40b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.5.src.tar.gz'; 		sha256='3defb9a09bed042403195e872dcbc8c6fae1485963332279668ec52e80a95a2d'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 09 Dec 2021 16:39:02 GMT
ENV GOPATH=/go
# Thu, 09 Dec 2021 16:39:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Dec 2021 16:39:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 09 Dec 2021 16:39:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3dfa4acb9eec45f56cd836373cf9bf145fb45d1ae4cbc3181c21d4d01d14037d`  
		Last Modified: Thu, 02 Dec 2021 02:47:22 GMT  
		Size: 55.9 MB (55937571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3245a08f8d7007d55bcf225301e2ba4bcbd38d83c944f9a0fe4ca5811ac6bf9f`  
		Last Modified: Thu, 02 Dec 2021 03:20:35 GMT  
		Size: 5.3 MB (5283147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff3b7dd8fe63a0512b577941dbb20701dc02abfdca700e55006d84c44cfc0e1`  
		Last Modified: Thu, 02 Dec 2021 03:20:35 GMT  
		Size: 11.3 MB (11250671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394078f1578cde892a871c190a95f65490ec769aa2c7aadf9d224b49f50f1a35`  
		Last Modified: Thu, 02 Dec 2021 03:21:05 GMT  
		Size: 55.9 MB (55917753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f1427cb0a246d3bc22cdb633be11255a274719f15c3b17f7fa878a61944f16`  
		Last Modified: Fri, 03 Dec 2021 04:50:20 GMT  
		Size: 87.2 MB (87222996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44988fb6e72652fee4753616a55d065e3b556d9d1f6c7a51c3a3421170e1945e`  
		Last Modified: Thu, 09 Dec 2021 16:53:36 GMT  
		Size: 105.6 MB (105616880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9dea4a1c128e7023a16b175d3936a17a8c823f136a69eede45875882314b0d`  
		Last Modified: Thu, 09 Dec 2021 16:53:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; mips64le

```console
$ docker pull golang@sha256:b310b422250c7faf29ad2e3c3966c861a3b19035f9a9913cabb1bd3cd486829f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (292004532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ccc089576ade669c4b061108336fedece4ec91c39da746a2a44e524a570f66`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 03:08:44 GMT
ADD file:40dd380a63b1628d2ba96873bcf6a035d95f158325e90ad46ed46a6866f06c36 in / 
# Thu, 02 Dec 2021 03:08:45 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 04:09:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 04:10:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 04:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Dec 2021 00:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Dec 2021 00:11:09 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Dec 2021 17:07:29 GMT
ENV GOLANG_VERSION=1.17.5
# Thu, 09 Dec 2021 17:17:27 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.5.linux-amd64.tar.gz'; 			sha256='bd78114b0d441b029c8fe0341f4910370925a4d270a6a590668840675b0c653e'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.5.linux-armv6l.tar.gz'; 			sha256='aa1fb6c53b4fe72f159333362a10aca37ae938bde8adc9c6eaf2a8e87d1e47de'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.5.linux-arm64.tar.gz'; 			sha256='6f95ce3da40d9ce1355e48f31f4eb6508382415ca4d7413b1e7a3314e6430e7e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.5.linux-386.tar.gz'; 			sha256='4f4914303bc18f24fd137a97e595735308f5ce81323c7224c12466fd763fc59f'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.5.linux-ppc64le.tar.gz'; 			sha256='3d4be616e568f0a02cb7f7769bcaafda4b0969ed0f9bb4277619930b96847e70'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.5.linux-s390x.tar.gz'; 			sha256='8087d4fe991e82804e6485c26568c2e0ee0bfde00ceb9015dc86cb6bf84ef40b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.5.src.tar.gz'; 		sha256='3defb9a09bed042403195e872dcbc8c6fae1485963332279668ec52e80a95a2d'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 09 Dec 2021 17:17:29 GMT
ENV GOPATH=/go
# Thu, 09 Dec 2021 17:17:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Dec 2021 17:17:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 09 Dec 2021 17:17:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0ddc107271364d08a7f7838aeeb4e5f1381785e292f448280a494b1e02dc4e1d`  
		Last Modified: Thu, 02 Dec 2021 03:17:13 GMT  
		Size: 53.2 MB (53183833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a316e34103c19d4dfaa32faac9aa612895a883b0b9ee9512437d61491e352a`  
		Last Modified: Thu, 02 Dec 2021 04:25:09 GMT  
		Size: 5.1 MB (5114991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581dfe9196165133ea6c0f84d927fcd80ddb219aadb032ae7e581cd0c8ff4c15`  
		Last Modified: Thu, 02 Dec 2021 04:25:12 GMT  
		Size: 10.9 MB (10873302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45f96d0b57eaaab4f2cadb251810c0fc66f400bc38f157386a5acaf3f22c9c4`  
		Last Modified: Thu, 02 Dec 2021 04:26:03 GMT  
		Size: 53.3 MB (53296541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b4940140c11f8c885a5fdc01a9c027dddd20a2fd0ed6d8f09045e9666c858c`  
		Last Modified: Sat, 04 Dec 2021 00:49:26 GMT  
		Size: 66.9 MB (66896907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eea01cc1e4cd843017e39c9580de60925270457472b52c8826201cbcbcafb3d`  
		Last Modified: Thu, 09 Dec 2021 17:45:40 GMT  
		Size: 102.6 MB (102638832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a03612ca386710a4d14980a589f836f4639ef085057d42750aad60675962d7`  
		Last Modified: Thu, 09 Dec 2021 17:44:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:d313e403bde752f5e8282bf23cd8c04ab5b31ed3de291b3d80556c0a979e281f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (315990875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e311275c2f76eccb9760845c300a8bb4caf9c33205988183c7a71b569797d3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 07:20:49 GMT
ADD file:781003f73ff5fb7313d2bd58dc99ae83adc49c419929d32a63c29a9d45b5a554 in / 
# Thu, 02 Dec 2021 07:20:54 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 12:05:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 12:06:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 12:08:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 16:04:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 16:04:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Dec 2021 16:16:39 GMT
ENV GOLANG_VERSION=1.17.5
# Thu, 09 Dec 2021 16:17:17 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.5.linux-amd64.tar.gz'; 			sha256='bd78114b0d441b029c8fe0341f4910370925a4d270a6a590668840675b0c653e'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.5.linux-armv6l.tar.gz'; 			sha256='aa1fb6c53b4fe72f159333362a10aca37ae938bde8adc9c6eaf2a8e87d1e47de'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.5.linux-arm64.tar.gz'; 			sha256='6f95ce3da40d9ce1355e48f31f4eb6508382415ca4d7413b1e7a3314e6430e7e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.5.linux-386.tar.gz'; 			sha256='4f4914303bc18f24fd137a97e595735308f5ce81323c7224c12466fd763fc59f'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.5.linux-ppc64le.tar.gz'; 			sha256='3d4be616e568f0a02cb7f7769bcaafda4b0969ed0f9bb4277619930b96847e70'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.5.linux-s390x.tar.gz'; 			sha256='8087d4fe991e82804e6485c26568c2e0ee0bfde00ceb9015dc86cb6bf84ef40b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.5.src.tar.gz'; 		sha256='3defb9a09bed042403195e872dcbc8c6fae1485963332279668ec52e80a95a2d'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 09 Dec 2021 16:17:26 GMT
ENV GOPATH=/go
# Thu, 09 Dec 2021 16:17:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Dec 2021 16:17:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 09 Dec 2021 16:17:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6ae53eb717439cac2dd934aaff8829ad7eadd86024d1ea6efc5bcd9ad4291200`  
		Last Modified: Thu, 02 Dec 2021 07:31:08 GMT  
		Size: 58.8 MB (58819590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fac4014676b1c485dd93f21955848a174e2d21b407aa34ffef66c57f1322051`  
		Last Modified: Thu, 02 Dec 2021 12:54:45 GMT  
		Size: 5.4 MB (5402059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8244759ab55b45af369ca2cf554b0c1302663446bb7781aeb3b8dda967f75dcc`  
		Last Modified: Thu, 02 Dec 2021 12:54:46 GMT  
		Size: 11.6 MB (11626130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b784ac8d3e562c2d41fcab748557f1be3e0b77ebfafcb308f9f8cb79d966bb3e`  
		Last Modified: Thu, 02 Dec 2021 12:55:13 GMT  
		Size: 58.9 MB (58851432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c8d1d0fb048cf158a18c0bf992b6482ea105cda5185eda63d53c28fd537db6`  
		Last Modified: Fri, 03 Dec 2021 16:10:54 GMT  
		Size: 80.3 MB (80254483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7fb66e3a1b7c5e0f40e519ef1fafb00f6af1257a8ce96d4ba8ef8f9804ab660`  
		Last Modified: Thu, 09 Dec 2021 16:33:18 GMT  
		Size: 101.0 MB (101037025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80031fd868a44c57dece2cb84ba83d18d03d6c0d5be6b17e45d901b2405c5144`  
		Last Modified: Thu, 09 Dec 2021 16:32:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; s390x

```console
$ docker pull golang@sha256:e7b14bcea31e1752d27e5a1d828ff72c1cd415f515caefc1e9521753c872912c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.4 MB (294441411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a3e019826bafa8e746d78b221d90349422d703aa75e73b03d4f5199e4db9c9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 07:18:46 GMT
ADD file:56acf855563ce8cc885f3c7619508d25f809dd0547557b5e6ed0aa9fd55266f2 in / 
# Thu, 02 Dec 2021 07:18:50 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 08:19:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 08:19:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 08:20:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:27:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:27:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Dec 2021 16:41:31 GMT
ENV GOLANG_VERSION=1.17.5
# Thu, 09 Dec 2021 16:41:59 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.5.linux-amd64.tar.gz'; 			sha256='bd78114b0d441b029c8fe0341f4910370925a4d270a6a590668840675b0c653e'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.5.linux-armv6l.tar.gz'; 			sha256='aa1fb6c53b4fe72f159333362a10aca37ae938bde8adc9c6eaf2a8e87d1e47de'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.5.linux-arm64.tar.gz'; 			sha256='6f95ce3da40d9ce1355e48f31f4eb6508382415ca4d7413b1e7a3314e6430e7e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.5.linux-386.tar.gz'; 			sha256='4f4914303bc18f24fd137a97e595735308f5ce81323c7224c12466fd763fc59f'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.5.linux-ppc64le.tar.gz'; 			sha256='3d4be616e568f0a02cb7f7769bcaafda4b0969ed0f9bb4277619930b96847e70'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.5.linux-s390x.tar.gz'; 			sha256='8087d4fe991e82804e6485c26568c2e0ee0bfde00ceb9015dc86cb6bf84ef40b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.5.src.tar.gz'; 		sha256='3defb9a09bed042403195e872dcbc8c6fae1485963332279668ec52e80a95a2d'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 09 Dec 2021 16:42:03 GMT
ENV GOPATH=/go
# Thu, 09 Dec 2021 16:42:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Dec 2021 16:42:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 09 Dec 2021 16:42:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f0bfe5b50d4f7032d3e697cb821ab18746c1148d2bf1076e29427de01f0f0d31`  
		Last Modified: Thu, 02 Dec 2021 07:24:51 GMT  
		Size: 53.2 MB (53207427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78df32473c2c9009a2fde73466fc374f10162fe8cb5e40ec350cf99849eda1e1`  
		Last Modified: Thu, 02 Dec 2021 08:28:16 GMT  
		Size: 5.1 MB (5137128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60904615bb71db53520ee987ffd6d1d277f29ccc77c39bfc8f40123924b4badf`  
		Last Modified: Thu, 02 Dec 2021 08:28:17 GMT  
		Size: 10.8 MB (10761085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05998656d393732a5c8f599ef697a5f1c51ecc104f0711885e652ad9a42fbfc9`  
		Last Modified: Thu, 02 Dec 2021 08:28:32 GMT  
		Size: 54.0 MB (54041540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07f90c846916cda9402c221911d3b1a5a03c0545fd77d07d55c72db1ba0a117`  
		Last Modified: Thu, 02 Dec 2021 17:31:46 GMT  
		Size: 65.5 MB (65502373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd816a64c2ba1416212baf69e41c045a6c503ac4bc4f658d1d24927f6b1b2a8`  
		Last Modified: Thu, 09 Dec 2021 16:51:41 GMT  
		Size: 105.8 MB (105791703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b238cb937549c0a990ab977b050388105e4264265d8a0c0a090670f5f19f3118`  
		Last Modified: Thu, 09 Dec 2021 16:51:28 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.20348.405; amd64

```console
$ docker pull golang@sha256:2e583daa64194e57f31717aaa3df24335542c0ca6b352670f3dee7bfdf177665
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2362627964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4f34c8ec874488b7fd7667cfbf3b9a2f69e5f331347eb41dae4e4843aa8c81`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 08 Dec 2021 01:54:07 GMT
RUN Install update ltsc2022-amd64
# Wed, 15 Dec 2021 00:40:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Dec 2021 00:40:22 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 Dec 2021 00:40:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 Dec 2021 00:40:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 Dec 2021 00:40:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 Dec 2021 00:41:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 Dec 2021 00:41:27 GMT
ENV GOPATH=C:\go
# Wed, 15 Dec 2021 00:42:02 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 Dec 2021 01:09:06 GMT
ENV GOLANG_VERSION=1.17.5
# Wed, 15 Dec 2021 01:12:13 GMT
RUN $url = 'https://dl.google.com/go/go1.17.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '671faf99cd5d81cd7e40936c0a94363c64d654faa0148d2af4bbc262555620b9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 Dec 2021 01:12:15 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4d1d74adc6a92e44b3cd592ec9459f1fff926eaf6fc20bb7526360bec71aefc0`  
		Size: 939.1 MB (939072515 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0b41c99bb368eaadf91343c8bfccaa11a92f02d60d86febeda9e009eaed579fa`  
		Last Modified: Wed, 15 Dec 2021 01:51:03 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7eb1a5e7dea0a53c9ea436a1dbe9567968300217e1ad744ef5fc0af5fd17e3d`  
		Last Modified: Wed, 15 Dec 2021 01:51:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18dfd01553a8cab256080e47c5c8111521866afb32c6f694b59683dbe2416be`  
		Last Modified: Wed, 15 Dec 2021 01:51:01 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad7e1ebdc3cbf59de41a76791006597e0f8927c01920f858f33f65d36ce0e4b`  
		Last Modified: Wed, 15 Dec 2021 01:51:01 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0532fcfb6c734340e3e1ab8c6c1416b21ae9239967a945bb1d9921e31232300d`  
		Last Modified: Wed, 15 Dec 2021 01:51:00 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b8a70b5f349c15ad0f783b3b04b14ea2a68730ecd0f0b9ea63f970c9870505`  
		Last Modified: Wed, 15 Dec 2021 01:51:07 GMT  
		Size: 25.7 MB (25708582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc2b44cb36f7cbe88bbfafea3b88eae5ec8d2554ac7e9934e5598ac613d7b1`  
		Last Modified: Wed, 15 Dec 2021 01:50:58 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f26f8a160719f2d2f778607a2ef1c8a213b65b76cdd2e67ced5d9ca5eef763`  
		Last Modified: Wed, 15 Dec 2021 01:50:59 GMT  
		Size: 534.0 KB (534011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f2b896d0d1b0352581accd1f6fb741ab47cf677e5009a5f24b25aa8b6bd264`  
		Last Modified: Wed, 15 Dec 2021 01:57:07 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c5c9b36e76d795af01d91c3bc9caf34efcccb9495ae2fa7271f442061bfdbb`  
		Last Modified: Wed, 15 Dec 2021 01:57:40 GMT  
		Size: 145.6 MB (145602903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7fcef36990e7cd881fdf895909687d53d11969584cf97991f936e01f145166`  
		Last Modified: Wed, 15 Dec 2021 01:57:07 GMT  
		Size: 1.6 KB (1571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.17763.2366; amd64

```console
$ docker pull golang@sha256:78c28420b41dddec7184a206a34126ebaecf223e10352e94e38e7222437e30d8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2879842281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a983bdfe4cd067c917c895f94c301efec12c6a5406c94148fcbcec26884e61`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 07 Dec 2021 04:56:01 GMT
RUN Install update 1809-amd64
# Wed, 15 Dec 2021 00:45:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Dec 2021 00:45:53 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 Dec 2021 00:45:54 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 Dec 2021 00:45:55 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 Dec 2021 00:45:57 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 Dec 2021 00:48:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 Dec 2021 00:48:32 GMT
ENV GOPATH=C:\go
# Wed, 15 Dec 2021 00:50:15 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 Dec 2021 01:12:34 GMT
ENV GOLANG_VERSION=1.17.5
# Wed, 15 Dec 2021 01:16:32 GMT
RUN $url = 'https://dl.google.com/go/go1.17.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '671faf99cd5d81cd7e40936c0a94363c64d654faa0148d2af4bbc262555620b9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 Dec 2021 01:16:34 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ee7a7ea9cf22f75886179907a41810a992e21f3d0c57cc10d2147ce9237701c`  
		Size: 990.3 MB (990271574 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aabd70b2463e8240ac41c7d726f6fcfc25424b74f20bb5e8642dbb9bc2b789c8`  
		Last Modified: Wed, 15 Dec 2021 01:53:57 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8639e414e28c147782b979f15c11cacfe3670dc5a898f9d0fc95ebadeb3f5a`  
		Last Modified: Wed, 15 Dec 2021 01:53:57 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a032d0c95307404bb3f5ccd3d69031082f2a3a1ab0eadd1ce3b12d931bd3e6`  
		Last Modified: Wed, 15 Dec 2021 01:53:54 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4ddbbfd5905588817615b135bf7431f7a67d054028d23d234b326a68097b39`  
		Last Modified: Wed, 15 Dec 2021 01:53:53 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22bfacbdbf128875fdbf7e39f4d3b2030fe3e310d9069f2a55924a2cf3e91ac`  
		Last Modified: Wed, 15 Dec 2021 01:53:53 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f566d739bb0bdf88e33c8c46b5751f6dcdf79a57d123fc0a559e3e189924cf4c`  
		Last Modified: Wed, 15 Dec 2021 01:54:00 GMT  
		Size: 25.5 MB (25463347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e73a67af47aee0d209f8dfd5ea371efb1b0c5205c8d5be95680c9675c302cb`  
		Last Modified: Wed, 15 Dec 2021 01:53:51 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9036358af62e5d57f75caa56f99c1236c8bd7a61e2dd902f023c4ab45877aee`  
		Last Modified: Wed, 15 Dec 2021 01:53:51 GMT  
		Size: 341.0 KB (341030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc974df3fe45444aea125b83adabae2710ee41380c4942cf6e9f3ec314ad44ae`  
		Last Modified: Wed, 15 Dec 2021 01:58:00 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3bca46d6d1c61b00e6039bef7fb53bdbcb27e1a704241d9194c9ac7df77503`  
		Last Modified: Wed, 15 Dec 2021 01:58:30 GMT  
		Size: 145.4 MB (145421900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d466e52bb071b3ebbc307bf2043ee7c57e2dfe885c586bfdf6cc0e7d4068d851`  
		Last Modified: Wed, 15 Dec 2021 01:57:57 GMT  
		Size: 1.6 KB (1560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.14393.4825; amd64

```console
$ docker pull golang@sha256:ef241ee21778edcf2279509fbf43d492938f471ba8ae7b03548688badb2500bf
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6450360107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310cc40b76dc3bb98696749abd725149a54ad822446937efc277ddf1e4469a4a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 08 Dec 2021 08:38:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Dec 2021 00:54:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Dec 2021 00:54:10 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 Dec 2021 00:54:11 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 Dec 2021 00:54:12 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 Dec 2021 00:54:13 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 Dec 2021 00:56:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 Dec 2021 00:56:06 GMT
ENV GOPATH=C:\go
# Wed, 15 Dec 2021 00:57:05 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 Dec 2021 01:16:47 GMT
ENV GOLANG_VERSION=1.17.5
# Wed, 15 Dec 2021 01:21:14 GMT
RUN $url = 'https://dl.google.com/go/go1.17.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '671faf99cd5d81cd7e40936c0a94363c64d654faa0148d2af4bbc262555620b9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 Dec 2021 01:21:16 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d026d646213ccf73d9f0584941d108253d62e73df2a74e070776884b7b0242b`  
		Size: 2.2 GB (2204728802 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e473536e08c92a08f92b05dcf009604fd3f0425171a596a8efeeeb5f69746a24`  
		Last Modified: Wed, 15 Dec 2021 01:54:48 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a097f1c6da1d1d6045b118791cf5076a7360b91373bae76209dbfa4609e661`  
		Last Modified: Wed, 15 Dec 2021 01:54:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32ba63b1b2e53158cc5902f8107d4421a8a12f929e4c67242ce3fa2cbc0553a`  
		Last Modified: Wed, 15 Dec 2021 01:54:46 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80515b90b11c42a574f7c31fcadd4d31668f93066540f17e3b0905fe12eacb59`  
		Last Modified: Wed, 15 Dec 2021 01:54:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002818a5b378a085c7e0c0f95258fb97a557afe6e00e35912ce0902965cd52d8`  
		Last Modified: Wed, 15 Dec 2021 01:54:44 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6826b991d808a789450cae893bca8fe52c185ba68567aa7c9ec3246d8b657b0`  
		Last Modified: Wed, 15 Dec 2021 01:54:51 GMT  
		Size: 25.4 MB (25419377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd193319409f137bee128603a046e69ee6159b35485612b9e65f81b4ecf814e6`  
		Last Modified: Wed, 15 Dec 2021 01:54:42 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915b9557c339e8e1394558abd44be62c971aa5b7a6294be429b85d48fdf24bfe`  
		Last Modified: Wed, 15 Dec 2021 01:54:42 GMT  
		Size: 327.7 KB (327679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d59d0085a49b20c89b965a3123994487d2e7783745047826b6d634ec132a3b`  
		Last Modified: Wed, 15 Dec 2021 01:58:48 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e325c3f626db4247c9a89671cc5c32e99fe3ddb747cef2ff9412048b364ea9ef`  
		Last Modified: Wed, 15 Dec 2021 01:59:22 GMT  
		Size: 149.9 MB (149887140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82982f6520d1d8a9a9c8dd886a740c4aca31cb91ff724690626f63744c02042d`  
		Last Modified: Wed, 15 Dec 2021 01:58:48 GMT  
		Size: 1.5 KB (1537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

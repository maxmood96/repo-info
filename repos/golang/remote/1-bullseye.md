## `golang:1-bullseye`

```console
$ docker pull golang@sha256:8e667633e3dd0eb79f573d07a07c3f54a737697a0afac6f7ece027e54945c593
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

### `golang:1-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:108962cc6510ab38693c529b1b8637956f902237728bbe5f16dcbcdc1556d5a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346102397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5993351274bca358c6673e6464b5efb48cd5a4403aeadec95196cdf08c685fa`
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
# Fri, 03 Dec 2021 10:58:37 GMT
ENV GOLANG_VERSION=1.17.3
# Fri, 03 Dec 2021 10:58:54 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 03 Dec 2021 10:58:56 GMT
ENV GOPATH=/go
# Fri, 03 Dec 2021 10:58:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 10:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 03 Dec 2021 10:58:57 GMT
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
	-	`sha256:a46d5aceda6a3c49f916a77000b2377e7599c786d01370b48a531f5ca5f8fb42`  
		Last Modified: Fri, 03 Dec 2021 11:02:42 GMT  
		Size: 134.8 MB (134804706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e59c4f341edfe59a3fb6ace0230f8d34f28e92abc37fc1dffd7a7f22c9aea5`  
		Last Modified: Fri, 03 Dec 2021 11:02:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; arm variant v5

```console
$ docker pull golang@sha256:cb316591db8fbb25ae9e6e3af76a568f58adf40e37413da55c1a0120b39825e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294536157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5084b56366a56525e2fe235823c8efe4b5916b24ac99be5c0b518908809459d`
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
# Fri, 03 Dec 2021 09:50:10 GMT
ENV GOLANG_VERSION=1.17.3
# Fri, 03 Dec 2021 09:54:23 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 03 Dec 2021 09:54:25 GMT
ENV GOPATH=/go
# Fri, 03 Dec 2021 09:54:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 09:54:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 03 Dec 2021 09:54:28 GMT
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
	-	`sha256:cc421ab71e506c907f9781466543dac25a16f806837953a88590346d17625d15`  
		Last Modified: Fri, 03 Dec 2021 10:08:54 GMT  
		Size: 105.4 MB (105404198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f571aa758b34a99ba9543f9cdd20edc7895e6e0d482bc1ebf1daec02237906`  
		Last Modified: Fri, 03 Dec 2021 10:07:46 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:23b6aa097fca6c0f339648e743a1bd06ad6aa86902a96d8426d1e0ec8d49421f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283413962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540fb15c6e6933898a729275b462c7455e5d7d771edc9ff7a3273e7496ab5e28`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 01:59:07 GMT
ADD file:43b45f65ff4ba720f6f9a107b5f80818d5ea6ebc4835840b11e9a506351da32f in / 
# Wed, 17 Nov 2021 01:59:08 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:41:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 02:42:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 02:43:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 15:21:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 15:21:29 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 15:21:30 GMT
ENV GOLANG_VERSION=1.17.3
# Tue, 30 Nov 2021 04:08:27 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 30 Nov 2021 04:08:28 GMT
ENV GOPATH=/go
# Tue, 30 Nov 2021 04:08:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Nov 2021 04:08:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 30 Nov 2021 04:08:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dbbf55137aab3c7acd1e012a70f1ea1adeaef8d39b474829965d3480a02bf572`  
		Last Modified: Wed, 17 Nov 2021 02:14:27 GMT  
		Size: 50.1 MB (50134152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1ae7a04cee77523f9e09a62b28632c56a700d0c481be7cddc566c835e7a71d`  
		Last Modified: Wed, 17 Nov 2021 03:04:13 GMT  
		Size: 4.9 MB (4922782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66894dfea839186e94448f6c25a37c6b3b1b42cece6332cc9d36336917e18a4`  
		Last Modified: Wed, 17 Nov 2021 03:04:14 GMT  
		Size: 10.2 MB (10216965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4502933ba6aa2071501257e094faa363699dc23995f798a124d688c2523240af`  
		Last Modified: Wed, 17 Nov 2021 03:05:05 GMT  
		Size: 50.3 MB (50327664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98948793a9adf3f1679c517671bd214bcf9e4ca905cb23951ae732167f41f5f`  
		Last Modified: Thu, 18 Nov 2021 15:31:47 GMT  
		Size: 64.7 MB (64727171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a8915911f4947e7905e868f5a17b0e61716095ba4c3abf76e4ae6748eb2d00`  
		Last Modified: Tue, 30 Nov 2021 04:30:14 GMT  
		Size: 103.1 MB (103085072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109a948c055d69a5e30bfa334d18b0ebbab31f63ab8d4a0990c62ebb7239a927`  
		Last Modified: Tue, 30 Nov 2021 04:29:07 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:1c4136362f61a74d9f64fac90226f9da55d8d6b61c316f71bc837fdffe6275e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.5 MB (307494083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa41b175271fd442aafbae5984a8d8857519144399d8d353c78e7273e05bd4a`
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
# Fri, 03 Dec 2021 05:06:27 GMT
ENV GOLANG_VERSION=1.17.3
# Fri, 03 Dec 2021 05:06:40 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 03 Dec 2021 05:06:41 GMT
ENV GOPATH=/go
# Fri, 03 Dec 2021 05:06:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 05:06:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 03 Dec 2021 05:06:45 GMT
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
	-	`sha256:d12c8da18c64aeb49358febe774ee8c2ae1ecf875c751969784919832f5e9034`  
		Last Modified: Fri, 03 Dec 2021 05:11:13 GMT  
		Size: 102.6 MB (102624783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4a745a31bc727dbe00da84cba0007e7a9e6d8b91e3e9e13f97330efd9e6be2`  
		Last Modified: Fri, 03 Dec 2021 05:10:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; 386

```console
$ docker pull golang@sha256:756307df1316bac4ab70c72ea304d74dd6d8e367be2e5abbf0eb6142d423ad8a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.2 MB (321229559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43da59732f3205e707d6d4da05fb17aec10d29aba2381de10537f186fbb9cdf7`
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
# Fri, 03 Dec 2021 04:42:23 GMT
ENV GOLANG_VERSION=1.17.3
# Fri, 03 Dec 2021 04:42:52 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 03 Dec 2021 04:42:55 GMT
ENV GOPATH=/go
# Fri, 03 Dec 2021 04:42:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 04:42:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 03 Dec 2021 04:42:56 GMT
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
	-	`sha256:3576bd75c552413356532d7c8650dc0023411fc309288193e78633040e3216b2`  
		Last Modified: Fri, 03 Dec 2021 04:50:24 GMT  
		Size: 105.6 MB (105617264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87d11456572a6929434b1444db0650aafe2605fe3726e06489b71aeb6cafc65`  
		Last Modified: Fri, 03 Dec 2021 04:49:44 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; mips64le

```console
$ docker pull golang@sha256:852f794c768822600e7f3af0ec4e62fc58f339a025e985a3a06d37d54a45667c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (292005455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43af522d7774e0690fb6b18674aad825e71b0cd8dd6932de0fd27a15d2424c5a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:09:46 GMT
ADD file:2971df49f24648b8d5166d87e392e2547d5b03469356f20d112ce6feb3c329fc in / 
# Wed, 17 Nov 2021 02:09:47 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 08:29:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 08:30:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 08:31:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 19 Nov 2021 00:29:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 19 Nov 2021 00:29:28 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 00:29:29 GMT
ENV GOLANG_VERSION=1.17.3
# Tue, 30 Nov 2021 01:17:21 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 30 Nov 2021 01:17:23 GMT
ENV GOPATH=/go
# Tue, 30 Nov 2021 01:17:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Nov 2021 01:17:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 30 Nov 2021 01:17:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b095a0b63d99a4c4cd9c1c353f381a69ef041e6f80798d807ae51a34b04920a0`  
		Last Modified: Wed, 17 Nov 2021 02:18:22 GMT  
		Size: 53.2 MB (53183806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2e37aff1692726b1ea3dd0b4eeb684072527295f8e981d3c45825327daea19`  
		Last Modified: Wed, 17 Nov 2021 08:45:38 GMT  
		Size: 5.1 MB (5114925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d4c0302ddd7a6cb573a156076dba9c593e09a0c321b32ae0f1da2bd36bc754`  
		Last Modified: Wed, 17 Nov 2021 08:45:41 GMT  
		Size: 10.9 MB (10873360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cde5eca075420fcfc6498f454dc040f1e236dea180a82a0d27d7a739ffd41c1`  
		Last Modified: Wed, 17 Nov 2021 08:46:32 GMT  
		Size: 53.3 MB (53296603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd05400d2151a7dfa5d38f97214fc54bf0d399823854c2c1035706251c87403`  
		Last Modified: Fri, 19 Nov 2021 01:08:03 GMT  
		Size: 66.9 MB (66896924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5717ee87d047778dad4caaabd34b585aef8547f08fa0089ed96845dfea4fd3`  
		Last Modified: Tue, 30 Nov 2021 01:45:40 GMT  
		Size: 102.6 MB (102639711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f46769ca7e960546e6259842c89efc27a60cb589bd6a87913c040b1d8e63000`  
		Last Modified: Tue, 30 Nov 2021 01:44:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; ppc64le

```console
$ docker pull golang@sha256:610b53542590e4b13aa55086ff7d6996f2473c9adf6a2b9e0924f09d5a285649
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (315979117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a60a745b9155f00233e9d60035f6ecbf0a6ee854fac6c224b96ae21b78d5bce`
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
# Fri, 03 Dec 2021 16:04:43 GMT
ENV GOLANG_VERSION=1.17.3
# Fri, 03 Dec 2021 16:05:14 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 03 Dec 2021 16:05:22 GMT
ENV GOPATH=/go
# Fri, 03 Dec 2021 16:05:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 16:05:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 03 Dec 2021 16:05:32 GMT
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
	-	`sha256:7773475a8649278d4b0d54d4b9708e09c3fef66e0bf4fa9abe8de17efb3fdb15`  
		Last Modified: Fri, 03 Dec 2021 16:11:02 GMT  
		Size: 101.0 MB (101025268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a081358ca4e814e62186dfa5948cbebde827590344d2077aa8c060706c63ac`  
		Last Modified: Fri, 03 Dec 2021 16:10:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; s390x

```console
$ docker pull golang@sha256:e357140d1894bef28d74f7246b34fe35a4b50db807039724a3c4bff8daec8002
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.4 MB (294440954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f94afcc9e5f63c2098648a6e2b467646d6218edd1d1fa82c32c3e3d30359bf9`
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
# Thu, 02 Dec 2021 17:27:35 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 02 Dec 2021 17:27:51 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 02 Dec 2021 17:27:57 GMT
ENV GOPATH=/go
# Thu, 02 Dec 2021 17:27:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 17:27:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 02 Dec 2021 17:27:58 GMT
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
	-	`sha256:f86f86b22a6585095740d4badee7c1a0ba0bcf8d14fedd4e03a9b56fa3679e9f`  
		Last Modified: Thu, 02 Dec 2021 17:31:50 GMT  
		Size: 105.8 MB (105791245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068a19caae45ac9e349b3fba9198231c894ae866114218b36480d4344e0aa010`  
		Last Modified: Thu, 02 Dec 2021 17:31:37 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

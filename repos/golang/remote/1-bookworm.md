## `golang:1-bookworm`

```console
$ docker pull golang@sha256:688ad7f282ce711cc28676531f45d5b840790e28a689fbd4e8e4ac181e23e9c4
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
$ docker pull golang@sha256:8269ba28a2798bdf9ca2ecdad99ed0503c61154794fa74f0dc84e35f6b375ae3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297165607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dec4c3381a67c6ff77cbe0fc9390fc02d2e5c2284f62cbc48c4eb97f613aa08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:15 GMT
ADD file:7d8adf68670e8dc2af6b8603870ea610fc65ecbb08799f2ca6a3134f5d47d289 in / 
# Tue, 19 Dec 2023 01:20:16 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:32:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:32:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 18:51:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 18:51:19 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:20:03 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:20:11 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.6.linux-mips64le.tar.gz'; 			sha256='eb309a611dfec52b98805e05bafbe769d3d5966aef05f17ec617c89ee5a9e484'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		go version
# Tue, 09 Jan 2024 22:20:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:20:12 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:20:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:20:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:20:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bc0734b949dcdcabe5bfdf0c8b9f44491e0fce04cb10c9c6e76282b9f6abdf01`  
		Last Modified: Tue, 19 Dec 2023 01:24:35 GMT  
		Size: 49.6 MB (49561579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5de22c0f5cd2ea2bb6c0524478db95bff5a294c99419ccd4a9d3ccc9873bad9`  
		Last Modified: Tue, 19 Dec 2023 04:41:08 GMT  
		Size: 24.0 MB (24046123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917ee5330e73737d6095a802333d311648959399ff2c067150890162e720f863`  
		Last Modified: Tue, 19 Dec 2023 04:41:27 GMT  
		Size: 64.1 MB (64131542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed956b3d08c0b1903d9af3e6850930eacf865b23f62bd8cf46eb1de1325c39b`  
		Last Modified: Tue, 19 Dec 2023 18:53:12 GMT  
		Size: 92.4 MB (92364552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6137e1fd63b6dee7575b1eac27fff24ea1655225472bdc59903f4e100bd3a7`  
		Last Modified: Tue, 09 Jan 2024 22:25:53 GMT  
		Size: 67.1 MB (67061655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abe907dfc234756afbb8d63ae6afd0f123e24462fcdc1562f8ec54c087e0937`  
		Last Modified: Tue, 09 Jan 2024 22:25:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:7788851c6e8d3b3a3eb2cce63453411c789da47b0eb0aa16899e55f52639d43c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258356123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea68c9e09fbc4ee989dc72b83c39f6d6cc479eca0f31b32ec3d78f1244e2ebf9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:07:39 GMT
ADD file:1633615de1824a95e35747f0133e90ab5ddc138574a83fb9c4f337cf45762574 in / 
# Tue, 19 Dec 2023 02:07:39 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:54:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:55:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 16:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 16:42:08 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:57:41 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:57:58 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.6.linux-mips64le.tar.gz'; 			sha256='eb309a611dfec52b98805e05bafbe769d3d5966aef05f17ec617c89ee5a9e484'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		go version
# Tue, 09 Jan 2024 22:57:59 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:57:59 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:58:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:58:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:89cc9e7932dc0f797e6c3fc84b4c6868fedaca1b174b38a51e152a23a643be7a`  
		Last Modified: Tue, 19 Dec 2023 02:11:28 GMT  
		Size: 45.2 MB (45156699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1cce8fac77d35b90037c77fcb46603ed4cdc1388009887c5132cbdf3531132`  
		Last Modified: Tue, 19 Dec 2023 08:06:19 GMT  
		Size: 21.9 MB (21949134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258af69dcb8426bcc3ebc63b670048d9d4191fd206986dd72f83a247768f7f65`  
		Last Modified: Tue, 19 Dec 2023 08:06:39 GMT  
		Size: 59.2 MB (59216125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319f226897e48df7637a7febe66c37fd1181e61ac179cf0f35663c749d3033a5`  
		Last Modified: Tue, 19 Dec 2023 16:44:20 GMT  
		Size: 66.2 MB (66201911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f3497d843660d079b8827ac7e7b2c08953fc52e852f691737b36baa3351223`  
		Last Modified: Tue, 09 Jan 2024 23:08:30 GMT  
		Size: 65.8 MB (65832098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfeede393d919565622523d50a544f60be6b284037a965bfb2de2f243501a9a`  
		Last Modified: Tue, 09 Jan 2024 23:08:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:aec7f36a37b8070b0c77da9c4850047a68445e2f5aaab9cc60bcabd5435433ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.7 MB (287720255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731876895c44807ed8434898f52ed92780286d7756b856efba10b65030576673`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:02 GMT
ADD file:412f80f75ed3e520f767e70b6b27fc81807f62fc5c6e5adf756507e33af9fa6b in / 
# Tue, 19 Dec 2023 01:41:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:34:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 20:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 20:01:39 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:39:37 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:39:44 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.6.linux-mips64le.tar.gz'; 			sha256='eb309a611dfec52b98805e05bafbe769d3d5966aef05f17ec617c89ee5a9e484'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		go version
# Tue, 09 Jan 2024 22:39:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:39:46 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:39:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:39:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:39:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b66b4ecd3ecfb67b3b7a2a44b0199cbdfc94965c8bd3fefab75cd2e612799740`  
		Last Modified: Tue, 19 Dec 2023 01:44:14 GMT  
		Size: 49.6 MB (49592259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c641d36985b2db859fc64c43a6dbf7c25cdf73e5d16d107fab1d95a840bb4e1`  
		Last Modified: Tue, 19 Dec 2023 11:42:17 GMT  
		Size: 23.6 MB (23582271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd8544b6e15c7a4096b1f48a67fb5bed2efba509fca597f1c164b582ab01c02`  
		Last Modified: Tue, 19 Dec 2023 11:42:35 GMT  
		Size: 64.0 MB (63988289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4149fb3c15c417a9ef7f8c7d04c13407fa7ee49bee88bcc4bd46626209e57a`  
		Last Modified: Tue, 19 Dec 2023 20:03:18 GMT  
		Size: 86.4 MB (86396122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e7cecbec8d6a8840176f30618cc8d2bcce9f76f0fd87b43df970467c7ffc75`  
		Last Modified: Tue, 09 Jan 2024 22:44:04 GMT  
		Size: 64.2 MB (64161159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7ee12d7f34243bcd246c2c74e1abaf89ecc750d0b827ea613cc2fcdd994986`  
		Last Modified: Tue, 09 Jan 2024 22:43:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:55f4ca6a77f6f8df5380aed13866b6810da22d503be374edd670af11dd909d05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296736086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9604cc9ba5e3e627e2a200f343afae375ecc10d8641cb110b7f7bb5fdf891f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:38:52 GMT
ADD file:c20aace531a43765f8c1b69c75d7f46a4ab443377a663ab47e0bb2ceb013a611 in / 
# Tue, 19 Dec 2023 01:38:55 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:25:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Dec 2023 00:48:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Dec 2023 00:48:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:38:30 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:38:43 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.6.linux-mips64le.tar.gz'; 			sha256='eb309a611dfec52b98805e05bafbe769d3d5966aef05f17ec617c89ee5a9e484'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		go version
# Tue, 09 Jan 2024 22:38:44 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:38:44 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:38:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:38:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:38:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9b51fe964cb335e4bc3b61dca07146c7a0aa4c31e5ae9fec90f2a950818a21a4`  
		Last Modified: Tue, 19 Dec 2023 01:43:18 GMT  
		Size: 50.6 MB (50582312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fb12d611be5489722de01a39ed212f0e3a188c63409b25d91b51db39be5cb9`  
		Last Modified: Tue, 19 Dec 2023 03:36:07 GMT  
		Size: 24.9 MB (24883625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a33947619311fada004e8d19522ee356dc9b4aefb1e43a67f9b239a793bef`  
		Last Modified: Tue, 19 Dec 2023 03:36:31 GMT  
		Size: 66.0 MB (65980921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51de471cfdd31c920400294e0d9d5101f4095c83e4122039556ef97f97c91bd0`  
		Last Modified: Wed, 20 Dec 2023 00:50:50 GMT  
		Size: 89.8 MB (89767642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb2f3bbf7d49a76fde7e957cf032eb42a7eb96e8e5359f620bdaa318daf121d`  
		Last Modified: Tue, 09 Jan 2024 22:47:32 GMT  
		Size: 65.5 MB (65521430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbda8571c6ad27cc89cbc7dcf208c629762be65d65a49329d3e9f88d7723b0bc`  
		Last Modified: Tue, 09 Jan 2024 22:47:16 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:d97b65e53830cce9850b67cd3f16f2f305305e55560211dade7b9f87076aed0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268061726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef56f0324aa173cdfadfbed93a634ec4f6159758c2881a948b7a809a9f5fecc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:12:55 GMT
ADD file:87d7b313e4309f5e9ad824dfd7dc6f9a85458ccb7056f5001dc6066e964eabcb in / 
# Tue, 19 Dec 2023 02:13:00 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:52:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Dec 2023 13:41:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Dec 2023 13:41:39 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:07:50 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:08:42 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.6.linux-mips64le.tar.gz'; 			sha256='eb309a611dfec52b98805e05bafbe769d3d5966aef05f17ec617c89ee5a9e484'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		go version
# Tue, 09 Jan 2024 22:08:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:08:57 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:09:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:09:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:09:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:659946beb815c8c0157caa0571c5512c4508ff0fe3bbb59e9513e933c7023366`  
		Last Modified: Tue, 19 Dec 2023 02:23:53 GMT  
		Size: 49.5 MB (49548860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65baf0481eb7e4d5215eb36d70ba1c460bd80282806d1e361c83f4c442ed9adf`  
		Last Modified: Tue, 19 Dec 2023 03:18:48 GMT  
		Size: 23.6 MB (23630657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3c3175afa4d6bd28886bc3fbd23dcc38227468b970b9dc18e6730d47f29cd0`  
		Last Modified: Tue, 19 Dec 2023 03:19:43 GMT  
		Size: 63.0 MB (62963274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fb41c0928fb62f5e7eb2170f368bde19585bc1b27c2804903996f4dd5caf0b`  
		Last Modified: Wed, 20 Dec 2023 14:12:54 GMT  
		Size: 69.7 MB (69716933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbf945db7a221d5826557ac8df90e91c318515dd1c9000fa175eb9721587937`  
		Last Modified: Tue, 09 Jan 2024 22:38:05 GMT  
		Size: 62.2 MB (62201876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1822b5a07940feb49af4add744db82120f98e2e54210e5780fd534ad8a7c810e`  
		Last Modified: Tue, 09 Jan 2024 22:37:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:f99c719a4610957e6f4565cf02bcdd9f1809de6b91a394513872062b1536a27d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303361385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0aa3084b9cf66324ee71ca9b54bea3f5f7a49abdadcc8b5498f4693e7ed4f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:31 GMT
ADD file:1728d055717ccd4f036c355a84deb6451942dd6e2c7998ee9d9d4edb3c02f7f4 in / 
# Tue, 19 Dec 2023 01:21:34 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:43:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:44:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 21:20:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 21:20:29 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:16:44 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:17:01 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.6.linux-mips64le.tar.gz'; 			sha256='eb309a611dfec52b98805e05bafbe769d3d5966aef05f17ec617c89ee5a9e484'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		go version
# Tue, 09 Jan 2024 22:17:05 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:17:05 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:17:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:17:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:17:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b5382b02d02e48b7676d14a370941b889916302c0c0a4ce6eed6a87ddd65e5a3`  
		Last Modified: Tue, 19 Dec 2023 01:25:50 GMT  
		Size: 53.6 MB (53557744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bef292d6dca0f2e01dadfb6697f50846fd2abe37345bd28c4b40d155bd3efb`  
		Last Modified: Tue, 19 Dec 2023 12:22:47 GMT  
		Size: 25.7 MB (25696155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397f3d69bf2380c69602528735990cbdbea6905ab14ff27daaf1ccd8e0599ad3`  
		Last Modified: Tue, 19 Dec 2023 12:23:09 GMT  
		Size: 69.6 MB (69582346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69caad595f2299d3bbf2cfb77feccc3afd23d59c5f559ba5861def5a9b000f0d`  
		Last Modified: Tue, 19 Dec 2023 21:24:09 GMT  
		Size: 90.3 MB (90335225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2409dbd7a17510703d7a22677263545e792ce07f7a1e50827f9f2c396124763c`  
		Last Modified: Tue, 09 Jan 2024 22:25:43 GMT  
		Size: 64.2 MB (64189761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8948bfad70b6345e6ccc0a0e800692a7e46454dfe970c1ab08aba45559f4d722`  
		Last Modified: Tue, 09 Jan 2024 22:25:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:f21d62ce09b5365a654d0336c3f125015880a70de0d4ef58b0c07a6b19dfca72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 MB (270289241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172195de2a12a93430564b6189f38fb95f578f5a90010103fbdb86925b236be1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:12 GMT
ADD file:5e36efc0891837fbd669c10cc5082f41b4ad22190feb2d516f4f0efd4890e772 in / 
# Tue, 19 Dec 2023 01:42:20 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:43:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:43:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:32:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:32:52 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:42:31 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:42:42 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.6.linux-mips64le.tar.gz'; 			sha256='eb309a611dfec52b98805e05bafbe769d3d5966aef05f17ec617c89ee5a9e484'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		go version
# Tue, 09 Jan 2024 22:42:47 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:42:47 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:42:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:42:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:42:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9ba06e3db941501f326f297f1b24643ce2b142581fc9f396effcbc7c63df4938`  
		Last Modified: Tue, 19 Dec 2023 01:47:24 GMT  
		Size: 47.9 MB (47917679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e564b911d9e033f9a67fcf5b0ddaad82153cceb2c4f54b63054a3c41bee756a1`  
		Last Modified: Tue, 19 Dec 2023 07:53:32 GMT  
		Size: 24.0 MB (24042818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea66ebaf962eb06e4d585525f721841b7431908eb06730bf77ec7484806f571`  
		Last Modified: Tue, 19 Dec 2023 07:53:47 GMT  
		Size: 63.1 MB (63127874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba001fe6ac86b58f0a8b0f69dc7fa7eed269c7494edda5c204fbf7f07a7fa4b8`  
		Last Modified: Tue, 19 Dec 2023 11:36:45 GMT  
		Size: 68.9 MB (68916174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea16c705221c90ee69b524ca82f8b8c5cde1e1b6fa6b8b2f0f55ce999131247c`  
		Last Modified: Tue, 09 Jan 2024 22:50:06 GMT  
		Size: 66.3 MB (66284540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8be8e8781a99375fbeebb0068114e7d5a8c3593df8b9e5f0710232f5734b9f`  
		Last Modified: Tue, 09 Jan 2024 22:49:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

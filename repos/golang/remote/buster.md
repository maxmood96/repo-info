## `golang:buster`

```console
$ docker pull golang@sha256:ff4ab723f30f8a8f74ee5c5c3d780aa0f3401ba7d746f1bc3372ac3fd67898cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `golang:buster` - linux; amd64

```console
$ docker pull golang@sha256:a23a7e49a820f9ae69df0fedf64f037cb15b004997effa93ec885e5032277bc1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.8 MB (317798991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb42f2526a722fa033cee51bc74088849afa3c22b843c33c4c7a5644414f5cd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:27 GMT
ADD file:575bf0d00d72810609a4118728923f11625b43de536352fe69a341086e4ebfd1 in / 
# Fri, 12 Mar 2021 02:20:28 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:49:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:49:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 04:13:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 04:14:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Mar 2021 04:14:00 GMT
ENV GOLANG_VERSION=1.16.2
# Sat, 13 Mar 2021 04:14:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Sat, 13 Mar 2021 04:14:12 GMT
ENV GOPATH=/go
# Sat, 13 Mar 2021 04:14:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Mar 2021 04:14:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 13 Mar 2021 04:14:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e22122b926a1a853d61887fa35c3fe53e05ee7dc0f2f488936dc9838bd0e230d`  
		Last Modified: Fri, 12 Mar 2021 02:25:38 GMT  
		Size: 50.4 MB (50400353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29e09ae83733d697508e34827538cc0129b8719b85db943041c5d37287bcb81`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 7.8 MB (7832474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e319e3daef68c36099bf3b534377a78d373f67bde3d156119c2463f5fe133ac5`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 10.0 MB (9997147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e499244fe254b6f980c82ea555f38e7a6527e5105545922005e88a6b81b01cac`  
		Last Modified: Fri, 12 Mar 2021 03:19:36 GMT  
		Size: 51.8 MB (51839506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec253d6133ed5960bf3c30c9d6e1e45b7fd705a5b4ec85d19aedcb00d1a0d0fa`  
		Last Modified: Sat, 13 Mar 2021 04:16:32 GMT  
		Size: 68.7 MB (68718988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07b05f2a22dca55194c797223a3b79a90f3be1243f806b7bb19c3e59247912f`  
		Last Modified: Sat, 13 Mar 2021 04:16:52 GMT  
		Size: 129.0 MB (129010367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f298da50fa054c31f3042de44a7c6a9d66e0c84b334977f2dcdef55a05aee192`  
		Last Modified: Sat, 13 Mar 2021 04:16:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; arm variant v5

```console
$ docker pull golang@sha256:1d7a938a71f426ae5486bd31ad931c6e5180d67ac6cf0e314af025483269af4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269262689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63d2104a7ec22e0d20c737c8cd7d83c5db1c108bbd61476053af5b6eed5e45c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:51:51 GMT
ADD file:691c50b877ea6a82b9d5613106b617c0d5918ce75d8ba5677fe51236375484f6 in / 
# Fri, 12 Mar 2021 01:51:56 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 04:03:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 04:03:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 04:04:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 12:32:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 12:32:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 12:32:56 GMT
ENV GOLANG_VERSION=1.16.2
# Fri, 12 Mar 2021 12:36:30 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 12 Mar 2021 12:36:35 GMT
ENV GOPATH=/go
# Fri, 12 Mar 2021 12:36:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 12:36:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 12 Mar 2021 12:36:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7eef935c67ffee30027811683de563ed45bcc70c9f0d2abfdaea90517d838208`  
		Last Modified: Fri, 12 Mar 2021 02:01:38 GMT  
		Size: 48.1 MB (48111577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fa779c2b1864e1f58436ee3b2f96f15f107c64a85cea5ef91784a64fa9cd20`  
		Last Modified: Fri, 12 Mar 2021 04:17:44 GMT  
		Size: 7.4 MB (7376656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe858453b935de87a2e8fb6f8ea6285b59d5d50c5222b8ee4a6fe0a5634ebb98`  
		Last Modified: Fri, 12 Mar 2021 04:17:44 GMT  
		Size: 9.7 MB (9687479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def552b806024ab1b88bcf047c02b52104ecd2cb2a616d4e8b3c4d5dbda2abd9`  
		Last Modified: Fri, 12 Mar 2021 04:18:18 GMT  
		Size: 49.6 MB (49572032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bc72aef151aa530a47d0f3a553ed27e0fbc425d42d4ec2b099b47a527471a4`  
		Last Modified: Fri, 12 Mar 2021 12:40:52 GMT  
		Size: 52.0 MB (52026914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961155178e25074bf0b406065bf2a327922bc9b4000cf9b40b01e2451c57628a`  
		Last Modified: Fri, 12 Mar 2021 12:41:07 GMT  
		Size: 102.5 MB (102487875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f72f37a7a2c1a828fa92c7898e4a138bed63213322d0717cfbbb8c6c492d303`  
		Last Modified: Fri, 12 Mar 2021 12:40:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:aec820a1254bea65c4a450ed3a33a7557b4a23eff8fcc11140b9bf53e42dd2fe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263154385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c526229a9d7a3f11c03fe6fe577a6b5d68420312bf51aae85bf31a8673bb44`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:59:39 GMT
ADD file:7a272c0a2bf029fde32186ff5d55a8ef335d159da9770327eedf010bd6e6c42d in / 
# Fri, 12 Mar 2021 01:59:44 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:32:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:32:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 03:33:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 21:27:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 21:27:02 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 21:27:03 GMT
ENV GOLANG_VERSION=1.16.2
# Fri, 12 Mar 2021 21:27:27 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 12 Mar 2021 21:27:32 GMT
ENV GOPATH=/go
# Fri, 12 Mar 2021 21:27:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 21:27:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 12 Mar 2021 21:27:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:199f83f6a2f5a375b8f94d3025f9bbdaca75f4ca46ad0aab2061c331588fa662`  
		Last Modified: Fri, 12 Mar 2021 02:10:00 GMT  
		Size: 45.9 MB (45868120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d535c087e97eba956c56d41b509048f3f9283744c2b2ef7fabbb6a75fe7d3c`  
		Last Modified: Fri, 12 Mar 2021 03:47:04 GMT  
		Size: 7.1 MB (7123778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cfc4c570eb98f73a8ab1d871e36ff43492038fa4c0279c70ccff1797447d2b`  
		Last Modified: Fri, 12 Mar 2021 03:47:04 GMT  
		Size: 9.3 MB (9343577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2cb364b2d38bcbf9b4e594b01bbf2a4d3509357468c391ebc39660a58df706`  
		Last Modified: Fri, 12 Mar 2021 03:47:29 GMT  
		Size: 47.4 MB (47356842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975302acd2fb1bd0e20fb9f2515189ca5236f1f3196fd01987a0678e59d60de2`  
		Last Modified: Fri, 12 Mar 2021 21:31:24 GMT  
		Size: 53.2 MB (53193016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac5ad6774229c311728aa83412ffabe9855e2a73f57a337309171638dcbb9cc`  
		Last Modified: Fri, 12 Mar 2021 21:31:42 GMT  
		Size: 100.3 MB (100268896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bf3e5167780bab74526d79e0c71105204f4adb527d3a8dab5df7c616dda728`  
		Last Modified: Fri, 12 Mar 2021 21:31:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e87ba3a72191846a32f464512073a561090d468f6d20dc68f9c4956ccf002c15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281201926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46b7c18e5b0d7c4a519c601a4de86416e44bbd4f6d64cd61b726d362340bea7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:53:16 GMT
ADD file:b2e2cca51e131b97e6a7e02af893c7f9b1f7a491b3d5fdaafa80409ed248a706 in / 
# Fri, 12 Mar 2021 01:53:20 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:29:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:29:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:30:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 19:42:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 19:42:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 19:42:40 GMT
ENV GOLANG_VERSION=1.16.2
# Fri, 12 Mar 2021 19:42:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 12 Mar 2021 19:43:01 GMT
ENV GOPATH=/go
# Fri, 12 Mar 2021 19:43:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 19:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 12 Mar 2021 19:43:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e9742a63e95a88f8685c4f23a73f7dd15e4039ac1862ce5753c53406a5f7c04a`  
		Last Modified: Fri, 12 Mar 2021 02:01:14 GMT  
		Size: 49.2 MB (49195763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90273c85fdda8648cee9282aa7b01faf0ec1f45451931985b3504c37cf1ac3e6`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 7.7 MB (7694407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685f873e984153af9a44cf556c7679b430b9c557d901c7d476725134f28754e7`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 10.0 MB (9984339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34041dfaf60ca49c213d83e89205fc2b7e222817c9728a4aa4f7d3f09d579c9`  
		Last Modified: Fri, 12 Mar 2021 02:43:54 GMT  
		Size: 52.2 MB (52165212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a0c71a3bdd5c6450fbd64071d7dc839a0bcb4b25cb4da17cee99e4003e08ba`  
		Last Modified: Fri, 12 Mar 2021 19:46:22 GMT  
		Size: 62.6 MB (62587002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a086f1a1722b807b6ba4f85da1d7425d05af6cdd2e1ea0b1fb5a26b60e49db32`  
		Last Modified: Fri, 12 Mar 2021 19:46:38 GMT  
		Size: 99.6 MB (99575048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d758bfab17e3578adf29f70b354ef2ac6daf97c874a46e1d2c5ffa47d3cc98c8`  
		Last Modified: Fri, 12 Mar 2021 19:46:08 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; 386

```console
$ docker pull golang@sha256:8a0cde434c30b3a8c1cfc615700a9a2b39ba2ca20d254e0195e074542743ad05
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.6 MB (299581424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127a1a7ff76f4b422ae75cf337570e87bf263846250ed2c699ddfb2522f84e90`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:44:10 GMT
ADD file:7fc865376477d0a3207f0488aa53a01be49cf76d0f075eb2d8dfb866f67472c2 in / 
# Fri, 12 Mar 2021 01:44:11 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:16:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:17:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 23:30:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 23:30:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 23:30:01 GMT
ENV GOLANG_VERSION=1.16.2
# Fri, 12 Mar 2021 23:30:25 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 12 Mar 2021 23:30:27 GMT
ENV GOPATH=/go
# Fri, 12 Mar 2021 23:30:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 23:30:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 12 Mar 2021 23:30:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a0450ef8e4ab4239c43726ef6f13a160860a6ab25f82c8f011ca37ee436324a2`  
		Last Modified: Fri, 12 Mar 2021 01:51:32 GMT  
		Size: 51.2 MB (51160386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f62290e3e304b8095d37508b9b2051cb2b2d26d61984ec27eb7560a808f020`  
		Last Modified: Fri, 12 Mar 2021 02:36:17 GMT  
		Size: 8.0 MB (7997281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78fb5d9226b64f0de7250162ff06d8a9871bcc020e50b44675068767d820a5f`  
		Last Modified: Fri, 12 Mar 2021 02:36:17 GMT  
		Size: 10.3 MB (10340057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6f80e285dc0ec638e021f54cc99edebfeba111ee99288f0674a32914c3c063`  
		Last Modified: Fri, 12 Mar 2021 02:36:44 GMT  
		Size: 53.4 MB (53437850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55b9c32865e9de27f672db06ef4c91b3685b5ee2613906814d653df0dd9cf0e`  
		Last Modified: Fri, 12 Mar 2021 23:35:09 GMT  
		Size: 73.6 MB (73587467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4dd4762290c0a377687a9591f288183b5f940c35811cc204a3d962c428f359`  
		Last Modified: Fri, 12 Mar 2021 23:35:12 GMT  
		Size: 103.1 MB (103058228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ec23964966fb2ba44e5bb800516c2bfc7b0db026602f3a4f9704088f398062`  
		Last Modified: Fri, 12 Mar 2021 23:34:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; mips64le

```console
$ docker pull golang@sha256:85b460eb391030f658f5c0fed5a1fc8dd5baef25c28b8dc65d5938c8c56b2a46
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.3 MB (271349025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6572433a2196e6c7cfda2699191a6a42765d8cd1a369d8b2523e919ced93b04`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:09:34 GMT
ADD file:06325f46842ab44ddc8f026cec1aa60e1d51e92c06d5d37d435670501f89ef1b in / 
# Fri, 12 Mar 2021 02:09:35 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:09:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:09:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 03:10:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 17:02:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 17:02:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 17:02:34 GMT
ENV GOLANG_VERSION=1.16.2
# Fri, 12 Mar 2021 17:10:31 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 12 Mar 2021 17:10:33 GMT
ENV GOPATH=/go
# Fri, 12 Mar 2021 17:10:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 17:10:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 12 Mar 2021 17:10:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:063dacdc6a9fbed24da8b5d2d05165ef7557b54ce19fe0b91a4862335c8b7e60`  
		Last Modified: Fri, 12 Mar 2021 02:16:24 GMT  
		Size: 49.0 MB (49029197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d5a861adfff510d33e8c071f72ea53c8aeabcb0a49b62df8bee74e957366e6`  
		Last Modified: Fri, 12 Mar 2021 03:20:32 GMT  
		Size: 7.3 MB (7250932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1212b9570329a399a09c641c48a72ac9fd4221db736f960336aa14f87e520750`  
		Last Modified: Fri, 12 Mar 2021 03:20:33 GMT  
		Size: 10.0 MB (10016364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4011f9b9f7577825f2681364dff75d914c3124696d66fe0649f3da873a2b94aa`  
		Last Modified: Fri, 12 Mar 2021 03:21:23 GMT  
		Size: 50.8 MB (50843323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2003b726e359ffd980ebc140b73e5572b05e5017538f2e462156d0f9f305ab64`  
		Last Modified: Fri, 12 Mar 2021 17:19:24 GMT  
		Size: 54.6 MB (54634716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaebe1c7a84ac3919c7be33c3cbca766e183df1594bc3ec452692ad2188b609e`  
		Last Modified: Fri, 12 Mar 2021 17:19:52 GMT  
		Size: 99.6 MB (99574368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705def3bec83e0ede7c2e381043d0a03bd60f6f9db744638242c4ff6a85e557a`  
		Last Modified: Fri, 12 Mar 2021 17:18:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; ppc64le

```console
$ docker pull golang@sha256:064377665c26ab428a83e1da3b76ed7496687e760f07d44f7d3ab60b11430dad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302267694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e45ac5680fa3310f22bfa19436d6f475c931a6c7c28221c31dfbe1852d977e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:31:55 GMT
ADD file:75cbd246f27dc871f6d43b196814d29950e19fbcf60ba31740b0f3b69d1eb5cf in / 
# Fri, 12 Mar 2021 02:32:10 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 11:02:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 11:03:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 11:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 02:26:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 02:26:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Mar 2021 02:26:45 GMT
ENV GOLANG_VERSION=1.16.2
# Sat, 13 Mar 2021 02:27:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Sat, 13 Mar 2021 02:27:42 GMT
ENV GOPATH=/go
# Sat, 13 Mar 2021 02:27:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Mar 2021 02:28:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 13 Mar 2021 02:28:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e82e55acc97d8fc958b57715031c249868ac5d8978e8d9f94ca4c15d553fe3cf`  
		Last Modified: Fri, 12 Mar 2021 02:44:17 GMT  
		Size: 54.1 MB (54136226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d7821ad6b4fb4c264f87306146cca85ae319c012535ca5ba869f297681f528`  
		Last Modified: Fri, 12 Mar 2021 12:00:12 GMT  
		Size: 8.3 MB (8271375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efadb27dbbd9968d195399537fc5c6be6627d842ed384ff4e9510632b9f24720`  
		Last Modified: Fri, 12 Mar 2021 12:00:09 GMT  
		Size: 10.7 MB (10727647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65fb57ad94f43eee037ef854e05c8d78064d228650a412c8cbf509359c99228`  
		Last Modified: Fri, 12 Mar 2021 12:02:19 GMT  
		Size: 57.5 MB (57456654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac5ab22b7e95f441d3508b3a27b8c2d834b3d529f3a85d9a0779557430be580`  
		Last Modified: Sat, 13 Mar 2021 02:32:05 GMT  
		Size: 73.6 MB (73624203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eab641465e4965fd5e63f8e9fc1a35cf27211c566c870bed8503bc0532cb708`  
		Last Modified: Sat, 13 Mar 2021 02:32:10 GMT  
		Size: 98.1 MB (98051433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36dbde775eecd3117b139dbcc663c1cee4c51c9e3f13a05b9a72ced725ee3cd9`  
		Last Modified: Sat, 13 Mar 2021 02:31:51 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; s390x

```console
$ docker pull golang@sha256:1e879437e58e9c909c91c7d0566b452451c5c60dbfb3e4462c3d76a41c29b175
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277602864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff2df2a40299cfdc1ff8d9abcf09dda7e7ae786088b887aa29b703369384e2c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:45:42 GMT
ADD file:c1bc4d97e132d650b9f7848521ea163735e8d93b365da94640ff25e0e01bc891 in / 
# Fri, 12 Mar 2021 01:45:47 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:31:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:31:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:32:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 08:46:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 08:46:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 08:46:57 GMT
ENV GOLANG_VERSION=1.16.2
# Fri, 12 Mar 2021 08:47:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 12 Mar 2021 08:47:24 GMT
ENV GOPATH=/go
# Fri, 12 Mar 2021 08:47:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 08:47:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 12 Mar 2021 08:47:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2fc1f9e428b932a8750b1c7f11f48b4c9a41328e9107b957451d8b8efbfd3fce`  
		Last Modified: Fri, 12 Mar 2021 01:50:13 GMT  
		Size: 49.0 MB (48969030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befe52bd5ee0309720b929d18591173abb18f1edb53333e9dd9bd9f183ccfb43`  
		Last Modified: Fri, 12 Mar 2021 02:39:33 GMT  
		Size: 7.4 MB (7399848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c50286b18ab639a9609fab3ff02da0b0c7f4463147aa750868999fd2cb3c670`  
		Last Modified: Fri, 12 Mar 2021 02:39:33 GMT  
		Size: 9.9 MB (9883075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957e17b0db43215705ba4f0a95f8a4a58939895c2b6675d2c09f3243643ef861`  
		Last Modified: Fri, 12 Mar 2021 02:39:48 GMT  
		Size: 51.4 MB (51380029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7a9047f4b8dd1f189f00fe8b4a3bb01c871f20592327add3cd1c9644b8b7917`  
		Last Modified: Fri, 12 Mar 2021 08:49:08 GMT  
		Size: 56.8 MB (56788510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a18f04c9ee3a8b588040fb08096e322b8b969d1e21aa08d7acc6ac4b4bc19d`  
		Last Modified: Fri, 12 Mar 2021 08:49:14 GMT  
		Size: 103.2 MB (103182216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84446f38fcbeadc4d858e4dfd161e1767e6cfccbd215513ba2fa8f2352cbcaa2`  
		Last Modified: Fri, 12 Mar 2021 08:49:00 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

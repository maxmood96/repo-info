## `golang:latest`

```console
$ docker pull golang@sha256:7ffa70183b7596e6bc1b78c132dbba9a6e05a26cd30eaa9832fecad64b83f029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 10
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `golang:latest` - linux; amd64

```console
$ docker pull golang@sha256:24e286ca5b48c690f29266a7086e1b7f77a4ddc1a47f6f8bf55d4b736eee073e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.6 MB (360551305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d4f5578ce3878c9d365e9cf30a97ebf77960c0dcdb52da6e8fe2808a4b64e7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:23:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:23:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 00:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 00:48:52 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 19:19:39 GMT
ENV GOLANG_VERSION=1.19.3
# Tue, 01 Nov 2022 19:19:53 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.3.linux-amd64.tar.gz'; 			sha256='74b9640724fd4e6bb0ed2a1bc44ae813a03f1e72a4c76253e2d5c015494430ba'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.3.linux-armv6l.tar.gz'; 			sha256='d2f8028ff3e84b93265084394e4b8316138e8967864267392d7fa2d3e4623f82'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.3.linux-arm64.tar.gz'; 			sha256='99de2fe112a52ab748fb175edea64b313a0c8d51d6157dba683a6be163fd5eab'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.3.linux-386.tar.gz'; 			sha256='4f055d40cbd3047b90f5b6c2d30a7fc6732aa1475f372f37ac574f725340aab3'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.3.linux-ppc64le.tar.gz'; 			sha256='741dad06e7b17fe2c9cd9586b4048cec087ca1f7a317389b14e89b26c25d3542'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.3.linux-s390x.tar.gz'; 			sha256='94a0d736a5cded92792d9aae6762c47fe8bcf54fd96c4d20fd883221db872957'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.3.src.tar.gz'; 		sha256='18ac263e39210bcf68d85f4370e97fb1734166995a1f63fb38b4f6e07d90d212'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 01 Nov 2022 19:19:54 GMT
ENV GOPATH=/go
# Tue, 01 Nov 2022 19:19:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 19:19:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Nov 2022 19:19:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4a4c6caea8801bb0b7377e10220a914da403bc93fa79663cbf2dcf1800b6f1`  
		Last Modified: Tue, 25 Oct 2022 09:47:36 GMT  
		Size: 5.2 MB (5164775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edced8587e6c18412817019074f5e04a8ede4e2fc89d06af13df3f80d78a70d`  
		Last Modified: Tue, 25 Oct 2022 09:47:36 GMT  
		Size: 10.9 MB (10877322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7969cffbf46e6a91291fd76b19ecbe93c03ea4ded0d14042aecb4c0c4211a43`  
		Last Modified: Tue, 25 Oct 2022 09:47:56 GMT  
		Size: 54.6 MB (54586464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa7548a174d51c2cadd24f9e629f436fbf1f501daba3e757d78c32f31c7fe83`  
		Last Modified: Wed, 26 Oct 2022 00:51:23 GMT  
		Size: 86.0 MB (85968442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f01728a4e155a49cc26989c315d6e9168832adbab874a83d3527b7127316f0`  
		Last Modified: Tue, 01 Nov 2022 19:29:11 GMT  
		Size: 148.9 MB (148907815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7094519954655e5688d14bd7d0645392f5fe39090f01db37931752e8bf5fa6b`  
		Last Modified: Tue, 01 Nov 2022 19:28:50 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; arm variant v5

```console
$ docker pull golang@sha256:4141084f9c8584d798a619430fe6232485d4252d5f315655e3344ec315d5123f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308613331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4677d344a3798f245cba2c9da72f04ed5957b9b27da3fac42ebabc23be6f02`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:06:19 GMT
ADD file:b314b98654e8532fd10a08a172ea5c3edb7d7a36c7faf85d06d14be12f7b83ef in / 
# Tue, 25 Oct 2022 03:06:19 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:12:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:12:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 06:12:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:57:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:57:03 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:48:23 GMT
ENV GOLANG_VERSION=1.19.3
# Tue, 01 Nov 2022 18:50:44 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.3.linux-amd64.tar.gz'; 			sha256='74b9640724fd4e6bb0ed2a1bc44ae813a03f1e72a4c76253e2d5c015494430ba'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.3.linux-armv6l.tar.gz'; 			sha256='d2f8028ff3e84b93265084394e4b8316138e8967864267392d7fa2d3e4623f82'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.3.linux-arm64.tar.gz'; 			sha256='99de2fe112a52ab748fb175edea64b313a0c8d51d6157dba683a6be163fd5eab'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.3.linux-386.tar.gz'; 			sha256='4f055d40cbd3047b90f5b6c2d30a7fc6732aa1475f372f37ac574f725340aab3'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.3.linux-ppc64le.tar.gz'; 			sha256='741dad06e7b17fe2c9cd9586b4048cec087ca1f7a317389b14e89b26c25d3542'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.3.linux-s390x.tar.gz'; 			sha256='94a0d736a5cded92792d9aae6762c47fe8bcf54fd96c4d20fd883221db872957'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.3.src.tar.gz'; 		sha256='18ac263e39210bcf68d85f4370e97fb1734166995a1f63fb38b4f6e07d90d212'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 01 Nov 2022 18:50:45 GMT
ENV GOPATH=/go
# Tue, 01 Nov 2022 18:50:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:50:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Nov 2022 18:50:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f0ecb08923b99bef3f82c2e88603bb53e3ed084c13252275c05039cc279c158`  
		Last Modified: Tue, 25 Oct 2022 03:11:15 GMT  
		Size: 52.5 MB (52547473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b399c5eb53b4c35fa33682a82d73bdc4b096cd78ae95fe36c4ed81d18f6849`  
		Last Modified: Tue, 25 Oct 2022 06:19:02 GMT  
		Size: 5.1 MB (5072235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ccdd06393cd3873a3cc8b9cbe170a2032fd61d1d545b7045b649faf2f4e732`  
		Last Modified: Tue, 25 Oct 2022 06:19:02 GMT  
		Size: 10.6 MB (10574279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aafe0e287af4e488dcda51195e4eb1ae1386e3265989c457172f32f6357bf26`  
		Last Modified: Tue, 25 Oct 2022 06:19:28 GMT  
		Size: 52.3 MB (52322157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd12d31bb97d2b018145d62602ea169f8eb5890a0c9990ed30115297d7b0331`  
		Last Modified: Tue, 25 Oct 2022 15:02:28 GMT  
		Size: 68.9 MB (68865696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c46502d55f0159ea52e38f75273e8f8d7456cbdad8b6ac80e3b35c3b3df0ede`  
		Last Modified: Tue, 01 Nov 2022 18:54:39 GMT  
		Size: 119.2 MB (119231364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae5d43da8b8dbbbcac03d8210e301118dfb0f892be471d839c4dbd7e963e64d`  
		Last Modified: Tue, 01 Nov 2022 18:54:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; arm variant v7

```console
$ docker pull golang@sha256:923e11809abbabf6610a7a6c8691317e3d4939adc7e7fdfa44b9b40e697ab957
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297324916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2748709861aee4be407a1fef5ca5d8261e5c3eb1423e61d771ab668a8a0580d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:06 GMT
ADD file:94d6b607b174c11c18753fac156b0ca5ecda941da3d456e136b8b14457810d37 in / 
# Tue, 25 Oct 2022 03:14:06 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 04:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 04:36:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Oct 2022 04:36:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 Oct 2022 03:10:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 Oct 2022 03:10:03 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:57:40 GMT
ENV GOLANG_VERSION=1.19.3
# Tue, 01 Nov 2022 18:57:55 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.3.linux-amd64.tar.gz'; 			sha256='74b9640724fd4e6bb0ed2a1bc44ae813a03f1e72a4c76253e2d5c015494430ba'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.3.linux-armv6l.tar.gz'; 			sha256='d2f8028ff3e84b93265084394e4b8316138e8967864267392d7fa2d3e4623f82'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.3.linux-arm64.tar.gz'; 			sha256='99de2fe112a52ab748fb175edea64b313a0c8d51d6157dba683a6be163fd5eab'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.3.linux-386.tar.gz'; 			sha256='4f055d40cbd3047b90f5b6c2d30a7fc6732aa1475f372f37ac574f725340aab3'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.3.linux-ppc64le.tar.gz'; 			sha256='741dad06e7b17fe2c9cd9586b4048cec087ca1f7a317389b14e89b26c25d3542'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.3.linux-s390x.tar.gz'; 			sha256='94a0d736a5cded92792d9aae6762c47fe8bcf54fd96c4d20fd883221db872957'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.3.src.tar.gz'; 		sha256='18ac263e39210bcf68d85f4370e97fb1734166995a1f63fb38b4f6e07d90d212'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 01 Nov 2022 18:57:56 GMT
ENV GOPATH=/go
# Tue, 01 Nov 2022 18:57:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:57:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Nov 2022 18:57:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a9bec1cbb822a75428a679c01f232b1af10cce0bdc1bf6507d26e8d79ad54300`  
		Last Modified: Tue, 25 Oct 2022 03:20:41 GMT  
		Size: 50.2 MB (50209987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9e47cd2446328779ff30de254793eaf539fec260638990e7d8dd3d29342fca`  
		Last Modified: Wed, 26 Oct 2022 05:10:38 GMT  
		Size: 4.9 MB (4932764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8deb44fa055f393de7346c484ab2ff3ef90e7efc4ebb018f932b377361e3b45`  
		Last Modified: Wed, 26 Oct 2022 05:10:38 GMT  
		Size: 10.2 MB (10218474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22aca21bac1ccd293dcbdab0f501e5f245365480a29e4d11572ddc5092e2287`  
		Last Modified: Wed, 26 Oct 2022 05:11:04 GMT  
		Size: 50.3 MB (50345195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f5be6f3d2ed5848e4dcc85b6d7f27282473847177c2271047663070fe09a36`  
		Last Modified: Thu, 27 Oct 2022 03:22:18 GMT  
		Size: 64.9 MB (64890965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f14319c54c5e327684ceec0a23098bf07ace2710faa0e55c58f4a3f0e36bbc6`  
		Last Modified: Tue, 01 Nov 2022 19:09:43 GMT  
		Size: 116.7 MB (116727405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6096ef5cd63b6552ba0132110d5fa461a9307b5731088cb898632030a8ad1c1`  
		Last Modified: Tue, 01 Nov 2022 19:09:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d0e625b278a6bd69879384eff03bccf8b5b877adcd4f8c983747fbdcab5a3211
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320914934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f48645b0176afbe1fc0a09d1c82272ee9d1cf53915b33a438fc4179ebeb36b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:55 GMT
ADD file:b16745ece8ef84c028d7e9ac4bf026ac64f885d4170bfcc9d435f237144a1b99 in / 
# Tue, 25 Oct 2022 05:45:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:58:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 07:59:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 08:09:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 08:09:13 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:39:44 GMT
ENV GOLANG_VERSION=1.19.3
# Tue, 01 Nov 2022 18:39:54 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.3.linux-amd64.tar.gz'; 			sha256='74b9640724fd4e6bb0ed2a1bc44ae813a03f1e72a4c76253e2d5c015494430ba'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.3.linux-armv6l.tar.gz'; 			sha256='d2f8028ff3e84b93265084394e4b8316138e8967864267392d7fa2d3e4623f82'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.3.linux-arm64.tar.gz'; 			sha256='99de2fe112a52ab748fb175edea64b313a0c8d51d6157dba683a6be163fd5eab'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.3.linux-386.tar.gz'; 			sha256='4f055d40cbd3047b90f5b6c2d30a7fc6732aa1475f372f37ac574f725340aab3'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.3.linux-ppc64le.tar.gz'; 			sha256='741dad06e7b17fe2c9cd9586b4048cec087ca1f7a317389b14e89b26c25d3542'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.3.linux-s390x.tar.gz'; 			sha256='94a0d736a5cded92792d9aae6762c47fe8bcf54fd96c4d20fd883221db872957'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.3.src.tar.gz'; 		sha256='18ac263e39210bcf68d85f4370e97fb1734166995a1f63fb38b4f6e07d90d212'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 01 Nov 2022 18:39:57 GMT
ENV GOPATH=/go
# Tue, 01 Nov 2022 18:39:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:39:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Nov 2022 18:39:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8e1d92e7d04d2a9a9880cb45dc3c32c2805912cd86abed96d0ada3ff28748205`  
		Last Modified: Tue, 25 Oct 2022 05:48:40 GMT  
		Size: 53.7 MB (53701966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66eadbf427bb41b3e329a95935c65b09c6d3b7a9c2fa8e08417e497df02ed996`  
		Last Modified: Tue, 25 Oct 2022 08:30:22 GMT  
		Size: 5.2 MB (5151506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9731f4e3bc3680179c10cece663cf0cfe0488918d6795406f4b76f07b787de`  
		Last Modified: Tue, 25 Oct 2022 08:30:22 GMT  
		Size: 10.9 MB (10874174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d337cb12fd7c6fe341850cd38e880f1806d49a65832c9804b06d00f9032382e0`  
		Last Modified: Tue, 25 Oct 2022 08:30:42 GMT  
		Size: 54.7 MB (54683990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70e778606f888a21badcd0a0dae68201b78b263e5bbc2532ee92e286646f7de`  
		Last Modified: Wed, 26 Oct 2022 08:16:29 GMT  
		Size: 81.4 MB (81371367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6698acbeca77f7142d9c60fbcf03cfd24ae5f19064a91cb73d0a115a4c6f1543`  
		Last Modified: Tue, 01 Nov 2022 18:47:11 GMT  
		Size: 115.1 MB (115131775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3866aabe327615f8b353df0e7bb850ee5d5794ac1dd6e4f5334cdd748fd82fa1`  
		Last Modified: Tue, 01 Nov 2022 18:46:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; 386

```console
$ docker pull golang@sha256:6bec140ccbf8ff44e0c4134343d17dd36f034cc64b32fd23bbe0e9cd040a5c5e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.3 MB (335269157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2792474407b45cbb8ad9b9c66ded048b11fb41635b073ab72003e6f8eab910e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 02:22:19 GMT
ADD file:aa26f69b37c3e144d08e17bb9be7302ec89ae0579121c874a35f336d7077fd3b in / 
# Tue, 25 Oct 2022 02:22:19 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 05:15:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 05:15:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 05:15:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:22:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:22:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:38:39 GMT
ENV GOLANG_VERSION=1.19.3
# Tue, 01 Nov 2022 18:38:53 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.3.linux-amd64.tar.gz'; 			sha256='74b9640724fd4e6bb0ed2a1bc44ae813a03f1e72a4c76253e2d5c015494430ba'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.3.linux-armv6l.tar.gz'; 			sha256='d2f8028ff3e84b93265084394e4b8316138e8967864267392d7fa2d3e4623f82'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.3.linux-arm64.tar.gz'; 			sha256='99de2fe112a52ab748fb175edea64b313a0c8d51d6157dba683a6be163fd5eab'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.3.linux-386.tar.gz'; 			sha256='4f055d40cbd3047b90f5b6c2d30a7fc6732aa1475f372f37ac574f725340aab3'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.3.linux-ppc64le.tar.gz'; 			sha256='741dad06e7b17fe2c9cd9586b4048cec087ca1f7a317389b14e89b26c25d3542'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.3.linux-s390x.tar.gz'; 			sha256='94a0d736a5cded92792d9aae6762c47fe8bcf54fd96c4d20fd883221db872957'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.3.src.tar.gz'; 		sha256='18ac263e39210bcf68d85f4370e97fb1734166995a1f63fb38b4f6e07d90d212'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 01 Nov 2022 18:38:54 GMT
ENV GOPATH=/go
# Tue, 01 Nov 2022 18:38:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:38:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Nov 2022 18:38:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8caf426a2703f99fb0be4b03411ecaa580d102f7c47ef43b422b6d7c13c380e2`  
		Last Modified: Tue, 25 Oct 2022 02:27:54 GMT  
		Size: 56.0 MB (56023960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b92a2ff5c72653a0679aa7f5e2bc695011c0a71faa424229e560957d204dab`  
		Last Modified: Tue, 25 Oct 2022 05:27:37 GMT  
		Size: 5.1 MB (5086887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6856a3002e686ceb6d48d078731366f576ed3adcb73bd49dcb300057732904`  
		Last Modified: Tue, 25 Oct 2022 05:27:38 GMT  
		Size: 11.0 MB (11032526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e88080d3b5ba1edc8623a97d068bd040dfb89f2bc7bdfc0984d11fc35ff5885`  
		Last Modified: Tue, 25 Oct 2022 05:28:00 GMT  
		Size: 55.9 MB (55924404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257d1a174521bbc2317acbc6ba9f9a91cb963244f0794bd1196e33e7ce794e4b`  
		Last Modified: Tue, 25 Oct 2022 18:26:25 GMT  
		Size: 87.2 MB (87163943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccf9ba421fd86e046ddceb2478f647fffaf50312944fc0e391743fa84472f49`  
		Last Modified: Tue, 01 Nov 2022 18:49:59 GMT  
		Size: 120.0 MB (120037312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb6ded94e951e325be30d81c6094fc5558d9208801e97e544f6b398abc629d8`  
		Last Modified: Tue, 01 Nov 2022 18:49:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; mips64le

```console
$ docker pull golang@sha256:1d88dc3a950292801b501d53ae1e8c2b2ffaf62b0a40dce281266870f56f03b4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (304023887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70763827df871a90ccbe3a3b73b22fa965a54eafbcdd8c09813f257222d2703`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 04:38:51 GMT
ADD file:617ca04150550c7e3a178e3ac85bb359b17a390090ce6ce72a6f2ed1db10ab63 in / 
# Tue, 25 Oct 2022 04:38:57 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:30:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:31:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 09:33:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 11:51:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 11:51:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 19:18:56 GMT
ENV GOLANG_VERSION=1.19.3
# Tue, 01 Nov 2022 19:31:15 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.3.linux-amd64.tar.gz'; 			sha256='74b9640724fd4e6bb0ed2a1bc44ae813a03f1e72a4c76253e2d5c015494430ba'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.3.linux-armv6l.tar.gz'; 			sha256='d2f8028ff3e84b93265084394e4b8316138e8967864267392d7fa2d3e4623f82'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.3.linux-arm64.tar.gz'; 			sha256='99de2fe112a52ab748fb175edea64b313a0c8d51d6157dba683a6be163fd5eab'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.3.linux-386.tar.gz'; 			sha256='4f055d40cbd3047b90f5b6c2d30a7fc6732aa1475f372f37ac574f725340aab3'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.3.linux-ppc64le.tar.gz'; 			sha256='741dad06e7b17fe2c9cd9586b4048cec087ca1f7a317389b14e89b26c25d3542'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.3.linux-s390x.tar.gz'; 			sha256='94a0d736a5cded92792d9aae6762c47fe8bcf54fd96c4d20fd883221db872957'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.3.src.tar.gz'; 		sha256='18ac263e39210bcf68d85f4370e97fb1734166995a1f63fb38b4f6e07d90d212'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 01 Nov 2022 19:31:23 GMT
ENV GOPATH=/go
# Tue, 01 Nov 2022 19:31:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 19:31:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Nov 2022 19:31:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e3c84cb4c321de8db072180e3509c5bbcf8e562ff11c03241bdf082184fe74d6`  
		Last Modified: Tue, 25 Oct 2022 04:46:42 GMT  
		Size: 53.3 MB (53265848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3db3e162cf97fdacf5ea7f9f3912781648668e28872229f94c59a0ede7eb374`  
		Last Modified: Tue, 25 Oct 2022 09:51:57 GMT  
		Size: 4.9 MB (4919493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb2f56957fe9f71a2e7c596a334686320ab2569f1a54e243bfcd3f42ebae17c`  
		Last Modified: Tue, 25 Oct 2022 09:51:59 GMT  
		Size: 10.7 MB (10661828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a581172d92713c67937b8552f2518b0661de8146176b186886f6dd01ea188`  
		Last Modified: Tue, 25 Oct 2022 09:52:48 GMT  
		Size: 53.3 MB (53306457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a848178ef525ebc98a0f61d2a5d95eecef3bd73db09468b43f281432335a45bc`  
		Last Modified: Wed, 26 Oct 2022 12:17:52 GMT  
		Size: 66.8 MB (66838109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cda3c2268651402b934254cac124a5fac60e0b32368a147a983ef102dad117`  
		Last Modified: Tue, 01 Nov 2022 19:45:53 GMT  
		Size: 115.0 MB (115032027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30e41bf9347f4238af1e6036bec7825c5339c5604e3eb9ac8fa80a325fdf317`  
		Last Modified: Tue, 01 Nov 2022 19:44:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:01b13cde94c411113c82e221f2748eb46e45e8c42551dc8dbdfdb2678092b184
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f3ea871260fb465423d5140907b75441f8a33a580dd6d8237566dae86aeea21`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:13:28 GMT
ADD file:c01a6cc4222fbeeda5c2d679c5b355539880a02c792c64861eb17b81a3678f45 in / 
# Tue, 25 Oct 2022 03:13:31 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:14:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 06:14:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:01:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:02:01 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 19:16:33 GMT
ENV GOLANG_VERSION=1.19.3
# Tue, 01 Nov 2022 19:16:57 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.3.linux-amd64.tar.gz'; 			sha256='74b9640724fd4e6bb0ed2a1bc44ae813a03f1e72a4c76253e2d5c015494430ba'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.3.linux-armv6l.tar.gz'; 			sha256='d2f8028ff3e84b93265084394e4b8316138e8967864267392d7fa2d3e4623f82'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.3.linux-arm64.tar.gz'; 			sha256='99de2fe112a52ab748fb175edea64b313a0c8d51d6157dba683a6be163fd5eab'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.3.linux-386.tar.gz'; 			sha256='4f055d40cbd3047b90f5b6c2d30a7fc6732aa1475f372f37ac574f725340aab3'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.3.linux-ppc64le.tar.gz'; 			sha256='741dad06e7b17fe2c9cd9586b4048cec087ca1f7a317389b14e89b26c25d3542'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.3.linux-s390x.tar.gz'; 			sha256='94a0d736a5cded92792d9aae6762c47fe8bcf54fd96c4d20fd883221db872957'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.3.src.tar.gz'; 		sha256='18ac263e39210bcf68d85f4370e97fb1734166995a1f63fb38b4f6e07d90d212'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 01 Nov 2022 19:17:02 GMT
ENV GOPATH=/go
# Tue, 01 Nov 2022 19:17:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 19:17:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Nov 2022 19:17:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ee5a342763ed1d31bef8cebe9f4cc5dd6d427f630da679a87da0427be7b22e3d`  
		Last Modified: Tue, 25 Oct 2022 03:18:52 GMT  
		Size: 58.9 MB (58916374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a4727f39cbcb19b39abdbd847eeceed842ef65f8514372024c48b913bc951a`  
		Last Modified: Tue, 25 Oct 2022 06:49:00 GMT  
		Size: 5.4 MB (5414507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe601e6c8a1ec9c69c49c65a53339202a65cea9d4f01d161fb34905c06a4a99`  
		Last Modified: Tue, 25 Oct 2022 06:49:01 GMT  
		Size: 11.6 MB (11630153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5055e27b58426c2b637b1c8c179e6abe306e3dfb55a9c170c73fb0d581c6cf3e`  
		Last Modified: Tue, 25 Oct 2022 06:49:31 GMT  
		Size: 58.9 MB (58867355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf936729b2411f0eda4222e8d64bfbdb2bbab95aa679a5b404a8def8f316c53`  
		Last Modified: Tue, 25 Oct 2022 18:05:05 GMT  
		Size: 80.4 MB (80419664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47df0270b44ecb5be4fc93007ba09d7e9fdd61a4fe661c8b98e057c618f9d5e7`  
		Last Modified: Tue, 01 Nov 2022 19:31:09 GMT  
		Size: 115.6 MB (115550757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77dd5df18eecaf1436fbf3335fb717473054f56caff5e2b0111c58b5926118e2`  
		Last Modified: Tue, 01 Nov 2022 19:30:42 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; s390x

```console
$ docker pull golang@sha256:f120e62975eb3fc7769d3b32adffccb29212f50bc451dd5c24f38477d418b64a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.9 MB (307947878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db301b1039f0fa72212b7fb71508bd4000deb7315d6712184b4d60707e5a500`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:14:24 GMT
ADD file:06f15d8a3c04752d271a052e820fb13fcdb76f0d18f6c9afb6e70391d10348ec in / 
# Tue, 25 Oct 2022 01:14:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:31:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:31:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 02:31:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 13:32:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 13:32:50 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:41:48 GMT
ENV GOLANG_VERSION=1.19.3
# Tue, 01 Nov 2022 18:42:36 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.3.linux-amd64.tar.gz'; 			sha256='74b9640724fd4e6bb0ed2a1bc44ae813a03f1e72a4c76253e2d5c015494430ba'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.3.linux-armv6l.tar.gz'; 			sha256='d2f8028ff3e84b93265084394e4b8316138e8967864267392d7fa2d3e4623f82'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.3.linux-arm64.tar.gz'; 			sha256='99de2fe112a52ab748fb175edea64b313a0c8d51d6157dba683a6be163fd5eab'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.3.linux-386.tar.gz'; 			sha256='4f055d40cbd3047b90f5b6c2d30a7fc6732aa1475f372f37ac574f725340aab3'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.3.linux-ppc64le.tar.gz'; 			sha256='741dad06e7b17fe2c9cd9586b4048cec087ca1f7a317389b14e89b26c25d3542'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.3.linux-s390x.tar.gz'; 			sha256='94a0d736a5cded92792d9aae6762c47fe8bcf54fd96c4d20fd883221db872957'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.3.src.tar.gz'; 		sha256='18ac263e39210bcf68d85f4370e97fb1734166995a1f63fb38b4f6e07d90d212'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 01 Nov 2022 18:42:56 GMT
ENV GOPATH=/go
# Tue, 01 Nov 2022 18:42:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:42:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Nov 2022 18:42:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a556186e8bea4ba9925d0c17bea2c12bfbb931653cfab1b980036800482cf0ad`  
		Last Modified: Tue, 25 Oct 2022 01:18:39 GMT  
		Size: 53.3 MB (53279106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1e8478a953d3a464d73e36e4032c979725bc79ce0eeb83aca30212de549b90`  
		Last Modified: Tue, 25 Oct 2022 02:49:32 GMT  
		Size: 5.1 MB (5148477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cdbee45ed722bfaf7e9ba90503afa7a0cf17b87fc1bfa1e87cbf49ca6bd7d9`  
		Last Modified: Tue, 25 Oct 2022 02:49:33 GMT  
		Size: 10.8 MB (10766704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76aacd12f54fec6c8f627f09641ea144eb6fefeebc8f9fc35de80c3e3ab11af7`  
		Last Modified: Tue, 25 Oct 2022 02:49:48 GMT  
		Size: 54.1 MB (54055853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68c70a67df68f7eae963aff382c1a55a1a2aad6ef574ed61c74ee941dcacf29`  
		Last Modified: Tue, 25 Oct 2022 13:35:18 GMT  
		Size: 65.7 MB (65667297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdfa204dfe1a012e2a48c39129a0717aa462c7f46d40e3eab9051d9445b34c3`  
		Last Modified: Tue, 01 Nov 2022 19:02:08 GMT  
		Size: 119.0 MB (119030285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af0d9d82e41d7d0df726cf6d9d696d9aafe6164ddf976b9942fc25a15ffe705`  
		Last Modified: Tue, 01 Nov 2022 19:01:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.20348.1129; amd64

```console
$ docker pull golang@sha256:2137e61bce6ec1d0d7141d0d809e825e99cf78ef26cdf2a8b597d56ccc5f1d57
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2658092440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e2dc34a0dd334e1fcd73e431123e2c70b91fca6a53d9ab859567da420cfc64`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 12:40:52 GMT
ENV GIT_VERSION=2.23.0
# Wed, 12 Oct 2022 12:40:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 12 Oct 2022 12:40:54 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 12 Oct 2022 12:40:55 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 12 Oct 2022 12:41:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 12 Oct 2022 12:41:26 GMT
ENV GOPATH=C:\go
# Wed, 12 Oct 2022 12:41:47 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 01 Nov 2022 19:15:18 GMT
ENV GOLANG_VERSION=1.19.3
# Tue, 01 Nov 2022 19:19:35 GMT
RUN $url = 'https://dl.google.com/go/go1.19.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'b51549a9f21ee053f8a3d8e38e45b1b8b282d976f3b60f1f89b37ac54e272d31'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 01 Nov 2022 19:19:38 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e9b54b31e104f64c9eb8a65ac0af5effd645bd00a77ea297b6015d28022a74`  
		Last Modified: Mon, 17 Oct 2022 21:39:11 GMT  
		Size: 1000.0 MB (1000028645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f8b589252b90e37349f39b9d4495646791b4050d7cd218336fcc4624b0ebe2`  
		Last Modified: Wed, 12 Oct 2022 13:15:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811ef63d5261b55ee6b499dbc7fcd1ed13386326466fb81a0801abbcbcb75d3f`  
		Last Modified: Wed, 12 Oct 2022 13:15:28 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816740cd643a7a4e72aa527cd033d0c95686c9725ff70dac3260b44dce508e73`  
		Last Modified: Wed, 12 Oct 2022 13:15:28 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599e30c8b316e75d786cfd91f97b9fae4c89fb00f3fce0619eb4e66bc3165521`  
		Last Modified: Wed, 12 Oct 2022 13:15:24 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77a0d37b81c920d4b783c0b2cfad656a4b8733960ba3afd4e0a1f39f202f948`  
		Last Modified: Wed, 12 Oct 2022 13:15:32 GMT  
		Size: 25.7 MB (25689345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b699f53b56e90279b0bb8ce4434f9b68bbc28fa30756476e22c7ef3dc869e24a`  
		Last Modified: Wed, 12 Oct 2022 13:15:21 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fcf632f60c89dd981a8a7fa084e738f55129b1786fd9a9e9f5ab8aa1e02d82`  
		Last Modified: Wed, 12 Oct 2022 13:15:24 GMT  
		Size: 526.5 KB (526519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8b0d888223c93af8f0c84ad35156f79df9b0d9ae107f61ded320d2a4fed5f3`  
		Last Modified: Tue, 01 Nov 2022 19:53:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49602de12fff655f45d03b1befdd7e56321771c65ed690492e4092da51046bb3`  
		Last Modified: Tue, 01 Nov 2022 19:54:22 GMT  
		Size: 157.8 MB (157838831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cb5ede4eaf1f86f7c0957639a8b53a0c6740df6fa395d3d286e32bff6b9195`  
		Last Modified: Tue, 01 Nov 2022 19:53:29 GMT  
		Size: 1.6 KB (1584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.17763.3532; amd64

```console
$ docker pull golang@sha256:e89a986d587c52f599d44074fbc47cb02983dbe1b6cc09b240fc58013ce54e1e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2956941465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb022e9ede6e94ca96461fb70e29ae76cd188420deb61a91917084d5a117eb29`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 12:45:06 GMT
ENV GIT_VERSION=2.23.0
# Wed, 12 Oct 2022 12:45:07 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 12 Oct 2022 12:45:08 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 12 Oct 2022 12:45:09 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 12 Oct 2022 12:46:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 12 Oct 2022 12:46:38 GMT
ENV GOPATH=C:\go
# Wed, 12 Oct 2022 12:47:37 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 01 Nov 2022 19:19:52 GMT
ENV GOLANG_VERSION=1.19.3
# Tue, 01 Nov 2022 19:25:48 GMT
RUN $url = 'https://dl.google.com/go/go1.19.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'b51549a9f21ee053f8a3d8e38e45b1b8b282d976f3b60f1f89b37ac54e272d31'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 01 Nov 2022 19:25:50 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6193ab94a0498ba6454e2a35e189837b37a2eb01403e8b62654bdc28a4569c`  
		Last Modified: Mon, 17 Oct 2022 21:52:22 GMT  
		Size: 849.2 MB (849228999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094a4c27e78f8821517fd551cd9e3d5f4b1e4199bdcd783b3fbda849e4995ad1`  
		Last Modified: Wed, 12 Oct 2022 13:16:26 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e91de5ff2103556b1048388473379f95d41247701f0911ebc7c530a861f3f5e`  
		Last Modified: Wed, 12 Oct 2022 13:16:22 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52642f9e5e3a52bef8ee5677bcb62a364e07003da51f16eb28b8a4ce34fe9f7d`  
		Last Modified: Wed, 12 Oct 2022 13:16:22 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26528ba698d400f5680be93457d24581b9e4e7a2399de7bb23cbd549f206613`  
		Last Modified: Wed, 12 Oct 2022 13:16:22 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c89703eb31300a2a39c85ce287a6b9fe88da033828368275bdbb53c2f7704c`  
		Last Modified: Wed, 12 Oct 2022 13:16:30 GMT  
		Size: 25.4 MB (25439927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8705eaae12fa4840be2d79e376eb1b4b7b18da881acad2892b1c47336e796f46`  
		Last Modified: Wed, 12 Oct 2022 13:16:19 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebda8897c2727e3b971c947385632df6f19de06da75e9f161200d43d1acf714`  
		Last Modified: Wed, 12 Oct 2022 13:16:19 GMT  
		Size: 315.0 KB (315035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8667d37dce62bb077cd534d490f047b61dfe9c30023659258862cada9cbd0ba`  
		Last Modified: Tue, 01 Nov 2022 19:54:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac8e32e89f1739964a644b8b8b5b44bbae9752f8ea1f87e93455ca36cc86a7d`  
		Last Modified: Tue, 01 Nov 2022 19:55:33 GMT  
		Size: 157.7 MB (157676844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cabbd4ff51bc72ab20efd9f4eb4ebb788679ef03c2fc9b8a72f711fe3558590`  
		Last Modified: Tue, 01 Nov 2022 19:54:40 GMT  
		Size: 1.5 KB (1459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

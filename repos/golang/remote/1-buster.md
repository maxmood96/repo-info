## `golang:1-buster`

```console
$ docker pull golang@sha256:ff227d2437e8d4575847d88871d09ff0394a0055773d0a68a48610379187c553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `golang:1-buster` - linux; amd64

```console
$ docker pull golang@sha256:56bdfc6376c062afb957353edf8b0637f5185732a8a125dafb6fa0c3b29b3537
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288902440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f5e21b97bad2c1a576af665baf38ceeeffd17f49c833835f87944785e071c1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:54 GMT
ADD file:4bf66d4081da52e8b692fcff96aad84d3e68bda4f62e870e8f4803153c70e24c in / 
# Wed, 11 Jan 2023 02:34:55 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:05:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:05:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 Jan 2023 03:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 21:51:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 21:51:10 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Feb 2023 21:45:28 GMT
ENV GOLANG_VERSION=1.20
# Wed, 01 Feb 2023 21:45:38 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.linux-amd64.tar.gz'; 			sha256='5a9ebcc65c1cce56e0d2dc616aff4c4cedcfbda8cc6f0288cc08cda3b18dcbf1'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.linux-armv6l.tar.gz'; 			sha256='ee8550213c62812f90dbfd3d098195adedd450379fd4d3bb2c85607fd5a2d283'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.linux-arm64.tar.gz'; 			sha256='17700b6e5108e2a2c3b1a43cd865d3f9c66b7f1c5f0cec26d3672cc131cc0994'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.linux-386.tar.gz'; 			sha256='1420582fb43a15dbe94760fdd92171315414c4afc21ffe9d3b5875f9386ebe53'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.linux-ppc64le.tar.gz'; 			sha256='bccbf89c83e0aab2911e57217159bf0fc49bb07c6eebd2c23ae30af18fc5368b'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.linux-s390x.tar.gz'; 			sha256='4460deffbc01fe5f31fe226d296e366c0d6059b280743aea49bf81ab62ab8be8'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.src.tar.gz'; 		sha256='3a29ff0421beaf6329292b8a46311c9fbf06c800077ceddef5fb7f8d5b1ace33'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 01 Feb 2023 21:45:39 GMT
ENV GOPATH=/go
# Wed, 01 Feb 2023 21:45:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Feb 2023 21:45:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 01 Feb 2023 21:45:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ac7f2e1c758675427623d0da4faa88b336c62466c15a98af61efd3f015282f2f`  
		Last Modified: Wed, 11 Jan 2023 02:39:26 GMT  
		Size: 50.4 MB (50448910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcdf7fce05b60278ea57279b4fd04f78778f80a6d64b6f875afc4bde32c2d1b`  
		Last Modified: Wed, 11 Jan 2023 03:13:10 GMT  
		Size: 7.9 MB (7859410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed0c2752d8478245519a7aab5e660053796af3c7ea7b34ad3df855b33ff5502`  
		Last Modified: Wed, 11 Jan 2023 03:13:09 GMT  
		Size: 10.0 MB (10001385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf01cd4ea334ab5c64bed24016c153dc7c276f552f468e564664e739dac31e09`  
		Last Modified: Wed, 11 Jan 2023 03:13:25 GMT  
		Size: 51.9 MB (51869329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b928198451ee0a62ae50350c612ee7612163a3e0b1cd867cbad9d8b54357c90e`  
		Last Modified: Wed, 11 Jan 2023 21:54:10 GMT  
		Size: 68.9 MB (68851835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083e189d4e42f3fa2a8cef8fbd485123d1581560dbb4f15e832c419e1264c3d2`  
		Last Modified: Wed, 01 Feb 2023 21:50:38 GMT  
		Size: 99.9 MB (99871416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59638583a71fc556d27c54fb18431458e065651733ec1dd8f5b34c7a80b11384`  
		Last Modified: Wed, 01 Feb 2023 21:50:25 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:12eb6fb69ebd73fc9a703bd02a8e02ce271432795563ecac8d6ab9673a3f3419
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260691920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6962909fb566b3b3b6886304d97ae7b119a0076ce8c81e06a97ca821448561`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 04:00:52 GMT
ADD file:7a8ada9998422200d8f422ba7967ecc0f2435715f4b69347f7c0eddf589b1dc5 in / 
# Wed, 11 Jan 2023 04:00:53 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 04:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 04:34:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 Jan 2023 04:35:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Jan 2023 00:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Jan 2023 00:49:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Feb 2023 02:32:32 GMT
ENV GOLANG_VERSION=1.20
# Thu, 02 Feb 2023 02:33:10 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.linux-amd64.tar.gz'; 			sha256='5a9ebcc65c1cce56e0d2dc616aff4c4cedcfbda8cc6f0288cc08cda3b18dcbf1'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.linux-armv6l.tar.gz'; 			sha256='ee8550213c62812f90dbfd3d098195adedd450379fd4d3bb2c85607fd5a2d283'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.linux-arm64.tar.gz'; 			sha256='17700b6e5108e2a2c3b1a43cd865d3f9c66b7f1c5f0cec26d3672cc131cc0994'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.linux-386.tar.gz'; 			sha256='1420582fb43a15dbe94760fdd92171315414c4afc21ffe9d3b5875f9386ebe53'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.linux-ppc64le.tar.gz'; 			sha256='bccbf89c83e0aab2911e57217159bf0fc49bb07c6eebd2c23ae30af18fc5368b'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.linux-s390x.tar.gz'; 			sha256='4460deffbc01fe5f31fe226d296e366c0d6059b280743aea49bf81ab62ab8be8'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.src.tar.gz'; 		sha256='3a29ff0421beaf6329292b8a46311c9fbf06c800077ceddef5fb7f8d5b1ace33'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Thu, 02 Feb 2023 02:33:11 GMT
ENV GOPATH=/go
# Thu, 02 Feb 2023 02:33:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Feb 2023 02:33:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 02 Feb 2023 02:33:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1af2e9dc936b1285f4472a18af1e9b913352d31b1238f1c158995d9c15b6024a`  
		Last Modified: Wed, 11 Jan 2023 04:08:13 GMT  
		Size: 45.9 MB (45915604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba37bd2b08543867db0934e29dd6c1476f71509aa0b42f10786733820b6c2008`  
		Last Modified: Wed, 11 Jan 2023 04:45:15 GMT  
		Size: 7.1 MB (7147799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe84c7428034fbe63e62868f1c420279eda084b4d396cc79161f73a9aeba29c`  
		Last Modified: Wed, 11 Jan 2023 04:45:15 GMT  
		Size: 9.3 MB (9349030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8389ce7126cbebf5244cba3ec839cd0c0cf2ff817fcc3f23a3ea989766c31570`  
		Last Modified: Wed, 11 Jan 2023 04:45:34 GMT  
		Size: 47.4 MB (47397357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad62d9a464fe9706f594e79509ad58868248fb3d121412b1e15091fed3495bca`  
		Last Modified: Thu, 12 Jan 2023 00:55:45 GMT  
		Size: 53.3 MB (53322228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9cd8b09a761eacbfd37ad982a2e018f4f6fc52f1a224d95a42b72d8a65e068e`  
		Last Modified: Thu, 02 Feb 2023 02:40:13 GMT  
		Size: 97.6 MB (97559776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81437fb2d7b4f40888bee6be2007c307596391c7903c22cd4cc552d07ad785b`  
		Last Modified: Thu, 02 Feb 2023 02:39:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:14887f5c4d6a389f48718c5357b3f913d9ad0ba01ab0b4ec217865d1762be2e2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.1 MB (277074349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4dd18ba1dcb9369d69b885b2f9886058855e37b05b6db6dae582cc8b052df4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:45 GMT
ADD file:0241487c3fb43506be1511724644c00339c32361e6b4c21a224d7190e4e1063b in / 
# Sat, 04 Feb 2023 06:17:46 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:47:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 06:47:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Feb 2023 06:47:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 20:37:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 20:37:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 20:37:30 GMT
ENV GOLANG_VERSION=1.20
# Sat, 04 Feb 2023 20:38:00 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.linux-amd64.tar.gz'; 			sha256='5a9ebcc65c1cce56e0d2dc616aff4c4cedcfbda8cc6f0288cc08cda3b18dcbf1'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.linux-armv6l.tar.gz'; 			sha256='ee8550213c62812f90dbfd3d098195adedd450379fd4d3bb2c85607fd5a2d283'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.linux-arm64.tar.gz'; 			sha256='17700b6e5108e2a2c3b1a43cd865d3f9c66b7f1c5f0cec26d3672cc131cc0994'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.linux-386.tar.gz'; 			sha256='1420582fb43a15dbe94760fdd92171315414c4afc21ffe9d3b5875f9386ebe53'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.linux-ppc64le.tar.gz'; 			sha256='bccbf89c83e0aab2911e57217159bf0fc49bb07c6eebd2c23ae30af18fc5368b'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.linux-s390x.tar.gz'; 			sha256='4460deffbc01fe5f31fe226d296e366c0d6059b280743aea49bf81ab62ab8be8'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.src.tar.gz'; 		sha256='3a29ff0421beaf6329292b8a46311c9fbf06c800077ceddef5fb7f8d5b1ace33'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Sat, 04 Feb 2023 20:38:01 GMT
ENV GOPATH=/go
# Sat, 04 Feb 2023 20:38:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 20:38:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 04 Feb 2023 20:38:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8e0a5a2afd38370f358c0a7154362a8d17faf709c206b40b1553a077f810c3b3`  
		Last Modified: Sat, 04 Feb 2023 06:21:43 GMT  
		Size: 49.2 MB (49239373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec9f4eeb3b61de38aae4678c79731cf85a809fe12a5e34b7c6043703f3ff600`  
		Last Modified: Sat, 04 Feb 2023 06:53:01 GMT  
		Size: 7.7 MB (7729353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3a72451e0eb2675bda2fe64354ac7eefce09a9d51825711cb59d895cea46d2`  
		Last Modified: Sat, 04 Feb 2023 06:53:01 GMT  
		Size: 10.0 MB (10003656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a612a40907fa6b93dcc878ffa9b0a5bf6307d5498b4685e2f5f3cd98993694`  
		Last Modified: Sat, 04 Feb 2023 06:53:16 GMT  
		Size: 52.2 MB (52191607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8abe101a0a98826561bb26c009b7870df987b16c301868a1029a401a5258a97`  
		Last Modified: Sat, 04 Feb 2023 20:40:12 GMT  
		Size: 62.7 MB (62714426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722467ea23cfb57d1a8e3b1a7a3f2b8e437c600994e4ab59dfac038cb9eac51e`  
		Last Modified: Sat, 04 Feb 2023 20:40:15 GMT  
		Size: 95.2 MB (95195779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0341bcd4c3d9776028a3c4d7d3eac5b503266fc63b8c4d5988dbb1fffa552e88`  
		Last Modified: Sat, 04 Feb 2023 20:40:05 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; 386

```console
$ docker pull golang@sha256:68e84570e92ae0155dbeab923494c2a5575611b35492426263275d636acc91e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296629544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697b01a2a4b9d15b3167f3f1f98e19c9e595adfc1cd7c3a1f57489926c8f08a9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 03:16:19 GMT
ADD file:8dffdae65db31d57b6a4946bc86469afb548c4c52bf49970da0b113ce9d79d67 in / 
# Wed, 11 Jan 2023 03:16:20 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:48:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 Jan 2023 03:48:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 18:27:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 18:27:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Feb 2023 22:41:01 GMT
ENV GOLANG_VERSION=1.20
# Wed, 01 Feb 2023 22:41:31 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.linux-amd64.tar.gz'; 			sha256='5a9ebcc65c1cce56e0d2dc616aff4c4cedcfbda8cc6f0288cc08cda3b18dcbf1'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.linux-armv6l.tar.gz'; 			sha256='ee8550213c62812f90dbfd3d098195adedd450379fd4d3bb2c85607fd5a2d283'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.linux-arm64.tar.gz'; 			sha256='17700b6e5108e2a2c3b1a43cd865d3f9c66b7f1c5f0cec26d3672cc131cc0994'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.linux-386.tar.gz'; 			sha256='1420582fb43a15dbe94760fdd92171315414c4afc21ffe9d3b5875f9386ebe53'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.linux-ppc64le.tar.gz'; 			sha256='bccbf89c83e0aab2911e57217159bf0fc49bb07c6eebd2c23ae30af18fc5368b'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.linux-s390x.tar.gz'; 			sha256='4460deffbc01fe5f31fe226d296e366c0d6059b280743aea49bf81ab62ab8be8'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.src.tar.gz'; 		sha256='3a29ff0421beaf6329292b8a46311c9fbf06c800077ceddef5fb7f8d5b1ace33'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 01 Feb 2023 22:41:32 GMT
ENV GOPATH=/go
# Wed, 01 Feb 2023 22:41:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Feb 2023 22:41:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 01 Feb 2023 22:41:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5a7dc875a0464942e7ebcaa41090f3f519845bd311f57a36c844c3c04ed97fa3`  
		Last Modified: Wed, 11 Jan 2023 03:22:23 GMT  
		Size: 51.2 MB (51207833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7694d94f77e5d95edd02e4559043234d6be7116378fe5d6e7588cb21efa07cda`  
		Last Modified: Wed, 11 Jan 2023 03:55:49 GMT  
		Size: 8.0 MB (8026066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8167061e46170114311ef3049f70a3fead0d705a5b732546acc30a1977468a8b`  
		Last Modified: Wed, 11 Jan 2023 03:55:49 GMT  
		Size: 10.1 MB (10128023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eede8eda1377eef853bf6fc8ea42636102facca526c270d36c37369da6472601`  
		Last Modified: Wed, 11 Jan 2023 03:56:08 GMT  
		Size: 53.5 MB (53472254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a76add64eaafeb9d615c7661563b38e6119138f2fd32c470af62c7ff7b20676`  
		Last Modified: Wed, 11 Jan 2023 18:32:11 GMT  
		Size: 73.5 MB (73492268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260254ddb353d6faa8397a70297537e952afdf62eb0eba6b941be477f5ef873e`  
		Last Modified: Wed, 01 Feb 2023 22:47:55 GMT  
		Size: 100.3 MB (100302974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752f3e74318315e5d1c0c874b164db0ffabc4e12154a389aa245df65e72254eb`  
		Last Modified: Wed, 01 Feb 2023 22:47:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

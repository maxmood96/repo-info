## `golang:rc-alpine3.14`

```console
$ docker pull golang@sha256:5fe676b0f517d7420ed816d747735b580c767d9a758319446823f64f9eeff7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `golang:rc-alpine3.14` - linux; amd64

```console
$ docker pull golang@sha256:c3996d2b62a2e1a2e8e7ffb704d3bddbe42c8eae35505a29b02339fe1f7cb7dd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118173783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285814c2053144f6cae5a0d9298db1742716f67adbeb011491baf94f246dd005`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 02:10:31 GMT
RUN apk add --no-cache ca-certificates
# Sat, 13 Nov 2021 02:10:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 02:10:33 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Dec 2021 00:23:37 GMT
ENV GOLANG_VERSION=1.18beta1
# Wed, 15 Dec 2021 00:26:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18beta1.src.tar.gz'; 		sha256='418c028db14699cb5b2d4907ad3a419d79f789b31916ef8764867e4a78e653a1'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 15 Dec 2021 00:26:07 GMT
ENV GOPATH=/go
# Wed, 15 Dec 2021 00:26:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Dec 2021 00:26:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 15 Dec 2021 00:26:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78c28b3bbf700f24e2e19b320a3a087668cdebd027afe2d87a7d96be65a543a`  
		Last Modified: Sat, 13 Nov 2021 02:25:04 GMT  
		Size: 282.0 KB (281969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248309d37e253af28a560213d3a52264be64a4d36bf2cb0da7ea77886962e400`  
		Last Modified: Sat, 13 Nov 2021 02:25:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725951dbd9d162a09201f6c4e0073866a7170579811b99fca6ce9985188e563b`  
		Last Modified: Wed, 15 Dec 2021 00:30:01 GMT  
		Size: 115.1 MB (115068522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea0d3eb206c4574e77d495379fc9c85b112c0ffea0c8f5176cea9df598014a4`  
		Last Modified: Wed, 15 Dec 2021 00:29:46 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-alpine3.14` - linux; arm variant v6

```console
$ docker pull golang@sha256:ce84e6bdcde3296b7a3f34c452784a93888abff682c77b7aee9e77382bc9e072
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114410217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d6e68f9ab954dc3984e719452444ac05462558fbee854e678732170db4c8b5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 03:10:01 GMT
RUN apk add --no-cache ca-certificates
# Sat, 13 Nov 2021 03:10:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 03:10:03 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Dec 2021 00:53:47 GMT
ENV GOLANG_VERSION=1.18beta1
# Wed, 15 Dec 2021 00:57:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18beta1.src.tar.gz'; 		sha256='418c028db14699cb5b2d4907ad3a419d79f789b31916ef8764867e4a78e653a1'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 15 Dec 2021 00:57:33 GMT
ENV GOPATH=/go
# Wed, 15 Dec 2021 00:57:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Dec 2021 00:57:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 15 Dec 2021 00:57:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae12653b711772d7e560f64cd4766c8f77b3141f6f7277559675933e1f5f6b3`  
		Last Modified: Sat, 13 Nov 2021 03:24:46 GMT  
		Size: 282.1 KB (282110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e842bfb6b84a49903edfad8514887109a35d6ad26bb7526f4fc2154e0993266`  
		Last Modified: Sat, 13 Nov 2021 03:24:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e175ff52af8cdce431f737219635f8a286b5effbce8ee81aed947984781bae79`  
		Last Modified: Wed, 15 Dec 2021 01:03:27 GMT  
		Size: 111.5 MB (111492407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e461faa09fe268774e30cfc297eb574fd967a96c7e4c1c54ce20b9e2399e9f`  
		Last Modified: Wed, 15 Dec 2021 01:02:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-alpine3.14` - linux; arm variant v7

```console
$ docker pull golang@sha256:a3c8b5fabdd9a27ae54c896f1d4d72f83984d663754d44b81de046967b337760
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113992765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db31d0853102e577ea0d16ae167d8cbc0cfa8022207cc25278fdf69bb298469`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 11:20:52 GMT
RUN apk add --no-cache ca-certificates
# Sat, 13 Nov 2021 11:20:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 11:20:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Dec 2021 01:08:00 GMT
ENV GOLANG_VERSION=1.18beta1
# Wed, 15 Dec 2021 01:11:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18beta1.src.tar.gz'; 		sha256='418c028db14699cb5b2d4907ad3a419d79f789b31916ef8764867e4a78e653a1'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 15 Dec 2021 01:11:39 GMT
ENV GOPATH=/go
# Wed, 15 Dec 2021 01:11:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Dec 2021 01:11:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 15 Dec 2021 01:11:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f548be3ae33f168d46bb5a079b02ea99b26adcc6037a7a83093ef75737b8ead`  
		Last Modified: Sat, 13 Nov 2021 11:37:20 GMT  
		Size: 281.3 KB (281273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053162e9c4e95b3bcce67319cd02ecce4432174930ad4d1c095873d7f4aa3348`  
		Last Modified: Sat, 13 Nov 2021 11:37:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef731050414e179820bf847f07ca571bfb734396ded024d32334119967b9987`  
		Last Modified: Wed, 15 Dec 2021 01:25:20 GMT  
		Size: 111.3 MB (111272565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4285c8c6bf05d08246a62669730c0ac45e81493607d2c75d4a9ae12394d2e9`  
		Last Modified: Wed, 15 Dec 2021 01:24:07 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:3ee40d83b30ed59e6c2c91ad0d971c64b028d22264c0ab92d678f1d12cdd1b28
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112960134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b8c641d935508462495d7c3d04800a5ca97c685df88f8f8284938a126a03ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 08:39:08 GMT
RUN apk add --no-cache ca-certificates
# Sat, 13 Nov 2021 08:39:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 08:39:10 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Dec 2021 00:43:19 GMT
ENV GOLANG_VERSION=1.18beta1
# Wed, 15 Dec 2021 00:44:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18beta1.src.tar.gz'; 		sha256='418c028db14699cb5b2d4907ad3a419d79f789b31916ef8764867e4a78e653a1'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 15 Dec 2021 00:44:50 GMT
ENV GOPATH=/go
# Wed, 15 Dec 2021 00:44:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Dec 2021 00:44:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 15 Dec 2021 00:44:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31131f141aeef3bf33028faecf3cb7d9d07c9ad6f9217e00d63ae69e9f1b77d`  
		Last Modified: Sat, 13 Nov 2021 08:46:56 GMT  
		Size: 281.9 KB (281925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3ae2225eebbae8fb0dcad25b2437676da54bca6a9c6be07df00313989ac0f2`  
		Last Modified: Sat, 13 Nov 2021 08:46:57 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a91c039f6fec08471c25e815ca50d7e4df35db1511f296d3bf7cfb6725a26f4`  
		Last Modified: Wed, 15 Dec 2021 00:49:53 GMT  
		Size: 110.0 MB (109960230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10920cb24b5dc9daf579874141dd817e5a34d76880ba7acc568dd563eee12fb`  
		Last Modified: Wed, 15 Dec 2021 00:49:37 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-alpine3.14` - linux; 386

```console
$ docker pull golang@sha256:95d9ae3e13a21faa05c7f67bac7733cb63646341606a8d3dc22d865828ed998d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123629730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b321e79412101f61bb022057708d296140836b772bf19b62ff89e547eb6fb8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:14:20 GMT
RUN apk add --no-cache ca-certificates
# Sat, 13 Nov 2021 05:14:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 05:14:23 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Dec 2021 00:44:01 GMT
ENV GOLANG_VERSION=1.18beta1
# Wed, 15 Dec 2021 00:47:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18beta1.src.tar.gz'; 		sha256='418c028db14699cb5b2d4907ad3a419d79f789b31916ef8764867e4a78e653a1'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 15 Dec 2021 00:47:26 GMT
ENV GOPATH=/go
# Wed, 15 Dec 2021 00:47:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Dec 2021 00:47:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 15 Dec 2021 00:47:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518125c3325ab41f5b0e1616e0303ad8daa40abe641e7b02cb1f5b556903789b`  
		Last Modified: Sat, 13 Nov 2021 05:42:46 GMT  
		Size: 282.5 KB (282476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778361f22ea82c71e1b0d3fbff47630eb6280ffdf8c9d43b88f7672a1063b45d`  
		Last Modified: Sat, 13 Nov 2021 05:42:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aac625ee9cdedcf814cbc26342734ee560944d2a5a8693c359a8080aff771cf`  
		Last Modified: Wed, 15 Dec 2021 00:54:29 GMT  
		Size: 120.5 MB (120515996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee76031dededd6c0de90cb99afa5d2a787943c5bd365ede2f3dfa1e8f4eeac8`  
		Last Modified: Wed, 15 Dec 2021 00:54:01 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-alpine3.14` - linux; ppc64le

```console
$ docker pull golang@sha256:08359023167c76381a7d317970f78b5b94510ed6e31540776ef4de6200627fe0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105794884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a44762ab9d9f451d09162a92c61e9f1f240f274ad1e5ee7fb6d860b5e97ab9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:02:31 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 06 Aug 2021 21:02:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 Aug 2021 21:02:46 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 21:02:50 GMT
ENV GOLANG_VERSION=1.17rc2
# Fri, 06 Aug 2021 21:05:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.17rc2.src.tar.gz'; 	sha256='5ab21d75552390c63087518e4eba2972fb009aea97ff2bcc42dff264c5f46fe9'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Aug 2021 21:05:15 GMT
ENV GOPATH=/go
# Fri, 06 Aug 2021 21:05:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 21:05:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Aug 2021 21:05:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f69fce9d10f5a5c047377039cda1fd5125aae4ec022be3dd7aede58be5a483`  
		Last Modified: Fri, 06 Aug 2021 21:12:42 GMT  
		Size: 283.6 KB (283642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fdcb934d4034adf5e88a3b7bff7a633580eb8c0f18480df4123a14c499558b`  
		Last Modified: Fri, 06 Aug 2021 21:12:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea265381facd1fe3c3ea9349ea965afe43b8dabc5923d1f0ab8d2fbd147aa288`  
		Last Modified: Fri, 06 Aug 2021 21:13:00 GMT  
		Size: 102.7 MB (102699779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1148804c28dcdc23583ccbbc1314361a5d0bde321633bbdbf705bbda39d5fb41`  
		Last Modified: Fri, 06 Aug 2021 21:12:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-alpine3.14` - linux; s390x

```console
$ docker pull golang@sha256:2720db824912bdd6253c90424c7d9fe3b21cddea9be9de70f25927c20770c61b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115895009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137652d2e4dd7c2ff623fc7f555c5d453a061195442894b0dfffdc2b402e8541`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:57:17 GMT
RUN apk add --no-cache ca-certificates
# Fri, 12 Nov 2021 21:57:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:57:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Dec 2021 00:44:42 GMT
ENV GOLANG_VERSION=1.18beta1
# Wed, 15 Dec 2021 00:46:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18beta1.src.tar.gz'; 		sha256='418c028db14699cb5b2d4907ad3a419d79f789b31916ef8764867e4a78e653a1'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 15 Dec 2021 00:46:31 GMT
ENV GOPATH=/go
# Wed, 15 Dec 2021 00:46:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Dec 2021 00:46:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 15 Dec 2021 00:46:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98670e9bf78af3e1c52d6774dcedad76407c2d72bebbe6e6f08171cd4353fa03`  
		Last Modified: Fri, 12 Nov 2021 22:05:24 GMT  
		Size: 282.4 KB (282378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479a5a7a0f8f8b10d3f6f46f5fc54fa00400c2b8b7ccbc69d3f4496932dd0a7c`  
		Last Modified: Fri, 12 Nov 2021 22:05:24 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd315101c3181c0be3c4e26f5443deaa9d9762a7d6e54ff641ed7fe8b8406451`  
		Last Modified: Wed, 15 Dec 2021 00:50:45 GMT  
		Size: 113.0 MB (113003043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221a187a45a58028ae6b0eba9ca7be6fc0758128bb59683a1931055635a2f780`  
		Last Modified: Wed, 15 Dec 2021 00:50:31 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

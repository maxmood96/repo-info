## `golang:alpine3.14`

```console
$ docker pull golang@sha256:76cc30a0d4aef1186407e8771205659abd9725163d057800942270bb66623c8b
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

### `golang:alpine3.14` - linux; amd64

```console
$ docker pull golang@sha256:3fa90f1a892c3f9f93149d530af36b2cdd6667888643e9ba9551493cf3e2f952
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118668285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825031d222a2ae0304c80bf776fa920142ad7908655bb5e28c5620844e4073e8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 06:34:58 GMT
RUN apk add --no-cache ca-certificates
# Sat, 19 Mar 2022 06:34:58 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 19 Mar 2022 06:34:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 06:34:58 GMT
ENV GOLANG_VERSION=1.18
# Fri, 25 Mar 2022 01:53:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.src.tar.gz'; 		sha256='38f423db4cc834883f2b52344282fa7a39fbb93650dc62a11fdf0be6409bdad6'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 		if [ "$GOARCH" = 'ppc64le' ]; then 			wget -O ppc64le-alpine.patch 'https://github.com/golang/go/commit/946167906ed8646c433c257b074a10e01f0a7dab.patch'; 			apk add --no-cache --virtual .build-patch patch; 			patch --strip=1 --input="$PWD/ppc64le-alpine.patch" --directory=/usr/local/go; 			apk del --no-network .build-patch; 			rm ppc64le-alpine.patch; 		fi; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 25 Mar 2022 01:53:04 GMT
ENV GOPATH=/go
# Fri, 25 Mar 2022 01:53:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Mar 2022 01:53:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 25 Mar 2022 01:53:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e98a1cdf8728e92e0580287c2e70dbb468f19ea467ca0a17d668b242b1b9338`  
		Last Modified: Sat, 19 Mar 2022 06:48:23 GMT  
		Size: 271.7 KB (271675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9ee354eeb8a66c68eca6da95581e91662872d5f79250b3ccfa53bfe2d96b7d`  
		Last Modified: Sat, 19 Mar 2022 06:48:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc62bfd84cb87ebf60919ee0e00d7ae944e54b7169300f53d7ba9961167f1a96`  
		Last Modified: Fri, 25 Mar 2022 01:55:03 GMT  
		Size: 115.6 MB (115580131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eec1e2d6b9ebc84c4ff1e568fa76870dd6173f1a7172c22a89d8c6d43af720`  
		Last Modified: Fri, 25 Mar 2022 01:54:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.14` - linux; arm variant v6

```console
$ docker pull golang@sha256:9768292cc8542e2f7fe3e9ace7e407a165fe27c94079c0db4d857956a9e36a4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114844702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0c51f22e3b82d8ef899f06fcd9879dd81c0962a45a44501d62b4083ab5815c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:23:34 GMT
RUN apk add --no-cache ca-certificates
# Thu, 17 Mar 2022 15:23:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 15:23:36 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 15:23:36 GMT
ENV GOLANG_VERSION=1.18
# Fri, 25 Mar 2022 00:57:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.src.tar.gz'; 		sha256='38f423db4cc834883f2b52344282fa7a39fbb93650dc62a11fdf0be6409bdad6'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 		if [ "$GOARCH" = 'ppc64le' ]; then 			wget -O ppc64le-alpine.patch 'https://github.com/golang/go/commit/946167906ed8646c433c257b074a10e01f0a7dab.patch'; 			apk add --no-cache --virtual .build-patch patch; 			patch --strip=1 --input="$PWD/ppc64le-alpine.patch" --directory=/usr/local/go; 			apk del --no-network .build-patch; 			rm ppc64le-alpine.patch; 		fi; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 25 Mar 2022 00:57:26 GMT
ENV GOPATH=/go
# Fri, 25 Mar 2022 00:57:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Mar 2022 00:57:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 25 Mar 2022 00:57:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274cc3ac903e4331155327a5593cf56cb9718433b43c056b5496d17fd7594c67`  
		Last Modified: Thu, 17 Mar 2022 15:33:36 GMT  
		Size: 272.1 KB (272098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee426ba3bff1dd9b6475196b95a58750531487f5dce93ad99cbccd7f548a4f3`  
		Last Modified: Thu, 17 Mar 2022 15:33:36 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a795667e28e507e884bc392850632244965175f88c769f6bdf13b653dbb61680`  
		Last Modified: Fri, 25 Mar 2022 01:02:13 GMT  
		Size: 111.9 MB (111942931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0f97306d4e31f76553f7aa24508c3407a864f764bc637a2a2d5becd29628ed`  
		Last Modified: Fri, 25 Mar 2022 01:01:04 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.14` - linux; arm variant v7

```console
$ docker pull golang@sha256:03fb2daf4445064c7a2561dfdd437899200248deba5376a211adf02cfa9ebc2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114413313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6281a7c0537dd8cd8709eec5ca9bd6e4888e96790c036f617633eea941c74361`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 17:21:06 GMT
ADD file:c25fcf153ea349f64e08a1bd0756ce550f2a081ad56cc40c89027d85d1bc26da in / 
# Thu, 17 Mar 2022 17:21:06 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:26:11 GMT
RUN apk add --no-cache ca-certificates
# Sat, 19 Mar 2022 00:26:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 19 Mar 2022 00:26:13 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 00:26:13 GMT
ENV GOLANG_VERSION=1.18
# Fri, 25 Mar 2022 04:52:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.src.tar.gz'; 		sha256='38f423db4cc834883f2b52344282fa7a39fbb93650dc62a11fdf0be6409bdad6'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 		if [ "$GOARCH" = 'ppc64le' ]; then 			wget -O ppc64le-alpine.patch 'https://github.com/golang/go/commit/946167906ed8646c433c257b074a10e01f0a7dab.patch'; 			apk add --no-cache --virtual .build-patch patch; 			patch --strip=1 --input="$PWD/ppc64le-alpine.patch" --directory=/usr/local/go; 			apk del --no-network .build-patch; 			rm ppc64le-alpine.patch; 		fi; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 25 Mar 2022 04:52:57 GMT
ENV GOPATH=/go
# Fri, 25 Mar 2022 04:52:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Mar 2022 04:52:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 25 Mar 2022 04:52:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c3a1157c36d8d156f7664fa098212ab2149a64bcb59767cdf4595a86617c17fd`  
		Last Modified: Thu, 17 Mar 2022 17:22:45 GMT  
		Size: 2.4 MB (2430456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22f339460248fda93db1d5d399b62f74a803ccdee1512eade2219894316e052`  
		Last Modified: Sat, 19 Mar 2022 00:43:56 GMT  
		Size: 271.1 KB (271069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a24d971ac285e082416d7f09fa5d4fd7265741b55eebe4c787d7ff5ee09f674`  
		Last Modified: Sat, 19 Mar 2022 00:43:56 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d4a5c66922d69dfb0c129b5bdd48125d911ce221fa6b6df61af198879b3ceb`  
		Last Modified: Fri, 25 Mar 2022 05:00:12 GMT  
		Size: 111.7 MB (111711479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fadfc68e77f9b3182c2f064819d5bedfa1fb265953d8e568cc0aeb558ad045`  
		Last Modified: Fri, 25 Mar 2022 04:58:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.14` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:9dfb41a4e83eb7b3b4568f3e562d81d15a391534d829a72871502ec3ebb112cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113394854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ffa84b30cee815995a4d83ce82cd64632bf990644a69ea8f77e736ffa8b6f1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 16:28:31 GMT
RUN apk add --no-cache ca-certificates
# Fri, 18 Mar 2022 16:28:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 18 Mar 2022 16:28:32 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 16:28:33 GMT
ENV GOLANG_VERSION=1.18
# Fri, 25 Mar 2022 03:06:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.src.tar.gz'; 		sha256='38f423db4cc834883f2b52344282fa7a39fbb93650dc62a11fdf0be6409bdad6'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 		if [ "$GOARCH" = 'ppc64le' ]; then 			wget -O ppc64le-alpine.patch 'https://github.com/golang/go/commit/946167906ed8646c433c257b074a10e01f0a7dab.patch'; 			apk add --no-cache --virtual .build-patch patch; 			patch --strip=1 --input="$PWD/ppc64le-alpine.patch" --directory=/usr/local/go; 			apk del --no-network .build-patch; 			rm ppc64le-alpine.patch; 		fi; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 25 Mar 2022 03:06:50 GMT
ENV GOPATH=/go
# Fri, 25 Mar 2022 03:06:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Mar 2022 03:06:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 25 Mar 2022 03:06:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7223a2507d43524dee355c03288258811035aa8f053accbdc32c336c3f6df91e`  
		Last Modified: Fri, 18 Mar 2022 16:39:04 GMT  
		Size: 271.8 KB (271752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b529949a5b726089bbfe2a886f1cc74a77929492a5dadfa649dc9f433c2c0a11`  
		Last Modified: Fri, 18 Mar 2022 16:39:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e98885a7b10116a9b37e8973b4468267d765aaca3899869d1614917088de85c`  
		Last Modified: Fri, 25 Mar 2022 03:09:42 GMT  
		Size: 110.4 MB (110406935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11a36418ff5f8d8dcdc3dac293b82e7b56323eef38200e57f42418e6d171351`  
		Last Modified: Fri, 25 Mar 2022 03:09:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.14` - linux; 386

```console
$ docker pull golang@sha256:ca08c2cf4fe1f3a33dd94419bc18fb996559a93a32a1a2a773dd81ac2d2f0706
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124058923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6f024272dd1268688b2314172e7fa38bd59d28b3343c780a3ba68f03d46550`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 14:59:36 GMT
ADD file:5bb8a2cf301e0add52528df0f7f5c5b3c9b14495c5aa85c8fd628731fcd348aa in / 
# Wed, 23 Mar 2022 14:59:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 17:54:52 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 17:54:53 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 17:54:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 17:54:55 GMT
ENV GOLANG_VERSION=1.18
# Fri, 25 Mar 2022 01:42:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.src.tar.gz'; 		sha256='38f423db4cc834883f2b52344282fa7a39fbb93650dc62a11fdf0be6409bdad6'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 		if [ "$GOARCH" = 'ppc64le' ]; then 			wget -O ppc64le-alpine.patch 'https://github.com/golang/go/commit/946167906ed8646c433c257b074a10e01f0a7dab.patch'; 			apk add --no-cache --virtual .build-patch patch; 			patch --strip=1 --input="$PWD/ppc64le-alpine.patch" --directory=/usr/local/go; 			apk del --no-network .build-patch; 			rm ppc64le-alpine.patch; 		fi; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 25 Mar 2022 01:42:36 GMT
ENV GOPATH=/go
# Fri, 25 Mar 2022 01:42:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Mar 2022 01:42:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 25 Mar 2022 01:42:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8fd9b2c548e42517da6865245538c8f53b774738b4fd7cb2d57ad8716e71748c`  
		Last Modified: Thu, 17 Mar 2022 16:35:25 GMT  
		Size: 2.8 MB (2823782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a372442158e2c7f5c16a36179f170064c48fcc1fd3852c2a9ed2e57e41aa846b`  
		Last Modified: Wed, 23 Mar 2022 18:05:41 GMT  
		Size: 272.2 KB (272201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae899f3f4e2b9c1d89bfa4ac0d1df6aa639352bb74da8255a91067d218887674`  
		Last Modified: Wed, 23 Mar 2022 18:05:40 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a23ceb275e4f2a0ca9782697b39d9033d16ba31aa82f8b84a26e049d94bb93c`  
		Last Modified: Fri, 25 Mar 2022 01:45:56 GMT  
		Size: 121.0 MB (120962660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8f87b6bf6b1aa46c776e893cedcbbaa259dbdea6f7abf180bab586861e69c2`  
		Last Modified: Fri, 25 Mar 2022 01:45:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.14` - linux; ppc64le

```console
$ docker pull golang@sha256:ad50ee9867ca14c0e5626df524af8bd774abf6f88fde0c4fa64a1af3ae0832cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113649682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1884f2c000ab0f747ac86bddc1de80aac6d524a257c900e7cb5ce3ce9be12065`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 18:18:43 GMT
ADD file:bf9c99d8209e0bed9fd3b62cbe691ebf3829d5a35e63e2b066f1f842577a6d24 in / 
# Thu, 17 Mar 2022 18:18:48 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 23:24:45 GMT
RUN apk add --no-cache ca-certificates
# Thu, 17 Mar 2022 23:24:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 23:25:05 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 20:06:20 GMT
ENV GOLANG_VERSION=1.18
# Fri, 25 Mar 2022 04:23:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.src.tar.gz'; 		sha256='38f423db4cc834883f2b52344282fa7a39fbb93650dc62a11fdf0be6409bdad6'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 		if [ "$GOARCH" = 'ppc64le' ]; then 			wget -O ppc64le-alpine.patch 'https://github.com/golang/go/commit/946167906ed8646c433c257b074a10e01f0a7dab.patch'; 			apk add --no-cache --virtual .build-patch patch; 			patch --strip=1 --input="$PWD/ppc64le-alpine.patch" --directory=/usr/local/go; 			apk del --no-network .build-patch; 			rm ppc64le-alpine.patch; 		fi; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 25 Mar 2022 04:23:22 GMT
ENV GOPATH=/go
# Fri, 25 Mar 2022 04:23:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Mar 2022 04:23:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 25 Mar 2022 04:24:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8b7e8363a93630a772b70e3cf72231f43c62addae0ee8e507c61d43e3781c4e7`  
		Last Modified: Thu, 17 Mar 2022 18:20:01 GMT  
		Size: 2.8 MB (2817281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ad6b3dcc4590050fb55a51f7946c4618781ac77bccba620eab58dcf082f6f4`  
		Last Modified: Thu, 17 Mar 2022 23:41:38 GMT  
		Size: 274.2 KB (274156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d047d8a33a2ff8899e4020cbfb6f3e3fda7c99191dd5780fdd2248dff3363831`  
		Last Modified: Thu, 17 Mar 2022 23:41:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637e54773e1b4254c6371398090cb6fdb2ec4194f4b26f3b0e7521492a0702ac`  
		Last Modified: Fri, 25 Mar 2022 04:28:44 GMT  
		Size: 110.6 MB (110557936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc6cbbd72a1dd706156ec605ec8f3afad1fd1a2a4b3c7152915dce0b2486172`  
		Last Modified: Fri, 25 Mar 2022 04:28:26 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.14` - linux; s390x

```console
$ docker pull golang@sha256:296866ad7f31604cbac054f4beaa95f1f981128c1a148e809670381aa21e932b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116356838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094ab565cbf585828d810d17ff4b5fe81b9be84b89540083b0ac844260b7e6cf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 00:43:50 GMT
RUN apk add --no-cache ca-certificates
# Fri, 18 Mar 2022 00:43:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 18 Mar 2022 00:43:51 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 00:43:51 GMT
ENV GOLANG_VERSION=1.18
# Fri, 25 Mar 2022 01:45:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.src.tar.gz'; 		sha256='38f423db4cc834883f2b52344282fa7a39fbb93650dc62a11fdf0be6409bdad6'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 		if [ "$GOARCH" = 'ppc64le' ]; then 			wget -O ppc64le-alpine.patch 'https://github.com/golang/go/commit/946167906ed8646c433c257b074a10e01f0a7dab.patch'; 			apk add --no-cache --virtual .build-patch patch; 			patch --strip=1 --input="$PWD/ppc64le-alpine.patch" --directory=/usr/local/go; 			apk del --no-network .build-patch; 			rm ppc64le-alpine.patch; 		fi; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 25 Mar 2022 01:45:19 GMT
ENV GOPATH=/go
# Fri, 25 Mar 2022 01:45:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Mar 2022 01:45:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 25 Mar 2022 01:45:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e00a1fa1c431d2d265e6458017e5f24e645bdbf674a76d5e2f95205022ebfc`  
		Last Modified: Fri, 18 Mar 2022 00:54:10 GMT  
		Size: 272.2 KB (272234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c20a9d97d267df13d7d278ba2d446748a7863be9ba003de56008170c3c8290`  
		Last Modified: Fri, 18 Mar 2022 00:54:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09bc20553448fbcdca9496944a3fe37d13ac4b525512939add765248001fee4a`  
		Last Modified: Fri, 25 Mar 2022 01:47:56 GMT  
		Size: 113.5 MB (113479088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ff1fecdf5f1679dfe94d9f70b2e733299e2779ab5a35ef41514efa4c8d1c6b`  
		Last Modified: Fri, 25 Mar 2022 01:47:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

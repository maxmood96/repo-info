## `golang:1-alpine3.13`

```console
$ docker pull golang@sha256:e03794dd20cea5409c3c491098b7b9e4efcaf0a024e3760b9b22a2bde135396a
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

### `golang:1-alpine3.13` - linux; amd64

```console
$ docker pull golang@sha256:bc1ddd3c29f72ddeb0d6309eeb5f83ebecf258b4205e28a60adc8254663074a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113125469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bca85c58f86d9c748c89ce9763e0258602260f68735462be6c683c5f0b60139`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 01:33:28 GMT
RUN apk add --no-cache ca-certificates
# Wed, 01 Sep 2021 01:33:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 01:33:29 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:22:53 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:25:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ -n "${GO386:-}" ]; then 				GO386= ./bootstrap.bash; 				export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 				"$GOROOT_BOOTSTRAP/bin/go" version; 			fi; 			./make.bash; 			if [ -n "${GO386:-}" ]; then 				rm -rf "$GOROOT_BOOTSTRAP"; 			fi; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:25:02 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:25:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:25:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:25:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d31006c564459c3ab61dcb3573d6413ff02369431035abaa13256f5b877acd`  
		Last Modified: Wed, 01 Sep 2021 01:39:19 GMT  
		Size: 281.3 KB (281266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5ccded82967bed4ba5aebd1b9c01408d64dd138c675b402d519adedd763667`  
		Last Modified: Wed, 01 Sep 2021 01:39:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befa318ab45e94e55b34925da34c85ed2f7ad535dd9b034d5bd645f5b4e0c196`  
		Last Modified: Thu, 04 Nov 2021 20:33:40 GMT  
		Size: 110.0 MB (110029815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c51fe716c9cf4f8dca7046634b2303d6c9575ff7a2c682eeb93f1d289b2564`  
		Last Modified: Thu, 04 Nov 2021 20:33:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.13` - linux; arm variant v6

```console
$ docker pull golang@sha256:e7412228550135f41f89b01dc30ff68266d43f3b5e01b3af3b520e002808473b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107829863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932aa0be002f658693b54325cd9ab5ebef7e7de8461b983c6312a0b5e977f778`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 01:53:32 GMT
RUN apk add --no-cache ca-certificates
# Wed, 01 Sep 2021 01:53:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 01:53:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:53:45 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:57:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ -n "${GO386:-}" ]; then 				GO386= ./bootstrap.bash; 				export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 				"$GOROOT_BOOTSTRAP/bin/go" version; 			fi; 			./make.bash; 			if [ -n "${GO386:-}" ]; then 				rm -rf "$GOROOT_BOOTSTRAP"; 			fi; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:57:08 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:57:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:57:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:57:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76d8000e98e761cd31fcdd9e077fbeeaf4f4615e71b2eb54aa32e89069c45ef`  
		Last Modified: Wed, 01 Sep 2021 02:01:58 GMT  
		Size: 281.4 KB (281383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4392afcb8e803339caecdcf35c2c35541c85b541a0de99995cc28175ad0b20b5`  
		Last Modified: Wed, 01 Sep 2021 02:01:58 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f385bb2c4654757489384f34099404e352404fe21b5089de5849db5094c0f425`  
		Last Modified: Thu, 04 Nov 2021 21:07:53 GMT  
		Size: 104.9 MB (104924411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6ed94b27cba5d84c221d440a646d8798154e911c02c0c95a68d4f0cde7f5d4`  
		Last Modified: Thu, 04 Nov 2021 21:06:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.13` - linux; arm variant v7

```console
$ docker pull golang@sha256:f6de80449a6449f16352b9c34a926151d03b7b7527676220b4a548bad5fbd48e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107406318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ce1a979bb783278829cbf9df9efd8d778cd2486257a6d28b1d0836af188b85`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 01 Sep 2021 01:26:54 GMT
ADD file:4a3cd5b6e6a9e76edf236ec86eb493ae8b09bf3220a8c0fdcaa474b9d6135ad3 in / 
# Wed, 01 Sep 2021 01:26:55 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 10:40:25 GMT
RUN apk add --no-cache ca-certificates
# Wed, 01 Sep 2021 10:40:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 10:40:27 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:04:18 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 21:07:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ -n "${GO386:-}" ]; then 				GO386= ./bootstrap.bash; 				export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 				"$GOROOT_BOOTSTRAP/bin/go" version; 			fi; 			./make.bash; 			if [ -n "${GO386:-}" ]; then 				rm -rf "$GOROOT_BOOTSTRAP"; 			fi; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 21:07:28 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 21:07:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:07:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 21:07:30 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:48fad15491f9799a77d01e4a4a3b0e201ca2aba6f0849c39afa1160d6f3d905a`  
		Last Modified: Wed, 01 Sep 2021 01:28:39 GMT  
		Size: 2.4 MB (2425373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba500b1ad9394bd77a9a5036a938998fe273fd4f8d428f6efc2345b25d2331d`  
		Last Modified: Wed, 01 Sep 2021 10:51:04 GMT  
		Size: 280.5 KB (280533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89346654a54b68c446574c84483861f67ec892039c026603a45f145fa4da5c`  
		Last Modified: Wed, 01 Sep 2021 10:51:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1d3aa819bc21f578425a996aad255aee6cdff973cfd1f98f6b39889df356e1`  
		Last Modified: Thu, 04 Nov 2021 21:26:20 GMT  
		Size: 104.7 MB (104700103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74d983d440eff6c71f75aac0adce21a31dc25028c39722727f8164a369b69e1`  
		Last Modified: Thu, 04 Nov 2021 21:25:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:1a52db9a19419e7e893dccd52a020cbbfaa7a0ea21f221a7be0d6206346b461a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107275095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbacf555fb9a8d0606fa10590fae99765600dd6fcc0f693e99328507494d756`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Tue, 12 Oct 2021 19:51:06 GMT
RUN apk add --no-cache ca-certificates
# Tue, 12 Oct 2021 19:51:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 12 Oct 2021 19:51:07 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:46:31 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:47:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ -n "${GO386:-}" ]; then 				GO386= ./bootstrap.bash; 				export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 				"$GOROOT_BOOTSTRAP/bin/go" version; 			fi; 			./make.bash; 			if [ -n "${GO386:-}" ]; then 				rm -rf "$GOROOT_BOOTSTRAP"; 			fi; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:47:51 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:47:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:47:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:47:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e377beb4e4e7cf8058b0601ad1d431fcae32540f3f22cd2417aa9477ef8cab`  
		Last Modified: Tue, 12 Oct 2021 19:56:58 GMT  
		Size: 281.3 KB (281297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a6371172ad346729ebb7e4df5a883f3984794469879a145f079c9e018e5980`  
		Last Modified: Tue, 12 Oct 2021 19:56:58 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bc1e8e53748f4bc4865d9418234826dd549e8976b82a7b2960cf49c1eb9b0a`  
		Last Modified: Thu, 04 Nov 2021 20:56:04 GMT  
		Size: 104.3 MB (104280510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f349a49292d30fa65e767bfd5aed266d9d3bf3f6f441c26aa197a11284b8a5`  
		Last Modified: Thu, 04 Nov 2021 20:55:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.13` - linux; 386

```console
$ docker pull golang@sha256:49b69d92ab7d051a234ff92ac6af4a4a6ea55c73d5cd4a2368160bfb37ddcc25
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 MB (250800708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3645ade38bd53595a504c95048a1190e181ed7f41015514bca9b150f270477c3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Tue, 31 Aug 2021 23:07:58 GMT
RUN apk add --no-cache ca-certificates
# Tue, 31 Aug 2021 23:07:58 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 31 Aug 2021 23:07:59 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Oct 2021 00:43:18 GMT
ENV GOLANG_VERSION=1.17.2
# Fri, 08 Oct 2021 00:48:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.2.src.tar.gz'; 		sha256='2255eb3e4e824dd7d5fcdc2e7f84534371c186312e546fb1086a34c17752f431'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ -n "${GO386:-}" ]; then 				GO386= ./bootstrap.bash; 				export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 				"$GOROOT_BOOTSTRAP/bin/go" version; 			fi; 			./make.bash; 			if [ -n "${GO386:-}" ]; then 				rm -rf "$GOROOT_BOOTSTRAP"; 			fi; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 08 Oct 2021 00:48:57 GMT
ENV GOPATH=/go
# Fri, 08 Oct 2021 00:48:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Oct 2021 00:48:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 08 Oct 2021 00:48:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f19a0a6f8c0a92e3d7a2c0024bdbf2614ae01a7e6fbba7a3b6b01022bde51e`  
		Last Modified: Tue, 31 Aug 2021 23:22:47 GMT  
		Size: 281.8 KB (281829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ee815a6af2e5c0707758072d8cb06d62c0d86d8b5648e0349d0c4ea89ba7bd`  
		Last Modified: Tue, 31 Aug 2021 23:22:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e084f48a87c85511de0e4f503cd0b52ab55d09f721d375e3e31455884c21a8`  
		Last Modified: Fri, 08 Oct 2021 01:02:49 GMT  
		Size: 247.7 MB (247697474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada7c143f679a7f1453ff9a7156365b7003dfe02d63b21c91e03f7a4170e05cb`  
		Last Modified: Fri, 08 Oct 2021 01:02:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.13` - linux; ppc64le

```console
$ docker pull golang@sha256:8cc53c35985d4fa7d3377fa7e5f88020a7d5c68fff8452ade2d820528ff1898c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105734402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d8efff33600e7a0fa9d1aae81db3f0b584d87888ec07e5e69fc72157a3db67`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 01 Sep 2021 02:42:40 GMT
ADD file:07a51f1a2f818bd1c1651832ce63cb1e0046a57994724cda6a20ff1a2a685295 in / 
# Wed, 01 Sep 2021 02:42:41 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 10:54:35 GMT
RUN apk add --no-cache ca-certificates
# Wed, 01 Sep 2021 10:54:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 10:54:45 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Oct 2021 01:29:54 GMT
ENV GOLANG_VERSION=1.17.2
# Fri, 08 Oct 2021 01:32:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.2.src.tar.gz'; 		sha256='2255eb3e4e824dd7d5fcdc2e7f84534371c186312e546fb1086a34c17752f431'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ -n "${GO386:-}" ]; then 				GO386= ./bootstrap.bash; 				export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 				"$GOROOT_BOOTSTRAP/bin/go" version; 			fi; 			./make.bash; 			if [ -n "${GO386:-}" ]; then 				rm -rf "$GOROOT_BOOTSTRAP"; 			fi; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 08 Oct 2021 01:32:29 GMT
ENV GOPATH=/go
# Fri, 08 Oct 2021 01:32:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Oct 2021 01:32:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 08 Oct 2021 01:32:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:39d9bf63205258fe1d085fd596101e6fc46ff796cda8d3ba2983e166a25b74db`  
		Last Modified: Wed, 01 Sep 2021 02:43:53 GMT  
		Size: 2.8 MB (2814813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483a27eef205e5b273f873edd86a228f661f47e55dcdf1d9298deccafd860ebe`  
		Last Modified: Wed, 01 Sep 2021 11:02:48 GMT  
		Size: 283.4 KB (283411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f23659f3abaa527f4dea1e061d2e29a582ac55431bd7be0a7e7c5a0af4230d9`  
		Last Modified: Wed, 01 Sep 2021 11:02:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a44165cd6ae6a353d96edde7e72b487ff7c6d26c32a54213d339fa7cbd50bf5`  
		Last Modified: Fri, 08 Oct 2021 01:50:06 GMT  
		Size: 102.6 MB (102635870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507802eead3039e4acb9f4416ca012946579d7aa17466a2c6d4994371b0f33ab`  
		Last Modified: Fri, 08 Oct 2021 01:48:36 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.13` - linux; s390x

```console
$ docker pull golang@sha256:2222ce1b78f386c8ade5703ac06a3d438d0287ca79a09866cf467b0f00993ab1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110470130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8fb47d9cbe8a39626b2968f9694bc9d7b0152cbaa6524c3d0956f47f144b2df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 01 Sep 2021 01:15:21 GMT
ADD file:def74c9e73d87d3c8b94cc0200f2723aea3a7462f8d2e0852db9da25c19855ac in / 
# Wed, 01 Sep 2021 01:15:22 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 13:04:27 GMT
RUN apk add --no-cache ca-certificates
# Wed, 01 Sep 2021 13:04:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 13:04:28 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:44:19 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:45:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ -n "${GO386:-}" ]; then 				GO386= ./bootstrap.bash; 				export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 				"$GOROOT_BOOTSTRAP/bin/go" version; 			fi; 			./make.bash; 			if [ -n "${GO386:-}" ]; then 				rm -rf "$GOROOT_BOOTSTRAP"; 			fi; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:45:55 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:45:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:45:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:45:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1d78e8a87395f597d24b8eb78423ccdcfd404846906154e15aea8be9541c3ae`  
		Last Modified: Wed, 01 Sep 2021 01:16:19 GMT  
		Size: 2.6 MB (2604390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973358510553cd1c675157ef15be86e748a79c7eda003cde74d9a852137faef1`  
		Last Modified: Wed, 01 Sep 2021 13:12:19 GMT  
		Size: 281.7 KB (281710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882da03ec0d273ff242b99b9e8da7da539deef2582cf1282fb0fae935f1784e4`  
		Last Modified: Wed, 01 Sep 2021 13:12:19 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d65772aeb4bb0d5d6ae8f5096ef987f54e5902c066442ceb3c2af6e48b028c`  
		Last Modified: Thu, 04 Nov 2021 20:52:40 GMT  
		Size: 107.6 MB (107583722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960e064211e080a09b0e22b20cc5a3a62e0d58a24cca1c80c63266bbdaa195d3`  
		Last Modified: Thu, 04 Nov 2021 20:52:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

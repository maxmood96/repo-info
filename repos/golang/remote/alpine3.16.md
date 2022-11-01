## `golang:alpine3.16`

```console
$ docker pull golang@sha256:8558ae624304387d18694b9ea065cc9813dd4f7f9bd5073edb237541f2d0561b
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

### `golang:alpine3.16` - linux; amd64

```console
$ docker pull golang@sha256:4e2a54594cfe7002a98c483c28f6f3a78e5c7f4010c355a8cf960292a3fdecfe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125366669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e31dcd72d8f194de8fbe04ac193fbf5b34b655480e36e3641d828145bf67517`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 21:16:53 GMT
RUN apk add --no-cache ca-certificates
# Thu, 06 Oct 2022 21:16:53 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 06 Oct 2022 21:16:53 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 19:20:19 GMT
ENV GOLANG_VERSION=1.19.3
# Tue, 01 Nov 2022 19:21:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.3.src.tar.gz'; 		sha256='18ac263e39210bcf68d85f4370e97fb1734166995a1f63fb38b4f6e07d90d212'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 01 Nov 2022 19:21:57 GMT
ENV GOPATH=/go
# Tue, 01 Nov 2022 19:21:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 19:21:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Nov 2022 19:21:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4583459ba0371c715f926a9bbd37a9dae909234f4b898220160425131eb53bd4`  
		Last Modified: Thu, 06 Oct 2022 21:24:52 GMT  
		Size: 284.7 KB (284734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c1e223e6f2123b855e0c95898eba50cb6a055881ba9023527c0a361761c1cf`  
		Last Modified: Thu, 06 Oct 2022 21:24:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbef1b99e503551b709afdb24ef66954c0792f99d76bb0018afd3a65a1347b5b`  
		Last Modified: Tue, 01 Nov 2022 19:30:19 GMT  
		Size: 122.3 MB (122275572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99825e86aac9391fd3d709522864ff3282479450067b8431df9c4f9e4da4da1`  
		Last Modified: Tue, 01 Nov 2022 19:30:03 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.16` - linux; arm variant v6

```console
$ docker pull golang@sha256:233c360a32cef65bdf6a82c23606ef42e240e77bc6854a59d9e214e11718aabf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121531978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac1f520cccddadc2d639d9d882924ec9f75e667c2654fd87f30fa75f5bde4ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Tue, 01 Nov 2022 18:49:34 GMT
RUN apk add --no-cache ca-certificates
# Tue, 01 Nov 2022 18:49:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Nov 2022 18:49:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:49:35 GMT
ENV GOLANG_VERSION=1.19.3
# Tue, 01 Nov 2022 18:51:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.3.src.tar.gz'; 		sha256='18ac263e39210bcf68d85f4370e97fb1734166995a1f63fb38b4f6e07d90d212'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 01 Nov 2022 18:51:57 GMT
ENV GOPATH=/go
# Tue, 01 Nov 2022 18:51:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:51:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Nov 2022 18:51:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e34adf14e74afbe714188593430596566b859daec67932063af22ae26cfb41`  
		Last Modified: Tue, 01 Nov 2022 18:59:56 GMT  
		Size: 284.6 KB (284604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30829221241bb1a4c4b78ced30216bd6e772290df6d02b43de82ec13847f2ea`  
		Last Modified: Tue, 01 Nov 2022 18:59:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5175fa50505ed8e1ebb1cc778186a5571aceaf68880fb7f30ce0a002543fde16`  
		Last Modified: Tue, 01 Nov 2022 19:00:18 GMT  
		Size: 118.6 MB (118633129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9462914fb6be31fa7883e2ac24e0b90c77b0dd01eed92e5eb2717d2d58757a21`  
		Last Modified: Tue, 01 Nov 2022 18:59:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.16` - linux; arm variant v7

```console
$ docker pull golang@sha256:71a80cd01b5cbcece40308dd330612e2089a92dc0c8b9c8b75bd003776d71c92
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121096096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7b0535e50b1a90695e570d5d662dec29c2244be30968d7f44c468202db659e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Thu, 27 Oct 2022 03:11:14 GMT
RUN apk add --no-cache ca-certificates
# Thu, 27 Oct 2022 03:11:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 27 Oct 2022 03:11:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:58:35 GMT
ENV GOLANG_VERSION=1.19.3
# Tue, 01 Nov 2022 19:00:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.3.src.tar.gz'; 		sha256='18ac263e39210bcf68d85f4370e97fb1734166995a1f63fb38b4f6e07d90d212'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 01 Nov 2022 19:00:36 GMT
ENV GOPATH=/go
# Tue, 01 Nov 2022 19:00:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 19:00:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Nov 2022 19:00:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb4eb882dd734293a28e32a55182efac09a590954d1c7e0ac4e9afd668b950f`  
		Last Modified: Thu, 27 Oct 2022 03:23:31 GMT  
		Size: 283.8 KB (283751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62601eba0f2135ba01bd7632b6cd5858fd87c654ebbd7aa446022efda221518`  
		Last Modified: Thu, 27 Oct 2022 03:23:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61f8cf932723cb79c6511c7a4565c26fc3c1a8b195b63a1b4f27567664469b8`  
		Last Modified: Tue, 01 Nov 2022 19:11:07 GMT  
		Size: 118.4 MB (118395001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06295a7c5807cf45167f1a47e93084873628c3417ae38bd41c276b71ba1c46ab`  
		Last Modified: Tue, 01 Nov 2022 19:10:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.16` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c1b7c8fb2603c387a668768f4a7fda4c2adb077c00a97b596ff6569f7a4c20ae
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119829428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cda4629debea4c0b45ed767dc2d8c97e6c8dcaae484e6d3985714055dc17ae5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Wed, 26 Oct 2022 08:09:57 GMT
RUN apk add --no-cache ca-certificates
# Wed, 26 Oct 2022 08:09:58 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 26 Oct 2022 08:09:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:40:17 GMT
ENV GOLANG_VERSION=1.19.3
# Tue, 01 Nov 2022 18:41:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.3.src.tar.gz'; 		sha256='18ac263e39210bcf68d85f4370e97fb1734166995a1f63fb38b4f6e07d90d212'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 01 Nov 2022 18:41:34 GMT
ENV GOPATH=/go
# Tue, 01 Nov 2022 18:41:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:41:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Nov 2022 18:41:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d82f9e3411d2eff49049d09ae871e53b96a0cc7dd335883f1fec28c43f9c86`  
		Last Modified: Wed, 26 Oct 2022 08:17:16 GMT  
		Size: 284.7 KB (284723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e169736571560c1a3278f9971532d55ddc4abfaef12e8c54c05f4644445d5520`  
		Last Modified: Wed, 26 Oct 2022 08:17:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc530f9a61e7c0e16b1cb3d48b70136b625cf624976acc638b9d6aef5525995`  
		Last Modified: Tue, 01 Nov 2022 18:48:07 GMT  
		Size: 116.8 MB (116836732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562d55c2123be45d40bfd4dd4dea65161ad3d83b50153de3cc0b63ec7a061f4b`  
		Last Modified: Tue, 01 Nov 2022 18:47:54 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.16` - linux; 386

```console
$ docker pull golang@sha256:7fc967f451ffd370b66049741b1a185dadade6e4850e6df7806f2c091c1d11d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125304721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01836a4b623ddf19cfc582526bf022e06db32a935cec554d7a59cccf0e2edddb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:03:09 GMT
RUN apk add --no-cache ca-certificates
# Thu, 06 Oct 2022 20:03:10 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 06 Oct 2022 20:03:11 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:39:37 GMT
ENV GOLANG_VERSION=1.19.3
# Tue, 01 Nov 2022 18:41:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.3.src.tar.gz'; 		sha256='18ac263e39210bcf68d85f4370e97fb1734166995a1f63fb38b4f6e07d90d212'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 01 Nov 2022 18:41:29 GMT
ENV GOPATH=/go
# Tue, 01 Nov 2022 18:41:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:41:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Nov 2022 18:41:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819ebac4c94521695651b1d165df9b6de5634219e8587fec39f818d8e6f4a820`  
		Last Modified: Thu, 06 Oct 2022 20:12:44 GMT  
		Size: 285.0 KB (284966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871ea3c49cd1feaf9e420d414e8676417e15f79d306b2853548dac73163bba43`  
		Last Modified: Thu, 06 Oct 2022 20:12:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b92396b12c553ae3545d7c7a04f607a8637bbb97c4b04b39aa1c2e452af02`  
		Last Modified: Tue, 01 Nov 2022 18:51:08 GMT  
		Size: 122.2 MB (122212354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90baa0baa2bcefc21fbd9de9e786ab8143553ad4bcf5c0177f04c82faeccc96`  
		Last Modified: Tue, 01 Nov 2022 18:50:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.16` - linux; ppc64le

```console
$ docker pull golang@sha256:a014cb8f097206fe40fb42810a0dc21ae33ca2cbb1a3f251b9d972c8ba58fd40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120328454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fefd636ae894b6f7c014e0f4d6999b6eab2422a891178fff81a0f47a5dac957`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:26:01 GMT
RUN apk add --no-cache ca-certificates
# Thu, 06 Oct 2022 20:26:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 06 Oct 2022 20:26:02 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 19:17:13 GMT
ENV GOLANG_VERSION=1.19.3
# Tue, 01 Nov 2022 19:19:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.3.src.tar.gz'; 		sha256='18ac263e39210bcf68d85f4370e97fb1734166995a1f63fb38b4f6e07d90d212'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 01 Nov 2022 19:20:03 GMT
ENV GOPATH=/go
# Tue, 01 Nov 2022 19:20:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 19:20:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Nov 2022 19:20:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36899d7325c2c25a7d8e61ef33bb1e93b83f811f462e9ddad81c86df87b0685`  
		Last Modified: Thu, 06 Oct 2022 20:39:18 GMT  
		Size: 286.7 KB (286747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9309524edda98df2abd6704c6f56004422a28b63364f028763ea000fc32d6eca`  
		Last Modified: Thu, 06 Oct 2022 20:39:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b608654249afe5c44e2b3f100f6b333302506cd24adc46afa3302bb03ff96e`  
		Last Modified: Tue, 01 Nov 2022 19:31:59 GMT  
		Size: 117.2 MB (117238077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93311758f4ff1a16fa50dab5c51c12dd47a1920496e07493f5452c97e24eff9c`  
		Last Modified: Tue, 01 Nov 2022 19:31:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.16` - linux; s390x

```console
$ docker pull golang@sha256:d00a72c2255cf22972ce257b01b305bb1f245541198b84633647b29022ff9d7c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123605335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2795304a1e17d87a59a6d45892d895c516a3baf3e42d61bf2e07577312aef37`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:16:09 GMT
RUN apk add --no-cache ca-certificates
# Thu, 06 Oct 2022 20:16:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 06 Oct 2022 20:16:11 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:43:10 GMT
ENV GOLANG_VERSION=1.19.3
# Tue, 01 Nov 2022 18:46:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.3.src.tar.gz'; 		sha256='18ac263e39210bcf68d85f4370e97fb1734166995a1f63fb38b4f6e07d90d212'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 01 Nov 2022 18:47:10 GMT
ENV GOPATH=/go
# Tue, 01 Nov 2022 18:47:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Nov 2022 18:47:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Nov 2022 18:47:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d31ae2e1f77c70a25e9cbeea435b4ab68149a4e17f9d4668768da8dd5ac68a`  
		Last Modified: Thu, 06 Oct 2022 20:26:52 GMT  
		Size: 285.0 KB (284954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2788e533105e3c00ed84523a8f99d7947c0bb8b12932018a3081ecc29964605`  
		Last Modified: Thu, 06 Oct 2022 20:26:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a12f83dfb1b48c3152a859b9b55b4483128b0be37e4877271cbd453b23fb43`  
		Last Modified: Tue, 01 Nov 2022 19:02:36 GMT  
		Size: 120.7 MB (120729474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e663873bb0a71689aee0be3ce5f4195e0b573039585fcc3182fe189e8e8fe05`  
		Last Modified: Tue, 01 Nov 2022 19:02:21 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

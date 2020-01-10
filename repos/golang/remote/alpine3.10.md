## `golang:alpine3.10`

```console
$ docker pull golang@sha256:106f88d92ef80c6f7b9f9eb22ae45b5d59d8994f0570a56cf7fe714d73e8a2ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `golang:alpine3.10` - linux; amd64

```console
$ docker pull golang@sha256:23a8fd604f8d1e60f8c372e088076aaeef5d2eb182caf6e0717dfc500417e1cb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129969702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fe0488e74ede7484140a81ccf57997372b4b7b3faef3a03690db4c3164dfac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 18:18:34 GMT
RUN apk add --no-cache 		ca-certificates
# Mon, 21 Oct 2019 18:18:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 05 Dec 2019 22:20:17 GMT
ENV GOLANG_VERSION=1.13.5
# Thu, 26 Dec 2019 21:31:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '27d356e2a0b30d9983b60a788cf225da5f914066b37a6b4f69d457ba55a626ff *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 26 Dec 2019 21:31:31 GMT
ENV GOPATH=/go
# Thu, 26 Dec 2019 21:31:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Dec 2019 21:31:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 26 Dec 2019 21:31:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef94372a977c02d425f12c8cbda5416e372b7a869a6c2b20342c589dba3eae5`  
		Last Modified: Mon, 21 Oct 2019 18:20:06 GMT  
		Size: 301.7 KB (301722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec62c064901392a6722bb47a377c01a381f4482b1ce094b6d28682b6b6279fd`  
		Last Modified: Mon, 21 Oct 2019 18:20:05 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e7d6ed9e7bc8ab978315026952018a0f21663d0b267f853165f8af5cc67450`  
		Last Modified: Thu, 26 Dec 2019 21:38:27 GMT  
		Size: 126.9 MB (126880566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53cbe00f74456f8ed71034811a0698c78a94aba1c0a6c01634f76c990fb9e701`  
		Last Modified: Thu, 26 Dec 2019 21:38:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.10` - linux; arm variant v6

```console
$ docker pull golang@sha256:8f55d8afd76853e7da25d3174adbaea91c6a0ee33526a941dd9a191aa9fe6f99
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125641671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cc53db06cc110d5edc0c1abb14852306e524161419996dd4da2bad0130653b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 21 Oct 2019 16:56:02 GMT
ADD file:d3c7d938a78143f106a6a467ce23b599198e041220e661e5326ba91054c353ef in / 
# Mon, 21 Oct 2019 16:56:04 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 16:57:30 GMT
RUN apk add --no-cache 		ca-certificates
# Mon, 21 Oct 2019 16:57:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 09 Jan 2020 23:57:35 GMT
ENV GOLANG_VERSION=1.13.6
# Fri, 10 Jan 2020 00:00:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'aae5be954bdc40bcf8006eb77e8d8a5dde412722bc8effcdaf9772620d06420c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 10 Jan 2020 00:00:29 GMT
ENV GOPATH=/go
# Fri, 10 Jan 2020 00:00:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2020 00:01:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 10 Jan 2020 00:01:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ecf664be551d26dcd221b7387283cdcc54f46c6789700d037fa3cd0c297f8645`  
		Last Modified: Mon, 21 Oct 2019 16:56:34 GMT  
		Size: 2.6 MB (2571309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4d69e9c49d276dea623c6b05666752b107b3ae7e7fb31faa84c28a89270f7a`  
		Last Modified: Mon, 21 Oct 2019 17:01:55 GMT  
		Size: 302.0 KB (302014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2665e2d25121195adad669aa3560768041a5fd3998c859fd6b324c11aac41e3f`  
		Last Modified: Mon, 21 Oct 2019 17:01:53 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665d86f55b4585a226b7ebbc6a3aee02a1b30ccc8708d36ec5a4b8ce1d27b676`  
		Last Modified: Fri, 10 Jan 2020 00:09:21 GMT  
		Size: 122.8 MB (122768038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d594ba4cde3136ca1ffe12b386320df16e606cc5927df613a6edba47f64e3da0`  
		Last Modified: Fri, 10 Jan 2020 00:08:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.10` - linux; arm variant v7

```console
$ docker pull golang@sha256:0ac5e3a6b5385932b79ec053719030429282385a96b086a15ae61c0995374c03
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125076503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d60d58ad2e7f97f1b3535e621e895208e74b407dd51e92810114e72a63de42b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 21 Oct 2019 18:15:18 GMT
ADD file:6b2893134302eabeb80e356fc4e5a29d9cd442362c382b3504688c014a734bb9 in / 
# Mon, 21 Oct 2019 18:15:31 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 18:52:36 GMT
RUN apk add --no-cache 		ca-certificates
# Mon, 21 Oct 2019 18:52:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Jan 2020 00:03:26 GMT
ENV GOLANG_VERSION=1.13.6
# Fri, 10 Jan 2020 00:05:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'aae5be954bdc40bcf8006eb77e8d8a5dde412722bc8effcdaf9772620d06420c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 10 Jan 2020 00:05:53 GMT
ENV GOPATH=/go
# Fri, 10 Jan 2020 00:05:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2020 00:05:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 10 Jan 2020 00:05:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:99fc70ac0b64db67086f98ceb3942600816eed98046abd6be5ad66f4614a9ca2`  
		Last Modified: Mon, 21 Oct 2019 18:16:16 GMT  
		Size: 2.4 MB (2378437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a417fcb3850a7455af93e93458e59d7f95bdbb16f1857e99d901142c8d2095eb`  
		Last Modified: Mon, 21 Oct 2019 18:54:57 GMT  
		Size: 300.9 KB (300946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a6ddf38e7cc67bd2f493ebb023839b57b404cc2299f2326c1771c3d559deda`  
		Last Modified: Mon, 21 Oct 2019 18:54:53 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5eb8ed59e5a34edb65250b29e73a484793a020fda072c51e385a60124cf0df7`  
		Last Modified: Fri, 10 Jan 2020 00:20:06 GMT  
		Size: 122.4 MB (122396812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab0ae761928b98480546e690b49441156720ca8a686951f1cbd29223f8c056`  
		Last Modified: Fri, 10 Jan 2020 00:17:41 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.10` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f946593b41ead9478d61fa683cc428a148f8bb90ad3c9238786fb6c788d0f1fe
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124243793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200c197d98c2155796be89d275f14fa2aaa393ab1ef86d7998aa1d286441e1ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 18:59:13 GMT
RUN apk add --no-cache 		ca-certificates
# Mon, 21 Oct 2019 18:59:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Jan 2020 00:00:26 GMT
ENV GOLANG_VERSION=1.13.6
# Fri, 10 Jan 2020 00:02:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'aae5be954bdc40bcf8006eb77e8d8a5dde412722bc8effcdaf9772620d06420c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 10 Jan 2020 00:02:48 GMT
ENV GOPATH=/go
# Fri, 10 Jan 2020 00:02:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2020 00:02:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 10 Jan 2020 00:02:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d523c651118b8110a7055546123bb301485868b779462028d410ad31ce758844`  
		Last Modified: Mon, 21 Oct 2019 19:00:39 GMT  
		Size: 302.3 KB (302343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46c404896130ad49e5b0a29fef854c53e121f275ffdd3c624399291cdb710c7`  
		Last Modified: Mon, 21 Oct 2019 19:00:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df08a2573c7e78be6d9ded40e6c0161631fa1fa7752e447a128e3ecb7c61f84`  
		Last Modified: Fri, 10 Jan 2020 00:12:35 GMT  
		Size: 121.2 MB (121223364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fef9d9ddfe8c823342ac171805dcb3789ac473327342f6a7d18073b4e5e06cd`  
		Last Modified: Fri, 10 Jan 2020 00:12:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.10` - linux; 386

```console
$ docker pull golang@sha256:5af59a6be46b025bd03c63d54b8a463b47672f81fcec46756c9abb37039731fe
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.7 MB (129663864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3342579fd9c79e00654aaec4a9baa12c09f604fb1dd23c081d0db773eaeadd99`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 21 Oct 2019 16:46:04 GMT
ADD file:dd3b3676fd9c1e0983ade68242b9b9ac5c477f3e4bfc97c2e78fd5db93a441c9 in / 
# Mon, 21 Oct 2019 16:46:04 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 17:41:33 GMT
RUN apk add --no-cache 		ca-certificates
# Mon, 21 Oct 2019 17:41:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 09 Jan 2020 23:42:10 GMT
ENV GOLANG_VERSION=1.13.6
# Thu, 09 Jan 2020 23:50:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'aae5be954bdc40bcf8006eb77e8d8a5dde412722bc8effcdaf9772620d06420c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 09 Jan 2020 23:50:02 GMT
ENV GOPATH=/go
# Thu, 09 Jan 2020 23:50:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Jan 2020 23:50:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 09 Jan 2020 23:50:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f913bd05bf684aaa4bc173d73cfbb58abb45587962d74f0aa71df36b6b489def`  
		Last Modified: Mon, 21 Oct 2019 16:46:25 GMT  
		Size: 2.8 MB (2785939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed468e91bdc7b0ff88c15190e8b33cddcff4ffc087d4246427e757e240eaa4e`  
		Last Modified: Mon, 21 Oct 2019 17:56:20 GMT  
		Size: 302.3 KB (302321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c287d4a5f78facdfedc09c2f6649db22aa7e0443288ec2c059a61ae6628e2`  
		Last Modified: Mon, 21 Oct 2019 17:56:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e026670192c960138e50dce728f38fa772c559e55b915e396caa7c861ca6a1ee`  
		Last Modified: Fri, 10 Jan 2020 00:00:27 GMT  
		Size: 126.6 MB (126575325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088764b52febbaa5392d77f424e9dcc97115ff567f2642bbf7c9834b5afb24b2`  
		Last Modified: Thu, 09 Jan 2020 23:58:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.10` - linux; ppc64le

```console
$ docker pull golang@sha256:4d5a19d83b2efe7b0488a4573389ef6968b72a728c849cddefc8993a2fd8850a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123092850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52374c232446cf34c7d727c4d46cf3378945e96146fc7cb1a876ccaf767400d2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 21 Oct 2019 17:52:55 GMT
ADD file:11a2dd0058b1642e9ee52239d03223819a53ca346fd42826eead7729c50e1257 in / 
# Mon, 21 Oct 2019 17:53:00 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 18:51:40 GMT
RUN apk add --no-cache 		ca-certificates
# Mon, 21 Oct 2019 18:51:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 05 Dec 2019 22:18:53 GMT
ENV GOLANG_VERSION=1.13.5
# Thu, 26 Dec 2019 21:48:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '27d356e2a0b30d9983b60a788cf225da5f914066b37a6b4f69d457ba55a626ff *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 26 Dec 2019 21:48:41 GMT
ENV GOPATH=/go
# Thu, 26 Dec 2019 21:48:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Dec 2019 21:48:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 26 Dec 2019 21:48:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd18d16ea896a0f0eb99be52a9722ffae9a5ac35cf28cb8b96f589352f8e71d6`  
		Last Modified: Mon, 21 Oct 2019 17:53:53 GMT  
		Size: 2.8 MB (2808504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d1409133b45bed937b154539e879dcba8c61a42497bad2df2f2d74a5fa1d6a`  
		Last Modified: Mon, 21 Oct 2019 18:57:23 GMT  
		Size: 304.5 KB (304451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3458aa07f9bf299f9ac4ae0da43afda61bf62f5c70589a15f457684d1c4ec3e7`  
		Last Modified: Mon, 21 Oct 2019 18:57:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf64ef277a11d47dc604c6a69301625fb6faf46439e9bff28b6565c889ea265`  
		Last Modified: Thu, 26 Dec 2019 22:01:20 GMT  
		Size: 120.0 MB (119979585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a4cf472a010e6ae799bd442405b884646ae607f816db37b0a01fcc776d56bb`  
		Last Modified: Thu, 26 Dec 2019 22:00:01 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.10` - linux; s390x

```console
$ docker pull golang@sha256:579dbe11b9b923f54ae5b128e2395500a961aad9b737b775be3feae1b45fce68
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.7 MB (129737448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3668e9bd4861182bfa3edf90c704d2ad2e20a312e466539fd27db720c83614`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 21 Oct 2019 16:47:28 GMT
ADD file:49020543846e4f93b34d71c0e4234ade7bd6dde3f45cb73784aa73ce0522c8bc in / 
# Mon, 21 Oct 2019 16:47:29 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 17:22:03 GMT
RUN apk add --no-cache 		ca-certificates
# Mon, 21 Oct 2019 17:22:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 09 Jan 2020 23:45:47 GMT
ENV GOLANG_VERSION=1.13.6
# Thu, 09 Jan 2020 23:46:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'aae5be954bdc40bcf8006eb77e8d8a5dde412722bc8effcdaf9772620d06420c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 09 Jan 2020 23:46:57 GMT
ENV GOPATH=/go
# Thu, 09 Jan 2020 23:46:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Jan 2020 23:46:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 09 Jan 2020 23:46:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb7172052a60e640810f01efff381654bf9ed44082461455cfcc6306d192d541`  
		Last Modified: Mon, 21 Oct 2019 16:48:40 GMT  
		Size: 2.6 MB (2573587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756641a81b92ce47e818c92880b4e1a144f10ceebe1934f176587bf3980e94ea`  
		Last Modified: Mon, 21 Oct 2019 17:34:27 GMT  
		Size: 302.4 KB (302371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30abe3a6a40d80e37f3089718a7b0610ccbbe5e4a45f4034a9a9c322d74585c8`  
		Last Modified: Mon, 21 Oct 2019 17:34:27 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74a70e13c0f8bf4319bec6c540ae8b97aafee13057ae57ceaadea50d637f6d8`  
		Last Modified: Thu, 09 Jan 2020 23:52:04 GMT  
		Size: 126.9 MB (126861210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779739b9bd53737a0b1832fa403513b29265e6e237a4a71d98e1ef4e804aff93`  
		Last Modified: Thu, 09 Jan 2020 23:51:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

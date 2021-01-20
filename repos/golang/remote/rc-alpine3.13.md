## `golang:rc-alpine3.13`

```console
$ docker pull golang@sha256:c5b1f3636e2e915a0ac3faf4213bf4ee3b228e76f2a0d9a5210b77929d64e46b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `golang:rc-alpine3.13` - linux; amd64

```console
$ docker pull golang@sha256:f3468ff7217e52a2c19cac102ab13a4e1557c6da6c512a25eefe5a7165dd53a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111454803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88467031de9e150408dc9c51d466c0cc418c8287af31ea7e2f44ce3e04422693`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 15 Jan 2021 02:23:51 GMT
ADD file:edbe213ae0c825a5bfbe569928cf20f683f334f93a093ccd0a3a014b7428e760 in / 
# Fri, 15 Jan 2021 02:23:51 GMT
CMD ["/bin/sh"]
# Tue, 19 Jan 2021 23:19:46 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 19 Jan 2021 23:19:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 19 Jan 2021 23:19:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jan 2021 23:19:47 GMT
ENV GOLANG_VERSION=1.16beta1
# Tue, 19 Jan 2021 23:22:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16beta1.src.tar.gz'; 	sha256='48e032c8cf71af4dc8119a29ee829c4fbd5265e32fd012564d4a70bb207695c1'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 19 Jan 2021 23:22:09 GMT
ENV GOPATH=/go
# Tue, 19 Jan 2021 23:22:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jan 2021 23:22:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 19 Jan 2021 23:22:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:596ba82af5aaa3e2fd9d6f955b8b94f0744a2b60710e3c243ba3e4a467f051d1`  
		Last Modified: Fri, 15 Jan 2021 02:08:10 GMT  
		Size: 2.8 MB (2810825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344f2904b0c622eb3da9e7d3d987e8391c91c10971edb21ff5bef3c2745e15d1`  
		Last Modified: Tue, 19 Jan 2021 23:28:32 GMT  
		Size: 281.2 KB (281197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bda26d9fa150845bfd0e1a61dd37c343746f2f08d5ec7edc4b289d09e8eca6`  
		Last Modified: Tue, 19 Jan 2021 23:28:32 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bc5beb9e0d8c9c315d18e29c5753ecb96742520be4635f07166d6854afc26d`  
		Last Modified: Tue, 19 Jan 2021 23:28:50 GMT  
		Size: 108.4 MB (108362503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f6c28db26dcb2ac4278f9b8bf71af4d4c4d03e365e931825a01f02decad763`  
		Last Modified: Tue, 19 Jan 2021 23:28:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-alpine3.13` - linux; arm variant v6

```console
$ docker pull golang@sha256:dee034953596ed932128c3fb4dd9d271e584211984d2c353d496f9e4eada4a3f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107510393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54f991f76cfdafb2492f1e4b38ce48b22b5c5ee634182c88518fcadac5ced12`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 15 Jan 2021 01:51:19 GMT
ADD file:f2665ccfd90cf53580dc87c3e57db7c223147c686554b1d6e3fc166cce818b3e in / 
# Fri, 15 Jan 2021 01:51:20 GMT
CMD ["/bin/sh"]
# Tue, 19 Jan 2021 22:51:00 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 19 Jan 2021 22:51:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 19 Jan 2021 22:51:03 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jan 2021 22:51:04 GMT
ENV GOLANG_VERSION=1.16beta1
# Tue, 19 Jan 2021 22:54:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16beta1.src.tar.gz'; 	sha256='48e032c8cf71af4dc8119a29ee829c4fbd5265e32fd012564d4a70bb207695c1'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 19 Jan 2021 22:54:15 GMT
ENV GOPATH=/go
# Tue, 19 Jan 2021 22:54:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jan 2021 22:54:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 19 Jan 2021 22:54:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b550170d5d44558603032e2371fa7a2fb3575b38b2c64ad8be4ab798bcad44d3`  
		Last Modified: Fri, 15 Jan 2021 01:52:01 GMT  
		Size: 2.6 MB (2621576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3e8887f9a7e4e34c54b9349e5b66afa3d18cb1a5a11305ddebd459b35aa2dc`  
		Last Modified: Tue, 19 Jan 2021 23:02:00 GMT  
		Size: 281.4 KB (281397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6657420542dbc9d4a0000b6b2938e9dfa54a445a19ce937442a1e9358fc05d`  
		Last Modified: Tue, 19 Jan 2021 23:02:01 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900d2360807c263358fd7e98a1ed0bbb1658f13459f9dad7cfaa214ab825f9d1`  
		Last Modified: Tue, 19 Jan 2021 23:02:34 GMT  
		Size: 104.6 MB (104607111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fc55bbcbcfaac180b6352d6f9df4251166a25a457cb5e0d5c9259038c5cab0`  
		Last Modified: Tue, 19 Jan 2021 23:01:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-alpine3.13` - linux; arm variant v7

```console
$ docker pull golang@sha256:e4174fb9182afef35897ca36ff7065f78b1495fc7ebcb18f704bce02d8e44c38
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107081354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83dc0ef666694aa9cdd23549749977e5b2ae48093feabc70d7452f94a916164e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 15 Jan 2021 01:58:27 GMT
ADD file:718d7c24a8d6ff0feb2843cf8c3ca4b7ef1fb523a45dea568404259a7b4e6f10 in / 
# Fri, 15 Jan 2021 01:58:29 GMT
CMD ["/bin/sh"]
# Tue, 19 Jan 2021 22:59:15 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 19 Jan 2021 22:59:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 19 Jan 2021 22:59:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jan 2021 22:59:19 GMT
ENV GOLANG_VERSION=1.16beta1
# Tue, 19 Jan 2021 23:01:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16beta1.src.tar.gz'; 	sha256='48e032c8cf71af4dc8119a29ee829c4fbd5265e32fd012564d4a70bb207695c1'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 19 Jan 2021 23:01:53 GMT
ENV GOPATH=/go
# Tue, 19 Jan 2021 23:01:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jan 2021 23:01:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 19 Jan 2021 23:01:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0f34ce5da94097b8c334f6b2065a010aced9855c3532e4462e9bd1b0a4c4b3f6`  
		Last Modified: Fri, 15 Jan 2021 01:59:13 GMT  
		Size: 2.4 MB (2422744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7080c4e9b37c27695262d3a55b2123a6aa03ea7bc84325acdb59d191cbf8c0`  
		Last Modified: Tue, 19 Jan 2021 23:09:25 GMT  
		Size: 280.5 KB (280535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa4c313f1145eca236e84580c343eb89f2ce209bcd337db611f572726b2a165`  
		Last Modified: Tue, 19 Jan 2021 23:09:28 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483e55fc20123408204f6048895ecdd77651c78f843ec7286a16a170077a2739`  
		Last Modified: Tue, 19 Jan 2021 23:09:59 GMT  
		Size: 104.4 MB (104377767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd4380712af14cf67b2cd992b0a6859cdc948e3c85a848dcfb2076cdbb6d7f8`  
		Last Modified: Tue, 19 Jan 2021 23:09:25 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:3a80e755bfc98ccb93af8a3ab31a5808ea6e2e6509f73f329bc4a1e7034d647e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106757988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1627e1c780636e9c6ce92a87fe4635a770601139a3c923a5dafe9959245e631e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 15 Jan 2021 01:47:51 GMT
ADD file:95be2cec37537b3fd70aeb1d4eb3479fc4a56b00ad7180788ddd7fa772ca65e7 in / 
# Fri, 15 Jan 2021 01:47:52 GMT
CMD ["/bin/sh"]
# Tue, 19 Jan 2021 22:40:00 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 19 Jan 2021 22:40:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 19 Jan 2021 22:40:03 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jan 2021 22:40:03 GMT
ENV GOLANG_VERSION=1.16beta1
# Tue, 19 Jan 2021 22:42:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16beta1.src.tar.gz'; 	sha256='48e032c8cf71af4dc8119a29ee829c4fbd5265e32fd012564d4a70bb207695c1'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 19 Jan 2021 22:42:19 GMT
ENV GOPATH=/go
# Tue, 19 Jan 2021 22:42:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jan 2021 22:42:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 19 Jan 2021 22:42:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:30d5333d20a68dd6ea3689e2c5692d7071f2d68e72c06f0b3b4c7e213df454e2`  
		Last Modified: Fri, 15 Jan 2021 01:48:29 GMT  
		Size: 2.7 MB (2710904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07698665516ca7cdecf151fd81dd0e98d0d8ed7aa69b231641030fa1a0e0e442`  
		Last Modified: Tue, 19 Jan 2021 22:48:55 GMT  
		Size: 281.5 KB (281493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c260f2b2e88e3fcae41f071b37c98ff375604141deda965426161ccfa9c678`  
		Last Modified: Tue, 19 Jan 2021 22:48:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74f968492529f91b1a8225e092d10e1db2689af622a34c7b1cc5ca3223944ea`  
		Last Modified: Tue, 19 Jan 2021 22:49:25 GMT  
		Size: 103.8 MB (103765280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242ca7a49020e32cb648321e7989ad77abef69f7cecc7e913053d817dca5489b`  
		Last Modified: Tue, 19 Jan 2021 22:48:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-alpine3.13` - linux; ppc64le

```console
$ docker pull golang@sha256:3bfb2f5f53441cc4c0568db0387d262aa9b0418cc138ff678094c505f7d68f1b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105287421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b07e89f53a8cb77d7a275f86f6264abc445eeb219a31e840ed92841f297c37c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 15 Jan 2021 02:41:43 GMT
ADD file:137e8f98476d5dceaeb2e8359f50eb818dee4c327e4492d16e87fb27d40aa891 in / 
# Fri, 15 Jan 2021 02:41:46 GMT
CMD ["/bin/sh"]
# Tue, 19 Jan 2021 23:18:08 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 19 Jan 2021 23:18:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 19 Jan 2021 23:18:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jan 2021 23:18:22 GMT
ENV GOLANG_VERSION=1.16beta1
# Tue, 19 Jan 2021 23:20:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16beta1.src.tar.gz'; 	sha256='48e032c8cf71af4dc8119a29ee829c4fbd5265e32fd012564d4a70bb207695c1'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 19 Jan 2021 23:20:29 GMT
ENV GOPATH=/go
# Tue, 19 Jan 2021 23:20:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jan 2021 23:20:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 19 Jan 2021 23:20:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cb0f06c26ffdc2117b9a3467f79e69cdf8d9c677a3c0bacabc8a694a9fe303a8`  
		Last Modified: Fri, 15 Jan 2021 02:42:19 GMT  
		Size: 2.8 MB (2812389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20435be1533582e913efc1cd947f7cf8ac91cf4d8c9336e9c99f2a4ca166f5f`  
		Last Modified: Tue, 19 Jan 2021 23:27:09 GMT  
		Size: 283.4 KB (283394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5233d7d81be74584fbfc275e26c09223a4751ec2addf75517f449df662c7fa`  
		Last Modified: Tue, 19 Jan 2021 23:27:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2f9db92c9f6f433e0f42fe414ec42c1fe2199c53c72e6438f7c62a2a3f7039`  
		Last Modified: Tue, 19 Jan 2021 23:27:29 GMT  
		Size: 102.2 MB (102191330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9937debeb4b4ac21c6808b9a2aeee5479ab51b7f42f99281aef4ff21ff16f9c9`  
		Last Modified: Tue, 19 Jan 2021 23:27:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-alpine3.13` - linux; s390x

```console
$ docker pull golang@sha256:de8ded82f77406dbeb6b9e046363d6f050d47246be583d3229ef0f13576921d8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110359344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b571478ac0b18783ce9ec4a2e0a742f8cfdcc326fcd43ea51a0a79e1a89d549c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 15 Jan 2021 01:51:34 GMT
ADD file:3ba807ca8ed73ca14224dd26a883f2399031fa32430f035cc5ae97b5e6db0ca7 in / 
# Fri, 15 Jan 2021 01:51:35 GMT
CMD ["/bin/sh"]
# Tue, 19 Jan 2021 22:41:50 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 19 Jan 2021 22:41:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 19 Jan 2021 22:41:52 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jan 2021 22:41:53 GMT
ENV GOLANG_VERSION=1.16beta1
# Tue, 19 Jan 2021 22:44:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16beta1.src.tar.gz'; 	sha256='48e032c8cf71af4dc8119a29ee829c4fbd5265e32fd012564d4a70bb207695c1'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 19 Jan 2021 22:44:57 GMT
ENV GOPATH=/go
# Tue, 19 Jan 2021 22:44:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jan 2021 22:44:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 19 Jan 2021 22:44:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3997176601fb5d5ac06922718668ede4acac00a5c0daef8a9099fd76ce93047f`  
		Last Modified: Fri, 15 Jan 2021 01:52:40 GMT  
		Size: 2.6 MB (2601720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb31ae3a2ea55d5765f99a57baf87f25fd69a463051d14aa6cf1a57eff925c1`  
		Last Modified: Tue, 19 Jan 2021 22:51:03 GMT  
		Size: 281.7 KB (281708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e959eca31141e89cb3b94dd613ad5a59a1969778e6ecf3f51d69e3d9eb193b3f`  
		Last Modified: Tue, 19 Jan 2021 22:51:03 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bced13e4180425c940dd741d5acaae371415472ff7cfa556286db0cfc3e952f1`  
		Last Modified: Tue, 19 Jan 2021 22:51:18 GMT  
		Size: 107.5 MB (107475607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da13b7d74f6c60c20f747ad2ab3a95f3c9e6b49c84f98d2e11abd06be1f021c`  
		Last Modified: Tue, 19 Jan 2021 22:49:46 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

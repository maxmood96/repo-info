## `caddy:2-builder`

```console
$ docker pull caddy@sha256:2b9027ed7b3b901ab880a0cf61ee08ad73abc257de45e161bc5a81ad4e7156a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:db7df697982aa4e88f145a10f80e7c967d3ee5d4d358889788a1913071546e3d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322794274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f459aeeb070c0235758c31ed9a327801de7388aa467764e53e342672cba0bf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:29:00 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 24 Apr 2020 14:29:01 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:29:01 GMT
ENV GOLANG_VERSION=1.14.2
# Fri, 24 Apr 2020 14:31:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '98de84e69726a66da7b4e58eac41b99cbe274d7e8906eeb8a5b7eb0aadee7f7c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 24 Apr 2020 14:31:21 GMT
ENV GOPATH=/go
# Fri, 24 Apr 2020 14:31:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2020 14:31:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 24 Apr 2020 14:31:22 GMT
WORKDIR /go
# Fri, 24 Apr 2020 22:56:31 GMT
WORKDIR /src
# Fri, 24 Apr 2020 22:56:32 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 04 May 2020 19:20:59 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Mon, 04 May 2020 19:21:00 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Mon, 04 May 2020 19:21:00 GMT
WORKDIR /src/caddy/cmd/caddy
# Mon, 04 May 2020 19:21:14 GMT
RUN go get -d ./...
# Mon, 04 May 2020 19:21:14 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Mon, 04 May 2020 19:21:15 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408f875501273f3af2a9cbff2a23e736585641e73da80dd81712518b28e7843c`  
		Last Modified: Fri, 24 Apr 2020 14:36:50 GMT  
		Size: 301.3 KB (301282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe522b08c9798748151fec9b7a908aca712cd102cfcbb8ed79d57d05b71e6cc4`  
		Last Modified: Fri, 24 Apr 2020 14:36:50 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618fff1cf170e1785ab64028237182717bc1e1287d03cf0888e424b7563ae5df`  
		Last Modified: Fri, 24 Apr 2020 14:37:17 GMT  
		Size: 132.0 MB (132009787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8b518583db0dc830a3a43c739d6cc91b7610c09d9eba918ae54b20a1dcd18c`  
		Last Modified: Fri, 24 Apr 2020 14:36:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7581717e36377b193dcae9cec5af534cec8f39f59c9bffe5eb7078fa8a8285f1`  
		Last Modified: Fri, 24 Apr 2020 22:56:58 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb722154abd62e5d5bd123de6de7e8570a1c2b311fd7fba8e422c29d38d4bb41`  
		Last Modified: Fri, 24 Apr 2020 22:56:59 GMT  
		Size: 8.2 MB (8177825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c811f2163b049a8ca302ad16c1bcc11fc76dbad41d7be306a792daaf5a42e0b2`  
		Last Modified: Mon, 04 May 2020 19:21:33 GMT  
		Size: 2.8 MB (2777485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd3ad56dcd643b994839d61853ed088efbdbf0080c97765633e13526819518e`  
		Last Modified: Mon, 04 May 2020 19:21:53 GMT  
		Size: 176.7 MB (176713544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d8fb1818ee37dd4a4968e91d5f27fcc6ead071958348cf84eb5548234bef62`  
		Last Modified: Mon, 04 May 2020 19:21:32 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2976508d22e89b43b5582902dbfd6f26063f6b7612ce470f8bca43b170f3b5a`  
		Last Modified: Mon, 04 May 2020 19:21:32 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:67ffeabbdb3a9f1cb9e2ad6cd54232dcdd34982c8385c5dd02c9ff8832abafc6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318365877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63190c4a0b594a90ad4c3da68dd98c39a7019a6864b6fa15b72ddc347514306`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:43:41 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 23 Apr 2020 17:43:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 15 May 2020 20:53:00 GMT
ENV GOLANG_VERSION=1.14.3
# Fri, 15 May 2020 21:42:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 15 May 2020 21:42:49 GMT
ENV GOPATH=/go
# Fri, 15 May 2020 21:42:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 21:42:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 15 May 2020 21:42:53 GMT
WORKDIR /go
# Fri, 15 May 2020 23:28:04 GMT
WORKDIR /src
# Fri, 15 May 2020 23:28:07 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 15 May 2020 23:28:07 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Fri, 15 May 2020 23:28:14 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 15 May 2020 23:28:15 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 15 May 2020 23:29:26 GMT
RUN go get -d ./...
# Fri, 15 May 2020 23:29:30 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Fri, 15 May 2020 23:29:31 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ace047eafbdd1d41e753db1fd1004be452f749a7de56a3d24b2614a64577f5`  
		Last Modified: Thu, 23 Apr 2020 18:03:18 GMT  
		Size: 301.6 KB (301629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d0031acb1953f56f2c2592c1c5882b29aa828d45deccabbb9a1b5483090a43`  
		Last Modified: Thu, 23 Apr 2020 18:03:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22048f6afd75ef565a9cc612911b01c67d897625b9ca36c60b894d6084696f92`  
		Last Modified: Fri, 15 May 2020 22:59:43 GMT  
		Size: 128.2 MB (128224697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b650a1fbc6e89ab4e30a8124c1986a5b57af9f767ce14247c12ab4626406211d`  
		Last Modified: Fri, 15 May 2020 22:58:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2953b4a08d70d0c5e852f46f654fb76fc4a3f4d84c10378f27537298ac4b0bc9`  
		Last Modified: Fri, 15 May 2020 23:29:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca20c0d8a5fd7c97070d7b2afbfbdf070ef8516d1444d97a7aef420012244f8`  
		Last Modified: Fri, 15 May 2020 23:29:47 GMT  
		Size: 7.8 MB (7794700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ae08a0ea808be3631e7222fe61adb555d0e0b72701058ae4c7f7e24990d8f0`  
		Last Modified: Fri, 15 May 2020 23:29:46 GMT  
		Size: 2.7 MB (2706779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4819b2bd69dec9549694cb4f3c2366750c619b6a5750ea944b035e0aa7b1e8c`  
		Last Modified: Fri, 15 May 2020 23:30:32 GMT  
		Size: 176.7 MB (176717010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b429e222d20612559d02209fa2408af52a51ad89b46a1077ca5391f01fb6f05`  
		Last Modified: Fri, 15 May 2020 23:29:45 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6052a006c556287b947a63516cf4be70b400cb52a23a9a7c55200d505394c706`  
		Last Modified: Fri, 15 May 2020 23:29:45 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:9d6434e970f35955684d4641cac3aa549b0c08f4bb862d040261536b655d456f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.0 MB (317024290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51393629ba564a6804df4ec7bca16f3196ba14ac48f47a9e12a801296e0a471`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:27:40 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 24 Apr 2020 02:27:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 May 2020 00:47:38 GMT
ENV GOLANG_VERSION=1.14.3
# Sat, 16 May 2020 01:12:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sat, 16 May 2020 01:12:52 GMT
ENV GOPATH=/go
# Sat, 16 May 2020 01:12:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 May 2020 01:12:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 16 May 2020 01:12:55 GMT
WORKDIR /go
# Sat, 16 May 2020 06:38:01 GMT
WORKDIR /src
# Sat, 16 May 2020 06:38:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 16 May 2020 06:38:05 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Sat, 16 May 2020 06:38:13 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Sat, 16 May 2020 06:38:14 GMT
WORKDIR /src/caddy/cmd/caddy
# Sat, 16 May 2020 06:39:12 GMT
RUN go get -d ./...
# Sat, 16 May 2020 06:39:20 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Sat, 16 May 2020 06:39:21 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a35d9f7887ef683587262c6f5ed88364f59775ff882c71bde03cc59f382ffd`  
		Last Modified: Fri, 24 Apr 2020 03:39:46 GMT  
		Size: 300.6 KB (300593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce21b09ea3d1107df35d9f41a664183faabfc461b8f093ab8e9a34d91e8e71b`  
		Last Modified: Fri, 24 Apr 2020 03:39:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888e8edf526a315ecceea6785f665113ffce2e1e0c8617daaf91786d53f6fb27`  
		Last Modified: Sat, 16 May 2020 01:57:54 GMT  
		Size: 127.8 MB (127843769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbf78654cd341d4acd2a92217585b18547f1b6afc166ac4334420966a2065e4`  
		Last Modified: Sat, 16 May 2020 01:57:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576e21e89111ed713cfd2dc75fe1261b364c56592b204bf170ab6a15dae771a6`  
		Last Modified: Sat, 16 May 2020 06:39:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d9c785f332b55c2da9f65c5c333bdb5d5b344fb2fae6ad8ccbcc14c49eaa9c`  
		Last Modified: Sat, 16 May 2020 06:39:44 GMT  
		Size: 7.0 MB (7026776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a632ccf2a4dfc372007b6d317687a7cd3ae291df232549a54931d4d1dc5615d2`  
		Last Modified: Sat, 16 May 2020 06:39:43 GMT  
		Size: 2.7 MB (2712787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beceec94d37853479988bfc576c12e97abc44224d1dbcf2658758ebd3c70a54f`  
		Last Modified: Sat, 16 May 2020 06:40:30 GMT  
		Size: 176.7 MB (176717178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcfee5b8c65815cd602ead3301a71126aff85ea944cb5c52ffad126a99dc74d`  
		Last Modified: Sat, 16 May 2020 06:39:43 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845f02b705caa5b416e93e2f497db8bb6c8f8c370b210e564b478adf0047774f`  
		Last Modified: Sat, 16 May 2020 06:39:43 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:65413b8a6070d687511dbe861d21ed44a312f7ffa211023457991bb5646ebb5c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317293370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0a980212bec64fe07dfd51210d5a9beb8c51b46112d030e3fa642d7cb6cdbf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 24 Apr 2020 09:30:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 09:30:23 GMT
ENV GOLANG_VERSION=1.14.2
# Fri, 24 Apr 2020 09:32:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '98de84e69726a66da7b4e58eac41b99cbe274d7e8906eeb8a5b7eb0aadee7f7c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 24 Apr 2020 09:33:01 GMT
ENV GOPATH=/go
# Fri, 24 Apr 2020 09:33:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2020 09:33:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 24 Apr 2020 09:33:05 GMT
WORKDIR /go
# Fri, 24 Apr 2020 16:37:05 GMT
WORKDIR /src
# Fri, 24 Apr 2020 16:37:08 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 04 May 2020 18:40:16 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Mon, 04 May 2020 18:40:19 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Mon, 04 May 2020 18:40:19 GMT
WORKDIR /src/caddy/cmd/caddy
# Mon, 04 May 2020 18:40:54 GMT
RUN go get -d ./...
# Mon, 04 May 2020 18:41:02 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Mon, 04 May 2020 18:41:03 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fc45ca0357821724e2824e141e2062d236dedad3d8654e0a390419ec9fe393`  
		Last Modified: Fri, 24 Apr 2020 09:38:53 GMT  
		Size: 301.8 KB (301770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6332e392c90a454bd9f70a303cda942eb0e131e321e82cb70b9346ece4a52a64`  
		Last Modified: Fri, 24 Apr 2020 09:38:53 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f4526528e3f6ae0b8c71779d660d4b102620e94433d0c4f6947916633995e6`  
		Last Modified: Fri, 24 Apr 2020 09:39:19 GMT  
		Size: 126.4 MB (126405852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ee41552244ce7a16b4e463105b5589cc09a8db04bfbe50ff7225cde4cdd451`  
		Last Modified: Fri, 24 Apr 2020 09:38:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563a0747953abe39285173699e5f790697a6be2542ba5e0f5b16192d0912e2f0`  
		Last Modified: Fri, 24 Apr 2020 16:38:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69aaff34b0ef81b132484a7de376ce72b73f8a83989082d5fc96a2aa0fe3d9e1`  
		Last Modified: Fri, 24 Apr 2020 16:38:13 GMT  
		Size: 8.4 MB (8365426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7155164f7bfe2bc096faa0234bc188d2987f3293378ea801beca87581da342a`  
		Last Modified: Mon, 04 May 2020 18:41:28 GMT  
		Size: 2.8 MB (2778320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fa11401b7a1ef681acf17261fcaaff4c74fe5bedc308459b0e5dabcae7f43b`  
		Last Modified: Mon, 04 May 2020 18:42:04 GMT  
		Size: 176.7 MB (176716448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d4f378aaa4bf54004f71d46ab8ca4e1d126429ad3b8ead65e3bb4411288cd67`  
		Last Modified: Mon, 04 May 2020 18:41:28 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe937c594b97e42cd01984fcf196d4956966b9b65080fcff9af1684e00a306b`  
		Last Modified: Mon, 04 May 2020 18:41:27 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:5205ac5211c5f245f204b54a2b004cdc41ce91041c606ef3551a350b45efd275
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316505959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8ac470c65b0a007cfaccde682c393133fb25f3d2af1a69b0f589a4a20037c9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:54:40 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 24 Apr 2020 02:54:46 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:54:47 GMT
ENV GOLANG_VERSION=1.14.2
# Fri, 24 Apr 2020 02:56:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '98de84e69726a66da7b4e58eac41b99cbe274d7e8906eeb8a5b7eb0aadee7f7c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 24 Apr 2020 02:56:45 GMT
ENV GOPATH=/go
# Fri, 24 Apr 2020 02:56:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2020 02:56:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 24 Apr 2020 02:56:55 GMT
WORKDIR /go
# Wed, 06 May 2020 15:31:27 GMT
WORKDIR /src
# Wed, 06 May 2020 15:31:35 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 06 May 2020 15:31:39 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Wed, 06 May 2020 15:31:48 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Wed, 06 May 2020 15:31:52 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 06 May 2020 15:35:54 GMT
RUN go get -d ./...
# Wed, 06 May 2020 15:36:10 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Wed, 06 May 2020 15:36:12 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b20efe26326b88a40e960e9cd11fce1b701b2cf370e8328f66fc846d23b5408`  
		Last Modified: Fri, 24 Apr 2020 03:02:11 GMT  
		Size: 304.0 KB (303974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7438e1bdec433812841560459973aca70d85a3b7661615d9c632998dd366f248`  
		Last Modified: Fri, 24 Apr 2020 03:02:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41d89786f016b744fb801f0ff91a29a60511c224273dbb81d30d34b718736b3`  
		Last Modified: Fri, 24 Apr 2020 03:03:01 GMT  
		Size: 125.2 MB (125172829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c574e7dc094c4290e974ce97ec4bf702c4f8ea0a9cfe7aef59d7deb25fdb1d1`  
		Last Modified: Fri, 24 Apr 2020 03:02:11 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f45c1dbc176be1e40a2173998f55ef10caad453eba5b5edd4871e32df8ccbed`  
		Last Modified: Wed, 06 May 2020 15:36:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667b23014167367918703043e5990905f44319cac67a60b406e4af2d67567ffb`  
		Last Modified: Wed, 06 May 2020 15:36:58 GMT  
		Size: 8.8 MB (8784614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78250cd110923f6771049a7001c6d5140b7746074be267637a3be6a5aa2540bb`  
		Last Modified: Wed, 06 May 2020 15:36:56 GMT  
		Size: 2.7 MB (2704741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6f4a438bd580666034d37a509ed8dbbe15d118377037e8f2548d4eaf476e2`  
		Last Modified: Wed, 06 May 2020 15:42:35 GMT  
		Size: 176.7 MB (176716832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06937c71f6106173573586aff1ab0997a976b95a145c76b9c446153fd993c4ca`  
		Last Modified: Wed, 06 May 2020 15:36:55 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38513384bc38dde3278d28d9d76869ae9b2a7947f7062c67d97b43eab0337252`  
		Last Modified: Wed, 06 May 2020 15:36:55 GMT  
		Size: 181.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:577597322d9dfafa1285515c8fad56c80e2e6666687c460c504ff9057ec8051e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322380651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67498fdb89e44ca98ffe0ed90f15059e1c785c58d997469a86c95815bca8e153`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 20:01:10 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 23 Apr 2020 20:01:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 15 May 2020 20:44:43 GMT
ENV GOLANG_VERSION=1.14.3
# Fri, 15 May 2020 20:45:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 15 May 2020 20:45:56 GMT
ENV GOPATH=/go
# Fri, 15 May 2020 20:45:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 20:45:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 15 May 2020 20:45:57 GMT
WORKDIR /go
# Fri, 15 May 2020 21:45:40 GMT
WORKDIR /src
# Fri, 15 May 2020 21:45:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 15 May 2020 21:45:42 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Fri, 15 May 2020 21:45:47 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 15 May 2020 21:45:47 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 15 May 2020 21:46:02 GMT
RUN go get -d ./...
# Fri, 15 May 2020 21:46:09 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Fri, 15 May 2020 21:46:09 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4bb5699ff3d626466b57d4c92bbf8a5410490fcece2b350c368cad50778b96d`  
		Last Modified: Thu, 23 Apr 2020 20:06:33 GMT  
		Size: 301.9 KB (301908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf86b8de56aab63659ca622083cd8174db3525f6baa42836863267efa18de0e2`  
		Last Modified: Thu, 23 Apr 2020 20:06:33 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953996d17e01ab26a510ab21d1b8e140a2a82a3a6d470890ee321abc0bd59fd3`  
		Last Modified: Fri, 15 May 2020 20:50:46 GMT  
		Size: 131.9 MB (131858758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef8c1c28767148ade729d11932d2312b1410b36186d0a9cde1e36c9ba3d301e`  
		Last Modified: Fri, 15 May 2020 20:50:44 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ed906c938756832f1f51a17e0d0646a48609eb7bb7748b193efcee9dab0764`  
		Last Modified: Fri, 15 May 2020 21:46:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53c7446c5e8e872a9d2bdfc7cc7f72ca494f91a3e1f8cb14508032e27f6abc2`  
		Last Modified: Fri, 15 May 2020 21:46:22 GMT  
		Size: 8.2 MB (8212441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d78bef69b13c0f6ef34dee6b17c2db47e19e4c33287e433e415481d9b3a3ce9`  
		Last Modified: Fri, 15 May 2020 21:46:21 GMT  
		Size: 2.7 MB (2708215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5eb0f1d42c2b99f724659a6fdfe4ed355920ecd7849c101c2f4fd300bf6f01`  
		Last Modified: Fri, 15 May 2020 21:46:42 GMT  
		Size: 176.7 MB (176715349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473a5b493d958f1054c96c252c5d6147a49bcc11a5262b58b54319e9b9fe558c`  
		Last Modified: Fri, 15 May 2020 21:46:52 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47634dd72ea6c819d83f449fe1b61d55c6a3866fcf9c2f0cb9fb92e1cf93d341`  
		Last Modified: Fri, 15 May 2020 21:46:52 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

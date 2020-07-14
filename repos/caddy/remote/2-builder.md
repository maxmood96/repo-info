## `caddy:2-builder`

```console
$ docker pull caddy@sha256:9f517902c39a9134a35050ef811be296b1277f9bef29c55da479c3cceb042d7c
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
$ docker pull caddy@sha256:a468f050249ced8980e344b3d89a4f8edaf8ede2b9ffc992e4299461c6df762f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.1 MB (331145798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fac412c11d24fd828ec634457e43ca5cf99bad8e5daa8f73d2b4ba84a353baa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:30:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Jul 2020 18:20:28 GMT
ENV GOLANG_VERSION=1.14.5
# Tue, 14 Jul 2020 18:22:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'ca4c080c90735e56152ac52cd77ae57fe573d1debb1a58e03da9cc362440315c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 14 Jul 2020 18:22:43 GMT
ENV GOPATH=/go
# Tue, 14 Jul 2020 18:22:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jul 2020 18:22:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Jul 2020 18:22:44 GMT
WORKDIR /go
# Tue, 14 Jul 2020 18:50:18 GMT
WORKDIR /src
# Tue, 14 Jul 2020 18:50:20 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 14 Jul 2020 18:50:20 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 14 Jul 2020 18:50:22 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 14 Jul 2020 18:50:22 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 14 Jul 2020 18:50:46 GMT
RUN go get -d ./...
# Tue, 14 Jul 2020 18:50:47 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 14 Jul 2020 18:50:48 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8968b2872e472e21554ca58b35a02277634f3e501cc04ab7b0d0963f60f54d`  
		Last Modified: Tue, 02 Jun 2020 01:44:13 GMT  
		Size: 282.6 KB (282603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92cc7c5fd73817407fa0e4de5e1fb262a9c0f34c35c7450a2d01a7cef79c62f`  
		Last Modified: Tue, 02 Jun 2020 01:44:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7194a02b5507b49034790a1bbee21430d6089dac1266f1767360907bc89a2f17`  
		Last Modified: Tue, 14 Jul 2020 18:32:30 GMT  
		Size: 132.5 MB (132502503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee87bd7b0b1fe764439f8582dd626cf527dcf16b58a357984448095a3c0332f1`  
		Last Modified: Tue, 14 Jul 2020 18:32:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081bcc9819518d6cf0c448e236991065a1f7f649cbb9db832056b0630ccc1e93`  
		Last Modified: Tue, 14 Jul 2020 18:51:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c079dcc1d64ef535a6c432fa04266ea0f86603266c82cc5d715a06ae4b94abf5`  
		Last Modified: Tue, 14 Jul 2020 18:51:07 GMT  
		Size: 8.3 MB (8310032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b418413d3dcfa28a50809f13f98f1bff269ced6817083fa82f16ad01726c820`  
		Last Modified: Tue, 14 Jul 2020 18:51:05 GMT  
		Size: 3.0 MB (3020904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0650055b3871b3ad17a05c11dad34e92bc33b09074f8956c1abc2fe327c6d1fa`  
		Last Modified: Tue, 14 Jul 2020 18:51:44 GMT  
		Size: 184.2 MB (184231183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a939101a911a86eacc1f03f6367077198147bf6ba6b2be62171d17400781071e`  
		Last Modified: Tue, 14 Jul 2020 18:51:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4014a6ed75083936c76ceab546774c30566ecd6c50815c4868b973291bf783fd`  
		Last Modified: Tue, 14 Jul 2020 18:51:04 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:576976b3ab5f2a86f7a5ddd4ea437f28385e1b68b0658442f2899800cbd61e8c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.4 MB (326364244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14aaf79c281ac4dda260a4e7aa7314107e5fdf503bd14f38071a64776c624b13`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 02:02:10 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 02:02:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 02 Jun 2020 02:02:29 GMT
ENV GOLANG_VERSION=1.14.4
# Tue, 02 Jun 2020 02:55:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '7011af3bbc2ac108d1b82ea8abb87b2e63f78844f0259be20cde4d42c5c40584 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 02 Jun 2020 02:56:02 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2020 02:56:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2020 02:56:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 02 Jun 2020 02:56:07 GMT
WORKDIR /go
# Mon, 15 Jun 2020 20:52:46 GMT
WORKDIR /src
# Mon, 15 Jun 2020 20:52:50 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 30 Jun 2020 23:49:51 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:49:54 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 30 Jun 2020 23:49:55 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 30 Jun 2020 23:50:38 GMT
RUN go get -d ./...
# Tue, 14 Jul 2020 00:49:32 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 14 Jul 2020 00:49:32 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c276dc457bae632c9eadd1ac69c1a756a9a67e050b0350a475b19663722191cf`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 282.8 KB (282778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f0819b703e39c232c6d0a8ac0f76d8f3c6856629db16fd6dd7b7ae69368281`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e66763a2c2fd4a68d63d58e30f372cf4ebdc811274c6979d891e5e0cb676d73`  
		Last Modified: Tue, 02 Jun 2020 05:22:08 GMT  
		Size: 128.2 MB (128209215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7367c813a205e4503e365f0492c4c2de22baead5b600a620d362655aa9cd483`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce88b922cbeaa0f67211b29ad7ed76847d7725e329cc620ff7dcc9257fba77e3`  
		Last Modified: Mon, 15 Jun 2020 20:54:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720f093e5ede770f019c0c7a14a3361e9648d5b00f7a171f8feaefab719955aa`  
		Last Modified: Mon, 15 Jun 2020 20:54:50 GMT  
		Size: 7.9 MB (7928846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87454bdd0b68cb419479596ea418f39e543899d1bcf4a9b8438e4a0af915d659`  
		Last Modified: Tue, 30 Jun 2020 23:51:17 GMT  
		Size: 3.1 MB (3099715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8248605a05ee8d00c6a13d2b522c366652ff839231107c73f8e02086e2ef5b1c`  
		Last Modified: Tue, 30 Jun 2020 23:52:04 GMT  
		Size: 184.2 MB (184239271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d2516156bc5b029c3cdb8ff73d5a14a1fa895581e22082d6ec51561e398246`  
		Last Modified: Tue, 14 Jul 2020 00:49:45 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990270e1d3af55a3669a82b4e9b7a9241550d8c746c91339b735be075273bb68`  
		Last Modified: Tue, 14 Jul 2020 00:49:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:0b98037197a347e2000043073bfbb5fe3e292c9f4179c0c7bf7dbaf15a6a2120
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.0 MB (325014327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edefb00c4749879195b2311e221bca2dd79046c6892bfc140420c416dd7d2f07`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:10:58 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:11:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 02 Jun 2020 01:11:01 GMT
ENV GOLANG_VERSION=1.14.4
# Tue, 02 Jun 2020 01:34:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '7011af3bbc2ac108d1b82ea8abb87b2e63f78844f0259be20cde4d42c5c40584 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 02 Jun 2020 01:34:38 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2020 01:34:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2020 01:34:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 02 Jun 2020 01:34:44 GMT
WORKDIR /go
# Mon, 15 Jun 2020 21:00:34 GMT
WORKDIR /src
# Mon, 15 Jun 2020 21:00:37 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 30 Jun 2020 23:58:20 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:58:24 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 30 Jun 2020 23:58:25 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 30 Jun 2020 23:59:13 GMT
RUN go get -d ./...
# Tue, 14 Jul 2020 00:57:37 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 14 Jul 2020 00:57:38 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8512c25ce227edddad11326504a9bab47e83f8b61c090c9dc95882452984ac62`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 281.9 KB (281892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87928ee7e6c788309b46621e351321410e4dde5374869ffa75f404b19e0e0c12`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754691c4bcf20eb06087104e5fc82d340991d9bf26c21cae6979f36e3bd38ca7`  
		Last Modified: Tue, 02 Jun 2020 03:52:16 GMT  
		Size: 127.8 MB (127846663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63238be1b74c86ab98841c3959a33d79a903d58ac50518d4fa65b2ea8c6a75ba`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a1abd4bf80876cf553a554662e0cb3c5c310601b937ee7749c6f828de9dfea`  
		Last Modified: Mon, 15 Jun 2020 21:02:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac591f152779d4cfd93fb1e2f29dfeb27073f3559e8cb0daf8ee5c6f58310dc`  
		Last Modified: Mon, 15 Jun 2020 21:02:23 GMT  
		Size: 7.1 MB (7144878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff70e09616486f12dbaa23bf518b25b4319b9191a192b458fb1a54ce5de4d3b`  
		Last Modified: Tue, 30 Jun 2020 23:59:55 GMT  
		Size: 3.1 MB (3097567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286df284eb60ab6779cc5d8f805e5ca5deecdc9b3cef6384bc1ff223e36c1d99`  
		Last Modified: Wed, 01 Jul 2020 00:00:45 GMT  
		Size: 184.2 MB (184235432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98152591dadc19f79550c5d880460db7daf0b14a95c298159c72d39ad46b14ef`  
		Last Modified: Tue, 14 Jul 2020 00:57:51 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5736c517c33115814b07c099d6bdcbf5e78f31ff698d9fa39e7693aabed85d9`  
		Last Modified: Tue, 14 Jul 2020 00:57:50 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:5506a78bc54fc30be64368450d33bf8ad6fe9c34e0eb431d6f1569a452d90e00
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325331662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d691999d8f5fb04014d78265f6b7516d3e164e8c945a47e0004b6fa328db55e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:57:21 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:58:08 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 02 Jun 2020 01:58:16 GMT
ENV GOLANG_VERSION=1.14.4
# Tue, 02 Jun 2020 02:00:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '7011af3bbc2ac108d1b82ea8abb87b2e63f78844f0259be20cde4d42c5c40584 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 02 Jun 2020 02:00:34 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2020 02:00:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2020 02:00:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 02 Jun 2020 02:01:01 GMT
WORKDIR /go
# Mon, 15 Jun 2020 20:42:55 GMT
WORKDIR /src
# Mon, 15 Jun 2020 20:42:58 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 30 Jun 2020 23:40:08 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:40:11 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 30 Jun 2020 23:40:12 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 30 Jun 2020 23:40:39 GMT
RUN go get -d ./...
# Tue, 14 Jul 2020 00:39:52 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 14 Jul 2020 00:39:53 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f711af9a0d350d42a1cb00f41feb32277e11189d70d84d76fdef5065f78c47`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 283.0 KB (282997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f96fe45779b3ba9e9daededd02c233c5c76715ef1c5e88dd10c7acbea8414f`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a10f6d585c919680bed516e83e217d8bb824ee48306a00ce36c94a2a42e127`  
		Last Modified: Tue, 02 Jun 2020 02:30:00 GMT  
		Size: 126.5 MB (126505030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fdc7971b1eac6baae4423fc0ecca822c4d0372de7bfbdb5a7451e3cdd06be30`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9d4bc6b21331beadc7877a16034ab0b38c0afcf3434fba21ae30649336cb92`  
		Last Modified: Mon, 15 Jun 2020 20:44:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebe763a900953fc839be7c307bee96cc4464502cd2cf875941354458648b2b4`  
		Last Modified: Mon, 15 Jun 2020 20:44:13 GMT  
		Size: 8.5 MB (8499921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40cc98ebf8ade7d14e8ba21309fb3ec00ecd3f5c26bcde20da0a4404592a452d`  
		Last Modified: Tue, 30 Jun 2020 23:41:16 GMT  
		Size: 3.1 MB (3097543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896511aaf0a6d921f248b7e9c422cafcf89eeb3767cb1c3b8fb120b99d130177`  
		Last Modified: Tue, 30 Jun 2020 23:41:57 GMT  
		Size: 184.2 MB (184237073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acff171601695c4eec7a859d160c7580c20bb6bbc4d9be626258471faaf2271c`  
		Last Modified: Tue, 14 Jul 2020 00:40:05 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb41e7930bed2f4006e871708175b451af98829c0df5cbe4d3bff198477b929`  
		Last Modified: Tue, 14 Jul 2020 00:40:05 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:3a2af0e8d357ee1b9ff8dc1c6a1acbbc8de68c1a62449fa6b31e6eac88c955fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324617617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6f2c92c32552ebc744e6037f35955c01ff853fe9450c41e6685b13d79d1905`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:29:37 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:29:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 02 Jun 2020 01:30:00 GMT
ENV GOLANG_VERSION=1.14.4
# Tue, 02 Jun 2020 01:32:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '7011af3bbc2ac108d1b82ea8abb87b2e63f78844f0259be20cde4d42c5c40584 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 02 Jun 2020 01:32:22 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2020 01:32:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2020 01:32:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 02 Jun 2020 01:32:46 GMT
WORKDIR /go
# Mon, 15 Jun 2020 21:20:48 GMT
WORKDIR /src
# Mon, 15 Jun 2020 21:20:57 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 01 Jul 2020 00:54:57 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Wed, 01 Jul 2020 00:55:18 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Wed, 01 Jul 2020 00:55:25 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 01 Jul 2020 01:00:44 GMT
RUN go get -d ./...
# Tue, 14 Jul 2020 01:18:23 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 14 Jul 2020 01:18:45 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d800b4e456ea05213bc7310b5d1b1706274430828a3c19a2fa8c6694733dc4`  
		Last Modified: Tue, 02 Jun 2020 01:48:21 GMT  
		Size: 285.0 KB (285034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a45a7c013c1132848fd122dfb4511c34ed884573ddfd7d8ad13d9a8a6157c42`  
		Last Modified: Tue, 02 Jun 2020 01:48:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa9f54e0b14ecd0984863bb950f61bd4bf436b6072e38800e7f963358557067`  
		Last Modified: Tue, 02 Jun 2020 01:48:47 GMT  
		Size: 125.3 MB (125263901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a41edd0480b633d5ed3f00eef305e8a7526c48f1fdde5ef350565830d40609`  
		Last Modified: Tue, 02 Jun 2020 01:48:20 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca1ca7c0085d0ffb2b0cb1bdabb73af28921fe105ac26bae09acee083eb4c72`  
		Last Modified: Mon, 15 Jun 2020 21:24:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55082f384c6dea8e172df520164ab7feeca61be6b9d38ab64bb2265b7f197b1`  
		Last Modified: Mon, 15 Jun 2020 21:24:49 GMT  
		Size: 8.9 MB (8919998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6576be449bd2776954e56f7254b1d88000e75ad86165473cf13427acc05615ca`  
		Last Modified: Wed, 01 Jul 2020 01:01:44 GMT  
		Size: 3.1 MB (3097500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9480caee021b774a13782504a3b88c52bcde123400ecce3b764df8cb7eb224`  
		Last Modified: Wed, 01 Jul 2020 01:02:12 GMT  
		Size: 184.2 MB (184244849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2247c00dc1fa3777d5a5931224c554572c6ac108b9a5fb8fc0e6dabf44c64a8`  
		Last Modified: Tue, 14 Jul 2020 01:19:13 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622d80757ba0ef8b05c657b6637d75168d573e6380b88e316cf2a308c68b84dc`  
		Last Modified: Tue, 14 Jul 2020 01:19:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:f994b04eb82e925976a32e4ae57f3f4bee51deb381f8309b1e9015fff0b24e95
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330350400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350053e99dd1b07d42622cbdb2095e61b6ef9c1eed37dd403caf95acfe468c55`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:53:15 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:53:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 02 Jun 2020 01:53:16 GMT
ENV GOLANG_VERSION=1.14.4
# Tue, 02 Jun 2020 01:54:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '7011af3bbc2ac108d1b82ea8abb87b2e63f78844f0259be20cde4d42c5c40584 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 02 Jun 2020 01:54:38 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2020 01:54:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2020 01:54:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 02 Jun 2020 01:54:39 GMT
WORKDIR /go
# Mon, 15 Jun 2020 20:43:26 GMT
WORKDIR /src
# Mon, 15 Jun 2020 20:43:28 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 30 Jun 2020 23:41:45 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:41:47 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 30 Jun 2020 23:41:48 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 30 Jun 2020 23:42:14 GMT
RUN go get -d ./...
# Tue, 14 Jul 2020 00:41:31 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 14 Jul 2020 00:41:32 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2094092570892a8483a3fc940b327cccddf0cb7affb2a628ef4c98e40b4830bd`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 283.1 KB (283144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64a1c2f9ba0751e3e55cf33ddc6f0fd325bce1e6d64ef921f6258c5115b3c0`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc125fe27a23a8501491445468375e7ea9db946b45cbd911a05a65cfb7c3334`  
		Last Modified: Tue, 02 Jun 2020 02:01:21 GMT  
		Size: 131.8 MB (131814783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7129c3822665192c1533e7d5ab270717e256b1b9844d6fd116852b00a29058e9`  
		Last Modified: Tue, 02 Jun 2020 02:01:34 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8d7ec191535d778fe97d9e282050d4140fab1236212ea77816ba1db178bae`  
		Last Modified: Mon, 15 Jun 2020 20:44:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a8d11ad8b6daae49f4e16f31468f03664af47d81d6792e5da6fb1eff11ee52`  
		Last Modified: Mon, 15 Jun 2020 20:44:32 GMT  
		Size: 8.4 MB (8352257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b8ff85b28f8ebc6d191d86a31b77fe5f1b972d7a27b84107f388dd9d7e94be`  
		Last Modified: Tue, 30 Jun 2020 23:42:56 GMT  
		Size: 3.1 MB (3099677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64998b03655d547eb0910c16089828b9da3dcfc52fe9d4630cc9af3f0f2a15a9`  
		Last Modified: Tue, 30 Jun 2020 23:43:18 GMT  
		Size: 184.2 MB (184233221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a406c4ee521764c51c342652e8a2cdca422111ef045b547581bfd61c5f05a76f`  
		Last Modified: Tue, 14 Jul 2020 00:41:42 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574690c50692595ac9bf784eab29a01c406c1e746859cf1e4b34f503f5aa8bdb`  
		Last Modified: Tue, 14 Jul 2020 00:41:47 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

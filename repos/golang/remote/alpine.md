## `golang:alpine`

```console
$ docker pull golang@sha256:3116782b7d4e7ad51454bbb0ab1291468b7cb23e2286f6fcce50d6163289b6dd
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

### `golang:alpine` - linux; amd64

```console
$ docker pull golang@sha256:e8c6ee8a59dab1e57c603073a616c99ead42b2690d504aa88302136e4d9744be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135466723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882dad32cc49c80d1378d900b0bc48c2632c1d009695776da4c29b9daeaf63f4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:06:05 GMT
RUN apk add --no-cache 		ca-certificates
# Sat, 18 Jan 2020 02:06:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 20 Mar 2020 03:28:16 GMT
ENV GOLANG_VERSION=1.14.1
# Fri, 20 Mar 2020 03:32:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '2ad2572115b0d1b4cb4c138e6b3a31cee6294cb48af75ee86bec3dca04507676 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 20 Mar 2020 03:32:30 GMT
ENV GOPATH=/go
# Fri, 20 Mar 2020 03:32:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2020 03:32:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 20 Mar 2020 03:32:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb0d8da1b304e1b4f86e0a2fb11185850170e41986ce261dc30ac043c6a4e55`  
		Last Modified: Sat, 18 Jan 2020 02:17:12 GMT  
		Size: 301.3 KB (301262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d909eff282003e2d64af08633f4ae58f8cab4efc0a83b86579b4bbcb0ac90956`  
		Last Modified: Sat, 18 Jan 2020 02:17:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee54efb7a800ebed6fba009fce76a08dab62d8ffcf3b45e3b76595c450c5ba7`  
		Last Modified: Fri, 20 Mar 2020 03:40:42 GMT  
		Size: 132.4 MB (132362223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c68adefad4108dd211ebd2097428c0546fb3c822ca6865a9577fa74e9f0a55f`  
		Last Modified: Fri, 20 Mar 2020 03:40:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:30b55bb24351861563e401581d7876078bf5a15c48aad942f3460e34912cec2f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131397324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917860cde53367ced2542d815f389b65ece59553c80eca3751c4ccae6164e3cb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 06:25:47 GMT
RUN apk add --no-cache 		ca-certificates
# Sat, 18 Jan 2020 06:26:01 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 20 Mar 2020 00:49:16 GMT
ENV GOLANG_VERSION=1.14.1
# Fri, 20 Mar 2020 01:27:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '2ad2572115b0d1b4cb4c138e6b3a31cee6294cb48af75ee86bec3dca04507676 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 20 Mar 2020 01:27:52 GMT
ENV GOPATH=/go
# Fri, 20 Mar 2020 01:28:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2020 01:28:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 20 Mar 2020 01:28:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2b137a297685be92f7479a03dea76067a2661aad0f67c91123273b54a624ec`  
		Last Modified: Sat, 18 Jan 2020 06:37:07 GMT  
		Size: 301.6 KB (301631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439690e0c083aac08ba3afdf74ba79b8f50b530aed84c1d194e232c8ee4713a1`  
		Last Modified: Sat, 18 Jan 2020 06:37:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01fc27f1e4ce143ab557a7623006242d6fb9ba7ce7bd845662973452d9976ed`  
		Last Modified: Fri, 20 Mar 2020 02:33:43 GMT  
		Size: 128.5 MB (128477820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cecb2fbe46a9cc65e22f82a0f0ddd437c13420079f09ed7348b4c43bce3d97`  
		Last Modified: Fri, 20 Mar 2020 02:32:34 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:25da6a8aeeb134e2f0795a015c79cf3ba6386729fab2fed9f645cd40c57fa747
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130798040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6821798f5bdceb4b904b74fca15ab43de7d7a67b3d29d784696ed1f626375c1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:05:43 GMT
RUN apk add --no-cache 		ca-certificates
# Sat, 18 Jan 2020 03:05:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 20 Mar 2020 01:19:56 GMT
ENV GOLANG_VERSION=1.14.1
# Fri, 20 Mar 2020 02:03:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '2ad2572115b0d1b4cb4c138e6b3a31cee6294cb48af75ee86bec3dca04507676 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 20 Mar 2020 02:03:23 GMT
ENV GOPATH=/go
# Fri, 20 Mar 2020 02:03:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2020 02:03:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 20 Mar 2020 02:03:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cc1a5632a818a23b346143b68a5f38c687431e4c6752c1c065fd45e4eb4cae`  
		Last Modified: Sat, 18 Jan 2020 03:15:43 GMT  
		Size: 300.6 KB (300566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321c622e107dd32aa9f0a955846018aa4ff6d211da03fb554cb91f1166eca153`  
		Last Modified: Sat, 18 Jan 2020 03:15:43 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562ae2b4676c7680859ff1b763f0f736d3298f641792f645182d4cc40f003993`  
		Last Modified: Fri, 20 Mar 2020 03:13:00 GMT  
		Size: 128.1 MB (128077611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a384b9b0af0c40295f9ee2b6e1d69d6577ac1aa76e5aa712285e2a6509b075d5`  
		Last Modified: Fri, 20 Mar 2020 03:12:07 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f3c9d5e06c215a4fe1426662a6153df4a93713a8c6de82376d0df1dacf1e71f2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129793949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690eeeeaa71204252527fe67d67967fcab83c62faa88850baf8515937920f6b7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 06:10:29 GMT
RUN apk add --no-cache 		ca-certificates
# Sat, 18 Jan 2020 06:10:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 20 Mar 2020 01:40:20 GMT
ENV GOLANG_VERSION=1.14.1
# Fri, 20 Mar 2020 01:45:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '2ad2572115b0d1b4cb4c138e6b3a31cee6294cb48af75ee86bec3dca04507676 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 20 Mar 2020 01:45:25 GMT
ENV GOPATH=/go
# Fri, 20 Mar 2020 01:45:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2020 01:46:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 20 Mar 2020 01:46:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b0fa9a238a4fa3f590c80e14c5732f811f7a17aa0b8102cea7e3a9d250fcd`  
		Last Modified: Sat, 18 Jan 2020 06:20:51 GMT  
		Size: 301.8 KB (301775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583d88f014275e361b79e5a5ccf10b177aafe63e5d44ccd5d3911ca9b924efac`  
		Last Modified: Sat, 18 Jan 2020 06:20:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e995a40ef7dc756e3741f07bf0c892da6e2fed7ca7db60712f7236e3b37cb63`  
		Last Modified: Fri, 20 Mar 2020 02:08:23 GMT  
		Size: 126.8 MB (126768789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d593a80447b5ce99ed0a06e4cf5c1b50769586b868c8a0ceb9fe03c9737c02a4`  
		Last Modified: Fri, 20 Mar 2020 02:07:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine` - linux; 386

```console
$ docker pull golang@sha256:193c35967c5706debd4375ab452f673d191804f58b094a92ddebb50c7155edbd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135440982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a0a461d256283f5e09f5871eaace70aa1c7938632aefb150f0dd7a6dd43e7f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:38:44 GMT
ADD file:381b617b92fe699ad4ef4f30e0d9599f89e43e252883348c420ebe2a0cccbd63 in / 
# Sat, 18 Jan 2020 01:38:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 07:02:55 GMT
RUN apk add --no-cache 		ca-certificates
# Sat, 18 Jan 2020 07:02:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 20 Mar 2020 03:54:31 GMT
ENV GOLANG_VERSION=1.14.1
# Fri, 20 Mar 2020 03:57:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '2ad2572115b0d1b4cb4c138e6b3a31cee6294cb48af75ee86bec3dca04507676 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 20 Mar 2020 03:57:49 GMT
ENV GOPATH=/go
# Fri, 20 Mar 2020 03:57:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2020 03:57:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 20 Mar 2020 03:57:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f024b1263dc58db07a458b73ae1a2dca02ca55bef1ccd1fa3fd50656551fadf2`  
		Last Modified: Sat, 18 Jan 2020 01:39:18 GMT  
		Size: 2.8 MB (2806560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51d08eae3dcf47cd450c87c9ea787c8293e63405c12eb6ab24dbc68d5f1c126`  
		Last Modified: Sat, 18 Jan 2020 07:11:57 GMT  
		Size: 301.9 KB (301918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93286c43ae8d1560f8d4f4591d4ac47b8532570a50267d7f0df83626ad9d77b7`  
		Last Modified: Sat, 18 Jan 2020 07:11:56 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086473301a38e9167bea22a45c5952b09b2492345944f21510defd3246271b45`  
		Last Modified: Fri, 20 Mar 2020 04:08:06 GMT  
		Size: 132.3 MB (132332227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188fcea89fcea8aa24868063e5fa3963b8e6772a1505c36d8b76e1f1d72227a3`  
		Last Modified: Fri, 20 Mar 2020 04:07:34 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:b3fe0328b2058460391748494d6790ddb00741b3071e0d8a5472ca679952174d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128641918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956b1f199afa8892e76db5c4d203a6f1e2abd3cf7dceb8930d4e682dfd9dad57`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 18 Jan 2020 02:20:41 GMT
ADD file:32ddb3d5255071cca51573ceee2464dd5a87c8d1cce514ae965b6e824d9ef24b in / 
# Sat, 18 Jan 2020 02:20:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:46:12 GMT
RUN apk add --no-cache 		ca-certificates
# Sat, 18 Jan 2020 04:46:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 20 Mar 2020 02:43:58 GMT
ENV GOLANG_VERSION=1.14.1
# Fri, 20 Mar 2020 02:46:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '2ad2572115b0d1b4cb4c138e6b3a31cee6294cb48af75ee86bec3dca04507676 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 20 Mar 2020 02:46:41 GMT
ENV GOPATH=/go
# Fri, 20 Mar 2020 02:46:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2020 02:46:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 20 Mar 2020 02:46:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd95c8a93e39dcaa0634a65d5b86a88bcd5c3092adb1f96504a7030faa165123`  
		Last Modified: Sat, 18 Jan 2020 02:21:25 GMT  
		Size: 2.8 MB (2822125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75713e636f3d39d3f2654c04e99be412afb204d9a236849bd298a759cbf05081`  
		Last Modified: Sat, 18 Jan 2020 04:54:33 GMT  
		Size: 304.0 KB (303987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2d35b38ecf395171885c1576a18a065e4580f2a1e83771da3f4de412af0712`  
		Last Modified: Sat, 18 Jan 2020 04:54:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141b6af7fc4114a457c723a2e80f920b89eaa0b40d0557b48126586a2e4b98f2`  
		Last Modified: Fri, 20 Mar 2020 02:57:07 GMT  
		Size: 125.5 MB (125515496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34b1919b516510f7d34080fb7fef21e8807a96511a0bedccf1919673accf336`  
		Last Modified: Fri, 20 Mar 2020 02:56:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine` - linux; s390x

```console
$ docker pull golang@sha256:fcd38b014e0a80f1671e6bcd5d24dc234880e03e2d20a150588b8b5aa9b1eb3a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (134989362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abf9ec8604adae27a573a5ebdbb72f53480935eb5125a52ff7d3e1c5dd07217`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:41:33 GMT
ADD file:a6f8b7d4ba199527053ef1ac710b5e318135cb6903cb9ad6fae4fe42e6ad0bf7 in / 
# Sat, 18 Jan 2020 01:41:33 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 01:42:23 GMT
RUN apk add --no-cache 		ca-certificates
# Sat, 18 Jan 2020 01:42:24 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 19 Mar 2020 23:42:16 GMT
ENV GOLANG_VERSION=1.14.1
# Thu, 19 Mar 2020 23:43:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '2ad2572115b0d1b4cb4c138e6b3a31cee6294cb48af75ee86bec3dca04507676 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 19 Mar 2020 23:43:53 GMT
ENV GOPATH=/go
# Thu, 19 Mar 2020 23:43:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Mar 2020 23:43:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 19 Mar 2020 23:43:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:176bad61a3a435da03ec603d2bd8f7a69286d92f21f447b17f21f0bc4e085bde`  
		Last Modified: Sat, 18 Jan 2020 01:41:59 GMT  
		Size: 2.6 MB (2582031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5098d3328eb232d7f1890bea7d184bb878fdd3fd6f662f587ed0a70612d5587`  
		Last Modified: Sat, 18 Jan 2020 01:47:22 GMT  
		Size: 301.8 KB (301795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95cfc0bf895b01244b27aba1473ab54b274b1d43e1aacc52256be747e0835a38`  
		Last Modified: Sat, 18 Jan 2020 01:47:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e39ee5a1ac60a33946f2c0387b5a3d790d3886b92212539bb2a85a4d3f6817e`  
		Last Modified: Thu, 19 Mar 2020 23:49:26 GMT  
		Size: 132.1 MB (132105225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1155a4c60ebe5b6fc34fb0b727943f4a9e195964511c2e31b89f50b601a7bfb9`  
		Last Modified: Thu, 19 Mar 2020 23:49:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

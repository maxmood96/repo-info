## `caddy:builder`

```console
$ docker pull caddy@sha256:e7f19375fb2af512955ebfe845d8ea78b32cae8c608d367d393cbc209fc2cf3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:0750762062e92c7e2e8aa0c2c7e80d5762f6771f9c38aee0d4369b562bdad52b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322833946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed310fb9f0cd01f3920b3f64f1697fea83efa462d6fefdd30cc519a005c6910b`
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
# Tue, 02 Jun 2020 01:32:50 GMT
ENV GOLANG_VERSION=1.14.4
# Tue, 02 Jun 2020 01:35:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '7011af3bbc2ac108d1b82ea8abb87b2e63f78844f0259be20cde4d42c5c40584 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 02 Jun 2020 01:35:10 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2020 01:35:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2020 01:35:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 02 Jun 2020 01:35:11 GMT
WORKDIR /go
# Tue, 02 Jun 2020 02:32:26 GMT
WORKDIR /src
# Tue, 02 Jun 2020 02:32:27 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 02 Jun 2020 02:32:27 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Tue, 02 Jun 2020 02:32:28 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 02 Jun 2020 02:32:29 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 02 Jun 2020 02:32:42 GMT
RUN go get -d ./...
# Tue, 02 Jun 2020 02:32:42 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Tue, 02 Jun 2020 02:32:42 GMT
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
	-	`sha256:cc1be7d07969680a19c74f96783bb978cfc281d9eb21dd6377a1ba0c60b22161`  
		Last Modified: Tue, 02 Jun 2020 01:45:12 GMT  
		Size: 132.1 MB (132121186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed5455f4aa4c7ceedfadd2f093fffcda763951c5ae506c6d92151ad6e4dae0e`  
		Last Modified: Tue, 02 Jun 2020 01:44:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45598100dcda08511c93d19c558a05a901b1a183efefa4cda30b7c7e6f93d03c`  
		Last Modified: Tue, 02 Jun 2020 02:32:53 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89489597245daae1172eaaf4fc1db5044f7684053f7428c9e2b93b567d6d50d`  
		Last Modified: Tue, 02 Jun 2020 02:32:54 GMT  
		Size: 8.2 MB (8177829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc24cd02350289621830e1a9e35520aaa1bc92133dd8b9f775d5d108f93126cc`  
		Last Modified: Tue, 02 Jun 2020 02:32:52 GMT  
		Size: 2.7 MB (2706286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4dbcd3eb953512768ffac90d7561911f8d07b650519e87a8f150417c4210b3`  
		Last Modified: Tue, 02 Jun 2020 02:33:13 GMT  
		Size: 176.7 MB (176713022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461dd6e5ccc455d939c9a53d58c106ce85ec9f7f0c674299b3d974445993dc8c`  
		Last Modified: Tue, 02 Jun 2020 02:32:52 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71023d2750548230f0a4dc5e3687b6c7a8faa42933147a45edaf1d1b0e7155a`  
		Last Modified: Tue, 02 Jun 2020 02:32:52 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f722d703d3a5a30563460536bd3a850b5175ad79c43c8a9397b0b3a5c8f100d3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318375279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb7124899c5889d20b2be36389f5a3f3741f34b9afba1078c43835dea3cd923`
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
# Tue, 02 Jun 2020 02:56:25 GMT
ENV GOLANG_VERSION=1.14.4
# Tue, 02 Jun 2020 03:51:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '7011af3bbc2ac108d1b82ea8abb87b2e63f78844f0259be20cde4d42c5c40584 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 02 Jun 2020 03:51:21 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2020 03:51:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2020 03:51:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 02 Jun 2020 03:51:26 GMT
WORKDIR /go
# Tue, 02 Jun 2020 05:40:14 GMT
WORKDIR /src
# Tue, 02 Jun 2020 05:40:16 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 02 Jun 2020 05:40:17 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Tue, 02 Jun 2020 05:40:19 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 02 Jun 2020 05:40:20 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 02 Jun 2020 05:41:15 GMT
RUN go get -d ./...
# Tue, 02 Jun 2020 05:41:20 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Tue, 02 Jun 2020 05:41:21 GMT
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
	-	`sha256:03c18b24b5eeba6322ca5f9b2eedb021ca9618b062bdf48b250ed4b201dc8050`  
		Last Modified: Tue, 02 Jun 2020 05:23:03 GMT  
		Size: 128.2 MB (128229189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de88420151b6ca5c6fc039fda4383cb82cf3566fa1cc6b2858d6fb47afe6ceb`  
		Last Modified: Tue, 02 Jun 2020 05:22:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f480e87ad21aa1d6eeb3d546b707aaaef59a9dc5dc0c6e5e14dcbe96c28cd9c`  
		Last Modified: Tue, 02 Jun 2020 05:41:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f74f503577c8c19df94e7f595796fd4e4e15166602d5843a4e28a694ef5e28f`  
		Last Modified: Tue, 02 Jun 2020 05:41:40 GMT  
		Size: 7.8 MB (7794708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12265e99f76b1fae972b3d710b32e05095595f8f0a5c088f78a217027939799`  
		Last Modified: Tue, 02 Jun 2020 05:41:38 GMT  
		Size: 2.7 MB (2712506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c581c17f5029909335c44e9a561b604aa98c4db79d38d9e87cae2749bcc658ce`  
		Last Modified: Tue, 02 Jun 2020 05:42:22 GMT  
		Size: 176.7 MB (176716184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57481f1b24f0912bad71decaec966f45bf686c9b218bd73fa4335d867d765ed7`  
		Last Modified: Tue, 02 Jun 2020 05:41:38 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd612876bd12eb68ab6685845a9b5cc04abca31e2e6292058dee233260487cf`  
		Last Modified: Tue, 02 Jun 2020 05:41:38 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:0c21b0ed54253ffdfa14547e326d48beebbf4b92bb8da76b92edb8c3c6abf04c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.0 MB (317037998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4388ab5685329446df0ddd799ba01c8a93d5feb07b8e6347d7c48a4827f0ac0c`
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
# Tue, 02 Jun 2020 01:35:08 GMT
ENV GOLANG_VERSION=1.14.4
# Tue, 02 Jun 2020 01:59:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '7011af3bbc2ac108d1b82ea8abb87b2e63f78844f0259be20cde4d42c5c40584 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 02 Jun 2020 01:59:49 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2020 01:59:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2020 01:59:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 02 Jun 2020 01:59:54 GMT
WORKDIR /go
# Tue, 02 Jun 2020 04:45:11 GMT
WORKDIR /src
# Tue, 02 Jun 2020 04:45:33 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 02 Jun 2020 04:45:42 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Tue, 02 Jun 2020 04:46:08 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 02 Jun 2020 04:46:18 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 02 Jun 2020 04:48:25 GMT
RUN go get -d ./...
# Tue, 02 Jun 2020 04:48:36 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Tue, 02 Jun 2020 04:48:46 GMT
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
	-	`sha256:3f154a497a43d3932627d4ed19f8a725b92bc6ff032696fd7d02c923aabfdfcd`  
		Last Modified: Tue, 02 Jun 2020 03:53:43 GMT  
		Size: 127.9 MB (127859153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356485fde635696dcdacee878dba8a58e09b58537b064b5f1661e5bbede500c1`  
		Last Modified: Tue, 02 Jun 2020 03:52:31 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955b3271dbcc86df5de81f5274c182306cd2a0e95581acd9a21262668cf2b88a`  
		Last Modified: Tue, 02 Jun 2020 04:49:24 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9e684ca35cc26b7059bb60e83771de2a6b96091a053dd7ecb7b81deeb696fd`  
		Last Modified: Tue, 02 Jun 2020 04:49:20 GMT  
		Size: 7.0 MB (7026779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1d162e820fa1c08e63c96be54a52b452f50218eeeee10b1260cd22d2250215`  
		Last Modified: Tue, 02 Jun 2020 04:49:20 GMT  
		Size: 2.7 MB (2712499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8138743a5c1e38d4db8ff61f24498d97cd9294a19cd9f2c6d88e8be776aa557e`  
		Last Modified: Tue, 02 Jun 2020 04:50:16 GMT  
		Size: 176.7 MB (176715788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e9777f9df18524b4ce10bcb6db5fb00912bde1d57de9ee77e0485b7ca87149`  
		Last Modified: Tue, 02 Jun 2020 04:49:20 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dbf791500a5a018208ecaed66e5d8afc28ca5be7ae31fb54c8b02c6dc02f68`  
		Last Modified: Tue, 02 Jun 2020 04:49:20 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:fa63e1ed3b5857fc2afa0da0e5f87e46c465ca4285b2f4256f033c7d0e075e16
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317306406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa08366dd0271d82e7194ee208f71f532fe0ef0edc70f7f2e9ace0fe35e206c`
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
# Tue, 02 Jun 2020 02:01:25 GMT
ENV GOLANG_VERSION=1.14.4
# Tue, 02 Jun 2020 02:05:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '7011af3bbc2ac108d1b82ea8abb87b2e63f78844f0259be20cde4d42c5c40584 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 02 Jun 2020 02:05:51 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2020 02:06:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2020 02:07:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 02 Jun 2020 02:07:23 GMT
WORKDIR /go
# Tue, 02 Jun 2020 03:54:39 GMT
WORKDIR /src
# Tue, 02 Jun 2020 03:55:18 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 02 Jun 2020 03:55:25 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Tue, 02 Jun 2020 03:56:04 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 02 Jun 2020 03:56:07 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 02 Jun 2020 03:57:15 GMT
RUN go get -d ./...
# Tue, 02 Jun 2020 03:57:23 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Tue, 02 Jun 2020 03:57:32 GMT
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
	-	`sha256:a4d8f54f55a2670968860ca35a8c2a0e2e526b543894d26874eae63fc6ce1532`  
		Last Modified: Tue, 02 Jun 2020 02:30:54 GMT  
		Size: 126.5 MB (126491009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2603d501b5a4a0cd3f6da1f592af79cba3b33143d7e3c4abd674ddc768193ec`  
		Last Modified: Tue, 02 Jun 2020 02:30:16 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2a6789a8ae4894bb21533776d982f6c268fcdcf9f33941f162b63755960e3b`  
		Last Modified: Tue, 02 Jun 2020 03:57:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c248984096d3b57adf469c453ec30db708388da2d14aab956f1204e917ca27c4`  
		Last Modified: Tue, 02 Jun 2020 03:57:58 GMT  
		Size: 8.4 MB (8365435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d43f4d0862815e18a79d45498f2fbcfd99029a2863caf46b05618fd0e1cd5fd`  
		Last Modified: Tue, 02 Jun 2020 03:57:54 GMT  
		Size: 2.7 MB (2706372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafe3a72624764aa34e658d59aff5bb317ff49f7624c43d47d9e5c575902a984`  
		Last Modified: Tue, 02 Jun 2020 03:58:33 GMT  
		Size: 176.7 MB (176716269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905e846552ef4792a1bc0924a7fafdf9fe2e669c5e91a25b222fc69a0ef958d0`  
		Last Modified: Tue, 02 Jun 2020 03:57:53 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ba0a8ecba94bf6fe06e59d7631f3e6ba4f79bbeccac3628b0b9bdb13825406`  
		Last Modified: Tue, 02 Jun 2020 03:57:53 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:6891c6d6490e09d98441446daa3f60dc3c0b1eef350bd60f15da70ce0c66e22d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 MB (316596303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d43482e81b370ae7732fbdf178f88ef7b057e0a406359ccbce7ad214d309fbf`
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
# Tue, 02 Jun 2020 01:32:58 GMT
ENV GOLANG_VERSION=1.14.4
# Tue, 02 Jun 2020 01:36:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '7011af3bbc2ac108d1b82ea8abb87b2e63f78844f0259be20cde4d42c5c40584 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 02 Jun 2020 01:36:14 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2020 01:36:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2020 01:36:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 02 Jun 2020 01:36:38 GMT
WORKDIR /go
# Tue, 02 Jun 2020 02:07:41 GMT
WORKDIR /src
# Tue, 02 Jun 2020 02:07:52 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 02 Jun 2020 02:07:56 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Tue, 02 Jun 2020 02:08:01 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 02 Jun 2020 02:08:03 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 02 Jun 2020 02:10:04 GMT
RUN go get -d ./...
# Tue, 02 Jun 2020 02:10:07 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Tue, 02 Jun 2020 02:10:10 GMT
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
	-	`sha256:665e10aea526140928afce65b052e28ac4f223162c45360135430121de27c7d7`  
		Last Modified: Tue, 02 Jun 2020 01:49:39 GMT  
		Size: 125.3 MB (125264184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1501bdd7b2a43f71acacc2d8a1122da868e702b75b2b680b69707544a4d2a6`  
		Last Modified: Tue, 02 Jun 2020 01:49:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e91f288ec567edbbf295fad3a3dadb1e59f32db4395eed7839b6ec89b8e2e1b`  
		Last Modified: Tue, 02 Jun 2020 02:10:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61996a2194cfe615b8d4f165ab0698f11f77f099cacb4305e2b4a48ecb23d85`  
		Last Modified: Tue, 02 Jun 2020 02:10:32 GMT  
		Size: 8.8 MB (8784628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5252de731606eac2f54796e9249033424cc547c2f7cfda78819e9bad6336d64b`  
		Last Modified: Tue, 02 Jun 2020 02:10:33 GMT  
		Size: 2.7 MB (2706339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3b270c7436a0d3b6f52d2c3ca32e87b1aa6b6cb910d93c8d8c146c281cb098`  
		Last Modified: Tue, 02 Jun 2020 02:10:57 GMT  
		Size: 176.7 MB (176714209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb2be7c1dce157b09712be8befda6ffc7db62d04638eb8de0ffcedc9c72ef9e`  
		Last Modified: Tue, 02 Jun 2020 02:10:29 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1a34918806b67ebe40004ce44428f56acf696819686c01055ec4bba3e40147`  
		Last Modified: Tue, 02 Jun 2020 02:10:30 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:947edd15c7a7b1de99ef6de49bfdba2c2f48b5ac85cdd68429a8d2b308b9fd39
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322334003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732919a18d2ee22b245cf74dbe9e1e6119e7364d09f35705c4641f8ab310185b`
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
# Tue, 02 Jun 2020 01:54:47 GMT
ENV GOLANG_VERSION=1.14.4
# Tue, 02 Jun 2020 01:56:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '7011af3bbc2ac108d1b82ea8abb87b2e63f78844f0259be20cde4d42c5c40584 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 02 Jun 2020 01:56:06 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2020 01:56:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2020 01:56:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 02 Jun 2020 01:56:07 GMT
WORKDIR /go
# Tue, 02 Jun 2020 02:18:58 GMT
WORKDIR /src
# Tue, 02 Jun 2020 02:18:59 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 02 Jun 2020 02:19:00 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Tue, 02 Jun 2020 02:19:01 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 02 Jun 2020 02:19:01 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 02 Jun 2020 02:19:20 GMT
RUN go get -d ./...
# Tue, 02 Jun 2020 02:19:28 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Tue, 02 Jun 2020 02:19:28 GMT
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
	-	`sha256:35fc33aefc5654dc9f18f8874ec5df3f0054d95efb6068093b66a806c1a47e54`  
		Last Modified: Tue, 02 Jun 2020 02:02:05 GMT  
		Size: 131.8 MB (131813328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb93b54892812fb36828c107902c548f3819372e46c12a6ecc0a7f79d29bdfd7`  
		Last Modified: Tue, 02 Jun 2020 02:01:43 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b29c909e9fef1d56ec58cb008cf363dead738a814985e79695e537b0d72ea53`  
		Last Modified: Tue, 02 Jun 2020 02:19:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1432be465a87de431d75d8d1cf02c7e3a11afc2f17e74071f56a6992f9f79ec`  
		Last Modified: Tue, 02 Jun 2020 02:19:40 GMT  
		Size: 8.2 MB (8212445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4868624099c4b67147b2c3310067ca317b998e011da3445bd20b30e6ea4a1f83`  
		Last Modified: Tue, 02 Jun 2020 02:19:39 GMT  
		Size: 2.7 MB (2706327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7621f436be1cd0adc948c7f4c2b6047e4fdf87b7f63644e5b832ab43cbea5a38`  
		Last Modified: Tue, 02 Jun 2020 02:20:13 GMT  
		Size: 176.7 MB (176716012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7181db5ca0fa079aa4c35d3206d2913d4d544419ff434d64f403c84b766044`  
		Last Modified: Tue, 02 Jun 2020 02:19:39 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eead0c695ec3fd46a6b5f762603d74e1b7757c7fd0f547ecd1ce7f1ab5d3a5`  
		Last Modified: Tue, 02 Jun 2020 02:20:09 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

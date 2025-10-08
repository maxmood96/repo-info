## `caddy:2-builder`

```console
$ docker pull caddy@sha256:4d2be51cdd15fc6872738bc1f26f7c0606c8bd135e7580d4fe6cf54810b19bb7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:4eb65fb153a45375ee43fb17580b5f7d75ed90b41d50fd560eb30ba9bfceddaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72300550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0fea734e4dc0638cddccf1eee0a22148fd1aa4bc591beb6a35eecadefcc0e5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOLANG_VERSION=1.25.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOTOOLCHAIN=local
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOPATH=/go
# Sat, 23 Aug 2025 03:19:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 03:19:59 GMT
COPY /target/ / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cb43161fc6dc3c8a304f6194e0dacd0b9f2348b4ccb83df9de4b60a8b389d0`  
		Last Modified: Tue, 07 Oct 2025 20:48:03 GMT  
		Size: 291.2 KB (291198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2aec7ef170b5f02e240ef6c8aac64fb96a14688ea0750c962c145c141f3830`  
		Last Modified: Tue, 07 Oct 2025 20:47:28 GMT  
		Size: 60.1 MB (60149177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18300489823e7c1e344fa6c1fa8a6350fa3c67b443964dea9c5d46f4c435b0f7`  
		Last Modified: Tue, 07 Oct 2025 20:48:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b20c86ec60f4a40d4f6cb2792acf767eb7c231730f86750704e33e042848e7`  
		Last Modified: Tue, 07 Oct 2025 21:16:10 GMT  
		Size: 6.2 MB (6213408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c691498c0bd60452bfad937bc36beaf34e3d8aa7ee1a8dc1f9dfaf435659ee`  
		Last Modified: Tue, 07 Oct 2025 21:16:10 GMT  
		Size: 1.8 MB (1846491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9401882f536f6c992beabe034ee44cbf148cf157e57e032003b3de5ae831c4b7`  
		Last Modified: Tue, 07 Oct 2025 21:16:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:fe6f814e59afeb95d4f1b61ef235d0635f3add0c4436772096e6bcd0a1e133d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 KB (300609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381be6b1f4f7e94b315cb1bd928774241cd08f1a8f9c805319d2928c0c9b60c2`

```dockerfile
```

-	Layers:
	-	`sha256:c7f76ca326f0a6d98c7af98ea26615289264ea863102c90eea4dddaf3c040bc6`  
		Last Modified: Wed, 08 Oct 2025 00:52:26 GMT  
		Size: 280.5 KB (280495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0247f8ee551f83976ba097f3d93d7cfa32673a7d8dedd82e939893e6fb2133e`  
		Last Modified: Wed, 08 Oct 2025 00:52:28 GMT  
		Size: 20.1 KB (20114 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:dbcb4b52a21e563618f662f7945295a4753fd2c6330bbd60e5144964d67eca41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70740771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0dc9068e3fe183a0d5a2ae55a16fbd8d890628395af264a2d89376511e3fff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOLANG_VERSION=1.25.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOTOOLCHAIN=local
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOPATH=/go
# Sat, 23 Aug 2025 03:19:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 03:19:59 GMT
COPY /target/ / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ab2d2f547d457177385ee8c584aeec12becde8a813a88d8e3692d56d6bdc11`  
		Last Modified: Tue, 07 Oct 2025 19:34:31 GMT  
		Size: 292.4 KB (292396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a729a3e231583976ae1f9cca817bd27dd00673c51d31bb2652e5b51a3d2ea3d`  
		Last Modified: Tue, 07 Oct 2025 19:34:35 GMT  
		Size: 59.1 MB (59074026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d646ee4c0b471ce651bb2f27d2e4931233fdd6815c76626a4dd325719044b1d7`  
		Last Modified: Tue, 07 Oct 2025 19:34:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f6991d0bd1dac463d19255050afce12898c6203eea1afdaffc7e382aa4b6b5`  
		Last Modified: Tue, 07 Oct 2025 20:12:14 GMT  
		Size: 6.1 MB (6127845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8829aa3ae0e4b71cef1f5bbd6677d28717d01f759bc91b802bb881fe92f418a`  
		Last Modified: Tue, 07 Oct 2025 20:12:17 GMT  
		Size: 1.7 MB (1745003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358c16be77d1aa138673ce1f4bf5b67b4c4eccf657f0acc0b632975954800bbb`  
		Last Modified: Tue, 07 Oct 2025 20:12:14 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:6f23375f3fae2b01324efb52c7047cec90a65be029dbe4af9e2b8f496871b295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7df9e3cbf651eb77e9c6c0209dbc6c40b3dead61d79f24c760a1984356a918`

```dockerfile
```

-	Layers:
	-	`sha256:92f3d64b31106af35280fbe4f489a177291948ea7aa509b75990dccd2f8d34a7`  
		Last Modified: Tue, 07 Oct 2025 21:52:47 GMT  
		Size: 20.0 KB (20025 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:55b114f5252af20f0b160f60b8e33dd28b0c979f9cd4f1223ff5b0ffa6c13045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69928250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d481af99da9494069c9116222dd4d7794083456e8e74cd739b338c7f28fbdc2e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOLANG_VERSION=1.25.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOTOOLCHAIN=local
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOPATH=/go
# Sat, 23 Aug 2025 03:19:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 03:19:59 GMT
COPY /target/ / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a288a79ca6a4350337b07c932262e8f347ed6880fe59b5563ac73c9f803137`  
		Last Modified: Tue, 07 Oct 2025 19:34:07 GMT  
		Size: 291.2 KB (291250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28977543608eb3d47060855462d9576fb750f3b4671b32d32fcc7f41fe2a4f4`  
		Last Modified: Tue, 07 Oct 2025 19:34:15 GMT  
		Size: 59.1 MB (59074083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1816d18ba2c391dce999f8d624e00e98d0750960159838ad5a758a1c823370d0`  
		Last Modified: Tue, 07 Oct 2025 19:34:07 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170a7711e720e61a5bea9c3e9f89d43f9b7cff046fdb448464ff7852495a7a29`  
		Last Modified: Tue, 07 Oct 2025 20:12:34 GMT  
		Size: 5.6 MB (5604533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37cd6cbc3ecaa5366265b2f2123fd3fc396bbd11f243ebbf65b2818815e3633`  
		Last Modified: Tue, 07 Oct 2025 20:12:31 GMT  
		Size: 1.7 MB (1738755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2a0ee9d76fad199709a7ed41987fed2b3a1328d22f52fe7a471b1d44816e92`  
		Last Modified: Tue, 07 Oct 2025 20:12:31 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:090872a581fa408bbcb6c36b988f85a4bf91ec6e9d77b041b9f7cfece1ae3499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 KB (303779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915116088f16b2607edef8699dce078a526f4daf9629312a3752f32988dad930`

```dockerfile
```

-	Layers:
	-	`sha256:19926eb98d13a1aa5d7d42a724a81a9c8ce3766554c90a492738310bbacbf158`  
		Last Modified: Tue, 07 Oct 2025 21:52:50 GMT  
		Size: 283.5 KB (283539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7acb47d7b9f091f502bbefcb2d9b1ddebe7f46211f298501aa5068160accaf25`  
		Last Modified: Tue, 07 Oct 2025 21:52:51 GMT  
		Size: 20.2 KB (20240 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:28c20c8d5c79bff85a1ecdf837438bb14cfe6d39577d09e1736333e030c48174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70050945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f64bf90acbf44558cd2643514517f920b14a9e7290622e76bb7eb2148d2af3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOLANG_VERSION=1.25.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOTOOLCHAIN=local
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOPATH=/go
# Sat, 23 Aug 2025 03:19:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 03:19:59 GMT
COPY /target/ / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caf2aa38194e3316af15efb06580b5313b6b61b78cf72e3b0e60a4f16867695`  
		Last Modified: Tue, 07 Oct 2025 19:34:24 GMT  
		Size: 294.2 KB (294173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66626199bcfab248906ccbdd0d977cc77ec2231a37f1710a42892109d86b2544`  
		Last Modified: Tue, 07 Oct 2025 19:34:30 GMT  
		Size: 57.6 MB (57647819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9329b66302da068245ed3133e27e7639b7a02a085eea51633dfcc2b5235878c`  
		Last Modified: Tue, 07 Oct 2025 19:34:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b583b391423c5f2cdf00c56a29e8223db59d8e39a0d51927768e24fa0344bea1`  
		Last Modified: Tue, 07 Oct 2025 20:12:28 GMT  
		Size: 6.3 MB (6261231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1896c4d7e6f8cb4114d3f54e0711a612f2c56eba974e387bc42ab3a48a3df1a1`  
		Last Modified: Tue, 07 Oct 2025 20:12:28 GMT  
		Size: 1.7 MB (1716381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981659c68f611dbe6c2ea8fba91db5ae7cb4eaac38ff210b2fe33d3450b16960`  
		Last Modified: Tue, 07 Oct 2025 20:12:27 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:447b6da8c0ce6c5d234988dc7c21df5d7f99dbd404333a71308b2767579d37bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 KB (300881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8611da94ba3561f3144275732519ec48c1182142d1f1cdd7abdbff7c0605b7d9`

```dockerfile
```

-	Layers:
	-	`sha256:5c60325b592b30ce07432c073988c1b49ceecad95190af6c4e50fbae26d4dd61`  
		Last Modified: Tue, 07 Oct 2025 21:52:54 GMT  
		Size: 280.6 KB (280599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0b0cb881f1d4cc1746c6affd041d1ade0d71b80981ad60e2720fe446b38bc4c`  
		Last Modified: Tue, 07 Oct 2025 21:52:55 GMT  
		Size: 20.3 KB (20282 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:bfd27c47f472adffc3c4b342bd11f75c44d66db2435ff4c4509f13542e0b3ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70413039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a643aa4a9d8707188dbdfc64bfc5c93b659470eab595533fd7d70095c1b8c748`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOLANG_VERSION=1.25.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOTOOLCHAIN=local
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOPATH=/go
# Sat, 23 Aug 2025 03:19:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 03:19:59 GMT
COPY /target/ / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaca2bbec3cff414f53adc5e9634f07a3fa7f1e3320dcbcc3b9d03910b13002d`  
		Last Modified: Mon, 06 Oct 2025 21:14:02 GMT  
		Size: 294.6 KB (294637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbab16c006e3e87a0bd86bfecf5ca21f23b4930a744517459433c08bfbfc59e0`  
		Last Modified: Tue, 07 Oct 2025 19:34:11 GMT  
		Size: 58.1 MB (58133794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fe88dcf3b18f587d64a41496f38d15ab3a9062aa436fbed7f50769b5a5117d`  
		Last Modified: Tue, 07 Oct 2025 19:36:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db3d6298b2f8a34ff2a490580e9c5ea2277eb347071a2ec6f1632325b583986`  
		Last Modified: Tue, 07 Oct 2025 20:28:06 GMT  
		Size: 6.6 MB (6550910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3c14c7bee57d4adc49ccce6ac034b13dcb5db867000c75647b217850ca8baf`  
		Last Modified: Tue, 07 Oct 2025 20:28:05 GMT  
		Size: 1.7 MB (1705995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fec154ff68a954f91b7bd72086666da7cd2388bc865261d0a25a10165a8c2d5`  
		Last Modified: Tue, 07 Oct 2025 20:28:05 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:1149c8da89183d39ed8f0a31f8caaaae75e95489a5a6342aeff9a583ce149bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 KB (298801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f390e23b0b41c71009cc5871a85ee36b3fabe5162c54c175ce2fa416f6680491`

```dockerfile
```

-	Layers:
	-	`sha256:969eb51652472e13fdd12f56aef9191d9b7e0c22cdca0aaf75e5c7166151115a`  
		Last Modified: Tue, 07 Oct 2025 21:52:58 GMT  
		Size: 278.6 KB (278616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4266f2f01d20f4f9f02587ce16e605d0cb56c8c1845365a8e76744b67a0bc91`  
		Last Modified: Tue, 07 Oct 2025 21:52:59 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; riscv64

```console
$ docker pull caddy@sha256:0fde6a6983fe51c0acb146b70eb8c8df63aa2bc912db989644f4f223de50d8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70576538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0464cc1a52bea2da627b70a70b28c91bee9bd256aeebd16f1e2366efbb7c71`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOLANG_VERSION=1.25.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOTOOLCHAIN=local
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOPATH=/go
# Sat, 23 Aug 2025 03:19:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 03:19:59 GMT
COPY /target/ / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cc4f79972d3401fde161bf76b9618d80cbd1ea7fcdbebdc630185f4cf612cd`  
		Last Modified: Tue, 07 Oct 2025 14:20:26 GMT  
		Size: 291.6 KB (291608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16d54fbaaf4f44943b5fd17aacabad20b0db0f29394c2b0f581a3a300b124c2`  
		Last Modified: Tue, 07 Oct 2025 19:40:12 GMT  
		Size: 58.7 MB (58670209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0eb0ec517215215e4738f4ed22dccbdd571638b449e06fb45910fe6c13bf32a`  
		Last Modified: Tue, 07 Oct 2025 19:43:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69d23250e929faa84021b94619116bd3d245f4b59453f1b9172309f0ea5f8da`  
		Last Modified: Tue, 07 Oct 2025 21:59:32 GMT  
		Size: 6.4 MB (6377120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ecbd34bf74a90b357655ba06e701f98148120c832975f78a0f26f1d93d585b`  
		Last Modified: Tue, 07 Oct 2025 21:59:32 GMT  
		Size: 1.7 MB (1724209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52857f9761fe43fb0c131c352f082b495d4cd959e4651c18ae99ea17e899675`  
		Last Modified: Tue, 07 Oct 2025 21:59:31 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3fd3f490dd581cadae05918741ee7b9fd4e06a249219588518ef0789c509a6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 KB (298796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cb3367c1fa6ae06bb44aebc276e6ec5e71f05f64300383031fec74acdb8029`

```dockerfile
```

-	Layers:
	-	`sha256:e6102514bee60ceb228d8c7e9d26aedbf6a0158de3052ace6739b4fdab282f28`  
		Last Modified: Wed, 08 Oct 2025 00:52:38 GMT  
		Size: 278.6 KB (278612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:620a83401f41c3e648853020bca837eb7ef9b9e651ba56af9d5272ddcaa6c030`  
		Last Modified: Wed, 08 Oct 2025 00:52:39 GMT  
		Size: 20.2 KB (20184 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:fe545b819b04e4631316e4d35f8a4ed024bc8b6ce28dc55a8beb0f49876cca24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71704662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837355b7ca8f1fadc32f483a8aaf771779498b1a09a21861f7599c6e500b70c6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOLANG_VERSION=1.25.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOTOOLCHAIN=local
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOPATH=/go
# Sat, 23 Aug 2025 03:19:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 03:19:59 GMT
COPY /target/ / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a4b5681964cbbac71727dc93824660a7b57f0fcfeb79eaa856084f3c55796e`  
		Last Modified: Mon, 06 Oct 2025 21:12:02 GMT  
		Size: 292.2 KB (292182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6429ba33a49b3f3080422ca98d26430f3e1c1ba8f8f41bc6d8af4cff9843f4da`  
		Last Modified: Tue, 07 Oct 2025 19:36:10 GMT  
		Size: 59.5 MB (59478805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cb90e3589cde6accb78ee3a4a577fbd3998fb696c061a079258149ad9758b6`  
		Last Modified: Tue, 07 Oct 2025 19:40:06 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b14013c99815ed3f97c915d71f33b5c259564001159d8f6b87a087316387c1c`  
		Last Modified: Tue, 07 Oct 2025 20:39:21 GMT  
		Size: 6.5 MB (6505260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaa8704567e642c9785b366700c077f06e5c3274bf0a2f34ea745b7a3eae6be`  
		Last Modified: Tue, 07 Oct 2025 20:39:20 GMT  
		Size: 1.8 MB (1782855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4ef5098c1fb46629cb880c4920744ba464d13d81bb9eb004f9d387bbc40cfb`  
		Last Modified: Tue, 07 Oct 2025 20:39:20 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:9a16a68f79c4215486319b7ade85e7889d5b478d28ffb5ddcffa57df6371b919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.7 KB (298659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5634305189bfd1996ae4dfeb59803421ba179809d452c543ffe03179f11e72e`

```dockerfile
```

-	Layers:
	-	`sha256:742a0a291c38881018fe3e966961c218e91ed740573431d58b25ceaa6ac39f40`  
		Last Modified: Tue, 07 Oct 2025 21:53:05 GMT  
		Size: 278.5 KB (278544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:262a602743c7ccde18939a7815658efb729575104661e09c5d5caf23ffc5cd8b`  
		Last Modified: Tue, 07 Oct 2025 21:53:06 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.26100.6584; amd64

```console
$ docker pull caddy@sha256:45612766f9a81d040ec6c38dcda8c0455f82675c787f46af642574668eda6fcf
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3687922565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beba592b60b4afe8e5dd88a965b2e75f33799aa9d07e1142c80b4cdb1a7d7096`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Tue, 07 Oct 2025 19:33:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Oct 2025 19:33:56 GMT
ENV GIT_VERSION=2.48.1
# Tue, 07 Oct 2025 19:33:57 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 07 Oct 2025 19:33:58 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 07 Oct 2025 19:33:58 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 07 Oct 2025 19:34:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 07 Oct 2025 19:34:33 GMT
ENV GOPATH=C:\go
# Tue, 07 Oct 2025 19:34:39 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Oct 2025 19:34:39 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:36:19 GMT
RUN $url = 'https://dl.google.com/go/go1.25.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c18b46f6aa44dbfcd54a9db19dd2fcc5ad684819addcfcf968aa75dad89a89c8'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 07 Oct 2025 19:36:20 GMT
WORKDIR C:\go
# Tue, 07 Oct 2025 20:11:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Oct 2025 20:11:31 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 07 Oct 2025 20:11:32 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 07 Oct 2025 20:11:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 07 Oct 2025 20:11:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 07 Oct 2025 20:11:40 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c930722fa7c27b5f2ebcabd1d48f0ae46ca0f73ac356015926639bd386b929`  
		Last Modified: Tue, 07 Oct 2025 19:45:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f28534faffd08baac64096bd10b6745e014b7345aa17e28356aa9db4ff8fcf8`  
		Last Modified: Tue, 07 Oct 2025 19:45:03 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829a0f666da6074e2b2d567760a1c76ed46b9da380d7ceadb553a8ff3e3c728b`  
		Last Modified: Tue, 07 Oct 2025 19:45:03 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec59792f5ba5dfb0c092b355a01157fa49d5881b9558abb40f0cbcf7e144c45`  
		Last Modified: Tue, 07 Oct 2025 19:45:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888bb4f563cdd2d81289f9ab878ad6566ef787bbae76c658fc98d85d3cb2598d`  
		Last Modified: Tue, 07 Oct 2025 19:45:04 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4ce5bd76392c952d3a401ad4ff2c1028c1cfaa77a6594dc331317b2e5a6097`  
		Last Modified: Tue, 07 Oct 2025 19:45:11 GMT  
		Size: 51.2 MB (51237312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccf4b274abdacf8985b388b8c531bcb842d9e84a3a790ecc872d9be15580667`  
		Last Modified: Tue, 07 Oct 2025 19:45:04 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5490d449e6678ba6cbc1af67fd8e2a19ea2e0e33e61e92de62454328c02474d`  
		Last Modified: Tue, 07 Oct 2025 19:45:04 GMT  
		Size: 353.2 KB (353221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3babdd19ee1f6f0d71eaf042b33d45818541c9f05cb69ea225a414f423538a1f`  
		Last Modified: Tue, 07 Oct 2025 19:45:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abb5f4d05f51b0eed124d4766c0914601db8a25f062531d1db8aed39da68eb4`  
		Last Modified: Tue, 07 Oct 2025 19:45:21 GMT  
		Size: 62.6 MB (62578590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b07091315c7619c64765c65e948733b3b88385392d329c100de65fcf269bc`  
		Last Modified: Tue, 07 Oct 2025 19:45:04 GMT  
		Size: 1.5 KB (1505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1699e8b8ec682fbfd5d7a69ad44d06ee2a7a6d9fa92c538d93183380abc31668`  
		Last Modified: Tue, 07 Oct 2025 20:12:07 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4a55ed9c24500af4d1b69c57e99fe8c8aabdd88acc1a21fd0af8ca4fd504e9`  
		Last Modified: Tue, 07 Oct 2025 20:12:07 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08082371c55bb8748e92920c154a9739b61d89eb49ef69cd48027b5f3a865a08`  
		Last Modified: Tue, 07 Oct 2025 20:12:07 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bdf4936d055887737af4dd9bdcf868c33ec70faeba6aa38a3979066820fa22`  
		Last Modified: Tue, 07 Oct 2025 20:12:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3991ee4ba1b9bc9782085d8a7cf422965b5e26f5434396f9da6f5b2a1ea7026`  
		Last Modified: Tue, 07 Oct 2025 20:12:07 GMT  
		Size: 2.3 MB (2296398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4713c6cdcce2284960a5122353d9e92f4db330eaf5bc65daf7a8cf3897e28fcc`  
		Last Modified: Tue, 07 Oct 2025 20:17:03 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.4171; amd64

```console
$ docker pull caddy@sha256:715492b0f944cd127eb6bbb8a4c0cc689f7707fa7a5e2b472fc6452b4f07b90d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2398610240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c6d1145422423f4bf0e98d89ef4f0a046b691c5549c52870927143d9f07d39`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Tue, 07 Oct 2025 19:34:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Oct 2025 19:34:31 GMT
ENV GIT_VERSION=2.48.1
# Tue, 07 Oct 2025 19:34:33 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 07 Oct 2025 19:34:34 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 07 Oct 2025 19:34:35 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 07 Oct 2025 19:35:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 07 Oct 2025 19:35:38 GMT
ENV GOPATH=C:\go
# Tue, 07 Oct 2025 19:35:44 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Oct 2025 19:35:44 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:37:16 GMT
RUN $url = 'https://dl.google.com/go/go1.25.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c18b46f6aa44dbfcd54a9db19dd2fcc5ad684819addcfcf968aa75dad89a89c8'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 07 Oct 2025 19:37:17 GMT
WORKDIR C:\go
# Tue, 07 Oct 2025 20:12:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Oct 2025 20:12:28 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 07 Oct 2025 20:12:28 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 07 Oct 2025 20:12:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 07 Oct 2025 20:12:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 07 Oct 2025 20:12:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84669fff65b3c9be81e40b9990f09af6d79236a36c89b48837a2c56193e23d4`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e60c3731686204945190028a490513225d391212a27fae945d09b2858d31e55`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715d31081e3081cc502401b5490ba7207796e551806afd0270bd8a99cd079aeb`  
		Last Modified: Tue, 07 Oct 2025 19:46:14 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0ae39107ec10a072379114022d2a65f0876026a506d6d97879b0690375ff5a`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448a9e7b99aa2b469a3ce0476da3574a6f1a3fd1a31ab60d087e3b241be8b602`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad8795f0cd8577898069910151345b5cceb653b95293f0e07bd3ef305d4b319`  
		Last Modified: Tue, 07 Oct 2025 19:46:21 GMT  
		Size: 51.2 MB (51222673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b85e42e9abcbae149b2e2d9b074fa1b76e74cd88f54622eaef24b9ea51ab81`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d664c422bbdd3f488f9b864b914e4867001ad3abd4164492dce75542a29e954`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 353.6 KB (353616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3564e813d9de7e1f20fa71a8b4a152f09f76719c04ba40966f67fbefadab5d`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02b4977a05998859250a8498907467403796eda2afc717329e301fd821c6f1b`  
		Last Modified: Tue, 07 Oct 2025 19:46:41 GMT  
		Size: 62.6 MB (62575489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fb0b5a044068825be258eb2d74f38322a83d5679674bb7247d7c482011f670`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd774b4fe59f6b1be84c9ca72d0ec51480732efec0d929ef8e9b38c2a3fc89dc`  
		Last Modified: Tue, 07 Oct 2025 20:13:06 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c00883df518d9fb471f8a5583a0e58e0373a64e003dc5396513f3f766eec53d`  
		Last Modified: Tue, 07 Oct 2025 20:13:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7881cce5aa1a5935de2405658071a0e5b1d9661b5487bc3c9aa9f53b6c5c10c1`  
		Last Modified: Tue, 07 Oct 2025 20:13:07 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b38591ce3e10db96fe64de0a8ebc6f65514f302b2028d68b100a86fadde6d60`  
		Last Modified: Tue, 07 Oct 2025 20:13:07 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aececf11534a88cf9a95165200a3a9f75ba72ec567775b4df9c7d596afc439f5`  
		Last Modified: Tue, 07 Oct 2025 20:13:07 GMT  
		Size: 2.3 MB (2296303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efede2e44e94f6e665f2ecf900a0cd611dff2a029759937c9b5a480d4b3df131`  
		Last Modified: Tue, 07 Oct 2025 20:13:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

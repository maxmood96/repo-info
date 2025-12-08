## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:5fd6c969b828a4ccfd18767fd0420507d1c36f1d0a8c217805268a4825b78fb7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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

### `caddy:2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:a834adfae397315e2c95f6b7862f527d1b2a6403b9fd79bd357fb0e9ae2ba3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72330949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258c6bbd204571a9b50ac7555116546433a8fc75bbb42b71e5184c95a52ba45c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 17:47:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:47:12 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:47:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:47:12 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:47:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:47:12 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:47:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:47:14 GMT
WORKDIR /go
# Tue, 02 Dec 2025 18:11:29 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 02 Dec 2025 18:11:29 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Dec 2025 18:11:29 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 02 Dec 2025 18:11:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Dec 2025 18:11:29 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Dec 2025 18:11:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Dec 2025 18:11:29 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Dec 2025 18:11:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cca2393419fe3a74cd2335a6f38c974ac4018810e984e58d4eb9f8504e71be1`  
		Last Modified: Tue, 02 Dec 2025 17:47:38 GMT  
		Size: 291.2 KB (291156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c445a0e108b509dd422d6adce512f16cb7edd37814e8e3509850820377bcf06`  
		Last Modified: Tue, 02 Dec 2025 17:47:39 GMT  
		Size: 60.2 MB (60151314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09615bee918a0a1913f982926164fe321067b4ae8a2bd5e632e16e062e052073`  
		Last Modified: Tue, 02 Dec 2025 17:47:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8c96573e700f65b0d360162f4d2161869123099dea8f91e451988309e767e`  
		Last Modified: Tue, 02 Dec 2025 18:11:42 GMT  
		Size: 6.2 MB (6238929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5017942da129d6bb1eb5e21e7a7eea419a8ce1d76aecc29d7354f6262e893b`  
		Last Modified: Tue, 02 Dec 2025 18:11:41 GMT  
		Size: 1.8 MB (1846506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1a6385d5ae2abe06a0906be396a908a3411aabeb8e84337f666144ae3f779d`  
		Last Modified: Tue, 02 Dec 2025 18:11:41 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:55321f971ec016b2ec7a702d70b160a459e0c7c05f0daf5ecedc7f296fb00ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 KB (299483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0311fbbee13e14a6af2e89113b344a4bd388ae758694807a0617c0c31ab49552`

```dockerfile
```

-	Layers:
	-	`sha256:66bb8c9a34684a60486d1423ef5921aee7eb2b6e0d00b9004085aee23e16c95e`  
		Last Modified: Tue, 02 Dec 2025 19:52:46 GMT  
		Size: 279.4 KB (279412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:573c722c698d70c0070ae3f104d888b1703e8a4e35f39131d62d33cef9e876ca`  
		Last Modified: Tue, 02 Dec 2025 19:52:47 GMT  
		Size: 20.1 KB (20071 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:16cebfd04e73412e0d7bd90ba5e758e17acaa432ed71c67d3a60a0ed18a10064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70767745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9915e55fc9e50a94fe5798cab53f6e89bc4e6adc9fa4bcca15be6c512b4a3412`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 17:46:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:47:35 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:47:35 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:47:35 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:47:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:47:35 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:47:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:47:37 GMT
WORKDIR /go
# Tue, 02 Dec 2025 17:53:55 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Dec 2025 17:53:55 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 02 Dec 2025 17:53:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Dec 2025 17:53:55 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Dec 2025 17:53:56 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Dec 2025 17:53:56 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018d563333bae8e633faf8bab936767992815a7a24d1f1c4c31fb84f26f383a2`  
		Last Modified: Tue, 02 Dec 2025 17:47:58 GMT  
		Size: 292.3 KB (292303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43dd4211ee5273ca0c5772840c1a03b86bde39c606d1c608d88cc81d6d76501`  
		Last Modified: Tue, 02 Dec 2025 17:47:55 GMT  
		Size: 59.1 MB (59071955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5368840f9d54bdcc8859d425dd09f7810866f7c939caf326919e8738ca36bb`  
		Last Modified: Tue, 02 Dec 2025 17:47:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc1b09b93b3274228cfe6ba3cebdd6de634ed3568d9bf1fd85932364d5d0bf6`  
		Last Modified: Tue, 02 Dec 2025 17:54:09 GMT  
		Size: 6.2 MB (6153812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3b0c2d5691a488a279f7d314b3f1a30e423a8b39bc4c940bbe91065cd1560e`  
		Last Modified: Tue, 02 Dec 2025 17:54:09 GMT  
		Size: 1.7 MB (1745003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c225b68159fd1187f8cf3273c1cc0e8c0d8863faa2a9f39a2ab66f6f7c2358cb`  
		Last Modified: Tue, 02 Dec 2025 17:54:09 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:16a1ef3bea71242faf318abfb56399e77b18445e94580eacb485feb57af12146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (19982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77d401a61882bbb02125983d553e57e9975ba1db3235b98ffb77e2dae743866`

```dockerfile
```

-	Layers:
	-	`sha256:16383fe11f1c432eaa133592a2d6ac32f762e6624754b79e20c378ef9a1f787c`  
		Last Modified: Tue, 02 Dec 2025 19:52:50 GMT  
		Size: 20.0 KB (19982 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:e8c0d23d0665a61b972f0be294f2364a2b71dc1d6a70ee66c69622b543bc4d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69953208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36171d95f9b4235dbe4d6d6b57dfea6b254792b8b41bc191e0908c3938f443e9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 17:48:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:48:36 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:48:36 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:48:36 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:48:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:48:36 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:48:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:48:38 GMT
WORKDIR /go
# Tue, 02 Dec 2025 17:53:43 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 02 Dec 2025 17:53:44 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Dec 2025 17:53:44 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 02 Dec 2025 17:53:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Dec 2025 17:53:44 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Dec 2025 17:53:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Dec 2025 17:53:44 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Dec 2025 17:53:44 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c503d8216e3d83c88f2e6fa55a973a50afa1ea035ad31e9d6a22606d88f7ea`  
		Last Modified: Tue, 02 Dec 2025 17:49:16 GMT  
		Size: 291.2 KB (291216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952f3ceca6918c986252a293f498004b3365bf2efd3e1b6be9d754f9e7c62cfe`  
		Last Modified: Tue, 02 Dec 2025 17:49:21 GMT  
		Size: 59.1 MB (59072062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24644c9c8d72b7eeaac69d4fd6498522e17774698cf1d50b5fd84284b60cf43`  
		Last Modified: Tue, 02 Dec 2025 17:49:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e58138cf5d9b4497c6823f7b1bb0f6d38f0dd7773883559a3dcdc01c5ee464`  
		Last Modified: Tue, 02 Dec 2025 17:53:59 GMT  
		Size: 5.6 MB (5629019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ebc84cd9cfb041d2bc4b45685d250e348f99eef96cfcd91b07985c701ff849`  
		Last Modified: Tue, 02 Dec 2025 17:53:59 GMT  
		Size: 1.7 MB (1738762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658ab19acefb6d9446c4eb855df4cdae421612a9b988d7b353f8a2a3a2f98111`  
		Last Modified: Tue, 02 Dec 2025 17:53:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:6b0fea91279ff349872a9a7d5053c928cc3b7b80db29eed176a6c2ff94293f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 KB (302653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0590b3ea8d9af1309490c0b9451c9f43fb5f6be8dea449e87a7ca3cb4371b1a`

```dockerfile
```

-	Layers:
	-	`sha256:6fd703da5f4153b30dac078ecf96bffc5cd631f6db81b8c835592f18e8fc3a61`  
		Last Modified: Tue, 02 Dec 2025 19:52:53 GMT  
		Size: 282.5 KB (282456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9200125f7c97fb83e6cf5c0297555ed7f98ebc7a67de180e4543b230d07cdc6f`  
		Last Modified: Tue, 02 Dec 2025 19:52:54 GMT  
		Size: 20.2 KB (20197 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:d4b709804a5eb8e745b6a2a3c8626cf97fa5bc0de00c05fe14400a669274e251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70090608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f08ccf21d029e70d077521c53bc3524e9afc1d313c371f8b9a1e0d9ce8e54d9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 17:47:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:47:18 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:47:18 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:47:18 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:47:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:47:18 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:47:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:47:20 GMT
WORKDIR /go
# Tue, 02 Dec 2025 17:53:51 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 02 Dec 2025 17:53:52 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Dec 2025 17:53:52 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 02 Dec 2025 17:53:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Dec 2025 17:53:52 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Dec 2025 17:53:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Dec 2025 17:53:52 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Dec 2025 17:53:52 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1cfd108ccaf6f7d493ade1fc03b1d84d7ee4dfb9aa1572d2e2701af0cf91a1`  
		Last Modified: Tue, 02 Dec 2025 17:47:56 GMT  
		Size: 294.1 KB (294111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0562e970c9af953828c5cdc69b3e362c523c3064c669aa8dda79020032e840`  
		Last Modified: Tue, 02 Dec 2025 17:48:05 GMT  
		Size: 57.7 MB (57650917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f7ff8173cdfbdd6ef409a95240bce9a61c2cd8cea2f9896f405a86dbf6a54c`  
		Last Modified: Tue, 02 Dec 2025 17:47:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2a8398e1a4a827999919a8b58f9ab5c482b6965602373d227c423845184144`  
		Last Modified: Tue, 02 Dec 2025 17:54:10 GMT  
		Size: 6.3 MB (6290538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4750492091e0574a0246f6daaaf99280dc91f1883f52b70d96e9582073f5ca08`  
		Last Modified: Tue, 02 Dec 2025 17:54:09 GMT  
		Size: 1.7 MB (1716383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4ebd1b229fd9a1f96a9d6442fd624d61b6d70349812b96bf6813790deb19e2`  
		Last Modified: Tue, 02 Dec 2025 17:54:10 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:bf1603db0366185051747d693124e17dd8e8c9a87eb711d6127be6037cdc7d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 KB (299754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82af0327a0a27020f824ec56e4b5a4fbad47d19705812af07632c7c3e7ab980e`

```dockerfile
```

-	Layers:
	-	`sha256:afa52fb9fa03f9f86bf997fefc84051d687a6703e4703897a73be3a44cf24334`  
		Last Modified: Tue, 02 Dec 2025 19:53:02 GMT  
		Size: 279.5 KB (279516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb183ad2cc2d3d951ea9eb8695c9bf75e71f377c3653d3df21efa42f58b16919`  
		Last Modified: Tue, 02 Dec 2025 19:53:03 GMT  
		Size: 20.2 KB (20238 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:7fe72e4f84420bf0ad62cc0bf9f41ebafc54624ae560ad1cb6769da0809af0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70448302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdfc78c34dc474038901e124323d784ce6b4012a7874e18796c2a543baa647bc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:43:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:46:09 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:46:09 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:46:09 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:46:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:46:09 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:48:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:48:50 GMT
WORKDIR /go
# Tue, 02 Dec 2025 18:03:11 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 02 Dec 2025 18:03:12 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Dec 2025 18:03:12 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 02 Dec 2025 18:03:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Dec 2025 18:03:12 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Dec 2025 18:03:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Dec 2025 18:03:13 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Dec 2025 18:03:13 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64958bce21ae47528776dd8bd6794140e1f5086c72ae8807ba8f48bb37fce769`  
		Last Modified: Mon, 24 Nov 2025 22:43:59 GMT  
		Size: 294.6 KB (294592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0da503e4b3d4a624ac596179648e9a31a4f87f7d37fdb8c7bef57190d6ed7d`  
		Last Modified: Tue, 02 Dec 2025 17:48:12 GMT  
		Size: 58.1 MB (58134946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fe3074abc6346584ebb7d175a96261ddfaf687149e8a47e8c83b0d8c9e1691`  
		Last Modified: Tue, 02 Dec 2025 17:49:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507a418cbf96acbbd99e7dde60aa1e7d1ebe60046dc7a597f01e8f3548c77f07`  
		Last Modified: Tue, 02 Dec 2025 18:03:55 GMT  
		Size: 6.6 MB (6579938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944c052f9491e8f59022f547ffd58d2167c72cf4c3f84340550856494ecf2810`  
		Last Modified: Tue, 02 Dec 2025 18:03:55 GMT  
		Size: 1.7 MB (1705993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c7d5ac87c3f9eb9030e21bb332aa98e8eb8ca6cc1fb159dc418d12eedf2427`  
		Last Modified: Tue, 02 Dec 2025 18:03:54 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:52767a417d350f03d34e81eb8d6c6b9dd74432f7adcfd490058cee4a35e1d536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 KB (297675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e535ae7a1f5372187b2eebef5da548596d4eac5427c3f3a36e2ade761e796a1`

```dockerfile
```

-	Layers:
	-	`sha256:1533ada75b956be681a439e223ced2743a3f93f07cf499594a2dba4b9fccc81d`  
		Last Modified: Tue, 02 Dec 2025 19:53:07 GMT  
		Size: 277.5 KB (277533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd82d8fdd260572a0f76ed1d23267e11e97f807d6c69aed00c57f4ee75f7034d`  
		Last Modified: Tue, 02 Dec 2025 19:53:07 GMT  
		Size: 20.1 KB (20142 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:94446f1b948644e339625b04d36bfee884f2b497bb10c3df4ac80f800eed1437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70600188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4cbe9ed08ca9800aa17d567cc7b5623d0b559f1ac57911d88577160bd78eba`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 07:20:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:47:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:47:21 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:55:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:55:48 GMT
WORKDIR /go
# Tue, 02 Dec 2025 20:25:32 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 02 Dec 2025 20:25:34 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Dec 2025 20:25:34 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 02 Dec 2025 20:25:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Dec 2025 20:25:34 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Dec 2025 20:25:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Dec 2025 20:25:34 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Dec 2025 20:25:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a984176d166c6f9d398140e2c603deed3f1a52311d2a418b830c1cfdaffb3c`  
		Last Modified: Tue, 25 Nov 2025 07:22:38 GMT  
		Size: 291.5 KB (291523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f6199a15922cf0533082f2bfb9bf03dc54fb7fdb4f830e8dae324efa57d8b9`  
		Last Modified: Tue, 02 Dec 2025 17:54:10 GMT  
		Size: 58.7 MB (58672443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dece81b84dd08929374b6e8e9e38b7015785ac31adf38602fb02b1dbd442d0ce`  
		Last Modified: Tue, 02 Dec 2025 17:57:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126003ba150c1d5c3ec1cc51aedbdad1ff2ebf9cc0346d5c6a5fdd1d040e342`  
		Last Modified: Tue, 02 Dec 2025 20:26:55 GMT  
		Size: 6.4 MB (6396184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeb197d3bfdc8bb806a9021109891a57c69fa39569a30c23c297202ed71e065`  
		Last Modified: Tue, 02 Dec 2025 20:26:54 GMT  
		Size: 1.7 MB (1724207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41546e4c12ec170a76a9f2e04e2c0eb7f230662517ed451e92d5205f26adcd3d`  
		Last Modified: Tue, 02 Dec 2025 20:26:55 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:292e1b44a7b48d3c100f5cd9b786cfa30d1ea6dd902c3d27792c33f984758965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 KB (297671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3ed4c766112c346341ef2ea370fcb59c276aa431a7cff99ca97c7cdef3ee21`

```dockerfile
```

-	Layers:
	-	`sha256:f3b3ab1c4b1ae7d0dc06a93a06151880fb6d4a385b5f0c30139001e4e02eb78b`  
		Last Modified: Tue, 02 Dec 2025 22:52:32 GMT  
		Size: 277.5 KB (277529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a57413cc0ec68e6250d1502ca3e0e071b769f341d9aa645aeea01e235aeadb7`  
		Last Modified: Tue, 02 Dec 2025 22:52:33 GMT  
		Size: 20.1 KB (20142 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:615ab708912200b1739267052386e6e5e410bf09de687ed7409dc29c37263466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71742561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb59cfabb0827d324a96c8a228170531ad467a6b652f5fb1b794fb2824d81d8b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:37:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:48:28 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:48:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:48:28 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:48:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:48:28 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:48:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:48:33 GMT
WORKDIR /go
# Tue, 02 Dec 2025 18:01:36 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 02 Dec 2025 18:01:38 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Dec 2025 18:01:38 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 02 Dec 2025 18:01:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Dec 2025 18:01:38 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Dec 2025 18:01:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Dec 2025 18:01:38 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Dec 2025 18:01:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94177cc1b10be488b5d187dad00f1ccc030bc5cd416e55c943d85498ded2fbfe`  
		Last Modified: Mon, 24 Nov 2025 22:38:27 GMT  
		Size: 292.1 KB (292150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036b6dba2ceabbb92eb6c9ebccd3e6b705dacf7cc4426156bbedfd17ad5dc53b`  
		Last Modified: Tue, 02 Dec 2025 17:49:47 GMT  
		Size: 59.5 MB (59487220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d419ba7d33a7aff89f4f162d7f80f73a4b62020a51e81530406474b71e63be`  
		Last Modified: Tue, 02 Dec 2025 17:49:42 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e812e33bbe640ef80e4bd1d6910458535194517187aa8141a259d4087077646`  
		Last Modified: Tue, 02 Dec 2025 18:02:06 GMT  
		Size: 6.5 MB (6530501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f087750e05991089cb1fd8e4cba2a14460b865e19b2f8b8325437c3b8ed0b5`  
		Last Modified: Tue, 02 Dec 2025 18:02:05 GMT  
		Size: 1.8 MB (1782855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397aacf75a4f7961aac3f2c54ddc13dfc2857f7a00febe10bc7a2648f3da559e`  
		Last Modified: Tue, 02 Dec 2025 18:02:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a8c5994027a61e8860f017aed90837a87ee3434a91cc17639f39f3cb6ee57615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 KB (297533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb541cfe3f58dd827a95393ba584eb40af9dbf61f0adc07dbf99fbf4226abb1a`

```dockerfile
```

-	Layers:
	-	`sha256:f84cda1fd66fb95148cdb8df8e7db4207232061f0b4c6f4ae8b554e11e3982a1`  
		Last Modified: Tue, 02 Dec 2025 19:53:14 GMT  
		Size: 277.5 KB (277461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:936c23c8e417a315213248aad810830a9fdd58a24b9623eb2879e3ef2c753dc6`  
		Last Modified: Tue, 02 Dec 2025 19:53:15 GMT  
		Size: 20.1 KB (20072 bytes)  
		MIME: application/vnd.in-toto+json

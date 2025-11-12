## `caddy:2-builder`

```console
$ docker pull caddy@sha256:6e3ed727ce8695fc58e0a8de8e5d11888f6463c430ea5b40e0b5f679ab734868
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
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:b7d6df3503422505e805655b0242134641f90bab239557cc35542945d3a18d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72331543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488c9f1bc07779b6c1f18dcde1100a251aa73df7d950ca0b0ea5b33840645c96`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 20:18:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 20:17:49 GMT
ENV GOLANG_VERSION=1.25.4
# Wed, 05 Nov 2025 20:17:49 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 20:17:49 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 20:17:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 20:17:49 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 20:18:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 20:18:33 GMT
WORKDIR /go
# Wed, 05 Nov 2025 21:12:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 05 Nov 2025 21:12:21 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 05 Nov 2025 21:12:21 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 05 Nov 2025 21:12:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 05 Nov 2025 21:12:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 05 Nov 2025 21:12:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 05 Nov 2025 21:12:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 05 Nov 2025 21:12:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005175e490b0ff92097d506946bbecbb38ca5479503236dcb3350f2da29b1cb`  
		Last Modified: Wed, 05 Nov 2025 20:18:45 GMT  
		Size: 291.2 KB (291160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9d4a4eea0de466b378fec1876ea74acd9465fc6a1d15368a117eeacaa21b7d`  
		Last Modified: Wed, 05 Nov 2025 20:18:32 GMT  
		Size: 60.2 MB (60151871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae96bccb6682de86f077a4ef76a3024218e06114ae177db9ad565f2be5a0e423`  
		Last Modified: Wed, 05 Nov 2025 20:18:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4294e4720bec219ca584a6f95adf5264b5e3adb01a5fd94b229b74dcbc5373ab`  
		Last Modified: Wed, 05 Nov 2025 21:12:35 GMT  
		Size: 6.2 MB (6238966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f51a717d61b468d33d694865c5e34abcd32ce5cfbd5a641ece068e385b5d9d`  
		Last Modified: Wed, 05 Nov 2025 21:12:34 GMT  
		Size: 1.8 MB (1846503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad13a2cdea7cd91b7d6b0ddbc058cd262f694df241fac9815ac1f5033f3abe88`  
		Last Modified: Wed, 05 Nov 2025 21:12:34 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:509a3e75a2ed037fb5b4e810d6fe8a43343a391c54ef7aee22f954a90f9c3ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 KB (299484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b15770c2f5661a5d2722ebfe434dd479fe25a437ead6d770b48219a842e76e2`

```dockerfile
```

-	Layers:
	-	`sha256:9b75e5dd3a94e2ef24ea66bad7d2e9fc72aedfd3f3a36a104a909208f2858d44`  
		Last Modified: Wed, 05 Nov 2025 22:52:49 GMT  
		Size: 279.4 KB (279412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:777cab13277301ca5dd1af82206eb3ac1599fcfc665966ff523ca99f0bb0fd30`  
		Last Modified: Wed, 05 Nov 2025 22:52:50 GMT  
		Size: 20.1 KB (20072 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:6b8a708359e0e712556977f70f4743dd09b0e271c60e6f4a9353ce30079a1968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70767807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3265db8f46a99368607dd8d06e7540c3f39cedec2793892ed833c0f9eb02b1e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 20:15:04 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 20:15:22 GMT
ENV GOLANG_VERSION=1.25.4
# Wed, 05 Nov 2025 20:15:22 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 20:15:22 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 20:15:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 20:15:22 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 20:15:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 20:15:24 GMT
WORKDIR /go
# Wed, 05 Nov 2025 21:15:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 05 Nov 2025 21:15:20 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 05 Nov 2025 21:15:20 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 05 Nov 2025 21:15:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 05 Nov 2025 21:15:20 GMT
ENV XCADDY_SETCAP=1
# Wed, 05 Nov 2025 21:15:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 05 Nov 2025 21:15:20 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 05 Nov 2025 21:15:20 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07afe75e6854373e30caf12c0d6e46cce3030ab72c031b93f11155b2e58891f3`  
		Last Modified: Wed, 05 Nov 2025 20:15:46 GMT  
		Size: 292.3 KB (292317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82229606d045e3bf5b3d666cc06b953ca48f62773919b720b3dfdeb45e64bc8e`  
		Last Modified: Wed, 05 Nov 2025 20:15:52 GMT  
		Size: 59.1 MB (59072045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e302011fea114ca069efc60577762159427692541e9be15f7af04f1b6c3a8b70`  
		Last Modified: Wed, 05 Nov 2025 20:15:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a62653d3eee0a56622a261db5953da25731a1ed1eccce31de44ee2c095257a`  
		Last Modified: Wed, 05 Nov 2025 21:15:33 GMT  
		Size: 6.2 MB (6153773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43be9a6385c3398e1a094b42a9c6e099ef994357967d33bff9da50102aee9de7`  
		Last Modified: Wed, 05 Nov 2025 21:15:31 GMT  
		Size: 1.7 MB (1745000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4de0866b834cdb07b0cccf6a2677affe19ef2cb39a03cee58182a2b382f0bc5`  
		Last Modified: Wed, 05 Nov 2025 21:15:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:35100a7355d5020363f2e131ef422de1d64857c99339ab978d538145c7268a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (19982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266a6d20866584afad468aa705bb6696df11c2d7ea69d632f976642ef1cadc22`

```dockerfile
```

-	Layers:
	-	`sha256:b9b3e07cfff5014b555277c2c2d5e61e682fb134559a39eed861918b6a190e2c`  
		Last Modified: Wed, 05 Nov 2025 22:52:54 GMT  
		Size: 20.0 KB (19982 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:b24913a950c825efafe37714cbe2d71e6899901d3d035aade3c40b12f0967d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69953323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94359de609d59b94b0e0428ace3986eaee137c4fb250246e3081b94597d787c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 20:17:08 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 20:17:32 GMT
ENV GOLANG_VERSION=1.25.4
# Wed, 05 Nov 2025 20:17:32 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 20:17:32 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 20:17:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 20:17:32 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 20:17:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 20:17:35 GMT
WORKDIR /go
# Wed, 05 Nov 2025 21:12:25 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 05 Nov 2025 21:12:26 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 05 Nov 2025 21:12:26 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 05 Nov 2025 21:12:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 05 Nov 2025 21:12:26 GMT
ENV XCADDY_SETCAP=1
# Wed, 05 Nov 2025 21:12:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 05 Nov 2025 21:12:26 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 05 Nov 2025 21:12:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1cbd4d00de10f1ccd8e9cd575f313cf0834eaf5e9a79f150a6890d42f5bc98`  
		Last Modified: Wed, 05 Nov 2025 20:17:54 GMT  
		Size: 291.2 KB (291214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005e5e3f870b603812d4e2b76f2d3cd35fb32a7d8a09fbbc4d31d3610a5033ab`  
		Last Modified: Wed, 05 Nov 2025 20:17:33 GMT  
		Size: 59.1 MB (59072180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a246aed21745c7139016120f286dc8eac916f4e8188ded36960e3ef1f52507d`  
		Last Modified: Wed, 05 Nov 2025 20:17:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a74136ed5344ba2aacf62a6dd33b4aa92c18c4fa46c6647ee7c9a669002877d`  
		Last Modified: Wed, 05 Nov 2025 21:12:46 GMT  
		Size: 5.6 MB (5629033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994bda66fe97569e887cca7dca13155499070bb928b4a772fe3107913e7a2522`  
		Last Modified: Wed, 05 Nov 2025 21:12:46 GMT  
		Size: 1.7 MB (1738751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834bca14a5cb705d3e5cacd4f95af7a8910d1b897aeb0d2a1912c9381d04fe25`  
		Last Modified: Wed, 05 Nov 2025 21:12:45 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:ec7e834e2a96c75616d972023f261e5a680e568d85f5086b1f837cdff6050444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 KB (302653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68599b310340d415f982e09a366ac1991ff1f374ee8a980710c03309abe32f8d`

```dockerfile
```

-	Layers:
	-	`sha256:204df3df0c31937b59ef98c59accaebf091729c9e9139a7925d87b6c33a872b6`  
		Last Modified: Wed, 05 Nov 2025 22:52:57 GMT  
		Size: 282.5 KB (282456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a02c1e0bbe3a84db7b11f8db4226b01996646980eb3052ff84b1de3c46d659fc`  
		Last Modified: Wed, 05 Nov 2025 22:52:58 GMT  
		Size: 20.2 KB (20197 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:e5e46d18ced024abe5e3c31d9b2728b1e24f450f5bfdec98dcbe424c1151919a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70091330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a93be93e53d451aef5f4dd58ebd748d2757d851d84559642701cebc73616b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 20:20:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 20:20:36 GMT
ENV GOLANG_VERSION=1.25.4
# Wed, 05 Nov 2025 20:20:36 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 20:20:36 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 20:20:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 20:20:36 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 20:20:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 20:20:38 GMT
WORKDIR /go
# Wed, 05 Nov 2025 21:13:36 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 05 Nov 2025 21:13:36 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 05 Nov 2025 21:13:36 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 05 Nov 2025 21:13:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 05 Nov 2025 21:13:36 GMT
ENV XCADDY_SETCAP=1
# Wed, 05 Nov 2025 21:13:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 05 Nov 2025 21:13:36 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 05 Nov 2025 21:13:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f1ad36a5a83c5a5f7482a06aefd78ca2e2c575913005ca05bbcf64fec9b080`  
		Last Modified: Wed, 05 Nov 2025 20:20:57 GMT  
		Size: 294.1 KB (294093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0cd0526a95aa822822b8c4a246e8d3cb0ad0abd58b11c3ff2e34a74e1ffe9b`  
		Last Modified: Wed, 05 Nov 2025 20:19:33 GMT  
		Size: 57.7 MB (57651672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b381f593327825af561f9a2d04f44104c8ad3ae820768cbd9a7acbed30f1fac5`  
		Last Modified: Wed, 05 Nov 2025 20:20:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f22bf86bcc9916a35615636c33214ea80eaed0429f1be527888ace0e3fa882f`  
		Last Modified: Wed, 05 Nov 2025 21:13:50 GMT  
		Size: 6.3 MB (6290519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9c8f376c8388ff4d82039296cf805780abef946af0837b9e31240c5d61bdca`  
		Last Modified: Wed, 05 Nov 2025 21:13:49 GMT  
		Size: 1.7 MB (1716385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981ace2b1abe8673b336fa16bbebff46c8c356395e9a577ca34e734273fd7981`  
		Last Modified: Wed, 05 Nov 2025 21:13:49 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:059c6491a8ba86162a7ff5edf6fab07c8495de6d2a5656dd26c57e159935e82e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 KB (299755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c986bc8a04a74c3f4d3b997e706a10b43e67bbc3c777e21cfa893ed065d157a7`

```dockerfile
```

-	Layers:
	-	`sha256:cf5dc752586ba56e4379b637f15ed704c2207bcaa763a6096958e8320ea32089`  
		Last Modified: Wed, 05 Nov 2025 22:53:01 GMT  
		Size: 279.5 KB (279516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ddf0643ebf28aced474ce8f90377befaa9bc6243e4dbc8b2fed6d22d2b73b60`  
		Last Modified: Wed, 05 Nov 2025 22:53:02 GMT  
		Size: 20.2 KB (20239 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:2e8c827e2da035afd5369be502762ae7e282a61ee193991b02814ca5f304f581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70446500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a798509e325c15b98db314e5678253ea425d0123e090b512881f662d3ca63172`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:17:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 20:14:57 GMT
ENV GOLANG_VERSION=1.25.4
# Wed, 05 Nov 2025 20:14:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 20:14:57 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 20:14:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 20:14:57 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 20:18:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 20:18:04 GMT
WORKDIR /go
# Wed, 05 Nov 2025 21:24:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 05 Nov 2025 21:24:29 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 05 Nov 2025 21:24:29 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 05 Nov 2025 21:24:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 05 Nov 2025 21:24:29 GMT
ENV XCADDY_SETCAP=1
# Wed, 05 Nov 2025 21:24:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 05 Nov 2025 21:24:30 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 05 Nov 2025 21:24:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c8bd62217b855f213063830cb5c2b3ccc4717b8ba91afea33b4f12c5e23dcc`  
		Last Modified: Mon, 03 Nov 2025 18:18:26 GMT  
		Size: 294.6 KB (294587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2470fe8e729e39478adbcf0e2206e2b0fe316cbf8e73d84d0bf464e839a1aa00`  
		Last Modified: Wed, 05 Nov 2025 20:16:13 GMT  
		Size: 58.1 MB (58133115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0834934dea77468ae0e5189e36b259141d724ddc3580509a4fa1548db653bef9`  
		Last Modified: Wed, 05 Nov 2025 20:18:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6487a575ff2a1e1f86491deab314df033cdaccb7df4919cf01b9915558608e`  
		Last Modified: Wed, 05 Nov 2025 21:24:57 GMT  
		Size: 6.6 MB (6579973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a840beb9e151c160a60f3501a2b563f150eda8b13232dcf305227e3b655201`  
		Last Modified: Wed, 05 Nov 2025 21:24:56 GMT  
		Size: 1.7 MB (1705993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d565b655d81bbd6fd7780a4a430e73154ae9eec9b48eeb58050461c5ef331141`  
		Last Modified: Wed, 05 Nov 2025 21:24:56 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3136f9fb165432c63fb0fa4237583c1e0d7ec64ae0fe5d9eceb44213e4053a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 KB (297675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54759e840bd7f86189e485c1eeaff00316084f38a6a1ef91eb174830f86cac47`

```dockerfile
```

-	Layers:
	-	`sha256:23e44129b9b860735d2c7acfc7bb06fea1eea3034443c6aeb3301a708db09686`  
		Last Modified: Wed, 05 Nov 2025 22:53:06 GMT  
		Size: 277.5 KB (277533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24e418c5d3fdf438ae519695d89bdba56118111d08814c76b5fe6c7baa119b4a`  
		Last Modified: Wed, 05 Nov 2025 22:53:07 GMT  
		Size: 20.1 KB (20142 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; riscv64

```console
$ docker pull caddy@sha256:968a5b033bbd8e8e661149845b1fdbe52f0358e719678c82d57c6c408a37c254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70596782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c585767f0fee2dde6acdd1f7f243001c004918b8b06725fbadcd75cd0a0439`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 10 Oct 2025 21:01:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 06 Nov 2025 10:41:10 GMT
ENV GOLANG_VERSION=1.25.4
# Thu, 06 Nov 2025 10:41:10 GMT
ENV GOTOOLCHAIN=local
# Thu, 06 Nov 2025 10:41:10 GMT
ENV GOPATH=/go
# Thu, 06 Nov 2025 10:41:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Nov 2025 10:41:10 GMT
COPY /target/ / # buildkit
# Thu, 06 Nov 2025 10:41:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 06 Nov 2025 10:41:28 GMT
WORKDIR /go
# Sat, 08 Nov 2025 07:46:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 08 Nov 2025 07:47:00 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 08 Nov 2025 07:47:00 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 08 Nov 2025 07:47:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 08 Nov 2025 07:47:00 GMT
ENV XCADDY_SETCAP=1
# Sat, 08 Nov 2025 07:47:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 08 Nov 2025 07:47:00 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 08 Nov 2025 07:47:00 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2055b904ba40ebefe03b802bf4885ac2708bb5c47a4294058815bff9a5ca3b`  
		Last Modified: Fri, 10 Oct 2025 21:04:20 GMT  
		Size: 291.5 KB (291511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4cca360a3248a39ae972bdd0361d5418adbfd7b32f2db3f769eda57df020d0`  
		Last Modified: Thu, 06 Nov 2025 10:44:12 GMT  
		Size: 58.7 MB (58669059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c9be576fbd7c4c196b61d3bf9d9a8cac7ab6dfa860cd11eb06c845b42a41d7`  
		Last Modified: Thu, 06 Nov 2025 10:44:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e57cf70d68a2459b91f3c8ec6e516e6d6b04b0af0d422a7b44cb537744abdb`  
		Last Modified: Sat, 08 Nov 2025 07:48:21 GMT  
		Size: 6.4 MB (6396165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19b6a1518b51ddd021456437deb39ecc9cfb4acd76d9979ebf648bc557fbe72`  
		Last Modified: Sat, 08 Nov 2025 07:48:21 GMT  
		Size: 1.7 MB (1724216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21711486e964d2a3cd60334a1661e3595da58b61eabf084122ea508e1bca072a`  
		Last Modified: Sat, 08 Nov 2025 07:48:20 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:112402b7d17092abe30cffec5ba1c621d93390f6722ca8e879a7ebe5e37d56e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 KB (297671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53faba075eb85e5d9b99b05ab342187e2426bf270302b8243622fdfc53865750`

```dockerfile
```

-	Layers:
	-	`sha256:e27bbde242b008b1f59f972ca8e8be5e5984fd4b81ddec1cc4583d8b9698e2f2`  
		Last Modified: Sat, 08 Nov 2025 10:52:32 GMT  
		Size: 277.5 KB (277529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a646bd279bf5e140e819c3f4b03968c85be34fbb0e9989ba792a3aa5d7ee4dca`  
		Last Modified: Sat, 08 Nov 2025 10:52:33 GMT  
		Size: 20.1 KB (20142 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:483a0adacb308608b24d94c2f715d6c828974d8075dc29da048612d4a58ec60a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71738978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47d8009c72763996885bf5b5ae3e62d05a345811798fb1f081fd20bf728c26e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:14:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 20:15:38 GMT
ENV GOLANG_VERSION=1.25.4
# Wed, 05 Nov 2025 20:15:38 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 20:15:38 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 20:15:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 20:15:38 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 20:18:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 20:18:32 GMT
WORKDIR /go
# Wed, 05 Nov 2025 21:22:17 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 05 Nov 2025 21:22:18 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 05 Nov 2025 21:22:18 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 05 Nov 2025 21:22:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 05 Nov 2025 21:22:18 GMT
ENV XCADDY_SETCAP=1
# Wed, 05 Nov 2025 21:22:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 05 Nov 2025 21:22:18 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 05 Nov 2025 21:22:18 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce53ff9bf2eef5053eb507e6c4a528322e0535fda9d363fa7b72a5259d021f2b`  
		Last Modified: Mon, 03 Nov 2025 18:14:51 GMT  
		Size: 292.2 KB (292156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fe2a4ea5a438feafc93392d55b50ea8eee2e47563087161685963824d4cb40`  
		Last Modified: Wed, 05 Nov 2025 20:16:44 GMT  
		Size: 59.5 MB (59483654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77654748a1a8b65734bda7544ee4f147fa0796982fc7bdf802e5662bf1bc5801`  
		Last Modified: Wed, 05 Nov 2025 20:18:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fce773c799a182b69e9bd3a303e8c2cba29ff9d3136a0ec3bf72e94b079f607`  
		Last Modified: Wed, 05 Nov 2025 21:22:36 GMT  
		Size: 6.5 MB (6530476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c200828366f007c399fe253c32fdd55c3470071e5e51b6751194bc7aab14024d`  
		Last Modified: Wed, 05 Nov 2025 21:22:36 GMT  
		Size: 1.8 MB (1782855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38110e8f434b39c8234cc113c847794d560b252b55276ab28e2a35a06b371f05`  
		Last Modified: Wed, 05 Nov 2025 21:22:36 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3b9c7b48cfc281e7723c2d4ad1206c0e0dcdd297f3d4a3461c69fe921ca9fdc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 KB (297532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777e79f27435eaded2d9716bf1f44fcc6e7ce2ff0a87b068c0c6137ff921b9a1`

```dockerfile
```

-	Layers:
	-	`sha256:3bb9f660abaf82628d14b3657da4737605c33a9b3cede32f4e0e455261c4f122`  
		Last Modified: Wed, 05 Nov 2025 22:53:13 GMT  
		Size: 277.5 KB (277461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:961d6446e641be0682a6a8bd80a859a383170e562590a1dbe1fa78ff9964b271`  
		Last Modified: Wed, 05 Nov 2025 22:53:14 GMT  
		Size: 20.1 KB (20071 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.26100.7171; amd64

```console
$ docker pull caddy@sha256:5dd7e11ecd46dc2a236f698d7542e0f19d020ae96d39e7b135c219f796083263
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3351893237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960da8a4d45ba99b8e16a6053d362300cb1494f4847367bd2db54630389a51f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:23:01 GMT
ENV GIT_VERSION=2.48.1
# Tue, 11 Nov 2025 19:23:02 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 11 Nov 2025 19:23:02 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 11 Nov 2025 19:23:03 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 11 Nov 2025 19:23:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:23:15 GMT
ENV GOPATH=C:\go
# Tue, 11 Nov 2025 19:23:20 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:23:20 GMT
ENV GOLANG_VERSION=1.25.4
# Tue, 11 Nov 2025 19:24:38 GMT
RUN $url = 'https://dl.google.com/go/go1.25.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '6dad204d42719795f22067553b2b042c0e710b32c5a00f6c67892865167fdfd0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:24:39 GMT
WORKDIR C:\go
# Tue, 11 Nov 2025 20:16:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 20:16:27 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 11 Nov 2025 20:16:27 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 11 Nov 2025 20:16:28 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 Nov 2025 20:16:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 Nov 2025 20:16:35 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b0dd942b2325bea867f58aeeb0af08752b535e7c2537bfab25eb44c3fdb8a0`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d9a7c57733598c262006db7cc864a6be8f74e4ad677025018444b66b84af55`  
		Last Modified: Tue, 11 Nov 2025 19:25:00 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d218b2e13e3d4cfe6cb49f852b6eb761b800684418d1037704bcbbf602e8343`  
		Last Modified: Tue, 11 Nov 2025 19:25:01 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286d99b5da106a868e2ce83dac0d213fb7a15c6507d832488c62a341b18d8a4c`  
		Last Modified: Tue, 11 Nov 2025 19:25:01 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a9624cd52cd3a3fd7ce42aeaca47ee244f771bcfe24bd1dbc48a163c4ec7aa`  
		Last Modified: Tue, 11 Nov 2025 19:25:00 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e5d112ec160584d1a7494e606ec5ff969cb0bfc3f6325af5ed624d65c36956`  
		Last Modified: Tue, 11 Nov 2025 19:25:06 GMT  
		Size: 51.2 MB (51219091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e9681653760e2846782d64c03f4770cf19697d04f250a460fad237223a3890`  
		Last Modified: Tue, 11 Nov 2025 19:25:01 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb4b1e7215f1022d263696481978d17bb18bfb9e5582f5afef1ba08b34bc4ee`  
		Last Modified: Tue, 11 Nov 2025 19:25:01 GMT  
		Size: 345.8 KB (345769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9560800b103aa4813b55f7f3ef862c1aa8b8070d16547107a470dd77b62d66c`  
		Last Modified: Tue, 11 Nov 2025 19:25:01 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a81600bf08117f42a9832ac12d7a83124dda09158f1ff798d15210632f10839`  
		Last Modified: Tue, 11 Nov 2025 19:25:13 GMT  
		Size: 62.6 MB (62565252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94e0407a4f61a29ea46f9188dd5ea02f1e0d017a9561bbae60be43a70e92ec5`  
		Last Modified: Tue, 11 Nov 2025 19:25:01 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4dcffc288b5dad20205182e17c873bbddb8272db79936f1604844a44ac2947`  
		Last Modified: Tue, 11 Nov 2025 20:16:49 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff732c4a9d1d014a27ba034079eaae1f1c68587165d556eabf8b8e4b0f594676`  
		Last Modified: Tue, 11 Nov 2025 20:16:49 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a48a167beac67e2c67b4c813599cf1683fe2dbcf8eb6426c40ddab10b57d03e`  
		Last Modified: Tue, 11 Nov 2025 20:16:49 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e6dd144156a1c4a8abe786e810492daa8ce1fbf2ac551dd2d9a0e21cc7c80c`  
		Last Modified: Tue, 11 Nov 2025 20:16:49 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6cd15e2e6313c55dc1fbd2a160285023a74634e046b54f4ac26044c34e42a2`  
		Last Modified: Tue, 11 Nov 2025 20:16:50 GMT  
		Size: 2.3 MB (2290123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92dd04e7d1bc123010c3d24d3c47d8f830615685cae1dc5c9376bd0bbc9817ef`  
		Last Modified: Tue, 11 Nov 2025 20:16:50 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.4405; amd64

```console
$ docker pull caddy@sha256:9594d0808254d72284be83640c15c56cc0f9551a3e2110ef6175928280db050d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1886575288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f1e3d2021857c8af1860b9ba144ff5271cb3fdf3c457a585f047b476996fdc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:21:45 GMT
ENV GIT_VERSION=2.48.1
# Tue, 11 Nov 2025 19:21:46 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 11 Nov 2025 19:21:46 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 11 Nov 2025 19:21:47 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 11 Nov 2025 19:22:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:22:02 GMT
ENV GOPATH=C:\go
# Tue, 11 Nov 2025 19:22:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:22:07 GMT
ENV GOLANG_VERSION=1.25.4
# Tue, 11 Nov 2025 19:23:40 GMT
RUN $url = 'https://dl.google.com/go/go1.25.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '6dad204d42719795f22067553b2b042c0e710b32c5a00f6c67892865167fdfd0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:23:41 GMT
WORKDIR C:\go
# Tue, 11 Nov 2025 20:17:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 20:17:11 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 11 Nov 2025 20:17:12 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 11 Nov 2025 20:17:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 Nov 2025 20:17:20 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 Nov 2025 20:17:21 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c47b7190b9ffc37d6229c244251af53d022884b4b7dab60e0c54d9354c4adc5`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e13f584c63654736fde4a175df8216409c15c6d7643ad9295de8a5abd2a4978`  
		Last Modified: Tue, 11 Nov 2025 19:24:20 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33739290334e540f49bac24464ef1cb56f154b41ac539feec548ed45ceba4dea`  
		Last Modified: Tue, 11 Nov 2025 19:24:20 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651148c569cba4ca28fc1a1a7e66b91d22bf248394b9e58fc7216718954d3d19`  
		Last Modified: Tue, 11 Nov 2025 19:24:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab9605f909b523b9d51e51e3594dd6393bd61f38075f6e1d80104dcc92a9512`  
		Last Modified: Tue, 11 Nov 2025 19:24:20 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a539a132a5c8c3884aeb9cd5d02c954e5ad7b16ae8111bcd5b32b7541069c416`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 51.4 MB (51355994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90651daee37041e751301786280046bf16d511bac6be140920137ddd93eb87f6`  
		Last Modified: Tue, 11 Nov 2025 19:24:20 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aba66b9244c160f1d7a4d876a11cadfb22bfade0fbaf21bdfe0284fc54e82a8`  
		Last Modified: Tue, 11 Nov 2025 19:24:20 GMT  
		Size: 345.9 KB (345917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1671c87189dd54542bcad772db6a5d01eec18455920d98e6d327823b96fcac0`  
		Last Modified: Tue, 11 Nov 2025 19:24:20 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4f6d6ea4acabdae52e7c4bd183a07c154acce63861c3312c4ab25e5982ed3e`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 62.6 MB (62568634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fda6eccbd8f7a48b7f4b9c7cb9a77ad2df38738eb523a57901d8b485d80f001`  
		Last Modified: Tue, 11 Nov 2025 19:24:19 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0897d23f3cdb97b5a66374968d878f3ab77359d4ae402bea1110f92b46c111db`  
		Last Modified: Tue, 11 Nov 2025 20:17:45 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7161a749e46d079a37af3a50f3da69dc4cfe9e487f3c5709febee61aca159b3f`  
		Last Modified: Tue, 11 Nov 2025 20:17:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf9d23cae18043d6e224478ea732492bba0e06711df87645b2ee5ae45975994`  
		Last Modified: Tue, 11 Nov 2025 20:17:46 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af09a0521fc25cfe8154503c9c640086af5e45dcf82dbb6a2ee371f5bbd10b51`  
		Last Modified: Tue, 11 Nov 2025 20:17:46 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d520633e45c829856995c04de150f18890ecb76e6f25843376eaeab11fbe7f0`  
		Last Modified: Tue, 11 Nov 2025 20:17:47 GMT  
		Size: 2.3 MB (2326026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172720edaa9d6b281586894b89a884a42a976ff9e6537a028ef1f177409a47e3`  
		Last Modified: Tue, 11 Nov 2025 20:17:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

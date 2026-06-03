## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:97b0e2504f8a28a9c8a62f509a8f1138102d2ddd5e7708b9b6ba0a3e6e6ec9db
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
$ docker pull caddy@sha256:3a77db624faf6469f8c6dbfb00324135fdf00962a8a40fe13b3eeea7a023cbf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79773780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7157bddeb263efa71eded61ef33031924d35671ffc8b1aa8edea39b1acb08a1a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:44:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:53 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:55 GMT
WORKDIR /go
# Wed, 03 Jun 2026 17:55:36 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 03 Jun 2026 17:55:37 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 03 Jun 2026 17:55:37 GMT
ENV CADDY_VERSION=v2.11.4
# Wed, 03 Jun 2026 17:55:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Jun 2026 17:55:37 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Jun 2026 17:55:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 03 Jun 2026 17:55:37 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 03 Jun 2026 17:55:37 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30edd47abbca5172a1775d1ba8a17aef65500a7a1ecc50af582706ad0c19ab`  
		Last Modified: Tue, 02 Jun 2026 21:45:09 GMT  
		Size: 290.2 KB (290247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aaa626ba3010d60ab55d9cdc69c0b12ebff5d1b5ece83ff220fb46a7709b3b`  
		Last Modified: Tue, 02 Jun 2026 21:44:37 GMT  
		Size: 67.3 MB (67283031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abecc8ee46932a01c961a896c3c87dd0efe1301916e124bdac46f96ae6e9dee`  
		Last Modified: Tue, 02 Jun 2026 21:45:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91925c255306d7236985c0216207f91a508d7e66c68a3a2ab98e9c8fed5f9b3`  
		Last Modified: Wed, 03 Jun 2026 17:55:45 GMT  
		Size: 6.5 MB (6489215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451f9ee165eddcf4cf529896df180cba59950efc5c84fc15af12fb4a854bf1c9`  
		Last Modified: Wed, 03 Jun 2026 17:55:45 GMT  
		Size: 1.8 MB (1846506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faad3a23a298def20bbc896063e1b6533fba18a47ee518dc396e680aed4a9725`  
		Last Modified: Wed, 03 Jun 2026 17:55:45 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:12646dba5594e635588e93be88f93985bdc035465d268cedd76ee437516bba8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 KB (300905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67f36352ffd4d5eb2a38fb88ef9175a7806dba3479ae7e851d9fd5dab3e73a2`

```dockerfile
```

-	Layers:
	-	`sha256:4779d07a8f3519fe95ee1ae97b0feeef1a6be5c017248b46b67cdca83038fa87`  
		Last Modified: Wed, 03 Jun 2026 17:55:45 GMT  
		Size: 280.8 KB (280776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7213d91d5691691c9b91be16191a0169a48d07d6a38358d18196fd13cb61743d`  
		Last Modified: Wed, 03 Jun 2026 17:55:44 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:8485cca6d0fcdc6bd504bb12accc25847d4838891c84b27adf6ea4964386d633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77801107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68b8f6b9011552d5c4ecebae5353f3980dc98c6985ae21b85d61e07ee30d3d6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:43:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:01 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:04 GMT
WORKDIR /go
# Wed, 03 Jun 2026 17:55:28 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 03 Jun 2026 17:55:29 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 03 Jun 2026 17:55:29 GMT
ENV CADDY_VERSION=v2.11.4
# Wed, 03 Jun 2026 17:55:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Jun 2026 17:55:29 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Jun 2026 17:55:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 03 Jun 2026 17:55:29 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 03 Jun 2026 17:55:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dc79104d8e3b9e93b7ff3163839b44dd0979c52b2f81f68e01be8f60d9d090`  
		Last Modified: Tue, 02 Jun 2026 21:44:16 GMT  
		Size: 291.0 KB (291036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb989b4b1329f80799d899b8d7259a6658047b39b2b670ed0cc8620dd1d357c`  
		Last Modified: Tue, 02 Jun 2026 21:44:18 GMT  
		Size: 65.8 MB (65785954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e947158a0266891a134507f0a6253aec12f2c7656af2daefbed99f399148f5`  
		Last Modified: Tue, 02 Jun 2026 21:44:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81208b38c9d91dd12c8562c3b2a1fec12410a6b039579c3a9a90d5c38f101038`  
		Last Modified: Wed, 03 Jun 2026 17:55:33 GMT  
		Size: 6.4 MB (6406664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9860ecacb6c6aa145537d38a12a16db21a73c43685acf9373127930cbd98e7`  
		Last Modified: Wed, 03 Jun 2026 17:55:34 GMT  
		Size: 1.7 MB (1744999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3996ad8903404a6de37dacb39c75e57ad04d7072a462d5641154550ebc819020`  
		Last Modified: Wed, 03 Jun 2026 17:55:33 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:3a9da5c8f62ecd277ae35c4f42ddd560645e7b25c6ddb2ad4d521d033bfd7b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c988194fc2608f21e24484ebdd93cd7ed6e73bfe779fc0a4ff4d255539ef3bba`

```dockerfile
```

-	Layers:
	-	`sha256:3d02349eb4bb8ee0bc6736e329b8a9b050161adb0f43c8bfab9c3e36270b37d8`  
		Last Modified: Wed, 03 Jun 2026 17:55:33 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:f2d04cd81dc1050608dbdd6b382822f93a97dcf7a2df78b69431b9265022d32c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76958157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c29e17db441d71a1241030a2ba1501e46a682eae549a85d0a8eebaba5aecce`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:44:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:51 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:54 GMT
WORKDIR /go
# Wed, 03 Jun 2026 17:55:27 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 03 Jun 2026 17:55:27 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 03 Jun 2026 17:55:27 GMT
ENV CADDY_VERSION=v2.11.4
# Wed, 03 Jun 2026 17:55:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Jun 2026 17:55:27 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Jun 2026 17:55:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 03 Jun 2026 17:55:27 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 03 Jun 2026 17:55:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa788fec666273423bc95c719209c3f49b0d2c1c28fdaf669e4ebcab932954`  
		Last Modified: Tue, 02 Jun 2026 21:45:08 GMT  
		Size: 290.2 KB (290169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f46eeae83dd5d801ff20835cd1ea98f630698b9c066e10ddf320a1c9d42c07`  
		Last Modified: Tue, 02 Jun 2026 21:45:10 GMT  
		Size: 65.8 MB (65786124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5494a0eb08b28e7075149245f5ff666eeadec03e6b1b08870ad1caa24151d00b`  
		Last Modified: Tue, 02 Jun 2026 21:45:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22358c6015a22ea3202794ba417e75c1ae4bcd0908a0571e8f091a1a5c0b506a`  
		Last Modified: Wed, 03 Jun 2026 17:55:35 GMT  
		Size: 5.9 MB (5859396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ee2ff8260ee71ca9ff9fcfbf63dcd9becf85a8dbcdeb33b1633f8f74812515`  
		Last Modified: Wed, 03 Jun 2026 17:55:35 GMT  
		Size: 1.7 MB (1738756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95686c364fea98cce0d8aa2035dea352d8beb7efa62bfe5cd744267510b23bd`  
		Last Modified: Wed, 03 Jun 2026 17:55:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:03bb353a154fc018133af34bffab0d32eca8409f9e181e3bcfe085b68fc501b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 KB (303422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abecb4fd1903b3b5931b21a69c8c811b723c2d4cf83979d96d1ac346f6ecc95a`

```dockerfile
```

-	Layers:
	-	`sha256:5fdccee6e67a8380e68fe3648160d07b42c4f00426b9369a40ec08713356a089`  
		Last Modified: Wed, 03 Jun 2026 17:55:35 GMT  
		Size: 283.2 KB (283168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25eb5cad048c16a6ac7829cc1cdf638f397279348d76e2ee54affe32e7bd821`  
		Last Modified: Wed, 03 Jun 2026 17:55:35 GMT  
		Size: 20.3 KB (20254 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:90e195cd02f78b352e629fe2161159bd085fdd88ac959e33a6146229a5d1ea5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76951887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf82b92cc67d2d3615d12b6e41af05749c7ba25b9f0d51460148d51726f0e76`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:43:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:43:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:43:58 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
WORKDIR /go
# Wed, 03 Jun 2026 17:54:05 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 03 Jun 2026 17:54:06 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 03 Jun 2026 17:54:06 GMT
ENV CADDY_VERSION=v2.11.4
# Wed, 03 Jun 2026 17:54:06 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Jun 2026 17:54:06 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Jun 2026 17:54:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 03 Jun 2026 17:54:06 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 03 Jun 2026 17:54:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2c0198c180cf41cbfd73e25946fc0ccc373d0fee89deb6e7eeec7b1f8612ee`  
		Last Modified: Tue, 02 Jun 2026 21:44:15 GMT  
		Size: 292.9 KB (292861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a477eaf154b7c8070862d9db01681f78c8a60ce90e8936310f6a906696df475a`  
		Last Modified: Tue, 02 Jun 2026 21:43:59 GMT  
		Size: 64.2 MB (64166971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cb4739b26b76346d1281fb8fac14c5bc8025bfc580405cc95aa21736e41116`  
		Last Modified: Tue, 02 Jun 2026 21:44:15 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23451b35362821591a5b47d450ba17664208f28bb185190ce6aac6aa280dc5d`  
		Last Modified: Wed, 03 Jun 2026 17:54:13 GMT  
		Size: 6.6 MB (6575216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d712da0a0c74844d6980129c405704e2d524a23ebf8a10ad041ce8bacc4bef89`  
		Last Modified: Wed, 03 Jun 2026 17:54:13 GMT  
		Size: 1.7 MB (1716380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84df7fd1b1366b8b802174c81a04133ee4422c44dea6cb95bdd27d72adf9daab`  
		Last Modified: Wed, 03 Jun 2026 17:54:13 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:c5d825bae24fe8df2d5a36db7af8d1a3b872b9aec5e1175a8510590b60bdd001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 KB (300523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c689a46a624dbc88f591abc80bc2a5a9417f5a8651908ec840908563647b915`

```dockerfile
```

-	Layers:
	-	`sha256:25edf13f3eb88208a1054a06f421118d95c1f02c9f32fa36e08a6d6cca105905`  
		Last Modified: Wed, 03 Jun 2026 17:54:13 GMT  
		Size: 280.2 KB (280230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88c84c11699b097b5a4156274e6d572e2ba064ffc5dda135fb8a314880394ee9`  
		Last Modified: Wed, 03 Jun 2026 17:54:13 GMT  
		Size: 20.3 KB (20293 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b412a8520c6ef455e2de85b338edab1504a3e0bd92947e55ff1680c896d8d9f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77577930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1415684e73c3cd888d03fabf39e8dcd6fc99818559f59dc6fbf6bfa9e668a0d0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:47:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:42:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:42:40 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:18 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:19:34 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 03 Jun 2026 17:53:57 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 03 Jun 2026 17:53:57 GMT
ENV CADDY_VERSION=v2.11.4
# Wed, 03 Jun 2026 17:53:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Jun 2026 17:53:57 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Jun 2026 17:53:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 03 Jun 2026 17:53:58 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 03 Jun 2026 17:53:58 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc45c5906cb105fa1bde6a534e8e48deced0c4556f99056c2f76204caa5c2`  
		Last Modified: Tue, 02 Jun 2026 16:47:39 GMT  
		Size: 293.4 KB (293393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94153723d1545849cb54e33c3f8f977f110afcb00da0d5d32236b24537c1a4a3`  
		Last Modified: Tue, 02 Jun 2026 21:43:46 GMT  
		Size: 64.8 MB (64840550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd4ff149d61b69213dc146324696a7a3af1a2b46684c6f928dfca1ae8489a0e`  
		Last Modified: Tue, 02 Jun 2026 21:44:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e3cb06425959c67588985a91f934858685c3d7e6f0a3094af6c96ef93508d2`  
		Last Modified: Tue, 02 Jun 2026 22:19:53 GMT  
		Size: 6.9 MB (6906465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031df02500ddace5c3b3866fe858d6b36aa4a90cc4efca20cb7a6de41776cf53`  
		Last Modified: Wed, 03 Jun 2026 17:54:24 GMT  
		Size: 1.7 MB (1705997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d8794eb51fa0aacdd783c4d8f927ca31bc2d38d65dbdea60048f15115a2c63`  
		Last Modified: Wed, 03 Jun 2026 17:54:24 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:00b0664beef9e5fe9d0983517b8cd2df1360f96489fc6cfd678fa7fc7cb0d85c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 KB (300398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea21f736aa1347e2c54bbd1865f805824f06f5eaa5cbbc5e76dc26a257b3fb76`

```dockerfile
```

-	Layers:
	-	`sha256:178d84350820df72f6defdc90b0253ea461a4144eaad7bf44933293c501be3a4`  
		Last Modified: Wed, 03 Jun 2026 17:54:24 GMT  
		Size: 280.2 KB (280199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19386e4b465187f583d4d1393f7f0f8cf2fa3fd14f0e55d3cfc9a2cb28e09adc`  
		Last Modified: Wed, 03 Jun 2026 17:54:24 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:851cb908798b1538ffe3a3053bb98a32903f158a7f1ca9eeafb0fa30f6f34f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77424217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dfc4a9d5f64621b356f7b47c6c48337fe32d5912cfc96a0484d5c999eabca9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 23:12:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 23:12:42 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 23:21:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 23:21:02 GMT
WORKDIR /go
# Wed, 03 Jun 2026 05:24:30 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 03 Jun 2026 05:24:32 GMT
ENV CADDY_VERSION=v2.11.3
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Jun 2026 05:24:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8f135b9aec9b42cabcdbc9e60e1e2b738fe71cb50c44dd091c53fb8edc94a`  
		Last Modified: Tue, 02 Jun 2026 23:19:15 GMT  
		Size: 65.1 MB (65148394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309c4848fcf3e91f4413c1666bace4337c4f1c12c50976959bd29ad011c4d936`  
		Last Modified: Tue, 02 Jun 2026 23:22:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc28d768f2c71e4a402e2f4424963bfaa465d9c4a2f36c428bd41b08e3d6d2d`  
		Last Modified: Wed, 03 Jun 2026 05:25:48 GMT  
		Size: 6.7 MB (6672809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b5d5e4441c4e23a30ad21c2b66c3a336df57c4bfda44ff5113b5b3be8e2ffc`  
		Last Modified: Wed, 03 Jun 2026 05:25:48 GMT  
		Size: 1.7 MB (1724208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa80fdf8a500696ba07bd03f2a260b2e578f3e7909bec500d7122de9d25041d6`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:dca192295748614e125d445ca613cc0972469b2e1774dca65dd6b47fe9d2682f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 KB (300394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a911353b6377828995df9827f453d124992e5ff9b7484ef6ebc4da9d7258c820`

```dockerfile
```

-	Layers:
	-	`sha256:e5bc98528c0380ded7049be92a37c9302d44d983dd53bba1648e04dedd55efb4`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 280.2 KB (280195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb92a4e503b3fefa7c0f01279adf8084dd01665b4d68fcef6d623b33d866cb16`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:7078c3c10133817bb694e551bae38c883581bb9d7293270a88b8a8eb267b07ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79094967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11cd8a7cece67a88ac40ed31533415d2d113f566e69b8d0c5e555139e92d2f4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:41:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:43:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:43:02 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:43:04 GMT
WORKDIR /go
# Wed, 03 Jun 2026 17:54:19 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 03 Jun 2026 17:54:19 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 03 Jun 2026 17:54:19 GMT
ENV CADDY_VERSION=v2.11.4
# Wed, 03 Jun 2026 17:54:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Jun 2026 17:54:19 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Jun 2026 17:54:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 03 Jun 2026 17:54:19 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 03 Jun 2026 17:54:19 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42ca9f29dfa6d3e969a05d12ba4b1dd9465b2ec31113dd62c26050eb7eeae28`  
		Last Modified: Tue, 02 Jun 2026 16:42:25 GMT  
		Size: 291.2 KB (291162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa95f9225fe123215e56024e7fcaa3f2eb9fb3081c2d6160ebae532ca6d5eefd`  
		Last Modified: Tue, 02 Jun 2026 21:43:22 GMT  
		Size: 66.5 MB (66513822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9138885877e3f590d4144dfc2ec737113acde73b99374df82c5be8c2901f3dd`  
		Last Modified: Tue, 02 Jun 2026 21:43:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a4cfed4452e5cf1eb994a4672a9aef1081dfa26cc444a89f5b9494045fcdcc`  
		Last Modified: Wed, 03 Jun 2026 17:54:32 GMT  
		Size: 6.8 MB (6780007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b328a88564b6512812f007392816473cbf6d7b79852353a2da71730905d8e52`  
		Last Modified: Wed, 03 Jun 2026 17:54:32 GMT  
		Size: 1.8 MB (1782856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cc723a53476d2094cc107288f5cb8cae5d068449f00f1763da37da344fbdfc`  
		Last Modified: Wed, 03 Jun 2026 17:54:32 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:71a51ed67154d8fdc92278746bb7adc02fdfd9b3a5e097137654b7adff4c94a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 KB (300254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c25b94fb226900b0e010c4420890817e876d9518fc72d39da95b0c1301ca058`

```dockerfile
```

-	Layers:
	-	`sha256:9113b23583cbc5d88aa2676c3e15be2e3eec8f986e90c34a9e18065b25ff1182`  
		Last Modified: Wed, 03 Jun 2026 17:54:32 GMT  
		Size: 280.1 KB (280125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3e8745fd54a3b2f3c0f1c062b067d6378601af9193503be472dec90a1f6d033`  
		Last Modified: Wed, 03 Jun 2026 17:54:31 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

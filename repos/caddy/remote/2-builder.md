## `caddy:2-builder`

```console
$ docker pull caddy@sha256:01668408cc26e2e00c9d067c30cb43b2ba14ad1f2808beda55503cb2a31f59dc
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
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:40aa5af183f83631ca8566ca076a1c05d14c02311d7a3e8fad9374c45d3574f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79756917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1004d20acbd8760e44024631ca39d76e358609a811e0498e1ffc9273890bc2c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Feb 2026 21:26:02 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:26:09 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:26:09 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:26:09 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:26:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:26:09 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:26:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:26:11 GMT
WORKDIR /go
# Wed, 11 Feb 2026 18:27:40 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 11 Feb 2026 18:27:41 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 11 Feb 2026 18:27:41 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 11 Feb 2026 18:27:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 11 Feb 2026 18:27:41 GMT
ENV XCADDY_SETCAP=1
# Wed, 11 Feb 2026 18:27:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 11 Feb 2026 18:27:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 11 Feb 2026 18:27:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e3cee16f61a04c1478b0bea063f6591a583f68c5ec96ad17bd6022fc6cf49e`  
		Last Modified: Tue, 10 Feb 2026 21:26:25 GMT  
		Size: 296.1 KB (296076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ede2856567d2593950de6f98f5d2763ae304caeb0ff577a1318c065a8fd650c`  
		Last Modified: Tue, 10 Feb 2026 21:25:34 GMT  
		Size: 67.2 MB (67176670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620ce275e86ec364135f603517679f51437c2da390313e710d0f78203dbae68a`  
		Last Modified: Tue, 10 Feb 2026 21:26:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2595a6a04d692fcd7228e0f397f605e8eb73bbadb74968c36cff3c31425abb`  
		Last Modified: Wed, 11 Feb 2026 18:27:49 GMT  
		Size: 6.6 MB (6575256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdad60f88c27edacbbe409539d5ceaa97751a9fc0b9d0e40a7f30fd4118ceb53`  
		Last Modified: Wed, 11 Feb 2026 18:27:49 GMT  
		Size: 1.8 MB (1846502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27b795db38fd1b4a22d50b1e88b0a5c30b5f6de3f480361313359b33a6711f3`  
		Last Modified: Wed, 11 Feb 2026 18:27:48 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:f8cddbac2bcece34d170d759165572f894bcea54c757b4cb3f85f9c6b3734740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 KB (304452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0a1651afbe3efd0284ca0d861dc77af430a603a10df8ecf8ace11ac8f65c43`

```dockerfile
```

-	Layers:
	-	`sha256:382e75c2bccd336563dc57077e3a23f27da27bedb6c46c19efb7951ca0941a46`  
		Last Modified: Wed, 11 Feb 2026 18:27:48 GMT  
		Size: 284.3 KB (284325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9203475b03da9e539ed86f11d3ee7f57225efa6da4a0f72d5791bf1bfbe85ce8`  
		Last Modified: Wed, 11 Feb 2026 18:27:48 GMT  
		Size: 20.1 KB (20127 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:433f2b3a8b3c5529e6650dcfa11ca71fa9f03547f8b2f9dc969661c2d19b8636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77830177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f989cd2ac392b414082a0aa7d81752eb19ccf1b6c2fb428caaf0fa5599e4a7b1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 10 Feb 2026 21:24:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:24:41 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:24:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:24:41 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:24:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:24:41 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:24:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:24:44 GMT
WORKDIR /go
# Wed, 11 Feb 2026 18:27:35 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 11 Feb 2026 18:27:36 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 11 Feb 2026 18:27:36 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 11 Feb 2026 18:27:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 11 Feb 2026 18:27:36 GMT
ENV XCADDY_SETCAP=1
# Wed, 11 Feb 2026 18:27:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 11 Feb 2026 18:27:36 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 11 Feb 2026 18:27:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82476015721696203da6d7b187ce059aa1747497aecfa10aab0ad0d3d8de072b`  
		Last Modified: Tue, 10 Feb 2026 21:24:56 GMT  
		Size: 297.3 KB (297256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d8c7cfc344092b4dd309b4dad51d70b234cbf828cceaf1db4ff123fb24a325`  
		Last Modified: Tue, 10 Feb 2026 21:24:58 GMT  
		Size: 65.7 MB (65732874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efdbe5ba0a73b91f46539c38bdf47319b90f50d65f7b619c548c3964edaa16e`  
		Last Modified: Tue, 10 Feb 2026 21:24:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17d9cf055e91530c0bcc8af31721b1abc8b8cf4e98831d732ee8572699cff5d`  
		Last Modified: Wed, 11 Feb 2026 18:27:40 GMT  
		Size: 6.5 MB (6484633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157e784ac10a20221bcf6b2eb3841c8dfd98f7afca007e0226d78abc26c837b5`  
		Last Modified: Wed, 11 Feb 2026 18:27:40 GMT  
		Size: 1.7 MB (1745000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fc873facddfa2f53e777069e1910f36d4bb6e0ec530f59518a095c95a5d5da`  
		Last Modified: Wed, 11 Feb 2026 18:27:40 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:91b9cdab82ad319b07e087f31194df156c2a64d0fce019f8b1903f3e342c1975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2d966295a53c7168f44f454fee093d895ac1a535b04e32ca84498f5132ec15`

```dockerfile
```

-	Layers:
	-	`sha256:0e78a852c0effa099a37edc2a9a6b0a7e661f86e7cd5755ce3180c2b970716ca`  
		Last Modified: Wed, 11 Feb 2026 18:27:40 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8fda8546f626ac909c38326f0c7c56dbde34b08526e8ec631e7e5082ccc37b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76984491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a3e7b4dcfe0dd1851eadc29ac99858c320948513a185fab455b109f3a2f892`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 10 Feb 2026 21:25:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:25:53 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:25:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:25:53 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:25:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:25:53 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:25:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:25:55 GMT
WORKDIR /go
# Wed, 11 Feb 2026 18:28:32 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 11 Feb 2026 18:28:33 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 11 Feb 2026 18:28:33 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 11 Feb 2026 18:28:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 11 Feb 2026 18:28:33 GMT
ENV XCADDY_SETCAP=1
# Wed, 11 Feb 2026 18:28:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 11 Feb 2026 18:28:33 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 11 Feb 2026 18:28:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fa6b9decca076b24306c10519b00d1508eda1afea03f299175186aa4610dd9`  
		Last Modified: Tue, 10 Feb 2026 21:26:09 GMT  
		Size: 296.2 KB (296203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb468d6c3aa96f0258422956f98c08c3bc799ec9552ffdc9be6851ba4d40573`  
		Last Modified: Tue, 10 Feb 2026 21:25:20 GMT  
		Size: 65.7 MB (65732884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6118fecef0033245b81c35f0d4b7665697c66691d88f774978bf9f5cce7b267`  
		Last Modified: Tue, 10 Feb 2026 21:26:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7d9eb99d912398cd8afef8b8f670148893f8b62bf2598d91bb72666004d02c`  
		Last Modified: Wed, 11 Feb 2026 18:28:41 GMT  
		Size: 5.9 MB (5934326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85fc969e6883aa8b037ecd659f3d9e2c2742bb80ab98778d8b4852ef1c71229`  
		Last Modified: Wed, 11 Feb 2026 18:28:41 GMT  
		Size: 1.7 MB (1738762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7044b08acf9f3f8ab9f1d41751e87566cb4ee0b9482dbdb893ee3bb27506b62`  
		Last Modified: Wed, 11 Feb 2026 18:28:41 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:5086f9fa6a520d6d8cbc06357e9ed431a0e4faccd348c9b4a14cb897a955c175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 KB (306971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bac523b30f98e7bc0351a057818dab6dc5513631ad91790595f0bc6982b35e8`

```dockerfile
```

-	Layers:
	-	`sha256:e6aea34a98280db806f75e2d22fea823a4426a7747b7da5bf588ce7af5226e1b`  
		Last Modified: Wed, 11 Feb 2026 18:28:40 GMT  
		Size: 286.7 KB (286717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9563e6918ecbd7f88f2edce25fe48dc8476f878204251c58b6c14fd1e5fec6`  
		Last Modified: Wed, 11 Feb 2026 18:28:40 GMT  
		Size: 20.3 KB (20254 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:c4b36a686ae5179ea5d2e06148f848f9783f7e6ed7b1b5d4db2cde5ee50b8bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76955131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d86a4523b9f761bf4b7ee216473b8c144510bae07e66a78f6fa2677c02b859`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 10 Feb 2026 21:25:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:26:06 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:26:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:26:06 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:26:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:26:06 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:26:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:26:08 GMT
WORKDIR /go
# Wed, 11 Feb 2026 18:28:15 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 11 Feb 2026 18:28:16 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 11 Feb 2026 18:28:16 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 11 Feb 2026 18:28:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 11 Feb 2026 18:28:16 GMT
ENV XCADDY_SETCAP=1
# Wed, 11 Feb 2026 18:28:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 11 Feb 2026 18:28:16 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 11 Feb 2026 18:28:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825d9c3a927a28ecf581a47fa574a1a5538d465afa93bb1a79f5a436b7216ca4`  
		Last Modified: Tue, 10 Feb 2026 21:26:23 GMT  
		Size: 298.8 KB (298830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5a418ef96019867316412a90ec8973c4ade493b1d6671994ae31514a8ef6cd`  
		Last Modified: Tue, 10 Feb 2026 21:25:38 GMT  
		Size: 64.1 MB (64084003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a52d54c85405c1aaea781ad1b2d56b6526341e5815e11e25961b7cdf03b5ae`  
		Last Modified: Tue, 10 Feb 2026 21:26:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3faa1b6553aee154ec509568baf3bb08ea81567122c7868325b65fbc5158028c`  
		Last Modified: Wed, 11 Feb 2026 18:28:24 GMT  
		Size: 6.7 MB (6658228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bc078aab501554c8be15f45d42e039562a91990ce68d652628ffad08a13727`  
		Last Modified: Wed, 11 Feb 2026 18:28:24 GMT  
		Size: 1.7 MB (1716386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27f2c7482597455ea91cb104313c6951f242c2035eb7ef843d52ff036fe068f`  
		Last Modified: Wed, 11 Feb 2026 18:28:24 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:b35c938131a5c7021a070e89678c6a78299c99e6b2bbe4a248ee600a57956a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 KB (304075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d829218e9721062f292fa0426b7c89939ae8a1ba8c4c472a51b15c8de746dbf6`

```dockerfile
```

-	Layers:
	-	`sha256:c5c9611fcde61a4df39a3e79e35cde9c7c99587bc4f5da72bc83485bf8e65500`  
		Last Modified: Wed, 11 Feb 2026 18:28:24 GMT  
		Size: 283.8 KB (283779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3930e9728bd8382e02820d24219dd8743bcaaa563c1d45af9f8e1bbbdfd8122`  
		Last Modified: Wed, 11 Feb 2026 18:28:24 GMT  
		Size: 20.3 KB (20296 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:ea3f9ee0b08d76e77c62963a0943484078bf3de00f59a8cddca66fa4a75f6928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77559287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a1fce25b49fa421aee38c57a4869a2b146e5aedac853a44b80efc4f2193c63`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:32:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:24:27 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:24:27 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:24:27 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:24:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:24:27 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:26:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:26:44 GMT
WORKDIR /go
# Wed, 11 Feb 2026 18:26:19 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 11 Feb 2026 18:27:26 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 11 Feb 2026 18:27:26 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 11 Feb 2026 18:27:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 11 Feb 2026 18:27:26 GMT
ENV XCADDY_SETCAP=1
# Wed, 11 Feb 2026 18:27:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 11 Feb 2026 18:27:28 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 11 Feb 2026 18:27:32 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e528c55315b3e5f2f548755f16a234f2386736177558710d4d0c6eaf02151f69`  
		Last Modified: Mon, 09 Feb 2026 20:33:09 GMT  
		Size: 299.3 KB (299264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb65e50af4c9d9d06b20c69b0731fa5479387927e011d4a6cf02c0de9c35733`  
		Last Modified: Tue, 10 Feb 2026 21:25:51 GMT  
		Size: 64.7 MB (64730602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12ec74696c53556914cd1f79d446767190917d608aabce7f4b38fe71a197a05`  
		Last Modified: Tue, 10 Feb 2026 21:27:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db55ee0861271f84f5ebc790f96a35795891c99745108b88bf37e0dbf3a0507b`  
		Last Modified: Wed, 11 Feb 2026 18:26:45 GMT  
		Size: 7.0 MB (6993188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d402bf010d281b8003d79c5aa7b2dd07a928261e954697bdf14c7198675d23`  
		Last Modified: Wed, 11 Feb 2026 18:28:01 GMT  
		Size: 1.7 MB (1705996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d15fed288f1b223c9b772b1c94df56980f0de304c59011514d1e1c812c7b30c`  
		Last Modified: Wed, 11 Feb 2026 18:28:01 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:959c5da1bb22ae736bcddceaa8ef6971555b62264623a58368de47604fead4e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 KB (303946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b5959cbe93feaea4e73f06c02ad78be26c9b8dfce5cba87154f3b19f3605dd`

```dockerfile
```

-	Layers:
	-	`sha256:242a69a584ac79f9dd8a5391cf6fb956a4317758d61622a5b2ecd78a7b4064a9`  
		Last Modified: Wed, 11 Feb 2026 18:28:01 GMT  
		Size: 283.7 KB (283748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc37a62a233b0fcd96d940e6145513eee26b7c41dd0046694756c460aabeebb4`  
		Last Modified: Wed, 11 Feb 2026 18:28:00 GMT  
		Size: 20.2 KB (20198 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; riscv64

```console
$ docker pull caddy@sha256:455158c87246eb41745685414641a5c2de39af90c4db36b61ba156f29e6d7c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77413349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc81982de821c1e32061e1edadc3e7bdb3cc2967959afec2d32e6398f31cd35c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:12:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:26:13 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:26:13 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:26:13 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:26:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:26:13 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:35:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:35:42 GMT
WORKDIR /go
# Wed, 11 Feb 2026 18:30:06 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 11 Feb 2026 18:35:30 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 11 Feb 2026 18:35:30 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 11 Feb 2026 18:35:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 11 Feb 2026 18:35:30 GMT
ENV XCADDY_SETCAP=1
# Wed, 11 Feb 2026 18:35:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 11 Feb 2026 18:35:31 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 11 Feb 2026 18:35:31 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f6a28a44ff91c18ab295ffef6822bbaccafe002bd1f4a117c179d363e86328`  
		Last Modified: Thu, 29 Jan 2026 19:14:45 GMT  
		Size: 296.5 KB (296505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e59666da981e3405c1b7fd86ade4932c92816496358034a16d9db56a3633b7`  
		Last Modified: Tue, 10 Feb 2026 21:32:56 GMT  
		Size: 65.1 MB (65055611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54e55455435872cd4c1ef9316e502246b291158a9caaceb025496243cd1b415`  
		Last Modified: Tue, 10 Feb 2026 21:36:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a4f2ae0e3d68dee53846ccfa4cc3232831844e786dbafe470c465a777ec5d9`  
		Last Modified: Wed, 11 Feb 2026 18:31:34 GMT  
		Size: 6.8 MB (6751132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27ec770ccdbfc136a7d76267c2b766bc2954a81a75cf1354accbd0d9126a6eb`  
		Last Modified: Wed, 11 Feb 2026 18:36:51 GMT  
		Size: 1.7 MB (1724221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6e07161c5503128c3bf2dd29288ed307650240932a87fd6331f91151e22829`  
		Last Modified: Wed, 11 Feb 2026 18:36:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:1418e0a047c09934e63d62f4fc8cd99e401c5b064900f57a41cb8190ef547702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 KB (303941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42bc7bc13609979518a3669aeedf998f177fbe18351fb9f015ea626c31fd717a`

```dockerfile
```

-	Layers:
	-	`sha256:d31c59108e5a4a5cfea80984b8887fc0964a396ce6baedd77efb3a3a7349400e`  
		Last Modified: Wed, 11 Feb 2026 18:36:51 GMT  
		Size: 283.7 KB (283744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99c2a0807b422fa1b85ba1a5c038de2a5266b754ea7a3fc88ddbe08572001686`  
		Last Modified: Wed, 11 Feb 2026 18:36:51 GMT  
		Size: 20.2 KB (20197 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:5cd5a8314f076c1b5c58e8ccd3440ed346f7e21b4521d76dcc7ce814f14fa984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79070358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb04e90ae34c63a7c8088672d869a51afd1e732a64d60433bc4c9c15703290cc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:00:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:24:12 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:24:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:24:12 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:24:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:24:12 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:24:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:24:18 GMT
WORKDIR /go
# Wed, 11 Feb 2026 18:26:15 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 11 Feb 2026 18:26:16 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 11 Feb 2026 18:26:16 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 11 Feb 2026 18:26:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 11 Feb 2026 18:26:16 GMT
ENV XCADDY_SETCAP=1
# Wed, 11 Feb 2026 18:26:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 11 Feb 2026 18:26:16 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 11 Feb 2026 18:26:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96012aea906c12635dfd37f261776f274a7fa57e016424f483ebb57edcd7c898`  
		Last Modified: Mon, 09 Feb 2026 20:00:44 GMT  
		Size: 297.2 KB (297174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0267cccbf93e93da2ed1297ad6771262243fba5de764f475d84248f8d84f3c28`  
		Last Modified: Tue, 10 Feb 2026 21:24:50 GMT  
		Size: 66.4 MB (66402757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1205873404541dd80f26800fffdfe4f93fa3bfaa4d5558142cbf8b4d08b79941`  
		Last Modified: Tue, 10 Feb 2026 21:24:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad02d07d516e212025a3e0970e7cec53ca1d0346c83b1e03baac6026edd5101`  
		Last Modified: Wed, 11 Feb 2026 18:26:28 GMT  
		Size: 6.9 MB (6861644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c12190cb85bdb72fef4a01ca15389c781199b7b1cd7bf820a9788dc151dbd79`  
		Last Modified: Wed, 11 Feb 2026 18:26:28 GMT  
		Size: 1.8 MB (1782857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589466ef9f108bc98567ce27712ba40f6ffcaaca59101b83ffb2271441ad1055`  
		Last Modified: Wed, 11 Feb 2026 18:26:28 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:703fbbcfea078fe44169fc6a78f3352eeae36ac3f7dcdf8cefff472162e8aa9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 KB (303803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9049f9a8435bc6c34b6731af1cd2d09019fc44fe2e46176629bac10a4942cf71`

```dockerfile
```

-	Layers:
	-	`sha256:45a32657df28d81c84c858e760e96d8a18d24bf4b013e8634f76ff6da23d2216`  
		Last Modified: Wed, 11 Feb 2026 18:26:28 GMT  
		Size: 283.7 KB (283674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:461c41f75de2f8ca8633c35300efb5808ced5f59a129e4960b5eef94dc0502ee`  
		Last Modified: Wed, 11 Feb 2026 18:26:28 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.26100.32370; amd64

```console
$ docker pull caddy@sha256:45ca44a785af0b24ceb715a0e1587ace942a9252f088bd1acc4868b9450163c2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2088430169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3bbff08502b20dba714924b2a16799d01b39f12902510fb853bde5211b257cc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:51:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 22:57:18 GMT
ENV GIT_VERSION=2.48.1
# Tue, 10 Feb 2026 22:57:18 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 10 Feb 2026 22:57:19 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 10 Feb 2026 22:57:19 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 10 Feb 2026 22:57:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 22:57:33 GMT
ENV GOPATH=C:\go
# Tue, 10 Feb 2026 22:57:38 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Feb 2026 22:57:38 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 22:59:03 GMT
RUN $url = 'https://dl.google.com/go/go1.26.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9bbe0fc64236b2b51f6255c05c4232532b8ecc0e6d2e00950bd3021d8a4d07d4'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 22:59:05 GMT
WORKDIR C:\go
# Wed, 11 Feb 2026 18:34:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 18:34:36 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 11 Feb 2026 18:34:37 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 11 Feb 2026 18:34:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 11 Feb 2026 18:34:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 11 Feb 2026 18:34:48 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f3641b48551abf691e707ba76f8b07a225d509249237749ad0c13cbcab89a6`  
		Last Modified: Tue, 10 Feb 2026 22:52:23 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dfafe2e4ec15681b59b09b2ea2f218a811a349d078b2cbaecc126feb929e2b`  
		Last Modified: Tue, 10 Feb 2026 22:59:18 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f90df82fe50dd6b5833a746c782a70988b3984ddf21c090d7d36129fe0f89f0`  
		Last Modified: Tue, 10 Feb 2026 22:59:17 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f052a5d8bf4f2827a95141c0b3c89390a04a735787707ab026025e7a498d313e`  
		Last Modified: Tue, 10 Feb 2026 22:59:16 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cab7931b4ab9cb79911a3504fff59396a710a90f2c03153fcda4d656c5fd8e5`  
		Last Modified: Tue, 10 Feb 2026 22:59:16 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1f3a56265f2532de676a227871566bf54f8aa0026966ec6e24d84ee7a7cbaf`  
		Last Modified: Tue, 10 Feb 2026 22:59:22 GMT  
		Size: 51.2 MB (51219241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec15bdcd174dd912379cd564ff80e30cacf595c1dceb3fa6174646abf3abb717`  
		Last Modified: Tue, 10 Feb 2026 22:59:15 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06e75f82ef8f5b262944577e66118aeb52f772e8651231eeaf6f719423cd29c`  
		Last Modified: Tue, 10 Feb 2026 22:59:15 GMT  
		Size: 343.4 KB (343397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd43e1c213d08a1667262b342e75f91b58cc736a17a346da75a58db846e3a068`  
		Last Modified: Tue, 10 Feb 2026 22:59:15 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62d46925baf3f405c1809cda2db6ee089e816de622c99360f77333d1a7bb267`  
		Last Modified: Tue, 10 Feb 2026 22:59:27 GMT  
		Size: 69.8 MB (69801863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445170f32e0feca8c866e6ee97a68bbcd335db232e7dc5a3da15ebd8d60c9f00`  
		Last Modified: Tue, 10 Feb 2026 22:59:15 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918f59d9c4124ea760be7ea926cf16103e67b1ea5b8f3fda9424eb4a16632bae`  
		Last Modified: Wed, 11 Feb 2026 18:34:53 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0180785d70aa0e6f093bfb5a64c5b02990a11d8743819622fedde95181e0e49f`  
		Last Modified: Wed, 11 Feb 2026 18:34:52 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa84bc9992ba9ac098e48dce21eed25530c5e149dd0f30864637076050a3918`  
		Last Modified: Wed, 11 Feb 2026 18:34:52 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552bc00f7f310dfd85b92d4378401eb1d3e31ef8460be2290c52a7dafa1e1a5c`  
		Last Modified: Wed, 11 Feb 2026 18:34:52 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011904aeba29593eca7114031b1e191995d3b1d59acef690b08cb8de65cf10d9`  
		Last Modified: Wed, 11 Feb 2026 18:34:52 GMT  
		Size: 2.3 MB (2288449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccdbdf8aa7d20d5d78870c4bbd062ee8fae7daa333802fd9496c173ea382c1d`  
		Last Modified: Wed, 11 Feb 2026 18:34:52 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.4773; amd64

```console
$ docker pull caddy@sha256:4bf875f29d62e3c5dbfe7e3ef19ebbfa84418a6899a5adb1c99803cc669434d9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1986443597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34e06091aab6676021bbbd3e644311a1e3f36a2ecd277494e91911b34443195`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Tue, 10 Feb 2026 22:50:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:03:30 GMT
ENV GIT_VERSION=2.48.1
# Tue, 10 Feb 2026 23:03:30 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 10 Feb 2026 23:03:31 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 10 Feb 2026 23:03:31 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 10 Feb 2026 23:03:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 23:03:47 GMT
ENV GOPATH=C:\go
# Tue, 10 Feb 2026 23:03:53 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Feb 2026 23:03:53 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 23:05:24 GMT
RUN $url = 'https://dl.google.com/go/go1.26.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9bbe0fc64236b2b51f6255c05c4232532b8ecc0e6d2e00950bd3021d8a4d07d4'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 23:05:25 GMT
WORKDIR C:\go
# Wed, 11 Feb 2026 18:34:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 18:34:40 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 11 Feb 2026 18:34:42 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 11 Feb 2026 18:34:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 11 Feb 2026 18:35:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 11 Feb 2026 18:35:43 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e5017e3b27d0eb763aca0362354553282eee78a4264a4b5ecd6f52bd60dcd3`  
		Last Modified: Tue, 10 Feb 2026 22:51:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b95eb7f9db13da3b6d5a9c1f5b928c8313709d5bb14a3f53420e4be3caa315`  
		Last Modified: Tue, 10 Feb 2026 23:05:39 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfc2b937390679a063d309d5a64b34308faa5e8abcf247077d5daceae4d4c63`  
		Last Modified: Tue, 10 Feb 2026 23:05:37 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca98983d227828c9e8f4dcb5d5aca80a2d284df14b1caf190b571bb39202749`  
		Last Modified: Tue, 10 Feb 2026 23:05:37 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42855f5ecb08216259cd3ed2021712ab32b0d3976be0eceead9e97dfba46fa6`  
		Last Modified: Tue, 10 Feb 2026 23:05:37 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73092cdfc8c30e1ee84abed47f8f94d66d4a988b9e233b3319ec1c86abb8808`  
		Last Modified: Tue, 10 Feb 2026 23:05:44 GMT  
		Size: 51.3 MB (51343122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44bab02ad025f8fbd35782c5df91cfde3cda91b0baa3981f15dbf377bdc67e9`  
		Last Modified: Tue, 10 Feb 2026 23:05:36 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a5fdf6bbf0735007d557610fac098c0e91123f0d4107c89e1d15f67ef9ba6b`  
		Last Modified: Tue, 10 Feb 2026 23:05:36 GMT  
		Size: 338.5 KB (338521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57cff3ba6a464501abf255ab10a3cc1596915aaf85b04addc0b511ddd373e40`  
		Last Modified: Tue, 10 Feb 2026 23:05:36 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b412fddaa3a4610afbb8ceb706036e1510e8a4e835d25b6d81d266d8ec001daf`  
		Last Modified: Tue, 10 Feb 2026 23:05:48 GMT  
		Size: 69.8 MB (69801464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb619cf00d530f21f2b6c7fd4c33b14be310c22afd5f310619aafcf630e182f6`  
		Last Modified: Tue, 10 Feb 2026 23:05:36 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc1a7148d32a35a936a559f065036353f8a903f7086b63243bf61152df8e5ec`  
		Last Modified: Wed, 11 Feb 2026 18:35:58 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fb0f3ccc3ba3852d73c84a3dd2d88c788edde986660b20ad6915f27a418686`  
		Last Modified: Wed, 11 Feb 2026 18:35:56 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0913e78c3cad8af53f7e3a29c28ed6c0f57ae243c33aba4d1273e5f03a360bae`  
		Last Modified: Wed, 11 Feb 2026 18:35:56 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab1f915ef8934e14e6de1ffc545d1d9d83ce08cc4f0d56c4d3531c271925261`  
		Last Modified: Wed, 11 Feb 2026 18:35:56 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f94036b75ffc4bc3e321cf7769dceb44e548c12b71a36dd5132eed112ffe6d`  
		Last Modified: Wed, 11 Feb 2026 18:35:57 GMT  
		Size: 2.3 MB (2286040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43ce354a6110569da4ac43d7c3e903e740b484592113e27e82311c184579c1e`  
		Last Modified: Wed, 11 Feb 2026 18:35:56 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

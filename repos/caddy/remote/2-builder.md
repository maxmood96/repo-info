## `caddy:2-builder`

```console
$ docker pull caddy@sha256:427ad6e5dacffe5577d77e3307fef61efdba832b6a78cc80e6f226975b56e1f1
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
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:db250d8ac333dbfb36d2082ae73b39f21d1316e42d441199f8fdef60aa578773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85743242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4fed372693e3e094c6ca0f1a55f4d71f8e0ce8f751c7a4158a8ad487996162`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbe7652777a557be7320acd6bafa585a401104296826b9790d94fa35f28480d`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 294.4 KB (294368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f05ace1117d62b655e04f6f73c83617e3e0febc38681dbedf58f477dd0658c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 74.0 MB (74047449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda4308841a6cc675c32eadc7ca82f1f5916886229ff6efcbc6e0f9015d73c80`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f167cb8105c9df8315499305c0ce83016c842a6c68f1e4424182dce22a3fe6d`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 5.9 MB (5939538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf2b30687fe7e3fa4f927c76a4e43b2db14a66b0e42a32ea9ddcdfa17e0c7d`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 1.8 MB (1835035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed24074f0fd5dc780dad0af8b4260d4205b3b89d7a666396c5b415abc85f2a8`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:75e70c9bd28699ef12d45bf9f03e28ff90a8d151d65e788697b9a7d7af5fe398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 KB (313626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8fc11bbdfee02d4bdc1dbac347ca232538947335e5e4d6788952c5a38c2494`

```dockerfile
```

-	Layers:
	-	`sha256:a19c370ffc738c2bca6c09b72807b6a1244b6294e4ba0df6aa29eaa2aac91efc`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 293.5 KB (293523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff92b5cdde37260cee10c8515c7ddc7fe46ee4c87c0b3cbfb1b3cf2f34be315`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ec24df61bf7606d181ee40ab713e0df69a89173fe117883dee14f1e0f8cd9bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83456315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc5eb1a64f9004a10a99b5a85fe75b0f0e58290eeb650f976d94e56f143fe3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ab5d3af8a0c99d02e713511deb39821a107d6d0ba6be4b2f6b0843085aea2a`  
		Last Modified: Tue, 07 Jan 2025 06:50:36 GMT  
		Size: 280.0 KB (279984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569843b3031b27806b4332ef906025ac81fe5ab3623a61a6d2306598bfd512bf`  
		Last Modified: Tue, 03 Dec 2024 22:28:55 GMT  
		Size: 72.2 MB (72198540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868f7227e5c7c8b4bac84441ac5dd24dd837136b8721a4f792daa15e57a2e9ea`  
		Last Modified: Tue, 07 Jan 2025 06:51:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8716a3e393f5147708dc6ab75310ace0722971636dcd1e92fc18a1a08d4310`  
		Last Modified: Tue, 07 Jan 2025 19:16:28 GMT  
		Size: 5.9 MB (5882962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d46024c53346834045856881a3323c9ccff4bd71a3f3f4c6064639d6e1706dc`  
		Last Modified: Tue, 07 Jan 2025 19:16:39 GMT  
		Size: 1.7 MB (1730294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12c0eba9000c85b2d1a02d8937fcd9c09c11ce473890d5e26a88237e4ce970d`  
		Last Modified: Tue, 07 Jan 2025 19:16:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:52a385666c18fcec928e4c9dffda6c64c1da8483006166e1b8efc40f8f5bbb5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02875baa9933babea5658c74ce320bc6e424b75883b7c032f466e85cdafb1ce8`

```dockerfile
```

-	Layers:
	-	`sha256:86ac3110d2be76dee5e418e092a98d1bfceb80f4af3c2e8eb67b6d8ac5bef969`  
		Last Modified: Tue, 07 Jan 2025 19:16:39 GMT  
		Size: 20.0 KB (20009 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:711550b3390725d352325fd551c237a75924d3a4d378d0a8c17d834d6bcae853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82660656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6208081873046fa65434043c2e1dd3a2966207bb5ade720526b54fb97606bfdd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb23a6598e9680ccc41dbb603b77f496c80c87db84ee993d3585d4db8daebd2e`  
		Last Modified: Tue, 07 Jan 2025 06:39:22 GMT  
		Size: 279.2 KB (279170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af30004a6a0d94684e60c07bbc44989294b76634fe7cc182dfb2140b1e8c877d`  
		Last Modified: Wed, 04 Dec 2024 07:17:17 GMT  
		Size: 72.2 MB (72198441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb64175fa34d7385f5a0720c5acb4845fb41cfffcdb03493609e11dc37a6fd3`  
		Last Modified: Tue, 07 Jan 2025 06:40:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfe46e461df3fdecb8a562830ba9b12245936fb2791b9cedbd7a8ca36b20058`  
		Last Modified: Tue, 07 Jan 2025 19:38:26 GMT  
		Size: 5.4 MB (5366898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84596fbb855fcd21b6ca4c90bd456908377d74cffb2445f95237309d2a484c32`  
		Last Modified: Tue, 07 Jan 2025 19:38:57 GMT  
		Size: 1.7 MB (1724266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a624d5a8ac42b5c2c1445a69ab87ced9badec3de749d9b8599880570b3cb273f`  
		Last Modified: Tue, 07 Jan 2025 19:38:56 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a8a75354935bc0c2b56ea5d8b81443bde300dba8442dd8b1af1d3b9a109e7839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 KB (310762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb03932eed79a6f6239c181f8ae39f1ac887fb5e37423392abb9df355f32f6d`

```dockerfile
```

-	Layers:
	-	`sha256:ff2ed6da1cb98be75248ee79a7a9982cac41e1383ac1c44a37c63f2d2da0d5bf`  
		Last Modified: Tue, 07 Jan 2025 19:38:56 GMT  
		Size: 290.5 KB (290538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e990bba3a097819e2870500e1ffb95d24a29d5089876af934f56a1f29952b84`  
		Last Modified: Tue, 07 Jan 2025 19:38:56 GMT  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:c11ef1d0a5c9ed229f43082f29f8ecf422a72aa72bdac93e7b6abc8706f8f7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82800608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce92f6eb0f78cd92a5b165889654838a71ce963d7d0eba1d64d0073ae223be0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4f93e44bdb513724a186600fdec99e49dc6de485ed4757e27b16ec93cbf7b4`  
		Last Modified: Tue, 07 Jan 2025 07:41:57 GMT  
		Size: 281.4 KB (281389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8f326b04424eb2027d1f0e3255fe568d71a5567f894a08cd86605ebe51c58`  
		Last Modified: Wed, 04 Dec 2024 01:41:07 GMT  
		Size: 70.7 MB (70673417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7497157ade0eb8e27bb99f1d2cbe466a3b159a321b071ec86638aa51639752f7`  
		Last Modified: Tue, 07 Jan 2025 07:42:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e208341eb37c26d31056e7b9148bfdf952c929003ac80f238023004a70d9fa`  
		Last Modified: Tue, 07 Jan 2025 17:23:51 GMT  
		Size: 6.1 MB (6057100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3a64dbd3a39b6007f76c39b6ee0c0720d4f4a40cc9dcc8dda3d042db4d37a0`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 1.7 MB (1701424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c23ad2d83091707b797b9ad6a73c160439fe1e6ee21e669643988449af62b5e`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:ccda48881787a1a9e2e973d61572f691776fed4ffd4e9b624b6bb0b73c9875b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.0 KB (308018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd4cc2f180b6209f339c8c9c89535d12602c5c9bb3a47255f9e1401e1f98fdd`

```dockerfile
```

-	Layers:
	-	`sha256:2d5335a62a98cd1fb5b9c13a01293700177a9dcae5897f6131a2f51a0de0c371`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 287.7 KB (287749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:509d779c7eb8321ae849c288781db7054c0c756218e63f2864a669f57f982089`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 20.3 KB (20269 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:ae070d55ed734bb9f26b8bd370a2505a74b68f8258358df545af4f86f19decf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82669759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4d45931cb6f86cb49eb2a88c2fb65ea04da6b51a5931231776eaa748c76c32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536d34381fd9ad3cee58f53559c0874fc783fd9067870f324d9d4e8f092a0015`  
		Last Modified: Wed, 08 Jan 2025 21:50:14 GMT  
		Size: 297.9 KB (297894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b834890572191b3d66e6bd561aad556f3c52e760e67fe9e31f02ad3d5139f55e`  
		Last Modified: Tue, 03 Dec 2024 23:35:02 GMT  
		Size: 70.8 MB (70839544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10173039484873ca3979a3698ef22d1edfdf1fb0aeabab8ad8b5abf80e36c0b`  
		Last Modified: Wed, 08 Jan 2025 21:52:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e90046d3ba1afd50a6d4a5c6c40609982d2342f650d63e92845f9680191fc04`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 6.3 MB (6261729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6020e3492fb8731819fb401ebf9bea060d1dba0da112cc369801cc6f75181`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 1.7 MB (1695595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd31426252091c11d90ffd2cb5692a5923c31dae3911af16cc2973b5164e1ef2`  
		Last Modified: Thu, 09 Jan 2025 03:30:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:e0dbaba01b809b9974e5b39e1949a4eba4c650e9c8add5d4940186740ae9c274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 KB (311839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6003454eef73ebaabead0aaf06b619bc1eccee16eaf04558aacc5148fc2e00f7`

```dockerfile
```

-	Layers:
	-	`sha256:5ef66216d744cfcfafeb2f64c715c6d373ca1dee38c77308d694033c36689144`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 291.7 KB (291666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a85f55b9730ad2b1de1532bd27f9a27055fa947fee10a1e04c3641ae2965051`  
		Last Modified: Thu, 09 Jan 2025 03:30:25 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; riscv64

```console
$ docker pull caddy@sha256:6526b547f327fdad247225ea542b9ce1cc77d687884dde4b14b75241e63aa3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82770124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bdb944f99feaf2e305e0d10a42df1c2bf6de1bd0d6138ea9f253171ca76699`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9da01c4ee7a2864330da14801bdf35f981730b5e2ffea0588c9ac48734e26b`  
		Last Modified: Wed, 13 Nov 2024 01:22:36 GMT  
		Size: 291.7 KB (291671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56ea5001679e325e9959f4e49e737d7b5d8a17fc575fd3810ab4495a88e73ee`  
		Last Modified: Tue, 03 Dec 2024 22:32:57 GMT  
		Size: 71.2 MB (71240920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933ab90a88816114ae116bd757c876eb44413901c2699659dffc92325a8501bb`  
		Last Modified: Tue, 03 Dec 2024 22:32:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb90820f994a13ba411ce9f13382e83c031ed0b2d2219db34d7e121af2ca4e4`  
		Last Modified: Tue, 03 Dec 2024 23:30:22 GMT  
		Size: 6.2 MB (6153816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0755a3f609dacb1c3c9cfd444c8e0e17d3164ff984a8c8b256ca23bfb5285abd`  
		Last Modified: Tue, 03 Dec 2024 23:32:07 GMT  
		Size: 1.7 MB (1711642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca049294665a12d4c46195094fc9caab2fe1dd23f4387a0bcafa5d4554ad85fc`  
		Last Modified: Tue, 03 Dec 2024 23:32:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:d34f32e4efec0fe90fb35c9ea61321bb53cbd7830923f55f6994fee7e22b2fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 KB (310615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3ff966024ddcb0d6b64a1ee4c2603f448aa7bb698535cc33c4fa10b1bde26d`

```dockerfile
```

-	Layers:
	-	`sha256:f83d644b47cbf45f33c3427c879684d93be2f3bb6a034dd204d813c0a3ad241a`  
		Last Modified: Tue, 03 Dec 2024 23:32:07 GMT  
		Size: 290.4 KB (290442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9073f9e18b020a4a883d3c1b52d5b8511b42396b8eb9972a0e5fc216f03d47ce`  
		Last Modified: Tue, 03 Dec 2024 23:32:06 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:6aa66a7c188127cf3b1d74c61ea008b95a1bdd86535cba563f3582710b036d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84682121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29cc61277738cb7914c72ff20d3bfd79b577ba6b5d721daae3058dc1dfa8244`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141e3fcf5173977fad664af74a255a69a2749551008af76945b144725f228f5f`  
		Last Modified: Tue, 07 Jan 2025 06:42:18 GMT  
		Size: 280.2 KB (280152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab153b4468df7f657167533fa78804e60b235edee0f04ec5dcc52a35b056da`  
		Last Modified: Tue, 03 Dec 2024 22:40:01 GMT  
		Size: 73.0 MB (72969813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9039b3f81c901f7abad17b0429809aa980ff70f25d072c8d64ee71f7db3e045`  
		Last Modified: Tue, 07 Jan 2025 06:42:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8aa38916b9a65afe6d745bc7b4405235419055139a947defb9ce792bb28b73`  
		Last Modified: Tue, 07 Jan 2025 16:55:39 GMT  
		Size: 6.2 MB (6200978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8fb1e6bc0540f6045137dc3088acea82454684beb33b47125d22823982d437`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 1.8 MB (1771406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788488d4f2b594a7b69ffa9ada90972f2be7de5973303ff5d5d6dee1ddb5270f`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:224cde432b86d4943a06974721e702e3be7c1723fd153c64411a1070d8127f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 KB (305797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914a49da35ae3856968dab023e6d0459b952fca4d12749f61dcda3b1a4bee0cc`

```dockerfile
```

-	Layers:
	-	`sha256:c767f61505dfabedc5ae5df8b49499a6c8fd64d5a2735c26bd1820abd6c01d2f`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 285.7 KB (285694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfeae3b8d465e03c17edddbdf5a198fd4d9a0c9a0c78e30622b17a5255100765`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:0189cfa4a4c02a3bb800a7e32a588f1264aa3f8eafa4b94e6ed4129cbe3ff2a7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2359343914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d72f15e0f30165074557b2b759d5db3e5947c39aee860af1bdf1e3877f65413`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:41:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:41:29 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:41:30 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:41:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:41:51 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:41:57 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:41:57 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:43:05 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:43:07 GMT
WORKDIR C:\go
# Wed, 08 Jan 2025 23:33:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:48 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 23:33:48 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 23:34:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 08 Jan 2025 23:34:57 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2203f205368ce649ffd4367d83cb7d0e0f349edd4a73d17bf72e1d1fd45547`  
		Last Modified: Wed, 11 Dec 2024 20:43:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a929050203563fde4afe1d48374621524ea8726dc8ca55d3c22d0ac7a798594`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1be8f168e721557e602e0b7a3a7cb7e068d12e159af7b67cbd570277d67b6d3`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a047a2e43f164719e30219f432eae6c44e556b5a49ad8de5c356eef5ceb9f2`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538affaf25305d64f324539f173d0eb2d2dd465cb1762b082450ad4c797f27c`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23c69a8ef4d7541c4f17aa73bdd2bc059fbf9e06bb80dba0c6780214385b946`  
		Last Modified: Wed, 11 Dec 2024 20:43:13 GMT  
		Size: 25.4 MB (25433638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8adf8499c2eb9b67d228fba4c9e69a29a2d7060f8b7c5592eacc3be4421710`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb262fe2ef81142570e16f48f8f03d4031993f7f4bdd1e8ddc6130f5ac401023`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 339.0 KB (338961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b81c31620602735496201938ab0373d338f5d0422cdb2fe31bf91e703561180`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027a3cd836a09077c7888a8a16d4e7bdf054357c81b2dfc19d8a0d373c88f51d`  
		Last Modified: Wed, 11 Dec 2024 20:43:22 GMT  
		Size: 77.3 MB (77349783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6072f4215eedb6bd6a3744f556ae0cd5807bf437d9168f5f06a714a4935e11ad`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ddd9caf64ad2db2b643ff3a12c821a4568fb6cab42c886d58ec94c55611183`  
		Last Modified: Wed, 08 Jan 2025 23:35:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9ad2ce3c975bdb8bb5a956ddacab8f088540115a28bdc8d3c28beab4329aec`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b21bef77b61f0857b5cfc4fdb89f2c1c74d5346d5c5813e145c298a5b86642`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5b2d84d7d2cf78270c6457f8ab87188b8d84fcbe934749c67f5a31364f3a84`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633f1f09b1a52df9107d2afb46ee59d7d749f2b38fb8bf1a07b9e0ba04de6e6e`  
		Last Modified: Wed, 08 Jan 2025 23:35:01 GMT  
		Size: 2.3 MB (2331000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450a1c75f8730f0ad6bb33eaa49034a16cc2b79db5b5098a4afd873dcc3ed769`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:ea06d27be71f8ef91c6d6f553d93e6261efe59e77edf8ca72c562150017510d1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2119855201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688816f8244428a55ae1ec4bd192c597ce0f04d19edda948e46a80ecfd9bf8ce`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:39:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:39:36 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:39:36 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:39:37 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:39:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:40:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:40:47 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:40:54 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:40:54 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:42:12 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:42:13 GMT
WORKDIR C:\go
# Wed, 08 Jan 2025 23:33:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:32 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 23:33:32 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 23:35:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 08 Jan 2025 23:35:04 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f3bbeb4e2782220c87261e5e9d61855baf0ace86081d92be83026dd5e8fcc2`  
		Last Modified: Wed, 11 Dec 2024 20:42:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241e544e87d299e404e0055ac6a3d562110f5dbac92ab40f5274757c352361`  
		Last Modified: Wed, 11 Dec 2024 20:42:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d65d85ef63918a2fe84d0a5c56c3c6b83838ea5060fc445cb586acaa3fc316`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3d89f6bf6b5749f5d1a48d1e66e0f5882aa8e07e2d3218b9a7e1f59c2dda0c`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54a47581ed1b6b7629a8abc75e2e6e45c36975a21ec95b65e8106e75c34aafa`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81645ff46b23f2588b64411ee4dd209ad3383c3b4376b70fa25b258296a5d05`  
		Last Modified: Wed, 11 Dec 2024 20:42:19 GMT  
		Size: 25.6 MB (25561663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619f9252e7182af97b30c9a01c651c8a8f83c521db1c842279b8adaf45bc17ac`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39e01c2f476af7e5c6236de3ec31577c6d3d4491c44d2e5cce185341f9d8a19`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 328.3 KB (328344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd74620f512254e194320e032040d3c01472e9f9c304c960171132f8a838cb7`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05934960da5aa39d60d727548d37d080612ea4164a25e09b3c3d9e310f6fa14f`  
		Last Modified: Wed, 11 Dec 2024 20:42:28 GMT  
		Size: 77.5 MB (77463395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d829f35d8061698251f21a9c2ad8cb0d344ddb5465b577017415f89f82d50aa`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0302b0fa76f2e0e3678e4ec6e3a77b56966df7cbd7788ff083f096d58f66eb9`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153b2e9a08ab9b486a49339207a0e3c35851ead887e82207dabf747c69de0ef9`  
		Last Modified: Wed, 08 Jan 2025 23:35:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb03d015e74d14f0a3566de1e456b2c92453ba713a378af8d0608061e2f9d06`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7da9a44214dc454bfc9248a3e2db15fda48ce69c4c8f426122a25540d604d20`  
		Last Modified: Wed, 08 Jan 2025 23:35:06 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0fc2d732d66c3b5aeb005f494441963afb2427e6b8eb07d9f0e0855a328c31`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 2.3 MB (2314451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165c45570296cf141f1579eb94ca900ddea076099f18b3f5e5dedf41c600a449`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

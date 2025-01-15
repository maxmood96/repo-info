## `caddy:builder`

```console
$ docker pull caddy@sha256:3e225bb553d4a38be7a952d007da2ee78c4567b5b4380592041325446eb37420
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

### `caddy:builder` - linux; amd64

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
		Last Modified: Fri, 13 Dec 2024 15:04:23 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:39:29 GMT  
		Size: 5.9 MB (5939538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf2b30687fe7e3fa4f927c76a4e43b2db14a66b0e42a32ea9ddcdfa17e0c7d`  
		Last Modified: Tue, 14 Jan 2025 20:50:20 GMT  
		Size: 1.8 MB (1835035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed24074f0fd5dc780dad0af8b4260d4205b3b89d7a666396c5b415abc85f2a8`  
		Last Modified: Tue, 14 Jan 2025 20:40:17 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

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

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:7dbecd7ecfdd06d7d1a6ab5dcb628e6d1303531be81f9e21dd4eaa626ed0ff25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83479808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae2009151cb702b3885023cfb88506af3c05ddabee1d3c3b2c62b654cb21fc8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
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
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69a70656b186536acaa70853744917e9a0b358e5475d451816ac52af6b864bc`  
		Last Modified: Wed, 08 Jan 2025 21:57:17 GMT  
		Size: 295.8 KB (295828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569843b3031b27806b4332ef906025ac81fe5ab3623a61a6d2306598bfd512bf`  
		Last Modified: Sat, 14 Dec 2024 01:29:44 GMT  
		Size: 72.2 MB (72198540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c486c35fbfbee8e03d7545b2b84ec7403d41d80c0b7da546b890610d47b8d50`  
		Last Modified: Tue, 14 Jan 2025 21:12:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99fa140c44987e7c840e3fbb9da14b5322e714525aa0688a30bb8ee51c4095f`  
		Last Modified: Thu, 09 Jan 2025 09:58:08 GMT  
		Size: 5.9 MB (5883087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16e7ccb64be2bead3e1245822a24f7500f2c3d1d067108fdf1d5f7e1af507dc`  
		Last Modified: Thu, 09 Jan 2025 09:58:08 GMT  
		Size: 1.7 MB (1730291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fb69e9217b5e797552af7bf1911000eb1ad280e795a5e1242ec23f65cad763`  
		Last Modified: Tue, 14 Jan 2025 21:12:29 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:45511251f23e7ec20ec67f0109b2cebbd1f8dd33b143ac49dece3f5c1cf1f8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc122653cea718e369b6b865c300efe3eac63c723d4e14987b8b5de6c99e1e6`

```dockerfile
```

-	Layers:
	-	`sha256:64380e8843fee378df551574e57439fb5ca0524d4b51948c7a1d34fe93d78d8e`  
		Last Modified: Thu, 09 Jan 2025 09:58:08 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:64e33a2dd8cd1ce718f609d48603d97f5f6395e0cf90b042ab6e36f8cf66036b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82680536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2875950e26bbb8ff7b2c72a132ba8da67938cc51dccf8d68602a7de0943c22`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
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
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Tue, 14 Jan 2025 20:45:20 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bf03070cac649166aa1b87cea610615d91250eff95c905990cea3c1d510e67`  
		Last Modified: Tue, 14 Jan 2025 21:12:25 GMT  
		Size: 294.8 KB (294759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af30004a6a0d94684e60c07bbc44989294b76634fe7cc182dfb2140b1e8c877d`  
		Last Modified: Wed, 04 Dec 2024 07:17:17 GMT  
		Size: 72.2 MB (72198441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524147eef8a9efa3143645376e1ffd9fe20097c93fdbc4b37746f8458b35b112`  
		Last Modified: Wed, 08 Jan 2025 22:35:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e31952d86190ab6aa98e9d3da3456f860e133f2591388f7f1a7c645ba63eca5`  
		Last Modified: Tue, 14 Jan 2025 21:12:24 GMT  
		Size: 5.4 MB (5366962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7d50a4c2e8145203d514b1e38cc654bf379fc7a2e29db2086ad964c87c97fe`  
		Last Modified: Tue, 14 Jan 2025 21:12:24 GMT  
		Size: 1.7 MB (1724269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4114d25b4004acc40beb62135f42bbfd768ccb9292847c59c4174bf7b57621f`  
		Last Modified: Tue, 14 Jan 2025 21:12:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:c27e25ef2c30789d1551617641d72e9d746256e9a5b4c96a9448aaad8ddf4a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 KB (316640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709181d033470a6fefb985236b79a4582d8688c2092a1cc04011cf9907c05a73`

```dockerfile
```

-	Layers:
	-	`sha256:a88ca0e084bb329a5af44f3a3b8ea5023c9f2bfa1dc1ca5727548e47bbdf24dc`  
		Last Modified: Thu, 09 Jan 2025 11:25:47 GMT  
		Size: 296.4 KB (296416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75794f36b3e75e907fafb5d832c8f4355a3e95b52fcfbb71b066b8218f849eeb`  
		Last Modified: Thu, 09 Jan 2025 11:25:46 GMT  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bbfae82243a829e9593fc0bfa97d3af1e37d77a3ad44cb05cd24a3d7c27988bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82821366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b5cecb64f1613043c25f61325038d0cd930aa64b1d4e7bbd3a5e1869d71bf0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07219bb1974a1749c2d7ad8e3c5020b1a9e55023216926da79ccd2a39b4eef`  
		Last Modified: Tue, 14 Jan 2025 20:44:49 GMT  
		Size: 297.5 KB (297474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8f326b04424eb2027d1f0e3255fe568d71a5567f894a08cd86605ebe51c58`  
		Last Modified: Wed, 04 Dec 2024 01:41:07 GMT  
		Size: 70.7 MB (70673417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717d10fbda110fc1d40b782baa31672954bcb08f995d44aaa54b47b2e932ea70`  
		Last Modified: Wed, 08 Jan 2025 22:41:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882e321bde4bdafa446fd1962d0797576f6796af509709c90bc9c950f4f87af6`  
		Last Modified: Thu, 09 Jan 2025 08:06:55 GMT  
		Size: 6.1 MB (6057684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f9ce18a6d85ad9b615e22c173348cca2a4a931d053cbeff8929e3989ed049c`  
		Last Modified: Thu, 09 Jan 2025 08:06:55 GMT  
		Size: 1.7 MB (1701431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f450489d3203cf7216825f2b97f7a72d29b66d33a662a714cc5febf746b50a`  
		Last Modified: Thu, 09 Jan 2025 08:06:55 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:c8dfe9bd4c0c38b45d8b1004f15a5bccdfb59a3b22a76383d4d74ee64275a32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.9 KB (313896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632aeeba6dcd23d8d76d0ae8b1e0096eef6b1d4fa2d983233a732cd835010401`

```dockerfile
```

-	Layers:
	-	`sha256:0ffae5512ba0ede60669830d2c5dd7a07a7f90552c2c41a5ed555aea67027d5b`  
		Last Modified: Thu, 09 Jan 2025 08:06:55 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aa61246a64fa4c5309eebf67940c88f819045dcf9fa57d1335b5387f43b9166`  
		Last Modified: Thu, 09 Jan 2025 08:06:55 GMT  
		Size: 20.3 KB (20269 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; ppc64le

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
		Last Modified: Wed, 15 Jan 2025 00:41:59 GMT  
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

### `caddy:builder` - unknown; unknown

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

### `caddy:builder` - linux; riscv64

```console
$ docker pull caddy@sha256:a45e57f1bfcd58b6ec0beb70f57537290c3c3c2df4bc34391d5c5005d6df4a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82774314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b76baeca89dfbe0655a2b863f5686b67feefe51e782a9e19fb9e0995aca924d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
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
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Tue, 14 Jan 2025 20:50:16 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816c3897a63cf7689a7beab4c1f1af77b6f15050c01df55852c40f878936f63b`  
		Last Modified: Fri, 10 Jan 2025 17:00:34 GMT  
		Size: 295.4 KB (295445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56ea5001679e325e9959f4e49e737d7b5d8a17fc575fd3810ab4495a88e73ee`  
		Last Modified: Sun, 15 Dec 2024 05:37:37 GMT  
		Size: 71.2 MB (71240920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91765e269643a82d9c52e463ec9314f16a49e4edf046b093e4c7b6aac5679190`  
		Last Modified: Fri, 10 Jan 2025 17:08:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b95057ce9d218a22da5963ff05f8fbba23f186bd0ffcade887a905203f4c6f2`  
		Last Modified: Sat, 11 Jan 2025 23:01:52 GMT  
		Size: 6.2 MB (6153790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab846edf1f8a4518970f1da18ac1d888ef6776b675cbe7ec55d36c0e11338aa4`  
		Last Modified: Sat, 11 Jan 2025 23:01:51 GMT  
		Size: 1.7 MB (1711642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500068c56edbc81af147962cd5f4034e528a787379500145681594efb19b6eaa`  
		Last Modified: Sat, 11 Jan 2025 23:01:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:84a3031b7de61ffe4fddc9aa43d775ea0996c17fb97f9f91b8cec2aa98da18d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 KB (311835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e7c9dd0533a805ef42c952e93218bbcdc6ab95090c8f7ad30c01c14dbf60e2`

```dockerfile
```

-	Layers:
	-	`sha256:8af7b29dbf5dbcf466a41c65d2df8ef46d723ebf28accfbb6f1ccd038fa02030`  
		Last Modified: Sat, 11 Jan 2025 23:01:50 GMT  
		Size: 291.7 KB (291662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9ff30dd40808a22f732757cde3950df668a208c01c7e0563a9ee0cf8fb6bc57`  
		Last Modified: Sat, 11 Jan 2025 23:01:50 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:b274f8dd383df498d31561f5d6c0715ed1374cb384376c126f2681c08d81b9f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84701722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3566230429cb554f2cff357992ec2191aab423a4a1c579122bc7f34d2d70cc6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
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
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Tue, 14 Jan 2025 21:25:41 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27beb3ecfc66a05c4717a47324657a7da44cd7a01b554efb4ced3c7c613a567`  
		Last Modified: Wed, 08 Jan 2025 22:26:47 GMT  
		Size: 295.7 KB (295699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab153b4468df7f657167533fa78804e60b235edee0f04ec5dcc52a35b056da`  
		Last Modified: Sat, 14 Dec 2024 06:33:23 GMT  
		Size: 73.0 MB (72969813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b18bb26d7f919379e3435b72f0bfcde89d64d33f8a4e91239032ce6aea3006`  
		Last Modified: Wed, 15 Jan 2025 00:41:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da55635fbf3355a7ded653fb76b0c9c654c9904f5ceda76c81f92971f996ba8a`  
		Last Modified: Thu, 09 Jan 2025 08:57:16 GMT  
		Size: 6.2 MB (6200889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9a7ac51a37e68ebd6f365fb1770f179e6e9fe37bdd70d4a32f8e7324aecf1d`  
		Last Modified: Thu, 09 Jan 2025 08:57:15 GMT  
		Size: 1.8 MB (1771409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81966008c57ec3c456ceeeaf5accf57b7a3be870fbb8237350d28b1cdf1399b1`  
		Last Modified: Thu, 09 Jan 2025 08:57:15 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:b2be29fc27e6ac6cfead8596d9e7b8dbd91f84559454b44c20bc534fc0985b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 KB (311675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ce0d4d9103bee4e797b63897da48bd4f8c93a3a6a743be33cec8927776b5fb`

```dockerfile
```

-	Layers:
	-	`sha256:5818d606e8838f4f98ed5c22af0e46e9e1a8c95b43779ab6f02386058e15fb1a`  
		Last Modified: Thu, 09 Jan 2025 08:57:15 GMT  
		Size: 291.6 KB (291572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1baf3395fadbb7b8dd4889a63c4761c199e546a8eb617f56b382d6dee350ab73`  
		Last Modified: Thu, 09 Jan 2025 08:57:15 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - windows version 10.0.20348.2966; amd64

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
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2203f205368ce649ffd4367d83cb7d0e0f349edd4a73d17bf72e1d1fd45547`  
		Last Modified: Sun, 15 Dec 2024 00:00:18 GMT  
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
		Last Modified: Sat, 14 Dec 2024 10:07:14 GMT  
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
		Last Modified: Sat, 14 Dec 2024 07:10:56 GMT  
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

### `caddy:builder` - windows version 10.0.17763.6659; amd64

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
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f3bbeb4e2782220c87261e5e9d61855baf0ace86081d92be83026dd5e8fcc2`  
		Last Modified: Sat, 14 Dec 2024 07:34:50 GMT  
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
		Last Modified: Mon, 16 Dec 2024 06:00:34 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54a47581ed1b6b7629a8abc75e2e6e45c36975a21ec95b65e8106e75c34aafa`  
		Last Modified: Fri, 13 Dec 2024 17:44:42 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81645ff46b23f2588b64411ee4dd209ad3383c3b4376b70fa25b258296a5d05`  
		Last Modified: Wed, 11 Dec 2024 20:42:19 GMT  
		Size: 25.6 MB (25561663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619f9252e7182af97b30c9a01c651c8a8f83c521db1c842279b8adaf45bc17ac`  
		Last Modified: Sat, 14 Dec 2024 07:35:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39e01c2f476af7e5c6236de3ec31577c6d3d4491c44d2e5cce185341f9d8a19`  
		Last Modified: Sat, 14 Dec 2024 07:35:08 GMT  
		Size: 328.3 KB (328344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd74620f512254e194320e032040d3c01472e9f9c304c960171132f8a838cb7`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05934960da5aa39d60d727548d37d080612ea4164a25e09b3c3d9e310f6fa14f`  
		Last Modified: Sun, 15 Dec 2024 17:15:40 GMT  
		Size: 77.5 MB (77463395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d829f35d8061698251f21a9c2ad8cb0d344ddb5465b577017415f89f82d50aa`  
		Last Modified: Fri, 13 Dec 2024 17:44:50 GMT  
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

## `caddy:builder`

```console
$ docker pull caddy@sha256:ad96b8121b095ad03ebe20937af903889e4940bb9f45cc698b008b8a5f585ff7
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
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:34ae73712ffd97809d971881808c4d0db881fa69b56246d4b3863e419e88b006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85746881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2ed03f0ed7ae14b85040ad36bc6008712203d454b13cbadf8abb8e1a7447ef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 17:30:49 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.6
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOTOOLCHAIN=local
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOPATH=/go
# Wed, 08 Jan 2025 17:30:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 17:30:49 GMT
COPY /target/ / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce2e074618e32c3d89dbd6c92352bb9516d71f79f18064e92ce561be95371f0`  
		Last Modified: Fri, 14 Feb 2025 20:38:47 GMT  
		Size: 294.4 KB (294377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd968b00abc2f44f5d74b014d2b833a05dd020b5f534f19dca853c409df33466`  
		Last Modified: Tue, 04 Feb 2025 21:17:30 GMT  
		Size: 74.0 MB (74045855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9983b2b2d9829df35b292baa9463c2ffcefaa85f5f7bcb8ef243ef80a9e5116`  
		Last Modified: Fri, 14 Feb 2025 20:38:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f84a7bc4b793932575684a6d40e0da77854d18e98cf2ddf9a009974c9e1f09`  
		Last Modified: Fri, 14 Feb 2025 22:53:39 GMT  
		Size: 5.9 MB (5944123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090413e706e5c6c633c06cce7ae0d5bcd9b7ed54789adc8d71b929b79b053fd4`  
		Last Modified: Fri, 14 Feb 2025 22:53:39 GMT  
		Size: 1.8 MB (1835036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c333b2c50aac3c2fea03e94fbeb588d412ec4ff5eab3d008090318319dafae5`  
		Last Modified: Fri, 14 Feb 2025 22:53:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:73f0fc6c4bdc1a236e086ce35189c9413ae82ddd0e62c97d04a0e66b6f44ffde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 KB (313626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c810c8205ea04cc40f2b6d74c58990d9535ccdac3ed8f9fbb564c1a167a4196`

```dockerfile
```

-	Layers:
	-	`sha256:02d783f2f3b5a1c7b10c3172b3c67b756ab976175d9658eb6a63f7948d8ed327`  
		Last Modified: Fri, 14 Feb 2025 22:52:43 GMT  
		Size: 293.5 KB (293523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4054c7be88689c7132544f9172a14c0333e041ebea6d83fca14fb26f9cca5e44`  
		Last Modified: Fri, 14 Feb 2025 22:52:44 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:73a4cf26ec35bcb94a2849092046d8ef7b0f83a55bb8afd16dc9100f34e42c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83484059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9adcf18ad60b5b1598196c25ac2720b35997d34938fabcbf161099e10494802`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 17:30:49 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.6
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOTOOLCHAIN=local
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOPATH=/go
# Wed, 08 Jan 2025 17:30:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 17:30:49 GMT
COPY /target/ / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
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
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 19:26:24 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737183f74dc0d53c3f643812192622c6f3f2d83b37c68a4ca351085678413983`  
		Last Modified: Sat, 15 Feb 2025 00:23:02 GMT  
		Size: 295.8 KB (295833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bc15bd6dff137475f22b6631116b4ea034384c5e21f31d1ca51949d8498e95`  
		Last Modified: Tue, 04 Feb 2025 21:50:42 GMT  
		Size: 72.2 MB (72195315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acaf6206fb5347d12cf0b4c629d378fd24607c9e451a2d64fe57c8d90abf671c`  
		Last Modified: Sat, 15 Feb 2025 00:23:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef388c2b032ca3398585993291d0abea370bcc9164cc66204974664806af9b7`  
		Last Modified: Sat, 15 Feb 2025 13:52:51 GMT  
		Size: 5.9 MB (5889499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3e91aeeab9274bbe04508f50b56f4d84fbe604b4de2dc5ac6bc282c0f78199`  
		Last Modified: Sat, 15 Feb 2025 13:52:50 GMT  
		Size: 1.7 MB (1730290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641c194052ee24c3d788b673594c528dff46f68ceb8a375a4a6efb8c80ef16d0`  
		Last Modified: Sat, 15 Feb 2025 13:52:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:27737e2b0b67b37c7088f2d36fcdabf42bd3c14babbc39d0b37ce1bad7e6854a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2be9301c685be9c80a5790c16299e93c86167128868dbdf7d63de122e7c515`

```dockerfile
```

-	Layers:
	-	`sha256:ed1625f79781d3ef237f1b2c843110a95ddde6e6be6b53595d787b1ee37609bd`  
		Last Modified: Sat, 15 Feb 2025 13:52:32 GMT  
		Size: 20.0 KB (20009 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:31e804a8616ebfa7dcfbd668328f3e6b9b1c5479692c9d1a09b1eb983a2e45ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82679076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc08c0db34f54bd37646e8bf862484ce00dd637ab748fcee615e4b601855740`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.6
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOTOOLCHAIN=local
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOPATH=/go
# Wed, 08 Jan 2025 17:30:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 17:30:49 GMT
COPY /target/ / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
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
	-	`sha256:889cc3ffbe9c2ad3a046f41cd3f0630b058873fcf3511968c20cf71cc826b741`  
		Last Modified: Wed, 05 Feb 2025 04:50:33 GMT  
		Size: 72.2 MB (72195337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82215554fc72369f17b924c4a3c16fba157828cb00294fc110f92c5adddb543f`  
		Last Modified: Wed, 05 Feb 2025 14:38:37 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68138c250441d1b03ff358917b7ab0048c951c310fafde8c2a5bbf269671447`  
		Last Modified: Wed, 05 Feb 2025 14:38:42 GMT  
		Size: 5.4 MB (5368609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d783e4087fa9fee2d65e6d87137e674e60062ef0a67b938ecc2382a8a2e7ae8`  
		Last Modified: Wed, 05 Feb 2025 19:44:27 GMT  
		Size: 1.7 MB (1724267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714e9021e6e97175328fb8f30d421c47a19f97be4f8516f88fe8a83c3ef5e2df`  
		Last Modified: Wed, 05 Feb 2025 14:38:37 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:d36c309ff4ccddac1a2abd26784a9b2ab64e2ea31f005e079291c6578579a11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 KB (316640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed51f0f2136e087faf763a7cb5f29edff2d6f3be7d0806fb8ea8323a535e8cd2`

```dockerfile
```

-	Layers:
	-	`sha256:c995eca9fa3272b6609c44aea22e1a068edd49f4c969d6d92ffe9dd02b4160ea`  
		Last Modified: Thu, 13 Feb 2025 04:52:29 GMT  
		Size: 296.4 KB (296416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e31f0440d5984d7d925061e9e4d1095d3ded492e17f9f194e4ee01642af27e9`  
		Last Modified: Thu, 13 Feb 2025 04:52:30 GMT  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:0fe68f9946f74fed504c5775d002cbe7492ff3d28e8468868272aeabd4862cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82823512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbad3cfbd501e6dcd6109367fa8e872f66c403feebe0243ce2290eb22668c87a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 17:30:49 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.6
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOTOOLCHAIN=local
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOPATH=/go
# Wed, 08 Jan 2025 17:30:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 17:30:49 GMT
COPY /target/ / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
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
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80759e590e8e3c48fc0aec3f03a2c66f281d0b1749e8673f0abece25ac95150`  
		Last Modified: Fri, 14 Feb 2025 23:34:55 GMT  
		Size: 297.5 KB (297467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7476bebdd25fd50c45ff4efca639719b1581613f3017c85f08e38a2d5a441f`  
		Last Modified: Wed, 05 Feb 2025 02:32:51 GMT  
		Size: 70.7 MB (70673148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98239ce14d325c828ea701d57f11c2981d61b8489d9c768da68c23d88e545b2`  
		Last Modified: Fri, 14 Feb 2025 23:34:55 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d137106448bf4104eafede7757b8a5c2a8aa06149e28ef415d3d1ff4c8252a`  
		Last Modified: Sat, 15 Feb 2025 11:00:04 GMT  
		Size: 6.1 MB (6059718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414a3993d1fb6c84ca924000759a69f5ba8c7097fe63c45314a38c6519536227`  
		Last Modified: Sat, 15 Feb 2025 11:00:05 GMT  
		Size: 1.7 MB (1701424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7627108d5060ae55e973f64b8a1cf746ca6b1a744b50cd43a0108c581c349c75`  
		Last Modified: Sat, 15 Feb 2025 11:00:05 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:8bbb2f7345effbf68ab329f3b5470765b0decb86412d4ba9d95405a784349fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.9 KB (313897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbe9542a6f61b8cbba1489ec60def905e047584a56ac611f3ad4bfd6d217b37`

```dockerfile
```

-	Layers:
	-	`sha256:d308d34d089162af92721f790f8e20e848d705e7505ac37c041a9419419e7962`  
		Last Modified: Sat, 15 Feb 2025 10:52:33 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a363dfd8e0f58219940aa119564c78555771a23f0f8137699bca709ea32695b1`  
		Last Modified: Sat, 15 Feb 2025 10:52:33 GMT  
		Size: 20.3 KB (20270 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:379123f8f7a565e59be596335eabcb0dfbbbe66e5ff55eeb6ef070b4e97d65a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82673519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa3e8d578f461c893ff1651fcfea003c5332978563cef31afe30f920cef6a61`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 17:30:49 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.6
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOTOOLCHAIN=local
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOPATH=/go
# Wed, 08 Jan 2025 17:30:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 17:30:49 GMT
COPY /target/ / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
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
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 14:35:49 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed507fc5d64b2e3137d471f9a078a4add3c6cf38450cd6a53d7d3aef6ffec60`  
		Last Modified: Sat, 15 Feb 2025 00:30:46 GMT  
		Size: 297.9 KB (297887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bc8515280eafb56fff5db8a8a3f9b1389a9563753c21ecf558291e30e86e2a`  
		Last Modified: Wed, 05 Feb 2025 01:00:24 GMT  
		Size: 70.8 MB (70838106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc9bcdccee2a0d8cfef38751716fc121927828c03875947a88b2ebe2cd13ad9`  
		Last Modified: Sat, 15 Feb 2025 00:31:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5785d2fc7c554435fc327853c4c0c87282fb332dc1786622d635cae7c8108f9`  
		Last Modified: Sat, 15 Feb 2025 13:51:10 GMT  
		Size: 6.3 MB (6265656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92014eef74432b5a817152069dd05d7e4e42b9b3f6dcfc7dff7d950291c024f7`  
		Last Modified: Sat, 15 Feb 2025 13:51:09 GMT  
		Size: 1.7 MB (1695599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132d27dbf099665a9123560bf318b53a192e2489332e5ef3898689e66dfb5259`  
		Last Modified: Sat, 15 Feb 2025 13:51:10 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:c86b1db690451f47431eb0180ad551ab639cad6b131ec3ecc2ccbabab0933f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 KB (311839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bbe5060c469b768feaf09e648228c690911911eb4f62ad447919c4107887ec`

```dockerfile
```

-	Layers:
	-	`sha256:21b324796153f69f1e584a360e6e98ad932c22c3bb4a2a45d6844b50aad8db81`  
		Last Modified: Sat, 15 Feb 2025 07:52:30 GMT  
		Size: 291.7 KB (291666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece6c0310a66c0faa6413a0dc614aafa6aacee36f7e8a17a6b5ecbc883f19e18`  
		Last Modified: Sat, 15 Feb 2025 07:52:30 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; riscv64

```console
$ docker pull caddy@sha256:12b587c0f835fc3f2184fe7233e91d2580a53c91c7e76cf528f9fe4d9e11e0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82771919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328982060872931dc05a246a310b43cf7b0640fa0b085ac717c26ca0e4b93444`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.6
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOTOOLCHAIN=local
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOPATH=/go
# Wed, 08 Jan 2025 17:30:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 17:30:49 GMT
COPY /target/ / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
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
		Last Modified: Wed, 22 Jan 2025 11:57:28 GMT  
		Size: 295.4 KB (295445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bcbafcf86e581c838713d6aa93c05a7dd1d0a064c9bb430f1bc2e58c504369`  
		Last Modified: Tue, 04 Feb 2025 22:04:15 GMT  
		Size: 71.2 MB (71236403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48a91ab3130df220b3603ac4e3497efb8af727ffbf26271e2564f354f009f7a`  
		Last Modified: Thu, 13 Feb 2025 00:27:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40620a122fbab51a40411b05a2726d79ccae63f7926da920a6952aae5102fa68`  
		Last Modified: Sat, 08 Feb 2025 06:11:50 GMT  
		Size: 6.2 MB (6155912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2be592ca0d5818174e0a83e1382dd89757ea635e8826d92c9217c1f021e589`  
		Last Modified: Sat, 08 Feb 2025 06:11:49 GMT  
		Size: 1.7 MB (1711641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308e7c62b98b4c064983b2fb097c0aa9e416991453bf4bc8c184c1515e7f140c`  
		Last Modified: Sat, 08 Feb 2025 06:11:49 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:c142b3e16a8370d96e598b626790f023ae5aa9338768b5f2e70859759af1ea8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 KB (311835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b16e73d2754b74098cf0df15d34e14d1a997d572ee7f832e22419bdb4b4868`

```dockerfile
```

-	Layers:
	-	`sha256:fd0ddaf09cc02171163474b7c6ffb8e790770cb6fe9b968a025949f8f9c50dc9`  
		Last Modified: Thu, 13 Feb 2025 04:52:34 GMT  
		Size: 291.7 KB (291662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a46f2b9bae3c18dde577d95958be57468cab827a245f1aeae22177293bc79c00`  
		Last Modified: Thu, 13 Feb 2025 04:52:34 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:ab21ce56d2087654d2ce6a20a51a19720e62a5f49a311435d4bea81528e16442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84696578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602bd64ee6e99885bf5fee5312dbbdabde8367e950d94e523b0032b44907f6f7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 17:30:49 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.6
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOTOOLCHAIN=local
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOPATH=/go
# Wed, 08 Jan 2025 17:30:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 17:30:49 GMT
COPY /target/ / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
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
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 14:36:22 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4709930918ff9545f85bd2e4cac3925cbdbb8c11ea2e9a6b1dfe4c10549f601f`  
		Last Modified: Sat, 15 Feb 2025 00:31:30 GMT  
		Size: 295.7 KB (295701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d83ebf4a35a49c6c207a7926517818d83cc97461292683260a534049331701e`  
		Last Modified: Wed, 05 Feb 2025 07:00:24 GMT  
		Size: 73.0 MB (72961478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0501f1685b438b21469e927fb77aa865d530a5f9aace4df50f67f0783564b250`  
		Last Modified: Sat, 15 Feb 2025 00:31:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff4612baa306cbbb0ffbc61b465adb516ceaf800e4e0c4aaeebd01fa516472f`  
		Last Modified: Sat, 15 Feb 2025 10:09:56 GMT  
		Size: 6.2 MB (6203277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236bda709ea73fd663d75cba3b3135102a047a7f48da0210665bb33621f8b7d3`  
		Last Modified: Sat, 15 Feb 2025 10:09:56 GMT  
		Size: 1.8 MB (1771408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab0836a2755ead326ae0ec5f1ffc645ea662b68200504d490e7caede4070b00`  
		Last Modified: Sat, 15 Feb 2025 10:09:56 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:1b3f2f40ae6195cbe83a7cb252aa67249fa895730568f8240255546724e2461c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 KB (311675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53246e39f2f04a09c6ae057d13c006cbc0b1af89f2715627a2616fb529473f91`

```dockerfile
```

-	Layers:
	-	`sha256:705f5050e216bbfedd79c745be07588afb1c4ba4ef0aed4a6fb7ed54b68e5308`  
		Last Modified: Sat, 15 Feb 2025 13:52:38 GMT  
		Size: 291.6 KB (291572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:455c5e420013a68376331d284da849663c38af36efdacfee52b7f284681e4375`  
		Last Modified: Sat, 15 Feb 2025 13:52:39 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - windows version 10.0.20348.3207; amd64

```console
$ docker pull caddy@sha256:07619251ff68ebef8405436fc43a57c58e605b56a0bb95d8b4216b8f1a1572a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2369360662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed69c31d4e15c835acc81136b46d9827ff79895df810edd9810e0f7d8ca37fb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:38:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:38:11 GMT
ENV GIT_VERSION=2.23.0
# Thu, 13 Feb 2025 00:38:12 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 13 Feb 2025 00:38:12 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 13 Feb 2025 00:38:13 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 13 Feb 2025 00:38:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:38:33 GMT
ENV GOPATH=C:\go
# Thu, 13 Feb 2025 00:38:40 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 13 Feb 2025 00:38:41 GMT
ENV GOLANG_VERSION=1.23.6
# Thu, 13 Feb 2025 00:39:49 GMT
RUN $url = 'https://dl.google.com/go/go1.23.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '53fec1586850b2cf5ad6438341ff7adc5f6700dd3ec1cfa3f5e8b141df190243'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:39:50 GMT
WORKDIR C:\go
# Thu, 13 Feb 2025 01:17:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 01:17:45 GMT
ENV XCADDY_VERSION=v0.4.4
# Thu, 13 Feb 2025 01:17:45 GMT
ENV CADDY_VERSION=v2.9.1
# Thu, 13 Feb 2025 01:17:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 13 Feb 2025 01:17:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 13 Feb 2025 01:17:58 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Wed, 12 Feb 2025 22:14:21 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b061b5942e3cdbf7ce63e1737064a535c1157574597314d919826580dbfa943`  
		Last Modified: Thu, 13 Feb 2025 01:08:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4053a70a2b1d69be7f850865177c2488dafa1e9fc818971edb00d0a4860ff309`  
		Last Modified: Thu, 13 Feb 2025 01:08:41 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc341f9ad471b7cfc01d646d543787e9abde725df143d6482734a66257ebca`  
		Last Modified: Thu, 13 Feb 2025 01:08:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d65dffbedce720f1d21797718f127a0041140836dbeac38ecb02050dfd19e4`  
		Last Modified: Thu, 13 Feb 2025 01:08:42 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ce400040308fc484161b1fbb96ad97e662ebe872067db820d942302d4cc643`  
		Last Modified: Thu, 13 Feb 2025 01:08:42 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d393ca8ee01c3541828b14536ba00e2daceb38790294c7cce7f8b5c7e9b4a55e`  
		Last Modified: Thu, 13 Feb 2025 01:08:44 GMT  
		Size: 25.5 MB (25450269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b03fcbe1d81c1441f8a5db3414017c1707b8ffc96545561b188e2e2958c90fd`  
		Last Modified: Thu, 13 Feb 2025 01:08:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa137d1f777695d48c23e22d2e409c5c19768f73898c91f97c580e1ec3f7f8`  
		Last Modified: Thu, 13 Feb 2025 01:08:43 GMT  
		Size: 347.1 KB (347141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6cadc9eae823f8303acc0b330df5b0dfa87970a195b7b5467aa6d298aa8308e`  
		Last Modified: Thu, 13 Feb 2025 01:08:44 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6a4ada837e113b0263909122a35cf9f3c1a482eff3a2fa7b847cf56c00e4c9`  
		Last Modified: Thu, 13 Feb 2025 01:08:48 GMT  
		Size: 77.4 MB (77365479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e019f1689554d1cc7b61fac20947a339a48a08647e4ef1b78d4ee8d6bd2d5024`  
		Last Modified: Thu, 13 Feb 2025 01:08:44 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac279f142c4f4e46a599b3ba1cb73f17a8fe2ed43a283b50d399fb2ba8c7705c`  
		Last Modified: Thu, 13 Feb 2025 04:52:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b72d6324de7d293e9163df9723c971aea3d5591d6ea486ed2576804d65e393`  
		Last Modified: Thu, 13 Feb 2025 04:52:38 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7bd69e532087f8eea828c3701205e51f68cf8f34663e6fa39a7af66e9369609`  
		Last Modified: Thu, 13 Feb 2025 04:52:38 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c50dd0cacf22a1c318f5362a0df2d8b32930b0eab21a7efe8ef6503bc603da`  
		Last Modified: Thu, 13 Feb 2025 04:52:38 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdb86a9893ed13641a0365290640ce2f3a20ac99ec55870d5757ebc80dc948e`  
		Last Modified: Thu, 13 Feb 2025 04:52:39 GMT  
		Size: 2.3 MB (2322863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795da10f3df28bc92396583e46ec89e4f0083a0984d07da7c4180b874f0bbf6b`  
		Last Modified: Thu, 13 Feb 2025 04:52:39 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.6893; amd64

```console
$ docker pull caddy@sha256:3e8705d53c87a9edc2e45a93a782f5b1190c1ceee53f51c118ff1325b47ae4e8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2242329732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d59d81a36d95186bd70accdee1671a70fdf7ff30f4fc49cbaa8b7baf4aa8cef`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:30:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:30:46 GMT
ENV GIT_VERSION=2.23.0
# Thu, 13 Feb 2025 00:30:46 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 13 Feb 2025 00:30:47 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 13 Feb 2025 00:30:48 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 13 Feb 2025 00:31:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:31:13 GMT
ENV GOPATH=C:\go
# Thu, 13 Feb 2025 00:31:20 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 13 Feb 2025 00:31:20 GMT
ENV GOLANG_VERSION=1.23.6
# Thu, 13 Feb 2025 00:32:32 GMT
RUN $url = 'https://dl.google.com/go/go1.23.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '53fec1586850b2cf5ad6438341ff7adc5f6700dd3ec1cfa3f5e8b141df190243'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:32:34 GMT
WORKDIR C:\go
# Thu, 13 Feb 2025 01:18:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 01:18:10 GMT
ENV XCADDY_VERSION=v0.4.4
# Thu, 13 Feb 2025 01:18:11 GMT
ENV CADDY_VERSION=v2.9.1
# Thu, 13 Feb 2025 01:18:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 13 Feb 2025 01:19:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 13 Feb 2025 01:19:03 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d136fde42e6e2bc91f5956d1e8ac33fc4084914e9982e16f2ddaa1a241fdfafe`  
		Last Modified: Thu, 13 Feb 2025 01:08:44 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af2a1616935cf9566cec5a3c62a7dc245e7c5af888145e48ea7ce3fbca2aa52`  
		Last Modified: Thu, 13 Feb 2025 01:08:44 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d857ea95e03ce72ba0cb753a4ac08d710617d9747b4146f005f4a4b2ecf7da`  
		Last Modified: Thu, 13 Feb 2025 01:08:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efeacb0745fe69e3fc393b6abd1b8685a3e6d4b442f3418888b88c570adef40`  
		Last Modified: Thu, 13 Feb 2025 01:08:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1944d354e141d0e6fab9973beb428631e15a12c7cf102d9164712bfc5ec2774e`  
		Last Modified: Thu, 13 Feb 2025 01:08:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a76bdabf7b0e00c0c95acbd81a11afb3c9e98e719a1e05fd131f224f1b6f5e`  
		Last Modified: Thu, 13 Feb 2025 01:08:46 GMT  
		Size: 25.4 MB (25429808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858d3ced918bc0d0c407242159a57e218ee53b65f3f1969c90bb33dbb289d37`  
		Last Modified: Thu, 13 Feb 2025 01:08:45 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b24259778625afcce89689eef634fd77a27e7d5bf6abdd9d17baa857abd515`  
		Last Modified: Thu, 13 Feb 2025 01:08:45 GMT  
		Size: 333.0 KB (332954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376aee295847eb57d8099b4a71488b21729dc5500e739f4d7a50ed8b99b48736`  
		Last Modified: Thu, 13 Feb 2025 01:08:45 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472f935a883cd53a550d97a611da1241b94339b34c6c9df9658cb698b8209d5a`  
		Last Modified: Thu, 13 Feb 2025 01:08:59 GMT  
		Size: 77.3 MB (77348156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ada68cd6c4090eea38d86ac6a8ca00d468b62ca4954c03e16a04d3985a57a0d`  
		Last Modified: Thu, 13 Feb 2025 01:08:46 GMT  
		Size: 1.5 KB (1453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ece25bc91fc0a7327a8f64cafb4cd0237ade2cfff8b55578f024ab9da6f91f`  
		Last Modified: Thu, 13 Feb 2025 04:52:36 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b5ce8692b8608aaac9d4b9bb62fa76c3c32ed01043d0652c9825d915045748`  
		Last Modified: Thu, 13 Feb 2025 04:52:37 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85a00f6d0a73986ac0efc0998a656c23ad2bb894ef1adaf894836a5af69a707`  
		Last Modified: Thu, 13 Feb 2025 04:52:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793ef1769ceadaed34f7a4fa52de949adce1b874dd8f84acf364d74ffa85d844`  
		Last Modified: Thu, 13 Feb 2025 04:52:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b4f2d615714064f24ef30715eba1159833340bf464fbb1df4726bebec90d3c`  
		Last Modified: Thu, 13 Feb 2025 04:52:38 GMT  
		Size: 2.3 MB (2292786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdd7fac213579eb6578cb8f231fbd80bf84b007ddea648ad35c5be58e7bb65e`  
		Last Modified: Thu, 13 Feb 2025 04:52:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

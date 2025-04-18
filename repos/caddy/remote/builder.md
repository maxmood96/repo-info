## `caddy:builder`

```console
$ docker pull caddy@sha256:1609bfce85bd4452a875e4d459f25e602c484b5a36e9c015511b5bdbd3539784
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
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:eac1b03dd8b8978d1ccc39fb509885bf8398617a9ff8919f8e10c04106d5a221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85758322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce2142b62e6f7757077b8f833462d8a80540a82a099be1ab232bb83502345ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 17:30:49 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.8
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
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfa0bcfca99d825e816b83475e52b3bea0bb348f93bc880d3e8a335b29be061`  
		Last Modified: Tue, 01 Apr 2025 17:07:27 GMT  
		Size: 294.4 KB (294389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eabb1d9476e2a74ca18f982fa2cd1a722047e0ac01f746221f76c65893fe80`  
		Last Modified: Tue, 01 Apr 2025 17:07:22 GMT  
		Size: 74.1 MB (74057106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957bedc73fa324a37dbcdc23afe3f306b015f4f9d38d04a9d918033937dc60e3`  
		Last Modified: Tue, 01 Apr 2025 17:07:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e24672d8f714239d9281a160a9e70617580226384232ec58d226002d837f9e`  
		Last Modified: Tue, 01 Apr 2025 17:10:28 GMT  
		Size: 5.9 MB (5944303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463f39d4bda3c9ab6ca9e1192981fa4ac830189ea265f9c1b11b524cb35864c`  
		Last Modified: Tue, 01 Apr 2025 17:10:28 GMT  
		Size: 1.8 MB (1835037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ce61a7bf41de9ba7c06e9f363c3ab4fe13fe72e645910970948b296606a6d7`  
		Last Modified: Tue, 01 Apr 2025 17:10:28 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:dce7d960d7dbd7c081785d111667fb917b6ea928965a7396fa90222852a3e965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.3 KB (307326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869537309def234519874a671147634bf2f2517b37de7acdff9950e17dc9c58d`

```dockerfile
```

-	Layers:
	-	`sha256:8f4e62d96cb3a322a8b16f8bbf6cb87fada5d54d66b215630a70479e292c1661`  
		Last Modified: Tue, 01 Apr 2025 17:10:28 GMT  
		Size: 287.2 KB (287223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4478e779468c4ecebdf0886c43878d601854c1e73c8e2f494553995edde7380`  
		Last Modified: Tue, 01 Apr 2025 17:10:28 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:db053f51d9f2d1c0f7171a0586dbbd35d5932f1e20cad9e125baf6acba62c5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83506022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197b9f43ec9413155d2f4b103422748988524a7acc5d3d51c70af957a12f64fe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 17:30:49 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.8
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
		Last Modified: Fri, 14 Feb 2025 18:28:14 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737183f74dc0d53c3f643812192622c6f3f2d83b37c68a4ca351085678413983`  
		Last Modified: Fri, 14 Feb 2025 22:17:11 GMT  
		Size: 295.8 KB (295833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a415b7da0e074a06dd7f3bed619e8b43397e534d21699c1d51a3c500f8db3e07`  
		Last Modified: Tue, 01 Apr 2025 17:08:22 GMT  
		Size: 72.2 MB (72216340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8066a0cb57eced0bfc44ad89662fb9532de3a1e2822b5b9a8801439b12046e`  
		Last Modified: Tue, 01 Apr 2025 17:08:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d64172f44e9c40db3fd4b0f3a7232ec7bc1b345d96bb363f79549759d7676e`  
		Last Modified: Tue, 01 Apr 2025 20:29:26 GMT  
		Size: 5.9 MB (5890437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3850b02ec53cbce3de47202402edfe8977518f1b876a1b3495531261c2ab4cf`  
		Last Modified: Tue, 01 Apr 2025 20:29:27 GMT  
		Size: 1.7 MB (1730290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1774549a6714488bd83360133fe43ee7742e61fbd21414b3fbc203336337b13`  
		Last Modified: Tue, 01 Apr 2025 20:29:27 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3f18084a54981a31bbf2f7a71a433ab5245dda0eb638a012d04360b2375a3236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8914f376a29fa4444fca91592db9ab2f8c613678c4ffa0da99d3951adb278c`

```dockerfile
```

-	Layers:
	-	`sha256:7023c97038c63a5b556c8e922f29d565f4cb811dddd4895e40fad7d1f084cbc8`  
		Last Modified: Tue, 01 Apr 2025 20:29:26 GMT  
		Size: 20.0 KB (20009 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d84a01bc49865c978e1da87681a635401bf2893b9f0b402d06af4a2ea4c8358c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82704538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8357fab6530d7197b6616a3dc641ec3c7676242a7e1b17046ed2cad9fccb35`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 17:30:49 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.8
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
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d221261a6f80d203497a55ccecdc4912512b230fd036ba2df848b8144d67bf`  
		Last Modified: Fri, 14 Feb 2025 22:11:53 GMT  
		Size: 294.8 KB (294754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06a665a1ebb95de508ffcf731226ca563bb487405f3c6fa714b02910f09db70`  
		Last Modified: Tue, 01 Apr 2025 17:10:55 GMT  
		Size: 72.2 MB (72216588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7995d29722705d5eaafaa1440945d953da3ae8c47a032d2be6802e09f2a1de27`  
		Last Modified: Tue, 01 Apr 2025 17:13:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3179868b71250d5da264aa7d6f4a690836c1dd1786d7c8f3472d3a90a8ddadd4`  
		Last Modified: Tue, 01 Apr 2025 20:48:46 GMT  
		Size: 5.4 MB (5372373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe7b9aa081550d2f0b83ac92673853e3fe572baff050d4e86339dbd78d361f0`  
		Last Modified: Tue, 01 Apr 2025 20:48:46 GMT  
		Size: 1.7 MB (1724261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6fa450e1ead6ea30b5b1d05893751d78dae1ecf65f69109b2b87880a399fc5`  
		Last Modified: Tue, 01 Apr 2025 20:48:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:32812559fa1172ae64baaa8e6e9f610a9b59724d121f8f54658c612aeaa188ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.3 KB (310340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca9315c0b8c60cd046b4b52976b1fac280bd9cefbe2403d31a5f382b3222415`

```dockerfile
```

-	Layers:
	-	`sha256:558b6601204c10822bc04e74e1768652e2f1493cbbb6656f4664fd3f451769e5`  
		Last Modified: Tue, 01 Apr 2025 20:48:45 GMT  
		Size: 290.1 KB (290116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3424c61f57613bf73542b55402cc201405cf5928ad3ce84f9db9bfb71030545b`  
		Last Modified: Tue, 01 Apr 2025 20:48:45 GMT  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:3665662b36469fff3893c8191bfe9f60417c26cc182e6df3ba5b3dc2db6f4668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82836390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fd13a9bd8170cf12b965be6125243a74ae6551dd1e6bd2e2a34e4588abde3c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 17:30:49 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.8
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
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634366ca850b96a5c7a0780daec3499faf6933b86acc8a8e99b70a5264f8f00e`  
		Last Modified: Mon, 24 Mar 2025 21:31:30 GMT  
		Size: 297.5 KB (297463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66ade281fe97eb70cd41e06b79a8aec5f7db1277a91fb7cdafb8dd984e5d365`  
		Last Modified: Tue, 01 Apr 2025 17:09:49 GMT  
		Size: 70.7 MB (70686122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd4ce6e94ec6dd72db5b6c6b7e3a34a04740bbe981797de44666af61850c7a`  
		Last Modified: Tue, 01 Apr 2025 17:11:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e49b0f2deddbc82353e52429d0cc8b31d5e581ae9313853501480a54e0bbc4a`  
		Last Modified: Tue, 01 Apr 2025 21:56:49 GMT  
		Size: 6.1 MB (6059623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1714dce4a30bd0088fd27768071e508b204f26f51e623b6441f24505f54339`  
		Last Modified: Tue, 01 Apr 2025 21:56:49 GMT  
		Size: 1.7 MB (1701426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cb74703acd278efc1ff1a9321b56d9b515d8d1bdade0122a44ac9b27e16af`  
		Last Modified: Tue, 01 Apr 2025 21:56:49 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:720199e1694cc1f7d0b13c1623ac7cae02732439fe5ab7c72f72e121fd5dc19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 KB (307597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf885f607bcefc3905232adca45120293c6c152fb837a6b178833e4f8e85ce6`

```dockerfile
```

-	Layers:
	-	`sha256:a21fd9e9b0b30b0a39a067f533644fc5dad0172b407a04677d3014683a0273f2`  
		Last Modified: Tue, 01 Apr 2025 21:56:49 GMT  
		Size: 287.3 KB (287327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a99975372e7f29c3b0bc9312fd92ce58241451c19ec1fe7bf191a18bea9f8308`  
		Last Modified: Tue, 01 Apr 2025 21:56:49 GMT  
		Size: 20.3 KB (20270 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:4df8481544c82659a17e8991c07b294b37b27550a7c45db3e48ff08842886a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82683459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d48393ce0bf9f6f05e3def3ead8b0d4bb5de1f9d56c57eb549c203839e9827`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 17:30:49 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.8
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
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15784993a892df626148136e939e65b594ed2f1456345704a3272ec8fd984c53`  
		Last Modified: Mon, 24 Mar 2025 21:51:53 GMT  
		Size: 297.9 KB (297899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16583f8c93ef98b97bd72e4a4fdfdcee9c10b68c76f5e4e50474d2aba6ec4a4a`  
		Last Modified: Tue, 01 Apr 2025 17:12:02 GMT  
		Size: 70.8 MB (70847690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a30041ae6438b91df114eaaac29a3195746866c6aa6ca72a5eee537836fdf9`  
		Last Modified: Tue, 01 Apr 2025 17:13:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a2f069e39aa10b229512c9ff2caa30e4b944d4e05c6ffe8af0bcea7d6f31bb`  
		Last Modified: Tue, 01 Apr 2025 17:44:41 GMT  
		Size: 6.3 MB (6265999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b1b66517ce7ba4e5d34c5bc3ac1735b7986c285efcaf67cc040c51fb963ef2`  
		Last Modified: Tue, 01 Apr 2025 17:44:40 GMT  
		Size: 1.7 MB (1695599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5416fb719e42fdabd423b8cb5ba9b91d15f8f9ddd086edb1b27d3253a4e1b4b`  
		Last Modified: Tue, 01 Apr 2025 17:44:40 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a32d399718aede30b7dad6d9e321721b306781fc1db556895169344d095e4b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 KB (305539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9340f2e9e2db34e635fd7244cd0fb7dee7a1785b421477db7bba953582f8fe22`

```dockerfile
```

-	Layers:
	-	`sha256:7ee7ab83e593df107ca70b88d37e87592a50238bcae70652abf9ceeeb83fd16d`  
		Last Modified: Tue, 01 Apr 2025 17:44:40 GMT  
		Size: 285.4 KB (285366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:249258d406287e3be7f9c31c523a6faa47d468bb720f61369b1f11412081ddee`  
		Last Modified: Tue, 01 Apr 2025 17:44:40 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; riscv64

```console
$ docker pull caddy@sha256:c882f35964b0514e3fce7a259d104f100b78f7ee5ab05b29a158197485babc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82803594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b187a9d2e74ce1cb5bc60a4f6810fcac527b919d713d74bb6cd99b02773d88e9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 17:30:49 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.8
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
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 18:57:42 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fa0de6a35b9467baeb7b28786dc580aa911bf02b2cc33ac7a44500327139a1`  
		Last Modified: Sun, 16 Feb 2025 06:13:57 GMT  
		Size: 295.4 KB (295446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416db10308598ecd7ddb7789053d372c356ae615b33daa5a6cd829ab8145de15`  
		Last Modified: Tue, 01 Apr 2025 17:20:53 GMT  
		Size: 71.3 MB (71261467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc55856597f2a179b96c947ed062e6740a7d87fb3b8347c0cfdd71f1025a09e6`  
		Last Modified: Tue, 01 Apr 2025 17:24:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0dde2daa348d3627a5018336e2d2ce1d0918306e6a1804cefaa57a8df218b2`  
		Last Modified: Tue, 01 Apr 2025 18:52:40 GMT  
		Size: 6.2 MB (6161216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbae2d38ac70ca9dde9e21d722da4ebfab4cc6ae1c5bb71129c3eaa7b10c58e`  
		Last Modified: Tue, 01 Apr 2025 18:52:39 GMT  
		Size: 1.7 MB (1711641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77330b6ef9e5beec99561729e14509aa0a88c5bb96a3d64a03bed5e5e46fb8b`  
		Last Modified: Tue, 01 Apr 2025 18:52:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3cacae743f7d2225d4a03fe80d456399fbb00b39e13bf5ae94504d32b0fb1d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 KB (305535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40881263816a1b1f7cce296f798b69e8f22ebd7cc41ee879e58712a724a46c77`

```dockerfile
```

-	Layers:
	-	`sha256:23bed703450ef186ab11a616a1a9dc00d2d43b4b48482cf6e216d125db8dece8`  
		Last Modified: Tue, 01 Apr 2025 18:52:39 GMT  
		Size: 285.4 KB (285362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0520663f741ffb41a09a56ab303a499ee0eb6c52fea2fcfa17e4c62b19cb81e`  
		Last Modified: Tue, 01 Apr 2025 18:52:38 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:9fd2cc215641ff280b04222156c0276923cee6d9123ebafa7f0a9394ea942906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84717584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454eb2fe67a07c27f6a1fdd88b8e40da0e3ee3f9d8526eb3d8084b9b039ace2d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 17:30:49 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.8
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
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f378f0ab9f92249cab05739adecf3318eef414f2bb034b8f1580eac04a7de99`  
		Last Modified: Mon, 24 Mar 2025 21:30:12 GMT  
		Size: 295.7 KB (295703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc10476fa2ad3d94c6a33bfc40cad375172e24a2b95fab33fe07809206fafcc`  
		Last Modified: Tue, 01 Apr 2025 17:11:13 GMT  
		Size: 73.0 MB (72982315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c64de63742f4e9c729d59d3686c9c96181a11ad431f8eff1fb75c70ba5957b9`  
		Last Modified: Tue, 01 Apr 2025 17:12:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09a56e37cfd1d04f8dff16438ecd1bcb7c682fd03abdc2ded80fd773e846175`  
		Last Modified: Tue, 01 Apr 2025 19:39:46 GMT  
		Size: 6.2 MB (6203444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b271deb194b0fab45946e60d15bea8bee872f4e1a668e7bc6f60a26ceb009a3`  
		Last Modified: Tue, 01 Apr 2025 19:39:46 GMT  
		Size: 1.8 MB (1771408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eef9e5cc4100c02de8f9ace7a8cc55db808552b0cd935ab55054c3eae1c8611`  
		Last Modified: Tue, 01 Apr 2025 19:39:46 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:5ef9c64aa548b983dba0c488de9a9b58f20b99c4550e2940faf56d38fa1fc2c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 KB (305374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19fd12ace0befec902a62daa89e6f8bbb1417dd5925e00d28b08f1d1fe8fe50`

```dockerfile
```

-	Layers:
	-	`sha256:f9c21e971c07a740c05420fc0a9d353d663791609936bce7ac8f66caca51bf47`  
		Last Modified: Tue, 01 Apr 2025 19:39:47 GMT  
		Size: 285.3 KB (285272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0348bc245d04f2dc2f807b82df72d5553f6f7fbab8c71f7f0e8873dcd079d796`  
		Last Modified: Tue, 01 Apr 2025 19:39:46 GMT  
		Size: 20.1 KB (20102 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - windows version 10.0.20348.3566; amd64

```console
$ docker pull caddy@sha256:d4e86bf6840a1ea13a005a401c20c216b234903bd2f1197361ead0ba332cdaf9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2404807153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0da42cfbff5bec8a997142271e79d222c34e5c5effed5da17081ec4532e93a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:16:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:16:08 GMT
ENV GIT_VERSION=2.48.1
# Fri, 18 Apr 2025 03:16:09 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Fri, 18 Apr 2025 03:16:10 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Fri, 18 Apr 2025 03:16:11 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Fri, 18 Apr 2025 03:16:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:16:32 GMT
ENV GOPATH=C:\go
# Fri, 18 Apr 2025 03:16:38 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:16:40 GMT
ENV GOLANG_VERSION=1.23.8
# Fri, 18 Apr 2025 03:17:44 GMT
RUN $url = 'https://dl.google.com/go/go1.23.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e0ad643f94875403830e84198dc9df6149647c924bfa91521f6eb29f4c013dc7'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:45 GMT
WORKDIR C:\go
# Fri, 18 Apr 2025 04:17:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 04:17:27 GMT
ENV XCADDY_VERSION=v0.4.4
# Fri, 18 Apr 2025 04:17:27 GMT
ENV CADDY_VERSION=v2.9.1
# Fri, 18 Apr 2025 04:17:28 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 18 Apr 2025 04:17:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 18 Apr 2025 04:17:41 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928c0f321e05845c89914a556c7a2028df7f108e64de9acd742cb59298319052`  
		Last Modified: Fri, 18 Apr 2025 03:17:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f045b5bc6f0695f8405c8c4eea8d45e4f5165454f8131efafdaa50b08d5907`  
		Last Modified: Fri, 18 Apr 2025 03:17:53 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727a19edaa05302e09ee84440abab477807119f191e756f3876f28d486ca3fb9`  
		Last Modified: Fri, 18 Apr 2025 03:17:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68eba7b5f0531e6fbeaf609d3720cb7829a8e0b772a6ba7dd9c9ed2bfed841c6`  
		Last Modified: Fri, 18 Apr 2025 03:17:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ad297dacea5705ef3dcd8bb787de66d167ed4f3df5044ed9c552ad74f6cb7f`  
		Last Modified: Fri, 18 Apr 2025 03:17:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b962fcde5950e1f060f23fdc1ded93030c5766e6bb724043933d39e0b870266`  
		Last Modified: Fri, 18 Apr 2025 03:17:58 GMT  
		Size: 51.2 MB (51194774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280b3e3a762067b28280926bc4906934d3329c9cd8643fad3431b8615acfeacf`  
		Last Modified: Fri, 18 Apr 2025 03:17:49 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808afa509f106e399586ea6bec970ee894c10600120f170ef8d8492886a4aeaf`  
		Last Modified: Fri, 18 Apr 2025 03:17:49 GMT  
		Size: 336.8 KB (336759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed32f2f547c14055e5e7ca27a20b78467efed5fa74e3cc6202c4db38d02a54a`  
		Last Modified: Fri, 18 Apr 2025 03:17:49 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac74ed2dce7eb887902902d56f1af4c81bafbd34924c14a79b7c75d1e7dcdcfc`  
		Last Modified: Fri, 18 Apr 2025 03:18:02 GMT  
		Size: 77.4 MB (77370408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311a828d4d5155fb8ac9729979a81963763e30a69570e3399a9a7e3d93c57ad5`  
		Last Modified: Fri, 18 Apr 2025 03:17:49 GMT  
		Size: 1.5 KB (1507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2def552a896a879addb693b85d219fe54067d6a83ef3918c9a2f4b81f51c4439`  
		Last Modified: Fri, 18 Apr 2025 04:17:46 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d5b78d505266ad4ac38836e47bbcdb25ae0e5f30c88b4c85cf9e5dfa0088d1`  
		Last Modified: Fri, 18 Apr 2025 04:17:45 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b28048981923642bbaca32aa947602ee865c35d31e38ba211e0ac7415210cc`  
		Last Modified: Fri, 18 Apr 2025 04:17:45 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ff39c735a1eb2a02ef1820ebc7cc7bb31d80941093513ce19ef6f9efada7d8`  
		Last Modified: Fri, 18 Apr 2025 04:17:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad75a75d045db1ac2a60a5926ac6af7aff2c8e609ac51d4a3405f8a748a7ec5`  
		Last Modified: Fri, 18 Apr 2025 04:17:45 GMT  
		Size: 2.3 MB (2305744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846f7e842a48ccbb06dcb8915f4e4881a61c10cc8819c12e81f64290a3a13393`  
		Last Modified: Fri, 18 Apr 2025 04:17:45 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.7249; amd64

```console
$ docker pull caddy@sha256:71e472e03591ea50e1cb07b532e43cfa1951ccc48433aa3c4175dd41b0a941ca
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296731047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891f49f0eed5b25d8e3838cb0d5303a5e7d83605e709209ec42b1217917ec06d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:17:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:17:07 GMT
ENV GIT_VERSION=2.48.1
# Fri, 18 Apr 2025 03:17:08 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Fri, 18 Apr 2025 03:17:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Fri, 18 Apr 2025 03:17:09 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Fri, 18 Apr 2025 03:18:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:18:03 GMT
ENV GOPATH=C:\go
# Fri, 18 Apr 2025 03:18:09 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:18:10 GMT
ENV GOLANG_VERSION=1.23.8
# Fri, 18 Apr 2025 03:19:19 GMT
RUN $url = 'https://dl.google.com/go/go1.23.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e0ad643f94875403830e84198dc9df6149647c924bfa91521f6eb29f4c013dc7'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:19:21 GMT
WORKDIR C:\go
# Fri, 18 Apr 2025 04:16:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 04:16:04 GMT
ENV XCADDY_VERSION=v0.4.4
# Fri, 18 Apr 2025 04:16:05 GMT
ENV CADDY_VERSION=v2.9.1
# Fri, 18 Apr 2025 04:16:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 18 Apr 2025 04:16:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 18 Apr 2025 04:16:42 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58abf569d39be3c925dc5f3f86dc1a988b54666b1ef1e12e53e7a71ceee179`  
		Last Modified: Fri, 18 Apr 2025 03:19:25 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830f09db3a63bcefe67c5e4c9edf039dd6ae6d2659ad1a8c73e98ad7cba6f5f6`  
		Last Modified: Fri, 18 Apr 2025 03:19:25 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714665fd638a59d67ec9f069d157ce0dce974ed7c9285c968cddc8627580f434`  
		Last Modified: Fri, 18 Apr 2025 03:19:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad74e1639eca81ea7f6918389decfcbd99eff8cc06d3b45df134905fe3ee644`  
		Last Modified: Fri, 18 Apr 2025 03:19:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4aa0dd71bcec799d3139dbf32c3b593be611239852195e362549d5ef53b12f`  
		Last Modified: Fri, 18 Apr 2025 03:19:24 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b03fb9f9ed271b4b8ba462e9599108f4f231edd3e9e31882613bf832581c5da`  
		Last Modified: Fri, 18 Apr 2025 03:19:30 GMT  
		Size: 51.2 MB (51198821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3807dff106c6843be9a5701c1480f12b6adc9107b47aa9ea3ebb5d581578496d`  
		Last Modified: Fri, 18 Apr 2025 03:19:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b8fa9bc2097fbe08d4713ba5b159b9111273e3cd51f3277f14ae56ed5dd74f`  
		Last Modified: Fri, 18 Apr 2025 03:19:23 GMT  
		Size: 332.8 KB (332775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61592680fbb790793d61381979f3bfe77e4832b89285cb3f7574a7f00dca59d1`  
		Last Modified: Fri, 18 Apr 2025 03:19:23 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88a6a4c6fe241e1cb17c9b14ce9eaaab1556394d408c7d194990d713b0b6584`  
		Last Modified: Fri, 18 Apr 2025 03:19:36 GMT  
		Size: 77.4 MB (77368125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac59c8176cabc693d38bb28cba053ca9b77e720f96eaa27ee36b62afedcbf233`  
		Last Modified: Fri, 18 Apr 2025 03:19:23 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773c895a04994047de08f3f8863ce0eaa74467648ade7b8b8a3a7cdf960fe31f`  
		Last Modified: Fri, 18 Apr 2025 04:16:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a6c544f1ed7c26dd9a0c400121eb56087d38c970f76a82c48b845070fa60cd`  
		Last Modified: Fri, 18 Apr 2025 04:16:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c230b51e27834248da729131f5e97bbce441d5561008186229a25239d5a5c2`  
		Last Modified: Fri, 18 Apr 2025 04:16:46 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af34efb9f83e576c821d2e94814a666eaaa97f073fefca44919a3c1ac4a7dab`  
		Last Modified: Fri, 18 Apr 2025 04:16:46 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afa25ca600f3cf6f81896b2f58775b493aed62a8d2723bee5afb5a3cc88722a`  
		Last Modified: Fri, 18 Apr 2025 04:16:46 GMT  
		Size: 2.3 MB (2288587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb49f30a8f60f9bcb1d07c71d971a539bbef0af450aa3831f17cf0293a67b711`  
		Last Modified: Fri, 18 Apr 2025 04:16:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

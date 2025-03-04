## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:a7902c93ca1de37114726b30bef473d61bfe6f402d41e2d30b3bd54f33a1fe65
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

### `caddy:builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:a2f67a2ac2fbd3ffdb2484c9453ac0c249c8f704ef7f017ccd4a399fe64dc6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85760375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c158d3005d5a113d748855c3f24a7059b9898cbdc03718afd866649f756efd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 17:30:49 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.7
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
	-	`sha256:8833042f23b55b241bbb6352d36795dec58ceae053fa5e7f68b7da568ede5a71`  
		Last Modified: Tue, 04 Mar 2025 21:17:18 GMT  
		Size: 294.4 KB (294381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca661eb024f09b95cfdf77781effc26400df52d97566fbd0fd4d45a67c3a3e6`  
		Last Modified: Tue, 04 Mar 2025 21:17:20 GMT  
		Size: 74.1 MB (74059363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5acb76e968064ef973541dc9568ddcc77a62715cc268ca0282004a1349897d8`  
		Last Modified: Tue, 04 Mar 2025 21:17:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec853fc7b6998e009b618593e9e453c8705042bba4f8be9ec7b69436fd1138e`  
		Last Modified: Tue, 04 Mar 2025 21:56:34 GMT  
		Size: 5.9 MB (5944107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836e6b44f0011f60d37d379ae6d4cd14d260bb1c0d59b2f78872dc4ce422dc8c`  
		Last Modified: Tue, 04 Mar 2025 21:56:34 GMT  
		Size: 1.8 MB (1835035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27240b2158b54e9a1c7399976b5ecf43f84ecee5fa358bbdbd9e33ab5376df16`  
		Last Modified: Tue, 04 Mar 2025 21:56:34 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:cfad844f3874c81a219f585aa6699446f81e02cd8b68f2acb5fc2908772495d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 KB (313626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267076870af23ee4938d057511441ba7f26662ab11bc7014e95a726cb2aa5104`

```dockerfile
```

-	Layers:
	-	`sha256:2abb7562a46d420e73002f184a249a6e83c9c1f0083cb04faacacb4c488b5225`  
		Last Modified: Tue, 04 Mar 2025 21:56:34 GMT  
		Size: 293.5 KB (293523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e2a939ab29f163177ce21ae797c736b6a6412f150d0834f17ab29be7c86ec5b`  
		Last Modified: Tue, 04 Mar 2025 21:56:34 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:2df164977063356bf834eb6ad2220094c5be08e65a9abf6827c17d84640f24c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83508930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703cf4f611bbf943a836b824d8970fbdcbefbbcd1d98a56ad323a2c8428aa831`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 17:30:49 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.7
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
	-	`sha256:ae1cb9bb62b9d0a841b8f2a4b9854e99ce695e5ceae00236680a8554297b6011`  
		Last Modified: Tue, 04 Mar 2025 21:18:17 GMT  
		Size: 72.2 MB (72220141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016db1ed3f77e7a5d7aaea7e284255d170b6c3e2e4f105bbe130f5e36cf1e511`  
		Last Modified: Tue, 04 Mar 2025 21:18:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af139ba3ae2c0ce83cfb6a6804886c8fc89bfcab5bf3bc82c11cf2665988757`  
		Last Modified: Tue, 04 Mar 2025 22:00:38 GMT  
		Size: 5.9 MB (5889537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae48dd6828d92ebf4b96d50478b5c507c4480d75d45e5a137864beded066f282`  
		Last Modified: Tue, 04 Mar 2025 22:00:38 GMT  
		Size: 1.7 MB (1730295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8062c5c4a5264098bd0d3a9d46cdb00cc2a08e126e80e4cc74932683d98e529f`  
		Last Modified: Tue, 04 Mar 2025 22:00:38 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:960b589a5d2ec3f9ee25ddb700051b305e9611dbdde7b00727241ebe1f18d30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b331a841de7b9d0b1222353d290f11a6920813e80d09c301a5810e1a6a086b4`

```dockerfile
```

-	Layers:
	-	`sha256:6d2a17871c17306df7743b221e3d3d68098952b38efaa9d882c6402d96b3844d`  
		Last Modified: Tue, 04 Mar 2025 22:00:37 GMT  
		Size: 20.0 KB (20009 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:0b870b66d8eddfbf3e8a896179413d8eddd0945b501e5cc4e27a82e51244084c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82682228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a1b85ffe4ef0691d4bb7c28f4e6b58f1847f902fddbfc910f58dcf3e49ab7d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 17:30:49 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
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
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d221261a6f80d203497a55ccecdc4912512b230fd036ba2df848b8144d67bf`  
		Last Modified: Fri, 14 Feb 2025 22:11:53 GMT  
		Size: 294.8 KB (294754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889cc3ffbe9c2ad3a046f41cd3f0630b058873fcf3511968c20cf71cc826b741`  
		Last Modified: Wed, 05 Feb 2025 00:37:25 GMT  
		Size: 72.2 MB (72195337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edb51c859689070158c926ecd3be14df0a60ffd724c684f75244b4c92edae49`  
		Last Modified: Fri, 14 Feb 2025 22:12:35 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aa0e5c1770fe4e90d461a666a0d5b6f617045eaba4363bcaf8445fca567a15`  
		Last Modified: Sat, 15 Feb 2025 14:14:38 GMT  
		Size: 5.4 MB (5371310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b964c301ba00eb21736f33a14c8944a50da4cfe943afb51c2c5821e91029139`  
		Last Modified: Sat, 15 Feb 2025 14:14:38 GMT  
		Size: 1.7 MB (1724267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db73aa8c58303a4bf0868b1d6f8f640cdea309d77167ea793860b879578d8faa`  
		Last Modified: Sat, 15 Feb 2025 14:14:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:be54d80461756762458304da3381b9a14a1cade2b6daffbc746eaea42b6b4b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 KB (316640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef035fdd956fd6e4b6f339f1bae1956a2c9fa582b311a71a68c75e630721f5d`

```dockerfile
```

-	Layers:
	-	`sha256:713a209f692aaaeeba0f096f150147ec5dccfc72e39793ca704c0d41b46d9059`  
		Last Modified: Sat, 15 Feb 2025 14:14:37 GMT  
		Size: 296.4 KB (296416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a14c58132e993bc4aefd4dca9371f25aad98a1b9f4cb84fcc5c5440f0e9bf5c9`  
		Last Modified: Sat, 15 Feb 2025 14:14:37 GMT  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm64 variant v8

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
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80759e590e8e3c48fc0aec3f03a2c66f281d0b1749e8673f0abece25ac95150`  
		Last Modified: Fri, 14 Feb 2025 23:00:09 GMT  
		Size: 297.5 KB (297467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7476bebdd25fd50c45ff4efca639719b1581613f3017c85f08e38a2d5a441f`  
		Last Modified: Wed, 05 Feb 2025 02:03:26 GMT  
		Size: 70.7 MB (70673148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98239ce14d325c828ea701d57f11c2981d61b8489d9c768da68c23d88e545b2`  
		Last Modified: Fri, 14 Feb 2025 23:01:06 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d137106448bf4104eafede7757b8a5c2a8aa06149e28ef415d3d1ff4c8252a`  
		Last Modified: Sat, 15 Feb 2025 09:51:30 GMT  
		Size: 6.1 MB (6059718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414a3993d1fb6c84ca924000759a69f5ba8c7097fe63c45314a38c6519536227`  
		Last Modified: Sat, 15 Feb 2025 09:51:30 GMT  
		Size: 1.7 MB (1701424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7627108d5060ae55e973f64b8a1cf746ca6b1a744b50cd43a0108c581c349c75`  
		Last Modified: Sat, 15 Feb 2025 09:51:29 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

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
		Last Modified: Sat, 15 Feb 2025 09:51:29 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a363dfd8e0f58219940aa119564c78555771a23f0f8137699bca709ea32695b1`  
		Last Modified: Sat, 15 Feb 2025 09:51:29 GMT  
		Size: 20.3 KB (20270 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:0c479dcc249c093ce38b2532ed37ccbef647351f39314b6c16d4c3ccc63f7e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82680490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8153d7dbe2c7c1e3dd652af221ee87b0dcb70efa06a23f6457f1047f11a23e03`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 17:30:49 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.7
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
	-	`sha256:8ed507fc5d64b2e3137d471f9a078a4add3c6cf38450cd6a53d7d3aef6ffec60`  
		Last Modified: Fri, 14 Feb 2025 22:08:09 GMT  
		Size: 297.9 KB (297887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b779c76ba8e4f618430055356e4cdb1f87533e9b166106cb46110f4d3af0be3a`  
		Last Modified: Tue, 04 Mar 2025 21:19:05 GMT  
		Size: 70.8 MB (70845042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571ae3987a7ec42a4f42a58a2a934d2a7d22c898be9edabd7664843ce7b9f38b`  
		Last Modified: Tue, 04 Mar 2025 21:19:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16914a7583ec332437e5b296bf805fea5015b05c9b58d38486dc52707f7a9ae`  
		Last Modified: Tue, 04 Mar 2025 22:05:14 GMT  
		Size: 6.3 MB (6265688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf9b378c8efda63e5e1c9f91e7d9c93fc2b738ab5833444840028e665140e70`  
		Last Modified: Tue, 04 Mar 2025 22:05:14 GMT  
		Size: 1.7 MB (1695602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f203341fef407a3fd600d8d791ca4804314af40c1d2d153d85f646d30c891a`  
		Last Modified: Tue, 04 Mar 2025 22:05:13 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:cc96035246abb84b0f2d15b6840bfc7719d08e9390ee57f5c1151b6131b02c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 KB (311839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41204d9328f581d93ec69dc63c9754e21123f7e95fda20a0ad3efdd40352e732`

```dockerfile
```

-	Layers:
	-	`sha256:9a4747df257716e42138295227ec94f3b33dee12a7c569e54859e457c088297a`  
		Last Modified: Tue, 04 Mar 2025 22:05:13 GMT  
		Size: 291.7 KB (291666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be5c6277a9937d1f1d97cecd24e9aa795e91b201da686086dfe1c3f69d512855`  
		Last Modified: Tue, 04 Mar 2025 22:05:13 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:a095d4d5c9cea6e52fb1ab3b9d5caacfbb5a900516a61f1ecc3b3c12f703d663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82777543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac34cd113f24eda9030feb2e5e7799cceb658b7999afd4051e91e3fe191adc1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 17:30:49 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
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
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 18:57:42 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fa0de6a35b9467baeb7b28786dc580aa911bf02b2cc33ac7a44500327139a1`  
		Last Modified: Sun, 16 Feb 2025 06:13:57 GMT  
		Size: 295.4 KB (295446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bcbafcf86e581c838713d6aa93c05a7dd1d0a064c9bb430f1bc2e58c504369`  
		Last Modified: Tue, 04 Feb 2025 19:37:04 GMT  
		Size: 71.2 MB (71236403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a87c7edca534ac5fd6250fb3687aec0e050782057a8e5506e3a56381c90086`  
		Last Modified: Sun, 16 Feb 2025 06:20:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ac917e45e64a72e0d9eb5947523981184d3a9d1975af20302140c93006d241`  
		Last Modified: Tue, 18 Feb 2025 14:53:19 GMT  
		Size: 6.2 MB (6160229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695624c0c3b1c949a5a604265251640863798b3154106bc061c326ca88c305e1`  
		Last Modified: Tue, 18 Feb 2025 14:53:19 GMT  
		Size: 1.7 MB (1711643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2e05fdfec2b162828059487aebead60fd34f4d6327d0da5858bc35ed67468`  
		Last Modified: Tue, 18 Feb 2025 14:53:18 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:3f026db7b35c1084972b42ff99cb97c17d04f6245bbecf3cc35ad8ee4e1027e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 KB (311835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c18132ff43ed7df6c7bf03813fb94feb83dc26b486ea63ead2014ea0f70079a`

```dockerfile
```

-	Layers:
	-	`sha256:bf08bd568cbdb9714c364d1f12d33049f9d1a8b08aa8c2e5ea10a232826112ea`  
		Last Modified: Tue, 18 Feb 2025 14:53:18 GMT  
		Size: 291.7 KB (291662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dd38a4e2e2acab30694c0775dee8e760383bd8abc083b3a1a6b388280bffa13`  
		Last Modified: Tue, 18 Feb 2025 14:53:18 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:218b3066536eaccef4d3f273bb44ded4bbb6dc81ffaade1495abc201c97ddc6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84711497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6406d7afe048cbccd43e0a9f3a6d82a92c2bd06778e06ea932df4bbb6181fe75`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 17:30:49 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.7
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
	-	`sha256:4709930918ff9545f85bd2e4cac3925cbdbb8c11ea2e9a6b1dfe4c10549f601f`  
		Last Modified: Fri, 14 Feb 2025 22:45:22 GMT  
		Size: 295.7 KB (295701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83f7a8e85cbe9a2fce67304b2f652e1d1d59db68c7adbaf5b4c7fe73bfc303d`  
		Last Modified: Tue, 04 Mar 2025 21:25:09 GMT  
		Size: 73.0 MB (72976392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cffc597a4c5212ab088ce228a8190c5129e391f5f5a976c2f87a020dee1555`  
		Last Modified: Tue, 04 Mar 2025 21:25:08 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caedc0079c923057a796282f30c25ca41578015e2a618d0c5ec3394ae3a90384`  
		Last Modified: Tue, 04 Mar 2025 22:03:31 GMT  
		Size: 6.2 MB (6203282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da969188d9248a87b99c12651c6fa7a289988f4f9632214c42025c2ae0c41de`  
		Last Modified: Tue, 04 Mar 2025 22:03:30 GMT  
		Size: 1.8 MB (1771408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafc1bba09c8093679afe2ea1c23c85927f0f340216145f0795edf980dda5966`  
		Last Modified: Tue, 04 Mar 2025 22:03:30 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:27ddb34c3c0231970ab4fb17d10c973e1eb86eb0ea0be3be8ab43b4b13d744d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 KB (311674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e67573793e1daeebc75587b132010f3712f3740312a5688a76b81cbb7fdc23`

```dockerfile
```

-	Layers:
	-	`sha256:7976e9482b4bf3e7a8ece16b050c55ab97724e8caa1e3745db94ddb1302dbe13`  
		Last Modified: Tue, 04 Mar 2025 22:03:30 GMT  
		Size: 291.6 KB (291572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db3100eca048e9f21eee1727e2515eaef14e217f0b348b984686e03de9e82869`  
		Last Modified: Tue, 04 Mar 2025 22:03:30 GMT  
		Size: 20.1 KB (20102 bytes)  
		MIME: application/vnd.in-toto+json

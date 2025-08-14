## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:cc6c40aa7cdea02ef9cb99f3c4e4664ecdb6066ae93ae52ed5288afc511e1241
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
$ docker pull caddy@sha256:99d4d683d02906da5bd1ef567be8d0f30232b642f490ba8856267fc527ecc91b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90828986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e70b6d32a283eb0fe24ff67c2c5526da427b391d53a2268d8ae87ff23ffcb63`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.6
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOTOOLCHAIN=local
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOPATH=/go
# Sat, 19 Apr 2025 03:51:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Apr 2025 03:51:58 GMT
COPY /target/ / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /go
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_VERSION=v0.4.4
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SETCAP=1
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1194203d4ccc8b528b208a9b4e6efab8d3ac41b47bbbb63e83fd98480d7c1d`  
		Last Modified: Wed, 06 Aug 2025 20:23:39 GMT  
		Size: 282.4 KB (282419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a940d118df69e65d813962f75e391b9f336d5575e2428d7605391a03d7617d2`  
		Last Modified: Wed, 06 Aug 2025 20:23:50 GMT  
		Size: 79.0 MB (79001391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb35d9e8082ae2b6fccc96f05a3381fe9887fd89643bae306e19499bdb4a3679`  
		Last Modified: Wed, 06 Aug 2025 20:23:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d4c8a5acbe47b5888384b8b92d1684191e1beade3f87374ce0d37e4b124858`  
		Last Modified: Wed, 06 Aug 2025 20:35:39 GMT  
		Size: 6.1 MB (6071978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b29cfdaeb4390703d49294638460f133cae20471b3fff29bac1843bc6f9b47`  
		Last Modified: Wed, 06 Aug 2025 20:35:39 GMT  
		Size: 1.8 MB (1835035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29464e65f7ccf4092a397457044ae5769fa429346f729f2699314fce4f290b9e`  
		Last Modified: Wed, 06 Aug 2025 20:35:38 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:6d78f1427b93cca1040c2e51164a81e2cae6add22611aebbfcda14267584dd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 KB (312455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1cb2764ee7cd76a7d85787a51ba60500436acdf179760c8e9942b8a1b63fd50`

```dockerfile
```

-	Layers:
	-	`sha256:df38b3cc998762c1eb6b087d8b433053b6f24e838ac9e4e7818d00eeb9b5ff5a`  
		Last Modified: Wed, 06 Aug 2025 21:52:38 GMT  
		Size: 292.3 KB (292340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b112e54dc755a39909a9b644f9cdd04dda8c544008dbc1779bc38da1ec70b7c5`  
		Last Modified: Wed, 06 Aug 2025 21:52:39 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:5ccacfab16594676503e58e25a3592d3b1e3252f38fe0f6a70bc393a1818a4b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88530488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f854de61657e9260663f5e48613d63f67b2518e80e8783af8be85fc32cd5dc08`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.6
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOTOOLCHAIN=local
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOPATH=/go
# Sat, 19 Apr 2025 03:51:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Apr 2025 03:51:58 GMT
COPY /target/ / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /go
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_VERSION=v0.4.4
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SETCAP=1
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4a214d6543aa5b234ca6b16aa4d8e27cbc22cad32bed5ef48890ed7409c406`  
		Last Modified: Tue, 15 Jul 2025 22:48:38 GMT  
		Size: 283.3 KB (283275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b3ba9f970533f6149a8363a5d83a4d9e332b0d07d7a676c826af1231f37c3e`  
		Last Modified: Wed, 06 Aug 2025 20:24:48 GMT  
		Size: 77.2 MB (77158633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4f02d9c0d54748907f00c1ae7da2c5d9ad2a2b3fa2d66664e427b6b0a6157f`  
		Last Modified: Wed, 06 Aug 2025 20:25:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e9ed46c00ae3fc31ae5a7c2f9e9fc7b6a117509ac8e073dc76696811a9a19a`  
		Last Modified: Wed, 06 Aug 2025 20:40:40 GMT  
		Size: 6.0 MB (5993881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2fb0dff59415c5dcfa79d2e826f48f0416e0c11f57d578e288699bd2217991`  
		Last Modified: Wed, 06 Aug 2025 20:40:41 GMT  
		Size: 1.7 MB (1730293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07925edee023a603b72b9d4e53ab30d73629c98ba9717482c407d97d44ded5e5`  
		Last Modified: Wed, 06 Aug 2025 20:40:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:552f1358b6d2dab742032363795f99368182b6d5ad90448ee069eab1712b2209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c902b37c8bfb8c8f4bcbd363a3ce6c4b67bc22d82fd1d1f913cce402d84253`

```dockerfile
```

-	Layers:
	-	`sha256:55784597966154f1cfbdae3e9b0362d69d568ca500435900c9fe0699fdc5208a`  
		Last Modified: Wed, 06 Aug 2025 21:52:43 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:bfe9bdbea6d946752b6724a610b83fe04f3e3b5241f531f5d629b0fed5280fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87732051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b85f0a24e8908264536780f933b6c35750c91266a81d079c5b3af645dffcb7f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.6
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOTOOLCHAIN=local
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOPATH=/go
# Sat, 19 Apr 2025 03:51:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Apr 2025 03:51:58 GMT
COPY /target/ / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /go
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_VERSION=v0.4.4
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SETCAP=1
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce1ad2f4fb08bb90f837004e5025b472d374435573f34a4ee7d7287172cfa5e`  
		Last Modified: Tue, 15 Jul 2025 22:36:22 GMT  
		Size: 282.5 KB (282462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88a5f94cbefc9dfb0fc5ddfd7290567a6380a2423913712f975ff3f1d3af5d`  
		Last Modified: Wed, 06 Aug 2025 20:26:52 GMT  
		Size: 77.2 MB (77158492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcd8a9a35afe023c1b33457e81c7a21c35b7c9be873ac300e817b21995f749f`  
		Last Modified: Wed, 06 Aug 2025 20:41:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23aa275492be7686e888bc2626738fc6f2ea82fbd6716a79678438953957b060`  
		Last Modified: Wed, 06 Aug 2025 20:48:27 GMT  
		Size: 5.5 MB (5469369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15879798bb9ad43fda07af509987d59287b51abe929325b45fe1c25a46e6f7c`  
		Last Modified: Wed, 06 Aug 2025 20:48:27 GMT  
		Size: 1.7 MB (1724265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3319d7a2fb186680b34a66ffbefaeb9bf75a785a8addba2d7fa3686ef0cc81fd`  
		Last Modified: Wed, 06 Aug 2025 20:48:26 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:4dcbaad88af88caba4216434da540f6a400786ebae53f7d6b404176e4fe4822a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 KB (315598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a843465d756ff4d93ce7884a3c45e6868c2227c473d8f22eb27b7a95f0107ba`

```dockerfile
```

-	Layers:
	-	`sha256:b3d7eb3e5f2e839f0ab2aba8ff99db12e4b02ea1097560d05a70888c9503395b`  
		Last Modified: Wed, 06 Aug 2025 21:52:46 GMT  
		Size: 295.4 KB (295362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e6345abb811c1f7aa26edd94f2e057ef0224bd7257aa77a95dc1ff395f51788`  
		Last Modified: Wed, 06 Aug 2025 21:52:47 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:54c8ad52341c7270fd7538e15194ee0dd2548aa5676c5b234b5d260c685eb73b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87338674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7b4cfb23a6d26b8ae63d5d861384976f64a51e0e93d1fbf381620c2f652a56`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.6
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOTOOLCHAIN=local
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOPATH=/go
# Sat, 19 Apr 2025 03:51:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Apr 2025 03:51:58 GMT
COPY /target/ / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /go
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_VERSION=v0.4.4
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SETCAP=1
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df80bb7562bd7e03fda0615c89df2976c21bcf7fd34bd1bfa24010374df289e7`  
		Last Modified: Mon, 28 Jul 2025 20:57:12 GMT  
		Size: 284.7 KB (284686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cff5f7a05b34c948079a4919c482f7dda90ac2f202c127ff11fd07e3182b32b`  
		Last Modified: Wed, 06 Aug 2025 20:25:24 GMT  
		Size: 75.2 MB (75246881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf63e98a50f73bdd8c62c11e276b7a902f36b07f207ba11a24d02b0f2daef988`  
		Last Modified: Wed, 06 Aug 2025 20:26:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987eef1a0e53faabbaa0dd92ccd8a4b096a46c9e07bfa1d1c54ab88b877ea7e`  
		Last Modified: Wed, 06 Aug 2025 21:48:01 GMT  
		Size: 6.1 MB (6118143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff643bf086c83ffd8c70f39ecf7c31c10abe82aa7913a7ace3c90e81922e01f`  
		Last Modified: Wed, 06 Aug 2025 21:47:58 GMT  
		Size: 1.7 MB (1701436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a979ab37d747a5db254233930fea001fd6d555162cca3e0aceb73d2a7915081`  
		Last Modified: Wed, 06 Aug 2025 21:47:57 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:8a653f33a11c87a35342c72f67a841595a65c0093e946d16330d2be0985aa74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 KB (312726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57547ab89d6d9295a3b49b511858825c1e489f4acf4621d028dd350c9a1ab6b`

```dockerfile
```

-	Layers:
	-	`sha256:af133bf96480b68e28dc29dc46a793241a3dfa9edd8364ad9cffc55a02134431`  
		Last Modified: Thu, 07 Aug 2025 00:52:39 GMT  
		Size: 292.4 KB (292444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c8ecb7700e72f38ec1a14d327b65bc1fcb1739dc5a57d56ccf9bf6642a31d73`  
		Last Modified: Thu, 07 Aug 2025 00:52:39 GMT  
		Size: 20.3 KB (20282 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:7225525efaf0ba4a7e7243b99a3e373ce2f4d646221645d0f1c7fb6861755524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87508879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63ae9c1574d1f7bcf8bc92ea08841be9bfefdd265576cb283654605013e1c00`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.6
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOTOOLCHAIN=local
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOPATH=/go
# Sat, 19 Apr 2025 03:51:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Apr 2025 03:51:58 GMT
COPY /target/ / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /go
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_VERSION=v0.4.4
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SETCAP=1
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4292e2d4d9d8706c1de48009e1d142646f4d2a8bd05fff7fc3f70c75ef02d1c0`  
		Last Modified: Tue, 15 Jul 2025 22:37:55 GMT  
		Size: 285.1 KB (285061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2f1d32945bbdba46316d812cc8a114f3cbd007e7d0738c103633bf98c8f35f`  
		Last Modified: Wed, 06 Aug 2025 20:27:31 GMT  
		Size: 75.6 MB (75560619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7725b30b21489a51aab04d3fb3b12b8dca56f7882ccf2388d8c4f749dbf78fcc`  
		Last Modified: Wed, 06 Aug 2025 20:29:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974c33f2210447a373a6b3260821c6f0618d51dc0d55edb2642cfe84611c4a1f`  
		Last Modified: Wed, 06 Aug 2025 21:18:28 GMT  
		Size: 6.4 MB (6397892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2170b701f739114006aa72fb742beb36da7cd34fb9bf79bb992371c062e97d77`  
		Last Modified: Wed, 06 Aug 2025 21:18:27 GMT  
		Size: 1.7 MB (1695590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6274a8cd1f084f8622d300e55fe0988622031e86d6e2ca863608b9c62869bbc`  
		Last Modified: Wed, 06 Aug 2025 21:18:26 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0e6c1c6b152aaa360a971fe086d1fa6397e8f4a23ceec9c21f6b431bb7f281ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 KB (310668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060b210058c07a3974079cd26ded034268dba954455603771333e1801b1aa588`

```dockerfile
```

-	Layers:
	-	`sha256:d01bf57906aa0af73b64ec28f698808ef9e710a4447ae1bd4488e185ded54150`  
		Last Modified: Thu, 07 Aug 2025 00:52:43 GMT  
		Size: 290.5 KB (290483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd857addc6028c5266e9a3a9e8c4458abdbae6d8200f63da592986ce193b6f3`  
		Last Modified: Thu, 07 Aug 2025 00:52:44 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:fb87571ab0cfe463d5b70a18f7fc659670b5c55747db3031ea04cb59192007d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87901339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc43b273027a52c8474444595317de4089d1356a37708213bb7d600ddde35e7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.6
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOTOOLCHAIN=local
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOPATH=/go
# Sat, 19 Apr 2025 03:51:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Apr 2025 03:51:58 GMT
COPY /target/ / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /go
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_VERSION=v0.4.4
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SETCAP=1
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0630095d87a868716a00796c50906a7361ad7a790e9e9151e3bb310f8846f6`  
		Last Modified: Thu, 17 Jul 2025 15:36:08 GMT  
		Size: 282.8 KB (282751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc03fbadbe664ad3d80e3509b96250ae628b3c572ce60e514d1ab20170b9d16f`  
		Last Modified: Wed, 06 Aug 2025 20:35:39 GMT  
		Size: 76.3 MB (76329537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3100604e2ac3ab2afb5cfbb5b614bf8a221677bd8062fec6e7c8d427bd3a227`  
		Last Modified: Wed, 06 Aug 2025 20:38:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7fcb5eb3236cdaf4c847395cb3593f761279c79096d30f3e7cf35380880458`  
		Last Modified: Wed, 06 Aug 2025 21:55:35 GMT  
		Size: 6.2 MB (6227728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ffbcd6b9606b2af427eeec605dcacf7cd7d3373be452b10e2bb22f249781e`  
		Last Modified: Wed, 06 Aug 2025 21:55:35 GMT  
		Size: 1.7 MB (1711639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cfb2de1c2d535f5db75d479624e79d3c03d09237fa02bfe0e3cdaca96319d6`  
		Last Modified: Wed, 06 Aug 2025 21:55:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e726fabc45a470f841e6101b22886180e210ce12d35e7294ff41bda3d5fca48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 KB (310664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b2a779549901a2e89720d3b51ed603f8cad90098f71519ddbb0679b33cb68`

```dockerfile
```

-	Layers:
	-	`sha256:ccc7ede165f095820a25ffb389a248d0b37c8e904fc5ab03cd1183fef473c6fd`  
		Last Modified: Thu, 07 Aug 2025 00:52:47 GMT  
		Size: 290.5 KB (290479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83f30acaaa6bd313ee7a3e5ee0cf46680343b632c7fc49a20989d0b539919b4f`  
		Last Modified: Thu, 07 Aug 2025 00:52:48 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:496a35efaddfd70bd8fc3a6c6c7604dc59e48cf7fe52c12cbae6d522aae7d722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89686251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab84ab64238bb037bc47fd85911f6a9456751a34a1e46d4c7c1e4ee7f580d2dd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.6
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOTOOLCHAIN=local
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOPATH=/go
# Sat, 19 Apr 2025 03:51:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Apr 2025 03:51:58 GMT
COPY /target/ / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /go
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_VERSION=v0.4.4
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SETCAP=1
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7c2184ed1d560f97be7198cd6f9baa12de8a0aff6bbb89596217c942ed2797`  
		Last Modified: Tue, 15 Jul 2025 22:45:47 GMT  
		Size: 283.4 KB (283425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e1a381c28a9856dd0ac521492a147ded6dad1df91bf78b9e3837491a808ff6`  
		Last Modified: Wed, 06 Aug 2025 20:27:31 GMT  
		Size: 77.8 MB (77803457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2779e3046c0431297763bbabe36216fd15556e7016bcc78ace7dbf1db77e0f`  
		Last Modified: Wed, 06 Aug 2025 20:29:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e4bf0eb55c7430dfd339bec4f2cf93f11492b07ed6a25b46242cadeb66e3f`  
		Last Modified: Wed, 06 Aug 2025 21:16:45 GMT  
		Size: 6.4 MB (6365270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cbd88bb54e64783a4e09a6f24f06c38cd43e3417c9245ddc6254bb7cad8944`  
		Last Modified: Wed, 06 Aug 2025 21:16:44 GMT  
		Size: 1.8 MB (1771408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c5f2672e2899c45cadf58ca45febe54fecfd64618dea09a3f796654c55ff47`  
		Last Modified: Wed, 06 Aug 2025 21:16:42 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:b43e1d7b99179d1686740dbd4935cc4ed2c9324aebc6f828ad470d4da4f72b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 KB (310504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f996428b5dbcd2c4ab02d70488411b4b8af1e63eaa04886e8a7b064651413e6f`

```dockerfile
```

-	Layers:
	-	`sha256:71c56c3a1efa119e463da9736e08ce282ad47675593540c2df83cc15582c6118`  
		Last Modified: Thu, 07 Aug 2025 00:52:51 GMT  
		Size: 290.4 KB (290389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e61bb1dd67e99e52e77cf1b51b76c5fd38bf37988a5aa7c95878046ae57ef127`  
		Last Modified: Thu, 07 Aug 2025 00:52:52 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:9edca605c07c8b5425d1985b4d4a1796329b11c3eba0b55f938e01916dcd96c8
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
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:5b34b43839bf2fefd2991f592fb74e60f8457eba01e4f379e8520bc8da42e4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90826590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30da546f540254a60a740c0d52fc47e7793156a481a8c1fa038c788e443a977e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.3
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcde94e77dfab30cceb8ba9b43d3c7ac5efb03bcd79b63cf02b60a0c23261582`  
		Last Modified: Thu, 08 May 2025 17:04:36 GMT  
		Size: 294.9 KB (294911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b00dc8dfbaa6cd7e39d09d4f1c726259b4d9a29c697192955da032f472d642`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 79.0 MB (78981573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b664c7c39c20f5e319a449219b9641bd2fdf7325727a3f69abe1e81bf0f726a`  
		Last Modified: Thu, 08 May 2025 17:04:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d5d728b3bd2939934fa62f169ecfc75184175e3bb15ecf8fffa9fbed1ff395`  
		Last Modified: Thu, 08 May 2025 17:11:35 GMT  
		Size: 6.1 MB (6072235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec286df111089e00a53c7b5c313ebf6f070b0ec18660117d2a9908d4495b6af`  
		Last Modified: Thu, 08 May 2025 17:11:35 GMT  
		Size: 1.8 MB (1835034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccb79cc4fabc1207a298e5e9bb6236331056764a33cffd456303244fc3fcf73`  
		Last Modified: Thu, 08 May 2025 17:11:36 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3ca2a74a4e9d3c62715c4ea3a96b02fd5d65d3381556a9f00ceb27748c0da6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 KB (313718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35c574c451ed26e50ed203b6f0a08f49e5a12ad28847735c24bf8e34ad3cfb0`

```dockerfile
```

-	Layers:
	-	`sha256:fae090ab08d1a25e48eeb9bb52e297e67276a5fd841bec97f9f310de3c5a1404`  
		Last Modified: Tue, 06 May 2025 20:07:53 GMT  
		Size: 293.6 KB (293603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e112c595b8b6aaa3c6b655a81e88b6a5768cfa2fbf20074c1a06ee4e757674`  
		Last Modified: Tue, 06 May 2025 20:07:53 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:c6e0ee9ce74b9ecf0df06549499a7928635a80722c793b8f252a4e3f05422356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88530665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb244786136b64a182c10e6b24c438f1b59050586c0fdbdf78c8305099c5933`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.3
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:39:12 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e897536fb13ccfca87cac1110a2b716225d73570f890064e1f163d9b5875cd3a`  
		Last Modified: Thu, 08 May 2025 18:18:07 GMT  
		Size: 77.1 MB (77144504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e205dd8a233395163fb7278cb76d5a78a5e21fd5108812f8a6abaaa1d2c0eb5`  
		Last Modified: Thu, 08 May 2025 18:17:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fe15c933d4b5f3e3ea539f7476117e9dc315c0dca4b04e9e915e32a8fde138`  
		Last Modified: Thu, 08 May 2025 18:17:59 GMT  
		Size: 6.0 MB (5994294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93cda4facf1554a7c7324b6dd5046d403992e0875f51cea089c351460a9048f`  
		Last Modified: Thu, 08 May 2025 18:17:59 GMT  
		Size: 1.7 MB (1730291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d386443b0e1c35e51e20dbe920127ea4acd792048154126ce848d65418324f`  
		Last Modified: Thu, 08 May 2025 18:17:58 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3b9851f28720b5386c271120d301e238d1830570d41a35a13071de2a0ec3adda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73f4dae2d5f40eb981ac5e2e9bf7f8c6ef70e7a24821ba09b22fa55f213192b`

```dockerfile
```

-	Layers:
	-	`sha256:0e23fd1530c53ab0b8a72d9fbe8d9b3c56bb77678cf21a11745e633458a507e6`  
		Last Modified: Tue, 06 May 2025 20:32:30 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:c4fdef7e70b582a7d5aba19ce1571f45cba70e80802a5cfd64bbeb03b66cd9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87732189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95ef9e02e17529c6943857bda3be01ca6f18e7c7c6c9c6a4aa2a25085f0e96b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.3
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77833ee7d3adeaa883db3f960686c769232a931d3442cfcc8bb6a4790098520`  
		Last Modified: Fri, 14 Feb 2025 23:49:34 GMT  
		Size: 295.2 KB (295199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f32012e82345c04270d988b1e520857596a775a43ec4b22744ab73bea39d15b`  
		Last Modified: Thu, 08 May 2025 17:05:42 GMT  
		Size: 77.1 MB (77144440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c23a49fcd1db2181cfd2a2ea5f43879dc7c393ddaf883fdbeca06dced4512fb`  
		Last Modified: Thu, 08 May 2025 17:14:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1e7f90cd423ece67bd30e8f8457c57753287f3cd8455ff0559d6094a2200c8`  
		Last Modified: Thu, 08 May 2025 18:18:05 GMT  
		Size: 5.5 MB (5469572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92d1c12f5164eb530ae85e5855a8163383869f43f117a4f568ff5c526119d96`  
		Last Modified: Thu, 08 May 2025 18:18:04 GMT  
		Size: 1.7 MB (1724265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40a17d6e5c7131d0a40b87d3ecb46e5bf14e4b012f989c52538e2825dc6dec5`  
		Last Modified: Thu, 08 May 2025 18:18:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:e09e235d6575e9790a57c6b7e4e3487b1fca40cacef070153a6b4a11aef07c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.7 KB (316684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83bcafcd181ad187caa1d194e542d80cf76b0908617ba5f935ef07b37d719074`

```dockerfile
```

-	Layers:
	-	`sha256:3434b9f05b64d3524d3a3e83fc60c0d05fcc3c7afa72af0cc62c08916a5349eb`  
		Last Modified: Tue, 06 May 2025 20:19:29 GMT  
		Size: 296.4 KB (296448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6caf191e01b5b4ff72eb495b94a73382d7ff6d0d7527929f4ba47658fe710ea`  
		Last Modified: Tue, 06 May 2025 20:19:29 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:71656f6ff8d4537604894e8f97151887246bbd1c74f9b0a332e06afcd4d53f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87341827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d538f19eb4b00dbc08e1f2ad2291ebbc131cc5a81094a75fcdd905bd82551c1a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.3
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2f34450ab6893f9de21e818c13da20ab31676614598eac0352797a074049df`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 297.9 KB (297874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae64884db43f30f8dbc9ec3362124d99c8bad23b957254ac52fb30413bd14a7`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 75.2 MB (75230554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdee32b0d6cb9863bfa2b0996b359506fd0a938301ae9bfdef13cb97a59b1e8`  
		Last Modified: Thu, 08 May 2025 17:04:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e22137a3f38ca622d6267ce2e9b89af69fa1a79374adb9f0c29e4494757bb6`  
		Last Modified: Thu, 08 May 2025 17:16:10 GMT  
		Size: 6.1 MB (6118344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32090eecb21ab788d303fc0d075bd6c1c482f3fc0ccdabf1bf330d1427561999`  
		Last Modified: Thu, 08 May 2025 17:16:09 GMT  
		Size: 1.7 MB (1701435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833a87979c7d526727a997810835991ce837b51122422083faf21558ad0f9fc0`  
		Last Modified: Thu, 08 May 2025 17:16:10 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:8431ede88c50d3961bbee063e0c0eda3241e94d4f8f644487256e27f8c326caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 KB (313989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a632bc75664b6893989d39a020d69a2f7b51a3d24781eef4ab3bebbce0c451`

```dockerfile
```

-	Layers:
	-	`sha256:93faa8f911c37ec92af3848841f8e5a0cda95d0b18c4f7eac7c5ddeb64adf455`  
		Last Modified: Tue, 06 May 2025 20:21:22 GMT  
		Size: 293.7 KB (293707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f0142aa8d984cf4539fff2c3d58a80cdcbe233135c7fd394d31b22979f2718a`  
		Last Modified: Tue, 06 May 2025 20:21:22 GMT  
		Size: 20.3 KB (20282 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:80a3aca400c14e5d92366cb03212f5c1eadf80c65a540cd6785a0811132b64f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87511256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94037e8da20d87d5f1f494141aa3f42fd8cdc6591d347583c9bc54456641e6d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.3
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d07c13e49694099e3952065321ca0fc45938d3a118b16ce109a83e147045f6`  
		Last Modified: Thu, 08 May 2025 18:21:43 GMT  
		Size: 298.3 KB (298290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f44821f8171df650a338e8fdd3b017af075382eee8cc2d34256864c2264897`  
		Last Modified: Thu, 08 May 2025 17:13:17 GMT  
		Size: 75.5 MB (75544493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36d8fe8d7595d2f87f7dde8e6a7f6b715f24f9b8112a6fa773367fb24c573ad`  
		Last Modified: Thu, 08 May 2025 18:21:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b225310d36db0f9444593597b462929399d348352822f193716ebaad9900f5`  
		Last Modified: Tue, 06 May 2025 20:17:44 GMT  
		Size: 6.4 MB (6397947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ccd23280ce9aaddcaa14ad3fecae2514212b0169f34220c75cfb58cdd151f0`  
		Last Modified: Tue, 06 May 2025 20:17:44 GMT  
		Size: 1.7 MB (1695589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4250f17bb780ca7700f6d310e7b0882352efdedc12bf55de668ec0976ec5ce0c`  
		Last Modified: Tue, 06 May 2025 20:17:44 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:fae282756aa52e2d858bae023a6a634f1eaf65a9ff88aad451d7cd3afea5ad86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 KB (311931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe39406bd23b128474e9e17e1786e2977e091761d768508f8f8a5920ee9c56a`

```dockerfile
```

-	Layers:
	-	`sha256:2b6c80936b539eb135b15be9b618066cd0c6840e3d3d718708ae3e55c908a90f`  
		Last Modified: Tue, 06 May 2025 20:17:44 GMT  
		Size: 291.7 KB (291746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62e1351ed1922a227aa97f787071cc22463220131fcce331353b438487893796`  
		Last Modified: Tue, 06 May 2025 20:17:43 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; riscv64

```console
$ docker pull caddy@sha256:ede955e16139533bf9517819ff53c117076ff3353a30900ebc4a0d880974f549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87900824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccd6515774fdb40e5273b3d53b738794665fb05e4b0fc72ba388f20962056df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.3
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd81befb40433dc7da0b53543acafce5d4aa75d9a2bc5815536bad6b9db1682b`  
		Last Modified: Sun, 16 Feb 2025 09:31:14 GMT  
		Size: 295.3 KB (295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4ce4a757d65543eb38e825fd00a5434bd6efef264c5b31052eab1a8e5fa09b`  
		Last Modified: Thu, 08 May 2025 17:12:53 GMT  
		Size: 76.3 MB (76313875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555e229a2d28126c4330a6abe25a2a95ad318d2cecd47079fa9c53484f9e6608`  
		Last Modified: Thu, 08 May 2025 17:12:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b088a122007abdc368abdfbd9cb59024f82e0a3e2ffffb7696a36c5afef8e9b`  
		Last Modified: Tue, 06 May 2025 21:23:14 GMT  
		Size: 6.2 MB (6227930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0323297cedc266dc1ffc039b9143b38cf29948d1072dc94ad48cea69b8c1b086`  
		Last Modified: Tue, 06 May 2025 21:23:14 GMT  
		Size: 1.7 MB (1711642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17548175a2a307cedde59681e34156f1b51fa828a1d26cdc86ec161e55d51fe2`  
		Last Modified: Tue, 06 May 2025 21:23:13 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:f6b7e8c0ab55e5b9e44bed64e6ccb281549d55510b67445b142099245b541b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 KB (311927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b831cc800a6bfea7404c54feb23fdb16fe70f1c0a1e522a71ad6e7741480702b`

```dockerfile
```

-	Layers:
	-	`sha256:891c9bbab47c825fb5386f62d4b4cb5ef6bd07ca11ed96b610f0c4fb373d20c2`  
		Last Modified: Tue, 06 May 2025 21:23:13 GMT  
		Size: 291.7 KB (291742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:587260bdf720f0e74a282f799627e4da02ef552f0a209b4bcab7ff43e6aedcba`  
		Last Modified: Tue, 06 May 2025 21:23:13 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:f7002ca7537c752f6abc667a51062ec0a96108b8449025ce2fa14594bb1d0baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89689215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaa1c65099e3920eab25b6d0060f54d0a785bb46926088bc5c850be074519ea`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.3
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd99af01c56b56dd8b4b638222a30d969ae806a266626016d5a030517f57428`  
		Last Modified: Thu, 08 May 2025 18:21:45 GMT  
		Size: 296.2 KB (296192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553e83890111f2cfa590a0023450ca3f44d60d123d688835ec1c4ba557b336f8`  
		Last Modified: Thu, 08 May 2025 18:02:40 GMT  
		Size: 77.8 MB (77787898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad9a5b0e376da7a0d7f9683b35cbd8e9729795bbc267d366b0e055a6f39e539`  
		Last Modified: Thu, 08 May 2025 18:21:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d850f8661517b8a9f5b8f1541531aaa3e647bd024b63b8ed9f6e878e09616a`  
		Last Modified: Tue, 06 May 2025 20:17:51 GMT  
		Size: 6.4 MB (6365560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a703b896c4ecc97e6367f67d4a711da3b02a0a6828fcde549729d64645575472`  
		Last Modified: Tue, 06 May 2025 20:17:50 GMT  
		Size: 1.8 MB (1771406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f10770fd8e5f7a730b5853591aca18bc28e62855096ab5e064caeb5c858871`  
		Last Modified: Fri, 09 May 2025 11:56:45 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:44444b5765575e3a7910548a4d68bf8e39e0af967c16c1d9a1cdfc04c890db5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 KB (311767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429e781bbc870b04b05c820d21b684d06972d53b56003dc1d6b416bbc69fd35a`

```dockerfile
```

-	Layers:
	-	`sha256:bd9c0347ab986d7e8d836a1765b11b22d1e0854c5e17cab1e759ac95a0986c5d`  
		Last Modified: Tue, 06 May 2025 20:17:50 GMT  
		Size: 291.7 KB (291652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f570d9fb1426348020a7e70d70894bc02c277f15a4598ed760b55f0e946777f`  
		Last Modified: Tue, 06 May 2025 20:17:50 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.20348.3692; amd64

```console
$ docker pull caddy@sha256:6d7b02ba210ee90c738c9c27d3985d484cfc57ee6974fdcfb6ee0243a4f8df31
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2404849429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0892e85f8ffd386f0300eb4746d89eee36c5d32d384e7bfd12783e1e2ef6cc72`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 20:58:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:58:59 GMT
ENV GIT_VERSION=2.48.1
# Wed, 14 May 2025 20:58:59 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 14 May 2025 20:59:00 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 14 May 2025 20:59:01 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 14 May 2025 20:59:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 May 2025 20:59:20 GMT
ENV GOPATH=C:\go
# Wed, 14 May 2025 20:59:25 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 May 2025 20:59:26 GMT
ENV GOLANG_VERSION=1.23.9
# Wed, 14 May 2025 21:00:35 GMT
RUN $url = 'https://dl.google.com/go/go1.23.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16409aa244b672de037389e9e39115cbf82633e5fa0d4db6ec1a9191ca00a1e1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 May 2025 21:00:36 GMT
WORKDIR C:\go
# Wed, 14 May 2025 21:16:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:16:21 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 14 May 2025 21:16:22 GMT
ENV CADDY_VERSION=v2.10.0
# Wed, 14 May 2025 21:16:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 May 2025 21:16:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 May 2025 21:16:35 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7851e376914407ee44b63283f59444316a659b2495eb72b046adf9c0f0cdfb`  
		Last Modified: Wed, 14 May 2025 21:00:44 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b1d0d25fa005ea190c43328cad3bdc7cd9cc2badf7295acfe710ce469df640`  
		Last Modified: Wed, 14 May 2025 21:00:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8c9abc90534c50799f85d9d34c87ca357cb1958d72a1e3f48ac20190b4c9f1`  
		Last Modified: Wed, 14 May 2025 21:00:42 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a189048c383ded714ac76135ae5679d809d8f177078e99bd6e15b9224d207d95`  
		Last Modified: Wed, 14 May 2025 21:00:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03047ba58131093de5c276d438ec5d13ac1ea43b6a4cd8aa0d4eb115ba37a932`  
		Last Modified: Wed, 14 May 2025 21:00:42 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc7ad0e5bfd3223f380b62113bbf1c1cd263358e1453d8119e75650809d29ea`  
		Last Modified: Wed, 14 May 2025 21:00:48 GMT  
		Size: 51.2 MB (51193109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e825425710a46fad26e66fc36ade4049046a593719d652bcbf2f24c57b7651a5`  
		Last Modified: Wed, 14 May 2025 21:00:40 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff6dc97f8f0c2f19b5852611f113de7342481c12956850511e9251fd12a8137`  
		Last Modified: Wed, 14 May 2025 21:00:40 GMT  
		Size: 335.3 KB (335301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882982efdecb446d3e3504e65eab58f03bed158e58f6a54ec2bb4e58b4814ae8`  
		Last Modified: Wed, 14 May 2025 21:00:40 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f51e03191c3b665fad2b78b24275caeadf41fcef79dafd7053517561ba4691`  
		Last Modified: Wed, 14 May 2025 21:00:52 GMT  
		Size: 77.4 MB (77370762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed72f2005cd738e72950eeaf7d1f9b3d5229a74fc3d88c4e05871f49a3f13c1`  
		Last Modified: Wed, 14 May 2025 21:00:40 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd34b450308b8f43d45f48b6536e70ac79bea43923dd59174f45178146da0876`  
		Last Modified: Wed, 14 May 2025 21:16:40 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c988bfce29c80e434fa2955797774a4467da9c24199ba21c932b0914b5a522e6`  
		Last Modified: Wed, 14 May 2025 21:16:38 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2b7d75369321e9e5ef4ff8b794109692ca1c10406abfc6be77606a2e83bbab`  
		Last Modified: Wed, 14 May 2025 21:16:38 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbaaa8823edd92e5c61b44e1217c3810113526e25a9bc5932a0ebea1e38082b`  
		Last Modified: Wed, 14 May 2025 21:16:38 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676b8e595d575273114b230b80515ee722eec0dac2cd5a3b3f1ef1fed99666e8`  
		Last Modified: Wed, 14 May 2025 21:16:39 GMT  
		Size: 2.3 MB (2305327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd65fe9967d5bbb64c54caecb4c927e3367abb5f14da03339931c9a837544cc5`  
		Last Modified: Wed, 14 May 2025 21:16:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.7314; amd64

```console
$ docker pull caddy@sha256:3d0db1094683206363d5436a2951fe0cfdca08795cb0cc3872e27062586e2971
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2314957245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c36f75d6bd73f1bd5660ab890ee20f16cf5ec2b8a2283c4a49c9a341440c52`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 20:54:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:54:27 GMT
ENV GIT_VERSION=2.48.1
# Wed, 14 May 2025 20:54:28 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 14 May 2025 20:54:29 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 14 May 2025 20:54:29 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 14 May 2025 20:54:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 May 2025 20:54:59 GMT
ENV GOPATH=C:\go
# Wed, 14 May 2025 20:55:05 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 May 2025 20:55:06 GMT
ENV GOLANG_VERSION=1.23.9
# Wed, 14 May 2025 20:56:22 GMT
RUN $url = 'https://dl.google.com/go/go1.23.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16409aa244b672de037389e9e39115cbf82633e5fa0d4db6ec1a9191ca00a1e1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 May 2025 20:56:23 GMT
WORKDIR C:\go
# Wed, 14 May 2025 21:21:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:21:20 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 14 May 2025 21:21:21 GMT
ENV CADDY_VERSION=v2.10.0
# Wed, 14 May 2025 21:21:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 May 2025 21:22:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 May 2025 21:22:20 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de08ea7e82787f3361bdfade133d3031ec514db766529474efe8f6b9a384bfca`  
		Last Modified: Wed, 14 May 2025 20:56:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe2dddd87a71782dbffed753b969d91b5a1866e1ff8ff672f54e962e47a8541`  
		Last Modified: Wed, 14 May 2025 20:56:31 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50215270a9e8d0565e83595f435d8844749f6565375cfeb9f6aecc4401f6e72`  
		Last Modified: Wed, 14 May 2025 20:56:29 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2f3354badfc3a7f851e55d438544c7fb22e3de2bcb331cf28190397baa5273`  
		Last Modified: Wed, 14 May 2025 20:56:29 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e2db41d077e01ffbb6bfe2c07bdc37d21ff5cf45ba96cd8ea281120dd033e9`  
		Last Modified: Wed, 14 May 2025 20:56:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43ee064087770fe9cbc3ffdf657376ae4aab5c8e0bd95d02e113b95609490d0`  
		Last Modified: Wed, 14 May 2025 20:56:35 GMT  
		Size: 51.2 MB (51215645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69771965c3632c59d408856a922ce9f7301c2d8df6e5314d024cf144035c90`  
		Last Modified: Wed, 14 May 2025 20:56:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41dac0667fd8971ecb101ca49614bdea29208736c9af4f14eb79a8bff4c3f24`  
		Last Modified: Wed, 14 May 2025 20:56:27 GMT  
		Size: 344.6 KB (344561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730d07daf8573056c48a5e652fcfd60c53f771f20f402f0d4e326e15f3157820`  
		Last Modified: Wed, 14 May 2025 20:56:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b2aa4123f0a54fa264048550c3260de41885ee9b655ea96e94f24faa4049d9`  
		Last Modified: Wed, 14 May 2025 20:56:39 GMT  
		Size: 77.4 MB (77385829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c5f0f648229a5404bc3907417eb1dfe9213170c82c79ace81adce5514f1597`  
		Last Modified: Wed, 14 May 2025 20:56:27 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8bce85b12630f09e007f9035a3c4e1fd711d1e897ea60d78caeb2fcf498c19`  
		Last Modified: Wed, 14 May 2025 21:22:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d9a5e4508cc8e2b3dbb476832f30badd5c7fbeae1c3f98a4332a4fa63d1272`  
		Last Modified: Wed, 14 May 2025 21:22:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eef18d05ab85c52a123146f0c129ed52c8c64bcfab570b344b84c71973eeaf9`  
		Last Modified: Wed, 14 May 2025 21:22:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3439eb435a1d389603dbc3dc108e1b1063eb2f3fb12c898e9703d82b6686317`  
		Last Modified: Wed, 14 May 2025 21:22:22 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fccdeceac765e0d23dec5361bece97d8dcc167d29fa8d34bd8b1ad181a9738`  
		Last Modified: Wed, 14 May 2025 21:22:23 GMT  
		Size: 2.3 MB (2276688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df7a8b64a5cd5bd7a70f079dc75c94fbab4c593b2cb07bd64644dd6ec724bff`  
		Last Modified: Wed, 14 May 2025 21:22:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

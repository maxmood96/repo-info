## `caddy:builder`

```console
$ docker pull caddy@sha256:e5612b84a4a8c0d452da55d3d7d97985a5039ef3be6e399fd7264bb070f30559
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
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:1100f99b41d9c4a4447685119b2e79a66da97fad47e8bc573471e0f717f12d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90832710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7af8270da624c34c4e0a26e86b99e51a6fa6907bc006ab3245633d1a6d1ad3d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.5
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
	-	`sha256:0a2e1e6a4873176dc44a570a9fa1bd56817f6ca2f36c3b0011823ba81009f34f`  
		Last Modified: Tue, 08 Jul 2025 18:07:56 GMT  
		Size: 294.9 KB (294890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e4aa2eec44b6580a06950b078a57600d112e526d555d23cbf8ffe311ec7f6f`  
		Last Modified: Tue, 08 Jul 2025 18:07:43 GMT  
		Size: 79.0 MB (78987727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e917b61ac86009f60bbe1898649508cde89d15efc4663896ac503e1c121d2d5e`  
		Last Modified: Tue, 08 Jul 2025 18:07:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754083e970b302f471e215cbd33a146bba7db3f47f15623021609812866b6e5e`  
		Last Modified: Tue, 08 Jul 2025 21:54:26 GMT  
		Size: 6.1 MB (6072220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b0209c8d2c1d5a8fccd01f2d9f0033f60bdfd8fa1e6ad9a0ce62c57aea2ee4`  
		Last Modified: Tue, 08 Jul 2025 21:54:26 GMT  
		Size: 1.8 MB (1835035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490fd943ac3d7c7a71d5167c8f26d64dc2465d12b3e591f17f5d7d2e8da288c`  
		Last Modified: Tue, 08 Jul 2025 21:54:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:c3e2bfc95fb44bd7002bb11471b1c849507a4c98baaddd9bb48b169c3b6fc0fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.0 KB (316997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813f04384de9e6bceac990485be98597ec22ae34b27f63678c94eb39a5101d9c`

```dockerfile
```

-	Layers:
	-	`sha256:595eeb979682cadab95e898b979137c36c88065f2b8aed964b332f4433ce59de`  
		Last Modified: Tue, 08 Jul 2025 21:52:53 GMT  
		Size: 296.9 KB (296882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27819e5ff9e16c57f6bc5aba8e68dd2bde62769bd0622cc22418fec381b6a816`  
		Last Modified: Tue, 08 Jul 2025 21:52:53 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:8e4992c9424febc643de8402b58fc98327ffdab20d787eac5cfdada5cfd58a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88534379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216db0382f2d14787ad0e1bc1a475823f04311189801a6283b4c975a9858de44`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.5
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
	-	`sha256:186b5813a05b4bb364e8003d5502e6ea1d97824bb24da93e87754a56748e4ee8`  
		Last Modified: Tue, 08 Jul 2025 20:24:18 GMT  
		Size: 77.1 MB (77148189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bea85afa2d5b58caf8f1894a707d48e365a9e39e3f0f3a0b204005eb623051b`  
		Last Modified: Tue, 08 Jul 2025 20:24:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d898c9ad21700da9fa2ea334eb98472cff7da11dba83e4a84884401a355bc084`  
		Last Modified: Tue, 08 Jul 2025 21:53:29 GMT  
		Size: 6.0 MB (5994324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8269f9c107c09ad496e52d01a3f4a061b245c7248fbdd534fff191ba082103`  
		Last Modified: Tue, 08 Jul 2025 21:53:28 GMT  
		Size: 1.7 MB (1730291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f741d95e138ac2832d5f402558f5aa2a3a1c0dcf0a9e2c9917c64c131ba3a570`  
		Last Modified: Tue, 08 Jul 2025 21:53:28 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:10aa1e287386d980e773093f78aa41674bb27b812804a5c70e84f9dc445101a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cae33a29ada24f4655d29f38c030c053519172375ec23a7b10436d0718393cd`

```dockerfile
```

-	Layers:
	-	`sha256:e8b1fd315f20b9f8041cfbb2fcdb24e4062c5b97dbb575ce80245ee9c91d1675`  
		Last Modified: Tue, 08 Jul 2025 21:52:57 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:9f53ea34afabc321255978dd6bd4852712ff3b0b0dbd58d681dc14d8365b7f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87735943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2b830771493e98e115e6bba8412cd016ad01d04cc41a1bc5bce5cdbd927c39`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.5
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
	-	`sha256:aeef88bc4f2274b5ba3079f27071c582942a7743e24b45296709956725ae01e5`  
		Last Modified: Tue, 08 Jul 2025 20:28:35 GMT  
		Size: 77.1 MB (77148190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c338e82f14f47a0f6e39faaa3560cc602b681ccb786db1c1ca2968debc4631a`  
		Last Modified: Tue, 08 Jul 2025 20:51:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a7d8755a9281e3d05626e9c954cc4f5faf4a91a1d8f765dc413a7b18b6e1b9`  
		Last Modified: Wed, 09 Jul 2025 01:02:30 GMT  
		Size: 5.5 MB (5469570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19b8b7d6215182e211c7fa17f3c349b02644b16623569f68b0ed8d21b65b983`  
		Last Modified: Wed, 09 Jul 2025 01:02:32 GMT  
		Size: 1.7 MB (1724271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d873c1d024a096d9cf22e856967d7a6205a2727678f08af3f170979d18535a2`  
		Last Modified: Wed, 09 Jul 2025 01:02:33 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:da2159e8fec9454b2214fd4a3ca6beb1753823bd303af1087fa820325490a0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.1 KB (320140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466bf257968e15199d2b56423fd3153b928df4cd9ea01a923bbd8381e400b256`

```dockerfile
```

-	Layers:
	-	`sha256:e6a1ff4df191c10c53e24e5456656611bfd7a50eadb86dd965a278c41f9df1a4`  
		Last Modified: Tue, 08 Jul 2025 21:53:00 GMT  
		Size: 299.9 KB (299904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b02049e6e0a9845afcd7aaeb88da1f2b51c9183c3d53493a432e3546ed20a8ee`  
		Last Modified: Tue, 08 Jul 2025 21:53:00 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:f763cd5f8407b711f342274fd4219f3f56280da6bae61c425772ba60ae691fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87345056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda8edfe3d99587a46314f823339396d7dcd343ec3e993ae58dc0b58bc342a94`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.5
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
	-	`sha256:b5b262260544cb39400e5dbb7647c5bec51158ea8b9b102d3b166fd952b3e386`  
		Last Modified: Tue, 08 Jul 2025 04:48:54 GMT  
		Size: 297.9 KB (297869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c935bad878b3741f10814aeb149f0e6cee7191c12a56261426a2bc9b1ef4a025`  
		Last Modified: Tue, 08 Jul 2025 19:18:42 GMT  
		Size: 75.2 MB (75233805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b474e5e3cbc34b3495cfb0e572f9a7e261cd136bac52898ab06cf0e5091be9b6`  
		Last Modified: Tue, 08 Jul 2025 20:25:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467d528fd81e1802747da14d1e1ad3b9bf326c0baeaa35cd823186e4c47d66e6`  
		Last Modified: Tue, 08 Jul 2025 21:57:12 GMT  
		Size: 6.1 MB (6118333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffd49652668b277246d1d1e09af7b7523e617a302ba3920249c6198d0d47668`  
		Last Modified: Tue, 08 Jul 2025 21:57:11 GMT  
		Size: 1.7 MB (1701430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42d54447bc3e44aab387b804179bd7ebe897b1c395d5edb90dc466fa7900bb7`  
		Last Modified: Tue, 08 Jul 2025 21:57:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:78e83d047d79b09d4e3bafd447b8f7f9558f16c3600a3d7f0865627ffa7d14a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 KB (317268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9ee099cecfbadd78a49f27b349d23769dc1f090d54ad2549d18260e19872ce`

```dockerfile
```

-	Layers:
	-	`sha256:bd7c66d27b5dd8e83cfb2ff3356687443c129dc7719b9e3aa8dff8ebe64fd956`  
		Last Modified: Tue, 08 Jul 2025 21:53:04 GMT  
		Size: 297.0 KB (296986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a43ed323670ccd40c89ff4657a3aa8d09a7f0e6bc0a6a4eb078c2a3370af20a7`  
		Last Modified: Tue, 08 Jul 2025 21:53:04 GMT  
		Size: 20.3 KB (20282 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:e6d5ec3224d91f99910bc74c2f591085f7745a3cc17fe83d2dcd82ef03264c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87512869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781e404ae49cab5877ad0d7dbc2ccdbe3b7a6b407868e04bde5cbec5c114e1c1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.5
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
	-	`sha256:70c63a5fe94812205aea92afffb34bfadb77e3c0f3a3740a18e9d23511a8ba7c`  
		Last Modified: Mon, 07 Jul 2025 22:29:09 GMT  
		Size: 298.3 KB (298294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6f6a1b062efccc0ac067d38bc08579d8743c17e9fb0836c0c72218b134b071`  
		Last Modified: Tue, 08 Jul 2025 20:32:19 GMT  
		Size: 75.5 MB (75546088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3120d7cc50e4a859fcd4cadd0674b1b3bd3f1f653bb9204e8c00a2768c402633`  
		Last Modified: Tue, 08 Jul 2025 20:52:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ecf30627dcc1c97cffd5c4c37747216e7140d3090482ef9663d46763d0816b`  
		Last Modified: Wed, 09 Jul 2025 01:02:55 GMT  
		Size: 6.4 MB (6397961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038197afb2eb721d8fe02d04071e85123a734120bc598e923ce5a9f7d3aa6bb3`  
		Last Modified: Wed, 09 Jul 2025 01:02:56 GMT  
		Size: 1.7 MB (1695591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4a38c8b0f258ec9f5f52af44d1c1242c3e6e23ca10e8b71a9441b5d56439e5`  
		Last Modified: Wed, 09 Jul 2025 01:02:58 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:5cd0cb6b6848e8ae38e383bbd7303dd2c9dce95bbf7261e79c12aa58462dd7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 KB (315210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75f8666b4fdc550fadf0f294a48e917674b8bfca9d1ca1dd3f107c0cd6ca21b`

```dockerfile
```

-	Layers:
	-	`sha256:69a4592b323b1700b8713b68989849cceb0d51467fdb28783fdb535bc24321c9`  
		Last Modified: Tue, 08 Jul 2025 21:53:08 GMT  
		Size: 295.0 KB (295025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33044bb4276f290162e09d363db70e9e13defcb3f799ca9faaf448d67e4b5566`  
		Last Modified: Tue, 08 Jul 2025 21:53:08 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; riscv64

```console
$ docker pull caddy@sha256:04091a35af6a1df83d3b0b6e287d550cf576e9aeb872b51fc40781833be32629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87907467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248a26ee3db8a04630a7f6002a08815ee84e33c0daf5c8e1ed58cb797bdb2648`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.5
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
	-	`sha256:52cd9ed6fac7568217f34218cd0e1fea9d2f462a88a11047ac17478fa9a20909`  
		Last Modified: Tue, 08 Jul 2025 20:38:27 GMT  
		Size: 76.3 MB (76320474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73b2902aed4354df0707eea61b9e00d0cb97b75fa9bb956d002c8b10dcadbb5`  
		Last Modified: Tue, 08 Jul 2025 20:52:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad842ad3fa9d1d5a64745b8788f55e777ddfc7ba8f6119468018db603c630725`  
		Last Modified: Wed, 09 Jul 2025 01:03:08 GMT  
		Size: 6.2 MB (6227976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b3c8102990c4b46d9d69121d68566c0869661c2cc2a3cf2a48343d798981ea`  
		Last Modified: Wed, 09 Jul 2025 01:03:10 GMT  
		Size: 1.7 MB (1711640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151dbedf6d21b506eeb616c05ca128aab0762e813829d0f3aea97d1f3b9cd6f4`  
		Last Modified: Wed, 09 Jul 2025 01:03:11 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a28080331bec75a6160324ed5ae6c87cf8b527d6596ce9b18fea9ffe7f79c769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 KB (315206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad904e1148cda10c3b977a0ab4acde15d57d8719d99e528ef87a661c97c3b2b`

```dockerfile
```

-	Layers:
	-	`sha256:6e021e76fc2d6ea177b04542cb458d90a7ddd40366abdcde572b4ad8b0aa3121`  
		Last Modified: Tue, 08 Jul 2025 21:53:12 GMT  
		Size: 295.0 KB (295021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ce2ebbc730b5fe2daf638b124fb6994d904d8ff8351f78b25ef460fa3ccf6f6`  
		Last Modified: Tue, 08 Jul 2025 21:53:12 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:6610a6887023b76d5459d84b23f5e244cdbfcaf45bc86929224fd6e348845fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89687910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026b7132728cc3b75f10f1782f18a60f9eb366bc63f5a1f988d7e5869b7eff13`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.5
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
	-	`sha256:7a414ab9dfbde1973f254ba5fbf45d0f21227d9d3460aa7790f894fe7cc3001c`  
		Last Modified: Mon, 07 Jul 2025 21:34:42 GMT  
		Size: 296.2 KB (296193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55eb74eff7f088d02f920366e1a995d4e9589bb0f02f8e2ecd32e17ad79d0277`  
		Last Modified: Tue, 08 Jul 2025 20:32:16 GMT  
		Size: 77.8 MB (77786603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b55398dd0e7db9524316ac05525e09496bd03839d65b04b4de547e90f35862`  
		Last Modified: Tue, 08 Jul 2025 20:52:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce758b129a784813319a6d25fd3779c9f41b058522b7af443c0ac29b093a1659`  
		Last Modified: Wed, 09 Jul 2025 01:03:22 GMT  
		Size: 6.4 MB (6365549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3444db10a67ebcf691d0a24b824aad291ff1d396e7aba67cff8116fbda5ae78f`  
		Last Modified: Wed, 09 Jul 2025 01:03:24 GMT  
		Size: 1.8 MB (1771406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d71aa96ef5d4df4bfe7cd9c3e4ee1a2a1b7c072f6e4616e82195eda6e1f15b`  
		Last Modified: Wed, 09 Jul 2025 01:03:25 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:d7b6d173833b35430d89dfe4960d1294e273dc637fc74ff1d5c60c826ddcd7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 KB (315046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277a34e6ab79fa61787219d41b4909947f1f73cb6edf5a779ef973af5070ec6d`

```dockerfile
```

-	Layers:
	-	`sha256:70362272b525ef5e14ced86c1eb1b161f25056fe2185ce0e5592598b3922ec34`  
		Last Modified: Tue, 08 Jul 2025 21:53:16 GMT  
		Size: 294.9 KB (294931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65832274f282b57ae85a13ed0e5cc466cbafe5a8e22c33f230b4407dd1465065`  
		Last Modified: Tue, 08 Jul 2025 21:53:16 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - windows version 10.0.26100.4652; amd64

```console
$ docker pull caddy@sha256:e08615b53b204b2c9b3855605053827eb1468c7a96565fa0d66eb784458e3663
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3622655059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78acfea1090af90a93fbe2e3cb9fa36522df8facd00e01d6b79509719d36b7af`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:08:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:09:00 GMT
ENV GIT_VERSION=2.48.1
# Wed, 09 Jul 2025 18:09:01 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 09 Jul 2025 18:09:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 09 Jul 2025 18:09:02 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 09 Jul 2025 18:09:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Jul 2025 18:09:21 GMT
ENV GOPATH=C:\go
# Wed, 09 Jul 2025 18:09:33 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Jul 2025 18:09:36 GMT
ENV GOLANG_VERSION=1.23.11
# Wed, 09 Jul 2025 18:10:55 GMT
RUN $url = 'https://dl.google.com/go/go1.23.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '1dbcf0b4183066550964b22890fe119b0b867b51f12c1eea4445c71494d98cbb'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Jul 2025 18:10:56 GMT
WORKDIR C:\go
# Wed, 09 Jul 2025 19:17:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 19:17:52 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 09 Jul 2025 19:17:53 GMT
ENV CADDY_VERSION=v2.10.0
# Wed, 09 Jul 2025 19:17:54 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 09 Jul 2025 19:18:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 09 Jul 2025 19:18:03 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcbd7b0a1f3608f39f45d38d77bd1d8bc99b8b80577690ae49f2495fc6d51ce`  
		Last Modified: Wed, 09 Jul 2025 19:08:51 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbefaf0dfdde287d90804b77898b45c5ef94d64a330ae064873881c761bf218`  
		Last Modified: Wed, 09 Jul 2025 19:08:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb68e41d9f4d1f374375d6645219cda0ddaa36113d1f6de7f661dcc381e3d3e`  
		Last Modified: Wed, 09 Jul 2025 19:08:52 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fe9c0ea90e66e5734a67ac053e1d758d6f475bedd4a0a4cf411cf5eab16032`  
		Last Modified: Wed, 09 Jul 2025 19:08:53 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae92a24674185f8654a71266e67646d71a52721cdfe87cec0377846f4b97542`  
		Last Modified: Wed, 09 Jul 2025 19:08:53 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a073cef6dcac6c9a7d197c817a0ba7463a191042ef8cc3fd26924f06cfe4b7`  
		Last Modified: Wed, 09 Jul 2025 19:08:57 GMT  
		Size: 51.2 MB (51224393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a142b5a59ef9074cd98a328d00ff1b222b524c32b4976ea998157bea7cff68d4`  
		Last Modified: Wed, 09 Jul 2025 19:08:58 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b98273005a94fbcd558eb28bec9d8c9832e22ea984227d40a64e73a40f0244c`  
		Last Modified: Wed, 09 Jul 2025 19:08:58 GMT  
		Size: 349.3 KB (349345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e0d84361bfc8c1417975e73de1980d410cca0eb1163ac65642bcd63e513714`  
		Last Modified: Wed, 09 Jul 2025 19:08:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5755fedbe82004c3d756748e97eba3bdedea06701d4b28861ed527deb5c0e4be`  
		Last Modified: Wed, 09 Jul 2025 19:09:04 GMT  
		Size: 77.6 MB (77569178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b71e50361dc3c925a544f3540fa202962be34f46130c8b953b34fceb7deffe4`  
		Last Modified: Wed, 09 Jul 2025 19:09:04 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69835399ef07b45b77c84283b3d1e37e690ffbdc9c0a712b3aad6f04649f896`  
		Last Modified: Wed, 09 Jul 2025 19:18:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fffe22c1e6fca6e3c2e2059f0a9b0d21045cf9adfe64be5991c4e5ab61315a6`  
		Last Modified: Wed, 09 Jul 2025 19:18:25 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26a888014944bafdd9dc0a933c960732c80aac346d49270ee44d43afd8ca3db`  
		Last Modified: Wed, 09 Jul 2025 19:18:25 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b9a901b33f24eee2332dd23dc56b016fb0a9c5daf4c6e018455e7843e981f9`  
		Last Modified: Wed, 09 Jul 2025 19:18:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4640e7aaffe985e1a621940c94da4557766c00f2d076ca830ef0feea9612b33b`  
		Last Modified: Wed, 09 Jul 2025 19:18:25 GMT  
		Size: 2.3 MB (2321607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ac0c444eb4fc566a4085085d1fdba33d255c8e8be137993e0e2ddc62fc3c17`  
		Last Modified: Wed, 09 Jul 2025 19:18:25 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.20348.3932; amd64

```console
$ docker pull caddy@sha256:6157527e6fed75616094f6972c71b6071e33f0b08893c85e0533de15e952b3a8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2411855254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019f86e07d38d1b42f1b594b8e8aec4fb77a2d8902a128dad780517a7f866afc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Wed, 09 Jul 2025 18:06:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:06:54 GMT
ENV GIT_VERSION=2.48.1
# Wed, 09 Jul 2025 18:06:55 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 09 Jul 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 09 Jul 2025 18:06:57 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 09 Jul 2025 18:07:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Jul 2025 18:07:12 GMT
ENV GOPATH=C:\go
# Wed, 09 Jul 2025 18:07:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Jul 2025 18:07:19 GMT
ENV GOLANG_VERSION=1.23.11
# Wed, 09 Jul 2025 18:08:42 GMT
RUN $url = 'https://dl.google.com/go/go1.23.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '1dbcf0b4183066550964b22890fe119b0b867b51f12c1eea4445c71494d98cbb'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Jul 2025 18:08:44 GMT
WORKDIR C:\go
# Wed, 09 Jul 2025 19:13:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 19:13:12 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 09 Jul 2025 19:13:13 GMT
ENV CADDY_VERSION=v2.10.0
# Wed, 09 Jul 2025 19:13:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 09 Jul 2025 19:13:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 09 Jul 2025 19:13:24 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2745ebe15879863c900dce4d31c26bf15ccee738684810a4da8a80661e177db`  
		Last Modified: Wed, 09 Jul 2025 19:08:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8c59e2205e76bf173e1adb30626fa055162c78e737cd885ddfde3e38da7c97`  
		Last Modified: Wed, 09 Jul 2025 19:08:23 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2064dd864243ca68b83f22659721fe314f91f72be9fcf817d50a5f51d17480bc`  
		Last Modified: Wed, 09 Jul 2025 19:08:24 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c95a267a4418f0f43234691b22ffa8802a69384afc61880060341914d366b9`  
		Last Modified: Wed, 09 Jul 2025 19:08:24 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2789cf42aec2ebfbc4d51c756814d66a539874fd86bfc068909b7ce98681dde8`  
		Last Modified: Wed, 09 Jul 2025 19:08:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09247b0e58bd7d8ef3fafdd53befa0ef937b69ac0e0a55fdd99b0b2247cacfee`  
		Last Modified: Wed, 09 Jul 2025 19:08:34 GMT  
		Size: 51.2 MB (51206953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fda979f3aaaba414ace25342fdc89d1c0a6a926e45b90d84f25a9d422c15f4e`  
		Last Modified: Wed, 09 Jul 2025 19:08:27 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7116352baab3f98ac01c1f89c7170bb0589d8422cc6c550b0eb9eadc603ea3f1`  
		Last Modified: Wed, 09 Jul 2025 19:08:28 GMT  
		Size: 337.7 KB (337733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827a448cbb745d34faceee965ec1e3cf7cf4fde294a58ee4f0012c86f0ff817d`  
		Last Modified: Wed, 09 Jul 2025 19:08:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2c26c99defc3e53522167daa91cf7d82c6a687c1cc10838207ce1e73b4897a`  
		Last Modified: Wed, 09 Jul 2025 19:08:39 GMT  
		Size: 77.4 MB (77381108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2229011fdc31aec49881431e85b45c3800c5c047a3853bc9d431374b36e7897b`  
		Last Modified: Wed, 09 Jul 2025 19:08:35 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0067d6269ed01504216f3a809b30fe79bed579a1b969a1fd7929a5123fb4937d`  
		Last Modified: Wed, 09 Jul 2025 19:13:38 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534065932e6c6f14765ce28756d1639ad783b824a44911be14fca31c9b2382a2`  
		Last Modified: Wed, 09 Jul 2025 19:13:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3564005115ce42bfa972ac9a6f48ef70533a50aab6e657e35b3d914b5ade26`  
		Last Modified: Wed, 09 Jul 2025 19:13:38 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda52088de19ecd387595510935df0a8ef9126daa402722cfcf5478ca2544da7`  
		Last Modified: Wed, 09 Jul 2025 19:13:38 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf9eaa51711f18e920204bb0c22283608df6f6f4d55ec68cb6e9f94e12f83bb`  
		Last Modified: Wed, 09 Jul 2025 19:13:39 GMT  
		Size: 2.3 MB (2308984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294a2a53c9ea826b813d14689893ea9558e44489dd1e18ed1c626dbb57df2cad`  
		Last Modified: Wed, 09 Jul 2025 19:13:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:7eeb82cc1c2b652e528ec564b148c6480dc83ca16421d72e241b6bed4b963613
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
$ docker pull caddy@sha256:c275aa7f6e798c53b6bf3fc5b00a215245f788d7fc64343ec1d758dc62e4a813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85728747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edfcce821446c167912c393d40e005a90f1a61ebd0a2c178b4318d952795b0a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.3
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5418e60db87de98b06e455a400579c7f27106374f3450aef2951989cf6c7f536`  
		Last Modified: Tue, 12 Nov 2024 02:13:18 GMT  
		Size: 290.9 KB (290885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79bddf330f7de2b96b69740174bc7152350ef81439db2dfa776fc3a9365dc80`  
		Last Modified: Thu, 07 Nov 2024 02:59:16 GMT  
		Size: 74.0 MB (74038999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f115f9222c8e1a0a23300412608c2f4a3d45a6a471af693ed24f073d76d9f288`  
		Last Modified: Tue, 12 Nov 2024 02:13:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e773015b803d352bfac571049e306057e124cd9e3d7c4d0476ca12c5ebae044`  
		Last Modified: Tue, 12 Nov 2024 03:11:21 GMT  
		Size: 5.9 MB (5939333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c88b957b49feac2fef45d4a06daa8a3626b140810eff2e62243fdd45d1c3700`  
		Last Modified: Tue, 12 Nov 2024 03:11:21 GMT  
		Size: 1.8 MB (1835034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bead5fc7bd8165a4a5e774ef832586995f990eaf6d22520b1ab031c877e668e`  
		Last Modified: Tue, 12 Nov 2024 03:11:20 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:d64099638d3698f8d45926fe80603ce9857ae1fb2abb2fc30a2551c50f62dda3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 KB (312409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f9d9960c2360085b842f32b932627449bb3efd7350bb2dc55395fae07df515`

```dockerfile
```

-	Layers:
	-	`sha256:0fa46a3794b7477eedef6db2e2b49f85c0ccb59f6eb0540b85b2d19fd57f3537`  
		Last Modified: Tue, 12 Nov 2024 03:11:20 GMT  
		Size: 292.3 KB (292306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afa972c396e0966f2270208cd34da9cdc87f96c19f96da58954b095c97bb2088`  
		Last Modified: Tue, 12 Nov 2024 03:11:20 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:8c76795c5e3af1b368dcf4524c3af5c824c73ffa3a3fe547358b2df3ce8ddffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83455398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee91143d2ae02bfa384de5483629de4ff870701896d7d02d3cec2d5c91b2af7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.3
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09660efa60074dd6fc7ed0eaa983537498c86f66f4ce6ec6fd9caf5018feac3`  
		Last Modified: Tue, 12 Nov 2024 06:28:18 GMT  
		Size: 291.8 KB (291778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6930abd3e962e7fc186f25f91e441a0655bacbb61cdd3456fbbb1368d3ebbb4`  
		Last Modified: Thu, 07 Nov 2024 02:59:03 GMT  
		Size: 72.2 MB (72183939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b873e9251e8e42989c326bb96af5cfea033f4d3ad66985cc8ec880e29aadd662`  
		Last Modified: Tue, 12 Nov 2024 06:36:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401c02c0cea80698e352567571b00904b934f63b9388347a9e0f4badc9fe9a9b`  
		Last Modified: Tue, 12 Nov 2024 17:18:18 GMT  
		Size: 5.9 MB (5882198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f7e11289c13a7b340589fd73e36a96cf84043f878f58ccc0fb5e889fc97c87`  
		Last Modified: Tue, 12 Nov 2024 17:18:59 GMT  
		Size: 1.7 MB (1730292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdd3a26fabc3d279bc3df5702b4d37da0216cae9c47ec3bd55a8ddc7e1f1c13`  
		Last Modified: Tue, 12 Nov 2024 17:18:59 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f077570112978045e51ed474b07e912ab7f443680f3e1906e3982a9046c04bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc3d06eb43f2002b4b750dd689dcae8802f8c160bcaf94653756a3b95fcac73`

```dockerfile
```

-	Layers:
	-	`sha256:7b7246e031d1b80caab0bfa639ca69ab492498b3498180978f6c7f22905af848`  
		Last Modified: Tue, 12 Nov 2024 17:18:59 GMT  
		Size: 20.0 KB (20009 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ca72ebe177b0090004be564a47668074d55420e5fa39405461a7dc3e313df575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82662623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e29b61c9c33b59f779d2e4456d2d3f45674588106acc78b70c863ef39d5f53f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.3
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692a5c99cf15c99e5e68f32ee94771988d92aa96b54f7c87c6ca7ecd4a4c3ef9`  
		Last Modified: Thu, 07 Nov 2024 03:01:47 GMT  
		Size: 291.0 KB (290959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e990400f8c0342109351b2ea2dff891387190e755f29d02b0f474578fc3d222`  
		Last Modified: Thu, 07 Nov 2024 02:59:45 GMT  
		Size: 72.2 MB (72184086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251afc28a17b6c762e549530d05085933556f149eecfe4bca0301753743f37db`  
		Last Modified: Thu, 07 Nov 2024 03:01:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea6892c349814daa00d811e2c307016e3da8ac020d4d04a0ffd6d17a9d3f4a1`  
		Last Modified: Thu, 07 Nov 2024 03:52:01 GMT  
		Size: 5.4 MB (5367214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757d5fdd0558f87edfcabc42070efc631ac4ed82d17001de1f6f322467ab8719`  
		Last Modified: Thu, 07 Nov 2024 03:52:22 GMT  
		Size: 1.7 MB (1724267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401b7da51849ec4890fcaf7f1f6122dc8a620da4c5d0c537b805f6599d80b339`  
		Last Modified: Thu, 07 Nov 2024 03:52:22 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:163dc93c301d519e18c6d503b3be7f7e120885bafdf2d7dcbabaa73589a4eb5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.5 KB (315454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877f125bb4f91760292a47c762b959b3bdb7458c434d71271cd0d9f8870bc1ee`

```dockerfile
```

-	Layers:
	-	`sha256:cf2c1d640a00d599b4d1fec9e117c8303b3640b50d9a8c6825a1fa59e3e5e264`  
		Last Modified: Thu, 07 Nov 2024 03:52:22 GMT  
		Size: 295.2 KB (295201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f10e5f43302401b54ce121a883842ac49ce6aab7514d6f5d934e6021236f3c`  
		Last Modified: Thu, 07 Nov 2024 03:52:22 GMT  
		Size: 20.3 KB (20253 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:c829b6c2b173e455fabe36a4f3175113722f20e65b24bf3c4733274b39921ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82809202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c032c12068a82c5a428c5956c6bfbeac85241b3e687adc6f109f042b63cf3e27`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.3
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a9dd7d6fc256d156365346b32d280a887ef75129be8a63ce1612b621fc9714`  
		Last Modified: Thu, 07 Nov 2024 03:00:57 GMT  
		Size: 293.5 KB (293527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323003b0d8ad8001283c9881b96c87e9fa38fb378aa4de93c4defd3899f30d2a`  
		Last Modified: Thu, 07 Nov 2024 02:59:17 GMT  
		Size: 70.7 MB (70668948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cf7f03564cac6b07fdbe6eaff976145adcb2737e465abf5d0c66ea7d293a11`  
		Last Modified: Thu, 07 Nov 2024 03:00:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370ae107474e42770db3e82929032593609157ceb0c225180bd79c2ea3a8e7f9`  
		Last Modified: Thu, 07 Nov 2024 03:54:04 GMT  
		Size: 6.1 MB (6057061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afedeabe65d1f865e22d03b191f62b2772f94b1b6bc84ee18d221626d363d79`  
		Last Modified: Thu, 07 Nov 2024 03:54:21 GMT  
		Size: 1.7 MB (1701425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755123dc58d6a25b6484d533e026bd703b36d96f49b9a9a3877d52d7a55e91e5`  
		Last Modified: Thu, 07 Nov 2024 03:54:20 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:382d045249f4ddd034fd60e1420d5f603f7b9c19cc6baa833600da898ee59ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 KB (312709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea5f8ef86e7158683fa5382c703180bfa74047ed02b2bfacca9861767e3d2a70`

```dockerfile
```

-	Layers:
	-	`sha256:44c09c7be731485f5859aa16cea2196a55e482c34d6a961ee7c2474382449c88`  
		Last Modified: Thu, 07 Nov 2024 03:54:20 GMT  
		Size: 292.4 KB (292409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d093729e2aab6b8e09af049c4764bff1adeaf1d86d9889cbd59ff3a59e31856e`  
		Last Modified: Thu, 07 Nov 2024 03:54:20 GMT  
		Size: 20.3 KB (20300 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:82c72c1f810a0cf90313fd83e694d5a8b8b2f53f06f8dda862c194b581595b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82652654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9e0f91eb65f7854fd045df0c6157bdffb5ae33315f3704a4d675b60583b718`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.3
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
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3873bb4db6d014ff18a3c4d7f5d4ef80493c562c62c0640979ceafbca23930d`  
		Last Modified: Tue, 12 Nov 2024 08:05:08 GMT  
		Size: 294.0 KB (294032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d45dcd888e3183671630e662953341e3111584ee0e6ca4f0d40e50580ea2de`  
		Last Modified: Thu, 07 Nov 2024 03:00:09 GMT  
		Size: 70.8 MB (70828478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7c8e4b36ae1306e411f533d94206075953e9d651e034156cba75c35a30a3ed`  
		Last Modified: Tue, 12 Nov 2024 08:59:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630931d16168e591b310777d6d4afc985040ba29eb192d2b6baab6209f32bdce`  
		Last Modified: Tue, 12 Nov 2024 22:29:58 GMT  
		Size: 6.3 MB (6261503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4fc5ae25cf149b853984daeca1f876f0f72e0396305e35371cdfc01049b3f8`  
		Last Modified: Tue, 12 Nov 2024 22:31:05 GMT  
		Size: 1.7 MB (1695589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4546a4e012ba7b24d355c20ab5648133f888156963841be68387a2bc07ff4cc7`  
		Last Modified: Tue, 12 Nov 2024 22:31:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:03e393e03c34518748bf386be4f1181d9e87a5f62a2b82065f14e9b59e180ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 KB (310619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14f631c002f7f155f0dc57ee0ae9048d0f8461281effa449a0a81621f836dfb`

```dockerfile
```

-	Layers:
	-	`sha256:e8b5545f201d0751fc4e290c6ddf6a2b7ad74dc6c26a912f7e9ef6b6ecb4672f`  
		Last Modified: Tue, 12 Nov 2024 22:31:05 GMT  
		Size: 290.4 KB (290446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a83852009535b4bbf11cbc5e80ead80cac31c4f5a0be96f032b20996b5c716`  
		Last Modified: Tue, 12 Nov 2024 22:31:05 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:d80b92da6040cf7eb376c24abd073761372d03158f248f195cd50ae59ca559c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82756156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab47ac48a95b6bac602e3ca657606f1d53f0fd69805b1d155eaba29e75f7eb0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.3
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
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d1647e2ae8eb941891fcb716820e5bec12b348afc0d29dbe6ad642a22cf24a`  
		Last Modified: Sat, 07 Sep 2024 18:50:29 GMT  
		Size: 291.7 KB (291675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c484c4d08cd9e67227d89dc190049950041d21e09449643180abb682468f67`  
		Last Modified: Thu, 07 Nov 2024 03:03:27 GMT  
		Size: 71.2 MB (71227144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc55b235be95f2ff6a9be1e2b0f111736c00f3d24f6b1e210a063c73a9ba427`  
		Last Modified: Thu, 07 Nov 2024 03:03:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72be57ca3a65091f5822d089e73d96f826474070dd1b1f722f5d815a786d4a73`  
		Last Modified: Thu, 07 Nov 2024 03:49:03 GMT  
		Size: 6.2 MB (6153649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7567e735f017a35ab95f183a9da675436a2df11f3de12d10078336f41f9cab9c`  
		Last Modified: Thu, 07 Nov 2024 03:50:55 GMT  
		Size: 1.7 MB (1711640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e89e20c12422bcb20bcb028754d62b69a0044173990ac3a961debd8a5cf674`  
		Last Modified: Thu, 07 Nov 2024 03:50:54 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0378a41052bac7baa55ba9f78676973ad61fca58ef3c45fbc1f58f5a440fa191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 KB (310642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2766364cf15d12699d794e984d8b55bd99e551ff5094c9c2f1240e66545d2612`

```dockerfile
```

-	Layers:
	-	`sha256:fbc4c8e4706c056e158e01baefc00575ece6131b871a935e9bca9605872a5b49`  
		Last Modified: Thu, 07 Nov 2024 03:50:54 GMT  
		Size: 290.4 KB (290441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d33d9ab9c4299afb03eefaa3908883170704c2081cd8c2d6c5dcd1a2142e4734`  
		Last Modified: Thu, 07 Nov 2024 03:50:54 GMT  
		Size: 20.2 KB (20201 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:e7e36ed56d47c90d802f903c8a83b0ca9fa065f19a8d1006fe76cacda14eef75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84676067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7c75766096a6ed38fbf1c8f86b9666a515af8f0195ad31a7d56a5d94f3ec6b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.3
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140cf6f32a5dac327c76fa8577bc2bd58aa8dbef28f69659ae30a5ae04e176c2`  
		Last Modified: Tue, 12 Nov 2024 08:40:30 GMT  
		Size: 291.9 KB (291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899e076c675a549e2d1bc5d05ac9fc56f919b55bb9ec6d441d414eb5acb3e0b`  
		Last Modified: Thu, 07 Nov 2024 03:03:52 GMT  
		Size: 72.9 MB (72949892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083a9ffd7c5257f0dec6798fb9cd74fb2756d20c98a60d4573babce75266a9a9`  
		Last Modified: Tue, 12 Nov 2024 09:36:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a508bf4bce2dc330b92fc38ab768604381dfece200d6d2fa86016fd6dae546c3`  
		Last Modified: Wed, 13 Nov 2024 01:58:33 GMT  
		Size: 6.2 MB (6200669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a75402270194ec135b1c404fec84907f51702168857a16adcfe6014da1fb82`  
		Last Modified: Wed, 13 Nov 2024 01:59:50 GMT  
		Size: 1.8 MB (1771406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7940aedc741389e2b336f8c612480a3ea46d6315f5e176f5c2d96ff22cd9e8bd`  
		Last Modified: Wed, 13 Nov 2024 01:59:50 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:c02a8288ecc209bd5b1665deacc84b13358db4fc608f0863b18985d53f93fca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 KB (310455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbfeea4c5936d2f88050773c90e90c04d087bd1a5e7dee0ad018b09f9c356a0`

```dockerfile
```

-	Layers:
	-	`sha256:0eab8973667fd6a108b263faf5849b8e17fc29d054adcf48a472b7bac2c4cb8d`  
		Last Modified: Wed, 13 Nov 2024 01:59:50 GMT  
		Size: 290.4 KB (290352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dab2cfad921ecaaa638b2e2efcaf3bd290db274017bbfa495fc4ca2e1f9bb34f`  
		Last Modified: Wed, 13 Nov 2024 01:59:50 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

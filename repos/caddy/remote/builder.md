## `caddy:builder`

```console
$ docker pull caddy@sha256:e8ae2ab1723d2c4d8479950bd5af1955371c7a92bb097c0d40e1550f090b28b3
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
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:627d3c6bbd6f38261900944ae92383b140a8ee01e5527f77775e5513eea88776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85694839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c863df5991e799155e9d77602d7058dc25c797b473ceb4c35a840b0174c99c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc291be95ef93b54538c2124bbdf5f42b7bccf8a251f9798053ead5c40537e4`  
		Last Modified: Tue, 01 Oct 2024 22:18:50 GMT  
		Size: 290.9 KB (290883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac1f1163629431c9f488c4d6ff6afb5c73021839723b50bafe245663ad3d9df`  
		Last Modified: Tue, 01 Oct 2024 22:18:51 GMT  
		Size: 74.0 MB (74006382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3c966382ef0825906eb814d4601bda027b55eaea8849b31b967db8440ca886`  
		Last Modified: Tue, 01 Oct 2024 22:18:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d32afef9fd89acbbd4d4a18499a8d490bea2aa3a2abc00ae6c5b1d453be588b`  
		Last Modified: Wed, 06 Nov 2024 20:17:10 GMT  
		Size: 5.9 MB (5938143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddf83d413839c5a3858085c4afb87de311d54354e76913aa0904f9314374edc`  
		Last Modified: Wed, 06 Nov 2024 20:17:10 GMT  
		Size: 1.8 MB (1835033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55de3eea9fc8c1bb8b792e0897a444d9a5d67f6c2b72a32017423d4ad36e5bf`  
		Last Modified: Wed, 06 Nov 2024 20:17:10 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:68daa7985586c9d288a7b011b3e37227bd5d1a874b9a8a78f77383579146ffec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.4 KB (311373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898f2c00b9c10baa9d26537b8e3c7c1b6d9290b4d077eb160bee1ce80e7cc9eb`

```dockerfile
```

-	Layers:
	-	`sha256:fcaf8cbd43028cd7c4cca1780fd5ed714c80d9b95d2c4c815762de3be3be641d`  
		Last Modified: Wed, 06 Nov 2024 20:17:10 GMT  
		Size: 291.3 KB (291270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:455be441562f76c0eb13ccf8bad19768797f2f38479757b45031496827bcf858`  
		Last Modified: Wed, 06 Nov 2024 20:17:10 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:cae854fa7debac67c609a19ce9f447e9c249ba9dbfb8dcbf8940f2e408be8934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83432322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161f7c99af5a0879556246750308c10e3648bfd5e09a2f3b3a682ab67cb95d6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b15e82573debca2fd0fd40f07ac032fefe7f9180bd45f4f9cf2c2afde7d486`  
		Last Modified: Sat, 07 Sep 2024 02:30:42 GMT  
		Size: 291.8 KB (291766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b1b9390cf2d540f3f141f77cdd7d696ac60b3ebfef2290308fa3bb76ea42c1`  
		Last Modified: Tue, 01 Oct 2024 22:19:57 GMT  
		Size: 72.2 MB (72161312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc9acb00958700a6c1b82f31efa4608a6d95bf71fe3e12f8f1e1721edc2f528`  
		Last Modified: Tue, 01 Oct 2024 22:19:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f55ad89d3ca2484cab855dd6c8534e91bbfbb271c501b15e7644f2993d4596`  
		Last Modified: Wed, 06 Nov 2024 20:16:53 GMT  
		Size: 5.9 MB (5881855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68bbde78dcb36e97e119dc5fe87dd8f55c8145180b1cba79ce33823b7a37f4f`  
		Last Modified: Wed, 06 Nov 2024 20:17:12 GMT  
		Size: 1.7 MB (1730291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94677c76cc7a96156b9eb06fe503b5dfc45e6de17a0d48fdc933eb4e6e02b04e`  
		Last Modified: Wed, 06 Nov 2024 20:17:11 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:c7a5a0f4726bba0267ee9c9b5f1a6f852d34aa7dd4673da394292720d4fdaef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6804493c2b3456a11413bedee74abc91ffce4f1401af7bc2479262339fad740`

```dockerfile
```

-	Layers:
	-	`sha256:d7090898630a7ca34b72ec039ead50819237e6f9f743764f970e50c0115683c0`  
		Last Modified: Wed, 06 Nov 2024 20:17:11 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:06389cb8beba434bb8f373e4a985979bfd8d8806ab544602ce9c0d2310e8fcc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82640085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98951fd9504d94c3bd783fd1ffd6a5ca9897057f62789934fce1ee0da7df27e1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
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
	-	`sha256:354df8adec1f26ac2f376cb666910440b4b25a704fec8a3d318f7aff11e80108`  
		Last Modified: Sat, 07 Sep 2024 02:43:40 GMT  
		Size: 290.9 KB (290948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda832285c268d03f9079f25d645da4f232d333a236aca4f5406f4294d01f183`  
		Last Modified: Tue, 01 Oct 2024 22:22:37 GMT  
		Size: 72.2 MB (72161385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307f1bb2903db1d93c3a9404426b26560014c99fccb1aaac8b1d5f7501b23bb1`  
		Last Modified: Tue, 01 Oct 2024 22:24:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4754dced2dbc8197e05b9273ddf455fe892470e8cc170491286d5451363605`  
		Last Modified: Wed, 06 Nov 2024 20:07:53 GMT  
		Size: 5.4 MB (5367390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0df3c4903754d47c96f31d40e79c4e3be79401410c160d1889661cc04bea05`  
		Last Modified: Wed, 06 Nov 2024 20:08:17 GMT  
		Size: 1.7 MB (1724268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebbc8aa51082609e8f94abc5588ff5264f41a2e1ef3041b02dc2513cb5f24f4`  
		Last Modified: Wed, 06 Nov 2024 20:08:16 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:d3b45e117f0547619f275905a1dc3bb88e239ebd971f2016ba0e251c2cc05dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 KB (314420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0ad8a409366699c6da0a84fa04473a56a811f2c7e46b3c5d71579971fecfb6`

```dockerfile
```

-	Layers:
	-	`sha256:325deb85910554ca0130c71af80d1480653dab33fb703574f47841108dcec1ed`  
		Last Modified: Wed, 06 Nov 2024 20:08:16 GMT  
		Size: 294.2 KB (294166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdc7935b05b490d011b153142033c7387d7d55d58952a1a473590c18e20126b3`  
		Last Modified: Wed, 06 Nov 2024 20:08:16 GMT  
		Size: 20.3 KB (20254 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:88ff6b1e550bbf67f1be68bd631d4f64159c1f7169570250ff9804214a9c84a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82784116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a964b12c0cbb4c88d209c15e037b7cf49130d1fa348c77689508457939e69154`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
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
	-	`sha256:55b35a11ae5eab5f9885f480b702f14893ab21d2d29f58cd678d35d2fde98e27`  
		Last Modified: Tue, 01 Oct 2024 22:23:44 GMT  
		Size: 293.5 KB (293518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37a00ec5f007d0ae73647c82b7d81d98a44fb7d073d06e633d656bca79db62a`  
		Last Modified: Tue, 01 Oct 2024 22:22:17 GMT  
		Size: 70.6 MB (70644133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b3750afda1ed5c34a5153357a453f4928aa99e9f60005309772f320263a9ea`  
		Last Modified: Tue, 01 Oct 2024 22:23:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fca3dab344e839a07c64475cf28a0f59e36853cba0a6064caed357b6b235108`  
		Last Modified: Wed, 06 Nov 2024 20:47:31 GMT  
		Size: 6.1 MB (6056804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220e8dc2bc765e88e648cb870618ab8be82bcd70cc3bb51c9eec49a948798ce7`  
		Last Modified: Wed, 06 Nov 2024 20:47:50 GMT  
		Size: 1.7 MB (1701423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06efea961a5140a0a32ed5389e6852beedb8c2aead8a50924ab21a45cfb52633`  
		Last Modified: Wed, 06 Nov 2024 20:47:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:f405b495f1a9e646c83dd6ea4795a09e2a962cbab791e6ef2f8e35ae4bd4bc3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 KB (311674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6985011357cbefb2e1d9f29cec65dac771c48a6d47672dd48c091f948e2158`

```dockerfile
```

-	Layers:
	-	`sha256:77a73a56cc385bfae7e8e81c57e623f5c95d6ca59887762967850092272e16ef`  
		Last Modified: Wed, 06 Nov 2024 20:47:50 GMT  
		Size: 291.4 KB (291374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d48577c5c5469aee39cae5ea0cde017f7d637c51aaf0f231dbceafe0a45e80`  
		Last Modified: Wed, 06 Nov 2024 20:47:49 GMT  
		Size: 20.3 KB (20300 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:a5089f49ba57463de2fd0631eac90d54c56e834fd56586f373e326ceaafa979a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82634695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b86aab8146f22c41be51ea225c9b5b99f6e4099599bf5394c57a29e50cad6dd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2777b92ee7dc04466b000faa6509a7d3ab582a06829100a0e5946b4fe3b87b2c`  
		Last Modified: Tue, 01 Oct 2024 22:26:01 GMT  
		Size: 294.0 KB (294025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdc178eefce949e69fe38c13cce1ba17fa50a129169fc4241e2ca8280bdbc6c`  
		Last Modified: Tue, 01 Oct 2024 22:25:17 GMT  
		Size: 70.8 MB (70810506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b35cb4fb96e048171bc4247d1b190dd8cd1fc15af949a27d43f5aa5b71c42c0`  
		Last Modified: Tue, 01 Oct 2024 22:26:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da789d9c073e9121a52a9ca76669bf552e869483c5d6fc7fe9b094b77d80c8ed`  
		Last Modified: Wed, 06 Nov 2024 21:09:43 GMT  
		Size: 6.3 MB (6261549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c210d579b0ea54a1b890ef288f3325c0ebfc197ac52ddfa5fdbf83ac8c8d5c`  
		Last Modified: Wed, 06 Nov 2024 21:10:12 GMT  
		Size: 1.7 MB (1695603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87963c6fb9e28c840441f32b81c4bca657f6cb4f7275b33d97060a73ac8d705`  
		Last Modified: Wed, 06 Nov 2024 21:10:12 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:af09e46acfc98eda5fd3b592d1979ec0131c4e20a5a790d275e1610609c83ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 KB (309613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe660961527c79f2484fbf01b5818297c6242f84f4e4886c0d96d86a03dcd04d`

```dockerfile
```

-	Layers:
	-	`sha256:6dc01300453a4e1d0a3f8a4f306d9dee88ba6af15a9751a7b040930c3f11403d`  
		Last Modified: Wed, 06 Nov 2024 21:10:12 GMT  
		Size: 289.4 KB (289410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:177670347ad13886efaae3313182cff9f76bc71bd82c9c6024443b86de85fa80`  
		Last Modified: Wed, 06 Nov 2024 21:10:12 GMT  
		Size: 20.2 KB (20203 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; riscv64

```console
$ docker pull caddy@sha256:36afb833951db625486b5f495b99ed2e08613f7c5a761ea59de540c25446a5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82738257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f62557fea9c75175c6141ea91641a40dcbdc73e909c39e912003579a5fa99ea`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
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
	-	`sha256:26156af92be8af78ec34e57540c2fb481adbad857c6767dc9fa18e63dd6a0d40`  
		Last Modified: Tue, 01 Oct 2024 22:35:50 GMT  
		Size: 71.2 MB (71209248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8de42508b00410480c75e286849a709ea0f3febf9ab4db82d481831621d9b44`  
		Last Modified: Tue, 01 Oct 2024 22:35:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637e244318ddeb92fc54f3cdda7218d0133e80706b8b201b206e27831146857a`  
		Last Modified: Wed, 06 Nov 2024 20:11:01 GMT  
		Size: 6.2 MB (6153646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64f07f7b0b8e23d73855aba160c443e04defc1128d6e93c331c996a73738310`  
		Last Modified: Wed, 06 Nov 2024 20:12:21 GMT  
		Size: 1.7 MB (1711643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1d7e71c13e1f2d1449da8d97d2b53c04e7bec28b83adcc7f3e0f8557d97ca4`  
		Last Modified: Wed, 06 Nov 2024 20:12:20 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:0846637464b5e09a8299f71e385ba7088f01476f8231a25bba8e469ebc67c6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 KB (309609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff577d17f02b972129a620ec73533fc4a394bb46b1301a8736313a49eb99ed2`

```dockerfile
```

-	Layers:
	-	`sha256:558a30ad90b33bc54ccbec3dabbd2c83167c46fc0ea77db7b55962e828b26d01`  
		Last Modified: Wed, 06 Nov 2024 20:12:20 GMT  
		Size: 289.4 KB (289406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3cb647325aac0cd2809790eff3f966e66172e9267ec3ee37b09f2fa187989b1`  
		Last Modified: Wed, 06 Nov 2024 20:12:20 GMT  
		Size: 20.2 KB (20203 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:7a2da66662470f70ce61d7ba369f729a67a057ca21fca7475834b0641f3e2d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84662175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86123b5653beba07d8eca4d43169c56b1be47b09c22e3cd5613502081d6877e0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c6a0ddb32c239716405fcb244342a8d9c9657fd7f86e86d8b5d11ec45f0543`  
		Last Modified: Tue, 01 Oct 2024 22:22:42 GMT  
		Size: 291.9 KB (291893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb0f3540aaee2844fb7022ba44453797a29663928ffe252ed090c5b51b28634`  
		Last Modified: Tue, 01 Oct 2024 22:21:50 GMT  
		Size: 72.9 MB (72935651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900f3cc689365ec7d295c9dddc92b244bae88e83c2fce2a586d0996c645bff7c`  
		Last Modified: Tue, 01 Oct 2024 22:22:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753fc55eb4c845cc6e76c67a7c09a3040fa621bdd7f5ba621f7edc7831e95bc0`  
		Last Modified: Wed, 06 Nov 2024 21:00:16 GMT  
		Size: 6.2 MB (6201032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96307d8df3abee28efd486ddd16c56bc575739ee190966e5a60807349e6e9b2`  
		Last Modified: Wed, 06 Nov 2024 21:00:55 GMT  
		Size: 1.8 MB (1771409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912d2e91dee7400b99602a236682f8f46a0c26c18a73a93dd786da0c38638cb4`  
		Last Modified: Wed, 06 Nov 2024 21:00:55 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:cd795762c56a1898471f5282afa15d22625454a6242daa71c5f035132e0a2ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 KB (309449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7482e19f94234c280fc2a39402d02ceb2155e5f0d38b212d25d9d0b697e5e0`

```dockerfile
```

-	Layers:
	-	`sha256:1ced9829b56bd51aaa1093369dc3d94a8e5c0586c80318167ad905d449172316`  
		Last Modified: Wed, 06 Nov 2024 21:00:55 GMT  
		Size: 289.3 KB (289316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a000d46444289b510071e6a3db89aca8c329ff0630a9d1d1e4400c9b470470`  
		Last Modified: Wed, 06 Nov 2024 21:00:55 GMT  
		Size: 20.1 KB (20133 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - windows version 10.0.20348.2762; amd64

```console
$ docker pull caddy@sha256:c56f98d90e2e457640fa1029aecefe833c6f75f13b427471652c79fd7de2b371
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1904913713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b66c100754f8193a531a79cb5b27951bdb0cb9445cb4eed080d746d695b3298`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:00:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:00:01 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Oct 2024 23:00:02 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Oct 2024 23:00:03 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Oct 2024 23:00:08 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Oct 2024 23:00:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:00:29 GMT
ENV GOPATH=C:\go
# Wed, 09 Oct 2024 23:00:34 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Oct 2024 23:00:35 GMT
ENV GOLANG_VERSION=1.23.2
# Wed, 09 Oct 2024 23:01:52 GMT
RUN $url = 'https://dl.google.com/go/go1.23.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bc28fe3002cd65cec65d0e4f6000584dacb8c71bfaff8801dfb532855ca42513'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:01:53 GMT
WORKDIR C:\go
# Wed, 06 Nov 2024 20:18:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 06 Nov 2024 20:18:56 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 20:18:57 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 20:18:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 20:19:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 06 Nov 2024 20:19:49 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5ee69cc7a7c00cdf4c7f1dbff132533631d0ad0ceaa5b5ff3db486c5b53c91`  
		Last Modified: Wed, 09 Oct 2024 23:02:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cbbe74f967f0f9a9ef684fce9a9aa625821acdbfe105c34435074aef0d4d18`  
		Last Modified: Wed, 09 Oct 2024 23:02:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf92431dccc391f1ee38a98f1ca77b1097bda8214d7419e6969cb3abf8430c4`  
		Last Modified: Wed, 09 Oct 2024 23:02:00 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41eaca868705c9e05560d53495acf3d495d0b7a06c6ca9b329fbd507d7d6edea`  
		Last Modified: Wed, 09 Oct 2024 23:02:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba929dd024b4609634374ae5172ba04b23b9a0d30aa37a2b7ca3d881d55c2b6`  
		Last Modified: Wed, 09 Oct 2024 23:01:59 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1298a5450abb7290201ff8c77efe56187bfa7a3ebef66eff603c77c1b506b6fa`  
		Last Modified: Wed, 09 Oct 2024 23:02:02 GMT  
		Size: 25.6 MB (25565156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64778e8a77ed158cfedca607e2abc463e88daa09877472b22079c2d7bb486626`  
		Last Modified: Wed, 09 Oct 2024 23:01:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ce14ff8404e31e6ceaaaaa071eea060149cdb4568c12d3539669a2744c2fff`  
		Last Modified: Wed, 09 Oct 2024 23:01:58 GMT  
		Size: 335.7 KB (335731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b91e7a00fd9533319ca369401b4fe2dcefda3dfa70aa511d56ca40081abd57`  
		Last Modified: Wed, 09 Oct 2024 23:01:58 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd6e8a148665bc2d68668af00265458e6f605be340e500fc302c1c9ca4e7437`  
		Last Modified: Wed, 09 Oct 2024 23:02:09 GMT  
		Size: 77.3 MB (77328388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74da972d21cb88b99cb078df72e224aff083f94475d206d2cd1f1536774545cd`  
		Last Modified: Wed, 09 Oct 2024 23:01:58 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee91de67bfd91bedb32266ee1feb36ef953cf5b4920f7ac3129a1fbdd15ce20e`  
		Last Modified: Wed, 06 Nov 2024 20:19:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b89ca81d6a876ce2ed2621d151d1028ec36299752455ba6440104ce85be6f5`  
		Last Modified: Wed, 06 Nov 2024 20:19:53 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5b704a5654724654404a1b3d0915be0a063f38cbb58e3b8fc513d499af3c7b`  
		Last Modified: Wed, 06 Nov 2024 20:19:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eadaedcf25f29bc48e9da359d5ab56dbae59d455ff13380fcde6b7a38ad8ea0`  
		Last Modified: Wed, 06 Nov 2024 20:19:53 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34c1826de8ed0a3ea7a0368d26b248b9c6bee6be0fa42579ed9056a668ccc65`  
		Last Modified: Wed, 06 Nov 2024 20:19:53 GMT  
		Size: 2.3 MB (2326054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3b36fbd02c354bbf4d2140c98092e9e14964e9d2d8f6ca5c86ff1375d74a23`  
		Last Modified: Wed, 06 Nov 2024 20:19:53 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.6414; amd64

```console
$ docker pull caddy@sha256:46ef9bb842aeb42e97219be1e781cffe92a1645805717e4269490912f9688667
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007515307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6cfb2c27d9224e95e7fae6d69bed060b05419bc8da8489bc23856eddb240ff`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 09 Oct 2024 23:07:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:07:08 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Oct 2024 23:07:09 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Oct 2024 23:07:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Oct 2024 23:07:10 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Oct 2024 23:08:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:08:17 GMT
ENV GOPATH=C:\go
# Wed, 09 Oct 2024 23:08:23 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Oct 2024 23:08:24 GMT
ENV GOLANG_VERSION=1.23.2
# Wed, 09 Oct 2024 23:10:26 GMT
RUN $url = 'https://dl.google.com/go/go1.23.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bc28fe3002cd65cec65d0e4f6000584dacb8c71bfaff8801dfb532855ca42513'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:10:27 GMT
WORKDIR C:\go
# Wed, 06 Nov 2024 20:21:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 06 Nov 2024 20:21:06 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 20:21:06 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 20:21:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 20:22:45 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 06 Nov 2024 20:22:46 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0b69ce3049c27995588e18993ed09137752980cac80c4663648f5089cd9275`  
		Last Modified: Wed, 09 Oct 2024 23:10:35 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbba7602ffdb33cd282009cf1d68032a22821a3999cb542a3ad983d4d826621b`  
		Last Modified: Wed, 09 Oct 2024 23:10:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85184f815a4ea0c2d893d89869ca572c31fb105c4c70b03706bd4f58ca4aaf0a`  
		Last Modified: Wed, 09 Oct 2024 23:10:33 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc241ab5ab4740281e28481724541dcc6e188f2ffa28e4861f5648d630ace57`  
		Last Modified: Wed, 09 Oct 2024 23:10:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c76426ffa00c2faa295c3cc1b31156e15134b0690e4a1b629a64fe729e7056`  
		Last Modified: Wed, 09 Oct 2024 23:10:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c03c0444578ea76cd2a730e33886d9c2ec957c31c4341bddd62b67f34508c3`  
		Last Modified: Wed, 09 Oct 2024 23:10:35 GMT  
		Size: 25.6 MB (25566436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81fe3d482d8c7ec1f9a8be4b592907ad8c05d338a0c9edb4a4b734a79eee532`  
		Last Modified: Wed, 09 Oct 2024 23:10:31 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1ed797d603bcaafab01b729f9f4997af2b4b044ee40a85449f400aead10eed`  
		Last Modified: Wed, 09 Oct 2024 23:10:31 GMT  
		Size: 324.8 KB (324810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54630601fb93553af5e9d2e83bb1e0d212cce73f4bea992c668aef743868d62d`  
		Last Modified: Wed, 09 Oct 2024 23:10:31 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc433f483b37ead71df015348df3261600f715ed35293715ecb7153d8b78a20c`  
		Last Modified: Wed, 09 Oct 2024 23:10:43 GMT  
		Size: 77.5 MB (77501886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2af687eb62f54159437b2fb0cf416cb98e217cc5a67ef09d2f3dfbf072c95c6`  
		Last Modified: Wed, 09 Oct 2024 23:10:31 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b48eb982a8ddb9d96ec1908a1ceb8ffc072012d11b4b2c06cbc69e80c29d1f7`  
		Last Modified: Wed, 06 Nov 2024 20:22:49 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d142374aa26d0721b8e7068b89972dfb13cfde709e7d91839bcd5749f1d461`  
		Last Modified: Wed, 06 Nov 2024 20:22:48 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821403f04f286922e0d17b7402ec9844d324459d3bc1b88ae7d8ee7e4e1ed39f`  
		Last Modified: Wed, 06 Nov 2024 20:22:48 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bfc36eb6f9de477a8778839a572e45d3cf59bdae9bc0c3562259126aeeaed7`  
		Last Modified: Wed, 06 Nov 2024 20:22:48 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216c7f0712937bdec08483e1b27c108cda4cf76038e194693f928435d7b876b0`  
		Last Modified: Wed, 06 Nov 2024 20:22:48 GMT  
		Size: 2.3 MB (2279819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e64f90f4a504808d7b0b814ed9f50b284874a0312064c27b68d17aa8fd3405`  
		Last Modified: Wed, 06 Nov 2024 20:22:48 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

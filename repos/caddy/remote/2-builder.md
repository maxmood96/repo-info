## `caddy:2-builder`

```console
$ docker pull caddy@sha256:0b67771fda573b19475cd37797852879f0446d5b9f9d93f0b1c81f80d659d71a
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

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:c7794ae58321269077ae1c1552c38728d592dad5659cd7d0b264dc0e76da18e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85728623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1501d8d2b104c73d567bf846ed7ab9d00475f5b6b4ce440920e85417afddaaf8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec3504c519ede37edbfeab3192c34fc3317c4556f73a6135b62d6acddecf7d9`  
		Last Modified: Thu, 07 Nov 2024 02:59:19 GMT  
		Size: 290.9 KB (290892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79bddf330f7de2b96b69740174bc7152350ef81439db2dfa776fc3a9365dc80`  
		Last Modified: Thu, 07 Nov 2024 02:59:16 GMT  
		Size: 74.0 MB (74038999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d736227ff64f235e10d886a357b3931714b743aa1283e3aae02a14d72947540`  
		Last Modified: Thu, 07 Nov 2024 02:59:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13828ffdd4389c93409123ef33f56b4424c807e39a213488c9d8691c3baa550f`  
		Last Modified: Thu, 07 Nov 2024 03:47:45 GMT  
		Size: 5.9 MB (5939298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bcca2936aa13ba4e3acc587e27d78bfc8fb59b0dfeccf2c95f83d8b069351cb`  
		Last Modified: Thu, 07 Nov 2024 03:47:45 GMT  
		Size: 1.8 MB (1835035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453eda5dc90fb55dd644a934b080e63df2df1ef8db8a3fdcc530ee06fabace28`  
		Last Modified: Thu, 07 Nov 2024 03:47:44 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:0d263fbb0cc21a1847815db57f50ae7c4ee13eb50098986d0f4907d823254e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 KB (312408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e88535f3f6a177f27181436943953cad8c1e24d5ccfd852db0f9a3c09f35f4d9`

```dockerfile
```

-	Layers:
	-	`sha256:7fc79eee0600288541d9689c3350deed6a4ee1a5f7064314e1535aa2a6b339be`  
		Last Modified: Thu, 07 Nov 2024 03:47:44 GMT  
		Size: 292.3 KB (292305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba6e92a3115232b800d2d0846a81a24543175c728e62156c171f2231845c235c`  
		Last Modified: Thu, 07 Nov 2024 03:47:44 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:7e06e7bed3576900724bf9128d70de01be5b082f69b36f4b80ea4e35e0d79635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83455282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f4d8cfca445b3cdee3af0ed8ae35cbf3d64f8fb51d9b274a2806ea1caeabd2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b15e82573debca2fd0fd40f07ac032fefe7f9180bd45f4f9cf2c2afde7d486`  
		Last Modified: Sat, 07 Sep 2024 02:30:42 GMT  
		Size: 291.8 KB (291766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6930abd3e962e7fc186f25f91e441a0655bacbb61cdd3456fbbb1368d3ebbb4`  
		Last Modified: Thu, 07 Nov 2024 02:59:03 GMT  
		Size: 72.2 MB (72183939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cbd67afa5dce215f171ef96e6a8c433a7fa35da4056ea98d54c33154aa16ac`  
		Last Modified: Thu, 07 Nov 2024 02:59:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256d0ebe20260d02c5fbc24f92305d1c893f4187cd643809b1e1b913aa3fc001`  
		Last Modified: Thu, 07 Nov 2024 03:47:08 GMT  
		Size: 5.9 MB (5882184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249136a9d884000ce5e8db8dbaeba99986dbc16aed76cb2bbc0b9584fd8cbeab`  
		Last Modified: Thu, 07 Nov 2024 03:47:29 GMT  
		Size: 1.7 MB (1730292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462490c9d439d4f3299cee2f85fb7c7aef3dc0dbc198f4d491afb44c1026f891`  
		Last Modified: Thu, 07 Nov 2024 03:47:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:36bb742d7aa6757a2a70e319738b1e3b98e7152e6dc0aa0a065d3f6563858276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a4c34ea357f381b6599fa9849136ca58e4b2ea98a782ebaf11161cb0f914d7`

```dockerfile
```

-	Layers:
	-	`sha256:afc93cebe674deeb0c45ea9385a2c0efec37ec535c87c5c31359df70cd8c4297`  
		Last Modified: Thu, 07 Nov 2024 03:47:29 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

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

### `caddy:2-builder` - unknown; unknown

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

### `caddy:2-builder` - linux; arm64 variant v8

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

### `caddy:2-builder` - unknown; unknown

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

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:4061691c86012db80082bc238a9552ef6cdc1ceabe3d5a1ef1b4846a73874ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82652651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500dbd25d4b186e89173a36d3c7d97206e9dae819d6c863067328dcfed9c273a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977bd9456f1b6f8f4f6980e045da412051b1eade2ac61e6b8469b4da52c93c14`  
		Last Modified: Thu, 07 Nov 2024 03:00:59 GMT  
		Size: 294.0 KB (294035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d45dcd888e3183671630e662953341e3111584ee0e6ca4f0d40e50580ea2de`  
		Last Modified: Thu, 07 Nov 2024 03:00:09 GMT  
		Size: 70.8 MB (70828478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575d60aafb46a5e5a1ed1b28ef7df9a44a573432b2679198eaecf6dff5d9a40e`  
		Last Modified: Thu, 07 Nov 2024 03:00:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6b81dd338c46344db4bc83d52c8c954f92deb8a8ca66c67566fc53f60bdc85`  
		Last Modified: Thu, 07 Nov 2024 03:47:32 GMT  
		Size: 6.3 MB (6261526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf9b45410a237c217a709f31db6cff1e18b07c00927c37e602ba62f1a106acc`  
		Last Modified: Thu, 07 Nov 2024 03:47:56 GMT  
		Size: 1.7 MB (1695601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3573d100752675013cdb0a76ea822ed4adc36289e8d93aae932c475763e273db`  
		Last Modified: Thu, 07 Nov 2024 03:47:56 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:084f3d23e5cdfc7215e1771a99c29a2c763ab170485927733d61dfd2d50a461c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 KB (310648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb913a5494c673b830a587d8d0c033f614b55cd1bcd13322756ca7f3cd93f0c9`

```dockerfile
```

-	Layers:
	-	`sha256:215768bcdc73bb6c815e05d1b37fc268efe3650f4633d10683c89997fbfd4504`  
		Last Modified: Thu, 07 Nov 2024 03:47:56 GMT  
		Size: 290.4 KB (290445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c16799e6f6b5a6d408f0defed060d44c46d82f36a30555e17b1cdd9e7199e24`  
		Last Modified: Thu, 07 Nov 2024 03:47:56 GMT  
		Size: 20.2 KB (20203 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; riscv64

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

### `caddy:2-builder` - unknown; unknown

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

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:3cfbd60de6afee664e529185504b3d4f03d02c8ef129ddd8f15c813e1e628b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84676007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93c27ff07b04fe58d0632a6e514a8215fadfa95b8ba815c26fd9308631b0d7d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4e1cbd4051c86d195b2fb96cfc17e7a43cdeb3b02d9c627067475b5a4d1cdd`  
		Last Modified: Thu, 07 Nov 2024 03:05:08 GMT  
		Size: 291.9 KB (291897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899e076c675a549e2d1bc5d05ac9fc56f919b55bb9ec6d441d414eb5acb3e0b`  
		Last Modified: Thu, 07 Nov 2024 03:03:52 GMT  
		Size: 72.9 MB (72949892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d622173296eb148f54cd87d18cae3a2b542c4de2fd4c4c57600f64a3449863a`  
		Last Modified: Thu, 07 Nov 2024 03:05:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1edb17c0048cda770653382600f524a8ff8ae9aace1b2f9a5fa1508b7d730a4`  
		Last Modified: Thu, 07 Nov 2024 03:47:44 GMT  
		Size: 6.2 MB (6200620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cdc3f2288d0fd4b070d492affe0adb43b0f7045f43b8310ef20e10f0cb7c7d`  
		Last Modified: Thu, 07 Nov 2024 03:48:19 GMT  
		Size: 1.8 MB (1771408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713f7d34eeafdb2b1bdcaf76058e5def92b9d4156acffc0f3a01c59cc7b8d280`  
		Last Modified: Thu, 07 Nov 2024 03:48:19 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:ba7746cb0ef5eb3b0a1e041b5160357bdb00a52c45ac608c8f0425cd8dae7016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 KB (310484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21fe5e9ad0831dbaa862dc651b60afedfb045d8b4d1e68b29897a674abd764ec`

```dockerfile
```

-	Layers:
	-	`sha256:e6cc73d9bacbc8b1f2cec2a4e122c1ac183d54a74479fd51ff82df867b6e17e7`  
		Last Modified: Thu, 07 Nov 2024 03:48:19 GMT  
		Size: 290.4 KB (290351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:680f138a6b8a3d963b33e1e04d9ad693374875bf0b06ce4fd98b2caaf5b3db52`  
		Last Modified: Thu, 07 Nov 2024 03:48:19 GMT  
		Size: 20.1 KB (20133 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.20348.2762; amd64

```console
$ docker pull caddy@sha256:67d5a2f7b462f74b4e48cdf32d9db455aaf28ed02d34688be2dffa97d622c66a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1904860570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9346e598e5835692b4fc86ea2510dc444f3ad32032fd301784be4c7bf9ebadc8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 07 Nov 2024 02:58:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 07 Nov 2024 02:58:54 GMT
ENV GIT_VERSION=2.23.0
# Thu, 07 Nov 2024 02:58:55 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 07 Nov 2024 02:58:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 07 Nov 2024 02:58:56 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 07 Nov 2024 03:00:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 07 Nov 2024 03:00:20 GMT
ENV GOPATH=C:\go
# Thu, 07 Nov 2024 03:00:29 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 07 Nov 2024 03:00:29 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 03:03:45 GMT
RUN $url = 'https://dl.google.com/go/go1.23.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '81968b563642096b8a7521171e2be6e77ff6f44032f7493b7bdec9d33f44f31d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 07 Nov 2024 03:03:47 GMT
WORKDIR C:\go
# Thu, 07 Nov 2024 03:48:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 07 Nov 2024 03:48:52 GMT
ENV XCADDY_VERSION=v0.4.4
# Thu, 07 Nov 2024 03:48:53 GMT
ENV CADDY_VERSION=v2.8.4
# Thu, 07 Nov 2024 03:48:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 07 Nov 2024 03:49:45 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 07 Nov 2024 03:49:46 GMT
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
	-	`sha256:93105cad37ac2db7852d9c8b1e6968933a0e1f1347105e4b7c94267918587bad`  
		Last Modified: Thu, 07 Nov 2024 03:03:51 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f258ce4d4a15b8de5b0df63fb077c75e9f79b218d6e9893554b7bf17b0f7b23`  
		Last Modified: Thu, 07 Nov 2024 03:03:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6dbba024fe19e5d4cee47b892915ccd03a9ad05807dbe33724f5d67ee52074`  
		Last Modified: Thu, 07 Nov 2024 03:03:50 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c247a7154b82eeeb58862435e636cbe0f711af9a8a337bd2b0d3fe6533924bb`  
		Last Modified: Thu, 07 Nov 2024 03:03:50 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13755730617540a514e08bbb1df08535cb6305df44f9869986537b5d882e92a2`  
		Last Modified: Thu, 07 Nov 2024 03:03:50 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05261f39a1942a46d4208b6be6fadec5f78de65d816a1ce2e6c9320baf7349d8`  
		Last Modified: Thu, 07 Nov 2024 03:03:52 GMT  
		Size: 25.6 MB (25585901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f528154fa38b2dc730f7440d9aa60f517673554ce026fc83168f2d3be6c9fb33`  
		Last Modified: Thu, 07 Nov 2024 03:03:49 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed056cbe6bf305b555e6e2d06d7e1bbe2e9c613bd976984d1e487fc7adc6d38`  
		Last Modified: Thu, 07 Nov 2024 03:03:49 GMT  
		Size: 314.9 KB (314883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266ba7e4821cd14be34bd35eb3a274f0ff3ace0c15ddb61d763c539f0f6c4c37`  
		Last Modified: Thu, 07 Nov 2024 03:03:49 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a85b28fd61ecb94994841e2e28952fa642e89311e234528492bebdafe02e6a3`  
		Last Modified: Thu, 07 Nov 2024 03:04:00 GMT  
		Size: 77.3 MB (77310229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d582fcbc46a78e9081e34f4b0150b686b26dd9028f80c856791b2ce53f65269`  
		Last Modified: Thu, 07 Nov 2024 03:03:49 GMT  
		Size: 1.5 KB (1457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedc941f717e5911ce2148e6ac1bcbfc7dfd2e9a2a65e3e6cda0fd8ff62e8aa4`  
		Last Modified: Thu, 07 Nov 2024 03:49:51 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d00909260cbff746f2221c019d1f7ead37c5e364569c498c0147e797756edad`  
		Last Modified: Thu, 07 Nov 2024 03:49:50 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1760a8be95eff11850e88d4df0928d6e297762cfa09dac2c26147271e3eff0f`  
		Last Modified: Thu, 07 Nov 2024 03:49:50 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c5524295b6e8dfa1f769b574c3ae759dd04d27875f2028600f27daadedc7e9`  
		Last Modified: Thu, 07 Nov 2024 03:49:50 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a3209cbd64cc68608c3d85c12a9f18742234d9c6b7a83304f9a58b94231109`  
		Last Modified: Thu, 07 Nov 2024 03:49:50 GMT  
		Size: 2.3 MB (2291024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca52e135e6f23cb3baea6e4edcf06875ec9d36b4a6a92f9ffdcd3ff8b8d32c05`  
		Last Modified: Thu, 07 Nov 2024 03:49:50 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.6414; amd64

```console
$ docker pull caddy@sha256:ce832d201acce034f73a7ad2cbad0880d458590d4b5ca98ed6d40eac1e6c8fc7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007430843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff50f71fafc8b4c437882f7b8677c389e29861b9f22c42f77eebabccb492f89`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 07 Nov 2024 02:58:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 07 Nov 2024 02:58:54 GMT
ENV GIT_VERSION=2.23.0
# Thu, 07 Nov 2024 02:58:55 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 07 Nov 2024 02:58:55 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 07 Nov 2024 02:58:56 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 07 Nov 2024 03:00:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 07 Nov 2024 03:00:19 GMT
ENV GOPATH=C:\go
# Thu, 07 Nov 2024 03:00:27 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 07 Nov 2024 03:00:28 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 03:02:21 GMT
RUN $url = 'https://dl.google.com/go/go1.23.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '81968b563642096b8a7521171e2be6e77ff6f44032f7493b7bdec9d33f44f31d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 07 Nov 2024 03:02:22 GMT
WORKDIR C:\go
# Thu, 07 Nov 2024 03:48:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 07 Nov 2024 03:48:37 GMT
ENV XCADDY_VERSION=v0.4.4
# Thu, 07 Nov 2024 03:48:38 GMT
ENV CADDY_VERSION=v2.8.4
# Thu, 07 Nov 2024 03:48:39 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 07 Nov 2024 03:49:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 07 Nov 2024 03:49:06 GMT
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
	-	`sha256:79479da7f7f1735d60cfc8070cf1b84dafacb2b3b3a98d9b1e934fbf97c9d9d4`  
		Last Modified: Thu, 07 Nov 2024 03:02:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e2590be1c3a65810977148270d41363883d20129d18f0ac0a1bbc321a37ed2`  
		Last Modified: Thu, 07 Nov 2024 03:02:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5fe598872a38f4e7557ee214d9d84db27fa9ab46458a9389d4bb9811959c6e`  
		Last Modified: Thu, 07 Nov 2024 03:02:28 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c9fc16abe34ef1c4af9f860e5a4d3614fe43a9c6d38af8ac2935ae63558565`  
		Last Modified: Thu, 07 Nov 2024 03:02:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551592e795ab2ca258e604f27ab5800321f70c90e25997624c283c7f05f47d21`  
		Last Modified: Thu, 07 Nov 2024 03:02:28 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae937cb9fb3f265d1d53fb7e61448a93a401d3edbe26a43af6b01974fb66f57a`  
		Last Modified: Thu, 07 Nov 2024 03:02:30 GMT  
		Size: 25.6 MB (25595147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8b73da8fdfe2bf9f94fe8c8149a86339e362a4789438b69aa3035dff6a12be`  
		Last Modified: Thu, 07 Nov 2024 03:02:26 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88ad30f34542f7c26f450f093601c118e4d1ecc49c780dc507a5f76a77014e8`  
		Last Modified: Thu, 07 Nov 2024 03:02:26 GMT  
		Size: 347.9 KB (347897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23f40948b9cc828d3e0779fe95176880d3f4240573c131940b69a72d4721d09`  
		Last Modified: Thu, 07 Nov 2024 03:02:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30d5b336ac154c42be9b040555efaaca0efbd9b6a4a6863f61a89d4632bc587`  
		Last Modified: Thu, 07 Nov 2024 03:02:37 GMT  
		Size: 77.3 MB (77339950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4510b45d687fbea6bf5de1579cd007c0e6579622858859701f0d5b45d56f6cf0`  
		Last Modified: Thu, 07 Nov 2024 03:02:26 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230da8fd44360a588d2b4dd0418d2ea5811e71ed9dffa90eae21e07b642f1bbf`  
		Last Modified: Thu, 07 Nov 2024 03:49:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574ca39f523c5b6a42a862a16ffad399162d9a12ea1e8a0cc08e5393ff3350f4`  
		Last Modified: Thu, 07 Nov 2024 03:49:10 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103d0f7006bd524f556e7b29ead5081649b16a747d4eacfb5b5a62790e5686da`  
		Last Modified: Thu, 07 Nov 2024 03:49:10 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501d2af8af1faa11338e7d54975b3cd73a0b0e62b592fe2cb1d161ffe2fe7a3d`  
		Last Modified: Thu, 07 Nov 2024 03:49:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7789106df25539d98743b3b4397858ec3ed250f36e0759b7b52281910a2612aa`  
		Last Modified: Thu, 07 Nov 2024 03:49:11 GMT  
		Size: 2.3 MB (2305578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51d55d7bb91ee81ee86523c249db0fc3f769d25f64eff1d8f10e006e34e346a`  
		Last Modified: Thu, 07 Nov 2024 03:49:10 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

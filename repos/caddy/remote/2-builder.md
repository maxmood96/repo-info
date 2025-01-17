## `caddy:2-builder`

```console
$ docker pull caddy@sha256:c83833bde861051d91fed3a194a187e39d9eee02c49acee864c22a64aab87e40
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
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:81b92e3a7498763e2f9bf94ac105e551715337bcbcadaa88f86cba605dd01bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85742961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d03d1ba2d293b10b1de701ca3060e89824bd98c3fc2d1f02b97457065cc81d6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.5
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd66d6ee63439a725825bd4d37f1932a31cc334250a8795de8da2d2d080aeaff`  
		Last Modified: Thu, 16 Jan 2025 22:06:02 GMT  
		Size: 294.4 KB (294390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d5e94dedf03123c13c33c9f461a159dffbfd2152083ecf3c4c39c215e73fba`  
		Last Modified: Thu, 16 Jan 2025 22:06:01 GMT  
		Size: 74.0 MB (74045677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d6cda956fc255ea19a86ccb4a179437431ee948c21cbcaacaaee7a51051e0e`  
		Last Modified: Thu, 16 Jan 2025 22:06:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baacec42f07cf3a575ba2bd53eb9f3a37641cd16504afad5e5a4ee3f0cce0634`  
		Last Modified: Thu, 16 Jan 2025 22:07:45 GMT  
		Size: 5.9 MB (5941005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae4091c76aba3ede8fa985626d4b5365fdf0db42c72a73e0522ec469c140714`  
		Last Modified: Thu, 16 Jan 2025 22:07:45 GMT  
		Size: 1.8 MB (1835038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9655ed7f934bedd73893e1aaf2a61c89cfae18db11341b2ee1aa0765c033ec`  
		Last Modified: Thu, 16 Jan 2025 22:07:44 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:098e76fb1b0621f6270cb69e6f2b27da4df4c765344e5c2b3026e6d22e80f9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 KB (313625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8639cc561b3a2d5fbc27c70165051d7289b53bf390727e8cfab5659d6f320f`

```dockerfile
```

-	Layers:
	-	`sha256:d32207d07f83d1a936477e57489c695d09b41d0669475b587632a5e0f7fb21e0`  
		Last Modified: Thu, 16 Jan 2025 22:07:44 GMT  
		Size: 293.5 KB (293523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef047e6ee1466d0fe2669fbaf4dd8a365ea9e398c3b4206793e98ee538a8b09`  
		Last Modified: Thu, 16 Jan 2025 22:07:44 GMT  
		Size: 20.1 KB (20102 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:53b33642ae67374f89f6951d01104a93dcbd88875484b4e74fd691b284844130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83476851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f599f910bea96b6431fabc2070207dcafb478b92f648ba13acb73724038c8dc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.5
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
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69a70656b186536acaa70853744917e9a0b358e5475d451816ac52af6b864bc`  
		Last Modified: Wed, 08 Jan 2025 21:57:17 GMT  
		Size: 295.8 KB (295828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40eea1e2711989cd934fafed2bad6150c1d5f7a6e606fa1c01c32b7223ec7d8`  
		Last Modified: Thu, 16 Jan 2025 22:07:51 GMT  
		Size: 72.2 MB (72193876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b032ae94ac39af81a1ecfaf55c897fedbc5b8cad8f6ce23171241acf705f733c`  
		Last Modified: Thu, 16 Jan 2025 22:08:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67da6ba668a45d3838d91ac4e065f305f7ece75a2c8b6f7a41986cd12d6b43e5`  
		Last Modified: Thu, 16 Jan 2025 22:46:30 GMT  
		Size: 5.9 MB (5884784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a15a4202fbf6c1ce9f201a03f7676d1d4b3c38a863ec8157b8dfc0f90010328`  
		Last Modified: Thu, 16 Jan 2025 22:46:30 GMT  
		Size: 1.7 MB (1730293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3ee89079eb617eeb2f6d91b9f128b931ea761b5b612931f10287db98050848`  
		Last Modified: Thu, 16 Jan 2025 22:46:29 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:0f6438cdf111abfa9b619dc216b2c9da56a6b8feaf9dbeff27b53e6eaab52ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ed998d19ac10571cf5d75ef21e60abd0f820bb4b4efb3369cf732684f1df68`

```dockerfile
```

-	Layers:
	-	`sha256:947dcb7480dd1fee87d3e97015b9b4d70d05a1cb71b2de0c9780396da147e8c1`  
		Last Modified: Thu, 16 Jan 2025 22:46:29 GMT  
		Size: 20.0 KB (20009 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d1157ff5ecc27c87f15baa4ccee3696fd11a0372c394b2f1f629f85a2c5eb03a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82677656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e76ded0375174ac55838e401856e3fdfea3aa92cc2ee40c118082f1c1ba11f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.5
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
		Last Modified: Wed, 08 Jan 2025 17:34:15 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bf03070cac649166aa1b87cea610615d91250eff95c905990cea3c1d510e67`  
		Last Modified: Wed, 08 Jan 2025 22:34:16 GMT  
		Size: 294.8 KB (294759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71181da0f46bebe3348744084ada18c7bb3fc1a115b2faa229669f2846f8a617`  
		Last Modified: Thu, 16 Jan 2025 22:10:17 GMT  
		Size: 72.2 MB (72193920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8bc543d95cb030f065e8d4e1924017af15123649eb283dcbaa694ce2ff7596`  
		Last Modified: Thu, 16 Jan 2025 22:12:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804493e90f3d91c4be5c10094abb28bf4efb37f7717e59ce694bcefe92781b66`  
		Last Modified: Thu, 16 Jan 2025 22:47:17 GMT  
		Size: 5.4 MB (5368601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f136b4c68a37acaf3d0b940543a6e9e57265d9a327c5e2132edb8801c02cf692`  
		Last Modified: Thu, 16 Jan 2025 22:47:17 GMT  
		Size: 1.7 MB (1724270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2d0795fa9c86f83a610db057aaf855d0d9f5eafb9afd9054fc73e5374ace93`  
		Last Modified: Thu, 16 Jan 2025 22:47:16 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:49fd65b7dc9f38f4a500e30584da735c27e7d27d7ba17b030ad52f531e940966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 KB (316640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46c121ab2d3c9104fec2882cd99fbbf99d368d4a56b49e8f5b31acf1ee506da`

```dockerfile
```

-	Layers:
	-	`sha256:44f78aae386910cf24d3c4918060cfdd893d37369fd4562a6d87f9035cd02002`  
		Last Modified: Thu, 16 Jan 2025 22:47:16 GMT  
		Size: 296.4 KB (296416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b99d0ddf1ab9b29997511ce199060554e6dfc62cc953a4b89e75ee9ca7071c5e`  
		Last Modified: Thu, 16 Jan 2025 22:47:16 GMT  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm64 variant v8

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
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07219bb1974a1749c2d7ad8e3c5020b1a9e55023216926da79ccd2a39b4eef`  
		Last Modified: Wed, 08 Jan 2025 22:40:18 GMT  
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

### `caddy:2-builder` - unknown; unknown

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

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:3471edaada2805fac7e919b004249dbd8f8bb8caf40094bac17ab2d2c4140112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82669170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1412b15649c5ea564abbca424faf16a346faa42ea3f9d0650003ecf7fd989a49`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.5
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
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536d34381fd9ad3cee58f53559c0874fc783fd9067870f324d9d4e8f092a0015`  
		Last Modified: Wed, 08 Jan 2025 21:50:14 GMT  
		Size: 297.9 KB (297894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37aa28c75acc922ecf6560fbabf0d9a7a340adc5cae50338cee3c28a1906cbf5`  
		Last Modified: Thu, 16 Jan 2025 22:10:08 GMT  
		Size: 70.8 MB (70838159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468f66bc815864adfd28f75f555dc32454e94f250541d3eef11d1c338d9c153a`  
		Last Modified: Thu, 16 Jan 2025 22:11:25 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e57e1504b97d7db399985cc735569a99674a2b0795f1b3ea26120d6eb816ae`  
		Last Modified: Thu, 16 Jan 2025 23:07:36 GMT  
		Size: 6.3 MB (6262519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b702d135232c2a2b48cfe667c7bfc789172eee99480db3a4e964dd880509919`  
		Last Modified: Thu, 16 Jan 2025 23:07:36 GMT  
		Size: 1.7 MB (1695601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872b5b2537d2312e59dc38a68ad9defc2e2a1272811a94112f0c3b8b27c3cc87`  
		Last Modified: Thu, 16 Jan 2025 23:07:36 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:e27de7ab7264012e6360a9061f93c5f0ed4cdae2af35c3d8e9bff9bac61fe7cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 KB (311839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7efce8fb238a3074152003e3f37bd2bcbdfe6ad6f8accae60d7864432804ee`

```dockerfile
```

-	Layers:
	-	`sha256:3fc4967d3cfebcb2e40a1e6aa93c5cb5223647e3fc56b63ecbb72aa5e3484150`  
		Last Modified: Thu, 16 Jan 2025 23:07:36 GMT  
		Size: 291.7 KB (291666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a59cc36ab26ffe2aae5f58a2524ac6309a9da27989c7a860d2e2d6e55385892`  
		Last Modified: Thu, 16 Jan 2025 23:07:35 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; riscv64

```console
$ docker pull caddy@sha256:cd64bf804be831a6f7ef695fce6144333b3cb9065075efeac7c49f9201cc2061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82770971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04038c8e6b06dedb8144202dd41aa3e54dd7db48a925fe5236c8853dc43b57a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.5
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
		Last Modified: Wed, 08 Jan 2025 17:49:41 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816c3897a63cf7689a7beab4c1f1af77b6f15050c01df55852c40f878936f63b`  
		Last Modified: Fri, 10 Jan 2025 17:00:34 GMT  
		Size: 295.4 KB (295445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9becc12d50f03eb54a28832963ed08e4345ac23e0b0333a0b4fcd21f803f32a`  
		Last Modified: Thu, 16 Jan 2025 22:19:50 GMT  
		Size: 71.2 MB (71235469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50070af0fa7df453d6770a2d0966ec7ea12ecd682e98699a383c0c072f2adf90`  
		Last Modified: Thu, 16 Jan 2025 22:22:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1520ac0992c174797b93919a453780e9859319f8e1ce77bf9a6e6a9d58a5c597`  
		Last Modified: Thu, 16 Jan 2025 22:48:39 GMT  
		Size: 6.2 MB (6155893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0007d6790780fcc946aab406dd5ed904c37484b1b225591cc2a22c2395b363`  
		Last Modified: Thu, 16 Jan 2025 22:48:39 GMT  
		Size: 1.7 MB (1711647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab45816bc60791a135eb0949007ee454e81966cfb5598064acedad9fb5c377e6`  
		Last Modified: Thu, 16 Jan 2025 22:48:38 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:4d4dfeb2ced3b5f05cf1a7093dbea071fcbdf7fc0468cf4803b8b6f047934ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 KB (311835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a71d268f8c512b1e0e4d1f930022461fe7c8d69bc36b33af2529f93b06122b`

```dockerfile
```

-	Layers:
	-	`sha256:23764420d144d63968d8611fb6c0587d14bb72710c82b1c8ee7f3788eb1ccaba`  
		Last Modified: Thu, 16 Jan 2025 22:48:38 GMT  
		Size: 291.7 KB (291662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b39edf90c736bf15ae3dfcc8d97fbf75538c8f40c9c40a8d2a69c604531a6bd3`  
		Last Modified: Thu, 16 Jan 2025 22:48:38 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:6c8b545713f1ed9635206b9d7d3f6edf29c13beb7ed00e678df92118c63a81c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84687573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b4466a09ee40681f5afa694762eab9ad2a393125bc443d0f4afa07f5263bdc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV GOLANG_VERSION=1.23.5
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
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27beb3ecfc66a05c4717a47324657a7da44cd7a01b554efb4ced3c7c613a567`  
		Last Modified: Wed, 08 Jan 2025 22:26:47 GMT  
		Size: 295.7 KB (295699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b567a3d856120b002d262f7c532f30adaa977477b055fda3e7047c19dfbefeb`  
		Last Modified: Thu, 16 Jan 2025 22:11:06 GMT  
		Size: 73.0 MB (72954684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4ad89383bd4ec340d6a2b82b4b5b7c338409021cd87f47871b0af971fa0fa0`  
		Last Modified: Thu, 16 Jan 2025 22:15:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62982304b5c6dc06a7abe1131b2451d082413cc84a9db0541bc4370dc48438c`  
		Last Modified: Thu, 16 Jan 2025 22:46:34 GMT  
		Size: 6.2 MB (6201869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570e35aefdaa0cd4ecb2d244b3e2fb7172fd50fa4e4a1549569eb0531325798f`  
		Last Modified: Thu, 16 Jan 2025 22:46:34 GMT  
		Size: 1.8 MB (1771407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605341ddf46a0c9fd9a61765edb30d1cc881314e4cd189541b3d32aeafb8375b`  
		Last Modified: Thu, 16 Jan 2025 22:46:33 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:6fa1bea1aa39b21361eee52e37208552ea46d4485756ecd2de9030863c52a252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 KB (311675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f289b363c14088b7f166e52ab0b2e619d978890e55440b7c3077f1c4cd840d4`

```dockerfile
```

-	Layers:
	-	`sha256:994a9c91d2bb2d6182e7c64e191486b54277f05c32be320a415a5dbd77af753f`  
		Last Modified: Thu, 16 Jan 2025 22:46:33 GMT  
		Size: 291.6 KB (291572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c8e68440ae68b86f428ec917b688fad43e56a1608575155eb9efe3506415d6d`  
		Last Modified: Thu, 16 Jan 2025 22:46:33 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.20348.3091; amd64

```console
$ docker pull caddy@sha256:5ed5a8ea10c4c0eca8cd00bd80664f853168f7d4f8a78c7363f54974776e0687
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2367801585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20857015c220c9e2dabbd6f93cb91a1e88d590b57672505586fbf317a0a18112`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 16 Jan 2025 22:15:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Jan 2025 22:15:56 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Jan 2025 22:15:57 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Jan 2025 22:15:57 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Jan 2025 22:15:58 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Jan 2025 22:16:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Jan 2025 22:16:17 GMT
ENV GOPATH=C:\go
# Thu, 16 Jan 2025 22:16:23 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Jan 2025 22:16:24 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 22:17:29 GMT
RUN $url = 'https://dl.google.com/go/go1.23.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '96d74945d7daeeb98a7978d0cf099321d7eb821b45f5c510373d545162d39c20'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 16 Jan 2025 22:17:30 GMT
WORKDIR C:\go
# Thu, 16 Jan 2025 22:58:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Jan 2025 22:58:18 GMT
ENV XCADDY_VERSION=v0.4.4
# Thu, 16 Jan 2025 22:58:19 GMT
ENV CADDY_VERSION=v2.9.1
# Thu, 16 Jan 2025 22:58:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 16 Jan 2025 22:58:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 16 Jan 2025 22:58:33 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d952af1573dbf1b2bed7298024560d0ceb679fff1b2adead8ff2c9554978fbbf`  
		Last Modified: Thu, 16 Jan 2025 22:17:35 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beacac7ab0e918a32c154b60cecdbebbafa259562869f30a90fd0c2f2067b265`  
		Last Modified: Thu, 16 Jan 2025 22:17:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca58064e70276dabf7a373c6f99d04970185879db38bf32d6eda3f659980d81b`  
		Last Modified: Thu, 16 Jan 2025 22:17:34 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd97f668c77dc722cfced02171b360e91a282a550c35e49be3c2e4a9cc11df39`  
		Last Modified: Thu, 16 Jan 2025 22:17:34 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7a7ed3c2824a96a570d679663719a80a3ffb1af841fabbdae661b9c20f5367`  
		Last Modified: Thu, 16 Jan 2025 22:17:34 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690bc9744cb7be357d7b7f69ebc130a4f30b5f3838ba3169e9d46bc9eebb58ef`  
		Last Modified: Thu, 16 Jan 2025 22:17:37 GMT  
		Size: 25.4 MB (25429053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee1e135349fdef766615331b5d2f2536fa0d3d36282e4c72bef80b5327bd2da`  
		Last Modified: Thu, 16 Jan 2025 22:17:33 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10beedcebb1ca2f4868c69ce86c9d1ee7253d250807127b226a6e6d43dd1a9e`  
		Last Modified: Thu, 16 Jan 2025 22:17:33 GMT  
		Size: 328.5 KB (328524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568d04f76f5a2b2110154d676da2d22ba6ff9c71b60dacfed5aa16ca6a4bce60`  
		Last Modified: Thu, 16 Jan 2025 22:17:33 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8119b88dddd1f34e1956279be61a0e1ba90a691a9421046fdb018ffe5592d8`  
		Last Modified: Thu, 16 Jan 2025 22:17:45 GMT  
		Size: 77.3 MB (77339262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736e4ec03e6e7efdc5f00bd9f6e556535015bfa4d81be4960c00fd67a4fbc581`  
		Last Modified: Thu, 16 Jan 2025 22:17:33 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f5becd4b5385bd16545e585bf914ecfa22873d7073e05c08436f0025dd4d5c`  
		Last Modified: Thu, 16 Jan 2025 22:58:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbaa982f98f00159af544b6cc71a0985a5feefd08bea7a562959fe08d93588ff`  
		Last Modified: Thu, 16 Jan 2025 22:58:35 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205b0f5f8da38e46340913b110ccab4f286d35b6a914e0e7cfe7588a46bad77d`  
		Last Modified: Thu, 16 Jan 2025 22:58:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa4d8f81ba83eec540f29a72d1f8811aad96822b7918f64159242ee5a8df17a`  
		Last Modified: Thu, 16 Jan 2025 22:58:35 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8683ae659c69036662d3e64f39c0dbfc28f4a69b00984648fe39e84617d18a32`  
		Last Modified: Thu, 16 Jan 2025 22:58:36 GMT  
		Size: 2.3 MB (2302680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ccefbdc911dfabfed8eeb999c636c4955b2d7c8565fa1b89e416f3fd432d50`  
		Last Modified: Thu, 16 Jan 2025 22:58:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.6775; amd64

```console
$ docker pull caddy@sha256:b4142324eb368e1cf76f6d3f84590f1ea8dd6cd1ab89e606e0f18c2bc810ddee
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227759598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9d1257abdab90ba941d6a9671edcac2c969c0dacd517dedf527b63e99ab7bc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 16 Jan 2025 22:13:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Jan 2025 22:13:40 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Jan 2025 22:13:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Jan 2025 22:13:41 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Jan 2025 22:13:42 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Jan 2025 22:14:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Jan 2025 22:14:36 GMT
ENV GOPATH=C:\go
# Thu, 16 Jan 2025 22:14:43 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Jan 2025 22:14:43 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 22:16:02 GMT
RUN $url = 'https://dl.google.com/go/go1.23.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '96d74945d7daeeb98a7978d0cf099321d7eb821b45f5c510373d545162d39c20'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 16 Jan 2025 22:16:04 GMT
WORKDIR C:\go
# Thu, 16 Jan 2025 23:14:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Jan 2025 23:14:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Thu, 16 Jan 2025 23:14:49 GMT
ENV CADDY_VERSION=v2.9.1
# Thu, 16 Jan 2025 23:14:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 16 Jan 2025 23:15:30 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 16 Jan 2025 23:15:31 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295c396480feacb07ad654aaed23c8c3445a13945981d9f5e82bf337c0fe5b32`  
		Last Modified: Thu, 16 Jan 2025 22:16:08 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c43fcf0c935727e3c30224d50f1620eebcc831b394f74fc283bf79f923a6644`  
		Last Modified: Thu, 16 Jan 2025 22:16:08 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a8b819603e004d5837b58511174a475712220b88e973ab125125ce8d894351`  
		Last Modified: Thu, 16 Jan 2025 22:16:08 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcfebe5fe59f481cdd5793fd54fea5b68a149e88717e92a14aadd3748e291c3`  
		Last Modified: Thu, 16 Jan 2025 22:16:07 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c33fbcfa1a0174182a91e2856bad06dee50170a7217b892cd0a406cede0c6d4`  
		Last Modified: Thu, 16 Jan 2025 22:16:07 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6a918a7464b3da214b4617aee86eea8a394dc778aacd82fb59de9057f87f91`  
		Last Modified: Thu, 16 Jan 2025 22:16:10 GMT  
		Size: 25.4 MB (25432311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d168287de8a4fcd61f7646f7f52f2c70c8fe39a67bb9570cc37228643b39fdb`  
		Last Modified: Thu, 16 Jan 2025 22:16:06 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bacec15598fc7cbb4b1368d06c39d199366c2fd48505d9b7fbe7889e8c79f6f`  
		Last Modified: Thu, 16 Jan 2025 22:16:07 GMT  
		Size: 344.2 KB (344215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53720edb2826bbf57cef354d0276a2fb3ca7011c8cacf12b63d31fcbd5bd5c8f`  
		Last Modified: Thu, 16 Jan 2025 22:16:07 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05418cdcfbcc42015879372547569f2f0b42c437906b4b6fc408bb6713458f30`  
		Last Modified: Thu, 16 Jan 2025 22:16:18 GMT  
		Size: 77.5 MB (77474252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edab9f2ed4207ee8271b81d4209a81191fbf9c54400591b73d854066825958fa`  
		Last Modified: Thu, 16 Jan 2025 22:16:06 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b524fa84357466d361fc275c727af6f96be3c103743a44c4bcffbcb3ae1eafce`  
		Last Modified: Thu, 16 Jan 2025 23:15:36 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d5990c1db792a62bc6b56448324ccb4ec64b6ea4c3e85568a93e19658d089a`  
		Last Modified: Thu, 16 Jan 2025 23:15:34 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e41bc841de880f5e1ec8177abf6dccfcca068f0072b1f349f7cde4bbd2abb2e`  
		Last Modified: Thu, 16 Jan 2025 23:15:34 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b468ba2d957f4ea6cfd5d11b974181b0cb7cdb33d8e5df4300eab1db10e1c9`  
		Last Modified: Thu, 16 Jan 2025 23:15:34 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950d4e1f74f28c01b77c417cfb6fb90f4aa90b7a108cd5f3e130088c55c0cd59`  
		Last Modified: Thu, 16 Jan 2025 23:15:35 GMT  
		Size: 2.3 MB (2279224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfa202af2b46035427ea8c8ada81156b058973e1a56956fca5fe7ed8f325b63`  
		Last Modified: Thu, 16 Jan 2025 23:15:34 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

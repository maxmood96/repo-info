## `caddy:2-builder`

```console
$ docker pull caddy@sha256:4516aa9ba50d7c3a6834dd92f6737f18ed9af5ead7dfdb01ab283cb96ab53ebe
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

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:83d6ff64a667c4b1a69ecadb9946c5c6b779a8da1cb1318a8796717a819bb599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90787194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf50d03244950e0616f679ea037cbee8e5dcb13b9811335d1e305c8d81464e3b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 16:30:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
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
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdff1cf77cc238c3b8e5663c583e181f4a737027e840204038f02071b9c7faf`  
		Last Modified: Tue, 01 Apr 2025 17:07:31 GMT  
		Size: 294.9 KB (294901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d296901bdc593d88a0813bb00eef0974b68222cba6add046b831c086a1c68c`  
		Last Modified: Tue, 01 Apr 2025 17:07:26 GMT  
		Size: 78.9 MB (78942217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efda6a9ec0ed27775d0887572a23317fed2c90e7dc2dbe7ce0dfebddc8ae41f6`  
		Last Modified: Tue, 01 Apr 2025 17:07:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d2f9ebe73d312f2b756c1e064f32804abdab78546220b5eabc10c9adf4cd3f`  
		Last Modified: Mon, 21 Apr 2025 22:34:53 GMT  
		Size: 6.1 MB (6072204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb3684e44506371a5bde488b7b554590968b415a88f7bb305c40be1325137be`  
		Last Modified: Mon, 21 Apr 2025 22:34:52 GMT  
		Size: 1.8 MB (1835033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab56084637a2b1f840222c17cc74c1231a6494e70a6d2dabc966bb34fdaf8e1`  
		Last Modified: Mon, 21 Apr 2025 22:34:51 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:7641a6b77b25d52be5cb2ada27e70d122aed2425fb631bf7beef4c9d7c79c1ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 KB (313717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b509cae98035d462abfb3478abd28730dd6fe7f3b268cdeb71a5c08eb5da63`

```dockerfile
```

-	Layers:
	-	`sha256:71e551c9ba0c6bb67690a1936aa113ca9706afc91f0bd5cf31837bac68de8796`  
		Last Modified: Mon, 21 Apr 2025 22:34:51 GMT  
		Size: 293.6 KB (293603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:602cd64046087056a772491f34ef777190c7a43b90ea4a4110b2ac3e123f1b19`  
		Last Modified: Mon, 21 Apr 2025 22:34:51 GMT  
		Size: 20.1 KB (20114 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:b6387615315b78f2064c32c418abb1bc35c24f22180d5462313842073790b911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88486954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c995256ce32b777b50f58076a4fcabce77022c1471aa8bd2590fa2e046b78cc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 16:30:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
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
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:09:20 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f7a72b848df6c57152561340e794d310a35691d8f3a552ab9db9fd598f168e`  
		Last Modified: Tue, 01 Apr 2025 17:07:08 GMT  
		Size: 77.1 MB (77100796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826258469c5a81a15e8bcf63f5e25a9e65fd6b35f331f66374ae306e61b8a0e5`  
		Last Modified: Tue, 01 Apr 2025 17:07:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09dd18af85543bedde634f071fb50f2bedc89e22face3c9926a37790ee12cf0a`  
		Last Modified: Mon, 21 Apr 2025 23:05:46 GMT  
		Size: 6.0 MB (5994292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de297fba50d21c5272e477e8386ac5427629f439e9c830fb8c5c604ce936e0f`  
		Last Modified: Mon, 21 Apr 2025 23:05:45 GMT  
		Size: 1.7 MB (1730292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b059a48b19187cd28e101b86e5eee8ce37e5ad9930d249f404d2eb0e382e307f`  
		Last Modified: Mon, 21 Apr 2025 23:05:45 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:ee33ced43297c53bc6b8ea21b1035f6c88ff081c2ecfa8c56d133bf1f1eea998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5335b4255fc6ac19c0bcdb42fa4c0a4bed4ecf4be186ab1939d43b79d4a3f58`

```dockerfile
```

-	Layers:
	-	`sha256:7deaf22240a421ac183eda77fc863eacdba5e2c4b64ffc52aa728ff1996c8c4c`  
		Last Modified: Mon, 21 Apr 2025 23:05:45 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:23a4af5bb5caec4f6d2d489673f88c1aba93f36dd500fdb339a2d02668dc37bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87688989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f79f4a0a63db1c0e61e488a80c0278451bd455e07efb386daca2114b8f230f5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 16:30:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
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
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77833ee7d3adeaa883db3f960686c769232a931d3442cfcc8bb6a4790098520`  
		Last Modified: Fri, 14 Feb 2025 21:47:46 GMT  
		Size: 295.2 KB (295199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9003e8a4d55742a1a2128c3dabddda68ec2c585f52d2aac5eaee8bd68089640`  
		Last Modified: Tue, 01 Apr 2025 17:07:37 GMT  
		Size: 77.1 MB (77101211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604386f0e0ec73dea2f63b76b965ec9784ab4cd60bc8bf8fd481a1bfc4b272f1`  
		Last Modified: Tue, 01 Apr 2025 17:09:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f080e0999db29a748a66704f61eb1044335e87942d5438f4b853563d5146df7`  
		Last Modified: Mon, 21 Apr 2025 23:43:16 GMT  
		Size: 5.5 MB (5469600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35fd245dc60ae5d6e39d2c965644a6df1700d9952ddb86bf13c9e527e7247be`  
		Last Modified: Mon, 21 Apr 2025 23:43:16 GMT  
		Size: 1.7 MB (1724265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e264a8dce294500e2490124bb788424501c8993d4551f2f9627280eb7a857bc9`  
		Last Modified: Mon, 21 Apr 2025 23:43:16 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:50ab1fb310cdee31456c50b6bb6db8642061ca59190cc6ec34c10aad474e827c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.7 KB (316684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000e8ccfa4c39e28c3e6ce546eab59ca525ec773e88d35c9af5ca5e200855e02`

```dockerfile
```

-	Layers:
	-	`sha256:39d43ee73d6b6a7da44bde9e3a98a2491899c9c669a95b7917e790eeac7a5b13`  
		Last Modified: Mon, 21 Apr 2025 23:43:16 GMT  
		Size: 296.4 KB (296448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64921663613ebe84262cad7469a97f741ac7ddafad97d553bcf63fc7145f1140`  
		Last Modified: Mon, 21 Apr 2025 23:43:15 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:d4d85b008f4a11b61ba8adc823d669e2105d2a9c52005b9f55941e541700b38c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87311485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bc430e70975f3406a92212a4966d327a6af0f45c7129a844bf5e495b4c8289`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 16:30:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
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
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e33b27c9b76515e1154a131a67e2f0fe88ba9e9bc48a1a704c790a0561e068`  
		Last Modified: Mon, 24 Mar 2025 21:29:27 GMT  
		Size: 297.9 KB (297871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a002eda2038f0953467f843586445333b2af3e827e57b15849040931f2903fb4`  
		Last Modified: Tue, 01 Apr 2025 17:07:27 GMT  
		Size: 75.2 MB (75200208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc8c2e8d985822b3b6ac5ae3a8c130feb27393e9e165e3e1cebea69d9e30f32`  
		Last Modified: Tue, 01 Apr 2025 17:08:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fc8c0bfcd99d76d69395e87c229d70d492e493820ee09e9d1b105da31546b7`  
		Last Modified: Mon, 21 Apr 2025 23:35:50 GMT  
		Size: 6.1 MB (6118355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005b4da9a5f90495df185171dc2a7d44205e368d3a947c0f2cf9479159392d93`  
		Last Modified: Mon, 21 Apr 2025 23:35:50 GMT  
		Size: 1.7 MB (1701430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c8db658bdeefb9725383da66ea36dea62564a8f7424efe3d78416b21c3fc85`  
		Last Modified: Mon, 21 Apr 2025 23:35:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:62632978e931bb4fcfa6a0b2914d99081c0e1bc62ded5aa83e98ecdc3d0000f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 KB (313989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6c9ba3c0bc8153983cd4f731735430f25236241d474cd8092028a71172c65b`

```dockerfile
```

-	Layers:
	-	`sha256:caf743574a407d836048c88cbf4ba791450a2418292a490758a42cf628273efd`  
		Last Modified: Mon, 21 Apr 2025 23:35:50 GMT  
		Size: 293.7 KB (293707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a685f5c0307443cc585ea35703fa4d7090ce3bd650d35c62f6194cb99e9b57e`  
		Last Modified: Mon, 21 Apr 2025 23:35:50 GMT  
		Size: 20.3 KB (20282 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:33cf1d9660c7fd9eb096bfe701cd8c5348ad76f9b1d734c7669da77284f338a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87468043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06be4edf44ac7147d724a2838b2c5b950e9e8388ae3cb87bb52f6d24b062c0ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 16:30:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
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
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27442ea8b4dc6fdf584c0b30a8e1943de4b659fd7ec220499d43ff5c7d4c1c8`  
		Last Modified: Mon, 24 Mar 2025 21:48:27 GMT  
		Size: 298.3 KB (298274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee95abad5ecea3c593f42714d65b6f62167cc9a1a7a50eaad85a7db940a3e7f3`  
		Last Modified: Tue, 01 Apr 2025 17:08:51 GMT  
		Size: 75.5 MB (75501286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc8a8fae114e6d1cabbae8d39a9b447bc2cbb6a893c766a392e70bf7d3a831e`  
		Last Modified: Tue, 01 Apr 2025 17:09:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221d9b6bcddb45fa372e608c547c7f16c93436f546917d54500a2aa20dd0f788`  
		Last Modified: Mon, 21 Apr 2025 23:49:53 GMT  
		Size: 6.4 MB (6397956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98a6696c5d89c20e8779e833f283f416125c66df9fc4364baa12bdf7b9433cb`  
		Last Modified: Mon, 21 Apr 2025 23:49:53 GMT  
		Size: 1.7 MB (1695591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12aed678d711b832e221ecf04bee39bf94e7c7535cbfa889295f31372444657`  
		Last Modified: Mon, 21 Apr 2025 23:49:52 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:1699e658e2702afacf635ee4ded565981bfb78c0f7d9c0925a02d8457ffadd4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 KB (311930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060df1122717a8fa7607718859b37f5933b3bc539792a75b859299e6030ecba5`

```dockerfile
```

-	Layers:
	-	`sha256:1f85366979d5df23cc957c3c140d29674ecb794d427e161df6a4628e8f25f4a0`  
		Last Modified: Mon, 21 Apr 2025 23:49:53 GMT  
		Size: 291.7 KB (291746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d93e6aceadddf1119c891b63166705002953184c0a4f78940c28dc115706b99`  
		Last Modified: Mon, 21 Apr 2025 23:49:52 GMT  
		Size: 20.2 KB (20184 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; riscv64

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

### `caddy:2-builder` - unknown; unknown

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

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:30952f189278c249fe5069f755b2079c7b7c92951c159c9e366ef70f3171e863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89645737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02398e31b6d83a645a9d9920b29e1679e967fdae9adf26162ff29ec6fbe75a99`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 16:30:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
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
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be80be2c55902add1c4b1f14066b1b4da724beaa2e355b53f8dd45b4887d9b9c`  
		Last Modified: Mon, 24 Mar 2025 21:26:52 GMT  
		Size: 296.2 KB (296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64586fca58b7ef9b98d81252f6468cd1afe274720313716be72d0e12ecde9791`  
		Last Modified: Tue, 01 Apr 2025 17:08:27 GMT  
		Size: 77.7 MB (77744430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e049e56da0eb21854c2d4985311d05149a497ab6647152db8a4110d93e6b2468`  
		Last Modified: Tue, 01 Apr 2025 17:09:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b73f489b3ae4d224f92a76c2bbea892543e2e7b3ca72e0f9b8adff2e33b845d`  
		Last Modified: Mon, 21 Apr 2025 23:15:36 GMT  
		Size: 6.4 MB (6365558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b557a5b2d1889af09d02d87997a3f0498996f74e827065868b5d28d0200ebe`  
		Last Modified: Mon, 21 Apr 2025 23:15:36 GMT  
		Size: 1.8 MB (1771408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467e67bcf04433c6136cc39ae0e7b7508fa6d1939f0734b876969bf782df6b73`  
		Last Modified: Mon, 21 Apr 2025 23:15:36 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:48287469d6c3d82a864284f94f98a270f561018b886e3cd8f3afa352050cec10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 KB (311767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66b3ecccb24061ad73b54159e21c1d04ed2df06e2c6039ddaeab037c00eb4b6`

```dockerfile
```

-	Layers:
	-	`sha256:a0614b59f15126c2573ca350dc90eec4ef8f22ec470a42933c40da158e610da2`  
		Last Modified: Mon, 21 Apr 2025 23:15:36 GMT  
		Size: 291.7 KB (291652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fbb72388af7a41647b6cb238f92d3daecd1068220618e5bdb9434948e105d4f`  
		Last Modified: Mon, 21 Apr 2025 23:15:36 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.20348.3566; amd64

```console
$ docker pull caddy@sha256:cdfd2c3b7d5a9fb4bb76172262ae151d73be5ea8afe61d08e448320960a46ba5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2404806762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d8241fa6b619c51c83acc4bc9795350101a92fe0dec318f08e98c5c7cc93da`
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
# Mon, 21 Apr 2025 22:42:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 21 Apr 2025 22:42:59 GMT
ENV XCADDY_VERSION=v0.4.4
# Mon, 21 Apr 2025 22:43:00 GMT
ENV CADDY_VERSION=v2.10.0
# Mon, 21 Apr 2025 22:43:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 21 Apr 2025 22:43:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 21 Apr 2025 22:43:15 GMT
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
	-	`sha256:3e62b6f9ab04c3a1b1dee2f5edbff887849c6a97eb6801b6d84221f75808c0dd`  
		Last Modified: Mon, 21 Apr 2025 22:43:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6efc43750ca7f4af4ddddbaa007f609c1ee541b0f612017c80c1abb89c60a7`  
		Last Modified: Mon, 21 Apr 2025 22:43:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aec376748e8ee776931a1bb5e13298acff17bff113f4c724b9fd894870d0ed9`  
		Last Modified: Mon, 21 Apr 2025 22:43:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b09a1066dc01b0485d929093cd66c8db502aa48e6e841362af5336d24a61306`  
		Last Modified: Mon, 21 Apr 2025 22:43:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16ad861b8d30ea2a8ad1d5bb875a94493d8d9edbbe71fde406360b69063e55e`  
		Last Modified: Mon, 21 Apr 2025 22:43:20 GMT  
		Size: 2.3 MB (2305347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016fcce398f29d63026b088a474a74ff4f01e06efd1ccc6a7be5b3cd34163df9`  
		Last Modified: Mon, 21 Apr 2025 22:43:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.7249; amd64

```console
$ docker pull caddy@sha256:a7ea1ef1309f1b533604f9e47fd8f46e9273b672a5b9143519518acb12aa4d62
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296732556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42bdf67b4ebde66b6747e9843e7fe550b06f0fe3c24c1c4254757b566d9ad6a2`
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
# Mon, 21 Apr 2025 22:44:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 21 Apr 2025 22:44:13 GMT
ENV XCADDY_VERSION=v0.4.4
# Mon, 21 Apr 2025 22:44:14 GMT
ENV CADDY_VERSION=v2.10.0
# Mon, 21 Apr 2025 22:44:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 21 Apr 2025 22:45:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 21 Apr 2025 22:45:03 GMT
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
	-	`sha256:233522a12b15b4ae3cc5ca6ed917af92ea0cdc99907df28370189264a45118ad`  
		Last Modified: Mon, 21 Apr 2025 22:45:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5210a01ed7decd576dbc999955e6a08f084c4ab3d9286c47c391cb32f4bfde28`  
		Last Modified: Mon, 21 Apr 2025 22:45:06 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f018eddc2a100b41a8ee2c91defbcea643392feacc69e79c3be0ed377eac3b01`  
		Last Modified: Mon, 21 Apr 2025 22:45:06 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b3f012693f4b9779457c37af2b07e24dbe97d1fa6d8f47a55d17c93eca2cca`  
		Last Modified: Mon, 21 Apr 2025 22:45:06 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d43af34798a541997ea8b16ad84b185ae0f3f847ba4abff7dc62c1efd86dcd5`  
		Last Modified: Mon, 21 Apr 2025 22:45:06 GMT  
		Size: 2.3 MB (2289949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27535f88ba33f080f88664920c0b5216b85d8acccfa68614c8430d654d4ead02`  
		Last Modified: Mon, 21 Apr 2025 22:45:06 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

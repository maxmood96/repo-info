## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:efedb356080be1cd5584baa80df964cbe3d85af049bbfee7775d9659e1809360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:683161d33599ee7740b25d8c0466e82bfd94e491c63bef744eda38919853dd62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76973779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e7c249761d733da653482a2b5259eaae803dee4354bc3562e48a601315e6ff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Tue, 05 Mar 2024 19:42:13 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 19:42:13 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 19:42:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 19:42:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 19:42:15 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e791cb90c3d0bf08a988f13b405c9947c74b5bc31c7c939197a7175f6c7f0e`  
		Last Modified: Sat, 27 Jan 2024 01:36:33 GMT  
		Size: 284.7 KB (284690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3da9c61ef062502252a549dbc1f90925a8d7b6ef0644ffbfaea77be8b6f058`  
		Last Modified: Tue, 05 Mar 2024 19:25:57 GMT  
		Size: 67.0 MB (67010725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1741a7c0e9ce85801257b76332c08a3abdf5069bf46b0e764a32219d92189dc5`  
		Last Modified: Tue, 05 Mar 2024 19:25:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc853d0ab24d3fe195e8492db2866ec9d01681c218bdff73afb081fa97cb002`  
		Last Modified: Tue, 05 Mar 2024 19:42:32 GMT  
		Size: 5.0 MB (4972975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea68e3f24bc6efb27b70b8c1870bf11b4a5fad53eb40e8ce77817c21586972d`  
		Last Modified: Tue, 05 Mar 2024 19:42:31 GMT  
		Size: 1.3 MB (1302236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ecce85dc39a9d244f2c3b1e0e89e72279e6d9f6b154afad2171642b11c137b`  
		Last Modified: Tue, 05 Mar 2024 19:42:31 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ece7f11958f255486a5be355c9180900873b391449f4258706b535d5177b40b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75407413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22234bb36f9348628e9caea0dac041e47e0df57676643cb27bc893380168cbd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Tue, 05 Mar 2024 23:00:43 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 23:00:43 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 23:00:44 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 23:00:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 23:00:44 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 23:00:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 23:00:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 23:00:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6033bb349d654a4ba7602191ed0372313ceca193751253005ad66a23d4dcb0ec`  
		Last Modified: Sat, 27 Jan 2024 09:20:38 GMT  
		Size: 284.9 KB (284872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bccd7f5c5a4f0abc0a23393d9a04f353b767b809c6ac950caaa731dd3768c8eb`  
		Last Modified: Tue, 05 Mar 2024 20:11:40 GMT  
		Size: 65.8 MB (65767479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33a4721f193119280f7dfc5baed0ce6a2d3b2eb94e31901d986ea54166c41ea`  
		Last Modified: Tue, 05 Mar 2024 20:11:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28b5e7a7f3d8467fb26f35d8b70ae0853d39fb4103058a0dc47dd62be3256d7`  
		Last Modified: Tue, 05 Mar 2024 23:01:07 GMT  
		Size: 5.0 MB (4958742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276c5f8fd9c641c6036e92487a700ea1b6cc811b8ac1578ff0f94803223f6e0d`  
		Last Modified: Tue, 05 Mar 2024 23:01:07 GMT  
		Size: 1.2 MB (1248648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db777cbc747c60df3dc9c90c42c55125b12f7c65e05a6b1ab52ec8de565848a9`  
		Last Modified: Tue, 05 Mar 2024 23:01:06 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:156f7188ad9f04c359241e42567a3cee24477cb1885639d634da45c042cc297e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2a4fac0ed075caa114df1d0fd560d017af28251032ec5015a49c0702fe3d48`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Tue, 05 Mar 2024 20:48:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:48:44 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:48:45 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:48:45 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:48:45 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:48:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:48:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:48:48 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf835181e2f4c73f7de0fe69c219658c3feddb5ba4e6850bc5b5af9555c08d1`  
		Last Modified: Sat, 27 Jan 2024 00:41:32 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f0c2683a0605dfb4fff92a0c34044c42624cbc47515f2262026e23ffa28b15`  
		Last Modified: Tue, 05 Mar 2024 20:01:25 GMT  
		Size: 65.8 MB (65767445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1570cef4f4f43311a29ff4036cc73329f8fe806fb19c51f3413b3073bfc70634`  
		Last Modified: Tue, 05 Mar 2024 20:01:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2640aa4bbda58460e9e4fd9b0a0969303c9a30ba9b9ff6424d9349f7c0ffbcd`  
		Last Modified: Tue, 05 Mar 2024 20:49:09 GMT  
		Size: 4.5 MB (4514657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5f06f998d08d9a0ca561581720f1399d9e1c6f64b4637370acd8eddc90418e`  
		Last Modified: Tue, 05 Mar 2024 20:49:08 GMT  
		Size: 1.2 MB (1246081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f58b57eb0adfeabad656db0f59a85f8373054397123d068fe68452663713a9f`  
		Last Modified: Tue, 05 Mar 2024 20:49:08 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b7d23a0e6f86ad993855c69a14f149837072ce99399627ee74d95e4705784d14
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73993792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0728d6faf4e6faebb8c082c95826cc671a39f43e1cd9ef0cfcd909a42435c9bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Tue, 05 Mar 2024 20:00:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:00:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:00:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:00:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:00:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e59bef827dc10d9c33cdf4762faf3f2987df2a0296378e2349ec6d5bc6a37f4`  
		Last Modified: Sat, 27 Jan 2024 05:33:17 GMT  
		Size: 286.3 KB (286302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a91045fa00056cff12698db93bed8fe188f9895b74e96e29b6a9f6a6e047937`  
		Last Modified: Tue, 05 Mar 2024 19:44:44 GMT  
		Size: 64.1 MB (64111148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f155e563ada2bb78e99decac187a48adcf9db3cd56e543bc0694674ef8a234`  
		Last Modified: Tue, 05 Mar 2024 19:44:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f627d8e1519d50a70f854d0342a035bd62a8cedf0d7a61351f7ac191accf21`  
		Last Modified: Tue, 05 Mar 2024 20:00:40 GMT  
		Size: 5.1 MB (5063926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cf96a60cd43a372ff273debacac6160f6842de4adc5e79eef190c8a791eecc`  
		Last Modified: Tue, 05 Mar 2024 20:00:39 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113a17d73127a40aa417b169724fea00b3b34ed479e7d3fb2b656325c7d131a8`  
		Last Modified: Tue, 05 Mar 2024 20:00:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:3321233002d79314df5692f81246bbcc2d0c9ba268c61792fd6269b1e64e6ff9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74219843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b9b8fd2c1e8bd5b65bfbd17b919aabf00faf29ce73a1702c8a2610afe5427c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Tue, 05 Mar 2024 19:40:39 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 19:40:40 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 19:40:40 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 19:40:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 19:40:41 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 19:40:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 19:40:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 19:40:44 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f92ca388ce06d6dddf0b5ad5ca0d5b82049994f1ad4da72bb5e48c5783dc009`  
		Last Modified: Sat, 27 Jan 2024 01:13:46 GMT  
		Size: 286.7 KB (286665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1323fc82438c3a0b40c7bcf18c7b4808edcec55b91135df534741787df9cbc`  
		Last Modified: Tue, 05 Mar 2024 19:25:03 GMT  
		Size: 64.1 MB (64126907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8630ef56928609490ea4cc1460f549f49e84ed6ff4f6bb7ffb5c3fa5e53f3027`  
		Last Modified: Tue, 05 Mar 2024 19:24:51 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c2f5a4fa35cf481005994eef4a926ba3b1cecb6ee2747d8080460c88a7fa6c`  
		Last Modified: Tue, 05 Mar 2024 19:41:02 GMT  
		Size: 5.3 MB (5270995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cba91d041ae77cf958d8509d23d6f741eec735e9bf9a24d489d0b8842db30c9`  
		Last Modified: Tue, 05 Mar 2024 19:41:01 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de13da806adead3ab5a4380c923e80ebddfc28b7b94d6e6f43b6cbb920acd85`  
		Last Modified: Tue, 05 Mar 2024 19:41:01 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:179342439e20a0f8308f5b3c8f51063386fb33fb38d9eda738dfd1d4b398280c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76101838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4eddf19e318b73f4fa90802285b549c08b6b015cfc8f36a11adbbf9c593fc2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Tue, 05 Mar 2024 20:58:12 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:58:12 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:58:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:58:13 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:58:13 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1b6899ff00172fd5c809d57028913a3c5aead2c05d0c3c01b15a5249c4ddec`  
		Last Modified: Sat, 27 Jan 2024 05:46:31 GMT  
		Size: 285.1 KB (285091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192deec459dbc25471d5ce96dbf84de90f9e77914e5074081b4aba0516977050`  
		Last Modified: Tue, 05 Mar 2024 20:12:42 GMT  
		Size: 66.2 MB (66218961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e6d46fb71afdd9825fc4397b4949daac74f5a564377560ed3cb3bb910da97f`  
		Last Modified: Tue, 05 Mar 2024 20:12:31 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad42b5ce4497969e7a2ebbdf9ada284081c50ce1744927873987c8075ed117fa`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 5.1 MB (5117256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea105a4685d829ffde13e2d0e06f02ec7f1e1381059eae15941a5aeb36d5f7a7`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1423e2dcf9499ee1179b946513f3194740bf64ee1f24d0a7688bde92f8773874`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

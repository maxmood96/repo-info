## `caddy:2-builder`

```console
$ docker pull caddy@sha256:75f5dafdf92bbf2c4217c169e4d2349c407df5a52df8cadcedd6e722d1bbe36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `caddy:2-builder` - linux; amd64

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

### `caddy:2-builder` - linux; arm variant v6

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

### `caddy:2-builder` - linux; arm variant v7

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

### `caddy:2-builder` - linux; arm64 variant v8

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

### `caddy:2-builder` - linux; ppc64le

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

### `caddy:2-builder` - linux; s390x

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

### `caddy:2-builder` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:deed166abe77b412a506924346166c58e03f6e35fb2836e7af244be01925eddf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054342050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7b95fb04081aaf80026e1bb52d4a79df79ea5aac969382123b16607318419f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:46:04 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:46:05 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:46:06 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:46:07 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:46:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:46:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:47:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:01:45 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:04:07 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:04:09 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:40:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:40:13 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:40:14 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:40:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:40:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:40:40 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0a2d972d6c007b69f2c3ea41c1fe5fad6b189bfe40efacdcaf910b884fb6bb`  
		Last Modified: Wed, 13 Mar 2024 02:13:35 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f3068df504cd61566fc5e038c996322e35f58e08e0c6ef6ce589b11de4eb93`  
		Last Modified: Wed, 13 Mar 2024 02:13:34 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98750f7d798b8a0b5199088d4860bce5d51320b2fc07440f211ec692f4bf63b4`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e43d1ea980f98746869d1942fc459ed402f307d4de5c435e325d2c9d534e99`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fc4a2ae5d19f3b766991bfec5347bd5192c19ede11e7dfbf8b7d698fc1323d`  
		Last Modified: Wed, 13 Mar 2024 02:13:38 GMT  
		Size: 25.6 MB (25551948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251908e7b1f95da24e9f4ec7c727a2662105696c9de2925ab36938572cfb9f79`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2927b1ac917c6e3261034f1c0cbb347c73f26593e997c505dfd04da18f966c1a`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 273.7 KB (273727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5d297a0f5c09416c27b06ff859cb837506ffabdf0faa0cb5112e0a34839aab`  
		Last Modified: Wed, 13 Mar 2024 02:15:44 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1412d17e78321071b9d6a4dbb609e6a24c2e829a90ed9ca7e20a72ede74d04`  
		Last Modified: Wed, 13 Mar 2024 02:16:03 GMT  
		Size: 69.4 MB (69363257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619eb2756fc98681ecf9e1220a72f64f2e3f3fe9e72edd3a6021ad0249b9b2a5`  
		Last Modified: Wed, 13 Mar 2024 02:15:44 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf19d565f6ad05c073e69610b1e850eaf1a6aa6806195ea601c4a47303140d27`  
		Last Modified: Wed, 13 Mar 2024 02:42:22 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279cafbdd3019482f630ef1d502ea930d8ee1cfd8f9977bb52059c87ddff7a55`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e9d1117318fed479ece2fe1c6f9b896efcca03021ea368d722153aca1f8bc9`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d106feccb912e361adb23c8a586aad6b6c8493698e3893f4b1a2cd40bdd03cb4`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e766bc3c556143c937c2d95209a8d6370902ee4f31471f2a35c4d7045d361af6`  
		Last Modified: Wed, 13 Mar 2024 02:42:20 GMT  
		Size: 1.7 MB (1676188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39236cd34ad31ef892f22ac798c76cb384eb17ff72d5881539cbee398708be72`  
		Last Modified: Wed, 13 Mar 2024 02:42:20 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:53d965e8f604060a1c65cdf2a722300b8ff2f7a36494b6c0ba0c315fc7ffd2c2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221957582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daee73c43fffad7bf7cfb8399d58db63aaa5f6727affb62b8d370b9760df81f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:49:48 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:49:49 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:49:50 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:49:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:51:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:51:29 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:52:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:04:28 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:07:38 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:07:39 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:38:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:38:30 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:38:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:38:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:39:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:39:54 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc39f00be83bc8d2b0e0f2123fce0278f495e47f8a969bf03ec57df5f98cbda`  
		Last Modified: Wed, 13 Mar 2024 02:14:08 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f8b9e441646ef17118a0d394fa50244ef70c9e053c5b7d33e648796c8df90e`  
		Last Modified: Wed, 13 Mar 2024 02:14:07 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8759cd20778bf436a14e59cb31806b28212fcd510d8de32d44e49a9f39656f3d`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d99a22ebabf5f80d07ad166a24eace1c2fa31cef2566a179bfec0d6407513e`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfdb963b4125b258828e1fbac783c993a6845ad94973fad173f5dd25be3c34b`  
		Last Modified: Wed, 13 Mar 2024 02:14:12 GMT  
		Size: 25.5 MB (25540238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae89960ac90d33a751006d43faf1cbd1309b448658a447bb19dddabdbee17a9`  
		Last Modified: Wed, 13 Mar 2024 02:14:04 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff0bdcb61a7230b8b00d6e08d739c64fc0342dc675ed99fe6d35885cf1aa369`  
		Last Modified: Wed, 13 Mar 2024 02:14:05 GMT  
		Size: 272.6 KB (272572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c052d4b938689fbc1637386d1e61efa391787bd8128ee6d093464bad09b0231`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e82772a8bffddc9f4a46c65cfa48f47938d84feb3730231762158c98014e47a`  
		Last Modified: Wed, 13 Mar 2024 02:16:31 GMT  
		Size: 69.4 MB (69350702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbffcc4012ecf27a404cc40eb63c43a880ad5104a82ee619fd0669acb2b5a710`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fcd0eeed9adb7d9bf391df7f194150cb8ee56a63bc679cf147a14185381c3b`  
		Last Modified: Wed, 13 Mar 2024 02:42:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d74d351932d9ba6c92c9398e69d6736df75938a6ba3b7f1055206a1ed80b48`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db51f1e77d8641618afadb6f8c1ad073c4f72bb79099a00b0cabcbc8f5579248`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43620705f408ca0a7894137080f7947cc45d10badb0c7668ae1d46464494001b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdaa0771d9c8b704195f821c3a9c23a5d9ff5e7e9b29335b835ce237f9d4dd50`  
		Last Modified: Wed, 13 Mar 2024 02:42:03 GMT  
		Size: 1.7 MB (1676257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010496734b493d0bc1b1a73566306e98777144ff64c5c886cf84de3af4fd971b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

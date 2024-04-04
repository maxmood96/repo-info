## `caddy:2-builder`

```console
$ docker pull caddy@sha256:337a28e320ef730ff4b2ef87ddf4702710240940a30f236059259925de47bba2
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
$ docker pull caddy@sha256:1b98f3fd892c1605c157cc3a049bded9d706ffd51d9a753e18ab07510d0d9e2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76971330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e800cc7a9c84d26699931116102217b923104964e820bba39098ea1b544f5e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:41:31 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:41:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:41:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:41:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:41:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7862e08f4a3ed79ba32d02613b9c596dea827892605f23ebad6c4860ecfd1a4d`  
		Last Modified: Sat, 16 Mar 2024 08:03:57 GMT  
		Size: 284.7 KB (284695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df492c9dc93cdba9fed81e4389415b485127c9cb37c86b79b3f142702574a5a`  
		Last Modified: Wed, 03 Apr 2024 17:02:10 GMT  
		Size: 67.0 MB (67008211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7629e6793208752706519ae9acfbe8b7ad6bdd634d81a69dbcfed6930884369c`  
		Last Modified: Wed, 03 Apr 2024 17:02:00 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3317a43f465a5aebb363d397b3672606d18a5e247747ffd2684c1d0f74de0c6`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 5.0 MB (4973037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f015372e3250fa052df943aed69b26ce6d683b45328456139b9ab7ea453fdf`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 1.3 MB (1302233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6212759f5b367912c99a78b73d4277c50b224f19fe85ce2a3a9fbc94ed16be`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a925804363a91c2468468c2ab1c1de2c770fe02812a21b1bdc1e9d8d65a5241b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75406613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acc712a703abf58b426c0681a4f724105efc534e813fca8d7e1769f2df5ebfe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 20:22:32 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 20:22:32 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 20:22:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 20:22:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 20:22:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18595ac3d5791e4d7e7dbcffcbf63e97e29974bd7191f7779889293f06709605`  
		Last Modified: Sat, 16 Mar 2024 01:27:12 GMT  
		Size: 284.9 KB (284879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72bd013141c752021b5b309e9868c02341e86fc25f37a89ccec1311ad14b2fd`  
		Last Modified: Wed, 03 Apr 2024 17:01:10 GMT  
		Size: 65.8 MB (65766638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea289abae69e0933683886761310d242609c9941f5964366d9fb5bae890969`  
		Last Modified: Wed, 03 Apr 2024 17:00:57 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c466f5631c550594140cdcbad1c11c2549f51578de8dbf2181ab68d36e3860`  
		Last Modified: Wed, 03 Apr 2024 20:22:50 GMT  
		Size: 5.0 MB (4958760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c206e1c4695681bec33b38b6cb25bc40da76dd756937418fda1f1841f07a6b`  
		Last Modified: Wed, 03 Apr 2024 20:22:49 GMT  
		Size: 1.2 MB (1248664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1617709771cc71f393f3e93e93292a3024d9ec67376e73101934b6f2d2a14c`  
		Last Modified: Wed, 03 Apr 2024 20:22:48 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:a31ab129389e3b3ac05560de4c52b0c6eada751beddf9acac3e8f35b9ef8c890
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64ab8f668dda6c40c8b5f34a24568989c2d59aa3868bca24a60d427bae87453`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:19:54 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:19:54 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:19:55 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:19:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:19:56 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:19:59 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03de95814623b83a4328b4db2e23b14214f57c18389a27379988469d9b6bbccc`  
		Last Modified: Sat, 16 Mar 2024 00:51:49 GMT  
		Size: 284.1 KB (284082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef743b67b508d786f3e8c07ac7dca5aae6ea84a61aa62040b9488dcb2a61415`  
		Last Modified: Wed, 03 Apr 2024 17:04:20 GMT  
		Size: 65.8 MB (65766731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebfed2c271f130a93577b99cfaa3d4478590defaf383477153c1651a8e99a9`  
		Last Modified: Wed, 03 Apr 2024 17:04:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b09688e6219de2aeb2517b1fa78a0827e04df6051fd6bffe0eaec255bef97a`  
		Last Modified: Wed, 03 Apr 2024 17:20:22 GMT  
		Size: 4.5 MB (4514632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c14897ae7beed5a75683641e846e60b36c4ee61bdc37b9f469f54e1f4cf3fa`  
		Last Modified: Wed, 03 Apr 2024 17:20:21 GMT  
		Size: 1.2 MB (1246085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b24f949532888fed8d67d1c3b6a71965df7120dca4ae0931796d19ed24f9eb0`  
		Last Modified: Wed, 03 Apr 2024 17:20:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9abc7c94f1374507e4fb3b81219f95268cd31f587383aa65ed562e3632f31ad3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73990594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53bd0a763baf79c779ab2df43b12f525bb58428beda8002ee1d684d7d6b97bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:17:39 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:17:39 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:17:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:17:41 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:17:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c4102457739613c6fcb205a5a8e7dbc8383d57dade0a4502b1bca7b100a4d`  
		Last Modified: Sat, 16 Mar 2024 02:38:03 GMT  
		Size: 286.3 KB (286314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6de4b400683f0c2362cd880beab320a91316cc24f9f1ecbf576711db2be1bcd`  
		Last Modified: Wed, 03 Apr 2024 17:02:05 GMT  
		Size: 64.1 MB (64107935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cb2a7552d02e7b8e08bf29d0ad4ff98976de8d65f841ce2d42311feeefde4c`  
		Last Modified: Wed, 03 Apr 2024 17:00:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47f7261edc01476f5c0b0525e8f13cc9657f43606014d847afa574f072909ac`  
		Last Modified: Wed, 03 Apr 2024 17:17:57 GMT  
		Size: 5.1 MB (5063925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84aaf63ffe94c0dc9204c45df4cc7bb295e68028c5dc918d66c4b6a947a90783`  
		Last Modified: Wed, 03 Apr 2024 17:17:56 GMT  
		Size: 1.2 MB (1198447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c212b8dc9ff8e7943ac82424077aa3c9fa166ec6c2b15e1391120730607c83`  
		Last Modified: Wed, 03 Apr 2024 17:17:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:3a698c4439f62c22b347f40670cca759481b4368e86535ff7c8c90e26974a7b9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74222636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4c6495ce537716c6f5656c4b703e10cdc4908c76fee2d10efcde9ba1428bf2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:21:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:21:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:22:00 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:22:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:22:00 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:22:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:22:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:22:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e315e4c0ee7596e0eb7cc17d622c433e9fc4ef254b722e11e6794265328ea583`  
		Last Modified: Sat, 16 Mar 2024 00:32:12 GMT  
		Size: 286.7 KB (286670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc9420a97e4b56d60b6f6e43e57c1a0d5699839dfc799b4251d0499da4fdd88`  
		Last Modified: Wed, 03 Apr 2024 17:06:19 GMT  
		Size: 64.1 MB (64129697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a95c9b8692b60f2d2834350493299931b57072a905e77764ab2a07c7be44b7`  
		Last Modified: Wed, 03 Apr 2024 17:06:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c79cba53bb3aec5e78f2aa326cb786811cad80519236a541f8cafc627e297c`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 5.3 MB (5270996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69323be82d9f1dfdc2a178ab91b6388fa9c05bec31f9f1df95e1e1429ca4a3c7`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f305185cfe4c977fae095795eb511d3544f159d8622f4d8fc7b172edd3643`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:71bc6c7a27089f10bb8fb6a701c2d6e2e1b1b097cc301c0d7e0537f1a97b550d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76102402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06da9a536513bc321f389c5c495c8f107c86b098d3db35fd0730f8a8de9d99d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 18:44:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 18:44:20 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 18:44:20 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 18:44:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 18:44:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 18:44:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 18:44:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 18:44:26 GMT
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
	-	`sha256:a9c0594d97c8cf4a046ce171a13f9a84a6bbb0b217f0694c3c2bd4d4e5b04be4`  
		Last Modified: Wed, 03 Apr 2024 17:30:50 GMT  
		Size: 66.2 MB (66219505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd26c37806dce963a4a27ef2b2db557bd73ac7834ed03be5caee0fb00f7fd04`  
		Last Modified: Wed, 03 Apr 2024 17:30:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab984370b902d79aea4a3b6f6836818ad0c6ea617bb48b1d51510bdafc407394`  
		Last Modified: Wed, 03 Apr 2024 18:46:09 GMT  
		Size: 5.1 MB (5117274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddb778247a116db89ac5778d4d4f54943f6cb5761fa79984dc7b1e230388caf`  
		Last Modified: Wed, 03 Apr 2024 18:46:08 GMT  
		Size: 1.3 MB (1262392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fa7a5ae42d88199c81c0faeb5c2cbdc5d23284280bf6fc75f5392621db3480`  
		Last Modified: Wed, 03 Apr 2024 18:46:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:217de50aa2da8ce751fcf86af874352c567fd2890a7af933d96b71b9cd686ab7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054329601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5fca8b12e88afae211f90e44879d0eff32c2faddcf2f98239f84ff801975ab`
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
# Wed, 03 Apr 2024 17:11:09 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 17:13:34 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:13:36 GMT
WORKDIR C:\go
# Wed, 03 Apr 2024 17:46:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Apr 2024 17:46:15 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:46:16 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:46:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:46:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Apr 2024 17:46:41 GMT
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
	-	`sha256:bba8f7ecb6aa5358813c663a8a821d1558f9fc231d3724d61963281d33c2e29d`  
		Last Modified: Wed, 03 Apr 2024 17:26:14 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645f42306e40e7cd27968b015e4ffd34928e43341ed0891a002a7038a0e92aad`  
		Last Modified: Wed, 03 Apr 2024 17:26:34 GMT  
		Size: 69.4 MB (69360591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b143f0a2277fa1d64dd7e4b237cdd6dee7b9588492e8f25e1f9a6f851ea84e3b`  
		Last Modified: Wed, 03 Apr 2024 17:26:14 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1547026bfff2e6197321109a9232c8d890758f34e98389383329811ca6d0cc2a`  
		Last Modified: Wed, 03 Apr 2024 17:47:34 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07757497ec2b71297a55c100a7253a5180839f418c47af25edff072294bba64`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3f141b6cc8b1b397eaca67bc234dff3e69a2a848385cd18a6f71f0e672d18c`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0988228d5bf035f168b753ec12db6dd4984f8758ac9c0c1ff3d92dabaa4ea452`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebf104fa97c496c43790a481b80954576c09380b483c4bef5fea5a1d017cab4`  
		Last Modified: Wed, 03 Apr 2024 17:47:33 GMT  
		Size: 1.7 MB (1666185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c7907d9819b9165f71f85f596a1a535a4857f3af02b44444b224cf8d588e38`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:8d209986e9cd0835be85e8f65905a45f09bbcf92d15c8d09fc474cfd921f042b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221960398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb43e28d9922862c630fec0d1ba1aa98980080ac6eee5431d9d200d7d373590`
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
# Wed, 03 Apr 2024 17:13:54 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 17:17:31 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:17:33 GMT
WORKDIR C:\go
# Wed, 03 Apr 2024 17:44:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Apr 2024 17:44:32 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:44:32 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:44:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:45:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Apr 2024 17:45:58 GMT
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
	-	`sha256:584a26f47e4b040924987f5714e3904994464b2082794beebf1b84e0a4a711b3`  
		Last Modified: Wed, 03 Apr 2024 17:26:44 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e106baac3b372ef5b64f477236dcdd8c76bd7692c1d1a9a8c61596376a474f5e`  
		Last Modified: Wed, 03 Apr 2024 17:27:04 GMT  
		Size: 69.4 MB (69363419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e891eced875ee145e4fc5c147c8f84ff77215d4e5a1a86cff047c2697b417650`  
		Last Modified: Wed, 03 Apr 2024 17:26:44 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb621e6ec00bf92d79e37d3cb91e9ce4d633edce6c6618cbeeb19e40e482988`  
		Last Modified: Wed, 03 Apr 2024 17:47:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b816cd0d77c5e8e4f9e8e648b807ffb2e79e861b17670d9841ae2bf48852d2ba`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d0826717e8d6b364230bdd7ed7dd491d35a95be7323df3a90a68ded19a6ff5`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c00c4e7e6cf5e71b9dabdc9e7e221f5ce9450755ca1ad90c402e483f199ae8`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a2f091b6ab0aebf8b669a0f95d00a5b934be2ed7563f5bbf55986abe9d2efe`  
		Last Modified: Wed, 03 Apr 2024 17:47:17 GMT  
		Size: 1.7 MB (1666239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427e8173580c10665cb7ac17da9df0fdf012ced3b7aeb9262a86eced50bbb7c8`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

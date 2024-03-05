## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:87635260bd514d4be319457066f9dcc73ad763bdda83bc7edeb6e8db9f961374
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
$ docker pull caddy@sha256:89493aa84b348e455d5d5d3dd0f050644d7e3a9400cdc1a09d07545d95e85fd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75415278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921e0138a2eb31837973f479ce9117ffd13a871b9e3c1e3332f0689b85ec2e5d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 07:28:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 07:28:02 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 07:28:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 07:28:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 07:28:03 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 07:28:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 07:28:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 07:28:04 GMT
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
	-	`sha256:fa53b2f66831ea2a6a71d6469b90663284dc2a4ce3cb48320dd55896f9cd8d84`  
		Last Modified: Tue, 06 Feb 2024 23:32:01 GMT  
		Size: 65.8 MB (65767452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6d1ac72f2f91d206a9c3fa198f2e45b1f18fcfd8da385ab8c5e3288262790`  
		Last Modified: Tue, 06 Feb 2024 23:31:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6fbc6c4773d705c6048f1330050fc6200a9ae262d156ab7492ac01fc483010`  
		Last Modified: Wed, 07 Feb 2024 07:28:17 GMT  
		Size: 5.0 MB (4966629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdc84144fd70dfac8f705109ec0a92dc10a7dfc50838c6af32b442b918fcc6`  
		Last Modified: Wed, 07 Feb 2024 07:28:17 GMT  
		Size: 1.2 MB (1248656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78e6ef661fee931920aa3236f1af661d851378c52b31aa87ffc8558da5e48a5`  
		Last Modified: Wed, 07 Feb 2024 07:28:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ff0b3bb63b15b33debf9aea993bd84f4b246b7c7d4484db77832556ef074ca51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c07a4329692996a3988717e0eba3652501b15f09abc9597e4ad3b87250cb63d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 02:48:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 02:48:33 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 02:48:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 02:48:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 02:48:34 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 02:48:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 02:48:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 02:48:38 GMT
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
	-	`sha256:7113cf104f60011eb6444102f15ef72cdd45fcb4c9caf77828b5fbc38dab492e`  
		Last Modified: Wed, 07 Feb 2024 02:23:31 GMT  
		Size: 65.8 MB (65767658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a6e0f5354f83f214823ce1d03ea8a7eab56425405c4ca69940f2f3dde97a80`  
		Last Modified: Wed, 07 Feb 2024 02:23:15 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f390b29274db9c266f41d8708269d5dda362068060acd663c445ce335597d742`  
		Last Modified: Wed, 07 Feb 2024 02:49:00 GMT  
		Size: 4.5 MB (4514221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399e806721f760b662ba77d6b0d28a03a0c91cfb57e9d60a85f9016392605507`  
		Last Modified: Wed, 07 Feb 2024 02:48:59 GMT  
		Size: 1.2 MB (1246089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5225c4821fb8eb5d3c9024e1b8b00504669f1ced491c2e93b97b5400673970c2`  
		Last Modified: Wed, 07 Feb 2024 02:48:59 GMT  
		Size: 405.0 B  
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
$ docker pull caddy@sha256:fad88c033e71179f3df4bf1a5b2e9d0d0264bcbaa498b911238fc07787bbace2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76100380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914aa8aec00e9a7014cfcc15953ecea9afcc02ceae16b98a5643c211c018e323`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 03:55:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 03:55:23 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 03:55:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 03:55:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 03:55:24 GMT
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
	-	`sha256:667df4a2c04946a51104abaa6f5ed310f5428e8423a5229c6a93e33a7bfd3afa`  
		Last Modified: Tue, 06 Feb 2024 22:15:10 GMT  
		Size: 66.2 MB (66217776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed37103477a46e4048ca49195fde1e764f57b71cb5abadd05970bee2e2f29cc`  
		Last Modified: Tue, 06 Feb 2024 22:14:59 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d511e031e1b91b289c43c1a2190ee22aa5f38fe22568e3b6e23cdf96db48b`  
		Last Modified: Wed, 07 Feb 2024 03:56:50 GMT  
		Size: 5.1 MB (5116980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255f032cffa62a5bea76ec237a6dfe24caf125994ad6151aed12f4ae30860c02`  
		Last Modified: Wed, 07 Feb 2024 03:56:50 GMT  
		Size: 1.3 MB (1262391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8b53fd06bb1ce493aa5cc33297d87b8edfe9fd834896df28185e9c3f9b8480`  
		Last Modified: Wed, 07 Feb 2024 03:56:49 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

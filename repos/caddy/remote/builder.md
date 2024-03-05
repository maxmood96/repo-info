## `caddy:builder`

```console
$ docker pull caddy@sha256:fbb715163e8d79484b0b40ed1c36035efc029153bfd104559bd4ba90a5451ea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `caddy:builder` - linux; amd64

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

### `caddy:builder` - linux; arm variant v6

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

### `caddy:builder` - linux; arm variant v7

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

### `caddy:builder` - linux; arm64 variant v8

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

### `caddy:builder` - linux; ppc64le

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

### `caddy:builder` - linux; s390x

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

### `caddy:builder` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:e924a818b35c77fa77b850501f876fa811c43019e884675210e1232eb23b13a6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007476156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69198d50697c7c62515331afda3b6b548388fe7ecfbec519f7bcb8e8ab8e5155`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:27:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:27:25 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:27:26 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:27:27 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:28:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:28:04 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:28:25 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:27:34 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 19:29:55 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:29:57 GMT
WORKDIR C:\go
# Tue, 05 Mar 2024 20:03:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 20:03:28 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:03:29 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:03:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:03:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 05 Mar 2024 20:03:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac8de2d709384a84400f6f072b2d3d4c4d454ee27f8ec716db4964eabac3f8`  
		Last Modified: Wed, 14 Feb 2024 20:55:46 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70115ee0ce6c09f30645181ec6f80fe9ece4e9b51628fdbaa85ebd4e0ae979e1`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab323644de57af1911793c0a10501a7b21640f8e58484665dc2258f482cb943`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae53fd363daebfb127c2ba7e51543cf93130802d95e194fc71db09c52b9fe10c`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a9a35030c2076331610dfe4c22866525c2b0ac219981d900f1b6178af5241`  
		Last Modified: Wed, 14 Feb 2024 20:55:50 GMT  
		Size: 25.5 MB (25534020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ab59c20a7391d04f68a3dc2b9d6eb4cfd1e7af0ddd33e30d2cd19f13535c0`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a35884f3b4e6aa2080cc34668faeabacc75000ef04e2fe4ec3e76f166d992e4`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 266.0 KB (265989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c81949701f9fd28f5c42cfa101f1e2c2858efdb4032e3c3a221ae64417094d`  
		Last Modified: Tue, 05 Mar 2024 19:41:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07bf58a4a94d97d30abeee1c89ea03f4d6bb5ae58ba58a108ab8c14ce86d04`  
		Last Modified: Tue, 05 Mar 2024 19:42:12 GMT  
		Size: 69.4 MB (69350261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff66f61d5b04d89a7cd43a5718c2738ee8c932ff7976238576fcce4a9205188`  
		Last Modified: Tue, 05 Mar 2024 19:41:52 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fff8f151323c49bef4ab32c69e1b7fb0bc1c38c418bc58f8d552450f83ddb4`  
		Last Modified: Tue, 05 Mar 2024 20:04:48 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad11e6d0d7e8e1cdeb21675479688d12574b1f3aaf78c017dcb3f3f0e461e94`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3bac1fc388577dc02e99cece1f2418b768a6b9131f03ccb3a12b5130d0657c`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2023c4236e1ee6e1e21d75518a4e0b041879053cca3a4d196a736c11ef937885`  
		Last Modified: Tue, 05 Mar 2024 20:04:45 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646022f7531f95a5e75674d8b4716cd2b10acf7080eacbcf1a9146ec3c17a381`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.7 MB (1653517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a594d21bdd61142fc0e9073bca5c902365dcacea37bc8513a5868bccebfd5e5`  
		Last Modified: Tue, 05 Mar 2024 20:04:45 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:63e3bb18f43a20a50a640e33d80c15d6447e5c49eb758ad2ac92dd3c2215e1d9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177356061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bf8c2ce948dfc3bc85a84137d8ed09be2f3b755821c887f151431733f69def`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:31:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:31:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:31:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:31:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:33:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:33:15 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:34:38 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:30:18 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 19:33:39 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:33:40 GMT
WORKDIR C:\go
# Tue, 05 Mar 2024 20:00:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 20:00:06 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:00:06 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:00:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:03:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 05 Mar 2024 20:03:10 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001ba7ca58e0032ab21885ed5be98699fa0e8693d84ce59492bbdeb45a1f5b89`  
		Last Modified: Wed, 14 Feb 2024 20:57:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964f6547b697b5014d27c4ae5aa9115c1686907b1f2524f8f0de888da7a79bd8`  
		Last Modified: Wed, 14 Feb 2024 20:57:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f83e22effb8739ec3fdcae64612cffac4ee7579638549caf47c70342693285`  
		Last Modified: Wed, 14 Feb 2024 20:57:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce41b07883cf81f89185e0e1b4fc65b39258a3f1aaff0ce01028854071ddecb`  
		Last Modified: Wed, 14 Feb 2024 20:57:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7954912de33be8cc7e1e4ea36180acfc8bb6cc7b7dc043d43d5912cfd171cd3`  
		Last Modified: Wed, 14 Feb 2024 20:57:33 GMT  
		Size: 25.6 MB (25560320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c63eb439e08d84b2f39090a2a87819fe70e5dfe666f3d4c4d3985acfd1364b0`  
		Last Modified: Wed, 14 Feb 2024 20:57:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fef719b5ba36fc0af1638fb03777e938c25331563e1d178a89bae94d428c8fb`  
		Last Modified: Wed, 14 Feb 2024 20:57:27 GMT  
		Size: 285.4 KB (285394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8d167b3e7ee16cfc662a87231b4084716742686d31d5b82e887b234efec2e9`  
		Last Modified: Tue, 05 Mar 2024 19:42:21 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28621adc2c564252debe98669a98b5db5ce45172ce843466e26b8b689b114a`  
		Last Modified: Tue, 05 Mar 2024 19:42:40 GMT  
		Size: 69.4 MB (69364712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c43bdc8404f132a84e8a0f4c69e490b01b908e8633abcfe604de71e205648`  
		Last Modified: Tue, 05 Mar 2024 19:42:21 GMT  
		Size: 1.5 KB (1545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcc239c5226abef94ce51a464e18875c9ff8a1fded12c55a44a3396d065d9a0`  
		Last Modified: Tue, 05 Mar 2024 20:04:31 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92819fb904e989755feedb88fdac313dd0614617cb2124f845e1beb9ef0b7840`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866ca856d15d8b11f3251d0e1e751bce5ccd3d04170d016b81a7e721ee811cff`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478c6e5efb5198c62dae853963d276055bc2ce33ae70aca26cba13a16359a054`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806deb5a287a2c1cfa951ac44704c97b32856f31e9d0012590d79e5b068279f1`  
		Last Modified: Tue, 05 Mar 2024 20:04:30 GMT  
		Size: 1.7 MB (1678307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bb868ab3b0ea5f9e471cb10db42cf456ce7dfe4ecb2ec8769a9c97c105483e`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:77da1a24d1e545997915238c0d1c6b314b61bd0bf3da01df7938a174cb19eab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:f5820e4f785ad77eda1e6265eec746804a4d3d9dec085c8846f606a30f36ae72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76972179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38305f810227323a4f7fc8231d958e2abd8596cd054d351b935fadd3a4046f4a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Wed, 07 Feb 2024 00:38:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 00:38:28 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 00:38:28 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 00:38:28 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 00:38:28 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 00:38:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 00:38:30 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 00:38:30 GMT
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
	-	`sha256:d18ba8e8dd02491f11cea93df354c71628a2360674a625c205e213ef6fd82127`  
		Last Modified: Tue, 06 Feb 2024 23:56:58 GMT  
		Size: 67.0 MB (67009643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf023d266d667210cf5767c01f2f4f68e40c297e0bdecf73799744ddac1026`  
		Last Modified: Tue, 06 Feb 2024 23:56:47 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bbab491c1ff9b40f6e8ffcde7f0576e0fcb9aec805080e4cfc3f8a40b9d126`  
		Last Modified: Wed, 07 Feb 2024 00:38:44 GMT  
		Size: 5.0 MB (4972454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c3f34e72a63db2bb935012ecbf4b81d4d73f3bf60143c01083741069365688`  
		Last Modified: Wed, 07 Feb 2024 00:38:44 GMT  
		Size: 1.3 MB (1302238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124c95a679587c86642e7b83ac153d88957deec2a30c808a870ff6731cef0e35`  
		Last Modified: Wed, 07 Feb 2024 00:38:44 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f61b9cec41316565b283ca5a058b2b6dc78fa87098ee59b0b1b043e88f086d88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75415281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7101422a502816b72ebd4a42dddaffe642537ea77f658c239caaa0617495f71e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 23:48:27 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 23:48:27 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 23:48:27 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 23:48:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 23:48:27 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 23:48:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 23:48:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 23:48:29 GMT
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
	-	`sha256:60d05bf663c38e8f217d66a26d5394ab51d1220d3e92c7eff4d0b4a5a5c1321d`  
		Last Modified: Tue, 06 Feb 2024 23:48:43 GMT  
		Size: 5.0 MB (4966637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95afb54e33993779986fea5b1ae437a3a70ae2df1e5d947acc6bbb9f5db1b565`  
		Last Modified: Tue, 06 Feb 2024 23:48:43 GMT  
		Size: 1.2 MB (1248651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed34e0e9c00549ff9bfb7fb40eadcfeae335c11073647378839b35ea0d6b7fa8`  
		Last Modified: Tue, 06 Feb 2024 23:48:43 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

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

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bee0d79c6d83f0f253201d3c21afebe471923903c79a57fc165382018992582b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73998590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43afba92f6c2f26ccd2d5a34a29409424cb5d7437f186994917fd86a2a330c21`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
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
# Wed, 07 Feb 2024 03:27:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 03:27:19 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 03:27:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 03:27:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 03:27:21 GMT
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
	-	`sha256:328d8fad75fb04ebff991b2c11c5988722931b5300239657bc1b4961655df05f`  
		Last Modified: Tue, 06 Feb 2024 20:50:08 GMT  
		Size: 64.1 MB (64109254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62899699addead1db84d09ab10dc0a0cbde16beb64c81cde0f84af2fa9b30f39`  
		Last Modified: Tue, 06 Feb 2024 20:50:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ff1670edc3c20a6a9614ecb3f794095053b0a2bc5c3d8a27ffb6771b4e8de5`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 5.1 MB (5070614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6bfbf28b1c962164432ab027c42dcb68debdd9c90fe50d3fdec0bac01a2a1b`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 1.2 MB (1198449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dec8839aa12d34c5fc6d220df303a7b58562c777e2281fb6b912cabcb3b808`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:ff608ed0346698200d108d948d192f9d9977f35b9ee6dba5dc437eecb95eff13
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74213050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3961610a4cc67151079da941b2fa3b5f9e84fdbadf7ddfc2345914f2e7d34270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
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
# Wed, 07 Feb 2024 02:38:42 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 02:38:43 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 02:38:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 02:38:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 02:38:44 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 02:38:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 02:38:47 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 02:38:48 GMT
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
	-	`sha256:31ef3661c7b713c28d8e0ae3c73dc823022f6a6e8a65c6fd2f00aa13dd6be4e4`  
		Last Modified: Tue, 06 Feb 2024 20:39:21 GMT  
		Size: 64.1 MB (64120440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7f0aa3654740d4016d469bad05baafdfc3be78e2f6ebc6f938501a1f4cd056`  
		Last Modified: Tue, 06 Feb 2024 20:39:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189f1d64ec6387010de82030584f95d2f1cb77480534f720a6c8051e1c053202`  
		Last Modified: Wed, 07 Feb 2024 02:39:06 GMT  
		Size: 5.3 MB (5270668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439fb1dfa6333e4624dc554a68c980b15bda052268ac48be84e477697d3fa5fc`  
		Last Modified: Wed, 07 Feb 2024 02:39:05 GMT  
		Size: 1.2 MB (1186180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b46e2bfe6d57573d777ff909c837b014c894d5f5c65212804d738620cb252e2`  
		Last Modified: Wed, 07 Feb 2024 02:39:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

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

### `caddy:2-builder` - windows version 10.0.20348.2227; amd64

```console
$ docker pull caddy@sha256:4814d63f1ac1d7e2334ff267279eed3b5533e0f94ad926fe9b3f11064e087406
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1997072166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d833851f7e1c400f60d5591428c91912a576258fb5b2fd93a0cdd0b228b07d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:22:59 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:23:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:23:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:23:02 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:23:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:23:36 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:23:55 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Feb 2024 20:15:33 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:17:57 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Feb 2024 20:17:58 GMT
WORKDIR C:\go
# Tue, 06 Feb 2024 21:01:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Feb 2024 21:01:18 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:01:19 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:01:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:01:44 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Feb 2024 21:01:45 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb0a528ee25f289459dfa0d84bac9a14b9127f771882f0b60425ffaab79933`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3069ddb372bc0087899e61a271374e1b4423cfd9056ff2725874a89af15c2a1`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0841fad0c7557916603463fc9615983e0ad786338880d3d99c005dd50ecf3b6`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1ae6fa2010fb779b06f0fc8a74830b01c9a87769fc35818fccdd5b7e7ea45`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4cd94fbe72557ed410a8f0aa0361ffc9ec2b2ecd96dc803b91c5ce0f34d077`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b3e385378ebc3f79f2c065897b323f0b1cfc97f3f8979c4530d0791e3e9523`  
		Last Modified: Thu, 11 Jan 2024 00:01:30 GMT  
		Size: 25.5 MB (25529890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbdf5bbf3fb6a215313abb55339dcee6260ef50d2c50d2b781476d5af12e840`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7fd79e14c60629d3157a4363f602b919ba92aa10209a2e6ac40b7c86a75316`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 261.7 KB (261737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d6abeee495b14ea2e44bb00f28c38212af6d923a1d5c148dd3eb083e1788d2`  
		Last Modified: Tue, 06 Feb 2024 20:38:27 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699b8adf45cf387aabdaea0b829e6bf5dee7a05e7eaf5519d3b0f5fe071e14a`  
		Last Modified: Tue, 06 Feb 2024 20:38:45 GMT  
		Size: 69.4 MB (69373765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60a6e8aaafdd337241c619e2cd664dbfd6052a133b148c86845f227a25ea14`  
		Last Modified: Tue, 06 Feb 2024 20:38:27 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6796689d52835dc674b67907c3e03bb20425e0e76be6963eaeb04e035d2c7f`  
		Last Modified: Tue, 06 Feb 2024 21:02:41 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657c487d0aab792a6141c8f2b5d1ef4564310178c60f883cb8e301cb752930ff`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bcd5a55d300a69a6a7202fda4cdb55a8e4f3645145c962279bc958c9efdf5a`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fc1b6232aab1694132043a6674117073dc98b00635546605582fabd31300`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f7ea8d310ffb3ab0f46fbb75e4a90192f694357210b16fa4867a1c593cf2e`  
		Last Modified: Tue, 06 Feb 2024 21:02:39 GMT  
		Size: 1.7 MB (1675717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f756efa4d252460db4055d7da93b4667f4b1537f46882db730596bac57eb677`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.5329; amd64

```console
$ docker pull caddy@sha256:882f417e3efb3b9a8d1ade5245808ac22c5c1ea57a1352c72b6652b3a3238ecf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2166627810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6206308760870c6bbbd479176af11a35608423c94c08b69c418649ce2d281f3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:26:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:26:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:26:45 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:26:46 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:28:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:28:09 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:29:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Feb 2024 20:18:16 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:21:36 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Feb 2024 20:21:37 GMT
WORKDIR C:\go
# Tue, 06 Feb 2024 20:59:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Feb 2024 20:59:49 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 20:59:50 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 20:59:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:01:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Feb 2024 21:01:01 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8ac948dab7d4d3a44ab44e27a80115467b2f5fba68a58b377fef3e920bc5eb`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a2d0f9e9eca6932479b4446cdad2350fe376cd5102106ac4938d8552073ee1`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3baf188f2343abdd0b6b9307f8adcc91c698473839c28dbba9e3b50117d7df5`  
		Last Modified: Thu, 11 Jan 2024 00:03:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83f321def9731da0b67b8c9c7c573a95237ff9d906d16394dfc3dd845bd806`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3185717e4484ba21a137fb6d471a72ee842364637f999013cbd8b7a633ccfa`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d432d7f01be369829a69831b58f259bc1d30ccb67bc46a16211f95454e2d026b`  
		Last Modified: Thu, 11 Jan 2024 00:03:06 GMT  
		Size: 25.6 MB (25555277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481ab54aaa7ea3f3af1db424c6fda8a4bf6e63fe0bc92e2e319db55c66952d5`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4579730b543c234b271242a1f8b94332944911daa12fe4493f4daad09e6e6a1`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 284.0 KB (284031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57342fc3b749de0a8e32c9f1f9eece3c3855ea5d8b63b70682518058c40ba349`  
		Last Modified: Tue, 06 Feb 2024 20:38:59 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d092fd3744c0081064bac79e4fb322e2f6e9d0d8e744bb837bccd7f9b844e8`  
		Last Modified: Tue, 06 Feb 2024 20:39:17 GMT  
		Size: 69.4 MB (69370513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a8538533cb5606cc3e717f0431791fcd99ca7c1b935f5586f465bbd0c9d457`  
		Last Modified: Tue, 06 Feb 2024 20:38:59 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ba50226998b42d6500ba479c1fbf0f3e588807488f728c91715ac893e69838`  
		Last Modified: Tue, 06 Feb 2024 21:02:24 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74292b50264f2db380dc5a9a8baaa5d229ff8efd2699e40fc6f478a25d59c0d0`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e574cef27624cb2b445968d4f051529c8c02dc6bf599ea131f51164de4939536`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14832cf23b08465f9e60489cda03b116fb6be01de86762232ed2f3b3aa8cf2a4`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e89456cebd7c16015a94dda1edb8a055ef730bc8c289b8eae13b1867371376f`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.7 MB (1677010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874ea9f0878170aeeae3da252653488f0677348bdb3f6cd9a87ccb3d064bde10`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

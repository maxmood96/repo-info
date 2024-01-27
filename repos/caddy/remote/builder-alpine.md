## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:665475e0504fa47bdf257673b6f4384769e72350f8953f232c0f39b88884421b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:09513acee0757eaafeea861313a51d37b907cde693899b4d85bffa691d7eca06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77024166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e2950806b4846bc8384039f8e0ced6b55a43843627c3c7bcb574d00da87e36`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 03:39:23 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 03:39:23 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 03:39:24 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:39:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 03:39:24 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 03:39:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 03:39:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 03:39:25 GMT
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
	-	`sha256:c4b77ba268427b27996c293cddcbb1af065ac97d6f64fff6d3ee0adce318de44`  
		Last Modified: Sat, 27 Jan 2024 01:37:37 GMT  
		Size: 67.1 MB (67061623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5c147192a9317b4f575377244f4c3d96df9c9108d6147e10cd2becfdcfdc75`  
		Last Modified: Sat, 27 Jan 2024 01:37:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426789fa51aac91ce386d0cf62e3c5b4fd91cc19da6cb9449035a1aad2a1cb4b`  
		Last Modified: Sat, 27 Jan 2024 03:39:53 GMT  
		Size: 5.0 MB (4972458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848439cf5d4cf7d00a316abe8d0c04005a28d2e60f11875549cbbeec7db5cafc`  
		Last Modified: Sat, 27 Jan 2024 03:39:53 GMT  
		Size: 1.3 MB (1302243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61744c717cfe93977f876b739f3c692e919bb8cf098d233db8af67c532d77cd`  
		Last Modified: Sat, 27 Jan 2024 03:39:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f7f15d8dc37358732c441ac4c62c2ac4967b16eb93863621dfc5cacf0b9dc1c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75479956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b694cc61283aebb38db78010935fc8281778bc08c35e7816a8c8819d3727a6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 13:22:00 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 13:22:00 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 13:22:00 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 13:22:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 13:22:01 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 13:22:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 13:22:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 13:22:02 GMT
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
	-	`sha256:a31e5472cbeca7cc0b8f9272fbe547db898349f9b598c6b975f2c4efeeb63aee`  
		Last Modified: Sat, 27 Jan 2024 09:21:48 GMT  
		Size: 65.8 MB (65832091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b979a15e6ae0ded8491c78ec0740e6ece1aaaa584d10fdb89131c53427aba66`  
		Last Modified: Sat, 27 Jan 2024 09:21:32 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31abdea622b745b38e9215bf8062f71c377f48b2049bf07a5cd650743c069abb`  
		Last Modified: Sat, 27 Jan 2024 13:22:18 GMT  
		Size: 5.0 MB (4966664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f06e6a7ead4077a0b30ee09128ded6d14cd9bd7f450ef457f559c9e5b59938`  
		Last Modified: Sat, 27 Jan 2024 13:22:18 GMT  
		Size: 1.2 MB (1248661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba060f027200c3446f1acab0c00b2f4a9e8acf8610c46591daa3d8d7434aafd`  
		Last Modified: Sat, 27 Jan 2024 13:22:17 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:24d4c79acefde6b15b06516f4d247f63feb6120e5924662cf93c152a84cf2a3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74778442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a23a424216f39567ebe4688764b059db7a781bf3ed2f644cd91d211d3e972e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 00:44:54 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 00:44:54 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 00:44:54 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:44:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 00:44:55 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 00:44:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 00:44:59 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 00:44:59 GMT
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
	-	`sha256:57d8c4fb3f22d529458327ade3a5db59d1f41b1bec9bf71099c5b2686ab97b2e`  
		Last Modified: Sat, 27 Jan 2024 00:43:07 GMT  
		Size: 65.8 MB (65832077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f01886f7d0804601543454491ce79cb78f0e6912e4ce568efc2de5cdc65069`  
		Last Modified: Sat, 27 Jan 2024 00:42:53 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7d2f28610886c56c618c48751654152eaa7d00fd18dd5a5f13cf21785328eb`  
		Last Modified: Sat, 27 Jan 2024 00:45:36 GMT  
		Size: 4.5 MB (4514196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c10a312255fcdf2e7df4f632021a68b0f5af10c6add4f80ad21c89d8c4aa04e`  
		Last Modified: Sat, 27 Jan 2024 00:45:35 GMT  
		Size: 1.2 MB (1246085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf59f44de4fc0e35b785d09df04bf7e159c5d30fae80cde193981050895aa35d`  
		Last Modified: Sat, 27 Jan 2024 00:45:35 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:aa49c7852aa064f9230be6c2dcfc0d3393c319ec0155cb258265cd577bed63dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74050253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923f4a5af971e80db5eacd7ce79bedc88f20963086773007b5cb0646934641c3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 10:06:06 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 10:06:06 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 10:06:06 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 10:06:06 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 10:06:06 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 10:06:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 10:06:08 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 10:06:08 GMT
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
	-	`sha256:1713aedec2461e4dc3bbe5ac62c3205985f492b47c0b442bc841e5574487d888`  
		Last Modified: Sat, 27 Jan 2024 05:34:12 GMT  
		Size: 64.2 MB (64160929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a7628120291f3f48cf53c449dbd811fea0d0d996b14b6b6dbdc3f1d26dda84`  
		Last Modified: Sat, 27 Jan 2024 05:34:04 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b32e5d33e0c9163bda7520c2322c564efcaa575118a3debb5e7eb90d6df3b51`  
		Last Modified: Sat, 27 Jan 2024 10:06:22 GMT  
		Size: 5.1 MB (5070602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94967d7741b59f8ebbc67c1a4eda9d4d0f9f8149a975b397bded5674be6ecf96`  
		Last Modified: Sat, 27 Jan 2024 10:06:21 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfecb210c68deee816f9d792263232052b34bee27531def56ce27531e142f180`  
		Last Modified: Sat, 27 Jan 2024 10:06:21 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:471a754cf1127792d23f9b080604e646d32f492a163f453f3dbfd3603ae07f25
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74282242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d2388af15b3ee792eecee3d12192838d939990f6fdd5efa36640a08212b713`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 07:23:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 07:23:54 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 07:23:55 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 07:23:56 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 07:23:56 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 07:23:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 07:23:59 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 07:24:00 GMT
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
	-	`sha256:d700c54ec866f695bef0bc415778c8ddb43eadf9261e70a2f637311800aede72`  
		Last Modified: Sat, 27 Jan 2024 01:14:55 GMT  
		Size: 64.2 MB (64189633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ede5bb66dea9cf97d432b8c6f420a24eb74bafa68b07e31be034fdba8333363`  
		Last Modified: Sat, 27 Jan 2024 01:14:44 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628cb7a520a11082a02c2187bbae9ae42adeaf9a423d19143de9fe54e2d4258a`  
		Last Modified: Sat, 27 Jan 2024 07:24:17 GMT  
		Size: 5.3 MB (5270671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5690c3a15774df55279e94527f678d4b2adec3fd88d15ae1322b1507e5d0a5b9`  
		Last Modified: Sat, 27 Jan 2024 07:24:17 GMT  
		Size: 1.2 MB (1186175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8105d8c6b6901cb74658ae0318cbf4b87e527277321bde7e2a4399b2679174f3`  
		Last Modified: Sat, 27 Jan 2024 07:24:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:25c4422b5cf06de48acecb96441e14f50db37a05c9353138f1f0f8b476680bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76167035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06a921e90d95d0edd27e62d87f24a3fced554bde075b4b48f9099611fecb599`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 14:17:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 14:17:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 14:17:32 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 14:17:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 14:17:33 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 14:17:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 14:17:36 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 14:17:36 GMT
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
	-	`sha256:b94763531102ae1af628e5b55ca073b0c0fbd6aab9f221a28f3895303ddd975d`  
		Last Modified: Sat, 27 Jan 2024 05:47:26 GMT  
		Size: 66.3 MB (66284463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd03f53bee613b790f5b2286c4561428b2b2da6234df368a3a50d5ad91d58b9a`  
		Last Modified: Sat, 27 Jan 2024 05:47:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c299d55132b1737b4877e997f9881e05bd66727a05f8502f6fc38969031381ce`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 5.1 MB (5116950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60611bccc71deeef6872096a6f8a89a7e7af13c5027eb639b2ee7c182855d85`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 1.3 MB (1262387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fda9b2eed36da0393b2486d62a5c2c8ed03d6f3e38b27aae0fb6a57259b22e`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

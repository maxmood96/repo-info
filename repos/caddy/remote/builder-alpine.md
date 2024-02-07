## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:40170f4b62181b00e1bcd663e5bc80d6d43533840be49e72a214ddbc15ac52a0
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

### `caddy:builder-alpine` - linux; arm variant v6

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

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:c80d0eabc3c5c1e92b026b7e2c2c35b4783472f984fe455da2ddddedce5b416c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25cc1ad71b8526356adff18f79ddbb3ff658a705a74e76800ee8f8172d4551f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
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
# Tue, 06 Feb 2024 21:55:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:55:58 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:55:58 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:55:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:55:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:56:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:56:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:56:02 GMT
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
	-	`sha256:99e2cd4f5b6025c32b2853d34aa0bcf57d85f2d44b2e412e2ba4e6dd0159ac1f`  
		Last Modified: Tue, 06 Feb 2024 21:29:51 GMT  
		Size: 65.8 MB (65767453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d160b5a79dd98fde6c0642c78daa3c77f077ad44a16b27b65a3b24fff23c603f`  
		Last Modified: Tue, 06 Feb 2024 21:29:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5735d56095a062d062dbd8c2d92cff873a457010035f0a7bf754444cdda79e1`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 4.5 MB (4514266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e601fac0470697a15f02c34e269f0e19119d88f46ffbcdddc5300417e3aab4b`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 1.2 MB (1246089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caff9a4e5a9e81ccc2e586bdbd72039b0d2bcc929751e08afbcffd6dbff11931`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:31f32db6814a94ad3cac5661dbda0a586162eb0b22b3e6ccdeb3e72b55cb9b76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73998584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c56aa1b8e6d877694eff62d87142b579cb7d523e8f22c16615b9ec3c5e3bae3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
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
# Tue, 06 Feb 2024 21:33:04 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:33:04 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:33:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:33:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:33:06 GMT
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
	-	`sha256:1745cea878add1608edd8710a879d4925a33b6e27329531c9c1cdd2c0e79c91a`  
		Last Modified: Tue, 06 Feb 2024 21:33:21 GMT  
		Size: 5.1 MB (5070613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f6d9da6844caff2a0af124b9c01f0bf0abd2be340e5d2c67ab135a7cca76d`  
		Last Modified: Tue, 06 Feb 2024 21:33:21 GMT  
		Size: 1.2 MB (1198444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca8afc86b60749044b9b64230a9f9c67c20aa089b99562732169c4e6a807628`  
		Last Modified: Tue, 06 Feb 2024 21:33:20 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b4effdad9be7ca7509b54d46638823940081fdf20f3000aaf9b3a691ace61f17
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74213039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10cf81cb43dc269c0ea9f820417d703e172313e228a17bdf7cffe96f4d2e742`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
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
# Tue, 06 Feb 2024 21:14:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:14:22 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:14:23 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:14:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:14:24 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:14:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:14:27 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:14:27 GMT
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
	-	`sha256:53242ccbc16994912810b389fdd1f7cb7cb1a3223cec7dcac1d4d00340e2f6de`  
		Last Modified: Tue, 06 Feb 2024 21:14:45 GMT  
		Size: 5.3 MB (5270660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c055ede766eec14283da8e4f87ab21f6a84f8ceff065d702bc31c9bf9ef23757`  
		Last Modified: Tue, 06 Feb 2024 21:14:45 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbe5c0b6966115344269e3c2b83ef21af0ebd897ee5a670604887f27d3da882`  
		Last Modified: Tue, 06 Feb 2024 21:14:44 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:a117c5e1fce71371998cb4714bfd5e51ec2e872e66607e689f70f36cb8d669b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76100364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d206850df57bacba10b80b73b54b11e42600a00f61b8359a8654b61869d447`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
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
# Tue, 06 Feb 2024 23:18:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 23:18:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 23:18:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 23:18:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 23:18:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 23:18:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 23:18:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 23:18:23 GMT
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
	-	`sha256:157967ce6b6aee7bd83e944f7423deb918942e78cd22483b7185e682d3087a8e`  
		Last Modified: Tue, 06 Feb 2024 23:19:52 GMT  
		Size: 5.1 MB (5116968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3127dd07e8d4eb877bd535c99a9b3d8b1435d1ef3bce8533687e510b574bf8d`  
		Last Modified: Tue, 06 Feb 2024 23:19:51 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5531a6884024118a0c4ea03cb2592f4364d360b0fc995d056514e8b9aae42df8`  
		Last Modified: Tue, 06 Feb 2024 23:19:51 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

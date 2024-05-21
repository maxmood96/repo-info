<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.19`](#nats2-alpine319)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.19`](#nats210-alpine319)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.16`](#nats21016)
-	[`nats:2.10.16-alpine`](#nats21016-alpine)
-	[`nats:2.10.16-alpine3.19`](#nats21016-alpine319)
-	[`nats:2.10.16-linux`](#nats21016-linux)
-	[`nats:2.10.16-nanoserver`](#nats21016-nanoserver)
-	[`nats:2.10.16-nanoserver-1809`](#nats21016-nanoserver-1809)
-	[`nats:2.10.16-scratch`](#nats21016-scratch)
-	[`nats:2.10.16-windowsservercore`](#nats21016-windowsservercore)
-	[`nats:2.10.16-windowsservercore-1809`](#nats21016-windowsservercore-1809)
-	[`nats:2.9`](#nats29)
-	[`nats:2.9-alpine`](#nats29-alpine)
-	[`nats:2.9-alpine3.18`](#nats29-alpine318)
-	[`nats:2.9-linux`](#nats29-linux)
-	[`nats:2.9-nanoserver`](#nats29-nanoserver)
-	[`nats:2.9-nanoserver-1809`](#nats29-nanoserver-1809)
-	[`nats:2.9-scratch`](#nats29-scratch)
-	[`nats:2.9-windowsservercore`](#nats29-windowsservercore)
-	[`nats:2.9-windowsservercore-1809`](#nats29-windowsservercore-1809)
-	[`nats:2.9.25`](#nats2925)
-	[`nats:2.9.25-alpine`](#nats2925-alpine)
-	[`nats:2.9.25-alpine3.18`](#nats2925-alpine318)
-	[`nats:2.9.25-linux`](#nats2925-linux)
-	[`nats:2.9.25-nanoserver`](#nats2925-nanoserver)
-	[`nats:2.9.25-nanoserver-1809`](#nats2925-nanoserver-1809)
-	[`nats:2.9.25-scratch`](#nats2925-scratch)
-	[`nats:2.9.25-windowsservercore`](#nats2925-windowsservercore)
-	[`nats:2.9.25-windowsservercore-1809`](#nats2925-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.19`](#natsalpine319)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:cdb229a4805b0e2e5d123ecd65665c8485ec814499093392b4213aa8e9420615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5820; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:da851c45cfe95a52ab3e6b013241c2e5271d28f7c0b136f1047c108fbabf859e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2ed2be6ead45418e9fc8d5da88a292fcbb6879e7dcc4db9126a45c5176f6d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:33 GMT
COPY file:0aba91b853d0eaf7d63d52b084d7546996e8db198a221ad2c77a29c916538108 in /nats-server 
# Tue, 21 May 2024 22:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:33 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772a5dc6e4bbb9f932bcf1232f3a7830303a955bbac3775e90153ce66ac9bd8d`  
		Last Modified: Tue, 21 May 2024 22:50:23 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:c655a24000047ea7fc1f1c8c4b1e9c282ac92e2d9706d5aaec92934ab55b72b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb15c7fb2d9a1f5c89f39c7be34daef5e45d98f6454a74e07c7051a7e9223370`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:03:59 GMT
COPY file:ed3148eb9af051d444f42876fc76b54a26455984f4a53bbdf1058b0e11e8b336 in /nats-server 
# Tue, 21 May 2024 23:03:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:03:59 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:59 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:03:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8193d445aa5ad5ea1f96740679c84ff3087a86b1d13258defc8bc3a21f395d18`  
		Last Modified: Tue, 21 May 2024 23:04:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:64d7152e25fd1648d59fe3fda7da9461723b0fa6905b144971bac30def679c99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850b1061eaa54e26469184edc02f606e471c4d9416a0a6bc6068251f90fc0c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:31 GMT
COPY file:dc57eab26dd732b695752b0df8adf307bcbd19553cba75ac3ac2975e7d2cd86f in /nats-server 
# Tue, 21 May 2024 23:21:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:31 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af7d01d01fa2b520a97d19101ea36ea9b96e8124f2fdc1bb7076f976ab01ee`  
		Last Modified: Tue, 21 May 2024 23:22:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:d7f6dd76a8d365ac199d2e1767531fd74bf13cd2c78dba7ac042b8ed1937c4fc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c128c5b164984dd4d70a48c9af0281112501c7ca458ff244d718d50a31dadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:33 GMT
COPY file:e17294dc512d40e8e54498c73c890fd5204a41873c3567f7c18aa532ba727dc3 in /nats-server 
# Tue, 21 May 2024 23:21:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:34 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a45efcc2dc003ec8d53cb55ac8512bb7b4c35bcbd7a761991ef4c1b3147dfd3`  
		Last Modified: Tue, 21 May 2024 23:22:14 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:a9a0d93cb6a669f0fc2d842220f3a517c5c4ac5b345f0e2dc6aa8267c6fc76a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56c6e37910e564eec4963a6cbe0df805262ea12e504977a860f55fc52a39d05`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:30 GMT
COPY file:359d868ca3e4f687575abd568ad941a9d2682ed2ca604af3309b28b73679d2b7 in /nats-server 
# Tue, 21 May 2024 23:21:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:30 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0c0c15d382278c746e463dce4639563f785a5f07f552c8f5caceb88a87d424`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:958a15d708d62f00bc9918e2283ecab5d12a85d54187bb5301593f33c452a6dc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160734385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bceedc7adb4c9ed6737507c649ee6ff628321a49b2274fbed9b74f50ca19557`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:17:18 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be448c0648b4e415641d5d7504a60f23cb03b4b00b0211021d9fbf697157d4ff`  
		Last Modified: Tue, 21 May 2024 23:18:13 GMT  
		Size: 5.8 MB (5786623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17add0d9ad6ce3c2580f4f65cc11d1d7c6eb572e2df535e9b7d1538394ef668e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c916da7655fd8a5653ae241bc5e9e7657b62c26bce65ae68453896906234d11e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696dcba679ec709b4b8fa95dcd27de7889439d88a304ac3770ac1e6f32f8010c`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4a7a4b5fb58cd41e8b7478c971ce9a63da9d056aed725662939f3f108cc898`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:3d01bb9c1bc4eedb5b06973ff4793609453c8e49dbe4653c5a689dfffb305dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:6fb38aaa7467fc0f95b9b8b82667e13a6ab33e88328266114cd5972fd4ce7a36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9593547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed50fb89a515fd8a7ac65959ec5c4447b3224af721405ffb59482b5edcf8b7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:04:51 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:04:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:04:54 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:04:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74b83a0e28b2579e281f6a89215c7220be68fd968d6f29a63794abbc28c1264`  
		Last Modified: Fri, 12 Apr 2024 01:05:34 GMT  
		Size: 6.2 MB (6183818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb31291d77521460d7df0a79503a8b9457e85667ae9d4fc313a127f66b5bbee6`  
		Last Modified: Fri, 12 Apr 2024 01:05:32 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287ee2a0c75e9620dfa28523cdd568ab557a6356d4696dff7d6053cb24ddc57e`  
		Last Modified: Fri, 12 Apr 2024 01:05:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:1adfb327abdec112e1ef8e07b47a65e9359224a5c2fd6f41d5d37b9674e6f65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14527215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daad98a5ab46e9563fb76d02ee9d0b4a4e520beab7c3a1a8c7b6914115c24170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 22:49:24 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 22:49:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 22:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 22:49:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 22:49:28 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 22:49:28 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 22:49:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c50cc966eb4cbc4a4b881ff20948920be4f45ab8e2cf62ab712cac444395ee`  
		Last Modified: Tue, 21 May 2024 22:50:04 GMT  
		Size: 6.0 MB (5977107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482b47d1cf301cc352bae57642f522722da3324f7b667b1c7ab9a6727d88f527`  
		Last Modified: Tue, 21 May 2024 22:50:03 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9121bc5ccbbd746d1fb23bd55dddbf3d7e34dfc3cb7df700f8ca078f0ec344`  
		Last Modified: Tue, 21 May 2024 22:50:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df155a51d233cc945101d877e9a8d394d4b8114026d50c46107ca509e73414a4`  
		Last Modified: Tue, 21 May 2024 22:50:04 GMT  
		Size: 5.4 MB (5383712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a3f56e81749917f8b07128d633c16d54338fb686f6ddcaa849a23b024cdc62cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14259407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afd587d768a05bc1431c931ab535c88081752285018604a5cae23518073a5fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:03:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:03:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:03:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:03:49 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:03:49 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:03:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e9b04dcae92028f76d8d03593f5da713c1b30e4413f516ac6feb1931c7b2e6`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 6.0 MB (5966263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42806fb40884dc31d08d85dc9811fd14e2d5c8a3f1d355140fe35d2b0e8572`  
		Last Modified: Tue, 21 May 2024 23:04:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da704e6a7abb5014e315123b47670ed2c5da374a12abe0c8a16ac5c00984bc5b`  
		Last Modified: Tue, 21 May 2024 23:04:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2a13bc359472f8406932f00ed1e4a78c2bd57597328886fca2d157b4fd875f`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 5.4 MB (5373248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8e0de73f92a021e34a4a3a2d9fe7db10ea0c5374f6acc4839aafa07f83389a89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14486423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30706d32b39530e9b48913eb6b49e5b607cdf805b5b583ca6a10da052e8c863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:10 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:13 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:13 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e451ccd47ce6074c0eb5a19f953f3cf1b5f7582fa1629fb446c5e98df5bca96b`  
		Last Modified: Tue, 21 May 2024 23:22:04 GMT  
		Size: 5.9 MB (5865815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91c46871a02794fd3e02f3a96648cfe21cc7bba92e4a12880704bc4f5099fa6`  
		Last Modified: Tue, 21 May 2024 23:22:03 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0973b29973a14e29ca26a3bf6ce557a818c454e502f2a1625d12916b94a63c7f`  
		Last Modified: Tue, 21 May 2024 23:22:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d832ebe187b943a16762d91e06cfed3a2af866c23fb50873bc206b8ff64b15`  
		Last Modified: Tue, 21 May 2024 23:22:04 GMT  
		Size: 5.3 MB (5271890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:0b37f107c7121fb4970a680686bf47c0bdc6e221f073948f91fe1ccf935a8069
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14453737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff3f441c8f17081f4726462e440f695fc1f61e1a2f10e242f42e4bd984077bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:08 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:15 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:16 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8c871a04ac5c3a745fc1b9fc0bf0df8eb4429cfc19a6d0c0e5dc82ead6caa5`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.8 MB (5844103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856cdce720d8bce5ea7df85548fc0591d2f54a82aaa905dcf4d5c862d090a59e`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29cb8a321e6c477eee1702a71c5d6712719ebf97439a8e5ce5e98052caa4d73`  
		Last Modified: Tue, 21 May 2024 23:21:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74163ae1a817e733dfe24bdc0793bd29a32f24f194a83320208429d1d8a41355`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.3 MB (5250277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:6d5ae5c55bd610f20af66cdcb962dc1467df57e229a88bd21e4aa67b0125a4bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14983722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e6fda5c2edf46ae713164e45bc6d3db65c81e9d94751fa2b474f4491b6dee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:19 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:23 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:23 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03de2766ed1b649ad8022c7178d9fb18b54afafd6768b26cc8418bc8ee6ca3`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 6.2 MB (6166358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca420f0a7f6b1e669c0fc2fb845bb3a3e3b5918ae5e6ca274bbe962f098a7c9`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08ad1d4d29a3891a6cef4dd154aebf959965bbae6c2df8f3f88d4d0b617b06f`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e270d0402a827b66e36de07d5f201dc2ad24fdf690b07d53315ef189c7d5aaa`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.6 MB (5573725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.19`

```console
$ docker pull nats@sha256:3d01bb9c1bc4eedb5b06973ff4793609453c8e49dbe4653c5a689dfffb305dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:6fb38aaa7467fc0f95b9b8b82667e13a6ab33e88328266114cd5972fd4ce7a36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9593547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed50fb89a515fd8a7ac65959ec5c4447b3224af721405ffb59482b5edcf8b7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:04:51 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:04:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:04:54 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:04:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74b83a0e28b2579e281f6a89215c7220be68fd968d6f29a63794abbc28c1264`  
		Last Modified: Fri, 12 Apr 2024 01:05:34 GMT  
		Size: 6.2 MB (6183818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb31291d77521460d7df0a79503a8b9457e85667ae9d4fc313a127f66b5bbee6`  
		Last Modified: Fri, 12 Apr 2024 01:05:32 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287ee2a0c75e9620dfa28523cdd568ab557a6356d4696dff7d6053cb24ddc57e`  
		Last Modified: Fri, 12 Apr 2024 01:05:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:1adfb327abdec112e1ef8e07b47a65e9359224a5c2fd6f41d5d37b9674e6f65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14527215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daad98a5ab46e9563fb76d02ee9d0b4a4e520beab7c3a1a8c7b6914115c24170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 22:49:24 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 22:49:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 22:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 22:49:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 22:49:28 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 22:49:28 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 22:49:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c50cc966eb4cbc4a4b881ff20948920be4f45ab8e2cf62ab712cac444395ee`  
		Last Modified: Tue, 21 May 2024 22:50:04 GMT  
		Size: 6.0 MB (5977107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482b47d1cf301cc352bae57642f522722da3324f7b667b1c7ab9a6727d88f527`  
		Last Modified: Tue, 21 May 2024 22:50:03 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9121bc5ccbbd746d1fb23bd55dddbf3d7e34dfc3cb7df700f8ca078f0ec344`  
		Last Modified: Tue, 21 May 2024 22:50:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df155a51d233cc945101d877e9a8d394d4b8114026d50c46107ca509e73414a4`  
		Last Modified: Tue, 21 May 2024 22:50:04 GMT  
		Size: 5.4 MB (5383712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:a3f56e81749917f8b07128d633c16d54338fb686f6ddcaa849a23b024cdc62cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14259407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afd587d768a05bc1431c931ab535c88081752285018604a5cae23518073a5fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:03:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:03:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:03:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:03:49 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:03:49 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:03:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e9b04dcae92028f76d8d03593f5da713c1b30e4413f516ac6feb1931c7b2e6`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 6.0 MB (5966263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42806fb40884dc31d08d85dc9811fd14e2d5c8a3f1d355140fe35d2b0e8572`  
		Last Modified: Tue, 21 May 2024 23:04:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da704e6a7abb5014e315123b47670ed2c5da374a12abe0c8a16ac5c00984bc5b`  
		Last Modified: Tue, 21 May 2024 23:04:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2a13bc359472f8406932f00ed1e4a78c2bd57597328886fca2d157b4fd875f`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 5.4 MB (5373248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8e0de73f92a021e34a4a3a2d9fe7db10ea0c5374f6acc4839aafa07f83389a89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14486423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30706d32b39530e9b48913eb6b49e5b607cdf805b5b583ca6a10da052e8c863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:10 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:13 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:13 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e451ccd47ce6074c0eb5a19f953f3cf1b5f7582fa1629fb446c5e98df5bca96b`  
		Last Modified: Tue, 21 May 2024 23:22:04 GMT  
		Size: 5.9 MB (5865815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91c46871a02794fd3e02f3a96648cfe21cc7bba92e4a12880704bc4f5099fa6`  
		Last Modified: Tue, 21 May 2024 23:22:03 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0973b29973a14e29ca26a3bf6ce557a818c454e502f2a1625d12916b94a63c7f`  
		Last Modified: Tue, 21 May 2024 23:22:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d832ebe187b943a16762d91e06cfed3a2af866c23fb50873bc206b8ff64b15`  
		Last Modified: Tue, 21 May 2024 23:22:04 GMT  
		Size: 5.3 MB (5271890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:0b37f107c7121fb4970a680686bf47c0bdc6e221f073948f91fe1ccf935a8069
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14453737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff3f441c8f17081f4726462e440f695fc1f61e1a2f10e242f42e4bd984077bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:08 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:15 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:16 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8c871a04ac5c3a745fc1b9fc0bf0df8eb4429cfc19a6d0c0e5dc82ead6caa5`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.8 MB (5844103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856cdce720d8bce5ea7df85548fc0591d2f54a82aaa905dcf4d5c862d090a59e`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29cb8a321e6c477eee1702a71c5d6712719ebf97439a8e5ce5e98052caa4d73`  
		Last Modified: Tue, 21 May 2024 23:21:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74163ae1a817e733dfe24bdc0793bd29a32f24f194a83320208429d1d8a41355`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.3 MB (5250277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:6d5ae5c55bd610f20af66cdcb962dc1467df57e229a88bd21e4aa67b0125a4bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14983722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e6fda5c2edf46ae713164e45bc6d3db65c81e9d94751fa2b474f4491b6dee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:19 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:23 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:23 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03de2766ed1b649ad8022c7178d9fb18b54afafd6768b26cc8418bc8ee6ca3`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 6.2 MB (6166358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca420f0a7f6b1e669c0fc2fb845bb3a3e3b5918ae5e6ca274bbe962f098a7c9`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08ad1d4d29a3891a6cef4dd154aebf959965bbae6c2df8f3f88d4d0b617b06f`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e270d0402a827b66e36de07d5f201dc2ad24fdf690b07d53315ef189c7d5aaa`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.6 MB (5573725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:0bec822da126d2b61e51f4ef77397ea35d96e27ba61e8a46379bf6bb2ee34874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:da851c45cfe95a52ab3e6b013241c2e5271d28f7c0b136f1047c108fbabf859e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2ed2be6ead45418e9fc8d5da88a292fcbb6879e7dcc4db9126a45c5176f6d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:33 GMT
COPY file:0aba91b853d0eaf7d63d52b084d7546996e8db198a221ad2c77a29c916538108 in /nats-server 
# Tue, 21 May 2024 22:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:33 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772a5dc6e4bbb9f932bcf1232f3a7830303a955bbac3775e90153ce66ac9bd8d`  
		Last Modified: Tue, 21 May 2024 22:50:23 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:c655a24000047ea7fc1f1c8c4b1e9c282ac92e2d9706d5aaec92934ab55b72b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb15c7fb2d9a1f5c89f39c7be34daef5e45d98f6454a74e07c7051a7e9223370`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:03:59 GMT
COPY file:ed3148eb9af051d444f42876fc76b54a26455984f4a53bbdf1058b0e11e8b336 in /nats-server 
# Tue, 21 May 2024 23:03:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:03:59 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:59 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:03:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8193d445aa5ad5ea1f96740679c84ff3087a86b1d13258defc8bc3a21f395d18`  
		Last Modified: Tue, 21 May 2024 23:04:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:64d7152e25fd1648d59fe3fda7da9461723b0fa6905b144971bac30def679c99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850b1061eaa54e26469184edc02f606e471c4d9416a0a6bc6068251f90fc0c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:31 GMT
COPY file:dc57eab26dd732b695752b0df8adf307bcbd19553cba75ac3ac2975e7d2cd86f in /nats-server 
# Tue, 21 May 2024 23:21:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:31 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af7d01d01fa2b520a97d19101ea36ea9b96e8124f2fdc1bb7076f976ab01ee`  
		Last Modified: Tue, 21 May 2024 23:22:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:d7f6dd76a8d365ac199d2e1767531fd74bf13cd2c78dba7ac042b8ed1937c4fc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c128c5b164984dd4d70a48c9af0281112501c7ca458ff244d718d50a31dadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:33 GMT
COPY file:e17294dc512d40e8e54498c73c890fd5204a41873c3567f7c18aa532ba727dc3 in /nats-server 
# Tue, 21 May 2024 23:21:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:34 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a45efcc2dc003ec8d53cb55ac8512bb7b4c35bcbd7a761991ef4c1b3147dfd3`  
		Last Modified: Tue, 21 May 2024 23:22:14 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:a9a0d93cb6a669f0fc2d842220f3a517c5c4ac5b345f0e2dc6aa8267c6fc76a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56c6e37910e564eec4963a6cbe0df805262ea12e504977a860f55fc52a39d05`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:30 GMT
COPY file:359d868ca3e4f687575abd568ad941a9d2682ed2ca604af3309b28b73679d2b7 in /nats-server 
# Tue, 21 May 2024 23:21:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:30 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0c0c15d382278c746e463dce4639563f785a5f07f552c8f5caceb88a87d424`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:003d8791c50c4203ecf629af340c97c71cacca7c43091cb6d0b2537d80fbbec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:958a15d708d62f00bc9918e2283ecab5d12a85d54187bb5301593f33c452a6dc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160734385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bceedc7adb4c9ed6737507c649ee6ff628321a49b2274fbed9b74f50ca19557`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:17:18 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be448c0648b4e415641d5d7504a60f23cb03b4b00b0211021d9fbf697157d4ff`  
		Last Modified: Tue, 21 May 2024 23:18:13 GMT  
		Size: 5.8 MB (5786623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17add0d9ad6ce3c2580f4f65cc11d1d7c6eb572e2df535e9b7d1538394ef668e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c916da7655fd8a5653ae241bc5e9e7657b62c26bce65ae68453896906234d11e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696dcba679ec709b4b8fa95dcd27de7889439d88a304ac3770ac1e6f32f8010c`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4a7a4b5fb58cd41e8b7478c971ce9a63da9d056aed725662939f3f108cc898`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:003d8791c50c4203ecf629af340c97c71cacca7c43091cb6d0b2537d80fbbec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:958a15d708d62f00bc9918e2283ecab5d12a85d54187bb5301593f33c452a6dc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160734385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bceedc7adb4c9ed6737507c649ee6ff628321a49b2274fbed9b74f50ca19557`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:17:18 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be448c0648b4e415641d5d7504a60f23cb03b4b00b0211021d9fbf697157d4ff`  
		Last Modified: Tue, 21 May 2024 23:18:13 GMT  
		Size: 5.8 MB (5786623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17add0d9ad6ce3c2580f4f65cc11d1d7c6eb572e2df535e9b7d1538394ef668e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c916da7655fd8a5653ae241bc5e9e7657b62c26bce65ae68453896906234d11e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696dcba679ec709b4b8fa95dcd27de7889439d88a304ac3770ac1e6f32f8010c`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4a7a4b5fb58cd41e8b7478c971ce9a63da9d056aed725662939f3f108cc898`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:0bec822da126d2b61e51f4ef77397ea35d96e27ba61e8a46379bf6bb2ee34874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:da851c45cfe95a52ab3e6b013241c2e5271d28f7c0b136f1047c108fbabf859e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2ed2be6ead45418e9fc8d5da88a292fcbb6879e7dcc4db9126a45c5176f6d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:33 GMT
COPY file:0aba91b853d0eaf7d63d52b084d7546996e8db198a221ad2c77a29c916538108 in /nats-server 
# Tue, 21 May 2024 22:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:33 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772a5dc6e4bbb9f932bcf1232f3a7830303a955bbac3775e90153ce66ac9bd8d`  
		Last Modified: Tue, 21 May 2024 22:50:23 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:c655a24000047ea7fc1f1c8c4b1e9c282ac92e2d9706d5aaec92934ab55b72b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb15c7fb2d9a1f5c89f39c7be34daef5e45d98f6454a74e07c7051a7e9223370`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:03:59 GMT
COPY file:ed3148eb9af051d444f42876fc76b54a26455984f4a53bbdf1058b0e11e8b336 in /nats-server 
# Tue, 21 May 2024 23:03:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:03:59 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:59 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:03:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8193d445aa5ad5ea1f96740679c84ff3087a86b1d13258defc8bc3a21f395d18`  
		Last Modified: Tue, 21 May 2024 23:04:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:64d7152e25fd1648d59fe3fda7da9461723b0fa6905b144971bac30def679c99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850b1061eaa54e26469184edc02f606e471c4d9416a0a6bc6068251f90fc0c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:31 GMT
COPY file:dc57eab26dd732b695752b0df8adf307bcbd19553cba75ac3ac2975e7d2cd86f in /nats-server 
# Tue, 21 May 2024 23:21:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:31 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af7d01d01fa2b520a97d19101ea36ea9b96e8124f2fdc1bb7076f976ab01ee`  
		Last Modified: Tue, 21 May 2024 23:22:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:d7f6dd76a8d365ac199d2e1767531fd74bf13cd2c78dba7ac042b8ed1937c4fc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c128c5b164984dd4d70a48c9af0281112501c7ca458ff244d718d50a31dadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:33 GMT
COPY file:e17294dc512d40e8e54498c73c890fd5204a41873c3567f7c18aa532ba727dc3 in /nats-server 
# Tue, 21 May 2024 23:21:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:34 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a45efcc2dc003ec8d53cb55ac8512bb7b4c35bcbd7a761991ef4c1b3147dfd3`  
		Last Modified: Tue, 21 May 2024 23:22:14 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:a9a0d93cb6a669f0fc2d842220f3a517c5c4ac5b345f0e2dc6aa8267c6fc76a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56c6e37910e564eec4963a6cbe0df805262ea12e504977a860f55fc52a39d05`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:30 GMT
COPY file:359d868ca3e4f687575abd568ad941a9d2682ed2ca604af3309b28b73679d2b7 in /nats-server 
# Tue, 21 May 2024 23:21:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:30 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0c0c15d382278c746e463dce4639563f785a5f07f552c8f5caceb88a87d424`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:5b3e38cc7df1ccd71cb1357b316228b34861c6c37727ca7ffd148b73e64b321b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:fc57a2fbc1740965db1c40c59291ef89a6d9f5f235b4d963f4d0602ae0666443
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186249989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b64d1c4d9a958ede215514048d16b164a246beedd0c21e6c59ff3d07f069867`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:14:46 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:14:47 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.16/nats-server-v2.10.16-windows-amd64.zip
# Tue, 21 May 2024 23:14:48 GMT
ENV NATS_SERVER_SHASUM=22a5ef3a54200ebdebaa325822f477c89dc6533ec6fc1f531d897aa876517ccf
# Tue, 21 May 2024 23:15:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 21 May 2024 23:16:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 21 May 2024 23:16:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:16:58 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:16:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:16:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d075cbe94bdd5f06bdabff0ae1baa13ad48a75f808800d9c9cf7d554470d866`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a88d0da7a6579af9c2bdff927235dee0c94b1bfc1cec3787d05218c6a55ec3c`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f922389c5664c8e701d97ef08d1cc52e256e6002e475dacd84e45e12ccaf8cc0`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096dd602404c378351787720a7178c38038189543894dcbe1ce4b5260124b8af`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 445.9 KB (445881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bad7b47779f08ea37f050914a7169eb3be6ad32530159df515b046af95396`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 6.1 MB (6079688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c3b9fbec461537454b31d72f007b18f9d7d0449481a6532b4bc0465145b360`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93647e59b4740ef7e3e440c385dfc114fbae9e7fa990db167023a7040f182a11`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445badc8d13b259ba8343872927775698cdbb81b6013fa153680a9052fea5330`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da65ffc80b4f6a0ef8841c9d2e497145d917917587c49470ad4ca54c6cf78de`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:5b3e38cc7df1ccd71cb1357b316228b34861c6c37727ca7ffd148b73e64b321b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:fc57a2fbc1740965db1c40c59291ef89a6d9f5f235b4d963f4d0602ae0666443
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186249989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b64d1c4d9a958ede215514048d16b164a246beedd0c21e6c59ff3d07f069867`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:14:46 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:14:47 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.16/nats-server-v2.10.16-windows-amd64.zip
# Tue, 21 May 2024 23:14:48 GMT
ENV NATS_SERVER_SHASUM=22a5ef3a54200ebdebaa325822f477c89dc6533ec6fc1f531d897aa876517ccf
# Tue, 21 May 2024 23:15:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 21 May 2024 23:16:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 21 May 2024 23:16:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:16:58 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:16:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:16:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d075cbe94bdd5f06bdabff0ae1baa13ad48a75f808800d9c9cf7d554470d866`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a88d0da7a6579af9c2bdff927235dee0c94b1bfc1cec3787d05218c6a55ec3c`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f922389c5664c8e701d97ef08d1cc52e256e6002e475dacd84e45e12ccaf8cc0`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096dd602404c378351787720a7178c38038189543894dcbe1ce4b5260124b8af`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 445.9 KB (445881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bad7b47779f08ea37f050914a7169eb3be6ad32530159df515b046af95396`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 6.1 MB (6079688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c3b9fbec461537454b31d72f007b18f9d7d0449481a6532b4bc0465145b360`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93647e59b4740ef7e3e440c385dfc114fbae9e7fa990db167023a7040f182a11`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445badc8d13b259ba8343872927775698cdbb81b6013fa153680a9052fea5330`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da65ffc80b4f6a0ef8841c9d2e497145d917917587c49470ad4ca54c6cf78de`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:cdb229a4805b0e2e5d123ecd65665c8485ec814499093392b4213aa8e9420615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:da851c45cfe95a52ab3e6b013241c2e5271d28f7c0b136f1047c108fbabf859e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2ed2be6ead45418e9fc8d5da88a292fcbb6879e7dcc4db9126a45c5176f6d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:33 GMT
COPY file:0aba91b853d0eaf7d63d52b084d7546996e8db198a221ad2c77a29c916538108 in /nats-server 
# Tue, 21 May 2024 22:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:33 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772a5dc6e4bbb9f932bcf1232f3a7830303a955bbac3775e90153ce66ac9bd8d`  
		Last Modified: Tue, 21 May 2024 22:50:23 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:c655a24000047ea7fc1f1c8c4b1e9c282ac92e2d9706d5aaec92934ab55b72b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb15c7fb2d9a1f5c89f39c7be34daef5e45d98f6454a74e07c7051a7e9223370`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:03:59 GMT
COPY file:ed3148eb9af051d444f42876fc76b54a26455984f4a53bbdf1058b0e11e8b336 in /nats-server 
# Tue, 21 May 2024 23:03:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:03:59 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:59 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:03:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8193d445aa5ad5ea1f96740679c84ff3087a86b1d13258defc8bc3a21f395d18`  
		Last Modified: Tue, 21 May 2024 23:04:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:64d7152e25fd1648d59fe3fda7da9461723b0fa6905b144971bac30def679c99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850b1061eaa54e26469184edc02f606e471c4d9416a0a6bc6068251f90fc0c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:31 GMT
COPY file:dc57eab26dd732b695752b0df8adf307bcbd19553cba75ac3ac2975e7d2cd86f in /nats-server 
# Tue, 21 May 2024 23:21:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:31 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af7d01d01fa2b520a97d19101ea36ea9b96e8124f2fdc1bb7076f976ab01ee`  
		Last Modified: Tue, 21 May 2024 23:22:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:d7f6dd76a8d365ac199d2e1767531fd74bf13cd2c78dba7ac042b8ed1937c4fc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c128c5b164984dd4d70a48c9af0281112501c7ca458ff244d718d50a31dadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:33 GMT
COPY file:e17294dc512d40e8e54498c73c890fd5204a41873c3567f7c18aa532ba727dc3 in /nats-server 
# Tue, 21 May 2024 23:21:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:34 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a45efcc2dc003ec8d53cb55ac8512bb7b4c35bcbd7a761991ef4c1b3147dfd3`  
		Last Modified: Tue, 21 May 2024 23:22:14 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:a9a0d93cb6a669f0fc2d842220f3a517c5c4ac5b345f0e2dc6aa8267c6fc76a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56c6e37910e564eec4963a6cbe0df805262ea12e504977a860f55fc52a39d05`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:30 GMT
COPY file:359d868ca3e4f687575abd568ad941a9d2682ed2ca604af3309b28b73679d2b7 in /nats-server 
# Tue, 21 May 2024 23:21:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:30 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0c0c15d382278c746e463dce4639563f785a5f07f552c8f5caceb88a87d424`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:958a15d708d62f00bc9918e2283ecab5d12a85d54187bb5301593f33c452a6dc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160734385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bceedc7adb4c9ed6737507c649ee6ff628321a49b2274fbed9b74f50ca19557`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:17:18 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be448c0648b4e415641d5d7504a60f23cb03b4b00b0211021d9fbf697157d4ff`  
		Last Modified: Tue, 21 May 2024 23:18:13 GMT  
		Size: 5.8 MB (5786623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17add0d9ad6ce3c2580f4f65cc11d1d7c6eb572e2df535e9b7d1538394ef668e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c916da7655fd8a5653ae241bc5e9e7657b62c26bce65ae68453896906234d11e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696dcba679ec709b4b8fa95dcd27de7889439d88a304ac3770ac1e6f32f8010c`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4a7a4b5fb58cd41e8b7478c971ce9a63da9d056aed725662939f3f108cc898`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:3d01bb9c1bc4eedb5b06973ff4793609453c8e49dbe4653c5a689dfffb305dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:6fb38aaa7467fc0f95b9b8b82667e13a6ab33e88328266114cd5972fd4ce7a36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9593547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed50fb89a515fd8a7ac65959ec5c4447b3224af721405ffb59482b5edcf8b7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:04:51 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:04:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:04:54 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:04:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74b83a0e28b2579e281f6a89215c7220be68fd968d6f29a63794abbc28c1264`  
		Last Modified: Fri, 12 Apr 2024 01:05:34 GMT  
		Size: 6.2 MB (6183818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb31291d77521460d7df0a79503a8b9457e85667ae9d4fc313a127f66b5bbee6`  
		Last Modified: Fri, 12 Apr 2024 01:05:32 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287ee2a0c75e9620dfa28523cdd568ab557a6356d4696dff7d6053cb24ddc57e`  
		Last Modified: Fri, 12 Apr 2024 01:05:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:1adfb327abdec112e1ef8e07b47a65e9359224a5c2fd6f41d5d37b9674e6f65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14527215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daad98a5ab46e9563fb76d02ee9d0b4a4e520beab7c3a1a8c7b6914115c24170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 22:49:24 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 22:49:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 22:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 22:49:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 22:49:28 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 22:49:28 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 22:49:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c50cc966eb4cbc4a4b881ff20948920be4f45ab8e2cf62ab712cac444395ee`  
		Last Modified: Tue, 21 May 2024 22:50:04 GMT  
		Size: 6.0 MB (5977107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482b47d1cf301cc352bae57642f522722da3324f7b667b1c7ab9a6727d88f527`  
		Last Modified: Tue, 21 May 2024 22:50:03 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9121bc5ccbbd746d1fb23bd55dddbf3d7e34dfc3cb7df700f8ca078f0ec344`  
		Last Modified: Tue, 21 May 2024 22:50:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df155a51d233cc945101d877e9a8d394d4b8114026d50c46107ca509e73414a4`  
		Last Modified: Tue, 21 May 2024 22:50:04 GMT  
		Size: 5.4 MB (5383712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a3f56e81749917f8b07128d633c16d54338fb686f6ddcaa849a23b024cdc62cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14259407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afd587d768a05bc1431c931ab535c88081752285018604a5cae23518073a5fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:03:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:03:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:03:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:03:49 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:03:49 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:03:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e9b04dcae92028f76d8d03593f5da713c1b30e4413f516ac6feb1931c7b2e6`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 6.0 MB (5966263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42806fb40884dc31d08d85dc9811fd14e2d5c8a3f1d355140fe35d2b0e8572`  
		Last Modified: Tue, 21 May 2024 23:04:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da704e6a7abb5014e315123b47670ed2c5da374a12abe0c8a16ac5c00984bc5b`  
		Last Modified: Tue, 21 May 2024 23:04:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2a13bc359472f8406932f00ed1e4a78c2bd57597328886fca2d157b4fd875f`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 5.4 MB (5373248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8e0de73f92a021e34a4a3a2d9fe7db10ea0c5374f6acc4839aafa07f83389a89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14486423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30706d32b39530e9b48913eb6b49e5b607cdf805b5b583ca6a10da052e8c863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:10 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:13 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:13 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e451ccd47ce6074c0eb5a19f953f3cf1b5f7582fa1629fb446c5e98df5bca96b`  
		Last Modified: Tue, 21 May 2024 23:22:04 GMT  
		Size: 5.9 MB (5865815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91c46871a02794fd3e02f3a96648cfe21cc7bba92e4a12880704bc4f5099fa6`  
		Last Modified: Tue, 21 May 2024 23:22:03 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0973b29973a14e29ca26a3bf6ce557a818c454e502f2a1625d12916b94a63c7f`  
		Last Modified: Tue, 21 May 2024 23:22:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d832ebe187b943a16762d91e06cfed3a2af866c23fb50873bc206b8ff64b15`  
		Last Modified: Tue, 21 May 2024 23:22:04 GMT  
		Size: 5.3 MB (5271890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:0b37f107c7121fb4970a680686bf47c0bdc6e221f073948f91fe1ccf935a8069
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14453737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff3f441c8f17081f4726462e440f695fc1f61e1a2f10e242f42e4bd984077bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:08 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:15 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:16 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8c871a04ac5c3a745fc1b9fc0bf0df8eb4429cfc19a6d0c0e5dc82ead6caa5`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.8 MB (5844103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856cdce720d8bce5ea7df85548fc0591d2f54a82aaa905dcf4d5c862d090a59e`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29cb8a321e6c477eee1702a71c5d6712719ebf97439a8e5ce5e98052caa4d73`  
		Last Modified: Tue, 21 May 2024 23:21:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74163ae1a817e733dfe24bdc0793bd29a32f24f194a83320208429d1d8a41355`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.3 MB (5250277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:6d5ae5c55bd610f20af66cdcb962dc1467df57e229a88bd21e4aa67b0125a4bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14983722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e6fda5c2edf46ae713164e45bc6d3db65c81e9d94751fa2b474f4491b6dee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:19 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:23 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:23 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03de2766ed1b649ad8022c7178d9fb18b54afafd6768b26cc8418bc8ee6ca3`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 6.2 MB (6166358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca420f0a7f6b1e669c0fc2fb845bb3a3e3b5918ae5e6ca274bbe962f098a7c9`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08ad1d4d29a3891a6cef4dd154aebf959965bbae6c2df8f3f88d4d0b617b06f`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e270d0402a827b66e36de07d5f201dc2ad24fdf690b07d53315ef189c7d5aaa`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.6 MB (5573725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.19`

```console
$ docker pull nats@sha256:3d01bb9c1bc4eedb5b06973ff4793609453c8e49dbe4653c5a689dfffb305dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:6fb38aaa7467fc0f95b9b8b82667e13a6ab33e88328266114cd5972fd4ce7a36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9593547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed50fb89a515fd8a7ac65959ec5c4447b3224af721405ffb59482b5edcf8b7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:04:51 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:04:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:04:54 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:04:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74b83a0e28b2579e281f6a89215c7220be68fd968d6f29a63794abbc28c1264`  
		Last Modified: Fri, 12 Apr 2024 01:05:34 GMT  
		Size: 6.2 MB (6183818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb31291d77521460d7df0a79503a8b9457e85667ae9d4fc313a127f66b5bbee6`  
		Last Modified: Fri, 12 Apr 2024 01:05:32 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287ee2a0c75e9620dfa28523cdd568ab557a6356d4696dff7d6053cb24ddc57e`  
		Last Modified: Fri, 12 Apr 2024 01:05:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:1adfb327abdec112e1ef8e07b47a65e9359224a5c2fd6f41d5d37b9674e6f65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14527215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daad98a5ab46e9563fb76d02ee9d0b4a4e520beab7c3a1a8c7b6914115c24170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 22:49:24 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 22:49:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 22:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 22:49:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 22:49:28 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 22:49:28 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 22:49:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c50cc966eb4cbc4a4b881ff20948920be4f45ab8e2cf62ab712cac444395ee`  
		Last Modified: Tue, 21 May 2024 22:50:04 GMT  
		Size: 6.0 MB (5977107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482b47d1cf301cc352bae57642f522722da3324f7b667b1c7ab9a6727d88f527`  
		Last Modified: Tue, 21 May 2024 22:50:03 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9121bc5ccbbd746d1fb23bd55dddbf3d7e34dfc3cb7df700f8ca078f0ec344`  
		Last Modified: Tue, 21 May 2024 22:50:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df155a51d233cc945101d877e9a8d394d4b8114026d50c46107ca509e73414a4`  
		Last Modified: Tue, 21 May 2024 22:50:04 GMT  
		Size: 5.4 MB (5383712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:a3f56e81749917f8b07128d633c16d54338fb686f6ddcaa849a23b024cdc62cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14259407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afd587d768a05bc1431c931ab535c88081752285018604a5cae23518073a5fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:03:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:03:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:03:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:03:49 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:03:49 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:03:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e9b04dcae92028f76d8d03593f5da713c1b30e4413f516ac6feb1931c7b2e6`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 6.0 MB (5966263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42806fb40884dc31d08d85dc9811fd14e2d5c8a3f1d355140fe35d2b0e8572`  
		Last Modified: Tue, 21 May 2024 23:04:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da704e6a7abb5014e315123b47670ed2c5da374a12abe0c8a16ac5c00984bc5b`  
		Last Modified: Tue, 21 May 2024 23:04:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2a13bc359472f8406932f00ed1e4a78c2bd57597328886fca2d157b4fd875f`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 5.4 MB (5373248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8e0de73f92a021e34a4a3a2d9fe7db10ea0c5374f6acc4839aafa07f83389a89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14486423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30706d32b39530e9b48913eb6b49e5b607cdf805b5b583ca6a10da052e8c863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:10 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:13 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:13 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e451ccd47ce6074c0eb5a19f953f3cf1b5f7582fa1629fb446c5e98df5bca96b`  
		Last Modified: Tue, 21 May 2024 23:22:04 GMT  
		Size: 5.9 MB (5865815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91c46871a02794fd3e02f3a96648cfe21cc7bba92e4a12880704bc4f5099fa6`  
		Last Modified: Tue, 21 May 2024 23:22:03 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0973b29973a14e29ca26a3bf6ce557a818c454e502f2a1625d12916b94a63c7f`  
		Last Modified: Tue, 21 May 2024 23:22:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d832ebe187b943a16762d91e06cfed3a2af866c23fb50873bc206b8ff64b15`  
		Last Modified: Tue, 21 May 2024 23:22:04 GMT  
		Size: 5.3 MB (5271890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:0b37f107c7121fb4970a680686bf47c0bdc6e221f073948f91fe1ccf935a8069
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14453737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff3f441c8f17081f4726462e440f695fc1f61e1a2f10e242f42e4bd984077bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:08 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:15 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:16 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8c871a04ac5c3a745fc1b9fc0bf0df8eb4429cfc19a6d0c0e5dc82ead6caa5`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.8 MB (5844103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856cdce720d8bce5ea7df85548fc0591d2f54a82aaa905dcf4d5c862d090a59e`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29cb8a321e6c477eee1702a71c5d6712719ebf97439a8e5ce5e98052caa4d73`  
		Last Modified: Tue, 21 May 2024 23:21:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74163ae1a817e733dfe24bdc0793bd29a32f24f194a83320208429d1d8a41355`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.3 MB (5250277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:6d5ae5c55bd610f20af66cdcb962dc1467df57e229a88bd21e4aa67b0125a4bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14983722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e6fda5c2edf46ae713164e45bc6d3db65c81e9d94751fa2b474f4491b6dee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:19 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:23 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:23 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03de2766ed1b649ad8022c7178d9fb18b54afafd6768b26cc8418bc8ee6ca3`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 6.2 MB (6166358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca420f0a7f6b1e669c0fc2fb845bb3a3e3b5918ae5e6ca274bbe962f098a7c9`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08ad1d4d29a3891a6cef4dd154aebf959965bbae6c2df8f3f88d4d0b617b06f`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e270d0402a827b66e36de07d5f201dc2ad24fdf690b07d53315ef189c7d5aaa`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.6 MB (5573725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:0bec822da126d2b61e51f4ef77397ea35d96e27ba61e8a46379bf6bb2ee34874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:da851c45cfe95a52ab3e6b013241c2e5271d28f7c0b136f1047c108fbabf859e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2ed2be6ead45418e9fc8d5da88a292fcbb6879e7dcc4db9126a45c5176f6d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:33 GMT
COPY file:0aba91b853d0eaf7d63d52b084d7546996e8db198a221ad2c77a29c916538108 in /nats-server 
# Tue, 21 May 2024 22:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:33 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772a5dc6e4bbb9f932bcf1232f3a7830303a955bbac3775e90153ce66ac9bd8d`  
		Last Modified: Tue, 21 May 2024 22:50:23 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:c655a24000047ea7fc1f1c8c4b1e9c282ac92e2d9706d5aaec92934ab55b72b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb15c7fb2d9a1f5c89f39c7be34daef5e45d98f6454a74e07c7051a7e9223370`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:03:59 GMT
COPY file:ed3148eb9af051d444f42876fc76b54a26455984f4a53bbdf1058b0e11e8b336 in /nats-server 
# Tue, 21 May 2024 23:03:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:03:59 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:59 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:03:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8193d445aa5ad5ea1f96740679c84ff3087a86b1d13258defc8bc3a21f395d18`  
		Last Modified: Tue, 21 May 2024 23:04:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:64d7152e25fd1648d59fe3fda7da9461723b0fa6905b144971bac30def679c99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850b1061eaa54e26469184edc02f606e471c4d9416a0a6bc6068251f90fc0c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:31 GMT
COPY file:dc57eab26dd732b695752b0df8adf307bcbd19553cba75ac3ac2975e7d2cd86f in /nats-server 
# Tue, 21 May 2024 23:21:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:31 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af7d01d01fa2b520a97d19101ea36ea9b96e8124f2fdc1bb7076f976ab01ee`  
		Last Modified: Tue, 21 May 2024 23:22:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:d7f6dd76a8d365ac199d2e1767531fd74bf13cd2c78dba7ac042b8ed1937c4fc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c128c5b164984dd4d70a48c9af0281112501c7ca458ff244d718d50a31dadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:33 GMT
COPY file:e17294dc512d40e8e54498c73c890fd5204a41873c3567f7c18aa532ba727dc3 in /nats-server 
# Tue, 21 May 2024 23:21:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:34 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a45efcc2dc003ec8d53cb55ac8512bb7b4c35bcbd7a761991ef4c1b3147dfd3`  
		Last Modified: Tue, 21 May 2024 23:22:14 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:a9a0d93cb6a669f0fc2d842220f3a517c5c4ac5b345f0e2dc6aa8267c6fc76a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56c6e37910e564eec4963a6cbe0df805262ea12e504977a860f55fc52a39d05`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:30 GMT
COPY file:359d868ca3e4f687575abd568ad941a9d2682ed2ca604af3309b28b73679d2b7 in /nats-server 
# Tue, 21 May 2024 23:21:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:30 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0c0c15d382278c746e463dce4639563f785a5f07f552c8f5caceb88a87d424`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:003d8791c50c4203ecf629af340c97c71cacca7c43091cb6d0b2537d80fbbec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:958a15d708d62f00bc9918e2283ecab5d12a85d54187bb5301593f33c452a6dc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160734385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bceedc7adb4c9ed6737507c649ee6ff628321a49b2274fbed9b74f50ca19557`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:17:18 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be448c0648b4e415641d5d7504a60f23cb03b4b00b0211021d9fbf697157d4ff`  
		Last Modified: Tue, 21 May 2024 23:18:13 GMT  
		Size: 5.8 MB (5786623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17add0d9ad6ce3c2580f4f65cc11d1d7c6eb572e2df535e9b7d1538394ef668e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c916da7655fd8a5653ae241bc5e9e7657b62c26bce65ae68453896906234d11e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696dcba679ec709b4b8fa95dcd27de7889439d88a304ac3770ac1e6f32f8010c`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4a7a4b5fb58cd41e8b7478c971ce9a63da9d056aed725662939f3f108cc898`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:003d8791c50c4203ecf629af340c97c71cacca7c43091cb6d0b2537d80fbbec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:958a15d708d62f00bc9918e2283ecab5d12a85d54187bb5301593f33c452a6dc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160734385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bceedc7adb4c9ed6737507c649ee6ff628321a49b2274fbed9b74f50ca19557`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:17:18 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be448c0648b4e415641d5d7504a60f23cb03b4b00b0211021d9fbf697157d4ff`  
		Last Modified: Tue, 21 May 2024 23:18:13 GMT  
		Size: 5.8 MB (5786623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17add0d9ad6ce3c2580f4f65cc11d1d7c6eb572e2df535e9b7d1538394ef668e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c916da7655fd8a5653ae241bc5e9e7657b62c26bce65ae68453896906234d11e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696dcba679ec709b4b8fa95dcd27de7889439d88a304ac3770ac1e6f32f8010c`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4a7a4b5fb58cd41e8b7478c971ce9a63da9d056aed725662939f3f108cc898`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:0bec822da126d2b61e51f4ef77397ea35d96e27ba61e8a46379bf6bb2ee34874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:da851c45cfe95a52ab3e6b013241c2e5271d28f7c0b136f1047c108fbabf859e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2ed2be6ead45418e9fc8d5da88a292fcbb6879e7dcc4db9126a45c5176f6d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:33 GMT
COPY file:0aba91b853d0eaf7d63d52b084d7546996e8db198a221ad2c77a29c916538108 in /nats-server 
# Tue, 21 May 2024 22:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:33 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772a5dc6e4bbb9f932bcf1232f3a7830303a955bbac3775e90153ce66ac9bd8d`  
		Last Modified: Tue, 21 May 2024 22:50:23 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:c655a24000047ea7fc1f1c8c4b1e9c282ac92e2d9706d5aaec92934ab55b72b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb15c7fb2d9a1f5c89f39c7be34daef5e45d98f6454a74e07c7051a7e9223370`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:03:59 GMT
COPY file:ed3148eb9af051d444f42876fc76b54a26455984f4a53bbdf1058b0e11e8b336 in /nats-server 
# Tue, 21 May 2024 23:03:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:03:59 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:59 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:03:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8193d445aa5ad5ea1f96740679c84ff3087a86b1d13258defc8bc3a21f395d18`  
		Last Modified: Tue, 21 May 2024 23:04:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:64d7152e25fd1648d59fe3fda7da9461723b0fa6905b144971bac30def679c99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850b1061eaa54e26469184edc02f606e471c4d9416a0a6bc6068251f90fc0c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:31 GMT
COPY file:dc57eab26dd732b695752b0df8adf307bcbd19553cba75ac3ac2975e7d2cd86f in /nats-server 
# Tue, 21 May 2024 23:21:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:31 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af7d01d01fa2b520a97d19101ea36ea9b96e8124f2fdc1bb7076f976ab01ee`  
		Last Modified: Tue, 21 May 2024 23:22:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:d7f6dd76a8d365ac199d2e1767531fd74bf13cd2c78dba7ac042b8ed1937c4fc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c128c5b164984dd4d70a48c9af0281112501c7ca458ff244d718d50a31dadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:33 GMT
COPY file:e17294dc512d40e8e54498c73c890fd5204a41873c3567f7c18aa532ba727dc3 in /nats-server 
# Tue, 21 May 2024 23:21:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:34 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a45efcc2dc003ec8d53cb55ac8512bb7b4c35bcbd7a761991ef4c1b3147dfd3`  
		Last Modified: Tue, 21 May 2024 23:22:14 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:a9a0d93cb6a669f0fc2d842220f3a517c5c4ac5b345f0e2dc6aa8267c6fc76a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56c6e37910e564eec4963a6cbe0df805262ea12e504977a860f55fc52a39d05`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:30 GMT
COPY file:359d868ca3e4f687575abd568ad941a9d2682ed2ca604af3309b28b73679d2b7 in /nats-server 
# Tue, 21 May 2024 23:21:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:30 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0c0c15d382278c746e463dce4639563f785a5f07f552c8f5caceb88a87d424`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:5b3e38cc7df1ccd71cb1357b316228b34861c6c37727ca7ffd148b73e64b321b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:fc57a2fbc1740965db1c40c59291ef89a6d9f5f235b4d963f4d0602ae0666443
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186249989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b64d1c4d9a958ede215514048d16b164a246beedd0c21e6c59ff3d07f069867`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:14:46 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:14:47 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.16/nats-server-v2.10.16-windows-amd64.zip
# Tue, 21 May 2024 23:14:48 GMT
ENV NATS_SERVER_SHASUM=22a5ef3a54200ebdebaa325822f477c89dc6533ec6fc1f531d897aa876517ccf
# Tue, 21 May 2024 23:15:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 21 May 2024 23:16:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 21 May 2024 23:16:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:16:58 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:16:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:16:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d075cbe94bdd5f06bdabff0ae1baa13ad48a75f808800d9c9cf7d554470d866`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a88d0da7a6579af9c2bdff927235dee0c94b1bfc1cec3787d05218c6a55ec3c`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f922389c5664c8e701d97ef08d1cc52e256e6002e475dacd84e45e12ccaf8cc0`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096dd602404c378351787720a7178c38038189543894dcbe1ce4b5260124b8af`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 445.9 KB (445881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bad7b47779f08ea37f050914a7169eb3be6ad32530159df515b046af95396`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 6.1 MB (6079688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c3b9fbec461537454b31d72f007b18f9d7d0449481a6532b4bc0465145b360`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93647e59b4740ef7e3e440c385dfc114fbae9e7fa990db167023a7040f182a11`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445badc8d13b259ba8343872927775698cdbb81b6013fa153680a9052fea5330`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da65ffc80b4f6a0ef8841c9d2e497145d917917587c49470ad4ca54c6cf78de`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:5b3e38cc7df1ccd71cb1357b316228b34861c6c37727ca7ffd148b73e64b321b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:fc57a2fbc1740965db1c40c59291ef89a6d9f5f235b4d963f4d0602ae0666443
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186249989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b64d1c4d9a958ede215514048d16b164a246beedd0c21e6c59ff3d07f069867`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:14:46 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:14:47 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.16/nats-server-v2.10.16-windows-amd64.zip
# Tue, 21 May 2024 23:14:48 GMT
ENV NATS_SERVER_SHASUM=22a5ef3a54200ebdebaa325822f477c89dc6533ec6fc1f531d897aa876517ccf
# Tue, 21 May 2024 23:15:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 21 May 2024 23:16:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 21 May 2024 23:16:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:16:58 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:16:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:16:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d075cbe94bdd5f06bdabff0ae1baa13ad48a75f808800d9c9cf7d554470d866`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a88d0da7a6579af9c2bdff927235dee0c94b1bfc1cec3787d05218c6a55ec3c`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f922389c5664c8e701d97ef08d1cc52e256e6002e475dacd84e45e12ccaf8cc0`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096dd602404c378351787720a7178c38038189543894dcbe1ce4b5260124b8af`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 445.9 KB (445881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bad7b47779f08ea37f050914a7169eb3be6ad32530159df515b046af95396`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 6.1 MB (6079688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c3b9fbec461537454b31d72f007b18f9d7d0449481a6532b4bc0465145b360`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93647e59b4740ef7e3e440c385dfc114fbae9e7fa990db167023a7040f182a11`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445badc8d13b259ba8343872927775698cdbb81b6013fa153680a9052fea5330`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da65ffc80b4f6a0ef8841c9d2e497145d917917587c49470ad4ca54c6cf78de`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.16`

```console
$ docker pull nats@sha256:c6157cfd07187e8728e1a2a3afe18b63edeb708b78a15fbad9520868b2f0c51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:da851c45cfe95a52ab3e6b013241c2e5271d28f7c0b136f1047c108fbabf859e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2ed2be6ead45418e9fc8d5da88a292fcbb6879e7dcc4db9126a45c5176f6d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:33 GMT
COPY file:0aba91b853d0eaf7d63d52b084d7546996e8db198a221ad2c77a29c916538108 in /nats-server 
# Tue, 21 May 2024 22:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:33 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772a5dc6e4bbb9f932bcf1232f3a7830303a955bbac3775e90153ce66ac9bd8d`  
		Last Modified: Tue, 21 May 2024 22:50:23 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:c655a24000047ea7fc1f1c8c4b1e9c282ac92e2d9706d5aaec92934ab55b72b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb15c7fb2d9a1f5c89f39c7be34daef5e45d98f6454a74e07c7051a7e9223370`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:03:59 GMT
COPY file:ed3148eb9af051d444f42876fc76b54a26455984f4a53bbdf1058b0e11e8b336 in /nats-server 
# Tue, 21 May 2024 23:03:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:03:59 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:59 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:03:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8193d445aa5ad5ea1f96740679c84ff3087a86b1d13258defc8bc3a21f395d18`  
		Last Modified: Tue, 21 May 2024 23:04:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:64d7152e25fd1648d59fe3fda7da9461723b0fa6905b144971bac30def679c99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850b1061eaa54e26469184edc02f606e471c4d9416a0a6bc6068251f90fc0c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:31 GMT
COPY file:dc57eab26dd732b695752b0df8adf307bcbd19553cba75ac3ac2975e7d2cd86f in /nats-server 
# Tue, 21 May 2024 23:21:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:31 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af7d01d01fa2b520a97d19101ea36ea9b96e8124f2fdc1bb7076f976ab01ee`  
		Last Modified: Tue, 21 May 2024 23:22:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16` - linux; ppc64le

```console
$ docker pull nats@sha256:d7f6dd76a8d365ac199d2e1767531fd74bf13cd2c78dba7ac042b8ed1937c4fc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c128c5b164984dd4d70a48c9af0281112501c7ca458ff244d718d50a31dadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:33 GMT
COPY file:e17294dc512d40e8e54498c73c890fd5204a41873c3567f7c18aa532ba727dc3 in /nats-server 
# Tue, 21 May 2024 23:21:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:34 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a45efcc2dc003ec8d53cb55ac8512bb7b4c35bcbd7a761991ef4c1b3147dfd3`  
		Last Modified: Tue, 21 May 2024 23:22:14 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16` - linux; s390x

```console
$ docker pull nats@sha256:a9a0d93cb6a669f0fc2d842220f3a517c5c4ac5b345f0e2dc6aa8267c6fc76a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56c6e37910e564eec4963a6cbe0df805262ea12e504977a860f55fc52a39d05`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:30 GMT
COPY file:359d868ca3e4f687575abd568ad941a9d2682ed2ca604af3309b28b73679d2b7 in /nats-server 
# Tue, 21 May 2024 23:21:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:30 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0c0c15d382278c746e463dce4639563f785a5f07f552c8f5caceb88a87d424`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:958a15d708d62f00bc9918e2283ecab5d12a85d54187bb5301593f33c452a6dc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160734385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bceedc7adb4c9ed6737507c649ee6ff628321a49b2274fbed9b74f50ca19557`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:17:18 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be448c0648b4e415641d5d7504a60f23cb03b4b00b0211021d9fbf697157d4ff`  
		Last Modified: Tue, 21 May 2024 23:18:13 GMT  
		Size: 5.8 MB (5786623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17add0d9ad6ce3c2580f4f65cc11d1d7c6eb572e2df535e9b7d1538394ef668e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c916da7655fd8a5653ae241bc5e9e7657b62c26bce65ae68453896906234d11e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696dcba679ec709b4b8fa95dcd27de7889439d88a304ac3770ac1e6f32f8010c`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4a7a4b5fb58cd41e8b7478c971ce9a63da9d056aed725662939f3f108cc898`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.16-alpine`

```console
$ docker pull nats@sha256:62a623c42f938862130356aae82076ed10c54b8e70dc46557613f002d16c5464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.16-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:1adfb327abdec112e1ef8e07b47a65e9359224a5c2fd6f41d5d37b9674e6f65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14527215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daad98a5ab46e9563fb76d02ee9d0b4a4e520beab7c3a1a8c7b6914115c24170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 22:49:24 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 22:49:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 22:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 22:49:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 22:49:28 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 22:49:28 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 22:49:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c50cc966eb4cbc4a4b881ff20948920be4f45ab8e2cf62ab712cac444395ee`  
		Last Modified: Tue, 21 May 2024 22:50:04 GMT  
		Size: 6.0 MB (5977107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482b47d1cf301cc352bae57642f522722da3324f7b667b1c7ab9a6727d88f527`  
		Last Modified: Tue, 21 May 2024 22:50:03 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9121bc5ccbbd746d1fb23bd55dddbf3d7e34dfc3cb7df700f8ca078f0ec344`  
		Last Modified: Tue, 21 May 2024 22:50:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df155a51d233cc945101d877e9a8d394d4b8114026d50c46107ca509e73414a4`  
		Last Modified: Tue, 21 May 2024 22:50:04 GMT  
		Size: 5.4 MB (5383712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a3f56e81749917f8b07128d633c16d54338fb686f6ddcaa849a23b024cdc62cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14259407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afd587d768a05bc1431c931ab535c88081752285018604a5cae23518073a5fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:03:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:03:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:03:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:03:49 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:03:49 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:03:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e9b04dcae92028f76d8d03593f5da713c1b30e4413f516ac6feb1931c7b2e6`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 6.0 MB (5966263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42806fb40884dc31d08d85dc9811fd14e2d5c8a3f1d355140fe35d2b0e8572`  
		Last Modified: Tue, 21 May 2024 23:04:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da704e6a7abb5014e315123b47670ed2c5da374a12abe0c8a16ac5c00984bc5b`  
		Last Modified: Tue, 21 May 2024 23:04:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2a13bc359472f8406932f00ed1e4a78c2bd57597328886fca2d157b4fd875f`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 5.4 MB (5373248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8e0de73f92a021e34a4a3a2d9fe7db10ea0c5374f6acc4839aafa07f83389a89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14486423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30706d32b39530e9b48913eb6b49e5b607cdf805b5b583ca6a10da052e8c863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:10 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:13 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:13 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e451ccd47ce6074c0eb5a19f953f3cf1b5f7582fa1629fb446c5e98df5bca96b`  
		Last Modified: Tue, 21 May 2024 23:22:04 GMT  
		Size: 5.9 MB (5865815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91c46871a02794fd3e02f3a96648cfe21cc7bba92e4a12880704bc4f5099fa6`  
		Last Modified: Tue, 21 May 2024 23:22:03 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0973b29973a14e29ca26a3bf6ce557a818c454e502f2a1625d12916b94a63c7f`  
		Last Modified: Tue, 21 May 2024 23:22:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d832ebe187b943a16762d91e06cfed3a2af866c23fb50873bc206b8ff64b15`  
		Last Modified: Tue, 21 May 2024 23:22:04 GMT  
		Size: 5.3 MB (5271890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:0b37f107c7121fb4970a680686bf47c0bdc6e221f073948f91fe1ccf935a8069
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14453737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff3f441c8f17081f4726462e440f695fc1f61e1a2f10e242f42e4bd984077bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:08 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:15 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:16 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8c871a04ac5c3a745fc1b9fc0bf0df8eb4429cfc19a6d0c0e5dc82ead6caa5`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.8 MB (5844103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856cdce720d8bce5ea7df85548fc0591d2f54a82aaa905dcf4d5c862d090a59e`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29cb8a321e6c477eee1702a71c5d6712719ebf97439a8e5ce5e98052caa4d73`  
		Last Modified: Tue, 21 May 2024 23:21:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74163ae1a817e733dfe24bdc0793bd29a32f24f194a83320208429d1d8a41355`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.3 MB (5250277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-alpine` - linux; s390x

```console
$ docker pull nats@sha256:6d5ae5c55bd610f20af66cdcb962dc1467df57e229a88bd21e4aa67b0125a4bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14983722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e6fda5c2edf46ae713164e45bc6d3db65c81e9d94751fa2b474f4491b6dee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:19 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:23 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:23 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03de2766ed1b649ad8022c7178d9fb18b54afafd6768b26cc8418bc8ee6ca3`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 6.2 MB (6166358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca420f0a7f6b1e669c0fc2fb845bb3a3e3b5918ae5e6ca274bbe962f098a7c9`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08ad1d4d29a3891a6cef4dd154aebf959965bbae6c2df8f3f88d4d0b617b06f`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e270d0402a827b66e36de07d5f201dc2ad24fdf690b07d53315ef189c7d5aaa`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.6 MB (5573725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.16-alpine3.19`

```console
$ docker pull nats@sha256:62a623c42f938862130356aae82076ed10c54b8e70dc46557613f002d16c5464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.16-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:1adfb327abdec112e1ef8e07b47a65e9359224a5c2fd6f41d5d37b9674e6f65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14527215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daad98a5ab46e9563fb76d02ee9d0b4a4e520beab7c3a1a8c7b6914115c24170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 22:49:24 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 22:49:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 22:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 22:49:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 22:49:28 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 22:49:28 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 22:49:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c50cc966eb4cbc4a4b881ff20948920be4f45ab8e2cf62ab712cac444395ee`  
		Last Modified: Tue, 21 May 2024 22:50:04 GMT  
		Size: 6.0 MB (5977107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482b47d1cf301cc352bae57642f522722da3324f7b667b1c7ab9a6727d88f527`  
		Last Modified: Tue, 21 May 2024 22:50:03 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9121bc5ccbbd746d1fb23bd55dddbf3d7e34dfc3cb7df700f8ca078f0ec344`  
		Last Modified: Tue, 21 May 2024 22:50:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df155a51d233cc945101d877e9a8d394d4b8114026d50c46107ca509e73414a4`  
		Last Modified: Tue, 21 May 2024 22:50:04 GMT  
		Size: 5.4 MB (5383712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:a3f56e81749917f8b07128d633c16d54338fb686f6ddcaa849a23b024cdc62cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14259407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afd587d768a05bc1431c931ab535c88081752285018604a5cae23518073a5fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:03:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:03:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:03:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:03:49 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:03:49 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:03:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e9b04dcae92028f76d8d03593f5da713c1b30e4413f516ac6feb1931c7b2e6`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 6.0 MB (5966263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42806fb40884dc31d08d85dc9811fd14e2d5c8a3f1d355140fe35d2b0e8572`  
		Last Modified: Tue, 21 May 2024 23:04:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da704e6a7abb5014e315123b47670ed2c5da374a12abe0c8a16ac5c00984bc5b`  
		Last Modified: Tue, 21 May 2024 23:04:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2a13bc359472f8406932f00ed1e4a78c2bd57597328886fca2d157b4fd875f`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 5.4 MB (5373248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8e0de73f92a021e34a4a3a2d9fe7db10ea0c5374f6acc4839aafa07f83389a89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14486423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30706d32b39530e9b48913eb6b49e5b607cdf805b5b583ca6a10da052e8c863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:10 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:13 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:13 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e451ccd47ce6074c0eb5a19f953f3cf1b5f7582fa1629fb446c5e98df5bca96b`  
		Last Modified: Tue, 21 May 2024 23:22:04 GMT  
		Size: 5.9 MB (5865815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91c46871a02794fd3e02f3a96648cfe21cc7bba92e4a12880704bc4f5099fa6`  
		Last Modified: Tue, 21 May 2024 23:22:03 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0973b29973a14e29ca26a3bf6ce557a818c454e502f2a1625d12916b94a63c7f`  
		Last Modified: Tue, 21 May 2024 23:22:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d832ebe187b943a16762d91e06cfed3a2af866c23fb50873bc206b8ff64b15`  
		Last Modified: Tue, 21 May 2024 23:22:04 GMT  
		Size: 5.3 MB (5271890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:0b37f107c7121fb4970a680686bf47c0bdc6e221f073948f91fe1ccf935a8069
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14453737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff3f441c8f17081f4726462e440f695fc1f61e1a2f10e242f42e4bd984077bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:08 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:15 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:16 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8c871a04ac5c3a745fc1b9fc0bf0df8eb4429cfc19a6d0c0e5dc82ead6caa5`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.8 MB (5844103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856cdce720d8bce5ea7df85548fc0591d2f54a82aaa905dcf4d5c862d090a59e`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29cb8a321e6c477eee1702a71c5d6712719ebf97439a8e5ce5e98052caa4d73`  
		Last Modified: Tue, 21 May 2024 23:21:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74163ae1a817e733dfe24bdc0793bd29a32f24f194a83320208429d1d8a41355`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.3 MB (5250277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:6d5ae5c55bd610f20af66cdcb962dc1467df57e229a88bd21e4aa67b0125a4bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14983722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e6fda5c2edf46ae713164e45bc6d3db65c81e9d94751fa2b474f4491b6dee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:19 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:23 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:23 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03de2766ed1b649ad8022c7178d9fb18b54afafd6768b26cc8418bc8ee6ca3`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 6.2 MB (6166358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca420f0a7f6b1e669c0fc2fb845bb3a3e3b5918ae5e6ca274bbe962f098a7c9`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08ad1d4d29a3891a6cef4dd154aebf959965bbae6c2df8f3f88d4d0b617b06f`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e270d0402a827b66e36de07d5f201dc2ad24fdf690b07d53315ef189c7d5aaa`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.6 MB (5573725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.16-linux`

```console
$ docker pull nats@sha256:7077c2249d0d2b2e437335db62bf930515467a7683f3cec894eb8ed1c5523abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.16-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:da851c45cfe95a52ab3e6b013241c2e5271d28f7c0b136f1047c108fbabf859e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2ed2be6ead45418e9fc8d5da88a292fcbb6879e7dcc4db9126a45c5176f6d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:33 GMT
COPY file:0aba91b853d0eaf7d63d52b084d7546996e8db198a221ad2c77a29c916538108 in /nats-server 
# Tue, 21 May 2024 22:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:33 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772a5dc6e4bbb9f932bcf1232f3a7830303a955bbac3775e90153ce66ac9bd8d`  
		Last Modified: Tue, 21 May 2024 22:50:23 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:c655a24000047ea7fc1f1c8c4b1e9c282ac92e2d9706d5aaec92934ab55b72b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb15c7fb2d9a1f5c89f39c7be34daef5e45d98f6454a74e07c7051a7e9223370`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:03:59 GMT
COPY file:ed3148eb9af051d444f42876fc76b54a26455984f4a53bbdf1058b0e11e8b336 in /nats-server 
# Tue, 21 May 2024 23:03:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:03:59 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:59 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:03:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8193d445aa5ad5ea1f96740679c84ff3087a86b1d13258defc8bc3a21f395d18`  
		Last Modified: Tue, 21 May 2024 23:04:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:64d7152e25fd1648d59fe3fda7da9461723b0fa6905b144971bac30def679c99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850b1061eaa54e26469184edc02f606e471c4d9416a0a6bc6068251f90fc0c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:31 GMT
COPY file:dc57eab26dd732b695752b0df8adf307bcbd19553cba75ac3ac2975e7d2cd86f in /nats-server 
# Tue, 21 May 2024 23:21:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:31 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af7d01d01fa2b520a97d19101ea36ea9b96e8124f2fdc1bb7076f976ab01ee`  
		Last Modified: Tue, 21 May 2024 23:22:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:d7f6dd76a8d365ac199d2e1767531fd74bf13cd2c78dba7ac042b8ed1937c4fc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c128c5b164984dd4d70a48c9af0281112501c7ca458ff244d718d50a31dadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:33 GMT
COPY file:e17294dc512d40e8e54498c73c890fd5204a41873c3567f7c18aa532ba727dc3 in /nats-server 
# Tue, 21 May 2024 23:21:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:34 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a45efcc2dc003ec8d53cb55ac8512bb7b4c35bcbd7a761991ef4c1b3147dfd3`  
		Last Modified: Tue, 21 May 2024 23:22:14 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-linux` - linux; s390x

```console
$ docker pull nats@sha256:a9a0d93cb6a669f0fc2d842220f3a517c5c4ac5b345f0e2dc6aa8267c6fc76a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56c6e37910e564eec4963a6cbe0df805262ea12e504977a860f55fc52a39d05`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:30 GMT
COPY file:359d868ca3e4f687575abd568ad941a9d2682ed2ca604af3309b28b73679d2b7 in /nats-server 
# Tue, 21 May 2024 23:21:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:30 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0c0c15d382278c746e463dce4639563f785a5f07f552c8f5caceb88a87d424`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.16-nanoserver`

```console
$ docker pull nats@sha256:003d8791c50c4203ecf629af340c97c71cacca7c43091cb6d0b2537d80fbbec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10.16-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:958a15d708d62f00bc9918e2283ecab5d12a85d54187bb5301593f33c452a6dc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160734385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bceedc7adb4c9ed6737507c649ee6ff628321a49b2274fbed9b74f50ca19557`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:17:18 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be448c0648b4e415641d5d7504a60f23cb03b4b00b0211021d9fbf697157d4ff`  
		Last Modified: Tue, 21 May 2024 23:18:13 GMT  
		Size: 5.8 MB (5786623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17add0d9ad6ce3c2580f4f65cc11d1d7c6eb572e2df535e9b7d1538394ef668e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c916da7655fd8a5653ae241bc5e9e7657b62c26bce65ae68453896906234d11e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696dcba679ec709b4b8fa95dcd27de7889439d88a304ac3770ac1e6f32f8010c`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4a7a4b5fb58cd41e8b7478c971ce9a63da9d056aed725662939f3f108cc898`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.16-nanoserver-1809`

```console
$ docker pull nats@sha256:003d8791c50c4203ecf629af340c97c71cacca7c43091cb6d0b2537d80fbbec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10.16-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:958a15d708d62f00bc9918e2283ecab5d12a85d54187bb5301593f33c452a6dc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160734385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bceedc7adb4c9ed6737507c649ee6ff628321a49b2274fbed9b74f50ca19557`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:17:18 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be448c0648b4e415641d5d7504a60f23cb03b4b00b0211021d9fbf697157d4ff`  
		Last Modified: Tue, 21 May 2024 23:18:13 GMT  
		Size: 5.8 MB (5786623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17add0d9ad6ce3c2580f4f65cc11d1d7c6eb572e2df535e9b7d1538394ef668e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c916da7655fd8a5653ae241bc5e9e7657b62c26bce65ae68453896906234d11e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696dcba679ec709b4b8fa95dcd27de7889439d88a304ac3770ac1e6f32f8010c`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4a7a4b5fb58cd41e8b7478c971ce9a63da9d056aed725662939f3f108cc898`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.16-scratch`

```console
$ docker pull nats@sha256:7077c2249d0d2b2e437335db62bf930515467a7683f3cec894eb8ed1c5523abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.16-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:da851c45cfe95a52ab3e6b013241c2e5271d28f7c0b136f1047c108fbabf859e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2ed2be6ead45418e9fc8d5da88a292fcbb6879e7dcc4db9126a45c5176f6d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:33 GMT
COPY file:0aba91b853d0eaf7d63d52b084d7546996e8db198a221ad2c77a29c916538108 in /nats-server 
# Tue, 21 May 2024 22:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:33 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772a5dc6e4bbb9f932bcf1232f3a7830303a955bbac3775e90153ce66ac9bd8d`  
		Last Modified: Tue, 21 May 2024 22:50:23 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:c655a24000047ea7fc1f1c8c4b1e9c282ac92e2d9706d5aaec92934ab55b72b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb15c7fb2d9a1f5c89f39c7be34daef5e45d98f6454a74e07c7051a7e9223370`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:03:59 GMT
COPY file:ed3148eb9af051d444f42876fc76b54a26455984f4a53bbdf1058b0e11e8b336 in /nats-server 
# Tue, 21 May 2024 23:03:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:03:59 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:59 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:03:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8193d445aa5ad5ea1f96740679c84ff3087a86b1d13258defc8bc3a21f395d18`  
		Last Modified: Tue, 21 May 2024 23:04:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:64d7152e25fd1648d59fe3fda7da9461723b0fa6905b144971bac30def679c99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850b1061eaa54e26469184edc02f606e471c4d9416a0a6bc6068251f90fc0c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:31 GMT
COPY file:dc57eab26dd732b695752b0df8adf307bcbd19553cba75ac3ac2975e7d2cd86f in /nats-server 
# Tue, 21 May 2024 23:21:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:31 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af7d01d01fa2b520a97d19101ea36ea9b96e8124f2fdc1bb7076f976ab01ee`  
		Last Modified: Tue, 21 May 2024 23:22:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:d7f6dd76a8d365ac199d2e1767531fd74bf13cd2c78dba7ac042b8ed1937c4fc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c128c5b164984dd4d70a48c9af0281112501c7ca458ff244d718d50a31dadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:33 GMT
COPY file:e17294dc512d40e8e54498c73c890fd5204a41873c3567f7c18aa532ba727dc3 in /nats-server 
# Tue, 21 May 2024 23:21:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:34 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a45efcc2dc003ec8d53cb55ac8512bb7b4c35bcbd7a761991ef4c1b3147dfd3`  
		Last Modified: Tue, 21 May 2024 23:22:14 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-scratch` - linux; s390x

```console
$ docker pull nats@sha256:a9a0d93cb6a669f0fc2d842220f3a517c5c4ac5b345f0e2dc6aa8267c6fc76a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56c6e37910e564eec4963a6cbe0df805262ea12e504977a860f55fc52a39d05`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:30 GMT
COPY file:359d868ca3e4f687575abd568ad941a9d2682ed2ca604af3309b28b73679d2b7 in /nats-server 
# Tue, 21 May 2024 23:21:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:30 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0c0c15d382278c746e463dce4639563f785a5f07f552c8f5caceb88a87d424`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.16-windowsservercore`

```console
$ docker pull nats@sha256:5b3e38cc7df1ccd71cb1357b316228b34861c6c37727ca7ffd148b73e64b321b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10.16-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:fc57a2fbc1740965db1c40c59291ef89a6d9f5f235b4d963f4d0602ae0666443
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186249989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b64d1c4d9a958ede215514048d16b164a246beedd0c21e6c59ff3d07f069867`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:14:46 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:14:47 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.16/nats-server-v2.10.16-windows-amd64.zip
# Tue, 21 May 2024 23:14:48 GMT
ENV NATS_SERVER_SHASUM=22a5ef3a54200ebdebaa325822f477c89dc6533ec6fc1f531d897aa876517ccf
# Tue, 21 May 2024 23:15:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 21 May 2024 23:16:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 21 May 2024 23:16:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:16:58 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:16:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:16:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d075cbe94bdd5f06bdabff0ae1baa13ad48a75f808800d9c9cf7d554470d866`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a88d0da7a6579af9c2bdff927235dee0c94b1bfc1cec3787d05218c6a55ec3c`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f922389c5664c8e701d97ef08d1cc52e256e6002e475dacd84e45e12ccaf8cc0`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096dd602404c378351787720a7178c38038189543894dcbe1ce4b5260124b8af`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 445.9 KB (445881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bad7b47779f08ea37f050914a7169eb3be6ad32530159df515b046af95396`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 6.1 MB (6079688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c3b9fbec461537454b31d72f007b18f9d7d0449481a6532b4bc0465145b360`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93647e59b4740ef7e3e440c385dfc114fbae9e7fa990db167023a7040f182a11`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445badc8d13b259ba8343872927775698cdbb81b6013fa153680a9052fea5330`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da65ffc80b4f6a0ef8841c9d2e497145d917917587c49470ad4ca54c6cf78de`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.16-windowsservercore-1809`

```console
$ docker pull nats@sha256:5b3e38cc7df1ccd71cb1357b316228b34861c6c37727ca7ffd148b73e64b321b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10.16-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:fc57a2fbc1740965db1c40c59291ef89a6d9f5f235b4d963f4d0602ae0666443
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186249989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b64d1c4d9a958ede215514048d16b164a246beedd0c21e6c59ff3d07f069867`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:14:46 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:14:47 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.16/nats-server-v2.10.16-windows-amd64.zip
# Tue, 21 May 2024 23:14:48 GMT
ENV NATS_SERVER_SHASUM=22a5ef3a54200ebdebaa325822f477c89dc6533ec6fc1f531d897aa876517ccf
# Tue, 21 May 2024 23:15:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 21 May 2024 23:16:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 21 May 2024 23:16:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:16:58 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:16:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:16:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d075cbe94bdd5f06bdabff0ae1baa13ad48a75f808800d9c9cf7d554470d866`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a88d0da7a6579af9c2bdff927235dee0c94b1bfc1cec3787d05218c6a55ec3c`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f922389c5664c8e701d97ef08d1cc52e256e6002e475dacd84e45e12ccaf8cc0`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096dd602404c378351787720a7178c38038189543894dcbe1ce4b5260124b8af`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 445.9 KB (445881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bad7b47779f08ea37f050914a7169eb3be6ad32530159df515b046af95396`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 6.1 MB (6079688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c3b9fbec461537454b31d72f007b18f9d7d0449481a6532b4bc0465145b360`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93647e59b4740ef7e3e440c385dfc114fbae9e7fa990db167023a7040f182a11`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445badc8d13b259ba8343872927775698cdbb81b6013fa153680a9052fea5330`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da65ffc80b4f6a0ef8841c9d2e497145d917917587c49470ad4ca54c6cf78de`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:304bed978067ef523d6e3aa77e1f1717b827b8d6c5baf1c78e556cf4d3b12464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9` - linux; amd64

```console
$ docker pull nats@sha256:a2b677be6bd67324258eee1db031ebfd408991ceba89862e17189288c0d0f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765403d3b7754e8f0f9d0c6ae93da0a2297e954b85bca6ec745e84b2d8638fc0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e338e1c824f87e6ce72124da6e3d777f3f418713befd0195137683f46e4e1e`  
		Last Modified: Sat, 16 Mar 2024 08:50:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:e0eeceb084ee407f5fdf2c9ff501e853326762b58edaaac9c93aee7605ea5f77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6917eed10d2cd0036454dee22b532edf61d4b43b6a8d3b1117cc1ce8fe84f0cb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:41 GMT
COPY file:c91938af94e907afc4053e7b9b221c96a3a796390c72aa27e6cdc69cbc2e50fe in /nats-server 
# Tue, 21 May 2024 22:49:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:41 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:41 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac900b7ea4db288a304d6a9a611d1253cbe18116cfadc80ce1d2bbe84295c4c`  
		Last Modified: Tue, 21 May 2024 22:50:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:1b0bd6397add72c741c200daf09367c5d37052523e3621a4baaeb9ab01762b39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4446835dad1b223138d6dd81c214e38af1766720fae74bbf60bf947ac1825a89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:04:08 GMT
COPY file:4166ef26e5f4d76f4236def6255036c2ec16bb0d39069109368691c8c9b07794 in /nats-server 
# Tue, 21 May 2024 23:04:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:04:09 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:04:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:04:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974ae30a1f353a4d0bd00de5a08f9ecc27f144da48d8df53634aa3dac0155ec3`  
		Last Modified: Tue, 21 May 2024 23:05:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a0d9b774f22c54324a0ab4f3655d765b1ac6429f32ef1d1fd3646c01aa2ece6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb8955439c1273916ef09921ad162bb04598d7c76f2e8cb70cbea8ef96aba2a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:40 GMT
COPY file:09d5bdf277f00324c49a245e4c25f7ddb616792eed408850aa1f25fb9c5b29bf in /nats-server 
# Tue, 21 May 2024 23:21:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:41 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:41 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e411bc03a898bad85e270e7b6d6a7fda880cf990361ced51a97cc34cfe8dc59`  
		Last Modified: Tue, 21 May 2024 23:22:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:d42f8a26d0a5aa8d937a907345d86e3f83f23c6e2e122fb73fc7398c93ae0ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:1aea9dab74b20605f294be5bd85d0bc480c031d5e95c17fcf78c0dfaf9d4ae7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd29f2466f179a37884517245d3609223965061df9fbb94a0b4ee45c696ab419`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:49:09 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:49:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:49:13 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:49:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52662615decef836729c27772fd956ed34f2b5a42bc2c0e27b7f1eb8ec6e1dd`  
		Last Modified: Sat, 16 Mar 2024 08:50:12 GMT  
		Size: 5.9 MB (5870718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d9309bea9cbbcb371347e1cfc9015482aa44da15dcc2954ecefce3dd2a50e6`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3d9f573e3a20c89b35599721c0737fae89e39e35012f0b2e821fd4d20afc48`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:afbbbffa03b5dc96d7390ac4a70a9a57f63e46c6ca6eed595657d2cd4211ba2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13776283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998620028feb70288fa193a5c336ae2310c872d048ca529566d133acaa09e885`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:44:39 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:44:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 22:49:38 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 22:49:38 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 22:49:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9137c4a337449facc87ef5ee3665c96a549e6e3536ae94d4299bcbc6dfdea7b2`  
		Last Modified: Sat, 16 Mar 2024 08:45:41 GMT  
		Size: 5.6 MB (5607208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a13df67924e990510d98bc0085d0395451ccb1c5d874eeb4f25a87bdba9e01`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64427c3156bb49e3065365fe9f79f632a084854abe87577aab4f8bf4575330cc`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea3a2b188d2dc5d13fae4c7b0ac5a419dfdad99ae0922d41a708b1d96166b6c`  
		Last Modified: Tue, 21 May 2024 22:50:43 GMT  
		Size: 5.0 MB (5021016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b4526301fb3191e0862d578ad6228345b3ff7033384cba66a79072ab6ade32e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13517737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0c353f9c3cfc12c6d9045047479df07add8babff08fce917ecaf733aa8bb79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:53:27 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 00:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:04:03 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:04:03 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:04:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:04:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd76eaf9560c3a02d86b302defb4b6b8a8a7ee892505b05ac0ab7ac9038c1a7`  
		Last Modified: Sat, 16 Mar 2024 00:54:35 GMT  
		Size: 5.6 MB (5599769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6e0adcaf71449171b6cbe6d69146a1af1cb15863f657f1c08562110247555e`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5a74349ed6863e93d568b2c4cf9cd67c565717d30af0148dcfb2cc8a41891`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b19508e6e23c4078402907516b8443810d87a28ad0765a959af1c910de98c5`  
		Last Modified: Tue, 21 May 2024 23:05:14 GMT  
		Size: 5.0 MB (5015574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:725039dde6d59314ae6e7c9137dae8f02abd58094da728e7a80875f599ca1b62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13565532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591f330fd0dde446fcf9661ccb63f7e02496c0f99dcd4ec95175191f39829ff3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 04:04:12 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 04:04:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:37 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:37 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3560e79b148c5e98949b1f08ed73634c8c7826d700277cf260bf3cb6d5f00d`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 5.4 MB (5408722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b5e756dbfadc026b321fece391fa35f53130fa5c59ebb201fddb9a745238e8`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ad59f09b7cfe9ed625b71c2f8de7ab974a5db023d95fbe97fa8c2d36077d09`  
		Last Modified: Sat, 16 Mar 2024 04:05:13 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60955e77e334955d10424a95224aa3b42d40215470d1f7318631cc18f37abdc`  
		Last Modified: Tue, 21 May 2024 23:22:43 GMT  
		Size: 4.8 MB (4822451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.18`

```console
$ docker pull nats@sha256:d42f8a26d0a5aa8d937a907345d86e3f83f23c6e2e122fb73fc7398c93ae0ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:1aea9dab74b20605f294be5bd85d0bc480c031d5e95c17fcf78c0dfaf9d4ae7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd29f2466f179a37884517245d3609223965061df9fbb94a0b4ee45c696ab419`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:49:09 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:49:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:49:13 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:49:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52662615decef836729c27772fd956ed34f2b5a42bc2c0e27b7f1eb8ec6e1dd`  
		Last Modified: Sat, 16 Mar 2024 08:50:12 GMT  
		Size: 5.9 MB (5870718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d9309bea9cbbcb371347e1cfc9015482aa44da15dcc2954ecefce3dd2a50e6`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3d9f573e3a20c89b35599721c0737fae89e39e35012f0b2e821fd4d20afc48`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:afbbbffa03b5dc96d7390ac4a70a9a57f63e46c6ca6eed595657d2cd4211ba2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13776283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998620028feb70288fa193a5c336ae2310c872d048ca529566d133acaa09e885`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:44:39 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:44:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 22:49:38 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 22:49:38 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 22:49:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9137c4a337449facc87ef5ee3665c96a549e6e3536ae94d4299bcbc6dfdea7b2`  
		Last Modified: Sat, 16 Mar 2024 08:45:41 GMT  
		Size: 5.6 MB (5607208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a13df67924e990510d98bc0085d0395451ccb1c5d874eeb4f25a87bdba9e01`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64427c3156bb49e3065365fe9f79f632a084854abe87577aab4f8bf4575330cc`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea3a2b188d2dc5d13fae4c7b0ac5a419dfdad99ae0922d41a708b1d96166b6c`  
		Last Modified: Tue, 21 May 2024 22:50:43 GMT  
		Size: 5.0 MB (5021016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:b4526301fb3191e0862d578ad6228345b3ff7033384cba66a79072ab6ade32e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13517737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0c353f9c3cfc12c6d9045047479df07add8babff08fce917ecaf733aa8bb79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:53:27 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 00:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:04:03 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:04:03 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:04:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:04:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd76eaf9560c3a02d86b302defb4b6b8a8a7ee892505b05ac0ab7ac9038c1a7`  
		Last Modified: Sat, 16 Mar 2024 00:54:35 GMT  
		Size: 5.6 MB (5599769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6e0adcaf71449171b6cbe6d69146a1af1cb15863f657f1c08562110247555e`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5a74349ed6863e93d568b2c4cf9cd67c565717d30af0148dcfb2cc8a41891`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b19508e6e23c4078402907516b8443810d87a28ad0765a959af1c910de98c5`  
		Last Modified: Tue, 21 May 2024 23:05:14 GMT  
		Size: 5.0 MB (5015574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:725039dde6d59314ae6e7c9137dae8f02abd58094da728e7a80875f599ca1b62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13565532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591f330fd0dde446fcf9661ccb63f7e02496c0f99dcd4ec95175191f39829ff3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 04:04:12 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 04:04:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:37 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:37 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3560e79b148c5e98949b1f08ed73634c8c7826d700277cf260bf3cb6d5f00d`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 5.4 MB (5408722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b5e756dbfadc026b321fece391fa35f53130fa5c59ebb201fddb9a745238e8`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ad59f09b7cfe9ed625b71c2f8de7ab974a5db023d95fbe97fa8c2d36077d09`  
		Last Modified: Sat, 16 Mar 2024 04:05:13 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60955e77e334955d10424a95224aa3b42d40215470d1f7318631cc18f37abdc`  
		Last Modified: Tue, 21 May 2024 23:22:43 GMT  
		Size: 4.8 MB (4822451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:304bed978067ef523d6e3aa77e1f1717b827b8d6c5baf1c78e556cf4d3b12464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:a2b677be6bd67324258eee1db031ebfd408991ceba89862e17189288c0d0f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765403d3b7754e8f0f9d0c6ae93da0a2297e954b85bca6ec745e84b2d8638fc0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e338e1c824f87e6ce72124da6e3d777f3f418713befd0195137683f46e4e1e`  
		Last Modified: Sat, 16 Mar 2024 08:50:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:e0eeceb084ee407f5fdf2c9ff501e853326762b58edaaac9c93aee7605ea5f77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6917eed10d2cd0036454dee22b532edf61d4b43b6a8d3b1117cc1ce8fe84f0cb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:41 GMT
COPY file:c91938af94e907afc4053e7b9b221c96a3a796390c72aa27e6cdc69cbc2e50fe in /nats-server 
# Tue, 21 May 2024 22:49:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:41 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:41 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac900b7ea4db288a304d6a9a611d1253cbe18116cfadc80ce1d2bbe84295c4c`  
		Last Modified: Tue, 21 May 2024 22:50:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:1b0bd6397add72c741c200daf09367c5d37052523e3621a4baaeb9ab01762b39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4446835dad1b223138d6dd81c214e38af1766720fae74bbf60bf947ac1825a89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:04:08 GMT
COPY file:4166ef26e5f4d76f4236def6255036c2ec16bb0d39069109368691c8c9b07794 in /nats-server 
# Tue, 21 May 2024 23:04:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:04:09 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:04:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:04:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974ae30a1f353a4d0bd00de5a08f9ecc27f144da48d8df53634aa3dac0155ec3`  
		Last Modified: Tue, 21 May 2024 23:05:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a0d9b774f22c54324a0ab4f3655d765b1ac6429f32ef1d1fd3646c01aa2ece6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb8955439c1273916ef09921ad162bb04598d7c76f2e8cb70cbea8ef96aba2a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:40 GMT
COPY file:09d5bdf277f00324c49a245e4c25f7ddb616792eed408850aa1f25fb9c5b29bf in /nats-server 
# Tue, 21 May 2024 23:21:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:41 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:41 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e411bc03a898bad85e270e7b6d6a7fda880cf990361ced51a97cc34cfe8dc59`  
		Last Modified: Tue, 21 May 2024 23:22:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver`

```console
$ docker pull nats@sha256:8b8699adecfb4e2088dc8cc3dbd27fbdeb02a6d9a8cfc3f94eb134a5cfb27085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:5caa448ed8d0d2681eccfda619261ba7fed209e3192080f5c22afdf65c5a7985
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160278012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f476e3e4260dc494484d8f4202d52f0ae5ff49dbea1c915fcbf7056ac4917158`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:12:43 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 15 May 2024 21:12:44 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:12:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:12:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:12:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f6907cb5ae64d5580cc2ed0c53877b5a15073904eb506586822016671ca762`  
		Last Modified: Wed, 15 May 2024 21:13:59 GMT  
		Size: 5.3 MB (5330226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cec024febaaea2c85546b54fb6fd50962237c51b4e58a0b02a2256064133da`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5015bfc52f47ca9a764991cd8418e81e26d703a8f2236ec898e3c6cb198577`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2480d004d8c19f4e5ee9979ad207627882d4aa001160082a0242da6ce84dc5`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de69389d566bdac0778f7de71a98be01137b5e20527e8561831e8345143bc73d`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:8b8699adecfb4e2088dc8cc3dbd27fbdeb02a6d9a8cfc3f94eb134a5cfb27085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:5caa448ed8d0d2681eccfda619261ba7fed209e3192080f5c22afdf65c5a7985
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160278012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f476e3e4260dc494484d8f4202d52f0ae5ff49dbea1c915fcbf7056ac4917158`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:12:43 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 15 May 2024 21:12:44 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:12:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:12:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:12:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f6907cb5ae64d5580cc2ed0c53877b5a15073904eb506586822016671ca762`  
		Last Modified: Wed, 15 May 2024 21:13:59 GMT  
		Size: 5.3 MB (5330226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cec024febaaea2c85546b54fb6fd50962237c51b4e58a0b02a2256064133da`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5015bfc52f47ca9a764991cd8418e81e26d703a8f2236ec898e3c6cb198577`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2480d004d8c19f4e5ee9979ad207627882d4aa001160082a0242da6ce84dc5`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de69389d566bdac0778f7de71a98be01137b5e20527e8561831e8345143bc73d`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:304bed978067ef523d6e3aa77e1f1717b827b8d6c5baf1c78e556cf4d3b12464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:a2b677be6bd67324258eee1db031ebfd408991ceba89862e17189288c0d0f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765403d3b7754e8f0f9d0c6ae93da0a2297e954b85bca6ec745e84b2d8638fc0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e338e1c824f87e6ce72124da6e3d777f3f418713befd0195137683f46e4e1e`  
		Last Modified: Sat, 16 Mar 2024 08:50:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:e0eeceb084ee407f5fdf2c9ff501e853326762b58edaaac9c93aee7605ea5f77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6917eed10d2cd0036454dee22b532edf61d4b43b6a8d3b1117cc1ce8fe84f0cb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:41 GMT
COPY file:c91938af94e907afc4053e7b9b221c96a3a796390c72aa27e6cdc69cbc2e50fe in /nats-server 
# Tue, 21 May 2024 22:49:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:41 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:41 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac900b7ea4db288a304d6a9a611d1253cbe18116cfadc80ce1d2bbe84295c4c`  
		Last Modified: Tue, 21 May 2024 22:50:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:1b0bd6397add72c741c200daf09367c5d37052523e3621a4baaeb9ab01762b39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4446835dad1b223138d6dd81c214e38af1766720fae74bbf60bf947ac1825a89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:04:08 GMT
COPY file:4166ef26e5f4d76f4236def6255036c2ec16bb0d39069109368691c8c9b07794 in /nats-server 
# Tue, 21 May 2024 23:04:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:04:09 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:04:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:04:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974ae30a1f353a4d0bd00de5a08f9ecc27f144da48d8df53634aa3dac0155ec3`  
		Last Modified: Tue, 21 May 2024 23:05:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a0d9b774f22c54324a0ab4f3655d765b1ac6429f32ef1d1fd3646c01aa2ece6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb8955439c1273916ef09921ad162bb04598d7c76f2e8cb70cbea8ef96aba2a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:40 GMT
COPY file:09d5bdf277f00324c49a245e4c25f7ddb616792eed408850aa1f25fb9c5b29bf in /nats-server 
# Tue, 21 May 2024 23:21:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:41 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:41 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e411bc03a898bad85e270e7b6d6a7fda880cf990361ced51a97cc34cfe8dc59`  
		Last Modified: Tue, 21 May 2024 23:22:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore`

```console
$ docker pull nats@sha256:d105a2aec5d7607b2d64b7e727bb299d6639906b90f65c62aec1c023646fb629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:d6c8ef52baefbd23d260c0968de8a3a9e623c5a1e6c1c084fc4cc9c4bd083955
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2185759588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fc18a9a5bd3a99e5270cd5ccbb602d851b0d82af6fc71a20f0f9e988882048`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:09:07 GMT
ENV NATS_SERVER=2.9.25
# Wed, 15 May 2024 21:09:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 15 May 2024 21:09:09 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 15 May 2024 21:10:23 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 May 2024 21:12:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 15 May 2024 21:12:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:12:20 GMT
EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:12:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:12:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89ee38c395afa6a56d89d2fb6a4e4416a29532867ac749ed891d8afbcda1135`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849d3d89dda77cca52a136f7b2efd5d49db6a15023779c247271b88e617af134`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495bf4363371aaf97d2f904389bb10eaa3084ae31144835f977ff70ff65cbfa8`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29960b46711d8942c7067c001f2cf2da2e307d07df0496e770982e7a94dd1885`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 432.5 KB (432533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b49209267b4fe2543a0f5fa467f5ca0fa4d48b310dd00a04976d3ca886bc8f`  
		Last Modified: Wed, 15 May 2024 21:13:47 GMT  
		Size: 5.6 MB (5602269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67580450fcb49521ca804f4b54bd2bd07ebc4f3263724a69998c832ae9983d9e`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c707e65fefffaaeb1d096da9ef99da0eb845614c50f044b8352cd2ae8534b39e`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97529e380ed09b82c2db2acc2e2135a082f3dfc94d51d32058a554fa0fe35067`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a52fda9fb0314e5eb96e601bc6d393b2e5d480a135c2ffb1de54122fb9e5fee`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:d105a2aec5d7607b2d64b7e727bb299d6639906b90f65c62aec1c023646fb629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:d6c8ef52baefbd23d260c0968de8a3a9e623c5a1e6c1c084fc4cc9c4bd083955
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2185759588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fc18a9a5bd3a99e5270cd5ccbb602d851b0d82af6fc71a20f0f9e988882048`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:09:07 GMT
ENV NATS_SERVER=2.9.25
# Wed, 15 May 2024 21:09:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 15 May 2024 21:09:09 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 15 May 2024 21:10:23 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 May 2024 21:12:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 15 May 2024 21:12:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:12:20 GMT
EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:12:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:12:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89ee38c395afa6a56d89d2fb6a4e4416a29532867ac749ed891d8afbcda1135`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849d3d89dda77cca52a136f7b2efd5d49db6a15023779c247271b88e617af134`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495bf4363371aaf97d2f904389bb10eaa3084ae31144835f977ff70ff65cbfa8`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29960b46711d8942c7067c001f2cf2da2e307d07df0496e770982e7a94dd1885`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 432.5 KB (432533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b49209267b4fe2543a0f5fa467f5ca0fa4d48b310dd00a04976d3ca886bc8f`  
		Last Modified: Wed, 15 May 2024 21:13:47 GMT  
		Size: 5.6 MB (5602269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67580450fcb49521ca804f4b54bd2bd07ebc4f3263724a69998c832ae9983d9e`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c707e65fefffaaeb1d096da9ef99da0eb845614c50f044b8352cd2ae8534b39e`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97529e380ed09b82c2db2acc2e2135a082f3dfc94d51d32058a554fa0fe35067`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a52fda9fb0314e5eb96e601bc6d393b2e5d480a135c2ffb1de54122fb9e5fee`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25`

```console
$ docker pull nats@sha256:304bed978067ef523d6e3aa77e1f1717b827b8d6c5baf1c78e556cf4d3b12464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25` - linux; amd64

```console
$ docker pull nats@sha256:a2b677be6bd67324258eee1db031ebfd408991ceba89862e17189288c0d0f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765403d3b7754e8f0f9d0c6ae93da0a2297e954b85bca6ec745e84b2d8638fc0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e338e1c824f87e6ce72124da6e3d777f3f418713befd0195137683f46e4e1e`  
		Last Modified: Sat, 16 Mar 2024 08:50:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25` - linux; arm variant v6

```console
$ docker pull nats@sha256:e0eeceb084ee407f5fdf2c9ff501e853326762b58edaaac9c93aee7605ea5f77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6917eed10d2cd0036454dee22b532edf61d4b43b6a8d3b1117cc1ce8fe84f0cb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:41 GMT
COPY file:c91938af94e907afc4053e7b9b221c96a3a796390c72aa27e6cdc69cbc2e50fe in /nats-server 
# Tue, 21 May 2024 22:49:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:41 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:41 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac900b7ea4db288a304d6a9a611d1253cbe18116cfadc80ce1d2bbe84295c4c`  
		Last Modified: Tue, 21 May 2024 22:50:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25` - linux; arm variant v7

```console
$ docker pull nats@sha256:1b0bd6397add72c741c200daf09367c5d37052523e3621a4baaeb9ab01762b39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4446835dad1b223138d6dd81c214e38af1766720fae74bbf60bf947ac1825a89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:04:08 GMT
COPY file:4166ef26e5f4d76f4236def6255036c2ec16bb0d39069109368691c8c9b07794 in /nats-server 
# Tue, 21 May 2024 23:04:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:04:09 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:04:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:04:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974ae30a1f353a4d0bd00de5a08f9ecc27f144da48d8df53634aa3dac0155ec3`  
		Last Modified: Tue, 21 May 2024 23:05:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a0d9b774f22c54324a0ab4f3655d765b1ac6429f32ef1d1fd3646c01aa2ece6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb8955439c1273916ef09921ad162bb04598d7c76f2e8cb70cbea8ef96aba2a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:40 GMT
COPY file:09d5bdf277f00324c49a245e4c25f7ddb616792eed408850aa1f25fb9c5b29bf in /nats-server 
# Tue, 21 May 2024 23:21:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:41 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:41 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e411bc03a898bad85e270e7b6d6a7fda880cf990361ced51a97cc34cfe8dc59`  
		Last Modified: Tue, 21 May 2024 23:22:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-alpine`

```console
$ docker pull nats@sha256:d42f8a26d0a5aa8d937a907345d86e3f83f23c6e2e122fb73fc7398c93ae0ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-alpine` - linux; amd64

```console
$ docker pull nats@sha256:1aea9dab74b20605f294be5bd85d0bc480c031d5e95c17fcf78c0dfaf9d4ae7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd29f2466f179a37884517245d3609223965061df9fbb94a0b4ee45c696ab419`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:49:09 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:49:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:49:13 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:49:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52662615decef836729c27772fd956ed34f2b5a42bc2c0e27b7f1eb8ec6e1dd`  
		Last Modified: Sat, 16 Mar 2024 08:50:12 GMT  
		Size: 5.9 MB (5870718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d9309bea9cbbcb371347e1cfc9015482aa44da15dcc2954ecefce3dd2a50e6`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3d9f573e3a20c89b35599721c0737fae89e39e35012f0b2e821fd4d20afc48`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:afbbbffa03b5dc96d7390ac4a70a9a57f63e46c6ca6eed595657d2cd4211ba2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13776283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998620028feb70288fa193a5c336ae2310c872d048ca529566d133acaa09e885`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:44:39 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:44:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 22:49:38 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 22:49:38 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 22:49:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9137c4a337449facc87ef5ee3665c96a549e6e3536ae94d4299bcbc6dfdea7b2`  
		Last Modified: Sat, 16 Mar 2024 08:45:41 GMT  
		Size: 5.6 MB (5607208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a13df67924e990510d98bc0085d0395451ccb1c5d874eeb4f25a87bdba9e01`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64427c3156bb49e3065365fe9f79f632a084854abe87577aab4f8bf4575330cc`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea3a2b188d2dc5d13fae4c7b0ac5a419dfdad99ae0922d41a708b1d96166b6c`  
		Last Modified: Tue, 21 May 2024 22:50:43 GMT  
		Size: 5.0 MB (5021016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b4526301fb3191e0862d578ad6228345b3ff7033384cba66a79072ab6ade32e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13517737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0c353f9c3cfc12c6d9045047479df07add8babff08fce917ecaf733aa8bb79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:53:27 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 00:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:04:03 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:04:03 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:04:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:04:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd76eaf9560c3a02d86b302defb4b6b8a8a7ee892505b05ac0ab7ac9038c1a7`  
		Last Modified: Sat, 16 Mar 2024 00:54:35 GMT  
		Size: 5.6 MB (5599769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6e0adcaf71449171b6cbe6d69146a1af1cb15863f657f1c08562110247555e`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5a74349ed6863e93d568b2c4cf9cd67c565717d30af0148dcfb2cc8a41891`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b19508e6e23c4078402907516b8443810d87a28ad0765a959af1c910de98c5`  
		Last Modified: Tue, 21 May 2024 23:05:14 GMT  
		Size: 5.0 MB (5015574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:725039dde6d59314ae6e7c9137dae8f02abd58094da728e7a80875f599ca1b62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13565532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591f330fd0dde446fcf9661ccb63f7e02496c0f99dcd4ec95175191f39829ff3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 04:04:12 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 04:04:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:37 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:37 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3560e79b148c5e98949b1f08ed73634c8c7826d700277cf260bf3cb6d5f00d`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 5.4 MB (5408722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b5e756dbfadc026b321fece391fa35f53130fa5c59ebb201fddb9a745238e8`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ad59f09b7cfe9ed625b71c2f8de7ab974a5db023d95fbe97fa8c2d36077d09`  
		Last Modified: Sat, 16 Mar 2024 04:05:13 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60955e77e334955d10424a95224aa3b42d40215470d1f7318631cc18f37abdc`  
		Last Modified: Tue, 21 May 2024 23:22:43 GMT  
		Size: 4.8 MB (4822451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-alpine3.18`

```console
$ docker pull nats@sha256:d42f8a26d0a5aa8d937a907345d86e3f83f23c6e2e122fb73fc7398c93ae0ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:1aea9dab74b20605f294be5bd85d0bc480c031d5e95c17fcf78c0dfaf9d4ae7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd29f2466f179a37884517245d3609223965061df9fbb94a0b4ee45c696ab419`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:49:09 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:49:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:49:13 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:49:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52662615decef836729c27772fd956ed34f2b5a42bc2c0e27b7f1eb8ec6e1dd`  
		Last Modified: Sat, 16 Mar 2024 08:50:12 GMT  
		Size: 5.9 MB (5870718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d9309bea9cbbcb371347e1cfc9015482aa44da15dcc2954ecefce3dd2a50e6`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3d9f573e3a20c89b35599721c0737fae89e39e35012f0b2e821fd4d20afc48`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:afbbbffa03b5dc96d7390ac4a70a9a57f63e46c6ca6eed595657d2cd4211ba2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13776283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998620028feb70288fa193a5c336ae2310c872d048ca529566d133acaa09e885`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:44:39 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:44:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 22:49:38 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 22:49:38 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 22:49:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9137c4a337449facc87ef5ee3665c96a549e6e3536ae94d4299bcbc6dfdea7b2`  
		Last Modified: Sat, 16 Mar 2024 08:45:41 GMT  
		Size: 5.6 MB (5607208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a13df67924e990510d98bc0085d0395451ccb1c5d874eeb4f25a87bdba9e01`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64427c3156bb49e3065365fe9f79f632a084854abe87577aab4f8bf4575330cc`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea3a2b188d2dc5d13fae4c7b0ac5a419dfdad99ae0922d41a708b1d96166b6c`  
		Last Modified: Tue, 21 May 2024 22:50:43 GMT  
		Size: 5.0 MB (5021016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:b4526301fb3191e0862d578ad6228345b3ff7033384cba66a79072ab6ade32e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13517737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0c353f9c3cfc12c6d9045047479df07add8babff08fce917ecaf733aa8bb79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:53:27 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 00:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:04:03 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:04:03 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:04:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:04:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd76eaf9560c3a02d86b302defb4b6b8a8a7ee892505b05ac0ab7ac9038c1a7`  
		Last Modified: Sat, 16 Mar 2024 00:54:35 GMT  
		Size: 5.6 MB (5599769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6e0adcaf71449171b6cbe6d69146a1af1cb15863f657f1c08562110247555e`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5a74349ed6863e93d568b2c4cf9cd67c565717d30af0148dcfb2cc8a41891`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b19508e6e23c4078402907516b8443810d87a28ad0765a959af1c910de98c5`  
		Last Modified: Tue, 21 May 2024 23:05:14 GMT  
		Size: 5.0 MB (5015574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:725039dde6d59314ae6e7c9137dae8f02abd58094da728e7a80875f599ca1b62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13565532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591f330fd0dde446fcf9661ccb63f7e02496c0f99dcd4ec95175191f39829ff3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 04:04:12 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 04:04:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:37 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:37 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3560e79b148c5e98949b1f08ed73634c8c7826d700277cf260bf3cb6d5f00d`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 5.4 MB (5408722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b5e756dbfadc026b321fece391fa35f53130fa5c59ebb201fddb9a745238e8`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ad59f09b7cfe9ed625b71c2f8de7ab974a5db023d95fbe97fa8c2d36077d09`  
		Last Modified: Sat, 16 Mar 2024 04:05:13 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60955e77e334955d10424a95224aa3b42d40215470d1f7318631cc18f37abdc`  
		Last Modified: Tue, 21 May 2024 23:22:43 GMT  
		Size: 4.8 MB (4822451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-linux`

```console
$ docker pull nats@sha256:304bed978067ef523d6e3aa77e1f1717b827b8d6c5baf1c78e556cf4d3b12464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-linux` - linux; amd64

```console
$ docker pull nats@sha256:a2b677be6bd67324258eee1db031ebfd408991ceba89862e17189288c0d0f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765403d3b7754e8f0f9d0c6ae93da0a2297e954b85bca6ec745e84b2d8638fc0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e338e1c824f87e6ce72124da6e3d777f3f418713befd0195137683f46e4e1e`  
		Last Modified: Sat, 16 Mar 2024 08:50:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:e0eeceb084ee407f5fdf2c9ff501e853326762b58edaaac9c93aee7605ea5f77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6917eed10d2cd0036454dee22b532edf61d4b43b6a8d3b1117cc1ce8fe84f0cb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:41 GMT
COPY file:c91938af94e907afc4053e7b9b221c96a3a796390c72aa27e6cdc69cbc2e50fe in /nats-server 
# Tue, 21 May 2024 22:49:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:41 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:41 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac900b7ea4db288a304d6a9a611d1253cbe18116cfadc80ce1d2bbe84295c4c`  
		Last Modified: Tue, 21 May 2024 22:50:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:1b0bd6397add72c741c200daf09367c5d37052523e3621a4baaeb9ab01762b39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4446835dad1b223138d6dd81c214e38af1766720fae74bbf60bf947ac1825a89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:04:08 GMT
COPY file:4166ef26e5f4d76f4236def6255036c2ec16bb0d39069109368691c8c9b07794 in /nats-server 
# Tue, 21 May 2024 23:04:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:04:09 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:04:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:04:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974ae30a1f353a4d0bd00de5a08f9ecc27f144da48d8df53634aa3dac0155ec3`  
		Last Modified: Tue, 21 May 2024 23:05:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a0d9b774f22c54324a0ab4f3655d765b1ac6429f32ef1d1fd3646c01aa2ece6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb8955439c1273916ef09921ad162bb04598d7c76f2e8cb70cbea8ef96aba2a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:40 GMT
COPY file:09d5bdf277f00324c49a245e4c25f7ddb616792eed408850aa1f25fb9c5b29bf in /nats-server 
# Tue, 21 May 2024 23:21:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:41 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:41 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e411bc03a898bad85e270e7b6d6a7fda880cf990361ced51a97cc34cfe8dc59`  
		Last Modified: Tue, 21 May 2024 23:22:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-nanoserver`

```console
$ docker pull nats@sha256:8b8699adecfb4e2088dc8cc3dbd27fbdeb02a6d9a8cfc3f94eb134a5cfb27085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.9.25-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:5caa448ed8d0d2681eccfda619261ba7fed209e3192080f5c22afdf65c5a7985
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160278012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f476e3e4260dc494484d8f4202d52f0ae5ff49dbea1c915fcbf7056ac4917158`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:12:43 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 15 May 2024 21:12:44 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:12:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:12:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:12:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f6907cb5ae64d5580cc2ed0c53877b5a15073904eb506586822016671ca762`  
		Last Modified: Wed, 15 May 2024 21:13:59 GMT  
		Size: 5.3 MB (5330226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cec024febaaea2c85546b54fb6fd50962237c51b4e58a0b02a2256064133da`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5015bfc52f47ca9a764991cd8418e81e26d703a8f2236ec898e3c6cb198577`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2480d004d8c19f4e5ee9979ad207627882d4aa001160082a0242da6ce84dc5`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de69389d566bdac0778f7de71a98be01137b5e20527e8561831e8345143bc73d`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-nanoserver-1809`

```console
$ docker pull nats@sha256:8b8699adecfb4e2088dc8cc3dbd27fbdeb02a6d9a8cfc3f94eb134a5cfb27085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.9.25-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:5caa448ed8d0d2681eccfda619261ba7fed209e3192080f5c22afdf65c5a7985
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160278012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f476e3e4260dc494484d8f4202d52f0ae5ff49dbea1c915fcbf7056ac4917158`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:12:43 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 15 May 2024 21:12:44 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:12:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:12:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:12:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f6907cb5ae64d5580cc2ed0c53877b5a15073904eb506586822016671ca762`  
		Last Modified: Wed, 15 May 2024 21:13:59 GMT  
		Size: 5.3 MB (5330226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cec024febaaea2c85546b54fb6fd50962237c51b4e58a0b02a2256064133da`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5015bfc52f47ca9a764991cd8418e81e26d703a8f2236ec898e3c6cb198577`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2480d004d8c19f4e5ee9979ad207627882d4aa001160082a0242da6ce84dc5`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de69389d566bdac0778f7de71a98be01137b5e20527e8561831e8345143bc73d`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-scratch`

```console
$ docker pull nats@sha256:304bed978067ef523d6e3aa77e1f1717b827b8d6c5baf1c78e556cf4d3b12464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-scratch` - linux; amd64

```console
$ docker pull nats@sha256:a2b677be6bd67324258eee1db031ebfd408991ceba89862e17189288c0d0f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765403d3b7754e8f0f9d0c6ae93da0a2297e954b85bca6ec745e84b2d8638fc0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e338e1c824f87e6ce72124da6e3d777f3f418713befd0195137683f46e4e1e`  
		Last Modified: Sat, 16 Mar 2024 08:50:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:e0eeceb084ee407f5fdf2c9ff501e853326762b58edaaac9c93aee7605ea5f77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6917eed10d2cd0036454dee22b532edf61d4b43b6a8d3b1117cc1ce8fe84f0cb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:41 GMT
COPY file:c91938af94e907afc4053e7b9b221c96a3a796390c72aa27e6cdc69cbc2e50fe in /nats-server 
# Tue, 21 May 2024 22:49:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:41 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:41 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac900b7ea4db288a304d6a9a611d1253cbe18116cfadc80ce1d2bbe84295c4c`  
		Last Modified: Tue, 21 May 2024 22:50:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:1b0bd6397add72c741c200daf09367c5d37052523e3621a4baaeb9ab01762b39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4446835dad1b223138d6dd81c214e38af1766720fae74bbf60bf947ac1825a89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:04:08 GMT
COPY file:4166ef26e5f4d76f4236def6255036c2ec16bb0d39069109368691c8c9b07794 in /nats-server 
# Tue, 21 May 2024 23:04:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:04:09 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:04:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:04:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974ae30a1f353a4d0bd00de5a08f9ecc27f144da48d8df53634aa3dac0155ec3`  
		Last Modified: Tue, 21 May 2024 23:05:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a0d9b774f22c54324a0ab4f3655d765b1ac6429f32ef1d1fd3646c01aa2ece6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb8955439c1273916ef09921ad162bb04598d7c76f2e8cb70cbea8ef96aba2a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:40 GMT
COPY file:09d5bdf277f00324c49a245e4c25f7ddb616792eed408850aa1f25fb9c5b29bf in /nats-server 
# Tue, 21 May 2024 23:21:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:41 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:41 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e411bc03a898bad85e270e7b6d6a7fda880cf990361ced51a97cc34cfe8dc59`  
		Last Modified: Tue, 21 May 2024 23:22:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-windowsservercore`

```console
$ docker pull nats@sha256:d105a2aec5d7607b2d64b7e727bb299d6639906b90f65c62aec1c023646fb629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.9.25-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:d6c8ef52baefbd23d260c0968de8a3a9e623c5a1e6c1c084fc4cc9c4bd083955
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2185759588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fc18a9a5bd3a99e5270cd5ccbb602d851b0d82af6fc71a20f0f9e988882048`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:09:07 GMT
ENV NATS_SERVER=2.9.25
# Wed, 15 May 2024 21:09:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 15 May 2024 21:09:09 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 15 May 2024 21:10:23 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 May 2024 21:12:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 15 May 2024 21:12:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:12:20 GMT
EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:12:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:12:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89ee38c395afa6a56d89d2fb6a4e4416a29532867ac749ed891d8afbcda1135`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849d3d89dda77cca52a136f7b2efd5d49db6a15023779c247271b88e617af134`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495bf4363371aaf97d2f904389bb10eaa3084ae31144835f977ff70ff65cbfa8`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29960b46711d8942c7067c001f2cf2da2e307d07df0496e770982e7a94dd1885`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 432.5 KB (432533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b49209267b4fe2543a0f5fa467f5ca0fa4d48b310dd00a04976d3ca886bc8f`  
		Last Modified: Wed, 15 May 2024 21:13:47 GMT  
		Size: 5.6 MB (5602269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67580450fcb49521ca804f4b54bd2bd07ebc4f3263724a69998c832ae9983d9e`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c707e65fefffaaeb1d096da9ef99da0eb845614c50f044b8352cd2ae8534b39e`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97529e380ed09b82c2db2acc2e2135a082f3dfc94d51d32058a554fa0fe35067`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a52fda9fb0314e5eb96e601bc6d393b2e5d480a135c2ffb1de54122fb9e5fee`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-windowsservercore-1809`

```console
$ docker pull nats@sha256:d105a2aec5d7607b2d64b7e727bb299d6639906b90f65c62aec1c023646fb629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.9.25-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:d6c8ef52baefbd23d260c0968de8a3a9e623c5a1e6c1c084fc4cc9c4bd083955
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2185759588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fc18a9a5bd3a99e5270cd5ccbb602d851b0d82af6fc71a20f0f9e988882048`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:09:07 GMT
ENV NATS_SERVER=2.9.25
# Wed, 15 May 2024 21:09:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 15 May 2024 21:09:09 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 15 May 2024 21:10:23 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 May 2024 21:12:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 15 May 2024 21:12:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:12:20 GMT
EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:12:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:12:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89ee38c395afa6a56d89d2fb6a4e4416a29532867ac749ed891d8afbcda1135`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849d3d89dda77cca52a136f7b2efd5d49db6a15023779c247271b88e617af134`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495bf4363371aaf97d2f904389bb10eaa3084ae31144835f977ff70ff65cbfa8`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29960b46711d8942c7067c001f2cf2da2e307d07df0496e770982e7a94dd1885`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 432.5 KB (432533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b49209267b4fe2543a0f5fa467f5ca0fa4d48b310dd00a04976d3ca886bc8f`  
		Last Modified: Wed, 15 May 2024 21:13:47 GMT  
		Size: 5.6 MB (5602269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67580450fcb49521ca804f4b54bd2bd07ebc4f3263724a69998c832ae9983d9e`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c707e65fefffaaeb1d096da9ef99da0eb845614c50f044b8352cd2ae8534b39e`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97529e380ed09b82c2db2acc2e2135a082f3dfc94d51d32058a554fa0fe35067`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a52fda9fb0314e5eb96e601bc6d393b2e5d480a135c2ffb1de54122fb9e5fee`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:3d01bb9c1bc4eedb5b06973ff4793609453c8e49dbe4653c5a689dfffb305dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:6fb38aaa7467fc0f95b9b8b82667e13a6ab33e88328266114cd5972fd4ce7a36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9593547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed50fb89a515fd8a7ac65959ec5c4447b3224af721405ffb59482b5edcf8b7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:04:51 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:04:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:04:54 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:04:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74b83a0e28b2579e281f6a89215c7220be68fd968d6f29a63794abbc28c1264`  
		Last Modified: Fri, 12 Apr 2024 01:05:34 GMT  
		Size: 6.2 MB (6183818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb31291d77521460d7df0a79503a8b9457e85667ae9d4fc313a127f66b5bbee6`  
		Last Modified: Fri, 12 Apr 2024 01:05:32 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287ee2a0c75e9620dfa28523cdd568ab557a6356d4696dff7d6053cb24ddc57e`  
		Last Modified: Fri, 12 Apr 2024 01:05:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:1adfb327abdec112e1ef8e07b47a65e9359224a5c2fd6f41d5d37b9674e6f65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14527215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daad98a5ab46e9563fb76d02ee9d0b4a4e520beab7c3a1a8c7b6914115c24170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 22:49:24 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 22:49:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 22:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 22:49:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 22:49:28 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 22:49:28 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 22:49:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c50cc966eb4cbc4a4b881ff20948920be4f45ab8e2cf62ab712cac444395ee`  
		Last Modified: Tue, 21 May 2024 22:50:04 GMT  
		Size: 6.0 MB (5977107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482b47d1cf301cc352bae57642f522722da3324f7b667b1c7ab9a6727d88f527`  
		Last Modified: Tue, 21 May 2024 22:50:03 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9121bc5ccbbd746d1fb23bd55dddbf3d7e34dfc3cb7df700f8ca078f0ec344`  
		Last Modified: Tue, 21 May 2024 22:50:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df155a51d233cc945101d877e9a8d394d4b8114026d50c46107ca509e73414a4`  
		Last Modified: Tue, 21 May 2024 22:50:04 GMT  
		Size: 5.4 MB (5383712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a3f56e81749917f8b07128d633c16d54338fb686f6ddcaa849a23b024cdc62cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14259407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afd587d768a05bc1431c931ab535c88081752285018604a5cae23518073a5fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:03:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:03:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:03:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:03:49 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:03:49 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:03:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e9b04dcae92028f76d8d03593f5da713c1b30e4413f516ac6feb1931c7b2e6`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 6.0 MB (5966263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42806fb40884dc31d08d85dc9811fd14e2d5c8a3f1d355140fe35d2b0e8572`  
		Last Modified: Tue, 21 May 2024 23:04:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da704e6a7abb5014e315123b47670ed2c5da374a12abe0c8a16ac5c00984bc5b`  
		Last Modified: Tue, 21 May 2024 23:04:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2a13bc359472f8406932f00ed1e4a78c2bd57597328886fca2d157b4fd875f`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 5.4 MB (5373248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8e0de73f92a021e34a4a3a2d9fe7db10ea0c5374f6acc4839aafa07f83389a89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14486423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30706d32b39530e9b48913eb6b49e5b607cdf805b5b583ca6a10da052e8c863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:10 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:13 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:13 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e451ccd47ce6074c0eb5a19f953f3cf1b5f7582fa1629fb446c5e98df5bca96b`  
		Last Modified: Tue, 21 May 2024 23:22:04 GMT  
		Size: 5.9 MB (5865815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91c46871a02794fd3e02f3a96648cfe21cc7bba92e4a12880704bc4f5099fa6`  
		Last Modified: Tue, 21 May 2024 23:22:03 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0973b29973a14e29ca26a3bf6ce557a818c454e502f2a1625d12916b94a63c7f`  
		Last Modified: Tue, 21 May 2024 23:22:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d832ebe187b943a16762d91e06cfed3a2af866c23fb50873bc206b8ff64b15`  
		Last Modified: Tue, 21 May 2024 23:22:04 GMT  
		Size: 5.3 MB (5271890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:0b37f107c7121fb4970a680686bf47c0bdc6e221f073948f91fe1ccf935a8069
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14453737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff3f441c8f17081f4726462e440f695fc1f61e1a2f10e242f42e4bd984077bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:08 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:15 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:16 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8c871a04ac5c3a745fc1b9fc0bf0df8eb4429cfc19a6d0c0e5dc82ead6caa5`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.8 MB (5844103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856cdce720d8bce5ea7df85548fc0591d2f54a82aaa905dcf4d5c862d090a59e`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29cb8a321e6c477eee1702a71c5d6712719ebf97439a8e5ce5e98052caa4d73`  
		Last Modified: Tue, 21 May 2024 23:21:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74163ae1a817e733dfe24bdc0793bd29a32f24f194a83320208429d1d8a41355`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.3 MB (5250277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:6d5ae5c55bd610f20af66cdcb962dc1467df57e229a88bd21e4aa67b0125a4bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14983722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e6fda5c2edf46ae713164e45bc6d3db65c81e9d94751fa2b474f4491b6dee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:19 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:23 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:23 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03de2766ed1b649ad8022c7178d9fb18b54afafd6768b26cc8418bc8ee6ca3`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 6.2 MB (6166358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca420f0a7f6b1e669c0fc2fb845bb3a3e3b5918ae5e6ca274bbe962f098a7c9`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08ad1d4d29a3891a6cef4dd154aebf959965bbae6c2df8f3f88d4d0b617b06f`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e270d0402a827b66e36de07d5f201dc2ad24fdf690b07d53315ef189c7d5aaa`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.6 MB (5573725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.19`

```console
$ docker pull nats@sha256:866569467e526287a31ed970a0349637336661050d0d103af519d44dfb46905a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:d8db0ade59946baad440b32e1e29e559bedf8c4ef184449c18cec3b09e651a1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15418627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c8a1867e3ade5b29f586d4af425c5af2c5b77d83afc82d6b4df3c1197a1179`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:34:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:34:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:34:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:34:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:34:48 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:34:48 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:34:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:34:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930875d3c07e9c11015b7a87cc3680faf0cf5f431f1fbdc3538f0dc7fbba5f73`  
		Last Modified: Tue, 21 May 2024 23:35:28 GMT  
		Size: 6.3 MB (6300481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c58623f692b1176118937a136b2a84de7bde4a57cff6c875eedf3a05a8c8c11`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859a16e256149aa535e3b92a42035dc1171480b2582e419a0d652cf9d40267ee`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfa5674686a490dd961d0c0c057b4ab79ec8ef711fe45c5ee02be48beefddf6`  
		Last Modified: Tue, 21 May 2024 23:35:28 GMT  
		Size: 5.7 MB (5708415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:1adfb327abdec112e1ef8e07b47a65e9359224a5c2fd6f41d5d37b9674e6f65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14527215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daad98a5ab46e9563fb76d02ee9d0b4a4e520beab7c3a1a8c7b6914115c24170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 22:49:24 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 22:49:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 22:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 22:49:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 22:49:28 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 22:49:28 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 22:49:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c50cc966eb4cbc4a4b881ff20948920be4f45ab8e2cf62ab712cac444395ee`  
		Last Modified: Tue, 21 May 2024 22:50:04 GMT  
		Size: 6.0 MB (5977107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482b47d1cf301cc352bae57642f522722da3324f7b667b1c7ab9a6727d88f527`  
		Last Modified: Tue, 21 May 2024 22:50:03 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9121bc5ccbbd746d1fb23bd55dddbf3d7e34dfc3cb7df700f8ca078f0ec344`  
		Last Modified: Tue, 21 May 2024 22:50:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df155a51d233cc945101d877e9a8d394d4b8114026d50c46107ca509e73414a4`  
		Last Modified: Tue, 21 May 2024 22:50:04 GMT  
		Size: 5.4 MB (5383712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:a3f56e81749917f8b07128d633c16d54338fb686f6ddcaa849a23b024cdc62cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14259407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afd587d768a05bc1431c931ab535c88081752285018604a5cae23518073a5fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:03:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:03:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:03:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:03:49 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:03:49 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:03:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e9b04dcae92028f76d8d03593f5da713c1b30e4413f516ac6feb1931c7b2e6`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 6.0 MB (5966263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42806fb40884dc31d08d85dc9811fd14e2d5c8a3f1d355140fe35d2b0e8572`  
		Last Modified: Tue, 21 May 2024 23:04:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da704e6a7abb5014e315123b47670ed2c5da374a12abe0c8a16ac5c00984bc5b`  
		Last Modified: Tue, 21 May 2024 23:04:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2a13bc359472f8406932f00ed1e4a78c2bd57597328886fca2d157b4fd875f`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 5.4 MB (5373248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8e0de73f92a021e34a4a3a2d9fe7db10ea0c5374f6acc4839aafa07f83389a89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14486423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30706d32b39530e9b48913eb6b49e5b607cdf805b5b583ca6a10da052e8c863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:10 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:13 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:13 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e451ccd47ce6074c0eb5a19f953f3cf1b5f7582fa1629fb446c5e98df5bca96b`  
		Last Modified: Tue, 21 May 2024 23:22:04 GMT  
		Size: 5.9 MB (5865815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91c46871a02794fd3e02f3a96648cfe21cc7bba92e4a12880704bc4f5099fa6`  
		Last Modified: Tue, 21 May 2024 23:22:03 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0973b29973a14e29ca26a3bf6ce557a818c454e502f2a1625d12916b94a63c7f`  
		Last Modified: Tue, 21 May 2024 23:22:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d832ebe187b943a16762d91e06cfed3a2af866c23fb50873bc206b8ff64b15`  
		Last Modified: Tue, 21 May 2024 23:22:04 GMT  
		Size: 5.3 MB (5271890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:0b37f107c7121fb4970a680686bf47c0bdc6e221f073948f91fe1ccf935a8069
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14453737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff3f441c8f17081f4726462e440f695fc1f61e1a2f10e242f42e4bd984077bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:08 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:15 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:16 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8c871a04ac5c3a745fc1b9fc0bf0df8eb4429cfc19a6d0c0e5dc82ead6caa5`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.8 MB (5844103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856cdce720d8bce5ea7df85548fc0591d2f54a82aaa905dcf4d5c862d090a59e`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29cb8a321e6c477eee1702a71c5d6712719ebf97439a8e5ce5e98052caa4d73`  
		Last Modified: Tue, 21 May 2024 23:21:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74163ae1a817e733dfe24bdc0793bd29a32f24f194a83320208429d1d8a41355`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.3 MB (5250277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:6d5ae5c55bd610f20af66cdcb962dc1467df57e229a88bd21e4aa67b0125a4bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14983722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e6fda5c2edf46ae713164e45bc6d3db65c81e9d94751fa2b474f4491b6dee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:19 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:23 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:23 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03de2766ed1b649ad8022c7178d9fb18b54afafd6768b26cc8418bc8ee6ca3`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 6.2 MB (6166358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca420f0a7f6b1e669c0fc2fb845bb3a3e3b5918ae5e6ca274bbe962f098a7c9`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08ad1d4d29a3891a6cef4dd154aebf959965bbae6c2df8f3f88d4d0b617b06f`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e270d0402a827b66e36de07d5f201dc2ad24fdf690b07d53315ef189c7d5aaa`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.6 MB (5573725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:cdb229a4805b0e2e5d123ecd65665c8485ec814499093392b4213aa8e9420615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5820; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:da851c45cfe95a52ab3e6b013241c2e5271d28f7c0b136f1047c108fbabf859e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2ed2be6ead45418e9fc8d5da88a292fcbb6879e7dcc4db9126a45c5176f6d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:33 GMT
COPY file:0aba91b853d0eaf7d63d52b084d7546996e8db198a221ad2c77a29c916538108 in /nats-server 
# Tue, 21 May 2024 22:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:33 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772a5dc6e4bbb9f932bcf1232f3a7830303a955bbac3775e90153ce66ac9bd8d`  
		Last Modified: Tue, 21 May 2024 22:50:23 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:c655a24000047ea7fc1f1c8c4b1e9c282ac92e2d9706d5aaec92934ab55b72b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb15c7fb2d9a1f5c89f39c7be34daef5e45d98f6454a74e07c7051a7e9223370`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:03:59 GMT
COPY file:ed3148eb9af051d444f42876fc76b54a26455984f4a53bbdf1058b0e11e8b336 in /nats-server 
# Tue, 21 May 2024 23:03:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:03:59 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:59 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:03:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8193d445aa5ad5ea1f96740679c84ff3087a86b1d13258defc8bc3a21f395d18`  
		Last Modified: Tue, 21 May 2024 23:04:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:64d7152e25fd1648d59fe3fda7da9461723b0fa6905b144971bac30def679c99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850b1061eaa54e26469184edc02f606e471c4d9416a0a6bc6068251f90fc0c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:31 GMT
COPY file:dc57eab26dd732b695752b0df8adf307bcbd19553cba75ac3ac2975e7d2cd86f in /nats-server 
# Tue, 21 May 2024 23:21:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:31 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af7d01d01fa2b520a97d19101ea36ea9b96e8124f2fdc1bb7076f976ab01ee`  
		Last Modified: Tue, 21 May 2024 23:22:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:d7f6dd76a8d365ac199d2e1767531fd74bf13cd2c78dba7ac042b8ed1937c4fc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c128c5b164984dd4d70a48c9af0281112501c7ca458ff244d718d50a31dadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:33 GMT
COPY file:e17294dc512d40e8e54498c73c890fd5204a41873c3567f7c18aa532ba727dc3 in /nats-server 
# Tue, 21 May 2024 23:21:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:34 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a45efcc2dc003ec8d53cb55ac8512bb7b4c35bcbd7a761991ef4c1b3147dfd3`  
		Last Modified: Tue, 21 May 2024 23:22:14 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:a9a0d93cb6a669f0fc2d842220f3a517c5c4ac5b345f0e2dc6aa8267c6fc76a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56c6e37910e564eec4963a6cbe0df805262ea12e504977a860f55fc52a39d05`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:30 GMT
COPY file:359d868ca3e4f687575abd568ad941a9d2682ed2ca604af3309b28b73679d2b7 in /nats-server 
# Tue, 21 May 2024 23:21:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:30 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0c0c15d382278c746e463dce4639563f785a5f07f552c8f5caceb88a87d424`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:958a15d708d62f00bc9918e2283ecab5d12a85d54187bb5301593f33c452a6dc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160734385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bceedc7adb4c9ed6737507c649ee6ff628321a49b2274fbed9b74f50ca19557`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:17:18 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be448c0648b4e415641d5d7504a60f23cb03b4b00b0211021d9fbf697157d4ff`  
		Last Modified: Tue, 21 May 2024 23:18:13 GMT  
		Size: 5.8 MB (5786623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17add0d9ad6ce3c2580f4f65cc11d1d7c6eb572e2df535e9b7d1538394ef668e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c916da7655fd8a5653ae241bc5e9e7657b62c26bce65ae68453896906234d11e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696dcba679ec709b4b8fa95dcd27de7889439d88a304ac3770ac1e6f32f8010c`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4a7a4b5fb58cd41e8b7478c971ce9a63da9d056aed725662939f3f108cc898`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:0bec822da126d2b61e51f4ef77397ea35d96e27ba61e8a46379bf6bb2ee34874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:da851c45cfe95a52ab3e6b013241c2e5271d28f7c0b136f1047c108fbabf859e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2ed2be6ead45418e9fc8d5da88a292fcbb6879e7dcc4db9126a45c5176f6d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:33 GMT
COPY file:0aba91b853d0eaf7d63d52b084d7546996e8db198a221ad2c77a29c916538108 in /nats-server 
# Tue, 21 May 2024 22:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:33 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772a5dc6e4bbb9f932bcf1232f3a7830303a955bbac3775e90153ce66ac9bd8d`  
		Last Modified: Tue, 21 May 2024 22:50:23 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:c655a24000047ea7fc1f1c8c4b1e9c282ac92e2d9706d5aaec92934ab55b72b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb15c7fb2d9a1f5c89f39c7be34daef5e45d98f6454a74e07c7051a7e9223370`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:03:59 GMT
COPY file:ed3148eb9af051d444f42876fc76b54a26455984f4a53bbdf1058b0e11e8b336 in /nats-server 
# Tue, 21 May 2024 23:03:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:03:59 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:59 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:03:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8193d445aa5ad5ea1f96740679c84ff3087a86b1d13258defc8bc3a21f395d18`  
		Last Modified: Tue, 21 May 2024 23:04:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:64d7152e25fd1648d59fe3fda7da9461723b0fa6905b144971bac30def679c99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850b1061eaa54e26469184edc02f606e471c4d9416a0a6bc6068251f90fc0c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:31 GMT
COPY file:dc57eab26dd732b695752b0df8adf307bcbd19553cba75ac3ac2975e7d2cd86f in /nats-server 
# Tue, 21 May 2024 23:21:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:31 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af7d01d01fa2b520a97d19101ea36ea9b96e8124f2fdc1bb7076f976ab01ee`  
		Last Modified: Tue, 21 May 2024 23:22:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:d7f6dd76a8d365ac199d2e1767531fd74bf13cd2c78dba7ac042b8ed1937c4fc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c128c5b164984dd4d70a48c9af0281112501c7ca458ff244d718d50a31dadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:33 GMT
COPY file:e17294dc512d40e8e54498c73c890fd5204a41873c3567f7c18aa532ba727dc3 in /nats-server 
# Tue, 21 May 2024 23:21:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:34 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a45efcc2dc003ec8d53cb55ac8512bb7b4c35bcbd7a761991ef4c1b3147dfd3`  
		Last Modified: Tue, 21 May 2024 23:22:14 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:a9a0d93cb6a669f0fc2d842220f3a517c5c4ac5b345f0e2dc6aa8267c6fc76a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56c6e37910e564eec4963a6cbe0df805262ea12e504977a860f55fc52a39d05`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:30 GMT
COPY file:359d868ca3e4f687575abd568ad941a9d2682ed2ca604af3309b28b73679d2b7 in /nats-server 
# Tue, 21 May 2024 23:21:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:30 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0c0c15d382278c746e463dce4639563f785a5f07f552c8f5caceb88a87d424`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:003d8791c50c4203ecf629af340c97c71cacca7c43091cb6d0b2537d80fbbec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:958a15d708d62f00bc9918e2283ecab5d12a85d54187bb5301593f33c452a6dc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160734385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bceedc7adb4c9ed6737507c649ee6ff628321a49b2274fbed9b74f50ca19557`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:17:18 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be448c0648b4e415641d5d7504a60f23cb03b4b00b0211021d9fbf697157d4ff`  
		Last Modified: Tue, 21 May 2024 23:18:13 GMT  
		Size: 5.8 MB (5786623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17add0d9ad6ce3c2580f4f65cc11d1d7c6eb572e2df535e9b7d1538394ef668e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c916da7655fd8a5653ae241bc5e9e7657b62c26bce65ae68453896906234d11e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696dcba679ec709b4b8fa95dcd27de7889439d88a304ac3770ac1e6f32f8010c`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4a7a4b5fb58cd41e8b7478c971ce9a63da9d056aed725662939f3f108cc898`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:003d8791c50c4203ecf629af340c97c71cacca7c43091cb6d0b2537d80fbbec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:958a15d708d62f00bc9918e2283ecab5d12a85d54187bb5301593f33c452a6dc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160734385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bceedc7adb4c9ed6737507c649ee6ff628321a49b2274fbed9b74f50ca19557`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:17:18 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:17:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:17:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be448c0648b4e415641d5d7504a60f23cb03b4b00b0211021d9fbf697157d4ff`  
		Last Modified: Tue, 21 May 2024 23:18:13 GMT  
		Size: 5.8 MB (5786623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17add0d9ad6ce3c2580f4f65cc11d1d7c6eb572e2df535e9b7d1538394ef668e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c916da7655fd8a5653ae241bc5e9e7657b62c26bce65ae68453896906234d11e`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696dcba679ec709b4b8fa95dcd27de7889439d88a304ac3770ac1e6f32f8010c`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4a7a4b5fb58cd41e8b7478c971ce9a63da9d056aed725662939f3f108cc898`  
		Last Modified: Tue, 21 May 2024 23:18:12 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:0bec822da126d2b61e51f4ef77397ea35d96e27ba61e8a46379bf6bb2ee34874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:da851c45cfe95a52ab3e6b013241c2e5271d28f7c0b136f1047c108fbabf859e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2ed2be6ead45418e9fc8d5da88a292fcbb6879e7dcc4db9126a45c5176f6d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 22:49:33 GMT
COPY file:0aba91b853d0eaf7d63d52b084d7546996e8db198a221ad2c77a29c916538108 in /nats-server 
# Tue, 21 May 2024 22:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 22:49:33 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 22:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772a5dc6e4bbb9f932bcf1232f3a7830303a955bbac3775e90153ce66ac9bd8d`  
		Last Modified: Tue, 21 May 2024 22:50:23 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:c655a24000047ea7fc1f1c8c4b1e9c282ac92e2d9706d5aaec92934ab55b72b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb15c7fb2d9a1f5c89f39c7be34daef5e45d98f6454a74e07c7051a7e9223370`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:03:59 GMT
COPY file:ed3148eb9af051d444f42876fc76b54a26455984f4a53bbdf1058b0e11e8b336 in /nats-server 
# Tue, 21 May 2024 23:03:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:03:59 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:59 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:03:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8193d445aa5ad5ea1f96740679c84ff3087a86b1d13258defc8bc3a21f395d18`  
		Last Modified: Tue, 21 May 2024 23:04:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:64d7152e25fd1648d59fe3fda7da9461723b0fa6905b144971bac30def679c99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850b1061eaa54e26469184edc02f606e471c4d9416a0a6bc6068251f90fc0c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:31 GMT
COPY file:dc57eab26dd732b695752b0df8adf307bcbd19553cba75ac3ac2975e7d2cd86f in /nats-server 
# Tue, 21 May 2024 23:21:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:31 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af7d01d01fa2b520a97d19101ea36ea9b96e8124f2fdc1bb7076f976ab01ee`  
		Last Modified: Tue, 21 May 2024 23:22:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:d7f6dd76a8d365ac199d2e1767531fd74bf13cd2c78dba7ac042b8ed1937c4fc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c128c5b164984dd4d70a48c9af0281112501c7ca458ff244d718d50a31dadb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:33 GMT
COPY file:e17294dc512d40e8e54498c73c890fd5204a41873c3567f7c18aa532ba727dc3 in /nats-server 
# Tue, 21 May 2024 23:21:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:34 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a45efcc2dc003ec8d53cb55ac8512bb7b4c35bcbd7a761991ef4c1b3147dfd3`  
		Last Modified: Tue, 21 May 2024 23:22:14 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:a9a0d93cb6a669f0fc2d842220f3a517c5c4ac5b345f0e2dc6aa8267c6fc76a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56c6e37910e564eec4963a6cbe0df805262ea12e504977a860f55fc52a39d05`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 21 May 2024 23:21:30 GMT
COPY file:359d868ca3e4f687575abd568ad941a9d2682ed2ca604af3309b28b73679d2b7 in /nats-server 
# Tue, 21 May 2024 23:21:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 21 May 2024 23:21:30 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 21 May 2024 23:21:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0c0c15d382278c746e463dce4639563f785a5f07f552c8f5caceb88a87d424`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:5b3e38cc7df1ccd71cb1357b316228b34861c6c37727ca7ffd148b73e64b321b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:fc57a2fbc1740965db1c40c59291ef89a6d9f5f235b4d963f4d0602ae0666443
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186249989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b64d1c4d9a958ede215514048d16b164a246beedd0c21e6c59ff3d07f069867`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:14:46 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:14:47 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.16/nats-server-v2.10.16-windows-amd64.zip
# Tue, 21 May 2024 23:14:48 GMT
ENV NATS_SERVER_SHASUM=22a5ef3a54200ebdebaa325822f477c89dc6533ec6fc1f531d897aa876517ccf
# Tue, 21 May 2024 23:15:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 21 May 2024 23:16:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 21 May 2024 23:16:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:16:58 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:16:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:16:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d075cbe94bdd5f06bdabff0ae1baa13ad48a75f808800d9c9cf7d554470d866`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a88d0da7a6579af9c2bdff927235dee0c94b1bfc1cec3787d05218c6a55ec3c`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f922389c5664c8e701d97ef08d1cc52e256e6002e475dacd84e45e12ccaf8cc0`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096dd602404c378351787720a7178c38038189543894dcbe1ce4b5260124b8af`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 445.9 KB (445881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bad7b47779f08ea37f050914a7169eb3be6ad32530159df515b046af95396`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 6.1 MB (6079688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c3b9fbec461537454b31d72f007b18f9d7d0449481a6532b4bc0465145b360`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93647e59b4740ef7e3e440c385dfc114fbae9e7fa990db167023a7040f182a11`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445badc8d13b259ba8343872927775698cdbb81b6013fa153680a9052fea5330`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da65ffc80b4f6a0ef8841c9d2e497145d917917587c49470ad4ca54c6cf78de`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:5b3e38cc7df1ccd71cb1357b316228b34861c6c37727ca7ffd148b73e64b321b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:fc57a2fbc1740965db1c40c59291ef89a6d9f5f235b4d963f4d0602ae0666443
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186249989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b64d1c4d9a958ede215514048d16b164a246beedd0c21e6c59ff3d07f069867`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Tue, 21 May 2024 23:14:46 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:14:47 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.16/nats-server-v2.10.16-windows-amd64.zip
# Tue, 21 May 2024 23:14:48 GMT
ENV NATS_SERVER_SHASUM=22a5ef3a54200ebdebaa325822f477c89dc6533ec6fc1f531d897aa876517ccf
# Tue, 21 May 2024 23:15:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 21 May 2024 23:16:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 21 May 2024 23:16:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 21 May 2024 23:16:58 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:16:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 21 May 2024 23:16:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d075cbe94bdd5f06bdabff0ae1baa13ad48a75f808800d9c9cf7d554470d866`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a88d0da7a6579af9c2bdff927235dee0c94b1bfc1cec3787d05218c6a55ec3c`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f922389c5664c8e701d97ef08d1cc52e256e6002e475dacd84e45e12ccaf8cc0`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096dd602404c378351787720a7178c38038189543894dcbe1ce4b5260124b8af`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 445.9 KB (445881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bad7b47779f08ea37f050914a7169eb3be6ad32530159df515b046af95396`  
		Last Modified: Tue, 21 May 2024 23:17:59 GMT  
		Size: 6.1 MB (6079688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c3b9fbec461537454b31d72f007b18f9d7d0449481a6532b4bc0465145b360`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93647e59b4740ef7e3e440c385dfc114fbae9e7fa990db167023a7040f182a11`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445badc8d13b259ba8343872927775698cdbb81b6013fa153680a9052fea5330`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da65ffc80b4f6a0ef8841c9d2e497145d917917587c49470ad4ca54c6cf78de`  
		Last Modified: Tue, 21 May 2024 23:17:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

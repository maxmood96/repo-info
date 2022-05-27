<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.15`](#nats2-alpine315)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.8`](#nats28)
-	[`nats:2.8-alpine`](#nats28-alpine)
-	[`nats:2.8-alpine3.15`](#nats28-alpine315)
-	[`nats:2.8-linux`](#nats28-linux)
-	[`nats:2.8-nanoserver`](#nats28-nanoserver)
-	[`nats:2.8-nanoserver-1809`](#nats28-nanoserver-1809)
-	[`nats:2.8-scratch`](#nats28-scratch)
-	[`nats:2.8-windowsservercore`](#nats28-windowsservercore)
-	[`nats:2.8-windowsservercore-1809`](#nats28-windowsservercore-1809)
-	[`nats:2.8.4`](#nats284)
-	[`nats:2.8.4-alpine`](#nats284-alpine)
-	[`nats:2.8.4-alpine3.15`](#nats284-alpine315)
-	[`nats:2.8.4-linux`](#nats284-linux)
-	[`nats:2.8.4-nanoserver`](#nats284-nanoserver)
-	[`nats:2.8.4-nanoserver-1809`](#nats284-nanoserver-1809)
-	[`nats:2.8.4-scratch`](#nats284-scratch)
-	[`nats:2.8.4-windowsservercore`](#nats284-windowsservercore)
-	[`nats:2.8.4-windowsservercore-1809`](#nats284-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.15`](#natsalpine315)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:9686d73262f91e44c10b838eecbab53e705d2f4be5718efe92dfdf9f86f4e786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2928; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:796298f636925dedbbdfa537f42423dffd3a69b70c3a9bf4fd0982886a4b745d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842c053e15bdb38e697668b1f0721313203f7c2297eb6d79000f20858dc97854`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:38:26 GMT
COPY file:c866dea678e8cec7cbd0798a1dbdefc45e992d9df374709f6000bac517589a1b in /nats-server 
# Fri, 27 May 2022 00:38:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:38:27 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:38:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:38:27 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:38:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e5797f39fa0527a3dd0a137353b40f97c71134e7eb38373d9791c5f1392885b`  
		Last Modified: Fri, 27 May 2022 00:39:15 GMT  
		Size: 4.6 MB (4591087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3b732adf61929b0b23ca08934cd89923e9cd9d7061544e76bbce57a9fa1e4`  
		Last Modified: Fri, 27 May 2022 00:39:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:7df9a2712c9b7e57f228a270f9fdfaf95f8662890dd90719ab08952fe93cc99d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86f50672b8fb25a83d599295659904a27d366e8cad89089ddb9171c79e31c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:56:05 GMT
COPY file:8de8b0cf8e6edf54e413c112cd66aed537abed387a26ba749a9293d43cdf6594 in /nats-server 
# Thu, 26 May 2022 23:56:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:56:05 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:56:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:56:06 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:56:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:770fa9c168613edbe7aa7007d2cf8492c6570efc1ddab217fa32772c6b72dd48`  
		Last Modified: Thu, 26 May 2022 23:58:21 GMT  
		Size: 4.2 MB (4245317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d80ba54887e3752f04df58e1ab68c9805dc2aee54c543d487d8d51a2c88afc1`  
		Last Modified: Thu, 26 May 2022 23:58:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:208577394199773ff99d68d668bf4830314a173d7de8407e2bc5666b1d6d4a34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96128257f8f2facb4a2f726619b86453544d9108ec209c3665ec78c2dd14acf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2841d6664b8897473f39b595b9aa4b28e749f587dc1afa4a0027ae507f37ee1f in /nats-server 
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:25:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:25:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:25:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f533e6e439ee51f1cf94458f821a20ed162b542d356340957091882ad881d5c1`  
		Last Modified: Fri, 27 May 2022 00:28:16 GMT  
		Size: 4.2 MB (4242287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1306305db51c19253939f28312d2e4a694eab31b920aeef7d9a4d0a0b76f045`  
		Last Modified: Fri, 27 May 2022 00:28:13 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:87b1afbd78a75ee48cb6b37a8522bbb01f5e9b5047b095b16cc4f241774a48d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bce5ae01237736c7e0447d8cd1b2dbe252eab3ab5ac3b05d98b646b2575cee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:53:56 GMT
COPY file:2dbd94c6c11f89ceba3241f1efe469d0a06f0aae91abb77f3d79756676d0be57 in /nats-server 
# Thu, 26 May 2022 23:53:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:53:57 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:53:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:54:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c74770da2ea808362085edd6dead652091b3e3d34c1e32c50015a6a5bb36c02`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 4.2 MB (4227378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988af7458b707048622e497d5ae818b77d3a24ed0295a7897ced8f003179f7f9`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:73e71a703e620efe92f4bdcfc0c525c8c472f4bb82d4ab6a57a8e560cf79b5fb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107773608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effb063d7055b399920066dd934fcbc50ff93b5460629fdcf20c7a4ff27ca62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:26:00 GMT
RUN cmd /S /C #(nop) COPY file:88c957e774978b3592c1072a38fbf2d578a30b42e89604bf16828cccd9f86b17 in C:\nats-server.exe 
# Fri, 27 May 2022 00:26:01 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:26:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23039a0ccbad6fe276c7cbdbe79f9f030b86f2178198f439eeed20e1ff64877b`  
		Last Modified: Fri, 27 May 2022 01:15:17 GMT  
		Size: 4.6 MB (4633261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59573cd0506705779a3d37bf4d344d3589369ce3279557bd5bda46df763cf5b`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efde216ebb9b658047beb227fed499b9c7596c5e58f2401bfb16e16b24114701`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909550900786c7eead4015a4b0b2ac76493686621fab1d9aa15fa40fd569265`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a62fba798d3b46ba25a1df431d84098e426985250293108cfec350146ddfc0f`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:24d2a7b7394e612109c861692f83d5ac3bb5d44e61d07002b333335564e0c76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:4199deae36b30cf612a8a5ac96614e60dba809dd72d73a5d3534faa521a12261
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48fd9739aa3f72822ff0234951c748e1933512aff2aa6631c4cf8e4f9b6692c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:37:50 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:37:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 May 2022 00:37:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 May 2022 00:37:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 May 2022 00:37:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 May 2022 00:37:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415d0ea53c276a355c1209aed0a7e21521ddf40ad8a8e0ec3d72d8593a2ba455`  
		Last Modified: Fri, 27 May 2022 00:38:52 GMT  
		Size: 4.9 MB (4864532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05146d3cba39de864032f28506c4921cd565c57aeb729108ac8d0b11c3276bbc`  
		Last Modified: Fri, 27 May 2022 00:38:51 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc9a9ede479a70c4e0d44d902e64c19eca0cd12baf3624ecf0e77d74fde28ef`  
		Last Modified: Fri, 27 May 2022 00:38:51 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:8b48b81efe06e10f92980ce446aa199c35e591e6e61f6a508e8e5b83b993c75c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7141581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fcaa7e9654b63fb8642995444c1d4e0c884d6bfc2a16fdb8a7a39e137b5208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 23:55:37 GMT
ENV NATS_SERVER=2.8.4
# Thu, 26 May 2022 23:55:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 26 May 2022 23:55:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 26 May 2022 23:55:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 26 May 2022 23:55:43 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:55:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 May 2022 23:55:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50f68c47a108ab599d7f0e191ffaf378e6dce6a928151e691d8ea726aeb928`  
		Last Modified: Thu, 26 May 2022 23:57:46 GMT  
		Size: 4.5 MB (4518611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4cb9d5e8d247c55e5f7e46c8d54ea485f55806c24444feaf62725d6ba170f1`  
		Last Modified: Thu, 26 May 2022 23:57:43 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c6a3cdd4a881f42229288ebba9a675d7abe171cd2b2838becae58d1aad6ab`  
		Last Modified: Thu, 26 May 2022 23:57:43 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ba8d5358e4179eedb8812098fe9aafac97d3cbc262c5c661e8f7a0c91a5bbcb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6939129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eca0f2ec4b22a18d9e30a03a72c0b72555d4cdbcbcb8ff15552cc1d01442c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:25:21 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:25:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 May 2022 00:25:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 May 2022 00:25:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 May 2022 00:25:26 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 May 2022 00:25:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f90a00ed33ea115d275ac961047e5009b1e24e2103dbfaed2ab8f52856c975`  
		Last Modified: Fri, 27 May 2022 00:27:40 GMT  
		Size: 4.5 MB (4513806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd41cd9dfa9b3a42fea8a47e1a69c57faa29f3cdd27489fc7f4fe699d283f899`  
		Last Modified: Fri, 27 May 2022 00:27:37 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed506c19493a71093e162dbcebe70d57fc6c372d9c201a32ef0515b66da395b7`  
		Last Modified: Fri, 27 May 2022 00:27:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:068170580c70c9c06e2050fa9c6f66ec28f61c9062663cf2b45db2eed7e6b3d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7218027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fa83e475ee42455e6e7021633d7a98bb6496a5a75621f389dff13b1ceaa343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 23:53:38 GMT
ENV NATS_SERVER=2.8.4
# Thu, 26 May 2022 23:53:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 26 May 2022 23:53:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 26 May 2022 23:53:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 26 May 2022 23:53:43 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 May 2022 23:53:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48649cc80ad9a6544bde7c572f66e6a5f2c0e918923a957045cfea77bbf31bb`  
		Last Modified: Thu, 26 May 2022 23:54:50 GMT  
		Size: 4.5 MB (4500578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bbb498a8d1c04c80271b66119f843bc9a68cf260f1fc0005babdb8ef1820b8`  
		Last Modified: Thu, 26 May 2022 23:54:49 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ca2313cb9b3e722a83aa9f01456f583d124cbb90aa75908b33a0c37ecdaeb`  
		Last Modified: Thu, 26 May 2022 23:54:49 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.15`

```console
$ docker pull nats@sha256:24d2a7b7394e612109c861692f83d5ac3bb5d44e61d07002b333335564e0c76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:4199deae36b30cf612a8a5ac96614e60dba809dd72d73a5d3534faa521a12261
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48fd9739aa3f72822ff0234951c748e1933512aff2aa6631c4cf8e4f9b6692c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:37:50 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:37:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 May 2022 00:37:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 May 2022 00:37:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 May 2022 00:37:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 May 2022 00:37:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415d0ea53c276a355c1209aed0a7e21521ddf40ad8a8e0ec3d72d8593a2ba455`  
		Last Modified: Fri, 27 May 2022 00:38:52 GMT  
		Size: 4.9 MB (4864532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05146d3cba39de864032f28506c4921cd565c57aeb729108ac8d0b11c3276bbc`  
		Last Modified: Fri, 27 May 2022 00:38:51 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc9a9ede479a70c4e0d44d902e64c19eca0cd12baf3624ecf0e77d74fde28ef`  
		Last Modified: Fri, 27 May 2022 00:38:51 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:8b48b81efe06e10f92980ce446aa199c35e591e6e61f6a508e8e5b83b993c75c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7141581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fcaa7e9654b63fb8642995444c1d4e0c884d6bfc2a16fdb8a7a39e137b5208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 23:55:37 GMT
ENV NATS_SERVER=2.8.4
# Thu, 26 May 2022 23:55:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 26 May 2022 23:55:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 26 May 2022 23:55:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 26 May 2022 23:55:43 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:55:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 May 2022 23:55:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50f68c47a108ab599d7f0e191ffaf378e6dce6a928151e691d8ea726aeb928`  
		Last Modified: Thu, 26 May 2022 23:57:46 GMT  
		Size: 4.5 MB (4518611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4cb9d5e8d247c55e5f7e46c8d54ea485f55806c24444feaf62725d6ba170f1`  
		Last Modified: Thu, 26 May 2022 23:57:43 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c6a3cdd4a881f42229288ebba9a675d7abe171cd2b2838becae58d1aad6ab`  
		Last Modified: Thu, 26 May 2022 23:57:43 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ba8d5358e4179eedb8812098fe9aafac97d3cbc262c5c661e8f7a0c91a5bbcb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6939129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eca0f2ec4b22a18d9e30a03a72c0b72555d4cdbcbcb8ff15552cc1d01442c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:25:21 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:25:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 May 2022 00:25:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 May 2022 00:25:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 May 2022 00:25:26 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 May 2022 00:25:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f90a00ed33ea115d275ac961047e5009b1e24e2103dbfaed2ab8f52856c975`  
		Last Modified: Fri, 27 May 2022 00:27:40 GMT  
		Size: 4.5 MB (4513806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd41cd9dfa9b3a42fea8a47e1a69c57faa29f3cdd27489fc7f4fe699d283f899`  
		Last Modified: Fri, 27 May 2022 00:27:37 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed506c19493a71093e162dbcebe70d57fc6c372d9c201a32ef0515b66da395b7`  
		Last Modified: Fri, 27 May 2022 00:27:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:068170580c70c9c06e2050fa9c6f66ec28f61c9062663cf2b45db2eed7e6b3d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7218027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fa83e475ee42455e6e7021633d7a98bb6496a5a75621f389dff13b1ceaa343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 23:53:38 GMT
ENV NATS_SERVER=2.8.4
# Thu, 26 May 2022 23:53:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 26 May 2022 23:53:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 26 May 2022 23:53:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 26 May 2022 23:53:43 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 May 2022 23:53:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48649cc80ad9a6544bde7c572f66e6a5f2c0e918923a957045cfea77bbf31bb`  
		Last Modified: Thu, 26 May 2022 23:54:50 GMT  
		Size: 4.5 MB (4500578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bbb498a8d1c04c80271b66119f843bc9a68cf260f1fc0005babdb8ef1820b8`  
		Last Modified: Thu, 26 May 2022 23:54:49 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ca2313cb9b3e722a83aa9f01456f583d124cbb90aa75908b33a0c37ecdaeb`  
		Last Modified: Thu, 26 May 2022 23:54:49 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:6e96b99197f9d66e34df638ca22426d21963c643bfd0c987b45f1aecb814bc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:796298f636925dedbbdfa537f42423dffd3a69b70c3a9bf4fd0982886a4b745d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842c053e15bdb38e697668b1f0721313203f7c2297eb6d79000f20858dc97854`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:38:26 GMT
COPY file:c866dea678e8cec7cbd0798a1dbdefc45e992d9df374709f6000bac517589a1b in /nats-server 
# Fri, 27 May 2022 00:38:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:38:27 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:38:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:38:27 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:38:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e5797f39fa0527a3dd0a137353b40f97c71134e7eb38373d9791c5f1392885b`  
		Last Modified: Fri, 27 May 2022 00:39:15 GMT  
		Size: 4.6 MB (4591087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3b732adf61929b0b23ca08934cd89923e9cd9d7061544e76bbce57a9fa1e4`  
		Last Modified: Fri, 27 May 2022 00:39:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7df9a2712c9b7e57f228a270f9fdfaf95f8662890dd90719ab08952fe93cc99d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86f50672b8fb25a83d599295659904a27d366e8cad89089ddb9171c79e31c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:56:05 GMT
COPY file:8de8b0cf8e6edf54e413c112cd66aed537abed387a26ba749a9293d43cdf6594 in /nats-server 
# Thu, 26 May 2022 23:56:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:56:05 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:56:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:56:06 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:56:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:770fa9c168613edbe7aa7007d2cf8492c6570efc1ddab217fa32772c6b72dd48`  
		Last Modified: Thu, 26 May 2022 23:58:21 GMT  
		Size: 4.2 MB (4245317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d80ba54887e3752f04df58e1ab68c9805dc2aee54c543d487d8d51a2c88afc1`  
		Last Modified: Thu, 26 May 2022 23:58:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:208577394199773ff99d68d668bf4830314a173d7de8407e2bc5666b1d6d4a34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96128257f8f2facb4a2f726619b86453544d9108ec209c3665ec78c2dd14acf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2841d6664b8897473f39b595b9aa4b28e749f587dc1afa4a0027ae507f37ee1f in /nats-server 
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:25:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:25:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:25:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f533e6e439ee51f1cf94458f821a20ed162b542d356340957091882ad881d5c1`  
		Last Modified: Fri, 27 May 2022 00:28:16 GMT  
		Size: 4.2 MB (4242287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1306305db51c19253939f28312d2e4a694eab31b920aeef7d9a4d0a0b76f045`  
		Last Modified: Fri, 27 May 2022 00:28:13 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:87b1afbd78a75ee48cb6b37a8522bbb01f5e9b5047b095b16cc4f241774a48d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bce5ae01237736c7e0447d8cd1b2dbe252eab3ab5ac3b05d98b646b2575cee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:53:56 GMT
COPY file:2dbd94c6c11f89ceba3241f1efe469d0a06f0aae91abb77f3d79756676d0be57 in /nats-server 
# Thu, 26 May 2022 23:53:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:53:57 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:53:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:54:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c74770da2ea808362085edd6dead652091b3e3d34c1e32c50015a6a5bb36c02`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 4.2 MB (4227378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988af7458b707048622e497d5ae818b77d3a24ed0295a7897ced8f003179f7f9`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:9843c2cc2398441da615f9933feb523a1f638c3f3213b593f3e5e7921e1fd74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:73e71a703e620efe92f4bdcfc0c525c8c472f4bb82d4ab6a57a8e560cf79b5fb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107773608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effb063d7055b399920066dd934fcbc50ff93b5460629fdcf20c7a4ff27ca62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:26:00 GMT
RUN cmd /S /C #(nop) COPY file:88c957e774978b3592c1072a38fbf2d578a30b42e89604bf16828cccd9f86b17 in C:\nats-server.exe 
# Fri, 27 May 2022 00:26:01 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:26:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23039a0ccbad6fe276c7cbdbe79f9f030b86f2178198f439eeed20e1ff64877b`  
		Last Modified: Fri, 27 May 2022 01:15:17 GMT  
		Size: 4.6 MB (4633261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59573cd0506705779a3d37bf4d344d3589369ce3279557bd5bda46df763cf5b`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efde216ebb9b658047beb227fed499b9c7596c5e58f2401bfb16e16b24114701`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909550900786c7eead4015a4b0b2ac76493686621fab1d9aa15fa40fd569265`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a62fba798d3b46ba25a1df431d84098e426985250293108cfec350146ddfc0f`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:9843c2cc2398441da615f9933feb523a1f638c3f3213b593f3e5e7921e1fd74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:73e71a703e620efe92f4bdcfc0c525c8c472f4bb82d4ab6a57a8e560cf79b5fb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107773608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effb063d7055b399920066dd934fcbc50ff93b5460629fdcf20c7a4ff27ca62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:26:00 GMT
RUN cmd /S /C #(nop) COPY file:88c957e774978b3592c1072a38fbf2d578a30b42e89604bf16828cccd9f86b17 in C:\nats-server.exe 
# Fri, 27 May 2022 00:26:01 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:26:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23039a0ccbad6fe276c7cbdbe79f9f030b86f2178198f439eeed20e1ff64877b`  
		Last Modified: Fri, 27 May 2022 01:15:17 GMT  
		Size: 4.6 MB (4633261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59573cd0506705779a3d37bf4d344d3589369ce3279557bd5bda46df763cf5b`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efde216ebb9b658047beb227fed499b9c7596c5e58f2401bfb16e16b24114701`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909550900786c7eead4015a4b0b2ac76493686621fab1d9aa15fa40fd569265`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a62fba798d3b46ba25a1df431d84098e426985250293108cfec350146ddfc0f`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:6e96b99197f9d66e34df638ca22426d21963c643bfd0c987b45f1aecb814bc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:796298f636925dedbbdfa537f42423dffd3a69b70c3a9bf4fd0982886a4b745d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842c053e15bdb38e697668b1f0721313203f7c2297eb6d79000f20858dc97854`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:38:26 GMT
COPY file:c866dea678e8cec7cbd0798a1dbdefc45e992d9df374709f6000bac517589a1b in /nats-server 
# Fri, 27 May 2022 00:38:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:38:27 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:38:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:38:27 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:38:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e5797f39fa0527a3dd0a137353b40f97c71134e7eb38373d9791c5f1392885b`  
		Last Modified: Fri, 27 May 2022 00:39:15 GMT  
		Size: 4.6 MB (4591087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3b732adf61929b0b23ca08934cd89923e9cd9d7061544e76bbce57a9fa1e4`  
		Last Modified: Fri, 27 May 2022 00:39:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7df9a2712c9b7e57f228a270f9fdfaf95f8662890dd90719ab08952fe93cc99d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86f50672b8fb25a83d599295659904a27d366e8cad89089ddb9171c79e31c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:56:05 GMT
COPY file:8de8b0cf8e6edf54e413c112cd66aed537abed387a26ba749a9293d43cdf6594 in /nats-server 
# Thu, 26 May 2022 23:56:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:56:05 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:56:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:56:06 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:56:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:770fa9c168613edbe7aa7007d2cf8492c6570efc1ddab217fa32772c6b72dd48`  
		Last Modified: Thu, 26 May 2022 23:58:21 GMT  
		Size: 4.2 MB (4245317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d80ba54887e3752f04df58e1ab68c9805dc2aee54c543d487d8d51a2c88afc1`  
		Last Modified: Thu, 26 May 2022 23:58:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:208577394199773ff99d68d668bf4830314a173d7de8407e2bc5666b1d6d4a34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96128257f8f2facb4a2f726619b86453544d9108ec209c3665ec78c2dd14acf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2841d6664b8897473f39b595b9aa4b28e749f587dc1afa4a0027ae507f37ee1f in /nats-server 
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:25:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:25:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:25:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f533e6e439ee51f1cf94458f821a20ed162b542d356340957091882ad881d5c1`  
		Last Modified: Fri, 27 May 2022 00:28:16 GMT  
		Size: 4.2 MB (4242287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1306305db51c19253939f28312d2e4a694eab31b920aeef7d9a4d0a0b76f045`  
		Last Modified: Fri, 27 May 2022 00:28:13 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:87b1afbd78a75ee48cb6b37a8522bbb01f5e9b5047b095b16cc4f241774a48d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bce5ae01237736c7e0447d8cd1b2dbe252eab3ab5ac3b05d98b646b2575cee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:53:56 GMT
COPY file:2dbd94c6c11f89ceba3241f1efe469d0a06f0aae91abb77f3d79756676d0be57 in /nats-server 
# Thu, 26 May 2022 23:53:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:53:57 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:53:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:54:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c74770da2ea808362085edd6dead652091b3e3d34c1e32c50015a6a5bb36c02`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 4.2 MB (4227378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988af7458b707048622e497d5ae818b77d3a24ed0295a7897ced8f003179f7f9`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:21e6b0cbe3d42465b9005d70c7795eeaf812457704fed30ce2ff785c6378a14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:611c3122e7feffc2768797eac1184a3ffc57c69ed7f023bf7066607f0b006177
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2509547985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16ab36597c6cc5b853a849d91bff282fe7575d89c8d72bacf35977f112ddff2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:23:15 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:23:16 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.4/nats-server-v2.8.4-windows-amd64.zip
# Fri, 27 May 2022 00:23:17 GMT
ENV NATS_SERVER_SHASUM=911e8b77cf288c6e0997891d1400e5cc59dedd928e8f1685650c468674b52dc8
# Fri, 27 May 2022 00:24:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 27 May 2022 00:25:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 27 May 2022 00:25:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:25:40 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e46883112793fbc3f4ba503e0c3adda871fe219fa4792e791c1b0131ec4b76a`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270932ccc85285da4c78794de461bdbf36ec177518c5c609edf7332a3c0e9903`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a573a05b073e99843fb03188f4140e47a95892936eee597e6612b68dea7a276a`  
		Last Modified: Fri, 27 May 2022 01:14:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceeeeb1511ea57b0f10413c14390340603ed50966f7f91aad559fcc32284a027`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 497.4 KB (497353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee183f3745d31b3ab9904f03c5506b37bda08b06abc88817563f753d699c4aba`  
		Last Modified: Fri, 27 May 2022 01:14:55 GMT  
		Size: 5.0 MB (4981575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e67025d9a010ea39c79da6be0497e87fda67f62551adc4d81a0e83f06ee4527`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea59effc695238f40330bf321e135d548663a258eb2de36e3cbd0ecc2eb4f0e`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e27ce3724613991b447f6c75de82694a6e3df3a5e6b2f6cb4044f7aa89f3ca`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08833d90efc546bc030a1d2c6f4b15d21da31004d9c19858e051a00407eecc56`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:21e6b0cbe3d42465b9005d70c7795eeaf812457704fed30ce2ff785c6378a14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:611c3122e7feffc2768797eac1184a3ffc57c69ed7f023bf7066607f0b006177
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2509547985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16ab36597c6cc5b853a849d91bff282fe7575d89c8d72bacf35977f112ddff2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:23:15 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:23:16 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.4/nats-server-v2.8.4-windows-amd64.zip
# Fri, 27 May 2022 00:23:17 GMT
ENV NATS_SERVER_SHASUM=911e8b77cf288c6e0997891d1400e5cc59dedd928e8f1685650c468674b52dc8
# Fri, 27 May 2022 00:24:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 27 May 2022 00:25:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 27 May 2022 00:25:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:25:40 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e46883112793fbc3f4ba503e0c3adda871fe219fa4792e791c1b0131ec4b76a`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270932ccc85285da4c78794de461bdbf36ec177518c5c609edf7332a3c0e9903`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a573a05b073e99843fb03188f4140e47a95892936eee597e6612b68dea7a276a`  
		Last Modified: Fri, 27 May 2022 01:14:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceeeeb1511ea57b0f10413c14390340603ed50966f7f91aad559fcc32284a027`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 497.4 KB (497353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee183f3745d31b3ab9904f03c5506b37bda08b06abc88817563f753d699c4aba`  
		Last Modified: Fri, 27 May 2022 01:14:55 GMT  
		Size: 5.0 MB (4981575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e67025d9a010ea39c79da6be0497e87fda67f62551adc4d81a0e83f06ee4527`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea59effc695238f40330bf321e135d548663a258eb2de36e3cbd0ecc2eb4f0e`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e27ce3724613991b447f6c75de82694a6e3df3a5e6b2f6cb4044f7aa89f3ca`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08833d90efc546bc030a1d2c6f4b15d21da31004d9c19858e051a00407eecc56`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8`

```console
$ docker pull nats@sha256:9686d73262f91e44c10b838eecbab53e705d2f4be5718efe92dfdf9f86f4e786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2928; amd64

### `nats:2.8` - linux; amd64

```console
$ docker pull nats@sha256:796298f636925dedbbdfa537f42423dffd3a69b70c3a9bf4fd0982886a4b745d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842c053e15bdb38e697668b1f0721313203f7c2297eb6d79000f20858dc97854`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:38:26 GMT
COPY file:c866dea678e8cec7cbd0798a1dbdefc45e992d9df374709f6000bac517589a1b in /nats-server 
# Fri, 27 May 2022 00:38:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:38:27 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:38:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:38:27 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:38:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e5797f39fa0527a3dd0a137353b40f97c71134e7eb38373d9791c5f1392885b`  
		Last Modified: Fri, 27 May 2022 00:39:15 GMT  
		Size: 4.6 MB (4591087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3b732adf61929b0b23ca08934cd89923e9cd9d7061544e76bbce57a9fa1e4`  
		Last Modified: Fri, 27 May 2022 00:39:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8` - linux; arm variant v6

```console
$ docker pull nats@sha256:7df9a2712c9b7e57f228a270f9fdfaf95f8662890dd90719ab08952fe93cc99d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86f50672b8fb25a83d599295659904a27d366e8cad89089ddb9171c79e31c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:56:05 GMT
COPY file:8de8b0cf8e6edf54e413c112cd66aed537abed387a26ba749a9293d43cdf6594 in /nats-server 
# Thu, 26 May 2022 23:56:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:56:05 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:56:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:56:06 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:56:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:770fa9c168613edbe7aa7007d2cf8492c6570efc1ddab217fa32772c6b72dd48`  
		Last Modified: Thu, 26 May 2022 23:58:21 GMT  
		Size: 4.2 MB (4245317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d80ba54887e3752f04df58e1ab68c9805dc2aee54c543d487d8d51a2c88afc1`  
		Last Modified: Thu, 26 May 2022 23:58:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8` - linux; arm variant v7

```console
$ docker pull nats@sha256:208577394199773ff99d68d668bf4830314a173d7de8407e2bc5666b1d6d4a34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96128257f8f2facb4a2f726619b86453544d9108ec209c3665ec78c2dd14acf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2841d6664b8897473f39b595b9aa4b28e749f587dc1afa4a0027ae507f37ee1f in /nats-server 
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:25:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:25:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:25:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f533e6e439ee51f1cf94458f821a20ed162b542d356340957091882ad881d5c1`  
		Last Modified: Fri, 27 May 2022 00:28:16 GMT  
		Size: 4.2 MB (4242287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1306305db51c19253939f28312d2e4a694eab31b920aeef7d9a4d0a0b76f045`  
		Last Modified: Fri, 27 May 2022 00:28:13 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:87b1afbd78a75ee48cb6b37a8522bbb01f5e9b5047b095b16cc4f241774a48d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bce5ae01237736c7e0447d8cd1b2dbe252eab3ab5ac3b05d98b646b2575cee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:53:56 GMT
COPY file:2dbd94c6c11f89ceba3241f1efe469d0a06f0aae91abb77f3d79756676d0be57 in /nats-server 
# Thu, 26 May 2022 23:53:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:53:57 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:53:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:54:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c74770da2ea808362085edd6dead652091b3e3d34c1e32c50015a6a5bb36c02`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 4.2 MB (4227378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988af7458b707048622e497d5ae818b77d3a24ed0295a7897ced8f003179f7f9`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:73e71a703e620efe92f4bdcfc0c525c8c472f4bb82d4ab6a57a8e560cf79b5fb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107773608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effb063d7055b399920066dd934fcbc50ff93b5460629fdcf20c7a4ff27ca62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:26:00 GMT
RUN cmd /S /C #(nop) COPY file:88c957e774978b3592c1072a38fbf2d578a30b42e89604bf16828cccd9f86b17 in C:\nats-server.exe 
# Fri, 27 May 2022 00:26:01 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:26:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23039a0ccbad6fe276c7cbdbe79f9f030b86f2178198f439eeed20e1ff64877b`  
		Last Modified: Fri, 27 May 2022 01:15:17 GMT  
		Size: 4.6 MB (4633261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59573cd0506705779a3d37bf4d344d3589369ce3279557bd5bda46df763cf5b`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efde216ebb9b658047beb227fed499b9c7596c5e58f2401bfb16e16b24114701`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909550900786c7eead4015a4b0b2ac76493686621fab1d9aa15fa40fd569265`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a62fba798d3b46ba25a1df431d84098e426985250293108cfec350146ddfc0f`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-alpine`

```console
$ docker pull nats@sha256:24d2a7b7394e612109c861692f83d5ac3bb5d44e61d07002b333335564e0c76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.8-alpine` - linux; amd64

```console
$ docker pull nats@sha256:4199deae36b30cf612a8a5ac96614e60dba809dd72d73a5d3534faa521a12261
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48fd9739aa3f72822ff0234951c748e1933512aff2aa6631c4cf8e4f9b6692c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:37:50 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:37:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 May 2022 00:37:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 May 2022 00:37:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 May 2022 00:37:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 May 2022 00:37:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415d0ea53c276a355c1209aed0a7e21521ddf40ad8a8e0ec3d72d8593a2ba455`  
		Last Modified: Fri, 27 May 2022 00:38:52 GMT  
		Size: 4.9 MB (4864532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05146d3cba39de864032f28506c4921cd565c57aeb729108ac8d0b11c3276bbc`  
		Last Modified: Fri, 27 May 2022 00:38:51 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc9a9ede479a70c4e0d44d902e64c19eca0cd12baf3624ecf0e77d74fde28ef`  
		Last Modified: Fri, 27 May 2022 00:38:51 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:8b48b81efe06e10f92980ce446aa199c35e591e6e61f6a508e8e5b83b993c75c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7141581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fcaa7e9654b63fb8642995444c1d4e0c884d6bfc2a16fdb8a7a39e137b5208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 23:55:37 GMT
ENV NATS_SERVER=2.8.4
# Thu, 26 May 2022 23:55:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 26 May 2022 23:55:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 26 May 2022 23:55:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 26 May 2022 23:55:43 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:55:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 May 2022 23:55:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50f68c47a108ab599d7f0e191ffaf378e6dce6a928151e691d8ea726aeb928`  
		Last Modified: Thu, 26 May 2022 23:57:46 GMT  
		Size: 4.5 MB (4518611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4cb9d5e8d247c55e5f7e46c8d54ea485f55806c24444feaf62725d6ba170f1`  
		Last Modified: Thu, 26 May 2022 23:57:43 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c6a3cdd4a881f42229288ebba9a675d7abe171cd2b2838becae58d1aad6ab`  
		Last Modified: Thu, 26 May 2022 23:57:43 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ba8d5358e4179eedb8812098fe9aafac97d3cbc262c5c661e8f7a0c91a5bbcb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6939129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eca0f2ec4b22a18d9e30a03a72c0b72555d4cdbcbcb8ff15552cc1d01442c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:25:21 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:25:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 May 2022 00:25:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 May 2022 00:25:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 May 2022 00:25:26 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 May 2022 00:25:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f90a00ed33ea115d275ac961047e5009b1e24e2103dbfaed2ab8f52856c975`  
		Last Modified: Fri, 27 May 2022 00:27:40 GMT  
		Size: 4.5 MB (4513806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd41cd9dfa9b3a42fea8a47e1a69c57faa29f3cdd27489fc7f4fe699d283f899`  
		Last Modified: Fri, 27 May 2022 00:27:37 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed506c19493a71093e162dbcebe70d57fc6c372d9c201a32ef0515b66da395b7`  
		Last Modified: Fri, 27 May 2022 00:27:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:068170580c70c9c06e2050fa9c6f66ec28f61c9062663cf2b45db2eed7e6b3d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7218027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fa83e475ee42455e6e7021633d7a98bb6496a5a75621f389dff13b1ceaa343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 23:53:38 GMT
ENV NATS_SERVER=2.8.4
# Thu, 26 May 2022 23:53:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 26 May 2022 23:53:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 26 May 2022 23:53:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 26 May 2022 23:53:43 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 May 2022 23:53:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48649cc80ad9a6544bde7c572f66e6a5f2c0e918923a957045cfea77bbf31bb`  
		Last Modified: Thu, 26 May 2022 23:54:50 GMT  
		Size: 4.5 MB (4500578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bbb498a8d1c04c80271b66119f843bc9a68cf260f1fc0005babdb8ef1820b8`  
		Last Modified: Thu, 26 May 2022 23:54:49 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ca2313cb9b3e722a83aa9f01456f583d124cbb90aa75908b33a0c37ecdaeb`  
		Last Modified: Thu, 26 May 2022 23:54:49 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-alpine3.15`

```console
$ docker pull nats@sha256:24d2a7b7394e612109c861692f83d5ac3bb5d44e61d07002b333335564e0c76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.8-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:4199deae36b30cf612a8a5ac96614e60dba809dd72d73a5d3534faa521a12261
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48fd9739aa3f72822ff0234951c748e1933512aff2aa6631c4cf8e4f9b6692c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:37:50 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:37:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 May 2022 00:37:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 May 2022 00:37:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 May 2022 00:37:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 May 2022 00:37:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415d0ea53c276a355c1209aed0a7e21521ddf40ad8a8e0ec3d72d8593a2ba455`  
		Last Modified: Fri, 27 May 2022 00:38:52 GMT  
		Size: 4.9 MB (4864532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05146d3cba39de864032f28506c4921cd565c57aeb729108ac8d0b11c3276bbc`  
		Last Modified: Fri, 27 May 2022 00:38:51 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc9a9ede479a70c4e0d44d902e64c19eca0cd12baf3624ecf0e77d74fde28ef`  
		Last Modified: Fri, 27 May 2022 00:38:51 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:8b48b81efe06e10f92980ce446aa199c35e591e6e61f6a508e8e5b83b993c75c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7141581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fcaa7e9654b63fb8642995444c1d4e0c884d6bfc2a16fdb8a7a39e137b5208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 23:55:37 GMT
ENV NATS_SERVER=2.8.4
# Thu, 26 May 2022 23:55:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 26 May 2022 23:55:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 26 May 2022 23:55:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 26 May 2022 23:55:43 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:55:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 May 2022 23:55:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50f68c47a108ab599d7f0e191ffaf378e6dce6a928151e691d8ea726aeb928`  
		Last Modified: Thu, 26 May 2022 23:57:46 GMT  
		Size: 4.5 MB (4518611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4cb9d5e8d247c55e5f7e46c8d54ea485f55806c24444feaf62725d6ba170f1`  
		Last Modified: Thu, 26 May 2022 23:57:43 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c6a3cdd4a881f42229288ebba9a675d7abe171cd2b2838becae58d1aad6ab`  
		Last Modified: Thu, 26 May 2022 23:57:43 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ba8d5358e4179eedb8812098fe9aafac97d3cbc262c5c661e8f7a0c91a5bbcb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6939129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eca0f2ec4b22a18d9e30a03a72c0b72555d4cdbcbcb8ff15552cc1d01442c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:25:21 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:25:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 May 2022 00:25:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 May 2022 00:25:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 May 2022 00:25:26 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 May 2022 00:25:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f90a00ed33ea115d275ac961047e5009b1e24e2103dbfaed2ab8f52856c975`  
		Last Modified: Fri, 27 May 2022 00:27:40 GMT  
		Size: 4.5 MB (4513806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd41cd9dfa9b3a42fea8a47e1a69c57faa29f3cdd27489fc7f4fe699d283f899`  
		Last Modified: Fri, 27 May 2022 00:27:37 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed506c19493a71093e162dbcebe70d57fc6c372d9c201a32ef0515b66da395b7`  
		Last Modified: Fri, 27 May 2022 00:27:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:068170580c70c9c06e2050fa9c6f66ec28f61c9062663cf2b45db2eed7e6b3d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7218027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fa83e475ee42455e6e7021633d7a98bb6496a5a75621f389dff13b1ceaa343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 23:53:38 GMT
ENV NATS_SERVER=2.8.4
# Thu, 26 May 2022 23:53:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 26 May 2022 23:53:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 26 May 2022 23:53:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 26 May 2022 23:53:43 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 May 2022 23:53:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48649cc80ad9a6544bde7c572f66e6a5f2c0e918923a957045cfea77bbf31bb`  
		Last Modified: Thu, 26 May 2022 23:54:50 GMT  
		Size: 4.5 MB (4500578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bbb498a8d1c04c80271b66119f843bc9a68cf260f1fc0005babdb8ef1820b8`  
		Last Modified: Thu, 26 May 2022 23:54:49 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ca2313cb9b3e722a83aa9f01456f583d124cbb90aa75908b33a0c37ecdaeb`  
		Last Modified: Thu, 26 May 2022 23:54:49 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-linux`

```console
$ docker pull nats@sha256:6e96b99197f9d66e34df638ca22426d21963c643bfd0c987b45f1aecb814bc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.8-linux` - linux; amd64

```console
$ docker pull nats@sha256:796298f636925dedbbdfa537f42423dffd3a69b70c3a9bf4fd0982886a4b745d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842c053e15bdb38e697668b1f0721313203f7c2297eb6d79000f20858dc97854`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:38:26 GMT
COPY file:c866dea678e8cec7cbd0798a1dbdefc45e992d9df374709f6000bac517589a1b in /nats-server 
# Fri, 27 May 2022 00:38:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:38:27 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:38:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:38:27 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:38:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e5797f39fa0527a3dd0a137353b40f97c71134e7eb38373d9791c5f1392885b`  
		Last Modified: Fri, 27 May 2022 00:39:15 GMT  
		Size: 4.6 MB (4591087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3b732adf61929b0b23ca08934cd89923e9cd9d7061544e76bbce57a9fa1e4`  
		Last Modified: Fri, 27 May 2022 00:39:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7df9a2712c9b7e57f228a270f9fdfaf95f8662890dd90719ab08952fe93cc99d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86f50672b8fb25a83d599295659904a27d366e8cad89089ddb9171c79e31c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:56:05 GMT
COPY file:8de8b0cf8e6edf54e413c112cd66aed537abed387a26ba749a9293d43cdf6594 in /nats-server 
# Thu, 26 May 2022 23:56:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:56:05 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:56:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:56:06 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:56:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:770fa9c168613edbe7aa7007d2cf8492c6570efc1ddab217fa32772c6b72dd48`  
		Last Modified: Thu, 26 May 2022 23:58:21 GMT  
		Size: 4.2 MB (4245317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d80ba54887e3752f04df58e1ab68c9805dc2aee54c543d487d8d51a2c88afc1`  
		Last Modified: Thu, 26 May 2022 23:58:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:208577394199773ff99d68d668bf4830314a173d7de8407e2bc5666b1d6d4a34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96128257f8f2facb4a2f726619b86453544d9108ec209c3665ec78c2dd14acf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2841d6664b8897473f39b595b9aa4b28e749f587dc1afa4a0027ae507f37ee1f in /nats-server 
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:25:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:25:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:25:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f533e6e439ee51f1cf94458f821a20ed162b542d356340957091882ad881d5c1`  
		Last Modified: Fri, 27 May 2022 00:28:16 GMT  
		Size: 4.2 MB (4242287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1306305db51c19253939f28312d2e4a694eab31b920aeef7d9a4d0a0b76f045`  
		Last Modified: Fri, 27 May 2022 00:28:13 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:87b1afbd78a75ee48cb6b37a8522bbb01f5e9b5047b095b16cc4f241774a48d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bce5ae01237736c7e0447d8cd1b2dbe252eab3ab5ac3b05d98b646b2575cee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:53:56 GMT
COPY file:2dbd94c6c11f89ceba3241f1efe469d0a06f0aae91abb77f3d79756676d0be57 in /nats-server 
# Thu, 26 May 2022 23:53:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:53:57 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:53:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:54:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c74770da2ea808362085edd6dead652091b3e3d34c1e32c50015a6a5bb36c02`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 4.2 MB (4227378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988af7458b707048622e497d5ae818b77d3a24ed0295a7897ced8f003179f7f9`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-nanoserver`

```console
$ docker pull nats@sha256:9843c2cc2398441da615f9933feb523a1f638c3f3213b593f3e5e7921e1fd74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2.8-nanoserver` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:73e71a703e620efe92f4bdcfc0c525c8c472f4bb82d4ab6a57a8e560cf79b5fb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107773608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effb063d7055b399920066dd934fcbc50ff93b5460629fdcf20c7a4ff27ca62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:26:00 GMT
RUN cmd /S /C #(nop) COPY file:88c957e774978b3592c1072a38fbf2d578a30b42e89604bf16828cccd9f86b17 in C:\nats-server.exe 
# Fri, 27 May 2022 00:26:01 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:26:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23039a0ccbad6fe276c7cbdbe79f9f030b86f2178198f439eeed20e1ff64877b`  
		Last Modified: Fri, 27 May 2022 01:15:17 GMT  
		Size: 4.6 MB (4633261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59573cd0506705779a3d37bf4d344d3589369ce3279557bd5bda46df763cf5b`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efde216ebb9b658047beb227fed499b9c7596c5e58f2401bfb16e16b24114701`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909550900786c7eead4015a4b0b2ac76493686621fab1d9aa15fa40fd569265`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a62fba798d3b46ba25a1df431d84098e426985250293108cfec350146ddfc0f`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-nanoserver-1809`

```console
$ docker pull nats@sha256:9843c2cc2398441da615f9933feb523a1f638c3f3213b593f3e5e7921e1fd74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2.8-nanoserver-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:73e71a703e620efe92f4bdcfc0c525c8c472f4bb82d4ab6a57a8e560cf79b5fb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107773608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effb063d7055b399920066dd934fcbc50ff93b5460629fdcf20c7a4ff27ca62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:26:00 GMT
RUN cmd /S /C #(nop) COPY file:88c957e774978b3592c1072a38fbf2d578a30b42e89604bf16828cccd9f86b17 in C:\nats-server.exe 
# Fri, 27 May 2022 00:26:01 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:26:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23039a0ccbad6fe276c7cbdbe79f9f030b86f2178198f439eeed20e1ff64877b`  
		Last Modified: Fri, 27 May 2022 01:15:17 GMT  
		Size: 4.6 MB (4633261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59573cd0506705779a3d37bf4d344d3589369ce3279557bd5bda46df763cf5b`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efde216ebb9b658047beb227fed499b9c7596c5e58f2401bfb16e16b24114701`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909550900786c7eead4015a4b0b2ac76493686621fab1d9aa15fa40fd569265`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a62fba798d3b46ba25a1df431d84098e426985250293108cfec350146ddfc0f`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-scratch`

```console
$ docker pull nats@sha256:6e96b99197f9d66e34df638ca22426d21963c643bfd0c987b45f1aecb814bc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.8-scratch` - linux; amd64

```console
$ docker pull nats@sha256:796298f636925dedbbdfa537f42423dffd3a69b70c3a9bf4fd0982886a4b745d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842c053e15bdb38e697668b1f0721313203f7c2297eb6d79000f20858dc97854`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:38:26 GMT
COPY file:c866dea678e8cec7cbd0798a1dbdefc45e992d9df374709f6000bac517589a1b in /nats-server 
# Fri, 27 May 2022 00:38:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:38:27 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:38:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:38:27 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:38:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e5797f39fa0527a3dd0a137353b40f97c71134e7eb38373d9791c5f1392885b`  
		Last Modified: Fri, 27 May 2022 00:39:15 GMT  
		Size: 4.6 MB (4591087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3b732adf61929b0b23ca08934cd89923e9cd9d7061544e76bbce57a9fa1e4`  
		Last Modified: Fri, 27 May 2022 00:39:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7df9a2712c9b7e57f228a270f9fdfaf95f8662890dd90719ab08952fe93cc99d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86f50672b8fb25a83d599295659904a27d366e8cad89089ddb9171c79e31c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:56:05 GMT
COPY file:8de8b0cf8e6edf54e413c112cd66aed537abed387a26ba749a9293d43cdf6594 in /nats-server 
# Thu, 26 May 2022 23:56:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:56:05 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:56:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:56:06 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:56:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:770fa9c168613edbe7aa7007d2cf8492c6570efc1ddab217fa32772c6b72dd48`  
		Last Modified: Thu, 26 May 2022 23:58:21 GMT  
		Size: 4.2 MB (4245317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d80ba54887e3752f04df58e1ab68c9805dc2aee54c543d487d8d51a2c88afc1`  
		Last Modified: Thu, 26 May 2022 23:58:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:208577394199773ff99d68d668bf4830314a173d7de8407e2bc5666b1d6d4a34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96128257f8f2facb4a2f726619b86453544d9108ec209c3665ec78c2dd14acf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2841d6664b8897473f39b595b9aa4b28e749f587dc1afa4a0027ae507f37ee1f in /nats-server 
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:25:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:25:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:25:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f533e6e439ee51f1cf94458f821a20ed162b542d356340957091882ad881d5c1`  
		Last Modified: Fri, 27 May 2022 00:28:16 GMT  
		Size: 4.2 MB (4242287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1306305db51c19253939f28312d2e4a694eab31b920aeef7d9a4d0a0b76f045`  
		Last Modified: Fri, 27 May 2022 00:28:13 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:87b1afbd78a75ee48cb6b37a8522bbb01f5e9b5047b095b16cc4f241774a48d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bce5ae01237736c7e0447d8cd1b2dbe252eab3ab5ac3b05d98b646b2575cee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:53:56 GMT
COPY file:2dbd94c6c11f89ceba3241f1efe469d0a06f0aae91abb77f3d79756676d0be57 in /nats-server 
# Thu, 26 May 2022 23:53:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:53:57 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:53:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:54:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c74770da2ea808362085edd6dead652091b3e3d34c1e32c50015a6a5bb36c02`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 4.2 MB (4227378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988af7458b707048622e497d5ae818b77d3a24ed0295a7897ced8f003179f7f9`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-windowsservercore`

```console
$ docker pull nats@sha256:21e6b0cbe3d42465b9005d70c7795eeaf812457704fed30ce2ff785c6378a14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2.8-windowsservercore` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:611c3122e7feffc2768797eac1184a3ffc57c69ed7f023bf7066607f0b006177
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2509547985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16ab36597c6cc5b853a849d91bff282fe7575d89c8d72bacf35977f112ddff2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:23:15 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:23:16 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.4/nats-server-v2.8.4-windows-amd64.zip
# Fri, 27 May 2022 00:23:17 GMT
ENV NATS_SERVER_SHASUM=911e8b77cf288c6e0997891d1400e5cc59dedd928e8f1685650c468674b52dc8
# Fri, 27 May 2022 00:24:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 27 May 2022 00:25:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 27 May 2022 00:25:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:25:40 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e46883112793fbc3f4ba503e0c3adda871fe219fa4792e791c1b0131ec4b76a`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270932ccc85285da4c78794de461bdbf36ec177518c5c609edf7332a3c0e9903`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a573a05b073e99843fb03188f4140e47a95892936eee597e6612b68dea7a276a`  
		Last Modified: Fri, 27 May 2022 01:14:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceeeeb1511ea57b0f10413c14390340603ed50966f7f91aad559fcc32284a027`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 497.4 KB (497353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee183f3745d31b3ab9904f03c5506b37bda08b06abc88817563f753d699c4aba`  
		Last Modified: Fri, 27 May 2022 01:14:55 GMT  
		Size: 5.0 MB (4981575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e67025d9a010ea39c79da6be0497e87fda67f62551adc4d81a0e83f06ee4527`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea59effc695238f40330bf321e135d548663a258eb2de36e3cbd0ecc2eb4f0e`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e27ce3724613991b447f6c75de82694a6e3df3a5e6b2f6cb4044f7aa89f3ca`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08833d90efc546bc030a1d2c6f4b15d21da31004d9c19858e051a00407eecc56`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-windowsservercore-1809`

```console
$ docker pull nats@sha256:21e6b0cbe3d42465b9005d70c7795eeaf812457704fed30ce2ff785c6378a14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2.8-windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:611c3122e7feffc2768797eac1184a3ffc57c69ed7f023bf7066607f0b006177
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2509547985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16ab36597c6cc5b853a849d91bff282fe7575d89c8d72bacf35977f112ddff2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:23:15 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:23:16 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.4/nats-server-v2.8.4-windows-amd64.zip
# Fri, 27 May 2022 00:23:17 GMT
ENV NATS_SERVER_SHASUM=911e8b77cf288c6e0997891d1400e5cc59dedd928e8f1685650c468674b52dc8
# Fri, 27 May 2022 00:24:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 27 May 2022 00:25:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 27 May 2022 00:25:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:25:40 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e46883112793fbc3f4ba503e0c3adda871fe219fa4792e791c1b0131ec4b76a`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270932ccc85285da4c78794de461bdbf36ec177518c5c609edf7332a3c0e9903`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a573a05b073e99843fb03188f4140e47a95892936eee597e6612b68dea7a276a`  
		Last Modified: Fri, 27 May 2022 01:14:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceeeeb1511ea57b0f10413c14390340603ed50966f7f91aad559fcc32284a027`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 497.4 KB (497353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee183f3745d31b3ab9904f03c5506b37bda08b06abc88817563f753d699c4aba`  
		Last Modified: Fri, 27 May 2022 01:14:55 GMT  
		Size: 5.0 MB (4981575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e67025d9a010ea39c79da6be0497e87fda67f62551adc4d81a0e83f06ee4527`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea59effc695238f40330bf321e135d548663a258eb2de36e3cbd0ecc2eb4f0e`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e27ce3724613991b447f6c75de82694a6e3df3a5e6b2f6cb4044f7aa89f3ca`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08833d90efc546bc030a1d2c6f4b15d21da31004d9c19858e051a00407eecc56`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8.4`

```console
$ docker pull nats@sha256:9686d73262f91e44c10b838eecbab53e705d2f4be5718efe92dfdf9f86f4e786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2928; amd64

### `nats:2.8.4` - linux; amd64

```console
$ docker pull nats@sha256:796298f636925dedbbdfa537f42423dffd3a69b70c3a9bf4fd0982886a4b745d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842c053e15bdb38e697668b1f0721313203f7c2297eb6d79000f20858dc97854`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:38:26 GMT
COPY file:c866dea678e8cec7cbd0798a1dbdefc45e992d9df374709f6000bac517589a1b in /nats-server 
# Fri, 27 May 2022 00:38:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:38:27 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:38:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:38:27 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:38:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e5797f39fa0527a3dd0a137353b40f97c71134e7eb38373d9791c5f1392885b`  
		Last Modified: Fri, 27 May 2022 00:39:15 GMT  
		Size: 4.6 MB (4591087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3b732adf61929b0b23ca08934cd89923e9cd9d7061544e76bbce57a9fa1e4`  
		Last Modified: Fri, 27 May 2022 00:39:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8.4` - linux; arm variant v6

```console
$ docker pull nats@sha256:7df9a2712c9b7e57f228a270f9fdfaf95f8662890dd90719ab08952fe93cc99d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86f50672b8fb25a83d599295659904a27d366e8cad89089ddb9171c79e31c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:56:05 GMT
COPY file:8de8b0cf8e6edf54e413c112cd66aed537abed387a26ba749a9293d43cdf6594 in /nats-server 
# Thu, 26 May 2022 23:56:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:56:05 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:56:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:56:06 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:56:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:770fa9c168613edbe7aa7007d2cf8492c6570efc1ddab217fa32772c6b72dd48`  
		Last Modified: Thu, 26 May 2022 23:58:21 GMT  
		Size: 4.2 MB (4245317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d80ba54887e3752f04df58e1ab68c9805dc2aee54c543d487d8d51a2c88afc1`  
		Last Modified: Thu, 26 May 2022 23:58:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8.4` - linux; arm variant v7

```console
$ docker pull nats@sha256:208577394199773ff99d68d668bf4830314a173d7de8407e2bc5666b1d6d4a34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96128257f8f2facb4a2f726619b86453544d9108ec209c3665ec78c2dd14acf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2841d6664b8897473f39b595b9aa4b28e749f587dc1afa4a0027ae507f37ee1f in /nats-server 
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:25:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:25:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:25:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f533e6e439ee51f1cf94458f821a20ed162b542d356340957091882ad881d5c1`  
		Last Modified: Fri, 27 May 2022 00:28:16 GMT  
		Size: 4.2 MB (4242287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1306305db51c19253939f28312d2e4a694eab31b920aeef7d9a4d0a0b76f045`  
		Last Modified: Fri, 27 May 2022 00:28:13 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8.4` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:87b1afbd78a75ee48cb6b37a8522bbb01f5e9b5047b095b16cc4f241774a48d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bce5ae01237736c7e0447d8cd1b2dbe252eab3ab5ac3b05d98b646b2575cee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:53:56 GMT
COPY file:2dbd94c6c11f89ceba3241f1efe469d0a06f0aae91abb77f3d79756676d0be57 in /nats-server 
# Thu, 26 May 2022 23:53:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:53:57 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:53:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:54:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c74770da2ea808362085edd6dead652091b3e3d34c1e32c50015a6a5bb36c02`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 4.2 MB (4227378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988af7458b707048622e497d5ae818b77d3a24ed0295a7897ced8f003179f7f9`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8.4` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:73e71a703e620efe92f4bdcfc0c525c8c472f4bb82d4ab6a57a8e560cf79b5fb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107773608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effb063d7055b399920066dd934fcbc50ff93b5460629fdcf20c7a4ff27ca62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:26:00 GMT
RUN cmd /S /C #(nop) COPY file:88c957e774978b3592c1072a38fbf2d578a30b42e89604bf16828cccd9f86b17 in C:\nats-server.exe 
# Fri, 27 May 2022 00:26:01 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:26:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23039a0ccbad6fe276c7cbdbe79f9f030b86f2178198f439eeed20e1ff64877b`  
		Last Modified: Fri, 27 May 2022 01:15:17 GMT  
		Size: 4.6 MB (4633261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59573cd0506705779a3d37bf4d344d3589369ce3279557bd5bda46df763cf5b`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efde216ebb9b658047beb227fed499b9c7596c5e58f2401bfb16e16b24114701`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909550900786c7eead4015a4b0b2ac76493686621fab1d9aa15fa40fd569265`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a62fba798d3b46ba25a1df431d84098e426985250293108cfec350146ddfc0f`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8.4-alpine`

```console
$ docker pull nats@sha256:24d2a7b7394e612109c861692f83d5ac3bb5d44e61d07002b333335564e0c76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.8.4-alpine` - linux; amd64

```console
$ docker pull nats@sha256:4199deae36b30cf612a8a5ac96614e60dba809dd72d73a5d3534faa521a12261
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48fd9739aa3f72822ff0234951c748e1933512aff2aa6631c4cf8e4f9b6692c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:37:50 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:37:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 May 2022 00:37:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 May 2022 00:37:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 May 2022 00:37:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 May 2022 00:37:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415d0ea53c276a355c1209aed0a7e21521ddf40ad8a8e0ec3d72d8593a2ba455`  
		Last Modified: Fri, 27 May 2022 00:38:52 GMT  
		Size: 4.9 MB (4864532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05146d3cba39de864032f28506c4921cd565c57aeb729108ac8d0b11c3276bbc`  
		Last Modified: Fri, 27 May 2022 00:38:51 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc9a9ede479a70c4e0d44d902e64c19eca0cd12baf3624ecf0e77d74fde28ef`  
		Last Modified: Fri, 27 May 2022 00:38:51 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8.4-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:8b48b81efe06e10f92980ce446aa199c35e591e6e61f6a508e8e5b83b993c75c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7141581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fcaa7e9654b63fb8642995444c1d4e0c884d6bfc2a16fdb8a7a39e137b5208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 23:55:37 GMT
ENV NATS_SERVER=2.8.4
# Thu, 26 May 2022 23:55:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 26 May 2022 23:55:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 26 May 2022 23:55:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 26 May 2022 23:55:43 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:55:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 May 2022 23:55:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50f68c47a108ab599d7f0e191ffaf378e6dce6a928151e691d8ea726aeb928`  
		Last Modified: Thu, 26 May 2022 23:57:46 GMT  
		Size: 4.5 MB (4518611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4cb9d5e8d247c55e5f7e46c8d54ea485f55806c24444feaf62725d6ba170f1`  
		Last Modified: Thu, 26 May 2022 23:57:43 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c6a3cdd4a881f42229288ebba9a675d7abe171cd2b2838becae58d1aad6ab`  
		Last Modified: Thu, 26 May 2022 23:57:43 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8.4-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ba8d5358e4179eedb8812098fe9aafac97d3cbc262c5c661e8f7a0c91a5bbcb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6939129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eca0f2ec4b22a18d9e30a03a72c0b72555d4cdbcbcb8ff15552cc1d01442c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:25:21 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:25:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 May 2022 00:25:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 May 2022 00:25:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 May 2022 00:25:26 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 May 2022 00:25:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f90a00ed33ea115d275ac961047e5009b1e24e2103dbfaed2ab8f52856c975`  
		Last Modified: Fri, 27 May 2022 00:27:40 GMT  
		Size: 4.5 MB (4513806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd41cd9dfa9b3a42fea8a47e1a69c57faa29f3cdd27489fc7f4fe699d283f899`  
		Last Modified: Fri, 27 May 2022 00:27:37 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed506c19493a71093e162dbcebe70d57fc6c372d9c201a32ef0515b66da395b7`  
		Last Modified: Fri, 27 May 2022 00:27:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8.4-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:068170580c70c9c06e2050fa9c6f66ec28f61c9062663cf2b45db2eed7e6b3d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7218027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fa83e475ee42455e6e7021633d7a98bb6496a5a75621f389dff13b1ceaa343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 23:53:38 GMT
ENV NATS_SERVER=2.8.4
# Thu, 26 May 2022 23:53:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 26 May 2022 23:53:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 26 May 2022 23:53:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 26 May 2022 23:53:43 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 May 2022 23:53:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48649cc80ad9a6544bde7c572f66e6a5f2c0e918923a957045cfea77bbf31bb`  
		Last Modified: Thu, 26 May 2022 23:54:50 GMT  
		Size: 4.5 MB (4500578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bbb498a8d1c04c80271b66119f843bc9a68cf260f1fc0005babdb8ef1820b8`  
		Last Modified: Thu, 26 May 2022 23:54:49 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ca2313cb9b3e722a83aa9f01456f583d124cbb90aa75908b33a0c37ecdaeb`  
		Last Modified: Thu, 26 May 2022 23:54:49 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8.4-alpine3.15`

```console
$ docker pull nats@sha256:24d2a7b7394e612109c861692f83d5ac3bb5d44e61d07002b333335564e0c76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.8.4-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:4199deae36b30cf612a8a5ac96614e60dba809dd72d73a5d3534faa521a12261
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48fd9739aa3f72822ff0234951c748e1933512aff2aa6631c4cf8e4f9b6692c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:37:50 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:37:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 May 2022 00:37:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 May 2022 00:37:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 May 2022 00:37:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 May 2022 00:37:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415d0ea53c276a355c1209aed0a7e21521ddf40ad8a8e0ec3d72d8593a2ba455`  
		Last Modified: Fri, 27 May 2022 00:38:52 GMT  
		Size: 4.9 MB (4864532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05146d3cba39de864032f28506c4921cd565c57aeb729108ac8d0b11c3276bbc`  
		Last Modified: Fri, 27 May 2022 00:38:51 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc9a9ede479a70c4e0d44d902e64c19eca0cd12baf3624ecf0e77d74fde28ef`  
		Last Modified: Fri, 27 May 2022 00:38:51 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8.4-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:8b48b81efe06e10f92980ce446aa199c35e591e6e61f6a508e8e5b83b993c75c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7141581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fcaa7e9654b63fb8642995444c1d4e0c884d6bfc2a16fdb8a7a39e137b5208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 23:55:37 GMT
ENV NATS_SERVER=2.8.4
# Thu, 26 May 2022 23:55:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 26 May 2022 23:55:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 26 May 2022 23:55:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 26 May 2022 23:55:43 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:55:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 May 2022 23:55:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50f68c47a108ab599d7f0e191ffaf378e6dce6a928151e691d8ea726aeb928`  
		Last Modified: Thu, 26 May 2022 23:57:46 GMT  
		Size: 4.5 MB (4518611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4cb9d5e8d247c55e5f7e46c8d54ea485f55806c24444feaf62725d6ba170f1`  
		Last Modified: Thu, 26 May 2022 23:57:43 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c6a3cdd4a881f42229288ebba9a675d7abe171cd2b2838becae58d1aad6ab`  
		Last Modified: Thu, 26 May 2022 23:57:43 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8.4-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ba8d5358e4179eedb8812098fe9aafac97d3cbc262c5c661e8f7a0c91a5bbcb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6939129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eca0f2ec4b22a18d9e30a03a72c0b72555d4cdbcbcb8ff15552cc1d01442c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:25:21 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:25:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 May 2022 00:25:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 May 2022 00:25:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 May 2022 00:25:26 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 May 2022 00:25:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f90a00ed33ea115d275ac961047e5009b1e24e2103dbfaed2ab8f52856c975`  
		Last Modified: Fri, 27 May 2022 00:27:40 GMT  
		Size: 4.5 MB (4513806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd41cd9dfa9b3a42fea8a47e1a69c57faa29f3cdd27489fc7f4fe699d283f899`  
		Last Modified: Fri, 27 May 2022 00:27:37 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed506c19493a71093e162dbcebe70d57fc6c372d9c201a32ef0515b66da395b7`  
		Last Modified: Fri, 27 May 2022 00:27:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8.4-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:068170580c70c9c06e2050fa9c6f66ec28f61c9062663cf2b45db2eed7e6b3d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7218027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fa83e475ee42455e6e7021633d7a98bb6496a5a75621f389dff13b1ceaa343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 23:53:38 GMT
ENV NATS_SERVER=2.8.4
# Thu, 26 May 2022 23:53:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 26 May 2022 23:53:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 26 May 2022 23:53:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 26 May 2022 23:53:43 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 May 2022 23:53:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48649cc80ad9a6544bde7c572f66e6a5f2c0e918923a957045cfea77bbf31bb`  
		Last Modified: Thu, 26 May 2022 23:54:50 GMT  
		Size: 4.5 MB (4500578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bbb498a8d1c04c80271b66119f843bc9a68cf260f1fc0005babdb8ef1820b8`  
		Last Modified: Thu, 26 May 2022 23:54:49 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ca2313cb9b3e722a83aa9f01456f583d124cbb90aa75908b33a0c37ecdaeb`  
		Last Modified: Thu, 26 May 2022 23:54:49 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8.4-linux`

```console
$ docker pull nats@sha256:6e96b99197f9d66e34df638ca22426d21963c643bfd0c987b45f1aecb814bc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.8.4-linux` - linux; amd64

```console
$ docker pull nats@sha256:796298f636925dedbbdfa537f42423dffd3a69b70c3a9bf4fd0982886a4b745d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842c053e15bdb38e697668b1f0721313203f7c2297eb6d79000f20858dc97854`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:38:26 GMT
COPY file:c866dea678e8cec7cbd0798a1dbdefc45e992d9df374709f6000bac517589a1b in /nats-server 
# Fri, 27 May 2022 00:38:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:38:27 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:38:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:38:27 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:38:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e5797f39fa0527a3dd0a137353b40f97c71134e7eb38373d9791c5f1392885b`  
		Last Modified: Fri, 27 May 2022 00:39:15 GMT  
		Size: 4.6 MB (4591087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3b732adf61929b0b23ca08934cd89923e9cd9d7061544e76bbce57a9fa1e4`  
		Last Modified: Fri, 27 May 2022 00:39:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8.4-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7df9a2712c9b7e57f228a270f9fdfaf95f8662890dd90719ab08952fe93cc99d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86f50672b8fb25a83d599295659904a27d366e8cad89089ddb9171c79e31c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:56:05 GMT
COPY file:8de8b0cf8e6edf54e413c112cd66aed537abed387a26ba749a9293d43cdf6594 in /nats-server 
# Thu, 26 May 2022 23:56:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:56:05 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:56:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:56:06 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:56:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:770fa9c168613edbe7aa7007d2cf8492c6570efc1ddab217fa32772c6b72dd48`  
		Last Modified: Thu, 26 May 2022 23:58:21 GMT  
		Size: 4.2 MB (4245317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d80ba54887e3752f04df58e1ab68c9805dc2aee54c543d487d8d51a2c88afc1`  
		Last Modified: Thu, 26 May 2022 23:58:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8.4-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:208577394199773ff99d68d668bf4830314a173d7de8407e2bc5666b1d6d4a34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96128257f8f2facb4a2f726619b86453544d9108ec209c3665ec78c2dd14acf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2841d6664b8897473f39b595b9aa4b28e749f587dc1afa4a0027ae507f37ee1f in /nats-server 
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:25:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:25:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:25:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f533e6e439ee51f1cf94458f821a20ed162b542d356340957091882ad881d5c1`  
		Last Modified: Fri, 27 May 2022 00:28:16 GMT  
		Size: 4.2 MB (4242287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1306305db51c19253939f28312d2e4a694eab31b920aeef7d9a4d0a0b76f045`  
		Last Modified: Fri, 27 May 2022 00:28:13 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8.4-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:87b1afbd78a75ee48cb6b37a8522bbb01f5e9b5047b095b16cc4f241774a48d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bce5ae01237736c7e0447d8cd1b2dbe252eab3ab5ac3b05d98b646b2575cee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:53:56 GMT
COPY file:2dbd94c6c11f89ceba3241f1efe469d0a06f0aae91abb77f3d79756676d0be57 in /nats-server 
# Thu, 26 May 2022 23:53:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:53:57 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:53:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:54:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c74770da2ea808362085edd6dead652091b3e3d34c1e32c50015a6a5bb36c02`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 4.2 MB (4227378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988af7458b707048622e497d5ae818b77d3a24ed0295a7897ced8f003179f7f9`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8.4-nanoserver`

```console
$ docker pull nats@sha256:9843c2cc2398441da615f9933feb523a1f638c3f3213b593f3e5e7921e1fd74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2.8.4-nanoserver` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:73e71a703e620efe92f4bdcfc0c525c8c472f4bb82d4ab6a57a8e560cf79b5fb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107773608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effb063d7055b399920066dd934fcbc50ff93b5460629fdcf20c7a4ff27ca62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:26:00 GMT
RUN cmd /S /C #(nop) COPY file:88c957e774978b3592c1072a38fbf2d578a30b42e89604bf16828cccd9f86b17 in C:\nats-server.exe 
# Fri, 27 May 2022 00:26:01 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:26:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23039a0ccbad6fe276c7cbdbe79f9f030b86f2178198f439eeed20e1ff64877b`  
		Last Modified: Fri, 27 May 2022 01:15:17 GMT  
		Size: 4.6 MB (4633261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59573cd0506705779a3d37bf4d344d3589369ce3279557bd5bda46df763cf5b`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efde216ebb9b658047beb227fed499b9c7596c5e58f2401bfb16e16b24114701`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909550900786c7eead4015a4b0b2ac76493686621fab1d9aa15fa40fd569265`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a62fba798d3b46ba25a1df431d84098e426985250293108cfec350146ddfc0f`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8.4-nanoserver-1809`

```console
$ docker pull nats@sha256:9843c2cc2398441da615f9933feb523a1f638c3f3213b593f3e5e7921e1fd74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2.8.4-nanoserver-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:73e71a703e620efe92f4bdcfc0c525c8c472f4bb82d4ab6a57a8e560cf79b5fb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107773608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effb063d7055b399920066dd934fcbc50ff93b5460629fdcf20c7a4ff27ca62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:26:00 GMT
RUN cmd /S /C #(nop) COPY file:88c957e774978b3592c1072a38fbf2d578a30b42e89604bf16828cccd9f86b17 in C:\nats-server.exe 
# Fri, 27 May 2022 00:26:01 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:26:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23039a0ccbad6fe276c7cbdbe79f9f030b86f2178198f439eeed20e1ff64877b`  
		Last Modified: Fri, 27 May 2022 01:15:17 GMT  
		Size: 4.6 MB (4633261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59573cd0506705779a3d37bf4d344d3589369ce3279557bd5bda46df763cf5b`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efde216ebb9b658047beb227fed499b9c7596c5e58f2401bfb16e16b24114701`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909550900786c7eead4015a4b0b2ac76493686621fab1d9aa15fa40fd569265`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a62fba798d3b46ba25a1df431d84098e426985250293108cfec350146ddfc0f`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8.4-scratch`

```console
$ docker pull nats@sha256:6e96b99197f9d66e34df638ca22426d21963c643bfd0c987b45f1aecb814bc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.8.4-scratch` - linux; amd64

```console
$ docker pull nats@sha256:796298f636925dedbbdfa537f42423dffd3a69b70c3a9bf4fd0982886a4b745d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842c053e15bdb38e697668b1f0721313203f7c2297eb6d79000f20858dc97854`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:38:26 GMT
COPY file:c866dea678e8cec7cbd0798a1dbdefc45e992d9df374709f6000bac517589a1b in /nats-server 
# Fri, 27 May 2022 00:38:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:38:27 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:38:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:38:27 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:38:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e5797f39fa0527a3dd0a137353b40f97c71134e7eb38373d9791c5f1392885b`  
		Last Modified: Fri, 27 May 2022 00:39:15 GMT  
		Size: 4.6 MB (4591087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3b732adf61929b0b23ca08934cd89923e9cd9d7061544e76bbce57a9fa1e4`  
		Last Modified: Fri, 27 May 2022 00:39:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8.4-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7df9a2712c9b7e57f228a270f9fdfaf95f8662890dd90719ab08952fe93cc99d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86f50672b8fb25a83d599295659904a27d366e8cad89089ddb9171c79e31c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:56:05 GMT
COPY file:8de8b0cf8e6edf54e413c112cd66aed537abed387a26ba749a9293d43cdf6594 in /nats-server 
# Thu, 26 May 2022 23:56:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:56:05 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:56:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:56:06 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:56:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:770fa9c168613edbe7aa7007d2cf8492c6570efc1ddab217fa32772c6b72dd48`  
		Last Modified: Thu, 26 May 2022 23:58:21 GMT  
		Size: 4.2 MB (4245317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d80ba54887e3752f04df58e1ab68c9805dc2aee54c543d487d8d51a2c88afc1`  
		Last Modified: Thu, 26 May 2022 23:58:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8.4-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:208577394199773ff99d68d668bf4830314a173d7de8407e2bc5666b1d6d4a34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96128257f8f2facb4a2f726619b86453544d9108ec209c3665ec78c2dd14acf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2841d6664b8897473f39b595b9aa4b28e749f587dc1afa4a0027ae507f37ee1f in /nats-server 
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:25:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:25:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:25:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f533e6e439ee51f1cf94458f821a20ed162b542d356340957091882ad881d5c1`  
		Last Modified: Fri, 27 May 2022 00:28:16 GMT  
		Size: 4.2 MB (4242287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1306305db51c19253939f28312d2e4a694eab31b920aeef7d9a4d0a0b76f045`  
		Last Modified: Fri, 27 May 2022 00:28:13 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8.4-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:87b1afbd78a75ee48cb6b37a8522bbb01f5e9b5047b095b16cc4f241774a48d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bce5ae01237736c7e0447d8cd1b2dbe252eab3ab5ac3b05d98b646b2575cee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:53:56 GMT
COPY file:2dbd94c6c11f89ceba3241f1efe469d0a06f0aae91abb77f3d79756676d0be57 in /nats-server 
# Thu, 26 May 2022 23:53:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:53:57 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:53:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:54:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c74770da2ea808362085edd6dead652091b3e3d34c1e32c50015a6a5bb36c02`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 4.2 MB (4227378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988af7458b707048622e497d5ae818b77d3a24ed0295a7897ced8f003179f7f9`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8.4-windowsservercore`

```console
$ docker pull nats@sha256:21e6b0cbe3d42465b9005d70c7795eeaf812457704fed30ce2ff785c6378a14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2.8.4-windowsservercore` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:611c3122e7feffc2768797eac1184a3ffc57c69ed7f023bf7066607f0b006177
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2509547985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16ab36597c6cc5b853a849d91bff282fe7575d89c8d72bacf35977f112ddff2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:23:15 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:23:16 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.4/nats-server-v2.8.4-windows-amd64.zip
# Fri, 27 May 2022 00:23:17 GMT
ENV NATS_SERVER_SHASUM=911e8b77cf288c6e0997891d1400e5cc59dedd928e8f1685650c468674b52dc8
# Fri, 27 May 2022 00:24:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 27 May 2022 00:25:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 27 May 2022 00:25:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:25:40 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e46883112793fbc3f4ba503e0c3adda871fe219fa4792e791c1b0131ec4b76a`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270932ccc85285da4c78794de461bdbf36ec177518c5c609edf7332a3c0e9903`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a573a05b073e99843fb03188f4140e47a95892936eee597e6612b68dea7a276a`  
		Last Modified: Fri, 27 May 2022 01:14:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceeeeb1511ea57b0f10413c14390340603ed50966f7f91aad559fcc32284a027`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 497.4 KB (497353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee183f3745d31b3ab9904f03c5506b37bda08b06abc88817563f753d699c4aba`  
		Last Modified: Fri, 27 May 2022 01:14:55 GMT  
		Size: 5.0 MB (4981575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e67025d9a010ea39c79da6be0497e87fda67f62551adc4d81a0e83f06ee4527`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea59effc695238f40330bf321e135d548663a258eb2de36e3cbd0ecc2eb4f0e`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e27ce3724613991b447f6c75de82694a6e3df3a5e6b2f6cb4044f7aa89f3ca`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08833d90efc546bc030a1d2c6f4b15d21da31004d9c19858e051a00407eecc56`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8.4-windowsservercore-1809`

```console
$ docker pull nats@sha256:21e6b0cbe3d42465b9005d70c7795eeaf812457704fed30ce2ff785c6378a14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2.8.4-windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:611c3122e7feffc2768797eac1184a3ffc57c69ed7f023bf7066607f0b006177
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2509547985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16ab36597c6cc5b853a849d91bff282fe7575d89c8d72bacf35977f112ddff2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:23:15 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:23:16 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.4/nats-server-v2.8.4-windows-amd64.zip
# Fri, 27 May 2022 00:23:17 GMT
ENV NATS_SERVER_SHASUM=911e8b77cf288c6e0997891d1400e5cc59dedd928e8f1685650c468674b52dc8
# Fri, 27 May 2022 00:24:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 27 May 2022 00:25:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 27 May 2022 00:25:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:25:40 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e46883112793fbc3f4ba503e0c3adda871fe219fa4792e791c1b0131ec4b76a`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270932ccc85285da4c78794de461bdbf36ec177518c5c609edf7332a3c0e9903`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a573a05b073e99843fb03188f4140e47a95892936eee597e6612b68dea7a276a`  
		Last Modified: Fri, 27 May 2022 01:14:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceeeeb1511ea57b0f10413c14390340603ed50966f7f91aad559fcc32284a027`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 497.4 KB (497353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee183f3745d31b3ab9904f03c5506b37bda08b06abc88817563f753d699c4aba`  
		Last Modified: Fri, 27 May 2022 01:14:55 GMT  
		Size: 5.0 MB (4981575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e67025d9a010ea39c79da6be0497e87fda67f62551adc4d81a0e83f06ee4527`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea59effc695238f40330bf321e135d548663a258eb2de36e3cbd0ecc2eb4f0e`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e27ce3724613991b447f6c75de82694a6e3df3a5e6b2f6cb4044f7aa89f3ca`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08833d90efc546bc030a1d2c6f4b15d21da31004d9c19858e051a00407eecc56`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:24d2a7b7394e612109c861692f83d5ac3bb5d44e61d07002b333335564e0c76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:4199deae36b30cf612a8a5ac96614e60dba809dd72d73a5d3534faa521a12261
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48fd9739aa3f72822ff0234951c748e1933512aff2aa6631c4cf8e4f9b6692c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:37:50 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:37:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 May 2022 00:37:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 May 2022 00:37:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 May 2022 00:37:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 May 2022 00:37:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415d0ea53c276a355c1209aed0a7e21521ddf40ad8a8e0ec3d72d8593a2ba455`  
		Last Modified: Fri, 27 May 2022 00:38:52 GMT  
		Size: 4.9 MB (4864532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05146d3cba39de864032f28506c4921cd565c57aeb729108ac8d0b11c3276bbc`  
		Last Modified: Fri, 27 May 2022 00:38:51 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc9a9ede479a70c4e0d44d902e64c19eca0cd12baf3624ecf0e77d74fde28ef`  
		Last Modified: Fri, 27 May 2022 00:38:51 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:8b48b81efe06e10f92980ce446aa199c35e591e6e61f6a508e8e5b83b993c75c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7141581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fcaa7e9654b63fb8642995444c1d4e0c884d6bfc2a16fdb8a7a39e137b5208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 23:55:37 GMT
ENV NATS_SERVER=2.8.4
# Thu, 26 May 2022 23:55:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 26 May 2022 23:55:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 26 May 2022 23:55:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 26 May 2022 23:55:43 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:55:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 May 2022 23:55:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50f68c47a108ab599d7f0e191ffaf378e6dce6a928151e691d8ea726aeb928`  
		Last Modified: Thu, 26 May 2022 23:57:46 GMT  
		Size: 4.5 MB (4518611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4cb9d5e8d247c55e5f7e46c8d54ea485f55806c24444feaf62725d6ba170f1`  
		Last Modified: Thu, 26 May 2022 23:57:43 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c6a3cdd4a881f42229288ebba9a675d7abe171cd2b2838becae58d1aad6ab`  
		Last Modified: Thu, 26 May 2022 23:57:43 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ba8d5358e4179eedb8812098fe9aafac97d3cbc262c5c661e8f7a0c91a5bbcb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6939129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eca0f2ec4b22a18d9e30a03a72c0b72555d4cdbcbcb8ff15552cc1d01442c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:25:21 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:25:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 May 2022 00:25:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 May 2022 00:25:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 May 2022 00:25:26 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 May 2022 00:25:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f90a00ed33ea115d275ac961047e5009b1e24e2103dbfaed2ab8f52856c975`  
		Last Modified: Fri, 27 May 2022 00:27:40 GMT  
		Size: 4.5 MB (4513806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd41cd9dfa9b3a42fea8a47e1a69c57faa29f3cdd27489fc7f4fe699d283f899`  
		Last Modified: Fri, 27 May 2022 00:27:37 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed506c19493a71093e162dbcebe70d57fc6c372d9c201a32ef0515b66da395b7`  
		Last Modified: Fri, 27 May 2022 00:27:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:068170580c70c9c06e2050fa9c6f66ec28f61c9062663cf2b45db2eed7e6b3d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7218027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fa83e475ee42455e6e7021633d7a98bb6496a5a75621f389dff13b1ceaa343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 23:53:38 GMT
ENV NATS_SERVER=2.8.4
# Thu, 26 May 2022 23:53:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 26 May 2022 23:53:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 26 May 2022 23:53:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 26 May 2022 23:53:43 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 May 2022 23:53:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48649cc80ad9a6544bde7c572f66e6a5f2c0e918923a957045cfea77bbf31bb`  
		Last Modified: Thu, 26 May 2022 23:54:50 GMT  
		Size: 4.5 MB (4500578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bbb498a8d1c04c80271b66119f843bc9a68cf260f1fc0005babdb8ef1820b8`  
		Last Modified: Thu, 26 May 2022 23:54:49 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ca2313cb9b3e722a83aa9f01456f583d124cbb90aa75908b33a0c37ecdaeb`  
		Last Modified: Thu, 26 May 2022 23:54:49 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.15`

```console
$ docker pull nats@sha256:24d2a7b7394e612109c861692f83d5ac3bb5d44e61d07002b333335564e0c76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:4199deae36b30cf612a8a5ac96614e60dba809dd72d73a5d3534faa521a12261
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48fd9739aa3f72822ff0234951c748e1933512aff2aa6631c4cf8e4f9b6692c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:37:50 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:37:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 May 2022 00:37:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 May 2022 00:37:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 May 2022 00:37:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 May 2022 00:37:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415d0ea53c276a355c1209aed0a7e21521ddf40ad8a8e0ec3d72d8593a2ba455`  
		Last Modified: Fri, 27 May 2022 00:38:52 GMT  
		Size: 4.9 MB (4864532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05146d3cba39de864032f28506c4921cd565c57aeb729108ac8d0b11c3276bbc`  
		Last Modified: Fri, 27 May 2022 00:38:51 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc9a9ede479a70c4e0d44d902e64c19eca0cd12baf3624ecf0e77d74fde28ef`  
		Last Modified: Fri, 27 May 2022 00:38:51 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:8b48b81efe06e10f92980ce446aa199c35e591e6e61f6a508e8e5b83b993c75c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7141581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fcaa7e9654b63fb8642995444c1d4e0c884d6bfc2a16fdb8a7a39e137b5208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 23:55:37 GMT
ENV NATS_SERVER=2.8.4
# Thu, 26 May 2022 23:55:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 26 May 2022 23:55:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 26 May 2022 23:55:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 26 May 2022 23:55:43 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:55:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 May 2022 23:55:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50f68c47a108ab599d7f0e191ffaf378e6dce6a928151e691d8ea726aeb928`  
		Last Modified: Thu, 26 May 2022 23:57:46 GMT  
		Size: 4.5 MB (4518611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4cb9d5e8d247c55e5f7e46c8d54ea485f55806c24444feaf62725d6ba170f1`  
		Last Modified: Thu, 26 May 2022 23:57:43 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c6a3cdd4a881f42229288ebba9a675d7abe171cd2b2838becae58d1aad6ab`  
		Last Modified: Thu, 26 May 2022 23:57:43 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ba8d5358e4179eedb8812098fe9aafac97d3cbc262c5c661e8f7a0c91a5bbcb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6939129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eca0f2ec4b22a18d9e30a03a72c0b72555d4cdbcbcb8ff15552cc1d01442c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:25:21 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:25:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 May 2022 00:25:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 May 2022 00:25:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 May 2022 00:25:26 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 May 2022 00:25:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f90a00ed33ea115d275ac961047e5009b1e24e2103dbfaed2ab8f52856c975`  
		Last Modified: Fri, 27 May 2022 00:27:40 GMT  
		Size: 4.5 MB (4513806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd41cd9dfa9b3a42fea8a47e1a69c57faa29f3cdd27489fc7f4fe699d283f899`  
		Last Modified: Fri, 27 May 2022 00:27:37 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed506c19493a71093e162dbcebe70d57fc6c372d9c201a32ef0515b66da395b7`  
		Last Modified: Fri, 27 May 2022 00:27:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:068170580c70c9c06e2050fa9c6f66ec28f61c9062663cf2b45db2eed7e6b3d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7218027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fa83e475ee42455e6e7021633d7a98bb6496a5a75621f389dff13b1ceaa343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 23:53:38 GMT
ENV NATS_SERVER=2.8.4
# Thu, 26 May 2022 23:53:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 26 May 2022 23:53:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 26 May 2022 23:53:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 26 May 2022 23:53:43 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 May 2022 23:53:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48649cc80ad9a6544bde7c572f66e6a5f2c0e918923a957045cfea77bbf31bb`  
		Last Modified: Thu, 26 May 2022 23:54:50 GMT  
		Size: 4.5 MB (4500578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bbb498a8d1c04c80271b66119f843bc9a68cf260f1fc0005babdb8ef1820b8`  
		Last Modified: Thu, 26 May 2022 23:54:49 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ca2313cb9b3e722a83aa9f01456f583d124cbb90aa75908b33a0c37ecdaeb`  
		Last Modified: Thu, 26 May 2022 23:54:49 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:9686d73262f91e44c10b838eecbab53e705d2f4be5718efe92dfdf9f86f4e786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2928; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:796298f636925dedbbdfa537f42423dffd3a69b70c3a9bf4fd0982886a4b745d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842c053e15bdb38e697668b1f0721313203f7c2297eb6d79000f20858dc97854`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:38:26 GMT
COPY file:c866dea678e8cec7cbd0798a1dbdefc45e992d9df374709f6000bac517589a1b in /nats-server 
# Fri, 27 May 2022 00:38:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:38:27 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:38:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:38:27 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:38:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e5797f39fa0527a3dd0a137353b40f97c71134e7eb38373d9791c5f1392885b`  
		Last Modified: Fri, 27 May 2022 00:39:15 GMT  
		Size: 4.6 MB (4591087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3b732adf61929b0b23ca08934cd89923e9cd9d7061544e76bbce57a9fa1e4`  
		Last Modified: Fri, 27 May 2022 00:39:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:7df9a2712c9b7e57f228a270f9fdfaf95f8662890dd90719ab08952fe93cc99d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86f50672b8fb25a83d599295659904a27d366e8cad89089ddb9171c79e31c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:56:05 GMT
COPY file:8de8b0cf8e6edf54e413c112cd66aed537abed387a26ba749a9293d43cdf6594 in /nats-server 
# Thu, 26 May 2022 23:56:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:56:05 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:56:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:56:06 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:56:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:770fa9c168613edbe7aa7007d2cf8492c6570efc1ddab217fa32772c6b72dd48`  
		Last Modified: Thu, 26 May 2022 23:58:21 GMT  
		Size: 4.2 MB (4245317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d80ba54887e3752f04df58e1ab68c9805dc2aee54c543d487d8d51a2c88afc1`  
		Last Modified: Thu, 26 May 2022 23:58:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:208577394199773ff99d68d668bf4830314a173d7de8407e2bc5666b1d6d4a34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96128257f8f2facb4a2f726619b86453544d9108ec209c3665ec78c2dd14acf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2841d6664b8897473f39b595b9aa4b28e749f587dc1afa4a0027ae507f37ee1f in /nats-server 
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:25:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:25:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:25:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f533e6e439ee51f1cf94458f821a20ed162b542d356340957091882ad881d5c1`  
		Last Modified: Fri, 27 May 2022 00:28:16 GMT  
		Size: 4.2 MB (4242287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1306305db51c19253939f28312d2e4a694eab31b920aeef7d9a4d0a0b76f045`  
		Last Modified: Fri, 27 May 2022 00:28:13 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:87b1afbd78a75ee48cb6b37a8522bbb01f5e9b5047b095b16cc4f241774a48d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bce5ae01237736c7e0447d8cd1b2dbe252eab3ab5ac3b05d98b646b2575cee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:53:56 GMT
COPY file:2dbd94c6c11f89ceba3241f1efe469d0a06f0aae91abb77f3d79756676d0be57 in /nats-server 
# Thu, 26 May 2022 23:53:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:53:57 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:53:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:54:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c74770da2ea808362085edd6dead652091b3e3d34c1e32c50015a6a5bb36c02`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 4.2 MB (4227378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988af7458b707048622e497d5ae818b77d3a24ed0295a7897ced8f003179f7f9`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:73e71a703e620efe92f4bdcfc0c525c8c472f4bb82d4ab6a57a8e560cf79b5fb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107773608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effb063d7055b399920066dd934fcbc50ff93b5460629fdcf20c7a4ff27ca62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:26:00 GMT
RUN cmd /S /C #(nop) COPY file:88c957e774978b3592c1072a38fbf2d578a30b42e89604bf16828cccd9f86b17 in C:\nats-server.exe 
# Fri, 27 May 2022 00:26:01 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:26:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23039a0ccbad6fe276c7cbdbe79f9f030b86f2178198f439eeed20e1ff64877b`  
		Last Modified: Fri, 27 May 2022 01:15:17 GMT  
		Size: 4.6 MB (4633261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59573cd0506705779a3d37bf4d344d3589369ce3279557bd5bda46df763cf5b`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efde216ebb9b658047beb227fed499b9c7596c5e58f2401bfb16e16b24114701`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909550900786c7eead4015a4b0b2ac76493686621fab1d9aa15fa40fd569265`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a62fba798d3b46ba25a1df431d84098e426985250293108cfec350146ddfc0f`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:6e96b99197f9d66e34df638ca22426d21963c643bfd0c987b45f1aecb814bc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:796298f636925dedbbdfa537f42423dffd3a69b70c3a9bf4fd0982886a4b745d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842c053e15bdb38e697668b1f0721313203f7c2297eb6d79000f20858dc97854`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:38:26 GMT
COPY file:c866dea678e8cec7cbd0798a1dbdefc45e992d9df374709f6000bac517589a1b in /nats-server 
# Fri, 27 May 2022 00:38:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:38:27 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:38:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:38:27 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:38:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e5797f39fa0527a3dd0a137353b40f97c71134e7eb38373d9791c5f1392885b`  
		Last Modified: Fri, 27 May 2022 00:39:15 GMT  
		Size: 4.6 MB (4591087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3b732adf61929b0b23ca08934cd89923e9cd9d7061544e76bbce57a9fa1e4`  
		Last Modified: Fri, 27 May 2022 00:39:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7df9a2712c9b7e57f228a270f9fdfaf95f8662890dd90719ab08952fe93cc99d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86f50672b8fb25a83d599295659904a27d366e8cad89089ddb9171c79e31c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:56:05 GMT
COPY file:8de8b0cf8e6edf54e413c112cd66aed537abed387a26ba749a9293d43cdf6594 in /nats-server 
# Thu, 26 May 2022 23:56:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:56:05 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:56:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:56:06 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:56:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:770fa9c168613edbe7aa7007d2cf8492c6570efc1ddab217fa32772c6b72dd48`  
		Last Modified: Thu, 26 May 2022 23:58:21 GMT  
		Size: 4.2 MB (4245317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d80ba54887e3752f04df58e1ab68c9805dc2aee54c543d487d8d51a2c88afc1`  
		Last Modified: Thu, 26 May 2022 23:58:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:208577394199773ff99d68d668bf4830314a173d7de8407e2bc5666b1d6d4a34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96128257f8f2facb4a2f726619b86453544d9108ec209c3665ec78c2dd14acf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2841d6664b8897473f39b595b9aa4b28e749f587dc1afa4a0027ae507f37ee1f in /nats-server 
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:25:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:25:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:25:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f533e6e439ee51f1cf94458f821a20ed162b542d356340957091882ad881d5c1`  
		Last Modified: Fri, 27 May 2022 00:28:16 GMT  
		Size: 4.2 MB (4242287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1306305db51c19253939f28312d2e4a694eab31b920aeef7d9a4d0a0b76f045`  
		Last Modified: Fri, 27 May 2022 00:28:13 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:87b1afbd78a75ee48cb6b37a8522bbb01f5e9b5047b095b16cc4f241774a48d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bce5ae01237736c7e0447d8cd1b2dbe252eab3ab5ac3b05d98b646b2575cee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:53:56 GMT
COPY file:2dbd94c6c11f89ceba3241f1efe469d0a06f0aae91abb77f3d79756676d0be57 in /nats-server 
# Thu, 26 May 2022 23:53:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:53:57 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:53:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:54:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c74770da2ea808362085edd6dead652091b3e3d34c1e32c50015a6a5bb36c02`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 4.2 MB (4227378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988af7458b707048622e497d5ae818b77d3a24ed0295a7897ced8f003179f7f9`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:9843c2cc2398441da615f9933feb523a1f638c3f3213b593f3e5e7921e1fd74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:nanoserver` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:73e71a703e620efe92f4bdcfc0c525c8c472f4bb82d4ab6a57a8e560cf79b5fb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107773608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effb063d7055b399920066dd934fcbc50ff93b5460629fdcf20c7a4ff27ca62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:26:00 GMT
RUN cmd /S /C #(nop) COPY file:88c957e774978b3592c1072a38fbf2d578a30b42e89604bf16828cccd9f86b17 in C:\nats-server.exe 
# Fri, 27 May 2022 00:26:01 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:26:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23039a0ccbad6fe276c7cbdbe79f9f030b86f2178198f439eeed20e1ff64877b`  
		Last Modified: Fri, 27 May 2022 01:15:17 GMT  
		Size: 4.6 MB (4633261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59573cd0506705779a3d37bf4d344d3589369ce3279557bd5bda46df763cf5b`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efde216ebb9b658047beb227fed499b9c7596c5e58f2401bfb16e16b24114701`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909550900786c7eead4015a4b0b2ac76493686621fab1d9aa15fa40fd569265`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a62fba798d3b46ba25a1df431d84098e426985250293108cfec350146ddfc0f`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:9843c2cc2398441da615f9933feb523a1f638c3f3213b593f3e5e7921e1fd74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:73e71a703e620efe92f4bdcfc0c525c8c472f4bb82d4ab6a57a8e560cf79b5fb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107773608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effb063d7055b399920066dd934fcbc50ff93b5460629fdcf20c7a4ff27ca62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:26:00 GMT
RUN cmd /S /C #(nop) COPY file:88c957e774978b3592c1072a38fbf2d578a30b42e89604bf16828cccd9f86b17 in C:\nats-server.exe 
# Fri, 27 May 2022 00:26:01 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:26:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23039a0ccbad6fe276c7cbdbe79f9f030b86f2178198f439eeed20e1ff64877b`  
		Last Modified: Fri, 27 May 2022 01:15:17 GMT  
		Size: 4.6 MB (4633261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59573cd0506705779a3d37bf4d344d3589369ce3279557bd5bda46df763cf5b`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efde216ebb9b658047beb227fed499b9c7596c5e58f2401bfb16e16b24114701`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909550900786c7eead4015a4b0b2ac76493686621fab1d9aa15fa40fd569265`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a62fba798d3b46ba25a1df431d84098e426985250293108cfec350146ddfc0f`  
		Last Modified: Fri, 27 May 2022 01:15:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:6e96b99197f9d66e34df638ca22426d21963c643bfd0c987b45f1aecb814bc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:796298f636925dedbbdfa537f42423dffd3a69b70c3a9bf4fd0982886a4b745d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842c053e15bdb38e697668b1f0721313203f7c2297eb6d79000f20858dc97854`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:38:26 GMT
COPY file:c866dea678e8cec7cbd0798a1dbdefc45e992d9df374709f6000bac517589a1b in /nats-server 
# Fri, 27 May 2022 00:38:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:38:27 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:38:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:38:27 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:38:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e5797f39fa0527a3dd0a137353b40f97c71134e7eb38373d9791c5f1392885b`  
		Last Modified: Fri, 27 May 2022 00:39:15 GMT  
		Size: 4.6 MB (4591087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3b732adf61929b0b23ca08934cd89923e9cd9d7061544e76bbce57a9fa1e4`  
		Last Modified: Fri, 27 May 2022 00:39:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7df9a2712c9b7e57f228a270f9fdfaf95f8662890dd90719ab08952fe93cc99d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86f50672b8fb25a83d599295659904a27d366e8cad89089ddb9171c79e31c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:56:05 GMT
COPY file:8de8b0cf8e6edf54e413c112cd66aed537abed387a26ba749a9293d43cdf6594 in /nats-server 
# Thu, 26 May 2022 23:56:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:56:05 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:56:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:56:06 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:56:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:770fa9c168613edbe7aa7007d2cf8492c6570efc1ddab217fa32772c6b72dd48`  
		Last Modified: Thu, 26 May 2022 23:58:21 GMT  
		Size: 4.2 MB (4245317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d80ba54887e3752f04df58e1ab68c9805dc2aee54c543d487d8d51a2c88afc1`  
		Last Modified: Thu, 26 May 2022 23:58:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:208577394199773ff99d68d668bf4830314a173d7de8407e2bc5666b1d6d4a34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96128257f8f2facb4a2f726619b86453544d9108ec209c3665ec78c2dd14acf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2841d6664b8897473f39b595b9aa4b28e749f587dc1afa4a0027ae507f37ee1f in /nats-server 
# Fri, 27 May 2022 00:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 May 2022 00:25:52 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 May 2022 00:25:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 May 2022 00:25:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f533e6e439ee51f1cf94458f821a20ed162b542d356340957091882ad881d5c1`  
		Last Modified: Fri, 27 May 2022 00:28:16 GMT  
		Size: 4.2 MB (4242287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1306305db51c19253939f28312d2e4a694eab31b920aeef7d9a4d0a0b76f045`  
		Last Modified: Fri, 27 May 2022 00:28:13 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:87b1afbd78a75ee48cb6b37a8522bbb01f5e9b5047b095b16cc4f241774a48d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bce5ae01237736c7e0447d8cd1b2dbe252eab3ab5ac3b05d98b646b2575cee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:53:56 GMT
COPY file:2dbd94c6c11f89ceba3241f1efe469d0a06f0aae91abb77f3d79756676d0be57 in /nats-server 
# Thu, 26 May 2022 23:53:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:53:57 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:53:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:54:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c74770da2ea808362085edd6dead652091b3e3d34c1e32c50015a6a5bb36c02`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 4.2 MB (4227378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988af7458b707048622e497d5ae818b77d3a24ed0295a7897ced8f003179f7f9`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:21e6b0cbe3d42465b9005d70c7795eeaf812457704fed30ce2ff785c6378a14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:windowsservercore` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:611c3122e7feffc2768797eac1184a3ffc57c69ed7f023bf7066607f0b006177
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2509547985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16ab36597c6cc5b853a849d91bff282fe7575d89c8d72bacf35977f112ddff2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:23:15 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:23:16 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.4/nats-server-v2.8.4-windows-amd64.zip
# Fri, 27 May 2022 00:23:17 GMT
ENV NATS_SERVER_SHASUM=911e8b77cf288c6e0997891d1400e5cc59dedd928e8f1685650c468674b52dc8
# Fri, 27 May 2022 00:24:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 27 May 2022 00:25:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 27 May 2022 00:25:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:25:40 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e46883112793fbc3f4ba503e0c3adda871fe219fa4792e791c1b0131ec4b76a`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270932ccc85285da4c78794de461bdbf36ec177518c5c609edf7332a3c0e9903`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a573a05b073e99843fb03188f4140e47a95892936eee597e6612b68dea7a276a`  
		Last Modified: Fri, 27 May 2022 01:14:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceeeeb1511ea57b0f10413c14390340603ed50966f7f91aad559fcc32284a027`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 497.4 KB (497353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee183f3745d31b3ab9904f03c5506b37bda08b06abc88817563f753d699c4aba`  
		Last Modified: Fri, 27 May 2022 01:14:55 GMT  
		Size: 5.0 MB (4981575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e67025d9a010ea39c79da6be0497e87fda67f62551adc4d81a0e83f06ee4527`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea59effc695238f40330bf321e135d548663a258eb2de36e3cbd0ecc2eb4f0e`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e27ce3724613991b447f6c75de82694a6e3df3a5e6b2f6cb4044f7aa89f3ca`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08833d90efc546bc030a1d2c6f4b15d21da31004d9c19858e051a00407eecc56`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:21e6b0cbe3d42465b9005d70c7795eeaf812457704fed30ce2ff785c6378a14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:611c3122e7feffc2768797eac1184a3ffc57c69ed7f023bf7066607f0b006177
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2509547985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16ab36597c6cc5b853a849d91bff282fe7575d89c8d72bacf35977f112ddff2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Fri, 27 May 2022 00:23:15 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:23:16 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.4/nats-server-v2.8.4-windows-amd64.zip
# Fri, 27 May 2022 00:23:17 GMT
ENV NATS_SERVER_SHASUM=911e8b77cf288c6e0997891d1400e5cc59dedd928e8f1685650c468674b52dc8
# Fri, 27 May 2022 00:24:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 27 May 2022 00:25:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 27 May 2022 00:25:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:25:40 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e46883112793fbc3f4ba503e0c3adda871fe219fa4792e791c1b0131ec4b76a`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270932ccc85285da4c78794de461bdbf36ec177518c5c609edf7332a3c0e9903`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a573a05b073e99843fb03188f4140e47a95892936eee597e6612b68dea7a276a`  
		Last Modified: Fri, 27 May 2022 01:14:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceeeeb1511ea57b0f10413c14390340603ed50966f7f91aad559fcc32284a027`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 497.4 KB (497353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee183f3745d31b3ab9904f03c5506b37bda08b06abc88817563f753d699c4aba`  
		Last Modified: Fri, 27 May 2022 01:14:55 GMT  
		Size: 5.0 MB (4981575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e67025d9a010ea39c79da6be0497e87fda67f62551adc4d81a0e83f06ee4527`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea59effc695238f40330bf321e135d548663a258eb2de36e3cbd0ecc2eb4f0e`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e27ce3724613991b447f6c75de82694a6e3df3a5e6b2f6cb4044f7aa89f3ca`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08833d90efc546bc030a1d2c6f4b15d21da31004d9c19858e051a00407eecc56`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

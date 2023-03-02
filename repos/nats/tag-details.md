<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.17`](#nats2-alpine317)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.9`](#nats29)
-	[`nats:2.9-alpine`](#nats29-alpine)
-	[`nats:2.9-alpine3.17`](#nats29-alpine317)
-	[`nats:2.9-linux`](#nats29-linux)
-	[`nats:2.9-nanoserver`](#nats29-nanoserver)
-	[`nats:2.9-nanoserver-1809`](#nats29-nanoserver-1809)
-	[`nats:2.9-scratch`](#nats29-scratch)
-	[`nats:2.9-windowsservercore`](#nats29-windowsservercore)
-	[`nats:2.9-windowsservercore-1809`](#nats29-windowsservercore-1809)
-	[`nats:2.9.15`](#nats2915)
-	[`nats:2.9.15-alpine`](#nats2915-alpine)
-	[`nats:2.9.15-alpine3.17`](#nats2915-alpine317)
-	[`nats:2.9.15-linux`](#nats2915-linux)
-	[`nats:2.9.15-nanoserver`](#nats2915-nanoserver)
-	[`nats:2.9.15-nanoserver-1809`](#nats2915-nanoserver-1809)
-	[`nats:2.9.15-scratch`](#nats2915-scratch)
-	[`nats:2.9.15-windowsservercore`](#nats2915-windowsservercore)
-	[`nats:2.9.15-windowsservercore-1809`](#nats2915-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.17`](#natsalpine317)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:04fcc71e7d416348e8761b4081931d735d3774f5b14d33b724cc6caad6037893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4010; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:1a82b1b261d169994fc6162f2f25894a49e20971560f8b2dff4f90eefb32b421
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74665a2673c052e85d3417cec864d1aabab3263f3328051037a133d9b85765ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:32a9f093b76345e99bd81ff00eabc5ab1ae6c2bdc7d6c843c923049ea3c620ce in /nats-server 
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 19:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:20:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 19:20:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 19:20:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:436f213323b997ad7aca1675cce2c9a9366e3cd51995b9829835ab9762901f98`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (4972530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb98c93488e5f33bab9a8b331c5fbe988a9dd644e39cc15e6626550ec05e541`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e1ba487c56a25895759177de201768f40c51ceeedca983afa03875039445bb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60b5d45617b9109e120de34ac32b0647324dba3d69d2c56366545e50c2484c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:614e1182091dacdaa5043752e8239600bae8aa334cfd383cc326d1753d3eba64 in /nats-server 
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:49:36 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d859c106d4072b51eee7be282394c7f0c288186311ae904751cd95c3cf9468ae`  
		Last Modified: Thu, 02 Mar 2023 18:50:54 GMT  
		Size: 4.7 MB (4739343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e7000b41bf11d721897d126c1e72201203bcc8e9716daad77d7d42ae97853a`  
		Last Modified: Thu, 02 Mar 2023 18:50:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:644eac35d964521bc85286defaf1bae093b36618fe862eedff9a996e330fc60c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4731109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e814afeda8d92b2fb3dcdacf4648234504c6e4cd7fc24cce256cc588a439d7e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:a63786ae76c5e718a4952dd30b2265019e1ca48099ad19279d2e77e5ad704bfc in /nats-server 
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:57:50 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:57:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:57:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e714c80855fb90cb44f135a04bf323493a749536bb9106eb3ef4e69a70682897`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 4.7 MB (4730600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e020ba411c44ee7d23b6bdbd966700955c2d087afd3d79a9ad51e0390e8e7b6`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:35ef84ac5e9bb0d0229fb1a773677d6ee7b23bb58937427d20aaa36987562373
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4559479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f367536d7ef4331c52bf405914c6f7affdccdb8eed05fb4c981efe519fd06f00`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:23081283f9b4d8145ad2b3a276cc08fcb49c4850e322db9560525e495d1bf362 in /nats-server 
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:40:16 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:40:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:40:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:40:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a910efaa632bb8401dbca7cfe541f6dc4da71ea38708992ef153250254493114`  
		Last Modified: Thu, 02 Mar 2023 18:41:09 GMT  
		Size: 4.6 MB (4558972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be7fc9abf13897cf1a5e7026f6a49b3308d5a864640e1f4b6e526ee95f093fc`  
		Last Modified: Thu, 02 Mar 2023 18:41:08 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:43348610453f5ecf2cb1eb6b88a459f7ad59353df14950ea55d72a27737f66af
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111708291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94392dbb17d455d1e80a3bc24798e3e1d761cbcd472f1616a352d0995335dbf0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Feb 2023 10:14:28 GMT
RUN Apply image 10.0.17763.4010
# Thu, 16 Feb 2023 02:07:44 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:19:54 GMT
RUN cmd /S /C #(nop) COPY file:c0761502e8e3e74fa63209f49b4d4f61a9c596c726f61d96e045d0b22538ada5 in C:\nats-server.exe 
# Thu, 02 Mar 2023 19:19:55 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:00eaf3341cd3cc6b72f91399cb3bd1aba30eb7eead7596532fe54c4bf1b010d7`  
		Last Modified: Thu, 16 Feb 2023 00:31:21 GMT  
		Size: 106.7 MB (106674970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce19f72ba3efadcebf91b9628f9e85de500fcaa86b6ec8076169cc4bb312c0`  
		Last Modified: Thu, 16 Feb 2023 02:08:32 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4653b8562b98f6d770621adbd89d3392ed2c490da6c30dec79027c7e24ca6b`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (5026943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283f9c4ca607d846e0fc14dd248b106caf329d7c20316e59898b4a202459a77`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c525626770477530f07d56e4934dd0c036e55624d0182762d6df8afbc46aa99`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cda701c245116defdc445fe6ef3e38f73716d9f527f2876d1843abaef3ca11`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec7890747cf0e8bf22b460262ebe10c19f91d00c0710a010fbe2d48d81ca8f0`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:f2f2b0e23c7f9fd142e4882d4f4c1cc9c3a6efb17d23b8b16c837d79ff59ca84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:9947eac2dedc476378d9cac73c7df6cba2f1a23da12137214cdc254a15863a46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8635785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d6b3fd56dc8fe20a6e41de4afeacff348a53e1ab388f535f404e9cf74c084d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 19:19:49 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 19:19:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 19:19:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 19:19:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 19:19:52 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:19:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08472afe1eaab0ac7a92349d2da3b64cafacc125426338b278e2fc3b006bd52`  
		Last Modified: Thu, 02 Mar 2023 19:20:25 GMT  
		Size: 5.3 MB (5260338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5ae32cc4383cc8cabea2eba8667d1ff1aaa9bf699469141395387df31c5c4b`  
		Last Modified: Thu, 02 Mar 2023 19:20:24 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3f805284c458c477cde0410e2f6835ab92c5fd6b464cfd6c07cf3d52643c23`  
		Last Modified: Thu, 02 Mar 2023 19:20:24 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d7d52fa58f1f77d24ded7e34e2be977eb4474da0ae5e81639e144de15e0c9bf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8135732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4abf0b19eb2e841ac4255d1702b59ec4fb05a30e60561a5cfd8efcd2c8e4b24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:49:28 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:49:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:49:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:49:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:49:31 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:49:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2d8c7c008839e4297490fe62726b0511bb9a7c6486b7f97b106788aa11c6f8`  
		Last Modified: Thu, 02 Mar 2023 18:50:25 GMT  
		Size: 5.0 MB (5023847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8437de52ce6ce410d6359afa18a00cc025d2f5846e854d4b4e398f9eb16ce1c5`  
		Last Modified: Thu, 02 Mar 2023 18:50:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98d271690d33766c10fca8cfd7d844162956eb2db3195e9bf3e21ed587c7f60`  
		Last Modified: Thu, 02 Mar 2023 18:50:24 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d0f535bd276e1b92c60c9b8fe33cb90d439049071159843142c026302b54bf7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7887576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b405c7e2612cb810f225540c61a3eb1f02c1efbb3910aa30aa7b46b068fef2db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:31 GMT
ADD file:143b601fcc6b5d7d95d3e5ccad3fec7081191a47e28d4f9294a7fb2499cab1af in / 
# Fri, 10 Feb 2023 21:51:31 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:57:36 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:57:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:57:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:57:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:57:39 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:57:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6fb81ff47bd6d7db0ed86c9b951ad6417ec73ab60af6d22daa604076a902629c`  
		Last Modified: Fri, 10 Feb 2023 21:52:33 GMT  
		Size: 2.9 MB (2868494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19b56339a1ba27c396a17554216f8da9ef664a78ec52c24c39630ad6b00ccea`  
		Last Modified: Thu, 02 Mar 2023 18:58:37 GMT  
		Size: 5.0 MB (5018081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6919af5eaed170352d5fcbc4a52cdfd188a277c02b8c39538f0626a12afc6e`  
		Last Modified: Thu, 02 Mar 2023 18:58:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99bb0ebd369abc6e32fcdbdbade73f2a1504cb8edae42327051d1343b982a8b`  
		Last Modified: Thu, 02 Mar 2023 18:58:36 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:31516678d6c3c1c5d7444e85d06618022258cfb3a23bbed0e44a358bbf7fea1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8104002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f18af0a035256392dde53a51a48628b107ebad3b4b6627160aaab7a964ce40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:39:45 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:39:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:39:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:39:47 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:39:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f03396fa041b5be75e5a939ff3aadaff2e65f529a07bcbd4748b581e3e193e1`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 4.8 MB (4841045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cceddcd111b1a86e5348af7dccf8c0b0d1c1dfec305c026bd9351bd0d1cce7`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca183fb542756060f50207e2bdac939b035a4f4ff2075b0371f87399242950a2`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.17`

```console
$ docker pull nats@sha256:f2f2b0e23c7f9fd142e4882d4f4c1cc9c3a6efb17d23b8b16c837d79ff59ca84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.17` - linux; amd64

```console
$ docker pull nats@sha256:9947eac2dedc476378d9cac73c7df6cba2f1a23da12137214cdc254a15863a46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8635785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d6b3fd56dc8fe20a6e41de4afeacff348a53e1ab388f535f404e9cf74c084d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 19:19:49 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 19:19:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 19:19:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 19:19:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 19:19:52 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:19:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08472afe1eaab0ac7a92349d2da3b64cafacc125426338b278e2fc3b006bd52`  
		Last Modified: Thu, 02 Mar 2023 19:20:25 GMT  
		Size: 5.3 MB (5260338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5ae32cc4383cc8cabea2eba8667d1ff1aaa9bf699469141395387df31c5c4b`  
		Last Modified: Thu, 02 Mar 2023 19:20:24 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3f805284c458c477cde0410e2f6835ab92c5fd6b464cfd6c07cf3d52643c23`  
		Last Modified: Thu, 02 Mar 2023 19:20:24 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.17` - linux; arm variant v6

```console
$ docker pull nats@sha256:d7d52fa58f1f77d24ded7e34e2be977eb4474da0ae5e81639e144de15e0c9bf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8135732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4abf0b19eb2e841ac4255d1702b59ec4fb05a30e60561a5cfd8efcd2c8e4b24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:49:28 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:49:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:49:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:49:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:49:31 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:49:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2d8c7c008839e4297490fe62726b0511bb9a7c6486b7f97b106788aa11c6f8`  
		Last Modified: Thu, 02 Mar 2023 18:50:25 GMT  
		Size: 5.0 MB (5023847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8437de52ce6ce410d6359afa18a00cc025d2f5846e854d4b4e398f9eb16ce1c5`  
		Last Modified: Thu, 02 Mar 2023 18:50:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98d271690d33766c10fca8cfd7d844162956eb2db3195e9bf3e21ed587c7f60`  
		Last Modified: Thu, 02 Mar 2023 18:50:24 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.17` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d0f535bd276e1b92c60c9b8fe33cb90d439049071159843142c026302b54bf7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7887576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b405c7e2612cb810f225540c61a3eb1f02c1efbb3910aa30aa7b46b068fef2db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:31 GMT
ADD file:143b601fcc6b5d7d95d3e5ccad3fec7081191a47e28d4f9294a7fb2499cab1af in / 
# Fri, 10 Feb 2023 21:51:31 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:57:36 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:57:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:57:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:57:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:57:39 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:57:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6fb81ff47bd6d7db0ed86c9b951ad6417ec73ab60af6d22daa604076a902629c`  
		Last Modified: Fri, 10 Feb 2023 21:52:33 GMT  
		Size: 2.9 MB (2868494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19b56339a1ba27c396a17554216f8da9ef664a78ec52c24c39630ad6b00ccea`  
		Last Modified: Thu, 02 Mar 2023 18:58:37 GMT  
		Size: 5.0 MB (5018081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6919af5eaed170352d5fcbc4a52cdfd188a277c02b8c39538f0626a12afc6e`  
		Last Modified: Thu, 02 Mar 2023 18:58:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99bb0ebd369abc6e32fcdbdbade73f2a1504cb8edae42327051d1343b982a8b`  
		Last Modified: Thu, 02 Mar 2023 18:58:36 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:31516678d6c3c1c5d7444e85d06618022258cfb3a23bbed0e44a358bbf7fea1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8104002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f18af0a035256392dde53a51a48628b107ebad3b4b6627160aaab7a964ce40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:39:45 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:39:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:39:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:39:47 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:39:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f03396fa041b5be75e5a939ff3aadaff2e65f529a07bcbd4748b581e3e193e1`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 4.8 MB (4841045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cceddcd111b1a86e5348af7dccf8c0b0d1c1dfec305c026bd9351bd0d1cce7`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca183fb542756060f50207e2bdac939b035a4f4ff2075b0371f87399242950a2`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:e9767cfa85287292db74b0533d910366598f93e18b3c60706cf1c25ab7f657be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:1a82b1b261d169994fc6162f2f25894a49e20971560f8b2dff4f90eefb32b421
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74665a2673c052e85d3417cec864d1aabab3263f3328051037a133d9b85765ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:32a9f093b76345e99bd81ff00eabc5ab1ae6c2bdc7d6c843c923049ea3c620ce in /nats-server 
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 19:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:20:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 19:20:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 19:20:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:436f213323b997ad7aca1675cce2c9a9366e3cd51995b9829835ab9762901f98`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (4972530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb98c93488e5f33bab9a8b331c5fbe988a9dd644e39cc15e6626550ec05e541`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e1ba487c56a25895759177de201768f40c51ceeedca983afa03875039445bb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60b5d45617b9109e120de34ac32b0647324dba3d69d2c56366545e50c2484c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:614e1182091dacdaa5043752e8239600bae8aa334cfd383cc326d1753d3eba64 in /nats-server 
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:49:36 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d859c106d4072b51eee7be282394c7f0c288186311ae904751cd95c3cf9468ae`  
		Last Modified: Thu, 02 Mar 2023 18:50:54 GMT  
		Size: 4.7 MB (4739343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e7000b41bf11d721897d126c1e72201203bcc8e9716daad77d7d42ae97853a`  
		Last Modified: Thu, 02 Mar 2023 18:50:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:644eac35d964521bc85286defaf1bae093b36618fe862eedff9a996e330fc60c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4731109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e814afeda8d92b2fb3dcdacf4648234504c6e4cd7fc24cce256cc588a439d7e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:a63786ae76c5e718a4952dd30b2265019e1ca48099ad19279d2e77e5ad704bfc in /nats-server 
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:57:50 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:57:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:57:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e714c80855fb90cb44f135a04bf323493a749536bb9106eb3ef4e69a70682897`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 4.7 MB (4730600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e020ba411c44ee7d23b6bdbd966700955c2d087afd3d79a9ad51e0390e8e7b6`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:35ef84ac5e9bb0d0229fb1a773677d6ee7b23bb58937427d20aaa36987562373
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4559479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f367536d7ef4331c52bf405914c6f7affdccdb8eed05fb4c981efe519fd06f00`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:23081283f9b4d8145ad2b3a276cc08fcb49c4850e322db9560525e495d1bf362 in /nats-server 
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:40:16 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:40:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:40:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:40:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a910efaa632bb8401dbca7cfe541f6dc4da71ea38708992ef153250254493114`  
		Last Modified: Thu, 02 Mar 2023 18:41:09 GMT  
		Size: 4.6 MB (4558972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be7fc9abf13897cf1a5e7026f6a49b3308d5a864640e1f4b6e526ee95f093fc`  
		Last Modified: Thu, 02 Mar 2023 18:41:08 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:c180f2dccb457181af8c515978403a11167dcc1a60e490d49ce3bc48d5df44b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:43348610453f5ecf2cb1eb6b88a459f7ad59353df14950ea55d72a27737f66af
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111708291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94392dbb17d455d1e80a3bc24798e3e1d761cbcd472f1616a352d0995335dbf0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Feb 2023 10:14:28 GMT
RUN Apply image 10.0.17763.4010
# Thu, 16 Feb 2023 02:07:44 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:19:54 GMT
RUN cmd /S /C #(nop) COPY file:c0761502e8e3e74fa63209f49b4d4f61a9c596c726f61d96e045d0b22538ada5 in C:\nats-server.exe 
# Thu, 02 Mar 2023 19:19:55 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:00eaf3341cd3cc6b72f91399cb3bd1aba30eb7eead7596532fe54c4bf1b010d7`  
		Last Modified: Thu, 16 Feb 2023 00:31:21 GMT  
		Size: 106.7 MB (106674970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce19f72ba3efadcebf91b9628f9e85de500fcaa86b6ec8076169cc4bb312c0`  
		Last Modified: Thu, 16 Feb 2023 02:08:32 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4653b8562b98f6d770621adbd89d3392ed2c490da6c30dec79027c7e24ca6b`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (5026943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283f9c4ca607d846e0fc14dd248b106caf329d7c20316e59898b4a202459a77`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c525626770477530f07d56e4934dd0c036e55624d0182762d6df8afbc46aa99`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cda701c245116defdc445fe6ef3e38f73716d9f527f2876d1843abaef3ca11`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec7890747cf0e8bf22b460262ebe10c19f91d00c0710a010fbe2d48d81ca8f0`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:c180f2dccb457181af8c515978403a11167dcc1a60e490d49ce3bc48d5df44b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:43348610453f5ecf2cb1eb6b88a459f7ad59353df14950ea55d72a27737f66af
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111708291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94392dbb17d455d1e80a3bc24798e3e1d761cbcd472f1616a352d0995335dbf0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Feb 2023 10:14:28 GMT
RUN Apply image 10.0.17763.4010
# Thu, 16 Feb 2023 02:07:44 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:19:54 GMT
RUN cmd /S /C #(nop) COPY file:c0761502e8e3e74fa63209f49b4d4f61a9c596c726f61d96e045d0b22538ada5 in C:\nats-server.exe 
# Thu, 02 Mar 2023 19:19:55 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:00eaf3341cd3cc6b72f91399cb3bd1aba30eb7eead7596532fe54c4bf1b010d7`  
		Last Modified: Thu, 16 Feb 2023 00:31:21 GMT  
		Size: 106.7 MB (106674970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce19f72ba3efadcebf91b9628f9e85de500fcaa86b6ec8076169cc4bb312c0`  
		Last Modified: Thu, 16 Feb 2023 02:08:32 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4653b8562b98f6d770621adbd89d3392ed2c490da6c30dec79027c7e24ca6b`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (5026943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283f9c4ca607d846e0fc14dd248b106caf329d7c20316e59898b4a202459a77`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c525626770477530f07d56e4934dd0c036e55624d0182762d6df8afbc46aa99`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cda701c245116defdc445fe6ef3e38f73716d9f527f2876d1843abaef3ca11`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec7890747cf0e8bf22b460262ebe10c19f91d00c0710a010fbe2d48d81ca8f0`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:e9767cfa85287292db74b0533d910366598f93e18b3c60706cf1c25ab7f657be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:1a82b1b261d169994fc6162f2f25894a49e20971560f8b2dff4f90eefb32b421
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74665a2673c052e85d3417cec864d1aabab3263f3328051037a133d9b85765ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:32a9f093b76345e99bd81ff00eabc5ab1ae6c2bdc7d6c843c923049ea3c620ce in /nats-server 
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 19:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:20:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 19:20:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 19:20:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:436f213323b997ad7aca1675cce2c9a9366e3cd51995b9829835ab9762901f98`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (4972530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb98c93488e5f33bab9a8b331c5fbe988a9dd644e39cc15e6626550ec05e541`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e1ba487c56a25895759177de201768f40c51ceeedca983afa03875039445bb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60b5d45617b9109e120de34ac32b0647324dba3d69d2c56366545e50c2484c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:614e1182091dacdaa5043752e8239600bae8aa334cfd383cc326d1753d3eba64 in /nats-server 
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:49:36 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d859c106d4072b51eee7be282394c7f0c288186311ae904751cd95c3cf9468ae`  
		Last Modified: Thu, 02 Mar 2023 18:50:54 GMT  
		Size: 4.7 MB (4739343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e7000b41bf11d721897d126c1e72201203bcc8e9716daad77d7d42ae97853a`  
		Last Modified: Thu, 02 Mar 2023 18:50:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:644eac35d964521bc85286defaf1bae093b36618fe862eedff9a996e330fc60c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4731109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e814afeda8d92b2fb3dcdacf4648234504c6e4cd7fc24cce256cc588a439d7e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:a63786ae76c5e718a4952dd30b2265019e1ca48099ad19279d2e77e5ad704bfc in /nats-server 
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:57:50 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:57:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:57:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e714c80855fb90cb44f135a04bf323493a749536bb9106eb3ef4e69a70682897`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 4.7 MB (4730600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e020ba411c44ee7d23b6bdbd966700955c2d087afd3d79a9ad51e0390e8e7b6`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:35ef84ac5e9bb0d0229fb1a773677d6ee7b23bb58937427d20aaa36987562373
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4559479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f367536d7ef4331c52bf405914c6f7affdccdb8eed05fb4c981efe519fd06f00`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:23081283f9b4d8145ad2b3a276cc08fcb49c4850e322db9560525e495d1bf362 in /nats-server 
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:40:16 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:40:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:40:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:40:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a910efaa632bb8401dbca7cfe541f6dc4da71ea38708992ef153250254493114`  
		Last Modified: Thu, 02 Mar 2023 18:41:09 GMT  
		Size: 4.6 MB (4558972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be7fc9abf13897cf1a5e7026f6a49b3308d5a864640e1f4b6e526ee95f093fc`  
		Last Modified: Thu, 02 Mar 2023 18:41:08 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:6f1f4d7a55b14f4ef4ace0d86d512d62c86510fb3fc2e6235285dee00889deaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:1f57dd803e325796896529880709c0362fc7725ed025a1938061deae3c16926b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1968846299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc817364b97d6849687256fb1e283d68bec70f8fc8cf071fd8f6c3c50ab52b70`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Thu, 16 Feb 2023 00:42:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Feb 2023 02:04:44 GMT
ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:15:51 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 19:15:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.15/nats-server-v2.9.15-windows-amd64.zip
# Thu, 02 Mar 2023 19:15:53 GMT
ENV NATS_SERVER_SHASUM=090f5c310beeb94f603898c6940f2793c292b20c131e578967fc2cdbd01bd42a
# Thu, 02 Mar 2023 19:17:24 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Mar 2023 19:19:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Mar 2023 19:19:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:32 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531f6c3ad9784fc2870ea5ca08c4adccd9318602ed534d822e12b8b658a7b0b6`  
		Last Modified: Thu, 16 Feb 2023 01:37:30 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724509671085dbea52985b930945ecf6cb7694ecee9924bc0226a51a4e01d8a5`  
		Last Modified: Thu, 16 Feb 2023 02:08:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e3c3097c0a4a64935c2f4363011e3e5f02920d5a60f3c71bcbf747ba399daf`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70160f2cef619deb4f1c1bc53f46ee10a33db33dcc93ca0359df7f4191a3812`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600113a59a91ef36bca5a64b4f37eff2ea8dfc7a4e1c63e481009b3c4e5e1375`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64284e36d579640133af5182d567ba35684371aa3d2ebbf3765f442ab0acd3ca`  
		Last Modified: Thu, 02 Mar 2023 19:20:32 GMT  
		Size: 501.6 KB (501609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c0da48daccd70430c8b64cb1c57aff91648fdf57a29e3e747c1177b4b8302b`  
		Last Modified: Thu, 02 Mar 2023 19:20:30 GMT  
		Size: 5.4 MB (5373677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb96b758b91e4d2cfb8b02ed79af5fa5de692cbe61a0779831b75dec1b035e0b`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 2.0 KB (1994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ed891c87e5a2b154abfcbcafb6918c7aa542f2329ecc53362fe6d6708965fa`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae3f74335a8506b631d307e76d730bcbd5e1adaac877411aed88734555005e3`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b31fc962f6aeb0c4f712833073342f7a145a6843e633151eb95263e41ed874`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:6f1f4d7a55b14f4ef4ace0d86d512d62c86510fb3fc2e6235285dee00889deaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:1f57dd803e325796896529880709c0362fc7725ed025a1938061deae3c16926b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1968846299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc817364b97d6849687256fb1e283d68bec70f8fc8cf071fd8f6c3c50ab52b70`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Thu, 16 Feb 2023 00:42:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Feb 2023 02:04:44 GMT
ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:15:51 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 19:15:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.15/nats-server-v2.9.15-windows-amd64.zip
# Thu, 02 Mar 2023 19:15:53 GMT
ENV NATS_SERVER_SHASUM=090f5c310beeb94f603898c6940f2793c292b20c131e578967fc2cdbd01bd42a
# Thu, 02 Mar 2023 19:17:24 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Mar 2023 19:19:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Mar 2023 19:19:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:32 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531f6c3ad9784fc2870ea5ca08c4adccd9318602ed534d822e12b8b658a7b0b6`  
		Last Modified: Thu, 16 Feb 2023 01:37:30 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724509671085dbea52985b930945ecf6cb7694ecee9924bc0226a51a4e01d8a5`  
		Last Modified: Thu, 16 Feb 2023 02:08:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e3c3097c0a4a64935c2f4363011e3e5f02920d5a60f3c71bcbf747ba399daf`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70160f2cef619deb4f1c1bc53f46ee10a33db33dcc93ca0359df7f4191a3812`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600113a59a91ef36bca5a64b4f37eff2ea8dfc7a4e1c63e481009b3c4e5e1375`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64284e36d579640133af5182d567ba35684371aa3d2ebbf3765f442ab0acd3ca`  
		Last Modified: Thu, 02 Mar 2023 19:20:32 GMT  
		Size: 501.6 KB (501609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c0da48daccd70430c8b64cb1c57aff91648fdf57a29e3e747c1177b4b8302b`  
		Last Modified: Thu, 02 Mar 2023 19:20:30 GMT  
		Size: 5.4 MB (5373677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb96b758b91e4d2cfb8b02ed79af5fa5de692cbe61a0779831b75dec1b035e0b`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 2.0 KB (1994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ed891c87e5a2b154abfcbcafb6918c7aa542f2329ecc53362fe6d6708965fa`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae3f74335a8506b631d307e76d730bcbd5e1adaac877411aed88734555005e3`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b31fc962f6aeb0c4f712833073342f7a145a6843e633151eb95263e41ed874`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:04fcc71e7d416348e8761b4081931d735d3774f5b14d33b724cc6caad6037893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4010; amd64

### `nats:2.9` - linux; amd64

```console
$ docker pull nats@sha256:1a82b1b261d169994fc6162f2f25894a49e20971560f8b2dff4f90eefb32b421
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74665a2673c052e85d3417cec864d1aabab3263f3328051037a133d9b85765ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:32a9f093b76345e99bd81ff00eabc5ab1ae6c2bdc7d6c843c923049ea3c620ce in /nats-server 
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 19:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:20:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 19:20:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 19:20:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:436f213323b997ad7aca1675cce2c9a9366e3cd51995b9829835ab9762901f98`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (4972530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb98c93488e5f33bab9a8b331c5fbe988a9dd644e39cc15e6626550ec05e541`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e1ba487c56a25895759177de201768f40c51ceeedca983afa03875039445bb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60b5d45617b9109e120de34ac32b0647324dba3d69d2c56366545e50c2484c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:614e1182091dacdaa5043752e8239600bae8aa334cfd383cc326d1753d3eba64 in /nats-server 
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:49:36 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d859c106d4072b51eee7be282394c7f0c288186311ae904751cd95c3cf9468ae`  
		Last Modified: Thu, 02 Mar 2023 18:50:54 GMT  
		Size: 4.7 MB (4739343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e7000b41bf11d721897d126c1e72201203bcc8e9716daad77d7d42ae97853a`  
		Last Modified: Thu, 02 Mar 2023 18:50:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:644eac35d964521bc85286defaf1bae093b36618fe862eedff9a996e330fc60c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4731109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e814afeda8d92b2fb3dcdacf4648234504c6e4cd7fc24cce256cc588a439d7e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:a63786ae76c5e718a4952dd30b2265019e1ca48099ad19279d2e77e5ad704bfc in /nats-server 
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:57:50 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:57:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:57:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e714c80855fb90cb44f135a04bf323493a749536bb9106eb3ef4e69a70682897`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 4.7 MB (4730600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e020ba411c44ee7d23b6bdbd966700955c2d087afd3d79a9ad51e0390e8e7b6`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:35ef84ac5e9bb0d0229fb1a773677d6ee7b23bb58937427d20aaa36987562373
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4559479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f367536d7ef4331c52bf405914c6f7affdccdb8eed05fb4c981efe519fd06f00`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:23081283f9b4d8145ad2b3a276cc08fcb49c4850e322db9560525e495d1bf362 in /nats-server 
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:40:16 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:40:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:40:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:40:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a910efaa632bb8401dbca7cfe541f6dc4da71ea38708992ef153250254493114`  
		Last Modified: Thu, 02 Mar 2023 18:41:09 GMT  
		Size: 4.6 MB (4558972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be7fc9abf13897cf1a5e7026f6a49b3308d5a864640e1f4b6e526ee95f093fc`  
		Last Modified: Thu, 02 Mar 2023 18:41:08 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:43348610453f5ecf2cb1eb6b88a459f7ad59353df14950ea55d72a27737f66af
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111708291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94392dbb17d455d1e80a3bc24798e3e1d761cbcd472f1616a352d0995335dbf0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Feb 2023 10:14:28 GMT
RUN Apply image 10.0.17763.4010
# Thu, 16 Feb 2023 02:07:44 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:19:54 GMT
RUN cmd /S /C #(nop) COPY file:c0761502e8e3e74fa63209f49b4d4f61a9c596c726f61d96e045d0b22538ada5 in C:\nats-server.exe 
# Thu, 02 Mar 2023 19:19:55 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:00eaf3341cd3cc6b72f91399cb3bd1aba30eb7eead7596532fe54c4bf1b010d7`  
		Last Modified: Thu, 16 Feb 2023 00:31:21 GMT  
		Size: 106.7 MB (106674970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce19f72ba3efadcebf91b9628f9e85de500fcaa86b6ec8076169cc4bb312c0`  
		Last Modified: Thu, 16 Feb 2023 02:08:32 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4653b8562b98f6d770621adbd89d3392ed2c490da6c30dec79027c7e24ca6b`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (5026943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283f9c4ca607d846e0fc14dd248b106caf329d7c20316e59898b4a202459a77`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c525626770477530f07d56e4934dd0c036e55624d0182762d6df8afbc46aa99`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cda701c245116defdc445fe6ef3e38f73716d9f527f2876d1843abaef3ca11`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec7890747cf0e8bf22b460262ebe10c19f91d00c0710a010fbe2d48d81ca8f0`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:f2f2b0e23c7f9fd142e4882d4f4c1cc9c3a6efb17d23b8b16c837d79ff59ca84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:9947eac2dedc476378d9cac73c7df6cba2f1a23da12137214cdc254a15863a46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8635785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d6b3fd56dc8fe20a6e41de4afeacff348a53e1ab388f535f404e9cf74c084d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 19:19:49 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 19:19:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 19:19:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 19:19:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 19:19:52 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:19:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08472afe1eaab0ac7a92349d2da3b64cafacc125426338b278e2fc3b006bd52`  
		Last Modified: Thu, 02 Mar 2023 19:20:25 GMT  
		Size: 5.3 MB (5260338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5ae32cc4383cc8cabea2eba8667d1ff1aaa9bf699469141395387df31c5c4b`  
		Last Modified: Thu, 02 Mar 2023 19:20:24 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3f805284c458c477cde0410e2f6835ab92c5fd6b464cfd6c07cf3d52643c23`  
		Last Modified: Thu, 02 Mar 2023 19:20:24 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d7d52fa58f1f77d24ded7e34e2be977eb4474da0ae5e81639e144de15e0c9bf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8135732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4abf0b19eb2e841ac4255d1702b59ec4fb05a30e60561a5cfd8efcd2c8e4b24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:49:28 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:49:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:49:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:49:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:49:31 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:49:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2d8c7c008839e4297490fe62726b0511bb9a7c6486b7f97b106788aa11c6f8`  
		Last Modified: Thu, 02 Mar 2023 18:50:25 GMT  
		Size: 5.0 MB (5023847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8437de52ce6ce410d6359afa18a00cc025d2f5846e854d4b4e398f9eb16ce1c5`  
		Last Modified: Thu, 02 Mar 2023 18:50:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98d271690d33766c10fca8cfd7d844162956eb2db3195e9bf3e21ed587c7f60`  
		Last Modified: Thu, 02 Mar 2023 18:50:24 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d0f535bd276e1b92c60c9b8fe33cb90d439049071159843142c026302b54bf7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7887576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b405c7e2612cb810f225540c61a3eb1f02c1efbb3910aa30aa7b46b068fef2db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:31 GMT
ADD file:143b601fcc6b5d7d95d3e5ccad3fec7081191a47e28d4f9294a7fb2499cab1af in / 
# Fri, 10 Feb 2023 21:51:31 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:57:36 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:57:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:57:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:57:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:57:39 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:57:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6fb81ff47bd6d7db0ed86c9b951ad6417ec73ab60af6d22daa604076a902629c`  
		Last Modified: Fri, 10 Feb 2023 21:52:33 GMT  
		Size: 2.9 MB (2868494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19b56339a1ba27c396a17554216f8da9ef664a78ec52c24c39630ad6b00ccea`  
		Last Modified: Thu, 02 Mar 2023 18:58:37 GMT  
		Size: 5.0 MB (5018081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6919af5eaed170352d5fcbc4a52cdfd188a277c02b8c39538f0626a12afc6e`  
		Last Modified: Thu, 02 Mar 2023 18:58:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99bb0ebd369abc6e32fcdbdbade73f2a1504cb8edae42327051d1343b982a8b`  
		Last Modified: Thu, 02 Mar 2023 18:58:36 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:31516678d6c3c1c5d7444e85d06618022258cfb3a23bbed0e44a358bbf7fea1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8104002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f18af0a035256392dde53a51a48628b107ebad3b4b6627160aaab7a964ce40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:39:45 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:39:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:39:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:39:47 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:39:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f03396fa041b5be75e5a939ff3aadaff2e65f529a07bcbd4748b581e3e193e1`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 4.8 MB (4841045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cceddcd111b1a86e5348af7dccf8c0b0d1c1dfec305c026bd9351bd0d1cce7`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca183fb542756060f50207e2bdac939b035a4f4ff2075b0371f87399242950a2`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.17`

```console
$ docker pull nats@sha256:f2f2b0e23c7f9fd142e4882d4f4c1cc9c3a6efb17d23b8b16c837d79ff59ca84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.17` - linux; amd64

```console
$ docker pull nats@sha256:9947eac2dedc476378d9cac73c7df6cba2f1a23da12137214cdc254a15863a46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8635785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d6b3fd56dc8fe20a6e41de4afeacff348a53e1ab388f535f404e9cf74c084d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 19:19:49 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 19:19:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 19:19:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 19:19:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 19:19:52 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:19:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08472afe1eaab0ac7a92349d2da3b64cafacc125426338b278e2fc3b006bd52`  
		Last Modified: Thu, 02 Mar 2023 19:20:25 GMT  
		Size: 5.3 MB (5260338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5ae32cc4383cc8cabea2eba8667d1ff1aaa9bf699469141395387df31c5c4b`  
		Last Modified: Thu, 02 Mar 2023 19:20:24 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3f805284c458c477cde0410e2f6835ab92c5fd6b464cfd6c07cf3d52643c23`  
		Last Modified: Thu, 02 Mar 2023 19:20:24 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.17` - linux; arm variant v6

```console
$ docker pull nats@sha256:d7d52fa58f1f77d24ded7e34e2be977eb4474da0ae5e81639e144de15e0c9bf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8135732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4abf0b19eb2e841ac4255d1702b59ec4fb05a30e60561a5cfd8efcd2c8e4b24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:49:28 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:49:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:49:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:49:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:49:31 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:49:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2d8c7c008839e4297490fe62726b0511bb9a7c6486b7f97b106788aa11c6f8`  
		Last Modified: Thu, 02 Mar 2023 18:50:25 GMT  
		Size: 5.0 MB (5023847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8437de52ce6ce410d6359afa18a00cc025d2f5846e854d4b4e398f9eb16ce1c5`  
		Last Modified: Thu, 02 Mar 2023 18:50:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98d271690d33766c10fca8cfd7d844162956eb2db3195e9bf3e21ed587c7f60`  
		Last Modified: Thu, 02 Mar 2023 18:50:24 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.17` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d0f535bd276e1b92c60c9b8fe33cb90d439049071159843142c026302b54bf7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7887576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b405c7e2612cb810f225540c61a3eb1f02c1efbb3910aa30aa7b46b068fef2db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:31 GMT
ADD file:143b601fcc6b5d7d95d3e5ccad3fec7081191a47e28d4f9294a7fb2499cab1af in / 
# Fri, 10 Feb 2023 21:51:31 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:57:36 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:57:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:57:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:57:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:57:39 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:57:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6fb81ff47bd6d7db0ed86c9b951ad6417ec73ab60af6d22daa604076a902629c`  
		Last Modified: Fri, 10 Feb 2023 21:52:33 GMT  
		Size: 2.9 MB (2868494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19b56339a1ba27c396a17554216f8da9ef664a78ec52c24c39630ad6b00ccea`  
		Last Modified: Thu, 02 Mar 2023 18:58:37 GMT  
		Size: 5.0 MB (5018081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6919af5eaed170352d5fcbc4a52cdfd188a277c02b8c39538f0626a12afc6e`  
		Last Modified: Thu, 02 Mar 2023 18:58:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99bb0ebd369abc6e32fcdbdbade73f2a1504cb8edae42327051d1343b982a8b`  
		Last Modified: Thu, 02 Mar 2023 18:58:36 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:31516678d6c3c1c5d7444e85d06618022258cfb3a23bbed0e44a358bbf7fea1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8104002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f18af0a035256392dde53a51a48628b107ebad3b4b6627160aaab7a964ce40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:39:45 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:39:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:39:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:39:47 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:39:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f03396fa041b5be75e5a939ff3aadaff2e65f529a07bcbd4748b581e3e193e1`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 4.8 MB (4841045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cceddcd111b1a86e5348af7dccf8c0b0d1c1dfec305c026bd9351bd0d1cce7`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca183fb542756060f50207e2bdac939b035a4f4ff2075b0371f87399242950a2`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:e9767cfa85287292db74b0533d910366598f93e18b3c60706cf1c25ab7f657be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:1a82b1b261d169994fc6162f2f25894a49e20971560f8b2dff4f90eefb32b421
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74665a2673c052e85d3417cec864d1aabab3263f3328051037a133d9b85765ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:32a9f093b76345e99bd81ff00eabc5ab1ae6c2bdc7d6c843c923049ea3c620ce in /nats-server 
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 19:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:20:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 19:20:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 19:20:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:436f213323b997ad7aca1675cce2c9a9366e3cd51995b9829835ab9762901f98`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (4972530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb98c93488e5f33bab9a8b331c5fbe988a9dd644e39cc15e6626550ec05e541`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e1ba487c56a25895759177de201768f40c51ceeedca983afa03875039445bb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60b5d45617b9109e120de34ac32b0647324dba3d69d2c56366545e50c2484c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:614e1182091dacdaa5043752e8239600bae8aa334cfd383cc326d1753d3eba64 in /nats-server 
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:49:36 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d859c106d4072b51eee7be282394c7f0c288186311ae904751cd95c3cf9468ae`  
		Last Modified: Thu, 02 Mar 2023 18:50:54 GMT  
		Size: 4.7 MB (4739343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e7000b41bf11d721897d126c1e72201203bcc8e9716daad77d7d42ae97853a`  
		Last Modified: Thu, 02 Mar 2023 18:50:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:644eac35d964521bc85286defaf1bae093b36618fe862eedff9a996e330fc60c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4731109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e814afeda8d92b2fb3dcdacf4648234504c6e4cd7fc24cce256cc588a439d7e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:a63786ae76c5e718a4952dd30b2265019e1ca48099ad19279d2e77e5ad704bfc in /nats-server 
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:57:50 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:57:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:57:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e714c80855fb90cb44f135a04bf323493a749536bb9106eb3ef4e69a70682897`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 4.7 MB (4730600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e020ba411c44ee7d23b6bdbd966700955c2d087afd3d79a9ad51e0390e8e7b6`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:35ef84ac5e9bb0d0229fb1a773677d6ee7b23bb58937427d20aaa36987562373
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4559479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f367536d7ef4331c52bf405914c6f7affdccdb8eed05fb4c981efe519fd06f00`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:23081283f9b4d8145ad2b3a276cc08fcb49c4850e322db9560525e495d1bf362 in /nats-server 
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:40:16 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:40:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:40:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:40:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a910efaa632bb8401dbca7cfe541f6dc4da71ea38708992ef153250254493114`  
		Last Modified: Thu, 02 Mar 2023 18:41:09 GMT  
		Size: 4.6 MB (4558972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be7fc9abf13897cf1a5e7026f6a49b3308d5a864640e1f4b6e526ee95f093fc`  
		Last Modified: Thu, 02 Mar 2023 18:41:08 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver`

```console
$ docker pull nats@sha256:c180f2dccb457181af8c515978403a11167dcc1a60e490d49ce3bc48d5df44b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:43348610453f5ecf2cb1eb6b88a459f7ad59353df14950ea55d72a27737f66af
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111708291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94392dbb17d455d1e80a3bc24798e3e1d761cbcd472f1616a352d0995335dbf0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Feb 2023 10:14:28 GMT
RUN Apply image 10.0.17763.4010
# Thu, 16 Feb 2023 02:07:44 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:19:54 GMT
RUN cmd /S /C #(nop) COPY file:c0761502e8e3e74fa63209f49b4d4f61a9c596c726f61d96e045d0b22538ada5 in C:\nats-server.exe 
# Thu, 02 Mar 2023 19:19:55 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:00eaf3341cd3cc6b72f91399cb3bd1aba30eb7eead7596532fe54c4bf1b010d7`  
		Last Modified: Thu, 16 Feb 2023 00:31:21 GMT  
		Size: 106.7 MB (106674970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce19f72ba3efadcebf91b9628f9e85de500fcaa86b6ec8076169cc4bb312c0`  
		Last Modified: Thu, 16 Feb 2023 02:08:32 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4653b8562b98f6d770621adbd89d3392ed2c490da6c30dec79027c7e24ca6b`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (5026943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283f9c4ca607d846e0fc14dd248b106caf329d7c20316e59898b4a202459a77`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c525626770477530f07d56e4934dd0c036e55624d0182762d6df8afbc46aa99`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cda701c245116defdc445fe6ef3e38f73716d9f527f2876d1843abaef3ca11`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec7890747cf0e8bf22b460262ebe10c19f91d00c0710a010fbe2d48d81ca8f0`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:c180f2dccb457181af8c515978403a11167dcc1a60e490d49ce3bc48d5df44b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:43348610453f5ecf2cb1eb6b88a459f7ad59353df14950ea55d72a27737f66af
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111708291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94392dbb17d455d1e80a3bc24798e3e1d761cbcd472f1616a352d0995335dbf0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Feb 2023 10:14:28 GMT
RUN Apply image 10.0.17763.4010
# Thu, 16 Feb 2023 02:07:44 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:19:54 GMT
RUN cmd /S /C #(nop) COPY file:c0761502e8e3e74fa63209f49b4d4f61a9c596c726f61d96e045d0b22538ada5 in C:\nats-server.exe 
# Thu, 02 Mar 2023 19:19:55 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:00eaf3341cd3cc6b72f91399cb3bd1aba30eb7eead7596532fe54c4bf1b010d7`  
		Last Modified: Thu, 16 Feb 2023 00:31:21 GMT  
		Size: 106.7 MB (106674970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce19f72ba3efadcebf91b9628f9e85de500fcaa86b6ec8076169cc4bb312c0`  
		Last Modified: Thu, 16 Feb 2023 02:08:32 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4653b8562b98f6d770621adbd89d3392ed2c490da6c30dec79027c7e24ca6b`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (5026943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283f9c4ca607d846e0fc14dd248b106caf329d7c20316e59898b4a202459a77`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c525626770477530f07d56e4934dd0c036e55624d0182762d6df8afbc46aa99`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cda701c245116defdc445fe6ef3e38f73716d9f527f2876d1843abaef3ca11`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec7890747cf0e8bf22b460262ebe10c19f91d00c0710a010fbe2d48d81ca8f0`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:e9767cfa85287292db74b0533d910366598f93e18b3c60706cf1c25ab7f657be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:1a82b1b261d169994fc6162f2f25894a49e20971560f8b2dff4f90eefb32b421
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74665a2673c052e85d3417cec864d1aabab3263f3328051037a133d9b85765ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:32a9f093b76345e99bd81ff00eabc5ab1ae6c2bdc7d6c843c923049ea3c620ce in /nats-server 
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 19:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:20:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 19:20:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 19:20:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:436f213323b997ad7aca1675cce2c9a9366e3cd51995b9829835ab9762901f98`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (4972530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb98c93488e5f33bab9a8b331c5fbe988a9dd644e39cc15e6626550ec05e541`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e1ba487c56a25895759177de201768f40c51ceeedca983afa03875039445bb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60b5d45617b9109e120de34ac32b0647324dba3d69d2c56366545e50c2484c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:614e1182091dacdaa5043752e8239600bae8aa334cfd383cc326d1753d3eba64 in /nats-server 
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:49:36 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d859c106d4072b51eee7be282394c7f0c288186311ae904751cd95c3cf9468ae`  
		Last Modified: Thu, 02 Mar 2023 18:50:54 GMT  
		Size: 4.7 MB (4739343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e7000b41bf11d721897d126c1e72201203bcc8e9716daad77d7d42ae97853a`  
		Last Modified: Thu, 02 Mar 2023 18:50:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:644eac35d964521bc85286defaf1bae093b36618fe862eedff9a996e330fc60c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4731109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e814afeda8d92b2fb3dcdacf4648234504c6e4cd7fc24cce256cc588a439d7e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:a63786ae76c5e718a4952dd30b2265019e1ca48099ad19279d2e77e5ad704bfc in /nats-server 
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:57:50 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:57:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:57:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e714c80855fb90cb44f135a04bf323493a749536bb9106eb3ef4e69a70682897`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 4.7 MB (4730600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e020ba411c44ee7d23b6bdbd966700955c2d087afd3d79a9ad51e0390e8e7b6`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:35ef84ac5e9bb0d0229fb1a773677d6ee7b23bb58937427d20aaa36987562373
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4559479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f367536d7ef4331c52bf405914c6f7affdccdb8eed05fb4c981efe519fd06f00`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:23081283f9b4d8145ad2b3a276cc08fcb49c4850e322db9560525e495d1bf362 in /nats-server 
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:40:16 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:40:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:40:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:40:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a910efaa632bb8401dbca7cfe541f6dc4da71ea38708992ef153250254493114`  
		Last Modified: Thu, 02 Mar 2023 18:41:09 GMT  
		Size: 4.6 MB (4558972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be7fc9abf13897cf1a5e7026f6a49b3308d5a864640e1f4b6e526ee95f093fc`  
		Last Modified: Thu, 02 Mar 2023 18:41:08 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore`

```console
$ docker pull nats@sha256:6f1f4d7a55b14f4ef4ace0d86d512d62c86510fb3fc2e6235285dee00889deaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:1f57dd803e325796896529880709c0362fc7725ed025a1938061deae3c16926b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1968846299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc817364b97d6849687256fb1e283d68bec70f8fc8cf071fd8f6c3c50ab52b70`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Thu, 16 Feb 2023 00:42:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Feb 2023 02:04:44 GMT
ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:15:51 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 19:15:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.15/nats-server-v2.9.15-windows-amd64.zip
# Thu, 02 Mar 2023 19:15:53 GMT
ENV NATS_SERVER_SHASUM=090f5c310beeb94f603898c6940f2793c292b20c131e578967fc2cdbd01bd42a
# Thu, 02 Mar 2023 19:17:24 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Mar 2023 19:19:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Mar 2023 19:19:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:32 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531f6c3ad9784fc2870ea5ca08c4adccd9318602ed534d822e12b8b658a7b0b6`  
		Last Modified: Thu, 16 Feb 2023 01:37:30 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724509671085dbea52985b930945ecf6cb7694ecee9924bc0226a51a4e01d8a5`  
		Last Modified: Thu, 16 Feb 2023 02:08:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e3c3097c0a4a64935c2f4363011e3e5f02920d5a60f3c71bcbf747ba399daf`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70160f2cef619deb4f1c1bc53f46ee10a33db33dcc93ca0359df7f4191a3812`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600113a59a91ef36bca5a64b4f37eff2ea8dfc7a4e1c63e481009b3c4e5e1375`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64284e36d579640133af5182d567ba35684371aa3d2ebbf3765f442ab0acd3ca`  
		Last Modified: Thu, 02 Mar 2023 19:20:32 GMT  
		Size: 501.6 KB (501609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c0da48daccd70430c8b64cb1c57aff91648fdf57a29e3e747c1177b4b8302b`  
		Last Modified: Thu, 02 Mar 2023 19:20:30 GMT  
		Size: 5.4 MB (5373677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb96b758b91e4d2cfb8b02ed79af5fa5de692cbe61a0779831b75dec1b035e0b`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 2.0 KB (1994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ed891c87e5a2b154abfcbcafb6918c7aa542f2329ecc53362fe6d6708965fa`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae3f74335a8506b631d307e76d730bcbd5e1adaac877411aed88734555005e3`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b31fc962f6aeb0c4f712833073342f7a145a6843e633151eb95263e41ed874`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:6f1f4d7a55b14f4ef4ace0d86d512d62c86510fb3fc2e6235285dee00889deaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:1f57dd803e325796896529880709c0362fc7725ed025a1938061deae3c16926b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1968846299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc817364b97d6849687256fb1e283d68bec70f8fc8cf071fd8f6c3c50ab52b70`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Thu, 16 Feb 2023 00:42:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Feb 2023 02:04:44 GMT
ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:15:51 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 19:15:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.15/nats-server-v2.9.15-windows-amd64.zip
# Thu, 02 Mar 2023 19:15:53 GMT
ENV NATS_SERVER_SHASUM=090f5c310beeb94f603898c6940f2793c292b20c131e578967fc2cdbd01bd42a
# Thu, 02 Mar 2023 19:17:24 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Mar 2023 19:19:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Mar 2023 19:19:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:32 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531f6c3ad9784fc2870ea5ca08c4adccd9318602ed534d822e12b8b658a7b0b6`  
		Last Modified: Thu, 16 Feb 2023 01:37:30 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724509671085dbea52985b930945ecf6cb7694ecee9924bc0226a51a4e01d8a5`  
		Last Modified: Thu, 16 Feb 2023 02:08:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e3c3097c0a4a64935c2f4363011e3e5f02920d5a60f3c71bcbf747ba399daf`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70160f2cef619deb4f1c1bc53f46ee10a33db33dcc93ca0359df7f4191a3812`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600113a59a91ef36bca5a64b4f37eff2ea8dfc7a4e1c63e481009b3c4e5e1375`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64284e36d579640133af5182d567ba35684371aa3d2ebbf3765f442ab0acd3ca`  
		Last Modified: Thu, 02 Mar 2023 19:20:32 GMT  
		Size: 501.6 KB (501609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c0da48daccd70430c8b64cb1c57aff91648fdf57a29e3e747c1177b4b8302b`  
		Last Modified: Thu, 02 Mar 2023 19:20:30 GMT  
		Size: 5.4 MB (5373677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb96b758b91e4d2cfb8b02ed79af5fa5de692cbe61a0779831b75dec1b035e0b`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 2.0 KB (1994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ed891c87e5a2b154abfcbcafb6918c7aa542f2329ecc53362fe6d6708965fa`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae3f74335a8506b631d307e76d730bcbd5e1adaac877411aed88734555005e3`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b31fc962f6aeb0c4f712833073342f7a145a6843e633151eb95263e41ed874`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.15`

```console
$ docker pull nats@sha256:04fcc71e7d416348e8761b4081931d735d3774f5b14d33b724cc6caad6037893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4010; amd64

### `nats:2.9.15` - linux; amd64

```console
$ docker pull nats@sha256:1a82b1b261d169994fc6162f2f25894a49e20971560f8b2dff4f90eefb32b421
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74665a2673c052e85d3417cec864d1aabab3263f3328051037a133d9b85765ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:32a9f093b76345e99bd81ff00eabc5ab1ae6c2bdc7d6c843c923049ea3c620ce in /nats-server 
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 19:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:20:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 19:20:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 19:20:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:436f213323b997ad7aca1675cce2c9a9366e3cd51995b9829835ab9762901f98`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (4972530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb98c93488e5f33bab9a8b331c5fbe988a9dd644e39cc15e6626550ec05e541`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e1ba487c56a25895759177de201768f40c51ceeedca983afa03875039445bb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60b5d45617b9109e120de34ac32b0647324dba3d69d2c56366545e50c2484c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:614e1182091dacdaa5043752e8239600bae8aa334cfd383cc326d1753d3eba64 in /nats-server 
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:49:36 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d859c106d4072b51eee7be282394c7f0c288186311ae904751cd95c3cf9468ae`  
		Last Modified: Thu, 02 Mar 2023 18:50:54 GMT  
		Size: 4.7 MB (4739343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e7000b41bf11d721897d126c1e72201203bcc8e9716daad77d7d42ae97853a`  
		Last Modified: Thu, 02 Mar 2023 18:50:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:644eac35d964521bc85286defaf1bae093b36618fe862eedff9a996e330fc60c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4731109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e814afeda8d92b2fb3dcdacf4648234504c6e4cd7fc24cce256cc588a439d7e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:a63786ae76c5e718a4952dd30b2265019e1ca48099ad19279d2e77e5ad704bfc in /nats-server 
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:57:50 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:57:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:57:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e714c80855fb90cb44f135a04bf323493a749536bb9106eb3ef4e69a70682897`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 4.7 MB (4730600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e020ba411c44ee7d23b6bdbd966700955c2d087afd3d79a9ad51e0390e8e7b6`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:35ef84ac5e9bb0d0229fb1a773677d6ee7b23bb58937427d20aaa36987562373
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4559479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f367536d7ef4331c52bf405914c6f7affdccdb8eed05fb4c981efe519fd06f00`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:23081283f9b4d8145ad2b3a276cc08fcb49c4850e322db9560525e495d1bf362 in /nats-server 
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:40:16 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:40:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:40:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:40:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a910efaa632bb8401dbca7cfe541f6dc4da71ea38708992ef153250254493114`  
		Last Modified: Thu, 02 Mar 2023 18:41:09 GMT  
		Size: 4.6 MB (4558972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be7fc9abf13897cf1a5e7026f6a49b3308d5a864640e1f4b6e526ee95f093fc`  
		Last Modified: Thu, 02 Mar 2023 18:41:08 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.15` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:43348610453f5ecf2cb1eb6b88a459f7ad59353df14950ea55d72a27737f66af
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111708291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94392dbb17d455d1e80a3bc24798e3e1d761cbcd472f1616a352d0995335dbf0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Feb 2023 10:14:28 GMT
RUN Apply image 10.0.17763.4010
# Thu, 16 Feb 2023 02:07:44 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:19:54 GMT
RUN cmd /S /C #(nop) COPY file:c0761502e8e3e74fa63209f49b4d4f61a9c596c726f61d96e045d0b22538ada5 in C:\nats-server.exe 
# Thu, 02 Mar 2023 19:19:55 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:00eaf3341cd3cc6b72f91399cb3bd1aba30eb7eead7596532fe54c4bf1b010d7`  
		Last Modified: Thu, 16 Feb 2023 00:31:21 GMT  
		Size: 106.7 MB (106674970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce19f72ba3efadcebf91b9628f9e85de500fcaa86b6ec8076169cc4bb312c0`  
		Last Modified: Thu, 16 Feb 2023 02:08:32 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4653b8562b98f6d770621adbd89d3392ed2c490da6c30dec79027c7e24ca6b`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (5026943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283f9c4ca607d846e0fc14dd248b106caf329d7c20316e59898b4a202459a77`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c525626770477530f07d56e4934dd0c036e55624d0182762d6df8afbc46aa99`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cda701c245116defdc445fe6ef3e38f73716d9f527f2876d1843abaef3ca11`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec7890747cf0e8bf22b460262ebe10c19f91d00c0710a010fbe2d48d81ca8f0`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.15-alpine`

```console
$ docker pull nats@sha256:f2f2b0e23c7f9fd142e4882d4f4c1cc9c3a6efb17d23b8b16c837d79ff59ca84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.15-alpine` - linux; amd64

```console
$ docker pull nats@sha256:9947eac2dedc476378d9cac73c7df6cba2f1a23da12137214cdc254a15863a46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8635785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d6b3fd56dc8fe20a6e41de4afeacff348a53e1ab388f535f404e9cf74c084d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 19:19:49 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 19:19:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 19:19:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 19:19:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 19:19:52 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:19:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08472afe1eaab0ac7a92349d2da3b64cafacc125426338b278e2fc3b006bd52`  
		Last Modified: Thu, 02 Mar 2023 19:20:25 GMT  
		Size: 5.3 MB (5260338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5ae32cc4383cc8cabea2eba8667d1ff1aaa9bf699469141395387df31c5c4b`  
		Last Modified: Thu, 02 Mar 2023 19:20:24 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3f805284c458c477cde0410e2f6835ab92c5fd6b464cfd6c07cf3d52643c23`  
		Last Modified: Thu, 02 Mar 2023 19:20:24 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.15-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d7d52fa58f1f77d24ded7e34e2be977eb4474da0ae5e81639e144de15e0c9bf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8135732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4abf0b19eb2e841ac4255d1702b59ec4fb05a30e60561a5cfd8efcd2c8e4b24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:49:28 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:49:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:49:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:49:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:49:31 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:49:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2d8c7c008839e4297490fe62726b0511bb9a7c6486b7f97b106788aa11c6f8`  
		Last Modified: Thu, 02 Mar 2023 18:50:25 GMT  
		Size: 5.0 MB (5023847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8437de52ce6ce410d6359afa18a00cc025d2f5846e854d4b4e398f9eb16ce1c5`  
		Last Modified: Thu, 02 Mar 2023 18:50:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98d271690d33766c10fca8cfd7d844162956eb2db3195e9bf3e21ed587c7f60`  
		Last Modified: Thu, 02 Mar 2023 18:50:24 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.15-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d0f535bd276e1b92c60c9b8fe33cb90d439049071159843142c026302b54bf7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7887576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b405c7e2612cb810f225540c61a3eb1f02c1efbb3910aa30aa7b46b068fef2db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:31 GMT
ADD file:143b601fcc6b5d7d95d3e5ccad3fec7081191a47e28d4f9294a7fb2499cab1af in / 
# Fri, 10 Feb 2023 21:51:31 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:57:36 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:57:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:57:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:57:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:57:39 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:57:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6fb81ff47bd6d7db0ed86c9b951ad6417ec73ab60af6d22daa604076a902629c`  
		Last Modified: Fri, 10 Feb 2023 21:52:33 GMT  
		Size: 2.9 MB (2868494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19b56339a1ba27c396a17554216f8da9ef664a78ec52c24c39630ad6b00ccea`  
		Last Modified: Thu, 02 Mar 2023 18:58:37 GMT  
		Size: 5.0 MB (5018081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6919af5eaed170352d5fcbc4a52cdfd188a277c02b8c39538f0626a12afc6e`  
		Last Modified: Thu, 02 Mar 2023 18:58:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99bb0ebd369abc6e32fcdbdbade73f2a1504cb8edae42327051d1343b982a8b`  
		Last Modified: Thu, 02 Mar 2023 18:58:36 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.15-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:31516678d6c3c1c5d7444e85d06618022258cfb3a23bbed0e44a358bbf7fea1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8104002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f18af0a035256392dde53a51a48628b107ebad3b4b6627160aaab7a964ce40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:39:45 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:39:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:39:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:39:47 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:39:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f03396fa041b5be75e5a939ff3aadaff2e65f529a07bcbd4748b581e3e193e1`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 4.8 MB (4841045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cceddcd111b1a86e5348af7dccf8c0b0d1c1dfec305c026bd9351bd0d1cce7`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca183fb542756060f50207e2bdac939b035a4f4ff2075b0371f87399242950a2`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.15-alpine3.17`

```console
$ docker pull nats@sha256:f2f2b0e23c7f9fd142e4882d4f4c1cc9c3a6efb17d23b8b16c837d79ff59ca84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.15-alpine3.17` - linux; amd64

```console
$ docker pull nats@sha256:9947eac2dedc476378d9cac73c7df6cba2f1a23da12137214cdc254a15863a46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8635785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d6b3fd56dc8fe20a6e41de4afeacff348a53e1ab388f535f404e9cf74c084d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 19:19:49 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 19:19:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 19:19:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 19:19:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 19:19:52 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:19:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08472afe1eaab0ac7a92349d2da3b64cafacc125426338b278e2fc3b006bd52`  
		Last Modified: Thu, 02 Mar 2023 19:20:25 GMT  
		Size: 5.3 MB (5260338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5ae32cc4383cc8cabea2eba8667d1ff1aaa9bf699469141395387df31c5c4b`  
		Last Modified: Thu, 02 Mar 2023 19:20:24 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3f805284c458c477cde0410e2f6835ab92c5fd6b464cfd6c07cf3d52643c23`  
		Last Modified: Thu, 02 Mar 2023 19:20:24 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.15-alpine3.17` - linux; arm variant v6

```console
$ docker pull nats@sha256:d7d52fa58f1f77d24ded7e34e2be977eb4474da0ae5e81639e144de15e0c9bf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8135732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4abf0b19eb2e841ac4255d1702b59ec4fb05a30e60561a5cfd8efcd2c8e4b24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:49:28 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:49:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:49:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:49:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:49:31 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:49:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2d8c7c008839e4297490fe62726b0511bb9a7c6486b7f97b106788aa11c6f8`  
		Last Modified: Thu, 02 Mar 2023 18:50:25 GMT  
		Size: 5.0 MB (5023847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8437de52ce6ce410d6359afa18a00cc025d2f5846e854d4b4e398f9eb16ce1c5`  
		Last Modified: Thu, 02 Mar 2023 18:50:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98d271690d33766c10fca8cfd7d844162956eb2db3195e9bf3e21ed587c7f60`  
		Last Modified: Thu, 02 Mar 2023 18:50:24 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.15-alpine3.17` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d0f535bd276e1b92c60c9b8fe33cb90d439049071159843142c026302b54bf7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7887576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b405c7e2612cb810f225540c61a3eb1f02c1efbb3910aa30aa7b46b068fef2db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:31 GMT
ADD file:143b601fcc6b5d7d95d3e5ccad3fec7081191a47e28d4f9294a7fb2499cab1af in / 
# Fri, 10 Feb 2023 21:51:31 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:57:36 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:57:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:57:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:57:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:57:39 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:57:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6fb81ff47bd6d7db0ed86c9b951ad6417ec73ab60af6d22daa604076a902629c`  
		Last Modified: Fri, 10 Feb 2023 21:52:33 GMT  
		Size: 2.9 MB (2868494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19b56339a1ba27c396a17554216f8da9ef664a78ec52c24c39630ad6b00ccea`  
		Last Modified: Thu, 02 Mar 2023 18:58:37 GMT  
		Size: 5.0 MB (5018081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6919af5eaed170352d5fcbc4a52cdfd188a277c02b8c39538f0626a12afc6e`  
		Last Modified: Thu, 02 Mar 2023 18:58:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99bb0ebd369abc6e32fcdbdbade73f2a1504cb8edae42327051d1343b982a8b`  
		Last Modified: Thu, 02 Mar 2023 18:58:36 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.15-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:31516678d6c3c1c5d7444e85d06618022258cfb3a23bbed0e44a358bbf7fea1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8104002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f18af0a035256392dde53a51a48628b107ebad3b4b6627160aaab7a964ce40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:39:45 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:39:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:39:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:39:47 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:39:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f03396fa041b5be75e5a939ff3aadaff2e65f529a07bcbd4748b581e3e193e1`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 4.8 MB (4841045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cceddcd111b1a86e5348af7dccf8c0b0d1c1dfec305c026bd9351bd0d1cce7`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca183fb542756060f50207e2bdac939b035a4f4ff2075b0371f87399242950a2`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.15-linux`

```console
$ docker pull nats@sha256:e9767cfa85287292db74b0533d910366598f93e18b3c60706cf1c25ab7f657be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.15-linux` - linux; amd64

```console
$ docker pull nats@sha256:1a82b1b261d169994fc6162f2f25894a49e20971560f8b2dff4f90eefb32b421
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74665a2673c052e85d3417cec864d1aabab3263f3328051037a133d9b85765ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:32a9f093b76345e99bd81ff00eabc5ab1ae6c2bdc7d6c843c923049ea3c620ce in /nats-server 
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 19:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:20:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 19:20:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 19:20:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:436f213323b997ad7aca1675cce2c9a9366e3cd51995b9829835ab9762901f98`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (4972530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb98c93488e5f33bab9a8b331c5fbe988a9dd644e39cc15e6626550ec05e541`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.15-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e1ba487c56a25895759177de201768f40c51ceeedca983afa03875039445bb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60b5d45617b9109e120de34ac32b0647324dba3d69d2c56366545e50c2484c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:614e1182091dacdaa5043752e8239600bae8aa334cfd383cc326d1753d3eba64 in /nats-server 
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:49:36 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d859c106d4072b51eee7be282394c7f0c288186311ae904751cd95c3cf9468ae`  
		Last Modified: Thu, 02 Mar 2023 18:50:54 GMT  
		Size: 4.7 MB (4739343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e7000b41bf11d721897d126c1e72201203bcc8e9716daad77d7d42ae97853a`  
		Last Modified: Thu, 02 Mar 2023 18:50:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.15-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:644eac35d964521bc85286defaf1bae093b36618fe862eedff9a996e330fc60c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4731109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e814afeda8d92b2fb3dcdacf4648234504c6e4cd7fc24cce256cc588a439d7e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:a63786ae76c5e718a4952dd30b2265019e1ca48099ad19279d2e77e5ad704bfc in /nats-server 
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:57:50 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:57:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:57:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e714c80855fb90cb44f135a04bf323493a749536bb9106eb3ef4e69a70682897`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 4.7 MB (4730600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e020ba411c44ee7d23b6bdbd966700955c2d087afd3d79a9ad51e0390e8e7b6`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.15-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:35ef84ac5e9bb0d0229fb1a773677d6ee7b23bb58937427d20aaa36987562373
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4559479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f367536d7ef4331c52bf405914c6f7affdccdb8eed05fb4c981efe519fd06f00`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:23081283f9b4d8145ad2b3a276cc08fcb49c4850e322db9560525e495d1bf362 in /nats-server 
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:40:16 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:40:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:40:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:40:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a910efaa632bb8401dbca7cfe541f6dc4da71ea38708992ef153250254493114`  
		Last Modified: Thu, 02 Mar 2023 18:41:09 GMT  
		Size: 4.6 MB (4558972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be7fc9abf13897cf1a5e7026f6a49b3308d5a864640e1f4b6e526ee95f093fc`  
		Last Modified: Thu, 02 Mar 2023 18:41:08 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.15-nanoserver`

```console
$ docker pull nats@sha256:c180f2dccb457181af8c515978403a11167dcc1a60e490d49ce3bc48d5df44b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `nats:2.9.15-nanoserver` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:43348610453f5ecf2cb1eb6b88a459f7ad59353df14950ea55d72a27737f66af
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111708291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94392dbb17d455d1e80a3bc24798e3e1d761cbcd472f1616a352d0995335dbf0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Feb 2023 10:14:28 GMT
RUN Apply image 10.0.17763.4010
# Thu, 16 Feb 2023 02:07:44 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:19:54 GMT
RUN cmd /S /C #(nop) COPY file:c0761502e8e3e74fa63209f49b4d4f61a9c596c726f61d96e045d0b22538ada5 in C:\nats-server.exe 
# Thu, 02 Mar 2023 19:19:55 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:00eaf3341cd3cc6b72f91399cb3bd1aba30eb7eead7596532fe54c4bf1b010d7`  
		Last Modified: Thu, 16 Feb 2023 00:31:21 GMT  
		Size: 106.7 MB (106674970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce19f72ba3efadcebf91b9628f9e85de500fcaa86b6ec8076169cc4bb312c0`  
		Last Modified: Thu, 16 Feb 2023 02:08:32 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4653b8562b98f6d770621adbd89d3392ed2c490da6c30dec79027c7e24ca6b`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (5026943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283f9c4ca607d846e0fc14dd248b106caf329d7c20316e59898b4a202459a77`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c525626770477530f07d56e4934dd0c036e55624d0182762d6df8afbc46aa99`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cda701c245116defdc445fe6ef3e38f73716d9f527f2876d1843abaef3ca11`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec7890747cf0e8bf22b460262ebe10c19f91d00c0710a010fbe2d48d81ca8f0`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.15-nanoserver-1809`

```console
$ docker pull nats@sha256:c180f2dccb457181af8c515978403a11167dcc1a60e490d49ce3bc48d5df44b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `nats:2.9.15-nanoserver-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:43348610453f5ecf2cb1eb6b88a459f7ad59353df14950ea55d72a27737f66af
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111708291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94392dbb17d455d1e80a3bc24798e3e1d761cbcd472f1616a352d0995335dbf0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Feb 2023 10:14:28 GMT
RUN Apply image 10.0.17763.4010
# Thu, 16 Feb 2023 02:07:44 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:19:54 GMT
RUN cmd /S /C #(nop) COPY file:c0761502e8e3e74fa63209f49b4d4f61a9c596c726f61d96e045d0b22538ada5 in C:\nats-server.exe 
# Thu, 02 Mar 2023 19:19:55 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:00eaf3341cd3cc6b72f91399cb3bd1aba30eb7eead7596532fe54c4bf1b010d7`  
		Last Modified: Thu, 16 Feb 2023 00:31:21 GMT  
		Size: 106.7 MB (106674970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce19f72ba3efadcebf91b9628f9e85de500fcaa86b6ec8076169cc4bb312c0`  
		Last Modified: Thu, 16 Feb 2023 02:08:32 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4653b8562b98f6d770621adbd89d3392ed2c490da6c30dec79027c7e24ca6b`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (5026943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283f9c4ca607d846e0fc14dd248b106caf329d7c20316e59898b4a202459a77`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c525626770477530f07d56e4934dd0c036e55624d0182762d6df8afbc46aa99`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cda701c245116defdc445fe6ef3e38f73716d9f527f2876d1843abaef3ca11`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec7890747cf0e8bf22b460262ebe10c19f91d00c0710a010fbe2d48d81ca8f0`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.15-scratch`

```console
$ docker pull nats@sha256:e9767cfa85287292db74b0533d910366598f93e18b3c60706cf1c25ab7f657be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.15-scratch` - linux; amd64

```console
$ docker pull nats@sha256:1a82b1b261d169994fc6162f2f25894a49e20971560f8b2dff4f90eefb32b421
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74665a2673c052e85d3417cec864d1aabab3263f3328051037a133d9b85765ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:32a9f093b76345e99bd81ff00eabc5ab1ae6c2bdc7d6c843c923049ea3c620ce in /nats-server 
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 19:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:20:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 19:20:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 19:20:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:436f213323b997ad7aca1675cce2c9a9366e3cd51995b9829835ab9762901f98`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (4972530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb98c93488e5f33bab9a8b331c5fbe988a9dd644e39cc15e6626550ec05e541`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.15-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e1ba487c56a25895759177de201768f40c51ceeedca983afa03875039445bb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60b5d45617b9109e120de34ac32b0647324dba3d69d2c56366545e50c2484c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:614e1182091dacdaa5043752e8239600bae8aa334cfd383cc326d1753d3eba64 in /nats-server 
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:49:36 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d859c106d4072b51eee7be282394c7f0c288186311ae904751cd95c3cf9468ae`  
		Last Modified: Thu, 02 Mar 2023 18:50:54 GMT  
		Size: 4.7 MB (4739343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e7000b41bf11d721897d126c1e72201203bcc8e9716daad77d7d42ae97853a`  
		Last Modified: Thu, 02 Mar 2023 18:50:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.15-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:644eac35d964521bc85286defaf1bae093b36618fe862eedff9a996e330fc60c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4731109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e814afeda8d92b2fb3dcdacf4648234504c6e4cd7fc24cce256cc588a439d7e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:a63786ae76c5e718a4952dd30b2265019e1ca48099ad19279d2e77e5ad704bfc in /nats-server 
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:57:50 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:57:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:57:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e714c80855fb90cb44f135a04bf323493a749536bb9106eb3ef4e69a70682897`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 4.7 MB (4730600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e020ba411c44ee7d23b6bdbd966700955c2d087afd3d79a9ad51e0390e8e7b6`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.15-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:35ef84ac5e9bb0d0229fb1a773677d6ee7b23bb58937427d20aaa36987562373
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4559479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f367536d7ef4331c52bf405914c6f7affdccdb8eed05fb4c981efe519fd06f00`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:23081283f9b4d8145ad2b3a276cc08fcb49c4850e322db9560525e495d1bf362 in /nats-server 
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:40:16 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:40:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:40:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:40:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a910efaa632bb8401dbca7cfe541f6dc4da71ea38708992ef153250254493114`  
		Last Modified: Thu, 02 Mar 2023 18:41:09 GMT  
		Size: 4.6 MB (4558972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be7fc9abf13897cf1a5e7026f6a49b3308d5a864640e1f4b6e526ee95f093fc`  
		Last Modified: Thu, 02 Mar 2023 18:41:08 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.15-windowsservercore`

```console
$ docker pull nats@sha256:6f1f4d7a55b14f4ef4ace0d86d512d62c86510fb3fc2e6235285dee00889deaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `nats:2.9.15-windowsservercore` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:1f57dd803e325796896529880709c0362fc7725ed025a1938061deae3c16926b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1968846299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc817364b97d6849687256fb1e283d68bec70f8fc8cf071fd8f6c3c50ab52b70`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Thu, 16 Feb 2023 00:42:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Feb 2023 02:04:44 GMT
ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:15:51 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 19:15:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.15/nats-server-v2.9.15-windows-amd64.zip
# Thu, 02 Mar 2023 19:15:53 GMT
ENV NATS_SERVER_SHASUM=090f5c310beeb94f603898c6940f2793c292b20c131e578967fc2cdbd01bd42a
# Thu, 02 Mar 2023 19:17:24 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Mar 2023 19:19:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Mar 2023 19:19:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:32 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531f6c3ad9784fc2870ea5ca08c4adccd9318602ed534d822e12b8b658a7b0b6`  
		Last Modified: Thu, 16 Feb 2023 01:37:30 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724509671085dbea52985b930945ecf6cb7694ecee9924bc0226a51a4e01d8a5`  
		Last Modified: Thu, 16 Feb 2023 02:08:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e3c3097c0a4a64935c2f4363011e3e5f02920d5a60f3c71bcbf747ba399daf`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70160f2cef619deb4f1c1bc53f46ee10a33db33dcc93ca0359df7f4191a3812`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600113a59a91ef36bca5a64b4f37eff2ea8dfc7a4e1c63e481009b3c4e5e1375`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64284e36d579640133af5182d567ba35684371aa3d2ebbf3765f442ab0acd3ca`  
		Last Modified: Thu, 02 Mar 2023 19:20:32 GMT  
		Size: 501.6 KB (501609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c0da48daccd70430c8b64cb1c57aff91648fdf57a29e3e747c1177b4b8302b`  
		Last Modified: Thu, 02 Mar 2023 19:20:30 GMT  
		Size: 5.4 MB (5373677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb96b758b91e4d2cfb8b02ed79af5fa5de692cbe61a0779831b75dec1b035e0b`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 2.0 KB (1994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ed891c87e5a2b154abfcbcafb6918c7aa542f2329ecc53362fe6d6708965fa`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae3f74335a8506b631d307e76d730bcbd5e1adaac877411aed88734555005e3`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b31fc962f6aeb0c4f712833073342f7a145a6843e633151eb95263e41ed874`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.15-windowsservercore-1809`

```console
$ docker pull nats@sha256:6f1f4d7a55b14f4ef4ace0d86d512d62c86510fb3fc2e6235285dee00889deaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `nats:2.9.15-windowsservercore-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:1f57dd803e325796896529880709c0362fc7725ed025a1938061deae3c16926b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1968846299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc817364b97d6849687256fb1e283d68bec70f8fc8cf071fd8f6c3c50ab52b70`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Thu, 16 Feb 2023 00:42:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Feb 2023 02:04:44 GMT
ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:15:51 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 19:15:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.15/nats-server-v2.9.15-windows-amd64.zip
# Thu, 02 Mar 2023 19:15:53 GMT
ENV NATS_SERVER_SHASUM=090f5c310beeb94f603898c6940f2793c292b20c131e578967fc2cdbd01bd42a
# Thu, 02 Mar 2023 19:17:24 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Mar 2023 19:19:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Mar 2023 19:19:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:32 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531f6c3ad9784fc2870ea5ca08c4adccd9318602ed534d822e12b8b658a7b0b6`  
		Last Modified: Thu, 16 Feb 2023 01:37:30 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724509671085dbea52985b930945ecf6cb7694ecee9924bc0226a51a4e01d8a5`  
		Last Modified: Thu, 16 Feb 2023 02:08:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e3c3097c0a4a64935c2f4363011e3e5f02920d5a60f3c71bcbf747ba399daf`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70160f2cef619deb4f1c1bc53f46ee10a33db33dcc93ca0359df7f4191a3812`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600113a59a91ef36bca5a64b4f37eff2ea8dfc7a4e1c63e481009b3c4e5e1375`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64284e36d579640133af5182d567ba35684371aa3d2ebbf3765f442ab0acd3ca`  
		Last Modified: Thu, 02 Mar 2023 19:20:32 GMT  
		Size: 501.6 KB (501609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c0da48daccd70430c8b64cb1c57aff91648fdf57a29e3e747c1177b4b8302b`  
		Last Modified: Thu, 02 Mar 2023 19:20:30 GMT  
		Size: 5.4 MB (5373677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb96b758b91e4d2cfb8b02ed79af5fa5de692cbe61a0779831b75dec1b035e0b`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 2.0 KB (1994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ed891c87e5a2b154abfcbcafb6918c7aa542f2329ecc53362fe6d6708965fa`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae3f74335a8506b631d307e76d730bcbd5e1adaac877411aed88734555005e3`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b31fc962f6aeb0c4f712833073342f7a145a6843e633151eb95263e41ed874`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:f2f2b0e23c7f9fd142e4882d4f4c1cc9c3a6efb17d23b8b16c837d79ff59ca84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:9947eac2dedc476378d9cac73c7df6cba2f1a23da12137214cdc254a15863a46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8635785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d6b3fd56dc8fe20a6e41de4afeacff348a53e1ab388f535f404e9cf74c084d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 19:19:49 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 19:19:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 19:19:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 19:19:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 19:19:52 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:19:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08472afe1eaab0ac7a92349d2da3b64cafacc125426338b278e2fc3b006bd52`  
		Last Modified: Thu, 02 Mar 2023 19:20:25 GMT  
		Size: 5.3 MB (5260338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5ae32cc4383cc8cabea2eba8667d1ff1aaa9bf699469141395387df31c5c4b`  
		Last Modified: Thu, 02 Mar 2023 19:20:24 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3f805284c458c477cde0410e2f6835ab92c5fd6b464cfd6c07cf3d52643c23`  
		Last Modified: Thu, 02 Mar 2023 19:20:24 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d7d52fa58f1f77d24ded7e34e2be977eb4474da0ae5e81639e144de15e0c9bf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8135732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4abf0b19eb2e841ac4255d1702b59ec4fb05a30e60561a5cfd8efcd2c8e4b24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:49:28 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:49:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:49:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:49:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:49:31 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:49:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2d8c7c008839e4297490fe62726b0511bb9a7c6486b7f97b106788aa11c6f8`  
		Last Modified: Thu, 02 Mar 2023 18:50:25 GMT  
		Size: 5.0 MB (5023847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8437de52ce6ce410d6359afa18a00cc025d2f5846e854d4b4e398f9eb16ce1c5`  
		Last Modified: Thu, 02 Mar 2023 18:50:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98d271690d33766c10fca8cfd7d844162956eb2db3195e9bf3e21ed587c7f60`  
		Last Modified: Thu, 02 Mar 2023 18:50:24 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d0f535bd276e1b92c60c9b8fe33cb90d439049071159843142c026302b54bf7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7887576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b405c7e2612cb810f225540c61a3eb1f02c1efbb3910aa30aa7b46b068fef2db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:31 GMT
ADD file:143b601fcc6b5d7d95d3e5ccad3fec7081191a47e28d4f9294a7fb2499cab1af in / 
# Fri, 10 Feb 2023 21:51:31 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:57:36 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:57:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:57:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:57:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:57:39 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:57:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6fb81ff47bd6d7db0ed86c9b951ad6417ec73ab60af6d22daa604076a902629c`  
		Last Modified: Fri, 10 Feb 2023 21:52:33 GMT  
		Size: 2.9 MB (2868494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19b56339a1ba27c396a17554216f8da9ef664a78ec52c24c39630ad6b00ccea`  
		Last Modified: Thu, 02 Mar 2023 18:58:37 GMT  
		Size: 5.0 MB (5018081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6919af5eaed170352d5fcbc4a52cdfd188a277c02b8c39538f0626a12afc6e`  
		Last Modified: Thu, 02 Mar 2023 18:58:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99bb0ebd369abc6e32fcdbdbade73f2a1504cb8edae42327051d1343b982a8b`  
		Last Modified: Thu, 02 Mar 2023 18:58:36 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:31516678d6c3c1c5d7444e85d06618022258cfb3a23bbed0e44a358bbf7fea1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8104002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f18af0a035256392dde53a51a48628b107ebad3b4b6627160aaab7a964ce40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:39:45 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:39:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:39:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:39:47 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:39:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f03396fa041b5be75e5a939ff3aadaff2e65f529a07bcbd4748b581e3e193e1`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 4.8 MB (4841045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cceddcd111b1a86e5348af7dccf8c0b0d1c1dfec305c026bd9351bd0d1cce7`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca183fb542756060f50207e2bdac939b035a4f4ff2075b0371f87399242950a2`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.17`

```console
$ docker pull nats@sha256:f2f2b0e23c7f9fd142e4882d4f4c1cc9c3a6efb17d23b8b16c837d79ff59ca84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.17` - linux; amd64

```console
$ docker pull nats@sha256:9947eac2dedc476378d9cac73c7df6cba2f1a23da12137214cdc254a15863a46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8635785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d6b3fd56dc8fe20a6e41de4afeacff348a53e1ab388f535f404e9cf74c084d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 19:19:49 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 19:19:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 19:19:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 19:19:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 19:19:52 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:19:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08472afe1eaab0ac7a92349d2da3b64cafacc125426338b278e2fc3b006bd52`  
		Last Modified: Thu, 02 Mar 2023 19:20:25 GMT  
		Size: 5.3 MB (5260338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5ae32cc4383cc8cabea2eba8667d1ff1aaa9bf699469141395387df31c5c4b`  
		Last Modified: Thu, 02 Mar 2023 19:20:24 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3f805284c458c477cde0410e2f6835ab92c5fd6b464cfd6c07cf3d52643c23`  
		Last Modified: Thu, 02 Mar 2023 19:20:24 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.17` - linux; arm variant v6

```console
$ docker pull nats@sha256:d7d52fa58f1f77d24ded7e34e2be977eb4474da0ae5e81639e144de15e0c9bf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8135732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4abf0b19eb2e841ac4255d1702b59ec4fb05a30e60561a5cfd8efcd2c8e4b24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:49:28 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:49:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:49:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:49:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:49:31 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:49:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2d8c7c008839e4297490fe62726b0511bb9a7c6486b7f97b106788aa11c6f8`  
		Last Modified: Thu, 02 Mar 2023 18:50:25 GMT  
		Size: 5.0 MB (5023847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8437de52ce6ce410d6359afa18a00cc025d2f5846e854d4b4e398f9eb16ce1c5`  
		Last Modified: Thu, 02 Mar 2023 18:50:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98d271690d33766c10fca8cfd7d844162956eb2db3195e9bf3e21ed587c7f60`  
		Last Modified: Thu, 02 Mar 2023 18:50:24 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.17` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d0f535bd276e1b92c60c9b8fe33cb90d439049071159843142c026302b54bf7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7887576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b405c7e2612cb810f225540c61a3eb1f02c1efbb3910aa30aa7b46b068fef2db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:31 GMT
ADD file:143b601fcc6b5d7d95d3e5ccad3fec7081191a47e28d4f9294a7fb2499cab1af in / 
# Fri, 10 Feb 2023 21:51:31 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:57:36 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:57:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:57:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:57:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:57:39 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:57:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6fb81ff47bd6d7db0ed86c9b951ad6417ec73ab60af6d22daa604076a902629c`  
		Last Modified: Fri, 10 Feb 2023 21:52:33 GMT  
		Size: 2.9 MB (2868494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19b56339a1ba27c396a17554216f8da9ef664a78ec52c24c39630ad6b00ccea`  
		Last Modified: Thu, 02 Mar 2023 18:58:37 GMT  
		Size: 5.0 MB (5018081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6919af5eaed170352d5fcbc4a52cdfd188a277c02b8c39538f0626a12afc6e`  
		Last Modified: Thu, 02 Mar 2023 18:58:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99bb0ebd369abc6e32fcdbdbade73f2a1504cb8edae42327051d1343b982a8b`  
		Last Modified: Thu, 02 Mar 2023 18:58:36 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.17` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:31516678d6c3c1c5d7444e85d06618022258cfb3a23bbed0e44a358bbf7fea1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8104002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f18af0a035256392dde53a51a48628b107ebad3b4b6627160aaab7a964ce40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 18:39:45 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 18:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Mar 2023 18:39:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 02 Mar 2023 18:39:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Mar 2023 18:39:47 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 18:39:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f03396fa041b5be75e5a939ff3aadaff2e65f529a07bcbd4748b581e3e193e1`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 4.8 MB (4841045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cceddcd111b1a86e5348af7dccf8c0b0d1c1dfec305c026bd9351bd0d1cce7`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca183fb542756060f50207e2bdac939b035a4f4ff2075b0371f87399242950a2`  
		Last Modified: Thu, 02 Mar 2023 18:40:46 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:04fcc71e7d416348e8761b4081931d735d3774f5b14d33b724cc6caad6037893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4010; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:1a82b1b261d169994fc6162f2f25894a49e20971560f8b2dff4f90eefb32b421
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74665a2673c052e85d3417cec864d1aabab3263f3328051037a133d9b85765ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:32a9f093b76345e99bd81ff00eabc5ab1ae6c2bdc7d6c843c923049ea3c620ce in /nats-server 
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 19:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:20:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 19:20:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 19:20:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:436f213323b997ad7aca1675cce2c9a9366e3cd51995b9829835ab9762901f98`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (4972530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb98c93488e5f33bab9a8b331c5fbe988a9dd644e39cc15e6626550ec05e541`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e1ba487c56a25895759177de201768f40c51ceeedca983afa03875039445bb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60b5d45617b9109e120de34ac32b0647324dba3d69d2c56366545e50c2484c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:614e1182091dacdaa5043752e8239600bae8aa334cfd383cc326d1753d3eba64 in /nats-server 
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:49:36 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d859c106d4072b51eee7be282394c7f0c288186311ae904751cd95c3cf9468ae`  
		Last Modified: Thu, 02 Mar 2023 18:50:54 GMT  
		Size: 4.7 MB (4739343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e7000b41bf11d721897d126c1e72201203bcc8e9716daad77d7d42ae97853a`  
		Last Modified: Thu, 02 Mar 2023 18:50:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:644eac35d964521bc85286defaf1bae093b36618fe862eedff9a996e330fc60c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4731109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e814afeda8d92b2fb3dcdacf4648234504c6e4cd7fc24cce256cc588a439d7e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:a63786ae76c5e718a4952dd30b2265019e1ca48099ad19279d2e77e5ad704bfc in /nats-server 
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:57:50 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:57:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:57:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e714c80855fb90cb44f135a04bf323493a749536bb9106eb3ef4e69a70682897`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 4.7 MB (4730600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e020ba411c44ee7d23b6bdbd966700955c2d087afd3d79a9ad51e0390e8e7b6`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:35ef84ac5e9bb0d0229fb1a773677d6ee7b23bb58937427d20aaa36987562373
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4559479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f367536d7ef4331c52bf405914c6f7affdccdb8eed05fb4c981efe519fd06f00`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:23081283f9b4d8145ad2b3a276cc08fcb49c4850e322db9560525e495d1bf362 in /nats-server 
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:40:16 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:40:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:40:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:40:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a910efaa632bb8401dbca7cfe541f6dc4da71ea38708992ef153250254493114`  
		Last Modified: Thu, 02 Mar 2023 18:41:09 GMT  
		Size: 4.6 MB (4558972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be7fc9abf13897cf1a5e7026f6a49b3308d5a864640e1f4b6e526ee95f093fc`  
		Last Modified: Thu, 02 Mar 2023 18:41:08 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:43348610453f5ecf2cb1eb6b88a459f7ad59353df14950ea55d72a27737f66af
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111708291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94392dbb17d455d1e80a3bc24798e3e1d761cbcd472f1616a352d0995335dbf0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Feb 2023 10:14:28 GMT
RUN Apply image 10.0.17763.4010
# Thu, 16 Feb 2023 02:07:44 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:19:54 GMT
RUN cmd /S /C #(nop) COPY file:c0761502e8e3e74fa63209f49b4d4f61a9c596c726f61d96e045d0b22538ada5 in C:\nats-server.exe 
# Thu, 02 Mar 2023 19:19:55 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:00eaf3341cd3cc6b72f91399cb3bd1aba30eb7eead7596532fe54c4bf1b010d7`  
		Last Modified: Thu, 16 Feb 2023 00:31:21 GMT  
		Size: 106.7 MB (106674970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce19f72ba3efadcebf91b9628f9e85de500fcaa86b6ec8076169cc4bb312c0`  
		Last Modified: Thu, 16 Feb 2023 02:08:32 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4653b8562b98f6d770621adbd89d3392ed2c490da6c30dec79027c7e24ca6b`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (5026943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283f9c4ca607d846e0fc14dd248b106caf329d7c20316e59898b4a202459a77`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c525626770477530f07d56e4934dd0c036e55624d0182762d6df8afbc46aa99`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cda701c245116defdc445fe6ef3e38f73716d9f527f2876d1843abaef3ca11`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec7890747cf0e8bf22b460262ebe10c19f91d00c0710a010fbe2d48d81ca8f0`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:e9767cfa85287292db74b0533d910366598f93e18b3c60706cf1c25ab7f657be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:1a82b1b261d169994fc6162f2f25894a49e20971560f8b2dff4f90eefb32b421
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74665a2673c052e85d3417cec864d1aabab3263f3328051037a133d9b85765ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:32a9f093b76345e99bd81ff00eabc5ab1ae6c2bdc7d6c843c923049ea3c620ce in /nats-server 
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 19:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:20:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 19:20:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 19:20:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:436f213323b997ad7aca1675cce2c9a9366e3cd51995b9829835ab9762901f98`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (4972530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb98c93488e5f33bab9a8b331c5fbe988a9dd644e39cc15e6626550ec05e541`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e1ba487c56a25895759177de201768f40c51ceeedca983afa03875039445bb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60b5d45617b9109e120de34ac32b0647324dba3d69d2c56366545e50c2484c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:614e1182091dacdaa5043752e8239600bae8aa334cfd383cc326d1753d3eba64 in /nats-server 
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:49:36 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d859c106d4072b51eee7be282394c7f0c288186311ae904751cd95c3cf9468ae`  
		Last Modified: Thu, 02 Mar 2023 18:50:54 GMT  
		Size: 4.7 MB (4739343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e7000b41bf11d721897d126c1e72201203bcc8e9716daad77d7d42ae97853a`  
		Last Modified: Thu, 02 Mar 2023 18:50:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:644eac35d964521bc85286defaf1bae093b36618fe862eedff9a996e330fc60c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4731109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e814afeda8d92b2fb3dcdacf4648234504c6e4cd7fc24cce256cc588a439d7e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:a63786ae76c5e718a4952dd30b2265019e1ca48099ad19279d2e77e5ad704bfc in /nats-server 
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:57:50 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:57:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:57:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e714c80855fb90cb44f135a04bf323493a749536bb9106eb3ef4e69a70682897`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 4.7 MB (4730600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e020ba411c44ee7d23b6bdbd966700955c2d087afd3d79a9ad51e0390e8e7b6`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:35ef84ac5e9bb0d0229fb1a773677d6ee7b23bb58937427d20aaa36987562373
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4559479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f367536d7ef4331c52bf405914c6f7affdccdb8eed05fb4c981efe519fd06f00`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:23081283f9b4d8145ad2b3a276cc08fcb49c4850e322db9560525e495d1bf362 in /nats-server 
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:40:16 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:40:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:40:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:40:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a910efaa632bb8401dbca7cfe541f6dc4da71ea38708992ef153250254493114`  
		Last Modified: Thu, 02 Mar 2023 18:41:09 GMT  
		Size: 4.6 MB (4558972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be7fc9abf13897cf1a5e7026f6a49b3308d5a864640e1f4b6e526ee95f093fc`  
		Last Modified: Thu, 02 Mar 2023 18:41:08 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:c180f2dccb457181af8c515978403a11167dcc1a60e490d49ce3bc48d5df44b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `nats:nanoserver` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:43348610453f5ecf2cb1eb6b88a459f7ad59353df14950ea55d72a27737f66af
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111708291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94392dbb17d455d1e80a3bc24798e3e1d761cbcd472f1616a352d0995335dbf0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Feb 2023 10:14:28 GMT
RUN Apply image 10.0.17763.4010
# Thu, 16 Feb 2023 02:07:44 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:19:54 GMT
RUN cmd /S /C #(nop) COPY file:c0761502e8e3e74fa63209f49b4d4f61a9c596c726f61d96e045d0b22538ada5 in C:\nats-server.exe 
# Thu, 02 Mar 2023 19:19:55 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:00eaf3341cd3cc6b72f91399cb3bd1aba30eb7eead7596532fe54c4bf1b010d7`  
		Last Modified: Thu, 16 Feb 2023 00:31:21 GMT  
		Size: 106.7 MB (106674970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce19f72ba3efadcebf91b9628f9e85de500fcaa86b6ec8076169cc4bb312c0`  
		Last Modified: Thu, 16 Feb 2023 02:08:32 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4653b8562b98f6d770621adbd89d3392ed2c490da6c30dec79027c7e24ca6b`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (5026943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283f9c4ca607d846e0fc14dd248b106caf329d7c20316e59898b4a202459a77`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c525626770477530f07d56e4934dd0c036e55624d0182762d6df8afbc46aa99`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cda701c245116defdc445fe6ef3e38f73716d9f527f2876d1843abaef3ca11`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec7890747cf0e8bf22b460262ebe10c19f91d00c0710a010fbe2d48d81ca8f0`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:c180f2dccb457181af8c515978403a11167dcc1a60e490d49ce3bc48d5df44b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:43348610453f5ecf2cb1eb6b88a459f7ad59353df14950ea55d72a27737f66af
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111708291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94392dbb17d455d1e80a3bc24798e3e1d761cbcd472f1616a352d0995335dbf0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Feb 2023 10:14:28 GMT
RUN Apply image 10.0.17763.4010
# Thu, 16 Feb 2023 02:07:44 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:19:54 GMT
RUN cmd /S /C #(nop) COPY file:c0761502e8e3e74fa63209f49b4d4f61a9c596c726f61d96e045d0b22538ada5 in C:\nats-server.exe 
# Thu, 02 Mar 2023 19:19:55 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:00eaf3341cd3cc6b72f91399cb3bd1aba30eb7eead7596532fe54c4bf1b010d7`  
		Last Modified: Thu, 16 Feb 2023 00:31:21 GMT  
		Size: 106.7 MB (106674970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce19f72ba3efadcebf91b9628f9e85de500fcaa86b6ec8076169cc4bb312c0`  
		Last Modified: Thu, 16 Feb 2023 02:08:32 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4653b8562b98f6d770621adbd89d3392ed2c490da6c30dec79027c7e24ca6b`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (5026943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283f9c4ca607d846e0fc14dd248b106caf329d7c20316e59898b4a202459a77`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c525626770477530f07d56e4934dd0c036e55624d0182762d6df8afbc46aa99`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cda701c245116defdc445fe6ef3e38f73716d9f527f2876d1843abaef3ca11`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec7890747cf0e8bf22b460262ebe10c19f91d00c0710a010fbe2d48d81ca8f0`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:e9767cfa85287292db74b0533d910366598f93e18b3c60706cf1c25ab7f657be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:1a82b1b261d169994fc6162f2f25894a49e20971560f8b2dff4f90eefb32b421
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74665a2673c052e85d3417cec864d1aabab3263f3328051037a133d9b85765ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:32a9f093b76345e99bd81ff00eabc5ab1ae6c2bdc7d6c843c923049ea3c620ce in /nats-server 
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 19:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:20:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 19:20:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 19:20:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:436f213323b997ad7aca1675cce2c9a9366e3cd51995b9829835ab9762901f98`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (4972530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb98c93488e5f33bab9a8b331c5fbe988a9dd644e39cc15e6626550ec05e541`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e1ba487c56a25895759177de201768f40c51ceeedca983afa03875039445bb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60b5d45617b9109e120de34ac32b0647324dba3d69d2c56366545e50c2484c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:614e1182091dacdaa5043752e8239600bae8aa334cfd383cc326d1753d3eba64 in /nats-server 
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:49:36 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d859c106d4072b51eee7be282394c7f0c288186311ae904751cd95c3cf9468ae`  
		Last Modified: Thu, 02 Mar 2023 18:50:54 GMT  
		Size: 4.7 MB (4739343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e7000b41bf11d721897d126c1e72201203bcc8e9716daad77d7d42ae97853a`  
		Last Modified: Thu, 02 Mar 2023 18:50:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:644eac35d964521bc85286defaf1bae093b36618fe862eedff9a996e330fc60c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4731109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e814afeda8d92b2fb3dcdacf4648234504c6e4cd7fc24cce256cc588a439d7e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:a63786ae76c5e718a4952dd30b2265019e1ca48099ad19279d2e77e5ad704bfc in /nats-server 
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:57:50 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:57:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:57:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e714c80855fb90cb44f135a04bf323493a749536bb9106eb3ef4e69a70682897`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 4.7 MB (4730600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e020ba411c44ee7d23b6bdbd966700955c2d087afd3d79a9ad51e0390e8e7b6`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:35ef84ac5e9bb0d0229fb1a773677d6ee7b23bb58937427d20aaa36987562373
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4559479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f367536d7ef4331c52bf405914c6f7affdccdb8eed05fb4c981efe519fd06f00`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:23081283f9b4d8145ad2b3a276cc08fcb49c4850e322db9560525e495d1bf362 in /nats-server 
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:40:16 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:40:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:40:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:40:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a910efaa632bb8401dbca7cfe541f6dc4da71ea38708992ef153250254493114`  
		Last Modified: Thu, 02 Mar 2023 18:41:09 GMT  
		Size: 4.6 MB (4558972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be7fc9abf13897cf1a5e7026f6a49b3308d5a864640e1f4b6e526ee95f093fc`  
		Last Modified: Thu, 02 Mar 2023 18:41:08 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:6f1f4d7a55b14f4ef4ace0d86d512d62c86510fb3fc2e6235285dee00889deaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `nats:windowsservercore` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:1f57dd803e325796896529880709c0362fc7725ed025a1938061deae3c16926b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1968846299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc817364b97d6849687256fb1e283d68bec70f8fc8cf071fd8f6c3c50ab52b70`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Thu, 16 Feb 2023 00:42:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Feb 2023 02:04:44 GMT
ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:15:51 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 19:15:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.15/nats-server-v2.9.15-windows-amd64.zip
# Thu, 02 Mar 2023 19:15:53 GMT
ENV NATS_SERVER_SHASUM=090f5c310beeb94f603898c6940f2793c292b20c131e578967fc2cdbd01bd42a
# Thu, 02 Mar 2023 19:17:24 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Mar 2023 19:19:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Mar 2023 19:19:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:32 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531f6c3ad9784fc2870ea5ca08c4adccd9318602ed534d822e12b8b658a7b0b6`  
		Last Modified: Thu, 16 Feb 2023 01:37:30 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724509671085dbea52985b930945ecf6cb7694ecee9924bc0226a51a4e01d8a5`  
		Last Modified: Thu, 16 Feb 2023 02:08:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e3c3097c0a4a64935c2f4363011e3e5f02920d5a60f3c71bcbf747ba399daf`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70160f2cef619deb4f1c1bc53f46ee10a33db33dcc93ca0359df7f4191a3812`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600113a59a91ef36bca5a64b4f37eff2ea8dfc7a4e1c63e481009b3c4e5e1375`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64284e36d579640133af5182d567ba35684371aa3d2ebbf3765f442ab0acd3ca`  
		Last Modified: Thu, 02 Mar 2023 19:20:32 GMT  
		Size: 501.6 KB (501609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c0da48daccd70430c8b64cb1c57aff91648fdf57a29e3e747c1177b4b8302b`  
		Last Modified: Thu, 02 Mar 2023 19:20:30 GMT  
		Size: 5.4 MB (5373677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb96b758b91e4d2cfb8b02ed79af5fa5de692cbe61a0779831b75dec1b035e0b`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 2.0 KB (1994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ed891c87e5a2b154abfcbcafb6918c7aa542f2329ecc53362fe6d6708965fa`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae3f74335a8506b631d307e76d730bcbd5e1adaac877411aed88734555005e3`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b31fc962f6aeb0c4f712833073342f7a145a6843e633151eb95263e41ed874`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:6f1f4d7a55b14f4ef4ace0d86d512d62c86510fb3fc2e6235285dee00889deaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:1f57dd803e325796896529880709c0362fc7725ed025a1938061deae3c16926b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1968846299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc817364b97d6849687256fb1e283d68bec70f8fc8cf071fd8f6c3c50ab52b70`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Thu, 16 Feb 2023 00:42:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Feb 2023 02:04:44 GMT
ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:15:51 GMT
ENV NATS_SERVER=2.9.15
# Thu, 02 Mar 2023 19:15:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.15/nats-server-v2.9.15-windows-amd64.zip
# Thu, 02 Mar 2023 19:15:53 GMT
ENV NATS_SERVER_SHASUM=090f5c310beeb94f603898c6940f2793c292b20c131e578967fc2cdbd01bd42a
# Thu, 02 Mar 2023 19:17:24 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Mar 2023 19:19:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Mar 2023 19:19:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:32 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531f6c3ad9784fc2870ea5ca08c4adccd9318602ed534d822e12b8b658a7b0b6`  
		Last Modified: Thu, 16 Feb 2023 01:37:30 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724509671085dbea52985b930945ecf6cb7694ecee9924bc0226a51a4e01d8a5`  
		Last Modified: Thu, 16 Feb 2023 02:08:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e3c3097c0a4a64935c2f4363011e3e5f02920d5a60f3c71bcbf747ba399daf`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70160f2cef619deb4f1c1bc53f46ee10a33db33dcc93ca0359df7f4191a3812`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600113a59a91ef36bca5a64b4f37eff2ea8dfc7a4e1c63e481009b3c4e5e1375`  
		Last Modified: Thu, 02 Mar 2023 19:20:31 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64284e36d579640133af5182d567ba35684371aa3d2ebbf3765f442ab0acd3ca`  
		Last Modified: Thu, 02 Mar 2023 19:20:32 GMT  
		Size: 501.6 KB (501609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c0da48daccd70430c8b64cb1c57aff91648fdf57a29e3e747c1177b4b8302b`  
		Last Modified: Thu, 02 Mar 2023 19:20:30 GMT  
		Size: 5.4 MB (5373677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb96b758b91e4d2cfb8b02ed79af5fa5de692cbe61a0779831b75dec1b035e0b`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 2.0 KB (1994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ed891c87e5a2b154abfcbcafb6918c7aa542f2329ecc53362fe6d6708965fa`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae3f74335a8506b631d307e76d730bcbd5e1adaac877411aed88734555005e3`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b31fc962f6aeb0c4f712833073342f7a145a6843e633151eb95263e41ed874`  
		Last Modified: Thu, 02 Mar 2023 19:20:29 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

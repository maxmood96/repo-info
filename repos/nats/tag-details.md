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
-	[`nats:2.7`](#nats27)
-	[`nats:2.7-alpine`](#nats27-alpine)
-	[`nats:2.7-alpine3.15`](#nats27-alpine315)
-	[`nats:2.7-linux`](#nats27-linux)
-	[`nats:2.7-nanoserver`](#nats27-nanoserver)
-	[`nats:2.7-nanoserver-1809`](#nats27-nanoserver-1809)
-	[`nats:2.7-scratch`](#nats27-scratch)
-	[`nats:2.7-windowsservercore`](#nats27-windowsservercore)
-	[`nats:2.7-windowsservercore-1809`](#nats27-windowsservercore-1809)
-	[`nats:2.7.0`](#nats270)
-	[`nats:2.7.0-alpine`](#nats270-alpine)
-	[`nats:2.7.0-alpine3.15`](#nats270-alpine315)
-	[`nats:2.7.0-linux`](#nats270-linux)
-	[`nats:2.7.0-nanoserver`](#nats270-nanoserver)
-	[`nats:2.7.0-nanoserver-1809`](#nats270-nanoserver-1809)
-	[`nats:2.7.0-scratch`](#nats270-scratch)
-	[`nats:2.7.0-windowsservercore`](#nats270-windowsservercore)
-	[`nats:2.7.0-windowsservercore-1809`](#nats270-windowsservercore-1809)
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
$ docker pull nats@sha256:08f87dbef4702c335b595c22a60955eda795d9dc2059dc6d5d1692e10f84379a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2452; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:b06db068fc05ac9f5c7e8ffc4dce11c880f881a04e0eb40ba835861cec37a7e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a534d8f4e2dc469a50383ab63dfa8e3c1e357e5f0dfa3d5de92592ed4e448864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:24:10 GMT
COPY file:4f0ebc4704f83777a3960e581d523bc013bb02a0cfb7e7f786516a6c49942e22 in /nats-server 
# Fri, 14 Jan 2022 18:24:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:24:11 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:24:11 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:24:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a98137475bb500ddd9f8416278069548db1131298356240d97df07b35a68f05e`  
		Last Modified: Fri, 14 Jan 2022 18:25:51 GMT  
		Size: 4.5 MB (4465555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866493868b198566f99c644afee3c392ed1225753255779f01c03c2bcf9bf89`  
		Last Modified: Fri, 14 Jan 2022 18:25:50 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:5548af7da41d68083d376352f0043468c1d3392b3ee8cf270074e41efdb7daf4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a6ba83aa0c651bc6443b87ad3aa75aa05a49015c60b0ba94433ed283182e9d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:54:41 GMT
COPY file:0bc79db49bf07145ed2820c48ab480154ad0fe7624645e978e1ab085987118ab in /nats-server 
# Fri, 14 Jan 2022 18:54:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:54:42 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:43 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:54:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1753283a9fe04770710f582c7edb68af20fff43cb6750b511b88edba870b6b0a`  
		Last Modified: Fri, 14 Jan 2022 18:57:08 GMT  
		Size: 4.1 MB (4130524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6144f16900b7c63ff5f07e50d96706eca97e1b1e9be9f15abbf3ba87d5727372`  
		Last Modified: Fri, 14 Jan 2022 18:57:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:bddc83bad582414e836c7e60fdf5658dabef500b7bc51fb8e18d6247e47f179c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3b7221c7fd3e3c292d74b2b00e056a887bf2fc9e0400f840107de9cca1dfd5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:58:28 GMT
COPY file:c678b429005ddd760afff9930c36320b6468ea514443a740c99ed69f0d9cd889 in /nats-server 
# Fri, 14 Jan 2022 18:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:58:29 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:58:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a42706d8cfe08c4bc9bc324ffc2e0f4757dd092aaaf7dfdb7a98124df24cde2b`  
		Last Modified: Fri, 14 Jan 2022 19:00:55 GMT  
		Size: 4.1 MB (4126980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4780c44069007ad60d46f2985dbe0e7eae3a04d7df9936f14a70b825ec84e73e`  
		Last Modified: Fri, 14 Jan 2022 19:00:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6404671cd360e397c582b0903bccde0c5ef78c3365c1515c184cf4c3465d06dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15eb321439fe02848e980c416856500b3d8a264944878381ad8ffd1aa1f00e79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:42:45 GMT
COPY file:35de8b46fa873fa93035ad9e0bd8add902aeeb3f777acb6477fe8ae33621069f in /nats-server 
# Fri, 14 Jan 2022 18:42:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:42:46 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:47 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:42:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:99635f3a9fe15a08eb7778c1228079183c996b57cbae1adb68626045408c36c0`  
		Last Modified: Fri, 14 Jan 2022 18:44:02 GMT  
		Size: 4.1 MB (4113430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c443fa2d7386b32c85a9d5d54923637c8b533da17f0755a42f2c3d16ac59b1f8`  
		Last Modified: Fri, 14 Jan 2022 18:44:01 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:3ff2f0040a64a2cf0a020c4eb0425d13237737b34ecbd6a71b3b32c605bf55c2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107546942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e123bd94ced8bc2f98dc409ee61a0d185c740b720cbdce2ddfdbee78ca5ed5e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 15:13:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:18:56 GMT
RUN cmd /S /C #(nop) COPY file:76b3d6cbfb5183e43d9331cddd3a7f906364b8f5f8f8290ae121e47be5ed179c in C:\nats-server.exe 
# Fri, 14 Jan 2022 18:18:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:19:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:19:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db05d2e76671d91772a070867bf6f050343319070602a0f8239706d5d4d98387`  
		Last Modified: Wed, 12 Jan 2022 15:14:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc49f734ff1c4186abb068d17466f00a620f7903745063b3cc8ccb9492056b1`  
		Last Modified: Fri, 14 Jan 2022 18:19:52 GMT  
		Size: 4.5 MB (4509480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8029445e0be8d33827e442dd586388ee37afb157556c5075c892d3ec04b51b4a`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee34369f11e6432c63a08a695b26eec114e7f590e3e8db49e6ff3c9c6bc69dc`  
		Last Modified: Fri, 14 Jan 2022 18:19:50 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e6014d55a66a18b9b23e3a9d224307e4e729b2131ab80e5d94fe591092f6ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c431522fbf1e1f293b432240df83b2be82c117965a01a88ac9d4f6ce8904569`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:86f63911d02c7d05e6c62592a784679b1f9cb74b60d10c6c4b4d84bdf773b8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:9d6193c3f8c966a9fd387d258cbfceb3200dc155e5f1a96f6694d4e32215a256
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7569415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b06173b70b1d7bc01311e68328c369c3aba532201c604f9c3f0448368fc71a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:23:38 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:23:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:23:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:23:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:23:41 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:23:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e250c9fddf0251b9995287f56761bb006e4f275b872349f80eb59756e8362097`  
		Last Modified: Fri, 14 Jan 2022 18:24:46 GMT  
		Size: 4.8 MB (4750002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3370d34129abaa0cf5ea03a4de6b432c98e961247e0db58152afef624d5116b6`  
		Last Modified: Fri, 14 Jan 2022 18:24:45 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e699db775f306d056ba3491ef1a78bd60f43f6d84ca190dd5556ab952670bd37`  
		Last Modified: Fri, 14 Jan 2022 18:24:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:9a3ef866b8c56865ef170349f9b6c96434c59b83c8bd00434ac2ba069aa4d1c7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7049035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe56fe3b27ad5f693e36b857dd1234ada2657a84c9066653b1ff0789f912fbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:54:13 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:54:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:54:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:54:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:54:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32aa97c3aebf0246aa45096afee59b2568a296682d22adefa585ddfab52017e1`  
		Last Modified: Fri, 14 Jan 2022 18:56:29 GMT  
		Size: 4.4 MB (4416614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f48d8423c0fa6eb844a29d92e258ae9a33aa6e6cd0b95b4b69a21e72a8e567`  
		Last Modified: Fri, 14 Jan 2022 18:56:27 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8f267cce64b19b253599578af343c8bdcdc79f689ec7d92f4bec4f822e7412`  
		Last Modified: Fri, 14 Jan 2022 18:56:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:d2013f3c37f60a2f02029ff0ed712f0479ef409c7cae118a1ae0521f9a08d2bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6844582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ca3b8a166d5dd0ed044d2e85cc20e4795344ac64a28e513b00faa630c84882`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:57:58 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:58:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:58:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:58:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:58:03 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:58:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07275e3fb0a7b967b5381c0e07db89c39d1cf4e7ee0a649d1c009e78a1d42fa`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 4.4 MB (4408818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835acb2136974c88d21e7071bad202e0d0e39db27d2f0f944858311a7e80f9b4`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1452ec30e6ef252b617a9d46cbd566d7eba05df01f47c577c0d25daaf6d22c`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a1d2244a63e3ab81295587aaae2262e796174a4fa8687a8c872a4442973f50ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7112096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57981de17d5ffc0d33e96bee5e34398ecf77b8501362fca71a6e674fc061594`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:42:28 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:42:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:42:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:42:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:42:33 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:42:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccbd6fe265a7e2fbeca62a169f7f0cb64925946674670bc265127450e775009`  
		Last Modified: Fri, 14 Jan 2022 18:43:34 GMT  
		Size: 4.4 MB (4395688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7772805886c77ac22f41f9354d7d92334e4af6d9404544ee286084143a4c44e`  
		Last Modified: Fri, 14 Jan 2022 18:43:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567aec11ea3ca34811b7531dd4a2d7680c6dd5a7c649133b735ce4517d926f0`  
		Last Modified: Fri, 14 Jan 2022 18:43:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.15`

```console
$ docker pull nats@sha256:86f63911d02c7d05e6c62592a784679b1f9cb74b60d10c6c4b4d84bdf773b8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:9d6193c3f8c966a9fd387d258cbfceb3200dc155e5f1a96f6694d4e32215a256
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7569415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b06173b70b1d7bc01311e68328c369c3aba532201c604f9c3f0448368fc71a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:23:38 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:23:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:23:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:23:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:23:41 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:23:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e250c9fddf0251b9995287f56761bb006e4f275b872349f80eb59756e8362097`  
		Last Modified: Fri, 14 Jan 2022 18:24:46 GMT  
		Size: 4.8 MB (4750002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3370d34129abaa0cf5ea03a4de6b432c98e961247e0db58152afef624d5116b6`  
		Last Modified: Fri, 14 Jan 2022 18:24:45 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e699db775f306d056ba3491ef1a78bd60f43f6d84ca190dd5556ab952670bd37`  
		Last Modified: Fri, 14 Jan 2022 18:24:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:9a3ef866b8c56865ef170349f9b6c96434c59b83c8bd00434ac2ba069aa4d1c7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7049035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe56fe3b27ad5f693e36b857dd1234ada2657a84c9066653b1ff0789f912fbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:54:13 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:54:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:54:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:54:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:54:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32aa97c3aebf0246aa45096afee59b2568a296682d22adefa585ddfab52017e1`  
		Last Modified: Fri, 14 Jan 2022 18:56:29 GMT  
		Size: 4.4 MB (4416614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f48d8423c0fa6eb844a29d92e258ae9a33aa6e6cd0b95b4b69a21e72a8e567`  
		Last Modified: Fri, 14 Jan 2022 18:56:27 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8f267cce64b19b253599578af343c8bdcdc79f689ec7d92f4bec4f822e7412`  
		Last Modified: Fri, 14 Jan 2022 18:56:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:d2013f3c37f60a2f02029ff0ed712f0479ef409c7cae118a1ae0521f9a08d2bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6844582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ca3b8a166d5dd0ed044d2e85cc20e4795344ac64a28e513b00faa630c84882`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:57:58 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:58:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:58:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:58:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:58:03 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:58:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07275e3fb0a7b967b5381c0e07db89c39d1cf4e7ee0a649d1c009e78a1d42fa`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 4.4 MB (4408818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835acb2136974c88d21e7071bad202e0d0e39db27d2f0f944858311a7e80f9b4`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1452ec30e6ef252b617a9d46cbd566d7eba05df01f47c577c0d25daaf6d22c`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a1d2244a63e3ab81295587aaae2262e796174a4fa8687a8c872a4442973f50ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7112096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57981de17d5ffc0d33e96bee5e34398ecf77b8501362fca71a6e674fc061594`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:42:28 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:42:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:42:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:42:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:42:33 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:42:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccbd6fe265a7e2fbeca62a169f7f0cb64925946674670bc265127450e775009`  
		Last Modified: Fri, 14 Jan 2022 18:43:34 GMT  
		Size: 4.4 MB (4395688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7772805886c77ac22f41f9354d7d92334e4af6d9404544ee286084143a4c44e`  
		Last Modified: Fri, 14 Jan 2022 18:43:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567aec11ea3ca34811b7531dd4a2d7680c6dd5a7c649133b735ce4517d926f0`  
		Last Modified: Fri, 14 Jan 2022 18:43:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:0383d160c6f8689a3e994283699c2c034ce4f0d5f007c389aaf6e52ceb07e169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:b06db068fc05ac9f5c7e8ffc4dce11c880f881a04e0eb40ba835861cec37a7e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a534d8f4e2dc469a50383ab63dfa8e3c1e357e5f0dfa3d5de92592ed4e448864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:24:10 GMT
COPY file:4f0ebc4704f83777a3960e581d523bc013bb02a0cfb7e7f786516a6c49942e22 in /nats-server 
# Fri, 14 Jan 2022 18:24:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:24:11 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:24:11 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:24:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a98137475bb500ddd9f8416278069548db1131298356240d97df07b35a68f05e`  
		Last Modified: Fri, 14 Jan 2022 18:25:51 GMT  
		Size: 4.5 MB (4465555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866493868b198566f99c644afee3c392ed1225753255779f01c03c2bcf9bf89`  
		Last Modified: Fri, 14 Jan 2022 18:25:50 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:5548af7da41d68083d376352f0043468c1d3392b3ee8cf270074e41efdb7daf4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a6ba83aa0c651bc6443b87ad3aa75aa05a49015c60b0ba94433ed283182e9d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:54:41 GMT
COPY file:0bc79db49bf07145ed2820c48ab480154ad0fe7624645e978e1ab085987118ab in /nats-server 
# Fri, 14 Jan 2022 18:54:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:54:42 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:43 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:54:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1753283a9fe04770710f582c7edb68af20fff43cb6750b511b88edba870b6b0a`  
		Last Modified: Fri, 14 Jan 2022 18:57:08 GMT  
		Size: 4.1 MB (4130524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6144f16900b7c63ff5f07e50d96706eca97e1b1e9be9f15abbf3ba87d5727372`  
		Last Modified: Fri, 14 Jan 2022 18:57:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:bddc83bad582414e836c7e60fdf5658dabef500b7bc51fb8e18d6247e47f179c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3b7221c7fd3e3c292d74b2b00e056a887bf2fc9e0400f840107de9cca1dfd5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:58:28 GMT
COPY file:c678b429005ddd760afff9930c36320b6468ea514443a740c99ed69f0d9cd889 in /nats-server 
# Fri, 14 Jan 2022 18:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:58:29 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:58:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a42706d8cfe08c4bc9bc324ffc2e0f4757dd092aaaf7dfdb7a98124df24cde2b`  
		Last Modified: Fri, 14 Jan 2022 19:00:55 GMT  
		Size: 4.1 MB (4126980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4780c44069007ad60d46f2985dbe0e7eae3a04d7df9936f14a70b825ec84e73e`  
		Last Modified: Fri, 14 Jan 2022 19:00:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6404671cd360e397c582b0903bccde0c5ef78c3365c1515c184cf4c3465d06dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15eb321439fe02848e980c416856500b3d8a264944878381ad8ffd1aa1f00e79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:42:45 GMT
COPY file:35de8b46fa873fa93035ad9e0bd8add902aeeb3f777acb6477fe8ae33621069f in /nats-server 
# Fri, 14 Jan 2022 18:42:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:42:46 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:47 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:42:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:99635f3a9fe15a08eb7778c1228079183c996b57cbae1adb68626045408c36c0`  
		Last Modified: Fri, 14 Jan 2022 18:44:02 GMT  
		Size: 4.1 MB (4113430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c443fa2d7386b32c85a9d5d54923637c8b533da17f0755a42f2c3d16ac59b1f8`  
		Last Modified: Fri, 14 Jan 2022 18:44:01 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:67cbb585b085b43bbb93c9bcce0569c7f180b4d7b9f6374fde7d23083236960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:3ff2f0040a64a2cf0a020c4eb0425d13237737b34ecbd6a71b3b32c605bf55c2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107546942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e123bd94ced8bc2f98dc409ee61a0d185c740b720cbdce2ddfdbee78ca5ed5e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 15:13:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:18:56 GMT
RUN cmd /S /C #(nop) COPY file:76b3d6cbfb5183e43d9331cddd3a7f906364b8f5f8f8290ae121e47be5ed179c in C:\nats-server.exe 
# Fri, 14 Jan 2022 18:18:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:19:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:19:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db05d2e76671d91772a070867bf6f050343319070602a0f8239706d5d4d98387`  
		Last Modified: Wed, 12 Jan 2022 15:14:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc49f734ff1c4186abb068d17466f00a620f7903745063b3cc8ccb9492056b1`  
		Last Modified: Fri, 14 Jan 2022 18:19:52 GMT  
		Size: 4.5 MB (4509480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8029445e0be8d33827e442dd586388ee37afb157556c5075c892d3ec04b51b4a`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee34369f11e6432c63a08a695b26eec114e7f590e3e8db49e6ff3c9c6bc69dc`  
		Last Modified: Fri, 14 Jan 2022 18:19:50 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e6014d55a66a18b9b23e3a9d224307e4e729b2131ab80e5d94fe591092f6ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c431522fbf1e1f293b432240df83b2be82c117965a01a88ac9d4f6ce8904569`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:67cbb585b085b43bbb93c9bcce0569c7f180b4d7b9f6374fde7d23083236960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:3ff2f0040a64a2cf0a020c4eb0425d13237737b34ecbd6a71b3b32c605bf55c2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107546942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e123bd94ced8bc2f98dc409ee61a0d185c740b720cbdce2ddfdbee78ca5ed5e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 15:13:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:18:56 GMT
RUN cmd /S /C #(nop) COPY file:76b3d6cbfb5183e43d9331cddd3a7f906364b8f5f8f8290ae121e47be5ed179c in C:\nats-server.exe 
# Fri, 14 Jan 2022 18:18:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:19:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:19:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db05d2e76671d91772a070867bf6f050343319070602a0f8239706d5d4d98387`  
		Last Modified: Wed, 12 Jan 2022 15:14:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc49f734ff1c4186abb068d17466f00a620f7903745063b3cc8ccb9492056b1`  
		Last Modified: Fri, 14 Jan 2022 18:19:52 GMT  
		Size: 4.5 MB (4509480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8029445e0be8d33827e442dd586388ee37afb157556c5075c892d3ec04b51b4a`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee34369f11e6432c63a08a695b26eec114e7f590e3e8db49e6ff3c9c6bc69dc`  
		Last Modified: Fri, 14 Jan 2022 18:19:50 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e6014d55a66a18b9b23e3a9d224307e4e729b2131ab80e5d94fe591092f6ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c431522fbf1e1f293b432240df83b2be82c117965a01a88ac9d4f6ce8904569`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:0383d160c6f8689a3e994283699c2c034ce4f0d5f007c389aaf6e52ceb07e169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:b06db068fc05ac9f5c7e8ffc4dce11c880f881a04e0eb40ba835861cec37a7e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a534d8f4e2dc469a50383ab63dfa8e3c1e357e5f0dfa3d5de92592ed4e448864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:24:10 GMT
COPY file:4f0ebc4704f83777a3960e581d523bc013bb02a0cfb7e7f786516a6c49942e22 in /nats-server 
# Fri, 14 Jan 2022 18:24:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:24:11 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:24:11 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:24:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a98137475bb500ddd9f8416278069548db1131298356240d97df07b35a68f05e`  
		Last Modified: Fri, 14 Jan 2022 18:25:51 GMT  
		Size: 4.5 MB (4465555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866493868b198566f99c644afee3c392ed1225753255779f01c03c2bcf9bf89`  
		Last Modified: Fri, 14 Jan 2022 18:25:50 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:5548af7da41d68083d376352f0043468c1d3392b3ee8cf270074e41efdb7daf4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a6ba83aa0c651bc6443b87ad3aa75aa05a49015c60b0ba94433ed283182e9d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:54:41 GMT
COPY file:0bc79db49bf07145ed2820c48ab480154ad0fe7624645e978e1ab085987118ab in /nats-server 
# Fri, 14 Jan 2022 18:54:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:54:42 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:43 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:54:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1753283a9fe04770710f582c7edb68af20fff43cb6750b511b88edba870b6b0a`  
		Last Modified: Fri, 14 Jan 2022 18:57:08 GMT  
		Size: 4.1 MB (4130524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6144f16900b7c63ff5f07e50d96706eca97e1b1e9be9f15abbf3ba87d5727372`  
		Last Modified: Fri, 14 Jan 2022 18:57:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bddc83bad582414e836c7e60fdf5658dabef500b7bc51fb8e18d6247e47f179c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3b7221c7fd3e3c292d74b2b00e056a887bf2fc9e0400f840107de9cca1dfd5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:58:28 GMT
COPY file:c678b429005ddd760afff9930c36320b6468ea514443a740c99ed69f0d9cd889 in /nats-server 
# Fri, 14 Jan 2022 18:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:58:29 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:58:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a42706d8cfe08c4bc9bc324ffc2e0f4757dd092aaaf7dfdb7a98124df24cde2b`  
		Last Modified: Fri, 14 Jan 2022 19:00:55 GMT  
		Size: 4.1 MB (4126980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4780c44069007ad60d46f2985dbe0e7eae3a04d7df9936f14a70b825ec84e73e`  
		Last Modified: Fri, 14 Jan 2022 19:00:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6404671cd360e397c582b0903bccde0c5ef78c3365c1515c184cf4c3465d06dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15eb321439fe02848e980c416856500b3d8a264944878381ad8ffd1aa1f00e79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:42:45 GMT
COPY file:35de8b46fa873fa93035ad9e0bd8add902aeeb3f777acb6477fe8ae33621069f in /nats-server 
# Fri, 14 Jan 2022 18:42:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:42:46 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:47 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:42:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:99635f3a9fe15a08eb7778c1228079183c996b57cbae1adb68626045408c36c0`  
		Last Modified: Fri, 14 Jan 2022 18:44:02 GMT  
		Size: 4.1 MB (4113430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c443fa2d7386b32c85a9d5d54923637c8b533da17f0755a42f2c3d16ac59b1f8`  
		Last Modified: Fri, 14 Jan 2022 18:44:01 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:50612c3b2250d06c68ca4b2218715a3c21ceae6dfdb4995a83fa9afbc7881cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:54567f33c76734505d235f002a89b70802128ad108c980307bf03e451f34c9e8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2717410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb238e1dd188f62c4fe45a66109d5ed19abfd1d7e11aebefd90cc3f2da94753`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 22:48:13 GMT
RUN Install update 1809-amd64
# Wed, 12 Jan 2022 13:54:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jan 2022 15:10:29 GMT
ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:15:28 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:15:29 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.0/nats-server-v2.7.0-windows-amd64.zip
# Fri, 14 Jan 2022 18:15:30 GMT
ENV NATS_SERVER_SHASUM=691b1a9e159f749bea7879f7141d1e47f531ae008bdc8426fb7e0085347f7657
# Fri, 14 Jan 2022 18:16:46 GMT
RUN Set-PSDebug -Trace 2
# Fri, 14 Jan 2022 18:18:31 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 14 Jan 2022 18:18:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:33 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:18:34 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:18:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:635f15ebd5b486e8a00bf217a0574a29550e5bbf08c1d021e1e308100b2e49b5`  
		Size: 993.9 MB (993898043 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:537828534783cff318d36854dbda0683aef7263e437c7c669de4092e1778959c`  
		Last Modified: Wed, 12 Jan 2022 15:14:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9576e7772519d67febb0ceb94d8f22531ea99f0c60c36e67a4f5a497c384f5e0`  
		Last Modified: Wed, 12 Jan 2022 15:14:30 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9c40c82e2a4a4f46ef0e92dd0996d9acb6e8c064f6bda7396f48d98a830806`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fc415ca91c0ef702c8be90cf064a0ad853fbc2197f6d23ce4021075c7c31ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cad8ea5aab62c1b4669ca21ee421254265ae0fa526303f34d4d4ce4944a4e3`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4a5b12ef3e0729dc379170f433144469137fb87c269a4a99942ed0a42c38e`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 338.6 KB (338632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187afc1c2121ca26ccb436661e781314b8c0033e5f7d393dfa6482647b35c032`  
		Last Modified: Fri, 14 Jan 2022 18:19:33 GMT  
		Size: 4.8 MB (4827999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f13ff9dec18a932ca99f41132ef4b3d9a9e46885f7a39fe99a066960c3c043`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e0eea58542a95fa0e451371e0304d937be8d6cb6b58b1b00d1325d61053ec9`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd13792fd02f90975cb571d7fbc95735d3ac1f4ea9324bb0ae219fafbe31321`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d46d787da89b4538d3f489455995f217d84669ecf1e402a558d10503d64f32b`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:50612c3b2250d06c68ca4b2218715a3c21ceae6dfdb4995a83fa9afbc7881cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:54567f33c76734505d235f002a89b70802128ad108c980307bf03e451f34c9e8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2717410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb238e1dd188f62c4fe45a66109d5ed19abfd1d7e11aebefd90cc3f2da94753`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 22:48:13 GMT
RUN Install update 1809-amd64
# Wed, 12 Jan 2022 13:54:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jan 2022 15:10:29 GMT
ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:15:28 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:15:29 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.0/nats-server-v2.7.0-windows-amd64.zip
# Fri, 14 Jan 2022 18:15:30 GMT
ENV NATS_SERVER_SHASUM=691b1a9e159f749bea7879f7141d1e47f531ae008bdc8426fb7e0085347f7657
# Fri, 14 Jan 2022 18:16:46 GMT
RUN Set-PSDebug -Trace 2
# Fri, 14 Jan 2022 18:18:31 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 14 Jan 2022 18:18:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:33 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:18:34 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:18:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:635f15ebd5b486e8a00bf217a0574a29550e5bbf08c1d021e1e308100b2e49b5`  
		Size: 993.9 MB (993898043 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:537828534783cff318d36854dbda0683aef7263e437c7c669de4092e1778959c`  
		Last Modified: Wed, 12 Jan 2022 15:14:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9576e7772519d67febb0ceb94d8f22531ea99f0c60c36e67a4f5a497c384f5e0`  
		Last Modified: Wed, 12 Jan 2022 15:14:30 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9c40c82e2a4a4f46ef0e92dd0996d9acb6e8c064f6bda7396f48d98a830806`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fc415ca91c0ef702c8be90cf064a0ad853fbc2197f6d23ce4021075c7c31ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cad8ea5aab62c1b4669ca21ee421254265ae0fa526303f34d4d4ce4944a4e3`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4a5b12ef3e0729dc379170f433144469137fb87c269a4a99942ed0a42c38e`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 338.6 KB (338632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187afc1c2121ca26ccb436661e781314b8c0033e5f7d393dfa6482647b35c032`  
		Last Modified: Fri, 14 Jan 2022 18:19:33 GMT  
		Size: 4.8 MB (4827999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f13ff9dec18a932ca99f41132ef4b3d9a9e46885f7a39fe99a066960c3c043`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e0eea58542a95fa0e451371e0304d937be8d6cb6b58b1b00d1325d61053ec9`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd13792fd02f90975cb571d7fbc95735d3ac1f4ea9324bb0ae219fafbe31321`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d46d787da89b4538d3f489455995f217d84669ecf1e402a558d10503d64f32b`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7`

```console
$ docker pull nats@sha256:08f87dbef4702c335b595c22a60955eda795d9dc2059dc6d5d1692e10f84379a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2452; amd64

### `nats:2.7` - linux; amd64

```console
$ docker pull nats@sha256:b06db068fc05ac9f5c7e8ffc4dce11c880f881a04e0eb40ba835861cec37a7e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a534d8f4e2dc469a50383ab63dfa8e3c1e357e5f0dfa3d5de92592ed4e448864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:24:10 GMT
COPY file:4f0ebc4704f83777a3960e581d523bc013bb02a0cfb7e7f786516a6c49942e22 in /nats-server 
# Fri, 14 Jan 2022 18:24:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:24:11 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:24:11 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:24:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a98137475bb500ddd9f8416278069548db1131298356240d97df07b35a68f05e`  
		Last Modified: Fri, 14 Jan 2022 18:25:51 GMT  
		Size: 4.5 MB (4465555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866493868b198566f99c644afee3c392ed1225753255779f01c03c2bcf9bf89`  
		Last Modified: Fri, 14 Jan 2022 18:25:50 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - linux; arm variant v6

```console
$ docker pull nats@sha256:5548af7da41d68083d376352f0043468c1d3392b3ee8cf270074e41efdb7daf4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a6ba83aa0c651bc6443b87ad3aa75aa05a49015c60b0ba94433ed283182e9d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:54:41 GMT
COPY file:0bc79db49bf07145ed2820c48ab480154ad0fe7624645e978e1ab085987118ab in /nats-server 
# Fri, 14 Jan 2022 18:54:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:54:42 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:43 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:54:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1753283a9fe04770710f582c7edb68af20fff43cb6750b511b88edba870b6b0a`  
		Last Modified: Fri, 14 Jan 2022 18:57:08 GMT  
		Size: 4.1 MB (4130524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6144f16900b7c63ff5f07e50d96706eca97e1b1e9be9f15abbf3ba87d5727372`  
		Last Modified: Fri, 14 Jan 2022 18:57:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - linux; arm variant v7

```console
$ docker pull nats@sha256:bddc83bad582414e836c7e60fdf5658dabef500b7bc51fb8e18d6247e47f179c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3b7221c7fd3e3c292d74b2b00e056a887bf2fc9e0400f840107de9cca1dfd5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:58:28 GMT
COPY file:c678b429005ddd760afff9930c36320b6468ea514443a740c99ed69f0d9cd889 in /nats-server 
# Fri, 14 Jan 2022 18:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:58:29 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:58:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a42706d8cfe08c4bc9bc324ffc2e0f4757dd092aaaf7dfdb7a98124df24cde2b`  
		Last Modified: Fri, 14 Jan 2022 19:00:55 GMT  
		Size: 4.1 MB (4126980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4780c44069007ad60d46f2985dbe0e7eae3a04d7df9936f14a70b825ec84e73e`  
		Last Modified: Fri, 14 Jan 2022 19:00:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6404671cd360e397c582b0903bccde0c5ef78c3365c1515c184cf4c3465d06dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15eb321439fe02848e980c416856500b3d8a264944878381ad8ffd1aa1f00e79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:42:45 GMT
COPY file:35de8b46fa873fa93035ad9e0bd8add902aeeb3f777acb6477fe8ae33621069f in /nats-server 
# Fri, 14 Jan 2022 18:42:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:42:46 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:47 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:42:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:99635f3a9fe15a08eb7778c1228079183c996b57cbae1adb68626045408c36c0`  
		Last Modified: Fri, 14 Jan 2022 18:44:02 GMT  
		Size: 4.1 MB (4113430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c443fa2d7386b32c85a9d5d54923637c8b533da17f0755a42f2c3d16ac59b1f8`  
		Last Modified: Fri, 14 Jan 2022 18:44:01 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:3ff2f0040a64a2cf0a020c4eb0425d13237737b34ecbd6a71b3b32c605bf55c2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107546942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e123bd94ced8bc2f98dc409ee61a0d185c740b720cbdce2ddfdbee78ca5ed5e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 15:13:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:18:56 GMT
RUN cmd /S /C #(nop) COPY file:76b3d6cbfb5183e43d9331cddd3a7f906364b8f5f8f8290ae121e47be5ed179c in C:\nats-server.exe 
# Fri, 14 Jan 2022 18:18:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:19:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:19:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db05d2e76671d91772a070867bf6f050343319070602a0f8239706d5d4d98387`  
		Last Modified: Wed, 12 Jan 2022 15:14:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc49f734ff1c4186abb068d17466f00a620f7903745063b3cc8ccb9492056b1`  
		Last Modified: Fri, 14 Jan 2022 18:19:52 GMT  
		Size: 4.5 MB (4509480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8029445e0be8d33827e442dd586388ee37afb157556c5075c892d3ec04b51b4a`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee34369f11e6432c63a08a695b26eec114e7f590e3e8db49e6ff3c9c6bc69dc`  
		Last Modified: Fri, 14 Jan 2022 18:19:50 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e6014d55a66a18b9b23e3a9d224307e4e729b2131ab80e5d94fe591092f6ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c431522fbf1e1f293b432240df83b2be82c117965a01a88ac9d4f6ce8904569`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-alpine`

```console
$ docker pull nats@sha256:86f63911d02c7d05e6c62592a784679b1f9cb74b60d10c6c4b4d84bdf773b8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-alpine` - linux; amd64

```console
$ docker pull nats@sha256:9d6193c3f8c966a9fd387d258cbfceb3200dc155e5f1a96f6694d4e32215a256
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7569415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b06173b70b1d7bc01311e68328c369c3aba532201c604f9c3f0448368fc71a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:23:38 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:23:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:23:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:23:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:23:41 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:23:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e250c9fddf0251b9995287f56761bb006e4f275b872349f80eb59756e8362097`  
		Last Modified: Fri, 14 Jan 2022 18:24:46 GMT  
		Size: 4.8 MB (4750002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3370d34129abaa0cf5ea03a4de6b432c98e961247e0db58152afef624d5116b6`  
		Last Modified: Fri, 14 Jan 2022 18:24:45 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e699db775f306d056ba3491ef1a78bd60f43f6d84ca190dd5556ab952670bd37`  
		Last Modified: Fri, 14 Jan 2022 18:24:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:9a3ef866b8c56865ef170349f9b6c96434c59b83c8bd00434ac2ba069aa4d1c7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7049035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe56fe3b27ad5f693e36b857dd1234ada2657a84c9066653b1ff0789f912fbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:54:13 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:54:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:54:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:54:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:54:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32aa97c3aebf0246aa45096afee59b2568a296682d22adefa585ddfab52017e1`  
		Last Modified: Fri, 14 Jan 2022 18:56:29 GMT  
		Size: 4.4 MB (4416614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f48d8423c0fa6eb844a29d92e258ae9a33aa6e6cd0b95b4b69a21e72a8e567`  
		Last Modified: Fri, 14 Jan 2022 18:56:27 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8f267cce64b19b253599578af343c8bdcdc79f689ec7d92f4bec4f822e7412`  
		Last Modified: Fri, 14 Jan 2022 18:56:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:d2013f3c37f60a2f02029ff0ed712f0479ef409c7cae118a1ae0521f9a08d2bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6844582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ca3b8a166d5dd0ed044d2e85cc20e4795344ac64a28e513b00faa630c84882`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:57:58 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:58:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:58:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:58:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:58:03 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:58:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07275e3fb0a7b967b5381c0e07db89c39d1cf4e7ee0a649d1c009e78a1d42fa`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 4.4 MB (4408818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835acb2136974c88d21e7071bad202e0d0e39db27d2f0f944858311a7e80f9b4`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1452ec30e6ef252b617a9d46cbd566d7eba05df01f47c577c0d25daaf6d22c`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a1d2244a63e3ab81295587aaae2262e796174a4fa8687a8c872a4442973f50ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7112096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57981de17d5ffc0d33e96bee5e34398ecf77b8501362fca71a6e674fc061594`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:42:28 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:42:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:42:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:42:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:42:33 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:42:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccbd6fe265a7e2fbeca62a169f7f0cb64925946674670bc265127450e775009`  
		Last Modified: Fri, 14 Jan 2022 18:43:34 GMT  
		Size: 4.4 MB (4395688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7772805886c77ac22f41f9354d7d92334e4af6d9404544ee286084143a4c44e`  
		Last Modified: Fri, 14 Jan 2022 18:43:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567aec11ea3ca34811b7531dd4a2d7680c6dd5a7c649133b735ce4517d926f0`  
		Last Modified: Fri, 14 Jan 2022 18:43:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-alpine3.15`

```console
$ docker pull nats@sha256:86f63911d02c7d05e6c62592a784679b1f9cb74b60d10c6c4b4d84bdf773b8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:9d6193c3f8c966a9fd387d258cbfceb3200dc155e5f1a96f6694d4e32215a256
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7569415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b06173b70b1d7bc01311e68328c369c3aba532201c604f9c3f0448368fc71a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:23:38 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:23:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:23:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:23:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:23:41 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:23:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e250c9fddf0251b9995287f56761bb006e4f275b872349f80eb59756e8362097`  
		Last Modified: Fri, 14 Jan 2022 18:24:46 GMT  
		Size: 4.8 MB (4750002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3370d34129abaa0cf5ea03a4de6b432c98e961247e0db58152afef624d5116b6`  
		Last Modified: Fri, 14 Jan 2022 18:24:45 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e699db775f306d056ba3491ef1a78bd60f43f6d84ca190dd5556ab952670bd37`  
		Last Modified: Fri, 14 Jan 2022 18:24:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:9a3ef866b8c56865ef170349f9b6c96434c59b83c8bd00434ac2ba069aa4d1c7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7049035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe56fe3b27ad5f693e36b857dd1234ada2657a84c9066653b1ff0789f912fbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:54:13 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:54:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:54:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:54:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:54:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32aa97c3aebf0246aa45096afee59b2568a296682d22adefa585ddfab52017e1`  
		Last Modified: Fri, 14 Jan 2022 18:56:29 GMT  
		Size: 4.4 MB (4416614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f48d8423c0fa6eb844a29d92e258ae9a33aa6e6cd0b95b4b69a21e72a8e567`  
		Last Modified: Fri, 14 Jan 2022 18:56:27 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8f267cce64b19b253599578af343c8bdcdc79f689ec7d92f4bec4f822e7412`  
		Last Modified: Fri, 14 Jan 2022 18:56:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:d2013f3c37f60a2f02029ff0ed712f0479ef409c7cae118a1ae0521f9a08d2bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6844582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ca3b8a166d5dd0ed044d2e85cc20e4795344ac64a28e513b00faa630c84882`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:57:58 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:58:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:58:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:58:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:58:03 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:58:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07275e3fb0a7b967b5381c0e07db89c39d1cf4e7ee0a649d1c009e78a1d42fa`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 4.4 MB (4408818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835acb2136974c88d21e7071bad202e0d0e39db27d2f0f944858311a7e80f9b4`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1452ec30e6ef252b617a9d46cbd566d7eba05df01f47c577c0d25daaf6d22c`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a1d2244a63e3ab81295587aaae2262e796174a4fa8687a8c872a4442973f50ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7112096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57981de17d5ffc0d33e96bee5e34398ecf77b8501362fca71a6e674fc061594`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:42:28 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:42:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:42:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:42:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:42:33 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:42:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccbd6fe265a7e2fbeca62a169f7f0cb64925946674670bc265127450e775009`  
		Last Modified: Fri, 14 Jan 2022 18:43:34 GMT  
		Size: 4.4 MB (4395688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7772805886c77ac22f41f9354d7d92334e4af6d9404544ee286084143a4c44e`  
		Last Modified: Fri, 14 Jan 2022 18:43:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567aec11ea3ca34811b7531dd4a2d7680c6dd5a7c649133b735ce4517d926f0`  
		Last Modified: Fri, 14 Jan 2022 18:43:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-linux`

```console
$ docker pull nats@sha256:0383d160c6f8689a3e994283699c2c034ce4f0d5f007c389aaf6e52ceb07e169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-linux` - linux; amd64

```console
$ docker pull nats@sha256:b06db068fc05ac9f5c7e8ffc4dce11c880f881a04e0eb40ba835861cec37a7e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a534d8f4e2dc469a50383ab63dfa8e3c1e357e5f0dfa3d5de92592ed4e448864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:24:10 GMT
COPY file:4f0ebc4704f83777a3960e581d523bc013bb02a0cfb7e7f786516a6c49942e22 in /nats-server 
# Fri, 14 Jan 2022 18:24:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:24:11 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:24:11 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:24:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a98137475bb500ddd9f8416278069548db1131298356240d97df07b35a68f05e`  
		Last Modified: Fri, 14 Jan 2022 18:25:51 GMT  
		Size: 4.5 MB (4465555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866493868b198566f99c644afee3c392ed1225753255779f01c03c2bcf9bf89`  
		Last Modified: Fri, 14 Jan 2022 18:25:50 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:5548af7da41d68083d376352f0043468c1d3392b3ee8cf270074e41efdb7daf4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a6ba83aa0c651bc6443b87ad3aa75aa05a49015c60b0ba94433ed283182e9d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:54:41 GMT
COPY file:0bc79db49bf07145ed2820c48ab480154ad0fe7624645e978e1ab085987118ab in /nats-server 
# Fri, 14 Jan 2022 18:54:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:54:42 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:43 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:54:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1753283a9fe04770710f582c7edb68af20fff43cb6750b511b88edba870b6b0a`  
		Last Modified: Fri, 14 Jan 2022 18:57:08 GMT  
		Size: 4.1 MB (4130524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6144f16900b7c63ff5f07e50d96706eca97e1b1e9be9f15abbf3ba87d5727372`  
		Last Modified: Fri, 14 Jan 2022 18:57:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:bddc83bad582414e836c7e60fdf5658dabef500b7bc51fb8e18d6247e47f179c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3b7221c7fd3e3c292d74b2b00e056a887bf2fc9e0400f840107de9cca1dfd5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:58:28 GMT
COPY file:c678b429005ddd760afff9930c36320b6468ea514443a740c99ed69f0d9cd889 in /nats-server 
# Fri, 14 Jan 2022 18:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:58:29 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:58:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a42706d8cfe08c4bc9bc324ffc2e0f4757dd092aaaf7dfdb7a98124df24cde2b`  
		Last Modified: Fri, 14 Jan 2022 19:00:55 GMT  
		Size: 4.1 MB (4126980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4780c44069007ad60d46f2985dbe0e7eae3a04d7df9936f14a70b825ec84e73e`  
		Last Modified: Fri, 14 Jan 2022 19:00:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6404671cd360e397c582b0903bccde0c5ef78c3365c1515c184cf4c3465d06dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15eb321439fe02848e980c416856500b3d8a264944878381ad8ffd1aa1f00e79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:42:45 GMT
COPY file:35de8b46fa873fa93035ad9e0bd8add902aeeb3f777acb6477fe8ae33621069f in /nats-server 
# Fri, 14 Jan 2022 18:42:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:42:46 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:47 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:42:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:99635f3a9fe15a08eb7778c1228079183c996b57cbae1adb68626045408c36c0`  
		Last Modified: Fri, 14 Jan 2022 18:44:02 GMT  
		Size: 4.1 MB (4113430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c443fa2d7386b32c85a9d5d54923637c8b533da17f0755a42f2c3d16ac59b1f8`  
		Last Modified: Fri, 14 Jan 2022 18:44:01 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-nanoserver`

```console
$ docker pull nats@sha256:67cbb585b085b43bbb93c9bcce0569c7f180b4d7b9f6374fde7d23083236960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `nats:2.7-nanoserver` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:3ff2f0040a64a2cf0a020c4eb0425d13237737b34ecbd6a71b3b32c605bf55c2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107546942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e123bd94ced8bc2f98dc409ee61a0d185c740b720cbdce2ddfdbee78ca5ed5e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 15:13:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:18:56 GMT
RUN cmd /S /C #(nop) COPY file:76b3d6cbfb5183e43d9331cddd3a7f906364b8f5f8f8290ae121e47be5ed179c in C:\nats-server.exe 
# Fri, 14 Jan 2022 18:18:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:19:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:19:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db05d2e76671d91772a070867bf6f050343319070602a0f8239706d5d4d98387`  
		Last Modified: Wed, 12 Jan 2022 15:14:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc49f734ff1c4186abb068d17466f00a620f7903745063b3cc8ccb9492056b1`  
		Last Modified: Fri, 14 Jan 2022 18:19:52 GMT  
		Size: 4.5 MB (4509480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8029445e0be8d33827e442dd586388ee37afb157556c5075c892d3ec04b51b4a`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee34369f11e6432c63a08a695b26eec114e7f590e3e8db49e6ff3c9c6bc69dc`  
		Last Modified: Fri, 14 Jan 2022 18:19:50 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e6014d55a66a18b9b23e3a9d224307e4e729b2131ab80e5d94fe591092f6ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c431522fbf1e1f293b432240df83b2be82c117965a01a88ac9d4f6ce8904569`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-nanoserver-1809`

```console
$ docker pull nats@sha256:67cbb585b085b43bbb93c9bcce0569c7f180b4d7b9f6374fde7d23083236960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `nats:2.7-nanoserver-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:3ff2f0040a64a2cf0a020c4eb0425d13237737b34ecbd6a71b3b32c605bf55c2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107546942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e123bd94ced8bc2f98dc409ee61a0d185c740b720cbdce2ddfdbee78ca5ed5e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 15:13:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:18:56 GMT
RUN cmd /S /C #(nop) COPY file:76b3d6cbfb5183e43d9331cddd3a7f906364b8f5f8f8290ae121e47be5ed179c in C:\nats-server.exe 
# Fri, 14 Jan 2022 18:18:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:19:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:19:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db05d2e76671d91772a070867bf6f050343319070602a0f8239706d5d4d98387`  
		Last Modified: Wed, 12 Jan 2022 15:14:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc49f734ff1c4186abb068d17466f00a620f7903745063b3cc8ccb9492056b1`  
		Last Modified: Fri, 14 Jan 2022 18:19:52 GMT  
		Size: 4.5 MB (4509480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8029445e0be8d33827e442dd586388ee37afb157556c5075c892d3ec04b51b4a`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee34369f11e6432c63a08a695b26eec114e7f590e3e8db49e6ff3c9c6bc69dc`  
		Last Modified: Fri, 14 Jan 2022 18:19:50 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e6014d55a66a18b9b23e3a9d224307e4e729b2131ab80e5d94fe591092f6ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c431522fbf1e1f293b432240df83b2be82c117965a01a88ac9d4f6ce8904569`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-scratch`

```console
$ docker pull nats@sha256:0383d160c6f8689a3e994283699c2c034ce4f0d5f007c389aaf6e52ceb07e169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-scratch` - linux; amd64

```console
$ docker pull nats@sha256:b06db068fc05ac9f5c7e8ffc4dce11c880f881a04e0eb40ba835861cec37a7e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a534d8f4e2dc469a50383ab63dfa8e3c1e357e5f0dfa3d5de92592ed4e448864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:24:10 GMT
COPY file:4f0ebc4704f83777a3960e581d523bc013bb02a0cfb7e7f786516a6c49942e22 in /nats-server 
# Fri, 14 Jan 2022 18:24:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:24:11 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:24:11 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:24:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a98137475bb500ddd9f8416278069548db1131298356240d97df07b35a68f05e`  
		Last Modified: Fri, 14 Jan 2022 18:25:51 GMT  
		Size: 4.5 MB (4465555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866493868b198566f99c644afee3c392ed1225753255779f01c03c2bcf9bf89`  
		Last Modified: Fri, 14 Jan 2022 18:25:50 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:5548af7da41d68083d376352f0043468c1d3392b3ee8cf270074e41efdb7daf4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a6ba83aa0c651bc6443b87ad3aa75aa05a49015c60b0ba94433ed283182e9d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:54:41 GMT
COPY file:0bc79db49bf07145ed2820c48ab480154ad0fe7624645e978e1ab085987118ab in /nats-server 
# Fri, 14 Jan 2022 18:54:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:54:42 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:43 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:54:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1753283a9fe04770710f582c7edb68af20fff43cb6750b511b88edba870b6b0a`  
		Last Modified: Fri, 14 Jan 2022 18:57:08 GMT  
		Size: 4.1 MB (4130524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6144f16900b7c63ff5f07e50d96706eca97e1b1e9be9f15abbf3ba87d5727372`  
		Last Modified: Fri, 14 Jan 2022 18:57:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bddc83bad582414e836c7e60fdf5658dabef500b7bc51fb8e18d6247e47f179c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3b7221c7fd3e3c292d74b2b00e056a887bf2fc9e0400f840107de9cca1dfd5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:58:28 GMT
COPY file:c678b429005ddd760afff9930c36320b6468ea514443a740c99ed69f0d9cd889 in /nats-server 
# Fri, 14 Jan 2022 18:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:58:29 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:58:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a42706d8cfe08c4bc9bc324ffc2e0f4757dd092aaaf7dfdb7a98124df24cde2b`  
		Last Modified: Fri, 14 Jan 2022 19:00:55 GMT  
		Size: 4.1 MB (4126980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4780c44069007ad60d46f2985dbe0e7eae3a04d7df9936f14a70b825ec84e73e`  
		Last Modified: Fri, 14 Jan 2022 19:00:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6404671cd360e397c582b0903bccde0c5ef78c3365c1515c184cf4c3465d06dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15eb321439fe02848e980c416856500b3d8a264944878381ad8ffd1aa1f00e79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:42:45 GMT
COPY file:35de8b46fa873fa93035ad9e0bd8add902aeeb3f777acb6477fe8ae33621069f in /nats-server 
# Fri, 14 Jan 2022 18:42:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:42:46 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:47 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:42:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:99635f3a9fe15a08eb7778c1228079183c996b57cbae1adb68626045408c36c0`  
		Last Modified: Fri, 14 Jan 2022 18:44:02 GMT  
		Size: 4.1 MB (4113430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c443fa2d7386b32c85a9d5d54923637c8b533da17f0755a42f2c3d16ac59b1f8`  
		Last Modified: Fri, 14 Jan 2022 18:44:01 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-windowsservercore`

```console
$ docker pull nats@sha256:50612c3b2250d06c68ca4b2218715a3c21ceae6dfdb4995a83fa9afbc7881cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `nats:2.7-windowsservercore` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:54567f33c76734505d235f002a89b70802128ad108c980307bf03e451f34c9e8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2717410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb238e1dd188f62c4fe45a66109d5ed19abfd1d7e11aebefd90cc3f2da94753`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 22:48:13 GMT
RUN Install update 1809-amd64
# Wed, 12 Jan 2022 13:54:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jan 2022 15:10:29 GMT
ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:15:28 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:15:29 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.0/nats-server-v2.7.0-windows-amd64.zip
# Fri, 14 Jan 2022 18:15:30 GMT
ENV NATS_SERVER_SHASUM=691b1a9e159f749bea7879f7141d1e47f531ae008bdc8426fb7e0085347f7657
# Fri, 14 Jan 2022 18:16:46 GMT
RUN Set-PSDebug -Trace 2
# Fri, 14 Jan 2022 18:18:31 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 14 Jan 2022 18:18:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:33 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:18:34 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:18:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:635f15ebd5b486e8a00bf217a0574a29550e5bbf08c1d021e1e308100b2e49b5`  
		Size: 993.9 MB (993898043 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:537828534783cff318d36854dbda0683aef7263e437c7c669de4092e1778959c`  
		Last Modified: Wed, 12 Jan 2022 15:14:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9576e7772519d67febb0ceb94d8f22531ea99f0c60c36e67a4f5a497c384f5e0`  
		Last Modified: Wed, 12 Jan 2022 15:14:30 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9c40c82e2a4a4f46ef0e92dd0996d9acb6e8c064f6bda7396f48d98a830806`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fc415ca91c0ef702c8be90cf064a0ad853fbc2197f6d23ce4021075c7c31ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cad8ea5aab62c1b4669ca21ee421254265ae0fa526303f34d4d4ce4944a4e3`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4a5b12ef3e0729dc379170f433144469137fb87c269a4a99942ed0a42c38e`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 338.6 KB (338632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187afc1c2121ca26ccb436661e781314b8c0033e5f7d393dfa6482647b35c032`  
		Last Modified: Fri, 14 Jan 2022 18:19:33 GMT  
		Size: 4.8 MB (4827999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f13ff9dec18a932ca99f41132ef4b3d9a9e46885f7a39fe99a066960c3c043`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e0eea58542a95fa0e451371e0304d937be8d6cb6b58b1b00d1325d61053ec9`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd13792fd02f90975cb571d7fbc95735d3ac1f4ea9324bb0ae219fafbe31321`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d46d787da89b4538d3f489455995f217d84669ecf1e402a558d10503d64f32b`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-windowsservercore-1809`

```console
$ docker pull nats@sha256:50612c3b2250d06c68ca4b2218715a3c21ceae6dfdb4995a83fa9afbc7881cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `nats:2.7-windowsservercore-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:54567f33c76734505d235f002a89b70802128ad108c980307bf03e451f34c9e8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2717410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb238e1dd188f62c4fe45a66109d5ed19abfd1d7e11aebefd90cc3f2da94753`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 22:48:13 GMT
RUN Install update 1809-amd64
# Wed, 12 Jan 2022 13:54:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jan 2022 15:10:29 GMT
ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:15:28 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:15:29 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.0/nats-server-v2.7.0-windows-amd64.zip
# Fri, 14 Jan 2022 18:15:30 GMT
ENV NATS_SERVER_SHASUM=691b1a9e159f749bea7879f7141d1e47f531ae008bdc8426fb7e0085347f7657
# Fri, 14 Jan 2022 18:16:46 GMT
RUN Set-PSDebug -Trace 2
# Fri, 14 Jan 2022 18:18:31 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 14 Jan 2022 18:18:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:33 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:18:34 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:18:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:635f15ebd5b486e8a00bf217a0574a29550e5bbf08c1d021e1e308100b2e49b5`  
		Size: 993.9 MB (993898043 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:537828534783cff318d36854dbda0683aef7263e437c7c669de4092e1778959c`  
		Last Modified: Wed, 12 Jan 2022 15:14:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9576e7772519d67febb0ceb94d8f22531ea99f0c60c36e67a4f5a497c384f5e0`  
		Last Modified: Wed, 12 Jan 2022 15:14:30 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9c40c82e2a4a4f46ef0e92dd0996d9acb6e8c064f6bda7396f48d98a830806`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fc415ca91c0ef702c8be90cf064a0ad853fbc2197f6d23ce4021075c7c31ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cad8ea5aab62c1b4669ca21ee421254265ae0fa526303f34d4d4ce4944a4e3`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4a5b12ef3e0729dc379170f433144469137fb87c269a4a99942ed0a42c38e`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 338.6 KB (338632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187afc1c2121ca26ccb436661e781314b8c0033e5f7d393dfa6482647b35c032`  
		Last Modified: Fri, 14 Jan 2022 18:19:33 GMT  
		Size: 4.8 MB (4827999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f13ff9dec18a932ca99f41132ef4b3d9a9e46885f7a39fe99a066960c3c043`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e0eea58542a95fa0e451371e0304d937be8d6cb6b58b1b00d1325d61053ec9`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd13792fd02f90975cb571d7fbc95735d3ac1f4ea9324bb0ae219fafbe31321`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d46d787da89b4538d3f489455995f217d84669ecf1e402a558d10503d64f32b`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.0`

```console
$ docker pull nats@sha256:08f87dbef4702c335b595c22a60955eda795d9dc2059dc6d5d1692e10f84379a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2452; amd64

### `nats:2.7.0` - linux; amd64

```console
$ docker pull nats@sha256:b06db068fc05ac9f5c7e8ffc4dce11c880f881a04e0eb40ba835861cec37a7e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a534d8f4e2dc469a50383ab63dfa8e3c1e357e5f0dfa3d5de92592ed4e448864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:24:10 GMT
COPY file:4f0ebc4704f83777a3960e581d523bc013bb02a0cfb7e7f786516a6c49942e22 in /nats-server 
# Fri, 14 Jan 2022 18:24:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:24:11 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:24:11 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:24:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a98137475bb500ddd9f8416278069548db1131298356240d97df07b35a68f05e`  
		Last Modified: Fri, 14 Jan 2022 18:25:51 GMT  
		Size: 4.5 MB (4465555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866493868b198566f99c644afee3c392ed1225753255779f01c03c2bcf9bf89`  
		Last Modified: Fri, 14 Jan 2022 18:25:50 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.0` - linux; arm variant v6

```console
$ docker pull nats@sha256:5548af7da41d68083d376352f0043468c1d3392b3ee8cf270074e41efdb7daf4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a6ba83aa0c651bc6443b87ad3aa75aa05a49015c60b0ba94433ed283182e9d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:54:41 GMT
COPY file:0bc79db49bf07145ed2820c48ab480154ad0fe7624645e978e1ab085987118ab in /nats-server 
# Fri, 14 Jan 2022 18:54:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:54:42 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:43 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:54:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1753283a9fe04770710f582c7edb68af20fff43cb6750b511b88edba870b6b0a`  
		Last Modified: Fri, 14 Jan 2022 18:57:08 GMT  
		Size: 4.1 MB (4130524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6144f16900b7c63ff5f07e50d96706eca97e1b1e9be9f15abbf3ba87d5727372`  
		Last Modified: Fri, 14 Jan 2022 18:57:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.0` - linux; arm variant v7

```console
$ docker pull nats@sha256:bddc83bad582414e836c7e60fdf5658dabef500b7bc51fb8e18d6247e47f179c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3b7221c7fd3e3c292d74b2b00e056a887bf2fc9e0400f840107de9cca1dfd5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:58:28 GMT
COPY file:c678b429005ddd760afff9930c36320b6468ea514443a740c99ed69f0d9cd889 in /nats-server 
# Fri, 14 Jan 2022 18:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:58:29 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:58:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a42706d8cfe08c4bc9bc324ffc2e0f4757dd092aaaf7dfdb7a98124df24cde2b`  
		Last Modified: Fri, 14 Jan 2022 19:00:55 GMT  
		Size: 4.1 MB (4126980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4780c44069007ad60d46f2985dbe0e7eae3a04d7df9936f14a70b825ec84e73e`  
		Last Modified: Fri, 14 Jan 2022 19:00:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.0` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6404671cd360e397c582b0903bccde0c5ef78c3365c1515c184cf4c3465d06dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15eb321439fe02848e980c416856500b3d8a264944878381ad8ffd1aa1f00e79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:42:45 GMT
COPY file:35de8b46fa873fa93035ad9e0bd8add902aeeb3f777acb6477fe8ae33621069f in /nats-server 
# Fri, 14 Jan 2022 18:42:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:42:46 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:47 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:42:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:99635f3a9fe15a08eb7778c1228079183c996b57cbae1adb68626045408c36c0`  
		Last Modified: Fri, 14 Jan 2022 18:44:02 GMT  
		Size: 4.1 MB (4113430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c443fa2d7386b32c85a9d5d54923637c8b533da17f0755a42f2c3d16ac59b1f8`  
		Last Modified: Fri, 14 Jan 2022 18:44:01 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.0` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:3ff2f0040a64a2cf0a020c4eb0425d13237737b34ecbd6a71b3b32c605bf55c2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107546942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e123bd94ced8bc2f98dc409ee61a0d185c740b720cbdce2ddfdbee78ca5ed5e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 15:13:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:18:56 GMT
RUN cmd /S /C #(nop) COPY file:76b3d6cbfb5183e43d9331cddd3a7f906364b8f5f8f8290ae121e47be5ed179c in C:\nats-server.exe 
# Fri, 14 Jan 2022 18:18:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:19:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:19:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db05d2e76671d91772a070867bf6f050343319070602a0f8239706d5d4d98387`  
		Last Modified: Wed, 12 Jan 2022 15:14:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc49f734ff1c4186abb068d17466f00a620f7903745063b3cc8ccb9492056b1`  
		Last Modified: Fri, 14 Jan 2022 18:19:52 GMT  
		Size: 4.5 MB (4509480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8029445e0be8d33827e442dd586388ee37afb157556c5075c892d3ec04b51b4a`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee34369f11e6432c63a08a695b26eec114e7f590e3e8db49e6ff3c9c6bc69dc`  
		Last Modified: Fri, 14 Jan 2022 18:19:50 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e6014d55a66a18b9b23e3a9d224307e4e729b2131ab80e5d94fe591092f6ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c431522fbf1e1f293b432240df83b2be82c117965a01a88ac9d4f6ce8904569`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.0-alpine`

```console
$ docker pull nats@sha256:86f63911d02c7d05e6c62592a784679b1f9cb74b60d10c6c4b4d84bdf773b8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.0-alpine` - linux; amd64

```console
$ docker pull nats@sha256:9d6193c3f8c966a9fd387d258cbfceb3200dc155e5f1a96f6694d4e32215a256
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7569415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b06173b70b1d7bc01311e68328c369c3aba532201c604f9c3f0448368fc71a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:23:38 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:23:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:23:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:23:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:23:41 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:23:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e250c9fddf0251b9995287f56761bb006e4f275b872349f80eb59756e8362097`  
		Last Modified: Fri, 14 Jan 2022 18:24:46 GMT  
		Size: 4.8 MB (4750002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3370d34129abaa0cf5ea03a4de6b432c98e961247e0db58152afef624d5116b6`  
		Last Modified: Fri, 14 Jan 2022 18:24:45 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e699db775f306d056ba3491ef1a78bd60f43f6d84ca190dd5556ab952670bd37`  
		Last Modified: Fri, 14 Jan 2022 18:24:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.0-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:9a3ef866b8c56865ef170349f9b6c96434c59b83c8bd00434ac2ba069aa4d1c7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7049035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe56fe3b27ad5f693e36b857dd1234ada2657a84c9066653b1ff0789f912fbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:54:13 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:54:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:54:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:54:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:54:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32aa97c3aebf0246aa45096afee59b2568a296682d22adefa585ddfab52017e1`  
		Last Modified: Fri, 14 Jan 2022 18:56:29 GMT  
		Size: 4.4 MB (4416614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f48d8423c0fa6eb844a29d92e258ae9a33aa6e6cd0b95b4b69a21e72a8e567`  
		Last Modified: Fri, 14 Jan 2022 18:56:27 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8f267cce64b19b253599578af343c8bdcdc79f689ec7d92f4bec4f822e7412`  
		Last Modified: Fri, 14 Jan 2022 18:56:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.0-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:d2013f3c37f60a2f02029ff0ed712f0479ef409c7cae118a1ae0521f9a08d2bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6844582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ca3b8a166d5dd0ed044d2e85cc20e4795344ac64a28e513b00faa630c84882`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:57:58 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:58:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:58:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:58:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:58:03 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:58:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07275e3fb0a7b967b5381c0e07db89c39d1cf4e7ee0a649d1c009e78a1d42fa`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 4.4 MB (4408818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835acb2136974c88d21e7071bad202e0d0e39db27d2f0f944858311a7e80f9b4`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1452ec30e6ef252b617a9d46cbd566d7eba05df01f47c577c0d25daaf6d22c`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.0-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a1d2244a63e3ab81295587aaae2262e796174a4fa8687a8c872a4442973f50ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7112096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57981de17d5ffc0d33e96bee5e34398ecf77b8501362fca71a6e674fc061594`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:42:28 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:42:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:42:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:42:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:42:33 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:42:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccbd6fe265a7e2fbeca62a169f7f0cb64925946674670bc265127450e775009`  
		Last Modified: Fri, 14 Jan 2022 18:43:34 GMT  
		Size: 4.4 MB (4395688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7772805886c77ac22f41f9354d7d92334e4af6d9404544ee286084143a4c44e`  
		Last Modified: Fri, 14 Jan 2022 18:43:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567aec11ea3ca34811b7531dd4a2d7680c6dd5a7c649133b735ce4517d926f0`  
		Last Modified: Fri, 14 Jan 2022 18:43:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.0-alpine3.15`

```console
$ docker pull nats@sha256:86f63911d02c7d05e6c62592a784679b1f9cb74b60d10c6c4b4d84bdf773b8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.0-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:9d6193c3f8c966a9fd387d258cbfceb3200dc155e5f1a96f6694d4e32215a256
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7569415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b06173b70b1d7bc01311e68328c369c3aba532201c604f9c3f0448368fc71a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:23:38 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:23:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:23:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:23:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:23:41 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:23:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e250c9fddf0251b9995287f56761bb006e4f275b872349f80eb59756e8362097`  
		Last Modified: Fri, 14 Jan 2022 18:24:46 GMT  
		Size: 4.8 MB (4750002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3370d34129abaa0cf5ea03a4de6b432c98e961247e0db58152afef624d5116b6`  
		Last Modified: Fri, 14 Jan 2022 18:24:45 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e699db775f306d056ba3491ef1a78bd60f43f6d84ca190dd5556ab952670bd37`  
		Last Modified: Fri, 14 Jan 2022 18:24:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.0-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:9a3ef866b8c56865ef170349f9b6c96434c59b83c8bd00434ac2ba069aa4d1c7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7049035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe56fe3b27ad5f693e36b857dd1234ada2657a84c9066653b1ff0789f912fbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:54:13 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:54:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:54:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:54:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:54:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32aa97c3aebf0246aa45096afee59b2568a296682d22adefa585ddfab52017e1`  
		Last Modified: Fri, 14 Jan 2022 18:56:29 GMT  
		Size: 4.4 MB (4416614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f48d8423c0fa6eb844a29d92e258ae9a33aa6e6cd0b95b4b69a21e72a8e567`  
		Last Modified: Fri, 14 Jan 2022 18:56:27 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8f267cce64b19b253599578af343c8bdcdc79f689ec7d92f4bec4f822e7412`  
		Last Modified: Fri, 14 Jan 2022 18:56:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.0-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:d2013f3c37f60a2f02029ff0ed712f0479ef409c7cae118a1ae0521f9a08d2bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6844582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ca3b8a166d5dd0ed044d2e85cc20e4795344ac64a28e513b00faa630c84882`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:57:58 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:58:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:58:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:58:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:58:03 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:58:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07275e3fb0a7b967b5381c0e07db89c39d1cf4e7ee0a649d1c009e78a1d42fa`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 4.4 MB (4408818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835acb2136974c88d21e7071bad202e0d0e39db27d2f0f944858311a7e80f9b4`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1452ec30e6ef252b617a9d46cbd566d7eba05df01f47c577c0d25daaf6d22c`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.0-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a1d2244a63e3ab81295587aaae2262e796174a4fa8687a8c872a4442973f50ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7112096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57981de17d5ffc0d33e96bee5e34398ecf77b8501362fca71a6e674fc061594`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:42:28 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:42:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:42:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:42:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:42:33 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:42:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccbd6fe265a7e2fbeca62a169f7f0cb64925946674670bc265127450e775009`  
		Last Modified: Fri, 14 Jan 2022 18:43:34 GMT  
		Size: 4.4 MB (4395688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7772805886c77ac22f41f9354d7d92334e4af6d9404544ee286084143a4c44e`  
		Last Modified: Fri, 14 Jan 2022 18:43:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567aec11ea3ca34811b7531dd4a2d7680c6dd5a7c649133b735ce4517d926f0`  
		Last Modified: Fri, 14 Jan 2022 18:43:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.0-linux`

```console
$ docker pull nats@sha256:0383d160c6f8689a3e994283699c2c034ce4f0d5f007c389aaf6e52ceb07e169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.0-linux` - linux; amd64

```console
$ docker pull nats@sha256:b06db068fc05ac9f5c7e8ffc4dce11c880f881a04e0eb40ba835861cec37a7e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a534d8f4e2dc469a50383ab63dfa8e3c1e357e5f0dfa3d5de92592ed4e448864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:24:10 GMT
COPY file:4f0ebc4704f83777a3960e581d523bc013bb02a0cfb7e7f786516a6c49942e22 in /nats-server 
# Fri, 14 Jan 2022 18:24:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:24:11 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:24:11 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:24:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a98137475bb500ddd9f8416278069548db1131298356240d97df07b35a68f05e`  
		Last Modified: Fri, 14 Jan 2022 18:25:51 GMT  
		Size: 4.5 MB (4465555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866493868b198566f99c644afee3c392ed1225753255779f01c03c2bcf9bf89`  
		Last Modified: Fri, 14 Jan 2022 18:25:50 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.0-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:5548af7da41d68083d376352f0043468c1d3392b3ee8cf270074e41efdb7daf4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a6ba83aa0c651bc6443b87ad3aa75aa05a49015c60b0ba94433ed283182e9d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:54:41 GMT
COPY file:0bc79db49bf07145ed2820c48ab480154ad0fe7624645e978e1ab085987118ab in /nats-server 
# Fri, 14 Jan 2022 18:54:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:54:42 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:43 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:54:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1753283a9fe04770710f582c7edb68af20fff43cb6750b511b88edba870b6b0a`  
		Last Modified: Fri, 14 Jan 2022 18:57:08 GMT  
		Size: 4.1 MB (4130524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6144f16900b7c63ff5f07e50d96706eca97e1b1e9be9f15abbf3ba87d5727372`  
		Last Modified: Fri, 14 Jan 2022 18:57:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.0-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:bddc83bad582414e836c7e60fdf5658dabef500b7bc51fb8e18d6247e47f179c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3b7221c7fd3e3c292d74b2b00e056a887bf2fc9e0400f840107de9cca1dfd5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:58:28 GMT
COPY file:c678b429005ddd760afff9930c36320b6468ea514443a740c99ed69f0d9cd889 in /nats-server 
# Fri, 14 Jan 2022 18:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:58:29 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:58:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a42706d8cfe08c4bc9bc324ffc2e0f4757dd092aaaf7dfdb7a98124df24cde2b`  
		Last Modified: Fri, 14 Jan 2022 19:00:55 GMT  
		Size: 4.1 MB (4126980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4780c44069007ad60d46f2985dbe0e7eae3a04d7df9936f14a70b825ec84e73e`  
		Last Modified: Fri, 14 Jan 2022 19:00:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.0-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6404671cd360e397c582b0903bccde0c5ef78c3365c1515c184cf4c3465d06dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15eb321439fe02848e980c416856500b3d8a264944878381ad8ffd1aa1f00e79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:42:45 GMT
COPY file:35de8b46fa873fa93035ad9e0bd8add902aeeb3f777acb6477fe8ae33621069f in /nats-server 
# Fri, 14 Jan 2022 18:42:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:42:46 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:47 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:42:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:99635f3a9fe15a08eb7778c1228079183c996b57cbae1adb68626045408c36c0`  
		Last Modified: Fri, 14 Jan 2022 18:44:02 GMT  
		Size: 4.1 MB (4113430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c443fa2d7386b32c85a9d5d54923637c8b533da17f0755a42f2c3d16ac59b1f8`  
		Last Modified: Fri, 14 Jan 2022 18:44:01 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.0-nanoserver`

```console
$ docker pull nats@sha256:67cbb585b085b43bbb93c9bcce0569c7f180b4d7b9f6374fde7d23083236960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `nats:2.7.0-nanoserver` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:3ff2f0040a64a2cf0a020c4eb0425d13237737b34ecbd6a71b3b32c605bf55c2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107546942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e123bd94ced8bc2f98dc409ee61a0d185c740b720cbdce2ddfdbee78ca5ed5e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 15:13:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:18:56 GMT
RUN cmd /S /C #(nop) COPY file:76b3d6cbfb5183e43d9331cddd3a7f906364b8f5f8f8290ae121e47be5ed179c in C:\nats-server.exe 
# Fri, 14 Jan 2022 18:18:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:19:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:19:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db05d2e76671d91772a070867bf6f050343319070602a0f8239706d5d4d98387`  
		Last Modified: Wed, 12 Jan 2022 15:14:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc49f734ff1c4186abb068d17466f00a620f7903745063b3cc8ccb9492056b1`  
		Last Modified: Fri, 14 Jan 2022 18:19:52 GMT  
		Size: 4.5 MB (4509480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8029445e0be8d33827e442dd586388ee37afb157556c5075c892d3ec04b51b4a`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee34369f11e6432c63a08a695b26eec114e7f590e3e8db49e6ff3c9c6bc69dc`  
		Last Modified: Fri, 14 Jan 2022 18:19:50 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e6014d55a66a18b9b23e3a9d224307e4e729b2131ab80e5d94fe591092f6ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c431522fbf1e1f293b432240df83b2be82c117965a01a88ac9d4f6ce8904569`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.0-nanoserver-1809`

```console
$ docker pull nats@sha256:67cbb585b085b43bbb93c9bcce0569c7f180b4d7b9f6374fde7d23083236960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `nats:2.7.0-nanoserver-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:3ff2f0040a64a2cf0a020c4eb0425d13237737b34ecbd6a71b3b32c605bf55c2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107546942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e123bd94ced8bc2f98dc409ee61a0d185c740b720cbdce2ddfdbee78ca5ed5e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 15:13:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:18:56 GMT
RUN cmd /S /C #(nop) COPY file:76b3d6cbfb5183e43d9331cddd3a7f906364b8f5f8f8290ae121e47be5ed179c in C:\nats-server.exe 
# Fri, 14 Jan 2022 18:18:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:19:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:19:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db05d2e76671d91772a070867bf6f050343319070602a0f8239706d5d4d98387`  
		Last Modified: Wed, 12 Jan 2022 15:14:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc49f734ff1c4186abb068d17466f00a620f7903745063b3cc8ccb9492056b1`  
		Last Modified: Fri, 14 Jan 2022 18:19:52 GMT  
		Size: 4.5 MB (4509480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8029445e0be8d33827e442dd586388ee37afb157556c5075c892d3ec04b51b4a`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee34369f11e6432c63a08a695b26eec114e7f590e3e8db49e6ff3c9c6bc69dc`  
		Last Modified: Fri, 14 Jan 2022 18:19:50 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e6014d55a66a18b9b23e3a9d224307e4e729b2131ab80e5d94fe591092f6ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c431522fbf1e1f293b432240df83b2be82c117965a01a88ac9d4f6ce8904569`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.0-scratch`

```console
$ docker pull nats@sha256:0383d160c6f8689a3e994283699c2c034ce4f0d5f007c389aaf6e52ceb07e169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.0-scratch` - linux; amd64

```console
$ docker pull nats@sha256:b06db068fc05ac9f5c7e8ffc4dce11c880f881a04e0eb40ba835861cec37a7e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a534d8f4e2dc469a50383ab63dfa8e3c1e357e5f0dfa3d5de92592ed4e448864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:24:10 GMT
COPY file:4f0ebc4704f83777a3960e581d523bc013bb02a0cfb7e7f786516a6c49942e22 in /nats-server 
# Fri, 14 Jan 2022 18:24:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:24:11 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:24:11 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:24:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a98137475bb500ddd9f8416278069548db1131298356240d97df07b35a68f05e`  
		Last Modified: Fri, 14 Jan 2022 18:25:51 GMT  
		Size: 4.5 MB (4465555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866493868b198566f99c644afee3c392ed1225753255779f01c03c2bcf9bf89`  
		Last Modified: Fri, 14 Jan 2022 18:25:50 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.0-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:5548af7da41d68083d376352f0043468c1d3392b3ee8cf270074e41efdb7daf4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a6ba83aa0c651bc6443b87ad3aa75aa05a49015c60b0ba94433ed283182e9d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:54:41 GMT
COPY file:0bc79db49bf07145ed2820c48ab480154ad0fe7624645e978e1ab085987118ab in /nats-server 
# Fri, 14 Jan 2022 18:54:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:54:42 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:43 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:54:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1753283a9fe04770710f582c7edb68af20fff43cb6750b511b88edba870b6b0a`  
		Last Modified: Fri, 14 Jan 2022 18:57:08 GMT  
		Size: 4.1 MB (4130524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6144f16900b7c63ff5f07e50d96706eca97e1b1e9be9f15abbf3ba87d5727372`  
		Last Modified: Fri, 14 Jan 2022 18:57:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.0-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bddc83bad582414e836c7e60fdf5658dabef500b7bc51fb8e18d6247e47f179c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3b7221c7fd3e3c292d74b2b00e056a887bf2fc9e0400f840107de9cca1dfd5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:58:28 GMT
COPY file:c678b429005ddd760afff9930c36320b6468ea514443a740c99ed69f0d9cd889 in /nats-server 
# Fri, 14 Jan 2022 18:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:58:29 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:58:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a42706d8cfe08c4bc9bc324ffc2e0f4757dd092aaaf7dfdb7a98124df24cde2b`  
		Last Modified: Fri, 14 Jan 2022 19:00:55 GMT  
		Size: 4.1 MB (4126980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4780c44069007ad60d46f2985dbe0e7eae3a04d7df9936f14a70b825ec84e73e`  
		Last Modified: Fri, 14 Jan 2022 19:00:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.0-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6404671cd360e397c582b0903bccde0c5ef78c3365c1515c184cf4c3465d06dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15eb321439fe02848e980c416856500b3d8a264944878381ad8ffd1aa1f00e79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:42:45 GMT
COPY file:35de8b46fa873fa93035ad9e0bd8add902aeeb3f777acb6477fe8ae33621069f in /nats-server 
# Fri, 14 Jan 2022 18:42:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:42:46 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:47 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:42:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:99635f3a9fe15a08eb7778c1228079183c996b57cbae1adb68626045408c36c0`  
		Last Modified: Fri, 14 Jan 2022 18:44:02 GMT  
		Size: 4.1 MB (4113430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c443fa2d7386b32c85a9d5d54923637c8b533da17f0755a42f2c3d16ac59b1f8`  
		Last Modified: Fri, 14 Jan 2022 18:44:01 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.0-windowsservercore`

```console
$ docker pull nats@sha256:50612c3b2250d06c68ca4b2218715a3c21ceae6dfdb4995a83fa9afbc7881cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `nats:2.7.0-windowsservercore` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:54567f33c76734505d235f002a89b70802128ad108c980307bf03e451f34c9e8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2717410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb238e1dd188f62c4fe45a66109d5ed19abfd1d7e11aebefd90cc3f2da94753`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 22:48:13 GMT
RUN Install update 1809-amd64
# Wed, 12 Jan 2022 13:54:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jan 2022 15:10:29 GMT
ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:15:28 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:15:29 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.0/nats-server-v2.7.0-windows-amd64.zip
# Fri, 14 Jan 2022 18:15:30 GMT
ENV NATS_SERVER_SHASUM=691b1a9e159f749bea7879f7141d1e47f531ae008bdc8426fb7e0085347f7657
# Fri, 14 Jan 2022 18:16:46 GMT
RUN Set-PSDebug -Trace 2
# Fri, 14 Jan 2022 18:18:31 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 14 Jan 2022 18:18:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:33 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:18:34 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:18:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:635f15ebd5b486e8a00bf217a0574a29550e5bbf08c1d021e1e308100b2e49b5`  
		Size: 993.9 MB (993898043 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:537828534783cff318d36854dbda0683aef7263e437c7c669de4092e1778959c`  
		Last Modified: Wed, 12 Jan 2022 15:14:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9576e7772519d67febb0ceb94d8f22531ea99f0c60c36e67a4f5a497c384f5e0`  
		Last Modified: Wed, 12 Jan 2022 15:14:30 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9c40c82e2a4a4f46ef0e92dd0996d9acb6e8c064f6bda7396f48d98a830806`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fc415ca91c0ef702c8be90cf064a0ad853fbc2197f6d23ce4021075c7c31ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cad8ea5aab62c1b4669ca21ee421254265ae0fa526303f34d4d4ce4944a4e3`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4a5b12ef3e0729dc379170f433144469137fb87c269a4a99942ed0a42c38e`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 338.6 KB (338632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187afc1c2121ca26ccb436661e781314b8c0033e5f7d393dfa6482647b35c032`  
		Last Modified: Fri, 14 Jan 2022 18:19:33 GMT  
		Size: 4.8 MB (4827999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f13ff9dec18a932ca99f41132ef4b3d9a9e46885f7a39fe99a066960c3c043`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e0eea58542a95fa0e451371e0304d937be8d6cb6b58b1b00d1325d61053ec9`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd13792fd02f90975cb571d7fbc95735d3ac1f4ea9324bb0ae219fafbe31321`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d46d787da89b4538d3f489455995f217d84669ecf1e402a558d10503d64f32b`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.0-windowsservercore-1809`

```console
$ docker pull nats@sha256:50612c3b2250d06c68ca4b2218715a3c21ceae6dfdb4995a83fa9afbc7881cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `nats:2.7.0-windowsservercore-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:54567f33c76734505d235f002a89b70802128ad108c980307bf03e451f34c9e8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2717410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb238e1dd188f62c4fe45a66109d5ed19abfd1d7e11aebefd90cc3f2da94753`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 22:48:13 GMT
RUN Install update 1809-amd64
# Wed, 12 Jan 2022 13:54:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jan 2022 15:10:29 GMT
ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:15:28 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:15:29 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.0/nats-server-v2.7.0-windows-amd64.zip
# Fri, 14 Jan 2022 18:15:30 GMT
ENV NATS_SERVER_SHASUM=691b1a9e159f749bea7879f7141d1e47f531ae008bdc8426fb7e0085347f7657
# Fri, 14 Jan 2022 18:16:46 GMT
RUN Set-PSDebug -Trace 2
# Fri, 14 Jan 2022 18:18:31 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 14 Jan 2022 18:18:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:33 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:18:34 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:18:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:635f15ebd5b486e8a00bf217a0574a29550e5bbf08c1d021e1e308100b2e49b5`  
		Size: 993.9 MB (993898043 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:537828534783cff318d36854dbda0683aef7263e437c7c669de4092e1778959c`  
		Last Modified: Wed, 12 Jan 2022 15:14:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9576e7772519d67febb0ceb94d8f22531ea99f0c60c36e67a4f5a497c384f5e0`  
		Last Modified: Wed, 12 Jan 2022 15:14:30 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9c40c82e2a4a4f46ef0e92dd0996d9acb6e8c064f6bda7396f48d98a830806`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fc415ca91c0ef702c8be90cf064a0ad853fbc2197f6d23ce4021075c7c31ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cad8ea5aab62c1b4669ca21ee421254265ae0fa526303f34d4d4ce4944a4e3`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4a5b12ef3e0729dc379170f433144469137fb87c269a4a99942ed0a42c38e`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 338.6 KB (338632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187afc1c2121ca26ccb436661e781314b8c0033e5f7d393dfa6482647b35c032`  
		Last Modified: Fri, 14 Jan 2022 18:19:33 GMT  
		Size: 4.8 MB (4827999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f13ff9dec18a932ca99f41132ef4b3d9a9e46885f7a39fe99a066960c3c043`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e0eea58542a95fa0e451371e0304d937be8d6cb6b58b1b00d1325d61053ec9`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd13792fd02f90975cb571d7fbc95735d3ac1f4ea9324bb0ae219fafbe31321`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d46d787da89b4538d3f489455995f217d84669ecf1e402a558d10503d64f32b`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:86f63911d02c7d05e6c62592a784679b1f9cb74b60d10c6c4b4d84bdf773b8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:9d6193c3f8c966a9fd387d258cbfceb3200dc155e5f1a96f6694d4e32215a256
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7569415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b06173b70b1d7bc01311e68328c369c3aba532201c604f9c3f0448368fc71a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:23:38 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:23:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:23:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:23:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:23:41 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:23:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e250c9fddf0251b9995287f56761bb006e4f275b872349f80eb59756e8362097`  
		Last Modified: Fri, 14 Jan 2022 18:24:46 GMT  
		Size: 4.8 MB (4750002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3370d34129abaa0cf5ea03a4de6b432c98e961247e0db58152afef624d5116b6`  
		Last Modified: Fri, 14 Jan 2022 18:24:45 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e699db775f306d056ba3491ef1a78bd60f43f6d84ca190dd5556ab952670bd37`  
		Last Modified: Fri, 14 Jan 2022 18:24:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:9a3ef866b8c56865ef170349f9b6c96434c59b83c8bd00434ac2ba069aa4d1c7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7049035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe56fe3b27ad5f693e36b857dd1234ada2657a84c9066653b1ff0789f912fbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:54:13 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:54:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:54:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:54:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:54:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32aa97c3aebf0246aa45096afee59b2568a296682d22adefa585ddfab52017e1`  
		Last Modified: Fri, 14 Jan 2022 18:56:29 GMT  
		Size: 4.4 MB (4416614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f48d8423c0fa6eb844a29d92e258ae9a33aa6e6cd0b95b4b69a21e72a8e567`  
		Last Modified: Fri, 14 Jan 2022 18:56:27 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8f267cce64b19b253599578af343c8bdcdc79f689ec7d92f4bec4f822e7412`  
		Last Modified: Fri, 14 Jan 2022 18:56:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:d2013f3c37f60a2f02029ff0ed712f0479ef409c7cae118a1ae0521f9a08d2bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6844582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ca3b8a166d5dd0ed044d2e85cc20e4795344ac64a28e513b00faa630c84882`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:57:58 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:58:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:58:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:58:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:58:03 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:58:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07275e3fb0a7b967b5381c0e07db89c39d1cf4e7ee0a649d1c009e78a1d42fa`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 4.4 MB (4408818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835acb2136974c88d21e7071bad202e0d0e39db27d2f0f944858311a7e80f9b4`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1452ec30e6ef252b617a9d46cbd566d7eba05df01f47c577c0d25daaf6d22c`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a1d2244a63e3ab81295587aaae2262e796174a4fa8687a8c872a4442973f50ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7112096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57981de17d5ffc0d33e96bee5e34398ecf77b8501362fca71a6e674fc061594`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:42:28 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:42:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:42:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:42:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:42:33 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:42:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccbd6fe265a7e2fbeca62a169f7f0cb64925946674670bc265127450e775009`  
		Last Modified: Fri, 14 Jan 2022 18:43:34 GMT  
		Size: 4.4 MB (4395688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7772805886c77ac22f41f9354d7d92334e4af6d9404544ee286084143a4c44e`  
		Last Modified: Fri, 14 Jan 2022 18:43:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567aec11ea3ca34811b7531dd4a2d7680c6dd5a7c649133b735ce4517d926f0`  
		Last Modified: Fri, 14 Jan 2022 18:43:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.15`

```console
$ docker pull nats@sha256:86f63911d02c7d05e6c62592a784679b1f9cb74b60d10c6c4b4d84bdf773b8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:9d6193c3f8c966a9fd387d258cbfceb3200dc155e5f1a96f6694d4e32215a256
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7569415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b06173b70b1d7bc01311e68328c369c3aba532201c604f9c3f0448368fc71a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:23:38 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:23:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:23:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:23:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:23:41 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:23:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e250c9fddf0251b9995287f56761bb006e4f275b872349f80eb59756e8362097`  
		Last Modified: Fri, 14 Jan 2022 18:24:46 GMT  
		Size: 4.8 MB (4750002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3370d34129abaa0cf5ea03a4de6b432c98e961247e0db58152afef624d5116b6`  
		Last Modified: Fri, 14 Jan 2022 18:24:45 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e699db775f306d056ba3491ef1a78bd60f43f6d84ca190dd5556ab952670bd37`  
		Last Modified: Fri, 14 Jan 2022 18:24:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:9a3ef866b8c56865ef170349f9b6c96434c59b83c8bd00434ac2ba069aa4d1c7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7049035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe56fe3b27ad5f693e36b857dd1234ada2657a84c9066653b1ff0789f912fbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:54:13 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:54:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:54:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:54:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:54:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32aa97c3aebf0246aa45096afee59b2568a296682d22adefa585ddfab52017e1`  
		Last Modified: Fri, 14 Jan 2022 18:56:29 GMT  
		Size: 4.4 MB (4416614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f48d8423c0fa6eb844a29d92e258ae9a33aa6e6cd0b95b4b69a21e72a8e567`  
		Last Modified: Fri, 14 Jan 2022 18:56:27 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8f267cce64b19b253599578af343c8bdcdc79f689ec7d92f4bec4f822e7412`  
		Last Modified: Fri, 14 Jan 2022 18:56:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:d2013f3c37f60a2f02029ff0ed712f0479ef409c7cae118a1ae0521f9a08d2bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6844582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ca3b8a166d5dd0ed044d2e85cc20e4795344ac64a28e513b00faa630c84882`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:57:58 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:58:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:58:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:58:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:58:03 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:58:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07275e3fb0a7b967b5381c0e07db89c39d1cf4e7ee0a649d1c009e78a1d42fa`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 4.4 MB (4408818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835acb2136974c88d21e7071bad202e0d0e39db27d2f0f944858311a7e80f9b4`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1452ec30e6ef252b617a9d46cbd566d7eba05df01f47c577c0d25daaf6d22c`  
		Last Modified: Fri, 14 Jan 2022 19:00:16 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a1d2244a63e3ab81295587aaae2262e796174a4fa8687a8c872a4442973f50ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7112096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57981de17d5ffc0d33e96bee5e34398ecf77b8501362fca71a6e674fc061594`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:42:28 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:42:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='411928ee9d180a44d9b8f28d3f85f34167f245792a9262fd268881bacd802c9b' ;; 		armhf) natsArch='arm6'; sha256='6fb74518c6f88c29ae9bac0d78db7d64bec6eef9972d5c643cb6e46c3090b67b' ;; 		armv7) natsArch='arm7'; sha256='79f292485c6a14b7a797119eb9a5cea92606dece31ef660e76255c69a6f715cf' ;; 		x86_64) natsArch='amd64'; sha256='b417e27fcec636a8f441788476a6e41b983ce2752793a9a8136ad48e616881a4' ;; 		x86) natsArch='386'; sha256='740afb36dc0d97f51ff7bd9286aa2b9d836b14f1b9f48b2113e7aacc17e6d508' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 14 Jan 2022 18:42:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 14 Jan 2022 18:42:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 14 Jan 2022 18:42:33 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:42:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccbd6fe265a7e2fbeca62a169f7f0cb64925946674670bc265127450e775009`  
		Last Modified: Fri, 14 Jan 2022 18:43:34 GMT  
		Size: 4.4 MB (4395688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7772805886c77ac22f41f9354d7d92334e4af6d9404544ee286084143a4c44e`  
		Last Modified: Fri, 14 Jan 2022 18:43:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567aec11ea3ca34811b7531dd4a2d7680c6dd5a7c649133b735ce4517d926f0`  
		Last Modified: Fri, 14 Jan 2022 18:43:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:08f87dbef4702c335b595c22a60955eda795d9dc2059dc6d5d1692e10f84379a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2452; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:b06db068fc05ac9f5c7e8ffc4dce11c880f881a04e0eb40ba835861cec37a7e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a534d8f4e2dc469a50383ab63dfa8e3c1e357e5f0dfa3d5de92592ed4e448864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:24:10 GMT
COPY file:4f0ebc4704f83777a3960e581d523bc013bb02a0cfb7e7f786516a6c49942e22 in /nats-server 
# Fri, 14 Jan 2022 18:24:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:24:11 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:24:11 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:24:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a98137475bb500ddd9f8416278069548db1131298356240d97df07b35a68f05e`  
		Last Modified: Fri, 14 Jan 2022 18:25:51 GMT  
		Size: 4.5 MB (4465555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866493868b198566f99c644afee3c392ed1225753255779f01c03c2bcf9bf89`  
		Last Modified: Fri, 14 Jan 2022 18:25:50 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:5548af7da41d68083d376352f0043468c1d3392b3ee8cf270074e41efdb7daf4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a6ba83aa0c651bc6443b87ad3aa75aa05a49015c60b0ba94433ed283182e9d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:54:41 GMT
COPY file:0bc79db49bf07145ed2820c48ab480154ad0fe7624645e978e1ab085987118ab in /nats-server 
# Fri, 14 Jan 2022 18:54:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:54:42 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:43 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:54:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1753283a9fe04770710f582c7edb68af20fff43cb6750b511b88edba870b6b0a`  
		Last Modified: Fri, 14 Jan 2022 18:57:08 GMT  
		Size: 4.1 MB (4130524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6144f16900b7c63ff5f07e50d96706eca97e1b1e9be9f15abbf3ba87d5727372`  
		Last Modified: Fri, 14 Jan 2022 18:57:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:bddc83bad582414e836c7e60fdf5658dabef500b7bc51fb8e18d6247e47f179c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3b7221c7fd3e3c292d74b2b00e056a887bf2fc9e0400f840107de9cca1dfd5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:58:28 GMT
COPY file:c678b429005ddd760afff9930c36320b6468ea514443a740c99ed69f0d9cd889 in /nats-server 
# Fri, 14 Jan 2022 18:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:58:29 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:58:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a42706d8cfe08c4bc9bc324ffc2e0f4757dd092aaaf7dfdb7a98124df24cde2b`  
		Last Modified: Fri, 14 Jan 2022 19:00:55 GMT  
		Size: 4.1 MB (4126980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4780c44069007ad60d46f2985dbe0e7eae3a04d7df9936f14a70b825ec84e73e`  
		Last Modified: Fri, 14 Jan 2022 19:00:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6404671cd360e397c582b0903bccde0c5ef78c3365c1515c184cf4c3465d06dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15eb321439fe02848e980c416856500b3d8a264944878381ad8ffd1aa1f00e79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:42:45 GMT
COPY file:35de8b46fa873fa93035ad9e0bd8add902aeeb3f777acb6477fe8ae33621069f in /nats-server 
# Fri, 14 Jan 2022 18:42:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:42:46 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:47 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:42:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:99635f3a9fe15a08eb7778c1228079183c996b57cbae1adb68626045408c36c0`  
		Last Modified: Fri, 14 Jan 2022 18:44:02 GMT  
		Size: 4.1 MB (4113430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c443fa2d7386b32c85a9d5d54923637c8b533da17f0755a42f2c3d16ac59b1f8`  
		Last Modified: Fri, 14 Jan 2022 18:44:01 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:3ff2f0040a64a2cf0a020c4eb0425d13237737b34ecbd6a71b3b32c605bf55c2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107546942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e123bd94ced8bc2f98dc409ee61a0d185c740b720cbdce2ddfdbee78ca5ed5e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 15:13:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:18:56 GMT
RUN cmd /S /C #(nop) COPY file:76b3d6cbfb5183e43d9331cddd3a7f906364b8f5f8f8290ae121e47be5ed179c in C:\nats-server.exe 
# Fri, 14 Jan 2022 18:18:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:19:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:19:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db05d2e76671d91772a070867bf6f050343319070602a0f8239706d5d4d98387`  
		Last Modified: Wed, 12 Jan 2022 15:14:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc49f734ff1c4186abb068d17466f00a620f7903745063b3cc8ccb9492056b1`  
		Last Modified: Fri, 14 Jan 2022 18:19:52 GMT  
		Size: 4.5 MB (4509480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8029445e0be8d33827e442dd586388ee37afb157556c5075c892d3ec04b51b4a`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee34369f11e6432c63a08a695b26eec114e7f590e3e8db49e6ff3c9c6bc69dc`  
		Last Modified: Fri, 14 Jan 2022 18:19:50 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e6014d55a66a18b9b23e3a9d224307e4e729b2131ab80e5d94fe591092f6ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c431522fbf1e1f293b432240df83b2be82c117965a01a88ac9d4f6ce8904569`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:0383d160c6f8689a3e994283699c2c034ce4f0d5f007c389aaf6e52ceb07e169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:b06db068fc05ac9f5c7e8ffc4dce11c880f881a04e0eb40ba835861cec37a7e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a534d8f4e2dc469a50383ab63dfa8e3c1e357e5f0dfa3d5de92592ed4e448864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:24:10 GMT
COPY file:4f0ebc4704f83777a3960e581d523bc013bb02a0cfb7e7f786516a6c49942e22 in /nats-server 
# Fri, 14 Jan 2022 18:24:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:24:11 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:24:11 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:24:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a98137475bb500ddd9f8416278069548db1131298356240d97df07b35a68f05e`  
		Last Modified: Fri, 14 Jan 2022 18:25:51 GMT  
		Size: 4.5 MB (4465555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866493868b198566f99c644afee3c392ed1225753255779f01c03c2bcf9bf89`  
		Last Modified: Fri, 14 Jan 2022 18:25:50 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:5548af7da41d68083d376352f0043468c1d3392b3ee8cf270074e41efdb7daf4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a6ba83aa0c651bc6443b87ad3aa75aa05a49015c60b0ba94433ed283182e9d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:54:41 GMT
COPY file:0bc79db49bf07145ed2820c48ab480154ad0fe7624645e978e1ab085987118ab in /nats-server 
# Fri, 14 Jan 2022 18:54:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:54:42 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:43 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:54:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1753283a9fe04770710f582c7edb68af20fff43cb6750b511b88edba870b6b0a`  
		Last Modified: Fri, 14 Jan 2022 18:57:08 GMT  
		Size: 4.1 MB (4130524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6144f16900b7c63ff5f07e50d96706eca97e1b1e9be9f15abbf3ba87d5727372`  
		Last Modified: Fri, 14 Jan 2022 18:57:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:bddc83bad582414e836c7e60fdf5658dabef500b7bc51fb8e18d6247e47f179c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3b7221c7fd3e3c292d74b2b00e056a887bf2fc9e0400f840107de9cca1dfd5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:58:28 GMT
COPY file:c678b429005ddd760afff9930c36320b6468ea514443a740c99ed69f0d9cd889 in /nats-server 
# Fri, 14 Jan 2022 18:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:58:29 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:58:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a42706d8cfe08c4bc9bc324ffc2e0f4757dd092aaaf7dfdb7a98124df24cde2b`  
		Last Modified: Fri, 14 Jan 2022 19:00:55 GMT  
		Size: 4.1 MB (4126980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4780c44069007ad60d46f2985dbe0e7eae3a04d7df9936f14a70b825ec84e73e`  
		Last Modified: Fri, 14 Jan 2022 19:00:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6404671cd360e397c582b0903bccde0c5ef78c3365c1515c184cf4c3465d06dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15eb321439fe02848e980c416856500b3d8a264944878381ad8ffd1aa1f00e79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:42:45 GMT
COPY file:35de8b46fa873fa93035ad9e0bd8add902aeeb3f777acb6477fe8ae33621069f in /nats-server 
# Fri, 14 Jan 2022 18:42:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:42:46 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:47 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:42:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:99635f3a9fe15a08eb7778c1228079183c996b57cbae1adb68626045408c36c0`  
		Last Modified: Fri, 14 Jan 2022 18:44:02 GMT  
		Size: 4.1 MB (4113430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c443fa2d7386b32c85a9d5d54923637c8b533da17f0755a42f2c3d16ac59b1f8`  
		Last Modified: Fri, 14 Jan 2022 18:44:01 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:67cbb585b085b43bbb93c9bcce0569c7f180b4d7b9f6374fde7d23083236960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `nats:nanoserver` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:3ff2f0040a64a2cf0a020c4eb0425d13237737b34ecbd6a71b3b32c605bf55c2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107546942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e123bd94ced8bc2f98dc409ee61a0d185c740b720cbdce2ddfdbee78ca5ed5e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 15:13:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:18:56 GMT
RUN cmd /S /C #(nop) COPY file:76b3d6cbfb5183e43d9331cddd3a7f906364b8f5f8f8290ae121e47be5ed179c in C:\nats-server.exe 
# Fri, 14 Jan 2022 18:18:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:19:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:19:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db05d2e76671d91772a070867bf6f050343319070602a0f8239706d5d4d98387`  
		Last Modified: Wed, 12 Jan 2022 15:14:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc49f734ff1c4186abb068d17466f00a620f7903745063b3cc8ccb9492056b1`  
		Last Modified: Fri, 14 Jan 2022 18:19:52 GMT  
		Size: 4.5 MB (4509480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8029445e0be8d33827e442dd586388ee37afb157556c5075c892d3ec04b51b4a`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee34369f11e6432c63a08a695b26eec114e7f590e3e8db49e6ff3c9c6bc69dc`  
		Last Modified: Fri, 14 Jan 2022 18:19:50 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e6014d55a66a18b9b23e3a9d224307e4e729b2131ab80e5d94fe591092f6ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c431522fbf1e1f293b432240df83b2be82c117965a01a88ac9d4f6ce8904569`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:67cbb585b085b43bbb93c9bcce0569c7f180b4d7b9f6374fde7d23083236960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:3ff2f0040a64a2cf0a020c4eb0425d13237737b34ecbd6a71b3b32c605bf55c2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107546942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e123bd94ced8bc2f98dc409ee61a0d185c740b720cbdce2ddfdbee78ca5ed5e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 15:13:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:18:56 GMT
RUN cmd /S /C #(nop) COPY file:76b3d6cbfb5183e43d9331cddd3a7f906364b8f5f8f8290ae121e47be5ed179c in C:\nats-server.exe 
# Fri, 14 Jan 2022 18:18:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:19:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:19:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db05d2e76671d91772a070867bf6f050343319070602a0f8239706d5d4d98387`  
		Last Modified: Wed, 12 Jan 2022 15:14:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc49f734ff1c4186abb068d17466f00a620f7903745063b3cc8ccb9492056b1`  
		Last Modified: Fri, 14 Jan 2022 18:19:52 GMT  
		Size: 4.5 MB (4509480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8029445e0be8d33827e442dd586388ee37afb157556c5075c892d3ec04b51b4a`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee34369f11e6432c63a08a695b26eec114e7f590e3e8db49e6ff3c9c6bc69dc`  
		Last Modified: Fri, 14 Jan 2022 18:19:50 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e6014d55a66a18b9b23e3a9d224307e4e729b2131ab80e5d94fe591092f6ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c431522fbf1e1f293b432240df83b2be82c117965a01a88ac9d4f6ce8904569`  
		Last Modified: Fri, 14 Jan 2022 18:19:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:0383d160c6f8689a3e994283699c2c034ce4f0d5f007c389aaf6e52ceb07e169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:b06db068fc05ac9f5c7e8ffc4dce11c880f881a04e0eb40ba835861cec37a7e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a534d8f4e2dc469a50383ab63dfa8e3c1e357e5f0dfa3d5de92592ed4e448864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:24:10 GMT
COPY file:4f0ebc4704f83777a3960e581d523bc013bb02a0cfb7e7f786516a6c49942e22 in /nats-server 
# Fri, 14 Jan 2022 18:24:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:24:11 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:24:11 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:24:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a98137475bb500ddd9f8416278069548db1131298356240d97df07b35a68f05e`  
		Last Modified: Fri, 14 Jan 2022 18:25:51 GMT  
		Size: 4.5 MB (4465555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866493868b198566f99c644afee3c392ed1225753255779f01c03c2bcf9bf89`  
		Last Modified: Fri, 14 Jan 2022 18:25:50 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:5548af7da41d68083d376352f0043468c1d3392b3ee8cf270074e41efdb7daf4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a6ba83aa0c651bc6443b87ad3aa75aa05a49015c60b0ba94433ed283182e9d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:54:41 GMT
COPY file:0bc79db49bf07145ed2820c48ab480154ad0fe7624645e978e1ab085987118ab in /nats-server 
# Fri, 14 Jan 2022 18:54:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:54:42 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:54:43 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:54:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1753283a9fe04770710f582c7edb68af20fff43cb6750b511b88edba870b6b0a`  
		Last Modified: Fri, 14 Jan 2022 18:57:08 GMT  
		Size: 4.1 MB (4130524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6144f16900b7c63ff5f07e50d96706eca97e1b1e9be9f15abbf3ba87d5727372`  
		Last Modified: Fri, 14 Jan 2022 18:57:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bddc83bad582414e836c7e60fdf5658dabef500b7bc51fb8e18d6247e47f179c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3b7221c7fd3e3c292d74b2b00e056a887bf2fc9e0400f840107de9cca1dfd5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:58:28 GMT
COPY file:c678b429005ddd760afff9930c36320b6468ea514443a740c99ed69f0d9cd889 in /nats-server 
# Fri, 14 Jan 2022 18:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:58:29 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:58:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:58:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a42706d8cfe08c4bc9bc324ffc2e0f4757dd092aaaf7dfdb7a98124df24cde2b`  
		Last Modified: Fri, 14 Jan 2022 19:00:55 GMT  
		Size: 4.1 MB (4126980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4780c44069007ad60d46f2985dbe0e7eae3a04d7df9936f14a70b825ec84e73e`  
		Last Modified: Fri, 14 Jan 2022 19:00:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6404671cd360e397c582b0903bccde0c5ef78c3365c1515c184cf4c3465d06dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15eb321439fe02848e980c416856500b3d8a264944878381ad8ffd1aa1f00e79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 14 Jan 2022 18:42:45 GMT
COPY file:35de8b46fa873fa93035ad9e0bd8add902aeeb3f777acb6477fe8ae33621069f in /nats-server 
# Fri, 14 Jan 2022 18:42:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 14 Jan 2022 18:42:46 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:42:47 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 14 Jan 2022 18:42:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:99635f3a9fe15a08eb7778c1228079183c996b57cbae1adb68626045408c36c0`  
		Last Modified: Fri, 14 Jan 2022 18:44:02 GMT  
		Size: 4.1 MB (4113430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c443fa2d7386b32c85a9d5d54923637c8b533da17f0755a42f2c3d16ac59b1f8`  
		Last Modified: Fri, 14 Jan 2022 18:44:01 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:50612c3b2250d06c68ca4b2218715a3c21ceae6dfdb4995a83fa9afbc7881cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `nats:windowsservercore` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:54567f33c76734505d235f002a89b70802128ad108c980307bf03e451f34c9e8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2717410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb238e1dd188f62c4fe45a66109d5ed19abfd1d7e11aebefd90cc3f2da94753`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 22:48:13 GMT
RUN Install update 1809-amd64
# Wed, 12 Jan 2022 13:54:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jan 2022 15:10:29 GMT
ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:15:28 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:15:29 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.0/nats-server-v2.7.0-windows-amd64.zip
# Fri, 14 Jan 2022 18:15:30 GMT
ENV NATS_SERVER_SHASUM=691b1a9e159f749bea7879f7141d1e47f531ae008bdc8426fb7e0085347f7657
# Fri, 14 Jan 2022 18:16:46 GMT
RUN Set-PSDebug -Trace 2
# Fri, 14 Jan 2022 18:18:31 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 14 Jan 2022 18:18:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:33 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:18:34 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:18:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:635f15ebd5b486e8a00bf217a0574a29550e5bbf08c1d021e1e308100b2e49b5`  
		Size: 993.9 MB (993898043 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:537828534783cff318d36854dbda0683aef7263e437c7c669de4092e1778959c`  
		Last Modified: Wed, 12 Jan 2022 15:14:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9576e7772519d67febb0ceb94d8f22531ea99f0c60c36e67a4f5a497c384f5e0`  
		Last Modified: Wed, 12 Jan 2022 15:14:30 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9c40c82e2a4a4f46ef0e92dd0996d9acb6e8c064f6bda7396f48d98a830806`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fc415ca91c0ef702c8be90cf064a0ad853fbc2197f6d23ce4021075c7c31ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cad8ea5aab62c1b4669ca21ee421254265ae0fa526303f34d4d4ce4944a4e3`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4a5b12ef3e0729dc379170f433144469137fb87c269a4a99942ed0a42c38e`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 338.6 KB (338632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187afc1c2121ca26ccb436661e781314b8c0033e5f7d393dfa6482647b35c032`  
		Last Modified: Fri, 14 Jan 2022 18:19:33 GMT  
		Size: 4.8 MB (4827999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f13ff9dec18a932ca99f41132ef4b3d9a9e46885f7a39fe99a066960c3c043`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e0eea58542a95fa0e451371e0304d937be8d6cb6b58b1b00d1325d61053ec9`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd13792fd02f90975cb571d7fbc95735d3ac1f4ea9324bb0ae219fafbe31321`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d46d787da89b4538d3f489455995f217d84669ecf1e402a558d10503d64f32b`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:50612c3b2250d06c68ca4b2218715a3c21ceae6dfdb4995a83fa9afbc7881cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull nats@sha256:54567f33c76734505d235f002a89b70802128ad108c980307bf03e451f34c9e8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2717410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb238e1dd188f62c4fe45a66109d5ed19abfd1d7e11aebefd90cc3f2da94753`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 22:48:13 GMT
RUN Install update 1809-amd64
# Wed, 12 Jan 2022 13:54:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jan 2022 15:10:29 GMT
ENV NATS_DOCKERIZED=1
# Fri, 14 Jan 2022 18:15:28 GMT
ENV NATS_SERVER=2.7.0
# Fri, 14 Jan 2022 18:15:29 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.0/nats-server-v2.7.0-windows-amd64.zip
# Fri, 14 Jan 2022 18:15:30 GMT
ENV NATS_SERVER_SHASUM=691b1a9e159f749bea7879f7141d1e47f531ae008bdc8426fb7e0085347f7657
# Fri, 14 Jan 2022 18:16:46 GMT
RUN Set-PSDebug -Trace 2
# Fri, 14 Jan 2022 18:18:31 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 14 Jan 2022 18:18:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jan 2022 18:18:33 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jan 2022 18:18:34 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jan 2022 18:18:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:635f15ebd5b486e8a00bf217a0574a29550e5bbf08c1d021e1e308100b2e49b5`  
		Size: 993.9 MB (993898043 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:537828534783cff318d36854dbda0683aef7263e437c7c669de4092e1778959c`  
		Last Modified: Wed, 12 Jan 2022 15:14:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9576e7772519d67febb0ceb94d8f22531ea99f0c60c36e67a4f5a497c384f5e0`  
		Last Modified: Wed, 12 Jan 2022 15:14:30 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9c40c82e2a4a4f46ef0e92dd0996d9acb6e8c064f6bda7396f48d98a830806`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fc415ca91c0ef702c8be90cf064a0ad853fbc2197f6d23ce4021075c7c31ba`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cad8ea5aab62c1b4669ca21ee421254265ae0fa526303f34d4d4ce4944a4e3`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4a5b12ef3e0729dc379170f433144469137fb87c269a4a99942ed0a42c38e`  
		Last Modified: Fri, 14 Jan 2022 18:19:34 GMT  
		Size: 338.6 KB (338632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187afc1c2121ca26ccb436661e781314b8c0033e5f7d393dfa6482647b35c032`  
		Last Modified: Fri, 14 Jan 2022 18:19:33 GMT  
		Size: 4.8 MB (4827999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f13ff9dec18a932ca99f41132ef4b3d9a9e46885f7a39fe99a066960c3c043`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e0eea58542a95fa0e451371e0304d937be8d6cb6b58b1b00d1325d61053ec9`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd13792fd02f90975cb571d7fbc95735d3ac1f4ea9324bb0ae219fafbe31321`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d46d787da89b4538d3f489455995f217d84669ecf1e402a558d10503d64f32b`  
		Last Modified: Fri, 14 Jan 2022 18:19:32 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

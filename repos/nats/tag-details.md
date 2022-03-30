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
-	[`nats:2.7.4`](#nats274)
-	[`nats:2.7.4-alpine`](#nats274-alpine)
-	[`nats:2.7.4-alpine3.15`](#nats274-alpine315)
-	[`nats:2.7.4-linux`](#nats274-linux)
-	[`nats:2.7.4-nanoserver`](#nats274-nanoserver)
-	[`nats:2.7.4-nanoserver-1809`](#nats274-nanoserver-1809)
-	[`nats:2.7.4-scratch`](#nats274-scratch)
-	[`nats:2.7.4-windowsservercore`](#nats274-windowsservercore)
-	[`nats:2.7.4-windowsservercore-1809`](#nats274-windowsservercore-1809)
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
$ docker pull nats@sha256:6f86d5bac0f78b01cf5f9f707008403b0792ff5029817f8afc23c895c5215cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2686; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:5102d9ad6d58bc95c08d14e8fe54b4cb432ac9237cec01d33dcbd8e4850cf447
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4510590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d053ccf4f981153bfbc620038e1ef8f4350bd08832ada50fb0a0fba84572be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:02a472480673a11c995d1ea52b63c55910490337313c1211b4877f5071117f27 in /nats-server 
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:25:51 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:25:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:25:51 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:25:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9292be658bded2e584005b2d2d3c989d58b8c84c43d30cbf498884e4da11d88`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 4.5 MB (4510082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053a12f02cf2d3d90a7d26739c64349d29833ccb5f6d04c6b28d8fff2443538`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:3256353a8d53c6257a1ec8c17b572529f87360bf3b105b470da8998266e05315
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5335fe9c64c80865dd34d7f1d94b52b6d4038ce714fb04d9f318a0393262dac7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:06:00 GMT
COPY file:63d2dc292853c2a6d99433d1e8a92c091a0c775ab65a2e453be73d5448e05594 in /nats-server 
# Wed, 09 Mar 2022 23:06:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:06:01 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:06:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:06:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:06:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c9142de49642e016c3df123dce55998ce71f3777b9433742a88aa91b23f9ae9`  
		Last Modified: Wed, 09 Mar 2022 23:08:21 GMT  
		Size: 4.2 MB (4174056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232eee2ffad4b2ab84d1a4aafd3be0df1c1066f57eab6f18a4b55344b74488be`  
		Last Modified: Wed, 09 Mar 2022 23:08:18 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:ed87fc96ebeace8ad252ad368ab68f1ef976daadae90f50d8f1f917364b8050c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c348e474d9b30a28b01ce9d8566ee12c3404e1a91cddfa31c8de44ba3c6b495b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:26:11 GMT
COPY file:143b3802bb689cd4b4badd2b1463feaa3881f20e6fd303b203aa25ea206fb684 in /nats-server 
# Wed, 09 Mar 2022 23:26:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:26:12 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:26:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:26:13 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c0d2f46ac12a6f6109f1f810a72658a0faa0b7301dfa2abc4f222012bab43639`  
		Last Modified: Wed, 09 Mar 2022 23:28:32 GMT  
		Size: 4.2 MB (4168878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4e39b35a6f91da4330c0e57dcc7c9e91270e4d54cf1097b98ad3ab1a1ca178`  
		Last Modified: Wed, 09 Mar 2022 23:28:29 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4cb4ef773edd64ce015945185e30502ff5c80ea967e3ebbdf0f8d3751016ff45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bb252022527ea75cce7f45ea7463fe04e9e5b5628152fb157822c0d01bc139`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:57:14 GMT
COPY file:6d6603ade462e58030bc93029992af55dac8b9eae7e4985b5c84dd49e1ee1be2 in /nats-server 
# Wed, 09 Mar 2022 22:57:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:57:15 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:57:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:57:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5663127c1a3d9c378ea8ac20e94b430188a9dbb2675ca0b26205f9a5e1b0bf36`  
		Last Modified: Wed, 09 Mar 2022 22:58:35 GMT  
		Size: 4.2 MB (4154114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc2c19c0a6d2b137b1891d3ee3716153114e9575e2a1bc966dd0660a4c7b72`  
		Last Modified: Wed, 09 Mar 2022 22:58:34 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:6d00c243dc589b03baf20fbe8c0a81279a5725d0774b275bbb9c3ebe329b570e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107611006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888ad60fdeb9e43dbbe336530422e503f539089048145cc1bbea7e51905b7095`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:16:59 GMT
RUN cmd /S /C #(nop) COPY file:741c07610cba7dd6badafc477fe411065386e3878f26a0bf50ed1d89036d6dcf in C:\nats-server.exe 
# Wed, 09 Mar 2022 23:17:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:17:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e02f868f2bb74e07262227b1156e17be47c4d960be7e9270cca8bc1dc6635b`  
		Last Modified: Wed, 09 Mar 2022 23:17:53 GMT  
		Size: 4.6 MB (4550038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9514eaf2c4a0d45ed2033bb85089d1fa90e61da7d517358225b5c6739051fcd7`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497be159edf0b99569392570b882cb48a2e72386befcbe1a0f454c6c02dba990`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c889054d0bd6db85b4b9c71958f5f7b8a6679ee127a701a521ee74961a3a528`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10493cee89e77ec8ec7093f8359147e7040171cbe811996808f6f1b860c78db`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:6bc6e4354e204e2b5a605bdbe7e36c95a99cd8075aa0da75292eec39b78fc2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:ddbbfa522c3602ac76b51284c184828f24be9fcb329665c8c835d0a0b5f71609
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33323e6971854b66bb8ff96bd008fee5ae9fea9f9118b96fd68ee148e42bef21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:04:37 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 12:04:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 12:04:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 12:04:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 12:04:39 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 12:04:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 12:04:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9a10b3bb713cc8101378783c4f52f75d8f834fa21f5fc136a30904bfcb4f9f`  
		Last Modified: Tue, 29 Mar 2022 12:05:12 GMT  
		Size: 4.8 MB (4783177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb87d96c1921472cce8519d8fb67b430106edf099c364e068ceecefd4ba7e00`  
		Last Modified: Tue, 29 Mar 2022 12:05:11 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c21f97f27e2c9ba2af1a903b9062eb0b884a9a6992c9d8964ecd84a2348cae`  
		Last Modified: Tue, 29 Mar 2022 12:05:11 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3fee8925082b25042ab9087ddcc5c293a612850d5244cb7775af22caca1f6d9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7070564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4e309ef1582f25174193504f16ecbc35a11f70c720953171928ee47ae18c5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:08:37 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 08:08:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 08:08:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 08:08:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 08:08:43 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 08:08:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:08:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5433d34ffede9d0eff77eaf04849e4b79ec0f7e200a2d117f5e58a50e0b82217`  
		Last Modified: Tue, 29 Mar 2022 08:10:45 GMT  
		Size: 4.4 MB (4447623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df1c1e8b65688f71ac5b1bd33b8077ef7a6394d79c1ec7dffcbc7914484d48c`  
		Last Modified: Tue, 29 Mar 2022 08:10:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da97cd054d0f3a42979a00c4d9c8a3255934903076031d8ecb9f73355e33cdc6`  
		Last Modified: Tue, 29 Mar 2022 08:10:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b8830dffd27a635e2d80d20fe9e49d0d4192fb89ee89cefad2386db8310c9f55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6869438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5fcef1f127b912a6983b0d1760f725714bd3d51423e173685ce10bc75c3c61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 21:56:38 GMT
ENV NATS_SERVER=2.7.4
# Wed, 23 Mar 2022 21:56:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 23 Mar 2022 21:56:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 23 Mar 2022 21:56:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 23 Mar 2022 21:56:43 GMT
EXPOSE 4222 6222 8222
# Wed, 23 Mar 2022 21:56:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 21:56:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8365d9448ab73a0b9418881d07622e7c116779f5f7ff600dcfbdc018626535`  
		Last Modified: Wed, 23 Mar 2022 21:58:49 GMT  
		Size: 4.4 MB (4441374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0ff5fa9c85f9c3dd3da4265f384e11366cecd9c22f80631d9be6411ca26f5a`  
		Last Modified: Wed, 23 Mar 2022 21:58:45 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0fbe9b4a8938c2752473cad2d4c7fedcf260481989f3d2ed6ae3a16890c0d6`  
		Last Modified: Wed, 23 Mar 2022 21:58:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e1d92c67b112506e1eba438169cabbae1e7df652747fced40ee09e49016709
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc357f18f7318c9dd8b86a35d7f8ade6041903325fe61edd036d0423b4ac7bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 19:27:05 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 19:27:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 19:27:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 19:27:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 19:27:11 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 19:27:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 19:27:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6838fdfa81afc565c161c1fee30401de3a013bfb571f5be3c3a993badc92f3f`  
		Last Modified: Tue, 29 Mar 2022 19:28:11 GMT  
		Size: 4.4 MB (4426412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dce858aad644833ca99f39e8757136a768b7f8ecfaae59ac4154e3823651dd`  
		Last Modified: Tue, 29 Mar 2022 19:28:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a6ab0d728bdc5bcab9e3d3e9236d289a5888dd54c1cd6cade53e1cac8f5c2`  
		Last Modified: Tue, 29 Mar 2022 19:28:11 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.15`

```console
$ docker pull nats@sha256:6bc6e4354e204e2b5a605bdbe7e36c95a99cd8075aa0da75292eec39b78fc2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:ddbbfa522c3602ac76b51284c184828f24be9fcb329665c8c835d0a0b5f71609
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33323e6971854b66bb8ff96bd008fee5ae9fea9f9118b96fd68ee148e42bef21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:04:37 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 12:04:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 12:04:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 12:04:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 12:04:39 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 12:04:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 12:04:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9a10b3bb713cc8101378783c4f52f75d8f834fa21f5fc136a30904bfcb4f9f`  
		Last Modified: Tue, 29 Mar 2022 12:05:12 GMT  
		Size: 4.8 MB (4783177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb87d96c1921472cce8519d8fb67b430106edf099c364e068ceecefd4ba7e00`  
		Last Modified: Tue, 29 Mar 2022 12:05:11 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c21f97f27e2c9ba2af1a903b9062eb0b884a9a6992c9d8964ecd84a2348cae`  
		Last Modified: Tue, 29 Mar 2022 12:05:11 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:3fee8925082b25042ab9087ddcc5c293a612850d5244cb7775af22caca1f6d9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7070564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4e309ef1582f25174193504f16ecbc35a11f70c720953171928ee47ae18c5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:08:37 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 08:08:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 08:08:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 08:08:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 08:08:43 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 08:08:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:08:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5433d34ffede9d0eff77eaf04849e4b79ec0f7e200a2d117f5e58a50e0b82217`  
		Last Modified: Tue, 29 Mar 2022 08:10:45 GMT  
		Size: 4.4 MB (4447623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df1c1e8b65688f71ac5b1bd33b8077ef7a6394d79c1ec7dffcbc7914484d48c`  
		Last Modified: Tue, 29 Mar 2022 08:10:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da97cd054d0f3a42979a00c4d9c8a3255934903076031d8ecb9f73355e33cdc6`  
		Last Modified: Tue, 29 Mar 2022 08:10:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:b8830dffd27a635e2d80d20fe9e49d0d4192fb89ee89cefad2386db8310c9f55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6869438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5fcef1f127b912a6983b0d1760f725714bd3d51423e173685ce10bc75c3c61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 21:56:38 GMT
ENV NATS_SERVER=2.7.4
# Wed, 23 Mar 2022 21:56:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 23 Mar 2022 21:56:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 23 Mar 2022 21:56:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 23 Mar 2022 21:56:43 GMT
EXPOSE 4222 6222 8222
# Wed, 23 Mar 2022 21:56:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 21:56:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8365d9448ab73a0b9418881d07622e7c116779f5f7ff600dcfbdc018626535`  
		Last Modified: Wed, 23 Mar 2022 21:58:49 GMT  
		Size: 4.4 MB (4441374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0ff5fa9c85f9c3dd3da4265f384e11366cecd9c22f80631d9be6411ca26f5a`  
		Last Modified: Wed, 23 Mar 2022 21:58:45 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0fbe9b4a8938c2752473cad2d4c7fedcf260481989f3d2ed6ae3a16890c0d6`  
		Last Modified: Wed, 23 Mar 2022 21:58:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e1d92c67b112506e1eba438169cabbae1e7df652747fced40ee09e49016709
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc357f18f7318c9dd8b86a35d7f8ade6041903325fe61edd036d0423b4ac7bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 19:27:05 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 19:27:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 19:27:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 19:27:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 19:27:11 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 19:27:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 19:27:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6838fdfa81afc565c161c1fee30401de3a013bfb571f5be3c3a993badc92f3f`  
		Last Modified: Tue, 29 Mar 2022 19:28:11 GMT  
		Size: 4.4 MB (4426412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dce858aad644833ca99f39e8757136a768b7f8ecfaae59ac4154e3823651dd`  
		Last Modified: Tue, 29 Mar 2022 19:28:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a6ab0d728bdc5bcab9e3d3e9236d289a5888dd54c1cd6cade53e1cac8f5c2`  
		Last Modified: Tue, 29 Mar 2022 19:28:11 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:162126c602bcb3293ff5401b486cba4da6a3df5ed3b28758b1e9b11faeb382e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:5102d9ad6d58bc95c08d14e8fe54b4cb432ac9237cec01d33dcbd8e4850cf447
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4510590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d053ccf4f981153bfbc620038e1ef8f4350bd08832ada50fb0a0fba84572be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:02a472480673a11c995d1ea52b63c55910490337313c1211b4877f5071117f27 in /nats-server 
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:25:51 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:25:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:25:51 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:25:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9292be658bded2e584005b2d2d3c989d58b8c84c43d30cbf498884e4da11d88`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 4.5 MB (4510082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053a12f02cf2d3d90a7d26739c64349d29833ccb5f6d04c6b28d8fff2443538`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:3256353a8d53c6257a1ec8c17b572529f87360bf3b105b470da8998266e05315
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5335fe9c64c80865dd34d7f1d94b52b6d4038ce714fb04d9f318a0393262dac7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:06:00 GMT
COPY file:63d2dc292853c2a6d99433d1e8a92c091a0c775ab65a2e453be73d5448e05594 in /nats-server 
# Wed, 09 Mar 2022 23:06:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:06:01 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:06:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:06:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:06:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c9142de49642e016c3df123dce55998ce71f3777b9433742a88aa91b23f9ae9`  
		Last Modified: Wed, 09 Mar 2022 23:08:21 GMT  
		Size: 4.2 MB (4174056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232eee2ffad4b2ab84d1a4aafd3be0df1c1066f57eab6f18a4b55344b74488be`  
		Last Modified: Wed, 09 Mar 2022 23:08:18 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:ed87fc96ebeace8ad252ad368ab68f1ef976daadae90f50d8f1f917364b8050c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c348e474d9b30a28b01ce9d8566ee12c3404e1a91cddfa31c8de44ba3c6b495b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:26:11 GMT
COPY file:143b3802bb689cd4b4badd2b1463feaa3881f20e6fd303b203aa25ea206fb684 in /nats-server 
# Wed, 09 Mar 2022 23:26:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:26:12 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:26:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:26:13 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c0d2f46ac12a6f6109f1f810a72658a0faa0b7301dfa2abc4f222012bab43639`  
		Last Modified: Wed, 09 Mar 2022 23:28:32 GMT  
		Size: 4.2 MB (4168878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4e39b35a6f91da4330c0e57dcc7c9e91270e4d54cf1097b98ad3ab1a1ca178`  
		Last Modified: Wed, 09 Mar 2022 23:28:29 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4cb4ef773edd64ce015945185e30502ff5c80ea967e3ebbdf0f8d3751016ff45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bb252022527ea75cce7f45ea7463fe04e9e5b5628152fb157822c0d01bc139`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:57:14 GMT
COPY file:6d6603ade462e58030bc93029992af55dac8b9eae7e4985b5c84dd49e1ee1be2 in /nats-server 
# Wed, 09 Mar 2022 22:57:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:57:15 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:57:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:57:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5663127c1a3d9c378ea8ac20e94b430188a9dbb2675ca0b26205f9a5e1b0bf36`  
		Last Modified: Wed, 09 Mar 2022 22:58:35 GMT  
		Size: 4.2 MB (4154114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc2c19c0a6d2b137b1891d3ee3716153114e9575e2a1bc966dd0660a4c7b72`  
		Last Modified: Wed, 09 Mar 2022 22:58:34 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:9654461ee3015e4abac8d6f24720ec089a72db6650768ac224cd6280735a70f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:6d00c243dc589b03baf20fbe8c0a81279a5725d0774b275bbb9c3ebe329b570e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107611006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888ad60fdeb9e43dbbe336530422e503f539089048145cc1bbea7e51905b7095`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:16:59 GMT
RUN cmd /S /C #(nop) COPY file:741c07610cba7dd6badafc477fe411065386e3878f26a0bf50ed1d89036d6dcf in C:\nats-server.exe 
# Wed, 09 Mar 2022 23:17:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:17:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e02f868f2bb74e07262227b1156e17be47c4d960be7e9270cca8bc1dc6635b`  
		Last Modified: Wed, 09 Mar 2022 23:17:53 GMT  
		Size: 4.6 MB (4550038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9514eaf2c4a0d45ed2033bb85089d1fa90e61da7d517358225b5c6739051fcd7`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497be159edf0b99569392570b882cb48a2e72386befcbe1a0f454c6c02dba990`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c889054d0bd6db85b4b9c71958f5f7b8a6679ee127a701a521ee74961a3a528`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10493cee89e77ec8ec7093f8359147e7040171cbe811996808f6f1b860c78db`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:9654461ee3015e4abac8d6f24720ec089a72db6650768ac224cd6280735a70f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:6d00c243dc589b03baf20fbe8c0a81279a5725d0774b275bbb9c3ebe329b570e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107611006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888ad60fdeb9e43dbbe336530422e503f539089048145cc1bbea7e51905b7095`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:16:59 GMT
RUN cmd /S /C #(nop) COPY file:741c07610cba7dd6badafc477fe411065386e3878f26a0bf50ed1d89036d6dcf in C:\nats-server.exe 
# Wed, 09 Mar 2022 23:17:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:17:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e02f868f2bb74e07262227b1156e17be47c4d960be7e9270cca8bc1dc6635b`  
		Last Modified: Wed, 09 Mar 2022 23:17:53 GMT  
		Size: 4.6 MB (4550038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9514eaf2c4a0d45ed2033bb85089d1fa90e61da7d517358225b5c6739051fcd7`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497be159edf0b99569392570b882cb48a2e72386befcbe1a0f454c6c02dba990`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c889054d0bd6db85b4b9c71958f5f7b8a6679ee127a701a521ee74961a3a528`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10493cee89e77ec8ec7093f8359147e7040171cbe811996808f6f1b860c78db`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:162126c602bcb3293ff5401b486cba4da6a3df5ed3b28758b1e9b11faeb382e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:5102d9ad6d58bc95c08d14e8fe54b4cb432ac9237cec01d33dcbd8e4850cf447
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4510590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d053ccf4f981153bfbc620038e1ef8f4350bd08832ada50fb0a0fba84572be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:02a472480673a11c995d1ea52b63c55910490337313c1211b4877f5071117f27 in /nats-server 
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:25:51 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:25:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:25:51 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:25:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9292be658bded2e584005b2d2d3c989d58b8c84c43d30cbf498884e4da11d88`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 4.5 MB (4510082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053a12f02cf2d3d90a7d26739c64349d29833ccb5f6d04c6b28d8fff2443538`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:3256353a8d53c6257a1ec8c17b572529f87360bf3b105b470da8998266e05315
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5335fe9c64c80865dd34d7f1d94b52b6d4038ce714fb04d9f318a0393262dac7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:06:00 GMT
COPY file:63d2dc292853c2a6d99433d1e8a92c091a0c775ab65a2e453be73d5448e05594 in /nats-server 
# Wed, 09 Mar 2022 23:06:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:06:01 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:06:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:06:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:06:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c9142de49642e016c3df123dce55998ce71f3777b9433742a88aa91b23f9ae9`  
		Last Modified: Wed, 09 Mar 2022 23:08:21 GMT  
		Size: 4.2 MB (4174056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232eee2ffad4b2ab84d1a4aafd3be0df1c1066f57eab6f18a4b55344b74488be`  
		Last Modified: Wed, 09 Mar 2022 23:08:18 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:ed87fc96ebeace8ad252ad368ab68f1ef976daadae90f50d8f1f917364b8050c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c348e474d9b30a28b01ce9d8566ee12c3404e1a91cddfa31c8de44ba3c6b495b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:26:11 GMT
COPY file:143b3802bb689cd4b4badd2b1463feaa3881f20e6fd303b203aa25ea206fb684 in /nats-server 
# Wed, 09 Mar 2022 23:26:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:26:12 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:26:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:26:13 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c0d2f46ac12a6f6109f1f810a72658a0faa0b7301dfa2abc4f222012bab43639`  
		Last Modified: Wed, 09 Mar 2022 23:28:32 GMT  
		Size: 4.2 MB (4168878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4e39b35a6f91da4330c0e57dcc7c9e91270e4d54cf1097b98ad3ab1a1ca178`  
		Last Modified: Wed, 09 Mar 2022 23:28:29 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4cb4ef773edd64ce015945185e30502ff5c80ea967e3ebbdf0f8d3751016ff45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bb252022527ea75cce7f45ea7463fe04e9e5b5628152fb157822c0d01bc139`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:57:14 GMT
COPY file:6d6603ade462e58030bc93029992af55dac8b9eae7e4985b5c84dd49e1ee1be2 in /nats-server 
# Wed, 09 Mar 2022 22:57:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:57:15 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:57:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:57:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5663127c1a3d9c378ea8ac20e94b430188a9dbb2675ca0b26205f9a5e1b0bf36`  
		Last Modified: Wed, 09 Mar 2022 22:58:35 GMT  
		Size: 4.2 MB (4154114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc2c19c0a6d2b137b1891d3ee3716153114e9575e2a1bc966dd0660a4c7b72`  
		Last Modified: Wed, 09 Mar 2022 22:58:34 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:de7fa8eefd8b38a00c8f113294fc03f91486cde9b572b109e98f44f2ffbf5b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:ebc084a1a8e19ddf44701886869f9009dccaf6485d52d791799326d6f89ab0d2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720689430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f84a261eca9a7469f56f24e432d4ea475732107a3ab4cf28174ee49e3ba364b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:14:16 GMT
ENV NATS_SERVER=2.7.4
# Wed, 09 Mar 2022 23:14:17 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.4/nats-server-v2.7.4-windows-amd64.zip
# Wed, 09 Mar 2022 23:14:18 GMT
ENV NATS_SERVER_SHASUM=0c98c505391e781f5f528817099dc727d83c997b3d48032c0f111d1452e8489b
# Wed, 09 Mar 2022 23:15:14 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:16:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:16:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:16:40 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:16:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:16:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301e780f30b10c083782e0d53ed487fd4d8f8d32ad6c9b9fd84d2fcc0745ee60`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7e8b0a6cef1b2ea81fcb039bc420172f4a60c3f329e6b495f9e1133e3e1534`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844fdd93ebcdfae84a099cefa8da35deaa056bff22b968bebf99205facdf928f`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f545db8b309b5166354fd80028d4bda3d85af353da1959ab615769a430d1c0`  
		Last Modified: Wed, 09 Mar 2022 23:17:34 GMT  
		Size: 348.6 KB (348621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502abb43626a3eb4c75cb441213dbb73cbb7b0df0b28ff4d77b4420ebeb536e9`  
		Last Modified: Wed, 09 Mar 2022 23:17:36 GMT  
		Size: 4.9 MB (4874834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cef267e6b969aa61db520018b018b4244a92bbceda7eba76208a24bf2bcfbaf`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57f349791c768e9ea1eaf48b6c342b2038779b4cdca397333cc20c73ded703`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06857fcc2d8c8a67e6e493c5d95e54a6bded7af6103d139e4a59072664088bff`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62c41a5b49cd11c0da902b5333c829bcc21ffcb561d931fc457eafa36ee6bc9`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:de7fa8eefd8b38a00c8f113294fc03f91486cde9b572b109e98f44f2ffbf5b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:ebc084a1a8e19ddf44701886869f9009dccaf6485d52d791799326d6f89ab0d2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720689430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f84a261eca9a7469f56f24e432d4ea475732107a3ab4cf28174ee49e3ba364b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:14:16 GMT
ENV NATS_SERVER=2.7.4
# Wed, 09 Mar 2022 23:14:17 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.4/nats-server-v2.7.4-windows-amd64.zip
# Wed, 09 Mar 2022 23:14:18 GMT
ENV NATS_SERVER_SHASUM=0c98c505391e781f5f528817099dc727d83c997b3d48032c0f111d1452e8489b
# Wed, 09 Mar 2022 23:15:14 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:16:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:16:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:16:40 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:16:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:16:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301e780f30b10c083782e0d53ed487fd4d8f8d32ad6c9b9fd84d2fcc0745ee60`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7e8b0a6cef1b2ea81fcb039bc420172f4a60c3f329e6b495f9e1133e3e1534`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844fdd93ebcdfae84a099cefa8da35deaa056bff22b968bebf99205facdf928f`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f545db8b309b5166354fd80028d4bda3d85af353da1959ab615769a430d1c0`  
		Last Modified: Wed, 09 Mar 2022 23:17:34 GMT  
		Size: 348.6 KB (348621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502abb43626a3eb4c75cb441213dbb73cbb7b0df0b28ff4d77b4420ebeb536e9`  
		Last Modified: Wed, 09 Mar 2022 23:17:36 GMT  
		Size: 4.9 MB (4874834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cef267e6b969aa61db520018b018b4244a92bbceda7eba76208a24bf2bcfbaf`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57f349791c768e9ea1eaf48b6c342b2038779b4cdca397333cc20c73ded703`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06857fcc2d8c8a67e6e493c5d95e54a6bded7af6103d139e4a59072664088bff`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62c41a5b49cd11c0da902b5333c829bcc21ffcb561d931fc457eafa36ee6bc9`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7`

```console
$ docker pull nats@sha256:6f86d5bac0f78b01cf5f9f707008403b0792ff5029817f8afc23c895c5215cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7` - linux; amd64

```console
$ docker pull nats@sha256:5102d9ad6d58bc95c08d14e8fe54b4cb432ac9237cec01d33dcbd8e4850cf447
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4510590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d053ccf4f981153bfbc620038e1ef8f4350bd08832ada50fb0a0fba84572be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:02a472480673a11c995d1ea52b63c55910490337313c1211b4877f5071117f27 in /nats-server 
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:25:51 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:25:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:25:51 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:25:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9292be658bded2e584005b2d2d3c989d58b8c84c43d30cbf498884e4da11d88`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 4.5 MB (4510082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053a12f02cf2d3d90a7d26739c64349d29833ccb5f6d04c6b28d8fff2443538`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - linux; arm variant v6

```console
$ docker pull nats@sha256:3256353a8d53c6257a1ec8c17b572529f87360bf3b105b470da8998266e05315
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5335fe9c64c80865dd34d7f1d94b52b6d4038ce714fb04d9f318a0393262dac7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:06:00 GMT
COPY file:63d2dc292853c2a6d99433d1e8a92c091a0c775ab65a2e453be73d5448e05594 in /nats-server 
# Wed, 09 Mar 2022 23:06:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:06:01 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:06:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:06:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:06:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c9142de49642e016c3df123dce55998ce71f3777b9433742a88aa91b23f9ae9`  
		Last Modified: Wed, 09 Mar 2022 23:08:21 GMT  
		Size: 4.2 MB (4174056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232eee2ffad4b2ab84d1a4aafd3be0df1c1066f57eab6f18a4b55344b74488be`  
		Last Modified: Wed, 09 Mar 2022 23:08:18 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - linux; arm variant v7

```console
$ docker pull nats@sha256:ed87fc96ebeace8ad252ad368ab68f1ef976daadae90f50d8f1f917364b8050c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c348e474d9b30a28b01ce9d8566ee12c3404e1a91cddfa31c8de44ba3c6b495b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:26:11 GMT
COPY file:143b3802bb689cd4b4badd2b1463feaa3881f20e6fd303b203aa25ea206fb684 in /nats-server 
# Wed, 09 Mar 2022 23:26:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:26:12 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:26:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:26:13 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c0d2f46ac12a6f6109f1f810a72658a0faa0b7301dfa2abc4f222012bab43639`  
		Last Modified: Wed, 09 Mar 2022 23:28:32 GMT  
		Size: 4.2 MB (4168878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4e39b35a6f91da4330c0e57dcc7c9e91270e4d54cf1097b98ad3ab1a1ca178`  
		Last Modified: Wed, 09 Mar 2022 23:28:29 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4cb4ef773edd64ce015945185e30502ff5c80ea967e3ebbdf0f8d3751016ff45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bb252022527ea75cce7f45ea7463fe04e9e5b5628152fb157822c0d01bc139`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:57:14 GMT
COPY file:6d6603ade462e58030bc93029992af55dac8b9eae7e4985b5c84dd49e1ee1be2 in /nats-server 
# Wed, 09 Mar 2022 22:57:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:57:15 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:57:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:57:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5663127c1a3d9c378ea8ac20e94b430188a9dbb2675ca0b26205f9a5e1b0bf36`  
		Last Modified: Wed, 09 Mar 2022 22:58:35 GMT  
		Size: 4.2 MB (4154114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc2c19c0a6d2b137b1891d3ee3716153114e9575e2a1bc966dd0660a4c7b72`  
		Last Modified: Wed, 09 Mar 2022 22:58:34 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:6d00c243dc589b03baf20fbe8c0a81279a5725d0774b275bbb9c3ebe329b570e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107611006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888ad60fdeb9e43dbbe336530422e503f539089048145cc1bbea7e51905b7095`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:16:59 GMT
RUN cmd /S /C #(nop) COPY file:741c07610cba7dd6badafc477fe411065386e3878f26a0bf50ed1d89036d6dcf in C:\nats-server.exe 
# Wed, 09 Mar 2022 23:17:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:17:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e02f868f2bb74e07262227b1156e17be47c4d960be7e9270cca8bc1dc6635b`  
		Last Modified: Wed, 09 Mar 2022 23:17:53 GMT  
		Size: 4.6 MB (4550038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9514eaf2c4a0d45ed2033bb85089d1fa90e61da7d517358225b5c6739051fcd7`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497be159edf0b99569392570b882cb48a2e72386befcbe1a0f454c6c02dba990`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c889054d0bd6db85b4b9c71958f5f7b8a6679ee127a701a521ee74961a3a528`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10493cee89e77ec8ec7093f8359147e7040171cbe811996808f6f1b860c78db`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-alpine`

```console
$ docker pull nats@sha256:6bc6e4354e204e2b5a605bdbe7e36c95a99cd8075aa0da75292eec39b78fc2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-alpine` - linux; amd64

```console
$ docker pull nats@sha256:ddbbfa522c3602ac76b51284c184828f24be9fcb329665c8c835d0a0b5f71609
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33323e6971854b66bb8ff96bd008fee5ae9fea9f9118b96fd68ee148e42bef21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:04:37 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 12:04:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 12:04:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 12:04:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 12:04:39 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 12:04:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 12:04:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9a10b3bb713cc8101378783c4f52f75d8f834fa21f5fc136a30904bfcb4f9f`  
		Last Modified: Tue, 29 Mar 2022 12:05:12 GMT  
		Size: 4.8 MB (4783177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb87d96c1921472cce8519d8fb67b430106edf099c364e068ceecefd4ba7e00`  
		Last Modified: Tue, 29 Mar 2022 12:05:11 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c21f97f27e2c9ba2af1a903b9062eb0b884a9a6992c9d8964ecd84a2348cae`  
		Last Modified: Tue, 29 Mar 2022 12:05:11 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3fee8925082b25042ab9087ddcc5c293a612850d5244cb7775af22caca1f6d9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7070564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4e309ef1582f25174193504f16ecbc35a11f70c720953171928ee47ae18c5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:08:37 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 08:08:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 08:08:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 08:08:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 08:08:43 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 08:08:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:08:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5433d34ffede9d0eff77eaf04849e4b79ec0f7e200a2d117f5e58a50e0b82217`  
		Last Modified: Tue, 29 Mar 2022 08:10:45 GMT  
		Size: 4.4 MB (4447623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df1c1e8b65688f71ac5b1bd33b8077ef7a6394d79c1ec7dffcbc7914484d48c`  
		Last Modified: Tue, 29 Mar 2022 08:10:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da97cd054d0f3a42979a00c4d9c8a3255934903076031d8ecb9f73355e33cdc6`  
		Last Modified: Tue, 29 Mar 2022 08:10:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b8830dffd27a635e2d80d20fe9e49d0d4192fb89ee89cefad2386db8310c9f55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6869438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5fcef1f127b912a6983b0d1760f725714bd3d51423e173685ce10bc75c3c61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 21:56:38 GMT
ENV NATS_SERVER=2.7.4
# Wed, 23 Mar 2022 21:56:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 23 Mar 2022 21:56:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 23 Mar 2022 21:56:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 23 Mar 2022 21:56:43 GMT
EXPOSE 4222 6222 8222
# Wed, 23 Mar 2022 21:56:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 21:56:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8365d9448ab73a0b9418881d07622e7c116779f5f7ff600dcfbdc018626535`  
		Last Modified: Wed, 23 Mar 2022 21:58:49 GMT  
		Size: 4.4 MB (4441374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0ff5fa9c85f9c3dd3da4265f384e11366cecd9c22f80631d9be6411ca26f5a`  
		Last Modified: Wed, 23 Mar 2022 21:58:45 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0fbe9b4a8938c2752473cad2d4c7fedcf260481989f3d2ed6ae3a16890c0d6`  
		Last Modified: Wed, 23 Mar 2022 21:58:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e1d92c67b112506e1eba438169cabbae1e7df652747fced40ee09e49016709
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc357f18f7318c9dd8b86a35d7f8ade6041903325fe61edd036d0423b4ac7bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 19:27:05 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 19:27:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 19:27:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 19:27:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 19:27:11 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 19:27:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 19:27:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6838fdfa81afc565c161c1fee30401de3a013bfb571f5be3c3a993badc92f3f`  
		Last Modified: Tue, 29 Mar 2022 19:28:11 GMT  
		Size: 4.4 MB (4426412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dce858aad644833ca99f39e8757136a768b7f8ecfaae59ac4154e3823651dd`  
		Last Modified: Tue, 29 Mar 2022 19:28:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a6ab0d728bdc5bcab9e3d3e9236d289a5888dd54c1cd6cade53e1cac8f5c2`  
		Last Modified: Tue, 29 Mar 2022 19:28:11 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-alpine3.15`

```console
$ docker pull nats@sha256:6bc6e4354e204e2b5a605bdbe7e36c95a99cd8075aa0da75292eec39b78fc2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:ddbbfa522c3602ac76b51284c184828f24be9fcb329665c8c835d0a0b5f71609
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33323e6971854b66bb8ff96bd008fee5ae9fea9f9118b96fd68ee148e42bef21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:04:37 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 12:04:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 12:04:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 12:04:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 12:04:39 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 12:04:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 12:04:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9a10b3bb713cc8101378783c4f52f75d8f834fa21f5fc136a30904bfcb4f9f`  
		Last Modified: Tue, 29 Mar 2022 12:05:12 GMT  
		Size: 4.8 MB (4783177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb87d96c1921472cce8519d8fb67b430106edf099c364e068ceecefd4ba7e00`  
		Last Modified: Tue, 29 Mar 2022 12:05:11 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c21f97f27e2c9ba2af1a903b9062eb0b884a9a6992c9d8964ecd84a2348cae`  
		Last Modified: Tue, 29 Mar 2022 12:05:11 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:3fee8925082b25042ab9087ddcc5c293a612850d5244cb7775af22caca1f6d9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7070564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4e309ef1582f25174193504f16ecbc35a11f70c720953171928ee47ae18c5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:08:37 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 08:08:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 08:08:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 08:08:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 08:08:43 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 08:08:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:08:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5433d34ffede9d0eff77eaf04849e4b79ec0f7e200a2d117f5e58a50e0b82217`  
		Last Modified: Tue, 29 Mar 2022 08:10:45 GMT  
		Size: 4.4 MB (4447623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df1c1e8b65688f71ac5b1bd33b8077ef7a6394d79c1ec7dffcbc7914484d48c`  
		Last Modified: Tue, 29 Mar 2022 08:10:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da97cd054d0f3a42979a00c4d9c8a3255934903076031d8ecb9f73355e33cdc6`  
		Last Modified: Tue, 29 Mar 2022 08:10:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:b8830dffd27a635e2d80d20fe9e49d0d4192fb89ee89cefad2386db8310c9f55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6869438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5fcef1f127b912a6983b0d1760f725714bd3d51423e173685ce10bc75c3c61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 21:56:38 GMT
ENV NATS_SERVER=2.7.4
# Wed, 23 Mar 2022 21:56:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 23 Mar 2022 21:56:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 23 Mar 2022 21:56:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 23 Mar 2022 21:56:43 GMT
EXPOSE 4222 6222 8222
# Wed, 23 Mar 2022 21:56:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 21:56:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8365d9448ab73a0b9418881d07622e7c116779f5f7ff600dcfbdc018626535`  
		Last Modified: Wed, 23 Mar 2022 21:58:49 GMT  
		Size: 4.4 MB (4441374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0ff5fa9c85f9c3dd3da4265f384e11366cecd9c22f80631d9be6411ca26f5a`  
		Last Modified: Wed, 23 Mar 2022 21:58:45 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0fbe9b4a8938c2752473cad2d4c7fedcf260481989f3d2ed6ae3a16890c0d6`  
		Last Modified: Wed, 23 Mar 2022 21:58:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e1d92c67b112506e1eba438169cabbae1e7df652747fced40ee09e49016709
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc357f18f7318c9dd8b86a35d7f8ade6041903325fe61edd036d0423b4ac7bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 19:27:05 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 19:27:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 19:27:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 19:27:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 19:27:11 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 19:27:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 19:27:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6838fdfa81afc565c161c1fee30401de3a013bfb571f5be3c3a993badc92f3f`  
		Last Modified: Tue, 29 Mar 2022 19:28:11 GMT  
		Size: 4.4 MB (4426412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dce858aad644833ca99f39e8757136a768b7f8ecfaae59ac4154e3823651dd`  
		Last Modified: Tue, 29 Mar 2022 19:28:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a6ab0d728bdc5bcab9e3d3e9236d289a5888dd54c1cd6cade53e1cac8f5c2`  
		Last Modified: Tue, 29 Mar 2022 19:28:11 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-linux`

```console
$ docker pull nats@sha256:162126c602bcb3293ff5401b486cba4da6a3df5ed3b28758b1e9b11faeb382e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-linux` - linux; amd64

```console
$ docker pull nats@sha256:5102d9ad6d58bc95c08d14e8fe54b4cb432ac9237cec01d33dcbd8e4850cf447
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4510590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d053ccf4f981153bfbc620038e1ef8f4350bd08832ada50fb0a0fba84572be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:02a472480673a11c995d1ea52b63c55910490337313c1211b4877f5071117f27 in /nats-server 
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:25:51 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:25:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:25:51 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:25:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9292be658bded2e584005b2d2d3c989d58b8c84c43d30cbf498884e4da11d88`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 4.5 MB (4510082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053a12f02cf2d3d90a7d26739c64349d29833ccb5f6d04c6b28d8fff2443538`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:3256353a8d53c6257a1ec8c17b572529f87360bf3b105b470da8998266e05315
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5335fe9c64c80865dd34d7f1d94b52b6d4038ce714fb04d9f318a0393262dac7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:06:00 GMT
COPY file:63d2dc292853c2a6d99433d1e8a92c091a0c775ab65a2e453be73d5448e05594 in /nats-server 
# Wed, 09 Mar 2022 23:06:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:06:01 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:06:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:06:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:06:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c9142de49642e016c3df123dce55998ce71f3777b9433742a88aa91b23f9ae9`  
		Last Modified: Wed, 09 Mar 2022 23:08:21 GMT  
		Size: 4.2 MB (4174056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232eee2ffad4b2ab84d1a4aafd3be0df1c1066f57eab6f18a4b55344b74488be`  
		Last Modified: Wed, 09 Mar 2022 23:08:18 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:ed87fc96ebeace8ad252ad368ab68f1ef976daadae90f50d8f1f917364b8050c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c348e474d9b30a28b01ce9d8566ee12c3404e1a91cddfa31c8de44ba3c6b495b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:26:11 GMT
COPY file:143b3802bb689cd4b4badd2b1463feaa3881f20e6fd303b203aa25ea206fb684 in /nats-server 
# Wed, 09 Mar 2022 23:26:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:26:12 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:26:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:26:13 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c0d2f46ac12a6f6109f1f810a72658a0faa0b7301dfa2abc4f222012bab43639`  
		Last Modified: Wed, 09 Mar 2022 23:28:32 GMT  
		Size: 4.2 MB (4168878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4e39b35a6f91da4330c0e57dcc7c9e91270e4d54cf1097b98ad3ab1a1ca178`  
		Last Modified: Wed, 09 Mar 2022 23:28:29 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4cb4ef773edd64ce015945185e30502ff5c80ea967e3ebbdf0f8d3751016ff45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bb252022527ea75cce7f45ea7463fe04e9e5b5628152fb157822c0d01bc139`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:57:14 GMT
COPY file:6d6603ade462e58030bc93029992af55dac8b9eae7e4985b5c84dd49e1ee1be2 in /nats-server 
# Wed, 09 Mar 2022 22:57:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:57:15 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:57:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:57:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5663127c1a3d9c378ea8ac20e94b430188a9dbb2675ca0b26205f9a5e1b0bf36`  
		Last Modified: Wed, 09 Mar 2022 22:58:35 GMT  
		Size: 4.2 MB (4154114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc2c19c0a6d2b137b1891d3ee3716153114e9575e2a1bc966dd0660a4c7b72`  
		Last Modified: Wed, 09 Mar 2022 22:58:34 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-nanoserver`

```console
$ docker pull nats@sha256:9654461ee3015e4abac8d6f24720ec089a72db6650768ac224cd6280735a70f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7-nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:6d00c243dc589b03baf20fbe8c0a81279a5725d0774b275bbb9c3ebe329b570e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107611006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888ad60fdeb9e43dbbe336530422e503f539089048145cc1bbea7e51905b7095`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:16:59 GMT
RUN cmd /S /C #(nop) COPY file:741c07610cba7dd6badafc477fe411065386e3878f26a0bf50ed1d89036d6dcf in C:\nats-server.exe 
# Wed, 09 Mar 2022 23:17:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:17:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e02f868f2bb74e07262227b1156e17be47c4d960be7e9270cca8bc1dc6635b`  
		Last Modified: Wed, 09 Mar 2022 23:17:53 GMT  
		Size: 4.6 MB (4550038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9514eaf2c4a0d45ed2033bb85089d1fa90e61da7d517358225b5c6739051fcd7`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497be159edf0b99569392570b882cb48a2e72386befcbe1a0f454c6c02dba990`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c889054d0bd6db85b4b9c71958f5f7b8a6679ee127a701a521ee74961a3a528`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10493cee89e77ec8ec7093f8359147e7040171cbe811996808f6f1b860c78db`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-nanoserver-1809`

```console
$ docker pull nats@sha256:9654461ee3015e4abac8d6f24720ec089a72db6650768ac224cd6280735a70f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:6d00c243dc589b03baf20fbe8c0a81279a5725d0774b275bbb9c3ebe329b570e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107611006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888ad60fdeb9e43dbbe336530422e503f539089048145cc1bbea7e51905b7095`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:16:59 GMT
RUN cmd /S /C #(nop) COPY file:741c07610cba7dd6badafc477fe411065386e3878f26a0bf50ed1d89036d6dcf in C:\nats-server.exe 
# Wed, 09 Mar 2022 23:17:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:17:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e02f868f2bb74e07262227b1156e17be47c4d960be7e9270cca8bc1dc6635b`  
		Last Modified: Wed, 09 Mar 2022 23:17:53 GMT  
		Size: 4.6 MB (4550038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9514eaf2c4a0d45ed2033bb85089d1fa90e61da7d517358225b5c6739051fcd7`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497be159edf0b99569392570b882cb48a2e72386befcbe1a0f454c6c02dba990`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c889054d0bd6db85b4b9c71958f5f7b8a6679ee127a701a521ee74961a3a528`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10493cee89e77ec8ec7093f8359147e7040171cbe811996808f6f1b860c78db`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-scratch`

```console
$ docker pull nats@sha256:162126c602bcb3293ff5401b486cba4da6a3df5ed3b28758b1e9b11faeb382e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-scratch` - linux; amd64

```console
$ docker pull nats@sha256:5102d9ad6d58bc95c08d14e8fe54b4cb432ac9237cec01d33dcbd8e4850cf447
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4510590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d053ccf4f981153bfbc620038e1ef8f4350bd08832ada50fb0a0fba84572be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:02a472480673a11c995d1ea52b63c55910490337313c1211b4877f5071117f27 in /nats-server 
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:25:51 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:25:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:25:51 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:25:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9292be658bded2e584005b2d2d3c989d58b8c84c43d30cbf498884e4da11d88`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 4.5 MB (4510082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053a12f02cf2d3d90a7d26739c64349d29833ccb5f6d04c6b28d8fff2443538`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:3256353a8d53c6257a1ec8c17b572529f87360bf3b105b470da8998266e05315
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5335fe9c64c80865dd34d7f1d94b52b6d4038ce714fb04d9f318a0393262dac7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:06:00 GMT
COPY file:63d2dc292853c2a6d99433d1e8a92c091a0c775ab65a2e453be73d5448e05594 in /nats-server 
# Wed, 09 Mar 2022 23:06:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:06:01 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:06:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:06:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:06:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c9142de49642e016c3df123dce55998ce71f3777b9433742a88aa91b23f9ae9`  
		Last Modified: Wed, 09 Mar 2022 23:08:21 GMT  
		Size: 4.2 MB (4174056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232eee2ffad4b2ab84d1a4aafd3be0df1c1066f57eab6f18a4b55344b74488be`  
		Last Modified: Wed, 09 Mar 2022 23:08:18 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:ed87fc96ebeace8ad252ad368ab68f1ef976daadae90f50d8f1f917364b8050c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c348e474d9b30a28b01ce9d8566ee12c3404e1a91cddfa31c8de44ba3c6b495b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:26:11 GMT
COPY file:143b3802bb689cd4b4badd2b1463feaa3881f20e6fd303b203aa25ea206fb684 in /nats-server 
# Wed, 09 Mar 2022 23:26:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:26:12 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:26:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:26:13 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c0d2f46ac12a6f6109f1f810a72658a0faa0b7301dfa2abc4f222012bab43639`  
		Last Modified: Wed, 09 Mar 2022 23:28:32 GMT  
		Size: 4.2 MB (4168878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4e39b35a6f91da4330c0e57dcc7c9e91270e4d54cf1097b98ad3ab1a1ca178`  
		Last Modified: Wed, 09 Mar 2022 23:28:29 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4cb4ef773edd64ce015945185e30502ff5c80ea967e3ebbdf0f8d3751016ff45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bb252022527ea75cce7f45ea7463fe04e9e5b5628152fb157822c0d01bc139`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:57:14 GMT
COPY file:6d6603ade462e58030bc93029992af55dac8b9eae7e4985b5c84dd49e1ee1be2 in /nats-server 
# Wed, 09 Mar 2022 22:57:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:57:15 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:57:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:57:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5663127c1a3d9c378ea8ac20e94b430188a9dbb2675ca0b26205f9a5e1b0bf36`  
		Last Modified: Wed, 09 Mar 2022 22:58:35 GMT  
		Size: 4.2 MB (4154114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc2c19c0a6d2b137b1891d3ee3716153114e9575e2a1bc966dd0660a4c7b72`  
		Last Modified: Wed, 09 Mar 2022 22:58:34 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-windowsservercore`

```console
$ docker pull nats@sha256:de7fa8eefd8b38a00c8f113294fc03f91486cde9b572b109e98f44f2ffbf5b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:ebc084a1a8e19ddf44701886869f9009dccaf6485d52d791799326d6f89ab0d2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720689430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f84a261eca9a7469f56f24e432d4ea475732107a3ab4cf28174ee49e3ba364b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:14:16 GMT
ENV NATS_SERVER=2.7.4
# Wed, 09 Mar 2022 23:14:17 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.4/nats-server-v2.7.4-windows-amd64.zip
# Wed, 09 Mar 2022 23:14:18 GMT
ENV NATS_SERVER_SHASUM=0c98c505391e781f5f528817099dc727d83c997b3d48032c0f111d1452e8489b
# Wed, 09 Mar 2022 23:15:14 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:16:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:16:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:16:40 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:16:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:16:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301e780f30b10c083782e0d53ed487fd4d8f8d32ad6c9b9fd84d2fcc0745ee60`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7e8b0a6cef1b2ea81fcb039bc420172f4a60c3f329e6b495f9e1133e3e1534`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844fdd93ebcdfae84a099cefa8da35deaa056bff22b968bebf99205facdf928f`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f545db8b309b5166354fd80028d4bda3d85af353da1959ab615769a430d1c0`  
		Last Modified: Wed, 09 Mar 2022 23:17:34 GMT  
		Size: 348.6 KB (348621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502abb43626a3eb4c75cb441213dbb73cbb7b0df0b28ff4d77b4420ebeb536e9`  
		Last Modified: Wed, 09 Mar 2022 23:17:36 GMT  
		Size: 4.9 MB (4874834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cef267e6b969aa61db520018b018b4244a92bbceda7eba76208a24bf2bcfbaf`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57f349791c768e9ea1eaf48b6c342b2038779b4cdca397333cc20c73ded703`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06857fcc2d8c8a67e6e493c5d95e54a6bded7af6103d139e4a59072664088bff`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62c41a5b49cd11c0da902b5333c829bcc21ffcb561d931fc457eafa36ee6bc9`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-windowsservercore-1809`

```console
$ docker pull nats@sha256:de7fa8eefd8b38a00c8f113294fc03f91486cde9b572b109e98f44f2ffbf5b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:ebc084a1a8e19ddf44701886869f9009dccaf6485d52d791799326d6f89ab0d2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720689430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f84a261eca9a7469f56f24e432d4ea475732107a3ab4cf28174ee49e3ba364b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:14:16 GMT
ENV NATS_SERVER=2.7.4
# Wed, 09 Mar 2022 23:14:17 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.4/nats-server-v2.7.4-windows-amd64.zip
# Wed, 09 Mar 2022 23:14:18 GMT
ENV NATS_SERVER_SHASUM=0c98c505391e781f5f528817099dc727d83c997b3d48032c0f111d1452e8489b
# Wed, 09 Mar 2022 23:15:14 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:16:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:16:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:16:40 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:16:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:16:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301e780f30b10c083782e0d53ed487fd4d8f8d32ad6c9b9fd84d2fcc0745ee60`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7e8b0a6cef1b2ea81fcb039bc420172f4a60c3f329e6b495f9e1133e3e1534`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844fdd93ebcdfae84a099cefa8da35deaa056bff22b968bebf99205facdf928f`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f545db8b309b5166354fd80028d4bda3d85af353da1959ab615769a430d1c0`  
		Last Modified: Wed, 09 Mar 2022 23:17:34 GMT  
		Size: 348.6 KB (348621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502abb43626a3eb4c75cb441213dbb73cbb7b0df0b28ff4d77b4420ebeb536e9`  
		Last Modified: Wed, 09 Mar 2022 23:17:36 GMT  
		Size: 4.9 MB (4874834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cef267e6b969aa61db520018b018b4244a92bbceda7eba76208a24bf2bcfbaf`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57f349791c768e9ea1eaf48b6c342b2038779b4cdca397333cc20c73ded703`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06857fcc2d8c8a67e6e493c5d95e54a6bded7af6103d139e4a59072664088bff`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62c41a5b49cd11c0da902b5333c829bcc21ffcb561d931fc457eafa36ee6bc9`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.4`

```console
$ docker pull nats@sha256:6f86d5bac0f78b01cf5f9f707008403b0792ff5029817f8afc23c895c5215cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7.4` - linux; amd64

```console
$ docker pull nats@sha256:5102d9ad6d58bc95c08d14e8fe54b4cb432ac9237cec01d33dcbd8e4850cf447
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4510590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d053ccf4f981153bfbc620038e1ef8f4350bd08832ada50fb0a0fba84572be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:02a472480673a11c995d1ea52b63c55910490337313c1211b4877f5071117f27 in /nats-server 
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:25:51 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:25:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:25:51 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:25:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9292be658bded2e584005b2d2d3c989d58b8c84c43d30cbf498884e4da11d88`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 4.5 MB (4510082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053a12f02cf2d3d90a7d26739c64349d29833ccb5f6d04c6b28d8fff2443538`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.4` - linux; arm variant v6

```console
$ docker pull nats@sha256:3256353a8d53c6257a1ec8c17b572529f87360bf3b105b470da8998266e05315
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5335fe9c64c80865dd34d7f1d94b52b6d4038ce714fb04d9f318a0393262dac7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:06:00 GMT
COPY file:63d2dc292853c2a6d99433d1e8a92c091a0c775ab65a2e453be73d5448e05594 in /nats-server 
# Wed, 09 Mar 2022 23:06:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:06:01 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:06:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:06:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:06:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c9142de49642e016c3df123dce55998ce71f3777b9433742a88aa91b23f9ae9`  
		Last Modified: Wed, 09 Mar 2022 23:08:21 GMT  
		Size: 4.2 MB (4174056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232eee2ffad4b2ab84d1a4aafd3be0df1c1066f57eab6f18a4b55344b74488be`  
		Last Modified: Wed, 09 Mar 2022 23:08:18 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.4` - linux; arm variant v7

```console
$ docker pull nats@sha256:ed87fc96ebeace8ad252ad368ab68f1ef976daadae90f50d8f1f917364b8050c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c348e474d9b30a28b01ce9d8566ee12c3404e1a91cddfa31c8de44ba3c6b495b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:26:11 GMT
COPY file:143b3802bb689cd4b4badd2b1463feaa3881f20e6fd303b203aa25ea206fb684 in /nats-server 
# Wed, 09 Mar 2022 23:26:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:26:12 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:26:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:26:13 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c0d2f46ac12a6f6109f1f810a72658a0faa0b7301dfa2abc4f222012bab43639`  
		Last Modified: Wed, 09 Mar 2022 23:28:32 GMT  
		Size: 4.2 MB (4168878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4e39b35a6f91da4330c0e57dcc7c9e91270e4d54cf1097b98ad3ab1a1ca178`  
		Last Modified: Wed, 09 Mar 2022 23:28:29 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.4` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4cb4ef773edd64ce015945185e30502ff5c80ea967e3ebbdf0f8d3751016ff45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bb252022527ea75cce7f45ea7463fe04e9e5b5628152fb157822c0d01bc139`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:57:14 GMT
COPY file:6d6603ade462e58030bc93029992af55dac8b9eae7e4985b5c84dd49e1ee1be2 in /nats-server 
# Wed, 09 Mar 2022 22:57:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:57:15 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:57:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:57:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5663127c1a3d9c378ea8ac20e94b430188a9dbb2675ca0b26205f9a5e1b0bf36`  
		Last Modified: Wed, 09 Mar 2022 22:58:35 GMT  
		Size: 4.2 MB (4154114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc2c19c0a6d2b137b1891d3ee3716153114e9575e2a1bc966dd0660a4c7b72`  
		Last Modified: Wed, 09 Mar 2022 22:58:34 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.4` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:6d00c243dc589b03baf20fbe8c0a81279a5725d0774b275bbb9c3ebe329b570e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107611006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888ad60fdeb9e43dbbe336530422e503f539089048145cc1bbea7e51905b7095`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:16:59 GMT
RUN cmd /S /C #(nop) COPY file:741c07610cba7dd6badafc477fe411065386e3878f26a0bf50ed1d89036d6dcf in C:\nats-server.exe 
# Wed, 09 Mar 2022 23:17:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:17:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e02f868f2bb74e07262227b1156e17be47c4d960be7e9270cca8bc1dc6635b`  
		Last Modified: Wed, 09 Mar 2022 23:17:53 GMT  
		Size: 4.6 MB (4550038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9514eaf2c4a0d45ed2033bb85089d1fa90e61da7d517358225b5c6739051fcd7`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497be159edf0b99569392570b882cb48a2e72386befcbe1a0f454c6c02dba990`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c889054d0bd6db85b4b9c71958f5f7b8a6679ee127a701a521ee74961a3a528`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10493cee89e77ec8ec7093f8359147e7040171cbe811996808f6f1b860c78db`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.4-alpine`

```console
$ docker pull nats@sha256:6bc6e4354e204e2b5a605bdbe7e36c95a99cd8075aa0da75292eec39b78fc2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.4-alpine` - linux; amd64

```console
$ docker pull nats@sha256:ddbbfa522c3602ac76b51284c184828f24be9fcb329665c8c835d0a0b5f71609
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33323e6971854b66bb8ff96bd008fee5ae9fea9f9118b96fd68ee148e42bef21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:04:37 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 12:04:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 12:04:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 12:04:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 12:04:39 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 12:04:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 12:04:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9a10b3bb713cc8101378783c4f52f75d8f834fa21f5fc136a30904bfcb4f9f`  
		Last Modified: Tue, 29 Mar 2022 12:05:12 GMT  
		Size: 4.8 MB (4783177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb87d96c1921472cce8519d8fb67b430106edf099c364e068ceecefd4ba7e00`  
		Last Modified: Tue, 29 Mar 2022 12:05:11 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c21f97f27e2c9ba2af1a903b9062eb0b884a9a6992c9d8964ecd84a2348cae`  
		Last Modified: Tue, 29 Mar 2022 12:05:11 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.4-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3fee8925082b25042ab9087ddcc5c293a612850d5244cb7775af22caca1f6d9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7070564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4e309ef1582f25174193504f16ecbc35a11f70c720953171928ee47ae18c5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:08:37 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 08:08:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 08:08:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 08:08:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 08:08:43 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 08:08:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:08:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5433d34ffede9d0eff77eaf04849e4b79ec0f7e200a2d117f5e58a50e0b82217`  
		Last Modified: Tue, 29 Mar 2022 08:10:45 GMT  
		Size: 4.4 MB (4447623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df1c1e8b65688f71ac5b1bd33b8077ef7a6394d79c1ec7dffcbc7914484d48c`  
		Last Modified: Tue, 29 Mar 2022 08:10:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da97cd054d0f3a42979a00c4d9c8a3255934903076031d8ecb9f73355e33cdc6`  
		Last Modified: Tue, 29 Mar 2022 08:10:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.4-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b8830dffd27a635e2d80d20fe9e49d0d4192fb89ee89cefad2386db8310c9f55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6869438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5fcef1f127b912a6983b0d1760f725714bd3d51423e173685ce10bc75c3c61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 21:56:38 GMT
ENV NATS_SERVER=2.7.4
# Wed, 23 Mar 2022 21:56:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 23 Mar 2022 21:56:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 23 Mar 2022 21:56:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 23 Mar 2022 21:56:43 GMT
EXPOSE 4222 6222 8222
# Wed, 23 Mar 2022 21:56:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 21:56:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8365d9448ab73a0b9418881d07622e7c116779f5f7ff600dcfbdc018626535`  
		Last Modified: Wed, 23 Mar 2022 21:58:49 GMT  
		Size: 4.4 MB (4441374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0ff5fa9c85f9c3dd3da4265f384e11366cecd9c22f80631d9be6411ca26f5a`  
		Last Modified: Wed, 23 Mar 2022 21:58:45 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0fbe9b4a8938c2752473cad2d4c7fedcf260481989f3d2ed6ae3a16890c0d6`  
		Last Modified: Wed, 23 Mar 2022 21:58:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.4-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e1d92c67b112506e1eba438169cabbae1e7df652747fced40ee09e49016709
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc357f18f7318c9dd8b86a35d7f8ade6041903325fe61edd036d0423b4ac7bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 19:27:05 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 19:27:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 19:27:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 19:27:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 19:27:11 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 19:27:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 19:27:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6838fdfa81afc565c161c1fee30401de3a013bfb571f5be3c3a993badc92f3f`  
		Last Modified: Tue, 29 Mar 2022 19:28:11 GMT  
		Size: 4.4 MB (4426412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dce858aad644833ca99f39e8757136a768b7f8ecfaae59ac4154e3823651dd`  
		Last Modified: Tue, 29 Mar 2022 19:28:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a6ab0d728bdc5bcab9e3d3e9236d289a5888dd54c1cd6cade53e1cac8f5c2`  
		Last Modified: Tue, 29 Mar 2022 19:28:11 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.4-alpine3.15`

```console
$ docker pull nats@sha256:6bc6e4354e204e2b5a605bdbe7e36c95a99cd8075aa0da75292eec39b78fc2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.4-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:ddbbfa522c3602ac76b51284c184828f24be9fcb329665c8c835d0a0b5f71609
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33323e6971854b66bb8ff96bd008fee5ae9fea9f9118b96fd68ee148e42bef21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:04:37 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 12:04:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 12:04:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 12:04:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 12:04:39 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 12:04:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 12:04:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9a10b3bb713cc8101378783c4f52f75d8f834fa21f5fc136a30904bfcb4f9f`  
		Last Modified: Tue, 29 Mar 2022 12:05:12 GMT  
		Size: 4.8 MB (4783177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb87d96c1921472cce8519d8fb67b430106edf099c364e068ceecefd4ba7e00`  
		Last Modified: Tue, 29 Mar 2022 12:05:11 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c21f97f27e2c9ba2af1a903b9062eb0b884a9a6992c9d8964ecd84a2348cae`  
		Last Modified: Tue, 29 Mar 2022 12:05:11 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.4-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:3fee8925082b25042ab9087ddcc5c293a612850d5244cb7775af22caca1f6d9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7070564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4e309ef1582f25174193504f16ecbc35a11f70c720953171928ee47ae18c5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:08:37 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 08:08:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 08:08:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 08:08:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 08:08:43 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 08:08:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:08:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5433d34ffede9d0eff77eaf04849e4b79ec0f7e200a2d117f5e58a50e0b82217`  
		Last Modified: Tue, 29 Mar 2022 08:10:45 GMT  
		Size: 4.4 MB (4447623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df1c1e8b65688f71ac5b1bd33b8077ef7a6394d79c1ec7dffcbc7914484d48c`  
		Last Modified: Tue, 29 Mar 2022 08:10:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da97cd054d0f3a42979a00c4d9c8a3255934903076031d8ecb9f73355e33cdc6`  
		Last Modified: Tue, 29 Mar 2022 08:10:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.4-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:b8830dffd27a635e2d80d20fe9e49d0d4192fb89ee89cefad2386db8310c9f55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6869438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5fcef1f127b912a6983b0d1760f725714bd3d51423e173685ce10bc75c3c61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 21:56:38 GMT
ENV NATS_SERVER=2.7.4
# Wed, 23 Mar 2022 21:56:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 23 Mar 2022 21:56:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 23 Mar 2022 21:56:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 23 Mar 2022 21:56:43 GMT
EXPOSE 4222 6222 8222
# Wed, 23 Mar 2022 21:56:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 21:56:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8365d9448ab73a0b9418881d07622e7c116779f5f7ff600dcfbdc018626535`  
		Last Modified: Wed, 23 Mar 2022 21:58:49 GMT  
		Size: 4.4 MB (4441374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0ff5fa9c85f9c3dd3da4265f384e11366cecd9c22f80631d9be6411ca26f5a`  
		Last Modified: Wed, 23 Mar 2022 21:58:45 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0fbe9b4a8938c2752473cad2d4c7fedcf260481989f3d2ed6ae3a16890c0d6`  
		Last Modified: Wed, 23 Mar 2022 21:58:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.4-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e1d92c67b112506e1eba438169cabbae1e7df652747fced40ee09e49016709
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc357f18f7318c9dd8b86a35d7f8ade6041903325fe61edd036d0423b4ac7bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 19:27:05 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 19:27:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 19:27:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 19:27:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 19:27:11 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 19:27:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 19:27:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6838fdfa81afc565c161c1fee30401de3a013bfb571f5be3c3a993badc92f3f`  
		Last Modified: Tue, 29 Mar 2022 19:28:11 GMT  
		Size: 4.4 MB (4426412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dce858aad644833ca99f39e8757136a768b7f8ecfaae59ac4154e3823651dd`  
		Last Modified: Tue, 29 Mar 2022 19:28:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a6ab0d728bdc5bcab9e3d3e9236d289a5888dd54c1cd6cade53e1cac8f5c2`  
		Last Modified: Tue, 29 Mar 2022 19:28:11 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.4-linux`

```console
$ docker pull nats@sha256:162126c602bcb3293ff5401b486cba4da6a3df5ed3b28758b1e9b11faeb382e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.4-linux` - linux; amd64

```console
$ docker pull nats@sha256:5102d9ad6d58bc95c08d14e8fe54b4cb432ac9237cec01d33dcbd8e4850cf447
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4510590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d053ccf4f981153bfbc620038e1ef8f4350bd08832ada50fb0a0fba84572be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:02a472480673a11c995d1ea52b63c55910490337313c1211b4877f5071117f27 in /nats-server 
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:25:51 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:25:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:25:51 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:25:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9292be658bded2e584005b2d2d3c989d58b8c84c43d30cbf498884e4da11d88`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 4.5 MB (4510082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053a12f02cf2d3d90a7d26739c64349d29833ccb5f6d04c6b28d8fff2443538`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.4-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:3256353a8d53c6257a1ec8c17b572529f87360bf3b105b470da8998266e05315
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5335fe9c64c80865dd34d7f1d94b52b6d4038ce714fb04d9f318a0393262dac7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:06:00 GMT
COPY file:63d2dc292853c2a6d99433d1e8a92c091a0c775ab65a2e453be73d5448e05594 in /nats-server 
# Wed, 09 Mar 2022 23:06:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:06:01 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:06:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:06:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:06:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c9142de49642e016c3df123dce55998ce71f3777b9433742a88aa91b23f9ae9`  
		Last Modified: Wed, 09 Mar 2022 23:08:21 GMT  
		Size: 4.2 MB (4174056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232eee2ffad4b2ab84d1a4aafd3be0df1c1066f57eab6f18a4b55344b74488be`  
		Last Modified: Wed, 09 Mar 2022 23:08:18 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.4-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:ed87fc96ebeace8ad252ad368ab68f1ef976daadae90f50d8f1f917364b8050c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c348e474d9b30a28b01ce9d8566ee12c3404e1a91cddfa31c8de44ba3c6b495b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:26:11 GMT
COPY file:143b3802bb689cd4b4badd2b1463feaa3881f20e6fd303b203aa25ea206fb684 in /nats-server 
# Wed, 09 Mar 2022 23:26:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:26:12 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:26:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:26:13 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c0d2f46ac12a6f6109f1f810a72658a0faa0b7301dfa2abc4f222012bab43639`  
		Last Modified: Wed, 09 Mar 2022 23:28:32 GMT  
		Size: 4.2 MB (4168878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4e39b35a6f91da4330c0e57dcc7c9e91270e4d54cf1097b98ad3ab1a1ca178`  
		Last Modified: Wed, 09 Mar 2022 23:28:29 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.4-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4cb4ef773edd64ce015945185e30502ff5c80ea967e3ebbdf0f8d3751016ff45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bb252022527ea75cce7f45ea7463fe04e9e5b5628152fb157822c0d01bc139`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:57:14 GMT
COPY file:6d6603ade462e58030bc93029992af55dac8b9eae7e4985b5c84dd49e1ee1be2 in /nats-server 
# Wed, 09 Mar 2022 22:57:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:57:15 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:57:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:57:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5663127c1a3d9c378ea8ac20e94b430188a9dbb2675ca0b26205f9a5e1b0bf36`  
		Last Modified: Wed, 09 Mar 2022 22:58:35 GMT  
		Size: 4.2 MB (4154114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc2c19c0a6d2b137b1891d3ee3716153114e9575e2a1bc966dd0660a4c7b72`  
		Last Modified: Wed, 09 Mar 2022 22:58:34 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.4-nanoserver`

```console
$ docker pull nats@sha256:9654461ee3015e4abac8d6f24720ec089a72db6650768ac224cd6280735a70f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7.4-nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:6d00c243dc589b03baf20fbe8c0a81279a5725d0774b275bbb9c3ebe329b570e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107611006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888ad60fdeb9e43dbbe336530422e503f539089048145cc1bbea7e51905b7095`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:16:59 GMT
RUN cmd /S /C #(nop) COPY file:741c07610cba7dd6badafc477fe411065386e3878f26a0bf50ed1d89036d6dcf in C:\nats-server.exe 
# Wed, 09 Mar 2022 23:17:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:17:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e02f868f2bb74e07262227b1156e17be47c4d960be7e9270cca8bc1dc6635b`  
		Last Modified: Wed, 09 Mar 2022 23:17:53 GMT  
		Size: 4.6 MB (4550038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9514eaf2c4a0d45ed2033bb85089d1fa90e61da7d517358225b5c6739051fcd7`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497be159edf0b99569392570b882cb48a2e72386befcbe1a0f454c6c02dba990`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c889054d0bd6db85b4b9c71958f5f7b8a6679ee127a701a521ee74961a3a528`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10493cee89e77ec8ec7093f8359147e7040171cbe811996808f6f1b860c78db`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.4-nanoserver-1809`

```console
$ docker pull nats@sha256:9654461ee3015e4abac8d6f24720ec089a72db6650768ac224cd6280735a70f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7.4-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:6d00c243dc589b03baf20fbe8c0a81279a5725d0774b275bbb9c3ebe329b570e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107611006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888ad60fdeb9e43dbbe336530422e503f539089048145cc1bbea7e51905b7095`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:16:59 GMT
RUN cmd /S /C #(nop) COPY file:741c07610cba7dd6badafc477fe411065386e3878f26a0bf50ed1d89036d6dcf in C:\nats-server.exe 
# Wed, 09 Mar 2022 23:17:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:17:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e02f868f2bb74e07262227b1156e17be47c4d960be7e9270cca8bc1dc6635b`  
		Last Modified: Wed, 09 Mar 2022 23:17:53 GMT  
		Size: 4.6 MB (4550038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9514eaf2c4a0d45ed2033bb85089d1fa90e61da7d517358225b5c6739051fcd7`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497be159edf0b99569392570b882cb48a2e72386befcbe1a0f454c6c02dba990`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c889054d0bd6db85b4b9c71958f5f7b8a6679ee127a701a521ee74961a3a528`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10493cee89e77ec8ec7093f8359147e7040171cbe811996808f6f1b860c78db`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.4-scratch`

```console
$ docker pull nats@sha256:162126c602bcb3293ff5401b486cba4da6a3df5ed3b28758b1e9b11faeb382e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.4-scratch` - linux; amd64

```console
$ docker pull nats@sha256:5102d9ad6d58bc95c08d14e8fe54b4cb432ac9237cec01d33dcbd8e4850cf447
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4510590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d053ccf4f981153bfbc620038e1ef8f4350bd08832ada50fb0a0fba84572be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:02a472480673a11c995d1ea52b63c55910490337313c1211b4877f5071117f27 in /nats-server 
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:25:51 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:25:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:25:51 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:25:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9292be658bded2e584005b2d2d3c989d58b8c84c43d30cbf498884e4da11d88`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 4.5 MB (4510082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053a12f02cf2d3d90a7d26739c64349d29833ccb5f6d04c6b28d8fff2443538`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.4-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:3256353a8d53c6257a1ec8c17b572529f87360bf3b105b470da8998266e05315
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5335fe9c64c80865dd34d7f1d94b52b6d4038ce714fb04d9f318a0393262dac7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:06:00 GMT
COPY file:63d2dc292853c2a6d99433d1e8a92c091a0c775ab65a2e453be73d5448e05594 in /nats-server 
# Wed, 09 Mar 2022 23:06:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:06:01 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:06:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:06:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:06:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c9142de49642e016c3df123dce55998ce71f3777b9433742a88aa91b23f9ae9`  
		Last Modified: Wed, 09 Mar 2022 23:08:21 GMT  
		Size: 4.2 MB (4174056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232eee2ffad4b2ab84d1a4aafd3be0df1c1066f57eab6f18a4b55344b74488be`  
		Last Modified: Wed, 09 Mar 2022 23:08:18 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.4-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:ed87fc96ebeace8ad252ad368ab68f1ef976daadae90f50d8f1f917364b8050c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c348e474d9b30a28b01ce9d8566ee12c3404e1a91cddfa31c8de44ba3c6b495b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:26:11 GMT
COPY file:143b3802bb689cd4b4badd2b1463feaa3881f20e6fd303b203aa25ea206fb684 in /nats-server 
# Wed, 09 Mar 2022 23:26:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:26:12 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:26:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:26:13 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c0d2f46ac12a6f6109f1f810a72658a0faa0b7301dfa2abc4f222012bab43639`  
		Last Modified: Wed, 09 Mar 2022 23:28:32 GMT  
		Size: 4.2 MB (4168878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4e39b35a6f91da4330c0e57dcc7c9e91270e4d54cf1097b98ad3ab1a1ca178`  
		Last Modified: Wed, 09 Mar 2022 23:28:29 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.4-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4cb4ef773edd64ce015945185e30502ff5c80ea967e3ebbdf0f8d3751016ff45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bb252022527ea75cce7f45ea7463fe04e9e5b5628152fb157822c0d01bc139`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:57:14 GMT
COPY file:6d6603ade462e58030bc93029992af55dac8b9eae7e4985b5c84dd49e1ee1be2 in /nats-server 
# Wed, 09 Mar 2022 22:57:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:57:15 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:57:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:57:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5663127c1a3d9c378ea8ac20e94b430188a9dbb2675ca0b26205f9a5e1b0bf36`  
		Last Modified: Wed, 09 Mar 2022 22:58:35 GMT  
		Size: 4.2 MB (4154114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc2c19c0a6d2b137b1891d3ee3716153114e9575e2a1bc966dd0660a4c7b72`  
		Last Modified: Wed, 09 Mar 2022 22:58:34 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.4-windowsservercore`

```console
$ docker pull nats@sha256:de7fa8eefd8b38a00c8f113294fc03f91486cde9b572b109e98f44f2ffbf5b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7.4-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:ebc084a1a8e19ddf44701886869f9009dccaf6485d52d791799326d6f89ab0d2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720689430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f84a261eca9a7469f56f24e432d4ea475732107a3ab4cf28174ee49e3ba364b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:14:16 GMT
ENV NATS_SERVER=2.7.4
# Wed, 09 Mar 2022 23:14:17 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.4/nats-server-v2.7.4-windows-amd64.zip
# Wed, 09 Mar 2022 23:14:18 GMT
ENV NATS_SERVER_SHASUM=0c98c505391e781f5f528817099dc727d83c997b3d48032c0f111d1452e8489b
# Wed, 09 Mar 2022 23:15:14 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:16:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:16:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:16:40 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:16:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:16:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301e780f30b10c083782e0d53ed487fd4d8f8d32ad6c9b9fd84d2fcc0745ee60`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7e8b0a6cef1b2ea81fcb039bc420172f4a60c3f329e6b495f9e1133e3e1534`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844fdd93ebcdfae84a099cefa8da35deaa056bff22b968bebf99205facdf928f`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f545db8b309b5166354fd80028d4bda3d85af353da1959ab615769a430d1c0`  
		Last Modified: Wed, 09 Mar 2022 23:17:34 GMT  
		Size: 348.6 KB (348621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502abb43626a3eb4c75cb441213dbb73cbb7b0df0b28ff4d77b4420ebeb536e9`  
		Last Modified: Wed, 09 Mar 2022 23:17:36 GMT  
		Size: 4.9 MB (4874834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cef267e6b969aa61db520018b018b4244a92bbceda7eba76208a24bf2bcfbaf`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57f349791c768e9ea1eaf48b6c342b2038779b4cdca397333cc20c73ded703`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06857fcc2d8c8a67e6e493c5d95e54a6bded7af6103d139e4a59072664088bff`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62c41a5b49cd11c0da902b5333c829bcc21ffcb561d931fc457eafa36ee6bc9`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.4-windowsservercore-1809`

```console
$ docker pull nats@sha256:de7fa8eefd8b38a00c8f113294fc03f91486cde9b572b109e98f44f2ffbf5b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7.4-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:ebc084a1a8e19ddf44701886869f9009dccaf6485d52d791799326d6f89ab0d2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720689430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f84a261eca9a7469f56f24e432d4ea475732107a3ab4cf28174ee49e3ba364b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:14:16 GMT
ENV NATS_SERVER=2.7.4
# Wed, 09 Mar 2022 23:14:17 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.4/nats-server-v2.7.4-windows-amd64.zip
# Wed, 09 Mar 2022 23:14:18 GMT
ENV NATS_SERVER_SHASUM=0c98c505391e781f5f528817099dc727d83c997b3d48032c0f111d1452e8489b
# Wed, 09 Mar 2022 23:15:14 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:16:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:16:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:16:40 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:16:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:16:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301e780f30b10c083782e0d53ed487fd4d8f8d32ad6c9b9fd84d2fcc0745ee60`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7e8b0a6cef1b2ea81fcb039bc420172f4a60c3f329e6b495f9e1133e3e1534`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844fdd93ebcdfae84a099cefa8da35deaa056bff22b968bebf99205facdf928f`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f545db8b309b5166354fd80028d4bda3d85af353da1959ab615769a430d1c0`  
		Last Modified: Wed, 09 Mar 2022 23:17:34 GMT  
		Size: 348.6 KB (348621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502abb43626a3eb4c75cb441213dbb73cbb7b0df0b28ff4d77b4420ebeb536e9`  
		Last Modified: Wed, 09 Mar 2022 23:17:36 GMT  
		Size: 4.9 MB (4874834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cef267e6b969aa61db520018b018b4244a92bbceda7eba76208a24bf2bcfbaf`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57f349791c768e9ea1eaf48b6c342b2038779b4cdca397333cc20c73ded703`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06857fcc2d8c8a67e6e493c5d95e54a6bded7af6103d139e4a59072664088bff`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62c41a5b49cd11c0da902b5333c829bcc21ffcb561d931fc457eafa36ee6bc9`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:6bc6e4354e204e2b5a605bdbe7e36c95a99cd8075aa0da75292eec39b78fc2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:ddbbfa522c3602ac76b51284c184828f24be9fcb329665c8c835d0a0b5f71609
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33323e6971854b66bb8ff96bd008fee5ae9fea9f9118b96fd68ee148e42bef21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:04:37 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 12:04:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 12:04:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 12:04:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 12:04:39 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 12:04:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 12:04:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9a10b3bb713cc8101378783c4f52f75d8f834fa21f5fc136a30904bfcb4f9f`  
		Last Modified: Tue, 29 Mar 2022 12:05:12 GMT  
		Size: 4.8 MB (4783177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb87d96c1921472cce8519d8fb67b430106edf099c364e068ceecefd4ba7e00`  
		Last Modified: Tue, 29 Mar 2022 12:05:11 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c21f97f27e2c9ba2af1a903b9062eb0b884a9a6992c9d8964ecd84a2348cae`  
		Last Modified: Tue, 29 Mar 2022 12:05:11 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3fee8925082b25042ab9087ddcc5c293a612850d5244cb7775af22caca1f6d9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7070564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4e309ef1582f25174193504f16ecbc35a11f70c720953171928ee47ae18c5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:08:37 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 08:08:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 08:08:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 08:08:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 08:08:43 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 08:08:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:08:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5433d34ffede9d0eff77eaf04849e4b79ec0f7e200a2d117f5e58a50e0b82217`  
		Last Modified: Tue, 29 Mar 2022 08:10:45 GMT  
		Size: 4.4 MB (4447623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df1c1e8b65688f71ac5b1bd33b8077ef7a6394d79c1ec7dffcbc7914484d48c`  
		Last Modified: Tue, 29 Mar 2022 08:10:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da97cd054d0f3a42979a00c4d9c8a3255934903076031d8ecb9f73355e33cdc6`  
		Last Modified: Tue, 29 Mar 2022 08:10:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b8830dffd27a635e2d80d20fe9e49d0d4192fb89ee89cefad2386db8310c9f55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6869438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5fcef1f127b912a6983b0d1760f725714bd3d51423e173685ce10bc75c3c61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 21:56:38 GMT
ENV NATS_SERVER=2.7.4
# Wed, 23 Mar 2022 21:56:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 23 Mar 2022 21:56:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 23 Mar 2022 21:56:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 23 Mar 2022 21:56:43 GMT
EXPOSE 4222 6222 8222
# Wed, 23 Mar 2022 21:56:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 21:56:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8365d9448ab73a0b9418881d07622e7c116779f5f7ff600dcfbdc018626535`  
		Last Modified: Wed, 23 Mar 2022 21:58:49 GMT  
		Size: 4.4 MB (4441374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0ff5fa9c85f9c3dd3da4265f384e11366cecd9c22f80631d9be6411ca26f5a`  
		Last Modified: Wed, 23 Mar 2022 21:58:45 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0fbe9b4a8938c2752473cad2d4c7fedcf260481989f3d2ed6ae3a16890c0d6`  
		Last Modified: Wed, 23 Mar 2022 21:58:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e1d92c67b112506e1eba438169cabbae1e7df652747fced40ee09e49016709
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc357f18f7318c9dd8b86a35d7f8ade6041903325fe61edd036d0423b4ac7bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 19:27:05 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 19:27:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 19:27:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 19:27:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 19:27:11 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 19:27:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 19:27:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6838fdfa81afc565c161c1fee30401de3a013bfb571f5be3c3a993badc92f3f`  
		Last Modified: Tue, 29 Mar 2022 19:28:11 GMT  
		Size: 4.4 MB (4426412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dce858aad644833ca99f39e8757136a768b7f8ecfaae59ac4154e3823651dd`  
		Last Modified: Tue, 29 Mar 2022 19:28:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a6ab0d728bdc5bcab9e3d3e9236d289a5888dd54c1cd6cade53e1cac8f5c2`  
		Last Modified: Tue, 29 Mar 2022 19:28:11 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.15`

```console
$ docker pull nats@sha256:6bc6e4354e204e2b5a605bdbe7e36c95a99cd8075aa0da75292eec39b78fc2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:ddbbfa522c3602ac76b51284c184828f24be9fcb329665c8c835d0a0b5f71609
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33323e6971854b66bb8ff96bd008fee5ae9fea9f9118b96fd68ee148e42bef21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:04:37 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 12:04:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 12:04:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 12:04:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 12:04:39 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 12:04:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 12:04:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9a10b3bb713cc8101378783c4f52f75d8f834fa21f5fc136a30904bfcb4f9f`  
		Last Modified: Tue, 29 Mar 2022 12:05:12 GMT  
		Size: 4.8 MB (4783177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb87d96c1921472cce8519d8fb67b430106edf099c364e068ceecefd4ba7e00`  
		Last Modified: Tue, 29 Mar 2022 12:05:11 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c21f97f27e2c9ba2af1a903b9062eb0b884a9a6992c9d8964ecd84a2348cae`  
		Last Modified: Tue, 29 Mar 2022 12:05:11 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:3fee8925082b25042ab9087ddcc5c293a612850d5244cb7775af22caca1f6d9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7070564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4e309ef1582f25174193504f16ecbc35a11f70c720953171928ee47ae18c5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:08:37 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 08:08:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 08:08:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 08:08:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 08:08:43 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 08:08:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:08:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5433d34ffede9d0eff77eaf04849e4b79ec0f7e200a2d117f5e58a50e0b82217`  
		Last Modified: Tue, 29 Mar 2022 08:10:45 GMT  
		Size: 4.4 MB (4447623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df1c1e8b65688f71ac5b1bd33b8077ef7a6394d79c1ec7dffcbc7914484d48c`  
		Last Modified: Tue, 29 Mar 2022 08:10:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da97cd054d0f3a42979a00c4d9c8a3255934903076031d8ecb9f73355e33cdc6`  
		Last Modified: Tue, 29 Mar 2022 08:10:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:b8830dffd27a635e2d80d20fe9e49d0d4192fb89ee89cefad2386db8310c9f55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6869438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5fcef1f127b912a6983b0d1760f725714bd3d51423e173685ce10bc75c3c61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 21:56:38 GMT
ENV NATS_SERVER=2.7.4
# Wed, 23 Mar 2022 21:56:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 23 Mar 2022 21:56:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 23 Mar 2022 21:56:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 23 Mar 2022 21:56:43 GMT
EXPOSE 4222 6222 8222
# Wed, 23 Mar 2022 21:56:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 21:56:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8365d9448ab73a0b9418881d07622e7c116779f5f7ff600dcfbdc018626535`  
		Last Modified: Wed, 23 Mar 2022 21:58:49 GMT  
		Size: 4.4 MB (4441374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0ff5fa9c85f9c3dd3da4265f384e11366cecd9c22f80631d9be6411ca26f5a`  
		Last Modified: Wed, 23 Mar 2022 21:58:45 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0fbe9b4a8938c2752473cad2d4c7fedcf260481989f3d2ed6ae3a16890c0d6`  
		Last Modified: Wed, 23 Mar 2022 21:58:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e1d92c67b112506e1eba438169cabbae1e7df652747fced40ee09e49016709
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc357f18f7318c9dd8b86a35d7f8ade6041903325fe61edd036d0423b4ac7bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 19:27:05 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 19:27:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 19:27:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 19:27:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 19:27:11 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 19:27:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 19:27:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6838fdfa81afc565c161c1fee30401de3a013bfb571f5be3c3a993badc92f3f`  
		Last Modified: Tue, 29 Mar 2022 19:28:11 GMT  
		Size: 4.4 MB (4426412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dce858aad644833ca99f39e8757136a768b7f8ecfaae59ac4154e3823651dd`  
		Last Modified: Tue, 29 Mar 2022 19:28:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a6ab0d728bdc5bcab9e3d3e9236d289a5888dd54c1cd6cade53e1cac8f5c2`  
		Last Modified: Tue, 29 Mar 2022 19:28:11 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:6f86d5bac0f78b01cf5f9f707008403b0792ff5029817f8afc23c895c5215cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2686; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:5102d9ad6d58bc95c08d14e8fe54b4cb432ac9237cec01d33dcbd8e4850cf447
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4510590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d053ccf4f981153bfbc620038e1ef8f4350bd08832ada50fb0a0fba84572be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:02a472480673a11c995d1ea52b63c55910490337313c1211b4877f5071117f27 in /nats-server 
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:25:51 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:25:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:25:51 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:25:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9292be658bded2e584005b2d2d3c989d58b8c84c43d30cbf498884e4da11d88`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 4.5 MB (4510082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053a12f02cf2d3d90a7d26739c64349d29833ccb5f6d04c6b28d8fff2443538`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:3256353a8d53c6257a1ec8c17b572529f87360bf3b105b470da8998266e05315
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5335fe9c64c80865dd34d7f1d94b52b6d4038ce714fb04d9f318a0393262dac7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:06:00 GMT
COPY file:63d2dc292853c2a6d99433d1e8a92c091a0c775ab65a2e453be73d5448e05594 in /nats-server 
# Wed, 09 Mar 2022 23:06:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:06:01 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:06:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:06:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:06:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c9142de49642e016c3df123dce55998ce71f3777b9433742a88aa91b23f9ae9`  
		Last Modified: Wed, 09 Mar 2022 23:08:21 GMT  
		Size: 4.2 MB (4174056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232eee2ffad4b2ab84d1a4aafd3be0df1c1066f57eab6f18a4b55344b74488be`  
		Last Modified: Wed, 09 Mar 2022 23:08:18 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:ed87fc96ebeace8ad252ad368ab68f1ef976daadae90f50d8f1f917364b8050c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c348e474d9b30a28b01ce9d8566ee12c3404e1a91cddfa31c8de44ba3c6b495b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:26:11 GMT
COPY file:143b3802bb689cd4b4badd2b1463feaa3881f20e6fd303b203aa25ea206fb684 in /nats-server 
# Wed, 09 Mar 2022 23:26:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:26:12 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:26:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:26:13 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c0d2f46ac12a6f6109f1f810a72658a0faa0b7301dfa2abc4f222012bab43639`  
		Last Modified: Wed, 09 Mar 2022 23:28:32 GMT  
		Size: 4.2 MB (4168878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4e39b35a6f91da4330c0e57dcc7c9e91270e4d54cf1097b98ad3ab1a1ca178`  
		Last Modified: Wed, 09 Mar 2022 23:28:29 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4cb4ef773edd64ce015945185e30502ff5c80ea967e3ebbdf0f8d3751016ff45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bb252022527ea75cce7f45ea7463fe04e9e5b5628152fb157822c0d01bc139`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:57:14 GMT
COPY file:6d6603ade462e58030bc93029992af55dac8b9eae7e4985b5c84dd49e1ee1be2 in /nats-server 
# Wed, 09 Mar 2022 22:57:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:57:15 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:57:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:57:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5663127c1a3d9c378ea8ac20e94b430188a9dbb2675ca0b26205f9a5e1b0bf36`  
		Last Modified: Wed, 09 Mar 2022 22:58:35 GMT  
		Size: 4.2 MB (4154114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc2c19c0a6d2b137b1891d3ee3716153114e9575e2a1bc966dd0660a4c7b72`  
		Last Modified: Wed, 09 Mar 2022 22:58:34 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:6d00c243dc589b03baf20fbe8c0a81279a5725d0774b275bbb9c3ebe329b570e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107611006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888ad60fdeb9e43dbbe336530422e503f539089048145cc1bbea7e51905b7095`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:16:59 GMT
RUN cmd /S /C #(nop) COPY file:741c07610cba7dd6badafc477fe411065386e3878f26a0bf50ed1d89036d6dcf in C:\nats-server.exe 
# Wed, 09 Mar 2022 23:17:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:17:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e02f868f2bb74e07262227b1156e17be47c4d960be7e9270cca8bc1dc6635b`  
		Last Modified: Wed, 09 Mar 2022 23:17:53 GMT  
		Size: 4.6 MB (4550038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9514eaf2c4a0d45ed2033bb85089d1fa90e61da7d517358225b5c6739051fcd7`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497be159edf0b99569392570b882cb48a2e72386befcbe1a0f454c6c02dba990`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c889054d0bd6db85b4b9c71958f5f7b8a6679ee127a701a521ee74961a3a528`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10493cee89e77ec8ec7093f8359147e7040171cbe811996808f6f1b860c78db`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:162126c602bcb3293ff5401b486cba4da6a3df5ed3b28758b1e9b11faeb382e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:5102d9ad6d58bc95c08d14e8fe54b4cb432ac9237cec01d33dcbd8e4850cf447
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4510590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d053ccf4f981153bfbc620038e1ef8f4350bd08832ada50fb0a0fba84572be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:02a472480673a11c995d1ea52b63c55910490337313c1211b4877f5071117f27 in /nats-server 
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:25:51 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:25:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:25:51 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:25:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9292be658bded2e584005b2d2d3c989d58b8c84c43d30cbf498884e4da11d88`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 4.5 MB (4510082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053a12f02cf2d3d90a7d26739c64349d29833ccb5f6d04c6b28d8fff2443538`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:3256353a8d53c6257a1ec8c17b572529f87360bf3b105b470da8998266e05315
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5335fe9c64c80865dd34d7f1d94b52b6d4038ce714fb04d9f318a0393262dac7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:06:00 GMT
COPY file:63d2dc292853c2a6d99433d1e8a92c091a0c775ab65a2e453be73d5448e05594 in /nats-server 
# Wed, 09 Mar 2022 23:06:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:06:01 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:06:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:06:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:06:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c9142de49642e016c3df123dce55998ce71f3777b9433742a88aa91b23f9ae9`  
		Last Modified: Wed, 09 Mar 2022 23:08:21 GMT  
		Size: 4.2 MB (4174056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232eee2ffad4b2ab84d1a4aafd3be0df1c1066f57eab6f18a4b55344b74488be`  
		Last Modified: Wed, 09 Mar 2022 23:08:18 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:ed87fc96ebeace8ad252ad368ab68f1ef976daadae90f50d8f1f917364b8050c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c348e474d9b30a28b01ce9d8566ee12c3404e1a91cddfa31c8de44ba3c6b495b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:26:11 GMT
COPY file:143b3802bb689cd4b4badd2b1463feaa3881f20e6fd303b203aa25ea206fb684 in /nats-server 
# Wed, 09 Mar 2022 23:26:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:26:12 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:26:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:26:13 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c0d2f46ac12a6f6109f1f810a72658a0faa0b7301dfa2abc4f222012bab43639`  
		Last Modified: Wed, 09 Mar 2022 23:28:32 GMT  
		Size: 4.2 MB (4168878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4e39b35a6f91da4330c0e57dcc7c9e91270e4d54cf1097b98ad3ab1a1ca178`  
		Last Modified: Wed, 09 Mar 2022 23:28:29 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4cb4ef773edd64ce015945185e30502ff5c80ea967e3ebbdf0f8d3751016ff45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bb252022527ea75cce7f45ea7463fe04e9e5b5628152fb157822c0d01bc139`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:57:14 GMT
COPY file:6d6603ade462e58030bc93029992af55dac8b9eae7e4985b5c84dd49e1ee1be2 in /nats-server 
# Wed, 09 Mar 2022 22:57:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:57:15 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:57:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:57:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5663127c1a3d9c378ea8ac20e94b430188a9dbb2675ca0b26205f9a5e1b0bf36`  
		Last Modified: Wed, 09 Mar 2022 22:58:35 GMT  
		Size: 4.2 MB (4154114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc2c19c0a6d2b137b1891d3ee3716153114e9575e2a1bc966dd0660a4c7b72`  
		Last Modified: Wed, 09 Mar 2022 22:58:34 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:9654461ee3015e4abac8d6f24720ec089a72db6650768ac224cd6280735a70f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:6d00c243dc589b03baf20fbe8c0a81279a5725d0774b275bbb9c3ebe329b570e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107611006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888ad60fdeb9e43dbbe336530422e503f539089048145cc1bbea7e51905b7095`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:16:59 GMT
RUN cmd /S /C #(nop) COPY file:741c07610cba7dd6badafc477fe411065386e3878f26a0bf50ed1d89036d6dcf in C:\nats-server.exe 
# Wed, 09 Mar 2022 23:17:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:17:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e02f868f2bb74e07262227b1156e17be47c4d960be7e9270cca8bc1dc6635b`  
		Last Modified: Wed, 09 Mar 2022 23:17:53 GMT  
		Size: 4.6 MB (4550038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9514eaf2c4a0d45ed2033bb85089d1fa90e61da7d517358225b5c6739051fcd7`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497be159edf0b99569392570b882cb48a2e72386befcbe1a0f454c6c02dba990`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c889054d0bd6db85b4b9c71958f5f7b8a6679ee127a701a521ee74961a3a528`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10493cee89e77ec8ec7093f8359147e7040171cbe811996808f6f1b860c78db`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:9654461ee3015e4abac8d6f24720ec089a72db6650768ac224cd6280735a70f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:6d00c243dc589b03baf20fbe8c0a81279a5725d0774b275bbb9c3ebe329b570e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107611006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888ad60fdeb9e43dbbe336530422e503f539089048145cc1bbea7e51905b7095`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:16:59 GMT
RUN cmd /S /C #(nop) COPY file:741c07610cba7dd6badafc477fe411065386e3878f26a0bf50ed1d89036d6dcf in C:\nats-server.exe 
# Wed, 09 Mar 2022 23:17:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:17:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:17:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e02f868f2bb74e07262227b1156e17be47c4d960be7e9270cca8bc1dc6635b`  
		Last Modified: Wed, 09 Mar 2022 23:17:53 GMT  
		Size: 4.6 MB (4550038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9514eaf2c4a0d45ed2033bb85089d1fa90e61da7d517358225b5c6739051fcd7`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497be159edf0b99569392570b882cb48a2e72386befcbe1a0f454c6c02dba990`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c889054d0bd6db85b4b9c71958f5f7b8a6679ee127a701a521ee74961a3a528`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10493cee89e77ec8ec7093f8359147e7040171cbe811996808f6f1b860c78db`  
		Last Modified: Wed, 09 Mar 2022 23:17:52 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:162126c602bcb3293ff5401b486cba4da6a3df5ed3b28758b1e9b11faeb382e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:5102d9ad6d58bc95c08d14e8fe54b4cb432ac9237cec01d33dcbd8e4850cf447
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4510590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d053ccf4f981153bfbc620038e1ef8f4350bd08832ada50fb0a0fba84572be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:02a472480673a11c995d1ea52b63c55910490337313c1211b4877f5071117f27 in /nats-server 
# Wed, 09 Mar 2022 22:25:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:25:51 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:25:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:25:51 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:25:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9292be658bded2e584005b2d2d3c989d58b8c84c43d30cbf498884e4da11d88`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 4.5 MB (4510082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053a12f02cf2d3d90a7d26739c64349d29833ccb5f6d04c6b28d8fff2443538`  
		Last Modified: Wed, 09 Mar 2022 22:26:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:3256353a8d53c6257a1ec8c17b572529f87360bf3b105b470da8998266e05315
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5335fe9c64c80865dd34d7f1d94b52b6d4038ce714fb04d9f318a0393262dac7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:06:00 GMT
COPY file:63d2dc292853c2a6d99433d1e8a92c091a0c775ab65a2e453be73d5448e05594 in /nats-server 
# Wed, 09 Mar 2022 23:06:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:06:01 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:06:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:06:02 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:06:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c9142de49642e016c3df123dce55998ce71f3777b9433742a88aa91b23f9ae9`  
		Last Modified: Wed, 09 Mar 2022 23:08:21 GMT  
		Size: 4.2 MB (4174056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232eee2ffad4b2ab84d1a4aafd3be0df1c1066f57eab6f18a4b55344b74488be`  
		Last Modified: Wed, 09 Mar 2022 23:08:18 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:ed87fc96ebeace8ad252ad368ab68f1ef976daadae90f50d8f1f917364b8050c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c348e474d9b30a28b01ce9d8566ee12c3404e1a91cddfa31c8de44ba3c6b495b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:26:11 GMT
COPY file:143b3802bb689cd4b4badd2b1463feaa3881f20e6fd303b203aa25ea206fb684 in /nats-server 
# Wed, 09 Mar 2022 23:26:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:26:12 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:26:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:26:13 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c0d2f46ac12a6f6109f1f810a72658a0faa0b7301dfa2abc4f222012bab43639`  
		Last Modified: Wed, 09 Mar 2022 23:28:32 GMT  
		Size: 4.2 MB (4168878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4e39b35a6f91da4330c0e57dcc7c9e91270e4d54cf1097b98ad3ab1a1ca178`  
		Last Modified: Wed, 09 Mar 2022 23:28:29 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4cb4ef773edd64ce015945185e30502ff5c80ea967e3ebbdf0f8d3751016ff45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bb252022527ea75cce7f45ea7463fe04e9e5b5628152fb157822c0d01bc139`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 22:57:14 GMT
COPY file:6d6603ade462e58030bc93029992af55dac8b9eae7e4985b5c84dd49e1ee1be2 in /nats-server 
# Wed, 09 Mar 2022 22:57:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 22:57:15 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 22:57:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 22:57:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 22:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5663127c1a3d9c378ea8ac20e94b430188a9dbb2675ca0b26205f9a5e1b0bf36`  
		Last Modified: Wed, 09 Mar 2022 22:58:35 GMT  
		Size: 4.2 MB (4154114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc2c19c0a6d2b137b1891d3ee3716153114e9575e2a1bc966dd0660a4c7b72`  
		Last Modified: Wed, 09 Mar 2022 22:58:34 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:de7fa8eefd8b38a00c8f113294fc03f91486cde9b572b109e98f44f2ffbf5b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:ebc084a1a8e19ddf44701886869f9009dccaf6485d52d791799326d6f89ab0d2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720689430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f84a261eca9a7469f56f24e432d4ea475732107a3ab4cf28174ee49e3ba364b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:14:16 GMT
ENV NATS_SERVER=2.7.4
# Wed, 09 Mar 2022 23:14:17 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.4/nats-server-v2.7.4-windows-amd64.zip
# Wed, 09 Mar 2022 23:14:18 GMT
ENV NATS_SERVER_SHASUM=0c98c505391e781f5f528817099dc727d83c997b3d48032c0f111d1452e8489b
# Wed, 09 Mar 2022 23:15:14 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:16:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:16:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:16:40 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:16:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:16:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301e780f30b10c083782e0d53ed487fd4d8f8d32ad6c9b9fd84d2fcc0745ee60`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7e8b0a6cef1b2ea81fcb039bc420172f4a60c3f329e6b495f9e1133e3e1534`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844fdd93ebcdfae84a099cefa8da35deaa056bff22b968bebf99205facdf928f`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f545db8b309b5166354fd80028d4bda3d85af353da1959ab615769a430d1c0`  
		Last Modified: Wed, 09 Mar 2022 23:17:34 GMT  
		Size: 348.6 KB (348621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502abb43626a3eb4c75cb441213dbb73cbb7b0df0b28ff4d77b4420ebeb536e9`  
		Last Modified: Wed, 09 Mar 2022 23:17:36 GMT  
		Size: 4.9 MB (4874834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cef267e6b969aa61db520018b018b4244a92bbceda7eba76208a24bf2bcfbaf`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57f349791c768e9ea1eaf48b6c342b2038779b4cdca397333cc20c73ded703`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06857fcc2d8c8a67e6e493c5d95e54a6bded7af6103d139e4a59072664088bff`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62c41a5b49cd11c0da902b5333c829bcc21ffcb561d931fc457eafa36ee6bc9`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:de7fa8eefd8b38a00c8f113294fc03f91486cde9b572b109e98f44f2ffbf5b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:ebc084a1a8e19ddf44701886869f9009dccaf6485d52d791799326d6f89ab0d2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720689430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f84a261eca9a7469f56f24e432d4ea475732107a3ab4cf28174ee49e3ba364b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:14:16 GMT
ENV NATS_SERVER=2.7.4
# Wed, 09 Mar 2022 23:14:17 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.4/nats-server-v2.7.4-windows-amd64.zip
# Wed, 09 Mar 2022 23:14:18 GMT
ENV NATS_SERVER_SHASUM=0c98c505391e781f5f528817099dc727d83c997b3d48032c0f111d1452e8489b
# Wed, 09 Mar 2022 23:15:14 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:16:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:16:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 23:16:40 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:16:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 23:16:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301e780f30b10c083782e0d53ed487fd4d8f8d32ad6c9b9fd84d2fcc0745ee60`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7e8b0a6cef1b2ea81fcb039bc420172f4a60c3f329e6b495f9e1133e3e1534`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844fdd93ebcdfae84a099cefa8da35deaa056bff22b968bebf99205facdf928f`  
		Last Modified: Wed, 09 Mar 2022 23:17:33 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f545db8b309b5166354fd80028d4bda3d85af353da1959ab615769a430d1c0`  
		Last Modified: Wed, 09 Mar 2022 23:17:34 GMT  
		Size: 348.6 KB (348621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502abb43626a3eb4c75cb441213dbb73cbb7b0df0b28ff4d77b4420ebeb536e9`  
		Last Modified: Wed, 09 Mar 2022 23:17:36 GMT  
		Size: 4.9 MB (4874834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cef267e6b969aa61db520018b018b4244a92bbceda7eba76208a24bf2bcfbaf`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57f349791c768e9ea1eaf48b6c342b2038779b4cdca397333cc20c73ded703`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06857fcc2d8c8a67e6e493c5d95e54a6bded7af6103d139e4a59072664088bff`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62c41a5b49cd11c0da902b5333c829bcc21ffcb561d931fc457eafa36ee6bc9`  
		Last Modified: Wed, 09 Mar 2022 23:17:31 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

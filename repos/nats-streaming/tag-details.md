<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats-streaming`

-	[`nats-streaming:0.24`](#nats-streaming024)
-	[`nats-streaming:0.24-alpine`](#nats-streaming024-alpine)
-	[`nats-streaming:0.24-alpine3.15`](#nats-streaming024-alpine315)
-	[`nats-streaming:0.24-linux`](#nats-streaming024-linux)
-	[`nats-streaming:0.24-nanoserver`](#nats-streaming024-nanoserver)
-	[`nats-streaming:0.24-nanoserver-1809`](#nats-streaming024-nanoserver-1809)
-	[`nats-streaming:0.24-scratch`](#nats-streaming024-scratch)
-	[`nats-streaming:0.24-windowsservercore`](#nats-streaming024-windowsservercore)
-	[`nats-streaming:0.24-windowsservercore-1809`](#nats-streaming024-windowsservercore-1809)
-	[`nats-streaming:0.24.2`](#nats-streaming0242)
-	[`nats-streaming:0.24.2-alpine`](#nats-streaming0242-alpine)
-	[`nats-streaming:0.24.2-alpine3.15`](#nats-streaming0242-alpine315)
-	[`nats-streaming:0.24.2-linux`](#nats-streaming0242-linux)
-	[`nats-streaming:0.24.2-nanoserver`](#nats-streaming0242-nanoserver)
-	[`nats-streaming:0.24.2-nanoserver-1809`](#nats-streaming0242-nanoserver-1809)
-	[`nats-streaming:0.24.2-scratch`](#nats-streaming0242-scratch)
-	[`nats-streaming:0.24.2-windowsservercore`](#nats-streaming0242-windowsservercore)
-	[`nats-streaming:0.24.2-windowsservercore-1809`](#nats-streaming0242-windowsservercore-1809)
-	[`nats-streaming:alpine`](#nats-streamingalpine)
-	[`nats-streaming:alpine3.15`](#nats-streamingalpine315)
-	[`nats-streaming:latest`](#nats-streaminglatest)
-	[`nats-streaming:linux`](#nats-streaminglinux)
-	[`nats-streaming:nanoserver`](#nats-streamingnanoserver)
-	[`nats-streaming:nanoserver-1809`](#nats-streamingnanoserver-1809)
-	[`nats-streaming:scratch`](#nats-streamingscratch)
-	[`nats-streaming:windowsservercore`](#nats-streamingwindowsservercore)
-	[`nats-streaming:windowsservercore-1809`](#nats-streamingwindowsservercore-1809)

## `nats-streaming:0.24`

```console
$ docker pull nats-streaming@sha256:6da3b6f566aacd181420cab281d4cd4b82b7ac6703dd4a65f2975cde905a8298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2565; amd64

### `nats-streaming:0.24` - linux; amd64

```console
$ docker pull nats-streaming@sha256:b0264ae003ad4b65e28ecd00f38f5bbdf7a937471c26111d88b6990ecc49bdbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7071520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc31f3812f5256ec02071ca3e295a5be59a2d326417a7b55569235b47a7a2fc9`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 02:19:54 GMT
COPY file:47ac28785512ec4ac0869ce12d480005915c64c985d55605a5d2ed5a852389fb in /nats-streaming-server 
# Fri, 25 Feb 2022 02:19:54 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:19:55 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 02:19:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6726d9237da5dd8f18cb24ee666179433f7a040706b881549b18eaccdb2b7b0c`  
		Last Modified: Fri, 25 Feb 2022 02:20:36 GMT  
		Size: 7.1 MB (7071520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:3d85afadae9925ec2a82250ddd268054b9844d01605ed3cf9d2b0a17cce21dfa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6587572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51f2eea369c9614b4ab5aeaa4dcd4ed04a754251557bdccdb339712935c2f63`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 02:53:52 GMT
COPY file:558cfcd3a5b3207402c443e2aac4e1a401ccbf8ee0c6f1b92251ef816558b646 in /nats-streaming-server 
# Fri, 25 Feb 2022 02:53:52 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:53:53 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 02:53:53 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a2f9d3181316d01f63a8016443dca42572e115447efd51051bc10f47d69fda7f`  
		Last Modified: Fri, 25 Feb 2022 02:55:46 GMT  
		Size: 6.6 MB (6587572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:91fe5ea5ea66dbce33f105342aa2c257de6efebcf2c84c517c76e43887994ba1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6577227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ae60167dced131f5b275c9a42d53766267caad88d5f2e8429543860190fa1f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 03:02:25 GMT
COPY file:81da864fb3ebeee9861cc8b3daa8a3454787d8decad14ec3d175e6bd72471275 in /nats-streaming-server 
# Fri, 25 Feb 2022 03:02:25 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:02:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 03:02:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:21fca66c0d285fa1440c4688da4adb5a2b07fb2d63f613af9f984b8bbfeab18f`  
		Last Modified: Fri, 25 Feb 2022 03:04:21 GMT  
		Size: 6.6 MB (6577227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:25f8d00ba1c21fb799a3c4f2cac7e1f828247ebeae544162daa80f83138fee9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9df95b5224c0937c31982baefb4b2eb1f16808dba0e58c13b9afa9a81bf8e71`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 03:03:58 GMT
COPY file:20e40bb6a5f58c9706bc32195e036ddbef77390672e5230781fec0d06314cd48 in /nats-streaming-server 
# Fri, 25 Feb 2022 03:03:58 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:03:59 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 03:04:00 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:cec2c76695402528056a4f2eeb40e25ac44052fb78855dce3f8a746df6656a94`  
		Last Modified: Fri, 25 Feb 2022 03:04:59 GMT  
		Size: 6.5 MB (6495743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats-streaming@sha256:869d74ad56522c6b9a695cd1db6d5c2d5789b67ac3abc60ef7486db75c5db40d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110269675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5932d54e1864e9f49901b4c39dfe687232bf2b59e8ecfd3242b36ad57e523536`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Feb 2022 02:20:56 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Fri, 25 Feb 2022 02:20:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:20:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 25 Feb 2022 02:21:01 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5030a6d1fb6074f83ecd43d63329d1ce9e47ce7abb822efe4b048525348294`  
		Last Modified: Fri, 25 Feb 2022 02:21:56 GMT  
		Size: 7.2 MB (7177970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68877bcb599a81befa9c6441501d142f7669207fa0787cee6e74f4ae3cb5aad`  
		Last Modified: Fri, 25 Feb 2022 02:21:55 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91344cbf81e04fb8ef879b3a388d8fcaa65d3a70106bd7f96b8954c9564cee32`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab42220f2fa6e2a4c6b6d10260b5cd783c0ba3cfdd4ff423484667ee782017e`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-alpine`

```console
$ docker pull nats-streaming@sha256:6c06d99e350dfd64d6f90744011e606d51bde2f02fe0fbfdcaa0a7ee8105ad52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:e0b5c46db65c6031b96850c7750125ae972bacaf7acd500a342529587f78cdb6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10163584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73fdc06ff9592dbaa07f7638b8ec5b77e29f0f50e5810e01addc1712d27b926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:19:43 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:19:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 02:19:46 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 02:19:46 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:19:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:19:46 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6d6be22662448ec27471291d386c2cf9e303b0c18135d61435ecab66e3d190`  
		Last Modified: Fri, 25 Feb 2022 02:20:17 GMT  
		Size: 7.3 MB (7344748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ef5642b30ec627703bbd9831a4eb2b34fbc32ce3af4c52751b3c13b05fa1f3`  
		Last Modified: Fri, 25 Feb 2022 02:20:16 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:16bfad93443d1e11ea456827a60788ffaaf287abd7a898abd66df24ce1973675
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9492160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7228f54cd28bbac00b2fd561e721cece5b97bdd93a8582be95db0a18ef521e3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:53:26 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 02:53:31 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 02:53:32 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:53:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:53:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162bf98370c73025244b6844c0fb4795edd0cf2437d3ccedad11cf1e27309826`  
		Last Modified: Fri, 25 Feb 2022 02:55:14 GMT  
		Size: 6.9 MB (6860315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64992fd6ef19b0475e618937bb5276e19cb2e256048d14fefcd9ceea4334d758`  
		Last Modified: Fri, 25 Feb 2022 02:55:10 GMT  
		Size: 424.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:353aec3dccf8ecf1b39edab2415d3ea3c9281434ddf10db8c7a1f36df0be9f7f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9285283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54087071c470d19a57112b054034098a0e6a491034a31578b6034a497fa0171`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:01:55 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 03:01:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 03:02:00 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 03:02:00 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:02:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:02:01 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fa952029dc8a0c57ab16e41b9b4d9f7302794c501d3c481e6576062a23683e`  
		Last Modified: Fri, 25 Feb 2022 03:03:50 GMT  
		Size: 6.9 MB (6850097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360fe50d6904c4c5e840ab926f40c58df2a2e6b905c7493ae065c23b443f4188`  
		Last Modified: Fri, 25 Feb 2022 03:03:45 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:2ee72ee2576a5cbbcc8b3cfb713c4f90292c80ec08ec0a3b156d8cd93c43de42
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9484460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b04cc618c6bdfcbe7e945393204707f2b00244897ddafba37db190dbdac9854`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:03:39 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 03:03:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 03:03:45 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 03:03:45 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:03:47 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c940513d538449d692b24e2bad765ddf948bdac501988eb123df158ee291d31`  
		Last Modified: Fri, 25 Feb 2022 03:04:36 GMT  
		Size: 6.8 MB (6768603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6d2d9b3fc25f46965b7cf1f1633f11e7f4a2fd071e9b86c544f74b4279599b`  
		Last Modified: Fri, 25 Feb 2022 03:04:35 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-alpine3.15`

```console
$ docker pull nats-streaming@sha256:6c06d99e350dfd64d6f90744011e606d51bde2f02fe0fbfdcaa0a7ee8105ad52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24-alpine3.15` - linux; amd64

```console
$ docker pull nats-streaming@sha256:e0b5c46db65c6031b96850c7750125ae972bacaf7acd500a342529587f78cdb6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10163584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73fdc06ff9592dbaa07f7638b8ec5b77e29f0f50e5810e01addc1712d27b926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:19:43 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:19:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 02:19:46 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 02:19:46 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:19:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:19:46 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6d6be22662448ec27471291d386c2cf9e303b0c18135d61435ecab66e3d190`  
		Last Modified: Fri, 25 Feb 2022 02:20:17 GMT  
		Size: 7.3 MB (7344748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ef5642b30ec627703bbd9831a4eb2b34fbc32ce3af4c52751b3c13b05fa1f3`  
		Last Modified: Fri, 25 Feb 2022 02:20:16 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:16bfad93443d1e11ea456827a60788ffaaf287abd7a898abd66df24ce1973675
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9492160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7228f54cd28bbac00b2fd561e721cece5b97bdd93a8582be95db0a18ef521e3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:53:26 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 02:53:31 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 02:53:32 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:53:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:53:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162bf98370c73025244b6844c0fb4795edd0cf2437d3ccedad11cf1e27309826`  
		Last Modified: Fri, 25 Feb 2022 02:55:14 GMT  
		Size: 6.9 MB (6860315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64992fd6ef19b0475e618937bb5276e19cb2e256048d14fefcd9ceea4334d758`  
		Last Modified: Fri, 25 Feb 2022 02:55:10 GMT  
		Size: 424.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:353aec3dccf8ecf1b39edab2415d3ea3c9281434ddf10db8c7a1f36df0be9f7f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9285283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54087071c470d19a57112b054034098a0e6a491034a31578b6034a497fa0171`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:01:55 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 03:01:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 03:02:00 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 03:02:00 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:02:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:02:01 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fa952029dc8a0c57ab16e41b9b4d9f7302794c501d3c481e6576062a23683e`  
		Last Modified: Fri, 25 Feb 2022 03:03:50 GMT  
		Size: 6.9 MB (6850097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360fe50d6904c4c5e840ab926f40c58df2a2e6b905c7493ae065c23b443f4188`  
		Last Modified: Fri, 25 Feb 2022 03:03:45 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:2ee72ee2576a5cbbcc8b3cfb713c4f90292c80ec08ec0a3b156d8cd93c43de42
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9484460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b04cc618c6bdfcbe7e945393204707f2b00244897ddafba37db190dbdac9854`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:03:39 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 03:03:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 03:03:45 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 03:03:45 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:03:47 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c940513d538449d692b24e2bad765ddf948bdac501988eb123df158ee291d31`  
		Last Modified: Fri, 25 Feb 2022 03:04:36 GMT  
		Size: 6.8 MB (6768603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6d2d9b3fc25f46965b7cf1f1633f11e7f4a2fd071e9b86c544f74b4279599b`  
		Last Modified: Fri, 25 Feb 2022 03:04:35 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-linux`

```console
$ docker pull nats-streaming@sha256:b21b852fe0586ae78b61cc93bb284833f978bb3769a98f8777181dddbfe6783b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:b0264ae003ad4b65e28ecd00f38f5bbdf7a937471c26111d88b6990ecc49bdbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7071520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc31f3812f5256ec02071ca3e295a5be59a2d326417a7b55569235b47a7a2fc9`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 02:19:54 GMT
COPY file:47ac28785512ec4ac0869ce12d480005915c64c985d55605a5d2ed5a852389fb in /nats-streaming-server 
# Fri, 25 Feb 2022 02:19:54 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:19:55 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 02:19:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6726d9237da5dd8f18cb24ee666179433f7a040706b881549b18eaccdb2b7b0c`  
		Last Modified: Fri, 25 Feb 2022 02:20:36 GMT  
		Size: 7.1 MB (7071520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:3d85afadae9925ec2a82250ddd268054b9844d01605ed3cf9d2b0a17cce21dfa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6587572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51f2eea369c9614b4ab5aeaa4dcd4ed04a754251557bdccdb339712935c2f63`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 02:53:52 GMT
COPY file:558cfcd3a5b3207402c443e2aac4e1a401ccbf8ee0c6f1b92251ef816558b646 in /nats-streaming-server 
# Fri, 25 Feb 2022 02:53:52 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:53:53 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 02:53:53 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a2f9d3181316d01f63a8016443dca42572e115447efd51051bc10f47d69fda7f`  
		Last Modified: Fri, 25 Feb 2022 02:55:46 GMT  
		Size: 6.6 MB (6587572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:91fe5ea5ea66dbce33f105342aa2c257de6efebcf2c84c517c76e43887994ba1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6577227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ae60167dced131f5b275c9a42d53766267caad88d5f2e8429543860190fa1f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 03:02:25 GMT
COPY file:81da864fb3ebeee9861cc8b3daa8a3454787d8decad14ec3d175e6bd72471275 in /nats-streaming-server 
# Fri, 25 Feb 2022 03:02:25 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:02:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 03:02:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:21fca66c0d285fa1440c4688da4adb5a2b07fb2d63f613af9f984b8bbfeab18f`  
		Last Modified: Fri, 25 Feb 2022 03:04:21 GMT  
		Size: 6.6 MB (6577227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:25f8d00ba1c21fb799a3c4f2cac7e1f828247ebeae544162daa80f83138fee9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9df95b5224c0937c31982baefb4b2eb1f16808dba0e58c13b9afa9a81bf8e71`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 03:03:58 GMT
COPY file:20e40bb6a5f58c9706bc32195e036ddbef77390672e5230781fec0d06314cd48 in /nats-streaming-server 
# Fri, 25 Feb 2022 03:03:58 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:03:59 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 03:04:00 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:cec2c76695402528056a4f2eeb40e25ac44052fb78855dce3f8a746df6656a94`  
		Last Modified: Fri, 25 Feb 2022 03:04:59 GMT  
		Size: 6.5 MB (6495743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-nanoserver`

```console
$ docker pull nats-streaming@sha256:8b491322c8ffd9bf3a1601284c03e767da655c349ab692aeac5e48c237c9ec8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats-streaming:0.24-nanoserver` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats-streaming@sha256:869d74ad56522c6b9a695cd1db6d5c2d5789b67ac3abc60ef7486db75c5db40d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110269675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5932d54e1864e9f49901b4c39dfe687232bf2b59e8ecfd3242b36ad57e523536`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Feb 2022 02:20:56 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Fri, 25 Feb 2022 02:20:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:20:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 25 Feb 2022 02:21:01 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5030a6d1fb6074f83ecd43d63329d1ce9e47ce7abb822efe4b048525348294`  
		Last Modified: Fri, 25 Feb 2022 02:21:56 GMT  
		Size: 7.2 MB (7177970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68877bcb599a81befa9c6441501d142f7669207fa0787cee6e74f4ae3cb5aad`  
		Last Modified: Fri, 25 Feb 2022 02:21:55 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91344cbf81e04fb8ef879b3a388d8fcaa65d3a70106bd7f96b8954c9564cee32`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab42220f2fa6e2a4c6b6d10260b5cd783c0ba3cfdd4ff423484667ee782017e`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:8b491322c8ffd9bf3a1601284c03e767da655c349ab692aeac5e48c237c9ec8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats-streaming:0.24-nanoserver-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats-streaming@sha256:869d74ad56522c6b9a695cd1db6d5c2d5789b67ac3abc60ef7486db75c5db40d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110269675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5932d54e1864e9f49901b4c39dfe687232bf2b59e8ecfd3242b36ad57e523536`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Feb 2022 02:20:56 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Fri, 25 Feb 2022 02:20:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:20:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 25 Feb 2022 02:21:01 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5030a6d1fb6074f83ecd43d63329d1ce9e47ce7abb822efe4b048525348294`  
		Last Modified: Fri, 25 Feb 2022 02:21:56 GMT  
		Size: 7.2 MB (7177970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68877bcb599a81befa9c6441501d142f7669207fa0787cee6e74f4ae3cb5aad`  
		Last Modified: Fri, 25 Feb 2022 02:21:55 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91344cbf81e04fb8ef879b3a388d8fcaa65d3a70106bd7f96b8954c9564cee32`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab42220f2fa6e2a4c6b6d10260b5cd783c0ba3cfdd4ff423484667ee782017e`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-scratch`

```console
$ docker pull nats-streaming@sha256:b21b852fe0586ae78b61cc93bb284833f978bb3769a98f8777181dddbfe6783b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:b0264ae003ad4b65e28ecd00f38f5bbdf7a937471c26111d88b6990ecc49bdbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7071520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc31f3812f5256ec02071ca3e295a5be59a2d326417a7b55569235b47a7a2fc9`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 02:19:54 GMT
COPY file:47ac28785512ec4ac0869ce12d480005915c64c985d55605a5d2ed5a852389fb in /nats-streaming-server 
# Fri, 25 Feb 2022 02:19:54 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:19:55 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 02:19:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6726d9237da5dd8f18cb24ee666179433f7a040706b881549b18eaccdb2b7b0c`  
		Last Modified: Fri, 25 Feb 2022 02:20:36 GMT  
		Size: 7.1 MB (7071520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:3d85afadae9925ec2a82250ddd268054b9844d01605ed3cf9d2b0a17cce21dfa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6587572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51f2eea369c9614b4ab5aeaa4dcd4ed04a754251557bdccdb339712935c2f63`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 02:53:52 GMT
COPY file:558cfcd3a5b3207402c443e2aac4e1a401ccbf8ee0c6f1b92251ef816558b646 in /nats-streaming-server 
# Fri, 25 Feb 2022 02:53:52 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:53:53 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 02:53:53 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a2f9d3181316d01f63a8016443dca42572e115447efd51051bc10f47d69fda7f`  
		Last Modified: Fri, 25 Feb 2022 02:55:46 GMT  
		Size: 6.6 MB (6587572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:91fe5ea5ea66dbce33f105342aa2c257de6efebcf2c84c517c76e43887994ba1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6577227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ae60167dced131f5b275c9a42d53766267caad88d5f2e8429543860190fa1f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 03:02:25 GMT
COPY file:81da864fb3ebeee9861cc8b3daa8a3454787d8decad14ec3d175e6bd72471275 in /nats-streaming-server 
# Fri, 25 Feb 2022 03:02:25 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:02:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 03:02:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:21fca66c0d285fa1440c4688da4adb5a2b07fb2d63f613af9f984b8bbfeab18f`  
		Last Modified: Fri, 25 Feb 2022 03:04:21 GMT  
		Size: 6.6 MB (6577227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:25f8d00ba1c21fb799a3c4f2cac7e1f828247ebeae544162daa80f83138fee9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9df95b5224c0937c31982baefb4b2eb1f16808dba0e58c13b9afa9a81bf8e71`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 03:03:58 GMT
COPY file:20e40bb6a5f58c9706bc32195e036ddbef77390672e5230781fec0d06314cd48 in /nats-streaming-server 
# Fri, 25 Feb 2022 03:03:58 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:03:59 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 03:04:00 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:cec2c76695402528056a4f2eeb40e25ac44052fb78855dce3f8a746df6656a94`  
		Last Modified: Fri, 25 Feb 2022 03:04:59 GMT  
		Size: 6.5 MB (6495743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-windowsservercore`

```console
$ docker pull nats-streaming@sha256:819b001ad6d44c72b199d7aac599345d3f20d8ee74b4a472a90acea9c399184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats-streaming:0.24-windowsservercore` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats-streaming@sha256:db604481a007d58765b7c40c26c49745cf093d4e49837b5bf0e93a4669f00911
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2721626080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e006b586ed1498bdbe651518f76ddeb751bc50fa16c0ec6680dc7e2947f3fb29`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 15:04:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Feb 2022 18:10:54 GMT
ENV NATS_DOCKERIZED=1
# Fri, 25 Feb 2022 02:17:55 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:17:55 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.2/nats-streaming-server-v0.24.2-windows-amd64.zip
# Fri, 25 Feb 2022 02:17:56 GMT
ENV NATS_STREAMING_SERVER_SHASUM=15a7692d56bc3b2d6fb84b89d631205a927a807d3c901e6929dfcb82445149d2
# Fri, 25 Feb 2022 02:18:56 GMT
RUN Set-PSDebug -Trace 2
# Fri, 25 Feb 2022 02:20:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 25 Feb 2022 02:20:45 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:20:45 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 25 Feb 2022 02:20:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f49d3791198cf2ea875fd54ce3bb715670742d4a58c00252395ad1b74036662a`  
		Last Modified: Wed, 09 Feb 2022 16:39:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4235aeeb4e8b577cc7aa26c7994ec94c94dd53a38764fc510b330b77cef4abad`  
		Last Modified: Wed, 09 Feb 2022 18:14:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c6d42960df831ce1448963636541141a4ec9089d489c5ee11b5e310cdbbbf`  
		Last Modified: Fri, 25 Feb 2022 02:21:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e40b6a7fa5407b7bc18d72dd18e47e4f538a618fe7aee3f63df8657eec3c822`  
		Last Modified: Fri, 25 Feb 2022 02:21:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ddf61c72a1d8861fc97f277505fbe4613829e3758bc385f97cdbc77d986fb3`  
		Last Modified: Fri, 25 Feb 2022 02:21:35 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0697e7113057967b17bb9804201e7ad14aba29e62471fd16c36b3c9efaaf2d`  
		Last Modified: Fri, 25 Feb 2022 02:21:33 GMT  
		Size: 374.2 KB (374241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6d53518d92b0f4b70d8d36384f340ec236cbac76d67c8ef7574480961946c1`  
		Last Modified: Fri, 25 Feb 2022 02:21:40 GMT  
		Size: 7.5 MB (7526089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d576464a46e0c69764bf23a274474e67f4f10707edf6e9879a6a6c07f7eeb22`  
		Last Modified: Fri, 25 Feb 2022 02:21:32 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c59dbff87a88dbf092b9fff74f90edd33ace3d56fd401555cdd81a28e22f2e1`  
		Last Modified: Fri, 25 Feb 2022 02:21:32 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6267c71e5c55502f4d5c4662d71f5393dcd6013bb813937fd072667ec810143`  
		Last Modified: Fri, 25 Feb 2022 02:21:32 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:819b001ad6d44c72b199d7aac599345d3f20d8ee74b4a472a90acea9c399184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats-streaming:0.24-windowsservercore-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats-streaming@sha256:db604481a007d58765b7c40c26c49745cf093d4e49837b5bf0e93a4669f00911
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2721626080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e006b586ed1498bdbe651518f76ddeb751bc50fa16c0ec6680dc7e2947f3fb29`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 15:04:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Feb 2022 18:10:54 GMT
ENV NATS_DOCKERIZED=1
# Fri, 25 Feb 2022 02:17:55 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:17:55 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.2/nats-streaming-server-v0.24.2-windows-amd64.zip
# Fri, 25 Feb 2022 02:17:56 GMT
ENV NATS_STREAMING_SERVER_SHASUM=15a7692d56bc3b2d6fb84b89d631205a927a807d3c901e6929dfcb82445149d2
# Fri, 25 Feb 2022 02:18:56 GMT
RUN Set-PSDebug -Trace 2
# Fri, 25 Feb 2022 02:20:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 25 Feb 2022 02:20:45 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:20:45 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 25 Feb 2022 02:20:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f49d3791198cf2ea875fd54ce3bb715670742d4a58c00252395ad1b74036662a`  
		Last Modified: Wed, 09 Feb 2022 16:39:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4235aeeb4e8b577cc7aa26c7994ec94c94dd53a38764fc510b330b77cef4abad`  
		Last Modified: Wed, 09 Feb 2022 18:14:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c6d42960df831ce1448963636541141a4ec9089d489c5ee11b5e310cdbbbf`  
		Last Modified: Fri, 25 Feb 2022 02:21:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e40b6a7fa5407b7bc18d72dd18e47e4f538a618fe7aee3f63df8657eec3c822`  
		Last Modified: Fri, 25 Feb 2022 02:21:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ddf61c72a1d8861fc97f277505fbe4613829e3758bc385f97cdbc77d986fb3`  
		Last Modified: Fri, 25 Feb 2022 02:21:35 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0697e7113057967b17bb9804201e7ad14aba29e62471fd16c36b3c9efaaf2d`  
		Last Modified: Fri, 25 Feb 2022 02:21:33 GMT  
		Size: 374.2 KB (374241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6d53518d92b0f4b70d8d36384f340ec236cbac76d67c8ef7574480961946c1`  
		Last Modified: Fri, 25 Feb 2022 02:21:40 GMT  
		Size: 7.5 MB (7526089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d576464a46e0c69764bf23a274474e67f4f10707edf6e9879a6a6c07f7eeb22`  
		Last Modified: Fri, 25 Feb 2022 02:21:32 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c59dbff87a88dbf092b9fff74f90edd33ace3d56fd401555cdd81a28e22f2e1`  
		Last Modified: Fri, 25 Feb 2022 02:21:32 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6267c71e5c55502f4d5c4662d71f5393dcd6013bb813937fd072667ec810143`  
		Last Modified: Fri, 25 Feb 2022 02:21:32 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.2`

```console
$ docker pull nats-streaming@sha256:6da3b6f566aacd181420cab281d4cd4b82b7ac6703dd4a65f2975cde905a8298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2565; amd64

### `nats-streaming:0.24.2` - linux; amd64

```console
$ docker pull nats-streaming@sha256:b0264ae003ad4b65e28ecd00f38f5bbdf7a937471c26111d88b6990ecc49bdbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7071520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc31f3812f5256ec02071ca3e295a5be59a2d326417a7b55569235b47a7a2fc9`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 02:19:54 GMT
COPY file:47ac28785512ec4ac0869ce12d480005915c64c985d55605a5d2ed5a852389fb in /nats-streaming-server 
# Fri, 25 Feb 2022 02:19:54 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:19:55 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 02:19:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6726d9237da5dd8f18cb24ee666179433f7a040706b881549b18eaccdb2b7b0c`  
		Last Modified: Fri, 25 Feb 2022 02:20:36 GMT  
		Size: 7.1 MB (7071520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.2` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:3d85afadae9925ec2a82250ddd268054b9844d01605ed3cf9d2b0a17cce21dfa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6587572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51f2eea369c9614b4ab5aeaa4dcd4ed04a754251557bdccdb339712935c2f63`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 02:53:52 GMT
COPY file:558cfcd3a5b3207402c443e2aac4e1a401ccbf8ee0c6f1b92251ef816558b646 in /nats-streaming-server 
# Fri, 25 Feb 2022 02:53:52 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:53:53 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 02:53:53 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a2f9d3181316d01f63a8016443dca42572e115447efd51051bc10f47d69fda7f`  
		Last Modified: Fri, 25 Feb 2022 02:55:46 GMT  
		Size: 6.6 MB (6587572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.2` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:91fe5ea5ea66dbce33f105342aa2c257de6efebcf2c84c517c76e43887994ba1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6577227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ae60167dced131f5b275c9a42d53766267caad88d5f2e8429543860190fa1f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 03:02:25 GMT
COPY file:81da864fb3ebeee9861cc8b3daa8a3454787d8decad14ec3d175e6bd72471275 in /nats-streaming-server 
# Fri, 25 Feb 2022 03:02:25 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:02:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 03:02:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:21fca66c0d285fa1440c4688da4adb5a2b07fb2d63f613af9f984b8bbfeab18f`  
		Last Modified: Fri, 25 Feb 2022 03:04:21 GMT  
		Size: 6.6 MB (6577227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.2` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:25f8d00ba1c21fb799a3c4f2cac7e1f828247ebeae544162daa80f83138fee9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9df95b5224c0937c31982baefb4b2eb1f16808dba0e58c13b9afa9a81bf8e71`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 03:03:58 GMT
COPY file:20e40bb6a5f58c9706bc32195e036ddbef77390672e5230781fec0d06314cd48 in /nats-streaming-server 
# Fri, 25 Feb 2022 03:03:58 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:03:59 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 03:04:00 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:cec2c76695402528056a4f2eeb40e25ac44052fb78855dce3f8a746df6656a94`  
		Last Modified: Fri, 25 Feb 2022 03:04:59 GMT  
		Size: 6.5 MB (6495743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.2` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats-streaming@sha256:869d74ad56522c6b9a695cd1db6d5c2d5789b67ac3abc60ef7486db75c5db40d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110269675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5932d54e1864e9f49901b4c39dfe687232bf2b59e8ecfd3242b36ad57e523536`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Feb 2022 02:20:56 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Fri, 25 Feb 2022 02:20:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:20:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 25 Feb 2022 02:21:01 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5030a6d1fb6074f83ecd43d63329d1ce9e47ce7abb822efe4b048525348294`  
		Last Modified: Fri, 25 Feb 2022 02:21:56 GMT  
		Size: 7.2 MB (7177970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68877bcb599a81befa9c6441501d142f7669207fa0787cee6e74f4ae3cb5aad`  
		Last Modified: Fri, 25 Feb 2022 02:21:55 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91344cbf81e04fb8ef879b3a388d8fcaa65d3a70106bd7f96b8954c9564cee32`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab42220f2fa6e2a4c6b6d10260b5cd783c0ba3cfdd4ff423484667ee782017e`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.2-alpine`

```console
$ docker pull nats-streaming@sha256:6c06d99e350dfd64d6f90744011e606d51bde2f02fe0fbfdcaa0a7ee8105ad52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24.2-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:e0b5c46db65c6031b96850c7750125ae972bacaf7acd500a342529587f78cdb6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10163584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73fdc06ff9592dbaa07f7638b8ec5b77e29f0f50e5810e01addc1712d27b926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:19:43 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:19:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 02:19:46 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 02:19:46 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:19:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:19:46 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6d6be22662448ec27471291d386c2cf9e303b0c18135d61435ecab66e3d190`  
		Last Modified: Fri, 25 Feb 2022 02:20:17 GMT  
		Size: 7.3 MB (7344748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ef5642b30ec627703bbd9831a4eb2b34fbc32ce3af4c52751b3c13b05fa1f3`  
		Last Modified: Fri, 25 Feb 2022 02:20:16 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.2-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:16bfad93443d1e11ea456827a60788ffaaf287abd7a898abd66df24ce1973675
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9492160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7228f54cd28bbac00b2fd561e721cece5b97bdd93a8582be95db0a18ef521e3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:53:26 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 02:53:31 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 02:53:32 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:53:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:53:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162bf98370c73025244b6844c0fb4795edd0cf2437d3ccedad11cf1e27309826`  
		Last Modified: Fri, 25 Feb 2022 02:55:14 GMT  
		Size: 6.9 MB (6860315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64992fd6ef19b0475e618937bb5276e19cb2e256048d14fefcd9ceea4334d758`  
		Last Modified: Fri, 25 Feb 2022 02:55:10 GMT  
		Size: 424.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.2-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:353aec3dccf8ecf1b39edab2415d3ea3c9281434ddf10db8c7a1f36df0be9f7f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9285283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54087071c470d19a57112b054034098a0e6a491034a31578b6034a497fa0171`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:01:55 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 03:01:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 03:02:00 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 03:02:00 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:02:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:02:01 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fa952029dc8a0c57ab16e41b9b4d9f7302794c501d3c481e6576062a23683e`  
		Last Modified: Fri, 25 Feb 2022 03:03:50 GMT  
		Size: 6.9 MB (6850097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360fe50d6904c4c5e840ab926f40c58df2a2e6b905c7493ae065c23b443f4188`  
		Last Modified: Fri, 25 Feb 2022 03:03:45 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:2ee72ee2576a5cbbcc8b3cfb713c4f90292c80ec08ec0a3b156d8cd93c43de42
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9484460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b04cc618c6bdfcbe7e945393204707f2b00244897ddafba37db190dbdac9854`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:03:39 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 03:03:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 03:03:45 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 03:03:45 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:03:47 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c940513d538449d692b24e2bad765ddf948bdac501988eb123df158ee291d31`  
		Last Modified: Fri, 25 Feb 2022 03:04:36 GMT  
		Size: 6.8 MB (6768603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6d2d9b3fc25f46965b7cf1f1633f11e7f4a2fd071e9b86c544f74b4279599b`  
		Last Modified: Fri, 25 Feb 2022 03:04:35 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.2-alpine3.15`

```console
$ docker pull nats-streaming@sha256:6c06d99e350dfd64d6f90744011e606d51bde2f02fe0fbfdcaa0a7ee8105ad52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24.2-alpine3.15` - linux; amd64

```console
$ docker pull nats-streaming@sha256:e0b5c46db65c6031b96850c7750125ae972bacaf7acd500a342529587f78cdb6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10163584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73fdc06ff9592dbaa07f7638b8ec5b77e29f0f50e5810e01addc1712d27b926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:19:43 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:19:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 02:19:46 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 02:19:46 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:19:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:19:46 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6d6be22662448ec27471291d386c2cf9e303b0c18135d61435ecab66e3d190`  
		Last Modified: Fri, 25 Feb 2022 02:20:17 GMT  
		Size: 7.3 MB (7344748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ef5642b30ec627703bbd9831a4eb2b34fbc32ce3af4c52751b3c13b05fa1f3`  
		Last Modified: Fri, 25 Feb 2022 02:20:16 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.2-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:16bfad93443d1e11ea456827a60788ffaaf287abd7a898abd66df24ce1973675
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9492160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7228f54cd28bbac00b2fd561e721cece5b97bdd93a8582be95db0a18ef521e3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:53:26 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 02:53:31 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 02:53:32 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:53:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:53:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162bf98370c73025244b6844c0fb4795edd0cf2437d3ccedad11cf1e27309826`  
		Last Modified: Fri, 25 Feb 2022 02:55:14 GMT  
		Size: 6.9 MB (6860315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64992fd6ef19b0475e618937bb5276e19cb2e256048d14fefcd9ceea4334d758`  
		Last Modified: Fri, 25 Feb 2022 02:55:10 GMT  
		Size: 424.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.2-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:353aec3dccf8ecf1b39edab2415d3ea3c9281434ddf10db8c7a1f36df0be9f7f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9285283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54087071c470d19a57112b054034098a0e6a491034a31578b6034a497fa0171`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:01:55 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 03:01:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 03:02:00 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 03:02:00 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:02:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:02:01 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fa952029dc8a0c57ab16e41b9b4d9f7302794c501d3c481e6576062a23683e`  
		Last Modified: Fri, 25 Feb 2022 03:03:50 GMT  
		Size: 6.9 MB (6850097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360fe50d6904c4c5e840ab926f40c58df2a2e6b905c7493ae065c23b443f4188`  
		Last Modified: Fri, 25 Feb 2022 03:03:45 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.2-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:2ee72ee2576a5cbbcc8b3cfb713c4f90292c80ec08ec0a3b156d8cd93c43de42
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9484460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b04cc618c6bdfcbe7e945393204707f2b00244897ddafba37db190dbdac9854`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:03:39 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 03:03:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 03:03:45 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 03:03:45 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:03:47 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c940513d538449d692b24e2bad765ddf948bdac501988eb123df158ee291d31`  
		Last Modified: Fri, 25 Feb 2022 03:04:36 GMT  
		Size: 6.8 MB (6768603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6d2d9b3fc25f46965b7cf1f1633f11e7f4a2fd071e9b86c544f74b4279599b`  
		Last Modified: Fri, 25 Feb 2022 03:04:35 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.2-linux`

```console
$ docker pull nats-streaming@sha256:b21b852fe0586ae78b61cc93bb284833f978bb3769a98f8777181dddbfe6783b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24.2-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:b0264ae003ad4b65e28ecd00f38f5bbdf7a937471c26111d88b6990ecc49bdbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7071520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc31f3812f5256ec02071ca3e295a5be59a2d326417a7b55569235b47a7a2fc9`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 02:19:54 GMT
COPY file:47ac28785512ec4ac0869ce12d480005915c64c985d55605a5d2ed5a852389fb in /nats-streaming-server 
# Fri, 25 Feb 2022 02:19:54 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:19:55 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 02:19:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6726d9237da5dd8f18cb24ee666179433f7a040706b881549b18eaccdb2b7b0c`  
		Last Modified: Fri, 25 Feb 2022 02:20:36 GMT  
		Size: 7.1 MB (7071520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.2-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:3d85afadae9925ec2a82250ddd268054b9844d01605ed3cf9d2b0a17cce21dfa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6587572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51f2eea369c9614b4ab5aeaa4dcd4ed04a754251557bdccdb339712935c2f63`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 02:53:52 GMT
COPY file:558cfcd3a5b3207402c443e2aac4e1a401ccbf8ee0c6f1b92251ef816558b646 in /nats-streaming-server 
# Fri, 25 Feb 2022 02:53:52 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:53:53 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 02:53:53 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a2f9d3181316d01f63a8016443dca42572e115447efd51051bc10f47d69fda7f`  
		Last Modified: Fri, 25 Feb 2022 02:55:46 GMT  
		Size: 6.6 MB (6587572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.2-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:91fe5ea5ea66dbce33f105342aa2c257de6efebcf2c84c517c76e43887994ba1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6577227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ae60167dced131f5b275c9a42d53766267caad88d5f2e8429543860190fa1f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 03:02:25 GMT
COPY file:81da864fb3ebeee9861cc8b3daa8a3454787d8decad14ec3d175e6bd72471275 in /nats-streaming-server 
# Fri, 25 Feb 2022 03:02:25 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:02:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 03:02:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:21fca66c0d285fa1440c4688da4adb5a2b07fb2d63f613af9f984b8bbfeab18f`  
		Last Modified: Fri, 25 Feb 2022 03:04:21 GMT  
		Size: 6.6 MB (6577227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.2-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:25f8d00ba1c21fb799a3c4f2cac7e1f828247ebeae544162daa80f83138fee9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9df95b5224c0937c31982baefb4b2eb1f16808dba0e58c13b9afa9a81bf8e71`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 03:03:58 GMT
COPY file:20e40bb6a5f58c9706bc32195e036ddbef77390672e5230781fec0d06314cd48 in /nats-streaming-server 
# Fri, 25 Feb 2022 03:03:58 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:03:59 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 03:04:00 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:cec2c76695402528056a4f2eeb40e25ac44052fb78855dce3f8a746df6656a94`  
		Last Modified: Fri, 25 Feb 2022 03:04:59 GMT  
		Size: 6.5 MB (6495743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.2-nanoserver`

```console
$ docker pull nats-streaming@sha256:8b491322c8ffd9bf3a1601284c03e767da655c349ab692aeac5e48c237c9ec8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats-streaming:0.24.2-nanoserver` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats-streaming@sha256:869d74ad56522c6b9a695cd1db6d5c2d5789b67ac3abc60ef7486db75c5db40d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110269675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5932d54e1864e9f49901b4c39dfe687232bf2b59e8ecfd3242b36ad57e523536`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Feb 2022 02:20:56 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Fri, 25 Feb 2022 02:20:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:20:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 25 Feb 2022 02:21:01 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5030a6d1fb6074f83ecd43d63329d1ce9e47ce7abb822efe4b048525348294`  
		Last Modified: Fri, 25 Feb 2022 02:21:56 GMT  
		Size: 7.2 MB (7177970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68877bcb599a81befa9c6441501d142f7669207fa0787cee6e74f4ae3cb5aad`  
		Last Modified: Fri, 25 Feb 2022 02:21:55 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91344cbf81e04fb8ef879b3a388d8fcaa65d3a70106bd7f96b8954c9564cee32`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab42220f2fa6e2a4c6b6d10260b5cd783c0ba3cfdd4ff423484667ee782017e`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.2-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:8b491322c8ffd9bf3a1601284c03e767da655c349ab692aeac5e48c237c9ec8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats-streaming:0.24.2-nanoserver-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats-streaming@sha256:869d74ad56522c6b9a695cd1db6d5c2d5789b67ac3abc60ef7486db75c5db40d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110269675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5932d54e1864e9f49901b4c39dfe687232bf2b59e8ecfd3242b36ad57e523536`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Feb 2022 02:20:56 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Fri, 25 Feb 2022 02:20:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:20:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 25 Feb 2022 02:21:01 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5030a6d1fb6074f83ecd43d63329d1ce9e47ce7abb822efe4b048525348294`  
		Last Modified: Fri, 25 Feb 2022 02:21:56 GMT  
		Size: 7.2 MB (7177970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68877bcb599a81befa9c6441501d142f7669207fa0787cee6e74f4ae3cb5aad`  
		Last Modified: Fri, 25 Feb 2022 02:21:55 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91344cbf81e04fb8ef879b3a388d8fcaa65d3a70106bd7f96b8954c9564cee32`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab42220f2fa6e2a4c6b6d10260b5cd783c0ba3cfdd4ff423484667ee782017e`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.2-scratch`

```console
$ docker pull nats-streaming@sha256:b21b852fe0586ae78b61cc93bb284833f978bb3769a98f8777181dddbfe6783b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24.2-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:b0264ae003ad4b65e28ecd00f38f5bbdf7a937471c26111d88b6990ecc49bdbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7071520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc31f3812f5256ec02071ca3e295a5be59a2d326417a7b55569235b47a7a2fc9`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 02:19:54 GMT
COPY file:47ac28785512ec4ac0869ce12d480005915c64c985d55605a5d2ed5a852389fb in /nats-streaming-server 
# Fri, 25 Feb 2022 02:19:54 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:19:55 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 02:19:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6726d9237da5dd8f18cb24ee666179433f7a040706b881549b18eaccdb2b7b0c`  
		Last Modified: Fri, 25 Feb 2022 02:20:36 GMT  
		Size: 7.1 MB (7071520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.2-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:3d85afadae9925ec2a82250ddd268054b9844d01605ed3cf9d2b0a17cce21dfa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6587572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51f2eea369c9614b4ab5aeaa4dcd4ed04a754251557bdccdb339712935c2f63`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 02:53:52 GMT
COPY file:558cfcd3a5b3207402c443e2aac4e1a401ccbf8ee0c6f1b92251ef816558b646 in /nats-streaming-server 
# Fri, 25 Feb 2022 02:53:52 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:53:53 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 02:53:53 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a2f9d3181316d01f63a8016443dca42572e115447efd51051bc10f47d69fda7f`  
		Last Modified: Fri, 25 Feb 2022 02:55:46 GMT  
		Size: 6.6 MB (6587572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.2-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:91fe5ea5ea66dbce33f105342aa2c257de6efebcf2c84c517c76e43887994ba1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6577227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ae60167dced131f5b275c9a42d53766267caad88d5f2e8429543860190fa1f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 03:02:25 GMT
COPY file:81da864fb3ebeee9861cc8b3daa8a3454787d8decad14ec3d175e6bd72471275 in /nats-streaming-server 
# Fri, 25 Feb 2022 03:02:25 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:02:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 03:02:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:21fca66c0d285fa1440c4688da4adb5a2b07fb2d63f613af9f984b8bbfeab18f`  
		Last Modified: Fri, 25 Feb 2022 03:04:21 GMT  
		Size: 6.6 MB (6577227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:25f8d00ba1c21fb799a3c4f2cac7e1f828247ebeae544162daa80f83138fee9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9df95b5224c0937c31982baefb4b2eb1f16808dba0e58c13b9afa9a81bf8e71`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 03:03:58 GMT
COPY file:20e40bb6a5f58c9706bc32195e036ddbef77390672e5230781fec0d06314cd48 in /nats-streaming-server 
# Fri, 25 Feb 2022 03:03:58 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:03:59 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 03:04:00 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:cec2c76695402528056a4f2eeb40e25ac44052fb78855dce3f8a746df6656a94`  
		Last Modified: Fri, 25 Feb 2022 03:04:59 GMT  
		Size: 6.5 MB (6495743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.2-windowsservercore`

```console
$ docker pull nats-streaming@sha256:819b001ad6d44c72b199d7aac599345d3f20d8ee74b4a472a90acea9c399184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats-streaming:0.24.2-windowsservercore` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats-streaming@sha256:db604481a007d58765b7c40c26c49745cf093d4e49837b5bf0e93a4669f00911
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2721626080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e006b586ed1498bdbe651518f76ddeb751bc50fa16c0ec6680dc7e2947f3fb29`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 15:04:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Feb 2022 18:10:54 GMT
ENV NATS_DOCKERIZED=1
# Fri, 25 Feb 2022 02:17:55 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:17:55 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.2/nats-streaming-server-v0.24.2-windows-amd64.zip
# Fri, 25 Feb 2022 02:17:56 GMT
ENV NATS_STREAMING_SERVER_SHASUM=15a7692d56bc3b2d6fb84b89d631205a927a807d3c901e6929dfcb82445149d2
# Fri, 25 Feb 2022 02:18:56 GMT
RUN Set-PSDebug -Trace 2
# Fri, 25 Feb 2022 02:20:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 25 Feb 2022 02:20:45 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:20:45 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 25 Feb 2022 02:20:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f49d3791198cf2ea875fd54ce3bb715670742d4a58c00252395ad1b74036662a`  
		Last Modified: Wed, 09 Feb 2022 16:39:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4235aeeb4e8b577cc7aa26c7994ec94c94dd53a38764fc510b330b77cef4abad`  
		Last Modified: Wed, 09 Feb 2022 18:14:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c6d42960df831ce1448963636541141a4ec9089d489c5ee11b5e310cdbbbf`  
		Last Modified: Fri, 25 Feb 2022 02:21:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e40b6a7fa5407b7bc18d72dd18e47e4f538a618fe7aee3f63df8657eec3c822`  
		Last Modified: Fri, 25 Feb 2022 02:21:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ddf61c72a1d8861fc97f277505fbe4613829e3758bc385f97cdbc77d986fb3`  
		Last Modified: Fri, 25 Feb 2022 02:21:35 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0697e7113057967b17bb9804201e7ad14aba29e62471fd16c36b3c9efaaf2d`  
		Last Modified: Fri, 25 Feb 2022 02:21:33 GMT  
		Size: 374.2 KB (374241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6d53518d92b0f4b70d8d36384f340ec236cbac76d67c8ef7574480961946c1`  
		Last Modified: Fri, 25 Feb 2022 02:21:40 GMT  
		Size: 7.5 MB (7526089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d576464a46e0c69764bf23a274474e67f4f10707edf6e9879a6a6c07f7eeb22`  
		Last Modified: Fri, 25 Feb 2022 02:21:32 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c59dbff87a88dbf092b9fff74f90edd33ace3d56fd401555cdd81a28e22f2e1`  
		Last Modified: Fri, 25 Feb 2022 02:21:32 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6267c71e5c55502f4d5c4662d71f5393dcd6013bb813937fd072667ec810143`  
		Last Modified: Fri, 25 Feb 2022 02:21:32 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.2-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:819b001ad6d44c72b199d7aac599345d3f20d8ee74b4a472a90acea9c399184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats-streaming:0.24.2-windowsservercore-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats-streaming@sha256:db604481a007d58765b7c40c26c49745cf093d4e49837b5bf0e93a4669f00911
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2721626080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e006b586ed1498bdbe651518f76ddeb751bc50fa16c0ec6680dc7e2947f3fb29`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 15:04:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Feb 2022 18:10:54 GMT
ENV NATS_DOCKERIZED=1
# Fri, 25 Feb 2022 02:17:55 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:17:55 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.2/nats-streaming-server-v0.24.2-windows-amd64.zip
# Fri, 25 Feb 2022 02:17:56 GMT
ENV NATS_STREAMING_SERVER_SHASUM=15a7692d56bc3b2d6fb84b89d631205a927a807d3c901e6929dfcb82445149d2
# Fri, 25 Feb 2022 02:18:56 GMT
RUN Set-PSDebug -Trace 2
# Fri, 25 Feb 2022 02:20:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 25 Feb 2022 02:20:45 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:20:45 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 25 Feb 2022 02:20:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f49d3791198cf2ea875fd54ce3bb715670742d4a58c00252395ad1b74036662a`  
		Last Modified: Wed, 09 Feb 2022 16:39:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4235aeeb4e8b577cc7aa26c7994ec94c94dd53a38764fc510b330b77cef4abad`  
		Last Modified: Wed, 09 Feb 2022 18:14:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c6d42960df831ce1448963636541141a4ec9089d489c5ee11b5e310cdbbbf`  
		Last Modified: Fri, 25 Feb 2022 02:21:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e40b6a7fa5407b7bc18d72dd18e47e4f538a618fe7aee3f63df8657eec3c822`  
		Last Modified: Fri, 25 Feb 2022 02:21:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ddf61c72a1d8861fc97f277505fbe4613829e3758bc385f97cdbc77d986fb3`  
		Last Modified: Fri, 25 Feb 2022 02:21:35 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0697e7113057967b17bb9804201e7ad14aba29e62471fd16c36b3c9efaaf2d`  
		Last Modified: Fri, 25 Feb 2022 02:21:33 GMT  
		Size: 374.2 KB (374241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6d53518d92b0f4b70d8d36384f340ec236cbac76d67c8ef7574480961946c1`  
		Last Modified: Fri, 25 Feb 2022 02:21:40 GMT  
		Size: 7.5 MB (7526089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d576464a46e0c69764bf23a274474e67f4f10707edf6e9879a6a6c07f7eeb22`  
		Last Modified: Fri, 25 Feb 2022 02:21:32 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c59dbff87a88dbf092b9fff74f90edd33ace3d56fd401555cdd81a28e22f2e1`  
		Last Modified: Fri, 25 Feb 2022 02:21:32 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6267c71e5c55502f4d5c4662d71f5393dcd6013bb813937fd072667ec810143`  
		Last Modified: Fri, 25 Feb 2022 02:21:32 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:6c06d99e350dfd64d6f90744011e606d51bde2f02fe0fbfdcaa0a7ee8105ad52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:e0b5c46db65c6031b96850c7750125ae972bacaf7acd500a342529587f78cdb6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10163584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73fdc06ff9592dbaa07f7638b8ec5b77e29f0f50e5810e01addc1712d27b926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:19:43 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:19:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 02:19:46 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 02:19:46 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:19:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:19:46 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6d6be22662448ec27471291d386c2cf9e303b0c18135d61435ecab66e3d190`  
		Last Modified: Fri, 25 Feb 2022 02:20:17 GMT  
		Size: 7.3 MB (7344748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ef5642b30ec627703bbd9831a4eb2b34fbc32ce3af4c52751b3c13b05fa1f3`  
		Last Modified: Fri, 25 Feb 2022 02:20:16 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:16bfad93443d1e11ea456827a60788ffaaf287abd7a898abd66df24ce1973675
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9492160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7228f54cd28bbac00b2fd561e721cece5b97bdd93a8582be95db0a18ef521e3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:53:26 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 02:53:31 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 02:53:32 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:53:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:53:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162bf98370c73025244b6844c0fb4795edd0cf2437d3ccedad11cf1e27309826`  
		Last Modified: Fri, 25 Feb 2022 02:55:14 GMT  
		Size: 6.9 MB (6860315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64992fd6ef19b0475e618937bb5276e19cb2e256048d14fefcd9ceea4334d758`  
		Last Modified: Fri, 25 Feb 2022 02:55:10 GMT  
		Size: 424.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:353aec3dccf8ecf1b39edab2415d3ea3c9281434ddf10db8c7a1f36df0be9f7f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9285283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54087071c470d19a57112b054034098a0e6a491034a31578b6034a497fa0171`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:01:55 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 03:01:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 03:02:00 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 03:02:00 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:02:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:02:01 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fa952029dc8a0c57ab16e41b9b4d9f7302794c501d3c481e6576062a23683e`  
		Last Modified: Fri, 25 Feb 2022 03:03:50 GMT  
		Size: 6.9 MB (6850097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360fe50d6904c4c5e840ab926f40c58df2a2e6b905c7493ae065c23b443f4188`  
		Last Modified: Fri, 25 Feb 2022 03:03:45 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:2ee72ee2576a5cbbcc8b3cfb713c4f90292c80ec08ec0a3b156d8cd93c43de42
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9484460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b04cc618c6bdfcbe7e945393204707f2b00244897ddafba37db190dbdac9854`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:03:39 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 03:03:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 03:03:45 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 03:03:45 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:03:47 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c940513d538449d692b24e2bad765ddf948bdac501988eb123df158ee291d31`  
		Last Modified: Fri, 25 Feb 2022 03:04:36 GMT  
		Size: 6.8 MB (6768603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6d2d9b3fc25f46965b7cf1f1633f11e7f4a2fd071e9b86c544f74b4279599b`  
		Last Modified: Fri, 25 Feb 2022 03:04:35 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.15`

```console
$ docker pull nats-streaming@sha256:6c06d99e350dfd64d6f90744011e606d51bde2f02fe0fbfdcaa0a7ee8105ad52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.15` - linux; amd64

```console
$ docker pull nats-streaming@sha256:e0b5c46db65c6031b96850c7750125ae972bacaf7acd500a342529587f78cdb6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10163584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73fdc06ff9592dbaa07f7638b8ec5b77e29f0f50e5810e01addc1712d27b926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:19:43 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:19:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 02:19:46 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 02:19:46 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:19:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:19:46 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6d6be22662448ec27471291d386c2cf9e303b0c18135d61435ecab66e3d190`  
		Last Modified: Fri, 25 Feb 2022 02:20:17 GMT  
		Size: 7.3 MB (7344748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ef5642b30ec627703bbd9831a4eb2b34fbc32ce3af4c52751b3c13b05fa1f3`  
		Last Modified: Fri, 25 Feb 2022 02:20:16 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.15` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:16bfad93443d1e11ea456827a60788ffaaf287abd7a898abd66df24ce1973675
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9492160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7228f54cd28bbac00b2fd561e721cece5b97bdd93a8582be95db0a18ef521e3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:53:26 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 02:53:31 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 02:53:32 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:53:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:53:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162bf98370c73025244b6844c0fb4795edd0cf2437d3ccedad11cf1e27309826`  
		Last Modified: Fri, 25 Feb 2022 02:55:14 GMT  
		Size: 6.9 MB (6860315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64992fd6ef19b0475e618937bb5276e19cb2e256048d14fefcd9ceea4334d758`  
		Last Modified: Fri, 25 Feb 2022 02:55:10 GMT  
		Size: 424.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.15` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:353aec3dccf8ecf1b39edab2415d3ea3c9281434ddf10db8c7a1f36df0be9f7f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9285283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54087071c470d19a57112b054034098a0e6a491034a31578b6034a497fa0171`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:01:55 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 03:01:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 03:02:00 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 03:02:00 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:02:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:02:01 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fa952029dc8a0c57ab16e41b9b4d9f7302794c501d3c481e6576062a23683e`  
		Last Modified: Fri, 25 Feb 2022 03:03:50 GMT  
		Size: 6.9 MB (6850097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360fe50d6904c4c5e840ab926f40c58df2a2e6b905c7493ae065c23b443f4188`  
		Last Modified: Fri, 25 Feb 2022 03:03:45 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:2ee72ee2576a5cbbcc8b3cfb713c4f90292c80ec08ec0a3b156d8cd93c43de42
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9484460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b04cc618c6bdfcbe7e945393204707f2b00244897ddafba37db190dbdac9854`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:03:39 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 03:03:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 03:03:45 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 03:03:45 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:03:47 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c940513d538449d692b24e2bad765ddf948bdac501988eb123df158ee291d31`  
		Last Modified: Fri, 25 Feb 2022 03:04:36 GMT  
		Size: 6.8 MB (6768603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6d2d9b3fc25f46965b7cf1f1633f11e7f4a2fd071e9b86c544f74b4279599b`  
		Last Modified: Fri, 25 Feb 2022 03:04:35 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:6da3b6f566aacd181420cab281d4cd4b82b7ac6703dd4a65f2975cde905a8298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2565; amd64

### `nats-streaming:latest` - linux; amd64

```console
$ docker pull nats-streaming@sha256:b0264ae003ad4b65e28ecd00f38f5bbdf7a937471c26111d88b6990ecc49bdbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7071520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc31f3812f5256ec02071ca3e295a5be59a2d326417a7b55569235b47a7a2fc9`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 02:19:54 GMT
COPY file:47ac28785512ec4ac0869ce12d480005915c64c985d55605a5d2ed5a852389fb in /nats-streaming-server 
# Fri, 25 Feb 2022 02:19:54 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:19:55 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 02:19:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6726d9237da5dd8f18cb24ee666179433f7a040706b881549b18eaccdb2b7b0c`  
		Last Modified: Fri, 25 Feb 2022 02:20:36 GMT  
		Size: 7.1 MB (7071520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:3d85afadae9925ec2a82250ddd268054b9844d01605ed3cf9d2b0a17cce21dfa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6587572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51f2eea369c9614b4ab5aeaa4dcd4ed04a754251557bdccdb339712935c2f63`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 02:53:52 GMT
COPY file:558cfcd3a5b3207402c443e2aac4e1a401ccbf8ee0c6f1b92251ef816558b646 in /nats-streaming-server 
# Fri, 25 Feb 2022 02:53:52 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:53:53 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 02:53:53 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a2f9d3181316d01f63a8016443dca42572e115447efd51051bc10f47d69fda7f`  
		Last Modified: Fri, 25 Feb 2022 02:55:46 GMT  
		Size: 6.6 MB (6587572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:91fe5ea5ea66dbce33f105342aa2c257de6efebcf2c84c517c76e43887994ba1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6577227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ae60167dced131f5b275c9a42d53766267caad88d5f2e8429543860190fa1f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 03:02:25 GMT
COPY file:81da864fb3ebeee9861cc8b3daa8a3454787d8decad14ec3d175e6bd72471275 in /nats-streaming-server 
# Fri, 25 Feb 2022 03:02:25 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:02:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 03:02:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:21fca66c0d285fa1440c4688da4adb5a2b07fb2d63f613af9f984b8bbfeab18f`  
		Last Modified: Fri, 25 Feb 2022 03:04:21 GMT  
		Size: 6.6 MB (6577227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:25f8d00ba1c21fb799a3c4f2cac7e1f828247ebeae544162daa80f83138fee9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9df95b5224c0937c31982baefb4b2eb1f16808dba0e58c13b9afa9a81bf8e71`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 03:03:58 GMT
COPY file:20e40bb6a5f58c9706bc32195e036ddbef77390672e5230781fec0d06314cd48 in /nats-streaming-server 
# Fri, 25 Feb 2022 03:03:58 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:03:59 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 03:04:00 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:cec2c76695402528056a4f2eeb40e25ac44052fb78855dce3f8a746df6656a94`  
		Last Modified: Fri, 25 Feb 2022 03:04:59 GMT  
		Size: 6.5 MB (6495743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats-streaming@sha256:869d74ad56522c6b9a695cd1db6d5c2d5789b67ac3abc60ef7486db75c5db40d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110269675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5932d54e1864e9f49901b4c39dfe687232bf2b59e8ecfd3242b36ad57e523536`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Feb 2022 02:20:56 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Fri, 25 Feb 2022 02:20:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:20:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 25 Feb 2022 02:21:01 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5030a6d1fb6074f83ecd43d63329d1ce9e47ce7abb822efe4b048525348294`  
		Last Modified: Fri, 25 Feb 2022 02:21:56 GMT  
		Size: 7.2 MB (7177970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68877bcb599a81befa9c6441501d142f7669207fa0787cee6e74f4ae3cb5aad`  
		Last Modified: Fri, 25 Feb 2022 02:21:55 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91344cbf81e04fb8ef879b3a388d8fcaa65d3a70106bd7f96b8954c9564cee32`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab42220f2fa6e2a4c6b6d10260b5cd783c0ba3cfdd4ff423484667ee782017e`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:b21b852fe0586ae78b61cc93bb284833f978bb3769a98f8777181dddbfe6783b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:b0264ae003ad4b65e28ecd00f38f5bbdf7a937471c26111d88b6990ecc49bdbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7071520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc31f3812f5256ec02071ca3e295a5be59a2d326417a7b55569235b47a7a2fc9`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 02:19:54 GMT
COPY file:47ac28785512ec4ac0869ce12d480005915c64c985d55605a5d2ed5a852389fb in /nats-streaming-server 
# Fri, 25 Feb 2022 02:19:54 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:19:55 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 02:19:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6726d9237da5dd8f18cb24ee666179433f7a040706b881549b18eaccdb2b7b0c`  
		Last Modified: Fri, 25 Feb 2022 02:20:36 GMT  
		Size: 7.1 MB (7071520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:3d85afadae9925ec2a82250ddd268054b9844d01605ed3cf9d2b0a17cce21dfa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6587572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51f2eea369c9614b4ab5aeaa4dcd4ed04a754251557bdccdb339712935c2f63`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 02:53:52 GMT
COPY file:558cfcd3a5b3207402c443e2aac4e1a401ccbf8ee0c6f1b92251ef816558b646 in /nats-streaming-server 
# Fri, 25 Feb 2022 02:53:52 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:53:53 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 02:53:53 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a2f9d3181316d01f63a8016443dca42572e115447efd51051bc10f47d69fda7f`  
		Last Modified: Fri, 25 Feb 2022 02:55:46 GMT  
		Size: 6.6 MB (6587572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:91fe5ea5ea66dbce33f105342aa2c257de6efebcf2c84c517c76e43887994ba1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6577227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ae60167dced131f5b275c9a42d53766267caad88d5f2e8429543860190fa1f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 03:02:25 GMT
COPY file:81da864fb3ebeee9861cc8b3daa8a3454787d8decad14ec3d175e6bd72471275 in /nats-streaming-server 
# Fri, 25 Feb 2022 03:02:25 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:02:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 03:02:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:21fca66c0d285fa1440c4688da4adb5a2b07fb2d63f613af9f984b8bbfeab18f`  
		Last Modified: Fri, 25 Feb 2022 03:04:21 GMT  
		Size: 6.6 MB (6577227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:25f8d00ba1c21fb799a3c4f2cac7e1f828247ebeae544162daa80f83138fee9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9df95b5224c0937c31982baefb4b2eb1f16808dba0e58c13b9afa9a81bf8e71`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 03:03:58 GMT
COPY file:20e40bb6a5f58c9706bc32195e036ddbef77390672e5230781fec0d06314cd48 in /nats-streaming-server 
# Fri, 25 Feb 2022 03:03:58 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:03:59 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 03:04:00 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:cec2c76695402528056a4f2eeb40e25ac44052fb78855dce3f8a746df6656a94`  
		Last Modified: Fri, 25 Feb 2022 03:04:59 GMT  
		Size: 6.5 MB (6495743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:8b491322c8ffd9bf3a1601284c03e767da655c349ab692aeac5e48c237c9ec8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats-streaming@sha256:869d74ad56522c6b9a695cd1db6d5c2d5789b67ac3abc60ef7486db75c5db40d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110269675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5932d54e1864e9f49901b4c39dfe687232bf2b59e8ecfd3242b36ad57e523536`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Feb 2022 02:20:56 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Fri, 25 Feb 2022 02:20:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:20:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 25 Feb 2022 02:21:01 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5030a6d1fb6074f83ecd43d63329d1ce9e47ce7abb822efe4b048525348294`  
		Last Modified: Fri, 25 Feb 2022 02:21:56 GMT  
		Size: 7.2 MB (7177970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68877bcb599a81befa9c6441501d142f7669207fa0787cee6e74f4ae3cb5aad`  
		Last Modified: Fri, 25 Feb 2022 02:21:55 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91344cbf81e04fb8ef879b3a388d8fcaa65d3a70106bd7f96b8954c9564cee32`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab42220f2fa6e2a4c6b6d10260b5cd783c0ba3cfdd4ff423484667ee782017e`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:8b491322c8ffd9bf3a1601284c03e767da655c349ab692aeac5e48c237c9ec8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats-streaming@sha256:869d74ad56522c6b9a695cd1db6d5c2d5789b67ac3abc60ef7486db75c5db40d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110269675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5932d54e1864e9f49901b4c39dfe687232bf2b59e8ecfd3242b36ad57e523536`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Feb 2022 02:20:56 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Fri, 25 Feb 2022 02:20:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:20:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 25 Feb 2022 02:21:01 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5030a6d1fb6074f83ecd43d63329d1ce9e47ce7abb822efe4b048525348294`  
		Last Modified: Fri, 25 Feb 2022 02:21:56 GMT  
		Size: 7.2 MB (7177970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68877bcb599a81befa9c6441501d142f7669207fa0787cee6e74f4ae3cb5aad`  
		Last Modified: Fri, 25 Feb 2022 02:21:55 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91344cbf81e04fb8ef879b3a388d8fcaa65d3a70106bd7f96b8954c9564cee32`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab42220f2fa6e2a4c6b6d10260b5cd783c0ba3cfdd4ff423484667ee782017e`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:b21b852fe0586ae78b61cc93bb284833f978bb3769a98f8777181dddbfe6783b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:b0264ae003ad4b65e28ecd00f38f5bbdf7a937471c26111d88b6990ecc49bdbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7071520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc31f3812f5256ec02071ca3e295a5be59a2d326417a7b55569235b47a7a2fc9`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 02:19:54 GMT
COPY file:47ac28785512ec4ac0869ce12d480005915c64c985d55605a5d2ed5a852389fb in /nats-streaming-server 
# Fri, 25 Feb 2022 02:19:54 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:19:55 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 02:19:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6726d9237da5dd8f18cb24ee666179433f7a040706b881549b18eaccdb2b7b0c`  
		Last Modified: Fri, 25 Feb 2022 02:20:36 GMT  
		Size: 7.1 MB (7071520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:3d85afadae9925ec2a82250ddd268054b9844d01605ed3cf9d2b0a17cce21dfa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6587572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51f2eea369c9614b4ab5aeaa4dcd4ed04a754251557bdccdb339712935c2f63`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 02:53:52 GMT
COPY file:558cfcd3a5b3207402c443e2aac4e1a401ccbf8ee0c6f1b92251ef816558b646 in /nats-streaming-server 
# Fri, 25 Feb 2022 02:53:52 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:53:53 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 02:53:53 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a2f9d3181316d01f63a8016443dca42572e115447efd51051bc10f47d69fda7f`  
		Last Modified: Fri, 25 Feb 2022 02:55:46 GMT  
		Size: 6.6 MB (6587572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:91fe5ea5ea66dbce33f105342aa2c257de6efebcf2c84c517c76e43887994ba1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6577227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ae60167dced131f5b275c9a42d53766267caad88d5f2e8429543860190fa1f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 03:02:25 GMT
COPY file:81da864fb3ebeee9861cc8b3daa8a3454787d8decad14ec3d175e6bd72471275 in /nats-streaming-server 
# Fri, 25 Feb 2022 03:02:25 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:02:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 03:02:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:21fca66c0d285fa1440c4688da4adb5a2b07fb2d63f613af9f984b8bbfeab18f`  
		Last Modified: Fri, 25 Feb 2022 03:04:21 GMT  
		Size: 6.6 MB (6577227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:25f8d00ba1c21fb799a3c4f2cac7e1f828247ebeae544162daa80f83138fee9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9df95b5224c0937c31982baefb4b2eb1f16808dba0e58c13b9afa9a81bf8e71`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 25 Feb 2022 03:03:58 GMT
COPY file:20e40bb6a5f58c9706bc32195e036ddbef77390672e5230781fec0d06314cd48 in /nats-streaming-server 
# Fri, 25 Feb 2022 03:03:58 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:03:59 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 25 Feb 2022 03:04:00 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:cec2c76695402528056a4f2eeb40e25ac44052fb78855dce3f8a746df6656a94`  
		Last Modified: Fri, 25 Feb 2022 03:04:59 GMT  
		Size: 6.5 MB (6495743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:819b001ad6d44c72b199d7aac599345d3f20d8ee74b4a472a90acea9c399184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats-streaming@sha256:db604481a007d58765b7c40c26c49745cf093d4e49837b5bf0e93a4669f00911
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2721626080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e006b586ed1498bdbe651518f76ddeb751bc50fa16c0ec6680dc7e2947f3fb29`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 15:04:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Feb 2022 18:10:54 GMT
ENV NATS_DOCKERIZED=1
# Fri, 25 Feb 2022 02:17:55 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:17:55 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.2/nats-streaming-server-v0.24.2-windows-amd64.zip
# Fri, 25 Feb 2022 02:17:56 GMT
ENV NATS_STREAMING_SERVER_SHASUM=15a7692d56bc3b2d6fb84b89d631205a927a807d3c901e6929dfcb82445149d2
# Fri, 25 Feb 2022 02:18:56 GMT
RUN Set-PSDebug -Trace 2
# Fri, 25 Feb 2022 02:20:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 25 Feb 2022 02:20:45 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:20:45 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 25 Feb 2022 02:20:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f49d3791198cf2ea875fd54ce3bb715670742d4a58c00252395ad1b74036662a`  
		Last Modified: Wed, 09 Feb 2022 16:39:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4235aeeb4e8b577cc7aa26c7994ec94c94dd53a38764fc510b330b77cef4abad`  
		Last Modified: Wed, 09 Feb 2022 18:14:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c6d42960df831ce1448963636541141a4ec9089d489c5ee11b5e310cdbbbf`  
		Last Modified: Fri, 25 Feb 2022 02:21:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e40b6a7fa5407b7bc18d72dd18e47e4f538a618fe7aee3f63df8657eec3c822`  
		Last Modified: Fri, 25 Feb 2022 02:21:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ddf61c72a1d8861fc97f277505fbe4613829e3758bc385f97cdbc77d986fb3`  
		Last Modified: Fri, 25 Feb 2022 02:21:35 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0697e7113057967b17bb9804201e7ad14aba29e62471fd16c36b3c9efaaf2d`  
		Last Modified: Fri, 25 Feb 2022 02:21:33 GMT  
		Size: 374.2 KB (374241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6d53518d92b0f4b70d8d36384f340ec236cbac76d67c8ef7574480961946c1`  
		Last Modified: Fri, 25 Feb 2022 02:21:40 GMT  
		Size: 7.5 MB (7526089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d576464a46e0c69764bf23a274474e67f4f10707edf6e9879a6a6c07f7eeb22`  
		Last Modified: Fri, 25 Feb 2022 02:21:32 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c59dbff87a88dbf092b9fff74f90edd33ace3d56fd401555cdd81a28e22f2e1`  
		Last Modified: Fri, 25 Feb 2022 02:21:32 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6267c71e5c55502f4d5c4662d71f5393dcd6013bb813937fd072667ec810143`  
		Last Modified: Fri, 25 Feb 2022 02:21:32 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:819b001ad6d44c72b199d7aac599345d3f20d8ee74b4a472a90acea9c399184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats-streaming@sha256:db604481a007d58765b7c40c26c49745cf093d4e49837b5bf0e93a4669f00911
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2721626080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e006b586ed1498bdbe651518f76ddeb751bc50fa16c0ec6680dc7e2947f3fb29`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 15:04:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Feb 2022 18:10:54 GMT
ENV NATS_DOCKERIZED=1
# Fri, 25 Feb 2022 02:17:55 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:17:55 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.2/nats-streaming-server-v0.24.2-windows-amd64.zip
# Fri, 25 Feb 2022 02:17:56 GMT
ENV NATS_STREAMING_SERVER_SHASUM=15a7692d56bc3b2d6fb84b89d631205a927a807d3c901e6929dfcb82445149d2
# Fri, 25 Feb 2022 02:18:56 GMT
RUN Set-PSDebug -Trace 2
# Fri, 25 Feb 2022 02:20:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 25 Feb 2022 02:20:45 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:20:45 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 25 Feb 2022 02:20:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f49d3791198cf2ea875fd54ce3bb715670742d4a58c00252395ad1b74036662a`  
		Last Modified: Wed, 09 Feb 2022 16:39:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4235aeeb4e8b577cc7aa26c7994ec94c94dd53a38764fc510b330b77cef4abad`  
		Last Modified: Wed, 09 Feb 2022 18:14:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c6d42960df831ce1448963636541141a4ec9089d489c5ee11b5e310cdbbbf`  
		Last Modified: Fri, 25 Feb 2022 02:21:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e40b6a7fa5407b7bc18d72dd18e47e4f538a618fe7aee3f63df8657eec3c822`  
		Last Modified: Fri, 25 Feb 2022 02:21:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ddf61c72a1d8861fc97f277505fbe4613829e3758bc385f97cdbc77d986fb3`  
		Last Modified: Fri, 25 Feb 2022 02:21:35 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0697e7113057967b17bb9804201e7ad14aba29e62471fd16c36b3c9efaaf2d`  
		Last Modified: Fri, 25 Feb 2022 02:21:33 GMT  
		Size: 374.2 KB (374241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6d53518d92b0f4b70d8d36384f340ec236cbac76d67c8ef7574480961946c1`  
		Last Modified: Fri, 25 Feb 2022 02:21:40 GMT  
		Size: 7.5 MB (7526089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d576464a46e0c69764bf23a274474e67f4f10707edf6e9879a6a6c07f7eeb22`  
		Last Modified: Fri, 25 Feb 2022 02:21:32 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c59dbff87a88dbf092b9fff74f90edd33ace3d56fd401555cdd81a28e22f2e1`  
		Last Modified: Fri, 25 Feb 2022 02:21:32 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6267c71e5c55502f4d5c4662d71f5393dcd6013bb813937fd072667ec810143`  
		Last Modified: Fri, 25 Feb 2022 02:21:32 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

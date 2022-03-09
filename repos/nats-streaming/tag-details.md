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
$ docker pull nats-streaming@sha256:04056f9afa2e74fda79032633aa78ecc4c67ef20e51db9e993ba02fb3ecc366d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2686; amd64

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

### `nats-streaming:0.24` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:16018303f8883d0b618c73bb51b73367af79afee54399caf17580a4ab8132e7f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110236791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba14e10d46fb18c3615d883ddc1e929197b6d59e5aae5f21c6eb5fe5ab8f968`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 19:07:25 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 19:07:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 19:07:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 19:07:28 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae434cf0b0889cb39a60312866cfbd6bced1f92991045cbfeb9cea4c44bd1509`  
		Last Modified: Wed, 09 Mar 2022 19:08:12 GMT  
		Size: 7.2 MB (7177899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7c446d1df8e0d38d307a4447d7b715fd3907ef0af25e9e5dd9366dd03e8606`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6e9207650a9cec087f8f7a765e3e8169c789ccdd259d105098b89d0e0cf37`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2fda85f9d643a2b20fca975f07a6ef77ebc839369a60e2dc853ee418e1dc1a`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.0 KB (1046 bytes)  
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
$ docker pull nats-streaming@sha256:5fd488e5fff30480c88610d1907786362e8ba0a2e06fc646a4320b5346f7bf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24-nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:16018303f8883d0b618c73bb51b73367af79afee54399caf17580a4ab8132e7f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110236791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba14e10d46fb18c3615d883ddc1e929197b6d59e5aae5f21c6eb5fe5ab8f968`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 19:07:25 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 19:07:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 19:07:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 19:07:28 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae434cf0b0889cb39a60312866cfbd6bced1f92991045cbfeb9cea4c44bd1509`  
		Last Modified: Wed, 09 Mar 2022 19:08:12 GMT  
		Size: 7.2 MB (7177899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7c446d1df8e0d38d307a4447d7b715fd3907ef0af25e9e5dd9366dd03e8606`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6e9207650a9cec087f8f7a765e3e8169c789ccdd259d105098b89d0e0cf37`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2fda85f9d643a2b20fca975f07a6ef77ebc839369a60e2dc853ee418e1dc1a`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:5fd488e5fff30480c88610d1907786362e8ba0a2e06fc646a4320b5346f7bf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:16018303f8883d0b618c73bb51b73367af79afee54399caf17580a4ab8132e7f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110236791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba14e10d46fb18c3615d883ddc1e929197b6d59e5aae5f21c6eb5fe5ab8f968`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 19:07:25 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 19:07:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 19:07:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 19:07:28 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae434cf0b0889cb39a60312866cfbd6bced1f92991045cbfeb9cea4c44bd1509`  
		Last Modified: Wed, 09 Mar 2022 19:08:12 GMT  
		Size: 7.2 MB (7177899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7c446d1df8e0d38d307a4447d7b715fd3907ef0af25e9e5dd9366dd03e8606`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6e9207650a9cec087f8f7a765e3e8169c789ccdd259d105098b89d0e0cf37`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2fda85f9d643a2b20fca975f07a6ef77ebc839369a60e2dc853ee418e1dc1a`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.0 KB (1046 bytes)  
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
$ docker pull nats-streaming@sha256:82835820afcb78483b97c00b341533ec394fc7c1192d3c6569f8c598cc564021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:7749db211dfdc0a6642314c963f1f383bd183e06dbd4fb8b99a6c18f2f499b2b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723316160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a46dcb0db91f6f28d5efc4bd56fc05ab6af16fb8f3deb249be7406096d428a0`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
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
# Wed, 09 Mar 2022 19:04:57 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Wed, 09 Mar 2022 19:04:57 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.2/nats-streaming-server-v0.24.2-windows-amd64.zip
# Wed, 09 Mar 2022 19:04:58 GMT
ENV NATS_STREAMING_SERVER_SHASUM=15a7692d56bc3b2d6fb84b89d631205a927a807d3c901e6929dfcb82445149d2
# Wed, 09 Mar 2022 19:05:48 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 19:07:16 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 19:07:17 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 19:07:18 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 19:07:19 GMT
CMD ["-m" "8222"]
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
	-	`sha256:e8ab5479852eba3e32045f3e492537280a70144a99b7164cf9c9c5aa0e4b9ebd`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e740f62a6d3153c4fdefce1f9838f26428d58afe0b3bb96927b811ffde9c175`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a11dc86b45efaac7b6a421e95bc811dd1a97c29d85974b533e97ffd2a83d9ca`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46607f70f1140bce133530301f4a0692e5236ea9cd6a9b1b7482774db0dc531`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 348.8 KB (348837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ff9f3526a0ffcc275327c7a3f06ea05a5a82b098a7b45a6826f248aca56d4e`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 7.5 MB (7503766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1003616890d106bb7759adc6bf0d8ec488064f6445e4c6779bda5649ce4b308a`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e687485b4f2a17bc24f6d048c162fdb41f9112d5734253caadc9edfd6e234f`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8269fe9a591e7bfacd9bf3405444e155c294d8954f1cca1931c88d23f70260a6`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:82835820afcb78483b97c00b341533ec394fc7c1192d3c6569f8c598cc564021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:7749db211dfdc0a6642314c963f1f383bd183e06dbd4fb8b99a6c18f2f499b2b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723316160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a46dcb0db91f6f28d5efc4bd56fc05ab6af16fb8f3deb249be7406096d428a0`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
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
# Wed, 09 Mar 2022 19:04:57 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Wed, 09 Mar 2022 19:04:57 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.2/nats-streaming-server-v0.24.2-windows-amd64.zip
# Wed, 09 Mar 2022 19:04:58 GMT
ENV NATS_STREAMING_SERVER_SHASUM=15a7692d56bc3b2d6fb84b89d631205a927a807d3c901e6929dfcb82445149d2
# Wed, 09 Mar 2022 19:05:48 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 19:07:16 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 19:07:17 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 19:07:18 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 19:07:19 GMT
CMD ["-m" "8222"]
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
	-	`sha256:e8ab5479852eba3e32045f3e492537280a70144a99b7164cf9c9c5aa0e4b9ebd`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e740f62a6d3153c4fdefce1f9838f26428d58afe0b3bb96927b811ffde9c175`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a11dc86b45efaac7b6a421e95bc811dd1a97c29d85974b533e97ffd2a83d9ca`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46607f70f1140bce133530301f4a0692e5236ea9cd6a9b1b7482774db0dc531`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 348.8 KB (348837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ff9f3526a0ffcc275327c7a3f06ea05a5a82b098a7b45a6826f248aca56d4e`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 7.5 MB (7503766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1003616890d106bb7759adc6bf0d8ec488064f6445e4c6779bda5649ce4b308a`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e687485b4f2a17bc24f6d048c162fdb41f9112d5734253caadc9edfd6e234f`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8269fe9a591e7bfacd9bf3405444e155c294d8954f1cca1931c88d23f70260a6`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.2`

```console
$ docker pull nats-streaming@sha256:04056f9afa2e74fda79032633aa78ecc4c67ef20e51db9e993ba02fb3ecc366d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2686; amd64

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

### `nats-streaming:0.24.2` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:16018303f8883d0b618c73bb51b73367af79afee54399caf17580a4ab8132e7f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110236791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba14e10d46fb18c3615d883ddc1e929197b6d59e5aae5f21c6eb5fe5ab8f968`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 19:07:25 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 19:07:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 19:07:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 19:07:28 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae434cf0b0889cb39a60312866cfbd6bced1f92991045cbfeb9cea4c44bd1509`  
		Last Modified: Wed, 09 Mar 2022 19:08:12 GMT  
		Size: 7.2 MB (7177899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7c446d1df8e0d38d307a4447d7b715fd3907ef0af25e9e5dd9366dd03e8606`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6e9207650a9cec087f8f7a765e3e8169c789ccdd259d105098b89d0e0cf37`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2fda85f9d643a2b20fca975f07a6ef77ebc839369a60e2dc853ee418e1dc1a`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.0 KB (1046 bytes)  
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
$ docker pull nats-streaming@sha256:5fd488e5fff30480c88610d1907786362e8ba0a2e06fc646a4320b5346f7bf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24.2-nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:16018303f8883d0b618c73bb51b73367af79afee54399caf17580a4ab8132e7f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110236791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba14e10d46fb18c3615d883ddc1e929197b6d59e5aae5f21c6eb5fe5ab8f968`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 19:07:25 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 19:07:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 19:07:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 19:07:28 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae434cf0b0889cb39a60312866cfbd6bced1f92991045cbfeb9cea4c44bd1509`  
		Last Modified: Wed, 09 Mar 2022 19:08:12 GMT  
		Size: 7.2 MB (7177899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7c446d1df8e0d38d307a4447d7b715fd3907ef0af25e9e5dd9366dd03e8606`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6e9207650a9cec087f8f7a765e3e8169c789ccdd259d105098b89d0e0cf37`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2fda85f9d643a2b20fca975f07a6ef77ebc839369a60e2dc853ee418e1dc1a`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.2-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:5fd488e5fff30480c88610d1907786362e8ba0a2e06fc646a4320b5346f7bf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24.2-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:16018303f8883d0b618c73bb51b73367af79afee54399caf17580a4ab8132e7f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110236791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba14e10d46fb18c3615d883ddc1e929197b6d59e5aae5f21c6eb5fe5ab8f968`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 19:07:25 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 19:07:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 19:07:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 19:07:28 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae434cf0b0889cb39a60312866cfbd6bced1f92991045cbfeb9cea4c44bd1509`  
		Last Modified: Wed, 09 Mar 2022 19:08:12 GMT  
		Size: 7.2 MB (7177899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7c446d1df8e0d38d307a4447d7b715fd3907ef0af25e9e5dd9366dd03e8606`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6e9207650a9cec087f8f7a765e3e8169c789ccdd259d105098b89d0e0cf37`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2fda85f9d643a2b20fca975f07a6ef77ebc839369a60e2dc853ee418e1dc1a`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.0 KB (1046 bytes)  
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
$ docker pull nats-streaming@sha256:82835820afcb78483b97c00b341533ec394fc7c1192d3c6569f8c598cc564021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24.2-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:7749db211dfdc0a6642314c963f1f383bd183e06dbd4fb8b99a6c18f2f499b2b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723316160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a46dcb0db91f6f28d5efc4bd56fc05ab6af16fb8f3deb249be7406096d428a0`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
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
# Wed, 09 Mar 2022 19:04:57 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Wed, 09 Mar 2022 19:04:57 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.2/nats-streaming-server-v0.24.2-windows-amd64.zip
# Wed, 09 Mar 2022 19:04:58 GMT
ENV NATS_STREAMING_SERVER_SHASUM=15a7692d56bc3b2d6fb84b89d631205a927a807d3c901e6929dfcb82445149d2
# Wed, 09 Mar 2022 19:05:48 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 19:07:16 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 19:07:17 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 19:07:18 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 19:07:19 GMT
CMD ["-m" "8222"]
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
	-	`sha256:e8ab5479852eba3e32045f3e492537280a70144a99b7164cf9c9c5aa0e4b9ebd`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e740f62a6d3153c4fdefce1f9838f26428d58afe0b3bb96927b811ffde9c175`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a11dc86b45efaac7b6a421e95bc811dd1a97c29d85974b533e97ffd2a83d9ca`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46607f70f1140bce133530301f4a0692e5236ea9cd6a9b1b7482774db0dc531`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 348.8 KB (348837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ff9f3526a0ffcc275327c7a3f06ea05a5a82b098a7b45a6826f248aca56d4e`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 7.5 MB (7503766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1003616890d106bb7759adc6bf0d8ec488064f6445e4c6779bda5649ce4b308a`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e687485b4f2a17bc24f6d048c162fdb41f9112d5734253caadc9edfd6e234f`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8269fe9a591e7bfacd9bf3405444e155c294d8954f1cca1931c88d23f70260a6`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.2-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:82835820afcb78483b97c00b341533ec394fc7c1192d3c6569f8c598cc564021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24.2-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:7749db211dfdc0a6642314c963f1f383bd183e06dbd4fb8b99a6c18f2f499b2b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723316160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a46dcb0db91f6f28d5efc4bd56fc05ab6af16fb8f3deb249be7406096d428a0`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
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
# Wed, 09 Mar 2022 19:04:57 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Wed, 09 Mar 2022 19:04:57 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.2/nats-streaming-server-v0.24.2-windows-amd64.zip
# Wed, 09 Mar 2022 19:04:58 GMT
ENV NATS_STREAMING_SERVER_SHASUM=15a7692d56bc3b2d6fb84b89d631205a927a807d3c901e6929dfcb82445149d2
# Wed, 09 Mar 2022 19:05:48 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 19:07:16 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 19:07:17 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 19:07:18 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 19:07:19 GMT
CMD ["-m" "8222"]
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
	-	`sha256:e8ab5479852eba3e32045f3e492537280a70144a99b7164cf9c9c5aa0e4b9ebd`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e740f62a6d3153c4fdefce1f9838f26428d58afe0b3bb96927b811ffde9c175`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a11dc86b45efaac7b6a421e95bc811dd1a97c29d85974b533e97ffd2a83d9ca`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46607f70f1140bce133530301f4a0692e5236ea9cd6a9b1b7482774db0dc531`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 348.8 KB (348837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ff9f3526a0ffcc275327c7a3f06ea05a5a82b098a7b45a6826f248aca56d4e`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 7.5 MB (7503766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1003616890d106bb7759adc6bf0d8ec488064f6445e4c6779bda5649ce4b308a`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e687485b4f2a17bc24f6d048c162fdb41f9112d5734253caadc9edfd6e234f`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8269fe9a591e7bfacd9bf3405444e155c294d8954f1cca1931c88d23f70260a6`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 1.3 KB (1294 bytes)  
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
$ docker pull nats-streaming@sha256:04056f9afa2e74fda79032633aa78ecc4c67ef20e51db9e993ba02fb3ecc366d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2686; amd64

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

### `nats-streaming:latest` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:16018303f8883d0b618c73bb51b73367af79afee54399caf17580a4ab8132e7f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110236791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba14e10d46fb18c3615d883ddc1e929197b6d59e5aae5f21c6eb5fe5ab8f968`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 19:07:25 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 19:07:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 19:07:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 19:07:28 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae434cf0b0889cb39a60312866cfbd6bced1f92991045cbfeb9cea4c44bd1509`  
		Last Modified: Wed, 09 Mar 2022 19:08:12 GMT  
		Size: 7.2 MB (7177899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7c446d1df8e0d38d307a4447d7b715fd3907ef0af25e9e5dd9366dd03e8606`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6e9207650a9cec087f8f7a765e3e8169c789ccdd259d105098b89d0e0cf37`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2fda85f9d643a2b20fca975f07a6ef77ebc839369a60e2dc853ee418e1dc1a`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.0 KB (1046 bytes)  
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
$ docker pull nats-streaming@sha256:5fd488e5fff30480c88610d1907786362e8ba0a2e06fc646a4320b5346f7bf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:16018303f8883d0b618c73bb51b73367af79afee54399caf17580a4ab8132e7f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110236791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba14e10d46fb18c3615d883ddc1e929197b6d59e5aae5f21c6eb5fe5ab8f968`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 19:07:25 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 19:07:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 19:07:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 19:07:28 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae434cf0b0889cb39a60312866cfbd6bced1f92991045cbfeb9cea4c44bd1509`  
		Last Modified: Wed, 09 Mar 2022 19:08:12 GMT  
		Size: 7.2 MB (7177899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7c446d1df8e0d38d307a4447d7b715fd3907ef0af25e9e5dd9366dd03e8606`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6e9207650a9cec087f8f7a765e3e8169c789ccdd259d105098b89d0e0cf37`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2fda85f9d643a2b20fca975f07a6ef77ebc839369a60e2dc853ee418e1dc1a`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:5fd488e5fff30480c88610d1907786362e8ba0a2e06fc646a4320b5346f7bf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:16018303f8883d0b618c73bb51b73367af79afee54399caf17580a4ab8132e7f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110236791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba14e10d46fb18c3615d883ddc1e929197b6d59e5aae5f21c6eb5fe5ab8f968`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 19:07:25 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 19:07:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 19:07:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 19:07:28 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae434cf0b0889cb39a60312866cfbd6bced1f92991045cbfeb9cea4c44bd1509`  
		Last Modified: Wed, 09 Mar 2022 19:08:12 GMT  
		Size: 7.2 MB (7177899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7c446d1df8e0d38d307a4447d7b715fd3907ef0af25e9e5dd9366dd03e8606`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6e9207650a9cec087f8f7a765e3e8169c789ccdd259d105098b89d0e0cf37`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2fda85f9d643a2b20fca975f07a6ef77ebc839369a60e2dc853ee418e1dc1a`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.0 KB (1046 bytes)  
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
$ docker pull nats-streaming@sha256:82835820afcb78483b97c00b341533ec394fc7c1192d3c6569f8c598cc564021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:7749db211dfdc0a6642314c963f1f383bd183e06dbd4fb8b99a6c18f2f499b2b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723316160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a46dcb0db91f6f28d5efc4bd56fc05ab6af16fb8f3deb249be7406096d428a0`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
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
# Wed, 09 Mar 2022 19:04:57 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Wed, 09 Mar 2022 19:04:57 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.2/nats-streaming-server-v0.24.2-windows-amd64.zip
# Wed, 09 Mar 2022 19:04:58 GMT
ENV NATS_STREAMING_SERVER_SHASUM=15a7692d56bc3b2d6fb84b89d631205a927a807d3c901e6929dfcb82445149d2
# Wed, 09 Mar 2022 19:05:48 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 19:07:16 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 19:07:17 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 19:07:18 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 19:07:19 GMT
CMD ["-m" "8222"]
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
	-	`sha256:e8ab5479852eba3e32045f3e492537280a70144a99b7164cf9c9c5aa0e4b9ebd`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e740f62a6d3153c4fdefce1f9838f26428d58afe0b3bb96927b811ffde9c175`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a11dc86b45efaac7b6a421e95bc811dd1a97c29d85974b533e97ffd2a83d9ca`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46607f70f1140bce133530301f4a0692e5236ea9cd6a9b1b7482774db0dc531`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 348.8 KB (348837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ff9f3526a0ffcc275327c7a3f06ea05a5a82b098a7b45a6826f248aca56d4e`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 7.5 MB (7503766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1003616890d106bb7759adc6bf0d8ec488064f6445e4c6779bda5649ce4b308a`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e687485b4f2a17bc24f6d048c162fdb41f9112d5734253caadc9edfd6e234f`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8269fe9a591e7bfacd9bf3405444e155c294d8954f1cca1931c88d23f70260a6`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:82835820afcb78483b97c00b341533ec394fc7c1192d3c6569f8c598cc564021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:7749db211dfdc0a6642314c963f1f383bd183e06dbd4fb8b99a6c18f2f499b2b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723316160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a46dcb0db91f6f28d5efc4bd56fc05ab6af16fb8f3deb249be7406096d428a0`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
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
# Wed, 09 Mar 2022 19:04:57 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Wed, 09 Mar 2022 19:04:57 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.2/nats-streaming-server-v0.24.2-windows-amd64.zip
# Wed, 09 Mar 2022 19:04:58 GMT
ENV NATS_STREAMING_SERVER_SHASUM=15a7692d56bc3b2d6fb84b89d631205a927a807d3c901e6929dfcb82445149d2
# Wed, 09 Mar 2022 19:05:48 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 19:07:16 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 19:07:17 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 19:07:18 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 19:07:19 GMT
CMD ["-m" "8222"]
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
	-	`sha256:e8ab5479852eba3e32045f3e492537280a70144a99b7164cf9c9c5aa0e4b9ebd`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e740f62a6d3153c4fdefce1f9838f26428d58afe0b3bb96927b811ffde9c175`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a11dc86b45efaac7b6a421e95bc811dd1a97c29d85974b533e97ffd2a83d9ca`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46607f70f1140bce133530301f4a0692e5236ea9cd6a9b1b7482774db0dc531`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 348.8 KB (348837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ff9f3526a0ffcc275327c7a3f06ea05a5a82b098a7b45a6826f248aca56d4e`  
		Last Modified: Wed, 09 Mar 2022 19:07:52 GMT  
		Size: 7.5 MB (7503766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1003616890d106bb7759adc6bf0d8ec488064f6445e4c6779bda5649ce4b308a`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e687485b4f2a17bc24f6d048c162fdb41f9112d5734253caadc9edfd6e234f`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8269fe9a591e7bfacd9bf3405444e155c294d8954f1cca1931c88d23f70260a6`  
		Last Modified: Wed, 09 Mar 2022 19:07:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

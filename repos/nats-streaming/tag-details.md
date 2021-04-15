<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats-streaming`

-	[`nats-streaming:0.21`](#nats-streaming021)
-	[`nats-streaming:0.21-alpine`](#nats-streaming021-alpine)
-	[`nats-streaming:0.21-alpine3.13`](#nats-streaming021-alpine313)
-	[`nats-streaming:0.21-linux`](#nats-streaming021-linux)
-	[`nats-streaming:0.21-nanoserver`](#nats-streaming021-nanoserver)
-	[`nats-streaming:0.21-nanoserver-1809`](#nats-streaming021-nanoserver-1809)
-	[`nats-streaming:0.21-scratch`](#nats-streaming021-scratch)
-	[`nats-streaming:0.21-windowsservercore`](#nats-streaming021-windowsservercore)
-	[`nats-streaming:0.21-windowsservercore-1809`](#nats-streaming021-windowsservercore-1809)
-	[`nats-streaming:0.21-windowsservercore-ltsc2016`](#nats-streaming021-windowsservercore-ltsc2016)
-	[`nats-streaming:0.21.1`](#nats-streaming0211)
-	[`nats-streaming:0.21.1-alpine`](#nats-streaming0211-alpine)
-	[`nats-streaming:0.21.1-alpine3.13`](#nats-streaming0211-alpine313)
-	[`nats-streaming:0.21.1-linux`](#nats-streaming0211-linux)
-	[`nats-streaming:0.21.1-nanoserver`](#nats-streaming0211-nanoserver)
-	[`nats-streaming:0.21.1-nanoserver-1809`](#nats-streaming0211-nanoserver-1809)
-	[`nats-streaming:0.21.1-scratch`](#nats-streaming0211-scratch)
-	[`nats-streaming:0.21.1-windowsservercore`](#nats-streaming0211-windowsservercore)
-	[`nats-streaming:0.21.1-windowsservercore-1809`](#nats-streaming0211-windowsservercore-1809)
-	[`nats-streaming:0.21.1-windowsservercore-ltsc2016`](#nats-streaming0211-windowsservercore-ltsc2016)
-	[`nats-streaming:alpine`](#nats-streamingalpine)
-	[`nats-streaming:alpine3.13`](#nats-streamingalpine313)
-	[`nats-streaming:latest`](#nats-streaminglatest)
-	[`nats-streaming:linux`](#nats-streaminglinux)
-	[`nats-streaming:nanoserver`](#nats-streamingnanoserver)
-	[`nats-streaming:nanoserver-1809`](#nats-streamingnanoserver-1809)
-	[`nats-streaming:scratch`](#nats-streamingscratch)
-	[`nats-streaming:windowsservercore`](#nats-streamingwindowsservercore)
-	[`nats-streaming:windowsservercore-1809`](#nats-streamingwindowsservercore-1809)
-	[`nats-streaming:windowsservercore-ltsc2016`](#nats-streamingwindowsservercore-ltsc2016)

## `nats-streaming:0.21`

```console
$ docker pull nats-streaming@sha256:4fc8a5fbef2b822d6456b521cd88bcc6db2c7a0df7a4e983c148018998ce2347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:0.21` - linux; amd64

```console
$ docker pull nats-streaming@sha256:aa6af76760541ce71d366ac25554ad7caa95aea8cd230dd2688fd76b0645b329
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31671965fc8e3e2d623279516e43fd9d1a5d8d82a19fe709c69d7bfe7ac50085`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 07:43:28 GMT
COPY file:2c21a07cd43acfd157f86c6cf727430cf07e201a3bf3668b2083f473385db991 in /nats-streaming-server 
# Sat, 06 Mar 2021 07:43:28 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 07:43:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 07:43:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6f1c3ed40f752c2108b0e5d9224fba83d5045dac3370f93a50d91af0bc201c05`  
		Last Modified: Sat, 06 Mar 2021 07:44:17 GMT  
		Size: 5.7 MB (5680474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:907a450228b0d46339c5af803a9475165f7cfd9d20d5e09e8f66f9d048d1f7b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c6d73cc983f6821e57de28a32cec901f28d3c5ada68aa9e71a1880962a9f07`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 02:10:29 GMT
COPY file:bd617234b457ddee67b99f0e411029c6d5badad5059fbd81239c0acfe92cd4b7 in /nats-streaming-server 
# Sat, 06 Mar 2021 02:10:30 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 02:10:31 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 02:10:31 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ef1f32aa7a9ce9c8d42c909d32f61dabfa957c0b6a2b3590cd5e5847fb634355`  
		Last Modified: Sat, 06 Mar 2021 02:11:15 GMT  
		Size: 5.3 MB (5252895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ae774aee41bd64306207d739d2290639f673c9c66c367a83f155a923fe8c13f6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce52186dd957f6b70b086fdcbc8212e079e5ed5e3e0013f8f72b3922535a56e`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 01:00:25 GMT
COPY file:546c18b3e8e91d453d1a325c6e4dbc3c945564c010676da1abe89a653a0dea84 in /nats-streaming-server 
# Sat, 06 Mar 2021 01:00:27 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:00:28 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 01:00:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ed8ed2aa5d978cf51ebe3454de1832aeb40919052c5cb17d5b63865c31fc03c7`  
		Last Modified: Sat, 06 Mar 2021 01:01:07 GMT  
		Size: 5.2 MB (5246286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:7fccb492771f9c26f12f03c49e84ba4fb4d7004c6d142f4a7b83337d92feda95
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e817dd7b95371ae514afe3154e4aeba302d94dbed618a0aba7ece8696c13c6`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 01:51:04 GMT
COPY file:ed938be8d92952afe74223a94317bf582d9bcf2c458a54733da01a37a65d421b in /nats-streaming-server 
# Sat, 06 Mar 2021 01:51:05 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:51:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 01:51:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f5ab53e298c8bd7b93e991f4b12e4015cde7d604e6d5ee086e994a86e0556094`  
		Last Modified: Sat, 06 Mar 2021 01:51:46 GMT  
		Size: 5.2 MB (5170586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:54818a8a35d4a6a4e9efd14ee26c405e9aff90c33b6d5ddd815ff4b4410dad8b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107155482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be925e76dc6a703aa26d065b798d75738366f16d758e6d881239034e4ebc3ac`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:30:32 GMT
RUN cmd /S /C #(nop) COPY file:189ca6af047e9f9cf54ab2176b48588e01c7497fe0b5b0d7b2614ebad66ed089 in C:\nats-streaming-server.exe 
# Wed, 14 Apr 2021 20:30:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:30:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:30:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8f5e1772f13f9dbd7806652f582319d4c94b5e221ddca9bdd7a9a08472b446`  
		Last Modified: Wed, 14 Apr 2021 20:35:48 GMT  
		Size: 5.8 MB (5810702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45528fb53c9d98e2841a65b4761f5e3e524204d43fa18f0f4e5bf517a6fd003`  
		Last Modified: Wed, 14 Apr 2021 20:35:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2de582a0cd8ce6292e31cfe6870e1766cf4ce33b53febbf987b8210419f90d0`  
		Last Modified: Wed, 14 Apr 2021 20:35:48 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a29154792d4c050924f398e1e63281f55a67fd9d0393fb45d94b0613d10302e`  
		Last Modified: Wed, 14 Apr 2021 20:35:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-alpine`

```console
$ docker pull nats-streaming@sha256:ed61be1c1e81fe7ff551c6520026d982ce60a6ad7e8c0007bf9259f623d434c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:72675b6fd1c18a33e5996e738dbca972714f365d257cd8adb172bca6aba6f0dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8775096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f64537c882c84c11c410a0f7e043a29ef4ff08cdaf4d45c7ff76bac1286bd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:09:41 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:09:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 14 Apr 2021 20:09:44 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Apr 2021 20:09:44 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:09:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 20:09:45 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c75bced29aa1bd74c9fff0d702a93a39840b2b4ed08bf2a036a2f1fb4673e14`  
		Last Modified: Wed, 14 Apr 2021 20:10:15 GMT  
		Size: 6.0 MB (5962706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd5e8ff68dafef8eeaffa582db26e788df6089e19711a01b79aae50d4dfe9f8`  
		Last Modified: Wed, 14 Apr 2021 20:10:14 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:b58e1f93f66f96078fcf3b303803071e8d8567a667c3fee21386dc868c770767
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8156493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cdc3ec23596c52616fcc585356877668c595ca8018193a01c9d3254f9f854f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:53:22 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 21:54:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 14 Apr 2021 21:54:19 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Apr 2021 21:54:24 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 21:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 21:54:29 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889d7d932cdf8fc9c44ea92f7b0f3dac698471c55ea07de27f7648bef4aed40f`  
		Last Modified: Wed, 14 Apr 2021 21:55:09 GMT  
		Size: 5.5 MB (5533941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ad50628fd5f31a6e02c55635819719b6483170b554049a864c5cdadd20f6f3`  
		Last Modified: Wed, 14 Apr 2021 21:55:04 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:94b3ca9270cb3d8f3cefd68364d5d44225308e48ea1f5894a328985d37dc81fc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ee314823b892bebafa97a7380df19d87652a5d88bbf7c333dfddaaae5c91c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:19:53 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 23:20:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 14 Apr 2021 23:20:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Apr 2021 23:20:19 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 23:20:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:20:38 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec26c8dde7f07735de5bedf2f5fbd6e39ff3e3b2f1811932a5edd0bd01b8725`  
		Last Modified: Wed, 14 Apr 2021 23:21:47 GMT  
		Size: 5.5 MB (5527163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723207646a20891f00477703c6c1c6a7575b5adbfd55d7fa35de8c71ba1fcaa7`  
		Last Modified: Wed, 14 Apr 2021 23:21:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:d1d627aeffa6f985495d72cccf40be8779569633f1e2924df6a989f925302973
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8164956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6f16daf45aac895a1900357375eb4226370f3d6c6a29795d1851e7cef0c41c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 00:22:24 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Thu, 15 Apr 2021 00:22:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 15 Apr 2021 00:22:35 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 15 Apr 2021 00:22:38 GMT
EXPOSE 4222 8222
# Thu, 15 Apr 2021 00:22:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 00:22:42 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88a3713287cdfd75676e7eb7ba86d05a503fe08cc3d375e825348cba80edcef`  
		Last Modified: Thu, 15 Apr 2021 00:25:13 GMT  
		Size: 5.5 MB (5452509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47b975e02a011a0ee3a4da4a81c5435fc11741969644281e8ec8f09f146341a`  
		Last Modified: Thu, 15 Apr 2021 00:25:10 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-alpine3.13`

```console
$ docker pull nats-streaming@sha256:ed61be1c1e81fe7ff551c6520026d982ce60a6ad7e8c0007bf9259f623d434c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21-alpine3.13` - linux; amd64

```console
$ docker pull nats-streaming@sha256:72675b6fd1c18a33e5996e738dbca972714f365d257cd8adb172bca6aba6f0dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8775096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f64537c882c84c11c410a0f7e043a29ef4ff08cdaf4d45c7ff76bac1286bd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:09:41 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:09:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 14 Apr 2021 20:09:44 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Apr 2021 20:09:44 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:09:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 20:09:45 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c75bced29aa1bd74c9fff0d702a93a39840b2b4ed08bf2a036a2f1fb4673e14`  
		Last Modified: Wed, 14 Apr 2021 20:10:15 GMT  
		Size: 6.0 MB (5962706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd5e8ff68dafef8eeaffa582db26e788df6089e19711a01b79aae50d4dfe9f8`  
		Last Modified: Wed, 14 Apr 2021 20:10:14 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-alpine3.13` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:b58e1f93f66f96078fcf3b303803071e8d8567a667c3fee21386dc868c770767
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8156493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cdc3ec23596c52616fcc585356877668c595ca8018193a01c9d3254f9f854f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:53:22 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 21:54:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 14 Apr 2021 21:54:19 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Apr 2021 21:54:24 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 21:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 21:54:29 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889d7d932cdf8fc9c44ea92f7b0f3dac698471c55ea07de27f7648bef4aed40f`  
		Last Modified: Wed, 14 Apr 2021 21:55:09 GMT  
		Size: 5.5 MB (5533941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ad50628fd5f31a6e02c55635819719b6483170b554049a864c5cdadd20f6f3`  
		Last Modified: Wed, 14 Apr 2021 21:55:04 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-alpine3.13` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:94b3ca9270cb3d8f3cefd68364d5d44225308e48ea1f5894a328985d37dc81fc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ee314823b892bebafa97a7380df19d87652a5d88bbf7c333dfddaaae5c91c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:19:53 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 23:20:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 14 Apr 2021 23:20:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Apr 2021 23:20:19 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 23:20:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:20:38 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec26c8dde7f07735de5bedf2f5fbd6e39ff3e3b2f1811932a5edd0bd01b8725`  
		Last Modified: Wed, 14 Apr 2021 23:21:47 GMT  
		Size: 5.5 MB (5527163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723207646a20891f00477703c6c1c6a7575b5adbfd55d7fa35de8c71ba1fcaa7`  
		Last Modified: Wed, 14 Apr 2021 23:21:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:d1d627aeffa6f985495d72cccf40be8779569633f1e2924df6a989f925302973
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8164956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6f16daf45aac895a1900357375eb4226370f3d6c6a29795d1851e7cef0c41c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 00:22:24 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Thu, 15 Apr 2021 00:22:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 15 Apr 2021 00:22:35 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 15 Apr 2021 00:22:38 GMT
EXPOSE 4222 8222
# Thu, 15 Apr 2021 00:22:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 00:22:42 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88a3713287cdfd75676e7eb7ba86d05a503fe08cc3d375e825348cba80edcef`  
		Last Modified: Thu, 15 Apr 2021 00:25:13 GMT  
		Size: 5.5 MB (5452509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47b975e02a011a0ee3a4da4a81c5435fc11741969644281e8ec8f09f146341a`  
		Last Modified: Thu, 15 Apr 2021 00:25:10 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-linux`

```console
$ docker pull nats-streaming@sha256:26603f9112b727df8e9736407a1ec1ab031317a9f6964ba0d407baea6b8d152c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:aa6af76760541ce71d366ac25554ad7caa95aea8cd230dd2688fd76b0645b329
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31671965fc8e3e2d623279516e43fd9d1a5d8d82a19fe709c69d7bfe7ac50085`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 07:43:28 GMT
COPY file:2c21a07cd43acfd157f86c6cf727430cf07e201a3bf3668b2083f473385db991 in /nats-streaming-server 
# Sat, 06 Mar 2021 07:43:28 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 07:43:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 07:43:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6f1c3ed40f752c2108b0e5d9224fba83d5045dac3370f93a50d91af0bc201c05`  
		Last Modified: Sat, 06 Mar 2021 07:44:17 GMT  
		Size: 5.7 MB (5680474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:907a450228b0d46339c5af803a9475165f7cfd9d20d5e09e8f66f9d048d1f7b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c6d73cc983f6821e57de28a32cec901f28d3c5ada68aa9e71a1880962a9f07`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 02:10:29 GMT
COPY file:bd617234b457ddee67b99f0e411029c6d5badad5059fbd81239c0acfe92cd4b7 in /nats-streaming-server 
# Sat, 06 Mar 2021 02:10:30 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 02:10:31 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 02:10:31 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ef1f32aa7a9ce9c8d42c909d32f61dabfa957c0b6a2b3590cd5e5847fb634355`  
		Last Modified: Sat, 06 Mar 2021 02:11:15 GMT  
		Size: 5.3 MB (5252895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ae774aee41bd64306207d739d2290639f673c9c66c367a83f155a923fe8c13f6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce52186dd957f6b70b086fdcbc8212e079e5ed5e3e0013f8f72b3922535a56e`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 01:00:25 GMT
COPY file:546c18b3e8e91d453d1a325c6e4dbc3c945564c010676da1abe89a653a0dea84 in /nats-streaming-server 
# Sat, 06 Mar 2021 01:00:27 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:00:28 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 01:00:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ed8ed2aa5d978cf51ebe3454de1832aeb40919052c5cb17d5b63865c31fc03c7`  
		Last Modified: Sat, 06 Mar 2021 01:01:07 GMT  
		Size: 5.2 MB (5246286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:7fccb492771f9c26f12f03c49e84ba4fb4d7004c6d142f4a7b83337d92feda95
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e817dd7b95371ae514afe3154e4aeba302d94dbed618a0aba7ece8696c13c6`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 01:51:04 GMT
COPY file:ed938be8d92952afe74223a94317bf582d9bcf2c458a54733da01a37a65d421b in /nats-streaming-server 
# Sat, 06 Mar 2021 01:51:05 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:51:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 01:51:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f5ab53e298c8bd7b93e991f4b12e4015cde7d604e6d5ee086e994a86e0556094`  
		Last Modified: Sat, 06 Mar 2021 01:51:46 GMT  
		Size: 5.2 MB (5170586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-nanoserver`

```console
$ docker pull nats-streaming@sha256:95bc515e031c568aebd0e0579c3247df2a2e0affdfc8edb253fa5f85c496d551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:0.21-nanoserver` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:54818a8a35d4a6a4e9efd14ee26c405e9aff90c33b6d5ddd815ff4b4410dad8b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107155482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be925e76dc6a703aa26d065b798d75738366f16d758e6d881239034e4ebc3ac`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:30:32 GMT
RUN cmd /S /C #(nop) COPY file:189ca6af047e9f9cf54ab2176b48588e01c7497fe0b5b0d7b2614ebad66ed089 in C:\nats-streaming-server.exe 
# Wed, 14 Apr 2021 20:30:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:30:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:30:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8f5e1772f13f9dbd7806652f582319d4c94b5e221ddca9bdd7a9a08472b446`  
		Last Modified: Wed, 14 Apr 2021 20:35:48 GMT  
		Size: 5.8 MB (5810702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45528fb53c9d98e2841a65b4761f5e3e524204d43fa18f0f4e5bf517a6fd003`  
		Last Modified: Wed, 14 Apr 2021 20:35:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2de582a0cd8ce6292e31cfe6870e1766cf4ce33b53febbf987b8210419f90d0`  
		Last Modified: Wed, 14 Apr 2021 20:35:48 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a29154792d4c050924f398e1e63281f55a67fd9d0393fb45d94b0613d10302e`  
		Last Modified: Wed, 14 Apr 2021 20:35:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:95bc515e031c568aebd0e0579c3247df2a2e0affdfc8edb253fa5f85c496d551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:0.21-nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:54818a8a35d4a6a4e9efd14ee26c405e9aff90c33b6d5ddd815ff4b4410dad8b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107155482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be925e76dc6a703aa26d065b798d75738366f16d758e6d881239034e4ebc3ac`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:30:32 GMT
RUN cmd /S /C #(nop) COPY file:189ca6af047e9f9cf54ab2176b48588e01c7497fe0b5b0d7b2614ebad66ed089 in C:\nats-streaming-server.exe 
# Wed, 14 Apr 2021 20:30:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:30:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:30:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8f5e1772f13f9dbd7806652f582319d4c94b5e221ddca9bdd7a9a08472b446`  
		Last Modified: Wed, 14 Apr 2021 20:35:48 GMT  
		Size: 5.8 MB (5810702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45528fb53c9d98e2841a65b4761f5e3e524204d43fa18f0f4e5bf517a6fd003`  
		Last Modified: Wed, 14 Apr 2021 20:35:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2de582a0cd8ce6292e31cfe6870e1766cf4ce33b53febbf987b8210419f90d0`  
		Last Modified: Wed, 14 Apr 2021 20:35:48 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a29154792d4c050924f398e1e63281f55a67fd9d0393fb45d94b0613d10302e`  
		Last Modified: Wed, 14 Apr 2021 20:35:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-scratch`

```console
$ docker pull nats-streaming@sha256:26603f9112b727df8e9736407a1ec1ab031317a9f6964ba0d407baea6b8d152c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:aa6af76760541ce71d366ac25554ad7caa95aea8cd230dd2688fd76b0645b329
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31671965fc8e3e2d623279516e43fd9d1a5d8d82a19fe709c69d7bfe7ac50085`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 07:43:28 GMT
COPY file:2c21a07cd43acfd157f86c6cf727430cf07e201a3bf3668b2083f473385db991 in /nats-streaming-server 
# Sat, 06 Mar 2021 07:43:28 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 07:43:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 07:43:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6f1c3ed40f752c2108b0e5d9224fba83d5045dac3370f93a50d91af0bc201c05`  
		Last Modified: Sat, 06 Mar 2021 07:44:17 GMT  
		Size: 5.7 MB (5680474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:907a450228b0d46339c5af803a9475165f7cfd9d20d5e09e8f66f9d048d1f7b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c6d73cc983f6821e57de28a32cec901f28d3c5ada68aa9e71a1880962a9f07`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 02:10:29 GMT
COPY file:bd617234b457ddee67b99f0e411029c6d5badad5059fbd81239c0acfe92cd4b7 in /nats-streaming-server 
# Sat, 06 Mar 2021 02:10:30 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 02:10:31 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 02:10:31 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ef1f32aa7a9ce9c8d42c909d32f61dabfa957c0b6a2b3590cd5e5847fb634355`  
		Last Modified: Sat, 06 Mar 2021 02:11:15 GMT  
		Size: 5.3 MB (5252895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ae774aee41bd64306207d739d2290639f673c9c66c367a83f155a923fe8c13f6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce52186dd957f6b70b086fdcbc8212e079e5ed5e3e0013f8f72b3922535a56e`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 01:00:25 GMT
COPY file:546c18b3e8e91d453d1a325c6e4dbc3c945564c010676da1abe89a653a0dea84 in /nats-streaming-server 
# Sat, 06 Mar 2021 01:00:27 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:00:28 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 01:00:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ed8ed2aa5d978cf51ebe3454de1832aeb40919052c5cb17d5b63865c31fc03c7`  
		Last Modified: Sat, 06 Mar 2021 01:01:07 GMT  
		Size: 5.2 MB (5246286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:7fccb492771f9c26f12f03c49e84ba4fb4d7004c6d142f4a7b83337d92feda95
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e817dd7b95371ae514afe3154e4aeba302d94dbed618a0aba7ece8696c13c6`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 01:51:04 GMT
COPY file:ed938be8d92952afe74223a94317bf582d9bcf2c458a54733da01a37a65d421b in /nats-streaming-server 
# Sat, 06 Mar 2021 01:51:05 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:51:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 01:51:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f5ab53e298c8bd7b93e991f4b12e4015cde7d604e6d5ee086e994a86e0556094`  
		Last Modified: Sat, 06 Mar 2021 01:51:46 GMT  
		Size: 5.2 MB (5170586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-windowsservercore`

```console
$ docker pull nats-streaming@sha256:a8102f4b4b7a4dd707584cb4127c67087e63f8b5bb46b66e8bcd6dc8565c6258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `nats-streaming:0.21-windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:d9b88aa3a330b3290906f99e7d6ecd15ca2a2e1d3971b9d9289b93d30c3cd169
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2485693134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edccba0ec32510e9cbd95e6fb54bc1cce5ffcda21318e14b15aef92d30b968a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 13:10:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Apr 2021 16:02:50 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:27:47 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:27:48 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Wed, 14 Apr 2021 20:27:49 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Wed, 14 Apr 2021 20:28:31 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 20:30:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 20:30:14 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:30:15 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:30:16 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2159a5d0f75ce11e6fe71e4260ede5c3c88a9eb76a0ff43ac6746b2b9b96775`  
		Last Modified: Wed, 14 Apr 2021 15:37:10 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e849354f21f856ec720d6daecc37978fd7246f376ba3c32fd63d4400cce357bc`  
		Last Modified: Wed, 14 Apr 2021 16:10:16 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117282a30c6a3fbb982bd59e09a51b1fef503b2c8b179319ba79482e99fe384e`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496226fe152ceeff1fa0f62ca2d7b6bc19faa001434219174ae46a5fd50a5062`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d2433ca3469117417315b440945cb8cd6772eb21571dd4179873e007da1d89`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939e907443a80f726b409bd6af9aac2d7d95ea075599cf36b47c67d96db68e5b`  
		Last Modified: Wed, 14 Apr 2021 20:35:33 GMT  
		Size: 5.1 MB (5072715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36493380d982f607672d92b042f6a6fba85e6c73a2514659ab314414e1e03ce5`  
		Last Modified: Wed, 14 Apr 2021 20:35:31 GMT  
		Size: 10.9 MB (10855200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c00d72188f4d2c91bcd99fcff6f8aaa8ecbddaf6e31490f52ea27ffa361240b`  
		Last Modified: Wed, 14 Apr 2021 20:35:27 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c24f1b01b5e8513e9c865e784023d71e169853d5b5d84d09f32a4ad347d6633`  
		Last Modified: Wed, 14 Apr 2021 20:35:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d461ef53125c21684fd7078f19d920864bc170e1419530a9799d4c4637f57e6c`  
		Last Modified: Wed, 14 Apr 2021 20:35:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull nats-streaming@sha256:fb1d8548b281cb5116d343ca84eeeb7b3b384ea4fbad8e15050fa042425a55e3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816454011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f2cd68f941eba9047e18e03d45bc6ad435c2f87e4374be7184090e2822cc37`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 13:22:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Apr 2021 16:05:33 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:30:43 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:30:45 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Wed, 14 Apr 2021 20:30:46 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Wed, 14 Apr 2021 20:32:29 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 20:34:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 20:34:43 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:34:44 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:34:46 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f616bb7876e6f944d82fa1802ffab5ca4931a63e1b999f0851b52120cda83539`  
		Last Modified: Wed, 14 Apr 2021 15:37:43 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfa54f43457753c391f21da5e9a5bf47c61c574c0da04b8614d0e84bf823f54`  
		Last Modified: Wed, 14 Apr 2021 16:11:03 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d8948e6263c2bac7f73817369684ee9ce80dcea983d2da7c4d7be9fa1b92da`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a701af2866e93c3ecf557b60b96c4c01276eb2e524382b5ad189843adbf3355`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fc8f88f56d9ac579fa5db162a04bdd9d01802dd45c4f75577dae3515349334`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff9002a73083bb7987c2c033559072c3803ffb30b5df7ec99d7236e718ac397`  
		Last Modified: Wed, 14 Apr 2021 20:36:04 GMT  
		Size: 5.6 MB (5646320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4a7bb20d404a5bac7e79831b31797bd1a2dbf58ab157ff26fafe63e748966e`  
		Last Modified: Wed, 14 Apr 2021 20:36:07 GMT  
		Size: 15.9 MB (15912932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ceea9dc7862bc910070631046bb01d0159fcd3afa884d913477ddea2ae4ef9`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e773fcabbbc441abd5c250e3169866ae46ab83e23543816209ecb0e60e0f60`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23273c3337d46e183210a490996b4c40d280c0fbeae6ad837f0be19167750c38`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:f7a8702b4cb6a52239985459aed34c3aede42735cd7c155284a82d0bea7b46c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:0.21-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:d9b88aa3a330b3290906f99e7d6ecd15ca2a2e1d3971b9d9289b93d30c3cd169
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2485693134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edccba0ec32510e9cbd95e6fb54bc1cce5ffcda21318e14b15aef92d30b968a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 13:10:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Apr 2021 16:02:50 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:27:47 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:27:48 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Wed, 14 Apr 2021 20:27:49 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Wed, 14 Apr 2021 20:28:31 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 20:30:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 20:30:14 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:30:15 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:30:16 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2159a5d0f75ce11e6fe71e4260ede5c3c88a9eb76a0ff43ac6746b2b9b96775`  
		Last Modified: Wed, 14 Apr 2021 15:37:10 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e849354f21f856ec720d6daecc37978fd7246f376ba3c32fd63d4400cce357bc`  
		Last Modified: Wed, 14 Apr 2021 16:10:16 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117282a30c6a3fbb982bd59e09a51b1fef503b2c8b179319ba79482e99fe384e`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496226fe152ceeff1fa0f62ca2d7b6bc19faa001434219174ae46a5fd50a5062`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d2433ca3469117417315b440945cb8cd6772eb21571dd4179873e007da1d89`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939e907443a80f726b409bd6af9aac2d7d95ea075599cf36b47c67d96db68e5b`  
		Last Modified: Wed, 14 Apr 2021 20:35:33 GMT  
		Size: 5.1 MB (5072715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36493380d982f607672d92b042f6a6fba85e6c73a2514659ab314414e1e03ce5`  
		Last Modified: Wed, 14 Apr 2021 20:35:31 GMT  
		Size: 10.9 MB (10855200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c00d72188f4d2c91bcd99fcff6f8aaa8ecbddaf6e31490f52ea27ffa361240b`  
		Last Modified: Wed, 14 Apr 2021 20:35:27 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c24f1b01b5e8513e9c865e784023d71e169853d5b5d84d09f32a4ad347d6633`  
		Last Modified: Wed, 14 Apr 2021 20:35:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d461ef53125c21684fd7078f19d920864bc170e1419530a9799d4c4637f57e6c`  
		Last Modified: Wed, 14 Apr 2021 20:35:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:0afaed268a1479f457d93dd9f8ec62024648ddba56bf49509b2a0de1523bf29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `nats-streaming:0.21-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull nats-streaming@sha256:fb1d8548b281cb5116d343ca84eeeb7b3b384ea4fbad8e15050fa042425a55e3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816454011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f2cd68f941eba9047e18e03d45bc6ad435c2f87e4374be7184090e2822cc37`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 13:22:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Apr 2021 16:05:33 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:30:43 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:30:45 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Wed, 14 Apr 2021 20:30:46 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Wed, 14 Apr 2021 20:32:29 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 20:34:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 20:34:43 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:34:44 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:34:46 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f616bb7876e6f944d82fa1802ffab5ca4931a63e1b999f0851b52120cda83539`  
		Last Modified: Wed, 14 Apr 2021 15:37:43 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfa54f43457753c391f21da5e9a5bf47c61c574c0da04b8614d0e84bf823f54`  
		Last Modified: Wed, 14 Apr 2021 16:11:03 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d8948e6263c2bac7f73817369684ee9ce80dcea983d2da7c4d7be9fa1b92da`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a701af2866e93c3ecf557b60b96c4c01276eb2e524382b5ad189843adbf3355`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fc8f88f56d9ac579fa5db162a04bdd9d01802dd45c4f75577dae3515349334`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff9002a73083bb7987c2c033559072c3803ffb30b5df7ec99d7236e718ac397`  
		Last Modified: Wed, 14 Apr 2021 20:36:04 GMT  
		Size: 5.6 MB (5646320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4a7bb20d404a5bac7e79831b31797bd1a2dbf58ab157ff26fafe63e748966e`  
		Last Modified: Wed, 14 Apr 2021 20:36:07 GMT  
		Size: 15.9 MB (15912932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ceea9dc7862bc910070631046bb01d0159fcd3afa884d913477ddea2ae4ef9`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e773fcabbbc441abd5c250e3169866ae46ab83e23543816209ecb0e60e0f60`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23273c3337d46e183210a490996b4c40d280c0fbeae6ad837f0be19167750c38`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.1`

```console
$ docker pull nats-streaming@sha256:4fc8a5fbef2b822d6456b521cd88bcc6db2c7a0df7a4e983c148018998ce2347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:0.21.1` - linux; amd64

```console
$ docker pull nats-streaming@sha256:aa6af76760541ce71d366ac25554ad7caa95aea8cd230dd2688fd76b0645b329
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31671965fc8e3e2d623279516e43fd9d1a5d8d82a19fe709c69d7bfe7ac50085`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 07:43:28 GMT
COPY file:2c21a07cd43acfd157f86c6cf727430cf07e201a3bf3668b2083f473385db991 in /nats-streaming-server 
# Sat, 06 Mar 2021 07:43:28 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 07:43:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 07:43:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6f1c3ed40f752c2108b0e5d9224fba83d5045dac3370f93a50d91af0bc201c05`  
		Last Modified: Sat, 06 Mar 2021 07:44:17 GMT  
		Size: 5.7 MB (5680474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:907a450228b0d46339c5af803a9475165f7cfd9d20d5e09e8f66f9d048d1f7b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c6d73cc983f6821e57de28a32cec901f28d3c5ada68aa9e71a1880962a9f07`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 02:10:29 GMT
COPY file:bd617234b457ddee67b99f0e411029c6d5badad5059fbd81239c0acfe92cd4b7 in /nats-streaming-server 
# Sat, 06 Mar 2021 02:10:30 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 02:10:31 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 02:10:31 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ef1f32aa7a9ce9c8d42c909d32f61dabfa957c0b6a2b3590cd5e5847fb634355`  
		Last Modified: Sat, 06 Mar 2021 02:11:15 GMT  
		Size: 5.3 MB (5252895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ae774aee41bd64306207d739d2290639f673c9c66c367a83f155a923fe8c13f6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce52186dd957f6b70b086fdcbc8212e079e5ed5e3e0013f8f72b3922535a56e`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 01:00:25 GMT
COPY file:546c18b3e8e91d453d1a325c6e4dbc3c945564c010676da1abe89a653a0dea84 in /nats-streaming-server 
# Sat, 06 Mar 2021 01:00:27 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:00:28 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 01:00:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ed8ed2aa5d978cf51ebe3454de1832aeb40919052c5cb17d5b63865c31fc03c7`  
		Last Modified: Sat, 06 Mar 2021 01:01:07 GMT  
		Size: 5.2 MB (5246286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:7fccb492771f9c26f12f03c49e84ba4fb4d7004c6d142f4a7b83337d92feda95
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e817dd7b95371ae514afe3154e4aeba302d94dbed618a0aba7ece8696c13c6`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 01:51:04 GMT
COPY file:ed938be8d92952afe74223a94317bf582d9bcf2c458a54733da01a37a65d421b in /nats-streaming-server 
# Sat, 06 Mar 2021 01:51:05 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:51:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 01:51:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f5ab53e298c8bd7b93e991f4b12e4015cde7d604e6d5ee086e994a86e0556094`  
		Last Modified: Sat, 06 Mar 2021 01:51:46 GMT  
		Size: 5.2 MB (5170586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:54818a8a35d4a6a4e9efd14ee26c405e9aff90c33b6d5ddd815ff4b4410dad8b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107155482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be925e76dc6a703aa26d065b798d75738366f16d758e6d881239034e4ebc3ac`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:30:32 GMT
RUN cmd /S /C #(nop) COPY file:189ca6af047e9f9cf54ab2176b48588e01c7497fe0b5b0d7b2614ebad66ed089 in C:\nats-streaming-server.exe 
# Wed, 14 Apr 2021 20:30:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:30:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:30:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8f5e1772f13f9dbd7806652f582319d4c94b5e221ddca9bdd7a9a08472b446`  
		Last Modified: Wed, 14 Apr 2021 20:35:48 GMT  
		Size: 5.8 MB (5810702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45528fb53c9d98e2841a65b4761f5e3e524204d43fa18f0f4e5bf517a6fd003`  
		Last Modified: Wed, 14 Apr 2021 20:35:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2de582a0cd8ce6292e31cfe6870e1766cf4ce33b53febbf987b8210419f90d0`  
		Last Modified: Wed, 14 Apr 2021 20:35:48 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a29154792d4c050924f398e1e63281f55a67fd9d0393fb45d94b0613d10302e`  
		Last Modified: Wed, 14 Apr 2021 20:35:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.1-alpine`

```console
$ docker pull nats-streaming@sha256:ed61be1c1e81fe7ff551c6520026d982ce60a6ad7e8c0007bf9259f623d434c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21.1-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:72675b6fd1c18a33e5996e738dbca972714f365d257cd8adb172bca6aba6f0dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8775096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f64537c882c84c11c410a0f7e043a29ef4ff08cdaf4d45c7ff76bac1286bd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:09:41 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:09:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 14 Apr 2021 20:09:44 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Apr 2021 20:09:44 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:09:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 20:09:45 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c75bced29aa1bd74c9fff0d702a93a39840b2b4ed08bf2a036a2f1fb4673e14`  
		Last Modified: Wed, 14 Apr 2021 20:10:15 GMT  
		Size: 6.0 MB (5962706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd5e8ff68dafef8eeaffa582db26e788df6089e19711a01b79aae50d4dfe9f8`  
		Last Modified: Wed, 14 Apr 2021 20:10:14 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:b58e1f93f66f96078fcf3b303803071e8d8567a667c3fee21386dc868c770767
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8156493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cdc3ec23596c52616fcc585356877668c595ca8018193a01c9d3254f9f854f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:53:22 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 21:54:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 14 Apr 2021 21:54:19 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Apr 2021 21:54:24 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 21:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 21:54:29 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889d7d932cdf8fc9c44ea92f7b0f3dac698471c55ea07de27f7648bef4aed40f`  
		Last Modified: Wed, 14 Apr 2021 21:55:09 GMT  
		Size: 5.5 MB (5533941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ad50628fd5f31a6e02c55635819719b6483170b554049a864c5cdadd20f6f3`  
		Last Modified: Wed, 14 Apr 2021 21:55:04 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:94b3ca9270cb3d8f3cefd68364d5d44225308e48ea1f5894a328985d37dc81fc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ee314823b892bebafa97a7380df19d87652a5d88bbf7c333dfddaaae5c91c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:19:53 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 23:20:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 14 Apr 2021 23:20:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Apr 2021 23:20:19 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 23:20:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:20:38 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec26c8dde7f07735de5bedf2f5fbd6e39ff3e3b2f1811932a5edd0bd01b8725`  
		Last Modified: Wed, 14 Apr 2021 23:21:47 GMT  
		Size: 5.5 MB (5527163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723207646a20891f00477703c6c1c6a7575b5adbfd55d7fa35de8c71ba1fcaa7`  
		Last Modified: Wed, 14 Apr 2021 23:21:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:d1d627aeffa6f985495d72cccf40be8779569633f1e2924df6a989f925302973
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8164956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6f16daf45aac895a1900357375eb4226370f3d6c6a29795d1851e7cef0c41c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 00:22:24 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Thu, 15 Apr 2021 00:22:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 15 Apr 2021 00:22:35 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 15 Apr 2021 00:22:38 GMT
EXPOSE 4222 8222
# Thu, 15 Apr 2021 00:22:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 00:22:42 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88a3713287cdfd75676e7eb7ba86d05a503fe08cc3d375e825348cba80edcef`  
		Last Modified: Thu, 15 Apr 2021 00:25:13 GMT  
		Size: 5.5 MB (5452509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47b975e02a011a0ee3a4da4a81c5435fc11741969644281e8ec8f09f146341a`  
		Last Modified: Thu, 15 Apr 2021 00:25:10 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.1-alpine3.13`

```console
$ docker pull nats-streaming@sha256:ed61be1c1e81fe7ff551c6520026d982ce60a6ad7e8c0007bf9259f623d434c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21.1-alpine3.13` - linux; amd64

```console
$ docker pull nats-streaming@sha256:72675b6fd1c18a33e5996e738dbca972714f365d257cd8adb172bca6aba6f0dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8775096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f64537c882c84c11c410a0f7e043a29ef4ff08cdaf4d45c7ff76bac1286bd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:09:41 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:09:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 14 Apr 2021 20:09:44 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Apr 2021 20:09:44 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:09:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 20:09:45 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c75bced29aa1bd74c9fff0d702a93a39840b2b4ed08bf2a036a2f1fb4673e14`  
		Last Modified: Wed, 14 Apr 2021 20:10:15 GMT  
		Size: 6.0 MB (5962706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd5e8ff68dafef8eeaffa582db26e788df6089e19711a01b79aae50d4dfe9f8`  
		Last Modified: Wed, 14 Apr 2021 20:10:14 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-alpine3.13` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:b58e1f93f66f96078fcf3b303803071e8d8567a667c3fee21386dc868c770767
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8156493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cdc3ec23596c52616fcc585356877668c595ca8018193a01c9d3254f9f854f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:53:22 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 21:54:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 14 Apr 2021 21:54:19 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Apr 2021 21:54:24 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 21:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 21:54:29 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889d7d932cdf8fc9c44ea92f7b0f3dac698471c55ea07de27f7648bef4aed40f`  
		Last Modified: Wed, 14 Apr 2021 21:55:09 GMT  
		Size: 5.5 MB (5533941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ad50628fd5f31a6e02c55635819719b6483170b554049a864c5cdadd20f6f3`  
		Last Modified: Wed, 14 Apr 2021 21:55:04 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-alpine3.13` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:94b3ca9270cb3d8f3cefd68364d5d44225308e48ea1f5894a328985d37dc81fc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ee314823b892bebafa97a7380df19d87652a5d88bbf7c333dfddaaae5c91c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:19:53 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 23:20:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 14 Apr 2021 23:20:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Apr 2021 23:20:19 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 23:20:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:20:38 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec26c8dde7f07735de5bedf2f5fbd6e39ff3e3b2f1811932a5edd0bd01b8725`  
		Last Modified: Wed, 14 Apr 2021 23:21:47 GMT  
		Size: 5.5 MB (5527163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723207646a20891f00477703c6c1c6a7575b5adbfd55d7fa35de8c71ba1fcaa7`  
		Last Modified: Wed, 14 Apr 2021 23:21:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:d1d627aeffa6f985495d72cccf40be8779569633f1e2924df6a989f925302973
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8164956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6f16daf45aac895a1900357375eb4226370f3d6c6a29795d1851e7cef0c41c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 00:22:24 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Thu, 15 Apr 2021 00:22:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 15 Apr 2021 00:22:35 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 15 Apr 2021 00:22:38 GMT
EXPOSE 4222 8222
# Thu, 15 Apr 2021 00:22:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 00:22:42 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88a3713287cdfd75676e7eb7ba86d05a503fe08cc3d375e825348cba80edcef`  
		Last Modified: Thu, 15 Apr 2021 00:25:13 GMT  
		Size: 5.5 MB (5452509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47b975e02a011a0ee3a4da4a81c5435fc11741969644281e8ec8f09f146341a`  
		Last Modified: Thu, 15 Apr 2021 00:25:10 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.1-linux`

```console
$ docker pull nats-streaming@sha256:26603f9112b727df8e9736407a1ec1ab031317a9f6964ba0d407baea6b8d152c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21.1-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:aa6af76760541ce71d366ac25554ad7caa95aea8cd230dd2688fd76b0645b329
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31671965fc8e3e2d623279516e43fd9d1a5d8d82a19fe709c69d7bfe7ac50085`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 07:43:28 GMT
COPY file:2c21a07cd43acfd157f86c6cf727430cf07e201a3bf3668b2083f473385db991 in /nats-streaming-server 
# Sat, 06 Mar 2021 07:43:28 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 07:43:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 07:43:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6f1c3ed40f752c2108b0e5d9224fba83d5045dac3370f93a50d91af0bc201c05`  
		Last Modified: Sat, 06 Mar 2021 07:44:17 GMT  
		Size: 5.7 MB (5680474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:907a450228b0d46339c5af803a9475165f7cfd9d20d5e09e8f66f9d048d1f7b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c6d73cc983f6821e57de28a32cec901f28d3c5ada68aa9e71a1880962a9f07`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 02:10:29 GMT
COPY file:bd617234b457ddee67b99f0e411029c6d5badad5059fbd81239c0acfe92cd4b7 in /nats-streaming-server 
# Sat, 06 Mar 2021 02:10:30 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 02:10:31 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 02:10:31 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ef1f32aa7a9ce9c8d42c909d32f61dabfa957c0b6a2b3590cd5e5847fb634355`  
		Last Modified: Sat, 06 Mar 2021 02:11:15 GMT  
		Size: 5.3 MB (5252895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ae774aee41bd64306207d739d2290639f673c9c66c367a83f155a923fe8c13f6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce52186dd957f6b70b086fdcbc8212e079e5ed5e3e0013f8f72b3922535a56e`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 01:00:25 GMT
COPY file:546c18b3e8e91d453d1a325c6e4dbc3c945564c010676da1abe89a653a0dea84 in /nats-streaming-server 
# Sat, 06 Mar 2021 01:00:27 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:00:28 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 01:00:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ed8ed2aa5d978cf51ebe3454de1832aeb40919052c5cb17d5b63865c31fc03c7`  
		Last Modified: Sat, 06 Mar 2021 01:01:07 GMT  
		Size: 5.2 MB (5246286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:7fccb492771f9c26f12f03c49e84ba4fb4d7004c6d142f4a7b83337d92feda95
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e817dd7b95371ae514afe3154e4aeba302d94dbed618a0aba7ece8696c13c6`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 01:51:04 GMT
COPY file:ed938be8d92952afe74223a94317bf582d9bcf2c458a54733da01a37a65d421b in /nats-streaming-server 
# Sat, 06 Mar 2021 01:51:05 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:51:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 01:51:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f5ab53e298c8bd7b93e991f4b12e4015cde7d604e6d5ee086e994a86e0556094`  
		Last Modified: Sat, 06 Mar 2021 01:51:46 GMT  
		Size: 5.2 MB (5170586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.1-nanoserver`

```console
$ docker pull nats-streaming@sha256:95bc515e031c568aebd0e0579c3247df2a2e0affdfc8edb253fa5f85c496d551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:0.21.1-nanoserver` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:54818a8a35d4a6a4e9efd14ee26c405e9aff90c33b6d5ddd815ff4b4410dad8b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107155482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be925e76dc6a703aa26d065b798d75738366f16d758e6d881239034e4ebc3ac`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:30:32 GMT
RUN cmd /S /C #(nop) COPY file:189ca6af047e9f9cf54ab2176b48588e01c7497fe0b5b0d7b2614ebad66ed089 in C:\nats-streaming-server.exe 
# Wed, 14 Apr 2021 20:30:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:30:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:30:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8f5e1772f13f9dbd7806652f582319d4c94b5e221ddca9bdd7a9a08472b446`  
		Last Modified: Wed, 14 Apr 2021 20:35:48 GMT  
		Size: 5.8 MB (5810702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45528fb53c9d98e2841a65b4761f5e3e524204d43fa18f0f4e5bf517a6fd003`  
		Last Modified: Wed, 14 Apr 2021 20:35:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2de582a0cd8ce6292e31cfe6870e1766cf4ce33b53febbf987b8210419f90d0`  
		Last Modified: Wed, 14 Apr 2021 20:35:48 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a29154792d4c050924f398e1e63281f55a67fd9d0393fb45d94b0613d10302e`  
		Last Modified: Wed, 14 Apr 2021 20:35:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.1-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:95bc515e031c568aebd0e0579c3247df2a2e0affdfc8edb253fa5f85c496d551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:0.21.1-nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:54818a8a35d4a6a4e9efd14ee26c405e9aff90c33b6d5ddd815ff4b4410dad8b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107155482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be925e76dc6a703aa26d065b798d75738366f16d758e6d881239034e4ebc3ac`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:30:32 GMT
RUN cmd /S /C #(nop) COPY file:189ca6af047e9f9cf54ab2176b48588e01c7497fe0b5b0d7b2614ebad66ed089 in C:\nats-streaming-server.exe 
# Wed, 14 Apr 2021 20:30:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:30:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:30:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8f5e1772f13f9dbd7806652f582319d4c94b5e221ddca9bdd7a9a08472b446`  
		Last Modified: Wed, 14 Apr 2021 20:35:48 GMT  
		Size: 5.8 MB (5810702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45528fb53c9d98e2841a65b4761f5e3e524204d43fa18f0f4e5bf517a6fd003`  
		Last Modified: Wed, 14 Apr 2021 20:35:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2de582a0cd8ce6292e31cfe6870e1766cf4ce33b53febbf987b8210419f90d0`  
		Last Modified: Wed, 14 Apr 2021 20:35:48 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a29154792d4c050924f398e1e63281f55a67fd9d0393fb45d94b0613d10302e`  
		Last Modified: Wed, 14 Apr 2021 20:35:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.1-scratch`

```console
$ docker pull nats-streaming@sha256:26603f9112b727df8e9736407a1ec1ab031317a9f6964ba0d407baea6b8d152c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21.1-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:aa6af76760541ce71d366ac25554ad7caa95aea8cd230dd2688fd76b0645b329
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31671965fc8e3e2d623279516e43fd9d1a5d8d82a19fe709c69d7bfe7ac50085`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 07:43:28 GMT
COPY file:2c21a07cd43acfd157f86c6cf727430cf07e201a3bf3668b2083f473385db991 in /nats-streaming-server 
# Sat, 06 Mar 2021 07:43:28 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 07:43:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 07:43:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6f1c3ed40f752c2108b0e5d9224fba83d5045dac3370f93a50d91af0bc201c05`  
		Last Modified: Sat, 06 Mar 2021 07:44:17 GMT  
		Size: 5.7 MB (5680474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:907a450228b0d46339c5af803a9475165f7cfd9d20d5e09e8f66f9d048d1f7b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c6d73cc983f6821e57de28a32cec901f28d3c5ada68aa9e71a1880962a9f07`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 02:10:29 GMT
COPY file:bd617234b457ddee67b99f0e411029c6d5badad5059fbd81239c0acfe92cd4b7 in /nats-streaming-server 
# Sat, 06 Mar 2021 02:10:30 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 02:10:31 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 02:10:31 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ef1f32aa7a9ce9c8d42c909d32f61dabfa957c0b6a2b3590cd5e5847fb634355`  
		Last Modified: Sat, 06 Mar 2021 02:11:15 GMT  
		Size: 5.3 MB (5252895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ae774aee41bd64306207d739d2290639f673c9c66c367a83f155a923fe8c13f6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce52186dd957f6b70b086fdcbc8212e079e5ed5e3e0013f8f72b3922535a56e`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 01:00:25 GMT
COPY file:546c18b3e8e91d453d1a325c6e4dbc3c945564c010676da1abe89a653a0dea84 in /nats-streaming-server 
# Sat, 06 Mar 2021 01:00:27 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:00:28 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 01:00:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ed8ed2aa5d978cf51ebe3454de1832aeb40919052c5cb17d5b63865c31fc03c7`  
		Last Modified: Sat, 06 Mar 2021 01:01:07 GMT  
		Size: 5.2 MB (5246286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:7fccb492771f9c26f12f03c49e84ba4fb4d7004c6d142f4a7b83337d92feda95
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e817dd7b95371ae514afe3154e4aeba302d94dbed618a0aba7ece8696c13c6`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 01:51:04 GMT
COPY file:ed938be8d92952afe74223a94317bf582d9bcf2c458a54733da01a37a65d421b in /nats-streaming-server 
# Sat, 06 Mar 2021 01:51:05 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:51:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 01:51:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f5ab53e298c8bd7b93e991f4b12e4015cde7d604e6d5ee086e994a86e0556094`  
		Last Modified: Sat, 06 Mar 2021 01:51:46 GMT  
		Size: 5.2 MB (5170586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.1-windowsservercore`

```console
$ docker pull nats-streaming@sha256:a8102f4b4b7a4dd707584cb4127c67087e63f8b5bb46b66e8bcd6dc8565c6258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `nats-streaming:0.21.1-windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:d9b88aa3a330b3290906f99e7d6ecd15ca2a2e1d3971b9d9289b93d30c3cd169
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2485693134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edccba0ec32510e9cbd95e6fb54bc1cce5ffcda21318e14b15aef92d30b968a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 13:10:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Apr 2021 16:02:50 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:27:47 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:27:48 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Wed, 14 Apr 2021 20:27:49 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Wed, 14 Apr 2021 20:28:31 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 20:30:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 20:30:14 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:30:15 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:30:16 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2159a5d0f75ce11e6fe71e4260ede5c3c88a9eb76a0ff43ac6746b2b9b96775`  
		Last Modified: Wed, 14 Apr 2021 15:37:10 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e849354f21f856ec720d6daecc37978fd7246f376ba3c32fd63d4400cce357bc`  
		Last Modified: Wed, 14 Apr 2021 16:10:16 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117282a30c6a3fbb982bd59e09a51b1fef503b2c8b179319ba79482e99fe384e`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496226fe152ceeff1fa0f62ca2d7b6bc19faa001434219174ae46a5fd50a5062`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d2433ca3469117417315b440945cb8cd6772eb21571dd4179873e007da1d89`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939e907443a80f726b409bd6af9aac2d7d95ea075599cf36b47c67d96db68e5b`  
		Last Modified: Wed, 14 Apr 2021 20:35:33 GMT  
		Size: 5.1 MB (5072715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36493380d982f607672d92b042f6a6fba85e6c73a2514659ab314414e1e03ce5`  
		Last Modified: Wed, 14 Apr 2021 20:35:31 GMT  
		Size: 10.9 MB (10855200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c00d72188f4d2c91bcd99fcff6f8aaa8ecbddaf6e31490f52ea27ffa361240b`  
		Last Modified: Wed, 14 Apr 2021 20:35:27 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c24f1b01b5e8513e9c865e784023d71e169853d5b5d84d09f32a4ad347d6633`  
		Last Modified: Wed, 14 Apr 2021 20:35:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d461ef53125c21684fd7078f19d920864bc170e1419530a9799d4c4637f57e6c`  
		Last Modified: Wed, 14 Apr 2021 20:35:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull nats-streaming@sha256:fb1d8548b281cb5116d343ca84eeeb7b3b384ea4fbad8e15050fa042425a55e3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816454011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f2cd68f941eba9047e18e03d45bc6ad435c2f87e4374be7184090e2822cc37`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 13:22:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Apr 2021 16:05:33 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:30:43 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:30:45 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Wed, 14 Apr 2021 20:30:46 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Wed, 14 Apr 2021 20:32:29 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 20:34:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 20:34:43 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:34:44 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:34:46 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f616bb7876e6f944d82fa1802ffab5ca4931a63e1b999f0851b52120cda83539`  
		Last Modified: Wed, 14 Apr 2021 15:37:43 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfa54f43457753c391f21da5e9a5bf47c61c574c0da04b8614d0e84bf823f54`  
		Last Modified: Wed, 14 Apr 2021 16:11:03 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d8948e6263c2bac7f73817369684ee9ce80dcea983d2da7c4d7be9fa1b92da`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a701af2866e93c3ecf557b60b96c4c01276eb2e524382b5ad189843adbf3355`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fc8f88f56d9ac579fa5db162a04bdd9d01802dd45c4f75577dae3515349334`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff9002a73083bb7987c2c033559072c3803ffb30b5df7ec99d7236e718ac397`  
		Last Modified: Wed, 14 Apr 2021 20:36:04 GMT  
		Size: 5.6 MB (5646320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4a7bb20d404a5bac7e79831b31797bd1a2dbf58ab157ff26fafe63e748966e`  
		Last Modified: Wed, 14 Apr 2021 20:36:07 GMT  
		Size: 15.9 MB (15912932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ceea9dc7862bc910070631046bb01d0159fcd3afa884d913477ddea2ae4ef9`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e773fcabbbc441abd5c250e3169866ae46ab83e23543816209ecb0e60e0f60`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23273c3337d46e183210a490996b4c40d280c0fbeae6ad837f0be19167750c38`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.1-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:f7a8702b4cb6a52239985459aed34c3aede42735cd7c155284a82d0bea7b46c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:0.21.1-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:d9b88aa3a330b3290906f99e7d6ecd15ca2a2e1d3971b9d9289b93d30c3cd169
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2485693134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edccba0ec32510e9cbd95e6fb54bc1cce5ffcda21318e14b15aef92d30b968a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 13:10:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Apr 2021 16:02:50 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:27:47 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:27:48 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Wed, 14 Apr 2021 20:27:49 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Wed, 14 Apr 2021 20:28:31 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 20:30:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 20:30:14 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:30:15 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:30:16 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2159a5d0f75ce11e6fe71e4260ede5c3c88a9eb76a0ff43ac6746b2b9b96775`  
		Last Modified: Wed, 14 Apr 2021 15:37:10 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e849354f21f856ec720d6daecc37978fd7246f376ba3c32fd63d4400cce357bc`  
		Last Modified: Wed, 14 Apr 2021 16:10:16 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117282a30c6a3fbb982bd59e09a51b1fef503b2c8b179319ba79482e99fe384e`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496226fe152ceeff1fa0f62ca2d7b6bc19faa001434219174ae46a5fd50a5062`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d2433ca3469117417315b440945cb8cd6772eb21571dd4179873e007da1d89`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939e907443a80f726b409bd6af9aac2d7d95ea075599cf36b47c67d96db68e5b`  
		Last Modified: Wed, 14 Apr 2021 20:35:33 GMT  
		Size: 5.1 MB (5072715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36493380d982f607672d92b042f6a6fba85e6c73a2514659ab314414e1e03ce5`  
		Last Modified: Wed, 14 Apr 2021 20:35:31 GMT  
		Size: 10.9 MB (10855200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c00d72188f4d2c91bcd99fcff6f8aaa8ecbddaf6e31490f52ea27ffa361240b`  
		Last Modified: Wed, 14 Apr 2021 20:35:27 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c24f1b01b5e8513e9c865e784023d71e169853d5b5d84d09f32a4ad347d6633`  
		Last Modified: Wed, 14 Apr 2021 20:35:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d461ef53125c21684fd7078f19d920864bc170e1419530a9799d4c4637f57e6c`  
		Last Modified: Wed, 14 Apr 2021 20:35:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.1-windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:0afaed268a1479f457d93dd9f8ec62024648ddba56bf49509b2a0de1523bf29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `nats-streaming:0.21.1-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull nats-streaming@sha256:fb1d8548b281cb5116d343ca84eeeb7b3b384ea4fbad8e15050fa042425a55e3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816454011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f2cd68f941eba9047e18e03d45bc6ad435c2f87e4374be7184090e2822cc37`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 13:22:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Apr 2021 16:05:33 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:30:43 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:30:45 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Wed, 14 Apr 2021 20:30:46 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Wed, 14 Apr 2021 20:32:29 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 20:34:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 20:34:43 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:34:44 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:34:46 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f616bb7876e6f944d82fa1802ffab5ca4931a63e1b999f0851b52120cda83539`  
		Last Modified: Wed, 14 Apr 2021 15:37:43 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfa54f43457753c391f21da5e9a5bf47c61c574c0da04b8614d0e84bf823f54`  
		Last Modified: Wed, 14 Apr 2021 16:11:03 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d8948e6263c2bac7f73817369684ee9ce80dcea983d2da7c4d7be9fa1b92da`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a701af2866e93c3ecf557b60b96c4c01276eb2e524382b5ad189843adbf3355`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fc8f88f56d9ac579fa5db162a04bdd9d01802dd45c4f75577dae3515349334`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff9002a73083bb7987c2c033559072c3803ffb30b5df7ec99d7236e718ac397`  
		Last Modified: Wed, 14 Apr 2021 20:36:04 GMT  
		Size: 5.6 MB (5646320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4a7bb20d404a5bac7e79831b31797bd1a2dbf58ab157ff26fafe63e748966e`  
		Last Modified: Wed, 14 Apr 2021 20:36:07 GMT  
		Size: 15.9 MB (15912932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ceea9dc7862bc910070631046bb01d0159fcd3afa884d913477ddea2ae4ef9`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e773fcabbbc441abd5c250e3169866ae46ab83e23543816209ecb0e60e0f60`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23273c3337d46e183210a490996b4c40d280c0fbeae6ad837f0be19167750c38`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:ed61be1c1e81fe7ff551c6520026d982ce60a6ad7e8c0007bf9259f623d434c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:72675b6fd1c18a33e5996e738dbca972714f365d257cd8adb172bca6aba6f0dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8775096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f64537c882c84c11c410a0f7e043a29ef4ff08cdaf4d45c7ff76bac1286bd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:09:41 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:09:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 14 Apr 2021 20:09:44 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Apr 2021 20:09:44 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:09:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 20:09:45 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c75bced29aa1bd74c9fff0d702a93a39840b2b4ed08bf2a036a2f1fb4673e14`  
		Last Modified: Wed, 14 Apr 2021 20:10:15 GMT  
		Size: 6.0 MB (5962706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd5e8ff68dafef8eeaffa582db26e788df6089e19711a01b79aae50d4dfe9f8`  
		Last Modified: Wed, 14 Apr 2021 20:10:14 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:b58e1f93f66f96078fcf3b303803071e8d8567a667c3fee21386dc868c770767
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8156493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cdc3ec23596c52616fcc585356877668c595ca8018193a01c9d3254f9f854f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:53:22 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 21:54:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 14 Apr 2021 21:54:19 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Apr 2021 21:54:24 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 21:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 21:54:29 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889d7d932cdf8fc9c44ea92f7b0f3dac698471c55ea07de27f7648bef4aed40f`  
		Last Modified: Wed, 14 Apr 2021 21:55:09 GMT  
		Size: 5.5 MB (5533941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ad50628fd5f31a6e02c55635819719b6483170b554049a864c5cdadd20f6f3`  
		Last Modified: Wed, 14 Apr 2021 21:55:04 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:94b3ca9270cb3d8f3cefd68364d5d44225308e48ea1f5894a328985d37dc81fc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ee314823b892bebafa97a7380df19d87652a5d88bbf7c333dfddaaae5c91c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:19:53 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 23:20:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 14 Apr 2021 23:20:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Apr 2021 23:20:19 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 23:20:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:20:38 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec26c8dde7f07735de5bedf2f5fbd6e39ff3e3b2f1811932a5edd0bd01b8725`  
		Last Modified: Wed, 14 Apr 2021 23:21:47 GMT  
		Size: 5.5 MB (5527163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723207646a20891f00477703c6c1c6a7575b5adbfd55d7fa35de8c71ba1fcaa7`  
		Last Modified: Wed, 14 Apr 2021 23:21:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:d1d627aeffa6f985495d72cccf40be8779569633f1e2924df6a989f925302973
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8164956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6f16daf45aac895a1900357375eb4226370f3d6c6a29795d1851e7cef0c41c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 00:22:24 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Thu, 15 Apr 2021 00:22:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 15 Apr 2021 00:22:35 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 15 Apr 2021 00:22:38 GMT
EXPOSE 4222 8222
# Thu, 15 Apr 2021 00:22:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 00:22:42 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88a3713287cdfd75676e7eb7ba86d05a503fe08cc3d375e825348cba80edcef`  
		Last Modified: Thu, 15 Apr 2021 00:25:13 GMT  
		Size: 5.5 MB (5452509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47b975e02a011a0ee3a4da4a81c5435fc11741969644281e8ec8f09f146341a`  
		Last Modified: Thu, 15 Apr 2021 00:25:10 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.13`

```console
$ docker pull nats-streaming@sha256:ed61be1c1e81fe7ff551c6520026d982ce60a6ad7e8c0007bf9259f623d434c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.13` - linux; amd64

```console
$ docker pull nats-streaming@sha256:72675b6fd1c18a33e5996e738dbca972714f365d257cd8adb172bca6aba6f0dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8775096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f64537c882c84c11c410a0f7e043a29ef4ff08cdaf4d45c7ff76bac1286bd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:09:41 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:09:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 14 Apr 2021 20:09:44 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Apr 2021 20:09:44 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:09:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 20:09:45 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c75bced29aa1bd74c9fff0d702a93a39840b2b4ed08bf2a036a2f1fb4673e14`  
		Last Modified: Wed, 14 Apr 2021 20:10:15 GMT  
		Size: 6.0 MB (5962706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd5e8ff68dafef8eeaffa582db26e788df6089e19711a01b79aae50d4dfe9f8`  
		Last Modified: Wed, 14 Apr 2021 20:10:14 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.13` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:b58e1f93f66f96078fcf3b303803071e8d8567a667c3fee21386dc868c770767
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8156493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cdc3ec23596c52616fcc585356877668c595ca8018193a01c9d3254f9f854f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:53:22 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 21:54:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 14 Apr 2021 21:54:19 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Apr 2021 21:54:24 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 21:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 21:54:29 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889d7d932cdf8fc9c44ea92f7b0f3dac698471c55ea07de27f7648bef4aed40f`  
		Last Modified: Wed, 14 Apr 2021 21:55:09 GMT  
		Size: 5.5 MB (5533941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ad50628fd5f31a6e02c55635819719b6483170b554049a864c5cdadd20f6f3`  
		Last Modified: Wed, 14 Apr 2021 21:55:04 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.13` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:94b3ca9270cb3d8f3cefd68364d5d44225308e48ea1f5894a328985d37dc81fc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ee314823b892bebafa97a7380df19d87652a5d88bbf7c333dfddaaae5c91c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:19:53 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 23:20:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 14 Apr 2021 23:20:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Apr 2021 23:20:19 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 23:20:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:20:38 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec26c8dde7f07735de5bedf2f5fbd6e39ff3e3b2f1811932a5edd0bd01b8725`  
		Last Modified: Wed, 14 Apr 2021 23:21:47 GMT  
		Size: 5.5 MB (5527163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723207646a20891f00477703c6c1c6a7575b5adbfd55d7fa35de8c71ba1fcaa7`  
		Last Modified: Wed, 14 Apr 2021 23:21:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:d1d627aeffa6f985495d72cccf40be8779569633f1e2924df6a989f925302973
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8164956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6f16daf45aac895a1900357375eb4226370f3d6c6a29795d1851e7cef0c41c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 00:22:24 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Thu, 15 Apr 2021 00:22:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 15 Apr 2021 00:22:35 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 15 Apr 2021 00:22:38 GMT
EXPOSE 4222 8222
# Thu, 15 Apr 2021 00:22:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 00:22:42 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88a3713287cdfd75676e7eb7ba86d05a503fe08cc3d375e825348cba80edcef`  
		Last Modified: Thu, 15 Apr 2021 00:25:13 GMT  
		Size: 5.5 MB (5452509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47b975e02a011a0ee3a4da4a81c5435fc11741969644281e8ec8f09f146341a`  
		Last Modified: Thu, 15 Apr 2021 00:25:10 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:4fc8a5fbef2b822d6456b521cd88bcc6db2c7a0df7a4e983c148018998ce2347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:latest` - linux; amd64

```console
$ docker pull nats-streaming@sha256:aa6af76760541ce71d366ac25554ad7caa95aea8cd230dd2688fd76b0645b329
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31671965fc8e3e2d623279516e43fd9d1a5d8d82a19fe709c69d7bfe7ac50085`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 07:43:28 GMT
COPY file:2c21a07cd43acfd157f86c6cf727430cf07e201a3bf3668b2083f473385db991 in /nats-streaming-server 
# Sat, 06 Mar 2021 07:43:28 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 07:43:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 07:43:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6f1c3ed40f752c2108b0e5d9224fba83d5045dac3370f93a50d91af0bc201c05`  
		Last Modified: Sat, 06 Mar 2021 07:44:17 GMT  
		Size: 5.7 MB (5680474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:907a450228b0d46339c5af803a9475165f7cfd9d20d5e09e8f66f9d048d1f7b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c6d73cc983f6821e57de28a32cec901f28d3c5ada68aa9e71a1880962a9f07`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 02:10:29 GMT
COPY file:bd617234b457ddee67b99f0e411029c6d5badad5059fbd81239c0acfe92cd4b7 in /nats-streaming-server 
# Sat, 06 Mar 2021 02:10:30 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 02:10:31 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 02:10:31 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ef1f32aa7a9ce9c8d42c909d32f61dabfa957c0b6a2b3590cd5e5847fb634355`  
		Last Modified: Sat, 06 Mar 2021 02:11:15 GMT  
		Size: 5.3 MB (5252895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ae774aee41bd64306207d739d2290639f673c9c66c367a83f155a923fe8c13f6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce52186dd957f6b70b086fdcbc8212e079e5ed5e3e0013f8f72b3922535a56e`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 01:00:25 GMT
COPY file:546c18b3e8e91d453d1a325c6e4dbc3c945564c010676da1abe89a653a0dea84 in /nats-streaming-server 
# Sat, 06 Mar 2021 01:00:27 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:00:28 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 01:00:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ed8ed2aa5d978cf51ebe3454de1832aeb40919052c5cb17d5b63865c31fc03c7`  
		Last Modified: Sat, 06 Mar 2021 01:01:07 GMT  
		Size: 5.2 MB (5246286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:7fccb492771f9c26f12f03c49e84ba4fb4d7004c6d142f4a7b83337d92feda95
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e817dd7b95371ae514afe3154e4aeba302d94dbed618a0aba7ece8696c13c6`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 01:51:04 GMT
COPY file:ed938be8d92952afe74223a94317bf582d9bcf2c458a54733da01a37a65d421b in /nats-streaming-server 
# Sat, 06 Mar 2021 01:51:05 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:51:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 01:51:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f5ab53e298c8bd7b93e991f4b12e4015cde7d604e6d5ee086e994a86e0556094`  
		Last Modified: Sat, 06 Mar 2021 01:51:46 GMT  
		Size: 5.2 MB (5170586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:54818a8a35d4a6a4e9efd14ee26c405e9aff90c33b6d5ddd815ff4b4410dad8b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107155482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be925e76dc6a703aa26d065b798d75738366f16d758e6d881239034e4ebc3ac`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:30:32 GMT
RUN cmd /S /C #(nop) COPY file:189ca6af047e9f9cf54ab2176b48588e01c7497fe0b5b0d7b2614ebad66ed089 in C:\nats-streaming-server.exe 
# Wed, 14 Apr 2021 20:30:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:30:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:30:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8f5e1772f13f9dbd7806652f582319d4c94b5e221ddca9bdd7a9a08472b446`  
		Last Modified: Wed, 14 Apr 2021 20:35:48 GMT  
		Size: 5.8 MB (5810702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45528fb53c9d98e2841a65b4761f5e3e524204d43fa18f0f4e5bf517a6fd003`  
		Last Modified: Wed, 14 Apr 2021 20:35:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2de582a0cd8ce6292e31cfe6870e1766cf4ce33b53febbf987b8210419f90d0`  
		Last Modified: Wed, 14 Apr 2021 20:35:48 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a29154792d4c050924f398e1e63281f55a67fd9d0393fb45d94b0613d10302e`  
		Last Modified: Wed, 14 Apr 2021 20:35:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:26603f9112b727df8e9736407a1ec1ab031317a9f6964ba0d407baea6b8d152c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:aa6af76760541ce71d366ac25554ad7caa95aea8cd230dd2688fd76b0645b329
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31671965fc8e3e2d623279516e43fd9d1a5d8d82a19fe709c69d7bfe7ac50085`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 07:43:28 GMT
COPY file:2c21a07cd43acfd157f86c6cf727430cf07e201a3bf3668b2083f473385db991 in /nats-streaming-server 
# Sat, 06 Mar 2021 07:43:28 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 07:43:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 07:43:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6f1c3ed40f752c2108b0e5d9224fba83d5045dac3370f93a50d91af0bc201c05`  
		Last Modified: Sat, 06 Mar 2021 07:44:17 GMT  
		Size: 5.7 MB (5680474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:907a450228b0d46339c5af803a9475165f7cfd9d20d5e09e8f66f9d048d1f7b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c6d73cc983f6821e57de28a32cec901f28d3c5ada68aa9e71a1880962a9f07`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 02:10:29 GMT
COPY file:bd617234b457ddee67b99f0e411029c6d5badad5059fbd81239c0acfe92cd4b7 in /nats-streaming-server 
# Sat, 06 Mar 2021 02:10:30 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 02:10:31 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 02:10:31 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ef1f32aa7a9ce9c8d42c909d32f61dabfa957c0b6a2b3590cd5e5847fb634355`  
		Last Modified: Sat, 06 Mar 2021 02:11:15 GMT  
		Size: 5.3 MB (5252895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ae774aee41bd64306207d739d2290639f673c9c66c367a83f155a923fe8c13f6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce52186dd957f6b70b086fdcbc8212e079e5ed5e3e0013f8f72b3922535a56e`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 01:00:25 GMT
COPY file:546c18b3e8e91d453d1a325c6e4dbc3c945564c010676da1abe89a653a0dea84 in /nats-streaming-server 
# Sat, 06 Mar 2021 01:00:27 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:00:28 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 01:00:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ed8ed2aa5d978cf51ebe3454de1832aeb40919052c5cb17d5b63865c31fc03c7`  
		Last Modified: Sat, 06 Mar 2021 01:01:07 GMT  
		Size: 5.2 MB (5246286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:7fccb492771f9c26f12f03c49e84ba4fb4d7004c6d142f4a7b83337d92feda95
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e817dd7b95371ae514afe3154e4aeba302d94dbed618a0aba7ece8696c13c6`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 01:51:04 GMT
COPY file:ed938be8d92952afe74223a94317bf582d9bcf2c458a54733da01a37a65d421b in /nats-streaming-server 
# Sat, 06 Mar 2021 01:51:05 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:51:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 01:51:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f5ab53e298c8bd7b93e991f4b12e4015cde7d604e6d5ee086e994a86e0556094`  
		Last Modified: Sat, 06 Mar 2021 01:51:46 GMT  
		Size: 5.2 MB (5170586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:95bc515e031c568aebd0e0579c3247df2a2e0affdfc8edb253fa5f85c496d551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:54818a8a35d4a6a4e9efd14ee26c405e9aff90c33b6d5ddd815ff4b4410dad8b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107155482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be925e76dc6a703aa26d065b798d75738366f16d758e6d881239034e4ebc3ac`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:30:32 GMT
RUN cmd /S /C #(nop) COPY file:189ca6af047e9f9cf54ab2176b48588e01c7497fe0b5b0d7b2614ebad66ed089 in C:\nats-streaming-server.exe 
# Wed, 14 Apr 2021 20:30:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:30:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:30:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8f5e1772f13f9dbd7806652f582319d4c94b5e221ddca9bdd7a9a08472b446`  
		Last Modified: Wed, 14 Apr 2021 20:35:48 GMT  
		Size: 5.8 MB (5810702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45528fb53c9d98e2841a65b4761f5e3e524204d43fa18f0f4e5bf517a6fd003`  
		Last Modified: Wed, 14 Apr 2021 20:35:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2de582a0cd8ce6292e31cfe6870e1766cf4ce33b53febbf987b8210419f90d0`  
		Last Modified: Wed, 14 Apr 2021 20:35:48 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a29154792d4c050924f398e1e63281f55a67fd9d0393fb45d94b0613d10302e`  
		Last Modified: Wed, 14 Apr 2021 20:35:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:95bc515e031c568aebd0e0579c3247df2a2e0affdfc8edb253fa5f85c496d551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:54818a8a35d4a6a4e9efd14ee26c405e9aff90c33b6d5ddd815ff4b4410dad8b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107155482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be925e76dc6a703aa26d065b798d75738366f16d758e6d881239034e4ebc3ac`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:30:32 GMT
RUN cmd /S /C #(nop) COPY file:189ca6af047e9f9cf54ab2176b48588e01c7497fe0b5b0d7b2614ebad66ed089 in C:\nats-streaming-server.exe 
# Wed, 14 Apr 2021 20:30:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:30:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:30:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8f5e1772f13f9dbd7806652f582319d4c94b5e221ddca9bdd7a9a08472b446`  
		Last Modified: Wed, 14 Apr 2021 20:35:48 GMT  
		Size: 5.8 MB (5810702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45528fb53c9d98e2841a65b4761f5e3e524204d43fa18f0f4e5bf517a6fd003`  
		Last Modified: Wed, 14 Apr 2021 20:35:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2de582a0cd8ce6292e31cfe6870e1766cf4ce33b53febbf987b8210419f90d0`  
		Last Modified: Wed, 14 Apr 2021 20:35:48 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a29154792d4c050924f398e1e63281f55a67fd9d0393fb45d94b0613d10302e`  
		Last Modified: Wed, 14 Apr 2021 20:35:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:26603f9112b727df8e9736407a1ec1ab031317a9f6964ba0d407baea6b8d152c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:aa6af76760541ce71d366ac25554ad7caa95aea8cd230dd2688fd76b0645b329
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31671965fc8e3e2d623279516e43fd9d1a5d8d82a19fe709c69d7bfe7ac50085`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 07:43:28 GMT
COPY file:2c21a07cd43acfd157f86c6cf727430cf07e201a3bf3668b2083f473385db991 in /nats-streaming-server 
# Sat, 06 Mar 2021 07:43:28 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 07:43:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 07:43:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6f1c3ed40f752c2108b0e5d9224fba83d5045dac3370f93a50d91af0bc201c05`  
		Last Modified: Sat, 06 Mar 2021 07:44:17 GMT  
		Size: 5.7 MB (5680474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:907a450228b0d46339c5af803a9475165f7cfd9d20d5e09e8f66f9d048d1f7b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c6d73cc983f6821e57de28a32cec901f28d3c5ada68aa9e71a1880962a9f07`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 02:10:29 GMT
COPY file:bd617234b457ddee67b99f0e411029c6d5badad5059fbd81239c0acfe92cd4b7 in /nats-streaming-server 
# Sat, 06 Mar 2021 02:10:30 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 02:10:31 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 02:10:31 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ef1f32aa7a9ce9c8d42c909d32f61dabfa957c0b6a2b3590cd5e5847fb634355`  
		Last Modified: Sat, 06 Mar 2021 02:11:15 GMT  
		Size: 5.3 MB (5252895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ae774aee41bd64306207d739d2290639f673c9c66c367a83f155a923fe8c13f6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce52186dd957f6b70b086fdcbc8212e079e5ed5e3e0013f8f72b3922535a56e`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 01:00:25 GMT
COPY file:546c18b3e8e91d453d1a325c6e4dbc3c945564c010676da1abe89a653a0dea84 in /nats-streaming-server 
# Sat, 06 Mar 2021 01:00:27 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:00:28 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 01:00:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ed8ed2aa5d978cf51ebe3454de1832aeb40919052c5cb17d5b63865c31fc03c7`  
		Last Modified: Sat, 06 Mar 2021 01:01:07 GMT  
		Size: 5.2 MB (5246286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:7fccb492771f9c26f12f03c49e84ba4fb4d7004c6d142f4a7b83337d92feda95
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e817dd7b95371ae514afe3154e4aeba302d94dbed618a0aba7ece8696c13c6`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 06 Mar 2021 01:51:04 GMT
COPY file:ed938be8d92952afe74223a94317bf582d9bcf2c458a54733da01a37a65d421b in /nats-streaming-server 
# Sat, 06 Mar 2021 01:51:05 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:51:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 06 Mar 2021 01:51:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f5ab53e298c8bd7b93e991f4b12e4015cde7d604e6d5ee086e994a86e0556094`  
		Last Modified: Sat, 06 Mar 2021 01:51:46 GMT  
		Size: 5.2 MB (5170586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:a8102f4b4b7a4dd707584cb4127c67087e63f8b5bb46b66e8bcd6dc8565c6258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:d9b88aa3a330b3290906f99e7d6ecd15ca2a2e1d3971b9d9289b93d30c3cd169
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2485693134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edccba0ec32510e9cbd95e6fb54bc1cce5ffcda21318e14b15aef92d30b968a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 13:10:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Apr 2021 16:02:50 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:27:47 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:27:48 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Wed, 14 Apr 2021 20:27:49 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Wed, 14 Apr 2021 20:28:31 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 20:30:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 20:30:14 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:30:15 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:30:16 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2159a5d0f75ce11e6fe71e4260ede5c3c88a9eb76a0ff43ac6746b2b9b96775`  
		Last Modified: Wed, 14 Apr 2021 15:37:10 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e849354f21f856ec720d6daecc37978fd7246f376ba3c32fd63d4400cce357bc`  
		Last Modified: Wed, 14 Apr 2021 16:10:16 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117282a30c6a3fbb982bd59e09a51b1fef503b2c8b179319ba79482e99fe384e`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496226fe152ceeff1fa0f62ca2d7b6bc19faa001434219174ae46a5fd50a5062`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d2433ca3469117417315b440945cb8cd6772eb21571dd4179873e007da1d89`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939e907443a80f726b409bd6af9aac2d7d95ea075599cf36b47c67d96db68e5b`  
		Last Modified: Wed, 14 Apr 2021 20:35:33 GMT  
		Size: 5.1 MB (5072715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36493380d982f607672d92b042f6a6fba85e6c73a2514659ab314414e1e03ce5`  
		Last Modified: Wed, 14 Apr 2021 20:35:31 GMT  
		Size: 10.9 MB (10855200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c00d72188f4d2c91bcd99fcff6f8aaa8ecbddaf6e31490f52ea27ffa361240b`  
		Last Modified: Wed, 14 Apr 2021 20:35:27 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c24f1b01b5e8513e9c865e784023d71e169853d5b5d84d09f32a4ad347d6633`  
		Last Modified: Wed, 14 Apr 2021 20:35:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d461ef53125c21684fd7078f19d920864bc170e1419530a9799d4c4637f57e6c`  
		Last Modified: Wed, 14 Apr 2021 20:35:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull nats-streaming@sha256:fb1d8548b281cb5116d343ca84eeeb7b3b384ea4fbad8e15050fa042425a55e3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816454011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f2cd68f941eba9047e18e03d45bc6ad435c2f87e4374be7184090e2822cc37`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 13:22:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Apr 2021 16:05:33 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:30:43 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:30:45 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Wed, 14 Apr 2021 20:30:46 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Wed, 14 Apr 2021 20:32:29 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 20:34:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 20:34:43 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:34:44 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:34:46 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f616bb7876e6f944d82fa1802ffab5ca4931a63e1b999f0851b52120cda83539`  
		Last Modified: Wed, 14 Apr 2021 15:37:43 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfa54f43457753c391f21da5e9a5bf47c61c574c0da04b8614d0e84bf823f54`  
		Last Modified: Wed, 14 Apr 2021 16:11:03 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d8948e6263c2bac7f73817369684ee9ce80dcea983d2da7c4d7be9fa1b92da`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a701af2866e93c3ecf557b60b96c4c01276eb2e524382b5ad189843adbf3355`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fc8f88f56d9ac579fa5db162a04bdd9d01802dd45c4f75577dae3515349334`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff9002a73083bb7987c2c033559072c3803ffb30b5df7ec99d7236e718ac397`  
		Last Modified: Wed, 14 Apr 2021 20:36:04 GMT  
		Size: 5.6 MB (5646320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4a7bb20d404a5bac7e79831b31797bd1a2dbf58ab157ff26fafe63e748966e`  
		Last Modified: Wed, 14 Apr 2021 20:36:07 GMT  
		Size: 15.9 MB (15912932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ceea9dc7862bc910070631046bb01d0159fcd3afa884d913477ddea2ae4ef9`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e773fcabbbc441abd5c250e3169866ae46ab83e23543816209ecb0e60e0f60`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23273c3337d46e183210a490996b4c40d280c0fbeae6ad837f0be19167750c38`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:f7a8702b4cb6a52239985459aed34c3aede42735cd7c155284a82d0bea7b46c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:d9b88aa3a330b3290906f99e7d6ecd15ca2a2e1d3971b9d9289b93d30c3cd169
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2485693134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edccba0ec32510e9cbd95e6fb54bc1cce5ffcda21318e14b15aef92d30b968a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 13:10:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Apr 2021 16:02:50 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:27:47 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:27:48 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Wed, 14 Apr 2021 20:27:49 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Wed, 14 Apr 2021 20:28:31 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 20:30:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 20:30:14 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:30:15 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:30:16 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2159a5d0f75ce11e6fe71e4260ede5c3c88a9eb76a0ff43ac6746b2b9b96775`  
		Last Modified: Wed, 14 Apr 2021 15:37:10 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e849354f21f856ec720d6daecc37978fd7246f376ba3c32fd63d4400cce357bc`  
		Last Modified: Wed, 14 Apr 2021 16:10:16 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117282a30c6a3fbb982bd59e09a51b1fef503b2c8b179319ba79482e99fe384e`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496226fe152ceeff1fa0f62ca2d7b6bc19faa001434219174ae46a5fd50a5062`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d2433ca3469117417315b440945cb8cd6772eb21571dd4179873e007da1d89`  
		Last Modified: Wed, 14 Apr 2021 20:35:30 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939e907443a80f726b409bd6af9aac2d7d95ea075599cf36b47c67d96db68e5b`  
		Last Modified: Wed, 14 Apr 2021 20:35:33 GMT  
		Size: 5.1 MB (5072715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36493380d982f607672d92b042f6a6fba85e6c73a2514659ab314414e1e03ce5`  
		Last Modified: Wed, 14 Apr 2021 20:35:31 GMT  
		Size: 10.9 MB (10855200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c00d72188f4d2c91bcd99fcff6f8aaa8ecbddaf6e31490f52ea27ffa361240b`  
		Last Modified: Wed, 14 Apr 2021 20:35:27 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c24f1b01b5e8513e9c865e784023d71e169853d5b5d84d09f32a4ad347d6633`  
		Last Modified: Wed, 14 Apr 2021 20:35:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d461ef53125c21684fd7078f19d920864bc170e1419530a9799d4c4637f57e6c`  
		Last Modified: Wed, 14 Apr 2021 20:35:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:0afaed268a1479f457d93dd9f8ec62024648ddba56bf49509b2a0de1523bf29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `nats-streaming:windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull nats-streaming@sha256:fb1d8548b281cb5116d343ca84eeeb7b3b384ea4fbad8e15050fa042425a55e3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816454011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f2cd68f941eba9047e18e03d45bc6ad435c2f87e4374be7184090e2822cc37`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 13:22:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Apr 2021 16:05:33 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 20:30:43 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Wed, 14 Apr 2021 20:30:45 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Wed, 14 Apr 2021 20:30:46 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Wed, 14 Apr 2021 20:32:29 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 20:34:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 20:34:43 GMT
EXPOSE 4222 8222
# Wed, 14 Apr 2021 20:34:44 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Apr 2021 20:34:46 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f616bb7876e6f944d82fa1802ffab5ca4931a63e1b999f0851b52120cda83539`  
		Last Modified: Wed, 14 Apr 2021 15:37:43 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfa54f43457753c391f21da5e9a5bf47c61c574c0da04b8614d0e84bf823f54`  
		Last Modified: Wed, 14 Apr 2021 16:11:03 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d8948e6263c2bac7f73817369684ee9ce80dcea983d2da7c4d7be9fa1b92da`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a701af2866e93c3ecf557b60b96c4c01276eb2e524382b5ad189843adbf3355`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fc8f88f56d9ac579fa5db162a04bdd9d01802dd45c4f75577dae3515349334`  
		Last Modified: Wed, 14 Apr 2021 20:36:05 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff9002a73083bb7987c2c033559072c3803ffb30b5df7ec99d7236e718ac397`  
		Last Modified: Wed, 14 Apr 2021 20:36:04 GMT  
		Size: 5.6 MB (5646320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4a7bb20d404a5bac7e79831b31797bd1a2dbf58ab157ff26fafe63e748966e`  
		Last Modified: Wed, 14 Apr 2021 20:36:07 GMT  
		Size: 15.9 MB (15912932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ceea9dc7862bc910070631046bb01d0159fcd3afa884d913477ddea2ae4ef9`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e773fcabbbc441abd5c250e3169866ae46ab83e23543816209ecb0e60e0f60`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23273c3337d46e183210a490996b4c40d280c0fbeae6ad837f0be19167750c38`  
		Last Modified: Wed, 14 Apr 2021 20:36:02 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

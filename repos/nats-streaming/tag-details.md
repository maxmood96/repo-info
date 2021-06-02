<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats-streaming`

-	[`nats-streaming:0.22`](#nats-streaming022)
-	[`nats-streaming:0.22-alpine`](#nats-streaming022-alpine)
-	[`nats-streaming:0.22-alpine3.13`](#nats-streaming022-alpine313)
-	[`nats-streaming:0.22-linux`](#nats-streaming022-linux)
-	[`nats-streaming:0.22-nanoserver`](#nats-streaming022-nanoserver)
-	[`nats-streaming:0.22-nanoserver-1809`](#nats-streaming022-nanoserver-1809)
-	[`nats-streaming:0.22-scratch`](#nats-streaming022-scratch)
-	[`nats-streaming:0.22-windowsservercore`](#nats-streaming022-windowsservercore)
-	[`nats-streaming:0.22-windowsservercore-1809`](#nats-streaming022-windowsservercore-1809)
-	[`nats-streaming:0.22-windowsservercore-ltsc2016`](#nats-streaming022-windowsservercore-ltsc2016)
-	[`nats-streaming:0.22.0`](#nats-streaming0220)
-	[`nats-streaming:0.22.0-alpine`](#nats-streaming0220-alpine)
-	[`nats-streaming:0.22.0-alpine3.13`](#nats-streaming0220-alpine313)
-	[`nats-streaming:0.22.0-linux`](#nats-streaming0220-linux)
-	[`nats-streaming:0.22.0-nanoserver`](#nats-streaming0220-nanoserver)
-	[`nats-streaming:0.22.0-nanoserver-1809`](#nats-streaming0220-nanoserver-1809)
-	[`nats-streaming:0.22.0-scratch`](#nats-streaming0220-scratch)
-	[`nats-streaming:0.22.0-windowsservercore`](#nats-streaming0220-windowsservercore)
-	[`nats-streaming:0.22.0-windowsservercore-1809`](#nats-streaming0220-windowsservercore-1809)
-	[`nats-streaming:0.22.0-windowsservercore-ltsc2016`](#nats-streaming0220-windowsservercore-ltsc2016)
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

## `nats-streaming:0.22`

```console
$ docker pull nats-streaming@sha256:bb7c4ca662ac7492f39584811919d6e9d3a1377df2ec02ddd09ca6ba8979baf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1935; amd64

### `nats-streaming:0.22` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ba1be2cd913a1e9f1ffc9445e5c04c169db333819beb7204deb3bc7c29fde5a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6800613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f2d32e0c9a23e5a9a5cb19c8b1404a9cc7af17915e33eabb71e55767848df7`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 05:47:24 GMT
COPY file:bbdef008b65f574a4e4593641e45dd6cdff5e8261d06d8f3959963f686dcdb78 in /nats-streaming-server 
# Wed, 02 Jun 2021 05:47:24 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 05:47:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 05:47:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:afa0998a9989cfec22c4ad772da3ca685ea7ccf963253ff9c27edf33a00d49c6`  
		Last Modified: Wed, 02 Jun 2021 05:48:07 GMT  
		Size: 6.8 MB (6800613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:1bef88847972d6206955fdc84742cb2505dcdf9ec86c2ef8bd6b5629c88ef2f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6269700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258e5207bc79452baf170c0dc0a5c955f71c72fadc9fff82bffecc06eb3e1e81`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 01 Jun 2021 23:54:46 GMT
COPY file:a4f69de3d07c6870dde4796b4de69a931a699d7e5b6ec30b2f25f6a23d66cb33 in /nats-streaming-server 
# Tue, 01 Jun 2021 23:54:47 GMT
EXPOSE 4222 8222
# Tue, 01 Jun 2021 23:54:47 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 01 Jun 2021 23:54:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8ab135edb380ca588ed7d11dbea1418006a6708ae7ae5effad8d86bcef90198e`  
		Last Modified: Tue, 01 Jun 2021 23:56:26 GMT  
		Size: 6.3 MB (6269700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:a6c122176a5ff4bdae9a653ebb1cf3e0672cd240250547b855ae0f8894496225
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6259769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccaf377f82ea563a543d1a8bcf9a53870f6427a0cacae9f9ad5e46e6c7eabff`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 03:13:19 GMT
COPY file:6e08520addf5d0c5d064e431d76487779d8fd8f4c03f71a72dc4e2c81812a922 in /nats-streaming-server 
# Wed, 02 Jun 2021 03:13:20 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 03:13:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 03:13:20 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:887fd90bbdf32bb85ec9e85b63e60eccca791d6c882e30de0c10e6e583ccbb65`  
		Last Modified: Wed, 02 Jun 2021 03:15:02 GMT  
		Size: 6.3 MB (6259769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bd5a415582b3f1d079d6498c12ea9138d7bde01dcd3a5f5a35a1731edf4c889f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6197708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d36744f70db176ba94e376a65c5edda55a7167035e7dffdf217e594c1ac283`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 02:14:00 GMT
COPY file:ef2047bb70888b72ef213e68689b3b8ae622cc597cd07b313c26b278418788bd in /nats-streaming-server 
# Wed, 02 Jun 2021 02:14:00 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 02:14:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 02:14:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ddf987a265c2be80179a2683a2d725f5a7e9fb477bc5752443a6d955be681a50`  
		Last Modified: Wed, 02 Jun 2021 02:15:07 GMT  
		Size: 6.2 MB (6197708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22` - windows version 10.0.17763.1935; amd64

```console
$ docker pull nats-streaming@sha256:f14d95a507285f7b6dac026a6d8f37deea8dd96b64f80602e388b3696f7cba25
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108314029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c511c19c4f82a1f431dc21df9c7ecf63522fff783e081e96479e17ad9dc77d6c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 May 2021 11:54:57 GMT
RUN Apply image 1809-amd64
# Wed, 12 May 2021 15:44:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:17:51 GMT
RUN cmd /S /C #(nop) COPY file:72a29a3f2d4a0bd237295ad8b2a317a32c76cbb8a1af898a564024d5013c0475 in C:\nats-streaming-server.exe 
# Wed, 02 Jun 2021 00:17:52 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:17:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:17:54 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b9043d31610e0dfa43b1afe286f8918b6e3bf69ece50f44424b29d48f20aa662`  
		Size: 101.4 MB (101375240 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95b58e21e5cdf4e2f9e5c87487734458885da325634d72f9c4e6583b353af06f`  
		Last Modified: Wed, 12 May 2021 15:49:02 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64768458156c8207b96c2a86ad6a981088c4a7f3e2d4678bc1c62a9f4e6fdc6`  
		Last Modified: Wed, 02 Jun 2021 00:22:54 GMT  
		Size: 6.9 MB (6934146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f298c3fb0faca6834b234589beddaa038a32c7a62ed70ad82b916372f0c88af`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e5c68c5466b75473483ef53e38622b28cb869445a4073ce864f39d9bb08284`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d375f4a29f433bf0c21962820308e15313a81506ef594ed0ff2c5bd73c0b33`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22-alpine`

```console
$ docker pull nats-streaming@sha256:e5497622caf68a352e1c334082035baa46d1739664b4ebcc86257ce2505e34e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.22-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:25457c5b382da1fb7ab66c4f977ad38915b109e9bf0d4440f2ae2f314d3bcc97
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9894969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443be2e221357fdae9e3405207feb4e1f061dce181882a1cf208543e029bc8fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 02 Jun 2021 05:47:13 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 05:47:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 02 Jun 2021 05:47:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 02 Jun 2021 05:47:16 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 05:47:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 05:47:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4795908dc4759b01d3e4dd956343fb777c34c32afc57d2a4a96014fa67a41206`  
		Last Modified: Wed, 02 Jun 2021 05:47:46 GMT  
		Size: 7.1 MB (7082579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf7f8694c616cf8f24559388ba77e2349a8da60a47001bfd26c85997d87b593`  
		Last Modified: Wed, 02 Jun 2021 05:47:45 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:8f5fec9c3508cacdf96a48dccfda3cb07ba922cc31faefcd9b82981ece64b14c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9175700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6654e93452d6f1e430cf9500177e35f139504b0058910421ad055b18d8bb2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Tue, 01 Jun 2021 23:54:27 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Tue, 01 Jun 2021 23:54:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 01 Jun 2021 23:54:31 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 01 Jun 2021 23:54:32 GMT
EXPOSE 4222 8222
# Tue, 01 Jun 2021 23:54:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jun 2021 23:54:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef7b36a5eb9baa587c0c795817923d783258f4ec2d50d157bc548fb861282c6`  
		Last Modified: Tue, 01 Jun 2021 23:55:55 GMT  
		Size: 6.6 MB (6553148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02404618fe373dc7f314135fe9ad25f49fe83b972a776fda8ef5562833d9b7fd`  
		Last Modified: Tue, 01 Jun 2021 23:55:53 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:094bdcea75742a31480bd4f5771f741f7490f46a7bade1b1e6836fc2ab0e14f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8967137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a7379dc428ab28ff200036e6f1a917c42724a035ffc0d548ecb01f9954593f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 02 Jun 2021 03:12:59 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 03:13:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 02 Jun 2021 03:13:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 02 Jun 2021 03:13:03 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 03:13:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 03:13:03 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcef365af48832fc326fce4ba5cec1feba2d3830122e812be8f7c68c4eba747b`  
		Last Modified: Wed, 02 Jun 2021 03:14:30 GMT  
		Size: 6.5 MB (6542570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773ab986cb0c82686f2f65fa84b5189bb9194ebe32dc1d4f734e8842539f05fc`  
		Last Modified: Wed, 02 Jun 2021 03:14:29 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:5eb6c5b61d4dbeb7672f8406165f20b9b1d7d4a0395afcf2d269111da790ce77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9192667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed6553f1ac545332570e83b8471deeb88f40974893612e479ac4e77aef1ceb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 02 Jun 2021 02:13:47 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 02:13:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 02 Jun 2021 02:13:50 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 02 Jun 2021 02:13:50 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 02:13:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 02:13:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad47f4d7a28ba6697d6f539329857f5249ee98701b1cff717964bc6cfe759973`  
		Last Modified: Wed, 02 Jun 2021 02:14:42 GMT  
		Size: 6.5 MB (6480219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1643b8a109e099ee5ee16cef792deb5613b1cb5f18472c0a9d8a66004a5eb7`  
		Last Modified: Wed, 02 Jun 2021 02:14:41 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22-alpine3.13`

```console
$ docker pull nats-streaming@sha256:e5497622caf68a352e1c334082035baa46d1739664b4ebcc86257ce2505e34e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.22-alpine3.13` - linux; amd64

```console
$ docker pull nats-streaming@sha256:25457c5b382da1fb7ab66c4f977ad38915b109e9bf0d4440f2ae2f314d3bcc97
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9894969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443be2e221357fdae9e3405207feb4e1f061dce181882a1cf208543e029bc8fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 02 Jun 2021 05:47:13 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 05:47:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 02 Jun 2021 05:47:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 02 Jun 2021 05:47:16 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 05:47:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 05:47:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4795908dc4759b01d3e4dd956343fb777c34c32afc57d2a4a96014fa67a41206`  
		Last Modified: Wed, 02 Jun 2021 05:47:46 GMT  
		Size: 7.1 MB (7082579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf7f8694c616cf8f24559388ba77e2349a8da60a47001bfd26c85997d87b593`  
		Last Modified: Wed, 02 Jun 2021 05:47:45 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22-alpine3.13` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:8f5fec9c3508cacdf96a48dccfda3cb07ba922cc31faefcd9b82981ece64b14c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9175700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6654e93452d6f1e430cf9500177e35f139504b0058910421ad055b18d8bb2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Tue, 01 Jun 2021 23:54:27 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Tue, 01 Jun 2021 23:54:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 01 Jun 2021 23:54:31 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 01 Jun 2021 23:54:32 GMT
EXPOSE 4222 8222
# Tue, 01 Jun 2021 23:54:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jun 2021 23:54:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef7b36a5eb9baa587c0c795817923d783258f4ec2d50d157bc548fb861282c6`  
		Last Modified: Tue, 01 Jun 2021 23:55:55 GMT  
		Size: 6.6 MB (6553148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02404618fe373dc7f314135fe9ad25f49fe83b972a776fda8ef5562833d9b7fd`  
		Last Modified: Tue, 01 Jun 2021 23:55:53 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22-alpine3.13` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:094bdcea75742a31480bd4f5771f741f7490f46a7bade1b1e6836fc2ab0e14f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8967137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a7379dc428ab28ff200036e6f1a917c42724a035ffc0d548ecb01f9954593f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 02 Jun 2021 03:12:59 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 03:13:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 02 Jun 2021 03:13:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 02 Jun 2021 03:13:03 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 03:13:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 03:13:03 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcef365af48832fc326fce4ba5cec1feba2d3830122e812be8f7c68c4eba747b`  
		Last Modified: Wed, 02 Jun 2021 03:14:30 GMT  
		Size: 6.5 MB (6542570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773ab986cb0c82686f2f65fa84b5189bb9194ebe32dc1d4f734e8842539f05fc`  
		Last Modified: Wed, 02 Jun 2021 03:14:29 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:5eb6c5b61d4dbeb7672f8406165f20b9b1d7d4a0395afcf2d269111da790ce77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9192667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed6553f1ac545332570e83b8471deeb88f40974893612e479ac4e77aef1ceb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 02 Jun 2021 02:13:47 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 02:13:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 02 Jun 2021 02:13:50 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 02 Jun 2021 02:13:50 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 02:13:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 02:13:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad47f4d7a28ba6697d6f539329857f5249ee98701b1cff717964bc6cfe759973`  
		Last Modified: Wed, 02 Jun 2021 02:14:42 GMT  
		Size: 6.5 MB (6480219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1643b8a109e099ee5ee16cef792deb5613b1cb5f18472c0a9d8a66004a5eb7`  
		Last Modified: Wed, 02 Jun 2021 02:14:41 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22-linux`

```console
$ docker pull nats-streaming@sha256:29a31360a13ce43c1a19b01d048213225f0ca3daaf0ac9f75e4ff9e21fcb656f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.22-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ba1be2cd913a1e9f1ffc9445e5c04c169db333819beb7204deb3bc7c29fde5a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6800613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f2d32e0c9a23e5a9a5cb19c8b1404a9cc7af17915e33eabb71e55767848df7`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 05:47:24 GMT
COPY file:bbdef008b65f574a4e4593641e45dd6cdff5e8261d06d8f3959963f686dcdb78 in /nats-streaming-server 
# Wed, 02 Jun 2021 05:47:24 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 05:47:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 05:47:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:afa0998a9989cfec22c4ad772da3ca685ea7ccf963253ff9c27edf33a00d49c6`  
		Last Modified: Wed, 02 Jun 2021 05:48:07 GMT  
		Size: 6.8 MB (6800613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:1bef88847972d6206955fdc84742cb2505dcdf9ec86c2ef8bd6b5629c88ef2f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6269700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258e5207bc79452baf170c0dc0a5c955f71c72fadc9fff82bffecc06eb3e1e81`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 01 Jun 2021 23:54:46 GMT
COPY file:a4f69de3d07c6870dde4796b4de69a931a699d7e5b6ec30b2f25f6a23d66cb33 in /nats-streaming-server 
# Tue, 01 Jun 2021 23:54:47 GMT
EXPOSE 4222 8222
# Tue, 01 Jun 2021 23:54:47 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 01 Jun 2021 23:54:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8ab135edb380ca588ed7d11dbea1418006a6708ae7ae5effad8d86bcef90198e`  
		Last Modified: Tue, 01 Jun 2021 23:56:26 GMT  
		Size: 6.3 MB (6269700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:a6c122176a5ff4bdae9a653ebb1cf3e0672cd240250547b855ae0f8894496225
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6259769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccaf377f82ea563a543d1a8bcf9a53870f6427a0cacae9f9ad5e46e6c7eabff`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 03:13:19 GMT
COPY file:6e08520addf5d0c5d064e431d76487779d8fd8f4c03f71a72dc4e2c81812a922 in /nats-streaming-server 
# Wed, 02 Jun 2021 03:13:20 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 03:13:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 03:13:20 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:887fd90bbdf32bb85ec9e85b63e60eccca791d6c882e30de0c10e6e583ccbb65`  
		Last Modified: Wed, 02 Jun 2021 03:15:02 GMT  
		Size: 6.3 MB (6259769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bd5a415582b3f1d079d6498c12ea9138d7bde01dcd3a5f5a35a1731edf4c889f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6197708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d36744f70db176ba94e376a65c5edda55a7167035e7dffdf217e594c1ac283`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 02:14:00 GMT
COPY file:ef2047bb70888b72ef213e68689b3b8ae622cc597cd07b313c26b278418788bd in /nats-streaming-server 
# Wed, 02 Jun 2021 02:14:00 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 02:14:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 02:14:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ddf987a265c2be80179a2683a2d725f5a7e9fb477bc5752443a6d955be681a50`  
		Last Modified: Wed, 02 Jun 2021 02:15:07 GMT  
		Size: 6.2 MB (6197708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22-nanoserver`

```console
$ docker pull nats-streaming@sha256:1dc0e94fc6d8cea9665e3cb1b7a07e9f0353f1fafa9f72295ce19916331997d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1935; amd64

### `nats-streaming:0.22-nanoserver` - windows version 10.0.17763.1935; amd64

```console
$ docker pull nats-streaming@sha256:f14d95a507285f7b6dac026a6d8f37deea8dd96b64f80602e388b3696f7cba25
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108314029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c511c19c4f82a1f431dc21df9c7ecf63522fff783e081e96479e17ad9dc77d6c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 May 2021 11:54:57 GMT
RUN Apply image 1809-amd64
# Wed, 12 May 2021 15:44:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:17:51 GMT
RUN cmd /S /C #(nop) COPY file:72a29a3f2d4a0bd237295ad8b2a317a32c76cbb8a1af898a564024d5013c0475 in C:\nats-streaming-server.exe 
# Wed, 02 Jun 2021 00:17:52 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:17:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:17:54 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b9043d31610e0dfa43b1afe286f8918b6e3bf69ece50f44424b29d48f20aa662`  
		Size: 101.4 MB (101375240 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95b58e21e5cdf4e2f9e5c87487734458885da325634d72f9c4e6583b353af06f`  
		Last Modified: Wed, 12 May 2021 15:49:02 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64768458156c8207b96c2a86ad6a981088c4a7f3e2d4678bc1c62a9f4e6fdc6`  
		Last Modified: Wed, 02 Jun 2021 00:22:54 GMT  
		Size: 6.9 MB (6934146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f298c3fb0faca6834b234589beddaa038a32c7a62ed70ad82b916372f0c88af`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e5c68c5466b75473483ef53e38622b28cb869445a4073ce864f39d9bb08284`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d375f4a29f433bf0c21962820308e15313a81506ef594ed0ff2c5bd73c0b33`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:1dc0e94fc6d8cea9665e3cb1b7a07e9f0353f1fafa9f72295ce19916331997d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1935; amd64

### `nats-streaming:0.22-nanoserver-1809` - windows version 10.0.17763.1935; amd64

```console
$ docker pull nats-streaming@sha256:f14d95a507285f7b6dac026a6d8f37deea8dd96b64f80602e388b3696f7cba25
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108314029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c511c19c4f82a1f431dc21df9c7ecf63522fff783e081e96479e17ad9dc77d6c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 May 2021 11:54:57 GMT
RUN Apply image 1809-amd64
# Wed, 12 May 2021 15:44:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:17:51 GMT
RUN cmd /S /C #(nop) COPY file:72a29a3f2d4a0bd237295ad8b2a317a32c76cbb8a1af898a564024d5013c0475 in C:\nats-streaming-server.exe 
# Wed, 02 Jun 2021 00:17:52 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:17:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:17:54 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b9043d31610e0dfa43b1afe286f8918b6e3bf69ece50f44424b29d48f20aa662`  
		Size: 101.4 MB (101375240 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95b58e21e5cdf4e2f9e5c87487734458885da325634d72f9c4e6583b353af06f`  
		Last Modified: Wed, 12 May 2021 15:49:02 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64768458156c8207b96c2a86ad6a981088c4a7f3e2d4678bc1c62a9f4e6fdc6`  
		Last Modified: Wed, 02 Jun 2021 00:22:54 GMT  
		Size: 6.9 MB (6934146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f298c3fb0faca6834b234589beddaa038a32c7a62ed70ad82b916372f0c88af`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e5c68c5466b75473483ef53e38622b28cb869445a4073ce864f39d9bb08284`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d375f4a29f433bf0c21962820308e15313a81506ef594ed0ff2c5bd73c0b33`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22-scratch`

```console
$ docker pull nats-streaming@sha256:29a31360a13ce43c1a19b01d048213225f0ca3daaf0ac9f75e4ff9e21fcb656f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.22-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ba1be2cd913a1e9f1ffc9445e5c04c169db333819beb7204deb3bc7c29fde5a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6800613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f2d32e0c9a23e5a9a5cb19c8b1404a9cc7af17915e33eabb71e55767848df7`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 05:47:24 GMT
COPY file:bbdef008b65f574a4e4593641e45dd6cdff5e8261d06d8f3959963f686dcdb78 in /nats-streaming-server 
# Wed, 02 Jun 2021 05:47:24 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 05:47:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 05:47:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:afa0998a9989cfec22c4ad772da3ca685ea7ccf963253ff9c27edf33a00d49c6`  
		Last Modified: Wed, 02 Jun 2021 05:48:07 GMT  
		Size: 6.8 MB (6800613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:1bef88847972d6206955fdc84742cb2505dcdf9ec86c2ef8bd6b5629c88ef2f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6269700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258e5207bc79452baf170c0dc0a5c955f71c72fadc9fff82bffecc06eb3e1e81`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 01 Jun 2021 23:54:46 GMT
COPY file:a4f69de3d07c6870dde4796b4de69a931a699d7e5b6ec30b2f25f6a23d66cb33 in /nats-streaming-server 
# Tue, 01 Jun 2021 23:54:47 GMT
EXPOSE 4222 8222
# Tue, 01 Jun 2021 23:54:47 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 01 Jun 2021 23:54:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8ab135edb380ca588ed7d11dbea1418006a6708ae7ae5effad8d86bcef90198e`  
		Last Modified: Tue, 01 Jun 2021 23:56:26 GMT  
		Size: 6.3 MB (6269700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:a6c122176a5ff4bdae9a653ebb1cf3e0672cd240250547b855ae0f8894496225
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6259769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccaf377f82ea563a543d1a8bcf9a53870f6427a0cacae9f9ad5e46e6c7eabff`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 03:13:19 GMT
COPY file:6e08520addf5d0c5d064e431d76487779d8fd8f4c03f71a72dc4e2c81812a922 in /nats-streaming-server 
# Wed, 02 Jun 2021 03:13:20 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 03:13:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 03:13:20 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:887fd90bbdf32bb85ec9e85b63e60eccca791d6c882e30de0c10e6e583ccbb65`  
		Last Modified: Wed, 02 Jun 2021 03:15:02 GMT  
		Size: 6.3 MB (6259769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bd5a415582b3f1d079d6498c12ea9138d7bde01dcd3a5f5a35a1731edf4c889f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6197708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d36744f70db176ba94e376a65c5edda55a7167035e7dffdf217e594c1ac283`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 02:14:00 GMT
COPY file:ef2047bb70888b72ef213e68689b3b8ae622cc597cd07b313c26b278418788bd in /nats-streaming-server 
# Wed, 02 Jun 2021 02:14:00 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 02:14:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 02:14:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ddf987a265c2be80179a2683a2d725f5a7e9fb477bc5752443a6d955be681a50`  
		Last Modified: Wed, 02 Jun 2021 02:15:07 GMT  
		Size: 6.2 MB (6197708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22-windowsservercore`

```console
$ docker pull nats-streaming@sha256:5fbee84f8c860aeec9fbdcc3133e17141649ee0baefa7bbfbd7148723e9e2912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1935; amd64
	-	windows version 10.0.14393.4402; amd64

### `nats-streaming:0.22-windowsservercore` - windows version 10.0.17763.1935; amd64

```console
$ docker pull nats-streaming@sha256:b4ef1c8cc8cd9078fb6754750750cad7a286844fe27d3fd1a0abbd5e2955d0a8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2491648944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5674c44573a2caccbd707fff099991bdbb2f9e9ec95be3b4a74e9e2bfe599197`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 08 May 2021 09:21:48 GMT
RUN Install update 1809-amd64
# Tue, 11 May 2021 23:54:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 May 2021 15:41:49 GMT
ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:15:23 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 00:15:24 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.22.0/nats-streaming-server-v0.22.0-windows-amd64.zip
# Wed, 02 Jun 2021 00:15:25 GMT
ENV GIT_DOWNLOAD_SHA256=436c16330efbd0767d9a69dcdf2d3badd4e2598fab23c4f4a192e9d9982c2c92
# Wed, 02 Jun 2021 00:16:08 GMT
RUN Set-PSDebug -Trace 2
# Wed, 02 Jun 2021 00:17:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 02 Jun 2021 00:17:40 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:17:41 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:17:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8116de3c91c3f1ef2d6c09b49ef5407c9b4d672896eb3af5182a997c3c5379c9`  
		Size: 756.2 MB (756156286 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c049a65ed9206719f5c04428cb853623400e8ab1668243872b1134775f752962`  
		Last Modified: Wed, 12 May 2021 00:41:58 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262d2305f11fe8f36ef3508b42686daac7e99da966ed02f4ded1927387b1b75b`  
		Last Modified: Wed, 12 May 2021 15:48:42 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24932ebb62fedf8bc966247332680ddb3a6793604c0ed8133db9e56b10333616`  
		Last Modified: Wed, 02 Jun 2021 00:22:35 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb436a7ae07957612fdf342254deba5631a36e070eff281192a9eac753cdc5f`  
		Last Modified: Wed, 02 Jun 2021 00:22:35 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:face841f208848bbb571c289ab673bbef75a4af464c1430ee20ef085563ffde7`  
		Last Modified: Wed, 02 Jun 2021 00:22:35 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb048e76e13a831ac87972c8bc1a28f8a94183505d50c49388e8414acc5eef08`  
		Last Modified: Wed, 02 Jun 2021 00:22:38 GMT  
		Size: 5.1 MB (5121106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64673f2be1fb01eaff52556ba05ce5242bf22987bfe1833a67c30942f1b5c201`  
		Last Modified: Wed, 02 Jun 2021 00:22:36 GMT  
		Size: 12.0 MB (12027291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1385b473d95e5015b5dfb3cee8ecc2e18fd698a628a816f749d8d33078bbda1a`  
		Last Modified: Wed, 02 Jun 2021 00:22:32 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad68fa43ed8fac2ccf3c70066b8b236c9d33b137dfaf7b1d7fcf589ecd3efde0`  
		Last Modified: Wed, 02 Jun 2021 00:22:32 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487c92830589b96248c25f62e361f55a630d1a2962964cf2191de4aaee556d78`  
		Last Modified: Wed, 02 Jun 2021 00:22:33 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22-windowsservercore` - windows version 10.0.14393.4402; amd64

```console
$ docker pull nats-streaming@sha256:4ec00239efea2ce9e8341045679e6a3e7c008bf54c1a2ed97ee48478a45be6ef
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818577847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ecc3bd85a796e373842d619a9259b900fa37a3c3507780f2c0e8d4fcd48d4e`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 26 Apr 2021 17:25:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 May 2021 23:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 May 2021 15:44:16 GMT
ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:18:02 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 00:18:03 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.22.0/nats-streaming-server-v0.22.0-windows-amd64.zip
# Wed, 02 Jun 2021 00:18:04 GMT
ENV GIT_DOWNLOAD_SHA256=436c16330efbd0767d9a69dcdf2d3badd4e2598fab23c4f4a192e9d9982c2c92
# Wed, 02 Jun 2021 00:19:38 GMT
RUN Set-PSDebug -Trace 2
# Wed, 02 Jun 2021 00:21:48 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 02 Jun 2021 00:21:49 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:21:50 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:21:51 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7f532f88613ca85064b055f6b93f8517bd05feba8fdce495a6ad1421573e765e`  
		Size: 1.7 GB (1725791397 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:50d0f4595a2bdc5dc0623fbee162be09d0631373eb9e82a0b1ec387ce1512c49`  
		Last Modified: Wed, 12 May 2021 00:46:32 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7998d92dbbcfc4e6dc106e75206a3cfde70fe601eb46b0515658f23dcd53ae`  
		Last Modified: Wed, 12 May 2021 15:49:26 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c54f8fb333eecc0b6838b82bdefec17dabd1e356ae640842f7d2623016bff34`  
		Last Modified: Wed, 02 Jun 2021 00:23:10 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caac90263041fd97d9787b47f96c2be639c606a1df8b7e779a6d159c2b51f080`  
		Last Modified: Wed, 02 Jun 2021 00:23:10 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543d9016ba1a5fbf9e855d8779b322554244ced48a97d1ea871faa720aa19cc4`  
		Last Modified: Wed, 02 Jun 2021 00:23:10 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b24da1a712f81c6fdd463b7e1d9e82ebf5a5d67320160da3e6e869675188e8`  
		Last Modified: Wed, 02 Jun 2021 00:23:08 GMT  
		Size: 5.7 MB (5700376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f1c189638ad48c571c54b98a6ac4de00054f1953a928836be2cbaccb4aa951`  
		Last Modified: Wed, 02 Jun 2021 00:23:11 GMT  
		Size: 17.1 MB (17088787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528e1a5b38c1b0120dfb058ce56e406344aef9df3953f2eb3f9fdb1e660b30eb`  
		Last Modified: Wed, 02 Jun 2021 00:23:06 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347dad5447a5c06c5d7e02f1d46766052ac70cc9196be60167d11fb944900088`  
		Last Modified: Wed, 02 Jun 2021 00:23:07 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32cce4e8dbbc2bb82c047ec6f45fc7221a29b36dcebae2ee53c6b17c24dfca2`  
		Last Modified: Wed, 02 Jun 2021 00:23:07 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:b9fde4c299c883fc1db3e776be8bd3006806bd0e69527271d2d8a1b38614ab9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1935; amd64

### `nats-streaming:0.22-windowsservercore-1809` - windows version 10.0.17763.1935; amd64

```console
$ docker pull nats-streaming@sha256:b4ef1c8cc8cd9078fb6754750750cad7a286844fe27d3fd1a0abbd5e2955d0a8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2491648944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5674c44573a2caccbd707fff099991bdbb2f9e9ec95be3b4a74e9e2bfe599197`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 08 May 2021 09:21:48 GMT
RUN Install update 1809-amd64
# Tue, 11 May 2021 23:54:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 May 2021 15:41:49 GMT
ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:15:23 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 00:15:24 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.22.0/nats-streaming-server-v0.22.0-windows-amd64.zip
# Wed, 02 Jun 2021 00:15:25 GMT
ENV GIT_DOWNLOAD_SHA256=436c16330efbd0767d9a69dcdf2d3badd4e2598fab23c4f4a192e9d9982c2c92
# Wed, 02 Jun 2021 00:16:08 GMT
RUN Set-PSDebug -Trace 2
# Wed, 02 Jun 2021 00:17:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 02 Jun 2021 00:17:40 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:17:41 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:17:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8116de3c91c3f1ef2d6c09b49ef5407c9b4d672896eb3af5182a997c3c5379c9`  
		Size: 756.2 MB (756156286 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c049a65ed9206719f5c04428cb853623400e8ab1668243872b1134775f752962`  
		Last Modified: Wed, 12 May 2021 00:41:58 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262d2305f11fe8f36ef3508b42686daac7e99da966ed02f4ded1927387b1b75b`  
		Last Modified: Wed, 12 May 2021 15:48:42 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24932ebb62fedf8bc966247332680ddb3a6793604c0ed8133db9e56b10333616`  
		Last Modified: Wed, 02 Jun 2021 00:22:35 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb436a7ae07957612fdf342254deba5631a36e070eff281192a9eac753cdc5f`  
		Last Modified: Wed, 02 Jun 2021 00:22:35 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:face841f208848bbb571c289ab673bbef75a4af464c1430ee20ef085563ffde7`  
		Last Modified: Wed, 02 Jun 2021 00:22:35 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb048e76e13a831ac87972c8bc1a28f8a94183505d50c49388e8414acc5eef08`  
		Last Modified: Wed, 02 Jun 2021 00:22:38 GMT  
		Size: 5.1 MB (5121106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64673f2be1fb01eaff52556ba05ce5242bf22987bfe1833a67c30942f1b5c201`  
		Last Modified: Wed, 02 Jun 2021 00:22:36 GMT  
		Size: 12.0 MB (12027291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1385b473d95e5015b5dfb3cee8ecc2e18fd698a628a816f749d8d33078bbda1a`  
		Last Modified: Wed, 02 Jun 2021 00:22:32 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad68fa43ed8fac2ccf3c70066b8b236c9d33b137dfaf7b1d7fcf589ecd3efde0`  
		Last Modified: Wed, 02 Jun 2021 00:22:32 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487c92830589b96248c25f62e361f55a630d1a2962964cf2191de4aaee556d78`  
		Last Modified: Wed, 02 Jun 2021 00:22:33 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22-windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:b388eabcc9ec2dafb5ba5344d26ec4177567009b06fac11bfbccb73a59329688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4402; amd64

### `nats-streaming:0.22-windowsservercore-ltsc2016` - windows version 10.0.14393.4402; amd64

```console
$ docker pull nats-streaming@sha256:4ec00239efea2ce9e8341045679e6a3e7c008bf54c1a2ed97ee48478a45be6ef
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818577847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ecc3bd85a796e373842d619a9259b900fa37a3c3507780f2c0e8d4fcd48d4e`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 26 Apr 2021 17:25:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 May 2021 23:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 May 2021 15:44:16 GMT
ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:18:02 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 00:18:03 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.22.0/nats-streaming-server-v0.22.0-windows-amd64.zip
# Wed, 02 Jun 2021 00:18:04 GMT
ENV GIT_DOWNLOAD_SHA256=436c16330efbd0767d9a69dcdf2d3badd4e2598fab23c4f4a192e9d9982c2c92
# Wed, 02 Jun 2021 00:19:38 GMT
RUN Set-PSDebug -Trace 2
# Wed, 02 Jun 2021 00:21:48 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 02 Jun 2021 00:21:49 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:21:50 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:21:51 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7f532f88613ca85064b055f6b93f8517bd05feba8fdce495a6ad1421573e765e`  
		Size: 1.7 GB (1725791397 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:50d0f4595a2bdc5dc0623fbee162be09d0631373eb9e82a0b1ec387ce1512c49`  
		Last Modified: Wed, 12 May 2021 00:46:32 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7998d92dbbcfc4e6dc106e75206a3cfde70fe601eb46b0515658f23dcd53ae`  
		Last Modified: Wed, 12 May 2021 15:49:26 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c54f8fb333eecc0b6838b82bdefec17dabd1e356ae640842f7d2623016bff34`  
		Last Modified: Wed, 02 Jun 2021 00:23:10 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caac90263041fd97d9787b47f96c2be639c606a1df8b7e779a6d159c2b51f080`  
		Last Modified: Wed, 02 Jun 2021 00:23:10 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543d9016ba1a5fbf9e855d8779b322554244ced48a97d1ea871faa720aa19cc4`  
		Last Modified: Wed, 02 Jun 2021 00:23:10 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b24da1a712f81c6fdd463b7e1d9e82ebf5a5d67320160da3e6e869675188e8`  
		Last Modified: Wed, 02 Jun 2021 00:23:08 GMT  
		Size: 5.7 MB (5700376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f1c189638ad48c571c54b98a6ac4de00054f1953a928836be2cbaccb4aa951`  
		Last Modified: Wed, 02 Jun 2021 00:23:11 GMT  
		Size: 17.1 MB (17088787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528e1a5b38c1b0120dfb058ce56e406344aef9df3953f2eb3f9fdb1e660b30eb`  
		Last Modified: Wed, 02 Jun 2021 00:23:06 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347dad5447a5c06c5d7e02f1d46766052ac70cc9196be60167d11fb944900088`  
		Last Modified: Wed, 02 Jun 2021 00:23:07 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32cce4e8dbbc2bb82c047ec6f45fc7221a29b36dcebae2ee53c6b17c24dfca2`  
		Last Modified: Wed, 02 Jun 2021 00:23:07 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22.0`

```console
$ docker pull nats-streaming@sha256:bb7c4ca662ac7492f39584811919d6e9d3a1377df2ec02ddd09ca6ba8979baf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1935; amd64

### `nats-streaming:0.22.0` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ba1be2cd913a1e9f1ffc9445e5c04c169db333819beb7204deb3bc7c29fde5a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6800613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f2d32e0c9a23e5a9a5cb19c8b1404a9cc7af17915e33eabb71e55767848df7`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 05:47:24 GMT
COPY file:bbdef008b65f574a4e4593641e45dd6cdff5e8261d06d8f3959963f686dcdb78 in /nats-streaming-server 
# Wed, 02 Jun 2021 05:47:24 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 05:47:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 05:47:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:afa0998a9989cfec22c4ad772da3ca685ea7ccf963253ff9c27edf33a00d49c6`  
		Last Modified: Wed, 02 Jun 2021 05:48:07 GMT  
		Size: 6.8 MB (6800613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22.0` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:1bef88847972d6206955fdc84742cb2505dcdf9ec86c2ef8bd6b5629c88ef2f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6269700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258e5207bc79452baf170c0dc0a5c955f71c72fadc9fff82bffecc06eb3e1e81`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 01 Jun 2021 23:54:46 GMT
COPY file:a4f69de3d07c6870dde4796b4de69a931a699d7e5b6ec30b2f25f6a23d66cb33 in /nats-streaming-server 
# Tue, 01 Jun 2021 23:54:47 GMT
EXPOSE 4222 8222
# Tue, 01 Jun 2021 23:54:47 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 01 Jun 2021 23:54:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8ab135edb380ca588ed7d11dbea1418006a6708ae7ae5effad8d86bcef90198e`  
		Last Modified: Tue, 01 Jun 2021 23:56:26 GMT  
		Size: 6.3 MB (6269700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22.0` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:a6c122176a5ff4bdae9a653ebb1cf3e0672cd240250547b855ae0f8894496225
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6259769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccaf377f82ea563a543d1a8bcf9a53870f6427a0cacae9f9ad5e46e6c7eabff`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 03:13:19 GMT
COPY file:6e08520addf5d0c5d064e431d76487779d8fd8f4c03f71a72dc4e2c81812a922 in /nats-streaming-server 
# Wed, 02 Jun 2021 03:13:20 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 03:13:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 03:13:20 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:887fd90bbdf32bb85ec9e85b63e60eccca791d6c882e30de0c10e6e583ccbb65`  
		Last Modified: Wed, 02 Jun 2021 03:15:02 GMT  
		Size: 6.3 MB (6259769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22.0` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bd5a415582b3f1d079d6498c12ea9138d7bde01dcd3a5f5a35a1731edf4c889f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6197708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d36744f70db176ba94e376a65c5edda55a7167035e7dffdf217e594c1ac283`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 02:14:00 GMT
COPY file:ef2047bb70888b72ef213e68689b3b8ae622cc597cd07b313c26b278418788bd in /nats-streaming-server 
# Wed, 02 Jun 2021 02:14:00 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 02:14:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 02:14:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ddf987a265c2be80179a2683a2d725f5a7e9fb477bc5752443a6d955be681a50`  
		Last Modified: Wed, 02 Jun 2021 02:15:07 GMT  
		Size: 6.2 MB (6197708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22.0` - windows version 10.0.17763.1935; amd64

```console
$ docker pull nats-streaming@sha256:f14d95a507285f7b6dac026a6d8f37deea8dd96b64f80602e388b3696f7cba25
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108314029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c511c19c4f82a1f431dc21df9c7ecf63522fff783e081e96479e17ad9dc77d6c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 May 2021 11:54:57 GMT
RUN Apply image 1809-amd64
# Wed, 12 May 2021 15:44:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:17:51 GMT
RUN cmd /S /C #(nop) COPY file:72a29a3f2d4a0bd237295ad8b2a317a32c76cbb8a1af898a564024d5013c0475 in C:\nats-streaming-server.exe 
# Wed, 02 Jun 2021 00:17:52 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:17:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:17:54 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b9043d31610e0dfa43b1afe286f8918b6e3bf69ece50f44424b29d48f20aa662`  
		Size: 101.4 MB (101375240 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95b58e21e5cdf4e2f9e5c87487734458885da325634d72f9c4e6583b353af06f`  
		Last Modified: Wed, 12 May 2021 15:49:02 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64768458156c8207b96c2a86ad6a981088c4a7f3e2d4678bc1c62a9f4e6fdc6`  
		Last Modified: Wed, 02 Jun 2021 00:22:54 GMT  
		Size: 6.9 MB (6934146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f298c3fb0faca6834b234589beddaa038a32c7a62ed70ad82b916372f0c88af`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e5c68c5466b75473483ef53e38622b28cb869445a4073ce864f39d9bb08284`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d375f4a29f433bf0c21962820308e15313a81506ef594ed0ff2c5bd73c0b33`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22.0-alpine`

```console
$ docker pull nats-streaming@sha256:e5497622caf68a352e1c334082035baa46d1739664b4ebcc86257ce2505e34e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.22.0-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:25457c5b382da1fb7ab66c4f977ad38915b109e9bf0d4440f2ae2f314d3bcc97
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9894969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443be2e221357fdae9e3405207feb4e1f061dce181882a1cf208543e029bc8fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 02 Jun 2021 05:47:13 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 05:47:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 02 Jun 2021 05:47:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 02 Jun 2021 05:47:16 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 05:47:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 05:47:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4795908dc4759b01d3e4dd956343fb777c34c32afc57d2a4a96014fa67a41206`  
		Last Modified: Wed, 02 Jun 2021 05:47:46 GMT  
		Size: 7.1 MB (7082579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf7f8694c616cf8f24559388ba77e2349a8da60a47001bfd26c85997d87b593`  
		Last Modified: Wed, 02 Jun 2021 05:47:45 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22.0-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:8f5fec9c3508cacdf96a48dccfda3cb07ba922cc31faefcd9b82981ece64b14c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9175700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6654e93452d6f1e430cf9500177e35f139504b0058910421ad055b18d8bb2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Tue, 01 Jun 2021 23:54:27 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Tue, 01 Jun 2021 23:54:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 01 Jun 2021 23:54:31 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 01 Jun 2021 23:54:32 GMT
EXPOSE 4222 8222
# Tue, 01 Jun 2021 23:54:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jun 2021 23:54:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef7b36a5eb9baa587c0c795817923d783258f4ec2d50d157bc548fb861282c6`  
		Last Modified: Tue, 01 Jun 2021 23:55:55 GMT  
		Size: 6.6 MB (6553148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02404618fe373dc7f314135fe9ad25f49fe83b972a776fda8ef5562833d9b7fd`  
		Last Modified: Tue, 01 Jun 2021 23:55:53 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22.0-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:094bdcea75742a31480bd4f5771f741f7490f46a7bade1b1e6836fc2ab0e14f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8967137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a7379dc428ab28ff200036e6f1a917c42724a035ffc0d548ecb01f9954593f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 02 Jun 2021 03:12:59 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 03:13:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 02 Jun 2021 03:13:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 02 Jun 2021 03:13:03 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 03:13:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 03:13:03 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcef365af48832fc326fce4ba5cec1feba2d3830122e812be8f7c68c4eba747b`  
		Last Modified: Wed, 02 Jun 2021 03:14:30 GMT  
		Size: 6.5 MB (6542570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773ab986cb0c82686f2f65fa84b5189bb9194ebe32dc1d4f734e8842539f05fc`  
		Last Modified: Wed, 02 Jun 2021 03:14:29 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22.0-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:5eb6c5b61d4dbeb7672f8406165f20b9b1d7d4a0395afcf2d269111da790ce77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9192667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed6553f1ac545332570e83b8471deeb88f40974893612e479ac4e77aef1ceb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 02 Jun 2021 02:13:47 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 02:13:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 02 Jun 2021 02:13:50 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 02 Jun 2021 02:13:50 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 02:13:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 02:13:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad47f4d7a28ba6697d6f539329857f5249ee98701b1cff717964bc6cfe759973`  
		Last Modified: Wed, 02 Jun 2021 02:14:42 GMT  
		Size: 6.5 MB (6480219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1643b8a109e099ee5ee16cef792deb5613b1cb5f18472c0a9d8a66004a5eb7`  
		Last Modified: Wed, 02 Jun 2021 02:14:41 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22.0-alpine3.13`

```console
$ docker pull nats-streaming@sha256:e5497622caf68a352e1c334082035baa46d1739664b4ebcc86257ce2505e34e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.22.0-alpine3.13` - linux; amd64

```console
$ docker pull nats-streaming@sha256:25457c5b382da1fb7ab66c4f977ad38915b109e9bf0d4440f2ae2f314d3bcc97
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9894969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443be2e221357fdae9e3405207feb4e1f061dce181882a1cf208543e029bc8fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 02 Jun 2021 05:47:13 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 05:47:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 02 Jun 2021 05:47:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 02 Jun 2021 05:47:16 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 05:47:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 05:47:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4795908dc4759b01d3e4dd956343fb777c34c32afc57d2a4a96014fa67a41206`  
		Last Modified: Wed, 02 Jun 2021 05:47:46 GMT  
		Size: 7.1 MB (7082579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf7f8694c616cf8f24559388ba77e2349a8da60a47001bfd26c85997d87b593`  
		Last Modified: Wed, 02 Jun 2021 05:47:45 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22.0-alpine3.13` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:8f5fec9c3508cacdf96a48dccfda3cb07ba922cc31faefcd9b82981ece64b14c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9175700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6654e93452d6f1e430cf9500177e35f139504b0058910421ad055b18d8bb2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Tue, 01 Jun 2021 23:54:27 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Tue, 01 Jun 2021 23:54:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 01 Jun 2021 23:54:31 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 01 Jun 2021 23:54:32 GMT
EXPOSE 4222 8222
# Tue, 01 Jun 2021 23:54:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jun 2021 23:54:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef7b36a5eb9baa587c0c795817923d783258f4ec2d50d157bc548fb861282c6`  
		Last Modified: Tue, 01 Jun 2021 23:55:55 GMT  
		Size: 6.6 MB (6553148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02404618fe373dc7f314135fe9ad25f49fe83b972a776fda8ef5562833d9b7fd`  
		Last Modified: Tue, 01 Jun 2021 23:55:53 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22.0-alpine3.13` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:094bdcea75742a31480bd4f5771f741f7490f46a7bade1b1e6836fc2ab0e14f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8967137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a7379dc428ab28ff200036e6f1a917c42724a035ffc0d548ecb01f9954593f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 02 Jun 2021 03:12:59 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 03:13:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 02 Jun 2021 03:13:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 02 Jun 2021 03:13:03 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 03:13:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 03:13:03 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcef365af48832fc326fce4ba5cec1feba2d3830122e812be8f7c68c4eba747b`  
		Last Modified: Wed, 02 Jun 2021 03:14:30 GMT  
		Size: 6.5 MB (6542570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773ab986cb0c82686f2f65fa84b5189bb9194ebe32dc1d4f734e8842539f05fc`  
		Last Modified: Wed, 02 Jun 2021 03:14:29 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22.0-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:5eb6c5b61d4dbeb7672f8406165f20b9b1d7d4a0395afcf2d269111da790ce77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9192667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed6553f1ac545332570e83b8471deeb88f40974893612e479ac4e77aef1ceb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 02 Jun 2021 02:13:47 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 02:13:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 02 Jun 2021 02:13:50 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 02 Jun 2021 02:13:50 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 02:13:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 02:13:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad47f4d7a28ba6697d6f539329857f5249ee98701b1cff717964bc6cfe759973`  
		Last Modified: Wed, 02 Jun 2021 02:14:42 GMT  
		Size: 6.5 MB (6480219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1643b8a109e099ee5ee16cef792deb5613b1cb5f18472c0a9d8a66004a5eb7`  
		Last Modified: Wed, 02 Jun 2021 02:14:41 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22.0-linux`

```console
$ docker pull nats-streaming@sha256:29a31360a13ce43c1a19b01d048213225f0ca3daaf0ac9f75e4ff9e21fcb656f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.22.0-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ba1be2cd913a1e9f1ffc9445e5c04c169db333819beb7204deb3bc7c29fde5a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6800613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f2d32e0c9a23e5a9a5cb19c8b1404a9cc7af17915e33eabb71e55767848df7`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 05:47:24 GMT
COPY file:bbdef008b65f574a4e4593641e45dd6cdff5e8261d06d8f3959963f686dcdb78 in /nats-streaming-server 
# Wed, 02 Jun 2021 05:47:24 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 05:47:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 05:47:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:afa0998a9989cfec22c4ad772da3ca685ea7ccf963253ff9c27edf33a00d49c6`  
		Last Modified: Wed, 02 Jun 2021 05:48:07 GMT  
		Size: 6.8 MB (6800613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22.0-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:1bef88847972d6206955fdc84742cb2505dcdf9ec86c2ef8bd6b5629c88ef2f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6269700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258e5207bc79452baf170c0dc0a5c955f71c72fadc9fff82bffecc06eb3e1e81`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 01 Jun 2021 23:54:46 GMT
COPY file:a4f69de3d07c6870dde4796b4de69a931a699d7e5b6ec30b2f25f6a23d66cb33 in /nats-streaming-server 
# Tue, 01 Jun 2021 23:54:47 GMT
EXPOSE 4222 8222
# Tue, 01 Jun 2021 23:54:47 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 01 Jun 2021 23:54:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8ab135edb380ca588ed7d11dbea1418006a6708ae7ae5effad8d86bcef90198e`  
		Last Modified: Tue, 01 Jun 2021 23:56:26 GMT  
		Size: 6.3 MB (6269700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22.0-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:a6c122176a5ff4bdae9a653ebb1cf3e0672cd240250547b855ae0f8894496225
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6259769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccaf377f82ea563a543d1a8bcf9a53870f6427a0cacae9f9ad5e46e6c7eabff`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 03:13:19 GMT
COPY file:6e08520addf5d0c5d064e431d76487779d8fd8f4c03f71a72dc4e2c81812a922 in /nats-streaming-server 
# Wed, 02 Jun 2021 03:13:20 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 03:13:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 03:13:20 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:887fd90bbdf32bb85ec9e85b63e60eccca791d6c882e30de0c10e6e583ccbb65`  
		Last Modified: Wed, 02 Jun 2021 03:15:02 GMT  
		Size: 6.3 MB (6259769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22.0-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bd5a415582b3f1d079d6498c12ea9138d7bde01dcd3a5f5a35a1731edf4c889f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6197708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d36744f70db176ba94e376a65c5edda55a7167035e7dffdf217e594c1ac283`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 02:14:00 GMT
COPY file:ef2047bb70888b72ef213e68689b3b8ae622cc597cd07b313c26b278418788bd in /nats-streaming-server 
# Wed, 02 Jun 2021 02:14:00 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 02:14:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 02:14:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ddf987a265c2be80179a2683a2d725f5a7e9fb477bc5752443a6d955be681a50`  
		Last Modified: Wed, 02 Jun 2021 02:15:07 GMT  
		Size: 6.2 MB (6197708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22.0-nanoserver`

```console
$ docker pull nats-streaming@sha256:1dc0e94fc6d8cea9665e3cb1b7a07e9f0353f1fafa9f72295ce19916331997d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1935; amd64

### `nats-streaming:0.22.0-nanoserver` - windows version 10.0.17763.1935; amd64

```console
$ docker pull nats-streaming@sha256:f14d95a507285f7b6dac026a6d8f37deea8dd96b64f80602e388b3696f7cba25
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108314029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c511c19c4f82a1f431dc21df9c7ecf63522fff783e081e96479e17ad9dc77d6c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 May 2021 11:54:57 GMT
RUN Apply image 1809-amd64
# Wed, 12 May 2021 15:44:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:17:51 GMT
RUN cmd /S /C #(nop) COPY file:72a29a3f2d4a0bd237295ad8b2a317a32c76cbb8a1af898a564024d5013c0475 in C:\nats-streaming-server.exe 
# Wed, 02 Jun 2021 00:17:52 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:17:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:17:54 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b9043d31610e0dfa43b1afe286f8918b6e3bf69ece50f44424b29d48f20aa662`  
		Size: 101.4 MB (101375240 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95b58e21e5cdf4e2f9e5c87487734458885da325634d72f9c4e6583b353af06f`  
		Last Modified: Wed, 12 May 2021 15:49:02 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64768458156c8207b96c2a86ad6a981088c4a7f3e2d4678bc1c62a9f4e6fdc6`  
		Last Modified: Wed, 02 Jun 2021 00:22:54 GMT  
		Size: 6.9 MB (6934146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f298c3fb0faca6834b234589beddaa038a32c7a62ed70ad82b916372f0c88af`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e5c68c5466b75473483ef53e38622b28cb869445a4073ce864f39d9bb08284`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d375f4a29f433bf0c21962820308e15313a81506ef594ed0ff2c5bd73c0b33`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22.0-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:1dc0e94fc6d8cea9665e3cb1b7a07e9f0353f1fafa9f72295ce19916331997d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1935; amd64

### `nats-streaming:0.22.0-nanoserver-1809` - windows version 10.0.17763.1935; amd64

```console
$ docker pull nats-streaming@sha256:f14d95a507285f7b6dac026a6d8f37deea8dd96b64f80602e388b3696f7cba25
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108314029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c511c19c4f82a1f431dc21df9c7ecf63522fff783e081e96479e17ad9dc77d6c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 May 2021 11:54:57 GMT
RUN Apply image 1809-amd64
# Wed, 12 May 2021 15:44:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:17:51 GMT
RUN cmd /S /C #(nop) COPY file:72a29a3f2d4a0bd237295ad8b2a317a32c76cbb8a1af898a564024d5013c0475 in C:\nats-streaming-server.exe 
# Wed, 02 Jun 2021 00:17:52 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:17:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:17:54 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b9043d31610e0dfa43b1afe286f8918b6e3bf69ece50f44424b29d48f20aa662`  
		Size: 101.4 MB (101375240 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95b58e21e5cdf4e2f9e5c87487734458885da325634d72f9c4e6583b353af06f`  
		Last Modified: Wed, 12 May 2021 15:49:02 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64768458156c8207b96c2a86ad6a981088c4a7f3e2d4678bc1c62a9f4e6fdc6`  
		Last Modified: Wed, 02 Jun 2021 00:22:54 GMT  
		Size: 6.9 MB (6934146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f298c3fb0faca6834b234589beddaa038a32c7a62ed70ad82b916372f0c88af`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e5c68c5466b75473483ef53e38622b28cb869445a4073ce864f39d9bb08284`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d375f4a29f433bf0c21962820308e15313a81506ef594ed0ff2c5bd73c0b33`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22.0-scratch`

```console
$ docker pull nats-streaming@sha256:29a31360a13ce43c1a19b01d048213225f0ca3daaf0ac9f75e4ff9e21fcb656f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.22.0-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ba1be2cd913a1e9f1ffc9445e5c04c169db333819beb7204deb3bc7c29fde5a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6800613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f2d32e0c9a23e5a9a5cb19c8b1404a9cc7af17915e33eabb71e55767848df7`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 05:47:24 GMT
COPY file:bbdef008b65f574a4e4593641e45dd6cdff5e8261d06d8f3959963f686dcdb78 in /nats-streaming-server 
# Wed, 02 Jun 2021 05:47:24 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 05:47:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 05:47:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:afa0998a9989cfec22c4ad772da3ca685ea7ccf963253ff9c27edf33a00d49c6`  
		Last Modified: Wed, 02 Jun 2021 05:48:07 GMT  
		Size: 6.8 MB (6800613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22.0-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:1bef88847972d6206955fdc84742cb2505dcdf9ec86c2ef8bd6b5629c88ef2f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6269700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258e5207bc79452baf170c0dc0a5c955f71c72fadc9fff82bffecc06eb3e1e81`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 01 Jun 2021 23:54:46 GMT
COPY file:a4f69de3d07c6870dde4796b4de69a931a699d7e5b6ec30b2f25f6a23d66cb33 in /nats-streaming-server 
# Tue, 01 Jun 2021 23:54:47 GMT
EXPOSE 4222 8222
# Tue, 01 Jun 2021 23:54:47 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 01 Jun 2021 23:54:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8ab135edb380ca588ed7d11dbea1418006a6708ae7ae5effad8d86bcef90198e`  
		Last Modified: Tue, 01 Jun 2021 23:56:26 GMT  
		Size: 6.3 MB (6269700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22.0-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:a6c122176a5ff4bdae9a653ebb1cf3e0672cd240250547b855ae0f8894496225
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6259769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccaf377f82ea563a543d1a8bcf9a53870f6427a0cacae9f9ad5e46e6c7eabff`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 03:13:19 GMT
COPY file:6e08520addf5d0c5d064e431d76487779d8fd8f4c03f71a72dc4e2c81812a922 in /nats-streaming-server 
# Wed, 02 Jun 2021 03:13:20 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 03:13:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 03:13:20 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:887fd90bbdf32bb85ec9e85b63e60eccca791d6c882e30de0c10e6e583ccbb65`  
		Last Modified: Wed, 02 Jun 2021 03:15:02 GMT  
		Size: 6.3 MB (6259769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22.0-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bd5a415582b3f1d079d6498c12ea9138d7bde01dcd3a5f5a35a1731edf4c889f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6197708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d36744f70db176ba94e376a65c5edda55a7167035e7dffdf217e594c1ac283`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 02:14:00 GMT
COPY file:ef2047bb70888b72ef213e68689b3b8ae622cc597cd07b313c26b278418788bd in /nats-streaming-server 
# Wed, 02 Jun 2021 02:14:00 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 02:14:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 02:14:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ddf987a265c2be80179a2683a2d725f5a7e9fb477bc5752443a6d955be681a50`  
		Last Modified: Wed, 02 Jun 2021 02:15:07 GMT  
		Size: 6.2 MB (6197708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22.0-windowsservercore`

```console
$ docker pull nats-streaming@sha256:5fbee84f8c860aeec9fbdcc3133e17141649ee0baefa7bbfbd7148723e9e2912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1935; amd64
	-	windows version 10.0.14393.4402; amd64

### `nats-streaming:0.22.0-windowsservercore` - windows version 10.0.17763.1935; amd64

```console
$ docker pull nats-streaming@sha256:b4ef1c8cc8cd9078fb6754750750cad7a286844fe27d3fd1a0abbd5e2955d0a8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2491648944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5674c44573a2caccbd707fff099991bdbb2f9e9ec95be3b4a74e9e2bfe599197`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 08 May 2021 09:21:48 GMT
RUN Install update 1809-amd64
# Tue, 11 May 2021 23:54:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 May 2021 15:41:49 GMT
ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:15:23 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 00:15:24 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.22.0/nats-streaming-server-v0.22.0-windows-amd64.zip
# Wed, 02 Jun 2021 00:15:25 GMT
ENV GIT_DOWNLOAD_SHA256=436c16330efbd0767d9a69dcdf2d3badd4e2598fab23c4f4a192e9d9982c2c92
# Wed, 02 Jun 2021 00:16:08 GMT
RUN Set-PSDebug -Trace 2
# Wed, 02 Jun 2021 00:17:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 02 Jun 2021 00:17:40 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:17:41 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:17:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8116de3c91c3f1ef2d6c09b49ef5407c9b4d672896eb3af5182a997c3c5379c9`  
		Size: 756.2 MB (756156286 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c049a65ed9206719f5c04428cb853623400e8ab1668243872b1134775f752962`  
		Last Modified: Wed, 12 May 2021 00:41:58 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262d2305f11fe8f36ef3508b42686daac7e99da966ed02f4ded1927387b1b75b`  
		Last Modified: Wed, 12 May 2021 15:48:42 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24932ebb62fedf8bc966247332680ddb3a6793604c0ed8133db9e56b10333616`  
		Last Modified: Wed, 02 Jun 2021 00:22:35 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb436a7ae07957612fdf342254deba5631a36e070eff281192a9eac753cdc5f`  
		Last Modified: Wed, 02 Jun 2021 00:22:35 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:face841f208848bbb571c289ab673bbef75a4af464c1430ee20ef085563ffde7`  
		Last Modified: Wed, 02 Jun 2021 00:22:35 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb048e76e13a831ac87972c8bc1a28f8a94183505d50c49388e8414acc5eef08`  
		Last Modified: Wed, 02 Jun 2021 00:22:38 GMT  
		Size: 5.1 MB (5121106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64673f2be1fb01eaff52556ba05ce5242bf22987bfe1833a67c30942f1b5c201`  
		Last Modified: Wed, 02 Jun 2021 00:22:36 GMT  
		Size: 12.0 MB (12027291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1385b473d95e5015b5dfb3cee8ecc2e18fd698a628a816f749d8d33078bbda1a`  
		Last Modified: Wed, 02 Jun 2021 00:22:32 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad68fa43ed8fac2ccf3c70066b8b236c9d33b137dfaf7b1d7fcf589ecd3efde0`  
		Last Modified: Wed, 02 Jun 2021 00:22:32 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487c92830589b96248c25f62e361f55a630d1a2962964cf2191de4aaee556d78`  
		Last Modified: Wed, 02 Jun 2021 00:22:33 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.22.0-windowsservercore` - windows version 10.0.14393.4402; amd64

```console
$ docker pull nats-streaming@sha256:4ec00239efea2ce9e8341045679e6a3e7c008bf54c1a2ed97ee48478a45be6ef
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818577847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ecc3bd85a796e373842d619a9259b900fa37a3c3507780f2c0e8d4fcd48d4e`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 26 Apr 2021 17:25:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 May 2021 23:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 May 2021 15:44:16 GMT
ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:18:02 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 00:18:03 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.22.0/nats-streaming-server-v0.22.0-windows-amd64.zip
# Wed, 02 Jun 2021 00:18:04 GMT
ENV GIT_DOWNLOAD_SHA256=436c16330efbd0767d9a69dcdf2d3badd4e2598fab23c4f4a192e9d9982c2c92
# Wed, 02 Jun 2021 00:19:38 GMT
RUN Set-PSDebug -Trace 2
# Wed, 02 Jun 2021 00:21:48 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 02 Jun 2021 00:21:49 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:21:50 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:21:51 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7f532f88613ca85064b055f6b93f8517bd05feba8fdce495a6ad1421573e765e`  
		Size: 1.7 GB (1725791397 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:50d0f4595a2bdc5dc0623fbee162be09d0631373eb9e82a0b1ec387ce1512c49`  
		Last Modified: Wed, 12 May 2021 00:46:32 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7998d92dbbcfc4e6dc106e75206a3cfde70fe601eb46b0515658f23dcd53ae`  
		Last Modified: Wed, 12 May 2021 15:49:26 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c54f8fb333eecc0b6838b82bdefec17dabd1e356ae640842f7d2623016bff34`  
		Last Modified: Wed, 02 Jun 2021 00:23:10 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caac90263041fd97d9787b47f96c2be639c606a1df8b7e779a6d159c2b51f080`  
		Last Modified: Wed, 02 Jun 2021 00:23:10 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543d9016ba1a5fbf9e855d8779b322554244ced48a97d1ea871faa720aa19cc4`  
		Last Modified: Wed, 02 Jun 2021 00:23:10 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b24da1a712f81c6fdd463b7e1d9e82ebf5a5d67320160da3e6e869675188e8`  
		Last Modified: Wed, 02 Jun 2021 00:23:08 GMT  
		Size: 5.7 MB (5700376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f1c189638ad48c571c54b98a6ac4de00054f1953a928836be2cbaccb4aa951`  
		Last Modified: Wed, 02 Jun 2021 00:23:11 GMT  
		Size: 17.1 MB (17088787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528e1a5b38c1b0120dfb058ce56e406344aef9df3953f2eb3f9fdb1e660b30eb`  
		Last Modified: Wed, 02 Jun 2021 00:23:06 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347dad5447a5c06c5d7e02f1d46766052ac70cc9196be60167d11fb944900088`  
		Last Modified: Wed, 02 Jun 2021 00:23:07 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32cce4e8dbbc2bb82c047ec6f45fc7221a29b36dcebae2ee53c6b17c24dfca2`  
		Last Modified: Wed, 02 Jun 2021 00:23:07 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22.0-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:b9fde4c299c883fc1db3e776be8bd3006806bd0e69527271d2d8a1b38614ab9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1935; amd64

### `nats-streaming:0.22.0-windowsservercore-1809` - windows version 10.0.17763.1935; amd64

```console
$ docker pull nats-streaming@sha256:b4ef1c8cc8cd9078fb6754750750cad7a286844fe27d3fd1a0abbd5e2955d0a8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2491648944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5674c44573a2caccbd707fff099991bdbb2f9e9ec95be3b4a74e9e2bfe599197`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 08 May 2021 09:21:48 GMT
RUN Install update 1809-amd64
# Tue, 11 May 2021 23:54:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 May 2021 15:41:49 GMT
ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:15:23 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 00:15:24 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.22.0/nats-streaming-server-v0.22.0-windows-amd64.zip
# Wed, 02 Jun 2021 00:15:25 GMT
ENV GIT_DOWNLOAD_SHA256=436c16330efbd0767d9a69dcdf2d3badd4e2598fab23c4f4a192e9d9982c2c92
# Wed, 02 Jun 2021 00:16:08 GMT
RUN Set-PSDebug -Trace 2
# Wed, 02 Jun 2021 00:17:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 02 Jun 2021 00:17:40 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:17:41 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:17:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8116de3c91c3f1ef2d6c09b49ef5407c9b4d672896eb3af5182a997c3c5379c9`  
		Size: 756.2 MB (756156286 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c049a65ed9206719f5c04428cb853623400e8ab1668243872b1134775f752962`  
		Last Modified: Wed, 12 May 2021 00:41:58 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262d2305f11fe8f36ef3508b42686daac7e99da966ed02f4ded1927387b1b75b`  
		Last Modified: Wed, 12 May 2021 15:48:42 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24932ebb62fedf8bc966247332680ddb3a6793604c0ed8133db9e56b10333616`  
		Last Modified: Wed, 02 Jun 2021 00:22:35 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb436a7ae07957612fdf342254deba5631a36e070eff281192a9eac753cdc5f`  
		Last Modified: Wed, 02 Jun 2021 00:22:35 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:face841f208848bbb571c289ab673bbef75a4af464c1430ee20ef085563ffde7`  
		Last Modified: Wed, 02 Jun 2021 00:22:35 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb048e76e13a831ac87972c8bc1a28f8a94183505d50c49388e8414acc5eef08`  
		Last Modified: Wed, 02 Jun 2021 00:22:38 GMT  
		Size: 5.1 MB (5121106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64673f2be1fb01eaff52556ba05ce5242bf22987bfe1833a67c30942f1b5c201`  
		Last Modified: Wed, 02 Jun 2021 00:22:36 GMT  
		Size: 12.0 MB (12027291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1385b473d95e5015b5dfb3cee8ecc2e18fd698a628a816f749d8d33078bbda1a`  
		Last Modified: Wed, 02 Jun 2021 00:22:32 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad68fa43ed8fac2ccf3c70066b8b236c9d33b137dfaf7b1d7fcf589ecd3efde0`  
		Last Modified: Wed, 02 Jun 2021 00:22:32 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487c92830589b96248c25f62e361f55a630d1a2962964cf2191de4aaee556d78`  
		Last Modified: Wed, 02 Jun 2021 00:22:33 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.22.0-windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:b388eabcc9ec2dafb5ba5344d26ec4177567009b06fac11bfbccb73a59329688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4402; amd64

### `nats-streaming:0.22.0-windowsservercore-ltsc2016` - windows version 10.0.14393.4402; amd64

```console
$ docker pull nats-streaming@sha256:4ec00239efea2ce9e8341045679e6a3e7c008bf54c1a2ed97ee48478a45be6ef
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818577847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ecc3bd85a796e373842d619a9259b900fa37a3c3507780f2c0e8d4fcd48d4e`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 26 Apr 2021 17:25:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 May 2021 23:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 May 2021 15:44:16 GMT
ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:18:02 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 00:18:03 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.22.0/nats-streaming-server-v0.22.0-windows-amd64.zip
# Wed, 02 Jun 2021 00:18:04 GMT
ENV GIT_DOWNLOAD_SHA256=436c16330efbd0767d9a69dcdf2d3badd4e2598fab23c4f4a192e9d9982c2c92
# Wed, 02 Jun 2021 00:19:38 GMT
RUN Set-PSDebug -Trace 2
# Wed, 02 Jun 2021 00:21:48 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 02 Jun 2021 00:21:49 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:21:50 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:21:51 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7f532f88613ca85064b055f6b93f8517bd05feba8fdce495a6ad1421573e765e`  
		Size: 1.7 GB (1725791397 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:50d0f4595a2bdc5dc0623fbee162be09d0631373eb9e82a0b1ec387ce1512c49`  
		Last Modified: Wed, 12 May 2021 00:46:32 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7998d92dbbcfc4e6dc106e75206a3cfde70fe601eb46b0515658f23dcd53ae`  
		Last Modified: Wed, 12 May 2021 15:49:26 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c54f8fb333eecc0b6838b82bdefec17dabd1e356ae640842f7d2623016bff34`  
		Last Modified: Wed, 02 Jun 2021 00:23:10 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caac90263041fd97d9787b47f96c2be639c606a1df8b7e779a6d159c2b51f080`  
		Last Modified: Wed, 02 Jun 2021 00:23:10 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543d9016ba1a5fbf9e855d8779b322554244ced48a97d1ea871faa720aa19cc4`  
		Last Modified: Wed, 02 Jun 2021 00:23:10 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b24da1a712f81c6fdd463b7e1d9e82ebf5a5d67320160da3e6e869675188e8`  
		Last Modified: Wed, 02 Jun 2021 00:23:08 GMT  
		Size: 5.7 MB (5700376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f1c189638ad48c571c54b98a6ac4de00054f1953a928836be2cbaccb4aa951`  
		Last Modified: Wed, 02 Jun 2021 00:23:11 GMT  
		Size: 17.1 MB (17088787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528e1a5b38c1b0120dfb058ce56e406344aef9df3953f2eb3f9fdb1e660b30eb`  
		Last Modified: Wed, 02 Jun 2021 00:23:06 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347dad5447a5c06c5d7e02f1d46766052ac70cc9196be60167d11fb944900088`  
		Last Modified: Wed, 02 Jun 2021 00:23:07 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32cce4e8dbbc2bb82c047ec6f45fc7221a29b36dcebae2ee53c6b17c24dfca2`  
		Last Modified: Wed, 02 Jun 2021 00:23:07 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:e5497622caf68a352e1c334082035baa46d1739664b4ebcc86257ce2505e34e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:25457c5b382da1fb7ab66c4f977ad38915b109e9bf0d4440f2ae2f314d3bcc97
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9894969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443be2e221357fdae9e3405207feb4e1f061dce181882a1cf208543e029bc8fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 02 Jun 2021 05:47:13 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 05:47:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 02 Jun 2021 05:47:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 02 Jun 2021 05:47:16 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 05:47:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 05:47:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4795908dc4759b01d3e4dd956343fb777c34c32afc57d2a4a96014fa67a41206`  
		Last Modified: Wed, 02 Jun 2021 05:47:46 GMT  
		Size: 7.1 MB (7082579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf7f8694c616cf8f24559388ba77e2349a8da60a47001bfd26c85997d87b593`  
		Last Modified: Wed, 02 Jun 2021 05:47:45 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:8f5fec9c3508cacdf96a48dccfda3cb07ba922cc31faefcd9b82981ece64b14c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9175700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6654e93452d6f1e430cf9500177e35f139504b0058910421ad055b18d8bb2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Tue, 01 Jun 2021 23:54:27 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Tue, 01 Jun 2021 23:54:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 01 Jun 2021 23:54:31 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 01 Jun 2021 23:54:32 GMT
EXPOSE 4222 8222
# Tue, 01 Jun 2021 23:54:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jun 2021 23:54:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef7b36a5eb9baa587c0c795817923d783258f4ec2d50d157bc548fb861282c6`  
		Last Modified: Tue, 01 Jun 2021 23:55:55 GMT  
		Size: 6.6 MB (6553148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02404618fe373dc7f314135fe9ad25f49fe83b972a776fda8ef5562833d9b7fd`  
		Last Modified: Tue, 01 Jun 2021 23:55:53 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:094bdcea75742a31480bd4f5771f741f7490f46a7bade1b1e6836fc2ab0e14f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8967137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a7379dc428ab28ff200036e6f1a917c42724a035ffc0d548ecb01f9954593f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 02 Jun 2021 03:12:59 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 03:13:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 02 Jun 2021 03:13:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 02 Jun 2021 03:13:03 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 03:13:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 03:13:03 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcef365af48832fc326fce4ba5cec1feba2d3830122e812be8f7c68c4eba747b`  
		Last Modified: Wed, 02 Jun 2021 03:14:30 GMT  
		Size: 6.5 MB (6542570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773ab986cb0c82686f2f65fa84b5189bb9194ebe32dc1d4f734e8842539f05fc`  
		Last Modified: Wed, 02 Jun 2021 03:14:29 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:5eb6c5b61d4dbeb7672f8406165f20b9b1d7d4a0395afcf2d269111da790ce77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9192667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed6553f1ac545332570e83b8471deeb88f40974893612e479ac4e77aef1ceb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 02 Jun 2021 02:13:47 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 02:13:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 02 Jun 2021 02:13:50 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 02 Jun 2021 02:13:50 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 02:13:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 02:13:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad47f4d7a28ba6697d6f539329857f5249ee98701b1cff717964bc6cfe759973`  
		Last Modified: Wed, 02 Jun 2021 02:14:42 GMT  
		Size: 6.5 MB (6480219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1643b8a109e099ee5ee16cef792deb5613b1cb5f18472c0a9d8a66004a5eb7`  
		Last Modified: Wed, 02 Jun 2021 02:14:41 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.13`

```console
$ docker pull nats-streaming@sha256:e5497622caf68a352e1c334082035baa46d1739664b4ebcc86257ce2505e34e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.13` - linux; amd64

```console
$ docker pull nats-streaming@sha256:25457c5b382da1fb7ab66c4f977ad38915b109e9bf0d4440f2ae2f314d3bcc97
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9894969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443be2e221357fdae9e3405207feb4e1f061dce181882a1cf208543e029bc8fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 02 Jun 2021 05:47:13 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 05:47:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 02 Jun 2021 05:47:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 02 Jun 2021 05:47:16 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 05:47:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 05:47:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4795908dc4759b01d3e4dd956343fb777c34c32afc57d2a4a96014fa67a41206`  
		Last Modified: Wed, 02 Jun 2021 05:47:46 GMT  
		Size: 7.1 MB (7082579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf7f8694c616cf8f24559388ba77e2349a8da60a47001bfd26c85997d87b593`  
		Last Modified: Wed, 02 Jun 2021 05:47:45 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.13` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:8f5fec9c3508cacdf96a48dccfda3cb07ba922cc31faefcd9b82981ece64b14c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9175700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6654e93452d6f1e430cf9500177e35f139504b0058910421ad055b18d8bb2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Tue, 01 Jun 2021 23:54:27 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Tue, 01 Jun 2021 23:54:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 01 Jun 2021 23:54:31 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 01 Jun 2021 23:54:32 GMT
EXPOSE 4222 8222
# Tue, 01 Jun 2021 23:54:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jun 2021 23:54:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef7b36a5eb9baa587c0c795817923d783258f4ec2d50d157bc548fb861282c6`  
		Last Modified: Tue, 01 Jun 2021 23:55:55 GMT  
		Size: 6.6 MB (6553148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02404618fe373dc7f314135fe9ad25f49fe83b972a776fda8ef5562833d9b7fd`  
		Last Modified: Tue, 01 Jun 2021 23:55:53 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.13` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:094bdcea75742a31480bd4f5771f741f7490f46a7bade1b1e6836fc2ab0e14f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8967137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a7379dc428ab28ff200036e6f1a917c42724a035ffc0d548ecb01f9954593f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 02 Jun 2021 03:12:59 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 03:13:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 02 Jun 2021 03:13:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 02 Jun 2021 03:13:03 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 03:13:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 03:13:03 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcef365af48832fc326fce4ba5cec1feba2d3830122e812be8f7c68c4eba747b`  
		Last Modified: Wed, 02 Jun 2021 03:14:30 GMT  
		Size: 6.5 MB (6542570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773ab986cb0c82686f2f65fa84b5189bb9194ebe32dc1d4f734e8842539f05fc`  
		Last Modified: Wed, 02 Jun 2021 03:14:29 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:5eb6c5b61d4dbeb7672f8406165f20b9b1d7d4a0395afcf2d269111da790ce77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9192667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed6553f1ac545332570e83b8471deeb88f40974893612e479ac4e77aef1ceb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 02 Jun 2021 02:13:47 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 02:13:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 02 Jun 2021 02:13:50 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 02 Jun 2021 02:13:50 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 02:13:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 02:13:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad47f4d7a28ba6697d6f539329857f5249ee98701b1cff717964bc6cfe759973`  
		Last Modified: Wed, 02 Jun 2021 02:14:42 GMT  
		Size: 6.5 MB (6480219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1643b8a109e099ee5ee16cef792deb5613b1cb5f18472c0a9d8a66004a5eb7`  
		Last Modified: Wed, 02 Jun 2021 02:14:41 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:bb7c4ca662ac7492f39584811919d6e9d3a1377df2ec02ddd09ca6ba8979baf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1935; amd64

### `nats-streaming:latest` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ba1be2cd913a1e9f1ffc9445e5c04c169db333819beb7204deb3bc7c29fde5a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6800613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f2d32e0c9a23e5a9a5cb19c8b1404a9cc7af17915e33eabb71e55767848df7`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 05:47:24 GMT
COPY file:bbdef008b65f574a4e4593641e45dd6cdff5e8261d06d8f3959963f686dcdb78 in /nats-streaming-server 
# Wed, 02 Jun 2021 05:47:24 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 05:47:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 05:47:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:afa0998a9989cfec22c4ad772da3ca685ea7ccf963253ff9c27edf33a00d49c6`  
		Last Modified: Wed, 02 Jun 2021 05:48:07 GMT  
		Size: 6.8 MB (6800613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:1bef88847972d6206955fdc84742cb2505dcdf9ec86c2ef8bd6b5629c88ef2f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6269700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258e5207bc79452baf170c0dc0a5c955f71c72fadc9fff82bffecc06eb3e1e81`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 01 Jun 2021 23:54:46 GMT
COPY file:a4f69de3d07c6870dde4796b4de69a931a699d7e5b6ec30b2f25f6a23d66cb33 in /nats-streaming-server 
# Tue, 01 Jun 2021 23:54:47 GMT
EXPOSE 4222 8222
# Tue, 01 Jun 2021 23:54:47 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 01 Jun 2021 23:54:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8ab135edb380ca588ed7d11dbea1418006a6708ae7ae5effad8d86bcef90198e`  
		Last Modified: Tue, 01 Jun 2021 23:56:26 GMT  
		Size: 6.3 MB (6269700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:a6c122176a5ff4bdae9a653ebb1cf3e0672cd240250547b855ae0f8894496225
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6259769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccaf377f82ea563a543d1a8bcf9a53870f6427a0cacae9f9ad5e46e6c7eabff`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 03:13:19 GMT
COPY file:6e08520addf5d0c5d064e431d76487779d8fd8f4c03f71a72dc4e2c81812a922 in /nats-streaming-server 
# Wed, 02 Jun 2021 03:13:20 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 03:13:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 03:13:20 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:887fd90bbdf32bb85ec9e85b63e60eccca791d6c882e30de0c10e6e583ccbb65`  
		Last Modified: Wed, 02 Jun 2021 03:15:02 GMT  
		Size: 6.3 MB (6259769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bd5a415582b3f1d079d6498c12ea9138d7bde01dcd3a5f5a35a1731edf4c889f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6197708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d36744f70db176ba94e376a65c5edda55a7167035e7dffdf217e594c1ac283`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 02:14:00 GMT
COPY file:ef2047bb70888b72ef213e68689b3b8ae622cc597cd07b313c26b278418788bd in /nats-streaming-server 
# Wed, 02 Jun 2021 02:14:00 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 02:14:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 02:14:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ddf987a265c2be80179a2683a2d725f5a7e9fb477bc5752443a6d955be681a50`  
		Last Modified: Wed, 02 Jun 2021 02:15:07 GMT  
		Size: 6.2 MB (6197708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.1935; amd64

```console
$ docker pull nats-streaming@sha256:f14d95a507285f7b6dac026a6d8f37deea8dd96b64f80602e388b3696f7cba25
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108314029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c511c19c4f82a1f431dc21df9c7ecf63522fff783e081e96479e17ad9dc77d6c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 May 2021 11:54:57 GMT
RUN Apply image 1809-amd64
# Wed, 12 May 2021 15:44:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:17:51 GMT
RUN cmd /S /C #(nop) COPY file:72a29a3f2d4a0bd237295ad8b2a317a32c76cbb8a1af898a564024d5013c0475 in C:\nats-streaming-server.exe 
# Wed, 02 Jun 2021 00:17:52 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:17:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:17:54 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b9043d31610e0dfa43b1afe286f8918b6e3bf69ece50f44424b29d48f20aa662`  
		Size: 101.4 MB (101375240 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95b58e21e5cdf4e2f9e5c87487734458885da325634d72f9c4e6583b353af06f`  
		Last Modified: Wed, 12 May 2021 15:49:02 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64768458156c8207b96c2a86ad6a981088c4a7f3e2d4678bc1c62a9f4e6fdc6`  
		Last Modified: Wed, 02 Jun 2021 00:22:54 GMT  
		Size: 6.9 MB (6934146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f298c3fb0faca6834b234589beddaa038a32c7a62ed70ad82b916372f0c88af`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e5c68c5466b75473483ef53e38622b28cb869445a4073ce864f39d9bb08284`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d375f4a29f433bf0c21962820308e15313a81506ef594ed0ff2c5bd73c0b33`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:29a31360a13ce43c1a19b01d048213225f0ca3daaf0ac9f75e4ff9e21fcb656f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ba1be2cd913a1e9f1ffc9445e5c04c169db333819beb7204deb3bc7c29fde5a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6800613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f2d32e0c9a23e5a9a5cb19c8b1404a9cc7af17915e33eabb71e55767848df7`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 05:47:24 GMT
COPY file:bbdef008b65f574a4e4593641e45dd6cdff5e8261d06d8f3959963f686dcdb78 in /nats-streaming-server 
# Wed, 02 Jun 2021 05:47:24 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 05:47:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 05:47:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:afa0998a9989cfec22c4ad772da3ca685ea7ccf963253ff9c27edf33a00d49c6`  
		Last Modified: Wed, 02 Jun 2021 05:48:07 GMT  
		Size: 6.8 MB (6800613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:1bef88847972d6206955fdc84742cb2505dcdf9ec86c2ef8bd6b5629c88ef2f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6269700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258e5207bc79452baf170c0dc0a5c955f71c72fadc9fff82bffecc06eb3e1e81`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 01 Jun 2021 23:54:46 GMT
COPY file:a4f69de3d07c6870dde4796b4de69a931a699d7e5b6ec30b2f25f6a23d66cb33 in /nats-streaming-server 
# Tue, 01 Jun 2021 23:54:47 GMT
EXPOSE 4222 8222
# Tue, 01 Jun 2021 23:54:47 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 01 Jun 2021 23:54:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8ab135edb380ca588ed7d11dbea1418006a6708ae7ae5effad8d86bcef90198e`  
		Last Modified: Tue, 01 Jun 2021 23:56:26 GMT  
		Size: 6.3 MB (6269700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:a6c122176a5ff4bdae9a653ebb1cf3e0672cd240250547b855ae0f8894496225
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6259769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccaf377f82ea563a543d1a8bcf9a53870f6427a0cacae9f9ad5e46e6c7eabff`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 03:13:19 GMT
COPY file:6e08520addf5d0c5d064e431d76487779d8fd8f4c03f71a72dc4e2c81812a922 in /nats-streaming-server 
# Wed, 02 Jun 2021 03:13:20 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 03:13:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 03:13:20 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:887fd90bbdf32bb85ec9e85b63e60eccca791d6c882e30de0c10e6e583ccbb65`  
		Last Modified: Wed, 02 Jun 2021 03:15:02 GMT  
		Size: 6.3 MB (6259769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bd5a415582b3f1d079d6498c12ea9138d7bde01dcd3a5f5a35a1731edf4c889f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6197708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d36744f70db176ba94e376a65c5edda55a7167035e7dffdf217e594c1ac283`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 02:14:00 GMT
COPY file:ef2047bb70888b72ef213e68689b3b8ae622cc597cd07b313c26b278418788bd in /nats-streaming-server 
# Wed, 02 Jun 2021 02:14:00 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 02:14:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 02:14:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ddf987a265c2be80179a2683a2d725f5a7e9fb477bc5752443a6d955be681a50`  
		Last Modified: Wed, 02 Jun 2021 02:15:07 GMT  
		Size: 6.2 MB (6197708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:1dc0e94fc6d8cea9665e3cb1b7a07e9f0353f1fafa9f72295ce19916331997d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1935; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.1935; amd64

```console
$ docker pull nats-streaming@sha256:f14d95a507285f7b6dac026a6d8f37deea8dd96b64f80602e388b3696f7cba25
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108314029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c511c19c4f82a1f431dc21df9c7ecf63522fff783e081e96479e17ad9dc77d6c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 May 2021 11:54:57 GMT
RUN Apply image 1809-amd64
# Wed, 12 May 2021 15:44:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:17:51 GMT
RUN cmd /S /C #(nop) COPY file:72a29a3f2d4a0bd237295ad8b2a317a32c76cbb8a1af898a564024d5013c0475 in C:\nats-streaming-server.exe 
# Wed, 02 Jun 2021 00:17:52 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:17:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:17:54 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b9043d31610e0dfa43b1afe286f8918b6e3bf69ece50f44424b29d48f20aa662`  
		Size: 101.4 MB (101375240 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95b58e21e5cdf4e2f9e5c87487734458885da325634d72f9c4e6583b353af06f`  
		Last Modified: Wed, 12 May 2021 15:49:02 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64768458156c8207b96c2a86ad6a981088c4a7f3e2d4678bc1c62a9f4e6fdc6`  
		Last Modified: Wed, 02 Jun 2021 00:22:54 GMT  
		Size: 6.9 MB (6934146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f298c3fb0faca6834b234589beddaa038a32c7a62ed70ad82b916372f0c88af`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e5c68c5466b75473483ef53e38622b28cb869445a4073ce864f39d9bb08284`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d375f4a29f433bf0c21962820308e15313a81506ef594ed0ff2c5bd73c0b33`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:1dc0e94fc6d8cea9665e3cb1b7a07e9f0353f1fafa9f72295ce19916331997d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1935; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.1935; amd64

```console
$ docker pull nats-streaming@sha256:f14d95a507285f7b6dac026a6d8f37deea8dd96b64f80602e388b3696f7cba25
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108314029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c511c19c4f82a1f431dc21df9c7ecf63522fff783e081e96479e17ad9dc77d6c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 May 2021 11:54:57 GMT
RUN Apply image 1809-amd64
# Wed, 12 May 2021 15:44:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:17:51 GMT
RUN cmd /S /C #(nop) COPY file:72a29a3f2d4a0bd237295ad8b2a317a32c76cbb8a1af898a564024d5013c0475 in C:\nats-streaming-server.exe 
# Wed, 02 Jun 2021 00:17:52 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:17:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:17:54 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b9043d31610e0dfa43b1afe286f8918b6e3bf69ece50f44424b29d48f20aa662`  
		Size: 101.4 MB (101375240 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95b58e21e5cdf4e2f9e5c87487734458885da325634d72f9c4e6583b353af06f`  
		Last Modified: Wed, 12 May 2021 15:49:02 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64768458156c8207b96c2a86ad6a981088c4a7f3e2d4678bc1c62a9f4e6fdc6`  
		Last Modified: Wed, 02 Jun 2021 00:22:54 GMT  
		Size: 6.9 MB (6934146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f298c3fb0faca6834b234589beddaa038a32c7a62ed70ad82b916372f0c88af`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e5c68c5466b75473483ef53e38622b28cb869445a4073ce864f39d9bb08284`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d375f4a29f433bf0c21962820308e15313a81506ef594ed0ff2c5bd73c0b33`  
		Last Modified: Wed, 02 Jun 2021 00:22:51 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:29a31360a13ce43c1a19b01d048213225f0ca3daaf0ac9f75e4ff9e21fcb656f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ba1be2cd913a1e9f1ffc9445e5c04c169db333819beb7204deb3bc7c29fde5a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6800613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f2d32e0c9a23e5a9a5cb19c8b1404a9cc7af17915e33eabb71e55767848df7`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 05:47:24 GMT
COPY file:bbdef008b65f574a4e4593641e45dd6cdff5e8261d06d8f3959963f686dcdb78 in /nats-streaming-server 
# Wed, 02 Jun 2021 05:47:24 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 05:47:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 05:47:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:afa0998a9989cfec22c4ad772da3ca685ea7ccf963253ff9c27edf33a00d49c6`  
		Last Modified: Wed, 02 Jun 2021 05:48:07 GMT  
		Size: 6.8 MB (6800613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:1bef88847972d6206955fdc84742cb2505dcdf9ec86c2ef8bd6b5629c88ef2f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6269700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258e5207bc79452baf170c0dc0a5c955f71c72fadc9fff82bffecc06eb3e1e81`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 01 Jun 2021 23:54:46 GMT
COPY file:a4f69de3d07c6870dde4796b4de69a931a699d7e5b6ec30b2f25f6a23d66cb33 in /nats-streaming-server 
# Tue, 01 Jun 2021 23:54:47 GMT
EXPOSE 4222 8222
# Tue, 01 Jun 2021 23:54:47 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 01 Jun 2021 23:54:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8ab135edb380ca588ed7d11dbea1418006a6708ae7ae5effad8d86bcef90198e`  
		Last Modified: Tue, 01 Jun 2021 23:56:26 GMT  
		Size: 6.3 MB (6269700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:a6c122176a5ff4bdae9a653ebb1cf3e0672cd240250547b855ae0f8894496225
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6259769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccaf377f82ea563a543d1a8bcf9a53870f6427a0cacae9f9ad5e46e6c7eabff`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 03:13:19 GMT
COPY file:6e08520addf5d0c5d064e431d76487779d8fd8f4c03f71a72dc4e2c81812a922 in /nats-streaming-server 
# Wed, 02 Jun 2021 03:13:20 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 03:13:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 03:13:20 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:887fd90bbdf32bb85ec9e85b63e60eccca791d6c882e30de0c10e6e583ccbb65`  
		Last Modified: Wed, 02 Jun 2021 03:15:02 GMT  
		Size: 6.3 MB (6259769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bd5a415582b3f1d079d6498c12ea9138d7bde01dcd3a5f5a35a1731edf4c889f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6197708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d36744f70db176ba94e376a65c5edda55a7167035e7dffdf217e594c1ac283`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Jun 2021 02:14:00 GMT
COPY file:ef2047bb70888b72ef213e68689b3b8ae622cc597cd07b313c26b278418788bd in /nats-streaming-server 
# Wed, 02 Jun 2021 02:14:00 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 02:14:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 02 Jun 2021 02:14:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ddf987a265c2be80179a2683a2d725f5a7e9fb477bc5752443a6d955be681a50`  
		Last Modified: Wed, 02 Jun 2021 02:15:07 GMT  
		Size: 6.2 MB (6197708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:5fbee84f8c860aeec9fbdcc3133e17141649ee0baefa7bbfbd7148723e9e2912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1935; amd64
	-	windows version 10.0.14393.4402; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.1935; amd64

```console
$ docker pull nats-streaming@sha256:b4ef1c8cc8cd9078fb6754750750cad7a286844fe27d3fd1a0abbd5e2955d0a8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2491648944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5674c44573a2caccbd707fff099991bdbb2f9e9ec95be3b4a74e9e2bfe599197`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 08 May 2021 09:21:48 GMT
RUN Install update 1809-amd64
# Tue, 11 May 2021 23:54:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 May 2021 15:41:49 GMT
ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:15:23 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 00:15:24 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.22.0/nats-streaming-server-v0.22.0-windows-amd64.zip
# Wed, 02 Jun 2021 00:15:25 GMT
ENV GIT_DOWNLOAD_SHA256=436c16330efbd0767d9a69dcdf2d3badd4e2598fab23c4f4a192e9d9982c2c92
# Wed, 02 Jun 2021 00:16:08 GMT
RUN Set-PSDebug -Trace 2
# Wed, 02 Jun 2021 00:17:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 02 Jun 2021 00:17:40 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:17:41 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:17:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8116de3c91c3f1ef2d6c09b49ef5407c9b4d672896eb3af5182a997c3c5379c9`  
		Size: 756.2 MB (756156286 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c049a65ed9206719f5c04428cb853623400e8ab1668243872b1134775f752962`  
		Last Modified: Wed, 12 May 2021 00:41:58 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262d2305f11fe8f36ef3508b42686daac7e99da966ed02f4ded1927387b1b75b`  
		Last Modified: Wed, 12 May 2021 15:48:42 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24932ebb62fedf8bc966247332680ddb3a6793604c0ed8133db9e56b10333616`  
		Last Modified: Wed, 02 Jun 2021 00:22:35 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb436a7ae07957612fdf342254deba5631a36e070eff281192a9eac753cdc5f`  
		Last Modified: Wed, 02 Jun 2021 00:22:35 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:face841f208848bbb571c289ab673bbef75a4af464c1430ee20ef085563ffde7`  
		Last Modified: Wed, 02 Jun 2021 00:22:35 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb048e76e13a831ac87972c8bc1a28f8a94183505d50c49388e8414acc5eef08`  
		Last Modified: Wed, 02 Jun 2021 00:22:38 GMT  
		Size: 5.1 MB (5121106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64673f2be1fb01eaff52556ba05ce5242bf22987bfe1833a67c30942f1b5c201`  
		Last Modified: Wed, 02 Jun 2021 00:22:36 GMT  
		Size: 12.0 MB (12027291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1385b473d95e5015b5dfb3cee8ecc2e18fd698a628a816f749d8d33078bbda1a`  
		Last Modified: Wed, 02 Jun 2021 00:22:32 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad68fa43ed8fac2ccf3c70066b8b236c9d33b137dfaf7b1d7fcf589ecd3efde0`  
		Last Modified: Wed, 02 Jun 2021 00:22:32 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487c92830589b96248c25f62e361f55a630d1a2962964cf2191de4aaee556d78`  
		Last Modified: Wed, 02 Jun 2021 00:22:33 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:windowsservercore` - windows version 10.0.14393.4402; amd64

```console
$ docker pull nats-streaming@sha256:4ec00239efea2ce9e8341045679e6a3e7c008bf54c1a2ed97ee48478a45be6ef
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818577847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ecc3bd85a796e373842d619a9259b900fa37a3c3507780f2c0e8d4fcd48d4e`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 26 Apr 2021 17:25:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 May 2021 23:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 May 2021 15:44:16 GMT
ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:18:02 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 00:18:03 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.22.0/nats-streaming-server-v0.22.0-windows-amd64.zip
# Wed, 02 Jun 2021 00:18:04 GMT
ENV GIT_DOWNLOAD_SHA256=436c16330efbd0767d9a69dcdf2d3badd4e2598fab23c4f4a192e9d9982c2c92
# Wed, 02 Jun 2021 00:19:38 GMT
RUN Set-PSDebug -Trace 2
# Wed, 02 Jun 2021 00:21:48 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 02 Jun 2021 00:21:49 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:21:50 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:21:51 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7f532f88613ca85064b055f6b93f8517bd05feba8fdce495a6ad1421573e765e`  
		Size: 1.7 GB (1725791397 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:50d0f4595a2bdc5dc0623fbee162be09d0631373eb9e82a0b1ec387ce1512c49`  
		Last Modified: Wed, 12 May 2021 00:46:32 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7998d92dbbcfc4e6dc106e75206a3cfde70fe601eb46b0515658f23dcd53ae`  
		Last Modified: Wed, 12 May 2021 15:49:26 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c54f8fb333eecc0b6838b82bdefec17dabd1e356ae640842f7d2623016bff34`  
		Last Modified: Wed, 02 Jun 2021 00:23:10 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caac90263041fd97d9787b47f96c2be639c606a1df8b7e779a6d159c2b51f080`  
		Last Modified: Wed, 02 Jun 2021 00:23:10 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543d9016ba1a5fbf9e855d8779b322554244ced48a97d1ea871faa720aa19cc4`  
		Last Modified: Wed, 02 Jun 2021 00:23:10 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b24da1a712f81c6fdd463b7e1d9e82ebf5a5d67320160da3e6e869675188e8`  
		Last Modified: Wed, 02 Jun 2021 00:23:08 GMT  
		Size: 5.7 MB (5700376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f1c189638ad48c571c54b98a6ac4de00054f1953a928836be2cbaccb4aa951`  
		Last Modified: Wed, 02 Jun 2021 00:23:11 GMT  
		Size: 17.1 MB (17088787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528e1a5b38c1b0120dfb058ce56e406344aef9df3953f2eb3f9fdb1e660b30eb`  
		Last Modified: Wed, 02 Jun 2021 00:23:06 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347dad5447a5c06c5d7e02f1d46766052ac70cc9196be60167d11fb944900088`  
		Last Modified: Wed, 02 Jun 2021 00:23:07 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32cce4e8dbbc2bb82c047ec6f45fc7221a29b36dcebae2ee53c6b17c24dfca2`  
		Last Modified: Wed, 02 Jun 2021 00:23:07 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:b9fde4c299c883fc1db3e776be8bd3006806bd0e69527271d2d8a1b38614ab9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1935; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.1935; amd64

```console
$ docker pull nats-streaming@sha256:b4ef1c8cc8cd9078fb6754750750cad7a286844fe27d3fd1a0abbd5e2955d0a8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2491648944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5674c44573a2caccbd707fff099991bdbb2f9e9ec95be3b4a74e9e2bfe599197`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 08 May 2021 09:21:48 GMT
RUN Install update 1809-amd64
# Tue, 11 May 2021 23:54:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 May 2021 15:41:49 GMT
ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:15:23 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 00:15:24 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.22.0/nats-streaming-server-v0.22.0-windows-amd64.zip
# Wed, 02 Jun 2021 00:15:25 GMT
ENV GIT_DOWNLOAD_SHA256=436c16330efbd0767d9a69dcdf2d3badd4e2598fab23c4f4a192e9d9982c2c92
# Wed, 02 Jun 2021 00:16:08 GMT
RUN Set-PSDebug -Trace 2
# Wed, 02 Jun 2021 00:17:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 02 Jun 2021 00:17:40 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:17:41 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:17:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8116de3c91c3f1ef2d6c09b49ef5407c9b4d672896eb3af5182a997c3c5379c9`  
		Size: 756.2 MB (756156286 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c049a65ed9206719f5c04428cb853623400e8ab1668243872b1134775f752962`  
		Last Modified: Wed, 12 May 2021 00:41:58 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262d2305f11fe8f36ef3508b42686daac7e99da966ed02f4ded1927387b1b75b`  
		Last Modified: Wed, 12 May 2021 15:48:42 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24932ebb62fedf8bc966247332680ddb3a6793604c0ed8133db9e56b10333616`  
		Last Modified: Wed, 02 Jun 2021 00:22:35 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb436a7ae07957612fdf342254deba5631a36e070eff281192a9eac753cdc5f`  
		Last Modified: Wed, 02 Jun 2021 00:22:35 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:face841f208848bbb571c289ab673bbef75a4af464c1430ee20ef085563ffde7`  
		Last Modified: Wed, 02 Jun 2021 00:22:35 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb048e76e13a831ac87972c8bc1a28f8a94183505d50c49388e8414acc5eef08`  
		Last Modified: Wed, 02 Jun 2021 00:22:38 GMT  
		Size: 5.1 MB (5121106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64673f2be1fb01eaff52556ba05ce5242bf22987bfe1833a67c30942f1b5c201`  
		Last Modified: Wed, 02 Jun 2021 00:22:36 GMT  
		Size: 12.0 MB (12027291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1385b473d95e5015b5dfb3cee8ecc2e18fd698a628a816f749d8d33078bbda1a`  
		Last Modified: Wed, 02 Jun 2021 00:22:32 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad68fa43ed8fac2ccf3c70066b8b236c9d33b137dfaf7b1d7fcf589ecd3efde0`  
		Last Modified: Wed, 02 Jun 2021 00:22:32 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487c92830589b96248c25f62e361f55a630d1a2962964cf2191de4aaee556d78`  
		Last Modified: Wed, 02 Jun 2021 00:22:33 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:b388eabcc9ec2dafb5ba5344d26ec4177567009b06fac11bfbccb73a59329688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4402; amd64

### `nats-streaming:windowsservercore-ltsc2016` - windows version 10.0.14393.4402; amd64

```console
$ docker pull nats-streaming@sha256:4ec00239efea2ce9e8341045679e6a3e7c008bf54c1a2ed97ee48478a45be6ef
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818577847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ecc3bd85a796e373842d619a9259b900fa37a3c3507780f2c0e8d4fcd48d4e`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 26 Apr 2021 17:25:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 May 2021 23:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 May 2021 15:44:16 GMT
ENV NATS_DOCKERIZED=1
# Wed, 02 Jun 2021 00:18:02 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Wed, 02 Jun 2021 00:18:03 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.22.0/nats-streaming-server-v0.22.0-windows-amd64.zip
# Wed, 02 Jun 2021 00:18:04 GMT
ENV GIT_DOWNLOAD_SHA256=436c16330efbd0767d9a69dcdf2d3badd4e2598fab23c4f4a192e9d9982c2c92
# Wed, 02 Jun 2021 00:19:38 GMT
RUN Set-PSDebug -Trace 2
# Wed, 02 Jun 2021 00:21:48 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 02 Jun 2021 00:21:49 GMT
EXPOSE 4222 8222
# Wed, 02 Jun 2021 00:21:50 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 02 Jun 2021 00:21:51 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7f532f88613ca85064b055f6b93f8517bd05feba8fdce495a6ad1421573e765e`  
		Size: 1.7 GB (1725791397 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:50d0f4595a2bdc5dc0623fbee162be09d0631373eb9e82a0b1ec387ce1512c49`  
		Last Modified: Wed, 12 May 2021 00:46:32 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7998d92dbbcfc4e6dc106e75206a3cfde70fe601eb46b0515658f23dcd53ae`  
		Last Modified: Wed, 12 May 2021 15:49:26 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c54f8fb333eecc0b6838b82bdefec17dabd1e356ae640842f7d2623016bff34`  
		Last Modified: Wed, 02 Jun 2021 00:23:10 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caac90263041fd97d9787b47f96c2be639c606a1df8b7e779a6d159c2b51f080`  
		Last Modified: Wed, 02 Jun 2021 00:23:10 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543d9016ba1a5fbf9e855d8779b322554244ced48a97d1ea871faa720aa19cc4`  
		Last Modified: Wed, 02 Jun 2021 00:23:10 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b24da1a712f81c6fdd463b7e1d9e82ebf5a5d67320160da3e6e869675188e8`  
		Last Modified: Wed, 02 Jun 2021 00:23:08 GMT  
		Size: 5.7 MB (5700376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f1c189638ad48c571c54b98a6ac4de00054f1953a928836be2cbaccb4aa951`  
		Last Modified: Wed, 02 Jun 2021 00:23:11 GMT  
		Size: 17.1 MB (17088787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528e1a5b38c1b0120dfb058ce56e406344aef9df3953f2eb3f9fdb1e660b30eb`  
		Last Modified: Wed, 02 Jun 2021 00:23:06 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347dad5447a5c06c5d7e02f1d46766052ac70cc9196be60167d11fb944900088`  
		Last Modified: Wed, 02 Jun 2021 00:23:07 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32cce4e8dbbc2bb82c047ec6f45fc7221a29b36dcebae2ee53c6b17c24dfca2`  
		Last Modified: Wed, 02 Jun 2021 00:23:07 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

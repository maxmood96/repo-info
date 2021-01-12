<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats-streaming`

-	[`nats-streaming:0.20`](#nats-streaming020)
-	[`nats-streaming:0.20.0`](#nats-streaming0200)
-	[`nats-streaming:0.20.0-alpine`](#nats-streaming0200-alpine)
-	[`nats-streaming:0.20.0-alpine3.12`](#nats-streaming0200-alpine312)
-	[`nats-streaming:0.20.0-linux`](#nats-streaming0200-linux)
-	[`nats-streaming:0.20.0-nanoserver`](#nats-streaming0200-nanoserver)
-	[`nats-streaming:0.20.0-nanoserver-1809`](#nats-streaming0200-nanoserver-1809)
-	[`nats-streaming:0.20.0-scratch`](#nats-streaming0200-scratch)
-	[`nats-streaming:0.20.0-windowsservercore`](#nats-streaming0200-windowsservercore)
-	[`nats-streaming:0.20.0-windowsservercore-1809`](#nats-streaming0200-windowsservercore-1809)
-	[`nats-streaming:0.20.0-windowsservercore-ltsc2016`](#nats-streaming0200-windowsservercore-ltsc2016)
-	[`nats-streaming:0.20-alpine`](#nats-streaming020-alpine)
-	[`nats-streaming:0.20-alpine3.12`](#nats-streaming020-alpine312)
-	[`nats-streaming:0.20-linux`](#nats-streaming020-linux)
-	[`nats-streaming:0.20-nanoserver`](#nats-streaming020-nanoserver)
-	[`nats-streaming:0.20-nanoserver-1809`](#nats-streaming020-nanoserver-1809)
-	[`nats-streaming:0.20-scratch`](#nats-streaming020-scratch)
-	[`nats-streaming:0.20-windowsservercore`](#nats-streaming020-windowsservercore)
-	[`nats-streaming:0.20-windowsservercore-1809`](#nats-streaming020-windowsservercore-1809)
-	[`nats-streaming:0.20-windowsservercore-ltsc2016`](#nats-streaming020-windowsservercore-ltsc2016)
-	[`nats-streaming:alpine`](#nats-streamingalpine)
-	[`nats-streaming:alpine3.12`](#nats-streamingalpine312)
-	[`nats-streaming:latest`](#nats-streaminglatest)
-	[`nats-streaming:linux`](#nats-streaminglinux)
-	[`nats-streaming:nanoserver`](#nats-streamingnanoserver)
-	[`nats-streaming:nanoserver-1809`](#nats-streamingnanoserver-1809)
-	[`nats-streaming:scratch`](#nats-streamingscratch)
-	[`nats-streaming:windowsservercore`](#nats-streamingwindowsservercore)
-	[`nats-streaming:windowsservercore-1809`](#nats-streamingwindowsservercore-1809)
-	[`nats-streaming:windowsservercore-ltsc2016`](#nats-streamingwindowsservercore-ltsc2016)

## `nats-streaming:0.20`

```console
$ docker pull nats-streaming@sha256:563a35fb6be5ca12bbbb1c8cb18196dfb1f08205de173985a8698e3ffb1bd8d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1637; amd64

### `nats-streaming:0.20` - linux; amd64

```console
$ docker pull nats-streaming@sha256:cd0162a7232de1eabe982554c8740e7edbac4747af3e99fa9bc38a480b4a4243
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1544c1524919e1458186fefae5f5ff415c37055742e531010fc2660b11db2339`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 12 Jan 2021 00:48:24 GMT
COPY file:acbca3cec2dc5172f21984b614cbcd90e6e4cf0bd9848c5ddcffb94615a02436 in /nats-streaming-server 
# Tue, 12 Jan 2021 00:48:24 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:48:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 12 Jan 2021 00:48:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0d51fde6ce3492f397e8a85dad354a9a45ab91310cf4abd6275101f3ef823587`  
		Last Modified: Tue, 12 Jan 2021 00:49:07 GMT  
		Size: 5.9 MB (5914730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:bbb3d771f9232932017b9cb9b501734367bc3560eed790695be682d94a8f3573
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed880c2955fd126b0ce38471e90c9467c9c739f55b4c789cec1a4575a41d36f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 11 Jan 2021 23:53:53 GMT
COPY file:617b9b5366d0d437ce471ad0763bdd7d350496612583dc2c7044dcde4d32257e in /nats-streaming-server 
# Mon, 11 Jan 2021 23:53:54 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:53:54 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 11 Jan 2021 23:53:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7cffcff2c5b4913dac660d7456365492a0393b1aa6f1812f6b7b46b250e1970d`  
		Last Modified: Mon, 11 Jan 2021 23:54:39 GMT  
		Size: 5.4 MB (5444243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b2d9250f9a4e3b25b2212f4e8c27c693cc5cfa0f83ca82a8005c90ae8372ab86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f1d3c5a1d429a3e2b1fc71f5bc023980c41d34ccb0a0482aca07b6cbb4d6f1`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 12 Jan 2021 00:19:09 GMT
COPY file:2b3fc04f11d3cc7cdfa09f93a79d8efe0889d24324b831fb35126470165c9027 in /nats-streaming-server 
# Tue, 12 Jan 2021 00:19:14 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:19:16 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 12 Jan 2021 00:19:17 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bf50122b11c4b5e2fa295a9456a93489ad25dd1e9bfefda1d572da1a57418205`  
		Last Modified: Tue, 12 Jan 2021 00:20:01 GMT  
		Size: 5.4 MB (5439328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:0f315491d4d14e634f971591c7f8bd0eb9aad59975fcdf867a51294df2e5efb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dba974517468c29a982c1b4a0b7744a93825122145a1dcc5f7e53c96119efa`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 11 Jan 2021 23:47:25 GMT
COPY file:5a251d4e6bafc9d9ea6f25cd37fd44252da405176da94cc580cdd663abecffa5 in /nats-streaming-server 
# Mon, 11 Jan 2021 23:47:26 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:47:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 11 Jan 2021 23:47:27 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:58239a1ea6494e431645c7ad156ed917333a248edbe6be76af8b7384d9339f07`  
		Last Modified: Mon, 11 Jan 2021 23:48:09 GMT  
		Size: 5.4 MB (5388538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats-streaming@sha256:dc8cb861e9ebd507f6052f70f00e5cd153ed10f3ce94b514ca53b0b66d68e1a6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107290057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f45933a0476064ac026d83b04912423ee2e0e38a5a0a13d9f6dd101b42deccd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:22:30 GMT
RUN cmd /S /C #(nop) COPY file:f2450ffeda74e33f820191eccf78b6647ce56865170e966bfa8e72afe6e46c36 in C:\nats-streaming-server.exe 
# Tue, 12 Jan 2021 00:22:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:22:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:22:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9a7966c40d2ea4e2a3a9732b1971a90e2c947c7436138dfeecc7a5dd475850`  
		Last Modified: Tue, 12 Jan 2021 00:26:57 GMT  
		Size: 6.0 MB (6021865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8709fe81a73f9b62174f38547b2d9da1bffe292d51b1b93b8fd6c4f89a924e9`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 814.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3718c1b6d751147f39ee7c4a6f1c5cea284aa100dfce6a8e622a16c6456c7d18`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe5aba04f48a9d07940a1f43378efa11f913918e6ebcead455135c3d0346504`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 823.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20.0`

```console
$ docker pull nats-streaming@sha256:563a35fb6be5ca12bbbb1c8cb18196dfb1f08205de173985a8698e3ffb1bd8d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1637; amd64

### `nats-streaming:0.20.0` - linux; amd64

```console
$ docker pull nats-streaming@sha256:cd0162a7232de1eabe982554c8740e7edbac4747af3e99fa9bc38a480b4a4243
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1544c1524919e1458186fefae5f5ff415c37055742e531010fc2660b11db2339`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 12 Jan 2021 00:48:24 GMT
COPY file:acbca3cec2dc5172f21984b614cbcd90e6e4cf0bd9848c5ddcffb94615a02436 in /nats-streaming-server 
# Tue, 12 Jan 2021 00:48:24 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:48:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 12 Jan 2021 00:48:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0d51fde6ce3492f397e8a85dad354a9a45ab91310cf4abd6275101f3ef823587`  
		Last Modified: Tue, 12 Jan 2021 00:49:07 GMT  
		Size: 5.9 MB (5914730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20.0` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:bbb3d771f9232932017b9cb9b501734367bc3560eed790695be682d94a8f3573
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed880c2955fd126b0ce38471e90c9467c9c739f55b4c789cec1a4575a41d36f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 11 Jan 2021 23:53:53 GMT
COPY file:617b9b5366d0d437ce471ad0763bdd7d350496612583dc2c7044dcde4d32257e in /nats-streaming-server 
# Mon, 11 Jan 2021 23:53:54 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:53:54 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 11 Jan 2021 23:53:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7cffcff2c5b4913dac660d7456365492a0393b1aa6f1812f6b7b46b250e1970d`  
		Last Modified: Mon, 11 Jan 2021 23:54:39 GMT  
		Size: 5.4 MB (5444243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20.0` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b2d9250f9a4e3b25b2212f4e8c27c693cc5cfa0f83ca82a8005c90ae8372ab86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f1d3c5a1d429a3e2b1fc71f5bc023980c41d34ccb0a0482aca07b6cbb4d6f1`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 12 Jan 2021 00:19:09 GMT
COPY file:2b3fc04f11d3cc7cdfa09f93a79d8efe0889d24324b831fb35126470165c9027 in /nats-streaming-server 
# Tue, 12 Jan 2021 00:19:14 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:19:16 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 12 Jan 2021 00:19:17 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bf50122b11c4b5e2fa295a9456a93489ad25dd1e9bfefda1d572da1a57418205`  
		Last Modified: Tue, 12 Jan 2021 00:20:01 GMT  
		Size: 5.4 MB (5439328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20.0` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:0f315491d4d14e634f971591c7f8bd0eb9aad59975fcdf867a51294df2e5efb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dba974517468c29a982c1b4a0b7744a93825122145a1dcc5f7e53c96119efa`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 11 Jan 2021 23:47:25 GMT
COPY file:5a251d4e6bafc9d9ea6f25cd37fd44252da405176da94cc580cdd663abecffa5 in /nats-streaming-server 
# Mon, 11 Jan 2021 23:47:26 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:47:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 11 Jan 2021 23:47:27 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:58239a1ea6494e431645c7ad156ed917333a248edbe6be76af8b7384d9339f07`  
		Last Modified: Mon, 11 Jan 2021 23:48:09 GMT  
		Size: 5.4 MB (5388538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20.0` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats-streaming@sha256:dc8cb861e9ebd507f6052f70f00e5cd153ed10f3ce94b514ca53b0b66d68e1a6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107290057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f45933a0476064ac026d83b04912423ee2e0e38a5a0a13d9f6dd101b42deccd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:22:30 GMT
RUN cmd /S /C #(nop) COPY file:f2450ffeda74e33f820191eccf78b6647ce56865170e966bfa8e72afe6e46c36 in C:\nats-streaming-server.exe 
# Tue, 12 Jan 2021 00:22:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:22:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:22:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9a7966c40d2ea4e2a3a9732b1971a90e2c947c7436138dfeecc7a5dd475850`  
		Last Modified: Tue, 12 Jan 2021 00:26:57 GMT  
		Size: 6.0 MB (6021865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8709fe81a73f9b62174f38547b2d9da1bffe292d51b1b93b8fd6c4f89a924e9`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 814.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3718c1b6d751147f39ee7c4a6f1c5cea284aa100dfce6a8e622a16c6456c7d18`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe5aba04f48a9d07940a1f43378efa11f913918e6ebcead455135c3d0346504`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 823.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20.0-alpine`

```console
$ docker pull nats-streaming@sha256:54ee921908bc93e1deb621ad5b769a4b1e66fd99781595cacb1e1f526cae5670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.20.0-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ee383fab395fb79ad35d3663e31ba2c1556e67dd1ae42c9a314b14f66d80afa6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8997281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2217d4d7856bf852cbd735ef2587447e243436346788e6acaf5f102bcfbf28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Tue, 12 Jan 2021 00:48:03 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:48:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 12 Jan 2021 00:48:05 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 12 Jan 2021 00:48:06 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:48:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 00:48:06 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9b99285c9495350a993a87920ea4ccf0c2c560a7047d0076af2648f08b7bea`  
		Last Modified: Tue, 12 Jan 2021 00:48:48 GMT  
		Size: 6.2 MB (6197794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244241c08cee6b44b104d2b942ec81d0a48351c78496d12ee991024881132576`  
		Last Modified: Tue, 12 Jan 2021 00:48:46 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20.0-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:18fd3ddc15d5b65b6ad1171abf76e359cca31b60730750546e0dc0368a805750
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8330755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0322ce6374b271fc98c0e0a12b42c00a722465006d75394c2ab41bbb47d50c46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Mon, 11 Jan 2021 23:53:38 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Mon, 11 Jan 2021 23:53:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 11 Jan 2021 23:53:43 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 11 Jan 2021 23:53:44 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:53:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Jan 2021 23:53:45 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54831e858eddfe2c245e8c154d4422ad61bc9a30c1cfe612ec35f7a12b1e529`  
		Last Modified: Mon, 11 Jan 2021 23:54:22 GMT  
		Size: 5.7 MB (5726171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412a9e8bb4d16b7ddec81004c2205411fc7b8830d0d2a0f3054a2fe0dc4664cd`  
		Last Modified: Mon, 11 Jan 2021 23:54:20 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20.0-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b41e2afb428f6345393616c70c1a9d2221db86ab84c6e37be6c252bebf974203
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8125466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfc9155e69d8a79c164c6c96d01ea612fb88e955066a7f2803d0054801875da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Tue, 12 Jan 2021 00:18:41 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:18:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 12 Jan 2021 00:18:54 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 12 Jan 2021 00:18:57 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:18:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 00:18:59 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9290155f6f3b723d2522ebaa0d1e2038dcd4f4c978c086bc43fd55a4d8284659`  
		Last Modified: Tue, 12 Jan 2021 00:19:43 GMT  
		Size: 5.7 MB (5717488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4715986f280e125e74cc7b430caa19329b3de9fcfcd40ae588f422be68c37ca`  
		Last Modified: Tue, 12 Jan 2021 00:19:42 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20.0-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ae8f52346c3d26a49ae885bf56785f3952c14c8622a97e18288ae0abedd51660
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f79e7574653a33192a8af07510cf1a7f03f5c02a77b49072304e701cf514cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Mon, 11 Jan 2021 23:47:10 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Mon, 11 Jan 2021 23:47:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 11 Jan 2021 23:47:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 11 Jan 2021 23:47:15 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:47:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Jan 2021 23:47:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e424273d6cedd00225b67fa1b47e0dd8bf4b2abfa19fbc27f7763f096aeb138`  
		Last Modified: Mon, 11 Jan 2021 23:47:54 GMT  
		Size: 5.7 MB (5668408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33979e718e15555239006f224ba6d995cf9d6d044a7f25493196839d4d5aed73`  
		Last Modified: Mon, 11 Jan 2021 23:47:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20.0-alpine3.12`

```console
$ docker pull nats-streaming@sha256:54ee921908bc93e1deb621ad5b769a4b1e66fd99781595cacb1e1f526cae5670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.20.0-alpine3.12` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ee383fab395fb79ad35d3663e31ba2c1556e67dd1ae42c9a314b14f66d80afa6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8997281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2217d4d7856bf852cbd735ef2587447e243436346788e6acaf5f102bcfbf28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Tue, 12 Jan 2021 00:48:03 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:48:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 12 Jan 2021 00:48:05 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 12 Jan 2021 00:48:06 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:48:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 00:48:06 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9b99285c9495350a993a87920ea4ccf0c2c560a7047d0076af2648f08b7bea`  
		Last Modified: Tue, 12 Jan 2021 00:48:48 GMT  
		Size: 6.2 MB (6197794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244241c08cee6b44b104d2b942ec81d0a48351c78496d12ee991024881132576`  
		Last Modified: Tue, 12 Jan 2021 00:48:46 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20.0-alpine3.12` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:18fd3ddc15d5b65b6ad1171abf76e359cca31b60730750546e0dc0368a805750
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8330755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0322ce6374b271fc98c0e0a12b42c00a722465006d75394c2ab41bbb47d50c46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Mon, 11 Jan 2021 23:53:38 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Mon, 11 Jan 2021 23:53:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 11 Jan 2021 23:53:43 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 11 Jan 2021 23:53:44 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:53:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Jan 2021 23:53:45 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54831e858eddfe2c245e8c154d4422ad61bc9a30c1cfe612ec35f7a12b1e529`  
		Last Modified: Mon, 11 Jan 2021 23:54:22 GMT  
		Size: 5.7 MB (5726171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412a9e8bb4d16b7ddec81004c2205411fc7b8830d0d2a0f3054a2fe0dc4664cd`  
		Last Modified: Mon, 11 Jan 2021 23:54:20 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20.0-alpine3.12` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b41e2afb428f6345393616c70c1a9d2221db86ab84c6e37be6c252bebf974203
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8125466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfc9155e69d8a79c164c6c96d01ea612fb88e955066a7f2803d0054801875da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Tue, 12 Jan 2021 00:18:41 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:18:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 12 Jan 2021 00:18:54 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 12 Jan 2021 00:18:57 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:18:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 00:18:59 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9290155f6f3b723d2522ebaa0d1e2038dcd4f4c978c086bc43fd55a4d8284659`  
		Last Modified: Tue, 12 Jan 2021 00:19:43 GMT  
		Size: 5.7 MB (5717488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4715986f280e125e74cc7b430caa19329b3de9fcfcd40ae588f422be68c37ca`  
		Last Modified: Tue, 12 Jan 2021 00:19:42 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20.0-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ae8f52346c3d26a49ae885bf56785f3952c14c8622a97e18288ae0abedd51660
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f79e7574653a33192a8af07510cf1a7f03f5c02a77b49072304e701cf514cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Mon, 11 Jan 2021 23:47:10 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Mon, 11 Jan 2021 23:47:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 11 Jan 2021 23:47:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 11 Jan 2021 23:47:15 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:47:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Jan 2021 23:47:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e424273d6cedd00225b67fa1b47e0dd8bf4b2abfa19fbc27f7763f096aeb138`  
		Last Modified: Mon, 11 Jan 2021 23:47:54 GMT  
		Size: 5.7 MB (5668408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33979e718e15555239006f224ba6d995cf9d6d044a7f25493196839d4d5aed73`  
		Last Modified: Mon, 11 Jan 2021 23:47:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20.0-linux`

```console
$ docker pull nats-streaming@sha256:f46b63443b02bc0089e72301ae260b1ef32ff25e755e67b633169945585ca12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.20.0-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:cd0162a7232de1eabe982554c8740e7edbac4747af3e99fa9bc38a480b4a4243
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1544c1524919e1458186fefae5f5ff415c37055742e531010fc2660b11db2339`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 12 Jan 2021 00:48:24 GMT
COPY file:acbca3cec2dc5172f21984b614cbcd90e6e4cf0bd9848c5ddcffb94615a02436 in /nats-streaming-server 
# Tue, 12 Jan 2021 00:48:24 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:48:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 12 Jan 2021 00:48:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0d51fde6ce3492f397e8a85dad354a9a45ab91310cf4abd6275101f3ef823587`  
		Last Modified: Tue, 12 Jan 2021 00:49:07 GMT  
		Size: 5.9 MB (5914730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20.0-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:bbb3d771f9232932017b9cb9b501734367bc3560eed790695be682d94a8f3573
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed880c2955fd126b0ce38471e90c9467c9c739f55b4c789cec1a4575a41d36f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 11 Jan 2021 23:53:53 GMT
COPY file:617b9b5366d0d437ce471ad0763bdd7d350496612583dc2c7044dcde4d32257e in /nats-streaming-server 
# Mon, 11 Jan 2021 23:53:54 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:53:54 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 11 Jan 2021 23:53:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7cffcff2c5b4913dac660d7456365492a0393b1aa6f1812f6b7b46b250e1970d`  
		Last Modified: Mon, 11 Jan 2021 23:54:39 GMT  
		Size: 5.4 MB (5444243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20.0-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b2d9250f9a4e3b25b2212f4e8c27c693cc5cfa0f83ca82a8005c90ae8372ab86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f1d3c5a1d429a3e2b1fc71f5bc023980c41d34ccb0a0482aca07b6cbb4d6f1`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 12 Jan 2021 00:19:09 GMT
COPY file:2b3fc04f11d3cc7cdfa09f93a79d8efe0889d24324b831fb35126470165c9027 in /nats-streaming-server 
# Tue, 12 Jan 2021 00:19:14 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:19:16 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 12 Jan 2021 00:19:17 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bf50122b11c4b5e2fa295a9456a93489ad25dd1e9bfefda1d572da1a57418205`  
		Last Modified: Tue, 12 Jan 2021 00:20:01 GMT  
		Size: 5.4 MB (5439328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20.0-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:0f315491d4d14e634f971591c7f8bd0eb9aad59975fcdf867a51294df2e5efb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dba974517468c29a982c1b4a0b7744a93825122145a1dcc5f7e53c96119efa`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 11 Jan 2021 23:47:25 GMT
COPY file:5a251d4e6bafc9d9ea6f25cd37fd44252da405176da94cc580cdd663abecffa5 in /nats-streaming-server 
# Mon, 11 Jan 2021 23:47:26 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:47:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 11 Jan 2021 23:47:27 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:58239a1ea6494e431645c7ad156ed917333a248edbe6be76af8b7384d9339f07`  
		Last Modified: Mon, 11 Jan 2021 23:48:09 GMT  
		Size: 5.4 MB (5388538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20.0-nanoserver`

```console
$ docker pull nats-streaming@sha256:327650283f674241324910a0f8feaa90317a150029496c2d027d86ee41002f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats-streaming:0.20.0-nanoserver` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats-streaming@sha256:dc8cb861e9ebd507f6052f70f00e5cd153ed10f3ce94b514ca53b0b66d68e1a6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107290057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f45933a0476064ac026d83b04912423ee2e0e38a5a0a13d9f6dd101b42deccd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:22:30 GMT
RUN cmd /S /C #(nop) COPY file:f2450ffeda74e33f820191eccf78b6647ce56865170e966bfa8e72afe6e46c36 in C:\nats-streaming-server.exe 
# Tue, 12 Jan 2021 00:22:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:22:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:22:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9a7966c40d2ea4e2a3a9732b1971a90e2c947c7436138dfeecc7a5dd475850`  
		Last Modified: Tue, 12 Jan 2021 00:26:57 GMT  
		Size: 6.0 MB (6021865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8709fe81a73f9b62174f38547b2d9da1bffe292d51b1b93b8fd6c4f89a924e9`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 814.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3718c1b6d751147f39ee7c4a6f1c5cea284aa100dfce6a8e622a16c6456c7d18`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe5aba04f48a9d07940a1f43378efa11f913918e6ebcead455135c3d0346504`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 823.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20.0-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:327650283f674241324910a0f8feaa90317a150029496c2d027d86ee41002f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats-streaming:0.20.0-nanoserver-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats-streaming@sha256:dc8cb861e9ebd507f6052f70f00e5cd153ed10f3ce94b514ca53b0b66d68e1a6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107290057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f45933a0476064ac026d83b04912423ee2e0e38a5a0a13d9f6dd101b42deccd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:22:30 GMT
RUN cmd /S /C #(nop) COPY file:f2450ffeda74e33f820191eccf78b6647ce56865170e966bfa8e72afe6e46c36 in C:\nats-streaming-server.exe 
# Tue, 12 Jan 2021 00:22:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:22:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:22:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9a7966c40d2ea4e2a3a9732b1971a90e2c947c7436138dfeecc7a5dd475850`  
		Last Modified: Tue, 12 Jan 2021 00:26:57 GMT  
		Size: 6.0 MB (6021865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8709fe81a73f9b62174f38547b2d9da1bffe292d51b1b93b8fd6c4f89a924e9`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 814.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3718c1b6d751147f39ee7c4a6f1c5cea284aa100dfce6a8e622a16c6456c7d18`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe5aba04f48a9d07940a1f43378efa11f913918e6ebcead455135c3d0346504`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 823.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20.0-scratch`

```console
$ docker pull nats-streaming@sha256:f46b63443b02bc0089e72301ae260b1ef32ff25e755e67b633169945585ca12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.20.0-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:cd0162a7232de1eabe982554c8740e7edbac4747af3e99fa9bc38a480b4a4243
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1544c1524919e1458186fefae5f5ff415c37055742e531010fc2660b11db2339`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 12 Jan 2021 00:48:24 GMT
COPY file:acbca3cec2dc5172f21984b614cbcd90e6e4cf0bd9848c5ddcffb94615a02436 in /nats-streaming-server 
# Tue, 12 Jan 2021 00:48:24 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:48:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 12 Jan 2021 00:48:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0d51fde6ce3492f397e8a85dad354a9a45ab91310cf4abd6275101f3ef823587`  
		Last Modified: Tue, 12 Jan 2021 00:49:07 GMT  
		Size: 5.9 MB (5914730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20.0-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:bbb3d771f9232932017b9cb9b501734367bc3560eed790695be682d94a8f3573
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed880c2955fd126b0ce38471e90c9467c9c739f55b4c789cec1a4575a41d36f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 11 Jan 2021 23:53:53 GMT
COPY file:617b9b5366d0d437ce471ad0763bdd7d350496612583dc2c7044dcde4d32257e in /nats-streaming-server 
# Mon, 11 Jan 2021 23:53:54 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:53:54 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 11 Jan 2021 23:53:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7cffcff2c5b4913dac660d7456365492a0393b1aa6f1812f6b7b46b250e1970d`  
		Last Modified: Mon, 11 Jan 2021 23:54:39 GMT  
		Size: 5.4 MB (5444243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20.0-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b2d9250f9a4e3b25b2212f4e8c27c693cc5cfa0f83ca82a8005c90ae8372ab86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f1d3c5a1d429a3e2b1fc71f5bc023980c41d34ccb0a0482aca07b6cbb4d6f1`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 12 Jan 2021 00:19:09 GMT
COPY file:2b3fc04f11d3cc7cdfa09f93a79d8efe0889d24324b831fb35126470165c9027 in /nats-streaming-server 
# Tue, 12 Jan 2021 00:19:14 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:19:16 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 12 Jan 2021 00:19:17 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bf50122b11c4b5e2fa295a9456a93489ad25dd1e9bfefda1d572da1a57418205`  
		Last Modified: Tue, 12 Jan 2021 00:20:01 GMT  
		Size: 5.4 MB (5439328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20.0-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:0f315491d4d14e634f971591c7f8bd0eb9aad59975fcdf867a51294df2e5efb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dba974517468c29a982c1b4a0b7744a93825122145a1dcc5f7e53c96119efa`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 11 Jan 2021 23:47:25 GMT
COPY file:5a251d4e6bafc9d9ea6f25cd37fd44252da405176da94cc580cdd663abecffa5 in /nats-streaming-server 
# Mon, 11 Jan 2021 23:47:26 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:47:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 11 Jan 2021 23:47:27 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:58239a1ea6494e431645c7ad156ed917333a248edbe6be76af8b7384d9339f07`  
		Last Modified: Mon, 11 Jan 2021 23:48:09 GMT  
		Size: 5.4 MB (5388538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20.0-windowsservercore`

```console
$ docker pull nats-streaming@sha256:ab4f90fa36638c93e8552a653422527a599d4a73f996c21353c484c6dc0a154e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64
	-	windows version 10.0.14393.4104; amd64

### `nats-streaming:0.20.0-windowsservercore` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats-streaming@sha256:1e9246d04cadc2e2c8c9f393c081c3f899ee17cc0c2604e670f4b2dfb473ae78
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2410998451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880b431ca994738c273eb95d89d0200e5faf1def000165c43c3b6d2195fb6ac7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 14:02:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:36:04 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:20:16 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:20:17 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.20.0/nats-streaming-server-v0.20.0-windows-amd64.zip
# Tue, 12 Jan 2021 00:20:18 GMT
ENV GIT_DOWNLOAD_SHA256=26ae310d3ec11617d380106a769236a6dc2209769c0c36d15cb6736db1b589cb
# Tue, 12 Jan 2021 00:20:50 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Jan 2021 00:22:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 12 Jan 2021 00:22:09 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:22:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:22:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:240407eb82b6591b0574396ec829a4a5cd9a75257a4663f9876942995275965d`  
		Last Modified: Wed, 09 Dec 2020 17:10:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9257be76bd37cad15d45905ec5910266409794a9dbd8a0428174f8b2f352a`  
		Last Modified: Wed, 09 Dec 2020 17:42:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ea2225c77eadc0189bc20fb84afed780b270881cda1af919808b4659ddfde4`  
		Last Modified: Tue, 12 Jan 2021 00:26:38 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e11834207f6dd2d9b771b24f539c5e44ba9c03e436eab5fb3d14b440761244`  
		Last Modified: Tue, 12 Jan 2021 00:26:36 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3d13a0cbb1f04703c664ea56832b37d3c72620db9f1322e3987b5939e63be7`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1b5c2d8ee1e18e7fd1d2758bb1d910114688b48e87b48b612bc04e7f9ab565`  
		Last Modified: Tue, 12 Jan 2021 00:26:35 GMT  
		Size: 4.9 MB (4866042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3b650e7eae667685fbdb190173a13f5d5f514356e6f86b28a5e117d8d365e5`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 15.2 MB (15248954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f14a725380678eee4b1fb7eb05c4604f8bcf3d3dbe55a664242327d3a889d9`  
		Last Modified: Tue, 12 Jan 2021 00:26:33 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968d5703b7cafe8fb35b9c28e5f6d99df9c64e2b9272652cd585e1505eda409`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd142e8fb60d24af64f85a7309313043c3e90c22e5f9ad18b37fcb2b05bb10cf`  
		Last Modified: Tue, 12 Jan 2021 00:26:30 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20.0-windowsservercore` - windows version 10.0.14393.4104; amd64

```console
$ docker pull nats-streaming@sha256:1c76108446fc8743e3272a3e5ebe44713cb0f271f791afbcb180b164eeceb30a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5790486404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677b831b855e37cf8ca7b05f3d97e02d9acd7b7f88c3e2cb94350d97dfd45506`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 14:41:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:38:10 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:22:38 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:22:39 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.20.0/nats-streaming-server-v0.20.0-windows-amd64.zip
# Tue, 12 Jan 2021 00:22:40 GMT
ENV GIT_DOWNLOAD_SHA256=26ae310d3ec11617d380106a769236a6dc2209769c0c36d15cb6736db1b589cb
# Tue, 12 Jan 2021 00:23:47 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Jan 2021 00:25:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 12 Jan 2021 00:25:47 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:25:48 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:25:49 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5a79f8be42bf1c358ccc82f32c1481de95c393ef97e712a321c1440d132fda9`  
		Last Modified: Wed, 09 Dec 2020 17:11:03 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d972336c8bcee0026c76e8f199cef405112a70aeef9917f07d2859f15162c1`  
		Last Modified: Wed, 09 Dec 2020 17:42:56 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36f4ebf3f9e4f08ccee6bfa20099991e715ee2894afc2a5ab488f99abde352e`  
		Last Modified: Tue, 12 Jan 2021 00:27:18 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbb72f3ad396e481a0b277ce3e34e967c03d0508866752c073f88ba79fe5ad9`  
		Last Modified: Tue, 12 Jan 2021 00:27:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5b181e3fbbd7a07117dea46bb1665bf7cb7d1c63893ba7e34253bc80329005`  
		Last Modified: Tue, 12 Jan 2021 00:27:17 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f188787bf90e9475900fcfe23b4560d8a3c339da882a6bd6a627200f050de787`  
		Last Modified: Tue, 12 Jan 2021 00:27:16 GMT  
		Size: 5.5 MB (5540955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648f80f9fceb0f132e4ecd6f30d636df20cfb7fd51954ae9945a657d622e7875`  
		Last Modified: Tue, 12 Jan 2021 00:27:32 GMT  
		Size: 16.1 MB (16092606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89c59b6b1299bdb040513b474b6d8a594a4bc7dbaded7aa867723807a1fc11a`  
		Last Modified: Tue, 12 Jan 2021 00:27:13 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec9cf99b11036b9be139f4bc0016e3ec80a666200e52ff82978706a12fa30b3`  
		Last Modified: Tue, 12 Jan 2021 00:27:13 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7278eff7db06794f2daef6b524a6e0ae1a8fc04d3924fb1bac92b6e449b539`  
		Last Modified: Tue, 12 Jan 2021 00:27:12 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20.0-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:ced4889038416616798fd8652bb25df54adc1f69b66e10590585517f761f3fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats-streaming:0.20.0-windowsservercore-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats-streaming@sha256:1e9246d04cadc2e2c8c9f393c081c3f899ee17cc0c2604e670f4b2dfb473ae78
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2410998451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880b431ca994738c273eb95d89d0200e5faf1def000165c43c3b6d2195fb6ac7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 14:02:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:36:04 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:20:16 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:20:17 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.20.0/nats-streaming-server-v0.20.0-windows-amd64.zip
# Tue, 12 Jan 2021 00:20:18 GMT
ENV GIT_DOWNLOAD_SHA256=26ae310d3ec11617d380106a769236a6dc2209769c0c36d15cb6736db1b589cb
# Tue, 12 Jan 2021 00:20:50 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Jan 2021 00:22:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 12 Jan 2021 00:22:09 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:22:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:22:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:240407eb82b6591b0574396ec829a4a5cd9a75257a4663f9876942995275965d`  
		Last Modified: Wed, 09 Dec 2020 17:10:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9257be76bd37cad15d45905ec5910266409794a9dbd8a0428174f8b2f352a`  
		Last Modified: Wed, 09 Dec 2020 17:42:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ea2225c77eadc0189bc20fb84afed780b270881cda1af919808b4659ddfde4`  
		Last Modified: Tue, 12 Jan 2021 00:26:38 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e11834207f6dd2d9b771b24f539c5e44ba9c03e436eab5fb3d14b440761244`  
		Last Modified: Tue, 12 Jan 2021 00:26:36 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3d13a0cbb1f04703c664ea56832b37d3c72620db9f1322e3987b5939e63be7`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1b5c2d8ee1e18e7fd1d2758bb1d910114688b48e87b48b612bc04e7f9ab565`  
		Last Modified: Tue, 12 Jan 2021 00:26:35 GMT  
		Size: 4.9 MB (4866042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3b650e7eae667685fbdb190173a13f5d5f514356e6f86b28a5e117d8d365e5`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 15.2 MB (15248954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f14a725380678eee4b1fb7eb05c4604f8bcf3d3dbe55a664242327d3a889d9`  
		Last Modified: Tue, 12 Jan 2021 00:26:33 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968d5703b7cafe8fb35b9c28e5f6d99df9c64e2b9272652cd585e1505eda409`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd142e8fb60d24af64f85a7309313043c3e90c22e5f9ad18b37fcb2b05bb10cf`  
		Last Modified: Tue, 12 Jan 2021 00:26:30 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20.0-windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:713e3b909647fd8bd890a4c0110e154cdad36588a4ff949fafe11a65cc7df24b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4104; amd64

### `nats-streaming:0.20.0-windowsservercore-ltsc2016` - windows version 10.0.14393.4104; amd64

```console
$ docker pull nats-streaming@sha256:1c76108446fc8743e3272a3e5ebe44713cb0f271f791afbcb180b164eeceb30a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5790486404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677b831b855e37cf8ca7b05f3d97e02d9acd7b7f88c3e2cb94350d97dfd45506`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 14:41:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:38:10 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:22:38 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:22:39 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.20.0/nats-streaming-server-v0.20.0-windows-amd64.zip
# Tue, 12 Jan 2021 00:22:40 GMT
ENV GIT_DOWNLOAD_SHA256=26ae310d3ec11617d380106a769236a6dc2209769c0c36d15cb6736db1b589cb
# Tue, 12 Jan 2021 00:23:47 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Jan 2021 00:25:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 12 Jan 2021 00:25:47 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:25:48 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:25:49 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5a79f8be42bf1c358ccc82f32c1481de95c393ef97e712a321c1440d132fda9`  
		Last Modified: Wed, 09 Dec 2020 17:11:03 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d972336c8bcee0026c76e8f199cef405112a70aeef9917f07d2859f15162c1`  
		Last Modified: Wed, 09 Dec 2020 17:42:56 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36f4ebf3f9e4f08ccee6bfa20099991e715ee2894afc2a5ab488f99abde352e`  
		Last Modified: Tue, 12 Jan 2021 00:27:18 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbb72f3ad396e481a0b277ce3e34e967c03d0508866752c073f88ba79fe5ad9`  
		Last Modified: Tue, 12 Jan 2021 00:27:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5b181e3fbbd7a07117dea46bb1665bf7cb7d1c63893ba7e34253bc80329005`  
		Last Modified: Tue, 12 Jan 2021 00:27:17 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f188787bf90e9475900fcfe23b4560d8a3c339da882a6bd6a627200f050de787`  
		Last Modified: Tue, 12 Jan 2021 00:27:16 GMT  
		Size: 5.5 MB (5540955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648f80f9fceb0f132e4ecd6f30d636df20cfb7fd51954ae9945a657d622e7875`  
		Last Modified: Tue, 12 Jan 2021 00:27:32 GMT  
		Size: 16.1 MB (16092606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89c59b6b1299bdb040513b474b6d8a594a4bc7dbaded7aa867723807a1fc11a`  
		Last Modified: Tue, 12 Jan 2021 00:27:13 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec9cf99b11036b9be139f4bc0016e3ec80a666200e52ff82978706a12fa30b3`  
		Last Modified: Tue, 12 Jan 2021 00:27:13 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7278eff7db06794f2daef6b524a6e0ae1a8fc04d3924fb1bac92b6e449b539`  
		Last Modified: Tue, 12 Jan 2021 00:27:12 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20-alpine`

```console
$ docker pull nats-streaming@sha256:54ee921908bc93e1deb621ad5b769a4b1e66fd99781595cacb1e1f526cae5670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.20-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ee383fab395fb79ad35d3663e31ba2c1556e67dd1ae42c9a314b14f66d80afa6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8997281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2217d4d7856bf852cbd735ef2587447e243436346788e6acaf5f102bcfbf28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Tue, 12 Jan 2021 00:48:03 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:48:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 12 Jan 2021 00:48:05 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 12 Jan 2021 00:48:06 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:48:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 00:48:06 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9b99285c9495350a993a87920ea4ccf0c2c560a7047d0076af2648f08b7bea`  
		Last Modified: Tue, 12 Jan 2021 00:48:48 GMT  
		Size: 6.2 MB (6197794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244241c08cee6b44b104d2b942ec81d0a48351c78496d12ee991024881132576`  
		Last Modified: Tue, 12 Jan 2021 00:48:46 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:18fd3ddc15d5b65b6ad1171abf76e359cca31b60730750546e0dc0368a805750
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8330755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0322ce6374b271fc98c0e0a12b42c00a722465006d75394c2ab41bbb47d50c46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Mon, 11 Jan 2021 23:53:38 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Mon, 11 Jan 2021 23:53:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 11 Jan 2021 23:53:43 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 11 Jan 2021 23:53:44 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:53:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Jan 2021 23:53:45 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54831e858eddfe2c245e8c154d4422ad61bc9a30c1cfe612ec35f7a12b1e529`  
		Last Modified: Mon, 11 Jan 2021 23:54:22 GMT  
		Size: 5.7 MB (5726171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412a9e8bb4d16b7ddec81004c2205411fc7b8830d0d2a0f3054a2fe0dc4664cd`  
		Last Modified: Mon, 11 Jan 2021 23:54:20 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b41e2afb428f6345393616c70c1a9d2221db86ab84c6e37be6c252bebf974203
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8125466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfc9155e69d8a79c164c6c96d01ea612fb88e955066a7f2803d0054801875da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Tue, 12 Jan 2021 00:18:41 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:18:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 12 Jan 2021 00:18:54 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 12 Jan 2021 00:18:57 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:18:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 00:18:59 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9290155f6f3b723d2522ebaa0d1e2038dcd4f4c978c086bc43fd55a4d8284659`  
		Last Modified: Tue, 12 Jan 2021 00:19:43 GMT  
		Size: 5.7 MB (5717488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4715986f280e125e74cc7b430caa19329b3de9fcfcd40ae588f422be68c37ca`  
		Last Modified: Tue, 12 Jan 2021 00:19:42 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ae8f52346c3d26a49ae885bf56785f3952c14c8622a97e18288ae0abedd51660
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f79e7574653a33192a8af07510cf1a7f03f5c02a77b49072304e701cf514cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Mon, 11 Jan 2021 23:47:10 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Mon, 11 Jan 2021 23:47:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 11 Jan 2021 23:47:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 11 Jan 2021 23:47:15 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:47:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Jan 2021 23:47:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e424273d6cedd00225b67fa1b47e0dd8bf4b2abfa19fbc27f7763f096aeb138`  
		Last Modified: Mon, 11 Jan 2021 23:47:54 GMT  
		Size: 5.7 MB (5668408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33979e718e15555239006f224ba6d995cf9d6d044a7f25493196839d4d5aed73`  
		Last Modified: Mon, 11 Jan 2021 23:47:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20-alpine3.12`

```console
$ docker pull nats-streaming@sha256:54ee921908bc93e1deb621ad5b769a4b1e66fd99781595cacb1e1f526cae5670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.20-alpine3.12` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ee383fab395fb79ad35d3663e31ba2c1556e67dd1ae42c9a314b14f66d80afa6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8997281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2217d4d7856bf852cbd735ef2587447e243436346788e6acaf5f102bcfbf28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Tue, 12 Jan 2021 00:48:03 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:48:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 12 Jan 2021 00:48:05 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 12 Jan 2021 00:48:06 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:48:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 00:48:06 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9b99285c9495350a993a87920ea4ccf0c2c560a7047d0076af2648f08b7bea`  
		Last Modified: Tue, 12 Jan 2021 00:48:48 GMT  
		Size: 6.2 MB (6197794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244241c08cee6b44b104d2b942ec81d0a48351c78496d12ee991024881132576`  
		Last Modified: Tue, 12 Jan 2021 00:48:46 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20-alpine3.12` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:18fd3ddc15d5b65b6ad1171abf76e359cca31b60730750546e0dc0368a805750
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8330755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0322ce6374b271fc98c0e0a12b42c00a722465006d75394c2ab41bbb47d50c46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Mon, 11 Jan 2021 23:53:38 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Mon, 11 Jan 2021 23:53:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 11 Jan 2021 23:53:43 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 11 Jan 2021 23:53:44 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:53:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Jan 2021 23:53:45 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54831e858eddfe2c245e8c154d4422ad61bc9a30c1cfe612ec35f7a12b1e529`  
		Last Modified: Mon, 11 Jan 2021 23:54:22 GMT  
		Size: 5.7 MB (5726171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412a9e8bb4d16b7ddec81004c2205411fc7b8830d0d2a0f3054a2fe0dc4664cd`  
		Last Modified: Mon, 11 Jan 2021 23:54:20 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20-alpine3.12` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b41e2afb428f6345393616c70c1a9d2221db86ab84c6e37be6c252bebf974203
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8125466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfc9155e69d8a79c164c6c96d01ea612fb88e955066a7f2803d0054801875da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Tue, 12 Jan 2021 00:18:41 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:18:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 12 Jan 2021 00:18:54 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 12 Jan 2021 00:18:57 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:18:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 00:18:59 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9290155f6f3b723d2522ebaa0d1e2038dcd4f4c978c086bc43fd55a4d8284659`  
		Last Modified: Tue, 12 Jan 2021 00:19:43 GMT  
		Size: 5.7 MB (5717488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4715986f280e125e74cc7b430caa19329b3de9fcfcd40ae588f422be68c37ca`  
		Last Modified: Tue, 12 Jan 2021 00:19:42 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ae8f52346c3d26a49ae885bf56785f3952c14c8622a97e18288ae0abedd51660
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f79e7574653a33192a8af07510cf1a7f03f5c02a77b49072304e701cf514cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Mon, 11 Jan 2021 23:47:10 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Mon, 11 Jan 2021 23:47:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 11 Jan 2021 23:47:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 11 Jan 2021 23:47:15 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:47:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Jan 2021 23:47:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e424273d6cedd00225b67fa1b47e0dd8bf4b2abfa19fbc27f7763f096aeb138`  
		Last Modified: Mon, 11 Jan 2021 23:47:54 GMT  
		Size: 5.7 MB (5668408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33979e718e15555239006f224ba6d995cf9d6d044a7f25493196839d4d5aed73`  
		Last Modified: Mon, 11 Jan 2021 23:47:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20-linux`

```console
$ docker pull nats-streaming@sha256:f46b63443b02bc0089e72301ae260b1ef32ff25e755e67b633169945585ca12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.20-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:cd0162a7232de1eabe982554c8740e7edbac4747af3e99fa9bc38a480b4a4243
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1544c1524919e1458186fefae5f5ff415c37055742e531010fc2660b11db2339`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 12 Jan 2021 00:48:24 GMT
COPY file:acbca3cec2dc5172f21984b614cbcd90e6e4cf0bd9848c5ddcffb94615a02436 in /nats-streaming-server 
# Tue, 12 Jan 2021 00:48:24 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:48:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 12 Jan 2021 00:48:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0d51fde6ce3492f397e8a85dad354a9a45ab91310cf4abd6275101f3ef823587`  
		Last Modified: Tue, 12 Jan 2021 00:49:07 GMT  
		Size: 5.9 MB (5914730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:bbb3d771f9232932017b9cb9b501734367bc3560eed790695be682d94a8f3573
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed880c2955fd126b0ce38471e90c9467c9c739f55b4c789cec1a4575a41d36f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 11 Jan 2021 23:53:53 GMT
COPY file:617b9b5366d0d437ce471ad0763bdd7d350496612583dc2c7044dcde4d32257e in /nats-streaming-server 
# Mon, 11 Jan 2021 23:53:54 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:53:54 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 11 Jan 2021 23:53:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7cffcff2c5b4913dac660d7456365492a0393b1aa6f1812f6b7b46b250e1970d`  
		Last Modified: Mon, 11 Jan 2021 23:54:39 GMT  
		Size: 5.4 MB (5444243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b2d9250f9a4e3b25b2212f4e8c27c693cc5cfa0f83ca82a8005c90ae8372ab86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f1d3c5a1d429a3e2b1fc71f5bc023980c41d34ccb0a0482aca07b6cbb4d6f1`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 12 Jan 2021 00:19:09 GMT
COPY file:2b3fc04f11d3cc7cdfa09f93a79d8efe0889d24324b831fb35126470165c9027 in /nats-streaming-server 
# Tue, 12 Jan 2021 00:19:14 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:19:16 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 12 Jan 2021 00:19:17 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bf50122b11c4b5e2fa295a9456a93489ad25dd1e9bfefda1d572da1a57418205`  
		Last Modified: Tue, 12 Jan 2021 00:20:01 GMT  
		Size: 5.4 MB (5439328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:0f315491d4d14e634f971591c7f8bd0eb9aad59975fcdf867a51294df2e5efb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dba974517468c29a982c1b4a0b7744a93825122145a1dcc5f7e53c96119efa`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 11 Jan 2021 23:47:25 GMT
COPY file:5a251d4e6bafc9d9ea6f25cd37fd44252da405176da94cc580cdd663abecffa5 in /nats-streaming-server 
# Mon, 11 Jan 2021 23:47:26 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:47:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 11 Jan 2021 23:47:27 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:58239a1ea6494e431645c7ad156ed917333a248edbe6be76af8b7384d9339f07`  
		Last Modified: Mon, 11 Jan 2021 23:48:09 GMT  
		Size: 5.4 MB (5388538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20-nanoserver`

```console
$ docker pull nats-streaming@sha256:327650283f674241324910a0f8feaa90317a150029496c2d027d86ee41002f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats-streaming:0.20-nanoserver` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats-streaming@sha256:dc8cb861e9ebd507f6052f70f00e5cd153ed10f3ce94b514ca53b0b66d68e1a6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107290057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f45933a0476064ac026d83b04912423ee2e0e38a5a0a13d9f6dd101b42deccd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:22:30 GMT
RUN cmd /S /C #(nop) COPY file:f2450ffeda74e33f820191eccf78b6647ce56865170e966bfa8e72afe6e46c36 in C:\nats-streaming-server.exe 
# Tue, 12 Jan 2021 00:22:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:22:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:22:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9a7966c40d2ea4e2a3a9732b1971a90e2c947c7436138dfeecc7a5dd475850`  
		Last Modified: Tue, 12 Jan 2021 00:26:57 GMT  
		Size: 6.0 MB (6021865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8709fe81a73f9b62174f38547b2d9da1bffe292d51b1b93b8fd6c4f89a924e9`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 814.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3718c1b6d751147f39ee7c4a6f1c5cea284aa100dfce6a8e622a16c6456c7d18`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe5aba04f48a9d07940a1f43378efa11f913918e6ebcead455135c3d0346504`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 823.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:327650283f674241324910a0f8feaa90317a150029496c2d027d86ee41002f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats-streaming:0.20-nanoserver-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats-streaming@sha256:dc8cb861e9ebd507f6052f70f00e5cd153ed10f3ce94b514ca53b0b66d68e1a6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107290057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f45933a0476064ac026d83b04912423ee2e0e38a5a0a13d9f6dd101b42deccd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:22:30 GMT
RUN cmd /S /C #(nop) COPY file:f2450ffeda74e33f820191eccf78b6647ce56865170e966bfa8e72afe6e46c36 in C:\nats-streaming-server.exe 
# Tue, 12 Jan 2021 00:22:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:22:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:22:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9a7966c40d2ea4e2a3a9732b1971a90e2c947c7436138dfeecc7a5dd475850`  
		Last Modified: Tue, 12 Jan 2021 00:26:57 GMT  
		Size: 6.0 MB (6021865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8709fe81a73f9b62174f38547b2d9da1bffe292d51b1b93b8fd6c4f89a924e9`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 814.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3718c1b6d751147f39ee7c4a6f1c5cea284aa100dfce6a8e622a16c6456c7d18`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe5aba04f48a9d07940a1f43378efa11f913918e6ebcead455135c3d0346504`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 823.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20-scratch`

```console
$ docker pull nats-streaming@sha256:f46b63443b02bc0089e72301ae260b1ef32ff25e755e67b633169945585ca12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.20-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:cd0162a7232de1eabe982554c8740e7edbac4747af3e99fa9bc38a480b4a4243
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1544c1524919e1458186fefae5f5ff415c37055742e531010fc2660b11db2339`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 12 Jan 2021 00:48:24 GMT
COPY file:acbca3cec2dc5172f21984b614cbcd90e6e4cf0bd9848c5ddcffb94615a02436 in /nats-streaming-server 
# Tue, 12 Jan 2021 00:48:24 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:48:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 12 Jan 2021 00:48:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0d51fde6ce3492f397e8a85dad354a9a45ab91310cf4abd6275101f3ef823587`  
		Last Modified: Tue, 12 Jan 2021 00:49:07 GMT  
		Size: 5.9 MB (5914730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:bbb3d771f9232932017b9cb9b501734367bc3560eed790695be682d94a8f3573
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed880c2955fd126b0ce38471e90c9467c9c739f55b4c789cec1a4575a41d36f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 11 Jan 2021 23:53:53 GMT
COPY file:617b9b5366d0d437ce471ad0763bdd7d350496612583dc2c7044dcde4d32257e in /nats-streaming-server 
# Mon, 11 Jan 2021 23:53:54 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:53:54 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 11 Jan 2021 23:53:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7cffcff2c5b4913dac660d7456365492a0393b1aa6f1812f6b7b46b250e1970d`  
		Last Modified: Mon, 11 Jan 2021 23:54:39 GMT  
		Size: 5.4 MB (5444243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b2d9250f9a4e3b25b2212f4e8c27c693cc5cfa0f83ca82a8005c90ae8372ab86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f1d3c5a1d429a3e2b1fc71f5bc023980c41d34ccb0a0482aca07b6cbb4d6f1`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 12 Jan 2021 00:19:09 GMT
COPY file:2b3fc04f11d3cc7cdfa09f93a79d8efe0889d24324b831fb35126470165c9027 in /nats-streaming-server 
# Tue, 12 Jan 2021 00:19:14 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:19:16 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 12 Jan 2021 00:19:17 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bf50122b11c4b5e2fa295a9456a93489ad25dd1e9bfefda1d572da1a57418205`  
		Last Modified: Tue, 12 Jan 2021 00:20:01 GMT  
		Size: 5.4 MB (5439328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:0f315491d4d14e634f971591c7f8bd0eb9aad59975fcdf867a51294df2e5efb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dba974517468c29a982c1b4a0b7744a93825122145a1dcc5f7e53c96119efa`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 11 Jan 2021 23:47:25 GMT
COPY file:5a251d4e6bafc9d9ea6f25cd37fd44252da405176da94cc580cdd663abecffa5 in /nats-streaming-server 
# Mon, 11 Jan 2021 23:47:26 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:47:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 11 Jan 2021 23:47:27 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:58239a1ea6494e431645c7ad156ed917333a248edbe6be76af8b7384d9339f07`  
		Last Modified: Mon, 11 Jan 2021 23:48:09 GMT  
		Size: 5.4 MB (5388538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20-windowsservercore`

```console
$ docker pull nats-streaming@sha256:ab4f90fa36638c93e8552a653422527a599d4a73f996c21353c484c6dc0a154e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64
	-	windows version 10.0.14393.4104; amd64

### `nats-streaming:0.20-windowsservercore` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats-streaming@sha256:1e9246d04cadc2e2c8c9f393c081c3f899ee17cc0c2604e670f4b2dfb473ae78
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2410998451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880b431ca994738c273eb95d89d0200e5faf1def000165c43c3b6d2195fb6ac7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 14:02:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:36:04 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:20:16 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:20:17 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.20.0/nats-streaming-server-v0.20.0-windows-amd64.zip
# Tue, 12 Jan 2021 00:20:18 GMT
ENV GIT_DOWNLOAD_SHA256=26ae310d3ec11617d380106a769236a6dc2209769c0c36d15cb6736db1b589cb
# Tue, 12 Jan 2021 00:20:50 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Jan 2021 00:22:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 12 Jan 2021 00:22:09 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:22:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:22:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:240407eb82b6591b0574396ec829a4a5cd9a75257a4663f9876942995275965d`  
		Last Modified: Wed, 09 Dec 2020 17:10:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9257be76bd37cad15d45905ec5910266409794a9dbd8a0428174f8b2f352a`  
		Last Modified: Wed, 09 Dec 2020 17:42:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ea2225c77eadc0189bc20fb84afed780b270881cda1af919808b4659ddfde4`  
		Last Modified: Tue, 12 Jan 2021 00:26:38 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e11834207f6dd2d9b771b24f539c5e44ba9c03e436eab5fb3d14b440761244`  
		Last Modified: Tue, 12 Jan 2021 00:26:36 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3d13a0cbb1f04703c664ea56832b37d3c72620db9f1322e3987b5939e63be7`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1b5c2d8ee1e18e7fd1d2758bb1d910114688b48e87b48b612bc04e7f9ab565`  
		Last Modified: Tue, 12 Jan 2021 00:26:35 GMT  
		Size: 4.9 MB (4866042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3b650e7eae667685fbdb190173a13f5d5f514356e6f86b28a5e117d8d365e5`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 15.2 MB (15248954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f14a725380678eee4b1fb7eb05c4604f8bcf3d3dbe55a664242327d3a889d9`  
		Last Modified: Tue, 12 Jan 2021 00:26:33 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968d5703b7cafe8fb35b9c28e5f6d99df9c64e2b9272652cd585e1505eda409`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd142e8fb60d24af64f85a7309313043c3e90c22e5f9ad18b37fcb2b05bb10cf`  
		Last Modified: Tue, 12 Jan 2021 00:26:30 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.20-windowsservercore` - windows version 10.0.14393.4104; amd64

```console
$ docker pull nats-streaming@sha256:1c76108446fc8743e3272a3e5ebe44713cb0f271f791afbcb180b164eeceb30a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5790486404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677b831b855e37cf8ca7b05f3d97e02d9acd7b7f88c3e2cb94350d97dfd45506`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 14:41:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:38:10 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:22:38 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:22:39 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.20.0/nats-streaming-server-v0.20.0-windows-amd64.zip
# Tue, 12 Jan 2021 00:22:40 GMT
ENV GIT_DOWNLOAD_SHA256=26ae310d3ec11617d380106a769236a6dc2209769c0c36d15cb6736db1b589cb
# Tue, 12 Jan 2021 00:23:47 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Jan 2021 00:25:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 12 Jan 2021 00:25:47 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:25:48 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:25:49 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5a79f8be42bf1c358ccc82f32c1481de95c393ef97e712a321c1440d132fda9`  
		Last Modified: Wed, 09 Dec 2020 17:11:03 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d972336c8bcee0026c76e8f199cef405112a70aeef9917f07d2859f15162c1`  
		Last Modified: Wed, 09 Dec 2020 17:42:56 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36f4ebf3f9e4f08ccee6bfa20099991e715ee2894afc2a5ab488f99abde352e`  
		Last Modified: Tue, 12 Jan 2021 00:27:18 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbb72f3ad396e481a0b277ce3e34e967c03d0508866752c073f88ba79fe5ad9`  
		Last Modified: Tue, 12 Jan 2021 00:27:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5b181e3fbbd7a07117dea46bb1665bf7cb7d1c63893ba7e34253bc80329005`  
		Last Modified: Tue, 12 Jan 2021 00:27:17 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f188787bf90e9475900fcfe23b4560d8a3c339da882a6bd6a627200f050de787`  
		Last Modified: Tue, 12 Jan 2021 00:27:16 GMT  
		Size: 5.5 MB (5540955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648f80f9fceb0f132e4ecd6f30d636df20cfb7fd51954ae9945a657d622e7875`  
		Last Modified: Tue, 12 Jan 2021 00:27:32 GMT  
		Size: 16.1 MB (16092606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89c59b6b1299bdb040513b474b6d8a594a4bc7dbaded7aa867723807a1fc11a`  
		Last Modified: Tue, 12 Jan 2021 00:27:13 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec9cf99b11036b9be139f4bc0016e3ec80a666200e52ff82978706a12fa30b3`  
		Last Modified: Tue, 12 Jan 2021 00:27:13 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7278eff7db06794f2daef6b524a6e0ae1a8fc04d3924fb1bac92b6e449b539`  
		Last Modified: Tue, 12 Jan 2021 00:27:12 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:ced4889038416616798fd8652bb25df54adc1f69b66e10590585517f761f3fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats-streaming:0.20-windowsservercore-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats-streaming@sha256:1e9246d04cadc2e2c8c9f393c081c3f899ee17cc0c2604e670f4b2dfb473ae78
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2410998451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880b431ca994738c273eb95d89d0200e5faf1def000165c43c3b6d2195fb6ac7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 14:02:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:36:04 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:20:16 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:20:17 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.20.0/nats-streaming-server-v0.20.0-windows-amd64.zip
# Tue, 12 Jan 2021 00:20:18 GMT
ENV GIT_DOWNLOAD_SHA256=26ae310d3ec11617d380106a769236a6dc2209769c0c36d15cb6736db1b589cb
# Tue, 12 Jan 2021 00:20:50 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Jan 2021 00:22:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 12 Jan 2021 00:22:09 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:22:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:22:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:240407eb82b6591b0574396ec829a4a5cd9a75257a4663f9876942995275965d`  
		Last Modified: Wed, 09 Dec 2020 17:10:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9257be76bd37cad15d45905ec5910266409794a9dbd8a0428174f8b2f352a`  
		Last Modified: Wed, 09 Dec 2020 17:42:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ea2225c77eadc0189bc20fb84afed780b270881cda1af919808b4659ddfde4`  
		Last Modified: Tue, 12 Jan 2021 00:26:38 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e11834207f6dd2d9b771b24f539c5e44ba9c03e436eab5fb3d14b440761244`  
		Last Modified: Tue, 12 Jan 2021 00:26:36 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3d13a0cbb1f04703c664ea56832b37d3c72620db9f1322e3987b5939e63be7`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1b5c2d8ee1e18e7fd1d2758bb1d910114688b48e87b48b612bc04e7f9ab565`  
		Last Modified: Tue, 12 Jan 2021 00:26:35 GMT  
		Size: 4.9 MB (4866042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3b650e7eae667685fbdb190173a13f5d5f514356e6f86b28a5e117d8d365e5`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 15.2 MB (15248954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f14a725380678eee4b1fb7eb05c4604f8bcf3d3dbe55a664242327d3a889d9`  
		Last Modified: Tue, 12 Jan 2021 00:26:33 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968d5703b7cafe8fb35b9c28e5f6d99df9c64e2b9272652cd585e1505eda409`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd142e8fb60d24af64f85a7309313043c3e90c22e5f9ad18b37fcb2b05bb10cf`  
		Last Modified: Tue, 12 Jan 2021 00:26:30 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.20-windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:713e3b909647fd8bd890a4c0110e154cdad36588a4ff949fafe11a65cc7df24b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4104; amd64

### `nats-streaming:0.20-windowsservercore-ltsc2016` - windows version 10.0.14393.4104; amd64

```console
$ docker pull nats-streaming@sha256:1c76108446fc8743e3272a3e5ebe44713cb0f271f791afbcb180b164eeceb30a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5790486404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677b831b855e37cf8ca7b05f3d97e02d9acd7b7f88c3e2cb94350d97dfd45506`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 14:41:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:38:10 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:22:38 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:22:39 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.20.0/nats-streaming-server-v0.20.0-windows-amd64.zip
# Tue, 12 Jan 2021 00:22:40 GMT
ENV GIT_DOWNLOAD_SHA256=26ae310d3ec11617d380106a769236a6dc2209769c0c36d15cb6736db1b589cb
# Tue, 12 Jan 2021 00:23:47 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Jan 2021 00:25:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 12 Jan 2021 00:25:47 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:25:48 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:25:49 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5a79f8be42bf1c358ccc82f32c1481de95c393ef97e712a321c1440d132fda9`  
		Last Modified: Wed, 09 Dec 2020 17:11:03 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d972336c8bcee0026c76e8f199cef405112a70aeef9917f07d2859f15162c1`  
		Last Modified: Wed, 09 Dec 2020 17:42:56 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36f4ebf3f9e4f08ccee6bfa20099991e715ee2894afc2a5ab488f99abde352e`  
		Last Modified: Tue, 12 Jan 2021 00:27:18 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbb72f3ad396e481a0b277ce3e34e967c03d0508866752c073f88ba79fe5ad9`  
		Last Modified: Tue, 12 Jan 2021 00:27:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5b181e3fbbd7a07117dea46bb1665bf7cb7d1c63893ba7e34253bc80329005`  
		Last Modified: Tue, 12 Jan 2021 00:27:17 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f188787bf90e9475900fcfe23b4560d8a3c339da882a6bd6a627200f050de787`  
		Last Modified: Tue, 12 Jan 2021 00:27:16 GMT  
		Size: 5.5 MB (5540955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648f80f9fceb0f132e4ecd6f30d636df20cfb7fd51954ae9945a657d622e7875`  
		Last Modified: Tue, 12 Jan 2021 00:27:32 GMT  
		Size: 16.1 MB (16092606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89c59b6b1299bdb040513b474b6d8a594a4bc7dbaded7aa867723807a1fc11a`  
		Last Modified: Tue, 12 Jan 2021 00:27:13 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec9cf99b11036b9be139f4bc0016e3ec80a666200e52ff82978706a12fa30b3`  
		Last Modified: Tue, 12 Jan 2021 00:27:13 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7278eff7db06794f2daef6b524a6e0ae1a8fc04d3924fb1bac92b6e449b539`  
		Last Modified: Tue, 12 Jan 2021 00:27:12 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:54ee921908bc93e1deb621ad5b769a4b1e66fd99781595cacb1e1f526cae5670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ee383fab395fb79ad35d3663e31ba2c1556e67dd1ae42c9a314b14f66d80afa6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8997281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2217d4d7856bf852cbd735ef2587447e243436346788e6acaf5f102bcfbf28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Tue, 12 Jan 2021 00:48:03 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:48:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 12 Jan 2021 00:48:05 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 12 Jan 2021 00:48:06 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:48:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 00:48:06 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9b99285c9495350a993a87920ea4ccf0c2c560a7047d0076af2648f08b7bea`  
		Last Modified: Tue, 12 Jan 2021 00:48:48 GMT  
		Size: 6.2 MB (6197794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244241c08cee6b44b104d2b942ec81d0a48351c78496d12ee991024881132576`  
		Last Modified: Tue, 12 Jan 2021 00:48:46 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:18fd3ddc15d5b65b6ad1171abf76e359cca31b60730750546e0dc0368a805750
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8330755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0322ce6374b271fc98c0e0a12b42c00a722465006d75394c2ab41bbb47d50c46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Mon, 11 Jan 2021 23:53:38 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Mon, 11 Jan 2021 23:53:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 11 Jan 2021 23:53:43 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 11 Jan 2021 23:53:44 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:53:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Jan 2021 23:53:45 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54831e858eddfe2c245e8c154d4422ad61bc9a30c1cfe612ec35f7a12b1e529`  
		Last Modified: Mon, 11 Jan 2021 23:54:22 GMT  
		Size: 5.7 MB (5726171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412a9e8bb4d16b7ddec81004c2205411fc7b8830d0d2a0f3054a2fe0dc4664cd`  
		Last Modified: Mon, 11 Jan 2021 23:54:20 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b41e2afb428f6345393616c70c1a9d2221db86ab84c6e37be6c252bebf974203
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8125466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfc9155e69d8a79c164c6c96d01ea612fb88e955066a7f2803d0054801875da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Tue, 12 Jan 2021 00:18:41 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:18:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 12 Jan 2021 00:18:54 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 12 Jan 2021 00:18:57 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:18:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 00:18:59 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9290155f6f3b723d2522ebaa0d1e2038dcd4f4c978c086bc43fd55a4d8284659`  
		Last Modified: Tue, 12 Jan 2021 00:19:43 GMT  
		Size: 5.7 MB (5717488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4715986f280e125e74cc7b430caa19329b3de9fcfcd40ae588f422be68c37ca`  
		Last Modified: Tue, 12 Jan 2021 00:19:42 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ae8f52346c3d26a49ae885bf56785f3952c14c8622a97e18288ae0abedd51660
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f79e7574653a33192a8af07510cf1a7f03f5c02a77b49072304e701cf514cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Mon, 11 Jan 2021 23:47:10 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Mon, 11 Jan 2021 23:47:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 11 Jan 2021 23:47:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 11 Jan 2021 23:47:15 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:47:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Jan 2021 23:47:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e424273d6cedd00225b67fa1b47e0dd8bf4b2abfa19fbc27f7763f096aeb138`  
		Last Modified: Mon, 11 Jan 2021 23:47:54 GMT  
		Size: 5.7 MB (5668408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33979e718e15555239006f224ba6d995cf9d6d044a7f25493196839d4d5aed73`  
		Last Modified: Mon, 11 Jan 2021 23:47:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.12`

```console
$ docker pull nats-streaming@sha256:54ee921908bc93e1deb621ad5b769a4b1e66fd99781595cacb1e1f526cae5670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.12` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ee383fab395fb79ad35d3663e31ba2c1556e67dd1ae42c9a314b14f66d80afa6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8997281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2217d4d7856bf852cbd735ef2587447e243436346788e6acaf5f102bcfbf28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Tue, 12 Jan 2021 00:48:03 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:48:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 12 Jan 2021 00:48:05 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 12 Jan 2021 00:48:06 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:48:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 00:48:06 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9b99285c9495350a993a87920ea4ccf0c2c560a7047d0076af2648f08b7bea`  
		Last Modified: Tue, 12 Jan 2021 00:48:48 GMT  
		Size: 6.2 MB (6197794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244241c08cee6b44b104d2b942ec81d0a48351c78496d12ee991024881132576`  
		Last Modified: Tue, 12 Jan 2021 00:48:46 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.12` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:18fd3ddc15d5b65b6ad1171abf76e359cca31b60730750546e0dc0368a805750
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8330755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0322ce6374b271fc98c0e0a12b42c00a722465006d75394c2ab41bbb47d50c46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Mon, 11 Jan 2021 23:53:38 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Mon, 11 Jan 2021 23:53:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 11 Jan 2021 23:53:43 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 11 Jan 2021 23:53:44 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:53:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Jan 2021 23:53:45 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54831e858eddfe2c245e8c154d4422ad61bc9a30c1cfe612ec35f7a12b1e529`  
		Last Modified: Mon, 11 Jan 2021 23:54:22 GMT  
		Size: 5.7 MB (5726171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412a9e8bb4d16b7ddec81004c2205411fc7b8830d0d2a0f3054a2fe0dc4664cd`  
		Last Modified: Mon, 11 Jan 2021 23:54:20 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.12` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b41e2afb428f6345393616c70c1a9d2221db86ab84c6e37be6c252bebf974203
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8125466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfc9155e69d8a79c164c6c96d01ea612fb88e955066a7f2803d0054801875da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Tue, 12 Jan 2021 00:18:41 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:18:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 12 Jan 2021 00:18:54 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 12 Jan 2021 00:18:57 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:18:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 00:18:59 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9290155f6f3b723d2522ebaa0d1e2038dcd4f4c978c086bc43fd55a4d8284659`  
		Last Modified: Tue, 12 Jan 2021 00:19:43 GMT  
		Size: 5.7 MB (5717488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4715986f280e125e74cc7b430caa19329b3de9fcfcd40ae588f422be68c37ca`  
		Last Modified: Tue, 12 Jan 2021 00:19:42 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ae8f52346c3d26a49ae885bf56785f3952c14c8622a97e18288ae0abedd51660
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f79e7574653a33192a8af07510cf1a7f03f5c02a77b49072304e701cf514cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Mon, 11 Jan 2021 23:47:10 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Mon, 11 Jan 2021 23:47:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='618008a4902916b6bdb26022343ab91313d4f7fc90b31d0c71ad9e75dc8299e4' ;; 		armhf) natsArch='arm6'; sha256='144b04f8f42793aee1b2deb3f6eb187648c37dcc32d526c607a0af99a847260d' ;; 		armv7) natsArch='arm7'; sha256='720f4a90d1dd536bc04639ae31c70ab46fb3e10556f0f261eb038fdce941f20c' ;; 		x86_64) natsArch='amd64'; sha256='098e2293cce5d457b92f3df35127789422562f1414427c406ffd03ea3bd687c9' ;; 		x86) natsArch='386'; sha256='322a290f4706f14d6ff8160ec437202bd282f61f0607741d0e4c38ef89b83451' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 11 Jan 2021 23:47:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 11 Jan 2021 23:47:15 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:47:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Jan 2021 23:47:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e424273d6cedd00225b67fa1b47e0dd8bf4b2abfa19fbc27f7763f096aeb138`  
		Last Modified: Mon, 11 Jan 2021 23:47:54 GMT  
		Size: 5.7 MB (5668408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33979e718e15555239006f224ba6d995cf9d6d044a7f25493196839d4d5aed73`  
		Last Modified: Mon, 11 Jan 2021 23:47:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:563a35fb6be5ca12bbbb1c8cb18196dfb1f08205de173985a8698e3ffb1bd8d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1637; amd64

### `nats-streaming:latest` - linux; amd64

```console
$ docker pull nats-streaming@sha256:cd0162a7232de1eabe982554c8740e7edbac4747af3e99fa9bc38a480b4a4243
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1544c1524919e1458186fefae5f5ff415c37055742e531010fc2660b11db2339`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 12 Jan 2021 00:48:24 GMT
COPY file:acbca3cec2dc5172f21984b614cbcd90e6e4cf0bd9848c5ddcffb94615a02436 in /nats-streaming-server 
# Tue, 12 Jan 2021 00:48:24 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:48:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 12 Jan 2021 00:48:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0d51fde6ce3492f397e8a85dad354a9a45ab91310cf4abd6275101f3ef823587`  
		Last Modified: Tue, 12 Jan 2021 00:49:07 GMT  
		Size: 5.9 MB (5914730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:bbb3d771f9232932017b9cb9b501734367bc3560eed790695be682d94a8f3573
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed880c2955fd126b0ce38471e90c9467c9c739f55b4c789cec1a4575a41d36f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 11 Jan 2021 23:53:53 GMT
COPY file:617b9b5366d0d437ce471ad0763bdd7d350496612583dc2c7044dcde4d32257e in /nats-streaming-server 
# Mon, 11 Jan 2021 23:53:54 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:53:54 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 11 Jan 2021 23:53:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7cffcff2c5b4913dac660d7456365492a0393b1aa6f1812f6b7b46b250e1970d`  
		Last Modified: Mon, 11 Jan 2021 23:54:39 GMT  
		Size: 5.4 MB (5444243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b2d9250f9a4e3b25b2212f4e8c27c693cc5cfa0f83ca82a8005c90ae8372ab86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f1d3c5a1d429a3e2b1fc71f5bc023980c41d34ccb0a0482aca07b6cbb4d6f1`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 12 Jan 2021 00:19:09 GMT
COPY file:2b3fc04f11d3cc7cdfa09f93a79d8efe0889d24324b831fb35126470165c9027 in /nats-streaming-server 
# Tue, 12 Jan 2021 00:19:14 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:19:16 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 12 Jan 2021 00:19:17 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bf50122b11c4b5e2fa295a9456a93489ad25dd1e9bfefda1d572da1a57418205`  
		Last Modified: Tue, 12 Jan 2021 00:20:01 GMT  
		Size: 5.4 MB (5439328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:0f315491d4d14e634f971591c7f8bd0eb9aad59975fcdf867a51294df2e5efb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dba974517468c29a982c1b4a0b7744a93825122145a1dcc5f7e53c96119efa`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 11 Jan 2021 23:47:25 GMT
COPY file:5a251d4e6bafc9d9ea6f25cd37fd44252da405176da94cc580cdd663abecffa5 in /nats-streaming-server 
# Mon, 11 Jan 2021 23:47:26 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:47:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 11 Jan 2021 23:47:27 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:58239a1ea6494e431645c7ad156ed917333a248edbe6be76af8b7384d9339f07`  
		Last Modified: Mon, 11 Jan 2021 23:48:09 GMT  
		Size: 5.4 MB (5388538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats-streaming@sha256:dc8cb861e9ebd507f6052f70f00e5cd153ed10f3ce94b514ca53b0b66d68e1a6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107290057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f45933a0476064ac026d83b04912423ee2e0e38a5a0a13d9f6dd101b42deccd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:22:30 GMT
RUN cmd /S /C #(nop) COPY file:f2450ffeda74e33f820191eccf78b6647ce56865170e966bfa8e72afe6e46c36 in C:\nats-streaming-server.exe 
# Tue, 12 Jan 2021 00:22:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:22:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:22:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9a7966c40d2ea4e2a3a9732b1971a90e2c947c7436138dfeecc7a5dd475850`  
		Last Modified: Tue, 12 Jan 2021 00:26:57 GMT  
		Size: 6.0 MB (6021865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8709fe81a73f9b62174f38547b2d9da1bffe292d51b1b93b8fd6c4f89a924e9`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 814.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3718c1b6d751147f39ee7c4a6f1c5cea284aa100dfce6a8e622a16c6456c7d18`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe5aba04f48a9d07940a1f43378efa11f913918e6ebcead455135c3d0346504`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 823.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:f46b63443b02bc0089e72301ae260b1ef32ff25e755e67b633169945585ca12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:cd0162a7232de1eabe982554c8740e7edbac4747af3e99fa9bc38a480b4a4243
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1544c1524919e1458186fefae5f5ff415c37055742e531010fc2660b11db2339`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 12 Jan 2021 00:48:24 GMT
COPY file:acbca3cec2dc5172f21984b614cbcd90e6e4cf0bd9848c5ddcffb94615a02436 in /nats-streaming-server 
# Tue, 12 Jan 2021 00:48:24 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:48:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 12 Jan 2021 00:48:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0d51fde6ce3492f397e8a85dad354a9a45ab91310cf4abd6275101f3ef823587`  
		Last Modified: Tue, 12 Jan 2021 00:49:07 GMT  
		Size: 5.9 MB (5914730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:bbb3d771f9232932017b9cb9b501734367bc3560eed790695be682d94a8f3573
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed880c2955fd126b0ce38471e90c9467c9c739f55b4c789cec1a4575a41d36f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 11 Jan 2021 23:53:53 GMT
COPY file:617b9b5366d0d437ce471ad0763bdd7d350496612583dc2c7044dcde4d32257e in /nats-streaming-server 
# Mon, 11 Jan 2021 23:53:54 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:53:54 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 11 Jan 2021 23:53:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7cffcff2c5b4913dac660d7456365492a0393b1aa6f1812f6b7b46b250e1970d`  
		Last Modified: Mon, 11 Jan 2021 23:54:39 GMT  
		Size: 5.4 MB (5444243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b2d9250f9a4e3b25b2212f4e8c27c693cc5cfa0f83ca82a8005c90ae8372ab86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f1d3c5a1d429a3e2b1fc71f5bc023980c41d34ccb0a0482aca07b6cbb4d6f1`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 12 Jan 2021 00:19:09 GMT
COPY file:2b3fc04f11d3cc7cdfa09f93a79d8efe0889d24324b831fb35126470165c9027 in /nats-streaming-server 
# Tue, 12 Jan 2021 00:19:14 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:19:16 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 12 Jan 2021 00:19:17 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bf50122b11c4b5e2fa295a9456a93489ad25dd1e9bfefda1d572da1a57418205`  
		Last Modified: Tue, 12 Jan 2021 00:20:01 GMT  
		Size: 5.4 MB (5439328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:0f315491d4d14e634f971591c7f8bd0eb9aad59975fcdf867a51294df2e5efb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dba974517468c29a982c1b4a0b7744a93825122145a1dcc5f7e53c96119efa`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 11 Jan 2021 23:47:25 GMT
COPY file:5a251d4e6bafc9d9ea6f25cd37fd44252da405176da94cc580cdd663abecffa5 in /nats-streaming-server 
# Mon, 11 Jan 2021 23:47:26 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:47:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 11 Jan 2021 23:47:27 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:58239a1ea6494e431645c7ad156ed917333a248edbe6be76af8b7384d9339f07`  
		Last Modified: Mon, 11 Jan 2021 23:48:09 GMT  
		Size: 5.4 MB (5388538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:327650283f674241324910a0f8feaa90317a150029496c2d027d86ee41002f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats-streaming@sha256:dc8cb861e9ebd507f6052f70f00e5cd153ed10f3ce94b514ca53b0b66d68e1a6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107290057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f45933a0476064ac026d83b04912423ee2e0e38a5a0a13d9f6dd101b42deccd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:22:30 GMT
RUN cmd /S /C #(nop) COPY file:f2450ffeda74e33f820191eccf78b6647ce56865170e966bfa8e72afe6e46c36 in C:\nats-streaming-server.exe 
# Tue, 12 Jan 2021 00:22:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:22:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:22:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9a7966c40d2ea4e2a3a9732b1971a90e2c947c7436138dfeecc7a5dd475850`  
		Last Modified: Tue, 12 Jan 2021 00:26:57 GMT  
		Size: 6.0 MB (6021865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8709fe81a73f9b62174f38547b2d9da1bffe292d51b1b93b8fd6c4f89a924e9`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 814.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3718c1b6d751147f39ee7c4a6f1c5cea284aa100dfce6a8e622a16c6456c7d18`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe5aba04f48a9d07940a1f43378efa11f913918e6ebcead455135c3d0346504`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 823.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:327650283f674241324910a0f8feaa90317a150029496c2d027d86ee41002f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats-streaming@sha256:dc8cb861e9ebd507f6052f70f00e5cd153ed10f3ce94b514ca53b0b66d68e1a6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107290057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f45933a0476064ac026d83b04912423ee2e0e38a5a0a13d9f6dd101b42deccd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:22:30 GMT
RUN cmd /S /C #(nop) COPY file:f2450ffeda74e33f820191eccf78b6647ce56865170e966bfa8e72afe6e46c36 in C:\nats-streaming-server.exe 
# Tue, 12 Jan 2021 00:22:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:22:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:22:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9a7966c40d2ea4e2a3a9732b1971a90e2c947c7436138dfeecc7a5dd475850`  
		Last Modified: Tue, 12 Jan 2021 00:26:57 GMT  
		Size: 6.0 MB (6021865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8709fe81a73f9b62174f38547b2d9da1bffe292d51b1b93b8fd6c4f89a924e9`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 814.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3718c1b6d751147f39ee7c4a6f1c5cea284aa100dfce6a8e622a16c6456c7d18`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe5aba04f48a9d07940a1f43378efa11f913918e6ebcead455135c3d0346504`  
		Last Modified: Tue, 12 Jan 2021 00:26:53 GMT  
		Size: 823.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:f46b63443b02bc0089e72301ae260b1ef32ff25e755e67b633169945585ca12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:cd0162a7232de1eabe982554c8740e7edbac4747af3e99fa9bc38a480b4a4243
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1544c1524919e1458186fefae5f5ff415c37055742e531010fc2660b11db2339`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 12 Jan 2021 00:48:24 GMT
COPY file:acbca3cec2dc5172f21984b614cbcd90e6e4cf0bd9848c5ddcffb94615a02436 in /nats-streaming-server 
# Tue, 12 Jan 2021 00:48:24 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:48:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 12 Jan 2021 00:48:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0d51fde6ce3492f397e8a85dad354a9a45ab91310cf4abd6275101f3ef823587`  
		Last Modified: Tue, 12 Jan 2021 00:49:07 GMT  
		Size: 5.9 MB (5914730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:bbb3d771f9232932017b9cb9b501734367bc3560eed790695be682d94a8f3573
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed880c2955fd126b0ce38471e90c9467c9c739f55b4c789cec1a4575a41d36f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 11 Jan 2021 23:53:53 GMT
COPY file:617b9b5366d0d437ce471ad0763bdd7d350496612583dc2c7044dcde4d32257e in /nats-streaming-server 
# Mon, 11 Jan 2021 23:53:54 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:53:54 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 11 Jan 2021 23:53:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7cffcff2c5b4913dac660d7456365492a0393b1aa6f1812f6b7b46b250e1970d`  
		Last Modified: Mon, 11 Jan 2021 23:54:39 GMT  
		Size: 5.4 MB (5444243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b2d9250f9a4e3b25b2212f4e8c27c693cc5cfa0f83ca82a8005c90ae8372ab86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f1d3c5a1d429a3e2b1fc71f5bc023980c41d34ccb0a0482aca07b6cbb4d6f1`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 12 Jan 2021 00:19:09 GMT
COPY file:2b3fc04f11d3cc7cdfa09f93a79d8efe0889d24324b831fb35126470165c9027 in /nats-streaming-server 
# Tue, 12 Jan 2021 00:19:14 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:19:16 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 12 Jan 2021 00:19:17 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bf50122b11c4b5e2fa295a9456a93489ad25dd1e9bfefda1d572da1a57418205`  
		Last Modified: Tue, 12 Jan 2021 00:20:01 GMT  
		Size: 5.4 MB (5439328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:0f315491d4d14e634f971591c7f8bd0eb9aad59975fcdf867a51294df2e5efb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dba974517468c29a982c1b4a0b7744a93825122145a1dcc5f7e53c96119efa`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 11 Jan 2021 23:47:25 GMT
COPY file:5a251d4e6bafc9d9ea6f25cd37fd44252da405176da94cc580cdd663abecffa5 in /nats-streaming-server 
# Mon, 11 Jan 2021 23:47:26 GMT
EXPOSE 4222 8222
# Mon, 11 Jan 2021 23:47:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 11 Jan 2021 23:47:27 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:58239a1ea6494e431645c7ad156ed917333a248edbe6be76af8b7384d9339f07`  
		Last Modified: Mon, 11 Jan 2021 23:48:09 GMT  
		Size: 5.4 MB (5388538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:ab4f90fa36638c93e8552a653422527a599d4a73f996c21353c484c6dc0a154e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64
	-	windows version 10.0.14393.4104; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats-streaming@sha256:1e9246d04cadc2e2c8c9f393c081c3f899ee17cc0c2604e670f4b2dfb473ae78
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2410998451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880b431ca994738c273eb95d89d0200e5faf1def000165c43c3b6d2195fb6ac7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 14:02:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:36:04 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:20:16 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:20:17 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.20.0/nats-streaming-server-v0.20.0-windows-amd64.zip
# Tue, 12 Jan 2021 00:20:18 GMT
ENV GIT_DOWNLOAD_SHA256=26ae310d3ec11617d380106a769236a6dc2209769c0c36d15cb6736db1b589cb
# Tue, 12 Jan 2021 00:20:50 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Jan 2021 00:22:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 12 Jan 2021 00:22:09 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:22:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:22:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:240407eb82b6591b0574396ec829a4a5cd9a75257a4663f9876942995275965d`  
		Last Modified: Wed, 09 Dec 2020 17:10:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9257be76bd37cad15d45905ec5910266409794a9dbd8a0428174f8b2f352a`  
		Last Modified: Wed, 09 Dec 2020 17:42:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ea2225c77eadc0189bc20fb84afed780b270881cda1af919808b4659ddfde4`  
		Last Modified: Tue, 12 Jan 2021 00:26:38 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e11834207f6dd2d9b771b24f539c5e44ba9c03e436eab5fb3d14b440761244`  
		Last Modified: Tue, 12 Jan 2021 00:26:36 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3d13a0cbb1f04703c664ea56832b37d3c72620db9f1322e3987b5939e63be7`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1b5c2d8ee1e18e7fd1d2758bb1d910114688b48e87b48b612bc04e7f9ab565`  
		Last Modified: Tue, 12 Jan 2021 00:26:35 GMT  
		Size: 4.9 MB (4866042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3b650e7eae667685fbdb190173a13f5d5f514356e6f86b28a5e117d8d365e5`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 15.2 MB (15248954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f14a725380678eee4b1fb7eb05c4604f8bcf3d3dbe55a664242327d3a889d9`  
		Last Modified: Tue, 12 Jan 2021 00:26:33 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968d5703b7cafe8fb35b9c28e5f6d99df9c64e2b9272652cd585e1505eda409`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd142e8fb60d24af64f85a7309313043c3e90c22e5f9ad18b37fcb2b05bb10cf`  
		Last Modified: Tue, 12 Jan 2021 00:26:30 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:windowsservercore` - windows version 10.0.14393.4104; amd64

```console
$ docker pull nats-streaming@sha256:1c76108446fc8743e3272a3e5ebe44713cb0f271f791afbcb180b164eeceb30a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5790486404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677b831b855e37cf8ca7b05f3d97e02d9acd7b7f88c3e2cb94350d97dfd45506`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 14:41:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:38:10 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:22:38 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:22:39 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.20.0/nats-streaming-server-v0.20.0-windows-amd64.zip
# Tue, 12 Jan 2021 00:22:40 GMT
ENV GIT_DOWNLOAD_SHA256=26ae310d3ec11617d380106a769236a6dc2209769c0c36d15cb6736db1b589cb
# Tue, 12 Jan 2021 00:23:47 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Jan 2021 00:25:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 12 Jan 2021 00:25:47 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:25:48 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:25:49 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5a79f8be42bf1c358ccc82f32c1481de95c393ef97e712a321c1440d132fda9`  
		Last Modified: Wed, 09 Dec 2020 17:11:03 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d972336c8bcee0026c76e8f199cef405112a70aeef9917f07d2859f15162c1`  
		Last Modified: Wed, 09 Dec 2020 17:42:56 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36f4ebf3f9e4f08ccee6bfa20099991e715ee2894afc2a5ab488f99abde352e`  
		Last Modified: Tue, 12 Jan 2021 00:27:18 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbb72f3ad396e481a0b277ce3e34e967c03d0508866752c073f88ba79fe5ad9`  
		Last Modified: Tue, 12 Jan 2021 00:27:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5b181e3fbbd7a07117dea46bb1665bf7cb7d1c63893ba7e34253bc80329005`  
		Last Modified: Tue, 12 Jan 2021 00:27:17 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f188787bf90e9475900fcfe23b4560d8a3c339da882a6bd6a627200f050de787`  
		Last Modified: Tue, 12 Jan 2021 00:27:16 GMT  
		Size: 5.5 MB (5540955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648f80f9fceb0f132e4ecd6f30d636df20cfb7fd51954ae9945a657d622e7875`  
		Last Modified: Tue, 12 Jan 2021 00:27:32 GMT  
		Size: 16.1 MB (16092606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89c59b6b1299bdb040513b474b6d8a594a4bc7dbaded7aa867723807a1fc11a`  
		Last Modified: Tue, 12 Jan 2021 00:27:13 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec9cf99b11036b9be139f4bc0016e3ec80a666200e52ff82978706a12fa30b3`  
		Last Modified: Tue, 12 Jan 2021 00:27:13 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7278eff7db06794f2daef6b524a6e0ae1a8fc04d3924fb1bac92b6e449b539`  
		Last Modified: Tue, 12 Jan 2021 00:27:12 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:ced4889038416616798fd8652bb25df54adc1f69b66e10590585517f761f3fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats-streaming@sha256:1e9246d04cadc2e2c8c9f393c081c3f899ee17cc0c2604e670f4b2dfb473ae78
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2410998451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880b431ca994738c273eb95d89d0200e5faf1def000165c43c3b6d2195fb6ac7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 14:02:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:36:04 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:20:16 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:20:17 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.20.0/nats-streaming-server-v0.20.0-windows-amd64.zip
# Tue, 12 Jan 2021 00:20:18 GMT
ENV GIT_DOWNLOAD_SHA256=26ae310d3ec11617d380106a769236a6dc2209769c0c36d15cb6736db1b589cb
# Tue, 12 Jan 2021 00:20:50 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Jan 2021 00:22:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 12 Jan 2021 00:22:09 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:22:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:22:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:240407eb82b6591b0574396ec829a4a5cd9a75257a4663f9876942995275965d`  
		Last Modified: Wed, 09 Dec 2020 17:10:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9257be76bd37cad15d45905ec5910266409794a9dbd8a0428174f8b2f352a`  
		Last Modified: Wed, 09 Dec 2020 17:42:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ea2225c77eadc0189bc20fb84afed780b270881cda1af919808b4659ddfde4`  
		Last Modified: Tue, 12 Jan 2021 00:26:38 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e11834207f6dd2d9b771b24f539c5e44ba9c03e436eab5fb3d14b440761244`  
		Last Modified: Tue, 12 Jan 2021 00:26:36 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3d13a0cbb1f04703c664ea56832b37d3c72620db9f1322e3987b5939e63be7`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1b5c2d8ee1e18e7fd1d2758bb1d910114688b48e87b48b612bc04e7f9ab565`  
		Last Modified: Tue, 12 Jan 2021 00:26:35 GMT  
		Size: 4.9 MB (4866042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3b650e7eae667685fbdb190173a13f5d5f514356e6f86b28a5e117d8d365e5`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 15.2 MB (15248954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f14a725380678eee4b1fb7eb05c4604f8bcf3d3dbe55a664242327d3a889d9`  
		Last Modified: Tue, 12 Jan 2021 00:26:33 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968d5703b7cafe8fb35b9c28e5f6d99df9c64e2b9272652cd585e1505eda409`  
		Last Modified: Tue, 12 Jan 2021 00:26:34 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd142e8fb60d24af64f85a7309313043c3e90c22e5f9ad18b37fcb2b05bb10cf`  
		Last Modified: Tue, 12 Jan 2021 00:26:30 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:713e3b909647fd8bd890a4c0110e154cdad36588a4ff949fafe11a65cc7df24b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4104; amd64

### `nats-streaming:windowsservercore-ltsc2016` - windows version 10.0.14393.4104; amd64

```console
$ docker pull nats-streaming@sha256:1c76108446fc8743e3272a3e5ebe44713cb0f271f791afbcb180b164eeceb30a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5790486404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677b831b855e37cf8ca7b05f3d97e02d9acd7b7f88c3e2cb94350d97dfd45506`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 14:41:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:38:10 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Jan 2021 00:22:38 GMT
ENV NATS_STREAMING_SERVER=0.20.0
# Tue, 12 Jan 2021 00:22:39 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.20.0/nats-streaming-server-v0.20.0-windows-amd64.zip
# Tue, 12 Jan 2021 00:22:40 GMT
ENV GIT_DOWNLOAD_SHA256=26ae310d3ec11617d380106a769236a6dc2209769c0c36d15cb6736db1b589cb
# Tue, 12 Jan 2021 00:23:47 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Jan 2021 00:25:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 12 Jan 2021 00:25:47 GMT
EXPOSE 4222 8222
# Tue, 12 Jan 2021 00:25:48 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 12 Jan 2021 00:25:49 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5a79f8be42bf1c358ccc82f32c1481de95c393ef97e712a321c1440d132fda9`  
		Last Modified: Wed, 09 Dec 2020 17:11:03 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d972336c8bcee0026c76e8f199cef405112a70aeef9917f07d2859f15162c1`  
		Last Modified: Wed, 09 Dec 2020 17:42:56 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36f4ebf3f9e4f08ccee6bfa20099991e715ee2894afc2a5ab488f99abde352e`  
		Last Modified: Tue, 12 Jan 2021 00:27:18 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbb72f3ad396e481a0b277ce3e34e967c03d0508866752c073f88ba79fe5ad9`  
		Last Modified: Tue, 12 Jan 2021 00:27:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5b181e3fbbd7a07117dea46bb1665bf7cb7d1c63893ba7e34253bc80329005`  
		Last Modified: Tue, 12 Jan 2021 00:27:17 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f188787bf90e9475900fcfe23b4560d8a3c339da882a6bd6a627200f050de787`  
		Last Modified: Tue, 12 Jan 2021 00:27:16 GMT  
		Size: 5.5 MB (5540955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648f80f9fceb0f132e4ecd6f30d636df20cfb7fd51954ae9945a657d622e7875`  
		Last Modified: Tue, 12 Jan 2021 00:27:32 GMT  
		Size: 16.1 MB (16092606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89c59b6b1299bdb040513b474b6d8a594a4bc7dbaded7aa867723807a1fc11a`  
		Last Modified: Tue, 12 Jan 2021 00:27:13 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec9cf99b11036b9be139f4bc0016e3ec80a666200e52ff82978706a12fa30b3`  
		Last Modified: Tue, 12 Jan 2021 00:27:13 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7278eff7db06794f2daef6b524a6e0ae1a8fc04d3924fb1bac92b6e449b539`  
		Last Modified: Tue, 12 Jan 2021 00:27:12 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

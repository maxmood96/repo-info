<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats-streaming`

-	[`nats-streaming:0.19`](#nats-streaming019)
-	[`nats-streaming:0.19.0`](#nats-streaming0190)
-	[`nats-streaming:0.19.0-alpine`](#nats-streaming0190-alpine)
-	[`nats-streaming:0.19.0-alpine3.12`](#nats-streaming0190-alpine312)
-	[`nats-streaming:0.19.0-linux`](#nats-streaming0190-linux)
-	[`nats-streaming:0.19.0-nanoserver`](#nats-streaming0190-nanoserver)
-	[`nats-streaming:0.19.0-nanoserver-1809`](#nats-streaming0190-nanoserver-1809)
-	[`nats-streaming:0.19.0-scratch`](#nats-streaming0190-scratch)
-	[`nats-streaming:0.19.0-windowsservercore`](#nats-streaming0190-windowsservercore)
-	[`nats-streaming:0.19.0-windowsservercore-1809`](#nats-streaming0190-windowsservercore-1809)
-	[`nats-streaming:0.19.0-windowsservercore-ltsc2016`](#nats-streaming0190-windowsservercore-ltsc2016)
-	[`nats-streaming:0.19-alpine`](#nats-streaming019-alpine)
-	[`nats-streaming:0.19-alpine3.12`](#nats-streaming019-alpine312)
-	[`nats-streaming:0.19-linux`](#nats-streaming019-linux)
-	[`nats-streaming:0.19-nanoserver`](#nats-streaming019-nanoserver)
-	[`nats-streaming:0.19-nanoserver-1809`](#nats-streaming019-nanoserver-1809)
-	[`nats-streaming:0.19-scratch`](#nats-streaming019-scratch)
-	[`nats-streaming:0.19-windowsservercore`](#nats-streaming019-windowsservercore)
-	[`nats-streaming:0.19-windowsservercore-1809`](#nats-streaming019-windowsservercore-1809)
-	[`nats-streaming:0.19-windowsservercore-ltsc2016`](#nats-streaming019-windowsservercore-ltsc2016)
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

## `nats-streaming:0.19`

```console
$ docker pull nats-streaming@sha256:ad99516ae96b71b512175c3fd60d580edecf6df8335e451053e9aea2e28bdffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1577; amd64

### `nats-streaming:0.19` - linux; amd64

```console
$ docker pull nats-streaming@sha256:053a4ca3955b9c5036e48bafb96c83003fe86c34c6928934e3fd1db0529a889c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6487259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a204b53252cabfc16952c1d2dc014dc6518d1a08d00bda1bc5008a139e37a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:33:13 GMT
COPY file:3ed83d1497b0535960e452435cb8b27e347f48da12693aa27ebaf9bff94d82de in /nats-streaming-server 
# Tue, 03 Nov 2020 00:33:13 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:33:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:57ac21f890a508f609eabea265197b18ce9dfe3e694034c7a06d37b536a707b2`  
		Last Modified: Tue, 03 Nov 2020 00:33:37 GMT  
		Size: 6.5 MB (6487259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:f334d10ef2a4663d8d7d920d96321cd97f050b82a5d55d588192f074f60dd814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecfd5ab4178a65e952a7cf1d248a556a6ae2c328ac8b68923146d64734db03`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Nov 2020 23:56:28 GMT
COPY file:d6896b1c93dcd497494c972f9274fcc634a4f4a8d63a0191bdb87f6336aec0d7 in /nats-streaming-server 
# Mon, 02 Nov 2020 23:56:28 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 02 Nov 2020 23:56:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7f165fb71ab77e8081dbfa13656cdf9e5e005002d6c3afa0aac40667a0f97af8`  
		Last Modified: Mon, 02 Nov 2020 23:57:04 GMT  
		Size: 6.0 MB (6049845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:5fd0943909d8aedafb888e099c9f64d234023ad780805ed7c939692ebfd8304d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37071e856ae40dc3c8c5e10b359d1640fd67a6110741c0957af2031032ed6ce`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:05:23 GMT
COPY file:d232132ddff1d85d3a2f5c80a91c80023cbc103d816387e06d604cf97238e52c in /nats-streaming-server 
# Tue, 03 Nov 2020 00:05:24 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:05:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c7227cc1040d04ca7763cfb53ab58bc32ae54921990516adf8e13374ac9ef29`  
		Last Modified: Tue, 03 Nov 2020 00:05:57 GMT  
		Size: 6.0 MB (6043163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c058fd3e9a8ac44263bf53fa2f6f1e8e8cb3e95cd223f8353fdafc50fe57e417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a80bd440362bd4a6743fee8134a3caf6271e3258e449fb106b19c050a3b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:43:38 GMT
COPY file:55e70ee826cd5a662497337a2488e22833672bd031d85b4ee39556ab1e80df08 in /nats-streaming-server 
# Tue, 03 Nov 2020 00:43:40 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:43:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3dc58a59de8a6ed19e9144b0189eb3b637a9e7fcd76ec6c6dc47561b2740a3a2`  
		Last Modified: Tue, 03 Nov 2020 00:44:19 GMT  
		Size: 6.0 MB (5978846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats-streaming@sha256:44cd613007d0ae80aa675e256fcf7ab09154970b8489a02e0d1969c6143d1f61
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107798464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7c11af94433f8f6727ec8b965b09721a359d79801411d21199752bff82c385`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:08:21 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:08:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdd54301a97b4ec40a4f7841d98c5c1650eb782b9fa39fa6fd69336f53ee64`  
		Last Modified: Wed, 11 Nov 2020 21:12:25 GMT  
		Size: 6.5 MB (6515173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e84d935a5287b8d02f7d552ad42e43d116f9f8e81a3ab6938ce0bf2f6a98cd`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9847a1462f5644588430244c224e5ee90473d31bf4d0c11157ec2a823aaae1ca`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 927.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e882e784f1673e88e962c1e9a1239de9107334f963eef6c696f80bd1a04f063`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0`

```console
$ docker pull nats-streaming@sha256:ad99516ae96b71b512175c3fd60d580edecf6df8335e451053e9aea2e28bdffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1577; amd64

### `nats-streaming:0.19.0` - linux; amd64

```console
$ docker pull nats-streaming@sha256:053a4ca3955b9c5036e48bafb96c83003fe86c34c6928934e3fd1db0529a889c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6487259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a204b53252cabfc16952c1d2dc014dc6518d1a08d00bda1bc5008a139e37a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:33:13 GMT
COPY file:3ed83d1497b0535960e452435cb8b27e347f48da12693aa27ebaf9bff94d82de in /nats-streaming-server 
# Tue, 03 Nov 2020 00:33:13 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:33:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:57ac21f890a508f609eabea265197b18ce9dfe3e694034c7a06d37b536a707b2`  
		Last Modified: Tue, 03 Nov 2020 00:33:37 GMT  
		Size: 6.5 MB (6487259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:f334d10ef2a4663d8d7d920d96321cd97f050b82a5d55d588192f074f60dd814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecfd5ab4178a65e952a7cf1d248a556a6ae2c328ac8b68923146d64734db03`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Nov 2020 23:56:28 GMT
COPY file:d6896b1c93dcd497494c972f9274fcc634a4f4a8d63a0191bdb87f6336aec0d7 in /nats-streaming-server 
# Mon, 02 Nov 2020 23:56:28 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 02 Nov 2020 23:56:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7f165fb71ab77e8081dbfa13656cdf9e5e005002d6c3afa0aac40667a0f97af8`  
		Last Modified: Mon, 02 Nov 2020 23:57:04 GMT  
		Size: 6.0 MB (6049845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:5fd0943909d8aedafb888e099c9f64d234023ad780805ed7c939692ebfd8304d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37071e856ae40dc3c8c5e10b359d1640fd67a6110741c0957af2031032ed6ce`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:05:23 GMT
COPY file:d232132ddff1d85d3a2f5c80a91c80023cbc103d816387e06d604cf97238e52c in /nats-streaming-server 
# Tue, 03 Nov 2020 00:05:24 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:05:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c7227cc1040d04ca7763cfb53ab58bc32ae54921990516adf8e13374ac9ef29`  
		Last Modified: Tue, 03 Nov 2020 00:05:57 GMT  
		Size: 6.0 MB (6043163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c058fd3e9a8ac44263bf53fa2f6f1e8e8cb3e95cd223f8353fdafc50fe57e417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a80bd440362bd4a6743fee8134a3caf6271e3258e449fb106b19c050a3b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:43:38 GMT
COPY file:55e70ee826cd5a662497337a2488e22833672bd031d85b4ee39556ab1e80df08 in /nats-streaming-server 
# Tue, 03 Nov 2020 00:43:40 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:43:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3dc58a59de8a6ed19e9144b0189eb3b637a9e7fcd76ec6c6dc47561b2740a3a2`  
		Last Modified: Tue, 03 Nov 2020 00:44:19 GMT  
		Size: 6.0 MB (5978846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats-streaming@sha256:44cd613007d0ae80aa675e256fcf7ab09154970b8489a02e0d1969c6143d1f61
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107798464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7c11af94433f8f6727ec8b965b09721a359d79801411d21199752bff82c385`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:08:21 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:08:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdd54301a97b4ec40a4f7841d98c5c1650eb782b9fa39fa6fd69336f53ee64`  
		Last Modified: Wed, 11 Nov 2020 21:12:25 GMT  
		Size: 6.5 MB (6515173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e84d935a5287b8d02f7d552ad42e43d116f9f8e81a3ab6938ce0bf2f6a98cd`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9847a1462f5644588430244c224e5ee90473d31bf4d0c11157ec2a823aaae1ca`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 927.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e882e784f1673e88e962c1e9a1239de9107334f963eef6c696f80bd1a04f063`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0-alpine`

```console
$ docker pull nats-streaming@sha256:5f15b51b2b447004408633f8f9458106fadad8f21393b1ed531071731e1ddb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.19.0-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:a8fcf986c14ae3ad60206bd6ebde23999c28f9967f05b9c81a760054539a683d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20b4ccbdde21c3fb61f4bd7fa3e83384f7e9d7f32f5bb86c88cd162a41403c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:33:01 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:33:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:33:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:33:04 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:33:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f211ef5561f154a9a5957cdf08a625861df698594add9ba490a54259e9a01cb1`  
		Last Modified: Tue, 03 Nov 2020 00:33:28 GMT  
		Size: 6.8 MB (6770312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eef7e98823e252892036fb4b7e5ccf695c556028fa2f7dd6dc314f625ba9eb9`  
		Last Modified: Tue, 03 Nov 2020 00:33:27 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:2a58d6644e94cc17212ec6a604029ebe9f855ceeee7fa66171bdc8aa6c7113ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8932203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8391afd58a04ec8cf1ab166357c9495c5aa4d32bc4bb4472e577874f42fe55d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:56:13 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Mon, 02 Nov 2020 23:56:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:56:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 02 Nov 2020 23:56:18 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:56:19 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cba1ed5b5094a02c017d654b758674905ec0bb2535d3311fcdd61dce32b319`  
		Last Modified: Mon, 02 Nov 2020 23:56:50 GMT  
		Size: 6.3 MB (6329871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3992f15ff4c1a7660c4a81854ec33d3e4973405c7095ceb0bd8a7865fff21c9f`  
		Last Modified: Mon, 02 Nov 2020 23:56:47 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:6a6c52fc272b91cff878ca25bddc432f19583a2e41e5e92288f0e64d0c649896
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8730479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4347330ee2d9b26f7fafaadc370627e71670505b340c9e4b54d791afcb3a6b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:05:05 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:05:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:05:09 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:05:10 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:05:11 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34033d6dabe9c0f77f765bf2fce39f1eef24c163cfa802ec78f0e2e1bea9da7c`  
		Last Modified: Tue, 03 Nov 2020 00:05:43 GMT  
		Size: 6.3 MB (6324384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0a98c9d7b5d859df80140920031b236b38ff88a4ff09d3bf8cfc5b9776e436`  
		Last Modified: Tue, 03 Nov 2020 00:05:40 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:36be57b574502addd00c81caaffedb9030eec583dbf4e3011a95aa7f998834aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8969159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b947ac7936fa0250ecf3f1aaa6e22a928bdb3cdd8f0dcbbc3b8912a0678290c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:43:12 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:43:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:43:21 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:43:23 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:43:27 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea83a41655c390ae2bea2fd6f2a83188ecb9c82e60ebde8040109e79a2eba5`  
		Last Modified: Tue, 03 Nov 2020 00:44:06 GMT  
		Size: 6.3 MB (6262183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eca3d16e3b7142a6392c550b0efad91076053f222028892a3ae01e63f58dec`  
		Last Modified: Tue, 03 Nov 2020 00:44:05 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0-alpine3.12`

```console
$ docker pull nats-streaming@sha256:5f15b51b2b447004408633f8f9458106fadad8f21393b1ed531071731e1ddb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.19.0-alpine3.12` - linux; amd64

```console
$ docker pull nats-streaming@sha256:a8fcf986c14ae3ad60206bd6ebde23999c28f9967f05b9c81a760054539a683d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20b4ccbdde21c3fb61f4bd7fa3e83384f7e9d7f32f5bb86c88cd162a41403c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:33:01 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:33:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:33:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:33:04 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:33:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f211ef5561f154a9a5957cdf08a625861df698594add9ba490a54259e9a01cb1`  
		Last Modified: Tue, 03 Nov 2020 00:33:28 GMT  
		Size: 6.8 MB (6770312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eef7e98823e252892036fb4b7e5ccf695c556028fa2f7dd6dc314f625ba9eb9`  
		Last Modified: Tue, 03 Nov 2020 00:33:27 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-alpine3.12` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:2a58d6644e94cc17212ec6a604029ebe9f855ceeee7fa66171bdc8aa6c7113ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8932203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8391afd58a04ec8cf1ab166357c9495c5aa4d32bc4bb4472e577874f42fe55d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:56:13 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Mon, 02 Nov 2020 23:56:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:56:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 02 Nov 2020 23:56:18 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:56:19 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cba1ed5b5094a02c017d654b758674905ec0bb2535d3311fcdd61dce32b319`  
		Last Modified: Mon, 02 Nov 2020 23:56:50 GMT  
		Size: 6.3 MB (6329871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3992f15ff4c1a7660c4a81854ec33d3e4973405c7095ceb0bd8a7865fff21c9f`  
		Last Modified: Mon, 02 Nov 2020 23:56:47 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-alpine3.12` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:6a6c52fc272b91cff878ca25bddc432f19583a2e41e5e92288f0e64d0c649896
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8730479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4347330ee2d9b26f7fafaadc370627e71670505b340c9e4b54d791afcb3a6b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:05:05 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:05:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:05:09 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:05:10 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:05:11 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34033d6dabe9c0f77f765bf2fce39f1eef24c163cfa802ec78f0e2e1bea9da7c`  
		Last Modified: Tue, 03 Nov 2020 00:05:43 GMT  
		Size: 6.3 MB (6324384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0a98c9d7b5d859df80140920031b236b38ff88a4ff09d3bf8cfc5b9776e436`  
		Last Modified: Tue, 03 Nov 2020 00:05:40 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:36be57b574502addd00c81caaffedb9030eec583dbf4e3011a95aa7f998834aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8969159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b947ac7936fa0250ecf3f1aaa6e22a928bdb3cdd8f0dcbbc3b8912a0678290c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:43:12 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:43:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:43:21 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:43:23 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:43:27 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea83a41655c390ae2bea2fd6f2a83188ecb9c82e60ebde8040109e79a2eba5`  
		Last Modified: Tue, 03 Nov 2020 00:44:06 GMT  
		Size: 6.3 MB (6262183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eca3d16e3b7142a6392c550b0efad91076053f222028892a3ae01e63f58dec`  
		Last Modified: Tue, 03 Nov 2020 00:44:05 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0-linux`

```console
$ docker pull nats-streaming@sha256:8001e4db36785bd692d9ae1c9ed3857d972692b385e36c08994794a5254bb78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.19.0-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:053a4ca3955b9c5036e48bafb96c83003fe86c34c6928934e3fd1db0529a889c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6487259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a204b53252cabfc16952c1d2dc014dc6518d1a08d00bda1bc5008a139e37a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:33:13 GMT
COPY file:3ed83d1497b0535960e452435cb8b27e347f48da12693aa27ebaf9bff94d82de in /nats-streaming-server 
# Tue, 03 Nov 2020 00:33:13 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:33:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:57ac21f890a508f609eabea265197b18ce9dfe3e694034c7a06d37b536a707b2`  
		Last Modified: Tue, 03 Nov 2020 00:33:37 GMT  
		Size: 6.5 MB (6487259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:f334d10ef2a4663d8d7d920d96321cd97f050b82a5d55d588192f074f60dd814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecfd5ab4178a65e952a7cf1d248a556a6ae2c328ac8b68923146d64734db03`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Nov 2020 23:56:28 GMT
COPY file:d6896b1c93dcd497494c972f9274fcc634a4f4a8d63a0191bdb87f6336aec0d7 in /nats-streaming-server 
# Mon, 02 Nov 2020 23:56:28 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 02 Nov 2020 23:56:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7f165fb71ab77e8081dbfa13656cdf9e5e005002d6c3afa0aac40667a0f97af8`  
		Last Modified: Mon, 02 Nov 2020 23:57:04 GMT  
		Size: 6.0 MB (6049845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:5fd0943909d8aedafb888e099c9f64d234023ad780805ed7c939692ebfd8304d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37071e856ae40dc3c8c5e10b359d1640fd67a6110741c0957af2031032ed6ce`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:05:23 GMT
COPY file:d232132ddff1d85d3a2f5c80a91c80023cbc103d816387e06d604cf97238e52c in /nats-streaming-server 
# Tue, 03 Nov 2020 00:05:24 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:05:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c7227cc1040d04ca7763cfb53ab58bc32ae54921990516adf8e13374ac9ef29`  
		Last Modified: Tue, 03 Nov 2020 00:05:57 GMT  
		Size: 6.0 MB (6043163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c058fd3e9a8ac44263bf53fa2f6f1e8e8cb3e95cd223f8353fdafc50fe57e417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a80bd440362bd4a6743fee8134a3caf6271e3258e449fb106b19c050a3b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:43:38 GMT
COPY file:55e70ee826cd5a662497337a2488e22833672bd031d85b4ee39556ab1e80df08 in /nats-streaming-server 
# Tue, 03 Nov 2020 00:43:40 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:43:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3dc58a59de8a6ed19e9144b0189eb3b637a9e7fcd76ec6c6dc47561b2740a3a2`  
		Last Modified: Tue, 03 Nov 2020 00:44:19 GMT  
		Size: 6.0 MB (5978846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0-nanoserver`

```console
$ docker pull nats-streaming@sha256:12751d89716d394331c32e35fbed0b0bdb912c970c0b5823ed7ebb6198731757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats-streaming:0.19.0-nanoserver` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats-streaming@sha256:44cd613007d0ae80aa675e256fcf7ab09154970b8489a02e0d1969c6143d1f61
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107798464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7c11af94433f8f6727ec8b965b09721a359d79801411d21199752bff82c385`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:08:21 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:08:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdd54301a97b4ec40a4f7841d98c5c1650eb782b9fa39fa6fd69336f53ee64`  
		Last Modified: Wed, 11 Nov 2020 21:12:25 GMT  
		Size: 6.5 MB (6515173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e84d935a5287b8d02f7d552ad42e43d116f9f8e81a3ab6938ce0bf2f6a98cd`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9847a1462f5644588430244c224e5ee90473d31bf4d0c11157ec2a823aaae1ca`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 927.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e882e784f1673e88e962c1e9a1239de9107334f963eef6c696f80bd1a04f063`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:12751d89716d394331c32e35fbed0b0bdb912c970c0b5823ed7ebb6198731757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats-streaming:0.19.0-nanoserver-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats-streaming@sha256:44cd613007d0ae80aa675e256fcf7ab09154970b8489a02e0d1969c6143d1f61
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107798464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7c11af94433f8f6727ec8b965b09721a359d79801411d21199752bff82c385`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:08:21 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:08:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdd54301a97b4ec40a4f7841d98c5c1650eb782b9fa39fa6fd69336f53ee64`  
		Last Modified: Wed, 11 Nov 2020 21:12:25 GMT  
		Size: 6.5 MB (6515173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e84d935a5287b8d02f7d552ad42e43d116f9f8e81a3ab6938ce0bf2f6a98cd`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9847a1462f5644588430244c224e5ee90473d31bf4d0c11157ec2a823aaae1ca`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 927.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e882e784f1673e88e962c1e9a1239de9107334f963eef6c696f80bd1a04f063`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0-scratch`

```console
$ docker pull nats-streaming@sha256:8001e4db36785bd692d9ae1c9ed3857d972692b385e36c08994794a5254bb78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.19.0-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:053a4ca3955b9c5036e48bafb96c83003fe86c34c6928934e3fd1db0529a889c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6487259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a204b53252cabfc16952c1d2dc014dc6518d1a08d00bda1bc5008a139e37a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:33:13 GMT
COPY file:3ed83d1497b0535960e452435cb8b27e347f48da12693aa27ebaf9bff94d82de in /nats-streaming-server 
# Tue, 03 Nov 2020 00:33:13 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:33:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:57ac21f890a508f609eabea265197b18ce9dfe3e694034c7a06d37b536a707b2`  
		Last Modified: Tue, 03 Nov 2020 00:33:37 GMT  
		Size: 6.5 MB (6487259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:f334d10ef2a4663d8d7d920d96321cd97f050b82a5d55d588192f074f60dd814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecfd5ab4178a65e952a7cf1d248a556a6ae2c328ac8b68923146d64734db03`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Nov 2020 23:56:28 GMT
COPY file:d6896b1c93dcd497494c972f9274fcc634a4f4a8d63a0191bdb87f6336aec0d7 in /nats-streaming-server 
# Mon, 02 Nov 2020 23:56:28 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 02 Nov 2020 23:56:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7f165fb71ab77e8081dbfa13656cdf9e5e005002d6c3afa0aac40667a0f97af8`  
		Last Modified: Mon, 02 Nov 2020 23:57:04 GMT  
		Size: 6.0 MB (6049845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:5fd0943909d8aedafb888e099c9f64d234023ad780805ed7c939692ebfd8304d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37071e856ae40dc3c8c5e10b359d1640fd67a6110741c0957af2031032ed6ce`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:05:23 GMT
COPY file:d232132ddff1d85d3a2f5c80a91c80023cbc103d816387e06d604cf97238e52c in /nats-streaming-server 
# Tue, 03 Nov 2020 00:05:24 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:05:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c7227cc1040d04ca7763cfb53ab58bc32ae54921990516adf8e13374ac9ef29`  
		Last Modified: Tue, 03 Nov 2020 00:05:57 GMT  
		Size: 6.0 MB (6043163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c058fd3e9a8ac44263bf53fa2f6f1e8e8cb3e95cd223f8353fdafc50fe57e417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a80bd440362bd4a6743fee8134a3caf6271e3258e449fb106b19c050a3b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:43:38 GMT
COPY file:55e70ee826cd5a662497337a2488e22833672bd031d85b4ee39556ab1e80df08 in /nats-streaming-server 
# Tue, 03 Nov 2020 00:43:40 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:43:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3dc58a59de8a6ed19e9144b0189eb3b637a9e7fcd76ec6c6dc47561b2740a3a2`  
		Last Modified: Tue, 03 Nov 2020 00:44:19 GMT  
		Size: 6.0 MB (5978846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0-windowsservercore`

```console
$ docker pull nats-streaming@sha256:fed1fdbe6cf90f50e143730f5723bfd36abeffebda44d72d35336e144d266c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64
	-	windows version 10.0.14393.4046; amd64

### `nats-streaming:0.19.0-windowsservercore` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats-streaming@sha256:e755a0f47c43b1e70859439f16decaa2b537c74f13a21233cc5dfa56946b9eed
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408607752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2a802c225aed1fa376c8c360c0f85bb4fc66c60f7252b572d17344853d5c34`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 14:18:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:01:32 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:06:07 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Wed, 11 Nov 2020 21:06:08 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Wed, 11 Nov 2020 21:06:09 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Wed, 11 Nov 2020 21:06:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 21:07:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 21:07:59 GMT
EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:08:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:08:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e03cd29396986910a2aaaf968e93bebcaf4b0101821290e0560b401893615ccf`  
		Last Modified: Wed, 11 Nov 2020 16:53:20 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d59214fb7b605a325f942085c8f9dbcc4fa01cb3626a6eaf07a0e437729d5e4`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ccb5a272f7fb60c5ebcc0895833f8d509159a12d346133338a7de41f5dbf1a`  
		Last Modified: Wed, 11 Nov 2020 21:12:01 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe86ff1d99293de35c3769b0edf2c049693415fce2d6c8984756fa96495f0c6d`  
		Last Modified: Wed, 11 Nov 2020 21:12:01 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72dc12d6621abb0db2c34f8038dfbd974eb00174dea1f54c523d67fb442efca`  
		Last Modified: Wed, 11 Nov 2020 21:12:00 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c90fa3489aac1add86a6b50c3f496d21100dd6742c75c3d557fad5ae4d7e9d`  
		Last Modified: Wed, 11 Nov 2020 21:11:58 GMT  
		Size: 4.8 MB (4849948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6e8fe6f10f86e278cd75d01e33e0b938a67c92da7768b69e71c935f48afc3`  
		Last Modified: Wed, 11 Nov 2020 21:12:01 GMT  
		Size: 15.7 MB (15719429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eceba769c18a7fcc04fee517704a192fa8be4d7088e154e7a50c88798edba8a`  
		Last Modified: Wed, 11 Nov 2020 21:11:57 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991cb5466ff2322d74e916ae72627b5135bb9145f2ed8e7685b074e97577df09`  
		Last Modified: Wed, 11 Nov 2020 21:11:57 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33136e45bd9883f075aa2c0808f6acbca8c87f35337e5510cd18b81286a9c685`  
		Last Modified: Wed, 11 Nov 2020 21:11:57 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-windowsservercore` - windows version 10.0.14393.4046; amd64

```console
$ docker pull nats-streaming@sha256:14845b830cedb23f3f7ed8f10807e8282b1aa7282e781cc093c81a9de949c424
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5792743732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2508615fd60d3454afda9bed5da8fc813dda0056e0a907e7383428d5adb1a5`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 14:26:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:03:39 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:08:29 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Wed, 11 Nov 2020 21:08:29 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Wed, 11 Nov 2020 21:08:30 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Wed, 11 Nov 2020 21:09:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 21:11:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 21:11:28 GMT
EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:11:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:11:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9affba5fa493b09d48e6bd56c0d7b0eb03d1dbaa80493dd08cb18a3c9ddfbb67`  
		Last Modified: Wed, 11 Nov 2020 16:54:10 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d795e5fc593aa74d082785c3c5a0c7852d30cfdd8a38a78310041e80dbb85b`  
		Last Modified: Wed, 11 Nov 2020 17:08:28 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c24da67ed7c6acb854c9dfb40d1a0d214c738a7cdb25cb13fb8eaa827bdaed`  
		Last Modified: Wed, 11 Nov 2020 21:12:42 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec404db08fd423d5c74b68d72f211ff9d0ff4dd5f06af915570c70221dc38a8d`  
		Last Modified: Wed, 11 Nov 2020 21:12:42 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8678193ddf486b932d452d114feb2f659b2b068f0f13fd8bbec010bfd721ac01`  
		Last Modified: Wed, 11 Nov 2020 21:12:42 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52a6f57a30a085cede0cec8050b64dcd7c5e4a8ca3014f6a052f4c3f7c4c935`  
		Last Modified: Wed, 11 Nov 2020 21:12:40 GMT  
		Size: 5.6 MB (5555036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df35b5161c0e10dd39781904d86655a44f5174f9cc5746b2dd2cbc835e72e8`  
		Last Modified: Wed, 11 Nov 2020 21:12:44 GMT  
		Size: 16.6 MB (16620665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46392d5e7ade5dba167c923acbdd2234f50929f5c380dc53527aa2f9ae1d1770`  
		Last Modified: Wed, 11 Nov 2020 21:12:39 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30d3e9fdbdc63c0c724a9739e25266e6b9b064801e212e7520eeef09a20a079`  
		Last Modified: Wed, 11 Nov 2020 21:12:39 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775e68e8a6de3cc6a0b1806887ac4d56cde5b1a9009b9e7eb3184ed457f4fd43`  
		Last Modified: Wed, 11 Nov 2020 21:12:39 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:27423c80379de66c39c6657edc21cb4086e162c76f91d2b3913005ab762d55ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats-streaming:0.19.0-windowsservercore-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats-streaming@sha256:e755a0f47c43b1e70859439f16decaa2b537c74f13a21233cc5dfa56946b9eed
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408607752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2a802c225aed1fa376c8c360c0f85bb4fc66c60f7252b572d17344853d5c34`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 14:18:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:01:32 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:06:07 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Wed, 11 Nov 2020 21:06:08 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Wed, 11 Nov 2020 21:06:09 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Wed, 11 Nov 2020 21:06:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 21:07:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 21:07:59 GMT
EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:08:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:08:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e03cd29396986910a2aaaf968e93bebcaf4b0101821290e0560b401893615ccf`  
		Last Modified: Wed, 11 Nov 2020 16:53:20 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d59214fb7b605a325f942085c8f9dbcc4fa01cb3626a6eaf07a0e437729d5e4`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ccb5a272f7fb60c5ebcc0895833f8d509159a12d346133338a7de41f5dbf1a`  
		Last Modified: Wed, 11 Nov 2020 21:12:01 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe86ff1d99293de35c3769b0edf2c049693415fce2d6c8984756fa96495f0c6d`  
		Last Modified: Wed, 11 Nov 2020 21:12:01 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72dc12d6621abb0db2c34f8038dfbd974eb00174dea1f54c523d67fb442efca`  
		Last Modified: Wed, 11 Nov 2020 21:12:00 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c90fa3489aac1add86a6b50c3f496d21100dd6742c75c3d557fad5ae4d7e9d`  
		Last Modified: Wed, 11 Nov 2020 21:11:58 GMT  
		Size: 4.8 MB (4849948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6e8fe6f10f86e278cd75d01e33e0b938a67c92da7768b69e71c935f48afc3`  
		Last Modified: Wed, 11 Nov 2020 21:12:01 GMT  
		Size: 15.7 MB (15719429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eceba769c18a7fcc04fee517704a192fa8be4d7088e154e7a50c88798edba8a`  
		Last Modified: Wed, 11 Nov 2020 21:11:57 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991cb5466ff2322d74e916ae72627b5135bb9145f2ed8e7685b074e97577df09`  
		Last Modified: Wed, 11 Nov 2020 21:11:57 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33136e45bd9883f075aa2c0808f6acbca8c87f35337e5510cd18b81286a9c685`  
		Last Modified: Wed, 11 Nov 2020 21:11:57 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0-windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:6c39e86cd4877f2acaed573b69f7da2e3aeebb06ce63bc39949d9572b8df86f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4046; amd64

### `nats-streaming:0.19.0-windowsservercore-ltsc2016` - windows version 10.0.14393.4046; amd64

```console
$ docker pull nats-streaming@sha256:14845b830cedb23f3f7ed8f10807e8282b1aa7282e781cc093c81a9de949c424
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5792743732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2508615fd60d3454afda9bed5da8fc813dda0056e0a907e7383428d5adb1a5`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 14:26:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:03:39 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:08:29 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Wed, 11 Nov 2020 21:08:29 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Wed, 11 Nov 2020 21:08:30 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Wed, 11 Nov 2020 21:09:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 21:11:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 21:11:28 GMT
EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:11:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:11:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9affba5fa493b09d48e6bd56c0d7b0eb03d1dbaa80493dd08cb18a3c9ddfbb67`  
		Last Modified: Wed, 11 Nov 2020 16:54:10 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d795e5fc593aa74d082785c3c5a0c7852d30cfdd8a38a78310041e80dbb85b`  
		Last Modified: Wed, 11 Nov 2020 17:08:28 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c24da67ed7c6acb854c9dfb40d1a0d214c738a7cdb25cb13fb8eaa827bdaed`  
		Last Modified: Wed, 11 Nov 2020 21:12:42 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec404db08fd423d5c74b68d72f211ff9d0ff4dd5f06af915570c70221dc38a8d`  
		Last Modified: Wed, 11 Nov 2020 21:12:42 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8678193ddf486b932d452d114feb2f659b2b068f0f13fd8bbec010bfd721ac01`  
		Last Modified: Wed, 11 Nov 2020 21:12:42 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52a6f57a30a085cede0cec8050b64dcd7c5e4a8ca3014f6a052f4c3f7c4c935`  
		Last Modified: Wed, 11 Nov 2020 21:12:40 GMT  
		Size: 5.6 MB (5555036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df35b5161c0e10dd39781904d86655a44f5174f9cc5746b2dd2cbc835e72e8`  
		Last Modified: Wed, 11 Nov 2020 21:12:44 GMT  
		Size: 16.6 MB (16620665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46392d5e7ade5dba167c923acbdd2234f50929f5c380dc53527aa2f9ae1d1770`  
		Last Modified: Wed, 11 Nov 2020 21:12:39 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30d3e9fdbdc63c0c724a9739e25266e6b9b064801e212e7520eeef09a20a079`  
		Last Modified: Wed, 11 Nov 2020 21:12:39 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775e68e8a6de3cc6a0b1806887ac4d56cde5b1a9009b9e7eb3184ed457f4fd43`  
		Last Modified: Wed, 11 Nov 2020 21:12:39 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19-alpine`

```console
$ docker pull nats-streaming@sha256:5f15b51b2b447004408633f8f9458106fadad8f21393b1ed531071731e1ddb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.19-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:a8fcf986c14ae3ad60206bd6ebde23999c28f9967f05b9c81a760054539a683d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20b4ccbdde21c3fb61f4bd7fa3e83384f7e9d7f32f5bb86c88cd162a41403c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:33:01 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:33:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:33:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:33:04 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:33:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f211ef5561f154a9a5957cdf08a625861df698594add9ba490a54259e9a01cb1`  
		Last Modified: Tue, 03 Nov 2020 00:33:28 GMT  
		Size: 6.8 MB (6770312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eef7e98823e252892036fb4b7e5ccf695c556028fa2f7dd6dc314f625ba9eb9`  
		Last Modified: Tue, 03 Nov 2020 00:33:27 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:2a58d6644e94cc17212ec6a604029ebe9f855ceeee7fa66171bdc8aa6c7113ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8932203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8391afd58a04ec8cf1ab166357c9495c5aa4d32bc4bb4472e577874f42fe55d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:56:13 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Mon, 02 Nov 2020 23:56:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:56:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 02 Nov 2020 23:56:18 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:56:19 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cba1ed5b5094a02c017d654b758674905ec0bb2535d3311fcdd61dce32b319`  
		Last Modified: Mon, 02 Nov 2020 23:56:50 GMT  
		Size: 6.3 MB (6329871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3992f15ff4c1a7660c4a81854ec33d3e4973405c7095ceb0bd8a7865fff21c9f`  
		Last Modified: Mon, 02 Nov 2020 23:56:47 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:6a6c52fc272b91cff878ca25bddc432f19583a2e41e5e92288f0e64d0c649896
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8730479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4347330ee2d9b26f7fafaadc370627e71670505b340c9e4b54d791afcb3a6b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:05:05 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:05:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:05:09 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:05:10 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:05:11 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34033d6dabe9c0f77f765bf2fce39f1eef24c163cfa802ec78f0e2e1bea9da7c`  
		Last Modified: Tue, 03 Nov 2020 00:05:43 GMT  
		Size: 6.3 MB (6324384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0a98c9d7b5d859df80140920031b236b38ff88a4ff09d3bf8cfc5b9776e436`  
		Last Modified: Tue, 03 Nov 2020 00:05:40 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:36be57b574502addd00c81caaffedb9030eec583dbf4e3011a95aa7f998834aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8969159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b947ac7936fa0250ecf3f1aaa6e22a928bdb3cdd8f0dcbbc3b8912a0678290c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:43:12 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:43:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:43:21 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:43:23 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:43:27 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea83a41655c390ae2bea2fd6f2a83188ecb9c82e60ebde8040109e79a2eba5`  
		Last Modified: Tue, 03 Nov 2020 00:44:06 GMT  
		Size: 6.3 MB (6262183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eca3d16e3b7142a6392c550b0efad91076053f222028892a3ae01e63f58dec`  
		Last Modified: Tue, 03 Nov 2020 00:44:05 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19-alpine3.12`

```console
$ docker pull nats-streaming@sha256:5f15b51b2b447004408633f8f9458106fadad8f21393b1ed531071731e1ddb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.19-alpine3.12` - linux; amd64

```console
$ docker pull nats-streaming@sha256:a8fcf986c14ae3ad60206bd6ebde23999c28f9967f05b9c81a760054539a683d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20b4ccbdde21c3fb61f4bd7fa3e83384f7e9d7f32f5bb86c88cd162a41403c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:33:01 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:33:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:33:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:33:04 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:33:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f211ef5561f154a9a5957cdf08a625861df698594add9ba490a54259e9a01cb1`  
		Last Modified: Tue, 03 Nov 2020 00:33:28 GMT  
		Size: 6.8 MB (6770312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eef7e98823e252892036fb4b7e5ccf695c556028fa2f7dd6dc314f625ba9eb9`  
		Last Modified: Tue, 03 Nov 2020 00:33:27 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-alpine3.12` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:2a58d6644e94cc17212ec6a604029ebe9f855ceeee7fa66171bdc8aa6c7113ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8932203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8391afd58a04ec8cf1ab166357c9495c5aa4d32bc4bb4472e577874f42fe55d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:56:13 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Mon, 02 Nov 2020 23:56:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:56:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 02 Nov 2020 23:56:18 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:56:19 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cba1ed5b5094a02c017d654b758674905ec0bb2535d3311fcdd61dce32b319`  
		Last Modified: Mon, 02 Nov 2020 23:56:50 GMT  
		Size: 6.3 MB (6329871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3992f15ff4c1a7660c4a81854ec33d3e4973405c7095ceb0bd8a7865fff21c9f`  
		Last Modified: Mon, 02 Nov 2020 23:56:47 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-alpine3.12` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:6a6c52fc272b91cff878ca25bddc432f19583a2e41e5e92288f0e64d0c649896
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8730479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4347330ee2d9b26f7fafaadc370627e71670505b340c9e4b54d791afcb3a6b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:05:05 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:05:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:05:09 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:05:10 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:05:11 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34033d6dabe9c0f77f765bf2fce39f1eef24c163cfa802ec78f0e2e1bea9da7c`  
		Last Modified: Tue, 03 Nov 2020 00:05:43 GMT  
		Size: 6.3 MB (6324384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0a98c9d7b5d859df80140920031b236b38ff88a4ff09d3bf8cfc5b9776e436`  
		Last Modified: Tue, 03 Nov 2020 00:05:40 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:36be57b574502addd00c81caaffedb9030eec583dbf4e3011a95aa7f998834aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8969159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b947ac7936fa0250ecf3f1aaa6e22a928bdb3cdd8f0dcbbc3b8912a0678290c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:43:12 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:43:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:43:21 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:43:23 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:43:27 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea83a41655c390ae2bea2fd6f2a83188ecb9c82e60ebde8040109e79a2eba5`  
		Last Modified: Tue, 03 Nov 2020 00:44:06 GMT  
		Size: 6.3 MB (6262183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eca3d16e3b7142a6392c550b0efad91076053f222028892a3ae01e63f58dec`  
		Last Modified: Tue, 03 Nov 2020 00:44:05 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19-linux`

```console
$ docker pull nats-streaming@sha256:8001e4db36785bd692d9ae1c9ed3857d972692b385e36c08994794a5254bb78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.19-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:053a4ca3955b9c5036e48bafb96c83003fe86c34c6928934e3fd1db0529a889c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6487259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a204b53252cabfc16952c1d2dc014dc6518d1a08d00bda1bc5008a139e37a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:33:13 GMT
COPY file:3ed83d1497b0535960e452435cb8b27e347f48da12693aa27ebaf9bff94d82de in /nats-streaming-server 
# Tue, 03 Nov 2020 00:33:13 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:33:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:57ac21f890a508f609eabea265197b18ce9dfe3e694034c7a06d37b536a707b2`  
		Last Modified: Tue, 03 Nov 2020 00:33:37 GMT  
		Size: 6.5 MB (6487259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:f334d10ef2a4663d8d7d920d96321cd97f050b82a5d55d588192f074f60dd814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecfd5ab4178a65e952a7cf1d248a556a6ae2c328ac8b68923146d64734db03`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Nov 2020 23:56:28 GMT
COPY file:d6896b1c93dcd497494c972f9274fcc634a4f4a8d63a0191bdb87f6336aec0d7 in /nats-streaming-server 
# Mon, 02 Nov 2020 23:56:28 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 02 Nov 2020 23:56:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7f165fb71ab77e8081dbfa13656cdf9e5e005002d6c3afa0aac40667a0f97af8`  
		Last Modified: Mon, 02 Nov 2020 23:57:04 GMT  
		Size: 6.0 MB (6049845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:5fd0943909d8aedafb888e099c9f64d234023ad780805ed7c939692ebfd8304d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37071e856ae40dc3c8c5e10b359d1640fd67a6110741c0957af2031032ed6ce`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:05:23 GMT
COPY file:d232132ddff1d85d3a2f5c80a91c80023cbc103d816387e06d604cf97238e52c in /nats-streaming-server 
# Tue, 03 Nov 2020 00:05:24 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:05:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c7227cc1040d04ca7763cfb53ab58bc32ae54921990516adf8e13374ac9ef29`  
		Last Modified: Tue, 03 Nov 2020 00:05:57 GMT  
		Size: 6.0 MB (6043163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c058fd3e9a8ac44263bf53fa2f6f1e8e8cb3e95cd223f8353fdafc50fe57e417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a80bd440362bd4a6743fee8134a3caf6271e3258e449fb106b19c050a3b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:43:38 GMT
COPY file:55e70ee826cd5a662497337a2488e22833672bd031d85b4ee39556ab1e80df08 in /nats-streaming-server 
# Tue, 03 Nov 2020 00:43:40 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:43:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3dc58a59de8a6ed19e9144b0189eb3b637a9e7fcd76ec6c6dc47561b2740a3a2`  
		Last Modified: Tue, 03 Nov 2020 00:44:19 GMT  
		Size: 6.0 MB (5978846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19-nanoserver`

```console
$ docker pull nats-streaming@sha256:12751d89716d394331c32e35fbed0b0bdb912c970c0b5823ed7ebb6198731757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats-streaming:0.19-nanoserver` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats-streaming@sha256:44cd613007d0ae80aa675e256fcf7ab09154970b8489a02e0d1969c6143d1f61
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107798464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7c11af94433f8f6727ec8b965b09721a359d79801411d21199752bff82c385`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:08:21 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:08:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdd54301a97b4ec40a4f7841d98c5c1650eb782b9fa39fa6fd69336f53ee64`  
		Last Modified: Wed, 11 Nov 2020 21:12:25 GMT  
		Size: 6.5 MB (6515173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e84d935a5287b8d02f7d552ad42e43d116f9f8e81a3ab6938ce0bf2f6a98cd`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9847a1462f5644588430244c224e5ee90473d31bf4d0c11157ec2a823aaae1ca`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 927.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e882e784f1673e88e962c1e9a1239de9107334f963eef6c696f80bd1a04f063`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:12751d89716d394331c32e35fbed0b0bdb912c970c0b5823ed7ebb6198731757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats-streaming:0.19-nanoserver-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats-streaming@sha256:44cd613007d0ae80aa675e256fcf7ab09154970b8489a02e0d1969c6143d1f61
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107798464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7c11af94433f8f6727ec8b965b09721a359d79801411d21199752bff82c385`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:08:21 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:08:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdd54301a97b4ec40a4f7841d98c5c1650eb782b9fa39fa6fd69336f53ee64`  
		Last Modified: Wed, 11 Nov 2020 21:12:25 GMT  
		Size: 6.5 MB (6515173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e84d935a5287b8d02f7d552ad42e43d116f9f8e81a3ab6938ce0bf2f6a98cd`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9847a1462f5644588430244c224e5ee90473d31bf4d0c11157ec2a823aaae1ca`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 927.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e882e784f1673e88e962c1e9a1239de9107334f963eef6c696f80bd1a04f063`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19-scratch`

```console
$ docker pull nats-streaming@sha256:8001e4db36785bd692d9ae1c9ed3857d972692b385e36c08994794a5254bb78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.19-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:053a4ca3955b9c5036e48bafb96c83003fe86c34c6928934e3fd1db0529a889c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6487259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a204b53252cabfc16952c1d2dc014dc6518d1a08d00bda1bc5008a139e37a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:33:13 GMT
COPY file:3ed83d1497b0535960e452435cb8b27e347f48da12693aa27ebaf9bff94d82de in /nats-streaming-server 
# Tue, 03 Nov 2020 00:33:13 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:33:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:57ac21f890a508f609eabea265197b18ce9dfe3e694034c7a06d37b536a707b2`  
		Last Modified: Tue, 03 Nov 2020 00:33:37 GMT  
		Size: 6.5 MB (6487259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:f334d10ef2a4663d8d7d920d96321cd97f050b82a5d55d588192f074f60dd814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecfd5ab4178a65e952a7cf1d248a556a6ae2c328ac8b68923146d64734db03`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Nov 2020 23:56:28 GMT
COPY file:d6896b1c93dcd497494c972f9274fcc634a4f4a8d63a0191bdb87f6336aec0d7 in /nats-streaming-server 
# Mon, 02 Nov 2020 23:56:28 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 02 Nov 2020 23:56:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7f165fb71ab77e8081dbfa13656cdf9e5e005002d6c3afa0aac40667a0f97af8`  
		Last Modified: Mon, 02 Nov 2020 23:57:04 GMT  
		Size: 6.0 MB (6049845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:5fd0943909d8aedafb888e099c9f64d234023ad780805ed7c939692ebfd8304d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37071e856ae40dc3c8c5e10b359d1640fd67a6110741c0957af2031032ed6ce`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:05:23 GMT
COPY file:d232132ddff1d85d3a2f5c80a91c80023cbc103d816387e06d604cf97238e52c in /nats-streaming-server 
# Tue, 03 Nov 2020 00:05:24 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:05:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c7227cc1040d04ca7763cfb53ab58bc32ae54921990516adf8e13374ac9ef29`  
		Last Modified: Tue, 03 Nov 2020 00:05:57 GMT  
		Size: 6.0 MB (6043163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c058fd3e9a8ac44263bf53fa2f6f1e8e8cb3e95cd223f8353fdafc50fe57e417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a80bd440362bd4a6743fee8134a3caf6271e3258e449fb106b19c050a3b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:43:38 GMT
COPY file:55e70ee826cd5a662497337a2488e22833672bd031d85b4ee39556ab1e80df08 in /nats-streaming-server 
# Tue, 03 Nov 2020 00:43:40 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:43:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3dc58a59de8a6ed19e9144b0189eb3b637a9e7fcd76ec6c6dc47561b2740a3a2`  
		Last Modified: Tue, 03 Nov 2020 00:44:19 GMT  
		Size: 6.0 MB (5978846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19-windowsservercore`

```console
$ docker pull nats-streaming@sha256:fed1fdbe6cf90f50e143730f5723bfd36abeffebda44d72d35336e144d266c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64
	-	windows version 10.0.14393.4046; amd64

### `nats-streaming:0.19-windowsservercore` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats-streaming@sha256:e755a0f47c43b1e70859439f16decaa2b537c74f13a21233cc5dfa56946b9eed
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408607752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2a802c225aed1fa376c8c360c0f85bb4fc66c60f7252b572d17344853d5c34`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 14:18:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:01:32 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:06:07 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Wed, 11 Nov 2020 21:06:08 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Wed, 11 Nov 2020 21:06:09 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Wed, 11 Nov 2020 21:06:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 21:07:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 21:07:59 GMT
EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:08:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:08:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e03cd29396986910a2aaaf968e93bebcaf4b0101821290e0560b401893615ccf`  
		Last Modified: Wed, 11 Nov 2020 16:53:20 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d59214fb7b605a325f942085c8f9dbcc4fa01cb3626a6eaf07a0e437729d5e4`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ccb5a272f7fb60c5ebcc0895833f8d509159a12d346133338a7de41f5dbf1a`  
		Last Modified: Wed, 11 Nov 2020 21:12:01 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe86ff1d99293de35c3769b0edf2c049693415fce2d6c8984756fa96495f0c6d`  
		Last Modified: Wed, 11 Nov 2020 21:12:01 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72dc12d6621abb0db2c34f8038dfbd974eb00174dea1f54c523d67fb442efca`  
		Last Modified: Wed, 11 Nov 2020 21:12:00 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c90fa3489aac1add86a6b50c3f496d21100dd6742c75c3d557fad5ae4d7e9d`  
		Last Modified: Wed, 11 Nov 2020 21:11:58 GMT  
		Size: 4.8 MB (4849948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6e8fe6f10f86e278cd75d01e33e0b938a67c92da7768b69e71c935f48afc3`  
		Last Modified: Wed, 11 Nov 2020 21:12:01 GMT  
		Size: 15.7 MB (15719429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eceba769c18a7fcc04fee517704a192fa8be4d7088e154e7a50c88798edba8a`  
		Last Modified: Wed, 11 Nov 2020 21:11:57 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991cb5466ff2322d74e916ae72627b5135bb9145f2ed8e7685b074e97577df09`  
		Last Modified: Wed, 11 Nov 2020 21:11:57 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33136e45bd9883f075aa2c0808f6acbca8c87f35337e5510cd18b81286a9c685`  
		Last Modified: Wed, 11 Nov 2020 21:11:57 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-windowsservercore` - windows version 10.0.14393.4046; amd64

```console
$ docker pull nats-streaming@sha256:14845b830cedb23f3f7ed8f10807e8282b1aa7282e781cc093c81a9de949c424
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5792743732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2508615fd60d3454afda9bed5da8fc813dda0056e0a907e7383428d5adb1a5`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 14:26:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:03:39 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:08:29 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Wed, 11 Nov 2020 21:08:29 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Wed, 11 Nov 2020 21:08:30 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Wed, 11 Nov 2020 21:09:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 21:11:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 21:11:28 GMT
EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:11:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:11:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9affba5fa493b09d48e6bd56c0d7b0eb03d1dbaa80493dd08cb18a3c9ddfbb67`  
		Last Modified: Wed, 11 Nov 2020 16:54:10 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d795e5fc593aa74d082785c3c5a0c7852d30cfdd8a38a78310041e80dbb85b`  
		Last Modified: Wed, 11 Nov 2020 17:08:28 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c24da67ed7c6acb854c9dfb40d1a0d214c738a7cdb25cb13fb8eaa827bdaed`  
		Last Modified: Wed, 11 Nov 2020 21:12:42 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec404db08fd423d5c74b68d72f211ff9d0ff4dd5f06af915570c70221dc38a8d`  
		Last Modified: Wed, 11 Nov 2020 21:12:42 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8678193ddf486b932d452d114feb2f659b2b068f0f13fd8bbec010bfd721ac01`  
		Last Modified: Wed, 11 Nov 2020 21:12:42 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52a6f57a30a085cede0cec8050b64dcd7c5e4a8ca3014f6a052f4c3f7c4c935`  
		Last Modified: Wed, 11 Nov 2020 21:12:40 GMT  
		Size: 5.6 MB (5555036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df35b5161c0e10dd39781904d86655a44f5174f9cc5746b2dd2cbc835e72e8`  
		Last Modified: Wed, 11 Nov 2020 21:12:44 GMT  
		Size: 16.6 MB (16620665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46392d5e7ade5dba167c923acbdd2234f50929f5c380dc53527aa2f9ae1d1770`  
		Last Modified: Wed, 11 Nov 2020 21:12:39 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30d3e9fdbdc63c0c724a9739e25266e6b9b064801e212e7520eeef09a20a079`  
		Last Modified: Wed, 11 Nov 2020 21:12:39 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775e68e8a6de3cc6a0b1806887ac4d56cde5b1a9009b9e7eb3184ed457f4fd43`  
		Last Modified: Wed, 11 Nov 2020 21:12:39 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:27423c80379de66c39c6657edc21cb4086e162c76f91d2b3913005ab762d55ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats-streaming:0.19-windowsservercore-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats-streaming@sha256:e755a0f47c43b1e70859439f16decaa2b537c74f13a21233cc5dfa56946b9eed
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408607752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2a802c225aed1fa376c8c360c0f85bb4fc66c60f7252b572d17344853d5c34`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 14:18:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:01:32 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:06:07 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Wed, 11 Nov 2020 21:06:08 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Wed, 11 Nov 2020 21:06:09 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Wed, 11 Nov 2020 21:06:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 21:07:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 21:07:59 GMT
EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:08:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:08:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e03cd29396986910a2aaaf968e93bebcaf4b0101821290e0560b401893615ccf`  
		Last Modified: Wed, 11 Nov 2020 16:53:20 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d59214fb7b605a325f942085c8f9dbcc4fa01cb3626a6eaf07a0e437729d5e4`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ccb5a272f7fb60c5ebcc0895833f8d509159a12d346133338a7de41f5dbf1a`  
		Last Modified: Wed, 11 Nov 2020 21:12:01 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe86ff1d99293de35c3769b0edf2c049693415fce2d6c8984756fa96495f0c6d`  
		Last Modified: Wed, 11 Nov 2020 21:12:01 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72dc12d6621abb0db2c34f8038dfbd974eb00174dea1f54c523d67fb442efca`  
		Last Modified: Wed, 11 Nov 2020 21:12:00 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c90fa3489aac1add86a6b50c3f496d21100dd6742c75c3d557fad5ae4d7e9d`  
		Last Modified: Wed, 11 Nov 2020 21:11:58 GMT  
		Size: 4.8 MB (4849948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6e8fe6f10f86e278cd75d01e33e0b938a67c92da7768b69e71c935f48afc3`  
		Last Modified: Wed, 11 Nov 2020 21:12:01 GMT  
		Size: 15.7 MB (15719429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eceba769c18a7fcc04fee517704a192fa8be4d7088e154e7a50c88798edba8a`  
		Last Modified: Wed, 11 Nov 2020 21:11:57 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991cb5466ff2322d74e916ae72627b5135bb9145f2ed8e7685b074e97577df09`  
		Last Modified: Wed, 11 Nov 2020 21:11:57 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33136e45bd9883f075aa2c0808f6acbca8c87f35337e5510cd18b81286a9c685`  
		Last Modified: Wed, 11 Nov 2020 21:11:57 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19-windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:6c39e86cd4877f2acaed573b69f7da2e3aeebb06ce63bc39949d9572b8df86f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4046; amd64

### `nats-streaming:0.19-windowsservercore-ltsc2016` - windows version 10.0.14393.4046; amd64

```console
$ docker pull nats-streaming@sha256:14845b830cedb23f3f7ed8f10807e8282b1aa7282e781cc093c81a9de949c424
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5792743732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2508615fd60d3454afda9bed5da8fc813dda0056e0a907e7383428d5adb1a5`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 14:26:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:03:39 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:08:29 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Wed, 11 Nov 2020 21:08:29 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Wed, 11 Nov 2020 21:08:30 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Wed, 11 Nov 2020 21:09:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 21:11:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 21:11:28 GMT
EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:11:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:11:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9affba5fa493b09d48e6bd56c0d7b0eb03d1dbaa80493dd08cb18a3c9ddfbb67`  
		Last Modified: Wed, 11 Nov 2020 16:54:10 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d795e5fc593aa74d082785c3c5a0c7852d30cfdd8a38a78310041e80dbb85b`  
		Last Modified: Wed, 11 Nov 2020 17:08:28 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c24da67ed7c6acb854c9dfb40d1a0d214c738a7cdb25cb13fb8eaa827bdaed`  
		Last Modified: Wed, 11 Nov 2020 21:12:42 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec404db08fd423d5c74b68d72f211ff9d0ff4dd5f06af915570c70221dc38a8d`  
		Last Modified: Wed, 11 Nov 2020 21:12:42 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8678193ddf486b932d452d114feb2f659b2b068f0f13fd8bbec010bfd721ac01`  
		Last Modified: Wed, 11 Nov 2020 21:12:42 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52a6f57a30a085cede0cec8050b64dcd7c5e4a8ca3014f6a052f4c3f7c4c935`  
		Last Modified: Wed, 11 Nov 2020 21:12:40 GMT  
		Size: 5.6 MB (5555036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df35b5161c0e10dd39781904d86655a44f5174f9cc5746b2dd2cbc835e72e8`  
		Last Modified: Wed, 11 Nov 2020 21:12:44 GMT  
		Size: 16.6 MB (16620665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46392d5e7ade5dba167c923acbdd2234f50929f5c380dc53527aa2f9ae1d1770`  
		Last Modified: Wed, 11 Nov 2020 21:12:39 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30d3e9fdbdc63c0c724a9739e25266e6b9b064801e212e7520eeef09a20a079`  
		Last Modified: Wed, 11 Nov 2020 21:12:39 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775e68e8a6de3cc6a0b1806887ac4d56cde5b1a9009b9e7eb3184ed457f4fd43`  
		Last Modified: Wed, 11 Nov 2020 21:12:39 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:5f15b51b2b447004408633f8f9458106fadad8f21393b1ed531071731e1ddb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:a8fcf986c14ae3ad60206bd6ebde23999c28f9967f05b9c81a760054539a683d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20b4ccbdde21c3fb61f4bd7fa3e83384f7e9d7f32f5bb86c88cd162a41403c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:33:01 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:33:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:33:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:33:04 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:33:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f211ef5561f154a9a5957cdf08a625861df698594add9ba490a54259e9a01cb1`  
		Last Modified: Tue, 03 Nov 2020 00:33:28 GMT  
		Size: 6.8 MB (6770312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eef7e98823e252892036fb4b7e5ccf695c556028fa2f7dd6dc314f625ba9eb9`  
		Last Modified: Tue, 03 Nov 2020 00:33:27 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:2a58d6644e94cc17212ec6a604029ebe9f855ceeee7fa66171bdc8aa6c7113ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8932203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8391afd58a04ec8cf1ab166357c9495c5aa4d32bc4bb4472e577874f42fe55d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:56:13 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Mon, 02 Nov 2020 23:56:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:56:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 02 Nov 2020 23:56:18 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:56:19 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cba1ed5b5094a02c017d654b758674905ec0bb2535d3311fcdd61dce32b319`  
		Last Modified: Mon, 02 Nov 2020 23:56:50 GMT  
		Size: 6.3 MB (6329871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3992f15ff4c1a7660c4a81854ec33d3e4973405c7095ceb0bd8a7865fff21c9f`  
		Last Modified: Mon, 02 Nov 2020 23:56:47 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:6a6c52fc272b91cff878ca25bddc432f19583a2e41e5e92288f0e64d0c649896
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8730479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4347330ee2d9b26f7fafaadc370627e71670505b340c9e4b54d791afcb3a6b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:05:05 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:05:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:05:09 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:05:10 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:05:11 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34033d6dabe9c0f77f765bf2fce39f1eef24c163cfa802ec78f0e2e1bea9da7c`  
		Last Modified: Tue, 03 Nov 2020 00:05:43 GMT  
		Size: 6.3 MB (6324384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0a98c9d7b5d859df80140920031b236b38ff88a4ff09d3bf8cfc5b9776e436`  
		Last Modified: Tue, 03 Nov 2020 00:05:40 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:36be57b574502addd00c81caaffedb9030eec583dbf4e3011a95aa7f998834aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8969159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b947ac7936fa0250ecf3f1aaa6e22a928bdb3cdd8f0dcbbc3b8912a0678290c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:43:12 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:43:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:43:21 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:43:23 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:43:27 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea83a41655c390ae2bea2fd6f2a83188ecb9c82e60ebde8040109e79a2eba5`  
		Last Modified: Tue, 03 Nov 2020 00:44:06 GMT  
		Size: 6.3 MB (6262183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eca3d16e3b7142a6392c550b0efad91076053f222028892a3ae01e63f58dec`  
		Last Modified: Tue, 03 Nov 2020 00:44:05 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.12`

```console
$ docker pull nats-streaming@sha256:5f15b51b2b447004408633f8f9458106fadad8f21393b1ed531071731e1ddb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.12` - linux; amd64

```console
$ docker pull nats-streaming@sha256:a8fcf986c14ae3ad60206bd6ebde23999c28f9967f05b9c81a760054539a683d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20b4ccbdde21c3fb61f4bd7fa3e83384f7e9d7f32f5bb86c88cd162a41403c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:33:01 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:33:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:33:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:33:04 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:33:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f211ef5561f154a9a5957cdf08a625861df698594add9ba490a54259e9a01cb1`  
		Last Modified: Tue, 03 Nov 2020 00:33:28 GMT  
		Size: 6.8 MB (6770312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eef7e98823e252892036fb4b7e5ccf695c556028fa2f7dd6dc314f625ba9eb9`  
		Last Modified: Tue, 03 Nov 2020 00:33:27 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.12` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:2a58d6644e94cc17212ec6a604029ebe9f855ceeee7fa66171bdc8aa6c7113ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8932203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8391afd58a04ec8cf1ab166357c9495c5aa4d32bc4bb4472e577874f42fe55d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:56:13 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Mon, 02 Nov 2020 23:56:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:56:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 02 Nov 2020 23:56:18 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:56:19 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cba1ed5b5094a02c017d654b758674905ec0bb2535d3311fcdd61dce32b319`  
		Last Modified: Mon, 02 Nov 2020 23:56:50 GMT  
		Size: 6.3 MB (6329871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3992f15ff4c1a7660c4a81854ec33d3e4973405c7095ceb0bd8a7865fff21c9f`  
		Last Modified: Mon, 02 Nov 2020 23:56:47 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.12` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:6a6c52fc272b91cff878ca25bddc432f19583a2e41e5e92288f0e64d0c649896
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8730479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4347330ee2d9b26f7fafaadc370627e71670505b340c9e4b54d791afcb3a6b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:05:05 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:05:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:05:09 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:05:10 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:05:11 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34033d6dabe9c0f77f765bf2fce39f1eef24c163cfa802ec78f0e2e1bea9da7c`  
		Last Modified: Tue, 03 Nov 2020 00:05:43 GMT  
		Size: 6.3 MB (6324384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0a98c9d7b5d859df80140920031b236b38ff88a4ff09d3bf8cfc5b9776e436`  
		Last Modified: Tue, 03 Nov 2020 00:05:40 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:36be57b574502addd00c81caaffedb9030eec583dbf4e3011a95aa7f998834aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8969159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b947ac7936fa0250ecf3f1aaa6e22a928bdb3cdd8f0dcbbc3b8912a0678290c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:43:12 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:43:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:43:21 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:43:23 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:43:27 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea83a41655c390ae2bea2fd6f2a83188ecb9c82e60ebde8040109e79a2eba5`  
		Last Modified: Tue, 03 Nov 2020 00:44:06 GMT  
		Size: 6.3 MB (6262183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eca3d16e3b7142a6392c550b0efad91076053f222028892a3ae01e63f58dec`  
		Last Modified: Tue, 03 Nov 2020 00:44:05 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:ad99516ae96b71b512175c3fd60d580edecf6df8335e451053e9aea2e28bdffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1577; amd64

### `nats-streaming:latest` - linux; amd64

```console
$ docker pull nats-streaming@sha256:053a4ca3955b9c5036e48bafb96c83003fe86c34c6928934e3fd1db0529a889c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6487259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a204b53252cabfc16952c1d2dc014dc6518d1a08d00bda1bc5008a139e37a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:33:13 GMT
COPY file:3ed83d1497b0535960e452435cb8b27e347f48da12693aa27ebaf9bff94d82de in /nats-streaming-server 
# Tue, 03 Nov 2020 00:33:13 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:33:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:57ac21f890a508f609eabea265197b18ce9dfe3e694034c7a06d37b536a707b2`  
		Last Modified: Tue, 03 Nov 2020 00:33:37 GMT  
		Size: 6.5 MB (6487259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:f334d10ef2a4663d8d7d920d96321cd97f050b82a5d55d588192f074f60dd814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecfd5ab4178a65e952a7cf1d248a556a6ae2c328ac8b68923146d64734db03`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Nov 2020 23:56:28 GMT
COPY file:d6896b1c93dcd497494c972f9274fcc634a4f4a8d63a0191bdb87f6336aec0d7 in /nats-streaming-server 
# Mon, 02 Nov 2020 23:56:28 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 02 Nov 2020 23:56:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7f165fb71ab77e8081dbfa13656cdf9e5e005002d6c3afa0aac40667a0f97af8`  
		Last Modified: Mon, 02 Nov 2020 23:57:04 GMT  
		Size: 6.0 MB (6049845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:5fd0943909d8aedafb888e099c9f64d234023ad780805ed7c939692ebfd8304d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37071e856ae40dc3c8c5e10b359d1640fd67a6110741c0957af2031032ed6ce`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:05:23 GMT
COPY file:d232132ddff1d85d3a2f5c80a91c80023cbc103d816387e06d604cf97238e52c in /nats-streaming-server 
# Tue, 03 Nov 2020 00:05:24 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:05:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c7227cc1040d04ca7763cfb53ab58bc32ae54921990516adf8e13374ac9ef29`  
		Last Modified: Tue, 03 Nov 2020 00:05:57 GMT  
		Size: 6.0 MB (6043163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c058fd3e9a8ac44263bf53fa2f6f1e8e8cb3e95cd223f8353fdafc50fe57e417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a80bd440362bd4a6743fee8134a3caf6271e3258e449fb106b19c050a3b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:43:38 GMT
COPY file:55e70ee826cd5a662497337a2488e22833672bd031d85b4ee39556ab1e80df08 in /nats-streaming-server 
# Tue, 03 Nov 2020 00:43:40 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:43:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3dc58a59de8a6ed19e9144b0189eb3b637a9e7fcd76ec6c6dc47561b2740a3a2`  
		Last Modified: Tue, 03 Nov 2020 00:44:19 GMT  
		Size: 6.0 MB (5978846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats-streaming@sha256:44cd613007d0ae80aa675e256fcf7ab09154970b8489a02e0d1969c6143d1f61
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107798464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7c11af94433f8f6727ec8b965b09721a359d79801411d21199752bff82c385`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:08:21 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:08:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdd54301a97b4ec40a4f7841d98c5c1650eb782b9fa39fa6fd69336f53ee64`  
		Last Modified: Wed, 11 Nov 2020 21:12:25 GMT  
		Size: 6.5 MB (6515173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e84d935a5287b8d02f7d552ad42e43d116f9f8e81a3ab6938ce0bf2f6a98cd`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9847a1462f5644588430244c224e5ee90473d31bf4d0c11157ec2a823aaae1ca`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 927.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e882e784f1673e88e962c1e9a1239de9107334f963eef6c696f80bd1a04f063`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:8001e4db36785bd692d9ae1c9ed3857d972692b385e36c08994794a5254bb78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:053a4ca3955b9c5036e48bafb96c83003fe86c34c6928934e3fd1db0529a889c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6487259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a204b53252cabfc16952c1d2dc014dc6518d1a08d00bda1bc5008a139e37a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:33:13 GMT
COPY file:3ed83d1497b0535960e452435cb8b27e347f48da12693aa27ebaf9bff94d82de in /nats-streaming-server 
# Tue, 03 Nov 2020 00:33:13 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:33:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:57ac21f890a508f609eabea265197b18ce9dfe3e694034c7a06d37b536a707b2`  
		Last Modified: Tue, 03 Nov 2020 00:33:37 GMT  
		Size: 6.5 MB (6487259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:f334d10ef2a4663d8d7d920d96321cd97f050b82a5d55d588192f074f60dd814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecfd5ab4178a65e952a7cf1d248a556a6ae2c328ac8b68923146d64734db03`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Nov 2020 23:56:28 GMT
COPY file:d6896b1c93dcd497494c972f9274fcc634a4f4a8d63a0191bdb87f6336aec0d7 in /nats-streaming-server 
# Mon, 02 Nov 2020 23:56:28 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 02 Nov 2020 23:56:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7f165fb71ab77e8081dbfa13656cdf9e5e005002d6c3afa0aac40667a0f97af8`  
		Last Modified: Mon, 02 Nov 2020 23:57:04 GMT  
		Size: 6.0 MB (6049845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:5fd0943909d8aedafb888e099c9f64d234023ad780805ed7c939692ebfd8304d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37071e856ae40dc3c8c5e10b359d1640fd67a6110741c0957af2031032ed6ce`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:05:23 GMT
COPY file:d232132ddff1d85d3a2f5c80a91c80023cbc103d816387e06d604cf97238e52c in /nats-streaming-server 
# Tue, 03 Nov 2020 00:05:24 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:05:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c7227cc1040d04ca7763cfb53ab58bc32ae54921990516adf8e13374ac9ef29`  
		Last Modified: Tue, 03 Nov 2020 00:05:57 GMT  
		Size: 6.0 MB (6043163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c058fd3e9a8ac44263bf53fa2f6f1e8e8cb3e95cd223f8353fdafc50fe57e417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a80bd440362bd4a6743fee8134a3caf6271e3258e449fb106b19c050a3b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:43:38 GMT
COPY file:55e70ee826cd5a662497337a2488e22833672bd031d85b4ee39556ab1e80df08 in /nats-streaming-server 
# Tue, 03 Nov 2020 00:43:40 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:43:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3dc58a59de8a6ed19e9144b0189eb3b637a9e7fcd76ec6c6dc47561b2740a3a2`  
		Last Modified: Tue, 03 Nov 2020 00:44:19 GMT  
		Size: 6.0 MB (5978846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:12751d89716d394331c32e35fbed0b0bdb912c970c0b5823ed7ebb6198731757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats-streaming@sha256:44cd613007d0ae80aa675e256fcf7ab09154970b8489a02e0d1969c6143d1f61
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107798464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7c11af94433f8f6727ec8b965b09721a359d79801411d21199752bff82c385`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:08:21 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:08:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdd54301a97b4ec40a4f7841d98c5c1650eb782b9fa39fa6fd69336f53ee64`  
		Last Modified: Wed, 11 Nov 2020 21:12:25 GMT  
		Size: 6.5 MB (6515173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e84d935a5287b8d02f7d552ad42e43d116f9f8e81a3ab6938ce0bf2f6a98cd`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9847a1462f5644588430244c224e5ee90473d31bf4d0c11157ec2a823aaae1ca`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 927.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e882e784f1673e88e962c1e9a1239de9107334f963eef6c696f80bd1a04f063`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:12751d89716d394331c32e35fbed0b0bdb912c970c0b5823ed7ebb6198731757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats-streaming@sha256:44cd613007d0ae80aa675e256fcf7ab09154970b8489a02e0d1969c6143d1f61
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107798464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7c11af94433f8f6727ec8b965b09721a359d79801411d21199752bff82c385`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:08:21 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:08:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdd54301a97b4ec40a4f7841d98c5c1650eb782b9fa39fa6fd69336f53ee64`  
		Last Modified: Wed, 11 Nov 2020 21:12:25 GMT  
		Size: 6.5 MB (6515173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e84d935a5287b8d02f7d552ad42e43d116f9f8e81a3ab6938ce0bf2f6a98cd`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9847a1462f5644588430244c224e5ee90473d31bf4d0c11157ec2a823aaae1ca`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 927.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e882e784f1673e88e962c1e9a1239de9107334f963eef6c696f80bd1a04f063`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:8001e4db36785bd692d9ae1c9ed3857d972692b385e36c08994794a5254bb78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:053a4ca3955b9c5036e48bafb96c83003fe86c34c6928934e3fd1db0529a889c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6487259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a204b53252cabfc16952c1d2dc014dc6518d1a08d00bda1bc5008a139e37a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:33:13 GMT
COPY file:3ed83d1497b0535960e452435cb8b27e347f48da12693aa27ebaf9bff94d82de in /nats-streaming-server 
# Tue, 03 Nov 2020 00:33:13 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:33:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:57ac21f890a508f609eabea265197b18ce9dfe3e694034c7a06d37b536a707b2`  
		Last Modified: Tue, 03 Nov 2020 00:33:37 GMT  
		Size: 6.5 MB (6487259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:f334d10ef2a4663d8d7d920d96321cd97f050b82a5d55d588192f074f60dd814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecfd5ab4178a65e952a7cf1d248a556a6ae2c328ac8b68923146d64734db03`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Nov 2020 23:56:28 GMT
COPY file:d6896b1c93dcd497494c972f9274fcc634a4f4a8d63a0191bdb87f6336aec0d7 in /nats-streaming-server 
# Mon, 02 Nov 2020 23:56:28 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 02 Nov 2020 23:56:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7f165fb71ab77e8081dbfa13656cdf9e5e005002d6c3afa0aac40667a0f97af8`  
		Last Modified: Mon, 02 Nov 2020 23:57:04 GMT  
		Size: 6.0 MB (6049845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:5fd0943909d8aedafb888e099c9f64d234023ad780805ed7c939692ebfd8304d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37071e856ae40dc3c8c5e10b359d1640fd67a6110741c0957af2031032ed6ce`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:05:23 GMT
COPY file:d232132ddff1d85d3a2f5c80a91c80023cbc103d816387e06d604cf97238e52c in /nats-streaming-server 
# Tue, 03 Nov 2020 00:05:24 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:05:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c7227cc1040d04ca7763cfb53ab58bc32ae54921990516adf8e13374ac9ef29`  
		Last Modified: Tue, 03 Nov 2020 00:05:57 GMT  
		Size: 6.0 MB (6043163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c058fd3e9a8ac44263bf53fa2f6f1e8e8cb3e95cd223f8353fdafc50fe57e417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a80bd440362bd4a6743fee8134a3caf6271e3258e449fb106b19c050a3b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:43:38 GMT
COPY file:55e70ee826cd5a662497337a2488e22833672bd031d85b4ee39556ab1e80df08 in /nats-streaming-server 
# Tue, 03 Nov 2020 00:43:40 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:43:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3dc58a59de8a6ed19e9144b0189eb3b637a9e7fcd76ec6c6dc47561b2740a3a2`  
		Last Modified: Tue, 03 Nov 2020 00:44:19 GMT  
		Size: 6.0 MB (5978846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:fed1fdbe6cf90f50e143730f5723bfd36abeffebda44d72d35336e144d266c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64
	-	windows version 10.0.14393.4046; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats-streaming@sha256:e755a0f47c43b1e70859439f16decaa2b537c74f13a21233cc5dfa56946b9eed
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408607752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2a802c225aed1fa376c8c360c0f85bb4fc66c60f7252b572d17344853d5c34`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 14:18:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:01:32 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:06:07 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Wed, 11 Nov 2020 21:06:08 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Wed, 11 Nov 2020 21:06:09 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Wed, 11 Nov 2020 21:06:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 21:07:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 21:07:59 GMT
EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:08:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:08:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e03cd29396986910a2aaaf968e93bebcaf4b0101821290e0560b401893615ccf`  
		Last Modified: Wed, 11 Nov 2020 16:53:20 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d59214fb7b605a325f942085c8f9dbcc4fa01cb3626a6eaf07a0e437729d5e4`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ccb5a272f7fb60c5ebcc0895833f8d509159a12d346133338a7de41f5dbf1a`  
		Last Modified: Wed, 11 Nov 2020 21:12:01 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe86ff1d99293de35c3769b0edf2c049693415fce2d6c8984756fa96495f0c6d`  
		Last Modified: Wed, 11 Nov 2020 21:12:01 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72dc12d6621abb0db2c34f8038dfbd974eb00174dea1f54c523d67fb442efca`  
		Last Modified: Wed, 11 Nov 2020 21:12:00 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c90fa3489aac1add86a6b50c3f496d21100dd6742c75c3d557fad5ae4d7e9d`  
		Last Modified: Wed, 11 Nov 2020 21:11:58 GMT  
		Size: 4.8 MB (4849948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6e8fe6f10f86e278cd75d01e33e0b938a67c92da7768b69e71c935f48afc3`  
		Last Modified: Wed, 11 Nov 2020 21:12:01 GMT  
		Size: 15.7 MB (15719429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eceba769c18a7fcc04fee517704a192fa8be4d7088e154e7a50c88798edba8a`  
		Last Modified: Wed, 11 Nov 2020 21:11:57 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991cb5466ff2322d74e916ae72627b5135bb9145f2ed8e7685b074e97577df09`  
		Last Modified: Wed, 11 Nov 2020 21:11:57 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33136e45bd9883f075aa2c0808f6acbca8c87f35337e5510cd18b81286a9c685`  
		Last Modified: Wed, 11 Nov 2020 21:11:57 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:windowsservercore` - windows version 10.0.14393.4046; amd64

```console
$ docker pull nats-streaming@sha256:14845b830cedb23f3f7ed8f10807e8282b1aa7282e781cc093c81a9de949c424
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5792743732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2508615fd60d3454afda9bed5da8fc813dda0056e0a907e7383428d5adb1a5`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 14:26:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:03:39 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:08:29 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Wed, 11 Nov 2020 21:08:29 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Wed, 11 Nov 2020 21:08:30 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Wed, 11 Nov 2020 21:09:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 21:11:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 21:11:28 GMT
EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:11:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:11:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9affba5fa493b09d48e6bd56c0d7b0eb03d1dbaa80493dd08cb18a3c9ddfbb67`  
		Last Modified: Wed, 11 Nov 2020 16:54:10 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d795e5fc593aa74d082785c3c5a0c7852d30cfdd8a38a78310041e80dbb85b`  
		Last Modified: Wed, 11 Nov 2020 17:08:28 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c24da67ed7c6acb854c9dfb40d1a0d214c738a7cdb25cb13fb8eaa827bdaed`  
		Last Modified: Wed, 11 Nov 2020 21:12:42 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec404db08fd423d5c74b68d72f211ff9d0ff4dd5f06af915570c70221dc38a8d`  
		Last Modified: Wed, 11 Nov 2020 21:12:42 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8678193ddf486b932d452d114feb2f659b2b068f0f13fd8bbec010bfd721ac01`  
		Last Modified: Wed, 11 Nov 2020 21:12:42 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52a6f57a30a085cede0cec8050b64dcd7c5e4a8ca3014f6a052f4c3f7c4c935`  
		Last Modified: Wed, 11 Nov 2020 21:12:40 GMT  
		Size: 5.6 MB (5555036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df35b5161c0e10dd39781904d86655a44f5174f9cc5746b2dd2cbc835e72e8`  
		Last Modified: Wed, 11 Nov 2020 21:12:44 GMT  
		Size: 16.6 MB (16620665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46392d5e7ade5dba167c923acbdd2234f50929f5c380dc53527aa2f9ae1d1770`  
		Last Modified: Wed, 11 Nov 2020 21:12:39 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30d3e9fdbdc63c0c724a9739e25266e6b9b064801e212e7520eeef09a20a079`  
		Last Modified: Wed, 11 Nov 2020 21:12:39 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775e68e8a6de3cc6a0b1806887ac4d56cde5b1a9009b9e7eb3184ed457f4fd43`  
		Last Modified: Wed, 11 Nov 2020 21:12:39 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:27423c80379de66c39c6657edc21cb4086e162c76f91d2b3913005ab762d55ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats-streaming@sha256:e755a0f47c43b1e70859439f16decaa2b537c74f13a21233cc5dfa56946b9eed
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408607752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2a802c225aed1fa376c8c360c0f85bb4fc66c60f7252b572d17344853d5c34`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 14:18:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:01:32 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:06:07 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Wed, 11 Nov 2020 21:06:08 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Wed, 11 Nov 2020 21:06:09 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Wed, 11 Nov 2020 21:06:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 21:07:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 21:07:59 GMT
EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:08:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:08:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e03cd29396986910a2aaaf968e93bebcaf4b0101821290e0560b401893615ccf`  
		Last Modified: Wed, 11 Nov 2020 16:53:20 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d59214fb7b605a325f942085c8f9dbcc4fa01cb3626a6eaf07a0e437729d5e4`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ccb5a272f7fb60c5ebcc0895833f8d509159a12d346133338a7de41f5dbf1a`  
		Last Modified: Wed, 11 Nov 2020 21:12:01 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe86ff1d99293de35c3769b0edf2c049693415fce2d6c8984756fa96495f0c6d`  
		Last Modified: Wed, 11 Nov 2020 21:12:01 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72dc12d6621abb0db2c34f8038dfbd974eb00174dea1f54c523d67fb442efca`  
		Last Modified: Wed, 11 Nov 2020 21:12:00 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c90fa3489aac1add86a6b50c3f496d21100dd6742c75c3d557fad5ae4d7e9d`  
		Last Modified: Wed, 11 Nov 2020 21:11:58 GMT  
		Size: 4.8 MB (4849948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6e8fe6f10f86e278cd75d01e33e0b938a67c92da7768b69e71c935f48afc3`  
		Last Modified: Wed, 11 Nov 2020 21:12:01 GMT  
		Size: 15.7 MB (15719429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eceba769c18a7fcc04fee517704a192fa8be4d7088e154e7a50c88798edba8a`  
		Last Modified: Wed, 11 Nov 2020 21:11:57 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991cb5466ff2322d74e916ae72627b5135bb9145f2ed8e7685b074e97577df09`  
		Last Modified: Wed, 11 Nov 2020 21:11:57 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33136e45bd9883f075aa2c0808f6acbca8c87f35337e5510cd18b81286a9c685`  
		Last Modified: Wed, 11 Nov 2020 21:11:57 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:6c39e86cd4877f2acaed573b69f7da2e3aeebb06ce63bc39949d9572b8df86f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4046; amd64

### `nats-streaming:windowsservercore-ltsc2016` - windows version 10.0.14393.4046; amd64

```console
$ docker pull nats-streaming@sha256:14845b830cedb23f3f7ed8f10807e8282b1aa7282e781cc093c81a9de949c424
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5792743732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2508615fd60d3454afda9bed5da8fc813dda0056e0a907e7383428d5adb1a5`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 14:26:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:03:39 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:08:29 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Wed, 11 Nov 2020 21:08:29 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Wed, 11 Nov 2020 21:08:30 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Wed, 11 Nov 2020 21:09:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 21:11:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 21:11:28 GMT
EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:11:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:11:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9affba5fa493b09d48e6bd56c0d7b0eb03d1dbaa80493dd08cb18a3c9ddfbb67`  
		Last Modified: Wed, 11 Nov 2020 16:54:10 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d795e5fc593aa74d082785c3c5a0c7852d30cfdd8a38a78310041e80dbb85b`  
		Last Modified: Wed, 11 Nov 2020 17:08:28 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c24da67ed7c6acb854c9dfb40d1a0d214c738a7cdb25cb13fb8eaa827bdaed`  
		Last Modified: Wed, 11 Nov 2020 21:12:42 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec404db08fd423d5c74b68d72f211ff9d0ff4dd5f06af915570c70221dc38a8d`  
		Last Modified: Wed, 11 Nov 2020 21:12:42 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8678193ddf486b932d452d114feb2f659b2b068f0f13fd8bbec010bfd721ac01`  
		Last Modified: Wed, 11 Nov 2020 21:12:42 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52a6f57a30a085cede0cec8050b64dcd7c5e4a8ca3014f6a052f4c3f7c4c935`  
		Last Modified: Wed, 11 Nov 2020 21:12:40 GMT  
		Size: 5.6 MB (5555036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df35b5161c0e10dd39781904d86655a44f5174f9cc5746b2dd2cbc835e72e8`  
		Last Modified: Wed, 11 Nov 2020 21:12:44 GMT  
		Size: 16.6 MB (16620665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46392d5e7ade5dba167c923acbdd2234f50929f5c380dc53527aa2f9ae1d1770`  
		Last Modified: Wed, 11 Nov 2020 21:12:39 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30d3e9fdbdc63c0c724a9739e25266e6b9b064801e212e7520eeef09a20a079`  
		Last Modified: Wed, 11 Nov 2020 21:12:39 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775e68e8a6de3cc6a0b1806887ac4d56cde5b1a9009b9e7eb3184ed457f4fd43`  
		Last Modified: Wed, 11 Nov 2020 21:12:39 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

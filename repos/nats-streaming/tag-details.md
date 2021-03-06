<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats-streaming`

-	[`nats-streaming:0.21`](#nats-streaming021)
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
-	[`nats-streaming:0.21-alpine`](#nats-streaming021-alpine)
-	[`nats-streaming:0.21-alpine3.13`](#nats-streaming021-alpine313)
-	[`nats-streaming:0.21-linux`](#nats-streaming021-linux)
-	[`nats-streaming:0.21-nanoserver`](#nats-streaming021-nanoserver)
-	[`nats-streaming:0.21-nanoserver-1809`](#nats-streaming021-nanoserver-1809)
-	[`nats-streaming:0.21-scratch`](#nats-streaming021-scratch)
-	[`nats-streaming:0.21-windowsservercore`](#nats-streaming021-windowsservercore)
-	[`nats-streaming:0.21-windowsservercore-1809`](#nats-streaming021-windowsservercore-1809)
-	[`nats-streaming:0.21-windowsservercore-ltsc2016`](#nats-streaming021-windowsservercore-ltsc2016)
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
$ docker pull nats-streaming@sha256:e20f1649bb8b602a05fba0747e306280e129553c66c4de0194e1b04211323f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1757; amd64

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

### `nats-streaming:0.21` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats-streaming@sha256:761a9fae9a83a35868947aef2fef38e986bf238e5df545d02276993a3b1b3043
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107221484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31afc843a4cfc0bbe00476e4e93f5a7d4dd8e2fe55f5f1b84fe05c80f156ba48`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Feb 2021 13:06:30 GMT
RUN Apply image 1809-amd64
# Wed, 10 Feb 2021 16:02:26 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:17:29 GMT
RUN cmd /S /C #(nop) COPY file:189ca6af047e9f9cf54ab2176b48588e01c7497fe0b5b0d7b2614ebad66ed089 in C:\nats-streaming-server.exe 
# Sat, 06 Mar 2021 01:17:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:17:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:17:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ba17af31b9276ee11fdf859681b442db50979a39eff4cea2a559a5755cedbe01`  
		Size: 101.4 MB (101406193 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23b613036f8aee9066e712b3aa58f10f2fde093623511a5658867f53a6d01b18`  
		Last Modified: Wed, 10 Feb 2021 16:06:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83af691df7b0ece70ab41860e2add2cc454b31906aa7abb756bb166f50de6a93`  
		Last Modified: Sat, 06 Mar 2021 01:22:01 GMT  
		Size: 5.8 MB (5810692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ce94d4e2b26f5b27f5cd89d3b8172128fa8188838fa7c7103014b7afc5be8`  
		Last Modified: Sat, 06 Mar 2021 01:22:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcb8576081380a9b80744572a7960fcb1d30c0d85ea4bba32d1705b82658cd8`  
		Last Modified: Sat, 06 Mar 2021 01:22:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c3224120f5baf4ab134c2118bac99a39bc6e3f2dba314eb0053720c1d6c52f`  
		Last Modified: Sat, 06 Mar 2021 01:21:59 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.1`

```console
$ docker pull nats-streaming@sha256:e20f1649bb8b602a05fba0747e306280e129553c66c4de0194e1b04211323f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1757; amd64

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

### `nats-streaming:0.21.1` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats-streaming@sha256:761a9fae9a83a35868947aef2fef38e986bf238e5df545d02276993a3b1b3043
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107221484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31afc843a4cfc0bbe00476e4e93f5a7d4dd8e2fe55f5f1b84fe05c80f156ba48`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Feb 2021 13:06:30 GMT
RUN Apply image 1809-amd64
# Wed, 10 Feb 2021 16:02:26 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:17:29 GMT
RUN cmd /S /C #(nop) COPY file:189ca6af047e9f9cf54ab2176b48588e01c7497fe0b5b0d7b2614ebad66ed089 in C:\nats-streaming-server.exe 
# Sat, 06 Mar 2021 01:17:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:17:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:17:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ba17af31b9276ee11fdf859681b442db50979a39eff4cea2a559a5755cedbe01`  
		Size: 101.4 MB (101406193 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23b613036f8aee9066e712b3aa58f10f2fde093623511a5658867f53a6d01b18`  
		Last Modified: Wed, 10 Feb 2021 16:06:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83af691df7b0ece70ab41860e2add2cc454b31906aa7abb756bb166f50de6a93`  
		Last Modified: Sat, 06 Mar 2021 01:22:01 GMT  
		Size: 5.8 MB (5810692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ce94d4e2b26f5b27f5cd89d3b8172128fa8188838fa7c7103014b7afc5be8`  
		Last Modified: Sat, 06 Mar 2021 01:22:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcb8576081380a9b80744572a7960fcb1d30c0d85ea4bba32d1705b82658cd8`  
		Last Modified: Sat, 06 Mar 2021 01:22:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c3224120f5baf4ab134c2118bac99a39bc6e3f2dba314eb0053720c1d6c52f`  
		Last Modified: Sat, 06 Mar 2021 01:21:59 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.1-alpine`

```console
$ docker pull nats-streaming@sha256:d1bdcae6e682c875288aec0e01b192c753c516ddde6e8b5228583b2cde0671db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21.1-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:701fa3e7165e338d3fb61b4f7068af826829b094fc089e1b7866466bc4cba85e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8774552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3593598c050f5241766331b8aed01f6c3f42b71938fc11f47bbfa18d74c829be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 07:43:18 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 07:43:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 07:43:22 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 07:43:22 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 07:43:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:43:23 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae3e2d2b3e48427fd1213fbc4722666443f13ca1a6709825a2afbbf6381367d`  
		Last Modified: Sat, 06 Mar 2021 07:43:55 GMT  
		Size: 6.0 MB (5962472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a250278b77e3fdc0d10076a12c9d14803a891ccfb31290836d192e35da8a03`  
		Last Modified: Sat, 06 Mar 2021 07:43:54 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:6e6342ad7cb068b835b89ea9a534a5d031418836e09dd04907b1c7781a787eab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8156393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf578d18e16a587dec248f8f093062db4b9b12f90b41e50665d077be5c7dd21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 02:07:53 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 02:07:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 02:07:59 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 02:08:00 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 02:08:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 02:08:02 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae8cb9f7543f85a647367b6296075ccec7611078640e00e238b5958d456441d`  
		Last Modified: Sat, 06 Mar 2021 02:11:00 GMT  
		Size: 5.5 MB (5533933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac816b3b3b8d0302c63a3e657025bf4130e66f886d23b00eab085156e4ee50c0`  
		Last Modified: Sat, 06 Mar 2021 02:10:56 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:782e4290f2c50dd5e8a0714f8cfa35d8575577910ff3252c757d3a64e6bd4d47
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88cdb45d1d7d80ee678f8f1ca18f6c67822632552ea1ceb8a6a91ecc72503f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 00:59:37 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 00:59:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 00:59:43 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 00:59:43 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 00:59:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 00:59:44 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b550ac0781e9d06a2d5602aa128b8085d9808f31821df0db0fdb3378e4beb64`  
		Last Modified: Sat, 06 Mar 2021 01:00:55 GMT  
		Size: 5.5 MB (5527196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9fcc13222a0356f1399ed180350034d92d18fa5262cd34421cb52915ca14df`  
		Last Modified: Sat, 06 Mar 2021 01:00:53 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:1740e224df015e33133a9db91519ebc8601bf64861cde979a2ed6c556b649395
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8164487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205e781a3be342b949194bab8b6fde3763da1876fe7fac88af8efa1a07b3f204`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 01:46:28 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:46:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 01:46:33 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 01:46:34 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:46:35 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e334db32136252e9605e0a6ef0426e8c0c50e757bb238a24330339d3dedbe84`  
		Last Modified: Sat, 06 Mar 2021 01:51:34 GMT  
		Size: 5.5 MB (5452492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e903d8d08305b07378aef2e8c19af9f0d6b899ce053c33e5b6022c07b155e2`  
		Last Modified: Sat, 06 Mar 2021 01:51:32 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.1-alpine3.13`

```console
$ docker pull nats-streaming@sha256:d1bdcae6e682c875288aec0e01b192c753c516ddde6e8b5228583b2cde0671db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21.1-alpine3.13` - linux; amd64

```console
$ docker pull nats-streaming@sha256:701fa3e7165e338d3fb61b4f7068af826829b094fc089e1b7866466bc4cba85e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8774552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3593598c050f5241766331b8aed01f6c3f42b71938fc11f47bbfa18d74c829be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 07:43:18 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 07:43:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 07:43:22 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 07:43:22 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 07:43:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:43:23 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae3e2d2b3e48427fd1213fbc4722666443f13ca1a6709825a2afbbf6381367d`  
		Last Modified: Sat, 06 Mar 2021 07:43:55 GMT  
		Size: 6.0 MB (5962472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a250278b77e3fdc0d10076a12c9d14803a891ccfb31290836d192e35da8a03`  
		Last Modified: Sat, 06 Mar 2021 07:43:54 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-alpine3.13` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:6e6342ad7cb068b835b89ea9a534a5d031418836e09dd04907b1c7781a787eab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8156393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf578d18e16a587dec248f8f093062db4b9b12f90b41e50665d077be5c7dd21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 02:07:53 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 02:07:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 02:07:59 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 02:08:00 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 02:08:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 02:08:02 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae8cb9f7543f85a647367b6296075ccec7611078640e00e238b5958d456441d`  
		Last Modified: Sat, 06 Mar 2021 02:11:00 GMT  
		Size: 5.5 MB (5533933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac816b3b3b8d0302c63a3e657025bf4130e66f886d23b00eab085156e4ee50c0`  
		Last Modified: Sat, 06 Mar 2021 02:10:56 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-alpine3.13` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:782e4290f2c50dd5e8a0714f8cfa35d8575577910ff3252c757d3a64e6bd4d47
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88cdb45d1d7d80ee678f8f1ca18f6c67822632552ea1ceb8a6a91ecc72503f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 00:59:37 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 00:59:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 00:59:43 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 00:59:43 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 00:59:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 00:59:44 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b550ac0781e9d06a2d5602aa128b8085d9808f31821df0db0fdb3378e4beb64`  
		Last Modified: Sat, 06 Mar 2021 01:00:55 GMT  
		Size: 5.5 MB (5527196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9fcc13222a0356f1399ed180350034d92d18fa5262cd34421cb52915ca14df`  
		Last Modified: Sat, 06 Mar 2021 01:00:53 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:1740e224df015e33133a9db91519ebc8601bf64861cde979a2ed6c556b649395
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8164487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205e781a3be342b949194bab8b6fde3763da1876fe7fac88af8efa1a07b3f204`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 01:46:28 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:46:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 01:46:33 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 01:46:34 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:46:35 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e334db32136252e9605e0a6ef0426e8c0c50e757bb238a24330339d3dedbe84`  
		Last Modified: Sat, 06 Mar 2021 01:51:34 GMT  
		Size: 5.5 MB (5452492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e903d8d08305b07378aef2e8c19af9f0d6b899ce053c33e5b6022c07b155e2`  
		Last Modified: Sat, 06 Mar 2021 01:51:32 GMT  
		Size: 423.0 B  
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
$ docker pull nats-streaming@sha256:89598ecf5789a91a088f41d45b7065bb5168b2cd62655910ad4623d146612f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `nats-streaming:0.21.1-nanoserver` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats-streaming@sha256:761a9fae9a83a35868947aef2fef38e986bf238e5df545d02276993a3b1b3043
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107221484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31afc843a4cfc0bbe00476e4e93f5a7d4dd8e2fe55f5f1b84fe05c80f156ba48`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Feb 2021 13:06:30 GMT
RUN Apply image 1809-amd64
# Wed, 10 Feb 2021 16:02:26 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:17:29 GMT
RUN cmd /S /C #(nop) COPY file:189ca6af047e9f9cf54ab2176b48588e01c7497fe0b5b0d7b2614ebad66ed089 in C:\nats-streaming-server.exe 
# Sat, 06 Mar 2021 01:17:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:17:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:17:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ba17af31b9276ee11fdf859681b442db50979a39eff4cea2a559a5755cedbe01`  
		Size: 101.4 MB (101406193 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23b613036f8aee9066e712b3aa58f10f2fde093623511a5658867f53a6d01b18`  
		Last Modified: Wed, 10 Feb 2021 16:06:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83af691df7b0ece70ab41860e2add2cc454b31906aa7abb756bb166f50de6a93`  
		Last Modified: Sat, 06 Mar 2021 01:22:01 GMT  
		Size: 5.8 MB (5810692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ce94d4e2b26f5b27f5cd89d3b8172128fa8188838fa7c7103014b7afc5be8`  
		Last Modified: Sat, 06 Mar 2021 01:22:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcb8576081380a9b80744572a7960fcb1d30c0d85ea4bba32d1705b82658cd8`  
		Last Modified: Sat, 06 Mar 2021 01:22:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c3224120f5baf4ab134c2118bac99a39bc6e3f2dba314eb0053720c1d6c52f`  
		Last Modified: Sat, 06 Mar 2021 01:21:59 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.1-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:89598ecf5789a91a088f41d45b7065bb5168b2cd62655910ad4623d146612f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `nats-streaming:0.21.1-nanoserver-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats-streaming@sha256:761a9fae9a83a35868947aef2fef38e986bf238e5df545d02276993a3b1b3043
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107221484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31afc843a4cfc0bbe00476e4e93f5a7d4dd8e2fe55f5f1b84fe05c80f156ba48`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Feb 2021 13:06:30 GMT
RUN Apply image 1809-amd64
# Wed, 10 Feb 2021 16:02:26 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:17:29 GMT
RUN cmd /S /C #(nop) COPY file:189ca6af047e9f9cf54ab2176b48588e01c7497fe0b5b0d7b2614ebad66ed089 in C:\nats-streaming-server.exe 
# Sat, 06 Mar 2021 01:17:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:17:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:17:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ba17af31b9276ee11fdf859681b442db50979a39eff4cea2a559a5755cedbe01`  
		Size: 101.4 MB (101406193 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23b613036f8aee9066e712b3aa58f10f2fde093623511a5658867f53a6d01b18`  
		Last Modified: Wed, 10 Feb 2021 16:06:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83af691df7b0ece70ab41860e2add2cc454b31906aa7abb756bb166f50de6a93`  
		Last Modified: Sat, 06 Mar 2021 01:22:01 GMT  
		Size: 5.8 MB (5810692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ce94d4e2b26f5b27f5cd89d3b8172128fa8188838fa7c7103014b7afc5be8`  
		Last Modified: Sat, 06 Mar 2021 01:22:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcb8576081380a9b80744572a7960fcb1d30c0d85ea4bba32d1705b82658cd8`  
		Last Modified: Sat, 06 Mar 2021 01:22:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c3224120f5baf4ab134c2118bac99a39bc6e3f2dba314eb0053720c1d6c52f`  
		Last Modified: Sat, 06 Mar 2021 01:21:59 GMT  
		Size: 1.2 KB (1178 bytes)  
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
$ docker pull nats-streaming@sha256:39d3f82fefd5da629c1d283f14a6d1195d51e491dd3ba5f08b418db860e930ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64
	-	windows version 10.0.14393.4225; amd64

### `nats-streaming:0.21.1-windowsservercore` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats-streaming@sha256:933cd8e0c95d2b799cd2d7f79f6ca02ed810d003ad461d98d37c1fa7437b74ad
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2459529438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9439320b463e26060941107b4a470296967394ba75dd8f3a936bfc440f893`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 06 Feb 2021 05:03:14 GMT
RUN Install update 1809-amd64
# Tue, 09 Feb 2021 20:26:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Feb 2021 16:00:30 GMT
ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:15:16 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:15:17 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Sat, 06 Mar 2021 01:15:18 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Sat, 06 Mar 2021 01:15:49 GMT
RUN Set-PSDebug -Trace 2
# Sat, 06 Mar 2021 01:17:09 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 06 Mar 2021 01:17:10 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:17:11 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:17:13 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db4edcf0861ff3fdc41851a5a218965ecb2ab6cf4ec9448fb80cc4b6792fd46c`  
		Size: 720.9 MB (720933935 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:751b8860e89a7e6999d74a11dc393620b118057ad881cb87f1d6e3653cb2db43`  
		Last Modified: Tue, 09 Feb 2021 20:48:09 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f01e717591f83c73890556e7a4c77e53caed8daf6c9b0150f497e094a4a698`  
		Last Modified: Wed, 10 Feb 2021 16:06:05 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ffc35aa8c784e2ae1c53bdf12ef4dca08443101be895d09b0fe3dd743f3966`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf80997c587a8af113076c94add4be4d39d952431447634ba07a94332e575649`  
		Last Modified: Sat, 06 Mar 2021 01:21:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bf4e6129fe21a7ad575932f2a76dc0dc6d1beb2f353c58f75c65e41c74c35e`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9644b7f129edd50be8299c9021153e7a54036686fb5987014479a65d0896403f`  
		Last Modified: Sat, 06 Mar 2021 01:21:43 GMT  
		Size: 5.1 MB (5051560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044214cbb3458d290a88f677c47be5f08804c225dde815bcd4ed960101a1a53b`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 15.2 MB (15199849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0b5cd3070da7067e3c89e605aae52c1ebe57b69b6f0436f2efaa3e6d3b589b`  
		Last Modified: Sat, 06 Mar 2021 01:21:41 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69bb3643d207d59a56cdf191a574ea0db42fb3e12ee906a4b31d9512ac81bdc`  
		Last Modified: Sat, 06 Mar 2021 01:21:42 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3499ca15c55e19bd3b457821bc3d8ac8c541acc3699caa9fddc86fe46516f742`  
		Last Modified: Sat, 06 Mar 2021 01:21:41 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.1-windowsservercore` - windows version 10.0.14393.4225; amd64

```console
$ docker pull nats-streaming@sha256:df3b53a02cd66afc7979ad3d26ac54b201d61be525e20e45869b8895a82c1889
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816641605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd5b51dd87a43e29fc8026a6b905220ce0aea225b49d4fda2c9a45eb20af25a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Jan 2021 18:11:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 09 Feb 2021 20:28:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Feb 2021 16:02:35 GMT
ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:17:41 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:17:42 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Sat, 06 Mar 2021 01:17:43 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Sat, 06 Mar 2021 01:18:59 GMT
RUN Set-PSDebug -Trace 2
# Sat, 06 Mar 2021 01:21:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 06 Mar 2021 01:21:02 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:21:03 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:21:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:62c48323ed8ac695b8cbe0ecedcc28ba185a234673ad9241df2b151dd00f9181`  
		Size: 1.7 GB (1725027107 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ac4a230905430e1aea27172a9432f576cc4a530e72bea516a2b304d2b7e9c101`  
		Last Modified: Tue, 09 Feb 2021 20:49:11 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc28e30e89dab2d0b2b2f6c3114771d9d803d5942c730de78d2dd457ad4ac40`  
		Last Modified: Wed, 10 Feb 2021 16:06:59 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9447653d0a16850c994a7ca22cc403b4d9e07f83ba703a49c2a8f0035ea3b2`  
		Last Modified: Sat, 06 Mar 2021 01:22:18 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de230524e4b4a35a37dd08da7aa5b91b9b4c04b1edd4f27d8b7cf42db1f95a3`  
		Last Modified: Sat, 06 Mar 2021 01:22:17 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5017c7dcbaf6ec2a5864ea835e8994c6b91e6843ab1a569fce89bcb0279553`  
		Last Modified: Sat, 06 Mar 2021 01:22:17 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e17f4ee95d03eb4824f5b3b7eea5d5f65d599b8c1cbdd6e89cfe2c89b5a3beb`  
		Last Modified: Sat, 06 Mar 2021 01:22:21 GMT  
		Size: 5.7 MB (5656691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8a39b96e5982b6d4c90f60c9826018614c19d1cdf81d6d948ef114821c0f43`  
		Last Modified: Sat, 06 Mar 2021 01:22:18 GMT  
		Size: 16.0 MB (15960741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8454607fef0da445f612c2b2261e24ab07cd1bb138974086b792904f7f65d12`  
		Last Modified: Sat, 06 Mar 2021 01:22:14 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c9e3ca292261806cf558098b1da9f980736d49c58d10c24903eb58c91be842`  
		Last Modified: Sat, 06 Mar 2021 01:22:14 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d384fa928942fa296f88281379207d56f5744aa668e620fa13afc300b129fdb`  
		Last Modified: Sat, 06 Mar 2021 01:22:15 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.1-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:b12e8b3dfa1b9d88660effe50501fa509603693f4fa5655587cdc080e8cd35c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `nats-streaming:0.21.1-windowsservercore-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats-streaming@sha256:933cd8e0c95d2b799cd2d7f79f6ca02ed810d003ad461d98d37c1fa7437b74ad
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2459529438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9439320b463e26060941107b4a470296967394ba75dd8f3a936bfc440f893`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 06 Feb 2021 05:03:14 GMT
RUN Install update 1809-amd64
# Tue, 09 Feb 2021 20:26:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Feb 2021 16:00:30 GMT
ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:15:16 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:15:17 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Sat, 06 Mar 2021 01:15:18 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Sat, 06 Mar 2021 01:15:49 GMT
RUN Set-PSDebug -Trace 2
# Sat, 06 Mar 2021 01:17:09 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 06 Mar 2021 01:17:10 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:17:11 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:17:13 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db4edcf0861ff3fdc41851a5a218965ecb2ab6cf4ec9448fb80cc4b6792fd46c`  
		Size: 720.9 MB (720933935 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:751b8860e89a7e6999d74a11dc393620b118057ad881cb87f1d6e3653cb2db43`  
		Last Modified: Tue, 09 Feb 2021 20:48:09 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f01e717591f83c73890556e7a4c77e53caed8daf6c9b0150f497e094a4a698`  
		Last Modified: Wed, 10 Feb 2021 16:06:05 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ffc35aa8c784e2ae1c53bdf12ef4dca08443101be895d09b0fe3dd743f3966`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf80997c587a8af113076c94add4be4d39d952431447634ba07a94332e575649`  
		Last Modified: Sat, 06 Mar 2021 01:21:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bf4e6129fe21a7ad575932f2a76dc0dc6d1beb2f353c58f75c65e41c74c35e`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9644b7f129edd50be8299c9021153e7a54036686fb5987014479a65d0896403f`  
		Last Modified: Sat, 06 Mar 2021 01:21:43 GMT  
		Size: 5.1 MB (5051560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044214cbb3458d290a88f677c47be5f08804c225dde815bcd4ed960101a1a53b`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 15.2 MB (15199849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0b5cd3070da7067e3c89e605aae52c1ebe57b69b6f0436f2efaa3e6d3b589b`  
		Last Modified: Sat, 06 Mar 2021 01:21:41 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69bb3643d207d59a56cdf191a574ea0db42fb3e12ee906a4b31d9512ac81bdc`  
		Last Modified: Sat, 06 Mar 2021 01:21:42 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3499ca15c55e19bd3b457821bc3d8ac8c541acc3699caa9fddc86fe46516f742`  
		Last Modified: Sat, 06 Mar 2021 01:21:41 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.1-windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:4860f1d8c292e793d0d5b54f0b02ec493d2621f348f176e3a0129acf483a1696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4225; amd64

### `nats-streaming:0.21.1-windowsservercore-ltsc2016` - windows version 10.0.14393.4225; amd64

```console
$ docker pull nats-streaming@sha256:df3b53a02cd66afc7979ad3d26ac54b201d61be525e20e45869b8895a82c1889
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816641605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd5b51dd87a43e29fc8026a6b905220ce0aea225b49d4fda2c9a45eb20af25a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Jan 2021 18:11:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 09 Feb 2021 20:28:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Feb 2021 16:02:35 GMT
ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:17:41 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:17:42 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Sat, 06 Mar 2021 01:17:43 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Sat, 06 Mar 2021 01:18:59 GMT
RUN Set-PSDebug -Trace 2
# Sat, 06 Mar 2021 01:21:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 06 Mar 2021 01:21:02 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:21:03 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:21:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:62c48323ed8ac695b8cbe0ecedcc28ba185a234673ad9241df2b151dd00f9181`  
		Size: 1.7 GB (1725027107 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ac4a230905430e1aea27172a9432f576cc4a530e72bea516a2b304d2b7e9c101`  
		Last Modified: Tue, 09 Feb 2021 20:49:11 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc28e30e89dab2d0b2b2f6c3114771d9d803d5942c730de78d2dd457ad4ac40`  
		Last Modified: Wed, 10 Feb 2021 16:06:59 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9447653d0a16850c994a7ca22cc403b4d9e07f83ba703a49c2a8f0035ea3b2`  
		Last Modified: Sat, 06 Mar 2021 01:22:18 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de230524e4b4a35a37dd08da7aa5b91b9b4c04b1edd4f27d8b7cf42db1f95a3`  
		Last Modified: Sat, 06 Mar 2021 01:22:17 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5017c7dcbaf6ec2a5864ea835e8994c6b91e6843ab1a569fce89bcb0279553`  
		Last Modified: Sat, 06 Mar 2021 01:22:17 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e17f4ee95d03eb4824f5b3b7eea5d5f65d599b8c1cbdd6e89cfe2c89b5a3beb`  
		Last Modified: Sat, 06 Mar 2021 01:22:21 GMT  
		Size: 5.7 MB (5656691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8a39b96e5982b6d4c90f60c9826018614c19d1cdf81d6d948ef114821c0f43`  
		Last Modified: Sat, 06 Mar 2021 01:22:18 GMT  
		Size: 16.0 MB (15960741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8454607fef0da445f612c2b2261e24ab07cd1bb138974086b792904f7f65d12`  
		Last Modified: Sat, 06 Mar 2021 01:22:14 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c9e3ca292261806cf558098b1da9f980736d49c58d10c24903eb58c91be842`  
		Last Modified: Sat, 06 Mar 2021 01:22:14 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d384fa928942fa296f88281379207d56f5744aa668e620fa13afc300b129fdb`  
		Last Modified: Sat, 06 Mar 2021 01:22:15 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-alpine`

```console
$ docker pull nats-streaming@sha256:d1bdcae6e682c875288aec0e01b192c753c516ddde6e8b5228583b2cde0671db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:701fa3e7165e338d3fb61b4f7068af826829b094fc089e1b7866466bc4cba85e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8774552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3593598c050f5241766331b8aed01f6c3f42b71938fc11f47bbfa18d74c829be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 07:43:18 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 07:43:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 07:43:22 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 07:43:22 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 07:43:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:43:23 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae3e2d2b3e48427fd1213fbc4722666443f13ca1a6709825a2afbbf6381367d`  
		Last Modified: Sat, 06 Mar 2021 07:43:55 GMT  
		Size: 6.0 MB (5962472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a250278b77e3fdc0d10076a12c9d14803a891ccfb31290836d192e35da8a03`  
		Last Modified: Sat, 06 Mar 2021 07:43:54 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:6e6342ad7cb068b835b89ea9a534a5d031418836e09dd04907b1c7781a787eab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8156393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf578d18e16a587dec248f8f093062db4b9b12f90b41e50665d077be5c7dd21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 02:07:53 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 02:07:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 02:07:59 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 02:08:00 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 02:08:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 02:08:02 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae8cb9f7543f85a647367b6296075ccec7611078640e00e238b5958d456441d`  
		Last Modified: Sat, 06 Mar 2021 02:11:00 GMT  
		Size: 5.5 MB (5533933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac816b3b3b8d0302c63a3e657025bf4130e66f886d23b00eab085156e4ee50c0`  
		Last Modified: Sat, 06 Mar 2021 02:10:56 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:782e4290f2c50dd5e8a0714f8cfa35d8575577910ff3252c757d3a64e6bd4d47
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88cdb45d1d7d80ee678f8f1ca18f6c67822632552ea1ceb8a6a91ecc72503f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 00:59:37 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 00:59:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 00:59:43 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 00:59:43 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 00:59:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 00:59:44 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b550ac0781e9d06a2d5602aa128b8085d9808f31821df0db0fdb3378e4beb64`  
		Last Modified: Sat, 06 Mar 2021 01:00:55 GMT  
		Size: 5.5 MB (5527196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9fcc13222a0356f1399ed180350034d92d18fa5262cd34421cb52915ca14df`  
		Last Modified: Sat, 06 Mar 2021 01:00:53 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:1740e224df015e33133a9db91519ebc8601bf64861cde979a2ed6c556b649395
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8164487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205e781a3be342b949194bab8b6fde3763da1876fe7fac88af8efa1a07b3f204`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 01:46:28 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:46:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 01:46:33 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 01:46:34 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:46:35 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e334db32136252e9605e0a6ef0426e8c0c50e757bb238a24330339d3dedbe84`  
		Last Modified: Sat, 06 Mar 2021 01:51:34 GMT  
		Size: 5.5 MB (5452492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e903d8d08305b07378aef2e8c19af9f0d6b899ce053c33e5b6022c07b155e2`  
		Last Modified: Sat, 06 Mar 2021 01:51:32 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-alpine3.13`

```console
$ docker pull nats-streaming@sha256:d1bdcae6e682c875288aec0e01b192c753c516ddde6e8b5228583b2cde0671db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21-alpine3.13` - linux; amd64

```console
$ docker pull nats-streaming@sha256:701fa3e7165e338d3fb61b4f7068af826829b094fc089e1b7866466bc4cba85e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8774552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3593598c050f5241766331b8aed01f6c3f42b71938fc11f47bbfa18d74c829be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 07:43:18 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 07:43:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 07:43:22 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 07:43:22 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 07:43:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:43:23 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae3e2d2b3e48427fd1213fbc4722666443f13ca1a6709825a2afbbf6381367d`  
		Last Modified: Sat, 06 Mar 2021 07:43:55 GMT  
		Size: 6.0 MB (5962472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a250278b77e3fdc0d10076a12c9d14803a891ccfb31290836d192e35da8a03`  
		Last Modified: Sat, 06 Mar 2021 07:43:54 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-alpine3.13` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:6e6342ad7cb068b835b89ea9a534a5d031418836e09dd04907b1c7781a787eab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8156393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf578d18e16a587dec248f8f093062db4b9b12f90b41e50665d077be5c7dd21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 02:07:53 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 02:07:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 02:07:59 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 02:08:00 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 02:08:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 02:08:02 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae8cb9f7543f85a647367b6296075ccec7611078640e00e238b5958d456441d`  
		Last Modified: Sat, 06 Mar 2021 02:11:00 GMT  
		Size: 5.5 MB (5533933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac816b3b3b8d0302c63a3e657025bf4130e66f886d23b00eab085156e4ee50c0`  
		Last Modified: Sat, 06 Mar 2021 02:10:56 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-alpine3.13` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:782e4290f2c50dd5e8a0714f8cfa35d8575577910ff3252c757d3a64e6bd4d47
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88cdb45d1d7d80ee678f8f1ca18f6c67822632552ea1ceb8a6a91ecc72503f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 00:59:37 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 00:59:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 00:59:43 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 00:59:43 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 00:59:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 00:59:44 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b550ac0781e9d06a2d5602aa128b8085d9808f31821df0db0fdb3378e4beb64`  
		Last Modified: Sat, 06 Mar 2021 01:00:55 GMT  
		Size: 5.5 MB (5527196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9fcc13222a0356f1399ed180350034d92d18fa5262cd34421cb52915ca14df`  
		Last Modified: Sat, 06 Mar 2021 01:00:53 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:1740e224df015e33133a9db91519ebc8601bf64861cde979a2ed6c556b649395
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8164487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205e781a3be342b949194bab8b6fde3763da1876fe7fac88af8efa1a07b3f204`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 01:46:28 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:46:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 01:46:33 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 01:46:34 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:46:35 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e334db32136252e9605e0a6ef0426e8c0c50e757bb238a24330339d3dedbe84`  
		Last Modified: Sat, 06 Mar 2021 01:51:34 GMT  
		Size: 5.5 MB (5452492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e903d8d08305b07378aef2e8c19af9f0d6b899ce053c33e5b6022c07b155e2`  
		Last Modified: Sat, 06 Mar 2021 01:51:32 GMT  
		Size: 423.0 B  
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
$ docker pull nats-streaming@sha256:89598ecf5789a91a088f41d45b7065bb5168b2cd62655910ad4623d146612f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `nats-streaming:0.21-nanoserver` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats-streaming@sha256:761a9fae9a83a35868947aef2fef38e986bf238e5df545d02276993a3b1b3043
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107221484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31afc843a4cfc0bbe00476e4e93f5a7d4dd8e2fe55f5f1b84fe05c80f156ba48`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Feb 2021 13:06:30 GMT
RUN Apply image 1809-amd64
# Wed, 10 Feb 2021 16:02:26 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:17:29 GMT
RUN cmd /S /C #(nop) COPY file:189ca6af047e9f9cf54ab2176b48588e01c7497fe0b5b0d7b2614ebad66ed089 in C:\nats-streaming-server.exe 
# Sat, 06 Mar 2021 01:17:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:17:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:17:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ba17af31b9276ee11fdf859681b442db50979a39eff4cea2a559a5755cedbe01`  
		Size: 101.4 MB (101406193 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23b613036f8aee9066e712b3aa58f10f2fde093623511a5658867f53a6d01b18`  
		Last Modified: Wed, 10 Feb 2021 16:06:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83af691df7b0ece70ab41860e2add2cc454b31906aa7abb756bb166f50de6a93`  
		Last Modified: Sat, 06 Mar 2021 01:22:01 GMT  
		Size: 5.8 MB (5810692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ce94d4e2b26f5b27f5cd89d3b8172128fa8188838fa7c7103014b7afc5be8`  
		Last Modified: Sat, 06 Mar 2021 01:22:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcb8576081380a9b80744572a7960fcb1d30c0d85ea4bba32d1705b82658cd8`  
		Last Modified: Sat, 06 Mar 2021 01:22:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c3224120f5baf4ab134c2118bac99a39bc6e3f2dba314eb0053720c1d6c52f`  
		Last Modified: Sat, 06 Mar 2021 01:21:59 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:89598ecf5789a91a088f41d45b7065bb5168b2cd62655910ad4623d146612f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `nats-streaming:0.21-nanoserver-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats-streaming@sha256:761a9fae9a83a35868947aef2fef38e986bf238e5df545d02276993a3b1b3043
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107221484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31afc843a4cfc0bbe00476e4e93f5a7d4dd8e2fe55f5f1b84fe05c80f156ba48`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Feb 2021 13:06:30 GMT
RUN Apply image 1809-amd64
# Wed, 10 Feb 2021 16:02:26 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:17:29 GMT
RUN cmd /S /C #(nop) COPY file:189ca6af047e9f9cf54ab2176b48588e01c7497fe0b5b0d7b2614ebad66ed089 in C:\nats-streaming-server.exe 
# Sat, 06 Mar 2021 01:17:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:17:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:17:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ba17af31b9276ee11fdf859681b442db50979a39eff4cea2a559a5755cedbe01`  
		Size: 101.4 MB (101406193 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23b613036f8aee9066e712b3aa58f10f2fde093623511a5658867f53a6d01b18`  
		Last Modified: Wed, 10 Feb 2021 16:06:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83af691df7b0ece70ab41860e2add2cc454b31906aa7abb756bb166f50de6a93`  
		Last Modified: Sat, 06 Mar 2021 01:22:01 GMT  
		Size: 5.8 MB (5810692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ce94d4e2b26f5b27f5cd89d3b8172128fa8188838fa7c7103014b7afc5be8`  
		Last Modified: Sat, 06 Mar 2021 01:22:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcb8576081380a9b80744572a7960fcb1d30c0d85ea4bba32d1705b82658cd8`  
		Last Modified: Sat, 06 Mar 2021 01:22:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c3224120f5baf4ab134c2118bac99a39bc6e3f2dba314eb0053720c1d6c52f`  
		Last Modified: Sat, 06 Mar 2021 01:21:59 GMT  
		Size: 1.2 KB (1178 bytes)  
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
$ docker pull nats-streaming@sha256:39d3f82fefd5da629c1d283f14a6d1195d51e491dd3ba5f08b418db860e930ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64
	-	windows version 10.0.14393.4225; amd64

### `nats-streaming:0.21-windowsservercore` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats-streaming@sha256:933cd8e0c95d2b799cd2d7f79f6ca02ed810d003ad461d98d37c1fa7437b74ad
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2459529438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9439320b463e26060941107b4a470296967394ba75dd8f3a936bfc440f893`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 06 Feb 2021 05:03:14 GMT
RUN Install update 1809-amd64
# Tue, 09 Feb 2021 20:26:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Feb 2021 16:00:30 GMT
ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:15:16 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:15:17 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Sat, 06 Mar 2021 01:15:18 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Sat, 06 Mar 2021 01:15:49 GMT
RUN Set-PSDebug -Trace 2
# Sat, 06 Mar 2021 01:17:09 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 06 Mar 2021 01:17:10 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:17:11 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:17:13 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db4edcf0861ff3fdc41851a5a218965ecb2ab6cf4ec9448fb80cc4b6792fd46c`  
		Size: 720.9 MB (720933935 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:751b8860e89a7e6999d74a11dc393620b118057ad881cb87f1d6e3653cb2db43`  
		Last Modified: Tue, 09 Feb 2021 20:48:09 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f01e717591f83c73890556e7a4c77e53caed8daf6c9b0150f497e094a4a698`  
		Last Modified: Wed, 10 Feb 2021 16:06:05 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ffc35aa8c784e2ae1c53bdf12ef4dca08443101be895d09b0fe3dd743f3966`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf80997c587a8af113076c94add4be4d39d952431447634ba07a94332e575649`  
		Last Modified: Sat, 06 Mar 2021 01:21:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bf4e6129fe21a7ad575932f2a76dc0dc6d1beb2f353c58f75c65e41c74c35e`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9644b7f129edd50be8299c9021153e7a54036686fb5987014479a65d0896403f`  
		Last Modified: Sat, 06 Mar 2021 01:21:43 GMT  
		Size: 5.1 MB (5051560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044214cbb3458d290a88f677c47be5f08804c225dde815bcd4ed960101a1a53b`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 15.2 MB (15199849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0b5cd3070da7067e3c89e605aae52c1ebe57b69b6f0436f2efaa3e6d3b589b`  
		Last Modified: Sat, 06 Mar 2021 01:21:41 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69bb3643d207d59a56cdf191a574ea0db42fb3e12ee906a4b31d9512ac81bdc`  
		Last Modified: Sat, 06 Mar 2021 01:21:42 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3499ca15c55e19bd3b457821bc3d8ac8c541acc3699caa9fddc86fe46516f742`  
		Last Modified: Sat, 06 Mar 2021 01:21:41 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-windowsservercore` - windows version 10.0.14393.4225; amd64

```console
$ docker pull nats-streaming@sha256:df3b53a02cd66afc7979ad3d26ac54b201d61be525e20e45869b8895a82c1889
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816641605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd5b51dd87a43e29fc8026a6b905220ce0aea225b49d4fda2c9a45eb20af25a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Jan 2021 18:11:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 09 Feb 2021 20:28:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Feb 2021 16:02:35 GMT
ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:17:41 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:17:42 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Sat, 06 Mar 2021 01:17:43 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Sat, 06 Mar 2021 01:18:59 GMT
RUN Set-PSDebug -Trace 2
# Sat, 06 Mar 2021 01:21:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 06 Mar 2021 01:21:02 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:21:03 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:21:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:62c48323ed8ac695b8cbe0ecedcc28ba185a234673ad9241df2b151dd00f9181`  
		Size: 1.7 GB (1725027107 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ac4a230905430e1aea27172a9432f576cc4a530e72bea516a2b304d2b7e9c101`  
		Last Modified: Tue, 09 Feb 2021 20:49:11 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc28e30e89dab2d0b2b2f6c3114771d9d803d5942c730de78d2dd457ad4ac40`  
		Last Modified: Wed, 10 Feb 2021 16:06:59 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9447653d0a16850c994a7ca22cc403b4d9e07f83ba703a49c2a8f0035ea3b2`  
		Last Modified: Sat, 06 Mar 2021 01:22:18 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de230524e4b4a35a37dd08da7aa5b91b9b4c04b1edd4f27d8b7cf42db1f95a3`  
		Last Modified: Sat, 06 Mar 2021 01:22:17 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5017c7dcbaf6ec2a5864ea835e8994c6b91e6843ab1a569fce89bcb0279553`  
		Last Modified: Sat, 06 Mar 2021 01:22:17 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e17f4ee95d03eb4824f5b3b7eea5d5f65d599b8c1cbdd6e89cfe2c89b5a3beb`  
		Last Modified: Sat, 06 Mar 2021 01:22:21 GMT  
		Size: 5.7 MB (5656691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8a39b96e5982b6d4c90f60c9826018614c19d1cdf81d6d948ef114821c0f43`  
		Last Modified: Sat, 06 Mar 2021 01:22:18 GMT  
		Size: 16.0 MB (15960741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8454607fef0da445f612c2b2261e24ab07cd1bb138974086b792904f7f65d12`  
		Last Modified: Sat, 06 Mar 2021 01:22:14 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c9e3ca292261806cf558098b1da9f980736d49c58d10c24903eb58c91be842`  
		Last Modified: Sat, 06 Mar 2021 01:22:14 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d384fa928942fa296f88281379207d56f5744aa668e620fa13afc300b129fdb`  
		Last Modified: Sat, 06 Mar 2021 01:22:15 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:b12e8b3dfa1b9d88660effe50501fa509603693f4fa5655587cdc080e8cd35c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `nats-streaming:0.21-windowsservercore-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats-streaming@sha256:933cd8e0c95d2b799cd2d7f79f6ca02ed810d003ad461d98d37c1fa7437b74ad
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2459529438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9439320b463e26060941107b4a470296967394ba75dd8f3a936bfc440f893`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 06 Feb 2021 05:03:14 GMT
RUN Install update 1809-amd64
# Tue, 09 Feb 2021 20:26:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Feb 2021 16:00:30 GMT
ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:15:16 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:15:17 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Sat, 06 Mar 2021 01:15:18 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Sat, 06 Mar 2021 01:15:49 GMT
RUN Set-PSDebug -Trace 2
# Sat, 06 Mar 2021 01:17:09 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 06 Mar 2021 01:17:10 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:17:11 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:17:13 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db4edcf0861ff3fdc41851a5a218965ecb2ab6cf4ec9448fb80cc4b6792fd46c`  
		Size: 720.9 MB (720933935 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:751b8860e89a7e6999d74a11dc393620b118057ad881cb87f1d6e3653cb2db43`  
		Last Modified: Tue, 09 Feb 2021 20:48:09 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f01e717591f83c73890556e7a4c77e53caed8daf6c9b0150f497e094a4a698`  
		Last Modified: Wed, 10 Feb 2021 16:06:05 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ffc35aa8c784e2ae1c53bdf12ef4dca08443101be895d09b0fe3dd743f3966`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf80997c587a8af113076c94add4be4d39d952431447634ba07a94332e575649`  
		Last Modified: Sat, 06 Mar 2021 01:21:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bf4e6129fe21a7ad575932f2a76dc0dc6d1beb2f353c58f75c65e41c74c35e`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9644b7f129edd50be8299c9021153e7a54036686fb5987014479a65d0896403f`  
		Last Modified: Sat, 06 Mar 2021 01:21:43 GMT  
		Size: 5.1 MB (5051560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044214cbb3458d290a88f677c47be5f08804c225dde815bcd4ed960101a1a53b`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 15.2 MB (15199849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0b5cd3070da7067e3c89e605aae52c1ebe57b69b6f0436f2efaa3e6d3b589b`  
		Last Modified: Sat, 06 Mar 2021 01:21:41 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69bb3643d207d59a56cdf191a574ea0db42fb3e12ee906a4b31d9512ac81bdc`  
		Last Modified: Sat, 06 Mar 2021 01:21:42 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3499ca15c55e19bd3b457821bc3d8ac8c541acc3699caa9fddc86fe46516f742`  
		Last Modified: Sat, 06 Mar 2021 01:21:41 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:4860f1d8c292e793d0d5b54f0b02ec493d2621f348f176e3a0129acf483a1696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4225; amd64

### `nats-streaming:0.21-windowsservercore-ltsc2016` - windows version 10.0.14393.4225; amd64

```console
$ docker pull nats-streaming@sha256:df3b53a02cd66afc7979ad3d26ac54b201d61be525e20e45869b8895a82c1889
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816641605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd5b51dd87a43e29fc8026a6b905220ce0aea225b49d4fda2c9a45eb20af25a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Jan 2021 18:11:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 09 Feb 2021 20:28:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Feb 2021 16:02:35 GMT
ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:17:41 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:17:42 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Sat, 06 Mar 2021 01:17:43 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Sat, 06 Mar 2021 01:18:59 GMT
RUN Set-PSDebug -Trace 2
# Sat, 06 Mar 2021 01:21:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 06 Mar 2021 01:21:02 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:21:03 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:21:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:62c48323ed8ac695b8cbe0ecedcc28ba185a234673ad9241df2b151dd00f9181`  
		Size: 1.7 GB (1725027107 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ac4a230905430e1aea27172a9432f576cc4a530e72bea516a2b304d2b7e9c101`  
		Last Modified: Tue, 09 Feb 2021 20:49:11 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc28e30e89dab2d0b2b2f6c3114771d9d803d5942c730de78d2dd457ad4ac40`  
		Last Modified: Wed, 10 Feb 2021 16:06:59 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9447653d0a16850c994a7ca22cc403b4d9e07f83ba703a49c2a8f0035ea3b2`  
		Last Modified: Sat, 06 Mar 2021 01:22:18 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de230524e4b4a35a37dd08da7aa5b91b9b4c04b1edd4f27d8b7cf42db1f95a3`  
		Last Modified: Sat, 06 Mar 2021 01:22:17 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5017c7dcbaf6ec2a5864ea835e8994c6b91e6843ab1a569fce89bcb0279553`  
		Last Modified: Sat, 06 Mar 2021 01:22:17 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e17f4ee95d03eb4824f5b3b7eea5d5f65d599b8c1cbdd6e89cfe2c89b5a3beb`  
		Last Modified: Sat, 06 Mar 2021 01:22:21 GMT  
		Size: 5.7 MB (5656691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8a39b96e5982b6d4c90f60c9826018614c19d1cdf81d6d948ef114821c0f43`  
		Last Modified: Sat, 06 Mar 2021 01:22:18 GMT  
		Size: 16.0 MB (15960741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8454607fef0da445f612c2b2261e24ab07cd1bb138974086b792904f7f65d12`  
		Last Modified: Sat, 06 Mar 2021 01:22:14 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c9e3ca292261806cf558098b1da9f980736d49c58d10c24903eb58c91be842`  
		Last Modified: Sat, 06 Mar 2021 01:22:14 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d384fa928942fa296f88281379207d56f5744aa668e620fa13afc300b129fdb`  
		Last Modified: Sat, 06 Mar 2021 01:22:15 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:d1bdcae6e682c875288aec0e01b192c753c516ddde6e8b5228583b2cde0671db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:701fa3e7165e338d3fb61b4f7068af826829b094fc089e1b7866466bc4cba85e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8774552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3593598c050f5241766331b8aed01f6c3f42b71938fc11f47bbfa18d74c829be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 07:43:18 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 07:43:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 07:43:22 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 07:43:22 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 07:43:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:43:23 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae3e2d2b3e48427fd1213fbc4722666443f13ca1a6709825a2afbbf6381367d`  
		Last Modified: Sat, 06 Mar 2021 07:43:55 GMT  
		Size: 6.0 MB (5962472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a250278b77e3fdc0d10076a12c9d14803a891ccfb31290836d192e35da8a03`  
		Last Modified: Sat, 06 Mar 2021 07:43:54 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:6e6342ad7cb068b835b89ea9a534a5d031418836e09dd04907b1c7781a787eab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8156393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf578d18e16a587dec248f8f093062db4b9b12f90b41e50665d077be5c7dd21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 02:07:53 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 02:07:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 02:07:59 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 02:08:00 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 02:08:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 02:08:02 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae8cb9f7543f85a647367b6296075ccec7611078640e00e238b5958d456441d`  
		Last Modified: Sat, 06 Mar 2021 02:11:00 GMT  
		Size: 5.5 MB (5533933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac816b3b3b8d0302c63a3e657025bf4130e66f886d23b00eab085156e4ee50c0`  
		Last Modified: Sat, 06 Mar 2021 02:10:56 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:782e4290f2c50dd5e8a0714f8cfa35d8575577910ff3252c757d3a64e6bd4d47
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88cdb45d1d7d80ee678f8f1ca18f6c67822632552ea1ceb8a6a91ecc72503f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 00:59:37 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 00:59:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 00:59:43 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 00:59:43 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 00:59:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 00:59:44 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b550ac0781e9d06a2d5602aa128b8085d9808f31821df0db0fdb3378e4beb64`  
		Last Modified: Sat, 06 Mar 2021 01:00:55 GMT  
		Size: 5.5 MB (5527196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9fcc13222a0356f1399ed180350034d92d18fa5262cd34421cb52915ca14df`  
		Last Modified: Sat, 06 Mar 2021 01:00:53 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:1740e224df015e33133a9db91519ebc8601bf64861cde979a2ed6c556b649395
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8164487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205e781a3be342b949194bab8b6fde3763da1876fe7fac88af8efa1a07b3f204`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 01:46:28 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:46:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 01:46:33 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 01:46:34 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:46:35 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e334db32136252e9605e0a6ef0426e8c0c50e757bb238a24330339d3dedbe84`  
		Last Modified: Sat, 06 Mar 2021 01:51:34 GMT  
		Size: 5.5 MB (5452492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e903d8d08305b07378aef2e8c19af9f0d6b899ce053c33e5b6022c07b155e2`  
		Last Modified: Sat, 06 Mar 2021 01:51:32 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.13`

```console
$ docker pull nats-streaming@sha256:d1bdcae6e682c875288aec0e01b192c753c516ddde6e8b5228583b2cde0671db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.13` - linux; amd64

```console
$ docker pull nats-streaming@sha256:701fa3e7165e338d3fb61b4f7068af826829b094fc089e1b7866466bc4cba85e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8774552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3593598c050f5241766331b8aed01f6c3f42b71938fc11f47bbfa18d74c829be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 07:43:18 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 07:43:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 07:43:22 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 07:43:22 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 07:43:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:43:23 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae3e2d2b3e48427fd1213fbc4722666443f13ca1a6709825a2afbbf6381367d`  
		Last Modified: Sat, 06 Mar 2021 07:43:55 GMT  
		Size: 6.0 MB (5962472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a250278b77e3fdc0d10076a12c9d14803a891ccfb31290836d192e35da8a03`  
		Last Modified: Sat, 06 Mar 2021 07:43:54 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.13` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:6e6342ad7cb068b835b89ea9a534a5d031418836e09dd04907b1c7781a787eab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8156393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf578d18e16a587dec248f8f093062db4b9b12f90b41e50665d077be5c7dd21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 02:07:53 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 02:07:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 02:07:59 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 02:08:00 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 02:08:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 02:08:02 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae8cb9f7543f85a647367b6296075ccec7611078640e00e238b5958d456441d`  
		Last Modified: Sat, 06 Mar 2021 02:11:00 GMT  
		Size: 5.5 MB (5533933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac816b3b3b8d0302c63a3e657025bf4130e66f886d23b00eab085156e4ee50c0`  
		Last Modified: Sat, 06 Mar 2021 02:10:56 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.13` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:782e4290f2c50dd5e8a0714f8cfa35d8575577910ff3252c757d3a64e6bd4d47
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88cdb45d1d7d80ee678f8f1ca18f6c67822632552ea1ceb8a6a91ecc72503f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 00:59:37 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 00:59:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 00:59:43 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 00:59:43 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 00:59:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 00:59:44 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b550ac0781e9d06a2d5602aa128b8085d9808f31821df0db0fdb3378e4beb64`  
		Last Modified: Sat, 06 Mar 2021 01:00:55 GMT  
		Size: 5.5 MB (5527196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9fcc13222a0356f1399ed180350034d92d18fa5262cd34421cb52915ca14df`  
		Last Modified: Sat, 06 Mar 2021 01:00:53 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:1740e224df015e33133a9db91519ebc8601bf64861cde979a2ed6c556b649395
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8164487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205e781a3be342b949194bab8b6fde3763da1876fe7fac88af8efa1a07b3f204`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 01:46:28 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:46:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='06d591a61084aab1046e818486c2ee7c3936214c92dc257084693d6ffe06342b' ;; 		armhf) natsArch='arm6'; sha256='085375782abe1bacbd6fc609ce6a6721f029cba312733479204c89bf92f1e188' ;; 		armv7) natsArch='arm7'; sha256='947d91512b47ba98198bef7f799670c40cf6949f2ba2e98b5c133e6166e9b97c' ;; 		x86_64) natsArch='amd64'; sha256='85fd7fd3c7b71cbc9043900f9110b028f1fdc042c6500eed065e6e2c3331f62e' ;; 		x86) natsArch='386'; sha256='475b0f015726af99c9ea779c8bbbeaa729ef90f43dd2715273fea81fb90ea63a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 06 Mar 2021 01:46:33 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 06 Mar 2021 01:46:34 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:46:35 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e334db32136252e9605e0a6ef0426e8c0c50e757bb238a24330339d3dedbe84`  
		Last Modified: Sat, 06 Mar 2021 01:51:34 GMT  
		Size: 5.5 MB (5452492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e903d8d08305b07378aef2e8c19af9f0d6b899ce053c33e5b6022c07b155e2`  
		Last Modified: Sat, 06 Mar 2021 01:51:32 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:e20f1649bb8b602a05fba0747e306280e129553c66c4de0194e1b04211323f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1757; amd64

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

### `nats-streaming:latest` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats-streaming@sha256:761a9fae9a83a35868947aef2fef38e986bf238e5df545d02276993a3b1b3043
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107221484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31afc843a4cfc0bbe00476e4e93f5a7d4dd8e2fe55f5f1b84fe05c80f156ba48`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Feb 2021 13:06:30 GMT
RUN Apply image 1809-amd64
# Wed, 10 Feb 2021 16:02:26 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:17:29 GMT
RUN cmd /S /C #(nop) COPY file:189ca6af047e9f9cf54ab2176b48588e01c7497fe0b5b0d7b2614ebad66ed089 in C:\nats-streaming-server.exe 
# Sat, 06 Mar 2021 01:17:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:17:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:17:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ba17af31b9276ee11fdf859681b442db50979a39eff4cea2a559a5755cedbe01`  
		Size: 101.4 MB (101406193 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23b613036f8aee9066e712b3aa58f10f2fde093623511a5658867f53a6d01b18`  
		Last Modified: Wed, 10 Feb 2021 16:06:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83af691df7b0ece70ab41860e2add2cc454b31906aa7abb756bb166f50de6a93`  
		Last Modified: Sat, 06 Mar 2021 01:22:01 GMT  
		Size: 5.8 MB (5810692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ce94d4e2b26f5b27f5cd89d3b8172128fa8188838fa7c7103014b7afc5be8`  
		Last Modified: Sat, 06 Mar 2021 01:22:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcb8576081380a9b80744572a7960fcb1d30c0d85ea4bba32d1705b82658cd8`  
		Last Modified: Sat, 06 Mar 2021 01:22:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c3224120f5baf4ab134c2118bac99a39bc6e3f2dba314eb0053720c1d6c52f`  
		Last Modified: Sat, 06 Mar 2021 01:21:59 GMT  
		Size: 1.2 KB (1178 bytes)  
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
$ docker pull nats-streaming@sha256:89598ecf5789a91a088f41d45b7065bb5168b2cd62655910ad4623d146612f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats-streaming@sha256:761a9fae9a83a35868947aef2fef38e986bf238e5df545d02276993a3b1b3043
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107221484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31afc843a4cfc0bbe00476e4e93f5a7d4dd8e2fe55f5f1b84fe05c80f156ba48`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Feb 2021 13:06:30 GMT
RUN Apply image 1809-amd64
# Wed, 10 Feb 2021 16:02:26 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:17:29 GMT
RUN cmd /S /C #(nop) COPY file:189ca6af047e9f9cf54ab2176b48588e01c7497fe0b5b0d7b2614ebad66ed089 in C:\nats-streaming-server.exe 
# Sat, 06 Mar 2021 01:17:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:17:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:17:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ba17af31b9276ee11fdf859681b442db50979a39eff4cea2a559a5755cedbe01`  
		Size: 101.4 MB (101406193 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23b613036f8aee9066e712b3aa58f10f2fde093623511a5658867f53a6d01b18`  
		Last Modified: Wed, 10 Feb 2021 16:06:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83af691df7b0ece70ab41860e2add2cc454b31906aa7abb756bb166f50de6a93`  
		Last Modified: Sat, 06 Mar 2021 01:22:01 GMT  
		Size: 5.8 MB (5810692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ce94d4e2b26f5b27f5cd89d3b8172128fa8188838fa7c7103014b7afc5be8`  
		Last Modified: Sat, 06 Mar 2021 01:22:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcb8576081380a9b80744572a7960fcb1d30c0d85ea4bba32d1705b82658cd8`  
		Last Modified: Sat, 06 Mar 2021 01:22:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c3224120f5baf4ab134c2118bac99a39bc6e3f2dba314eb0053720c1d6c52f`  
		Last Modified: Sat, 06 Mar 2021 01:21:59 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:89598ecf5789a91a088f41d45b7065bb5168b2cd62655910ad4623d146612f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats-streaming@sha256:761a9fae9a83a35868947aef2fef38e986bf238e5df545d02276993a3b1b3043
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107221484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31afc843a4cfc0bbe00476e4e93f5a7d4dd8e2fe55f5f1b84fe05c80f156ba48`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Feb 2021 13:06:30 GMT
RUN Apply image 1809-amd64
# Wed, 10 Feb 2021 16:02:26 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:17:29 GMT
RUN cmd /S /C #(nop) COPY file:189ca6af047e9f9cf54ab2176b48588e01c7497fe0b5b0d7b2614ebad66ed089 in C:\nats-streaming-server.exe 
# Sat, 06 Mar 2021 01:17:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:17:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:17:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ba17af31b9276ee11fdf859681b442db50979a39eff4cea2a559a5755cedbe01`  
		Size: 101.4 MB (101406193 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23b613036f8aee9066e712b3aa58f10f2fde093623511a5658867f53a6d01b18`  
		Last Modified: Wed, 10 Feb 2021 16:06:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83af691df7b0ece70ab41860e2add2cc454b31906aa7abb756bb166f50de6a93`  
		Last Modified: Sat, 06 Mar 2021 01:22:01 GMT  
		Size: 5.8 MB (5810692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ce94d4e2b26f5b27f5cd89d3b8172128fa8188838fa7c7103014b7afc5be8`  
		Last Modified: Sat, 06 Mar 2021 01:22:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcb8576081380a9b80744572a7960fcb1d30c0d85ea4bba32d1705b82658cd8`  
		Last Modified: Sat, 06 Mar 2021 01:22:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c3224120f5baf4ab134c2118bac99a39bc6e3f2dba314eb0053720c1d6c52f`  
		Last Modified: Sat, 06 Mar 2021 01:21:59 GMT  
		Size: 1.2 KB (1178 bytes)  
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
$ docker pull nats-streaming@sha256:39d3f82fefd5da629c1d283f14a6d1195d51e491dd3ba5f08b418db860e930ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64
	-	windows version 10.0.14393.4225; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats-streaming@sha256:933cd8e0c95d2b799cd2d7f79f6ca02ed810d003ad461d98d37c1fa7437b74ad
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2459529438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9439320b463e26060941107b4a470296967394ba75dd8f3a936bfc440f893`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 06 Feb 2021 05:03:14 GMT
RUN Install update 1809-amd64
# Tue, 09 Feb 2021 20:26:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Feb 2021 16:00:30 GMT
ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:15:16 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:15:17 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Sat, 06 Mar 2021 01:15:18 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Sat, 06 Mar 2021 01:15:49 GMT
RUN Set-PSDebug -Trace 2
# Sat, 06 Mar 2021 01:17:09 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 06 Mar 2021 01:17:10 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:17:11 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:17:13 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db4edcf0861ff3fdc41851a5a218965ecb2ab6cf4ec9448fb80cc4b6792fd46c`  
		Size: 720.9 MB (720933935 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:751b8860e89a7e6999d74a11dc393620b118057ad881cb87f1d6e3653cb2db43`  
		Last Modified: Tue, 09 Feb 2021 20:48:09 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f01e717591f83c73890556e7a4c77e53caed8daf6c9b0150f497e094a4a698`  
		Last Modified: Wed, 10 Feb 2021 16:06:05 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ffc35aa8c784e2ae1c53bdf12ef4dca08443101be895d09b0fe3dd743f3966`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf80997c587a8af113076c94add4be4d39d952431447634ba07a94332e575649`  
		Last Modified: Sat, 06 Mar 2021 01:21:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bf4e6129fe21a7ad575932f2a76dc0dc6d1beb2f353c58f75c65e41c74c35e`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9644b7f129edd50be8299c9021153e7a54036686fb5987014479a65d0896403f`  
		Last Modified: Sat, 06 Mar 2021 01:21:43 GMT  
		Size: 5.1 MB (5051560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044214cbb3458d290a88f677c47be5f08804c225dde815bcd4ed960101a1a53b`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 15.2 MB (15199849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0b5cd3070da7067e3c89e605aae52c1ebe57b69b6f0436f2efaa3e6d3b589b`  
		Last Modified: Sat, 06 Mar 2021 01:21:41 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69bb3643d207d59a56cdf191a574ea0db42fb3e12ee906a4b31d9512ac81bdc`  
		Last Modified: Sat, 06 Mar 2021 01:21:42 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3499ca15c55e19bd3b457821bc3d8ac8c541acc3699caa9fddc86fe46516f742`  
		Last Modified: Sat, 06 Mar 2021 01:21:41 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:windowsservercore` - windows version 10.0.14393.4225; amd64

```console
$ docker pull nats-streaming@sha256:df3b53a02cd66afc7979ad3d26ac54b201d61be525e20e45869b8895a82c1889
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816641605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd5b51dd87a43e29fc8026a6b905220ce0aea225b49d4fda2c9a45eb20af25a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Jan 2021 18:11:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 09 Feb 2021 20:28:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Feb 2021 16:02:35 GMT
ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:17:41 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:17:42 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Sat, 06 Mar 2021 01:17:43 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Sat, 06 Mar 2021 01:18:59 GMT
RUN Set-PSDebug -Trace 2
# Sat, 06 Mar 2021 01:21:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 06 Mar 2021 01:21:02 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:21:03 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:21:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:62c48323ed8ac695b8cbe0ecedcc28ba185a234673ad9241df2b151dd00f9181`  
		Size: 1.7 GB (1725027107 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ac4a230905430e1aea27172a9432f576cc4a530e72bea516a2b304d2b7e9c101`  
		Last Modified: Tue, 09 Feb 2021 20:49:11 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc28e30e89dab2d0b2b2f6c3114771d9d803d5942c730de78d2dd457ad4ac40`  
		Last Modified: Wed, 10 Feb 2021 16:06:59 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9447653d0a16850c994a7ca22cc403b4d9e07f83ba703a49c2a8f0035ea3b2`  
		Last Modified: Sat, 06 Mar 2021 01:22:18 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de230524e4b4a35a37dd08da7aa5b91b9b4c04b1edd4f27d8b7cf42db1f95a3`  
		Last Modified: Sat, 06 Mar 2021 01:22:17 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5017c7dcbaf6ec2a5864ea835e8994c6b91e6843ab1a569fce89bcb0279553`  
		Last Modified: Sat, 06 Mar 2021 01:22:17 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e17f4ee95d03eb4824f5b3b7eea5d5f65d599b8c1cbdd6e89cfe2c89b5a3beb`  
		Last Modified: Sat, 06 Mar 2021 01:22:21 GMT  
		Size: 5.7 MB (5656691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8a39b96e5982b6d4c90f60c9826018614c19d1cdf81d6d948ef114821c0f43`  
		Last Modified: Sat, 06 Mar 2021 01:22:18 GMT  
		Size: 16.0 MB (15960741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8454607fef0da445f612c2b2261e24ab07cd1bb138974086b792904f7f65d12`  
		Last Modified: Sat, 06 Mar 2021 01:22:14 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c9e3ca292261806cf558098b1da9f980736d49c58d10c24903eb58c91be842`  
		Last Modified: Sat, 06 Mar 2021 01:22:14 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d384fa928942fa296f88281379207d56f5744aa668e620fa13afc300b129fdb`  
		Last Modified: Sat, 06 Mar 2021 01:22:15 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:b12e8b3dfa1b9d88660effe50501fa509603693f4fa5655587cdc080e8cd35c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats-streaming@sha256:933cd8e0c95d2b799cd2d7f79f6ca02ed810d003ad461d98d37c1fa7437b74ad
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2459529438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9439320b463e26060941107b4a470296967394ba75dd8f3a936bfc440f893`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 06 Feb 2021 05:03:14 GMT
RUN Install update 1809-amd64
# Tue, 09 Feb 2021 20:26:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Feb 2021 16:00:30 GMT
ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:15:16 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:15:17 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Sat, 06 Mar 2021 01:15:18 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Sat, 06 Mar 2021 01:15:49 GMT
RUN Set-PSDebug -Trace 2
# Sat, 06 Mar 2021 01:17:09 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 06 Mar 2021 01:17:10 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:17:11 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:17:13 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db4edcf0861ff3fdc41851a5a218965ecb2ab6cf4ec9448fb80cc4b6792fd46c`  
		Size: 720.9 MB (720933935 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:751b8860e89a7e6999d74a11dc393620b118057ad881cb87f1d6e3653cb2db43`  
		Last Modified: Tue, 09 Feb 2021 20:48:09 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f01e717591f83c73890556e7a4c77e53caed8daf6c9b0150f497e094a4a698`  
		Last Modified: Wed, 10 Feb 2021 16:06:05 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ffc35aa8c784e2ae1c53bdf12ef4dca08443101be895d09b0fe3dd743f3966`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf80997c587a8af113076c94add4be4d39d952431447634ba07a94332e575649`  
		Last Modified: Sat, 06 Mar 2021 01:21:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bf4e6129fe21a7ad575932f2a76dc0dc6d1beb2f353c58f75c65e41c74c35e`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9644b7f129edd50be8299c9021153e7a54036686fb5987014479a65d0896403f`  
		Last Modified: Sat, 06 Mar 2021 01:21:43 GMT  
		Size: 5.1 MB (5051560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044214cbb3458d290a88f677c47be5f08804c225dde815bcd4ed960101a1a53b`  
		Last Modified: Sat, 06 Mar 2021 01:21:45 GMT  
		Size: 15.2 MB (15199849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0b5cd3070da7067e3c89e605aae52c1ebe57b69b6f0436f2efaa3e6d3b589b`  
		Last Modified: Sat, 06 Mar 2021 01:21:41 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69bb3643d207d59a56cdf191a574ea0db42fb3e12ee906a4b31d9512ac81bdc`  
		Last Modified: Sat, 06 Mar 2021 01:21:42 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3499ca15c55e19bd3b457821bc3d8ac8c541acc3699caa9fddc86fe46516f742`  
		Last Modified: Sat, 06 Mar 2021 01:21:41 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:4860f1d8c292e793d0d5b54f0b02ec493d2621f348f176e3a0129acf483a1696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4225; amd64

### `nats-streaming:windowsservercore-ltsc2016` - windows version 10.0.14393.4225; amd64

```console
$ docker pull nats-streaming@sha256:df3b53a02cd66afc7979ad3d26ac54b201d61be525e20e45869b8895a82c1889
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816641605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd5b51dd87a43e29fc8026a6b905220ce0aea225b49d4fda2c9a45eb20af25a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Jan 2021 18:11:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 09 Feb 2021 20:28:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Feb 2021 16:02:35 GMT
ENV NATS_DOCKERIZED=1
# Sat, 06 Mar 2021 01:17:41 GMT
ENV NATS_STREAMING_SERVER=0.21.1
# Sat, 06 Mar 2021 01:17:42 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.1/nats-streaming-server-v0.21.1-windows-amd64.zip
# Sat, 06 Mar 2021 01:17:43 GMT
ENV GIT_DOWNLOAD_SHA256=798ec9b686a8dcb4de93074f416eab067a0896b52ccfc05b65a5e21d55e634e5
# Sat, 06 Mar 2021 01:18:59 GMT
RUN Set-PSDebug -Trace 2
# Sat, 06 Mar 2021 01:21:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 06 Mar 2021 01:21:02 GMT
EXPOSE 4222 8222
# Sat, 06 Mar 2021 01:21:03 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 06 Mar 2021 01:21:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:62c48323ed8ac695b8cbe0ecedcc28ba185a234673ad9241df2b151dd00f9181`  
		Size: 1.7 GB (1725027107 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ac4a230905430e1aea27172a9432f576cc4a530e72bea516a2b304d2b7e9c101`  
		Last Modified: Tue, 09 Feb 2021 20:49:11 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc28e30e89dab2d0b2b2f6c3114771d9d803d5942c730de78d2dd457ad4ac40`  
		Last Modified: Wed, 10 Feb 2021 16:06:59 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9447653d0a16850c994a7ca22cc403b4d9e07f83ba703a49c2a8f0035ea3b2`  
		Last Modified: Sat, 06 Mar 2021 01:22:18 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de230524e4b4a35a37dd08da7aa5b91b9b4c04b1edd4f27d8b7cf42db1f95a3`  
		Last Modified: Sat, 06 Mar 2021 01:22:17 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5017c7dcbaf6ec2a5864ea835e8994c6b91e6843ab1a569fce89bcb0279553`  
		Last Modified: Sat, 06 Mar 2021 01:22:17 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e17f4ee95d03eb4824f5b3b7eea5d5f65d599b8c1cbdd6e89cfe2c89b5a3beb`  
		Last Modified: Sat, 06 Mar 2021 01:22:21 GMT  
		Size: 5.7 MB (5656691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8a39b96e5982b6d4c90f60c9826018614c19d1cdf81d6d948ef114821c0f43`  
		Last Modified: Sat, 06 Mar 2021 01:22:18 GMT  
		Size: 16.0 MB (15960741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8454607fef0da445f612c2b2261e24ab07cd1bb138974086b792904f7f65d12`  
		Last Modified: Sat, 06 Mar 2021 01:22:14 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c9e3ca292261806cf558098b1da9f980736d49c58d10c24903eb58c91be842`  
		Last Modified: Sat, 06 Mar 2021 01:22:14 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d384fa928942fa296f88281379207d56f5744aa668e620fa13afc300b129fdb`  
		Last Modified: Sat, 06 Mar 2021 01:22:15 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

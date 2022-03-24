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
-	[`nats-streaming:0.24.3`](#nats-streaming0243)
-	[`nats-streaming:0.24.3-alpine`](#nats-streaming0243-alpine)
-	[`nats-streaming:0.24.3-alpine3.15`](#nats-streaming0243-alpine315)
-	[`nats-streaming:0.24.3-linux`](#nats-streaming0243-linux)
-	[`nats-streaming:0.24.3-nanoserver`](#nats-streaming0243-nanoserver)
-	[`nats-streaming:0.24.3-nanoserver-1809`](#nats-streaming0243-nanoserver-1809)
-	[`nats-streaming:0.24.3-scratch`](#nats-streaming0243-scratch)
-	[`nats-streaming:0.24.3-windowsservercore`](#nats-streaming0243-windowsservercore)
-	[`nats-streaming:0.24.3-windowsservercore-1809`](#nats-streaming0243-windowsservercore-1809)
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
$ docker pull nats-streaming@sha256:9f8cedbf2e74e6679e9ab44848904ad048f1f9202d1dd72e203002605ba4a331
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
$ docker pull nats-streaming@sha256:eea355922fa3e329228180c171fe18939205a5828944f3c0ec23c0816eef7982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db0f18c883ff929dfaae3de15de5562de5be34b4a941aa05c6d52112b8e4c84`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:21:18 GMT
COPY file:6fcfe62a6cc0951979b80258fb3d207e13828d9234e227e1398cab40548702d7 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:21:18 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:21:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:64b920df5d588d78c6c317a08480a016eb7b6433705c1a3811a22e4e422e61d0`  
		Last Modified: Wed, 09 Mar 2022 23:22:00 GMT  
		Size: 7.1 MB (7081263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:36364386127a72bc130f59fb33c4119222fc6c671e33aea460f694025b82cd46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a965dc95f8a3e6631c5ca714f0aafd2acc1508a1f6d3298300876536949f11b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:49:55 GMT
COPY file:d62d923585419f7f9d263c0018d56cc159b1092bf7bae749223f339a514a81d9 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:49:56 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:49:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0b00cb53513f9c5bd72363c73ee281128c2cedd1d7653aa7278a2a6536c86a14`  
		Last Modified: Wed, 09 Mar 2022 23:51:50 GMT  
		Size: 6.6 MB (6597197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:c786255507edae1bf8167b3adbe962fa9c4ba18fd683462921df662c86e5f36f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6589565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb16b4f9d4a38de66adad0c74fd19049b37e96277e0cd459805b74bdf9474ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:29:51 GMT
COPY file:a5f2524f76b038dc99564d67f8cf6396171fe569b86b60aa9892eca88643b977 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:29:52 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:29:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:29:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:271fefa5e75537e471ab2e96d1b28b6614b2103db059b37f0e60bcc9b8ab40d8`  
		Last Modified: Wed, 09 Mar 2022 23:31:44 GMT  
		Size: 6.6 MB (6589565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bb6e16886863d8c84bc6427c4a45c43bca8f97adcddd602756dddc70fa826a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1fc4d49faf17ca5b2a9d116b2758a93de1af0ea5b526e23128bd6bbd00b5f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:41:07 GMT
COPY file:f47e5ea058ace7f6cdb8bca186dec2b15d364fff4ff67303ae8d2cfe38435050 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:41:07 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:41:08 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:41:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9e32cf3eae8c97676148171d71a3cc25149de87eecd89a137222b3b382cdf8f2`  
		Last Modified: Wed, 09 Mar 2022 23:42:13 GMT  
		Size: 6.5 MB (6510632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:bf5f4238170d36fdc3b99a4ab8acea5c5755564d3d97131d48d0730dee33bbdc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110249474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68219116c19a9ac4e2603cd23ba4233e15f3ab67ba4a4e9169a2c000801679cc`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:21:44 GMT
RUN cmd /S /C #(nop) COPY file:2bdfa73d50ba6f64f600945ecab061708a66086f5dd80ec5e00ad93c8bf3b8b6 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 23:21:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:47 GMT
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
	-	`sha256:3128e56b52a1dd66549cb7830a9bc9f9352ab11829fe936a4bd03858ac830160`  
		Last Modified: Wed, 09 Mar 2022 23:22:35 GMT  
		Size: 7.2 MB (7190251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c581f41ddfe2959d4092845a36fa343eaddd42a160cd818cbca5c31671bff`  
		Last Modified: Wed, 09 Mar 2022 23:22:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba79d16ae428589a386d36328db720a9ac0eb1abd0014da9992cb03cf4df1e`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c567d244b9f979dfa1c24fe471a72b7dc849619f91830d175ca5454f357a2eb`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-alpine`

```console
$ docker pull nats-streaming@sha256:91dac67ada020c90e09766553b35cc4f5ce99dd03b7623c1b57f2f849d5ee806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:9fe3aa5829e9d3182998a1e06fdff4e334ddca045e96a2c9b5d162a977c666ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10168066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c875f434580033077c192a32b1d977f044279a8d835e5a97eead41d7195778`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 18:05:00 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 23 Mar 2022 18:05:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 23 Mar 2022 18:05:02 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 23 Mar 2022 18:05:03 GMT
EXPOSE 4222 8222
# Wed, 23 Mar 2022 18:05:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 18:05:03 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20aab72565ea910dd4302002ee7884ba75c62a05cfc50cb36f5f50c0b9bef6a`  
		Last Modified: Wed, 23 Mar 2022 18:05:30 GMT  
		Size: 7.4 MB (7354957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658077bd609b4d5d035e07d270607b59edb37aa8513038d447e44d8ca0a3d236`  
		Last Modified: Wed, 23 Mar 2022 18:05:29 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:da5c30c24c088f46f350a97493d89e0bd7e6e89f360cd72875c0bc7b45f9aa37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9495158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d87fc81f7ee48be7761b2e5903e28d795c026df3dab00a2e5fd8fcd6f7890e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 23 Mar 2022 15:49:35 GMT
ADD file:fd7f6da4a48df653ae6dd18e6d5959008daf5ce429845c974982dc7d213342d9 in / 
# Wed, 23 Mar 2022 15:49:35 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:44:07 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 23 Mar 2022 19:44:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 23 Mar 2022 19:44:13 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 23 Mar 2022 19:44:13 GMT
EXPOSE 4222 8222
# Wed, 23 Mar 2022 19:44:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 19:44:14 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:4e012d7cd81aa4570d9d209a75131b32f34a3533d5d449d23fd875513922588e`  
		Last Modified: Wed, 23 Mar 2022 15:51:07 GMT  
		Size: 2.6 MB (2624816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa88f1fb7bbc792265d0d3b6e07493e48c8721131a58114f6e59fe67494a4a1`  
		Last Modified: Wed, 23 Mar 2022 19:45:54 GMT  
		Size: 6.9 MB (6869923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5862a837be7f24421ba3719cede078392fe5d98759e5dcffc4edd342b7a916`  
		Last Modified: Wed, 23 Mar 2022 19:45:49 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:916ce7f967ce4c50901a7781eb6b2ad8e1b329b12a2f814758c93ac48dcf4429
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9289636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36f59fd5dbc054e5c6be9c9de6ff416d207cddd3199efee42180a5eb02d4c74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 21:59:53 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 23 Mar 2022 21:59:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 23 Mar 2022 21:59:58 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 23 Mar 2022 21:59:58 GMT
EXPOSE 4222 8222
# Wed, 23 Mar 2022 21:59:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 21:59:59 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d781846a82ba534e1e0c19b9eca25d87ca255f45226036da71ea2686242197b7`  
		Last Modified: Wed, 23 Mar 2022 22:01:44 GMT  
		Size: 6.9 MB (6862153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecea31a7006920f966542a97535211ed2d35fa9a09c89d67dbe4faf8753850e8`  
		Last Modified: Wed, 23 Mar 2022 22:01:40 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:9ad69a391a12ffb8de8d3c4cdecbce7433e9e7e4c4edfd42097538769aed3501
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9498217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a113f8c2aefe142234f29e4737965aec98053e8555f311c16cce8983eff6796`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 06:16:44 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Thu, 24 Mar 2022 06:16:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 24 Mar 2022 06:16:49 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 24 Mar 2022 06:16:49 GMT
EXPOSE 4222 8222
# Thu, 24 Mar 2022 06:16:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 06:16:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2811a7be31f1cee7d325c47fc0fbd3af7e6118677b764b4cf99c5528c69a4a0`  
		Last Modified: Thu, 24 Mar 2022 06:17:36 GMT  
		Size: 6.8 MB (6783075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd313c83b529290b935a875a11190713accb8a493139667c860d27090ba9cccf`  
		Last Modified: Thu, 24 Mar 2022 06:17:35 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-alpine3.15`

```console
$ docker pull nats-streaming@sha256:91dac67ada020c90e09766553b35cc4f5ce99dd03b7623c1b57f2f849d5ee806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24-alpine3.15` - linux; amd64

```console
$ docker pull nats-streaming@sha256:9fe3aa5829e9d3182998a1e06fdff4e334ddca045e96a2c9b5d162a977c666ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10168066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c875f434580033077c192a32b1d977f044279a8d835e5a97eead41d7195778`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 18:05:00 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 23 Mar 2022 18:05:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 23 Mar 2022 18:05:02 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 23 Mar 2022 18:05:03 GMT
EXPOSE 4222 8222
# Wed, 23 Mar 2022 18:05:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 18:05:03 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20aab72565ea910dd4302002ee7884ba75c62a05cfc50cb36f5f50c0b9bef6a`  
		Last Modified: Wed, 23 Mar 2022 18:05:30 GMT  
		Size: 7.4 MB (7354957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658077bd609b4d5d035e07d270607b59edb37aa8513038d447e44d8ca0a3d236`  
		Last Modified: Wed, 23 Mar 2022 18:05:29 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:da5c30c24c088f46f350a97493d89e0bd7e6e89f360cd72875c0bc7b45f9aa37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9495158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d87fc81f7ee48be7761b2e5903e28d795c026df3dab00a2e5fd8fcd6f7890e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 23 Mar 2022 15:49:35 GMT
ADD file:fd7f6da4a48df653ae6dd18e6d5959008daf5ce429845c974982dc7d213342d9 in / 
# Wed, 23 Mar 2022 15:49:35 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:44:07 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 23 Mar 2022 19:44:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 23 Mar 2022 19:44:13 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 23 Mar 2022 19:44:13 GMT
EXPOSE 4222 8222
# Wed, 23 Mar 2022 19:44:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 19:44:14 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:4e012d7cd81aa4570d9d209a75131b32f34a3533d5d449d23fd875513922588e`  
		Last Modified: Wed, 23 Mar 2022 15:51:07 GMT  
		Size: 2.6 MB (2624816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa88f1fb7bbc792265d0d3b6e07493e48c8721131a58114f6e59fe67494a4a1`  
		Last Modified: Wed, 23 Mar 2022 19:45:54 GMT  
		Size: 6.9 MB (6869923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5862a837be7f24421ba3719cede078392fe5d98759e5dcffc4edd342b7a916`  
		Last Modified: Wed, 23 Mar 2022 19:45:49 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:916ce7f967ce4c50901a7781eb6b2ad8e1b329b12a2f814758c93ac48dcf4429
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9289636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36f59fd5dbc054e5c6be9c9de6ff416d207cddd3199efee42180a5eb02d4c74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 21:59:53 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 23 Mar 2022 21:59:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 23 Mar 2022 21:59:58 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 23 Mar 2022 21:59:58 GMT
EXPOSE 4222 8222
# Wed, 23 Mar 2022 21:59:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 21:59:59 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d781846a82ba534e1e0c19b9eca25d87ca255f45226036da71ea2686242197b7`  
		Last Modified: Wed, 23 Mar 2022 22:01:44 GMT  
		Size: 6.9 MB (6862153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecea31a7006920f966542a97535211ed2d35fa9a09c89d67dbe4faf8753850e8`  
		Last Modified: Wed, 23 Mar 2022 22:01:40 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:9ad69a391a12ffb8de8d3c4cdecbce7433e9e7e4c4edfd42097538769aed3501
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9498217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a113f8c2aefe142234f29e4737965aec98053e8555f311c16cce8983eff6796`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 06:16:44 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Thu, 24 Mar 2022 06:16:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 24 Mar 2022 06:16:49 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 24 Mar 2022 06:16:49 GMT
EXPOSE 4222 8222
# Thu, 24 Mar 2022 06:16:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 06:16:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2811a7be31f1cee7d325c47fc0fbd3af7e6118677b764b4cf99c5528c69a4a0`  
		Last Modified: Thu, 24 Mar 2022 06:17:36 GMT  
		Size: 6.8 MB (6783075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd313c83b529290b935a875a11190713accb8a493139667c860d27090ba9cccf`  
		Last Modified: Thu, 24 Mar 2022 06:17:35 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-linux`

```console
$ docker pull nats-streaming@sha256:4f097bcee579937a2b55f7702298c9d0ccf44bc8fc2820b81ef02b1a9b146e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eea355922fa3e329228180c171fe18939205a5828944f3c0ec23c0816eef7982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db0f18c883ff929dfaae3de15de5562de5be34b4a941aa05c6d52112b8e4c84`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:21:18 GMT
COPY file:6fcfe62a6cc0951979b80258fb3d207e13828d9234e227e1398cab40548702d7 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:21:18 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:21:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:64b920df5d588d78c6c317a08480a016eb7b6433705c1a3811a22e4e422e61d0`  
		Last Modified: Wed, 09 Mar 2022 23:22:00 GMT  
		Size: 7.1 MB (7081263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:36364386127a72bc130f59fb33c4119222fc6c671e33aea460f694025b82cd46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a965dc95f8a3e6631c5ca714f0aafd2acc1508a1f6d3298300876536949f11b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:49:55 GMT
COPY file:d62d923585419f7f9d263c0018d56cc159b1092bf7bae749223f339a514a81d9 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:49:56 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:49:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0b00cb53513f9c5bd72363c73ee281128c2cedd1d7653aa7278a2a6536c86a14`  
		Last Modified: Wed, 09 Mar 2022 23:51:50 GMT  
		Size: 6.6 MB (6597197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:c786255507edae1bf8167b3adbe962fa9c4ba18fd683462921df662c86e5f36f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6589565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb16b4f9d4a38de66adad0c74fd19049b37e96277e0cd459805b74bdf9474ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:29:51 GMT
COPY file:a5f2524f76b038dc99564d67f8cf6396171fe569b86b60aa9892eca88643b977 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:29:52 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:29:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:29:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:271fefa5e75537e471ab2e96d1b28b6614b2103db059b37f0e60bcc9b8ab40d8`  
		Last Modified: Wed, 09 Mar 2022 23:31:44 GMT  
		Size: 6.6 MB (6589565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bb6e16886863d8c84bc6427c4a45c43bca8f97adcddd602756dddc70fa826a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1fc4d49faf17ca5b2a9d116b2758a93de1af0ea5b526e23128bd6bbd00b5f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:41:07 GMT
COPY file:f47e5ea058ace7f6cdb8bca186dec2b15d364fff4ff67303ae8d2cfe38435050 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:41:07 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:41:08 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:41:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9e32cf3eae8c97676148171d71a3cc25149de87eecd89a137222b3b382cdf8f2`  
		Last Modified: Wed, 09 Mar 2022 23:42:13 GMT  
		Size: 6.5 MB (6510632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-nanoserver`

```console
$ docker pull nats-streaming@sha256:427167cf68f6cc7da882af2fe3a4b7c8089d370a60bdfb20d1c2f432095618d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24-nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:bf5f4238170d36fdc3b99a4ab8acea5c5755564d3d97131d48d0730dee33bbdc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110249474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68219116c19a9ac4e2603cd23ba4233e15f3ab67ba4a4e9169a2c000801679cc`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:21:44 GMT
RUN cmd /S /C #(nop) COPY file:2bdfa73d50ba6f64f600945ecab061708a66086f5dd80ec5e00ad93c8bf3b8b6 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 23:21:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:47 GMT
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
	-	`sha256:3128e56b52a1dd66549cb7830a9bc9f9352ab11829fe936a4bd03858ac830160`  
		Last Modified: Wed, 09 Mar 2022 23:22:35 GMT  
		Size: 7.2 MB (7190251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c581f41ddfe2959d4092845a36fa343eaddd42a160cd818cbca5c31671bff`  
		Last Modified: Wed, 09 Mar 2022 23:22:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba79d16ae428589a386d36328db720a9ac0eb1abd0014da9992cb03cf4df1e`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c567d244b9f979dfa1c24fe471a72b7dc849619f91830d175ca5454f357a2eb`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:427167cf68f6cc7da882af2fe3a4b7c8089d370a60bdfb20d1c2f432095618d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:bf5f4238170d36fdc3b99a4ab8acea5c5755564d3d97131d48d0730dee33bbdc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110249474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68219116c19a9ac4e2603cd23ba4233e15f3ab67ba4a4e9169a2c000801679cc`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:21:44 GMT
RUN cmd /S /C #(nop) COPY file:2bdfa73d50ba6f64f600945ecab061708a66086f5dd80ec5e00ad93c8bf3b8b6 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 23:21:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:47 GMT
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
	-	`sha256:3128e56b52a1dd66549cb7830a9bc9f9352ab11829fe936a4bd03858ac830160`  
		Last Modified: Wed, 09 Mar 2022 23:22:35 GMT  
		Size: 7.2 MB (7190251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c581f41ddfe2959d4092845a36fa343eaddd42a160cd818cbca5c31671bff`  
		Last Modified: Wed, 09 Mar 2022 23:22:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba79d16ae428589a386d36328db720a9ac0eb1abd0014da9992cb03cf4df1e`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c567d244b9f979dfa1c24fe471a72b7dc849619f91830d175ca5454f357a2eb`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-scratch`

```console
$ docker pull nats-streaming@sha256:4f097bcee579937a2b55f7702298c9d0ccf44bc8fc2820b81ef02b1a9b146e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eea355922fa3e329228180c171fe18939205a5828944f3c0ec23c0816eef7982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db0f18c883ff929dfaae3de15de5562de5be34b4a941aa05c6d52112b8e4c84`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:21:18 GMT
COPY file:6fcfe62a6cc0951979b80258fb3d207e13828d9234e227e1398cab40548702d7 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:21:18 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:21:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:64b920df5d588d78c6c317a08480a016eb7b6433705c1a3811a22e4e422e61d0`  
		Last Modified: Wed, 09 Mar 2022 23:22:00 GMT  
		Size: 7.1 MB (7081263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:36364386127a72bc130f59fb33c4119222fc6c671e33aea460f694025b82cd46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a965dc95f8a3e6631c5ca714f0aafd2acc1508a1f6d3298300876536949f11b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:49:55 GMT
COPY file:d62d923585419f7f9d263c0018d56cc159b1092bf7bae749223f339a514a81d9 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:49:56 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:49:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0b00cb53513f9c5bd72363c73ee281128c2cedd1d7653aa7278a2a6536c86a14`  
		Last Modified: Wed, 09 Mar 2022 23:51:50 GMT  
		Size: 6.6 MB (6597197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:c786255507edae1bf8167b3adbe962fa9c4ba18fd683462921df662c86e5f36f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6589565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb16b4f9d4a38de66adad0c74fd19049b37e96277e0cd459805b74bdf9474ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:29:51 GMT
COPY file:a5f2524f76b038dc99564d67f8cf6396171fe569b86b60aa9892eca88643b977 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:29:52 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:29:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:29:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:271fefa5e75537e471ab2e96d1b28b6614b2103db059b37f0e60bcc9b8ab40d8`  
		Last Modified: Wed, 09 Mar 2022 23:31:44 GMT  
		Size: 6.6 MB (6589565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bb6e16886863d8c84bc6427c4a45c43bca8f97adcddd602756dddc70fa826a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1fc4d49faf17ca5b2a9d116b2758a93de1af0ea5b526e23128bd6bbd00b5f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:41:07 GMT
COPY file:f47e5ea058ace7f6cdb8bca186dec2b15d364fff4ff67303ae8d2cfe38435050 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:41:07 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:41:08 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:41:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9e32cf3eae8c97676148171d71a3cc25149de87eecd89a137222b3b382cdf8f2`  
		Last Modified: Wed, 09 Mar 2022 23:42:13 GMT  
		Size: 6.5 MB (6510632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-windowsservercore`

```console
$ docker pull nats-streaming@sha256:112510afc4add9efb62621bbcbd4c03a62c4efa7bebfa2854d896a3b81b4822b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:38aa3744b326ea3530932f9ae38c5884a7cc4f4e5e71b77f330b5634d79fa79a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723329559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5125257a9aa0beaab36a017e9f82750b3aac24f4719374d6cc8e339fc187cdd`
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
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.3/nats-streaming-server-v0.24.3-windows-amd64.zip
# Wed, 09 Mar 2022 23:18:48 GMT
ENV NATS_STREAMING_SERVER_SHASUM=7473bfa7efd734ca6984907bc9586260031cca926883b468b4752557ecefaff0
# Wed, 09 Mar 2022 23:19:49 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:21:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:21:28 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:29 GMT
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
	-	`sha256:3b1aac6ec834525c931dc81bbbb6d32996b82fd755a3bd625af11f40b8fc66bb`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d303e56675a80a6fa4eef8ef31d6f93742709f41058dcf6e36b8ba6d71a466f8`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8122e4b6aba607bd3d7b17a847d8ab75da7d7cb7a2bbb035e4a31cfc1b7ce6`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393372fa0a20ba2589a43d177f33a0360245be974d231efaa7ab980bc342b574`  
		Last Modified: Wed, 09 Mar 2022 23:22:13 GMT  
		Size: 349.0 KB (348988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3cf158dc37e43f4d84e520f088e32b2851abbf4a70af92161ab5e0d7e3ecbd`  
		Last Modified: Wed, 09 Mar 2022 23:22:20 GMT  
		Size: 7.5 MB (7516588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fff4072b17e75a66709617708b8b9263dabe4a12c4e0a594fb52e058977fa83`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de86f56dd22fbee61ed7161f763ba9de61d7cbf9623b85a879723ea5670f6e20`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04add3ff0ef25a1f32aab83f90a95cffab3d4b55afd3eb376a861b36094a0b0`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:112510afc4add9efb62621bbcbd4c03a62c4efa7bebfa2854d896a3b81b4822b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:38aa3744b326ea3530932f9ae38c5884a7cc4f4e5e71b77f330b5634d79fa79a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723329559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5125257a9aa0beaab36a017e9f82750b3aac24f4719374d6cc8e339fc187cdd`
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
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.3/nats-streaming-server-v0.24.3-windows-amd64.zip
# Wed, 09 Mar 2022 23:18:48 GMT
ENV NATS_STREAMING_SERVER_SHASUM=7473bfa7efd734ca6984907bc9586260031cca926883b468b4752557ecefaff0
# Wed, 09 Mar 2022 23:19:49 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:21:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:21:28 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:29 GMT
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
	-	`sha256:3b1aac6ec834525c931dc81bbbb6d32996b82fd755a3bd625af11f40b8fc66bb`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d303e56675a80a6fa4eef8ef31d6f93742709f41058dcf6e36b8ba6d71a466f8`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8122e4b6aba607bd3d7b17a847d8ab75da7d7cb7a2bbb035e4a31cfc1b7ce6`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393372fa0a20ba2589a43d177f33a0360245be974d231efaa7ab980bc342b574`  
		Last Modified: Wed, 09 Mar 2022 23:22:13 GMT  
		Size: 349.0 KB (348988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3cf158dc37e43f4d84e520f088e32b2851abbf4a70af92161ab5e0d7e3ecbd`  
		Last Modified: Wed, 09 Mar 2022 23:22:20 GMT  
		Size: 7.5 MB (7516588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fff4072b17e75a66709617708b8b9263dabe4a12c4e0a594fb52e058977fa83`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de86f56dd22fbee61ed7161f763ba9de61d7cbf9623b85a879723ea5670f6e20`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04add3ff0ef25a1f32aab83f90a95cffab3d4b55afd3eb376a861b36094a0b0`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.3`

```console
$ docker pull nats-streaming@sha256:9f8cedbf2e74e6679e9ab44848904ad048f1f9202d1dd72e203002605ba4a331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24.3` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eea355922fa3e329228180c171fe18939205a5828944f3c0ec23c0816eef7982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db0f18c883ff929dfaae3de15de5562de5be34b4a941aa05c6d52112b8e4c84`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:21:18 GMT
COPY file:6fcfe62a6cc0951979b80258fb3d207e13828d9234e227e1398cab40548702d7 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:21:18 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:21:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:64b920df5d588d78c6c317a08480a016eb7b6433705c1a3811a22e4e422e61d0`  
		Last Modified: Wed, 09 Mar 2022 23:22:00 GMT  
		Size: 7.1 MB (7081263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:36364386127a72bc130f59fb33c4119222fc6c671e33aea460f694025b82cd46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a965dc95f8a3e6631c5ca714f0aafd2acc1508a1f6d3298300876536949f11b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:49:55 GMT
COPY file:d62d923585419f7f9d263c0018d56cc159b1092bf7bae749223f339a514a81d9 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:49:56 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:49:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0b00cb53513f9c5bd72363c73ee281128c2cedd1d7653aa7278a2a6536c86a14`  
		Last Modified: Wed, 09 Mar 2022 23:51:50 GMT  
		Size: 6.6 MB (6597197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:c786255507edae1bf8167b3adbe962fa9c4ba18fd683462921df662c86e5f36f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6589565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb16b4f9d4a38de66adad0c74fd19049b37e96277e0cd459805b74bdf9474ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:29:51 GMT
COPY file:a5f2524f76b038dc99564d67f8cf6396171fe569b86b60aa9892eca88643b977 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:29:52 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:29:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:29:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:271fefa5e75537e471ab2e96d1b28b6614b2103db059b37f0e60bcc9b8ab40d8`  
		Last Modified: Wed, 09 Mar 2022 23:31:44 GMT  
		Size: 6.6 MB (6589565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bb6e16886863d8c84bc6427c4a45c43bca8f97adcddd602756dddc70fa826a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1fc4d49faf17ca5b2a9d116b2758a93de1af0ea5b526e23128bd6bbd00b5f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:41:07 GMT
COPY file:f47e5ea058ace7f6cdb8bca186dec2b15d364fff4ff67303ae8d2cfe38435050 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:41:07 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:41:08 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:41:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9e32cf3eae8c97676148171d71a3cc25149de87eecd89a137222b3b382cdf8f2`  
		Last Modified: Wed, 09 Mar 2022 23:42:13 GMT  
		Size: 6.5 MB (6510632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:bf5f4238170d36fdc3b99a4ab8acea5c5755564d3d97131d48d0730dee33bbdc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110249474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68219116c19a9ac4e2603cd23ba4233e15f3ab67ba4a4e9169a2c000801679cc`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:21:44 GMT
RUN cmd /S /C #(nop) COPY file:2bdfa73d50ba6f64f600945ecab061708a66086f5dd80ec5e00ad93c8bf3b8b6 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 23:21:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:47 GMT
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
	-	`sha256:3128e56b52a1dd66549cb7830a9bc9f9352ab11829fe936a4bd03858ac830160`  
		Last Modified: Wed, 09 Mar 2022 23:22:35 GMT  
		Size: 7.2 MB (7190251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c581f41ddfe2959d4092845a36fa343eaddd42a160cd818cbca5c31671bff`  
		Last Modified: Wed, 09 Mar 2022 23:22:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba79d16ae428589a386d36328db720a9ac0eb1abd0014da9992cb03cf4df1e`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c567d244b9f979dfa1c24fe471a72b7dc849619f91830d175ca5454f357a2eb`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.3-alpine`

```console
$ docker pull nats-streaming@sha256:91dac67ada020c90e09766553b35cc4f5ce99dd03b7623c1b57f2f849d5ee806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24.3-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:9fe3aa5829e9d3182998a1e06fdff4e334ddca045e96a2c9b5d162a977c666ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10168066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c875f434580033077c192a32b1d977f044279a8d835e5a97eead41d7195778`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 18:05:00 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 23 Mar 2022 18:05:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 23 Mar 2022 18:05:02 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 23 Mar 2022 18:05:03 GMT
EXPOSE 4222 8222
# Wed, 23 Mar 2022 18:05:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 18:05:03 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20aab72565ea910dd4302002ee7884ba75c62a05cfc50cb36f5f50c0b9bef6a`  
		Last Modified: Wed, 23 Mar 2022 18:05:30 GMT  
		Size: 7.4 MB (7354957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658077bd609b4d5d035e07d270607b59edb37aa8513038d447e44d8ca0a3d236`  
		Last Modified: Wed, 23 Mar 2022 18:05:29 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:da5c30c24c088f46f350a97493d89e0bd7e6e89f360cd72875c0bc7b45f9aa37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9495158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d87fc81f7ee48be7761b2e5903e28d795c026df3dab00a2e5fd8fcd6f7890e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 23 Mar 2022 15:49:35 GMT
ADD file:fd7f6da4a48df653ae6dd18e6d5959008daf5ce429845c974982dc7d213342d9 in / 
# Wed, 23 Mar 2022 15:49:35 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:44:07 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 23 Mar 2022 19:44:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 23 Mar 2022 19:44:13 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 23 Mar 2022 19:44:13 GMT
EXPOSE 4222 8222
# Wed, 23 Mar 2022 19:44:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 19:44:14 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:4e012d7cd81aa4570d9d209a75131b32f34a3533d5d449d23fd875513922588e`  
		Last Modified: Wed, 23 Mar 2022 15:51:07 GMT  
		Size: 2.6 MB (2624816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa88f1fb7bbc792265d0d3b6e07493e48c8721131a58114f6e59fe67494a4a1`  
		Last Modified: Wed, 23 Mar 2022 19:45:54 GMT  
		Size: 6.9 MB (6869923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5862a837be7f24421ba3719cede078392fe5d98759e5dcffc4edd342b7a916`  
		Last Modified: Wed, 23 Mar 2022 19:45:49 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:916ce7f967ce4c50901a7781eb6b2ad8e1b329b12a2f814758c93ac48dcf4429
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9289636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36f59fd5dbc054e5c6be9c9de6ff416d207cddd3199efee42180a5eb02d4c74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 21:59:53 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 23 Mar 2022 21:59:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 23 Mar 2022 21:59:58 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 23 Mar 2022 21:59:58 GMT
EXPOSE 4222 8222
# Wed, 23 Mar 2022 21:59:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 21:59:59 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d781846a82ba534e1e0c19b9eca25d87ca255f45226036da71ea2686242197b7`  
		Last Modified: Wed, 23 Mar 2022 22:01:44 GMT  
		Size: 6.9 MB (6862153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecea31a7006920f966542a97535211ed2d35fa9a09c89d67dbe4faf8753850e8`  
		Last Modified: Wed, 23 Mar 2022 22:01:40 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:9ad69a391a12ffb8de8d3c4cdecbce7433e9e7e4c4edfd42097538769aed3501
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9498217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a113f8c2aefe142234f29e4737965aec98053e8555f311c16cce8983eff6796`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 06:16:44 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Thu, 24 Mar 2022 06:16:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 24 Mar 2022 06:16:49 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 24 Mar 2022 06:16:49 GMT
EXPOSE 4222 8222
# Thu, 24 Mar 2022 06:16:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 06:16:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2811a7be31f1cee7d325c47fc0fbd3af7e6118677b764b4cf99c5528c69a4a0`  
		Last Modified: Thu, 24 Mar 2022 06:17:36 GMT  
		Size: 6.8 MB (6783075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd313c83b529290b935a875a11190713accb8a493139667c860d27090ba9cccf`  
		Last Modified: Thu, 24 Mar 2022 06:17:35 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.3-alpine3.15`

```console
$ docker pull nats-streaming@sha256:91dac67ada020c90e09766553b35cc4f5ce99dd03b7623c1b57f2f849d5ee806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24.3-alpine3.15` - linux; amd64

```console
$ docker pull nats-streaming@sha256:9fe3aa5829e9d3182998a1e06fdff4e334ddca045e96a2c9b5d162a977c666ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10168066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c875f434580033077c192a32b1d977f044279a8d835e5a97eead41d7195778`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 18:05:00 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 23 Mar 2022 18:05:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 23 Mar 2022 18:05:02 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 23 Mar 2022 18:05:03 GMT
EXPOSE 4222 8222
# Wed, 23 Mar 2022 18:05:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 18:05:03 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20aab72565ea910dd4302002ee7884ba75c62a05cfc50cb36f5f50c0b9bef6a`  
		Last Modified: Wed, 23 Mar 2022 18:05:30 GMT  
		Size: 7.4 MB (7354957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658077bd609b4d5d035e07d270607b59edb37aa8513038d447e44d8ca0a3d236`  
		Last Modified: Wed, 23 Mar 2022 18:05:29 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:da5c30c24c088f46f350a97493d89e0bd7e6e89f360cd72875c0bc7b45f9aa37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9495158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d87fc81f7ee48be7761b2e5903e28d795c026df3dab00a2e5fd8fcd6f7890e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 23 Mar 2022 15:49:35 GMT
ADD file:fd7f6da4a48df653ae6dd18e6d5959008daf5ce429845c974982dc7d213342d9 in / 
# Wed, 23 Mar 2022 15:49:35 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:44:07 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 23 Mar 2022 19:44:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 23 Mar 2022 19:44:13 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 23 Mar 2022 19:44:13 GMT
EXPOSE 4222 8222
# Wed, 23 Mar 2022 19:44:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 19:44:14 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:4e012d7cd81aa4570d9d209a75131b32f34a3533d5d449d23fd875513922588e`  
		Last Modified: Wed, 23 Mar 2022 15:51:07 GMT  
		Size: 2.6 MB (2624816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa88f1fb7bbc792265d0d3b6e07493e48c8721131a58114f6e59fe67494a4a1`  
		Last Modified: Wed, 23 Mar 2022 19:45:54 GMT  
		Size: 6.9 MB (6869923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5862a837be7f24421ba3719cede078392fe5d98759e5dcffc4edd342b7a916`  
		Last Modified: Wed, 23 Mar 2022 19:45:49 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:916ce7f967ce4c50901a7781eb6b2ad8e1b329b12a2f814758c93ac48dcf4429
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9289636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36f59fd5dbc054e5c6be9c9de6ff416d207cddd3199efee42180a5eb02d4c74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 21:59:53 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 23 Mar 2022 21:59:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 23 Mar 2022 21:59:58 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 23 Mar 2022 21:59:58 GMT
EXPOSE 4222 8222
# Wed, 23 Mar 2022 21:59:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 21:59:59 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d781846a82ba534e1e0c19b9eca25d87ca255f45226036da71ea2686242197b7`  
		Last Modified: Wed, 23 Mar 2022 22:01:44 GMT  
		Size: 6.9 MB (6862153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecea31a7006920f966542a97535211ed2d35fa9a09c89d67dbe4faf8753850e8`  
		Last Modified: Wed, 23 Mar 2022 22:01:40 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:9ad69a391a12ffb8de8d3c4cdecbce7433e9e7e4c4edfd42097538769aed3501
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9498217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a113f8c2aefe142234f29e4737965aec98053e8555f311c16cce8983eff6796`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 06:16:44 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Thu, 24 Mar 2022 06:16:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 24 Mar 2022 06:16:49 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 24 Mar 2022 06:16:49 GMT
EXPOSE 4222 8222
# Thu, 24 Mar 2022 06:16:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 06:16:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2811a7be31f1cee7d325c47fc0fbd3af7e6118677b764b4cf99c5528c69a4a0`  
		Last Modified: Thu, 24 Mar 2022 06:17:36 GMT  
		Size: 6.8 MB (6783075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd313c83b529290b935a875a11190713accb8a493139667c860d27090ba9cccf`  
		Last Modified: Thu, 24 Mar 2022 06:17:35 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.3-linux`

```console
$ docker pull nats-streaming@sha256:4f097bcee579937a2b55f7702298c9d0ccf44bc8fc2820b81ef02b1a9b146e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24.3-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eea355922fa3e329228180c171fe18939205a5828944f3c0ec23c0816eef7982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db0f18c883ff929dfaae3de15de5562de5be34b4a941aa05c6d52112b8e4c84`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:21:18 GMT
COPY file:6fcfe62a6cc0951979b80258fb3d207e13828d9234e227e1398cab40548702d7 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:21:18 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:21:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:64b920df5d588d78c6c317a08480a016eb7b6433705c1a3811a22e4e422e61d0`  
		Last Modified: Wed, 09 Mar 2022 23:22:00 GMT  
		Size: 7.1 MB (7081263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:36364386127a72bc130f59fb33c4119222fc6c671e33aea460f694025b82cd46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a965dc95f8a3e6631c5ca714f0aafd2acc1508a1f6d3298300876536949f11b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:49:55 GMT
COPY file:d62d923585419f7f9d263c0018d56cc159b1092bf7bae749223f339a514a81d9 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:49:56 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:49:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0b00cb53513f9c5bd72363c73ee281128c2cedd1d7653aa7278a2a6536c86a14`  
		Last Modified: Wed, 09 Mar 2022 23:51:50 GMT  
		Size: 6.6 MB (6597197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:c786255507edae1bf8167b3adbe962fa9c4ba18fd683462921df662c86e5f36f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6589565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb16b4f9d4a38de66adad0c74fd19049b37e96277e0cd459805b74bdf9474ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:29:51 GMT
COPY file:a5f2524f76b038dc99564d67f8cf6396171fe569b86b60aa9892eca88643b977 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:29:52 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:29:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:29:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:271fefa5e75537e471ab2e96d1b28b6614b2103db059b37f0e60bcc9b8ab40d8`  
		Last Modified: Wed, 09 Mar 2022 23:31:44 GMT  
		Size: 6.6 MB (6589565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bb6e16886863d8c84bc6427c4a45c43bca8f97adcddd602756dddc70fa826a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1fc4d49faf17ca5b2a9d116b2758a93de1af0ea5b526e23128bd6bbd00b5f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:41:07 GMT
COPY file:f47e5ea058ace7f6cdb8bca186dec2b15d364fff4ff67303ae8d2cfe38435050 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:41:07 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:41:08 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:41:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9e32cf3eae8c97676148171d71a3cc25149de87eecd89a137222b3b382cdf8f2`  
		Last Modified: Wed, 09 Mar 2022 23:42:13 GMT  
		Size: 6.5 MB (6510632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.3-nanoserver`

```console
$ docker pull nats-streaming@sha256:427167cf68f6cc7da882af2fe3a4b7c8089d370a60bdfb20d1c2f432095618d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24.3-nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:bf5f4238170d36fdc3b99a4ab8acea5c5755564d3d97131d48d0730dee33bbdc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110249474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68219116c19a9ac4e2603cd23ba4233e15f3ab67ba4a4e9169a2c000801679cc`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:21:44 GMT
RUN cmd /S /C #(nop) COPY file:2bdfa73d50ba6f64f600945ecab061708a66086f5dd80ec5e00ad93c8bf3b8b6 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 23:21:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:47 GMT
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
	-	`sha256:3128e56b52a1dd66549cb7830a9bc9f9352ab11829fe936a4bd03858ac830160`  
		Last Modified: Wed, 09 Mar 2022 23:22:35 GMT  
		Size: 7.2 MB (7190251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c581f41ddfe2959d4092845a36fa343eaddd42a160cd818cbca5c31671bff`  
		Last Modified: Wed, 09 Mar 2022 23:22:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba79d16ae428589a386d36328db720a9ac0eb1abd0014da9992cb03cf4df1e`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c567d244b9f979dfa1c24fe471a72b7dc849619f91830d175ca5454f357a2eb`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.3-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:427167cf68f6cc7da882af2fe3a4b7c8089d370a60bdfb20d1c2f432095618d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24.3-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:bf5f4238170d36fdc3b99a4ab8acea5c5755564d3d97131d48d0730dee33bbdc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110249474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68219116c19a9ac4e2603cd23ba4233e15f3ab67ba4a4e9169a2c000801679cc`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:21:44 GMT
RUN cmd /S /C #(nop) COPY file:2bdfa73d50ba6f64f600945ecab061708a66086f5dd80ec5e00ad93c8bf3b8b6 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 23:21:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:47 GMT
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
	-	`sha256:3128e56b52a1dd66549cb7830a9bc9f9352ab11829fe936a4bd03858ac830160`  
		Last Modified: Wed, 09 Mar 2022 23:22:35 GMT  
		Size: 7.2 MB (7190251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c581f41ddfe2959d4092845a36fa343eaddd42a160cd818cbca5c31671bff`  
		Last Modified: Wed, 09 Mar 2022 23:22:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba79d16ae428589a386d36328db720a9ac0eb1abd0014da9992cb03cf4df1e`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c567d244b9f979dfa1c24fe471a72b7dc849619f91830d175ca5454f357a2eb`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.3-scratch`

```console
$ docker pull nats-streaming@sha256:4f097bcee579937a2b55f7702298c9d0ccf44bc8fc2820b81ef02b1a9b146e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24.3-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eea355922fa3e329228180c171fe18939205a5828944f3c0ec23c0816eef7982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db0f18c883ff929dfaae3de15de5562de5be34b4a941aa05c6d52112b8e4c84`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:21:18 GMT
COPY file:6fcfe62a6cc0951979b80258fb3d207e13828d9234e227e1398cab40548702d7 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:21:18 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:21:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:64b920df5d588d78c6c317a08480a016eb7b6433705c1a3811a22e4e422e61d0`  
		Last Modified: Wed, 09 Mar 2022 23:22:00 GMT  
		Size: 7.1 MB (7081263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:36364386127a72bc130f59fb33c4119222fc6c671e33aea460f694025b82cd46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a965dc95f8a3e6631c5ca714f0aafd2acc1508a1f6d3298300876536949f11b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:49:55 GMT
COPY file:d62d923585419f7f9d263c0018d56cc159b1092bf7bae749223f339a514a81d9 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:49:56 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:49:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0b00cb53513f9c5bd72363c73ee281128c2cedd1d7653aa7278a2a6536c86a14`  
		Last Modified: Wed, 09 Mar 2022 23:51:50 GMT  
		Size: 6.6 MB (6597197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:c786255507edae1bf8167b3adbe962fa9c4ba18fd683462921df662c86e5f36f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6589565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb16b4f9d4a38de66adad0c74fd19049b37e96277e0cd459805b74bdf9474ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:29:51 GMT
COPY file:a5f2524f76b038dc99564d67f8cf6396171fe569b86b60aa9892eca88643b977 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:29:52 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:29:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:29:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:271fefa5e75537e471ab2e96d1b28b6614b2103db059b37f0e60bcc9b8ab40d8`  
		Last Modified: Wed, 09 Mar 2022 23:31:44 GMT  
		Size: 6.6 MB (6589565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bb6e16886863d8c84bc6427c4a45c43bca8f97adcddd602756dddc70fa826a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1fc4d49faf17ca5b2a9d116b2758a93de1af0ea5b526e23128bd6bbd00b5f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:41:07 GMT
COPY file:f47e5ea058ace7f6cdb8bca186dec2b15d364fff4ff67303ae8d2cfe38435050 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:41:07 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:41:08 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:41:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9e32cf3eae8c97676148171d71a3cc25149de87eecd89a137222b3b382cdf8f2`  
		Last Modified: Wed, 09 Mar 2022 23:42:13 GMT  
		Size: 6.5 MB (6510632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.3-windowsservercore`

```console
$ docker pull nats-streaming@sha256:112510afc4add9efb62621bbcbd4c03a62c4efa7bebfa2854d896a3b81b4822b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24.3-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:38aa3744b326ea3530932f9ae38c5884a7cc4f4e5e71b77f330b5634d79fa79a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723329559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5125257a9aa0beaab36a017e9f82750b3aac24f4719374d6cc8e339fc187cdd`
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
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.3/nats-streaming-server-v0.24.3-windows-amd64.zip
# Wed, 09 Mar 2022 23:18:48 GMT
ENV NATS_STREAMING_SERVER_SHASUM=7473bfa7efd734ca6984907bc9586260031cca926883b468b4752557ecefaff0
# Wed, 09 Mar 2022 23:19:49 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:21:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:21:28 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:29 GMT
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
	-	`sha256:3b1aac6ec834525c931dc81bbbb6d32996b82fd755a3bd625af11f40b8fc66bb`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d303e56675a80a6fa4eef8ef31d6f93742709f41058dcf6e36b8ba6d71a466f8`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8122e4b6aba607bd3d7b17a847d8ab75da7d7cb7a2bbb035e4a31cfc1b7ce6`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393372fa0a20ba2589a43d177f33a0360245be974d231efaa7ab980bc342b574`  
		Last Modified: Wed, 09 Mar 2022 23:22:13 GMT  
		Size: 349.0 KB (348988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3cf158dc37e43f4d84e520f088e32b2851abbf4a70af92161ab5e0d7e3ecbd`  
		Last Modified: Wed, 09 Mar 2022 23:22:20 GMT  
		Size: 7.5 MB (7516588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fff4072b17e75a66709617708b8b9263dabe4a12c4e0a594fb52e058977fa83`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de86f56dd22fbee61ed7161f763ba9de61d7cbf9623b85a879723ea5670f6e20`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04add3ff0ef25a1f32aab83f90a95cffab3d4b55afd3eb376a861b36094a0b0`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.3-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:112510afc4add9efb62621bbcbd4c03a62c4efa7bebfa2854d896a3b81b4822b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24.3-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:38aa3744b326ea3530932f9ae38c5884a7cc4f4e5e71b77f330b5634d79fa79a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723329559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5125257a9aa0beaab36a017e9f82750b3aac24f4719374d6cc8e339fc187cdd`
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
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.3/nats-streaming-server-v0.24.3-windows-amd64.zip
# Wed, 09 Mar 2022 23:18:48 GMT
ENV NATS_STREAMING_SERVER_SHASUM=7473bfa7efd734ca6984907bc9586260031cca926883b468b4752557ecefaff0
# Wed, 09 Mar 2022 23:19:49 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:21:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:21:28 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:29 GMT
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
	-	`sha256:3b1aac6ec834525c931dc81bbbb6d32996b82fd755a3bd625af11f40b8fc66bb`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d303e56675a80a6fa4eef8ef31d6f93742709f41058dcf6e36b8ba6d71a466f8`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8122e4b6aba607bd3d7b17a847d8ab75da7d7cb7a2bbb035e4a31cfc1b7ce6`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393372fa0a20ba2589a43d177f33a0360245be974d231efaa7ab980bc342b574`  
		Last Modified: Wed, 09 Mar 2022 23:22:13 GMT  
		Size: 349.0 KB (348988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3cf158dc37e43f4d84e520f088e32b2851abbf4a70af92161ab5e0d7e3ecbd`  
		Last Modified: Wed, 09 Mar 2022 23:22:20 GMT  
		Size: 7.5 MB (7516588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fff4072b17e75a66709617708b8b9263dabe4a12c4e0a594fb52e058977fa83`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de86f56dd22fbee61ed7161f763ba9de61d7cbf9623b85a879723ea5670f6e20`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04add3ff0ef25a1f32aab83f90a95cffab3d4b55afd3eb376a861b36094a0b0`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:91dac67ada020c90e09766553b35cc4f5ce99dd03b7623c1b57f2f849d5ee806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:9fe3aa5829e9d3182998a1e06fdff4e334ddca045e96a2c9b5d162a977c666ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10168066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c875f434580033077c192a32b1d977f044279a8d835e5a97eead41d7195778`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 18:05:00 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 23 Mar 2022 18:05:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 23 Mar 2022 18:05:02 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 23 Mar 2022 18:05:03 GMT
EXPOSE 4222 8222
# Wed, 23 Mar 2022 18:05:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 18:05:03 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20aab72565ea910dd4302002ee7884ba75c62a05cfc50cb36f5f50c0b9bef6a`  
		Last Modified: Wed, 23 Mar 2022 18:05:30 GMT  
		Size: 7.4 MB (7354957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658077bd609b4d5d035e07d270607b59edb37aa8513038d447e44d8ca0a3d236`  
		Last Modified: Wed, 23 Mar 2022 18:05:29 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:da5c30c24c088f46f350a97493d89e0bd7e6e89f360cd72875c0bc7b45f9aa37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9495158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d87fc81f7ee48be7761b2e5903e28d795c026df3dab00a2e5fd8fcd6f7890e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 23 Mar 2022 15:49:35 GMT
ADD file:fd7f6da4a48df653ae6dd18e6d5959008daf5ce429845c974982dc7d213342d9 in / 
# Wed, 23 Mar 2022 15:49:35 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:44:07 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 23 Mar 2022 19:44:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 23 Mar 2022 19:44:13 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 23 Mar 2022 19:44:13 GMT
EXPOSE 4222 8222
# Wed, 23 Mar 2022 19:44:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 19:44:14 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:4e012d7cd81aa4570d9d209a75131b32f34a3533d5d449d23fd875513922588e`  
		Last Modified: Wed, 23 Mar 2022 15:51:07 GMT  
		Size: 2.6 MB (2624816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa88f1fb7bbc792265d0d3b6e07493e48c8721131a58114f6e59fe67494a4a1`  
		Last Modified: Wed, 23 Mar 2022 19:45:54 GMT  
		Size: 6.9 MB (6869923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5862a837be7f24421ba3719cede078392fe5d98759e5dcffc4edd342b7a916`  
		Last Modified: Wed, 23 Mar 2022 19:45:49 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:916ce7f967ce4c50901a7781eb6b2ad8e1b329b12a2f814758c93ac48dcf4429
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9289636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36f59fd5dbc054e5c6be9c9de6ff416d207cddd3199efee42180a5eb02d4c74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 21:59:53 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 23 Mar 2022 21:59:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 23 Mar 2022 21:59:58 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 23 Mar 2022 21:59:58 GMT
EXPOSE 4222 8222
# Wed, 23 Mar 2022 21:59:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 21:59:59 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d781846a82ba534e1e0c19b9eca25d87ca255f45226036da71ea2686242197b7`  
		Last Modified: Wed, 23 Mar 2022 22:01:44 GMT  
		Size: 6.9 MB (6862153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecea31a7006920f966542a97535211ed2d35fa9a09c89d67dbe4faf8753850e8`  
		Last Modified: Wed, 23 Mar 2022 22:01:40 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:9ad69a391a12ffb8de8d3c4cdecbce7433e9e7e4c4edfd42097538769aed3501
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9498217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a113f8c2aefe142234f29e4737965aec98053e8555f311c16cce8983eff6796`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 06:16:44 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Thu, 24 Mar 2022 06:16:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 24 Mar 2022 06:16:49 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 24 Mar 2022 06:16:49 GMT
EXPOSE 4222 8222
# Thu, 24 Mar 2022 06:16:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 06:16:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2811a7be31f1cee7d325c47fc0fbd3af7e6118677b764b4cf99c5528c69a4a0`  
		Last Modified: Thu, 24 Mar 2022 06:17:36 GMT  
		Size: 6.8 MB (6783075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd313c83b529290b935a875a11190713accb8a493139667c860d27090ba9cccf`  
		Last Modified: Thu, 24 Mar 2022 06:17:35 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.15`

```console
$ docker pull nats-streaming@sha256:91dac67ada020c90e09766553b35cc4f5ce99dd03b7623c1b57f2f849d5ee806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.15` - linux; amd64

```console
$ docker pull nats-streaming@sha256:9fe3aa5829e9d3182998a1e06fdff4e334ddca045e96a2c9b5d162a977c666ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10168066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c875f434580033077c192a32b1d977f044279a8d835e5a97eead41d7195778`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 18:05:00 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 23 Mar 2022 18:05:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 23 Mar 2022 18:05:02 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 23 Mar 2022 18:05:03 GMT
EXPOSE 4222 8222
# Wed, 23 Mar 2022 18:05:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 18:05:03 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20aab72565ea910dd4302002ee7884ba75c62a05cfc50cb36f5f50c0b9bef6a`  
		Last Modified: Wed, 23 Mar 2022 18:05:30 GMT  
		Size: 7.4 MB (7354957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658077bd609b4d5d035e07d270607b59edb37aa8513038d447e44d8ca0a3d236`  
		Last Modified: Wed, 23 Mar 2022 18:05:29 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.15` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:da5c30c24c088f46f350a97493d89e0bd7e6e89f360cd72875c0bc7b45f9aa37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9495158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d87fc81f7ee48be7761b2e5903e28d795c026df3dab00a2e5fd8fcd6f7890e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 23 Mar 2022 15:49:35 GMT
ADD file:fd7f6da4a48df653ae6dd18e6d5959008daf5ce429845c974982dc7d213342d9 in / 
# Wed, 23 Mar 2022 15:49:35 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:44:07 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 23 Mar 2022 19:44:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 23 Mar 2022 19:44:13 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 23 Mar 2022 19:44:13 GMT
EXPOSE 4222 8222
# Wed, 23 Mar 2022 19:44:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 19:44:14 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:4e012d7cd81aa4570d9d209a75131b32f34a3533d5d449d23fd875513922588e`  
		Last Modified: Wed, 23 Mar 2022 15:51:07 GMT  
		Size: 2.6 MB (2624816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa88f1fb7bbc792265d0d3b6e07493e48c8721131a58114f6e59fe67494a4a1`  
		Last Modified: Wed, 23 Mar 2022 19:45:54 GMT  
		Size: 6.9 MB (6869923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5862a837be7f24421ba3719cede078392fe5d98759e5dcffc4edd342b7a916`  
		Last Modified: Wed, 23 Mar 2022 19:45:49 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.15` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:916ce7f967ce4c50901a7781eb6b2ad8e1b329b12a2f814758c93ac48dcf4429
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9289636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36f59fd5dbc054e5c6be9c9de6ff416d207cddd3199efee42180a5eb02d4c74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 21:59:53 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 23 Mar 2022 21:59:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 23 Mar 2022 21:59:58 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 23 Mar 2022 21:59:58 GMT
EXPOSE 4222 8222
# Wed, 23 Mar 2022 21:59:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 21:59:59 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d781846a82ba534e1e0c19b9eca25d87ca255f45226036da71ea2686242197b7`  
		Last Modified: Wed, 23 Mar 2022 22:01:44 GMT  
		Size: 6.9 MB (6862153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecea31a7006920f966542a97535211ed2d35fa9a09c89d67dbe4faf8753850e8`  
		Last Modified: Wed, 23 Mar 2022 22:01:40 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:9ad69a391a12ffb8de8d3c4cdecbce7433e9e7e4c4edfd42097538769aed3501
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9498217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a113f8c2aefe142234f29e4737965aec98053e8555f311c16cce8983eff6796`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 06:16:44 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Thu, 24 Mar 2022 06:16:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 24 Mar 2022 06:16:49 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 24 Mar 2022 06:16:49 GMT
EXPOSE 4222 8222
# Thu, 24 Mar 2022 06:16:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 06:16:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2811a7be31f1cee7d325c47fc0fbd3af7e6118677b764b4cf99c5528c69a4a0`  
		Last Modified: Thu, 24 Mar 2022 06:17:36 GMT  
		Size: 6.8 MB (6783075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd313c83b529290b935a875a11190713accb8a493139667c860d27090ba9cccf`  
		Last Modified: Thu, 24 Mar 2022 06:17:35 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:9f8cedbf2e74e6679e9ab44848904ad048f1f9202d1dd72e203002605ba4a331
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
$ docker pull nats-streaming@sha256:eea355922fa3e329228180c171fe18939205a5828944f3c0ec23c0816eef7982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db0f18c883ff929dfaae3de15de5562de5be34b4a941aa05c6d52112b8e4c84`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:21:18 GMT
COPY file:6fcfe62a6cc0951979b80258fb3d207e13828d9234e227e1398cab40548702d7 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:21:18 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:21:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:64b920df5d588d78c6c317a08480a016eb7b6433705c1a3811a22e4e422e61d0`  
		Last Modified: Wed, 09 Mar 2022 23:22:00 GMT  
		Size: 7.1 MB (7081263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:36364386127a72bc130f59fb33c4119222fc6c671e33aea460f694025b82cd46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a965dc95f8a3e6631c5ca714f0aafd2acc1508a1f6d3298300876536949f11b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:49:55 GMT
COPY file:d62d923585419f7f9d263c0018d56cc159b1092bf7bae749223f339a514a81d9 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:49:56 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:49:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0b00cb53513f9c5bd72363c73ee281128c2cedd1d7653aa7278a2a6536c86a14`  
		Last Modified: Wed, 09 Mar 2022 23:51:50 GMT  
		Size: 6.6 MB (6597197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:c786255507edae1bf8167b3adbe962fa9c4ba18fd683462921df662c86e5f36f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6589565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb16b4f9d4a38de66adad0c74fd19049b37e96277e0cd459805b74bdf9474ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:29:51 GMT
COPY file:a5f2524f76b038dc99564d67f8cf6396171fe569b86b60aa9892eca88643b977 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:29:52 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:29:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:29:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:271fefa5e75537e471ab2e96d1b28b6614b2103db059b37f0e60bcc9b8ab40d8`  
		Last Modified: Wed, 09 Mar 2022 23:31:44 GMT  
		Size: 6.6 MB (6589565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bb6e16886863d8c84bc6427c4a45c43bca8f97adcddd602756dddc70fa826a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1fc4d49faf17ca5b2a9d116b2758a93de1af0ea5b526e23128bd6bbd00b5f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:41:07 GMT
COPY file:f47e5ea058ace7f6cdb8bca186dec2b15d364fff4ff67303ae8d2cfe38435050 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:41:07 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:41:08 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:41:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9e32cf3eae8c97676148171d71a3cc25149de87eecd89a137222b3b382cdf8f2`  
		Last Modified: Wed, 09 Mar 2022 23:42:13 GMT  
		Size: 6.5 MB (6510632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:bf5f4238170d36fdc3b99a4ab8acea5c5755564d3d97131d48d0730dee33bbdc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110249474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68219116c19a9ac4e2603cd23ba4233e15f3ab67ba4a4e9169a2c000801679cc`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:21:44 GMT
RUN cmd /S /C #(nop) COPY file:2bdfa73d50ba6f64f600945ecab061708a66086f5dd80ec5e00ad93c8bf3b8b6 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 23:21:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:47 GMT
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
	-	`sha256:3128e56b52a1dd66549cb7830a9bc9f9352ab11829fe936a4bd03858ac830160`  
		Last Modified: Wed, 09 Mar 2022 23:22:35 GMT  
		Size: 7.2 MB (7190251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c581f41ddfe2959d4092845a36fa343eaddd42a160cd818cbca5c31671bff`  
		Last Modified: Wed, 09 Mar 2022 23:22:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba79d16ae428589a386d36328db720a9ac0eb1abd0014da9992cb03cf4df1e`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c567d244b9f979dfa1c24fe471a72b7dc849619f91830d175ca5454f357a2eb`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:4f097bcee579937a2b55f7702298c9d0ccf44bc8fc2820b81ef02b1a9b146e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eea355922fa3e329228180c171fe18939205a5828944f3c0ec23c0816eef7982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db0f18c883ff929dfaae3de15de5562de5be34b4a941aa05c6d52112b8e4c84`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:21:18 GMT
COPY file:6fcfe62a6cc0951979b80258fb3d207e13828d9234e227e1398cab40548702d7 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:21:18 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:21:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:64b920df5d588d78c6c317a08480a016eb7b6433705c1a3811a22e4e422e61d0`  
		Last Modified: Wed, 09 Mar 2022 23:22:00 GMT  
		Size: 7.1 MB (7081263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:36364386127a72bc130f59fb33c4119222fc6c671e33aea460f694025b82cd46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a965dc95f8a3e6631c5ca714f0aafd2acc1508a1f6d3298300876536949f11b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:49:55 GMT
COPY file:d62d923585419f7f9d263c0018d56cc159b1092bf7bae749223f339a514a81d9 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:49:56 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:49:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0b00cb53513f9c5bd72363c73ee281128c2cedd1d7653aa7278a2a6536c86a14`  
		Last Modified: Wed, 09 Mar 2022 23:51:50 GMT  
		Size: 6.6 MB (6597197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:c786255507edae1bf8167b3adbe962fa9c4ba18fd683462921df662c86e5f36f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6589565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb16b4f9d4a38de66adad0c74fd19049b37e96277e0cd459805b74bdf9474ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:29:51 GMT
COPY file:a5f2524f76b038dc99564d67f8cf6396171fe569b86b60aa9892eca88643b977 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:29:52 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:29:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:29:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:271fefa5e75537e471ab2e96d1b28b6614b2103db059b37f0e60bcc9b8ab40d8`  
		Last Modified: Wed, 09 Mar 2022 23:31:44 GMT  
		Size: 6.6 MB (6589565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bb6e16886863d8c84bc6427c4a45c43bca8f97adcddd602756dddc70fa826a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1fc4d49faf17ca5b2a9d116b2758a93de1af0ea5b526e23128bd6bbd00b5f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:41:07 GMT
COPY file:f47e5ea058ace7f6cdb8bca186dec2b15d364fff4ff67303ae8d2cfe38435050 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:41:07 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:41:08 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:41:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9e32cf3eae8c97676148171d71a3cc25149de87eecd89a137222b3b382cdf8f2`  
		Last Modified: Wed, 09 Mar 2022 23:42:13 GMT  
		Size: 6.5 MB (6510632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:427167cf68f6cc7da882af2fe3a4b7c8089d370a60bdfb20d1c2f432095618d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:bf5f4238170d36fdc3b99a4ab8acea5c5755564d3d97131d48d0730dee33bbdc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110249474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68219116c19a9ac4e2603cd23ba4233e15f3ab67ba4a4e9169a2c000801679cc`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:21:44 GMT
RUN cmd /S /C #(nop) COPY file:2bdfa73d50ba6f64f600945ecab061708a66086f5dd80ec5e00ad93c8bf3b8b6 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 23:21:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:47 GMT
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
	-	`sha256:3128e56b52a1dd66549cb7830a9bc9f9352ab11829fe936a4bd03858ac830160`  
		Last Modified: Wed, 09 Mar 2022 23:22:35 GMT  
		Size: 7.2 MB (7190251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c581f41ddfe2959d4092845a36fa343eaddd42a160cd818cbca5c31671bff`  
		Last Modified: Wed, 09 Mar 2022 23:22:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba79d16ae428589a386d36328db720a9ac0eb1abd0014da9992cb03cf4df1e`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c567d244b9f979dfa1c24fe471a72b7dc849619f91830d175ca5454f357a2eb`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:427167cf68f6cc7da882af2fe3a4b7c8089d370a60bdfb20d1c2f432095618d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:bf5f4238170d36fdc3b99a4ab8acea5c5755564d3d97131d48d0730dee33bbdc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110249474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68219116c19a9ac4e2603cd23ba4233e15f3ab67ba4a4e9169a2c000801679cc`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:21:44 GMT
RUN cmd /S /C #(nop) COPY file:2bdfa73d50ba6f64f600945ecab061708a66086f5dd80ec5e00ad93c8bf3b8b6 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 23:21:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:47 GMT
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
	-	`sha256:3128e56b52a1dd66549cb7830a9bc9f9352ab11829fe936a4bd03858ac830160`  
		Last Modified: Wed, 09 Mar 2022 23:22:35 GMT  
		Size: 7.2 MB (7190251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c581f41ddfe2959d4092845a36fa343eaddd42a160cd818cbca5c31671bff`  
		Last Modified: Wed, 09 Mar 2022 23:22:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba79d16ae428589a386d36328db720a9ac0eb1abd0014da9992cb03cf4df1e`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c567d244b9f979dfa1c24fe471a72b7dc849619f91830d175ca5454f357a2eb`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:4f097bcee579937a2b55f7702298c9d0ccf44bc8fc2820b81ef02b1a9b146e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eea355922fa3e329228180c171fe18939205a5828944f3c0ec23c0816eef7982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db0f18c883ff929dfaae3de15de5562de5be34b4a941aa05c6d52112b8e4c84`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:21:18 GMT
COPY file:6fcfe62a6cc0951979b80258fb3d207e13828d9234e227e1398cab40548702d7 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:21:18 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:21:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:64b920df5d588d78c6c317a08480a016eb7b6433705c1a3811a22e4e422e61d0`  
		Last Modified: Wed, 09 Mar 2022 23:22:00 GMT  
		Size: 7.1 MB (7081263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:36364386127a72bc130f59fb33c4119222fc6c671e33aea460f694025b82cd46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a965dc95f8a3e6631c5ca714f0aafd2acc1508a1f6d3298300876536949f11b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:49:55 GMT
COPY file:d62d923585419f7f9d263c0018d56cc159b1092bf7bae749223f339a514a81d9 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:49:56 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:49:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0b00cb53513f9c5bd72363c73ee281128c2cedd1d7653aa7278a2a6536c86a14`  
		Last Modified: Wed, 09 Mar 2022 23:51:50 GMT  
		Size: 6.6 MB (6597197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:c786255507edae1bf8167b3adbe962fa9c4ba18fd683462921df662c86e5f36f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6589565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb16b4f9d4a38de66adad0c74fd19049b37e96277e0cd459805b74bdf9474ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:29:51 GMT
COPY file:a5f2524f76b038dc99564d67f8cf6396171fe569b86b60aa9892eca88643b977 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:29:52 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:29:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:29:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:271fefa5e75537e471ab2e96d1b28b6614b2103db059b37f0e60bcc9b8ab40d8`  
		Last Modified: Wed, 09 Mar 2022 23:31:44 GMT  
		Size: 6.6 MB (6589565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bb6e16886863d8c84bc6427c4a45c43bca8f97adcddd602756dddc70fa826a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1fc4d49faf17ca5b2a9d116b2758a93de1af0ea5b526e23128bd6bbd00b5f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:41:07 GMT
COPY file:f47e5ea058ace7f6cdb8bca186dec2b15d364fff4ff67303ae8d2cfe38435050 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:41:07 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:41:08 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:41:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9e32cf3eae8c97676148171d71a3cc25149de87eecd89a137222b3b382cdf8f2`  
		Last Modified: Wed, 09 Mar 2022 23:42:13 GMT  
		Size: 6.5 MB (6510632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:112510afc4add9efb62621bbcbd4c03a62c4efa7bebfa2854d896a3b81b4822b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:38aa3744b326ea3530932f9ae38c5884a7cc4f4e5e71b77f330b5634d79fa79a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723329559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5125257a9aa0beaab36a017e9f82750b3aac24f4719374d6cc8e339fc187cdd`
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
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.3/nats-streaming-server-v0.24.3-windows-amd64.zip
# Wed, 09 Mar 2022 23:18:48 GMT
ENV NATS_STREAMING_SERVER_SHASUM=7473bfa7efd734ca6984907bc9586260031cca926883b468b4752557ecefaff0
# Wed, 09 Mar 2022 23:19:49 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:21:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:21:28 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:29 GMT
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
	-	`sha256:3b1aac6ec834525c931dc81bbbb6d32996b82fd755a3bd625af11f40b8fc66bb`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d303e56675a80a6fa4eef8ef31d6f93742709f41058dcf6e36b8ba6d71a466f8`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8122e4b6aba607bd3d7b17a847d8ab75da7d7cb7a2bbb035e4a31cfc1b7ce6`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393372fa0a20ba2589a43d177f33a0360245be974d231efaa7ab980bc342b574`  
		Last Modified: Wed, 09 Mar 2022 23:22:13 GMT  
		Size: 349.0 KB (348988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3cf158dc37e43f4d84e520f088e32b2851abbf4a70af92161ab5e0d7e3ecbd`  
		Last Modified: Wed, 09 Mar 2022 23:22:20 GMT  
		Size: 7.5 MB (7516588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fff4072b17e75a66709617708b8b9263dabe4a12c4e0a594fb52e058977fa83`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de86f56dd22fbee61ed7161f763ba9de61d7cbf9623b85a879723ea5670f6e20`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04add3ff0ef25a1f32aab83f90a95cffab3d4b55afd3eb376a861b36094a0b0`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:112510afc4add9efb62621bbcbd4c03a62c4efa7bebfa2854d896a3b81b4822b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:38aa3744b326ea3530932f9ae38c5884a7cc4f4e5e71b77f330b5634d79fa79a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723329559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5125257a9aa0beaab36a017e9f82750b3aac24f4719374d6cc8e339fc187cdd`
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
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.3/nats-streaming-server-v0.24.3-windows-amd64.zip
# Wed, 09 Mar 2022 23:18:48 GMT
ENV NATS_STREAMING_SERVER_SHASUM=7473bfa7efd734ca6984907bc9586260031cca926883b468b4752557ecefaff0
# Wed, 09 Mar 2022 23:19:49 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:21:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:21:28 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:29 GMT
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
	-	`sha256:3b1aac6ec834525c931dc81bbbb6d32996b82fd755a3bd625af11f40b8fc66bb`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d303e56675a80a6fa4eef8ef31d6f93742709f41058dcf6e36b8ba6d71a466f8`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8122e4b6aba607bd3d7b17a847d8ab75da7d7cb7a2bbb035e4a31cfc1b7ce6`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393372fa0a20ba2589a43d177f33a0360245be974d231efaa7ab980bc342b574`  
		Last Modified: Wed, 09 Mar 2022 23:22:13 GMT  
		Size: 349.0 KB (348988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3cf158dc37e43f4d84e520f088e32b2851abbf4a70af92161ab5e0d7e3ecbd`  
		Last Modified: Wed, 09 Mar 2022 23:22:20 GMT  
		Size: 7.5 MB (7516588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fff4072b17e75a66709617708b8b9263dabe4a12c4e0a594fb52e058977fa83`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de86f56dd22fbee61ed7161f763ba9de61d7cbf9623b85a879723ea5670f6e20`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04add3ff0ef25a1f32aab83f90a95cffab3d4b55afd3eb376a861b36094a0b0`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

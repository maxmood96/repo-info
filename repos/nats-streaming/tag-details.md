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
-	[`nats-streaming:0.21.2`](#nats-streaming0212)
-	[`nats-streaming:0.21.2-alpine`](#nats-streaming0212-alpine)
-	[`nats-streaming:0.21.2-alpine3.13`](#nats-streaming0212-alpine313)
-	[`nats-streaming:0.21.2-linux`](#nats-streaming0212-linux)
-	[`nats-streaming:0.21.2-nanoserver`](#nats-streaming0212-nanoserver)
-	[`nats-streaming:0.21.2-nanoserver-1809`](#nats-streaming0212-nanoserver-1809)
-	[`nats-streaming:0.21.2-scratch`](#nats-streaming0212-scratch)
-	[`nats-streaming:0.21.2-windowsservercore`](#nats-streaming0212-windowsservercore)
-	[`nats-streaming:0.21.2-windowsservercore-1809`](#nats-streaming0212-windowsservercore-1809)
-	[`nats-streaming:0.21.2-windowsservercore-ltsc2016`](#nats-streaming0212-windowsservercore-ltsc2016)
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
$ docker pull nats-streaming@sha256:abea5a41eb4c8bf97ba0948419a58554540102007fc5b4495ef516916188809d
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
$ docker pull nats-streaming@sha256:883d4d7a47db4d1c911cf0c23dad30011b46727297d1158bede3d833455a49e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1e123176c313a4b94f8c0fdf6cac9abdd85a1bd6edf3f7cc6e7ed61852d19a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:25:32 GMT
COPY file:aefc6cbeadb611214d28b81a278a791c774a4bbc969528522aae7abe7c4e2784 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:25:32 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:25:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:25:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:087a668f89c4000c166ca5a16dd40fee8206986ce9b47a92d224b78214f3db5c`  
		Last Modified: Fri, 16 Apr 2021 21:26:16 GMT  
		Size: 5.7 MB (5680535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9dc93ca8dad040be30fe0949d19f04a6b1775750838d70d2fb12f3aa9f40b4f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba356cbd8fdcd90e529d00104791d07c50c101937487a0b8647b06226bfdef9a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:02:53 GMT
COPY file:c58b6e2180eb9d24d595f35c2205c2d9b4f80315beb0f166e20a7340cf3f2536 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:03:00 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:03:04 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:03:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3542c02ee947256ff50165b76289b4dd90e7c82bfb7b0b983b4d66d4b1128e9a`  
		Last Modified: Fri, 16 Apr 2021 21:03:44 GMT  
		Size: 5.3 MB (5253054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:10f5838646402cebd5c40f8f02991aad0ca3767b13b3024054e5e04026d3c778
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409bfb98a0a11b06fb4c8a044cda742270c21f5082ef80b63e7893cb4ce2f9c3`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:00:05 GMT
COPY file:7ad2a856b4d75bdc56fbd35738819610cc3c26111897fc883c3af7db16d4fa87 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:00:07 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:00:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:00:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:76bf01e9a89a0de09d5ab72dd4ec7e4c9f561a27756ceb73bf0365f192de2d18`  
		Last Modified: Fri, 16 Apr 2021 21:01:13 GMT  
		Size: 5.2 MB (5246280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:3bf4856546fa4657b125293b8ed701a22dd3861cd532a14281d7726210c726c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4acb30c8790d9ef8af675772eda5d9f3903a662d29132ef140463453eeb717`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:48:04 GMT
COPY file:b02a357b6e9250e52099dcc91c6a9a78682a192bd0850fabc93d5cdacb6fcfb3 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:48:05 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:48:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:48:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:fe1641db2bf227918d02728a21bd3b53989018d9c796246d3b96fcbbf75ded32`  
		Last Modified: Fri, 16 Apr 2021 21:48:50 GMT  
		Size: 5.2 MB (5170831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:61bce4686b4cb6f2e1e9563643ef604ff9e6db78b3ec8017bbbb244bba89c69c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107156045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cb251e2361dacf7f07021ad3cd15d4a21877b08d66b75ea5ecd3fc0f19c7f7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Apr 2021 21:17:55 GMT
RUN cmd /S /C #(nop) COPY file:adacf7e54ef5a782ae37764b59883ad6a48b32c36c576816360f94cba82ba458 in C:\nats-streaming-server.exe 
# Fri, 16 Apr 2021 21:17:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:17:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:17:59 GMT
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
	-	`sha256:2ab6d20feb9c03e1c8e6983c39be671e946eb6994a26c435c813829e681dbe57`  
		Last Modified: Fri, 16 Apr 2021 21:24:02 GMT  
		Size: 5.8 MB (5811210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ec8e35cf7e38f49d059085e4aab0b4e8df8689989934d6ca20c6b406c06bed`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1354e00c20faa27d7a6d7931702d4005d12c09da6139424792bb915725783e2b`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df10c9c723da873a08ebe210f4272cbdc0b9d047c4898a7e721e957bab6465e`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-alpine`

```console
$ docker pull nats-streaming@sha256:d204ac6b58553c9632e9797984adcace87b6539d257754f1d5bdf5e4a2a8d72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:402dacbb78f9bf5e9ea249c730f7905caa085ca665782e1cb4c6e7004f597689
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8774780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7ad70b17b46627026163460cce06023868f24d36a50cd9c261e7c6cba86e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:25:11 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:25:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:25:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:25:15 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:25:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:25:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269577e93d92e9e558c3607d8b5e74978c939fc643895de15fd70ef06b811323`  
		Last Modified: Fri, 16 Apr 2021 21:25:54 GMT  
		Size: 6.0 MB (5962389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fa1ca69a5dc5f7aecbfca382d45ab09423bb9d103c6567abc37af7b842073a`  
		Last Modified: Fri, 16 Apr 2021 21:25:54 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:e03de3640ce68bbb19cd2b5e8dc2a1454fbba1b369a4c236f09b6630197b6fa0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8156933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a345ef8cbbe68103787d05c9dbd22742cc95b726776cbf30298c3ca98487b63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:02:04 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:02:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:02:26 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:02:27 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:02:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:02:29 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e538f4430325ed9ef756e0e521a859c9466b9b7a45a8662e4f29f1ec5f8c3a7d`  
		Last Modified: Fri, 16 Apr 2021 21:03:32 GMT  
		Size: 5.5 MB (5534381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc165822006c8e13ee1ee6756545e0f021a059f974288d6c953febdeea6a83d3`  
		Last Modified: Fri, 16 Apr 2021 21:03:30 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ea133d32e6510a0d1822a1ea1cfcca41e3cbd747a3d69491aee62319937e892d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc13824ee86fb9d0c1609b885378ba366f3883903bfe990fb27464bce6c02686`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 20:59:08 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 20:59:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 20:59:13 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 20:59:14 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 20:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 20:59:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b86c52fd84fa988d60547be09b11af6fcac2dffa6b340e92b776a0fc89a298`  
		Last Modified: Fri, 16 Apr 2021 21:00:42 GMT  
		Size: 5.5 MB (5527039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b279e3ce6e5cfc3967a4acbf6dc2563f1715817b059d6f320b53cbc21b74e1`  
		Last Modified: Fri, 16 Apr 2021 21:00:40 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:febf36c660fc36bcbf3da9945707f541e81665b0d21a0f1c6c8220543697a757
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8165113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd79dce90e049636e2513bd55a0b3178cb59197d3dfc53cbed474dbbd5de0f1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:44:03 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:44:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:44:08 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:44:09 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:44:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:44:10 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a1a4dae3b1b310f0231f28f4db383d7605066343274881c5be1300ebe64f51`  
		Last Modified: Fri, 16 Apr 2021 21:48:37 GMT  
		Size: 5.5 MB (5452665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a06774842e75925d8884fc1ea5a3e83c2c8054d4fb443ad11021c5866b0617`  
		Last Modified: Fri, 16 Apr 2021 21:48:36 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-alpine3.13`

```console
$ docker pull nats-streaming@sha256:d204ac6b58553c9632e9797984adcace87b6539d257754f1d5bdf5e4a2a8d72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21-alpine3.13` - linux; amd64

```console
$ docker pull nats-streaming@sha256:402dacbb78f9bf5e9ea249c730f7905caa085ca665782e1cb4c6e7004f597689
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8774780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7ad70b17b46627026163460cce06023868f24d36a50cd9c261e7c6cba86e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:25:11 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:25:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:25:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:25:15 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:25:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:25:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269577e93d92e9e558c3607d8b5e74978c939fc643895de15fd70ef06b811323`  
		Last Modified: Fri, 16 Apr 2021 21:25:54 GMT  
		Size: 6.0 MB (5962389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fa1ca69a5dc5f7aecbfca382d45ab09423bb9d103c6567abc37af7b842073a`  
		Last Modified: Fri, 16 Apr 2021 21:25:54 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-alpine3.13` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:e03de3640ce68bbb19cd2b5e8dc2a1454fbba1b369a4c236f09b6630197b6fa0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8156933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a345ef8cbbe68103787d05c9dbd22742cc95b726776cbf30298c3ca98487b63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:02:04 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:02:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:02:26 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:02:27 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:02:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:02:29 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e538f4430325ed9ef756e0e521a859c9466b9b7a45a8662e4f29f1ec5f8c3a7d`  
		Last Modified: Fri, 16 Apr 2021 21:03:32 GMT  
		Size: 5.5 MB (5534381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc165822006c8e13ee1ee6756545e0f021a059f974288d6c953febdeea6a83d3`  
		Last Modified: Fri, 16 Apr 2021 21:03:30 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-alpine3.13` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ea133d32e6510a0d1822a1ea1cfcca41e3cbd747a3d69491aee62319937e892d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc13824ee86fb9d0c1609b885378ba366f3883903bfe990fb27464bce6c02686`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 20:59:08 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 20:59:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 20:59:13 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 20:59:14 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 20:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 20:59:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b86c52fd84fa988d60547be09b11af6fcac2dffa6b340e92b776a0fc89a298`  
		Last Modified: Fri, 16 Apr 2021 21:00:42 GMT  
		Size: 5.5 MB (5527039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b279e3ce6e5cfc3967a4acbf6dc2563f1715817b059d6f320b53cbc21b74e1`  
		Last Modified: Fri, 16 Apr 2021 21:00:40 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:febf36c660fc36bcbf3da9945707f541e81665b0d21a0f1c6c8220543697a757
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8165113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd79dce90e049636e2513bd55a0b3178cb59197d3dfc53cbed474dbbd5de0f1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:44:03 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:44:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:44:08 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:44:09 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:44:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:44:10 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a1a4dae3b1b310f0231f28f4db383d7605066343274881c5be1300ebe64f51`  
		Last Modified: Fri, 16 Apr 2021 21:48:37 GMT  
		Size: 5.5 MB (5452665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a06774842e75925d8884fc1ea5a3e83c2c8054d4fb443ad11021c5866b0617`  
		Last Modified: Fri, 16 Apr 2021 21:48:36 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-linux`

```console
$ docker pull nats-streaming@sha256:2bf298093b69248cb6e82aa7c64d50c1a45480ad23a8ced79a5ddf588ee69102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:883d4d7a47db4d1c911cf0c23dad30011b46727297d1158bede3d833455a49e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1e123176c313a4b94f8c0fdf6cac9abdd85a1bd6edf3f7cc6e7ed61852d19a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:25:32 GMT
COPY file:aefc6cbeadb611214d28b81a278a791c774a4bbc969528522aae7abe7c4e2784 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:25:32 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:25:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:25:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:087a668f89c4000c166ca5a16dd40fee8206986ce9b47a92d224b78214f3db5c`  
		Last Modified: Fri, 16 Apr 2021 21:26:16 GMT  
		Size: 5.7 MB (5680535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9dc93ca8dad040be30fe0949d19f04a6b1775750838d70d2fb12f3aa9f40b4f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba356cbd8fdcd90e529d00104791d07c50c101937487a0b8647b06226bfdef9a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:02:53 GMT
COPY file:c58b6e2180eb9d24d595f35c2205c2d9b4f80315beb0f166e20a7340cf3f2536 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:03:00 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:03:04 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:03:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3542c02ee947256ff50165b76289b4dd90e7c82bfb7b0b983b4d66d4b1128e9a`  
		Last Modified: Fri, 16 Apr 2021 21:03:44 GMT  
		Size: 5.3 MB (5253054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:10f5838646402cebd5c40f8f02991aad0ca3767b13b3024054e5e04026d3c778
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409bfb98a0a11b06fb4c8a044cda742270c21f5082ef80b63e7893cb4ce2f9c3`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:00:05 GMT
COPY file:7ad2a856b4d75bdc56fbd35738819610cc3c26111897fc883c3af7db16d4fa87 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:00:07 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:00:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:00:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:76bf01e9a89a0de09d5ab72dd4ec7e4c9f561a27756ceb73bf0365f192de2d18`  
		Last Modified: Fri, 16 Apr 2021 21:01:13 GMT  
		Size: 5.2 MB (5246280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:3bf4856546fa4657b125293b8ed701a22dd3861cd532a14281d7726210c726c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4acb30c8790d9ef8af675772eda5d9f3903a662d29132ef140463453eeb717`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:48:04 GMT
COPY file:b02a357b6e9250e52099dcc91c6a9a78682a192bd0850fabc93d5cdacb6fcfb3 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:48:05 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:48:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:48:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:fe1641db2bf227918d02728a21bd3b53989018d9c796246d3b96fcbbf75ded32`  
		Last Modified: Fri, 16 Apr 2021 21:48:50 GMT  
		Size: 5.2 MB (5170831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-nanoserver`

```console
$ docker pull nats-streaming@sha256:cba11565eb636b9f97847e3feefb1c750ed9f20f17906263428c122cd788056f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:0.21-nanoserver` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:61bce4686b4cb6f2e1e9563643ef604ff9e6db78b3ec8017bbbb244bba89c69c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107156045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cb251e2361dacf7f07021ad3cd15d4a21877b08d66b75ea5ecd3fc0f19c7f7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Apr 2021 21:17:55 GMT
RUN cmd /S /C #(nop) COPY file:adacf7e54ef5a782ae37764b59883ad6a48b32c36c576816360f94cba82ba458 in C:\nats-streaming-server.exe 
# Fri, 16 Apr 2021 21:17:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:17:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:17:59 GMT
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
	-	`sha256:2ab6d20feb9c03e1c8e6983c39be671e946eb6994a26c435c813829e681dbe57`  
		Last Modified: Fri, 16 Apr 2021 21:24:02 GMT  
		Size: 5.8 MB (5811210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ec8e35cf7e38f49d059085e4aab0b4e8df8689989934d6ca20c6b406c06bed`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1354e00c20faa27d7a6d7931702d4005d12c09da6139424792bb915725783e2b`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df10c9c723da873a08ebe210f4272cbdc0b9d047c4898a7e721e957bab6465e`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:cba11565eb636b9f97847e3feefb1c750ed9f20f17906263428c122cd788056f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:0.21-nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:61bce4686b4cb6f2e1e9563643ef604ff9e6db78b3ec8017bbbb244bba89c69c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107156045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cb251e2361dacf7f07021ad3cd15d4a21877b08d66b75ea5ecd3fc0f19c7f7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Apr 2021 21:17:55 GMT
RUN cmd /S /C #(nop) COPY file:adacf7e54ef5a782ae37764b59883ad6a48b32c36c576816360f94cba82ba458 in C:\nats-streaming-server.exe 
# Fri, 16 Apr 2021 21:17:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:17:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:17:59 GMT
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
	-	`sha256:2ab6d20feb9c03e1c8e6983c39be671e946eb6994a26c435c813829e681dbe57`  
		Last Modified: Fri, 16 Apr 2021 21:24:02 GMT  
		Size: 5.8 MB (5811210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ec8e35cf7e38f49d059085e4aab0b4e8df8689989934d6ca20c6b406c06bed`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1354e00c20faa27d7a6d7931702d4005d12c09da6139424792bb915725783e2b`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df10c9c723da873a08ebe210f4272cbdc0b9d047c4898a7e721e957bab6465e`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-scratch`

```console
$ docker pull nats-streaming@sha256:2bf298093b69248cb6e82aa7c64d50c1a45480ad23a8ced79a5ddf588ee69102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:883d4d7a47db4d1c911cf0c23dad30011b46727297d1158bede3d833455a49e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1e123176c313a4b94f8c0fdf6cac9abdd85a1bd6edf3f7cc6e7ed61852d19a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:25:32 GMT
COPY file:aefc6cbeadb611214d28b81a278a791c774a4bbc969528522aae7abe7c4e2784 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:25:32 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:25:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:25:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:087a668f89c4000c166ca5a16dd40fee8206986ce9b47a92d224b78214f3db5c`  
		Last Modified: Fri, 16 Apr 2021 21:26:16 GMT  
		Size: 5.7 MB (5680535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9dc93ca8dad040be30fe0949d19f04a6b1775750838d70d2fb12f3aa9f40b4f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba356cbd8fdcd90e529d00104791d07c50c101937487a0b8647b06226bfdef9a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:02:53 GMT
COPY file:c58b6e2180eb9d24d595f35c2205c2d9b4f80315beb0f166e20a7340cf3f2536 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:03:00 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:03:04 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:03:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3542c02ee947256ff50165b76289b4dd90e7c82bfb7b0b983b4d66d4b1128e9a`  
		Last Modified: Fri, 16 Apr 2021 21:03:44 GMT  
		Size: 5.3 MB (5253054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:10f5838646402cebd5c40f8f02991aad0ca3767b13b3024054e5e04026d3c778
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409bfb98a0a11b06fb4c8a044cda742270c21f5082ef80b63e7893cb4ce2f9c3`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:00:05 GMT
COPY file:7ad2a856b4d75bdc56fbd35738819610cc3c26111897fc883c3af7db16d4fa87 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:00:07 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:00:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:00:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:76bf01e9a89a0de09d5ab72dd4ec7e4c9f561a27756ceb73bf0365f192de2d18`  
		Last Modified: Fri, 16 Apr 2021 21:01:13 GMT  
		Size: 5.2 MB (5246280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:3bf4856546fa4657b125293b8ed701a22dd3861cd532a14281d7726210c726c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4acb30c8790d9ef8af675772eda5d9f3903a662d29132ef140463453eeb717`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:48:04 GMT
COPY file:b02a357b6e9250e52099dcc91c6a9a78682a192bd0850fabc93d5cdacb6fcfb3 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:48:05 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:48:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:48:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:fe1641db2bf227918d02728a21bd3b53989018d9c796246d3b96fcbbf75ded32`  
		Last Modified: Fri, 16 Apr 2021 21:48:50 GMT  
		Size: 5.2 MB (5170831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-windowsservercore`

```console
$ docker pull nats-streaming@sha256:98b9617ca151407afacb114ff81aff503c2ea4577b96209c8c5676361ca9557a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `nats-streaming:0.21-windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:46a11494d76fc259b7a9f8a0c27873460bf913594ca6f05a299234525b15094a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2485739262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b666c7480c5c11601af2df96a1489969fe78538e0945930ef51de2fe96c389a1`
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
# Fri, 16 Apr 2021 21:15:14 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:15:14 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.2/nats-streaming-server-v0.21.2-windows-amd64.zip
# Fri, 16 Apr 2021 21:15:15 GMT
ENV GIT_DOWNLOAD_SHA256=5d4367fea29116fcd70c364c8e808d6bc8e74214effbde83dd9548455bd06df2
# Fri, 16 Apr 2021 21:16:09 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Apr 2021 21:17:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 16 Apr 2021 21:17:43 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:17:44 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:17:45 GMT
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
	-	`sha256:63694c9279bb4c7122e4c15326493b2ffac8c6df264b45b2bc1542aa4763c785`  
		Last Modified: Fri, 16 Apr 2021 21:23:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7109d9070f9055006a72b16519d93e1ff1ba1e5421bc264c2197ef4e6a3edb0d`  
		Last Modified: Fri, 16 Apr 2021 21:23:46 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6023c32ca8ac978165d5409ef9087006ee445e04c5b93d707b0fb484faa1b3c3`  
		Last Modified: Fri, 16 Apr 2021 21:23:46 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc9c54c2bcc706204b7d4feaf8b3e66c9efaab5f43babd81045e31c318bc25c`  
		Last Modified: Fri, 16 Apr 2021 21:23:45 GMT  
		Size: 5.1 MB (5096185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208b0279ea22aad1e519ba1f2f927cf4598bdfbddf3a33b2c14e6356331b2f48`  
		Last Modified: Fri, 16 Apr 2021 21:23:47 GMT  
		Size: 10.9 MB (10877752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d04869441fc428a1ea7711da8ca9b0c8b6bdee6622751b6c44d98633fc9ded`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a25017dc98d8b32009d962f73fcf54adb74971347a78fb4f94b35da8c92179`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cc3678ca9e1a8f67aca7150e64f25b9f0a28cf4c07ecdaae86095d9fe09523`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21-windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull nats-streaming@sha256:2855b5d29b6f04637f9552d71cda49dcb3dc4d542d7ed205bfe8d97be393545f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816479551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbec025bd002885ef7f70a46dec4fe05d03313f3821b9d4f905ebe807c1f3f6`
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
# Fri, 16 Apr 2021 21:18:08 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:18:09 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.2/nats-streaming-server-v0.21.2-windows-amd64.zip
# Fri, 16 Apr 2021 21:18:10 GMT
ENV GIT_DOWNLOAD_SHA256=5d4367fea29116fcd70c364c8e808d6bc8e74214effbde83dd9548455bd06df2
# Fri, 16 Apr 2021 21:20:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Apr 2021 21:22:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 16 Apr 2021 21:22:44 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:22:46 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:22:47 GMT
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
	-	`sha256:bb633935c8262a169f8ce0f1c047198f3f981cf5315ebbdfb8aa7ba7e7d72bb5`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65576d29a65010c1357bcc65b8be2b2b1fdc9c4e43886372b8906fe1e108992b`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5de8efb2c9f3c99d2381a169ff4f442ca3b804a8a822584c54fa8673ef2f18`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a185c587f57ffd591baafd272bad6bdd76759232c6fb38c93ae2f951ef672d58`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 5.7 MB (5660316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58dea9968ebcd0bab739582d83245d50a4866d2bcbd2153d5dfa856e285fc810`  
		Last Modified: Fri, 16 Apr 2021 21:24:20 GMT  
		Size: 15.9 MB (15924139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d5db835b40ab66c30271634885e8fae5e1ba4c40c486a8cea2f021882824f8`  
		Last Modified: Fri, 16 Apr 2021 21:24:15 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2a1a71345bf095f4133c7fad40e22ecde64b60261ca6035b69111680d7f576`  
		Last Modified: Fri, 16 Apr 2021 21:24:16 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffed13d909a2d6c0c79217cee06b023d0e1bbe267704ea88f3d26b5b3fd6b5e9`  
		Last Modified: Fri, 16 Apr 2021 21:24:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:d68f4e2295d5a9c5bed66b3866e3d4ae3bc8af5f4e73fdcf584c03f4e1bbb82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:0.21-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:46a11494d76fc259b7a9f8a0c27873460bf913594ca6f05a299234525b15094a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2485739262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b666c7480c5c11601af2df96a1489969fe78538e0945930ef51de2fe96c389a1`
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
# Fri, 16 Apr 2021 21:15:14 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:15:14 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.2/nats-streaming-server-v0.21.2-windows-amd64.zip
# Fri, 16 Apr 2021 21:15:15 GMT
ENV GIT_DOWNLOAD_SHA256=5d4367fea29116fcd70c364c8e808d6bc8e74214effbde83dd9548455bd06df2
# Fri, 16 Apr 2021 21:16:09 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Apr 2021 21:17:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 16 Apr 2021 21:17:43 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:17:44 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:17:45 GMT
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
	-	`sha256:63694c9279bb4c7122e4c15326493b2ffac8c6df264b45b2bc1542aa4763c785`  
		Last Modified: Fri, 16 Apr 2021 21:23:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7109d9070f9055006a72b16519d93e1ff1ba1e5421bc264c2197ef4e6a3edb0d`  
		Last Modified: Fri, 16 Apr 2021 21:23:46 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6023c32ca8ac978165d5409ef9087006ee445e04c5b93d707b0fb484faa1b3c3`  
		Last Modified: Fri, 16 Apr 2021 21:23:46 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc9c54c2bcc706204b7d4feaf8b3e66c9efaab5f43babd81045e31c318bc25c`  
		Last Modified: Fri, 16 Apr 2021 21:23:45 GMT  
		Size: 5.1 MB (5096185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208b0279ea22aad1e519ba1f2f927cf4598bdfbddf3a33b2c14e6356331b2f48`  
		Last Modified: Fri, 16 Apr 2021 21:23:47 GMT  
		Size: 10.9 MB (10877752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d04869441fc428a1ea7711da8ca9b0c8b6bdee6622751b6c44d98633fc9ded`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a25017dc98d8b32009d962f73fcf54adb74971347a78fb4f94b35da8c92179`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cc3678ca9e1a8f67aca7150e64f25b9f0a28cf4c07ecdaae86095d9fe09523`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21-windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:aefa3b0d0213921ea947351c14fb151622e1e9cb7f3d6dd50ab2b3f35db87859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `nats-streaming:0.21-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull nats-streaming@sha256:2855b5d29b6f04637f9552d71cda49dcb3dc4d542d7ed205bfe8d97be393545f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816479551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbec025bd002885ef7f70a46dec4fe05d03313f3821b9d4f905ebe807c1f3f6`
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
# Fri, 16 Apr 2021 21:18:08 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:18:09 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.2/nats-streaming-server-v0.21.2-windows-amd64.zip
# Fri, 16 Apr 2021 21:18:10 GMT
ENV GIT_DOWNLOAD_SHA256=5d4367fea29116fcd70c364c8e808d6bc8e74214effbde83dd9548455bd06df2
# Fri, 16 Apr 2021 21:20:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Apr 2021 21:22:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 16 Apr 2021 21:22:44 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:22:46 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:22:47 GMT
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
	-	`sha256:bb633935c8262a169f8ce0f1c047198f3f981cf5315ebbdfb8aa7ba7e7d72bb5`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65576d29a65010c1357bcc65b8be2b2b1fdc9c4e43886372b8906fe1e108992b`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5de8efb2c9f3c99d2381a169ff4f442ca3b804a8a822584c54fa8673ef2f18`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a185c587f57ffd591baafd272bad6bdd76759232c6fb38c93ae2f951ef672d58`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 5.7 MB (5660316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58dea9968ebcd0bab739582d83245d50a4866d2bcbd2153d5dfa856e285fc810`  
		Last Modified: Fri, 16 Apr 2021 21:24:20 GMT  
		Size: 15.9 MB (15924139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d5db835b40ab66c30271634885e8fae5e1ba4c40c486a8cea2f021882824f8`  
		Last Modified: Fri, 16 Apr 2021 21:24:15 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2a1a71345bf095f4133c7fad40e22ecde64b60261ca6035b69111680d7f576`  
		Last Modified: Fri, 16 Apr 2021 21:24:16 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffed13d909a2d6c0c79217cee06b023d0e1bbe267704ea88f3d26b5b3fd6b5e9`  
		Last Modified: Fri, 16 Apr 2021 21:24:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.2`

```console
$ docker pull nats-streaming@sha256:abea5a41eb4c8bf97ba0948419a58554540102007fc5b4495ef516916188809d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:0.21.2` - linux; amd64

```console
$ docker pull nats-streaming@sha256:883d4d7a47db4d1c911cf0c23dad30011b46727297d1158bede3d833455a49e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1e123176c313a4b94f8c0fdf6cac9abdd85a1bd6edf3f7cc6e7ed61852d19a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:25:32 GMT
COPY file:aefc6cbeadb611214d28b81a278a791c774a4bbc969528522aae7abe7c4e2784 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:25:32 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:25:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:25:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:087a668f89c4000c166ca5a16dd40fee8206986ce9b47a92d224b78214f3db5c`  
		Last Modified: Fri, 16 Apr 2021 21:26:16 GMT  
		Size: 5.7 MB (5680535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.2` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9dc93ca8dad040be30fe0949d19f04a6b1775750838d70d2fb12f3aa9f40b4f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba356cbd8fdcd90e529d00104791d07c50c101937487a0b8647b06226bfdef9a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:02:53 GMT
COPY file:c58b6e2180eb9d24d595f35c2205c2d9b4f80315beb0f166e20a7340cf3f2536 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:03:00 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:03:04 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:03:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3542c02ee947256ff50165b76289b4dd90e7c82bfb7b0b983b4d66d4b1128e9a`  
		Last Modified: Fri, 16 Apr 2021 21:03:44 GMT  
		Size: 5.3 MB (5253054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.2` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:10f5838646402cebd5c40f8f02991aad0ca3767b13b3024054e5e04026d3c778
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409bfb98a0a11b06fb4c8a044cda742270c21f5082ef80b63e7893cb4ce2f9c3`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:00:05 GMT
COPY file:7ad2a856b4d75bdc56fbd35738819610cc3c26111897fc883c3af7db16d4fa87 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:00:07 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:00:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:00:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:76bf01e9a89a0de09d5ab72dd4ec7e4c9f561a27756ceb73bf0365f192de2d18`  
		Last Modified: Fri, 16 Apr 2021 21:01:13 GMT  
		Size: 5.2 MB (5246280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.2` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:3bf4856546fa4657b125293b8ed701a22dd3861cd532a14281d7726210c726c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4acb30c8790d9ef8af675772eda5d9f3903a662d29132ef140463453eeb717`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:48:04 GMT
COPY file:b02a357b6e9250e52099dcc91c6a9a78682a192bd0850fabc93d5cdacb6fcfb3 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:48:05 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:48:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:48:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:fe1641db2bf227918d02728a21bd3b53989018d9c796246d3b96fcbbf75ded32`  
		Last Modified: Fri, 16 Apr 2021 21:48:50 GMT  
		Size: 5.2 MB (5170831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.2` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:61bce4686b4cb6f2e1e9563643ef604ff9e6db78b3ec8017bbbb244bba89c69c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107156045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cb251e2361dacf7f07021ad3cd15d4a21877b08d66b75ea5ecd3fc0f19c7f7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Apr 2021 21:17:55 GMT
RUN cmd /S /C #(nop) COPY file:adacf7e54ef5a782ae37764b59883ad6a48b32c36c576816360f94cba82ba458 in C:\nats-streaming-server.exe 
# Fri, 16 Apr 2021 21:17:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:17:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:17:59 GMT
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
	-	`sha256:2ab6d20feb9c03e1c8e6983c39be671e946eb6994a26c435c813829e681dbe57`  
		Last Modified: Fri, 16 Apr 2021 21:24:02 GMT  
		Size: 5.8 MB (5811210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ec8e35cf7e38f49d059085e4aab0b4e8df8689989934d6ca20c6b406c06bed`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1354e00c20faa27d7a6d7931702d4005d12c09da6139424792bb915725783e2b`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df10c9c723da873a08ebe210f4272cbdc0b9d047c4898a7e721e957bab6465e`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.2-alpine`

```console
$ docker pull nats-streaming@sha256:d204ac6b58553c9632e9797984adcace87b6539d257754f1d5bdf5e4a2a8d72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21.2-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:402dacbb78f9bf5e9ea249c730f7905caa085ca665782e1cb4c6e7004f597689
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8774780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7ad70b17b46627026163460cce06023868f24d36a50cd9c261e7c6cba86e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:25:11 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:25:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:25:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:25:15 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:25:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:25:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269577e93d92e9e558c3607d8b5e74978c939fc643895de15fd70ef06b811323`  
		Last Modified: Fri, 16 Apr 2021 21:25:54 GMT  
		Size: 6.0 MB (5962389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fa1ca69a5dc5f7aecbfca382d45ab09423bb9d103c6567abc37af7b842073a`  
		Last Modified: Fri, 16 Apr 2021 21:25:54 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.2-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:e03de3640ce68bbb19cd2b5e8dc2a1454fbba1b369a4c236f09b6630197b6fa0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8156933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a345ef8cbbe68103787d05c9dbd22742cc95b726776cbf30298c3ca98487b63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:02:04 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:02:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:02:26 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:02:27 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:02:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:02:29 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e538f4430325ed9ef756e0e521a859c9466b9b7a45a8662e4f29f1ec5f8c3a7d`  
		Last Modified: Fri, 16 Apr 2021 21:03:32 GMT  
		Size: 5.5 MB (5534381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc165822006c8e13ee1ee6756545e0f021a059f974288d6c953febdeea6a83d3`  
		Last Modified: Fri, 16 Apr 2021 21:03:30 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.2-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ea133d32e6510a0d1822a1ea1cfcca41e3cbd747a3d69491aee62319937e892d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc13824ee86fb9d0c1609b885378ba366f3883903bfe990fb27464bce6c02686`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 20:59:08 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 20:59:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 20:59:13 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 20:59:14 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 20:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 20:59:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b86c52fd84fa988d60547be09b11af6fcac2dffa6b340e92b776a0fc89a298`  
		Last Modified: Fri, 16 Apr 2021 21:00:42 GMT  
		Size: 5.5 MB (5527039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b279e3ce6e5cfc3967a4acbf6dc2563f1715817b059d6f320b53cbc21b74e1`  
		Last Modified: Fri, 16 Apr 2021 21:00:40 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:febf36c660fc36bcbf3da9945707f541e81665b0d21a0f1c6c8220543697a757
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8165113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd79dce90e049636e2513bd55a0b3178cb59197d3dfc53cbed474dbbd5de0f1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:44:03 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:44:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:44:08 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:44:09 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:44:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:44:10 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a1a4dae3b1b310f0231f28f4db383d7605066343274881c5be1300ebe64f51`  
		Last Modified: Fri, 16 Apr 2021 21:48:37 GMT  
		Size: 5.5 MB (5452665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a06774842e75925d8884fc1ea5a3e83c2c8054d4fb443ad11021c5866b0617`  
		Last Modified: Fri, 16 Apr 2021 21:48:36 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.2-alpine3.13`

```console
$ docker pull nats-streaming@sha256:d204ac6b58553c9632e9797984adcace87b6539d257754f1d5bdf5e4a2a8d72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21.2-alpine3.13` - linux; amd64

```console
$ docker pull nats-streaming@sha256:402dacbb78f9bf5e9ea249c730f7905caa085ca665782e1cb4c6e7004f597689
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8774780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7ad70b17b46627026163460cce06023868f24d36a50cd9c261e7c6cba86e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:25:11 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:25:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:25:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:25:15 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:25:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:25:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269577e93d92e9e558c3607d8b5e74978c939fc643895de15fd70ef06b811323`  
		Last Modified: Fri, 16 Apr 2021 21:25:54 GMT  
		Size: 6.0 MB (5962389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fa1ca69a5dc5f7aecbfca382d45ab09423bb9d103c6567abc37af7b842073a`  
		Last Modified: Fri, 16 Apr 2021 21:25:54 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.2-alpine3.13` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:e03de3640ce68bbb19cd2b5e8dc2a1454fbba1b369a4c236f09b6630197b6fa0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8156933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a345ef8cbbe68103787d05c9dbd22742cc95b726776cbf30298c3ca98487b63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:02:04 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:02:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:02:26 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:02:27 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:02:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:02:29 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e538f4430325ed9ef756e0e521a859c9466b9b7a45a8662e4f29f1ec5f8c3a7d`  
		Last Modified: Fri, 16 Apr 2021 21:03:32 GMT  
		Size: 5.5 MB (5534381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc165822006c8e13ee1ee6756545e0f021a059f974288d6c953febdeea6a83d3`  
		Last Modified: Fri, 16 Apr 2021 21:03:30 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.2-alpine3.13` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ea133d32e6510a0d1822a1ea1cfcca41e3cbd747a3d69491aee62319937e892d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc13824ee86fb9d0c1609b885378ba366f3883903bfe990fb27464bce6c02686`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 20:59:08 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 20:59:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 20:59:13 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 20:59:14 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 20:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 20:59:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b86c52fd84fa988d60547be09b11af6fcac2dffa6b340e92b776a0fc89a298`  
		Last Modified: Fri, 16 Apr 2021 21:00:42 GMT  
		Size: 5.5 MB (5527039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b279e3ce6e5cfc3967a4acbf6dc2563f1715817b059d6f320b53cbc21b74e1`  
		Last Modified: Fri, 16 Apr 2021 21:00:40 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.2-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:febf36c660fc36bcbf3da9945707f541e81665b0d21a0f1c6c8220543697a757
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8165113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd79dce90e049636e2513bd55a0b3178cb59197d3dfc53cbed474dbbd5de0f1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:44:03 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:44:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:44:08 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:44:09 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:44:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:44:10 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a1a4dae3b1b310f0231f28f4db383d7605066343274881c5be1300ebe64f51`  
		Last Modified: Fri, 16 Apr 2021 21:48:37 GMT  
		Size: 5.5 MB (5452665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a06774842e75925d8884fc1ea5a3e83c2c8054d4fb443ad11021c5866b0617`  
		Last Modified: Fri, 16 Apr 2021 21:48:36 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.2-linux`

```console
$ docker pull nats-streaming@sha256:2bf298093b69248cb6e82aa7c64d50c1a45480ad23a8ced79a5ddf588ee69102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21.2-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:883d4d7a47db4d1c911cf0c23dad30011b46727297d1158bede3d833455a49e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1e123176c313a4b94f8c0fdf6cac9abdd85a1bd6edf3f7cc6e7ed61852d19a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:25:32 GMT
COPY file:aefc6cbeadb611214d28b81a278a791c774a4bbc969528522aae7abe7c4e2784 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:25:32 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:25:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:25:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:087a668f89c4000c166ca5a16dd40fee8206986ce9b47a92d224b78214f3db5c`  
		Last Modified: Fri, 16 Apr 2021 21:26:16 GMT  
		Size: 5.7 MB (5680535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.2-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9dc93ca8dad040be30fe0949d19f04a6b1775750838d70d2fb12f3aa9f40b4f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba356cbd8fdcd90e529d00104791d07c50c101937487a0b8647b06226bfdef9a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:02:53 GMT
COPY file:c58b6e2180eb9d24d595f35c2205c2d9b4f80315beb0f166e20a7340cf3f2536 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:03:00 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:03:04 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:03:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3542c02ee947256ff50165b76289b4dd90e7c82bfb7b0b983b4d66d4b1128e9a`  
		Last Modified: Fri, 16 Apr 2021 21:03:44 GMT  
		Size: 5.3 MB (5253054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.2-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:10f5838646402cebd5c40f8f02991aad0ca3767b13b3024054e5e04026d3c778
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409bfb98a0a11b06fb4c8a044cda742270c21f5082ef80b63e7893cb4ce2f9c3`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:00:05 GMT
COPY file:7ad2a856b4d75bdc56fbd35738819610cc3c26111897fc883c3af7db16d4fa87 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:00:07 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:00:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:00:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:76bf01e9a89a0de09d5ab72dd4ec7e4c9f561a27756ceb73bf0365f192de2d18`  
		Last Modified: Fri, 16 Apr 2021 21:01:13 GMT  
		Size: 5.2 MB (5246280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.2-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:3bf4856546fa4657b125293b8ed701a22dd3861cd532a14281d7726210c726c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4acb30c8790d9ef8af675772eda5d9f3903a662d29132ef140463453eeb717`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:48:04 GMT
COPY file:b02a357b6e9250e52099dcc91c6a9a78682a192bd0850fabc93d5cdacb6fcfb3 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:48:05 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:48:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:48:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:fe1641db2bf227918d02728a21bd3b53989018d9c796246d3b96fcbbf75ded32`  
		Last Modified: Fri, 16 Apr 2021 21:48:50 GMT  
		Size: 5.2 MB (5170831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.2-nanoserver`

```console
$ docker pull nats-streaming@sha256:cba11565eb636b9f97847e3feefb1c750ed9f20f17906263428c122cd788056f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:0.21.2-nanoserver` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:61bce4686b4cb6f2e1e9563643ef604ff9e6db78b3ec8017bbbb244bba89c69c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107156045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cb251e2361dacf7f07021ad3cd15d4a21877b08d66b75ea5ecd3fc0f19c7f7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Apr 2021 21:17:55 GMT
RUN cmd /S /C #(nop) COPY file:adacf7e54ef5a782ae37764b59883ad6a48b32c36c576816360f94cba82ba458 in C:\nats-streaming-server.exe 
# Fri, 16 Apr 2021 21:17:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:17:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:17:59 GMT
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
	-	`sha256:2ab6d20feb9c03e1c8e6983c39be671e946eb6994a26c435c813829e681dbe57`  
		Last Modified: Fri, 16 Apr 2021 21:24:02 GMT  
		Size: 5.8 MB (5811210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ec8e35cf7e38f49d059085e4aab0b4e8df8689989934d6ca20c6b406c06bed`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1354e00c20faa27d7a6d7931702d4005d12c09da6139424792bb915725783e2b`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df10c9c723da873a08ebe210f4272cbdc0b9d047c4898a7e721e957bab6465e`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.2-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:cba11565eb636b9f97847e3feefb1c750ed9f20f17906263428c122cd788056f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:0.21.2-nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:61bce4686b4cb6f2e1e9563643ef604ff9e6db78b3ec8017bbbb244bba89c69c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107156045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cb251e2361dacf7f07021ad3cd15d4a21877b08d66b75ea5ecd3fc0f19c7f7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Apr 2021 21:17:55 GMT
RUN cmd /S /C #(nop) COPY file:adacf7e54ef5a782ae37764b59883ad6a48b32c36c576816360f94cba82ba458 in C:\nats-streaming-server.exe 
# Fri, 16 Apr 2021 21:17:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:17:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:17:59 GMT
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
	-	`sha256:2ab6d20feb9c03e1c8e6983c39be671e946eb6994a26c435c813829e681dbe57`  
		Last Modified: Fri, 16 Apr 2021 21:24:02 GMT  
		Size: 5.8 MB (5811210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ec8e35cf7e38f49d059085e4aab0b4e8df8689989934d6ca20c6b406c06bed`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1354e00c20faa27d7a6d7931702d4005d12c09da6139424792bb915725783e2b`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df10c9c723da873a08ebe210f4272cbdc0b9d047c4898a7e721e957bab6465e`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.2-scratch`

```console
$ docker pull nats-streaming@sha256:2bf298093b69248cb6e82aa7c64d50c1a45480ad23a8ced79a5ddf588ee69102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.21.2-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:883d4d7a47db4d1c911cf0c23dad30011b46727297d1158bede3d833455a49e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1e123176c313a4b94f8c0fdf6cac9abdd85a1bd6edf3f7cc6e7ed61852d19a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:25:32 GMT
COPY file:aefc6cbeadb611214d28b81a278a791c774a4bbc969528522aae7abe7c4e2784 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:25:32 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:25:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:25:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:087a668f89c4000c166ca5a16dd40fee8206986ce9b47a92d224b78214f3db5c`  
		Last Modified: Fri, 16 Apr 2021 21:26:16 GMT  
		Size: 5.7 MB (5680535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.2-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9dc93ca8dad040be30fe0949d19f04a6b1775750838d70d2fb12f3aa9f40b4f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba356cbd8fdcd90e529d00104791d07c50c101937487a0b8647b06226bfdef9a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:02:53 GMT
COPY file:c58b6e2180eb9d24d595f35c2205c2d9b4f80315beb0f166e20a7340cf3f2536 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:03:00 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:03:04 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:03:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3542c02ee947256ff50165b76289b4dd90e7c82bfb7b0b983b4d66d4b1128e9a`  
		Last Modified: Fri, 16 Apr 2021 21:03:44 GMT  
		Size: 5.3 MB (5253054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.2-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:10f5838646402cebd5c40f8f02991aad0ca3767b13b3024054e5e04026d3c778
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409bfb98a0a11b06fb4c8a044cda742270c21f5082ef80b63e7893cb4ce2f9c3`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:00:05 GMT
COPY file:7ad2a856b4d75bdc56fbd35738819610cc3c26111897fc883c3af7db16d4fa87 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:00:07 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:00:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:00:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:76bf01e9a89a0de09d5ab72dd4ec7e4c9f561a27756ceb73bf0365f192de2d18`  
		Last Modified: Fri, 16 Apr 2021 21:01:13 GMT  
		Size: 5.2 MB (5246280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:3bf4856546fa4657b125293b8ed701a22dd3861cd532a14281d7726210c726c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4acb30c8790d9ef8af675772eda5d9f3903a662d29132ef140463453eeb717`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:48:04 GMT
COPY file:b02a357b6e9250e52099dcc91c6a9a78682a192bd0850fabc93d5cdacb6fcfb3 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:48:05 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:48:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:48:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:fe1641db2bf227918d02728a21bd3b53989018d9c796246d3b96fcbbf75ded32`  
		Last Modified: Fri, 16 Apr 2021 21:48:50 GMT  
		Size: 5.2 MB (5170831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.2-windowsservercore`

```console
$ docker pull nats-streaming@sha256:98b9617ca151407afacb114ff81aff503c2ea4577b96209c8c5676361ca9557a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `nats-streaming:0.21.2-windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:46a11494d76fc259b7a9f8a0c27873460bf913594ca6f05a299234525b15094a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2485739262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b666c7480c5c11601af2df96a1489969fe78538e0945930ef51de2fe96c389a1`
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
# Fri, 16 Apr 2021 21:15:14 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:15:14 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.2/nats-streaming-server-v0.21.2-windows-amd64.zip
# Fri, 16 Apr 2021 21:15:15 GMT
ENV GIT_DOWNLOAD_SHA256=5d4367fea29116fcd70c364c8e808d6bc8e74214effbde83dd9548455bd06df2
# Fri, 16 Apr 2021 21:16:09 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Apr 2021 21:17:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 16 Apr 2021 21:17:43 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:17:44 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:17:45 GMT
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
	-	`sha256:63694c9279bb4c7122e4c15326493b2ffac8c6df264b45b2bc1542aa4763c785`  
		Last Modified: Fri, 16 Apr 2021 21:23:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7109d9070f9055006a72b16519d93e1ff1ba1e5421bc264c2197ef4e6a3edb0d`  
		Last Modified: Fri, 16 Apr 2021 21:23:46 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6023c32ca8ac978165d5409ef9087006ee445e04c5b93d707b0fb484faa1b3c3`  
		Last Modified: Fri, 16 Apr 2021 21:23:46 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc9c54c2bcc706204b7d4feaf8b3e66c9efaab5f43babd81045e31c318bc25c`  
		Last Modified: Fri, 16 Apr 2021 21:23:45 GMT  
		Size: 5.1 MB (5096185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208b0279ea22aad1e519ba1f2f927cf4598bdfbddf3a33b2c14e6356331b2f48`  
		Last Modified: Fri, 16 Apr 2021 21:23:47 GMT  
		Size: 10.9 MB (10877752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d04869441fc428a1ea7711da8ca9b0c8b6bdee6622751b6c44d98633fc9ded`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a25017dc98d8b32009d962f73fcf54adb74971347a78fb4f94b35da8c92179`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cc3678ca9e1a8f67aca7150e64f25b9f0a28cf4c07ecdaae86095d9fe09523`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.21.2-windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull nats-streaming@sha256:2855b5d29b6f04637f9552d71cda49dcb3dc4d542d7ed205bfe8d97be393545f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816479551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbec025bd002885ef7f70a46dec4fe05d03313f3821b9d4f905ebe807c1f3f6`
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
# Fri, 16 Apr 2021 21:18:08 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:18:09 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.2/nats-streaming-server-v0.21.2-windows-amd64.zip
# Fri, 16 Apr 2021 21:18:10 GMT
ENV GIT_DOWNLOAD_SHA256=5d4367fea29116fcd70c364c8e808d6bc8e74214effbde83dd9548455bd06df2
# Fri, 16 Apr 2021 21:20:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Apr 2021 21:22:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 16 Apr 2021 21:22:44 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:22:46 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:22:47 GMT
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
	-	`sha256:bb633935c8262a169f8ce0f1c047198f3f981cf5315ebbdfb8aa7ba7e7d72bb5`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65576d29a65010c1357bcc65b8be2b2b1fdc9c4e43886372b8906fe1e108992b`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5de8efb2c9f3c99d2381a169ff4f442ca3b804a8a822584c54fa8673ef2f18`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a185c587f57ffd591baafd272bad6bdd76759232c6fb38c93ae2f951ef672d58`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 5.7 MB (5660316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58dea9968ebcd0bab739582d83245d50a4866d2bcbd2153d5dfa856e285fc810`  
		Last Modified: Fri, 16 Apr 2021 21:24:20 GMT  
		Size: 15.9 MB (15924139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d5db835b40ab66c30271634885e8fae5e1ba4c40c486a8cea2f021882824f8`  
		Last Modified: Fri, 16 Apr 2021 21:24:15 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2a1a71345bf095f4133c7fad40e22ecde64b60261ca6035b69111680d7f576`  
		Last Modified: Fri, 16 Apr 2021 21:24:16 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffed13d909a2d6c0c79217cee06b023d0e1bbe267704ea88f3d26b5b3fd6b5e9`  
		Last Modified: Fri, 16 Apr 2021 21:24:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.2-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:d68f4e2295d5a9c5bed66b3866e3d4ae3bc8af5f4e73fdcf584c03f4e1bbb82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:0.21.2-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:46a11494d76fc259b7a9f8a0c27873460bf913594ca6f05a299234525b15094a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2485739262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b666c7480c5c11601af2df96a1489969fe78538e0945930ef51de2fe96c389a1`
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
# Fri, 16 Apr 2021 21:15:14 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:15:14 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.2/nats-streaming-server-v0.21.2-windows-amd64.zip
# Fri, 16 Apr 2021 21:15:15 GMT
ENV GIT_DOWNLOAD_SHA256=5d4367fea29116fcd70c364c8e808d6bc8e74214effbde83dd9548455bd06df2
# Fri, 16 Apr 2021 21:16:09 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Apr 2021 21:17:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 16 Apr 2021 21:17:43 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:17:44 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:17:45 GMT
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
	-	`sha256:63694c9279bb4c7122e4c15326493b2ffac8c6df264b45b2bc1542aa4763c785`  
		Last Modified: Fri, 16 Apr 2021 21:23:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7109d9070f9055006a72b16519d93e1ff1ba1e5421bc264c2197ef4e6a3edb0d`  
		Last Modified: Fri, 16 Apr 2021 21:23:46 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6023c32ca8ac978165d5409ef9087006ee445e04c5b93d707b0fb484faa1b3c3`  
		Last Modified: Fri, 16 Apr 2021 21:23:46 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc9c54c2bcc706204b7d4feaf8b3e66c9efaab5f43babd81045e31c318bc25c`  
		Last Modified: Fri, 16 Apr 2021 21:23:45 GMT  
		Size: 5.1 MB (5096185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208b0279ea22aad1e519ba1f2f927cf4598bdfbddf3a33b2c14e6356331b2f48`  
		Last Modified: Fri, 16 Apr 2021 21:23:47 GMT  
		Size: 10.9 MB (10877752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d04869441fc428a1ea7711da8ca9b0c8b6bdee6622751b6c44d98633fc9ded`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a25017dc98d8b32009d962f73fcf54adb74971347a78fb4f94b35da8c92179`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cc3678ca9e1a8f67aca7150e64f25b9f0a28cf4c07ecdaae86095d9fe09523`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.21.2-windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:aefa3b0d0213921ea947351c14fb151622e1e9cb7f3d6dd50ab2b3f35db87859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `nats-streaming:0.21.2-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull nats-streaming@sha256:2855b5d29b6f04637f9552d71cda49dcb3dc4d542d7ed205bfe8d97be393545f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816479551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbec025bd002885ef7f70a46dec4fe05d03313f3821b9d4f905ebe807c1f3f6`
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
# Fri, 16 Apr 2021 21:18:08 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:18:09 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.2/nats-streaming-server-v0.21.2-windows-amd64.zip
# Fri, 16 Apr 2021 21:18:10 GMT
ENV GIT_DOWNLOAD_SHA256=5d4367fea29116fcd70c364c8e808d6bc8e74214effbde83dd9548455bd06df2
# Fri, 16 Apr 2021 21:20:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Apr 2021 21:22:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 16 Apr 2021 21:22:44 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:22:46 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:22:47 GMT
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
	-	`sha256:bb633935c8262a169f8ce0f1c047198f3f981cf5315ebbdfb8aa7ba7e7d72bb5`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65576d29a65010c1357bcc65b8be2b2b1fdc9c4e43886372b8906fe1e108992b`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5de8efb2c9f3c99d2381a169ff4f442ca3b804a8a822584c54fa8673ef2f18`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a185c587f57ffd591baafd272bad6bdd76759232c6fb38c93ae2f951ef672d58`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 5.7 MB (5660316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58dea9968ebcd0bab739582d83245d50a4866d2bcbd2153d5dfa856e285fc810`  
		Last Modified: Fri, 16 Apr 2021 21:24:20 GMT  
		Size: 15.9 MB (15924139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d5db835b40ab66c30271634885e8fae5e1ba4c40c486a8cea2f021882824f8`  
		Last Modified: Fri, 16 Apr 2021 21:24:15 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2a1a71345bf095f4133c7fad40e22ecde64b60261ca6035b69111680d7f576`  
		Last Modified: Fri, 16 Apr 2021 21:24:16 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffed13d909a2d6c0c79217cee06b023d0e1bbe267704ea88f3d26b5b3fd6b5e9`  
		Last Modified: Fri, 16 Apr 2021 21:24:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:d204ac6b58553c9632e9797984adcace87b6539d257754f1d5bdf5e4a2a8d72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:402dacbb78f9bf5e9ea249c730f7905caa085ca665782e1cb4c6e7004f597689
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8774780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7ad70b17b46627026163460cce06023868f24d36a50cd9c261e7c6cba86e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:25:11 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:25:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:25:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:25:15 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:25:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:25:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269577e93d92e9e558c3607d8b5e74978c939fc643895de15fd70ef06b811323`  
		Last Modified: Fri, 16 Apr 2021 21:25:54 GMT  
		Size: 6.0 MB (5962389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fa1ca69a5dc5f7aecbfca382d45ab09423bb9d103c6567abc37af7b842073a`  
		Last Modified: Fri, 16 Apr 2021 21:25:54 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:e03de3640ce68bbb19cd2b5e8dc2a1454fbba1b369a4c236f09b6630197b6fa0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8156933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a345ef8cbbe68103787d05c9dbd22742cc95b726776cbf30298c3ca98487b63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:02:04 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:02:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:02:26 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:02:27 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:02:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:02:29 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e538f4430325ed9ef756e0e521a859c9466b9b7a45a8662e4f29f1ec5f8c3a7d`  
		Last Modified: Fri, 16 Apr 2021 21:03:32 GMT  
		Size: 5.5 MB (5534381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc165822006c8e13ee1ee6756545e0f021a059f974288d6c953febdeea6a83d3`  
		Last Modified: Fri, 16 Apr 2021 21:03:30 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ea133d32e6510a0d1822a1ea1cfcca41e3cbd747a3d69491aee62319937e892d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc13824ee86fb9d0c1609b885378ba366f3883903bfe990fb27464bce6c02686`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 20:59:08 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 20:59:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 20:59:13 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 20:59:14 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 20:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 20:59:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b86c52fd84fa988d60547be09b11af6fcac2dffa6b340e92b776a0fc89a298`  
		Last Modified: Fri, 16 Apr 2021 21:00:42 GMT  
		Size: 5.5 MB (5527039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b279e3ce6e5cfc3967a4acbf6dc2563f1715817b059d6f320b53cbc21b74e1`  
		Last Modified: Fri, 16 Apr 2021 21:00:40 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:febf36c660fc36bcbf3da9945707f541e81665b0d21a0f1c6c8220543697a757
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8165113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd79dce90e049636e2513bd55a0b3178cb59197d3dfc53cbed474dbbd5de0f1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:44:03 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:44:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:44:08 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:44:09 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:44:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:44:10 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a1a4dae3b1b310f0231f28f4db383d7605066343274881c5be1300ebe64f51`  
		Last Modified: Fri, 16 Apr 2021 21:48:37 GMT  
		Size: 5.5 MB (5452665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a06774842e75925d8884fc1ea5a3e83c2c8054d4fb443ad11021c5866b0617`  
		Last Modified: Fri, 16 Apr 2021 21:48:36 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.13`

```console
$ docker pull nats-streaming@sha256:d204ac6b58553c9632e9797984adcace87b6539d257754f1d5bdf5e4a2a8d72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.13` - linux; amd64

```console
$ docker pull nats-streaming@sha256:402dacbb78f9bf5e9ea249c730f7905caa085ca665782e1cb4c6e7004f597689
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8774780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7ad70b17b46627026163460cce06023868f24d36a50cd9c261e7c6cba86e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:25:11 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:25:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:25:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:25:15 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:25:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:25:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269577e93d92e9e558c3607d8b5e74978c939fc643895de15fd70ef06b811323`  
		Last Modified: Fri, 16 Apr 2021 21:25:54 GMT  
		Size: 6.0 MB (5962389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fa1ca69a5dc5f7aecbfca382d45ab09423bb9d103c6567abc37af7b842073a`  
		Last Modified: Fri, 16 Apr 2021 21:25:54 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.13` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:e03de3640ce68bbb19cd2b5e8dc2a1454fbba1b369a4c236f09b6630197b6fa0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8156933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a345ef8cbbe68103787d05c9dbd22742cc95b726776cbf30298c3ca98487b63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:02:04 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:02:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:02:26 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:02:27 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:02:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:02:29 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e538f4430325ed9ef756e0e521a859c9466b9b7a45a8662e4f29f1ec5f8c3a7d`  
		Last Modified: Fri, 16 Apr 2021 21:03:32 GMT  
		Size: 5.5 MB (5534381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc165822006c8e13ee1ee6756545e0f021a059f974288d6c953febdeea6a83d3`  
		Last Modified: Fri, 16 Apr 2021 21:03:30 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.13` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ea133d32e6510a0d1822a1ea1cfcca41e3cbd747a3d69491aee62319937e892d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc13824ee86fb9d0c1609b885378ba366f3883903bfe990fb27464bce6c02686`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 20:59:08 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 20:59:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 20:59:13 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 20:59:14 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 20:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 20:59:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b86c52fd84fa988d60547be09b11af6fcac2dffa6b340e92b776a0fc89a298`  
		Last Modified: Fri, 16 Apr 2021 21:00:42 GMT  
		Size: 5.5 MB (5527039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b279e3ce6e5cfc3967a4acbf6dc2563f1715817b059d6f320b53cbc21b74e1`  
		Last Modified: Fri, 16 Apr 2021 21:00:40 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:febf36c660fc36bcbf3da9945707f541e81665b0d21a0f1c6c8220543697a757
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8165113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd79dce90e049636e2513bd55a0b3178cb59197d3dfc53cbed474dbbd5de0f1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:44:03 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:44:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:44:08 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:44:09 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:44:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:44:10 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a1a4dae3b1b310f0231f28f4db383d7605066343274881c5be1300ebe64f51`  
		Last Modified: Fri, 16 Apr 2021 21:48:37 GMT  
		Size: 5.5 MB (5452665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a06774842e75925d8884fc1ea5a3e83c2c8054d4fb443ad11021c5866b0617`  
		Last Modified: Fri, 16 Apr 2021 21:48:36 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:abea5a41eb4c8bf97ba0948419a58554540102007fc5b4495ef516916188809d
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
$ docker pull nats-streaming@sha256:883d4d7a47db4d1c911cf0c23dad30011b46727297d1158bede3d833455a49e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1e123176c313a4b94f8c0fdf6cac9abdd85a1bd6edf3f7cc6e7ed61852d19a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:25:32 GMT
COPY file:aefc6cbeadb611214d28b81a278a791c774a4bbc969528522aae7abe7c4e2784 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:25:32 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:25:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:25:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:087a668f89c4000c166ca5a16dd40fee8206986ce9b47a92d224b78214f3db5c`  
		Last Modified: Fri, 16 Apr 2021 21:26:16 GMT  
		Size: 5.7 MB (5680535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9dc93ca8dad040be30fe0949d19f04a6b1775750838d70d2fb12f3aa9f40b4f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba356cbd8fdcd90e529d00104791d07c50c101937487a0b8647b06226bfdef9a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:02:53 GMT
COPY file:c58b6e2180eb9d24d595f35c2205c2d9b4f80315beb0f166e20a7340cf3f2536 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:03:00 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:03:04 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:03:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3542c02ee947256ff50165b76289b4dd90e7c82bfb7b0b983b4d66d4b1128e9a`  
		Last Modified: Fri, 16 Apr 2021 21:03:44 GMT  
		Size: 5.3 MB (5253054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:10f5838646402cebd5c40f8f02991aad0ca3767b13b3024054e5e04026d3c778
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409bfb98a0a11b06fb4c8a044cda742270c21f5082ef80b63e7893cb4ce2f9c3`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:00:05 GMT
COPY file:7ad2a856b4d75bdc56fbd35738819610cc3c26111897fc883c3af7db16d4fa87 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:00:07 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:00:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:00:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:76bf01e9a89a0de09d5ab72dd4ec7e4c9f561a27756ceb73bf0365f192de2d18`  
		Last Modified: Fri, 16 Apr 2021 21:01:13 GMT  
		Size: 5.2 MB (5246280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:3bf4856546fa4657b125293b8ed701a22dd3861cd532a14281d7726210c726c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4acb30c8790d9ef8af675772eda5d9f3903a662d29132ef140463453eeb717`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:48:04 GMT
COPY file:b02a357b6e9250e52099dcc91c6a9a78682a192bd0850fabc93d5cdacb6fcfb3 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:48:05 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:48:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:48:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:fe1641db2bf227918d02728a21bd3b53989018d9c796246d3b96fcbbf75ded32`  
		Last Modified: Fri, 16 Apr 2021 21:48:50 GMT  
		Size: 5.2 MB (5170831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:61bce4686b4cb6f2e1e9563643ef604ff9e6db78b3ec8017bbbb244bba89c69c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107156045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cb251e2361dacf7f07021ad3cd15d4a21877b08d66b75ea5ecd3fc0f19c7f7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Apr 2021 21:17:55 GMT
RUN cmd /S /C #(nop) COPY file:adacf7e54ef5a782ae37764b59883ad6a48b32c36c576816360f94cba82ba458 in C:\nats-streaming-server.exe 
# Fri, 16 Apr 2021 21:17:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:17:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:17:59 GMT
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
	-	`sha256:2ab6d20feb9c03e1c8e6983c39be671e946eb6994a26c435c813829e681dbe57`  
		Last Modified: Fri, 16 Apr 2021 21:24:02 GMT  
		Size: 5.8 MB (5811210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ec8e35cf7e38f49d059085e4aab0b4e8df8689989934d6ca20c6b406c06bed`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1354e00c20faa27d7a6d7931702d4005d12c09da6139424792bb915725783e2b`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df10c9c723da873a08ebe210f4272cbdc0b9d047c4898a7e721e957bab6465e`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:2bf298093b69248cb6e82aa7c64d50c1a45480ad23a8ced79a5ddf588ee69102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:883d4d7a47db4d1c911cf0c23dad30011b46727297d1158bede3d833455a49e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1e123176c313a4b94f8c0fdf6cac9abdd85a1bd6edf3f7cc6e7ed61852d19a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:25:32 GMT
COPY file:aefc6cbeadb611214d28b81a278a791c774a4bbc969528522aae7abe7c4e2784 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:25:32 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:25:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:25:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:087a668f89c4000c166ca5a16dd40fee8206986ce9b47a92d224b78214f3db5c`  
		Last Modified: Fri, 16 Apr 2021 21:26:16 GMT  
		Size: 5.7 MB (5680535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9dc93ca8dad040be30fe0949d19f04a6b1775750838d70d2fb12f3aa9f40b4f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba356cbd8fdcd90e529d00104791d07c50c101937487a0b8647b06226bfdef9a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:02:53 GMT
COPY file:c58b6e2180eb9d24d595f35c2205c2d9b4f80315beb0f166e20a7340cf3f2536 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:03:00 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:03:04 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:03:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3542c02ee947256ff50165b76289b4dd90e7c82bfb7b0b983b4d66d4b1128e9a`  
		Last Modified: Fri, 16 Apr 2021 21:03:44 GMT  
		Size: 5.3 MB (5253054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:10f5838646402cebd5c40f8f02991aad0ca3767b13b3024054e5e04026d3c778
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409bfb98a0a11b06fb4c8a044cda742270c21f5082ef80b63e7893cb4ce2f9c3`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:00:05 GMT
COPY file:7ad2a856b4d75bdc56fbd35738819610cc3c26111897fc883c3af7db16d4fa87 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:00:07 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:00:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:00:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:76bf01e9a89a0de09d5ab72dd4ec7e4c9f561a27756ceb73bf0365f192de2d18`  
		Last Modified: Fri, 16 Apr 2021 21:01:13 GMT  
		Size: 5.2 MB (5246280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:3bf4856546fa4657b125293b8ed701a22dd3861cd532a14281d7726210c726c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4acb30c8790d9ef8af675772eda5d9f3903a662d29132ef140463453eeb717`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:48:04 GMT
COPY file:b02a357b6e9250e52099dcc91c6a9a78682a192bd0850fabc93d5cdacb6fcfb3 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:48:05 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:48:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:48:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:fe1641db2bf227918d02728a21bd3b53989018d9c796246d3b96fcbbf75ded32`  
		Last Modified: Fri, 16 Apr 2021 21:48:50 GMT  
		Size: 5.2 MB (5170831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:cba11565eb636b9f97847e3feefb1c750ed9f20f17906263428c122cd788056f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:61bce4686b4cb6f2e1e9563643ef604ff9e6db78b3ec8017bbbb244bba89c69c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107156045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cb251e2361dacf7f07021ad3cd15d4a21877b08d66b75ea5ecd3fc0f19c7f7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Apr 2021 21:17:55 GMT
RUN cmd /S /C #(nop) COPY file:adacf7e54ef5a782ae37764b59883ad6a48b32c36c576816360f94cba82ba458 in C:\nats-streaming-server.exe 
# Fri, 16 Apr 2021 21:17:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:17:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:17:59 GMT
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
	-	`sha256:2ab6d20feb9c03e1c8e6983c39be671e946eb6994a26c435c813829e681dbe57`  
		Last Modified: Fri, 16 Apr 2021 21:24:02 GMT  
		Size: 5.8 MB (5811210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ec8e35cf7e38f49d059085e4aab0b4e8df8689989934d6ca20c6b406c06bed`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1354e00c20faa27d7a6d7931702d4005d12c09da6139424792bb915725783e2b`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df10c9c723da873a08ebe210f4272cbdc0b9d047c4898a7e721e957bab6465e`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:cba11565eb636b9f97847e3feefb1c750ed9f20f17906263428c122cd788056f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:61bce4686b4cb6f2e1e9563643ef604ff9e6db78b3ec8017bbbb244bba89c69c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107156045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cb251e2361dacf7f07021ad3cd15d4a21877b08d66b75ea5ecd3fc0f19c7f7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Apr 2021 21:17:55 GMT
RUN cmd /S /C #(nop) COPY file:adacf7e54ef5a782ae37764b59883ad6a48b32c36c576816360f94cba82ba458 in C:\nats-streaming-server.exe 
# Fri, 16 Apr 2021 21:17:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:17:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:17:59 GMT
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
	-	`sha256:2ab6d20feb9c03e1c8e6983c39be671e946eb6994a26c435c813829e681dbe57`  
		Last Modified: Fri, 16 Apr 2021 21:24:02 GMT  
		Size: 5.8 MB (5811210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ec8e35cf7e38f49d059085e4aab0b4e8df8689989934d6ca20c6b406c06bed`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1354e00c20faa27d7a6d7931702d4005d12c09da6139424792bb915725783e2b`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df10c9c723da873a08ebe210f4272cbdc0b9d047c4898a7e721e957bab6465e`  
		Last Modified: Fri, 16 Apr 2021 21:24:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:2bf298093b69248cb6e82aa7c64d50c1a45480ad23a8ced79a5ddf588ee69102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:883d4d7a47db4d1c911cf0c23dad30011b46727297d1158bede3d833455a49e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1e123176c313a4b94f8c0fdf6cac9abdd85a1bd6edf3f7cc6e7ed61852d19a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:25:32 GMT
COPY file:aefc6cbeadb611214d28b81a278a791c774a4bbc969528522aae7abe7c4e2784 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:25:32 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:25:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:25:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:087a668f89c4000c166ca5a16dd40fee8206986ce9b47a92d224b78214f3db5c`  
		Last Modified: Fri, 16 Apr 2021 21:26:16 GMT  
		Size: 5.7 MB (5680535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9dc93ca8dad040be30fe0949d19f04a6b1775750838d70d2fb12f3aa9f40b4f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba356cbd8fdcd90e529d00104791d07c50c101937487a0b8647b06226bfdef9a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:02:53 GMT
COPY file:c58b6e2180eb9d24d595f35c2205c2d9b4f80315beb0f166e20a7340cf3f2536 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:03:00 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:03:04 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:03:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3542c02ee947256ff50165b76289b4dd90e7c82bfb7b0b983b4d66d4b1128e9a`  
		Last Modified: Fri, 16 Apr 2021 21:03:44 GMT  
		Size: 5.3 MB (5253054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:10f5838646402cebd5c40f8f02991aad0ca3767b13b3024054e5e04026d3c778
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409bfb98a0a11b06fb4c8a044cda742270c21f5082ef80b63e7893cb4ce2f9c3`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:00:05 GMT
COPY file:7ad2a856b4d75bdc56fbd35738819610cc3c26111897fc883c3af7db16d4fa87 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:00:07 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:00:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:00:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:76bf01e9a89a0de09d5ab72dd4ec7e4c9f561a27756ceb73bf0365f192de2d18`  
		Last Modified: Fri, 16 Apr 2021 21:01:13 GMT  
		Size: 5.2 MB (5246280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:3bf4856546fa4657b125293b8ed701a22dd3861cd532a14281d7726210c726c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4acb30c8790d9ef8af675772eda5d9f3903a662d29132ef140463453eeb717`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 16 Apr 2021 21:48:04 GMT
COPY file:b02a357b6e9250e52099dcc91c6a9a78682a192bd0850fabc93d5cdacb6fcfb3 in /nats-streaming-server 
# Fri, 16 Apr 2021 21:48:05 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:48:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 16 Apr 2021 21:48:07 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:fe1641db2bf227918d02728a21bd3b53989018d9c796246d3b96fcbbf75ded32`  
		Last Modified: Fri, 16 Apr 2021 21:48:50 GMT  
		Size: 5.2 MB (5170831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:98b9617ca151407afacb114ff81aff503c2ea4577b96209c8c5676361ca9557a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:46a11494d76fc259b7a9f8a0c27873460bf913594ca6f05a299234525b15094a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2485739262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b666c7480c5c11601af2df96a1489969fe78538e0945930ef51de2fe96c389a1`
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
# Fri, 16 Apr 2021 21:15:14 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:15:14 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.2/nats-streaming-server-v0.21.2-windows-amd64.zip
# Fri, 16 Apr 2021 21:15:15 GMT
ENV GIT_DOWNLOAD_SHA256=5d4367fea29116fcd70c364c8e808d6bc8e74214effbde83dd9548455bd06df2
# Fri, 16 Apr 2021 21:16:09 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Apr 2021 21:17:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 16 Apr 2021 21:17:43 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:17:44 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:17:45 GMT
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
	-	`sha256:63694c9279bb4c7122e4c15326493b2ffac8c6df264b45b2bc1542aa4763c785`  
		Last Modified: Fri, 16 Apr 2021 21:23:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7109d9070f9055006a72b16519d93e1ff1ba1e5421bc264c2197ef4e6a3edb0d`  
		Last Modified: Fri, 16 Apr 2021 21:23:46 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6023c32ca8ac978165d5409ef9087006ee445e04c5b93d707b0fb484faa1b3c3`  
		Last Modified: Fri, 16 Apr 2021 21:23:46 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc9c54c2bcc706204b7d4feaf8b3e66c9efaab5f43babd81045e31c318bc25c`  
		Last Modified: Fri, 16 Apr 2021 21:23:45 GMT  
		Size: 5.1 MB (5096185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208b0279ea22aad1e519ba1f2f927cf4598bdfbddf3a33b2c14e6356331b2f48`  
		Last Modified: Fri, 16 Apr 2021 21:23:47 GMT  
		Size: 10.9 MB (10877752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d04869441fc428a1ea7711da8ca9b0c8b6bdee6622751b6c44d98633fc9ded`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a25017dc98d8b32009d962f73fcf54adb74971347a78fb4f94b35da8c92179`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cc3678ca9e1a8f67aca7150e64f25b9f0a28cf4c07ecdaae86095d9fe09523`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull nats-streaming@sha256:2855b5d29b6f04637f9552d71cda49dcb3dc4d542d7ed205bfe8d97be393545f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816479551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbec025bd002885ef7f70a46dec4fe05d03313f3821b9d4f905ebe807c1f3f6`
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
# Fri, 16 Apr 2021 21:18:08 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:18:09 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.2/nats-streaming-server-v0.21.2-windows-amd64.zip
# Fri, 16 Apr 2021 21:18:10 GMT
ENV GIT_DOWNLOAD_SHA256=5d4367fea29116fcd70c364c8e808d6bc8e74214effbde83dd9548455bd06df2
# Fri, 16 Apr 2021 21:20:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Apr 2021 21:22:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 16 Apr 2021 21:22:44 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:22:46 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:22:47 GMT
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
	-	`sha256:bb633935c8262a169f8ce0f1c047198f3f981cf5315ebbdfb8aa7ba7e7d72bb5`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65576d29a65010c1357bcc65b8be2b2b1fdc9c4e43886372b8906fe1e108992b`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5de8efb2c9f3c99d2381a169ff4f442ca3b804a8a822584c54fa8673ef2f18`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a185c587f57ffd591baafd272bad6bdd76759232c6fb38c93ae2f951ef672d58`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 5.7 MB (5660316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58dea9968ebcd0bab739582d83245d50a4866d2bcbd2153d5dfa856e285fc810`  
		Last Modified: Fri, 16 Apr 2021 21:24:20 GMT  
		Size: 15.9 MB (15924139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d5db835b40ab66c30271634885e8fae5e1ba4c40c486a8cea2f021882824f8`  
		Last Modified: Fri, 16 Apr 2021 21:24:15 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2a1a71345bf095f4133c7fad40e22ecde64b60261ca6035b69111680d7f576`  
		Last Modified: Fri, 16 Apr 2021 21:24:16 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffed13d909a2d6c0c79217cee06b023d0e1bbe267704ea88f3d26b5b3fd6b5e9`  
		Last Modified: Fri, 16 Apr 2021 21:24:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:d68f4e2295d5a9c5bed66b3866e3d4ae3bc8af5f4e73fdcf584c03f4e1bbb82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats-streaming@sha256:46a11494d76fc259b7a9f8a0c27873460bf913594ca6f05a299234525b15094a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2485739262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b666c7480c5c11601af2df96a1489969fe78538e0945930ef51de2fe96c389a1`
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
# Fri, 16 Apr 2021 21:15:14 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:15:14 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.2/nats-streaming-server-v0.21.2-windows-amd64.zip
# Fri, 16 Apr 2021 21:15:15 GMT
ENV GIT_DOWNLOAD_SHA256=5d4367fea29116fcd70c364c8e808d6bc8e74214effbde83dd9548455bd06df2
# Fri, 16 Apr 2021 21:16:09 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Apr 2021 21:17:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 16 Apr 2021 21:17:43 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:17:44 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:17:45 GMT
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
	-	`sha256:63694c9279bb4c7122e4c15326493b2ffac8c6df264b45b2bc1542aa4763c785`  
		Last Modified: Fri, 16 Apr 2021 21:23:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7109d9070f9055006a72b16519d93e1ff1ba1e5421bc264c2197ef4e6a3edb0d`  
		Last Modified: Fri, 16 Apr 2021 21:23:46 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6023c32ca8ac978165d5409ef9087006ee445e04c5b93d707b0fb484faa1b3c3`  
		Last Modified: Fri, 16 Apr 2021 21:23:46 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc9c54c2bcc706204b7d4feaf8b3e66c9efaab5f43babd81045e31c318bc25c`  
		Last Modified: Fri, 16 Apr 2021 21:23:45 GMT  
		Size: 5.1 MB (5096185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208b0279ea22aad1e519ba1f2f927cf4598bdfbddf3a33b2c14e6356331b2f48`  
		Last Modified: Fri, 16 Apr 2021 21:23:47 GMT  
		Size: 10.9 MB (10877752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d04869441fc428a1ea7711da8ca9b0c8b6bdee6622751b6c44d98633fc9ded`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a25017dc98d8b32009d962f73fcf54adb74971347a78fb4f94b35da8c92179`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cc3678ca9e1a8f67aca7150e64f25b9f0a28cf4c07ecdaae86095d9fe09523`  
		Last Modified: Fri, 16 Apr 2021 21:23:44 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:aefa3b0d0213921ea947351c14fb151622e1e9cb7f3d6dd50ab2b3f35db87859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `nats-streaming:windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull nats-streaming@sha256:2855b5d29b6f04637f9552d71cda49dcb3dc4d542d7ed205bfe8d97be393545f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816479551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbec025bd002885ef7f70a46dec4fe05d03313f3821b9d4f905ebe807c1f3f6`
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
# Fri, 16 Apr 2021 21:18:08 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:18:09 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.2/nats-streaming-server-v0.21.2-windows-amd64.zip
# Fri, 16 Apr 2021 21:18:10 GMT
ENV GIT_DOWNLOAD_SHA256=5d4367fea29116fcd70c364c8e808d6bc8e74214effbde83dd9548455bd06df2
# Fri, 16 Apr 2021 21:20:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Apr 2021 21:22:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Fri, 16 Apr 2021 21:22:44 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:22:46 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 16 Apr 2021 21:22:47 GMT
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
	-	`sha256:bb633935c8262a169f8ce0f1c047198f3f981cf5315ebbdfb8aa7ba7e7d72bb5`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65576d29a65010c1357bcc65b8be2b2b1fdc9c4e43886372b8906fe1e108992b`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5de8efb2c9f3c99d2381a169ff4f442ca3b804a8a822584c54fa8673ef2f18`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a185c587f57ffd591baafd272bad6bdd76759232c6fb38c93ae2f951ef672d58`  
		Last Modified: Fri, 16 Apr 2021 21:24:18 GMT  
		Size: 5.7 MB (5660316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58dea9968ebcd0bab739582d83245d50a4866d2bcbd2153d5dfa856e285fc810`  
		Last Modified: Fri, 16 Apr 2021 21:24:20 GMT  
		Size: 15.9 MB (15924139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d5db835b40ab66c30271634885e8fae5e1ba4c40c486a8cea2f021882824f8`  
		Last Modified: Fri, 16 Apr 2021 21:24:15 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2a1a71345bf095f4133c7fad40e22ecde64b60261ca6035b69111680d7f576`  
		Last Modified: Fri, 16 Apr 2021 21:24:16 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffed13d909a2d6c0c79217cee06b023d0e1bbe267704ea88f3d26b5b3fd6b5e9`  
		Last Modified: Fri, 16 Apr 2021 21:24:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

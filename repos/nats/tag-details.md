<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.13`](#nats2-alpine313)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2-windowsservercore-ltsc2016`](#nats2-windowsservercore-ltsc2016)
-	[`nats:2.2`](#nats22)
-	[`nats:2.2-alpine`](#nats22-alpine)
-	[`nats:2.2-alpine3.13`](#nats22-alpine313)
-	[`nats:2.2-linux`](#nats22-linux)
-	[`nats:2.2-nanoserver`](#nats22-nanoserver)
-	[`nats:2.2-nanoserver-1809`](#nats22-nanoserver-1809)
-	[`nats:2.2-scratch`](#nats22-scratch)
-	[`nats:2.2-windowsservercore`](#nats22-windowsservercore)
-	[`nats:2.2-windowsservercore-1809`](#nats22-windowsservercore-1809)
-	[`nats:2.2-windowsservercore-ltsc2016`](#nats22-windowsservercore-ltsc2016)
-	[`nats:2.2.2`](#nats222)
-	[`nats:2.2.2-alpine`](#nats222-alpine)
-	[`nats:2.2.2-alpine3.13`](#nats222-alpine313)
-	[`nats:2.2.2-linux`](#nats222-linux)
-	[`nats:2.2.2-nanoserver`](#nats222-nanoserver)
-	[`nats:2.2.2-nanoserver-1809`](#nats222-nanoserver-1809)
-	[`nats:2.2.2-scratch`](#nats222-scratch)
-	[`nats:2.2.2-windowsservercore`](#nats222-windowsservercore)
-	[`nats:2.2.2-windowsservercore-1809`](#nats222-windowsservercore-1809)
-	[`nats:2.2.2-windowsservercore-ltsc2016`](#nats222-windowsservercore-ltsc2016)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.13`](#natsalpine313)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)
-	[`nats:windowsservercore-ltsc2016`](#natswindowsservercore-ltsc2016)

## `nats:2`

```console
$ docker pull nats@sha256:2e6c786ed41cd0411448a9a82407ae18dde139150e6fe0869db2c8b98913df90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1879; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:28d9b42f5045e931f540022b50d140778296614cc46fea7fedef50e26b1584e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1080c373df8961fed31f1a39e28cc6c25d6795e0d7c3d561f2d379cf92def32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:9bb0ab90c22cd1ed787dfe4292c36984fd21bc48b2174ddad3b1e218161e3cf2 in /nats-server 
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:30 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:30 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:10c4c9fb12b776e55b0ea8d3264f808ccc5caffaf56114cb844d5cb09786a6f1`  
		Last Modified: Thu, 22 Apr 2021 23:03:33 GMT  
		Size: 4.2 MB (4225473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473fec5c1cde7c5433c3e027919086bdd598e029899936541b2ec21ddb7847b0`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:a7a2c8f7194409c4dd75c93a6f9de11db1fc17bf1737db1c06240524e0b1858e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3895594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1fb4c72cd0448a5ba37409b399e5f04057f31f629ec5be8445008c54972c7f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 22:19:49 GMT
COPY file:64e71cd1d2e9467abd40785edd59f9612f1881becc619f3bedb155000a247b80 in /nats-server 
# Thu, 22 Apr 2021 22:19:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 22:19:51 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 22:19:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:238304e519d8648cca435478a5cebd819ed4063a311feaa2db6ec68565dde2d9`  
		Last Modified: Thu, 22 Apr 2021 22:20:38 GMT  
		Size: 3.9 MB (3895118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7507e43fa5a0838f598dd2a7130b2a5a79aa79cd6a06a73a1836fc2e6d6b5`  
		Last Modified: Thu, 22 Apr 2021 22:20:35 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:7a8f74c069f07b3f0b1351bc3aa1e2894ecc216e60c645973dcc81d261801b1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369c32ee391f07aae82ebd5e96f68ab9f24da31ffc8c257980974aaae2c38302`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:41 GMT
COPY file:4b22e9e541a652ab24ae042aa5e507153db95686a925c860d8e1d0d6abad10a3 in /nats-server 
# Thu, 22 Apr 2021 23:02:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:43 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:44 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65dc194b502e4ec7533d01c0251af4373a42f1054f5dc600b8d4aa96c6697a99`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 3.9 MB (3891497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bcc4ebf70a26891fd7de222893f55bb8968e80212d8fdba06e24381f864e08`  
		Last Modified: Thu, 22 Apr 2021 23:03:31 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8b6b6b66c99dbfca177d9c18db7748068af5b7b397ff6444bef7d8c5df1ba19
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3865538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2844c33ced18f889b04345db4c42c57c97e38a0c8a922035c8e9833f3c3062`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:34:22 GMT
COPY file:7c26ed7ed2d57f80534f12bf79cbe9c116a73d781f8e5d610a54d82baca800a3 in /nats-server 
# Thu, 22 Apr 2021 23:34:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:34:24 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:34:26 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:34:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3946fb3fc24631b9897efde5d957a63512d59c5745a8d0b8a4dca3171d07f77b`  
		Last Modified: Thu, 22 Apr 2021 23:35:18 GMT  
		Size: 3.9 MB (3865066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9203e1c4fb17a9b11e7579ecba8ba11004c1f5565dd8a2cd3d2fc45182152a6`  
		Last Modified: Thu, 22 Apr 2021 23:35:17 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:919213b7bc91d2592c5d1312c0a4afc4191259685c87e5411af02b2f857c7f22
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105629134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c2735946f6f419fec4d9b2c7c5ef0d1de10fcb5bed1024117d3bdecf2ab3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 Apr 2021 22:17:39 GMT
RUN cmd /S /C #(nop) COPY file:0bab6ea83b560e32beee362f5586c34607d68bc8fc2e12422611f377373c3392 in C:\nats-server.exe 
# Thu, 22 Apr 2021 22:17:40 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84508bc2e91e9b08b6992021bcf6575304a72e75fe2e112017331b04d5edc6b8`  
		Last Modified: Thu, 22 Apr 2021 22:32:27 GMT  
		Size: 4.3 MB (4282564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62907c5116573f0b8237cef0b1b52331d4945c3fed33b88e5c961e2f505420a9`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ae9d391bb3e00f300812200277f9faee92744173d7324e3993ef169a0cd1eb`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62014e35aec6648734dd1a046b17cd77df9db4b2f8b17d2272e303ae3b97903a`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908266ff2e3c49a426faa0a3fd232a8d8556b9bd9361c046faaa764058830852`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:a5951ad6ed2f6215ecb8a6a6aa245bc55a3ac612ddc2479dc5798d2540121dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:85bf09a4ed3123ecb7a16dbc7b9f06a257bd03c0c54d149953b5d1a2a34541e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7320048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29560428628215cddf73747b2d824f6479740731a1d2819a6d4c86a2bd8c03b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:01:56 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:02:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:02:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:02:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:02:01 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:02:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb9a564713c5c5be09227ec80bb9144b76b8542f70ea965b101aaf4b1fa53b4`  
		Last Modified: Thu, 22 Apr 2021 23:03:02 GMT  
		Size: 4.5 MB (4507111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28124858f0b78aef5b2801438e68b373ebd10fdc30a1f72a24ef20712477c8`  
		Last Modified: Thu, 22 Apr 2021 23:03:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a0a0c07581f940dea4209a67968c0ff9391514049ebbf7a5e571e4d4489742`  
		Last Modified: Thu, 22 Apr 2021 23:03:01 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c48f594973b2c6b8a6ac35419d06177ffa677c0d839d9aa820ad07b74e32967a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54260724cde664486b3039108cb2de4303dcab3684f8e76bde0e417c059d09f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 22:19:04 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 22:19:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 22:19:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 22:19:15 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 22:19:17 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 22:19:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225e3f411aa135344bc62f2742e1c53ad81de0be7ef0ba69bd0087d697095d72`  
		Last Modified: Thu, 22 Apr 2021 22:20:22 GMT  
		Size: 4.2 MB (4179946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946ec1abe0a4f7a9d236788aa4212122a4bc3c827f6b939ab69a13f7b9cca0ed`  
		Last Modified: Thu, 22 Apr 2021 22:20:21 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7167ed7e4981c0dc0102aa4c067cc5babc52159b625c9bafa71854328d8ccb05`  
		Last Modified: Thu, 22 Apr 2021 22:20:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a4e89657b36a323fabe9a59de08eea4ee63780449a82a688e04581fccf28c022
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971a7eb41bc06c66ab63ef164148b3913f1c0f62b366dc3e8a31fab3d33e9cfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:01:08 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:01:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:01:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:01:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:01:15 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:01:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:01:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d830dca5f399e6b2a26c9d5d4957df49a12ac964c46777b5052c8cdc6b90254`  
		Last Modified: Thu, 22 Apr 2021 23:03:17 GMT  
		Size: 4.2 MB (4171927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716e7fafa13bb0b3cbee84575af5654cd3b9facd11bb0d45e2722b5e0267331f`  
		Last Modified: Thu, 22 Apr 2021 23:03:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da0fc6dcd60240bdb6977965ef833756766f028b56d5ea1114476acffeb0510`  
		Last Modified: Thu, 22 Apr 2021 23:03:16 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9de557d8757ca4cdc59685058da10f7c3c90e47acdcf9100c5e9c560b16755a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6863978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77dfb5c08760abdb5ebe1228f8dc9fe7f548d16eae96e858ac2ec457a584ee10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:31:02 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:31:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:31:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:31:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:31:11 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:31:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85832337b2784bee768ef22ecd3e10c80d8259c92f4bc1a18c55d39f130dcb4a`  
		Last Modified: Thu, 22 Apr 2021 23:34:59 GMT  
		Size: 4.2 MB (4150983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa6771d491a7a8de32b346b875cfe8a23c4fd0e23573e85874dd1b3a6f74ed4`  
		Last Modified: Thu, 22 Apr 2021 23:34:59 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a05c19e3476eb485ff68727fc8f7cc7dfa788735e30a2b72906b844b9c3e56`  
		Last Modified: Thu, 22 Apr 2021 23:34:58 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.13`

```console
$ docker pull nats@sha256:a5951ad6ed2f6215ecb8a6a6aa245bc55a3ac612ddc2479dc5798d2540121dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.13` - linux; amd64

```console
$ docker pull nats@sha256:85bf09a4ed3123ecb7a16dbc7b9f06a257bd03c0c54d149953b5d1a2a34541e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7320048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29560428628215cddf73747b2d824f6479740731a1d2819a6d4c86a2bd8c03b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:01:56 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:02:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:02:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:02:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:02:01 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:02:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb9a564713c5c5be09227ec80bb9144b76b8542f70ea965b101aaf4b1fa53b4`  
		Last Modified: Thu, 22 Apr 2021 23:03:02 GMT  
		Size: 4.5 MB (4507111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28124858f0b78aef5b2801438e68b373ebd10fdc30a1f72a24ef20712477c8`  
		Last Modified: Thu, 22 Apr 2021 23:03:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a0a0c07581f940dea4209a67968c0ff9391514049ebbf7a5e571e4d4489742`  
		Last Modified: Thu, 22 Apr 2021 23:03:01 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.13` - linux; arm variant v6

```console
$ docker pull nats@sha256:c48f594973b2c6b8a6ac35419d06177ffa677c0d839d9aa820ad07b74e32967a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54260724cde664486b3039108cb2de4303dcab3684f8e76bde0e417c059d09f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 22:19:04 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 22:19:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 22:19:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 22:19:15 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 22:19:17 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 22:19:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225e3f411aa135344bc62f2742e1c53ad81de0be7ef0ba69bd0087d697095d72`  
		Last Modified: Thu, 22 Apr 2021 22:20:22 GMT  
		Size: 4.2 MB (4179946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946ec1abe0a4f7a9d236788aa4212122a4bc3c827f6b939ab69a13f7b9cca0ed`  
		Last Modified: Thu, 22 Apr 2021 22:20:21 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7167ed7e4981c0dc0102aa4c067cc5babc52159b625c9bafa71854328d8ccb05`  
		Last Modified: Thu, 22 Apr 2021 22:20:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.13` - linux; arm variant v7

```console
$ docker pull nats@sha256:a4e89657b36a323fabe9a59de08eea4ee63780449a82a688e04581fccf28c022
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971a7eb41bc06c66ab63ef164148b3913f1c0f62b366dc3e8a31fab3d33e9cfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:01:08 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:01:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:01:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:01:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:01:15 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:01:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:01:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d830dca5f399e6b2a26c9d5d4957df49a12ac964c46777b5052c8cdc6b90254`  
		Last Modified: Thu, 22 Apr 2021 23:03:17 GMT  
		Size: 4.2 MB (4171927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716e7fafa13bb0b3cbee84575af5654cd3b9facd11bb0d45e2722b5e0267331f`  
		Last Modified: Thu, 22 Apr 2021 23:03:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da0fc6dcd60240bdb6977965ef833756766f028b56d5ea1114476acffeb0510`  
		Last Modified: Thu, 22 Apr 2021 23:03:16 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9de557d8757ca4cdc59685058da10f7c3c90e47acdcf9100c5e9c560b16755a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6863978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77dfb5c08760abdb5ebe1228f8dc9fe7f548d16eae96e858ac2ec457a584ee10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:31:02 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:31:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:31:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:31:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:31:11 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:31:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85832337b2784bee768ef22ecd3e10c80d8259c92f4bc1a18c55d39f130dcb4a`  
		Last Modified: Thu, 22 Apr 2021 23:34:59 GMT  
		Size: 4.2 MB (4150983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa6771d491a7a8de32b346b875cfe8a23c4fd0e23573e85874dd1b3a6f74ed4`  
		Last Modified: Thu, 22 Apr 2021 23:34:59 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a05c19e3476eb485ff68727fc8f7cc7dfa788735e30a2b72906b844b9c3e56`  
		Last Modified: Thu, 22 Apr 2021 23:34:58 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:efb7005aa69eae8c01d32f56cf0a229b54aaf15f486b3f0c39ce1de41f19ab95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:28d9b42f5045e931f540022b50d140778296614cc46fea7fedef50e26b1584e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1080c373df8961fed31f1a39e28cc6c25d6795e0d7c3d561f2d379cf92def32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:9bb0ab90c22cd1ed787dfe4292c36984fd21bc48b2174ddad3b1e218161e3cf2 in /nats-server 
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:30 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:30 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:10c4c9fb12b776e55b0ea8d3264f808ccc5caffaf56114cb844d5cb09786a6f1`  
		Last Modified: Thu, 22 Apr 2021 23:03:33 GMT  
		Size: 4.2 MB (4225473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473fec5c1cde7c5433c3e027919086bdd598e029899936541b2ec21ddb7847b0`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:a7a2c8f7194409c4dd75c93a6f9de11db1fc17bf1737db1c06240524e0b1858e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3895594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1fb4c72cd0448a5ba37409b399e5f04057f31f629ec5be8445008c54972c7f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 22:19:49 GMT
COPY file:64e71cd1d2e9467abd40785edd59f9612f1881becc619f3bedb155000a247b80 in /nats-server 
# Thu, 22 Apr 2021 22:19:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 22:19:51 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 22:19:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:238304e519d8648cca435478a5cebd819ed4063a311feaa2db6ec68565dde2d9`  
		Last Modified: Thu, 22 Apr 2021 22:20:38 GMT  
		Size: 3.9 MB (3895118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7507e43fa5a0838f598dd2a7130b2a5a79aa79cd6a06a73a1836fc2e6d6b5`  
		Last Modified: Thu, 22 Apr 2021 22:20:35 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:7a8f74c069f07b3f0b1351bc3aa1e2894ecc216e60c645973dcc81d261801b1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369c32ee391f07aae82ebd5e96f68ab9f24da31ffc8c257980974aaae2c38302`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:41 GMT
COPY file:4b22e9e541a652ab24ae042aa5e507153db95686a925c860d8e1d0d6abad10a3 in /nats-server 
# Thu, 22 Apr 2021 23:02:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:43 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:44 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65dc194b502e4ec7533d01c0251af4373a42f1054f5dc600b8d4aa96c6697a99`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 3.9 MB (3891497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bcc4ebf70a26891fd7de222893f55bb8968e80212d8fdba06e24381f864e08`  
		Last Modified: Thu, 22 Apr 2021 23:03:31 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8b6b6b66c99dbfca177d9c18db7748068af5b7b397ff6444bef7d8c5df1ba19
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3865538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2844c33ced18f889b04345db4c42c57c97e38a0c8a922035c8e9833f3c3062`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:34:22 GMT
COPY file:7c26ed7ed2d57f80534f12bf79cbe9c116a73d781f8e5d610a54d82baca800a3 in /nats-server 
# Thu, 22 Apr 2021 23:34:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:34:24 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:34:26 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:34:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3946fb3fc24631b9897efde5d957a63512d59c5745a8d0b8a4dca3171d07f77b`  
		Last Modified: Thu, 22 Apr 2021 23:35:18 GMT  
		Size: 3.9 MB (3865066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9203e1c4fb17a9b11e7579ecba8ba11004c1f5565dd8a2cd3d2fc45182152a6`  
		Last Modified: Thu, 22 Apr 2021 23:35:17 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:cc81cb52f172686a965e1c4e8a55c36dc45bbf434782b00bb9f13b023b4e25c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:919213b7bc91d2592c5d1312c0a4afc4191259685c87e5411af02b2f857c7f22
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105629134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c2735946f6f419fec4d9b2c7c5ef0d1de10fcb5bed1024117d3bdecf2ab3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 Apr 2021 22:17:39 GMT
RUN cmd /S /C #(nop) COPY file:0bab6ea83b560e32beee362f5586c34607d68bc8fc2e12422611f377373c3392 in C:\nats-server.exe 
# Thu, 22 Apr 2021 22:17:40 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84508bc2e91e9b08b6992021bcf6575304a72e75fe2e112017331b04d5edc6b8`  
		Last Modified: Thu, 22 Apr 2021 22:32:27 GMT  
		Size: 4.3 MB (4282564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62907c5116573f0b8237cef0b1b52331d4945c3fed33b88e5c961e2f505420a9`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ae9d391bb3e00f300812200277f9faee92744173d7324e3993ef169a0cd1eb`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62014e35aec6648734dd1a046b17cd77df9db4b2f8b17d2272e303ae3b97903a`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908266ff2e3c49a426faa0a3fd232a8d8556b9bd9361c046faaa764058830852`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:cc81cb52f172686a965e1c4e8a55c36dc45bbf434782b00bb9f13b023b4e25c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:919213b7bc91d2592c5d1312c0a4afc4191259685c87e5411af02b2f857c7f22
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105629134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c2735946f6f419fec4d9b2c7c5ef0d1de10fcb5bed1024117d3bdecf2ab3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 Apr 2021 22:17:39 GMT
RUN cmd /S /C #(nop) COPY file:0bab6ea83b560e32beee362f5586c34607d68bc8fc2e12422611f377373c3392 in C:\nats-server.exe 
# Thu, 22 Apr 2021 22:17:40 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84508bc2e91e9b08b6992021bcf6575304a72e75fe2e112017331b04d5edc6b8`  
		Last Modified: Thu, 22 Apr 2021 22:32:27 GMT  
		Size: 4.3 MB (4282564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62907c5116573f0b8237cef0b1b52331d4945c3fed33b88e5c961e2f505420a9`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ae9d391bb3e00f300812200277f9faee92744173d7324e3993ef169a0cd1eb`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62014e35aec6648734dd1a046b17cd77df9db4b2f8b17d2272e303ae3b97903a`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908266ff2e3c49a426faa0a3fd232a8d8556b9bd9361c046faaa764058830852`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:efb7005aa69eae8c01d32f56cf0a229b54aaf15f486b3f0c39ce1de41f19ab95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:28d9b42f5045e931f540022b50d140778296614cc46fea7fedef50e26b1584e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1080c373df8961fed31f1a39e28cc6c25d6795e0d7c3d561f2d379cf92def32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:9bb0ab90c22cd1ed787dfe4292c36984fd21bc48b2174ddad3b1e218161e3cf2 in /nats-server 
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:30 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:30 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:10c4c9fb12b776e55b0ea8d3264f808ccc5caffaf56114cb844d5cb09786a6f1`  
		Last Modified: Thu, 22 Apr 2021 23:03:33 GMT  
		Size: 4.2 MB (4225473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473fec5c1cde7c5433c3e027919086bdd598e029899936541b2ec21ddb7847b0`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:a7a2c8f7194409c4dd75c93a6f9de11db1fc17bf1737db1c06240524e0b1858e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3895594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1fb4c72cd0448a5ba37409b399e5f04057f31f629ec5be8445008c54972c7f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 22:19:49 GMT
COPY file:64e71cd1d2e9467abd40785edd59f9612f1881becc619f3bedb155000a247b80 in /nats-server 
# Thu, 22 Apr 2021 22:19:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 22:19:51 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 22:19:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:238304e519d8648cca435478a5cebd819ed4063a311feaa2db6ec68565dde2d9`  
		Last Modified: Thu, 22 Apr 2021 22:20:38 GMT  
		Size: 3.9 MB (3895118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7507e43fa5a0838f598dd2a7130b2a5a79aa79cd6a06a73a1836fc2e6d6b5`  
		Last Modified: Thu, 22 Apr 2021 22:20:35 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:7a8f74c069f07b3f0b1351bc3aa1e2894ecc216e60c645973dcc81d261801b1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369c32ee391f07aae82ebd5e96f68ab9f24da31ffc8c257980974aaae2c38302`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:41 GMT
COPY file:4b22e9e541a652ab24ae042aa5e507153db95686a925c860d8e1d0d6abad10a3 in /nats-server 
# Thu, 22 Apr 2021 23:02:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:43 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:44 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65dc194b502e4ec7533d01c0251af4373a42f1054f5dc600b8d4aa96c6697a99`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 3.9 MB (3891497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bcc4ebf70a26891fd7de222893f55bb8968e80212d8fdba06e24381f864e08`  
		Last Modified: Thu, 22 Apr 2021 23:03:31 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8b6b6b66c99dbfca177d9c18db7748068af5b7b397ff6444bef7d8c5df1ba19
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3865538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2844c33ced18f889b04345db4c42c57c97e38a0c8a922035c8e9833f3c3062`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:34:22 GMT
COPY file:7c26ed7ed2d57f80534f12bf79cbe9c116a73d781f8e5d610a54d82baca800a3 in /nats-server 
# Thu, 22 Apr 2021 23:34:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:34:24 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:34:26 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:34:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3946fb3fc24631b9897efde5d957a63512d59c5745a8d0b8a4dca3171d07f77b`  
		Last Modified: Thu, 22 Apr 2021 23:35:18 GMT  
		Size: 3.9 MB (3865066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9203e1c4fb17a9b11e7579ecba8ba11004c1f5565dd8a2cd3d2fc45182152a6`  
		Last Modified: Thu, 22 Apr 2021 23:35:17 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:f8aac4b9cb4f642b2321c022c9d1273dad124d675bc48350043d8d0545ebaeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:58530c714d3a11ce4a69f36a318e08afa88440e0e4422dbf1102fed3efd596aa
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484209021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fee09ecc70f2cc3c43c0cb0d789a146b38405b764a400d452b89c335237e0c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Thu, 22 Apr 2021 22:15:14 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 22:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.2/nats-server-v2.2.2-windows-amd64.zip
# Thu, 22 Apr 2021 22:15:16 GMT
ENV GIT_DOWNLOAD_SHA256=644355111c8c31f129c962c3a2155041b8180c24dbe96353aaf31ce4dad25323
# Thu, 22 Apr 2021 22:15:59 GMT
RUN Set-PSDebug -Trace 2
# Thu, 22 Apr 2021 22:17:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 22 Apr 2021 22:17:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:16 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:18 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:9dc8f380778a8fd6b45de9b5c946a271bf272be729d066af5debbf40b12b7ec6`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb870516d41ed84b6f1bc0c60f0292342faeb98ae36340263425c735c1d28207`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98483cb65c9a5eee99c6e13f0d3cbe60b74547d81daeea891ae6726b003fea90`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6427780ae4e264dc775f5839a75c2ec3d102e7eb5cceb82b8755da23cb914f`  
		Last Modified: Thu, 22 Apr 2021 22:32:08 GMT  
		Size: 5.1 MB (5096294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b7a72b5ad5da2a8b5d04b05e199197127cdc0b77cd7ab256c1516a755ba461`  
		Last Modified: Thu, 22 Apr 2021 22:32:05 GMT  
		Size: 9.3 MB (9345478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d311a269622fcb4dbe064c650275cfb2da7df6070321b2eb1cc145fe9cc4d9`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 2.0 KB (1979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57c89d18cecb9ca10c1fb20c99fe03e263b36076914ede701f1c5a177fb6d29`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f12892bce1ff32498c5b6ee2685913a50ea0dd167aa5c55287c0464b8870c`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8884915b930db27ebd06dcd60062b41f4839548438632cb23f51876ed85a3397`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:f8aac4b9cb4f642b2321c022c9d1273dad124d675bc48350043d8d0545ebaeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:58530c714d3a11ce4a69f36a318e08afa88440e0e4422dbf1102fed3efd596aa
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484209021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fee09ecc70f2cc3c43c0cb0d789a146b38405b764a400d452b89c335237e0c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Thu, 22 Apr 2021 22:15:14 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 22:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.2/nats-server-v2.2.2-windows-amd64.zip
# Thu, 22 Apr 2021 22:15:16 GMT
ENV GIT_DOWNLOAD_SHA256=644355111c8c31f129c962c3a2155041b8180c24dbe96353aaf31ce4dad25323
# Thu, 22 Apr 2021 22:15:59 GMT
RUN Set-PSDebug -Trace 2
# Thu, 22 Apr 2021 22:17:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 22 Apr 2021 22:17:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:16 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:18 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:9dc8f380778a8fd6b45de9b5c946a271bf272be729d066af5debbf40b12b7ec6`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb870516d41ed84b6f1bc0c60f0292342faeb98ae36340263425c735c1d28207`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98483cb65c9a5eee99c6e13f0d3cbe60b74547d81daeea891ae6726b003fea90`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6427780ae4e264dc775f5839a75c2ec3d102e7eb5cceb82b8755da23cb914f`  
		Last Modified: Thu, 22 Apr 2021 22:32:08 GMT  
		Size: 5.1 MB (5096294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b7a72b5ad5da2a8b5d04b05e199197127cdc0b77cd7ab256c1516a755ba461`  
		Last Modified: Thu, 22 Apr 2021 22:32:05 GMT  
		Size: 9.3 MB (9345478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d311a269622fcb4dbe064c650275cfb2da7df6070321b2eb1cc145fe9cc4d9`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 2.0 KB (1979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57c89d18cecb9ca10c1fb20c99fe03e263b36076914ede701f1c5a177fb6d29`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f12892bce1ff32498c5b6ee2685913a50ea0dd167aa5c55287c0464b8870c`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8884915b930db27ebd06dcd60062b41f4839548438632cb23f51876ed85a3397`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:486439b61d7c8307b15b01bae5f574784e333ee642d1d3285e3bf61785ea00cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull nats@sha256:ad5ac25aa423d2df82324037dd73fec641098cd5f198cf98ccf19f4ae640d1f5
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5814950471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc9b58b0a6e7d867ee74a6023bf1768d2dad684760ace428c0bf425357fcc5c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Wed, 14 Apr 2021 16:05:33 GMT
ENV NATS_SERVER=2.2.1
# Wed, 14 Apr 2021 16:05:35 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.1/nats-server-v2.2.1-windows-amd64.zip
# Wed, 14 Apr 2021 16:05:35 GMT
ENV GIT_DOWNLOAD_SHA256=1f0d48a7ba9200e2572016a9f3e1ec7e630f0518cc0b40950c14ff3a5d900924
# Wed, 14 Apr 2021 16:06:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 16:09:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 16:09:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:09:20 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:09:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:09:23 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:04d71ba1c574073f9d5dd016585c2fe26ac560c192f7aa36ce54d4c12832997f`  
		Last Modified: Wed, 14 Apr 2021 16:11:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9f66539738348100cf9f1e6a5bc40e8c2123bafb9329f5df3cf20a2015db33`  
		Last Modified: Wed, 14 Apr 2021 16:11:00 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f2eae922462b2537c1d0d32d548cb10190f6bda0d02da57440cc229da692b3`  
		Last Modified: Wed, 14 Apr 2021 16:11:00 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea168f84532f340be87f19704511ee160cbdc5b9c6ad8962fcd80e9fb8efea7`  
		Last Modified: Wed, 14 Apr 2021 16:11:01 GMT  
		Size: 5.7 MB (5651953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eda2d9556eb5afaf10e6300ac36ddc1383144ae65671ca3a01b24bac150c540`  
		Last Modified: Wed, 14 Apr 2021 16:11:01 GMT  
		Size: 14.4 MB (14401439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a04b0d9d602bb1f9c6fb7925bb92959ebcff2c30e6ca6a658cdd9976d662d70`  
		Last Modified: Wed, 14 Apr 2021 16:10:57 GMT  
		Size: 2.0 KB (1984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5e865356a464c9006414a165a6d0ffb8f062fa737be2ad42e1aa58fcfca23c`  
		Last Modified: Wed, 14 Apr 2021 16:10:56 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3533148ddde03cc5f28669b26c30dee8685db418d250a4b4829e465c0be8a7e`  
		Last Modified: Wed, 14 Apr 2021 16:10:56 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4573099491ec9887bd66033f55b39f6b897d1f59f21f679fdff4f822ebd7ea15`  
		Last Modified: Wed, 14 Apr 2021 16:10:56 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2`

```console
$ docker pull nats@sha256:2e6c786ed41cd0411448a9a82407ae18dde139150e6fe0869db2c8b98913df90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1879; amd64

### `nats:2.2` - linux; amd64

```console
$ docker pull nats@sha256:28d9b42f5045e931f540022b50d140778296614cc46fea7fedef50e26b1584e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1080c373df8961fed31f1a39e28cc6c25d6795e0d7c3d561f2d379cf92def32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:9bb0ab90c22cd1ed787dfe4292c36984fd21bc48b2174ddad3b1e218161e3cf2 in /nats-server 
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:30 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:30 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:10c4c9fb12b776e55b0ea8d3264f808ccc5caffaf56114cb844d5cb09786a6f1`  
		Last Modified: Thu, 22 Apr 2021 23:03:33 GMT  
		Size: 4.2 MB (4225473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473fec5c1cde7c5433c3e027919086bdd598e029899936541b2ec21ddb7847b0`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2` - linux; arm variant v6

```console
$ docker pull nats@sha256:a7a2c8f7194409c4dd75c93a6f9de11db1fc17bf1737db1c06240524e0b1858e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3895594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1fb4c72cd0448a5ba37409b399e5f04057f31f629ec5be8445008c54972c7f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 22:19:49 GMT
COPY file:64e71cd1d2e9467abd40785edd59f9612f1881becc619f3bedb155000a247b80 in /nats-server 
# Thu, 22 Apr 2021 22:19:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 22:19:51 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 22:19:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:238304e519d8648cca435478a5cebd819ed4063a311feaa2db6ec68565dde2d9`  
		Last Modified: Thu, 22 Apr 2021 22:20:38 GMT  
		Size: 3.9 MB (3895118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7507e43fa5a0838f598dd2a7130b2a5a79aa79cd6a06a73a1836fc2e6d6b5`  
		Last Modified: Thu, 22 Apr 2021 22:20:35 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2` - linux; arm variant v7

```console
$ docker pull nats@sha256:7a8f74c069f07b3f0b1351bc3aa1e2894ecc216e60c645973dcc81d261801b1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369c32ee391f07aae82ebd5e96f68ab9f24da31ffc8c257980974aaae2c38302`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:41 GMT
COPY file:4b22e9e541a652ab24ae042aa5e507153db95686a925c860d8e1d0d6abad10a3 in /nats-server 
# Thu, 22 Apr 2021 23:02:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:43 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:44 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65dc194b502e4ec7533d01c0251af4373a42f1054f5dc600b8d4aa96c6697a99`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 3.9 MB (3891497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bcc4ebf70a26891fd7de222893f55bb8968e80212d8fdba06e24381f864e08`  
		Last Modified: Thu, 22 Apr 2021 23:03:31 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8b6b6b66c99dbfca177d9c18db7748068af5b7b397ff6444bef7d8c5df1ba19
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3865538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2844c33ced18f889b04345db4c42c57c97e38a0c8a922035c8e9833f3c3062`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:34:22 GMT
COPY file:7c26ed7ed2d57f80534f12bf79cbe9c116a73d781f8e5d610a54d82baca800a3 in /nats-server 
# Thu, 22 Apr 2021 23:34:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:34:24 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:34:26 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:34:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3946fb3fc24631b9897efde5d957a63512d59c5745a8d0b8a4dca3171d07f77b`  
		Last Modified: Thu, 22 Apr 2021 23:35:18 GMT  
		Size: 3.9 MB (3865066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9203e1c4fb17a9b11e7579ecba8ba11004c1f5565dd8a2cd3d2fc45182152a6`  
		Last Modified: Thu, 22 Apr 2021 23:35:17 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:919213b7bc91d2592c5d1312c0a4afc4191259685c87e5411af02b2f857c7f22
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105629134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c2735946f6f419fec4d9b2c7c5ef0d1de10fcb5bed1024117d3bdecf2ab3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 Apr 2021 22:17:39 GMT
RUN cmd /S /C #(nop) COPY file:0bab6ea83b560e32beee362f5586c34607d68bc8fc2e12422611f377373c3392 in C:\nats-server.exe 
# Thu, 22 Apr 2021 22:17:40 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84508bc2e91e9b08b6992021bcf6575304a72e75fe2e112017331b04d5edc6b8`  
		Last Modified: Thu, 22 Apr 2021 22:32:27 GMT  
		Size: 4.3 MB (4282564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62907c5116573f0b8237cef0b1b52331d4945c3fed33b88e5c961e2f505420a9`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ae9d391bb3e00f300812200277f9faee92744173d7324e3993ef169a0cd1eb`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62014e35aec6648734dd1a046b17cd77df9db4b2f8b17d2272e303ae3b97903a`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908266ff2e3c49a426faa0a3fd232a8d8556b9bd9361c046faaa764058830852`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2-alpine`

```console
$ docker pull nats@sha256:a5951ad6ed2f6215ecb8a6a6aa245bc55a3ac612ddc2479dc5798d2540121dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:85bf09a4ed3123ecb7a16dbc7b9f06a257bd03c0c54d149953b5d1a2a34541e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7320048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29560428628215cddf73747b2d824f6479740731a1d2819a6d4c86a2bd8c03b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:01:56 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:02:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:02:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:02:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:02:01 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:02:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb9a564713c5c5be09227ec80bb9144b76b8542f70ea965b101aaf4b1fa53b4`  
		Last Modified: Thu, 22 Apr 2021 23:03:02 GMT  
		Size: 4.5 MB (4507111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28124858f0b78aef5b2801438e68b373ebd10fdc30a1f72a24ef20712477c8`  
		Last Modified: Thu, 22 Apr 2021 23:03:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a0a0c07581f940dea4209a67968c0ff9391514049ebbf7a5e571e4d4489742`  
		Last Modified: Thu, 22 Apr 2021 23:03:01 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c48f594973b2c6b8a6ac35419d06177ffa677c0d839d9aa820ad07b74e32967a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54260724cde664486b3039108cb2de4303dcab3684f8e76bde0e417c059d09f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 22:19:04 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 22:19:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 22:19:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 22:19:15 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 22:19:17 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 22:19:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225e3f411aa135344bc62f2742e1c53ad81de0be7ef0ba69bd0087d697095d72`  
		Last Modified: Thu, 22 Apr 2021 22:20:22 GMT  
		Size: 4.2 MB (4179946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946ec1abe0a4f7a9d236788aa4212122a4bc3c827f6b939ab69a13f7b9cca0ed`  
		Last Modified: Thu, 22 Apr 2021 22:20:21 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7167ed7e4981c0dc0102aa4c067cc5babc52159b625c9bafa71854328d8ccb05`  
		Last Modified: Thu, 22 Apr 2021 22:20:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a4e89657b36a323fabe9a59de08eea4ee63780449a82a688e04581fccf28c022
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971a7eb41bc06c66ab63ef164148b3913f1c0f62b366dc3e8a31fab3d33e9cfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:01:08 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:01:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:01:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:01:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:01:15 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:01:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:01:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d830dca5f399e6b2a26c9d5d4957df49a12ac964c46777b5052c8cdc6b90254`  
		Last Modified: Thu, 22 Apr 2021 23:03:17 GMT  
		Size: 4.2 MB (4171927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716e7fafa13bb0b3cbee84575af5654cd3b9facd11bb0d45e2722b5e0267331f`  
		Last Modified: Thu, 22 Apr 2021 23:03:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da0fc6dcd60240bdb6977965ef833756766f028b56d5ea1114476acffeb0510`  
		Last Modified: Thu, 22 Apr 2021 23:03:16 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9de557d8757ca4cdc59685058da10f7c3c90e47acdcf9100c5e9c560b16755a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6863978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77dfb5c08760abdb5ebe1228f8dc9fe7f548d16eae96e858ac2ec457a584ee10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:31:02 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:31:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:31:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:31:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:31:11 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:31:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85832337b2784bee768ef22ecd3e10c80d8259c92f4bc1a18c55d39f130dcb4a`  
		Last Modified: Thu, 22 Apr 2021 23:34:59 GMT  
		Size: 4.2 MB (4150983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa6771d491a7a8de32b346b875cfe8a23c4fd0e23573e85874dd1b3a6f74ed4`  
		Last Modified: Thu, 22 Apr 2021 23:34:59 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a05c19e3476eb485ff68727fc8f7cc7dfa788735e30a2b72906b844b9c3e56`  
		Last Modified: Thu, 22 Apr 2021 23:34:58 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2-alpine3.13`

```console
$ docker pull nats@sha256:a5951ad6ed2f6215ecb8a6a6aa245bc55a3ac612ddc2479dc5798d2540121dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.2-alpine3.13` - linux; amd64

```console
$ docker pull nats@sha256:85bf09a4ed3123ecb7a16dbc7b9f06a257bd03c0c54d149953b5d1a2a34541e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7320048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29560428628215cddf73747b2d824f6479740731a1d2819a6d4c86a2bd8c03b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:01:56 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:02:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:02:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:02:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:02:01 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:02:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb9a564713c5c5be09227ec80bb9144b76b8542f70ea965b101aaf4b1fa53b4`  
		Last Modified: Thu, 22 Apr 2021 23:03:02 GMT  
		Size: 4.5 MB (4507111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28124858f0b78aef5b2801438e68b373ebd10fdc30a1f72a24ef20712477c8`  
		Last Modified: Thu, 22 Apr 2021 23:03:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a0a0c07581f940dea4209a67968c0ff9391514049ebbf7a5e571e4d4489742`  
		Last Modified: Thu, 22 Apr 2021 23:03:01 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-alpine3.13` - linux; arm variant v6

```console
$ docker pull nats@sha256:c48f594973b2c6b8a6ac35419d06177ffa677c0d839d9aa820ad07b74e32967a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54260724cde664486b3039108cb2de4303dcab3684f8e76bde0e417c059d09f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 22:19:04 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 22:19:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 22:19:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 22:19:15 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 22:19:17 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 22:19:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225e3f411aa135344bc62f2742e1c53ad81de0be7ef0ba69bd0087d697095d72`  
		Last Modified: Thu, 22 Apr 2021 22:20:22 GMT  
		Size: 4.2 MB (4179946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946ec1abe0a4f7a9d236788aa4212122a4bc3c827f6b939ab69a13f7b9cca0ed`  
		Last Modified: Thu, 22 Apr 2021 22:20:21 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7167ed7e4981c0dc0102aa4c067cc5babc52159b625c9bafa71854328d8ccb05`  
		Last Modified: Thu, 22 Apr 2021 22:20:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-alpine3.13` - linux; arm variant v7

```console
$ docker pull nats@sha256:a4e89657b36a323fabe9a59de08eea4ee63780449a82a688e04581fccf28c022
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971a7eb41bc06c66ab63ef164148b3913f1c0f62b366dc3e8a31fab3d33e9cfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:01:08 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:01:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:01:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:01:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:01:15 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:01:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:01:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d830dca5f399e6b2a26c9d5d4957df49a12ac964c46777b5052c8cdc6b90254`  
		Last Modified: Thu, 22 Apr 2021 23:03:17 GMT  
		Size: 4.2 MB (4171927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716e7fafa13bb0b3cbee84575af5654cd3b9facd11bb0d45e2722b5e0267331f`  
		Last Modified: Thu, 22 Apr 2021 23:03:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da0fc6dcd60240bdb6977965ef833756766f028b56d5ea1114476acffeb0510`  
		Last Modified: Thu, 22 Apr 2021 23:03:16 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9de557d8757ca4cdc59685058da10f7c3c90e47acdcf9100c5e9c560b16755a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6863978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77dfb5c08760abdb5ebe1228f8dc9fe7f548d16eae96e858ac2ec457a584ee10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:31:02 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:31:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:31:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:31:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:31:11 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:31:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85832337b2784bee768ef22ecd3e10c80d8259c92f4bc1a18c55d39f130dcb4a`  
		Last Modified: Thu, 22 Apr 2021 23:34:59 GMT  
		Size: 4.2 MB (4150983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa6771d491a7a8de32b346b875cfe8a23c4fd0e23573e85874dd1b3a6f74ed4`  
		Last Modified: Thu, 22 Apr 2021 23:34:59 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a05c19e3476eb485ff68727fc8f7cc7dfa788735e30a2b72906b844b9c3e56`  
		Last Modified: Thu, 22 Apr 2021 23:34:58 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2-linux`

```console
$ docker pull nats@sha256:efb7005aa69eae8c01d32f56cf0a229b54aaf15f486b3f0c39ce1de41f19ab95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.2-linux` - linux; amd64

```console
$ docker pull nats@sha256:28d9b42f5045e931f540022b50d140778296614cc46fea7fedef50e26b1584e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1080c373df8961fed31f1a39e28cc6c25d6795e0d7c3d561f2d379cf92def32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:9bb0ab90c22cd1ed787dfe4292c36984fd21bc48b2174ddad3b1e218161e3cf2 in /nats-server 
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:30 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:30 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:10c4c9fb12b776e55b0ea8d3264f808ccc5caffaf56114cb844d5cb09786a6f1`  
		Last Modified: Thu, 22 Apr 2021 23:03:33 GMT  
		Size: 4.2 MB (4225473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473fec5c1cde7c5433c3e027919086bdd598e029899936541b2ec21ddb7847b0`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:a7a2c8f7194409c4dd75c93a6f9de11db1fc17bf1737db1c06240524e0b1858e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3895594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1fb4c72cd0448a5ba37409b399e5f04057f31f629ec5be8445008c54972c7f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 22:19:49 GMT
COPY file:64e71cd1d2e9467abd40785edd59f9612f1881becc619f3bedb155000a247b80 in /nats-server 
# Thu, 22 Apr 2021 22:19:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 22:19:51 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 22:19:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:238304e519d8648cca435478a5cebd819ed4063a311feaa2db6ec68565dde2d9`  
		Last Modified: Thu, 22 Apr 2021 22:20:38 GMT  
		Size: 3.9 MB (3895118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7507e43fa5a0838f598dd2a7130b2a5a79aa79cd6a06a73a1836fc2e6d6b5`  
		Last Modified: Thu, 22 Apr 2021 22:20:35 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:7a8f74c069f07b3f0b1351bc3aa1e2894ecc216e60c645973dcc81d261801b1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369c32ee391f07aae82ebd5e96f68ab9f24da31ffc8c257980974aaae2c38302`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:41 GMT
COPY file:4b22e9e541a652ab24ae042aa5e507153db95686a925c860d8e1d0d6abad10a3 in /nats-server 
# Thu, 22 Apr 2021 23:02:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:43 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:44 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65dc194b502e4ec7533d01c0251af4373a42f1054f5dc600b8d4aa96c6697a99`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 3.9 MB (3891497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bcc4ebf70a26891fd7de222893f55bb8968e80212d8fdba06e24381f864e08`  
		Last Modified: Thu, 22 Apr 2021 23:03:31 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8b6b6b66c99dbfca177d9c18db7748068af5b7b397ff6444bef7d8c5df1ba19
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3865538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2844c33ced18f889b04345db4c42c57c97e38a0c8a922035c8e9833f3c3062`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:34:22 GMT
COPY file:7c26ed7ed2d57f80534f12bf79cbe9c116a73d781f8e5d610a54d82baca800a3 in /nats-server 
# Thu, 22 Apr 2021 23:34:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:34:24 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:34:26 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:34:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3946fb3fc24631b9897efde5d957a63512d59c5745a8d0b8a4dca3171d07f77b`  
		Last Modified: Thu, 22 Apr 2021 23:35:18 GMT  
		Size: 3.9 MB (3865066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9203e1c4fb17a9b11e7579ecba8ba11004c1f5565dd8a2cd3d2fc45182152a6`  
		Last Modified: Thu, 22 Apr 2021 23:35:17 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2-nanoserver`

```console
$ docker pull nats@sha256:cc81cb52f172686a965e1c4e8a55c36dc45bbf434782b00bb9f13b023b4e25c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2.2-nanoserver` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:919213b7bc91d2592c5d1312c0a4afc4191259685c87e5411af02b2f857c7f22
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105629134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c2735946f6f419fec4d9b2c7c5ef0d1de10fcb5bed1024117d3bdecf2ab3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 Apr 2021 22:17:39 GMT
RUN cmd /S /C #(nop) COPY file:0bab6ea83b560e32beee362f5586c34607d68bc8fc2e12422611f377373c3392 in C:\nats-server.exe 
# Thu, 22 Apr 2021 22:17:40 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84508bc2e91e9b08b6992021bcf6575304a72e75fe2e112017331b04d5edc6b8`  
		Last Modified: Thu, 22 Apr 2021 22:32:27 GMT  
		Size: 4.3 MB (4282564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62907c5116573f0b8237cef0b1b52331d4945c3fed33b88e5c961e2f505420a9`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ae9d391bb3e00f300812200277f9faee92744173d7324e3993ef169a0cd1eb`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62014e35aec6648734dd1a046b17cd77df9db4b2f8b17d2272e303ae3b97903a`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908266ff2e3c49a426faa0a3fd232a8d8556b9bd9361c046faaa764058830852`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2-nanoserver-1809`

```console
$ docker pull nats@sha256:cc81cb52f172686a965e1c4e8a55c36dc45bbf434782b00bb9f13b023b4e25c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2.2-nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:919213b7bc91d2592c5d1312c0a4afc4191259685c87e5411af02b2f857c7f22
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105629134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c2735946f6f419fec4d9b2c7c5ef0d1de10fcb5bed1024117d3bdecf2ab3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 Apr 2021 22:17:39 GMT
RUN cmd /S /C #(nop) COPY file:0bab6ea83b560e32beee362f5586c34607d68bc8fc2e12422611f377373c3392 in C:\nats-server.exe 
# Thu, 22 Apr 2021 22:17:40 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84508bc2e91e9b08b6992021bcf6575304a72e75fe2e112017331b04d5edc6b8`  
		Last Modified: Thu, 22 Apr 2021 22:32:27 GMT  
		Size: 4.3 MB (4282564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62907c5116573f0b8237cef0b1b52331d4945c3fed33b88e5c961e2f505420a9`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ae9d391bb3e00f300812200277f9faee92744173d7324e3993ef169a0cd1eb`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62014e35aec6648734dd1a046b17cd77df9db4b2f8b17d2272e303ae3b97903a`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908266ff2e3c49a426faa0a3fd232a8d8556b9bd9361c046faaa764058830852`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2-scratch`

```console
$ docker pull nats@sha256:efb7005aa69eae8c01d32f56cf0a229b54aaf15f486b3f0c39ce1de41f19ab95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:28d9b42f5045e931f540022b50d140778296614cc46fea7fedef50e26b1584e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1080c373df8961fed31f1a39e28cc6c25d6795e0d7c3d561f2d379cf92def32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:9bb0ab90c22cd1ed787dfe4292c36984fd21bc48b2174ddad3b1e218161e3cf2 in /nats-server 
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:30 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:30 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:10c4c9fb12b776e55b0ea8d3264f808ccc5caffaf56114cb844d5cb09786a6f1`  
		Last Modified: Thu, 22 Apr 2021 23:03:33 GMT  
		Size: 4.2 MB (4225473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473fec5c1cde7c5433c3e027919086bdd598e029899936541b2ec21ddb7847b0`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:a7a2c8f7194409c4dd75c93a6f9de11db1fc17bf1737db1c06240524e0b1858e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3895594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1fb4c72cd0448a5ba37409b399e5f04057f31f629ec5be8445008c54972c7f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 22:19:49 GMT
COPY file:64e71cd1d2e9467abd40785edd59f9612f1881becc619f3bedb155000a247b80 in /nats-server 
# Thu, 22 Apr 2021 22:19:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 22:19:51 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 22:19:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:238304e519d8648cca435478a5cebd819ed4063a311feaa2db6ec68565dde2d9`  
		Last Modified: Thu, 22 Apr 2021 22:20:38 GMT  
		Size: 3.9 MB (3895118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7507e43fa5a0838f598dd2a7130b2a5a79aa79cd6a06a73a1836fc2e6d6b5`  
		Last Modified: Thu, 22 Apr 2021 22:20:35 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:7a8f74c069f07b3f0b1351bc3aa1e2894ecc216e60c645973dcc81d261801b1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369c32ee391f07aae82ebd5e96f68ab9f24da31ffc8c257980974aaae2c38302`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:41 GMT
COPY file:4b22e9e541a652ab24ae042aa5e507153db95686a925c860d8e1d0d6abad10a3 in /nats-server 
# Thu, 22 Apr 2021 23:02:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:43 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:44 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65dc194b502e4ec7533d01c0251af4373a42f1054f5dc600b8d4aa96c6697a99`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 3.9 MB (3891497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bcc4ebf70a26891fd7de222893f55bb8968e80212d8fdba06e24381f864e08`  
		Last Modified: Thu, 22 Apr 2021 23:03:31 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8b6b6b66c99dbfca177d9c18db7748068af5b7b397ff6444bef7d8c5df1ba19
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3865538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2844c33ced18f889b04345db4c42c57c97e38a0c8a922035c8e9833f3c3062`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:34:22 GMT
COPY file:7c26ed7ed2d57f80534f12bf79cbe9c116a73d781f8e5d610a54d82baca800a3 in /nats-server 
# Thu, 22 Apr 2021 23:34:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:34:24 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:34:26 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:34:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3946fb3fc24631b9897efde5d957a63512d59c5745a8d0b8a4dca3171d07f77b`  
		Last Modified: Thu, 22 Apr 2021 23:35:18 GMT  
		Size: 3.9 MB (3865066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9203e1c4fb17a9b11e7579ecba8ba11004c1f5565dd8a2cd3d2fc45182152a6`  
		Last Modified: Thu, 22 Apr 2021 23:35:17 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2-windowsservercore`

```console
$ docker pull nats@sha256:f8aac4b9cb4f642b2321c022c9d1273dad124d675bc48350043d8d0545ebaeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2.2-windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:58530c714d3a11ce4a69f36a318e08afa88440e0e4422dbf1102fed3efd596aa
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484209021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fee09ecc70f2cc3c43c0cb0d789a146b38405b764a400d452b89c335237e0c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Thu, 22 Apr 2021 22:15:14 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 22:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.2/nats-server-v2.2.2-windows-amd64.zip
# Thu, 22 Apr 2021 22:15:16 GMT
ENV GIT_DOWNLOAD_SHA256=644355111c8c31f129c962c3a2155041b8180c24dbe96353aaf31ce4dad25323
# Thu, 22 Apr 2021 22:15:59 GMT
RUN Set-PSDebug -Trace 2
# Thu, 22 Apr 2021 22:17:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 22 Apr 2021 22:17:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:16 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:18 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:9dc8f380778a8fd6b45de9b5c946a271bf272be729d066af5debbf40b12b7ec6`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb870516d41ed84b6f1bc0c60f0292342faeb98ae36340263425c735c1d28207`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98483cb65c9a5eee99c6e13f0d3cbe60b74547d81daeea891ae6726b003fea90`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6427780ae4e264dc775f5839a75c2ec3d102e7eb5cceb82b8755da23cb914f`  
		Last Modified: Thu, 22 Apr 2021 22:32:08 GMT  
		Size: 5.1 MB (5096294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b7a72b5ad5da2a8b5d04b05e199197127cdc0b77cd7ab256c1516a755ba461`  
		Last Modified: Thu, 22 Apr 2021 22:32:05 GMT  
		Size: 9.3 MB (9345478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d311a269622fcb4dbe064c650275cfb2da7df6070321b2eb1cc145fe9cc4d9`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 2.0 KB (1979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57c89d18cecb9ca10c1fb20c99fe03e263b36076914ede701f1c5a177fb6d29`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f12892bce1ff32498c5b6ee2685913a50ea0dd167aa5c55287c0464b8870c`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8884915b930db27ebd06dcd60062b41f4839548438632cb23f51876ed85a3397`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2-windowsservercore-1809`

```console
$ docker pull nats@sha256:f8aac4b9cb4f642b2321c022c9d1273dad124d675bc48350043d8d0545ebaeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2.2-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:58530c714d3a11ce4a69f36a318e08afa88440e0e4422dbf1102fed3efd596aa
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484209021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fee09ecc70f2cc3c43c0cb0d789a146b38405b764a400d452b89c335237e0c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Thu, 22 Apr 2021 22:15:14 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 22:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.2/nats-server-v2.2.2-windows-amd64.zip
# Thu, 22 Apr 2021 22:15:16 GMT
ENV GIT_DOWNLOAD_SHA256=644355111c8c31f129c962c3a2155041b8180c24dbe96353aaf31ce4dad25323
# Thu, 22 Apr 2021 22:15:59 GMT
RUN Set-PSDebug -Trace 2
# Thu, 22 Apr 2021 22:17:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 22 Apr 2021 22:17:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:16 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:18 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:9dc8f380778a8fd6b45de9b5c946a271bf272be729d066af5debbf40b12b7ec6`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb870516d41ed84b6f1bc0c60f0292342faeb98ae36340263425c735c1d28207`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98483cb65c9a5eee99c6e13f0d3cbe60b74547d81daeea891ae6726b003fea90`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6427780ae4e264dc775f5839a75c2ec3d102e7eb5cceb82b8755da23cb914f`  
		Last Modified: Thu, 22 Apr 2021 22:32:08 GMT  
		Size: 5.1 MB (5096294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b7a72b5ad5da2a8b5d04b05e199197127cdc0b77cd7ab256c1516a755ba461`  
		Last Modified: Thu, 22 Apr 2021 22:32:05 GMT  
		Size: 9.3 MB (9345478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d311a269622fcb4dbe064c650275cfb2da7df6070321b2eb1cc145fe9cc4d9`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 2.0 KB (1979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57c89d18cecb9ca10c1fb20c99fe03e263b36076914ede701f1c5a177fb6d29`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f12892bce1ff32498c5b6ee2685913a50ea0dd167aa5c55287c0464b8870c`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8884915b930db27ebd06dcd60062b41f4839548438632cb23f51876ed85a3397`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:486439b61d7c8307b15b01bae5f574784e333ee642d1d3285e3bf61785ea00cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `nats:2.2-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull nats@sha256:ad5ac25aa423d2df82324037dd73fec641098cd5f198cf98ccf19f4ae640d1f5
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5814950471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc9b58b0a6e7d867ee74a6023bf1768d2dad684760ace428c0bf425357fcc5c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Wed, 14 Apr 2021 16:05:33 GMT
ENV NATS_SERVER=2.2.1
# Wed, 14 Apr 2021 16:05:35 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.1/nats-server-v2.2.1-windows-amd64.zip
# Wed, 14 Apr 2021 16:05:35 GMT
ENV GIT_DOWNLOAD_SHA256=1f0d48a7ba9200e2572016a9f3e1ec7e630f0518cc0b40950c14ff3a5d900924
# Wed, 14 Apr 2021 16:06:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 16:09:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 16:09:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:09:20 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:09:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:09:23 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:04d71ba1c574073f9d5dd016585c2fe26ac560c192f7aa36ce54d4c12832997f`  
		Last Modified: Wed, 14 Apr 2021 16:11:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9f66539738348100cf9f1e6a5bc40e8c2123bafb9329f5df3cf20a2015db33`  
		Last Modified: Wed, 14 Apr 2021 16:11:00 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f2eae922462b2537c1d0d32d548cb10190f6bda0d02da57440cc229da692b3`  
		Last Modified: Wed, 14 Apr 2021 16:11:00 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea168f84532f340be87f19704511ee160cbdc5b9c6ad8962fcd80e9fb8efea7`  
		Last Modified: Wed, 14 Apr 2021 16:11:01 GMT  
		Size: 5.7 MB (5651953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eda2d9556eb5afaf10e6300ac36ddc1383144ae65671ca3a01b24bac150c540`  
		Last Modified: Wed, 14 Apr 2021 16:11:01 GMT  
		Size: 14.4 MB (14401439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a04b0d9d602bb1f9c6fb7925bb92959ebcff2c30e6ca6a658cdd9976d662d70`  
		Last Modified: Wed, 14 Apr 2021 16:10:57 GMT  
		Size: 2.0 KB (1984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5e865356a464c9006414a165a6d0ffb8f062fa737be2ad42e1aa58fcfca23c`  
		Last Modified: Wed, 14 Apr 2021 16:10:56 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3533148ddde03cc5f28669b26c30dee8685db418d250a4b4829e465c0be8a7e`  
		Last Modified: Wed, 14 Apr 2021 16:10:56 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4573099491ec9887bd66033f55b39f6b897d1f59f21f679fdff4f822ebd7ea15`  
		Last Modified: Wed, 14 Apr 2021 16:10:56 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2.2`

```console
$ docker pull nats@sha256:2e6c786ed41cd0411448a9a82407ae18dde139150e6fe0869db2c8b98913df90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1879; amd64

### `nats:2.2.2` - linux; amd64

```console
$ docker pull nats@sha256:28d9b42f5045e931f540022b50d140778296614cc46fea7fedef50e26b1584e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1080c373df8961fed31f1a39e28cc6c25d6795e0d7c3d561f2d379cf92def32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:9bb0ab90c22cd1ed787dfe4292c36984fd21bc48b2174ddad3b1e218161e3cf2 in /nats-server 
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:30 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:30 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:10c4c9fb12b776e55b0ea8d3264f808ccc5caffaf56114cb844d5cb09786a6f1`  
		Last Modified: Thu, 22 Apr 2021 23:03:33 GMT  
		Size: 4.2 MB (4225473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473fec5c1cde7c5433c3e027919086bdd598e029899936541b2ec21ddb7847b0`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.2` - linux; arm variant v6

```console
$ docker pull nats@sha256:a7a2c8f7194409c4dd75c93a6f9de11db1fc17bf1737db1c06240524e0b1858e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3895594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1fb4c72cd0448a5ba37409b399e5f04057f31f629ec5be8445008c54972c7f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 22:19:49 GMT
COPY file:64e71cd1d2e9467abd40785edd59f9612f1881becc619f3bedb155000a247b80 in /nats-server 
# Thu, 22 Apr 2021 22:19:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 22:19:51 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 22:19:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:238304e519d8648cca435478a5cebd819ed4063a311feaa2db6ec68565dde2d9`  
		Last Modified: Thu, 22 Apr 2021 22:20:38 GMT  
		Size: 3.9 MB (3895118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7507e43fa5a0838f598dd2a7130b2a5a79aa79cd6a06a73a1836fc2e6d6b5`  
		Last Modified: Thu, 22 Apr 2021 22:20:35 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.2` - linux; arm variant v7

```console
$ docker pull nats@sha256:7a8f74c069f07b3f0b1351bc3aa1e2894ecc216e60c645973dcc81d261801b1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369c32ee391f07aae82ebd5e96f68ab9f24da31ffc8c257980974aaae2c38302`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:41 GMT
COPY file:4b22e9e541a652ab24ae042aa5e507153db95686a925c860d8e1d0d6abad10a3 in /nats-server 
# Thu, 22 Apr 2021 23:02:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:43 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:44 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65dc194b502e4ec7533d01c0251af4373a42f1054f5dc600b8d4aa96c6697a99`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 3.9 MB (3891497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bcc4ebf70a26891fd7de222893f55bb8968e80212d8fdba06e24381f864e08`  
		Last Modified: Thu, 22 Apr 2021 23:03:31 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8b6b6b66c99dbfca177d9c18db7748068af5b7b397ff6444bef7d8c5df1ba19
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3865538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2844c33ced18f889b04345db4c42c57c97e38a0c8a922035c8e9833f3c3062`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:34:22 GMT
COPY file:7c26ed7ed2d57f80534f12bf79cbe9c116a73d781f8e5d610a54d82baca800a3 in /nats-server 
# Thu, 22 Apr 2021 23:34:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:34:24 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:34:26 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:34:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3946fb3fc24631b9897efde5d957a63512d59c5745a8d0b8a4dca3171d07f77b`  
		Last Modified: Thu, 22 Apr 2021 23:35:18 GMT  
		Size: 3.9 MB (3865066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9203e1c4fb17a9b11e7579ecba8ba11004c1f5565dd8a2cd3d2fc45182152a6`  
		Last Modified: Thu, 22 Apr 2021 23:35:17 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.2` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:919213b7bc91d2592c5d1312c0a4afc4191259685c87e5411af02b2f857c7f22
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105629134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c2735946f6f419fec4d9b2c7c5ef0d1de10fcb5bed1024117d3bdecf2ab3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 Apr 2021 22:17:39 GMT
RUN cmd /S /C #(nop) COPY file:0bab6ea83b560e32beee362f5586c34607d68bc8fc2e12422611f377373c3392 in C:\nats-server.exe 
# Thu, 22 Apr 2021 22:17:40 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84508bc2e91e9b08b6992021bcf6575304a72e75fe2e112017331b04d5edc6b8`  
		Last Modified: Thu, 22 Apr 2021 22:32:27 GMT  
		Size: 4.3 MB (4282564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62907c5116573f0b8237cef0b1b52331d4945c3fed33b88e5c961e2f505420a9`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ae9d391bb3e00f300812200277f9faee92744173d7324e3993ef169a0cd1eb`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62014e35aec6648734dd1a046b17cd77df9db4b2f8b17d2272e303ae3b97903a`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908266ff2e3c49a426faa0a3fd232a8d8556b9bd9361c046faaa764058830852`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2.2-alpine`

```console
$ docker pull nats@sha256:a5951ad6ed2f6215ecb8a6a6aa245bc55a3ac612ddc2479dc5798d2540121dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.2.2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:85bf09a4ed3123ecb7a16dbc7b9f06a257bd03c0c54d149953b5d1a2a34541e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7320048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29560428628215cddf73747b2d824f6479740731a1d2819a6d4c86a2bd8c03b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:01:56 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:02:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:02:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:02:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:02:01 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:02:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb9a564713c5c5be09227ec80bb9144b76b8542f70ea965b101aaf4b1fa53b4`  
		Last Modified: Thu, 22 Apr 2021 23:03:02 GMT  
		Size: 4.5 MB (4507111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28124858f0b78aef5b2801438e68b373ebd10fdc30a1f72a24ef20712477c8`  
		Last Modified: Thu, 22 Apr 2021 23:03:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a0a0c07581f940dea4209a67968c0ff9391514049ebbf7a5e571e4d4489742`  
		Last Modified: Thu, 22 Apr 2021 23:03:01 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c48f594973b2c6b8a6ac35419d06177ffa677c0d839d9aa820ad07b74e32967a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54260724cde664486b3039108cb2de4303dcab3684f8e76bde0e417c059d09f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 22:19:04 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 22:19:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 22:19:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 22:19:15 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 22:19:17 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 22:19:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225e3f411aa135344bc62f2742e1c53ad81de0be7ef0ba69bd0087d697095d72`  
		Last Modified: Thu, 22 Apr 2021 22:20:22 GMT  
		Size: 4.2 MB (4179946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946ec1abe0a4f7a9d236788aa4212122a4bc3c827f6b939ab69a13f7b9cca0ed`  
		Last Modified: Thu, 22 Apr 2021 22:20:21 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7167ed7e4981c0dc0102aa4c067cc5babc52159b625c9bafa71854328d8ccb05`  
		Last Modified: Thu, 22 Apr 2021 22:20:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a4e89657b36a323fabe9a59de08eea4ee63780449a82a688e04581fccf28c022
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971a7eb41bc06c66ab63ef164148b3913f1c0f62b366dc3e8a31fab3d33e9cfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:01:08 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:01:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:01:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:01:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:01:15 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:01:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:01:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d830dca5f399e6b2a26c9d5d4957df49a12ac964c46777b5052c8cdc6b90254`  
		Last Modified: Thu, 22 Apr 2021 23:03:17 GMT  
		Size: 4.2 MB (4171927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716e7fafa13bb0b3cbee84575af5654cd3b9facd11bb0d45e2722b5e0267331f`  
		Last Modified: Thu, 22 Apr 2021 23:03:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da0fc6dcd60240bdb6977965ef833756766f028b56d5ea1114476acffeb0510`  
		Last Modified: Thu, 22 Apr 2021 23:03:16 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9de557d8757ca4cdc59685058da10f7c3c90e47acdcf9100c5e9c560b16755a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6863978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77dfb5c08760abdb5ebe1228f8dc9fe7f548d16eae96e858ac2ec457a584ee10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:31:02 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:31:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:31:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:31:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:31:11 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:31:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85832337b2784bee768ef22ecd3e10c80d8259c92f4bc1a18c55d39f130dcb4a`  
		Last Modified: Thu, 22 Apr 2021 23:34:59 GMT  
		Size: 4.2 MB (4150983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa6771d491a7a8de32b346b875cfe8a23c4fd0e23573e85874dd1b3a6f74ed4`  
		Last Modified: Thu, 22 Apr 2021 23:34:59 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a05c19e3476eb485ff68727fc8f7cc7dfa788735e30a2b72906b844b9c3e56`  
		Last Modified: Thu, 22 Apr 2021 23:34:58 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2.2-alpine3.13`

```console
$ docker pull nats@sha256:a5951ad6ed2f6215ecb8a6a6aa245bc55a3ac612ddc2479dc5798d2540121dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.2.2-alpine3.13` - linux; amd64

```console
$ docker pull nats@sha256:85bf09a4ed3123ecb7a16dbc7b9f06a257bd03c0c54d149953b5d1a2a34541e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7320048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29560428628215cddf73747b2d824f6479740731a1d2819a6d4c86a2bd8c03b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:01:56 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:02:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:02:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:02:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:02:01 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:02:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb9a564713c5c5be09227ec80bb9144b76b8542f70ea965b101aaf4b1fa53b4`  
		Last Modified: Thu, 22 Apr 2021 23:03:02 GMT  
		Size: 4.5 MB (4507111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28124858f0b78aef5b2801438e68b373ebd10fdc30a1f72a24ef20712477c8`  
		Last Modified: Thu, 22 Apr 2021 23:03:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a0a0c07581f940dea4209a67968c0ff9391514049ebbf7a5e571e4d4489742`  
		Last Modified: Thu, 22 Apr 2021 23:03:01 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.2-alpine3.13` - linux; arm variant v6

```console
$ docker pull nats@sha256:c48f594973b2c6b8a6ac35419d06177ffa677c0d839d9aa820ad07b74e32967a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54260724cde664486b3039108cb2de4303dcab3684f8e76bde0e417c059d09f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 22:19:04 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 22:19:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 22:19:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 22:19:15 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 22:19:17 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 22:19:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225e3f411aa135344bc62f2742e1c53ad81de0be7ef0ba69bd0087d697095d72`  
		Last Modified: Thu, 22 Apr 2021 22:20:22 GMT  
		Size: 4.2 MB (4179946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946ec1abe0a4f7a9d236788aa4212122a4bc3c827f6b939ab69a13f7b9cca0ed`  
		Last Modified: Thu, 22 Apr 2021 22:20:21 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7167ed7e4981c0dc0102aa4c067cc5babc52159b625c9bafa71854328d8ccb05`  
		Last Modified: Thu, 22 Apr 2021 22:20:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.2-alpine3.13` - linux; arm variant v7

```console
$ docker pull nats@sha256:a4e89657b36a323fabe9a59de08eea4ee63780449a82a688e04581fccf28c022
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971a7eb41bc06c66ab63ef164148b3913f1c0f62b366dc3e8a31fab3d33e9cfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:01:08 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:01:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:01:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:01:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:01:15 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:01:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:01:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d830dca5f399e6b2a26c9d5d4957df49a12ac964c46777b5052c8cdc6b90254`  
		Last Modified: Thu, 22 Apr 2021 23:03:17 GMT  
		Size: 4.2 MB (4171927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716e7fafa13bb0b3cbee84575af5654cd3b9facd11bb0d45e2722b5e0267331f`  
		Last Modified: Thu, 22 Apr 2021 23:03:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da0fc6dcd60240bdb6977965ef833756766f028b56d5ea1114476acffeb0510`  
		Last Modified: Thu, 22 Apr 2021 23:03:16 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.2-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9de557d8757ca4cdc59685058da10f7c3c90e47acdcf9100c5e9c560b16755a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6863978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77dfb5c08760abdb5ebe1228f8dc9fe7f548d16eae96e858ac2ec457a584ee10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:31:02 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:31:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:31:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:31:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:31:11 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:31:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85832337b2784bee768ef22ecd3e10c80d8259c92f4bc1a18c55d39f130dcb4a`  
		Last Modified: Thu, 22 Apr 2021 23:34:59 GMT  
		Size: 4.2 MB (4150983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa6771d491a7a8de32b346b875cfe8a23c4fd0e23573e85874dd1b3a6f74ed4`  
		Last Modified: Thu, 22 Apr 2021 23:34:59 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a05c19e3476eb485ff68727fc8f7cc7dfa788735e30a2b72906b844b9c3e56`  
		Last Modified: Thu, 22 Apr 2021 23:34:58 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2.2-linux`

```console
$ docker pull nats@sha256:efb7005aa69eae8c01d32f56cf0a229b54aaf15f486b3f0c39ce1de41f19ab95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.2.2-linux` - linux; amd64

```console
$ docker pull nats@sha256:28d9b42f5045e931f540022b50d140778296614cc46fea7fedef50e26b1584e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1080c373df8961fed31f1a39e28cc6c25d6795e0d7c3d561f2d379cf92def32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:9bb0ab90c22cd1ed787dfe4292c36984fd21bc48b2174ddad3b1e218161e3cf2 in /nats-server 
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:30 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:30 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:10c4c9fb12b776e55b0ea8d3264f808ccc5caffaf56114cb844d5cb09786a6f1`  
		Last Modified: Thu, 22 Apr 2021 23:03:33 GMT  
		Size: 4.2 MB (4225473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473fec5c1cde7c5433c3e027919086bdd598e029899936541b2ec21ddb7847b0`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:a7a2c8f7194409c4dd75c93a6f9de11db1fc17bf1737db1c06240524e0b1858e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3895594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1fb4c72cd0448a5ba37409b399e5f04057f31f629ec5be8445008c54972c7f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 22:19:49 GMT
COPY file:64e71cd1d2e9467abd40785edd59f9612f1881becc619f3bedb155000a247b80 in /nats-server 
# Thu, 22 Apr 2021 22:19:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 22:19:51 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 22:19:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:238304e519d8648cca435478a5cebd819ed4063a311feaa2db6ec68565dde2d9`  
		Last Modified: Thu, 22 Apr 2021 22:20:38 GMT  
		Size: 3.9 MB (3895118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7507e43fa5a0838f598dd2a7130b2a5a79aa79cd6a06a73a1836fc2e6d6b5`  
		Last Modified: Thu, 22 Apr 2021 22:20:35 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:7a8f74c069f07b3f0b1351bc3aa1e2894ecc216e60c645973dcc81d261801b1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369c32ee391f07aae82ebd5e96f68ab9f24da31ffc8c257980974aaae2c38302`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:41 GMT
COPY file:4b22e9e541a652ab24ae042aa5e507153db95686a925c860d8e1d0d6abad10a3 in /nats-server 
# Thu, 22 Apr 2021 23:02:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:43 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:44 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65dc194b502e4ec7533d01c0251af4373a42f1054f5dc600b8d4aa96c6697a99`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 3.9 MB (3891497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bcc4ebf70a26891fd7de222893f55bb8968e80212d8fdba06e24381f864e08`  
		Last Modified: Thu, 22 Apr 2021 23:03:31 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8b6b6b66c99dbfca177d9c18db7748068af5b7b397ff6444bef7d8c5df1ba19
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3865538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2844c33ced18f889b04345db4c42c57c97e38a0c8a922035c8e9833f3c3062`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:34:22 GMT
COPY file:7c26ed7ed2d57f80534f12bf79cbe9c116a73d781f8e5d610a54d82baca800a3 in /nats-server 
# Thu, 22 Apr 2021 23:34:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:34:24 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:34:26 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:34:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3946fb3fc24631b9897efde5d957a63512d59c5745a8d0b8a4dca3171d07f77b`  
		Last Modified: Thu, 22 Apr 2021 23:35:18 GMT  
		Size: 3.9 MB (3865066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9203e1c4fb17a9b11e7579ecba8ba11004c1f5565dd8a2cd3d2fc45182152a6`  
		Last Modified: Thu, 22 Apr 2021 23:35:17 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2.2-nanoserver`

```console
$ docker pull nats@sha256:cc81cb52f172686a965e1c4e8a55c36dc45bbf434782b00bb9f13b023b4e25c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2.2.2-nanoserver` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:919213b7bc91d2592c5d1312c0a4afc4191259685c87e5411af02b2f857c7f22
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105629134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c2735946f6f419fec4d9b2c7c5ef0d1de10fcb5bed1024117d3bdecf2ab3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 Apr 2021 22:17:39 GMT
RUN cmd /S /C #(nop) COPY file:0bab6ea83b560e32beee362f5586c34607d68bc8fc2e12422611f377373c3392 in C:\nats-server.exe 
# Thu, 22 Apr 2021 22:17:40 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84508bc2e91e9b08b6992021bcf6575304a72e75fe2e112017331b04d5edc6b8`  
		Last Modified: Thu, 22 Apr 2021 22:32:27 GMT  
		Size: 4.3 MB (4282564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62907c5116573f0b8237cef0b1b52331d4945c3fed33b88e5c961e2f505420a9`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ae9d391bb3e00f300812200277f9faee92744173d7324e3993ef169a0cd1eb`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62014e35aec6648734dd1a046b17cd77df9db4b2f8b17d2272e303ae3b97903a`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908266ff2e3c49a426faa0a3fd232a8d8556b9bd9361c046faaa764058830852`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2.2-nanoserver-1809`

```console
$ docker pull nats@sha256:cc81cb52f172686a965e1c4e8a55c36dc45bbf434782b00bb9f13b023b4e25c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2.2.2-nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:919213b7bc91d2592c5d1312c0a4afc4191259685c87e5411af02b2f857c7f22
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105629134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c2735946f6f419fec4d9b2c7c5ef0d1de10fcb5bed1024117d3bdecf2ab3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 Apr 2021 22:17:39 GMT
RUN cmd /S /C #(nop) COPY file:0bab6ea83b560e32beee362f5586c34607d68bc8fc2e12422611f377373c3392 in C:\nats-server.exe 
# Thu, 22 Apr 2021 22:17:40 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84508bc2e91e9b08b6992021bcf6575304a72e75fe2e112017331b04d5edc6b8`  
		Last Modified: Thu, 22 Apr 2021 22:32:27 GMT  
		Size: 4.3 MB (4282564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62907c5116573f0b8237cef0b1b52331d4945c3fed33b88e5c961e2f505420a9`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ae9d391bb3e00f300812200277f9faee92744173d7324e3993ef169a0cd1eb`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62014e35aec6648734dd1a046b17cd77df9db4b2f8b17d2272e303ae3b97903a`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908266ff2e3c49a426faa0a3fd232a8d8556b9bd9361c046faaa764058830852`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2.2-scratch`

```console
$ docker pull nats@sha256:efb7005aa69eae8c01d32f56cf0a229b54aaf15f486b3f0c39ce1de41f19ab95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.2.2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:28d9b42f5045e931f540022b50d140778296614cc46fea7fedef50e26b1584e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1080c373df8961fed31f1a39e28cc6c25d6795e0d7c3d561f2d379cf92def32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:9bb0ab90c22cd1ed787dfe4292c36984fd21bc48b2174ddad3b1e218161e3cf2 in /nats-server 
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:30 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:30 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:10c4c9fb12b776e55b0ea8d3264f808ccc5caffaf56114cb844d5cb09786a6f1`  
		Last Modified: Thu, 22 Apr 2021 23:03:33 GMT  
		Size: 4.2 MB (4225473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473fec5c1cde7c5433c3e027919086bdd598e029899936541b2ec21ddb7847b0`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:a7a2c8f7194409c4dd75c93a6f9de11db1fc17bf1737db1c06240524e0b1858e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3895594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1fb4c72cd0448a5ba37409b399e5f04057f31f629ec5be8445008c54972c7f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 22:19:49 GMT
COPY file:64e71cd1d2e9467abd40785edd59f9612f1881becc619f3bedb155000a247b80 in /nats-server 
# Thu, 22 Apr 2021 22:19:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 22:19:51 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 22:19:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:238304e519d8648cca435478a5cebd819ed4063a311feaa2db6ec68565dde2d9`  
		Last Modified: Thu, 22 Apr 2021 22:20:38 GMT  
		Size: 3.9 MB (3895118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7507e43fa5a0838f598dd2a7130b2a5a79aa79cd6a06a73a1836fc2e6d6b5`  
		Last Modified: Thu, 22 Apr 2021 22:20:35 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:7a8f74c069f07b3f0b1351bc3aa1e2894ecc216e60c645973dcc81d261801b1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369c32ee391f07aae82ebd5e96f68ab9f24da31ffc8c257980974aaae2c38302`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:41 GMT
COPY file:4b22e9e541a652ab24ae042aa5e507153db95686a925c860d8e1d0d6abad10a3 in /nats-server 
# Thu, 22 Apr 2021 23:02:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:43 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:44 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65dc194b502e4ec7533d01c0251af4373a42f1054f5dc600b8d4aa96c6697a99`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 3.9 MB (3891497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bcc4ebf70a26891fd7de222893f55bb8968e80212d8fdba06e24381f864e08`  
		Last Modified: Thu, 22 Apr 2021 23:03:31 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8b6b6b66c99dbfca177d9c18db7748068af5b7b397ff6444bef7d8c5df1ba19
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3865538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2844c33ced18f889b04345db4c42c57c97e38a0c8a922035c8e9833f3c3062`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:34:22 GMT
COPY file:7c26ed7ed2d57f80534f12bf79cbe9c116a73d781f8e5d610a54d82baca800a3 in /nats-server 
# Thu, 22 Apr 2021 23:34:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:34:24 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:34:26 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:34:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3946fb3fc24631b9897efde5d957a63512d59c5745a8d0b8a4dca3171d07f77b`  
		Last Modified: Thu, 22 Apr 2021 23:35:18 GMT  
		Size: 3.9 MB (3865066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9203e1c4fb17a9b11e7579ecba8ba11004c1f5565dd8a2cd3d2fc45182152a6`  
		Last Modified: Thu, 22 Apr 2021 23:35:17 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2.2-windowsservercore`

```console
$ docker pull nats@sha256:f8aac4b9cb4f642b2321c022c9d1273dad124d675bc48350043d8d0545ebaeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2.2.2-windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:58530c714d3a11ce4a69f36a318e08afa88440e0e4422dbf1102fed3efd596aa
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484209021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fee09ecc70f2cc3c43c0cb0d789a146b38405b764a400d452b89c335237e0c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Thu, 22 Apr 2021 22:15:14 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 22:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.2/nats-server-v2.2.2-windows-amd64.zip
# Thu, 22 Apr 2021 22:15:16 GMT
ENV GIT_DOWNLOAD_SHA256=644355111c8c31f129c962c3a2155041b8180c24dbe96353aaf31ce4dad25323
# Thu, 22 Apr 2021 22:15:59 GMT
RUN Set-PSDebug -Trace 2
# Thu, 22 Apr 2021 22:17:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 22 Apr 2021 22:17:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:16 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:18 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:9dc8f380778a8fd6b45de9b5c946a271bf272be729d066af5debbf40b12b7ec6`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb870516d41ed84b6f1bc0c60f0292342faeb98ae36340263425c735c1d28207`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98483cb65c9a5eee99c6e13f0d3cbe60b74547d81daeea891ae6726b003fea90`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6427780ae4e264dc775f5839a75c2ec3d102e7eb5cceb82b8755da23cb914f`  
		Last Modified: Thu, 22 Apr 2021 22:32:08 GMT  
		Size: 5.1 MB (5096294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b7a72b5ad5da2a8b5d04b05e199197127cdc0b77cd7ab256c1516a755ba461`  
		Last Modified: Thu, 22 Apr 2021 22:32:05 GMT  
		Size: 9.3 MB (9345478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d311a269622fcb4dbe064c650275cfb2da7df6070321b2eb1cc145fe9cc4d9`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 2.0 KB (1979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57c89d18cecb9ca10c1fb20c99fe03e263b36076914ede701f1c5a177fb6d29`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f12892bce1ff32498c5b6ee2685913a50ea0dd167aa5c55287c0464b8870c`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8884915b930db27ebd06dcd60062b41f4839548438632cb23f51876ed85a3397`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2.2-windowsservercore-1809`

```console
$ docker pull nats@sha256:f8aac4b9cb4f642b2321c022c9d1273dad124d675bc48350043d8d0545ebaeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2.2.2-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:58530c714d3a11ce4a69f36a318e08afa88440e0e4422dbf1102fed3efd596aa
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484209021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fee09ecc70f2cc3c43c0cb0d789a146b38405b764a400d452b89c335237e0c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Thu, 22 Apr 2021 22:15:14 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 22:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.2/nats-server-v2.2.2-windows-amd64.zip
# Thu, 22 Apr 2021 22:15:16 GMT
ENV GIT_DOWNLOAD_SHA256=644355111c8c31f129c962c3a2155041b8180c24dbe96353aaf31ce4dad25323
# Thu, 22 Apr 2021 22:15:59 GMT
RUN Set-PSDebug -Trace 2
# Thu, 22 Apr 2021 22:17:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 22 Apr 2021 22:17:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:16 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:18 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:9dc8f380778a8fd6b45de9b5c946a271bf272be729d066af5debbf40b12b7ec6`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb870516d41ed84b6f1bc0c60f0292342faeb98ae36340263425c735c1d28207`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98483cb65c9a5eee99c6e13f0d3cbe60b74547d81daeea891ae6726b003fea90`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6427780ae4e264dc775f5839a75c2ec3d102e7eb5cceb82b8755da23cb914f`  
		Last Modified: Thu, 22 Apr 2021 22:32:08 GMT  
		Size: 5.1 MB (5096294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b7a72b5ad5da2a8b5d04b05e199197127cdc0b77cd7ab256c1516a755ba461`  
		Last Modified: Thu, 22 Apr 2021 22:32:05 GMT  
		Size: 9.3 MB (9345478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d311a269622fcb4dbe064c650275cfb2da7df6070321b2eb1cc145fe9cc4d9`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 2.0 KB (1979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57c89d18cecb9ca10c1fb20c99fe03e263b36076914ede701f1c5a177fb6d29`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f12892bce1ff32498c5b6ee2685913a50ea0dd167aa5c55287c0464b8870c`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8884915b930db27ebd06dcd60062b41f4839548438632cb23f51876ed85a3397`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2.2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `nats:alpine`

```console
$ docker pull nats@sha256:a5951ad6ed2f6215ecb8a6a6aa245bc55a3ac612ddc2479dc5798d2540121dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:85bf09a4ed3123ecb7a16dbc7b9f06a257bd03c0c54d149953b5d1a2a34541e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7320048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29560428628215cddf73747b2d824f6479740731a1d2819a6d4c86a2bd8c03b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:01:56 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:02:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:02:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:02:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:02:01 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:02:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb9a564713c5c5be09227ec80bb9144b76b8542f70ea965b101aaf4b1fa53b4`  
		Last Modified: Thu, 22 Apr 2021 23:03:02 GMT  
		Size: 4.5 MB (4507111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28124858f0b78aef5b2801438e68b373ebd10fdc30a1f72a24ef20712477c8`  
		Last Modified: Thu, 22 Apr 2021 23:03:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a0a0c07581f940dea4209a67968c0ff9391514049ebbf7a5e571e4d4489742`  
		Last Modified: Thu, 22 Apr 2021 23:03:01 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c48f594973b2c6b8a6ac35419d06177ffa677c0d839d9aa820ad07b74e32967a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54260724cde664486b3039108cb2de4303dcab3684f8e76bde0e417c059d09f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 22:19:04 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 22:19:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 22:19:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 22:19:15 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 22:19:17 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 22:19:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225e3f411aa135344bc62f2742e1c53ad81de0be7ef0ba69bd0087d697095d72`  
		Last Modified: Thu, 22 Apr 2021 22:20:22 GMT  
		Size: 4.2 MB (4179946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946ec1abe0a4f7a9d236788aa4212122a4bc3c827f6b939ab69a13f7b9cca0ed`  
		Last Modified: Thu, 22 Apr 2021 22:20:21 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7167ed7e4981c0dc0102aa4c067cc5babc52159b625c9bafa71854328d8ccb05`  
		Last Modified: Thu, 22 Apr 2021 22:20:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a4e89657b36a323fabe9a59de08eea4ee63780449a82a688e04581fccf28c022
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971a7eb41bc06c66ab63ef164148b3913f1c0f62b366dc3e8a31fab3d33e9cfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:01:08 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:01:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:01:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:01:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:01:15 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:01:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:01:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d830dca5f399e6b2a26c9d5d4957df49a12ac964c46777b5052c8cdc6b90254`  
		Last Modified: Thu, 22 Apr 2021 23:03:17 GMT  
		Size: 4.2 MB (4171927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716e7fafa13bb0b3cbee84575af5654cd3b9facd11bb0d45e2722b5e0267331f`  
		Last Modified: Thu, 22 Apr 2021 23:03:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da0fc6dcd60240bdb6977965ef833756766f028b56d5ea1114476acffeb0510`  
		Last Modified: Thu, 22 Apr 2021 23:03:16 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9de557d8757ca4cdc59685058da10f7c3c90e47acdcf9100c5e9c560b16755a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6863978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77dfb5c08760abdb5ebe1228f8dc9fe7f548d16eae96e858ac2ec457a584ee10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:31:02 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:31:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:31:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:31:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:31:11 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:31:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85832337b2784bee768ef22ecd3e10c80d8259c92f4bc1a18c55d39f130dcb4a`  
		Last Modified: Thu, 22 Apr 2021 23:34:59 GMT  
		Size: 4.2 MB (4150983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa6771d491a7a8de32b346b875cfe8a23c4fd0e23573e85874dd1b3a6f74ed4`  
		Last Modified: Thu, 22 Apr 2021 23:34:59 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a05c19e3476eb485ff68727fc8f7cc7dfa788735e30a2b72906b844b9c3e56`  
		Last Modified: Thu, 22 Apr 2021 23:34:58 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.13`

```console
$ docker pull nats@sha256:a5951ad6ed2f6215ecb8a6a6aa245bc55a3ac612ddc2479dc5798d2540121dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.13` - linux; amd64

```console
$ docker pull nats@sha256:85bf09a4ed3123ecb7a16dbc7b9f06a257bd03c0c54d149953b5d1a2a34541e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7320048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29560428628215cddf73747b2d824f6479740731a1d2819a6d4c86a2bd8c03b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:01:56 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:02:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:02:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:02:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:02:01 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:02:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb9a564713c5c5be09227ec80bb9144b76b8542f70ea965b101aaf4b1fa53b4`  
		Last Modified: Thu, 22 Apr 2021 23:03:02 GMT  
		Size: 4.5 MB (4507111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28124858f0b78aef5b2801438e68b373ebd10fdc30a1f72a24ef20712477c8`  
		Last Modified: Thu, 22 Apr 2021 23:03:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a0a0c07581f940dea4209a67968c0ff9391514049ebbf7a5e571e4d4489742`  
		Last Modified: Thu, 22 Apr 2021 23:03:01 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.13` - linux; arm variant v6

```console
$ docker pull nats@sha256:c48f594973b2c6b8a6ac35419d06177ffa677c0d839d9aa820ad07b74e32967a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54260724cde664486b3039108cb2de4303dcab3684f8e76bde0e417c059d09f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 22:19:04 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 22:19:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 22:19:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 22:19:15 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 22:19:17 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 22:19:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225e3f411aa135344bc62f2742e1c53ad81de0be7ef0ba69bd0087d697095d72`  
		Last Modified: Thu, 22 Apr 2021 22:20:22 GMT  
		Size: 4.2 MB (4179946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946ec1abe0a4f7a9d236788aa4212122a4bc3c827f6b939ab69a13f7b9cca0ed`  
		Last Modified: Thu, 22 Apr 2021 22:20:21 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7167ed7e4981c0dc0102aa4c067cc5babc52159b625c9bafa71854328d8ccb05`  
		Last Modified: Thu, 22 Apr 2021 22:20:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.13` - linux; arm variant v7

```console
$ docker pull nats@sha256:a4e89657b36a323fabe9a59de08eea4ee63780449a82a688e04581fccf28c022
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971a7eb41bc06c66ab63ef164148b3913f1c0f62b366dc3e8a31fab3d33e9cfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:01:08 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:01:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:01:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:01:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:01:15 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:01:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:01:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d830dca5f399e6b2a26c9d5d4957df49a12ac964c46777b5052c8cdc6b90254`  
		Last Modified: Thu, 22 Apr 2021 23:03:17 GMT  
		Size: 4.2 MB (4171927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716e7fafa13bb0b3cbee84575af5654cd3b9facd11bb0d45e2722b5e0267331f`  
		Last Modified: Thu, 22 Apr 2021 23:03:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da0fc6dcd60240bdb6977965ef833756766f028b56d5ea1114476acffeb0510`  
		Last Modified: Thu, 22 Apr 2021 23:03:16 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9de557d8757ca4cdc59685058da10f7c3c90e47acdcf9100c5e9c560b16755a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6863978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77dfb5c08760abdb5ebe1228f8dc9fe7f548d16eae96e858ac2ec457a584ee10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 23:31:02 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 23:31:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='761b07893a86d26fd1defa058fcd4aec624e04c1d1063cb7fae6c9225a760884' ;; 		armhf) natsArch='arm6'; sha256='73e7fbcfae4b35695007d0a42c3553ee3f37b78e386e85a3dafe733cb07a3be1' ;; 		armv7) natsArch='arm7'; sha256='7f611c596cf34f96ffd8185b9e4be917bcaf377cdaf23bef2964a3d6348b50ba' ;; 		x86_64) natsArch='amd64'; sha256='21c980037f776d0402fce81fef1e1a4a4b55648131cd9c6c18f09165eefcc16d' ;; 		x86) natsArch='386'; sha256='59f193d5307f431b5293566ef180bc0f51090246bf9f31e5fffdf6e22f58f643' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 22 Apr 2021 23:31:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 22 Apr 2021 23:31:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Apr 2021 23:31:11 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 23:31:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85832337b2784bee768ef22ecd3e10c80d8259c92f4bc1a18c55d39f130dcb4a`  
		Last Modified: Thu, 22 Apr 2021 23:34:59 GMT  
		Size: 4.2 MB (4150983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa6771d491a7a8de32b346b875cfe8a23c4fd0e23573e85874dd1b3a6f74ed4`  
		Last Modified: Thu, 22 Apr 2021 23:34:59 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a05c19e3476eb485ff68727fc8f7cc7dfa788735e30a2b72906b844b9c3e56`  
		Last Modified: Thu, 22 Apr 2021 23:34:58 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:2e6c786ed41cd0411448a9a82407ae18dde139150e6fe0869db2c8b98913df90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1879; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:28d9b42f5045e931f540022b50d140778296614cc46fea7fedef50e26b1584e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1080c373df8961fed31f1a39e28cc6c25d6795e0d7c3d561f2d379cf92def32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:9bb0ab90c22cd1ed787dfe4292c36984fd21bc48b2174ddad3b1e218161e3cf2 in /nats-server 
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:30 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:30 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:10c4c9fb12b776e55b0ea8d3264f808ccc5caffaf56114cb844d5cb09786a6f1`  
		Last Modified: Thu, 22 Apr 2021 23:03:33 GMT  
		Size: 4.2 MB (4225473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473fec5c1cde7c5433c3e027919086bdd598e029899936541b2ec21ddb7847b0`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:a7a2c8f7194409c4dd75c93a6f9de11db1fc17bf1737db1c06240524e0b1858e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3895594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1fb4c72cd0448a5ba37409b399e5f04057f31f629ec5be8445008c54972c7f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 22:19:49 GMT
COPY file:64e71cd1d2e9467abd40785edd59f9612f1881becc619f3bedb155000a247b80 in /nats-server 
# Thu, 22 Apr 2021 22:19:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 22:19:51 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 22:19:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:238304e519d8648cca435478a5cebd819ed4063a311feaa2db6ec68565dde2d9`  
		Last Modified: Thu, 22 Apr 2021 22:20:38 GMT  
		Size: 3.9 MB (3895118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7507e43fa5a0838f598dd2a7130b2a5a79aa79cd6a06a73a1836fc2e6d6b5`  
		Last Modified: Thu, 22 Apr 2021 22:20:35 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:7a8f74c069f07b3f0b1351bc3aa1e2894ecc216e60c645973dcc81d261801b1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369c32ee391f07aae82ebd5e96f68ab9f24da31ffc8c257980974aaae2c38302`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:41 GMT
COPY file:4b22e9e541a652ab24ae042aa5e507153db95686a925c860d8e1d0d6abad10a3 in /nats-server 
# Thu, 22 Apr 2021 23:02:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:43 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:44 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65dc194b502e4ec7533d01c0251af4373a42f1054f5dc600b8d4aa96c6697a99`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 3.9 MB (3891497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bcc4ebf70a26891fd7de222893f55bb8968e80212d8fdba06e24381f864e08`  
		Last Modified: Thu, 22 Apr 2021 23:03:31 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8b6b6b66c99dbfca177d9c18db7748068af5b7b397ff6444bef7d8c5df1ba19
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3865538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2844c33ced18f889b04345db4c42c57c97e38a0c8a922035c8e9833f3c3062`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:34:22 GMT
COPY file:7c26ed7ed2d57f80534f12bf79cbe9c116a73d781f8e5d610a54d82baca800a3 in /nats-server 
# Thu, 22 Apr 2021 23:34:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:34:24 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:34:26 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:34:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3946fb3fc24631b9897efde5d957a63512d59c5745a8d0b8a4dca3171d07f77b`  
		Last Modified: Thu, 22 Apr 2021 23:35:18 GMT  
		Size: 3.9 MB (3865066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9203e1c4fb17a9b11e7579ecba8ba11004c1f5565dd8a2cd3d2fc45182152a6`  
		Last Modified: Thu, 22 Apr 2021 23:35:17 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:919213b7bc91d2592c5d1312c0a4afc4191259685c87e5411af02b2f857c7f22
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105629134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c2735946f6f419fec4d9b2c7c5ef0d1de10fcb5bed1024117d3bdecf2ab3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 Apr 2021 22:17:39 GMT
RUN cmd /S /C #(nop) COPY file:0bab6ea83b560e32beee362f5586c34607d68bc8fc2e12422611f377373c3392 in C:\nats-server.exe 
# Thu, 22 Apr 2021 22:17:40 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84508bc2e91e9b08b6992021bcf6575304a72e75fe2e112017331b04d5edc6b8`  
		Last Modified: Thu, 22 Apr 2021 22:32:27 GMT  
		Size: 4.3 MB (4282564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62907c5116573f0b8237cef0b1b52331d4945c3fed33b88e5c961e2f505420a9`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ae9d391bb3e00f300812200277f9faee92744173d7324e3993ef169a0cd1eb`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62014e35aec6648734dd1a046b17cd77df9db4b2f8b17d2272e303ae3b97903a`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908266ff2e3c49a426faa0a3fd232a8d8556b9bd9361c046faaa764058830852`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:efb7005aa69eae8c01d32f56cf0a229b54aaf15f486b3f0c39ce1de41f19ab95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:28d9b42f5045e931f540022b50d140778296614cc46fea7fedef50e26b1584e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1080c373df8961fed31f1a39e28cc6c25d6795e0d7c3d561f2d379cf92def32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:9bb0ab90c22cd1ed787dfe4292c36984fd21bc48b2174ddad3b1e218161e3cf2 in /nats-server 
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:30 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:30 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:10c4c9fb12b776e55b0ea8d3264f808ccc5caffaf56114cb844d5cb09786a6f1`  
		Last Modified: Thu, 22 Apr 2021 23:03:33 GMT  
		Size: 4.2 MB (4225473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473fec5c1cde7c5433c3e027919086bdd598e029899936541b2ec21ddb7847b0`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:a7a2c8f7194409c4dd75c93a6f9de11db1fc17bf1737db1c06240524e0b1858e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3895594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1fb4c72cd0448a5ba37409b399e5f04057f31f629ec5be8445008c54972c7f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 22:19:49 GMT
COPY file:64e71cd1d2e9467abd40785edd59f9612f1881becc619f3bedb155000a247b80 in /nats-server 
# Thu, 22 Apr 2021 22:19:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 22:19:51 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 22:19:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:238304e519d8648cca435478a5cebd819ed4063a311feaa2db6ec68565dde2d9`  
		Last Modified: Thu, 22 Apr 2021 22:20:38 GMT  
		Size: 3.9 MB (3895118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7507e43fa5a0838f598dd2a7130b2a5a79aa79cd6a06a73a1836fc2e6d6b5`  
		Last Modified: Thu, 22 Apr 2021 22:20:35 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:7a8f74c069f07b3f0b1351bc3aa1e2894ecc216e60c645973dcc81d261801b1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369c32ee391f07aae82ebd5e96f68ab9f24da31ffc8c257980974aaae2c38302`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:41 GMT
COPY file:4b22e9e541a652ab24ae042aa5e507153db95686a925c860d8e1d0d6abad10a3 in /nats-server 
# Thu, 22 Apr 2021 23:02:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:43 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:44 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65dc194b502e4ec7533d01c0251af4373a42f1054f5dc600b8d4aa96c6697a99`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 3.9 MB (3891497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bcc4ebf70a26891fd7de222893f55bb8968e80212d8fdba06e24381f864e08`  
		Last Modified: Thu, 22 Apr 2021 23:03:31 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8b6b6b66c99dbfca177d9c18db7748068af5b7b397ff6444bef7d8c5df1ba19
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3865538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2844c33ced18f889b04345db4c42c57c97e38a0c8a922035c8e9833f3c3062`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:34:22 GMT
COPY file:7c26ed7ed2d57f80534f12bf79cbe9c116a73d781f8e5d610a54d82baca800a3 in /nats-server 
# Thu, 22 Apr 2021 23:34:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:34:24 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:34:26 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:34:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3946fb3fc24631b9897efde5d957a63512d59c5745a8d0b8a4dca3171d07f77b`  
		Last Modified: Thu, 22 Apr 2021 23:35:18 GMT  
		Size: 3.9 MB (3865066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9203e1c4fb17a9b11e7579ecba8ba11004c1f5565dd8a2cd3d2fc45182152a6`  
		Last Modified: Thu, 22 Apr 2021 23:35:17 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:cc81cb52f172686a965e1c4e8a55c36dc45bbf434782b00bb9f13b023b4e25c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:nanoserver` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:919213b7bc91d2592c5d1312c0a4afc4191259685c87e5411af02b2f857c7f22
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105629134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c2735946f6f419fec4d9b2c7c5ef0d1de10fcb5bed1024117d3bdecf2ab3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 Apr 2021 22:17:39 GMT
RUN cmd /S /C #(nop) COPY file:0bab6ea83b560e32beee362f5586c34607d68bc8fc2e12422611f377373c3392 in C:\nats-server.exe 
# Thu, 22 Apr 2021 22:17:40 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84508bc2e91e9b08b6992021bcf6575304a72e75fe2e112017331b04d5edc6b8`  
		Last Modified: Thu, 22 Apr 2021 22:32:27 GMT  
		Size: 4.3 MB (4282564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62907c5116573f0b8237cef0b1b52331d4945c3fed33b88e5c961e2f505420a9`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ae9d391bb3e00f300812200277f9faee92744173d7324e3993ef169a0cd1eb`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62014e35aec6648734dd1a046b17cd77df9db4b2f8b17d2272e303ae3b97903a`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908266ff2e3c49a426faa0a3fd232a8d8556b9bd9361c046faaa764058830852`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:cc81cb52f172686a965e1c4e8a55c36dc45bbf434782b00bb9f13b023b4e25c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:919213b7bc91d2592c5d1312c0a4afc4191259685c87e5411af02b2f857c7f22
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105629134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c2735946f6f419fec4d9b2c7c5ef0d1de10fcb5bed1024117d3bdecf2ab3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 Apr 2021 22:17:39 GMT
RUN cmd /S /C #(nop) COPY file:0bab6ea83b560e32beee362f5586c34607d68bc8fc2e12422611f377373c3392 in C:\nats-server.exe 
# Thu, 22 Apr 2021 22:17:40 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84508bc2e91e9b08b6992021bcf6575304a72e75fe2e112017331b04d5edc6b8`  
		Last Modified: Thu, 22 Apr 2021 22:32:27 GMT  
		Size: 4.3 MB (4282564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62907c5116573f0b8237cef0b1b52331d4945c3fed33b88e5c961e2f505420a9`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ae9d391bb3e00f300812200277f9faee92744173d7324e3993ef169a0cd1eb`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62014e35aec6648734dd1a046b17cd77df9db4b2f8b17d2272e303ae3b97903a`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908266ff2e3c49a426faa0a3fd232a8d8556b9bd9361c046faaa764058830852`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:efb7005aa69eae8c01d32f56cf0a229b54aaf15f486b3f0c39ce1de41f19ab95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:28d9b42f5045e931f540022b50d140778296614cc46fea7fedef50e26b1584e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1080c373df8961fed31f1a39e28cc6c25d6795e0d7c3d561f2d379cf92def32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:9bb0ab90c22cd1ed787dfe4292c36984fd21bc48b2174ddad3b1e218161e3cf2 in /nats-server 
# Thu, 22 Apr 2021 23:02:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:30 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:30 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:10c4c9fb12b776e55b0ea8d3264f808ccc5caffaf56114cb844d5cb09786a6f1`  
		Last Modified: Thu, 22 Apr 2021 23:03:33 GMT  
		Size: 4.2 MB (4225473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473fec5c1cde7c5433c3e027919086bdd598e029899936541b2ec21ddb7847b0`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:a7a2c8f7194409c4dd75c93a6f9de11db1fc17bf1737db1c06240524e0b1858e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3895594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1fb4c72cd0448a5ba37409b399e5f04057f31f629ec5be8445008c54972c7f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 22:19:49 GMT
COPY file:64e71cd1d2e9467abd40785edd59f9612f1881becc619f3bedb155000a247b80 in /nats-server 
# Thu, 22 Apr 2021 22:19:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 22:19:51 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 22:19:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:238304e519d8648cca435478a5cebd819ed4063a311feaa2db6ec68565dde2d9`  
		Last Modified: Thu, 22 Apr 2021 22:20:38 GMT  
		Size: 3.9 MB (3895118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7507e43fa5a0838f598dd2a7130b2a5a79aa79cd6a06a73a1836fc2e6d6b5`  
		Last Modified: Thu, 22 Apr 2021 22:20:35 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:7a8f74c069f07b3f0b1351bc3aa1e2894ecc216e60c645973dcc81d261801b1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369c32ee391f07aae82ebd5e96f68ab9f24da31ffc8c257980974aaae2c38302`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:02:41 GMT
COPY file:4b22e9e541a652ab24ae042aa5e507153db95686a925c860d8e1d0d6abad10a3 in /nats-server 
# Thu, 22 Apr 2021 23:02:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:02:43 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:02:44 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:02:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65dc194b502e4ec7533d01c0251af4373a42f1054f5dc600b8d4aa96c6697a99`  
		Last Modified: Thu, 22 Apr 2021 23:03:32 GMT  
		Size: 3.9 MB (3891497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bcc4ebf70a26891fd7de222893f55bb8968e80212d8fdba06e24381f864e08`  
		Last Modified: Thu, 22 Apr 2021 23:03:31 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8b6b6b66c99dbfca177d9c18db7748068af5b7b397ff6444bef7d8c5df1ba19
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3865538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2844c33ced18f889b04345db4c42c57c97e38a0c8a922035c8e9833f3c3062`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Apr 2021 23:34:22 GMT
COPY file:7c26ed7ed2d57f80534f12bf79cbe9c116a73d781f8e5d610a54d82baca800a3 in /nats-server 
# Thu, 22 Apr 2021 23:34:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 22 Apr 2021 23:34:24 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 23:34:26 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Apr 2021 23:34:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3946fb3fc24631b9897efde5d957a63512d59c5745a8d0b8a4dca3171d07f77b`  
		Last Modified: Thu, 22 Apr 2021 23:35:18 GMT  
		Size: 3.9 MB (3865066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9203e1c4fb17a9b11e7579ecba8ba11004c1f5565dd8a2cd3d2fc45182152a6`  
		Last Modified: Thu, 22 Apr 2021 23:35:17 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:f8aac4b9cb4f642b2321c022c9d1273dad124d675bc48350043d8d0545ebaeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:58530c714d3a11ce4a69f36a318e08afa88440e0e4422dbf1102fed3efd596aa
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484209021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fee09ecc70f2cc3c43c0cb0d789a146b38405b764a400d452b89c335237e0c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Thu, 22 Apr 2021 22:15:14 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 22:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.2/nats-server-v2.2.2-windows-amd64.zip
# Thu, 22 Apr 2021 22:15:16 GMT
ENV GIT_DOWNLOAD_SHA256=644355111c8c31f129c962c3a2155041b8180c24dbe96353aaf31ce4dad25323
# Thu, 22 Apr 2021 22:15:59 GMT
RUN Set-PSDebug -Trace 2
# Thu, 22 Apr 2021 22:17:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 22 Apr 2021 22:17:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:16 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:18 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:9dc8f380778a8fd6b45de9b5c946a271bf272be729d066af5debbf40b12b7ec6`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb870516d41ed84b6f1bc0c60f0292342faeb98ae36340263425c735c1d28207`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98483cb65c9a5eee99c6e13f0d3cbe60b74547d81daeea891ae6726b003fea90`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6427780ae4e264dc775f5839a75c2ec3d102e7eb5cceb82b8755da23cb914f`  
		Last Modified: Thu, 22 Apr 2021 22:32:08 GMT  
		Size: 5.1 MB (5096294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b7a72b5ad5da2a8b5d04b05e199197127cdc0b77cd7ab256c1516a755ba461`  
		Last Modified: Thu, 22 Apr 2021 22:32:05 GMT  
		Size: 9.3 MB (9345478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d311a269622fcb4dbe064c650275cfb2da7df6070321b2eb1cc145fe9cc4d9`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 2.0 KB (1979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57c89d18cecb9ca10c1fb20c99fe03e263b36076914ede701f1c5a177fb6d29`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f12892bce1ff32498c5b6ee2685913a50ea0dd167aa5c55287c0464b8870c`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8884915b930db27ebd06dcd60062b41f4839548438632cb23f51876ed85a3397`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:f8aac4b9cb4f642b2321c022c9d1273dad124d675bc48350043d8d0545ebaeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:58530c714d3a11ce4a69f36a318e08afa88440e0e4422dbf1102fed3efd596aa
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484209021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fee09ecc70f2cc3c43c0cb0d789a146b38405b764a400d452b89c335237e0c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Thu, 22 Apr 2021 22:15:14 GMT
ENV NATS_SERVER=2.2.2
# Thu, 22 Apr 2021 22:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.2/nats-server-v2.2.2-windows-amd64.zip
# Thu, 22 Apr 2021 22:15:16 GMT
ENV GIT_DOWNLOAD_SHA256=644355111c8c31f129c962c3a2155041b8180c24dbe96353aaf31ce4dad25323
# Thu, 22 Apr 2021 22:15:59 GMT
RUN Set-PSDebug -Trace 2
# Thu, 22 Apr 2021 22:17:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 22 Apr 2021 22:17:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:16 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:18 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:9dc8f380778a8fd6b45de9b5c946a271bf272be729d066af5debbf40b12b7ec6`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb870516d41ed84b6f1bc0c60f0292342faeb98ae36340263425c735c1d28207`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98483cb65c9a5eee99c6e13f0d3cbe60b74547d81daeea891ae6726b003fea90`  
		Last Modified: Thu, 22 Apr 2021 22:32:06 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6427780ae4e264dc775f5839a75c2ec3d102e7eb5cceb82b8755da23cb914f`  
		Last Modified: Thu, 22 Apr 2021 22:32:08 GMT  
		Size: 5.1 MB (5096294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b7a72b5ad5da2a8b5d04b05e199197127cdc0b77cd7ab256c1516a755ba461`  
		Last Modified: Thu, 22 Apr 2021 22:32:05 GMT  
		Size: 9.3 MB (9345478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d311a269622fcb4dbe064c650275cfb2da7df6070321b2eb1cc145fe9cc4d9`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 2.0 KB (1979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57c89d18cecb9ca10c1fb20c99fe03e263b36076914ede701f1c5a177fb6d29`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f12892bce1ff32498c5b6ee2685913a50ea0dd167aa5c55287c0464b8870c`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8884915b930db27ebd06dcd60062b41f4839548438632cb23f51876ed85a3397`  
		Last Modified: Thu, 22 Apr 2021 22:32:03 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:486439b61d7c8307b15b01bae5f574784e333ee642d1d3285e3bf61785ea00cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull nats@sha256:ad5ac25aa423d2df82324037dd73fec641098cd5f198cf98ccf19f4ae640d1f5
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5814950471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc9b58b0a6e7d867ee74a6023bf1768d2dad684760ace428c0bf425357fcc5c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Wed, 14 Apr 2021 16:05:33 GMT
ENV NATS_SERVER=2.2.1
# Wed, 14 Apr 2021 16:05:35 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.1/nats-server-v2.2.1-windows-amd64.zip
# Wed, 14 Apr 2021 16:05:35 GMT
ENV GIT_DOWNLOAD_SHA256=1f0d48a7ba9200e2572016a9f3e1ec7e630f0518cc0b40950c14ff3a5d900924
# Wed, 14 Apr 2021 16:06:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 16:09:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 16:09:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:09:20 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:09:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:09:23 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:04d71ba1c574073f9d5dd016585c2fe26ac560c192f7aa36ce54d4c12832997f`  
		Last Modified: Wed, 14 Apr 2021 16:11:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9f66539738348100cf9f1e6a5bc40e8c2123bafb9329f5df3cf20a2015db33`  
		Last Modified: Wed, 14 Apr 2021 16:11:00 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f2eae922462b2537c1d0d32d548cb10190f6bda0d02da57440cc229da692b3`  
		Last Modified: Wed, 14 Apr 2021 16:11:00 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea168f84532f340be87f19704511ee160cbdc5b9c6ad8962fcd80e9fb8efea7`  
		Last Modified: Wed, 14 Apr 2021 16:11:01 GMT  
		Size: 5.7 MB (5651953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eda2d9556eb5afaf10e6300ac36ddc1383144ae65671ca3a01b24bac150c540`  
		Last Modified: Wed, 14 Apr 2021 16:11:01 GMT  
		Size: 14.4 MB (14401439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a04b0d9d602bb1f9c6fb7925bb92959ebcff2c30e6ca6a658cdd9976d662d70`  
		Last Modified: Wed, 14 Apr 2021 16:10:57 GMT  
		Size: 2.0 KB (1984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5e865356a464c9006414a165a6d0ffb8f062fa737be2ad42e1aa58fcfca23c`  
		Last Modified: Wed, 14 Apr 2021 16:10:56 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3533148ddde03cc5f28669b26c30dee8685db418d250a4b4829e465c0be8a7e`  
		Last Modified: Wed, 14 Apr 2021 16:10:56 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4573099491ec9887bd66033f55b39f6b897d1f59f21f679fdff4f822ebd7ea15`  
		Last Modified: Wed, 14 Apr 2021 16:10:56 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

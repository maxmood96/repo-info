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
-	[`nats:2.3`](#nats23)
-	[`nats:2.3-alpine`](#nats23-alpine)
-	[`nats:2.3-alpine3.13`](#nats23-alpine313)
-	[`nats:2.3-linux`](#nats23-linux)
-	[`nats:2.3-nanoserver`](#nats23-nanoserver)
-	[`nats:2.3-nanoserver-1809`](#nats23-nanoserver-1809)
-	[`nats:2.3-scratch`](#nats23-scratch)
-	[`nats:2.3-windowsservercore`](#nats23-windowsservercore)
-	[`nats:2.3-windowsservercore-1809`](#nats23-windowsservercore-1809)
-	[`nats:2.3-windowsservercore-ltsc2016`](#nats23-windowsservercore-ltsc2016)
-	[`nats:2.3.0`](#nats230)
-	[`nats:2.3.0-alpine`](#nats230-alpine)
-	[`nats:2.3.0-alpine3.13`](#nats230-alpine313)
-	[`nats:2.3.0-linux`](#nats230-linux)
-	[`nats:2.3.0-nanoserver`](#nats230-nanoserver)
-	[`nats:2.3.0-nanoserver-1809`](#nats230-nanoserver-1809)
-	[`nats:2.3.0-scratch`](#nats230-scratch)
-	[`nats:2.3.0-windowsservercore`](#nats230-windowsservercore)
-	[`nats:2.3.0-windowsservercore-1809`](#nats230-windowsservercore-1809)
-	[`nats:2.3.0-windowsservercore-ltsc2016`](#nats230-windowsservercore-ltsc2016)
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
$ docker pull nats@sha256:6aa7af6180050c241f606d59de7b4be510dbaddac5ae8855e5d84e4aae54ca42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1999; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:9ee8674607d72a7993a833da50a04bb798dc906079f7d4a3ff386ae9c7dad1b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24690f4c9243082798de0d5d0dcf537f0d65e65ba0e4c324f576019af6e88b71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:574cacffaccc18c0ebb219863832f97c5b4a301f1311490b79ebc4f7c91df1c5 in /nats-server 
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 18:20:54 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:55 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 18:20:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff7c72aa6eac78de3e8d419804aa418bec0a1d109825baafe6f27f8d5463c862`  
		Last Modified: Thu, 24 Jun 2021 18:21:47 GMT  
		Size: 4.3 MB (4335042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2e05cfe23a1b83926a7784d3a6f32ee581b1b20019023a53e605a28e098280`  
		Last Modified: Thu, 24 Jun 2021 18:21:45 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4d7fa672d2e979a1f71013d6c0ced4762a775e52c5fa1c597061e0661a4f564
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d818a3d14ec5abc722d14eefa80fd1bbb0cf49078b6a2fb3e54632e211c176c9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:f297049dd293f8bd69f8b37a6337b711a278a532e801780056f74049b995408b in /nats-server 
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:17:28 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:17:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f861ae2df753d566752887dd69fa7c0770cc5d866cf63d89323d119e6e132631`  
		Last Modified: Thu, 24 Jun 2021 19:20:11 GMT  
		Size: 4.0 MB (3992918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442ea4dc62b81dd101ec8289e6ef95821857d589dd412611e32dd41affe68138`  
		Last Modified: Thu, 24 Jun 2021 19:20:08 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:6796429bd41a95837772476ae383c344688bbfa91067d66187cff0919bb9bff5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f262b07aad3ac9672f6fdfdafb0486d87b7afa1949afa2bab951305a9191f6e4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Jun 2021 04:22:05 GMT
COPY file:e739b42ab72b567be37f2b08b7cc64858dc247505c5f9065cbc349f3f7cde026 in /nats-server 
# Fri, 25 Jun 2021 04:22:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 25 Jun 2021 04:22:06 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:22:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Jun 2021 04:22:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4eead17c506be0458b8b300048220b15977a1fb9f1dabb07031134fe7cd321bd`  
		Last Modified: Fri, 25 Jun 2021 04:24:25 GMT  
		Size: 4.0 MB (3987827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71186d5a22ac8937ee584ce8ff166469d1d6e857b4bca58533fb852beaf49aff`  
		Last Modified: Fri, 25 Jun 2021 04:24:23 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9af64abe7058267802b82eea320c8900f01e2900fc14c7819215cc38249b6a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b6ba9c13a2b4e06ce837ee797073c343df1705b660c37b3331e4afc500b19e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:5beb421ec5105e31f6e0b0a14e99795c4d0ca457385b898e67e502f8c1168b1c in /nats-server 
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:07:11 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:07:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:07:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4fa9662b0eb20e8acff5f956ac375b9e6d6bae55ed10b15783f5bdea6e212ca2`  
		Last Modified: Thu, 24 Jun 2021 19:08:34 GMT  
		Size: 4.0 MB (3958114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae902de5ccdf10f5ab555454aaf3ce99d7642bbc3961ef684412f5d45cd03ab`  
		Last Modified: Thu, 24 Jun 2021 19:08:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:c3d85580c0f97e9e7525ac25ff6dd2b46e30d0a28d8eae5922200f692c5f5420
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107067292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60db2a891b8d4acaed25bf0dfdd41e93f36804395b740b4fdc1e2bb452c6c1b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 15:55:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:39 GMT
RUN cmd /S /C #(nop) COPY file:bac1db2af96d2ddad22da9ae2b1252ad143dce10623146a5898a15a4e3f18d81 in C:\nats-server.exe 
# Thu, 24 Jun 2021 18:16:42 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:80d93ce19113bbf944b699f12e59395e0eabeb00ccd1fd5dc7df46bb115eba2f`  
		Last Modified: Wed, 09 Jun 2021 15:59:58 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec670391ee18da96972d36cee7981927664f13e0189b3d1f31b2c62e5ca0d4b`  
		Last Modified: Thu, 24 Jun 2021 18:21:31 GMT  
		Size: 4.4 MB (4389381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ee48b932f6c168a30dd680d51235836a69ad93983a5aa6ae510649498009d`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47216eb523d03d9b262b596ac92cdee9995cea672a4b3914a9f02a41a5ff422`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26d8e3fee7dfa3f7bf9b8af44b5f640be79d646bbcb96459100b6b39fe7bda`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348ad20da8616571c92e671840d54b660df38b670f5bf015aeaa2f6bed084657`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:ff5570b8f85ec8849d5b58316e2984352cc44e7f65a3cfeabb0cbbe9933db4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:11ac3d707fd53db8987f4e5432397c58bcd7fcd98e9c056088f709a58b4fc3a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2523bcf697d78fbb44315448e0c04248daa07f5741fc4c1d82224203a3a1a982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 18:20:14 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 18:20:17 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 18:20:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 18:20:17 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 18:20:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7669d67fb4cfb54da583e883237da0b279b1fb366b087a0a503ca26d962042`  
		Last Modified: Thu, 24 Jun 2021 18:21:21 GMT  
		Size: 4.6 MB (4615300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a63d38912003c0b7e278dc2e07a5e3595d926f114688e1eba7453d10771507`  
		Last Modified: Thu, 24 Jun 2021 18:21:20 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50aa5d23eab2b64578272b85b1840118f8ce74d4c8a076fd9fdbbf112b389a15`  
		Last Modified: Thu, 24 Jun 2021 18:21:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:afafd733f206092cfbf83b03d0d219e3ad9fc986d7b9bd1bcc813ba9a164e831
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6897059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a08095811cc4b9caf05423603dec24983d69af81a39a2b582c3fed0698cbcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 19:17:03 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 19:17:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 19:17:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 19:17:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 19:17:09 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 19:17:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072466ad1c8b3759328223593e85cddeedd93281cc285d4fbcc43c2aa77cff8b`  
		Last Modified: Thu, 24 Jun 2021 19:19:11 GMT  
		Size: 4.3 MB (4273957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040948b8c4aa41212a8812f47174f14427d9e2e336d534553442231f4f521882`  
		Last Modified: Thu, 24 Jun 2021 19:19:08 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7ac2240a33c4d9b574bff55265289f9093dcbe62577c93ce04d3b9b145e45e`  
		Last Modified: Thu, 24 Jun 2021 19:19:08 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:7f77835f7df0ca3c3fbc680a5df2e3a52df9b2bad2ad85a61c9c93588d554e1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6694378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31819633e547bc5673c5be989286c3fa84b4fa83c1cc7e1daac4586d53072bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 23:15:15 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Tue, 15 Jun 2021 23:15:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Jun 2021 04:21:38 GMT
ENV NATS_SERVER=2.3.0
# Fri, 25 Jun 2021 04:21:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 25 Jun 2021 04:21:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 25 Jun 2021 04:21:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Jun 2021 04:21:44 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:21:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Jun 2021 04:21:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b4716e8d6c6e6f099e638134cd5d5cb8d04256d758ebdfe9d484831feb75f6`  
		Last Modified: Fri, 25 Jun 2021 04:23:48 GMT  
		Size: 4.3 MB (4269265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b992d0d507b7fcd3c04c8337fde6b65f98ef5711af47b760054e79a2568c0990`  
		Last Modified: Fri, 25 Jun 2021 04:23:45 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ae15dff3a871a17e97c8114db82e6e7af74fdbb011e105314060415dcc93a3`  
		Last Modified: Fri, 25 Jun 2021 04:23:45 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e7be6da297d4e47e1cbf0cebebb0b28db6ceeb50f8e06e87609dce41de682f92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6953599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0539985a8e92b6e078f0f65ffce3ff416cfa3401034c750ec07b9da7150efce8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 19:06:45 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 19:06:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 19:06:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 19:06:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 19:06:48 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:06:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 19:06:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27d0993acd4f2a9aa99219b53b130917cfcaa7b5ab8f75f92c6853892b1fbd8`  
		Last Modified: Thu, 24 Jun 2021 19:08:02 GMT  
		Size: 4.2 MB (4240601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89210891c944f9ecbd826fe696a7f0a1399ac8628705331d9eb011d633fe7b2`  
		Last Modified: Thu, 24 Jun 2021 19:08:01 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e288f0bb2545133bb23a02793719cdc1076dc77f7c61c80c05c6351f9dc2c482`  
		Last Modified: Thu, 24 Jun 2021 19:08:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.13`

```console
$ docker pull nats@sha256:ff5570b8f85ec8849d5b58316e2984352cc44e7f65a3cfeabb0cbbe9933db4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.13` - linux; amd64

```console
$ docker pull nats@sha256:11ac3d707fd53db8987f4e5432397c58bcd7fcd98e9c056088f709a58b4fc3a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2523bcf697d78fbb44315448e0c04248daa07f5741fc4c1d82224203a3a1a982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 18:20:14 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 18:20:17 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 18:20:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 18:20:17 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 18:20:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7669d67fb4cfb54da583e883237da0b279b1fb366b087a0a503ca26d962042`  
		Last Modified: Thu, 24 Jun 2021 18:21:21 GMT  
		Size: 4.6 MB (4615300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a63d38912003c0b7e278dc2e07a5e3595d926f114688e1eba7453d10771507`  
		Last Modified: Thu, 24 Jun 2021 18:21:20 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50aa5d23eab2b64578272b85b1840118f8ce74d4c8a076fd9fdbbf112b389a15`  
		Last Modified: Thu, 24 Jun 2021 18:21:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.13` - linux; arm variant v6

```console
$ docker pull nats@sha256:afafd733f206092cfbf83b03d0d219e3ad9fc986d7b9bd1bcc813ba9a164e831
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6897059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a08095811cc4b9caf05423603dec24983d69af81a39a2b582c3fed0698cbcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 19:17:03 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 19:17:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 19:17:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 19:17:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 19:17:09 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 19:17:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072466ad1c8b3759328223593e85cddeedd93281cc285d4fbcc43c2aa77cff8b`  
		Last Modified: Thu, 24 Jun 2021 19:19:11 GMT  
		Size: 4.3 MB (4273957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040948b8c4aa41212a8812f47174f14427d9e2e336d534553442231f4f521882`  
		Last Modified: Thu, 24 Jun 2021 19:19:08 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7ac2240a33c4d9b574bff55265289f9093dcbe62577c93ce04d3b9b145e45e`  
		Last Modified: Thu, 24 Jun 2021 19:19:08 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.13` - linux; arm variant v7

```console
$ docker pull nats@sha256:7f77835f7df0ca3c3fbc680a5df2e3a52df9b2bad2ad85a61c9c93588d554e1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6694378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31819633e547bc5673c5be989286c3fa84b4fa83c1cc7e1daac4586d53072bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 23:15:15 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Tue, 15 Jun 2021 23:15:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Jun 2021 04:21:38 GMT
ENV NATS_SERVER=2.3.0
# Fri, 25 Jun 2021 04:21:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 25 Jun 2021 04:21:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 25 Jun 2021 04:21:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Jun 2021 04:21:44 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:21:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Jun 2021 04:21:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b4716e8d6c6e6f099e638134cd5d5cb8d04256d758ebdfe9d484831feb75f6`  
		Last Modified: Fri, 25 Jun 2021 04:23:48 GMT  
		Size: 4.3 MB (4269265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b992d0d507b7fcd3c04c8337fde6b65f98ef5711af47b760054e79a2568c0990`  
		Last Modified: Fri, 25 Jun 2021 04:23:45 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ae15dff3a871a17e97c8114db82e6e7af74fdbb011e105314060415dcc93a3`  
		Last Modified: Fri, 25 Jun 2021 04:23:45 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e7be6da297d4e47e1cbf0cebebb0b28db6ceeb50f8e06e87609dce41de682f92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6953599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0539985a8e92b6e078f0f65ffce3ff416cfa3401034c750ec07b9da7150efce8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 19:06:45 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 19:06:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 19:06:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 19:06:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 19:06:48 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:06:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 19:06:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27d0993acd4f2a9aa99219b53b130917cfcaa7b5ab8f75f92c6853892b1fbd8`  
		Last Modified: Thu, 24 Jun 2021 19:08:02 GMT  
		Size: 4.2 MB (4240601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89210891c944f9ecbd826fe696a7f0a1399ac8628705331d9eb011d633fe7b2`  
		Last Modified: Thu, 24 Jun 2021 19:08:01 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e288f0bb2545133bb23a02793719cdc1076dc77f7c61c80c05c6351f9dc2c482`  
		Last Modified: Thu, 24 Jun 2021 19:08:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:80eb5023b4f9a6a43ccb90613913d8bbd7fb1d60ed202af2e7e7425add895c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:9ee8674607d72a7993a833da50a04bb798dc906079f7d4a3ff386ae9c7dad1b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24690f4c9243082798de0d5d0dcf537f0d65e65ba0e4c324f576019af6e88b71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:574cacffaccc18c0ebb219863832f97c5b4a301f1311490b79ebc4f7c91df1c5 in /nats-server 
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 18:20:54 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:55 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 18:20:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff7c72aa6eac78de3e8d419804aa418bec0a1d109825baafe6f27f8d5463c862`  
		Last Modified: Thu, 24 Jun 2021 18:21:47 GMT  
		Size: 4.3 MB (4335042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2e05cfe23a1b83926a7784d3a6f32ee581b1b20019023a53e605a28e098280`  
		Last Modified: Thu, 24 Jun 2021 18:21:45 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4d7fa672d2e979a1f71013d6c0ced4762a775e52c5fa1c597061e0661a4f564
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d818a3d14ec5abc722d14eefa80fd1bbb0cf49078b6a2fb3e54632e211c176c9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:f297049dd293f8bd69f8b37a6337b711a278a532e801780056f74049b995408b in /nats-server 
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:17:28 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:17:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f861ae2df753d566752887dd69fa7c0770cc5d866cf63d89323d119e6e132631`  
		Last Modified: Thu, 24 Jun 2021 19:20:11 GMT  
		Size: 4.0 MB (3992918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442ea4dc62b81dd101ec8289e6ef95821857d589dd412611e32dd41affe68138`  
		Last Modified: Thu, 24 Jun 2021 19:20:08 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:6796429bd41a95837772476ae383c344688bbfa91067d66187cff0919bb9bff5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f262b07aad3ac9672f6fdfdafb0486d87b7afa1949afa2bab951305a9191f6e4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Jun 2021 04:22:05 GMT
COPY file:e739b42ab72b567be37f2b08b7cc64858dc247505c5f9065cbc349f3f7cde026 in /nats-server 
# Fri, 25 Jun 2021 04:22:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 25 Jun 2021 04:22:06 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:22:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Jun 2021 04:22:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4eead17c506be0458b8b300048220b15977a1fb9f1dabb07031134fe7cd321bd`  
		Last Modified: Fri, 25 Jun 2021 04:24:25 GMT  
		Size: 4.0 MB (3987827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71186d5a22ac8937ee584ce8ff166469d1d6e857b4bca58533fb852beaf49aff`  
		Last Modified: Fri, 25 Jun 2021 04:24:23 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9af64abe7058267802b82eea320c8900f01e2900fc14c7819215cc38249b6a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b6ba9c13a2b4e06ce837ee797073c343df1705b660c37b3331e4afc500b19e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:5beb421ec5105e31f6e0b0a14e99795c4d0ca457385b898e67e502f8c1168b1c in /nats-server 
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:07:11 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:07:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:07:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4fa9662b0eb20e8acff5f956ac375b9e6d6bae55ed10b15783f5bdea6e212ca2`  
		Last Modified: Thu, 24 Jun 2021 19:08:34 GMT  
		Size: 4.0 MB (3958114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae902de5ccdf10f5ab555454aaf3ce99d7642bbc3961ef684412f5d45cd03ab`  
		Last Modified: Thu, 24 Jun 2021 19:08:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:4ebe0f8afa0791f4642839c39904f87117ae2b491ef7cc3af12fe3ea313999b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:c3d85580c0f97e9e7525ac25ff6dd2b46e30d0a28d8eae5922200f692c5f5420
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107067292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60db2a891b8d4acaed25bf0dfdd41e93f36804395b740b4fdc1e2bb452c6c1b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 15:55:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:39 GMT
RUN cmd /S /C #(nop) COPY file:bac1db2af96d2ddad22da9ae2b1252ad143dce10623146a5898a15a4e3f18d81 in C:\nats-server.exe 
# Thu, 24 Jun 2021 18:16:42 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:80d93ce19113bbf944b699f12e59395e0eabeb00ccd1fd5dc7df46bb115eba2f`  
		Last Modified: Wed, 09 Jun 2021 15:59:58 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec670391ee18da96972d36cee7981927664f13e0189b3d1f31b2c62e5ca0d4b`  
		Last Modified: Thu, 24 Jun 2021 18:21:31 GMT  
		Size: 4.4 MB (4389381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ee48b932f6c168a30dd680d51235836a69ad93983a5aa6ae510649498009d`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47216eb523d03d9b262b596ac92cdee9995cea672a4b3914a9f02a41a5ff422`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26d8e3fee7dfa3f7bf9b8af44b5f640be79d646bbcb96459100b6b39fe7bda`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348ad20da8616571c92e671840d54b660df38b670f5bf015aeaa2f6bed084657`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:4ebe0f8afa0791f4642839c39904f87117ae2b491ef7cc3af12fe3ea313999b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:c3d85580c0f97e9e7525ac25ff6dd2b46e30d0a28d8eae5922200f692c5f5420
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107067292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60db2a891b8d4acaed25bf0dfdd41e93f36804395b740b4fdc1e2bb452c6c1b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 15:55:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:39 GMT
RUN cmd /S /C #(nop) COPY file:bac1db2af96d2ddad22da9ae2b1252ad143dce10623146a5898a15a4e3f18d81 in C:\nats-server.exe 
# Thu, 24 Jun 2021 18:16:42 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:80d93ce19113bbf944b699f12e59395e0eabeb00ccd1fd5dc7df46bb115eba2f`  
		Last Modified: Wed, 09 Jun 2021 15:59:58 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec670391ee18da96972d36cee7981927664f13e0189b3d1f31b2c62e5ca0d4b`  
		Last Modified: Thu, 24 Jun 2021 18:21:31 GMT  
		Size: 4.4 MB (4389381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ee48b932f6c168a30dd680d51235836a69ad93983a5aa6ae510649498009d`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47216eb523d03d9b262b596ac92cdee9995cea672a4b3914a9f02a41a5ff422`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26d8e3fee7dfa3f7bf9b8af44b5f640be79d646bbcb96459100b6b39fe7bda`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348ad20da8616571c92e671840d54b660df38b670f5bf015aeaa2f6bed084657`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:80eb5023b4f9a6a43ccb90613913d8bbd7fb1d60ed202af2e7e7425add895c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:9ee8674607d72a7993a833da50a04bb798dc906079f7d4a3ff386ae9c7dad1b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24690f4c9243082798de0d5d0dcf537f0d65e65ba0e4c324f576019af6e88b71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:574cacffaccc18c0ebb219863832f97c5b4a301f1311490b79ebc4f7c91df1c5 in /nats-server 
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 18:20:54 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:55 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 18:20:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff7c72aa6eac78de3e8d419804aa418bec0a1d109825baafe6f27f8d5463c862`  
		Last Modified: Thu, 24 Jun 2021 18:21:47 GMT  
		Size: 4.3 MB (4335042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2e05cfe23a1b83926a7784d3a6f32ee581b1b20019023a53e605a28e098280`  
		Last Modified: Thu, 24 Jun 2021 18:21:45 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4d7fa672d2e979a1f71013d6c0ced4762a775e52c5fa1c597061e0661a4f564
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d818a3d14ec5abc722d14eefa80fd1bbb0cf49078b6a2fb3e54632e211c176c9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:f297049dd293f8bd69f8b37a6337b711a278a532e801780056f74049b995408b in /nats-server 
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:17:28 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:17:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f861ae2df753d566752887dd69fa7c0770cc5d866cf63d89323d119e6e132631`  
		Last Modified: Thu, 24 Jun 2021 19:20:11 GMT  
		Size: 4.0 MB (3992918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442ea4dc62b81dd101ec8289e6ef95821857d589dd412611e32dd41affe68138`  
		Last Modified: Thu, 24 Jun 2021 19:20:08 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:6796429bd41a95837772476ae383c344688bbfa91067d66187cff0919bb9bff5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f262b07aad3ac9672f6fdfdafb0486d87b7afa1949afa2bab951305a9191f6e4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Jun 2021 04:22:05 GMT
COPY file:e739b42ab72b567be37f2b08b7cc64858dc247505c5f9065cbc349f3f7cde026 in /nats-server 
# Fri, 25 Jun 2021 04:22:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 25 Jun 2021 04:22:06 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:22:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Jun 2021 04:22:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4eead17c506be0458b8b300048220b15977a1fb9f1dabb07031134fe7cd321bd`  
		Last Modified: Fri, 25 Jun 2021 04:24:25 GMT  
		Size: 4.0 MB (3987827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71186d5a22ac8937ee584ce8ff166469d1d6e857b4bca58533fb852beaf49aff`  
		Last Modified: Fri, 25 Jun 2021 04:24:23 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9af64abe7058267802b82eea320c8900f01e2900fc14c7819215cc38249b6a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b6ba9c13a2b4e06ce837ee797073c343df1705b660c37b3331e4afc500b19e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:5beb421ec5105e31f6e0b0a14e99795c4d0ca457385b898e67e502f8c1168b1c in /nats-server 
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:07:11 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:07:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:07:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4fa9662b0eb20e8acff5f956ac375b9e6d6bae55ed10b15783f5bdea6e212ca2`  
		Last Modified: Thu, 24 Jun 2021 19:08:34 GMT  
		Size: 4.0 MB (3958114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae902de5ccdf10f5ab555454aaf3ce99d7642bbc3961ef684412f5d45cd03ab`  
		Last Modified: Thu, 24 Jun 2021 19:08:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:0a82183999395fc7ff72a6528b06205f06ca31baa3e914a3c43496de2242b3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64
	-	windows version 10.0.14393.4467; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:2b5fc0956f7fa5e8a5d73443e2b2cff10b2c5a1d750238f0c39d388ad230e889
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2646697143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3296c025e7c6bdec1087e1cd78a2af9c8398fde53f8acc26c4c2c62dade1e2fc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 13:15:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 15:52:54 GMT
ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:14:27 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:14:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.0/nats-server-v2.3.0-windows-amd64.zip
# Thu, 24 Jun 2021 18:14:33 GMT
ENV NATS_SERVER_SHASUM=4cf3cad0f3fc635a7be429ab13d852b1eea41c8f81b5d9ef7f21d93dd99a1f6f
# Thu, 24 Jun 2021 18:15:14 GMT
RUN Set-PSDebug -Trace 2
# Thu, 24 Jun 2021 18:16:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 24 Jun 2021 18:16:20 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:22 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae7d2dc4b590128efeafd375d02122e65a2525623ac2be100c1a390caf8a4b49`  
		Last Modified: Wed, 09 Jun 2021 15:28:02 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507a90d55d261855b42c7b5905599cdc274ca135ad962fffffe1fa6246c9bba7`  
		Last Modified: Wed, 09 Jun 2021 15:59:38 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29775406c1781fcc27d8bf50b4b0bfcd9418dda6cfae494e4d9383e0213df24b`  
		Last Modified: Thu, 24 Jun 2021 18:21:11 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3bf008ba6d0a427891ae36a26107b3e1f386cb9be8dbd0427623920c08cb93`  
		Last Modified: Thu, 24 Jun 2021 18:21:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35cb02232de3ac8c2255dee0bc6a718b0b3cb29b7baa3caf9825fae6519353c`  
		Last Modified: Thu, 24 Jun 2021 18:21:12 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8811ca1ef9b5e7b658fe9eb6dcf4145a8c7fc2108cddf27604a32625196d9435`  
		Last Modified: Thu, 24 Jun 2021 18:21:12 GMT  
		Size: 363.9 KB (363906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07799fa10e1ce0eeb453bb8919dd2756d7f46df37096e364eaef1cf48ee4d27b`  
		Last Modified: Thu, 24 Jun 2021 18:21:11 GMT  
		Size: 4.7 MB (4734976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7d8a61897a84ba84d3157167674e44f39375855accec3dbfd1bfcc8fb1911d`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.9 KB (1921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5675249b0aafebc9b96c1c5359219fa68fe30b7e67d7877c5d2a8c6083b153da`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42271808b9146dc5744c45edba3f979ab16c9a382b62c44320fa4f04f9ab0f97`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dd08bcc8b2cc2e24a6318d63fcc471176adf3acdf78b10ac15b1fa5527c568`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.4467; amd64

```console
$ docker pull nats@sha256:845b27a65fd56c97937856e216d7771d144a8b90c4cce3b45562de4761576f93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6270853814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87d244a19fd78d48d37bc35a9b3997f8dafc00fcce0da603d7a5aa6aa095429`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 13:26:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 15:55:27 GMT
ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:58 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:17:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.0/nats-server-v2.3.0-windows-amd64.zip
# Thu, 24 Jun 2021 18:17:03 GMT
ENV NATS_SERVER_SHASUM=4cf3cad0f3fc635a7be429ab13d852b1eea41c8f81b5d9ef7f21d93dd99a1f6f
# Thu, 24 Jun 2021 18:18:18 GMT
RUN Set-PSDebug -Trace 2
# Thu, 24 Jun 2021 18:20:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 24 Jun 2021 18:20:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:20:17 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:20:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2f52abeee6d6f4a925ad418b5e6200d4fca9bf92834ffc918b8bbaccd34251db`  
		Size: 2.2 GB (2195741359 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fa4e6085e5538e957ef06561fe1e62dff898da7f4bb577e81da74323aecab2d7`  
		Last Modified: Wed, 09 Jun 2021 15:28:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db57f94547be7109ad927e2f9d04a0501a2a5f0cb91ad8c4385eb32758f86b9`  
		Last Modified: Wed, 09 Jun 2021 16:00:21 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385a2e510feddc0676b3c17e1654e2430eb4ac4a8a775b78e89afaccc5fdc804`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c18a811e26704bd4bb49d57454d177eb277d065d5841d36f6fe5dce50a4fda`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154f452c578ee0bf6e0aa67510a192c41adaf4a94d974a0909c227cc29bf6b18`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45d0a6fab2e6e94ed71f11798975da67d62cc86ebc458ce3e3a12bbe7f250d8`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 352.1 KB (352114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d373c50c3af9ea67008c088d5b13b3963be0c55dea90c371d8a1be5ba44d2a84`  
		Last Modified: Thu, 24 Jun 2021 18:21:51 GMT  
		Size: 4.8 MB (4761699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1065e6f071db7571880f6c942f08e2565dde2da5ee37a3d79bdeca96583d8`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f1549b605bdde25fa57f56f24f602d8605121787ac6d452d1eae704c173ba5`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6659b0e6d881d37794c4ac62633dad4743618a980578bdbe8e7a4e5d617211`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c424710ae455acf452bd0eba0e1e696916ed091e236132a564e02b266431cc3`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:a673dfea57d51e9d21677796f5f72f60d13dab15b74dd8b2dfe32518cd6ca782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:2b5fc0956f7fa5e8a5d73443e2b2cff10b2c5a1d750238f0c39d388ad230e889
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2646697143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3296c025e7c6bdec1087e1cd78a2af9c8398fde53f8acc26c4c2c62dade1e2fc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 13:15:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 15:52:54 GMT
ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:14:27 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:14:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.0/nats-server-v2.3.0-windows-amd64.zip
# Thu, 24 Jun 2021 18:14:33 GMT
ENV NATS_SERVER_SHASUM=4cf3cad0f3fc635a7be429ab13d852b1eea41c8f81b5d9ef7f21d93dd99a1f6f
# Thu, 24 Jun 2021 18:15:14 GMT
RUN Set-PSDebug -Trace 2
# Thu, 24 Jun 2021 18:16:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 24 Jun 2021 18:16:20 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:22 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae7d2dc4b590128efeafd375d02122e65a2525623ac2be100c1a390caf8a4b49`  
		Last Modified: Wed, 09 Jun 2021 15:28:02 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507a90d55d261855b42c7b5905599cdc274ca135ad962fffffe1fa6246c9bba7`  
		Last Modified: Wed, 09 Jun 2021 15:59:38 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29775406c1781fcc27d8bf50b4b0bfcd9418dda6cfae494e4d9383e0213df24b`  
		Last Modified: Thu, 24 Jun 2021 18:21:11 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3bf008ba6d0a427891ae36a26107b3e1f386cb9be8dbd0427623920c08cb93`  
		Last Modified: Thu, 24 Jun 2021 18:21:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35cb02232de3ac8c2255dee0bc6a718b0b3cb29b7baa3caf9825fae6519353c`  
		Last Modified: Thu, 24 Jun 2021 18:21:12 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8811ca1ef9b5e7b658fe9eb6dcf4145a8c7fc2108cddf27604a32625196d9435`  
		Last Modified: Thu, 24 Jun 2021 18:21:12 GMT  
		Size: 363.9 KB (363906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07799fa10e1ce0eeb453bb8919dd2756d7f46df37096e364eaef1cf48ee4d27b`  
		Last Modified: Thu, 24 Jun 2021 18:21:11 GMT  
		Size: 4.7 MB (4734976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7d8a61897a84ba84d3157167674e44f39375855accec3dbfd1bfcc8fb1911d`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.9 KB (1921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5675249b0aafebc9b96c1c5359219fa68fe30b7e67d7877c5d2a8c6083b153da`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42271808b9146dc5744c45edba3f979ab16c9a382b62c44320fa4f04f9ab0f97`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dd08bcc8b2cc2e24a6318d63fcc471176adf3acdf78b10ac15b1fa5527c568`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:0e0a6967d374622f82cf5383e0c8751541a791a255a4c728eaa86e51af9560c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4467; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4467; amd64

```console
$ docker pull nats@sha256:845b27a65fd56c97937856e216d7771d144a8b90c4cce3b45562de4761576f93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6270853814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87d244a19fd78d48d37bc35a9b3997f8dafc00fcce0da603d7a5aa6aa095429`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 13:26:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 15:55:27 GMT
ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:58 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:17:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.0/nats-server-v2.3.0-windows-amd64.zip
# Thu, 24 Jun 2021 18:17:03 GMT
ENV NATS_SERVER_SHASUM=4cf3cad0f3fc635a7be429ab13d852b1eea41c8f81b5d9ef7f21d93dd99a1f6f
# Thu, 24 Jun 2021 18:18:18 GMT
RUN Set-PSDebug -Trace 2
# Thu, 24 Jun 2021 18:20:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 24 Jun 2021 18:20:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:20:17 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:20:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2f52abeee6d6f4a925ad418b5e6200d4fca9bf92834ffc918b8bbaccd34251db`  
		Size: 2.2 GB (2195741359 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fa4e6085e5538e957ef06561fe1e62dff898da7f4bb577e81da74323aecab2d7`  
		Last Modified: Wed, 09 Jun 2021 15:28:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db57f94547be7109ad927e2f9d04a0501a2a5f0cb91ad8c4385eb32758f86b9`  
		Last Modified: Wed, 09 Jun 2021 16:00:21 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385a2e510feddc0676b3c17e1654e2430eb4ac4a8a775b78e89afaccc5fdc804`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c18a811e26704bd4bb49d57454d177eb277d065d5841d36f6fe5dce50a4fda`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154f452c578ee0bf6e0aa67510a192c41adaf4a94d974a0909c227cc29bf6b18`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45d0a6fab2e6e94ed71f11798975da67d62cc86ebc458ce3e3a12bbe7f250d8`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 352.1 KB (352114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d373c50c3af9ea67008c088d5b13b3963be0c55dea90c371d8a1be5ba44d2a84`  
		Last Modified: Thu, 24 Jun 2021 18:21:51 GMT  
		Size: 4.8 MB (4761699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1065e6f071db7571880f6c942f08e2565dde2da5ee37a3d79bdeca96583d8`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f1549b605bdde25fa57f56f24f602d8605121787ac6d452d1eae704c173ba5`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6659b0e6d881d37794c4ac62633dad4743618a980578bdbe8e7a4e5d617211`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c424710ae455acf452bd0eba0e1e696916ed091e236132a564e02b266431cc3`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3`

```console
$ docker pull nats@sha256:6aa7af6180050c241f606d59de7b4be510dbaddac5ae8855e5d84e4aae54ca42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1999; amd64

### `nats:2.3` - linux; amd64

```console
$ docker pull nats@sha256:9ee8674607d72a7993a833da50a04bb798dc906079f7d4a3ff386ae9c7dad1b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24690f4c9243082798de0d5d0dcf537f0d65e65ba0e4c324f576019af6e88b71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:574cacffaccc18c0ebb219863832f97c5b4a301f1311490b79ebc4f7c91df1c5 in /nats-server 
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 18:20:54 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:55 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 18:20:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff7c72aa6eac78de3e8d419804aa418bec0a1d109825baafe6f27f8d5463c862`  
		Last Modified: Thu, 24 Jun 2021 18:21:47 GMT  
		Size: 4.3 MB (4335042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2e05cfe23a1b83926a7784d3a6f32ee581b1b20019023a53e605a28e098280`  
		Last Modified: Thu, 24 Jun 2021 18:21:45 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4d7fa672d2e979a1f71013d6c0ced4762a775e52c5fa1c597061e0661a4f564
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d818a3d14ec5abc722d14eefa80fd1bbb0cf49078b6a2fb3e54632e211c176c9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:f297049dd293f8bd69f8b37a6337b711a278a532e801780056f74049b995408b in /nats-server 
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:17:28 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:17:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f861ae2df753d566752887dd69fa7c0770cc5d866cf63d89323d119e6e132631`  
		Last Modified: Thu, 24 Jun 2021 19:20:11 GMT  
		Size: 4.0 MB (3992918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442ea4dc62b81dd101ec8289e6ef95821857d589dd412611e32dd41affe68138`  
		Last Modified: Thu, 24 Jun 2021 19:20:08 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3` - linux; arm variant v7

```console
$ docker pull nats@sha256:6796429bd41a95837772476ae383c344688bbfa91067d66187cff0919bb9bff5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f262b07aad3ac9672f6fdfdafb0486d87b7afa1949afa2bab951305a9191f6e4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Jun 2021 04:22:05 GMT
COPY file:e739b42ab72b567be37f2b08b7cc64858dc247505c5f9065cbc349f3f7cde026 in /nats-server 
# Fri, 25 Jun 2021 04:22:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 25 Jun 2021 04:22:06 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:22:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Jun 2021 04:22:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4eead17c506be0458b8b300048220b15977a1fb9f1dabb07031134fe7cd321bd`  
		Last Modified: Fri, 25 Jun 2021 04:24:25 GMT  
		Size: 4.0 MB (3987827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71186d5a22ac8937ee584ce8ff166469d1d6e857b4bca58533fb852beaf49aff`  
		Last Modified: Fri, 25 Jun 2021 04:24:23 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9af64abe7058267802b82eea320c8900f01e2900fc14c7819215cc38249b6a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b6ba9c13a2b4e06ce837ee797073c343df1705b660c37b3331e4afc500b19e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:5beb421ec5105e31f6e0b0a14e99795c4d0ca457385b898e67e502f8c1168b1c in /nats-server 
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:07:11 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:07:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:07:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4fa9662b0eb20e8acff5f956ac375b9e6d6bae55ed10b15783f5bdea6e212ca2`  
		Last Modified: Thu, 24 Jun 2021 19:08:34 GMT  
		Size: 4.0 MB (3958114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae902de5ccdf10f5ab555454aaf3ce99d7642bbc3961ef684412f5d45cd03ab`  
		Last Modified: Thu, 24 Jun 2021 19:08:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:c3d85580c0f97e9e7525ac25ff6dd2b46e30d0a28d8eae5922200f692c5f5420
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107067292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60db2a891b8d4acaed25bf0dfdd41e93f36804395b740b4fdc1e2bb452c6c1b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 15:55:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:39 GMT
RUN cmd /S /C #(nop) COPY file:bac1db2af96d2ddad22da9ae2b1252ad143dce10623146a5898a15a4e3f18d81 in C:\nats-server.exe 
# Thu, 24 Jun 2021 18:16:42 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:80d93ce19113bbf944b699f12e59395e0eabeb00ccd1fd5dc7df46bb115eba2f`  
		Last Modified: Wed, 09 Jun 2021 15:59:58 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec670391ee18da96972d36cee7981927664f13e0189b3d1f31b2c62e5ca0d4b`  
		Last Modified: Thu, 24 Jun 2021 18:21:31 GMT  
		Size: 4.4 MB (4389381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ee48b932f6c168a30dd680d51235836a69ad93983a5aa6ae510649498009d`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47216eb523d03d9b262b596ac92cdee9995cea672a4b3914a9f02a41a5ff422`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26d8e3fee7dfa3f7bf9b8af44b5f640be79d646bbcb96459100b6b39fe7bda`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348ad20da8616571c92e671840d54b660df38b670f5bf015aeaa2f6bed084657`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3-alpine`

```console
$ docker pull nats@sha256:ff5570b8f85ec8849d5b58316e2984352cc44e7f65a3cfeabb0cbbe9933db4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.3-alpine` - linux; amd64

```console
$ docker pull nats@sha256:11ac3d707fd53db8987f4e5432397c58bcd7fcd98e9c056088f709a58b4fc3a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2523bcf697d78fbb44315448e0c04248daa07f5741fc4c1d82224203a3a1a982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 18:20:14 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 18:20:17 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 18:20:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 18:20:17 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 18:20:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7669d67fb4cfb54da583e883237da0b279b1fb366b087a0a503ca26d962042`  
		Last Modified: Thu, 24 Jun 2021 18:21:21 GMT  
		Size: 4.6 MB (4615300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a63d38912003c0b7e278dc2e07a5e3595d926f114688e1eba7453d10771507`  
		Last Modified: Thu, 24 Jun 2021 18:21:20 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50aa5d23eab2b64578272b85b1840118f8ce74d4c8a076fd9fdbbf112b389a15`  
		Last Modified: Thu, 24 Jun 2021 18:21:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:afafd733f206092cfbf83b03d0d219e3ad9fc986d7b9bd1bcc813ba9a164e831
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6897059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a08095811cc4b9caf05423603dec24983d69af81a39a2b582c3fed0698cbcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 19:17:03 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 19:17:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 19:17:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 19:17:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 19:17:09 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 19:17:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072466ad1c8b3759328223593e85cddeedd93281cc285d4fbcc43c2aa77cff8b`  
		Last Modified: Thu, 24 Jun 2021 19:19:11 GMT  
		Size: 4.3 MB (4273957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040948b8c4aa41212a8812f47174f14427d9e2e336d534553442231f4f521882`  
		Last Modified: Thu, 24 Jun 2021 19:19:08 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7ac2240a33c4d9b574bff55265289f9093dcbe62577c93ce04d3b9b145e45e`  
		Last Modified: Thu, 24 Jun 2021 19:19:08 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:7f77835f7df0ca3c3fbc680a5df2e3a52df9b2bad2ad85a61c9c93588d554e1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6694378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31819633e547bc5673c5be989286c3fa84b4fa83c1cc7e1daac4586d53072bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 23:15:15 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Tue, 15 Jun 2021 23:15:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Jun 2021 04:21:38 GMT
ENV NATS_SERVER=2.3.0
# Fri, 25 Jun 2021 04:21:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 25 Jun 2021 04:21:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 25 Jun 2021 04:21:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Jun 2021 04:21:44 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:21:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Jun 2021 04:21:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b4716e8d6c6e6f099e638134cd5d5cb8d04256d758ebdfe9d484831feb75f6`  
		Last Modified: Fri, 25 Jun 2021 04:23:48 GMT  
		Size: 4.3 MB (4269265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b992d0d507b7fcd3c04c8337fde6b65f98ef5711af47b760054e79a2568c0990`  
		Last Modified: Fri, 25 Jun 2021 04:23:45 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ae15dff3a871a17e97c8114db82e6e7af74fdbb011e105314060415dcc93a3`  
		Last Modified: Fri, 25 Jun 2021 04:23:45 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e7be6da297d4e47e1cbf0cebebb0b28db6ceeb50f8e06e87609dce41de682f92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6953599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0539985a8e92b6e078f0f65ffce3ff416cfa3401034c750ec07b9da7150efce8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 19:06:45 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 19:06:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 19:06:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 19:06:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 19:06:48 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:06:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 19:06:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27d0993acd4f2a9aa99219b53b130917cfcaa7b5ab8f75f92c6853892b1fbd8`  
		Last Modified: Thu, 24 Jun 2021 19:08:02 GMT  
		Size: 4.2 MB (4240601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89210891c944f9ecbd826fe696a7f0a1399ac8628705331d9eb011d633fe7b2`  
		Last Modified: Thu, 24 Jun 2021 19:08:01 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e288f0bb2545133bb23a02793719cdc1076dc77f7c61c80c05c6351f9dc2c482`  
		Last Modified: Thu, 24 Jun 2021 19:08:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3-alpine3.13`

```console
$ docker pull nats@sha256:ff5570b8f85ec8849d5b58316e2984352cc44e7f65a3cfeabb0cbbe9933db4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.3-alpine3.13` - linux; amd64

```console
$ docker pull nats@sha256:11ac3d707fd53db8987f4e5432397c58bcd7fcd98e9c056088f709a58b4fc3a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2523bcf697d78fbb44315448e0c04248daa07f5741fc4c1d82224203a3a1a982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 18:20:14 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 18:20:17 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 18:20:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 18:20:17 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 18:20:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7669d67fb4cfb54da583e883237da0b279b1fb366b087a0a503ca26d962042`  
		Last Modified: Thu, 24 Jun 2021 18:21:21 GMT  
		Size: 4.6 MB (4615300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a63d38912003c0b7e278dc2e07a5e3595d926f114688e1eba7453d10771507`  
		Last Modified: Thu, 24 Jun 2021 18:21:20 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50aa5d23eab2b64578272b85b1840118f8ce74d4c8a076fd9fdbbf112b389a15`  
		Last Modified: Thu, 24 Jun 2021 18:21:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-alpine3.13` - linux; arm variant v6

```console
$ docker pull nats@sha256:afafd733f206092cfbf83b03d0d219e3ad9fc986d7b9bd1bcc813ba9a164e831
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6897059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a08095811cc4b9caf05423603dec24983d69af81a39a2b582c3fed0698cbcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 19:17:03 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 19:17:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 19:17:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 19:17:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 19:17:09 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 19:17:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072466ad1c8b3759328223593e85cddeedd93281cc285d4fbcc43c2aa77cff8b`  
		Last Modified: Thu, 24 Jun 2021 19:19:11 GMT  
		Size: 4.3 MB (4273957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040948b8c4aa41212a8812f47174f14427d9e2e336d534553442231f4f521882`  
		Last Modified: Thu, 24 Jun 2021 19:19:08 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7ac2240a33c4d9b574bff55265289f9093dcbe62577c93ce04d3b9b145e45e`  
		Last Modified: Thu, 24 Jun 2021 19:19:08 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-alpine3.13` - linux; arm variant v7

```console
$ docker pull nats@sha256:7f77835f7df0ca3c3fbc680a5df2e3a52df9b2bad2ad85a61c9c93588d554e1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6694378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31819633e547bc5673c5be989286c3fa84b4fa83c1cc7e1daac4586d53072bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 23:15:15 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Tue, 15 Jun 2021 23:15:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Jun 2021 04:21:38 GMT
ENV NATS_SERVER=2.3.0
# Fri, 25 Jun 2021 04:21:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 25 Jun 2021 04:21:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 25 Jun 2021 04:21:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Jun 2021 04:21:44 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:21:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Jun 2021 04:21:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b4716e8d6c6e6f099e638134cd5d5cb8d04256d758ebdfe9d484831feb75f6`  
		Last Modified: Fri, 25 Jun 2021 04:23:48 GMT  
		Size: 4.3 MB (4269265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b992d0d507b7fcd3c04c8337fde6b65f98ef5711af47b760054e79a2568c0990`  
		Last Modified: Fri, 25 Jun 2021 04:23:45 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ae15dff3a871a17e97c8114db82e6e7af74fdbb011e105314060415dcc93a3`  
		Last Modified: Fri, 25 Jun 2021 04:23:45 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e7be6da297d4e47e1cbf0cebebb0b28db6ceeb50f8e06e87609dce41de682f92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6953599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0539985a8e92b6e078f0f65ffce3ff416cfa3401034c750ec07b9da7150efce8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 19:06:45 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 19:06:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 19:06:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 19:06:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 19:06:48 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:06:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 19:06:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27d0993acd4f2a9aa99219b53b130917cfcaa7b5ab8f75f92c6853892b1fbd8`  
		Last Modified: Thu, 24 Jun 2021 19:08:02 GMT  
		Size: 4.2 MB (4240601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89210891c944f9ecbd826fe696a7f0a1399ac8628705331d9eb011d633fe7b2`  
		Last Modified: Thu, 24 Jun 2021 19:08:01 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e288f0bb2545133bb23a02793719cdc1076dc77f7c61c80c05c6351f9dc2c482`  
		Last Modified: Thu, 24 Jun 2021 19:08:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3-linux`

```console
$ docker pull nats@sha256:80eb5023b4f9a6a43ccb90613913d8bbd7fb1d60ed202af2e7e7425add895c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.3-linux` - linux; amd64

```console
$ docker pull nats@sha256:9ee8674607d72a7993a833da50a04bb798dc906079f7d4a3ff386ae9c7dad1b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24690f4c9243082798de0d5d0dcf537f0d65e65ba0e4c324f576019af6e88b71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:574cacffaccc18c0ebb219863832f97c5b4a301f1311490b79ebc4f7c91df1c5 in /nats-server 
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 18:20:54 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:55 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 18:20:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff7c72aa6eac78de3e8d419804aa418bec0a1d109825baafe6f27f8d5463c862`  
		Last Modified: Thu, 24 Jun 2021 18:21:47 GMT  
		Size: 4.3 MB (4335042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2e05cfe23a1b83926a7784d3a6f32ee581b1b20019023a53e605a28e098280`  
		Last Modified: Thu, 24 Jun 2021 18:21:45 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4d7fa672d2e979a1f71013d6c0ced4762a775e52c5fa1c597061e0661a4f564
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d818a3d14ec5abc722d14eefa80fd1bbb0cf49078b6a2fb3e54632e211c176c9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:f297049dd293f8bd69f8b37a6337b711a278a532e801780056f74049b995408b in /nats-server 
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:17:28 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:17:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f861ae2df753d566752887dd69fa7c0770cc5d866cf63d89323d119e6e132631`  
		Last Modified: Thu, 24 Jun 2021 19:20:11 GMT  
		Size: 4.0 MB (3992918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442ea4dc62b81dd101ec8289e6ef95821857d589dd412611e32dd41affe68138`  
		Last Modified: Thu, 24 Jun 2021 19:20:08 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:6796429bd41a95837772476ae383c344688bbfa91067d66187cff0919bb9bff5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f262b07aad3ac9672f6fdfdafb0486d87b7afa1949afa2bab951305a9191f6e4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Jun 2021 04:22:05 GMT
COPY file:e739b42ab72b567be37f2b08b7cc64858dc247505c5f9065cbc349f3f7cde026 in /nats-server 
# Fri, 25 Jun 2021 04:22:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 25 Jun 2021 04:22:06 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:22:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Jun 2021 04:22:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4eead17c506be0458b8b300048220b15977a1fb9f1dabb07031134fe7cd321bd`  
		Last Modified: Fri, 25 Jun 2021 04:24:25 GMT  
		Size: 4.0 MB (3987827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71186d5a22ac8937ee584ce8ff166469d1d6e857b4bca58533fb852beaf49aff`  
		Last Modified: Fri, 25 Jun 2021 04:24:23 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9af64abe7058267802b82eea320c8900f01e2900fc14c7819215cc38249b6a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b6ba9c13a2b4e06ce837ee797073c343df1705b660c37b3331e4afc500b19e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:5beb421ec5105e31f6e0b0a14e99795c4d0ca457385b898e67e502f8c1168b1c in /nats-server 
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:07:11 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:07:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:07:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4fa9662b0eb20e8acff5f956ac375b9e6d6bae55ed10b15783f5bdea6e212ca2`  
		Last Modified: Thu, 24 Jun 2021 19:08:34 GMT  
		Size: 4.0 MB (3958114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae902de5ccdf10f5ab555454aaf3ce99d7642bbc3961ef684412f5d45cd03ab`  
		Last Modified: Thu, 24 Jun 2021 19:08:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3-nanoserver`

```console
$ docker pull nats@sha256:4ebe0f8afa0791f4642839c39904f87117ae2b491ef7cc3af12fe3ea313999b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `nats:2.3-nanoserver` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:c3d85580c0f97e9e7525ac25ff6dd2b46e30d0a28d8eae5922200f692c5f5420
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107067292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60db2a891b8d4acaed25bf0dfdd41e93f36804395b740b4fdc1e2bb452c6c1b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 15:55:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:39 GMT
RUN cmd /S /C #(nop) COPY file:bac1db2af96d2ddad22da9ae2b1252ad143dce10623146a5898a15a4e3f18d81 in C:\nats-server.exe 
# Thu, 24 Jun 2021 18:16:42 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:80d93ce19113bbf944b699f12e59395e0eabeb00ccd1fd5dc7df46bb115eba2f`  
		Last Modified: Wed, 09 Jun 2021 15:59:58 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec670391ee18da96972d36cee7981927664f13e0189b3d1f31b2c62e5ca0d4b`  
		Last Modified: Thu, 24 Jun 2021 18:21:31 GMT  
		Size: 4.4 MB (4389381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ee48b932f6c168a30dd680d51235836a69ad93983a5aa6ae510649498009d`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47216eb523d03d9b262b596ac92cdee9995cea672a4b3914a9f02a41a5ff422`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26d8e3fee7dfa3f7bf9b8af44b5f640be79d646bbcb96459100b6b39fe7bda`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348ad20da8616571c92e671840d54b660df38b670f5bf015aeaa2f6bed084657`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3-nanoserver-1809`

```console
$ docker pull nats@sha256:4ebe0f8afa0791f4642839c39904f87117ae2b491ef7cc3af12fe3ea313999b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `nats:2.3-nanoserver-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:c3d85580c0f97e9e7525ac25ff6dd2b46e30d0a28d8eae5922200f692c5f5420
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107067292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60db2a891b8d4acaed25bf0dfdd41e93f36804395b740b4fdc1e2bb452c6c1b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 15:55:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:39 GMT
RUN cmd /S /C #(nop) COPY file:bac1db2af96d2ddad22da9ae2b1252ad143dce10623146a5898a15a4e3f18d81 in C:\nats-server.exe 
# Thu, 24 Jun 2021 18:16:42 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:80d93ce19113bbf944b699f12e59395e0eabeb00ccd1fd5dc7df46bb115eba2f`  
		Last Modified: Wed, 09 Jun 2021 15:59:58 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec670391ee18da96972d36cee7981927664f13e0189b3d1f31b2c62e5ca0d4b`  
		Last Modified: Thu, 24 Jun 2021 18:21:31 GMT  
		Size: 4.4 MB (4389381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ee48b932f6c168a30dd680d51235836a69ad93983a5aa6ae510649498009d`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47216eb523d03d9b262b596ac92cdee9995cea672a4b3914a9f02a41a5ff422`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26d8e3fee7dfa3f7bf9b8af44b5f640be79d646bbcb96459100b6b39fe7bda`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348ad20da8616571c92e671840d54b660df38b670f5bf015aeaa2f6bed084657`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3-scratch`

```console
$ docker pull nats@sha256:80eb5023b4f9a6a43ccb90613913d8bbd7fb1d60ed202af2e7e7425add895c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.3-scratch` - linux; amd64

```console
$ docker pull nats@sha256:9ee8674607d72a7993a833da50a04bb798dc906079f7d4a3ff386ae9c7dad1b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24690f4c9243082798de0d5d0dcf537f0d65e65ba0e4c324f576019af6e88b71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:574cacffaccc18c0ebb219863832f97c5b4a301f1311490b79ebc4f7c91df1c5 in /nats-server 
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 18:20:54 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:55 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 18:20:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff7c72aa6eac78de3e8d419804aa418bec0a1d109825baafe6f27f8d5463c862`  
		Last Modified: Thu, 24 Jun 2021 18:21:47 GMT  
		Size: 4.3 MB (4335042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2e05cfe23a1b83926a7784d3a6f32ee581b1b20019023a53e605a28e098280`  
		Last Modified: Thu, 24 Jun 2021 18:21:45 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4d7fa672d2e979a1f71013d6c0ced4762a775e52c5fa1c597061e0661a4f564
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d818a3d14ec5abc722d14eefa80fd1bbb0cf49078b6a2fb3e54632e211c176c9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:f297049dd293f8bd69f8b37a6337b711a278a532e801780056f74049b995408b in /nats-server 
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:17:28 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:17:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f861ae2df753d566752887dd69fa7c0770cc5d866cf63d89323d119e6e132631`  
		Last Modified: Thu, 24 Jun 2021 19:20:11 GMT  
		Size: 4.0 MB (3992918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442ea4dc62b81dd101ec8289e6ef95821857d589dd412611e32dd41affe68138`  
		Last Modified: Thu, 24 Jun 2021 19:20:08 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:6796429bd41a95837772476ae383c344688bbfa91067d66187cff0919bb9bff5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f262b07aad3ac9672f6fdfdafb0486d87b7afa1949afa2bab951305a9191f6e4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Jun 2021 04:22:05 GMT
COPY file:e739b42ab72b567be37f2b08b7cc64858dc247505c5f9065cbc349f3f7cde026 in /nats-server 
# Fri, 25 Jun 2021 04:22:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 25 Jun 2021 04:22:06 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:22:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Jun 2021 04:22:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4eead17c506be0458b8b300048220b15977a1fb9f1dabb07031134fe7cd321bd`  
		Last Modified: Fri, 25 Jun 2021 04:24:25 GMT  
		Size: 4.0 MB (3987827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71186d5a22ac8937ee584ce8ff166469d1d6e857b4bca58533fb852beaf49aff`  
		Last Modified: Fri, 25 Jun 2021 04:24:23 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9af64abe7058267802b82eea320c8900f01e2900fc14c7819215cc38249b6a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b6ba9c13a2b4e06ce837ee797073c343df1705b660c37b3331e4afc500b19e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:5beb421ec5105e31f6e0b0a14e99795c4d0ca457385b898e67e502f8c1168b1c in /nats-server 
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:07:11 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:07:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:07:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4fa9662b0eb20e8acff5f956ac375b9e6d6bae55ed10b15783f5bdea6e212ca2`  
		Last Modified: Thu, 24 Jun 2021 19:08:34 GMT  
		Size: 4.0 MB (3958114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae902de5ccdf10f5ab555454aaf3ce99d7642bbc3961ef684412f5d45cd03ab`  
		Last Modified: Thu, 24 Jun 2021 19:08:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3-windowsservercore`

```console
$ docker pull nats@sha256:0a82183999395fc7ff72a6528b06205f06ca31baa3e914a3c43496de2242b3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64
	-	windows version 10.0.14393.4467; amd64

### `nats:2.3-windowsservercore` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:2b5fc0956f7fa5e8a5d73443e2b2cff10b2c5a1d750238f0c39d388ad230e889
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2646697143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3296c025e7c6bdec1087e1cd78a2af9c8398fde53f8acc26c4c2c62dade1e2fc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 13:15:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 15:52:54 GMT
ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:14:27 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:14:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.0/nats-server-v2.3.0-windows-amd64.zip
# Thu, 24 Jun 2021 18:14:33 GMT
ENV NATS_SERVER_SHASUM=4cf3cad0f3fc635a7be429ab13d852b1eea41c8f81b5d9ef7f21d93dd99a1f6f
# Thu, 24 Jun 2021 18:15:14 GMT
RUN Set-PSDebug -Trace 2
# Thu, 24 Jun 2021 18:16:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 24 Jun 2021 18:16:20 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:22 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae7d2dc4b590128efeafd375d02122e65a2525623ac2be100c1a390caf8a4b49`  
		Last Modified: Wed, 09 Jun 2021 15:28:02 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507a90d55d261855b42c7b5905599cdc274ca135ad962fffffe1fa6246c9bba7`  
		Last Modified: Wed, 09 Jun 2021 15:59:38 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29775406c1781fcc27d8bf50b4b0bfcd9418dda6cfae494e4d9383e0213df24b`  
		Last Modified: Thu, 24 Jun 2021 18:21:11 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3bf008ba6d0a427891ae36a26107b3e1f386cb9be8dbd0427623920c08cb93`  
		Last Modified: Thu, 24 Jun 2021 18:21:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35cb02232de3ac8c2255dee0bc6a718b0b3cb29b7baa3caf9825fae6519353c`  
		Last Modified: Thu, 24 Jun 2021 18:21:12 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8811ca1ef9b5e7b658fe9eb6dcf4145a8c7fc2108cddf27604a32625196d9435`  
		Last Modified: Thu, 24 Jun 2021 18:21:12 GMT  
		Size: 363.9 KB (363906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07799fa10e1ce0eeb453bb8919dd2756d7f46df37096e364eaef1cf48ee4d27b`  
		Last Modified: Thu, 24 Jun 2021 18:21:11 GMT  
		Size: 4.7 MB (4734976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7d8a61897a84ba84d3157167674e44f39375855accec3dbfd1bfcc8fb1911d`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.9 KB (1921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5675249b0aafebc9b96c1c5359219fa68fe30b7e67d7877c5d2a8c6083b153da`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42271808b9146dc5744c45edba3f979ab16c9a382b62c44320fa4f04f9ab0f97`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dd08bcc8b2cc2e24a6318d63fcc471176adf3acdf78b10ac15b1fa5527c568`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-windowsservercore` - windows version 10.0.14393.4467; amd64

```console
$ docker pull nats@sha256:845b27a65fd56c97937856e216d7771d144a8b90c4cce3b45562de4761576f93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6270853814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87d244a19fd78d48d37bc35a9b3997f8dafc00fcce0da603d7a5aa6aa095429`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 13:26:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 15:55:27 GMT
ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:58 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:17:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.0/nats-server-v2.3.0-windows-amd64.zip
# Thu, 24 Jun 2021 18:17:03 GMT
ENV NATS_SERVER_SHASUM=4cf3cad0f3fc635a7be429ab13d852b1eea41c8f81b5d9ef7f21d93dd99a1f6f
# Thu, 24 Jun 2021 18:18:18 GMT
RUN Set-PSDebug -Trace 2
# Thu, 24 Jun 2021 18:20:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 24 Jun 2021 18:20:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:20:17 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:20:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2f52abeee6d6f4a925ad418b5e6200d4fca9bf92834ffc918b8bbaccd34251db`  
		Size: 2.2 GB (2195741359 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fa4e6085e5538e957ef06561fe1e62dff898da7f4bb577e81da74323aecab2d7`  
		Last Modified: Wed, 09 Jun 2021 15:28:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db57f94547be7109ad927e2f9d04a0501a2a5f0cb91ad8c4385eb32758f86b9`  
		Last Modified: Wed, 09 Jun 2021 16:00:21 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385a2e510feddc0676b3c17e1654e2430eb4ac4a8a775b78e89afaccc5fdc804`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c18a811e26704bd4bb49d57454d177eb277d065d5841d36f6fe5dce50a4fda`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154f452c578ee0bf6e0aa67510a192c41adaf4a94d974a0909c227cc29bf6b18`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45d0a6fab2e6e94ed71f11798975da67d62cc86ebc458ce3e3a12bbe7f250d8`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 352.1 KB (352114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d373c50c3af9ea67008c088d5b13b3963be0c55dea90c371d8a1be5ba44d2a84`  
		Last Modified: Thu, 24 Jun 2021 18:21:51 GMT  
		Size: 4.8 MB (4761699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1065e6f071db7571880f6c942f08e2565dde2da5ee37a3d79bdeca96583d8`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f1549b605bdde25fa57f56f24f602d8605121787ac6d452d1eae704c173ba5`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6659b0e6d881d37794c4ac62633dad4743618a980578bdbe8e7a4e5d617211`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c424710ae455acf452bd0eba0e1e696916ed091e236132a564e02b266431cc3`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3-windowsservercore-1809`

```console
$ docker pull nats@sha256:a673dfea57d51e9d21677796f5f72f60d13dab15b74dd8b2dfe32518cd6ca782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `nats:2.3-windowsservercore-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:2b5fc0956f7fa5e8a5d73443e2b2cff10b2c5a1d750238f0c39d388ad230e889
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2646697143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3296c025e7c6bdec1087e1cd78a2af9c8398fde53f8acc26c4c2c62dade1e2fc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 13:15:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 15:52:54 GMT
ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:14:27 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:14:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.0/nats-server-v2.3.0-windows-amd64.zip
# Thu, 24 Jun 2021 18:14:33 GMT
ENV NATS_SERVER_SHASUM=4cf3cad0f3fc635a7be429ab13d852b1eea41c8f81b5d9ef7f21d93dd99a1f6f
# Thu, 24 Jun 2021 18:15:14 GMT
RUN Set-PSDebug -Trace 2
# Thu, 24 Jun 2021 18:16:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 24 Jun 2021 18:16:20 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:22 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae7d2dc4b590128efeafd375d02122e65a2525623ac2be100c1a390caf8a4b49`  
		Last Modified: Wed, 09 Jun 2021 15:28:02 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507a90d55d261855b42c7b5905599cdc274ca135ad962fffffe1fa6246c9bba7`  
		Last Modified: Wed, 09 Jun 2021 15:59:38 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29775406c1781fcc27d8bf50b4b0bfcd9418dda6cfae494e4d9383e0213df24b`  
		Last Modified: Thu, 24 Jun 2021 18:21:11 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3bf008ba6d0a427891ae36a26107b3e1f386cb9be8dbd0427623920c08cb93`  
		Last Modified: Thu, 24 Jun 2021 18:21:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35cb02232de3ac8c2255dee0bc6a718b0b3cb29b7baa3caf9825fae6519353c`  
		Last Modified: Thu, 24 Jun 2021 18:21:12 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8811ca1ef9b5e7b658fe9eb6dcf4145a8c7fc2108cddf27604a32625196d9435`  
		Last Modified: Thu, 24 Jun 2021 18:21:12 GMT  
		Size: 363.9 KB (363906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07799fa10e1ce0eeb453bb8919dd2756d7f46df37096e364eaef1cf48ee4d27b`  
		Last Modified: Thu, 24 Jun 2021 18:21:11 GMT  
		Size: 4.7 MB (4734976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7d8a61897a84ba84d3157167674e44f39375855accec3dbfd1bfcc8fb1911d`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.9 KB (1921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5675249b0aafebc9b96c1c5359219fa68fe30b7e67d7877c5d2a8c6083b153da`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42271808b9146dc5744c45edba3f979ab16c9a382b62c44320fa4f04f9ab0f97`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dd08bcc8b2cc2e24a6318d63fcc471176adf3acdf78b10ac15b1fa5527c568`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:0e0a6967d374622f82cf5383e0c8751541a791a255a4c728eaa86e51af9560c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4467; amd64

### `nats:2.3-windowsservercore-ltsc2016` - windows version 10.0.14393.4467; amd64

```console
$ docker pull nats@sha256:845b27a65fd56c97937856e216d7771d144a8b90c4cce3b45562de4761576f93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6270853814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87d244a19fd78d48d37bc35a9b3997f8dafc00fcce0da603d7a5aa6aa095429`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 13:26:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 15:55:27 GMT
ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:58 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:17:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.0/nats-server-v2.3.0-windows-amd64.zip
# Thu, 24 Jun 2021 18:17:03 GMT
ENV NATS_SERVER_SHASUM=4cf3cad0f3fc635a7be429ab13d852b1eea41c8f81b5d9ef7f21d93dd99a1f6f
# Thu, 24 Jun 2021 18:18:18 GMT
RUN Set-PSDebug -Trace 2
# Thu, 24 Jun 2021 18:20:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 24 Jun 2021 18:20:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:20:17 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:20:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2f52abeee6d6f4a925ad418b5e6200d4fca9bf92834ffc918b8bbaccd34251db`  
		Size: 2.2 GB (2195741359 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fa4e6085e5538e957ef06561fe1e62dff898da7f4bb577e81da74323aecab2d7`  
		Last Modified: Wed, 09 Jun 2021 15:28:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db57f94547be7109ad927e2f9d04a0501a2a5f0cb91ad8c4385eb32758f86b9`  
		Last Modified: Wed, 09 Jun 2021 16:00:21 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385a2e510feddc0676b3c17e1654e2430eb4ac4a8a775b78e89afaccc5fdc804`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c18a811e26704bd4bb49d57454d177eb277d065d5841d36f6fe5dce50a4fda`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154f452c578ee0bf6e0aa67510a192c41adaf4a94d974a0909c227cc29bf6b18`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45d0a6fab2e6e94ed71f11798975da67d62cc86ebc458ce3e3a12bbe7f250d8`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 352.1 KB (352114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d373c50c3af9ea67008c088d5b13b3963be0c55dea90c371d8a1be5ba44d2a84`  
		Last Modified: Thu, 24 Jun 2021 18:21:51 GMT  
		Size: 4.8 MB (4761699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1065e6f071db7571880f6c942f08e2565dde2da5ee37a3d79bdeca96583d8`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f1549b605bdde25fa57f56f24f602d8605121787ac6d452d1eae704c173ba5`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6659b0e6d881d37794c4ac62633dad4743618a980578bdbe8e7a4e5d617211`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c424710ae455acf452bd0eba0e1e696916ed091e236132a564e02b266431cc3`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.0`

```console
$ docker pull nats@sha256:6aa7af6180050c241f606d59de7b4be510dbaddac5ae8855e5d84e4aae54ca42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1999; amd64

### `nats:2.3.0` - linux; amd64

```console
$ docker pull nats@sha256:9ee8674607d72a7993a833da50a04bb798dc906079f7d4a3ff386ae9c7dad1b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24690f4c9243082798de0d5d0dcf537f0d65e65ba0e4c324f576019af6e88b71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:574cacffaccc18c0ebb219863832f97c5b4a301f1311490b79ebc4f7c91df1c5 in /nats-server 
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 18:20:54 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:55 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 18:20:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff7c72aa6eac78de3e8d419804aa418bec0a1d109825baafe6f27f8d5463c862`  
		Last Modified: Thu, 24 Jun 2021 18:21:47 GMT  
		Size: 4.3 MB (4335042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2e05cfe23a1b83926a7784d3a6f32ee581b1b20019023a53e605a28e098280`  
		Last Modified: Thu, 24 Jun 2021 18:21:45 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.0` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4d7fa672d2e979a1f71013d6c0ced4762a775e52c5fa1c597061e0661a4f564
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d818a3d14ec5abc722d14eefa80fd1bbb0cf49078b6a2fb3e54632e211c176c9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:f297049dd293f8bd69f8b37a6337b711a278a532e801780056f74049b995408b in /nats-server 
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:17:28 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:17:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f861ae2df753d566752887dd69fa7c0770cc5d866cf63d89323d119e6e132631`  
		Last Modified: Thu, 24 Jun 2021 19:20:11 GMT  
		Size: 4.0 MB (3992918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442ea4dc62b81dd101ec8289e6ef95821857d589dd412611e32dd41affe68138`  
		Last Modified: Thu, 24 Jun 2021 19:20:08 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.0` - linux; arm variant v7

```console
$ docker pull nats@sha256:6796429bd41a95837772476ae383c344688bbfa91067d66187cff0919bb9bff5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f262b07aad3ac9672f6fdfdafb0486d87b7afa1949afa2bab951305a9191f6e4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Jun 2021 04:22:05 GMT
COPY file:e739b42ab72b567be37f2b08b7cc64858dc247505c5f9065cbc349f3f7cde026 in /nats-server 
# Fri, 25 Jun 2021 04:22:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 25 Jun 2021 04:22:06 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:22:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Jun 2021 04:22:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4eead17c506be0458b8b300048220b15977a1fb9f1dabb07031134fe7cd321bd`  
		Last Modified: Fri, 25 Jun 2021 04:24:25 GMT  
		Size: 4.0 MB (3987827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71186d5a22ac8937ee584ce8ff166469d1d6e857b4bca58533fb852beaf49aff`  
		Last Modified: Fri, 25 Jun 2021 04:24:23 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.0` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9af64abe7058267802b82eea320c8900f01e2900fc14c7819215cc38249b6a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b6ba9c13a2b4e06ce837ee797073c343df1705b660c37b3331e4afc500b19e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:5beb421ec5105e31f6e0b0a14e99795c4d0ca457385b898e67e502f8c1168b1c in /nats-server 
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:07:11 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:07:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:07:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4fa9662b0eb20e8acff5f956ac375b9e6d6bae55ed10b15783f5bdea6e212ca2`  
		Last Modified: Thu, 24 Jun 2021 19:08:34 GMT  
		Size: 4.0 MB (3958114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae902de5ccdf10f5ab555454aaf3ce99d7642bbc3961ef684412f5d45cd03ab`  
		Last Modified: Thu, 24 Jun 2021 19:08:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.0` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:c3d85580c0f97e9e7525ac25ff6dd2b46e30d0a28d8eae5922200f692c5f5420
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107067292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60db2a891b8d4acaed25bf0dfdd41e93f36804395b740b4fdc1e2bb452c6c1b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 15:55:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:39 GMT
RUN cmd /S /C #(nop) COPY file:bac1db2af96d2ddad22da9ae2b1252ad143dce10623146a5898a15a4e3f18d81 in C:\nats-server.exe 
# Thu, 24 Jun 2021 18:16:42 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:80d93ce19113bbf944b699f12e59395e0eabeb00ccd1fd5dc7df46bb115eba2f`  
		Last Modified: Wed, 09 Jun 2021 15:59:58 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec670391ee18da96972d36cee7981927664f13e0189b3d1f31b2c62e5ca0d4b`  
		Last Modified: Thu, 24 Jun 2021 18:21:31 GMT  
		Size: 4.4 MB (4389381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ee48b932f6c168a30dd680d51235836a69ad93983a5aa6ae510649498009d`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47216eb523d03d9b262b596ac92cdee9995cea672a4b3914a9f02a41a5ff422`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26d8e3fee7dfa3f7bf9b8af44b5f640be79d646bbcb96459100b6b39fe7bda`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348ad20da8616571c92e671840d54b660df38b670f5bf015aeaa2f6bed084657`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.0-alpine`

```console
$ docker pull nats@sha256:ff5570b8f85ec8849d5b58316e2984352cc44e7f65a3cfeabb0cbbe9933db4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.3.0-alpine` - linux; amd64

```console
$ docker pull nats@sha256:11ac3d707fd53db8987f4e5432397c58bcd7fcd98e9c056088f709a58b4fc3a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2523bcf697d78fbb44315448e0c04248daa07f5741fc4c1d82224203a3a1a982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 18:20:14 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 18:20:17 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 18:20:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 18:20:17 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 18:20:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7669d67fb4cfb54da583e883237da0b279b1fb366b087a0a503ca26d962042`  
		Last Modified: Thu, 24 Jun 2021 18:21:21 GMT  
		Size: 4.6 MB (4615300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a63d38912003c0b7e278dc2e07a5e3595d926f114688e1eba7453d10771507`  
		Last Modified: Thu, 24 Jun 2021 18:21:20 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50aa5d23eab2b64578272b85b1840118f8ce74d4c8a076fd9fdbbf112b389a15`  
		Last Modified: Thu, 24 Jun 2021 18:21:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.0-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:afafd733f206092cfbf83b03d0d219e3ad9fc986d7b9bd1bcc813ba9a164e831
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6897059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a08095811cc4b9caf05423603dec24983d69af81a39a2b582c3fed0698cbcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 19:17:03 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 19:17:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 19:17:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 19:17:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 19:17:09 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 19:17:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072466ad1c8b3759328223593e85cddeedd93281cc285d4fbcc43c2aa77cff8b`  
		Last Modified: Thu, 24 Jun 2021 19:19:11 GMT  
		Size: 4.3 MB (4273957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040948b8c4aa41212a8812f47174f14427d9e2e336d534553442231f4f521882`  
		Last Modified: Thu, 24 Jun 2021 19:19:08 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7ac2240a33c4d9b574bff55265289f9093dcbe62577c93ce04d3b9b145e45e`  
		Last Modified: Thu, 24 Jun 2021 19:19:08 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.0-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:7f77835f7df0ca3c3fbc680a5df2e3a52df9b2bad2ad85a61c9c93588d554e1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6694378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31819633e547bc5673c5be989286c3fa84b4fa83c1cc7e1daac4586d53072bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 23:15:15 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Tue, 15 Jun 2021 23:15:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Jun 2021 04:21:38 GMT
ENV NATS_SERVER=2.3.0
# Fri, 25 Jun 2021 04:21:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 25 Jun 2021 04:21:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 25 Jun 2021 04:21:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Jun 2021 04:21:44 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:21:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Jun 2021 04:21:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b4716e8d6c6e6f099e638134cd5d5cb8d04256d758ebdfe9d484831feb75f6`  
		Last Modified: Fri, 25 Jun 2021 04:23:48 GMT  
		Size: 4.3 MB (4269265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b992d0d507b7fcd3c04c8337fde6b65f98ef5711af47b760054e79a2568c0990`  
		Last Modified: Fri, 25 Jun 2021 04:23:45 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ae15dff3a871a17e97c8114db82e6e7af74fdbb011e105314060415dcc93a3`  
		Last Modified: Fri, 25 Jun 2021 04:23:45 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.0-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e7be6da297d4e47e1cbf0cebebb0b28db6ceeb50f8e06e87609dce41de682f92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6953599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0539985a8e92b6e078f0f65ffce3ff416cfa3401034c750ec07b9da7150efce8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 19:06:45 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 19:06:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 19:06:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 19:06:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 19:06:48 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:06:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 19:06:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27d0993acd4f2a9aa99219b53b130917cfcaa7b5ab8f75f92c6853892b1fbd8`  
		Last Modified: Thu, 24 Jun 2021 19:08:02 GMT  
		Size: 4.2 MB (4240601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89210891c944f9ecbd826fe696a7f0a1399ac8628705331d9eb011d633fe7b2`  
		Last Modified: Thu, 24 Jun 2021 19:08:01 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e288f0bb2545133bb23a02793719cdc1076dc77f7c61c80c05c6351f9dc2c482`  
		Last Modified: Thu, 24 Jun 2021 19:08:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.0-alpine3.13`

```console
$ docker pull nats@sha256:ff5570b8f85ec8849d5b58316e2984352cc44e7f65a3cfeabb0cbbe9933db4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.3.0-alpine3.13` - linux; amd64

```console
$ docker pull nats@sha256:11ac3d707fd53db8987f4e5432397c58bcd7fcd98e9c056088f709a58b4fc3a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2523bcf697d78fbb44315448e0c04248daa07f5741fc4c1d82224203a3a1a982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 18:20:14 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 18:20:17 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 18:20:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 18:20:17 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 18:20:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7669d67fb4cfb54da583e883237da0b279b1fb366b087a0a503ca26d962042`  
		Last Modified: Thu, 24 Jun 2021 18:21:21 GMT  
		Size: 4.6 MB (4615300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a63d38912003c0b7e278dc2e07a5e3595d926f114688e1eba7453d10771507`  
		Last Modified: Thu, 24 Jun 2021 18:21:20 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50aa5d23eab2b64578272b85b1840118f8ce74d4c8a076fd9fdbbf112b389a15`  
		Last Modified: Thu, 24 Jun 2021 18:21:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.0-alpine3.13` - linux; arm variant v6

```console
$ docker pull nats@sha256:afafd733f206092cfbf83b03d0d219e3ad9fc986d7b9bd1bcc813ba9a164e831
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6897059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a08095811cc4b9caf05423603dec24983d69af81a39a2b582c3fed0698cbcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 19:17:03 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 19:17:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 19:17:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 19:17:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 19:17:09 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 19:17:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072466ad1c8b3759328223593e85cddeedd93281cc285d4fbcc43c2aa77cff8b`  
		Last Modified: Thu, 24 Jun 2021 19:19:11 GMT  
		Size: 4.3 MB (4273957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040948b8c4aa41212a8812f47174f14427d9e2e336d534553442231f4f521882`  
		Last Modified: Thu, 24 Jun 2021 19:19:08 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7ac2240a33c4d9b574bff55265289f9093dcbe62577c93ce04d3b9b145e45e`  
		Last Modified: Thu, 24 Jun 2021 19:19:08 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.0-alpine3.13` - linux; arm variant v7

```console
$ docker pull nats@sha256:7f77835f7df0ca3c3fbc680a5df2e3a52df9b2bad2ad85a61c9c93588d554e1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6694378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31819633e547bc5673c5be989286c3fa84b4fa83c1cc7e1daac4586d53072bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 23:15:15 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Tue, 15 Jun 2021 23:15:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Jun 2021 04:21:38 GMT
ENV NATS_SERVER=2.3.0
# Fri, 25 Jun 2021 04:21:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 25 Jun 2021 04:21:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 25 Jun 2021 04:21:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Jun 2021 04:21:44 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:21:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Jun 2021 04:21:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b4716e8d6c6e6f099e638134cd5d5cb8d04256d758ebdfe9d484831feb75f6`  
		Last Modified: Fri, 25 Jun 2021 04:23:48 GMT  
		Size: 4.3 MB (4269265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b992d0d507b7fcd3c04c8337fde6b65f98ef5711af47b760054e79a2568c0990`  
		Last Modified: Fri, 25 Jun 2021 04:23:45 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ae15dff3a871a17e97c8114db82e6e7af74fdbb011e105314060415dcc93a3`  
		Last Modified: Fri, 25 Jun 2021 04:23:45 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.0-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e7be6da297d4e47e1cbf0cebebb0b28db6ceeb50f8e06e87609dce41de682f92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6953599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0539985a8e92b6e078f0f65ffce3ff416cfa3401034c750ec07b9da7150efce8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 19:06:45 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 19:06:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 19:06:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 19:06:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 19:06:48 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:06:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 19:06:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27d0993acd4f2a9aa99219b53b130917cfcaa7b5ab8f75f92c6853892b1fbd8`  
		Last Modified: Thu, 24 Jun 2021 19:08:02 GMT  
		Size: 4.2 MB (4240601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89210891c944f9ecbd826fe696a7f0a1399ac8628705331d9eb011d633fe7b2`  
		Last Modified: Thu, 24 Jun 2021 19:08:01 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e288f0bb2545133bb23a02793719cdc1076dc77f7c61c80c05c6351f9dc2c482`  
		Last Modified: Thu, 24 Jun 2021 19:08:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.0-linux`

```console
$ docker pull nats@sha256:80eb5023b4f9a6a43ccb90613913d8bbd7fb1d60ed202af2e7e7425add895c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.3.0-linux` - linux; amd64

```console
$ docker pull nats@sha256:9ee8674607d72a7993a833da50a04bb798dc906079f7d4a3ff386ae9c7dad1b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24690f4c9243082798de0d5d0dcf537f0d65e65ba0e4c324f576019af6e88b71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:574cacffaccc18c0ebb219863832f97c5b4a301f1311490b79ebc4f7c91df1c5 in /nats-server 
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 18:20:54 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:55 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 18:20:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff7c72aa6eac78de3e8d419804aa418bec0a1d109825baafe6f27f8d5463c862`  
		Last Modified: Thu, 24 Jun 2021 18:21:47 GMT  
		Size: 4.3 MB (4335042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2e05cfe23a1b83926a7784d3a6f32ee581b1b20019023a53e605a28e098280`  
		Last Modified: Thu, 24 Jun 2021 18:21:45 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.0-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4d7fa672d2e979a1f71013d6c0ced4762a775e52c5fa1c597061e0661a4f564
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d818a3d14ec5abc722d14eefa80fd1bbb0cf49078b6a2fb3e54632e211c176c9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:f297049dd293f8bd69f8b37a6337b711a278a532e801780056f74049b995408b in /nats-server 
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:17:28 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:17:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f861ae2df753d566752887dd69fa7c0770cc5d866cf63d89323d119e6e132631`  
		Last Modified: Thu, 24 Jun 2021 19:20:11 GMT  
		Size: 4.0 MB (3992918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442ea4dc62b81dd101ec8289e6ef95821857d589dd412611e32dd41affe68138`  
		Last Modified: Thu, 24 Jun 2021 19:20:08 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.0-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:6796429bd41a95837772476ae383c344688bbfa91067d66187cff0919bb9bff5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f262b07aad3ac9672f6fdfdafb0486d87b7afa1949afa2bab951305a9191f6e4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Jun 2021 04:22:05 GMT
COPY file:e739b42ab72b567be37f2b08b7cc64858dc247505c5f9065cbc349f3f7cde026 in /nats-server 
# Fri, 25 Jun 2021 04:22:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 25 Jun 2021 04:22:06 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:22:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Jun 2021 04:22:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4eead17c506be0458b8b300048220b15977a1fb9f1dabb07031134fe7cd321bd`  
		Last Modified: Fri, 25 Jun 2021 04:24:25 GMT  
		Size: 4.0 MB (3987827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71186d5a22ac8937ee584ce8ff166469d1d6e857b4bca58533fb852beaf49aff`  
		Last Modified: Fri, 25 Jun 2021 04:24:23 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.0-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9af64abe7058267802b82eea320c8900f01e2900fc14c7819215cc38249b6a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b6ba9c13a2b4e06ce837ee797073c343df1705b660c37b3331e4afc500b19e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:5beb421ec5105e31f6e0b0a14e99795c4d0ca457385b898e67e502f8c1168b1c in /nats-server 
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:07:11 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:07:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:07:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4fa9662b0eb20e8acff5f956ac375b9e6d6bae55ed10b15783f5bdea6e212ca2`  
		Last Modified: Thu, 24 Jun 2021 19:08:34 GMT  
		Size: 4.0 MB (3958114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae902de5ccdf10f5ab555454aaf3ce99d7642bbc3961ef684412f5d45cd03ab`  
		Last Modified: Thu, 24 Jun 2021 19:08:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.0-nanoserver`

```console
$ docker pull nats@sha256:4ebe0f8afa0791f4642839c39904f87117ae2b491ef7cc3af12fe3ea313999b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `nats:2.3.0-nanoserver` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:c3d85580c0f97e9e7525ac25ff6dd2b46e30d0a28d8eae5922200f692c5f5420
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107067292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60db2a891b8d4acaed25bf0dfdd41e93f36804395b740b4fdc1e2bb452c6c1b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 15:55:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:39 GMT
RUN cmd /S /C #(nop) COPY file:bac1db2af96d2ddad22da9ae2b1252ad143dce10623146a5898a15a4e3f18d81 in C:\nats-server.exe 
# Thu, 24 Jun 2021 18:16:42 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:80d93ce19113bbf944b699f12e59395e0eabeb00ccd1fd5dc7df46bb115eba2f`  
		Last Modified: Wed, 09 Jun 2021 15:59:58 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec670391ee18da96972d36cee7981927664f13e0189b3d1f31b2c62e5ca0d4b`  
		Last Modified: Thu, 24 Jun 2021 18:21:31 GMT  
		Size: 4.4 MB (4389381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ee48b932f6c168a30dd680d51235836a69ad93983a5aa6ae510649498009d`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47216eb523d03d9b262b596ac92cdee9995cea672a4b3914a9f02a41a5ff422`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26d8e3fee7dfa3f7bf9b8af44b5f640be79d646bbcb96459100b6b39fe7bda`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348ad20da8616571c92e671840d54b660df38b670f5bf015aeaa2f6bed084657`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.0-nanoserver-1809`

```console
$ docker pull nats@sha256:4ebe0f8afa0791f4642839c39904f87117ae2b491ef7cc3af12fe3ea313999b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `nats:2.3.0-nanoserver-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:c3d85580c0f97e9e7525ac25ff6dd2b46e30d0a28d8eae5922200f692c5f5420
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107067292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60db2a891b8d4acaed25bf0dfdd41e93f36804395b740b4fdc1e2bb452c6c1b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 15:55:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:39 GMT
RUN cmd /S /C #(nop) COPY file:bac1db2af96d2ddad22da9ae2b1252ad143dce10623146a5898a15a4e3f18d81 in C:\nats-server.exe 
# Thu, 24 Jun 2021 18:16:42 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:80d93ce19113bbf944b699f12e59395e0eabeb00ccd1fd5dc7df46bb115eba2f`  
		Last Modified: Wed, 09 Jun 2021 15:59:58 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec670391ee18da96972d36cee7981927664f13e0189b3d1f31b2c62e5ca0d4b`  
		Last Modified: Thu, 24 Jun 2021 18:21:31 GMT  
		Size: 4.4 MB (4389381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ee48b932f6c168a30dd680d51235836a69ad93983a5aa6ae510649498009d`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47216eb523d03d9b262b596ac92cdee9995cea672a4b3914a9f02a41a5ff422`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26d8e3fee7dfa3f7bf9b8af44b5f640be79d646bbcb96459100b6b39fe7bda`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348ad20da8616571c92e671840d54b660df38b670f5bf015aeaa2f6bed084657`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.0-scratch`

```console
$ docker pull nats@sha256:80eb5023b4f9a6a43ccb90613913d8bbd7fb1d60ed202af2e7e7425add895c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.3.0-scratch` - linux; amd64

```console
$ docker pull nats@sha256:9ee8674607d72a7993a833da50a04bb798dc906079f7d4a3ff386ae9c7dad1b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24690f4c9243082798de0d5d0dcf537f0d65e65ba0e4c324f576019af6e88b71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:574cacffaccc18c0ebb219863832f97c5b4a301f1311490b79ebc4f7c91df1c5 in /nats-server 
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 18:20:54 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:55 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 18:20:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff7c72aa6eac78de3e8d419804aa418bec0a1d109825baafe6f27f8d5463c862`  
		Last Modified: Thu, 24 Jun 2021 18:21:47 GMT  
		Size: 4.3 MB (4335042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2e05cfe23a1b83926a7784d3a6f32ee581b1b20019023a53e605a28e098280`  
		Last Modified: Thu, 24 Jun 2021 18:21:45 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.0-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4d7fa672d2e979a1f71013d6c0ced4762a775e52c5fa1c597061e0661a4f564
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d818a3d14ec5abc722d14eefa80fd1bbb0cf49078b6a2fb3e54632e211c176c9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:f297049dd293f8bd69f8b37a6337b711a278a532e801780056f74049b995408b in /nats-server 
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:17:28 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:17:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f861ae2df753d566752887dd69fa7c0770cc5d866cf63d89323d119e6e132631`  
		Last Modified: Thu, 24 Jun 2021 19:20:11 GMT  
		Size: 4.0 MB (3992918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442ea4dc62b81dd101ec8289e6ef95821857d589dd412611e32dd41affe68138`  
		Last Modified: Thu, 24 Jun 2021 19:20:08 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.0-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:6796429bd41a95837772476ae383c344688bbfa91067d66187cff0919bb9bff5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f262b07aad3ac9672f6fdfdafb0486d87b7afa1949afa2bab951305a9191f6e4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Jun 2021 04:22:05 GMT
COPY file:e739b42ab72b567be37f2b08b7cc64858dc247505c5f9065cbc349f3f7cde026 in /nats-server 
# Fri, 25 Jun 2021 04:22:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 25 Jun 2021 04:22:06 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:22:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Jun 2021 04:22:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4eead17c506be0458b8b300048220b15977a1fb9f1dabb07031134fe7cd321bd`  
		Last Modified: Fri, 25 Jun 2021 04:24:25 GMT  
		Size: 4.0 MB (3987827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71186d5a22ac8937ee584ce8ff166469d1d6e857b4bca58533fb852beaf49aff`  
		Last Modified: Fri, 25 Jun 2021 04:24:23 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.0-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9af64abe7058267802b82eea320c8900f01e2900fc14c7819215cc38249b6a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b6ba9c13a2b4e06ce837ee797073c343df1705b660c37b3331e4afc500b19e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:5beb421ec5105e31f6e0b0a14e99795c4d0ca457385b898e67e502f8c1168b1c in /nats-server 
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:07:11 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:07:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:07:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4fa9662b0eb20e8acff5f956ac375b9e6d6bae55ed10b15783f5bdea6e212ca2`  
		Last Modified: Thu, 24 Jun 2021 19:08:34 GMT  
		Size: 4.0 MB (3958114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae902de5ccdf10f5ab555454aaf3ce99d7642bbc3961ef684412f5d45cd03ab`  
		Last Modified: Thu, 24 Jun 2021 19:08:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.0-windowsservercore`

```console
$ docker pull nats@sha256:0a82183999395fc7ff72a6528b06205f06ca31baa3e914a3c43496de2242b3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64
	-	windows version 10.0.14393.4467; amd64

### `nats:2.3.0-windowsservercore` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:2b5fc0956f7fa5e8a5d73443e2b2cff10b2c5a1d750238f0c39d388ad230e889
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2646697143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3296c025e7c6bdec1087e1cd78a2af9c8398fde53f8acc26c4c2c62dade1e2fc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 13:15:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 15:52:54 GMT
ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:14:27 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:14:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.0/nats-server-v2.3.0-windows-amd64.zip
# Thu, 24 Jun 2021 18:14:33 GMT
ENV NATS_SERVER_SHASUM=4cf3cad0f3fc635a7be429ab13d852b1eea41c8f81b5d9ef7f21d93dd99a1f6f
# Thu, 24 Jun 2021 18:15:14 GMT
RUN Set-PSDebug -Trace 2
# Thu, 24 Jun 2021 18:16:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 24 Jun 2021 18:16:20 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:22 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae7d2dc4b590128efeafd375d02122e65a2525623ac2be100c1a390caf8a4b49`  
		Last Modified: Wed, 09 Jun 2021 15:28:02 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507a90d55d261855b42c7b5905599cdc274ca135ad962fffffe1fa6246c9bba7`  
		Last Modified: Wed, 09 Jun 2021 15:59:38 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29775406c1781fcc27d8bf50b4b0bfcd9418dda6cfae494e4d9383e0213df24b`  
		Last Modified: Thu, 24 Jun 2021 18:21:11 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3bf008ba6d0a427891ae36a26107b3e1f386cb9be8dbd0427623920c08cb93`  
		Last Modified: Thu, 24 Jun 2021 18:21:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35cb02232de3ac8c2255dee0bc6a718b0b3cb29b7baa3caf9825fae6519353c`  
		Last Modified: Thu, 24 Jun 2021 18:21:12 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8811ca1ef9b5e7b658fe9eb6dcf4145a8c7fc2108cddf27604a32625196d9435`  
		Last Modified: Thu, 24 Jun 2021 18:21:12 GMT  
		Size: 363.9 KB (363906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07799fa10e1ce0eeb453bb8919dd2756d7f46df37096e364eaef1cf48ee4d27b`  
		Last Modified: Thu, 24 Jun 2021 18:21:11 GMT  
		Size: 4.7 MB (4734976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7d8a61897a84ba84d3157167674e44f39375855accec3dbfd1bfcc8fb1911d`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.9 KB (1921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5675249b0aafebc9b96c1c5359219fa68fe30b7e67d7877c5d2a8c6083b153da`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42271808b9146dc5744c45edba3f979ab16c9a382b62c44320fa4f04f9ab0f97`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dd08bcc8b2cc2e24a6318d63fcc471176adf3acdf78b10ac15b1fa5527c568`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.0-windowsservercore` - windows version 10.0.14393.4467; amd64

```console
$ docker pull nats@sha256:845b27a65fd56c97937856e216d7771d144a8b90c4cce3b45562de4761576f93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6270853814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87d244a19fd78d48d37bc35a9b3997f8dafc00fcce0da603d7a5aa6aa095429`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 13:26:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 15:55:27 GMT
ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:58 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:17:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.0/nats-server-v2.3.0-windows-amd64.zip
# Thu, 24 Jun 2021 18:17:03 GMT
ENV NATS_SERVER_SHASUM=4cf3cad0f3fc635a7be429ab13d852b1eea41c8f81b5d9ef7f21d93dd99a1f6f
# Thu, 24 Jun 2021 18:18:18 GMT
RUN Set-PSDebug -Trace 2
# Thu, 24 Jun 2021 18:20:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 24 Jun 2021 18:20:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:20:17 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:20:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2f52abeee6d6f4a925ad418b5e6200d4fca9bf92834ffc918b8bbaccd34251db`  
		Size: 2.2 GB (2195741359 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fa4e6085e5538e957ef06561fe1e62dff898da7f4bb577e81da74323aecab2d7`  
		Last Modified: Wed, 09 Jun 2021 15:28:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db57f94547be7109ad927e2f9d04a0501a2a5f0cb91ad8c4385eb32758f86b9`  
		Last Modified: Wed, 09 Jun 2021 16:00:21 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385a2e510feddc0676b3c17e1654e2430eb4ac4a8a775b78e89afaccc5fdc804`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c18a811e26704bd4bb49d57454d177eb277d065d5841d36f6fe5dce50a4fda`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154f452c578ee0bf6e0aa67510a192c41adaf4a94d974a0909c227cc29bf6b18`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45d0a6fab2e6e94ed71f11798975da67d62cc86ebc458ce3e3a12bbe7f250d8`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 352.1 KB (352114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d373c50c3af9ea67008c088d5b13b3963be0c55dea90c371d8a1be5ba44d2a84`  
		Last Modified: Thu, 24 Jun 2021 18:21:51 GMT  
		Size: 4.8 MB (4761699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1065e6f071db7571880f6c942f08e2565dde2da5ee37a3d79bdeca96583d8`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f1549b605bdde25fa57f56f24f602d8605121787ac6d452d1eae704c173ba5`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6659b0e6d881d37794c4ac62633dad4743618a980578bdbe8e7a4e5d617211`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c424710ae455acf452bd0eba0e1e696916ed091e236132a564e02b266431cc3`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.0-windowsservercore-1809`

```console
$ docker pull nats@sha256:a673dfea57d51e9d21677796f5f72f60d13dab15b74dd8b2dfe32518cd6ca782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `nats:2.3.0-windowsservercore-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:2b5fc0956f7fa5e8a5d73443e2b2cff10b2c5a1d750238f0c39d388ad230e889
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2646697143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3296c025e7c6bdec1087e1cd78a2af9c8398fde53f8acc26c4c2c62dade1e2fc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 13:15:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 15:52:54 GMT
ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:14:27 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:14:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.0/nats-server-v2.3.0-windows-amd64.zip
# Thu, 24 Jun 2021 18:14:33 GMT
ENV NATS_SERVER_SHASUM=4cf3cad0f3fc635a7be429ab13d852b1eea41c8f81b5d9ef7f21d93dd99a1f6f
# Thu, 24 Jun 2021 18:15:14 GMT
RUN Set-PSDebug -Trace 2
# Thu, 24 Jun 2021 18:16:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 24 Jun 2021 18:16:20 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:22 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae7d2dc4b590128efeafd375d02122e65a2525623ac2be100c1a390caf8a4b49`  
		Last Modified: Wed, 09 Jun 2021 15:28:02 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507a90d55d261855b42c7b5905599cdc274ca135ad962fffffe1fa6246c9bba7`  
		Last Modified: Wed, 09 Jun 2021 15:59:38 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29775406c1781fcc27d8bf50b4b0bfcd9418dda6cfae494e4d9383e0213df24b`  
		Last Modified: Thu, 24 Jun 2021 18:21:11 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3bf008ba6d0a427891ae36a26107b3e1f386cb9be8dbd0427623920c08cb93`  
		Last Modified: Thu, 24 Jun 2021 18:21:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35cb02232de3ac8c2255dee0bc6a718b0b3cb29b7baa3caf9825fae6519353c`  
		Last Modified: Thu, 24 Jun 2021 18:21:12 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8811ca1ef9b5e7b658fe9eb6dcf4145a8c7fc2108cddf27604a32625196d9435`  
		Last Modified: Thu, 24 Jun 2021 18:21:12 GMT  
		Size: 363.9 KB (363906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07799fa10e1ce0eeb453bb8919dd2756d7f46df37096e364eaef1cf48ee4d27b`  
		Last Modified: Thu, 24 Jun 2021 18:21:11 GMT  
		Size: 4.7 MB (4734976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7d8a61897a84ba84d3157167674e44f39375855accec3dbfd1bfcc8fb1911d`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.9 KB (1921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5675249b0aafebc9b96c1c5359219fa68fe30b7e67d7877c5d2a8c6083b153da`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42271808b9146dc5744c45edba3f979ab16c9a382b62c44320fa4f04f9ab0f97`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dd08bcc8b2cc2e24a6318d63fcc471176adf3acdf78b10ac15b1fa5527c568`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.0-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:0e0a6967d374622f82cf5383e0c8751541a791a255a4c728eaa86e51af9560c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4467; amd64

### `nats:2.3.0-windowsservercore-ltsc2016` - windows version 10.0.14393.4467; amd64

```console
$ docker pull nats@sha256:845b27a65fd56c97937856e216d7771d144a8b90c4cce3b45562de4761576f93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6270853814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87d244a19fd78d48d37bc35a9b3997f8dafc00fcce0da603d7a5aa6aa095429`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 13:26:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 15:55:27 GMT
ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:58 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:17:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.0/nats-server-v2.3.0-windows-amd64.zip
# Thu, 24 Jun 2021 18:17:03 GMT
ENV NATS_SERVER_SHASUM=4cf3cad0f3fc635a7be429ab13d852b1eea41c8f81b5d9ef7f21d93dd99a1f6f
# Thu, 24 Jun 2021 18:18:18 GMT
RUN Set-PSDebug -Trace 2
# Thu, 24 Jun 2021 18:20:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 24 Jun 2021 18:20:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:20:17 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:20:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2f52abeee6d6f4a925ad418b5e6200d4fca9bf92834ffc918b8bbaccd34251db`  
		Size: 2.2 GB (2195741359 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fa4e6085e5538e957ef06561fe1e62dff898da7f4bb577e81da74323aecab2d7`  
		Last Modified: Wed, 09 Jun 2021 15:28:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db57f94547be7109ad927e2f9d04a0501a2a5f0cb91ad8c4385eb32758f86b9`  
		Last Modified: Wed, 09 Jun 2021 16:00:21 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385a2e510feddc0676b3c17e1654e2430eb4ac4a8a775b78e89afaccc5fdc804`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c18a811e26704bd4bb49d57454d177eb277d065d5841d36f6fe5dce50a4fda`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154f452c578ee0bf6e0aa67510a192c41adaf4a94d974a0909c227cc29bf6b18`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45d0a6fab2e6e94ed71f11798975da67d62cc86ebc458ce3e3a12bbe7f250d8`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 352.1 KB (352114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d373c50c3af9ea67008c088d5b13b3963be0c55dea90c371d8a1be5ba44d2a84`  
		Last Modified: Thu, 24 Jun 2021 18:21:51 GMT  
		Size: 4.8 MB (4761699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1065e6f071db7571880f6c942f08e2565dde2da5ee37a3d79bdeca96583d8`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f1549b605bdde25fa57f56f24f602d8605121787ac6d452d1eae704c173ba5`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6659b0e6d881d37794c4ac62633dad4743618a980578bdbe8e7a4e5d617211`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c424710ae455acf452bd0eba0e1e696916ed091e236132a564e02b266431cc3`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:ff5570b8f85ec8849d5b58316e2984352cc44e7f65a3cfeabb0cbbe9933db4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:11ac3d707fd53db8987f4e5432397c58bcd7fcd98e9c056088f709a58b4fc3a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2523bcf697d78fbb44315448e0c04248daa07f5741fc4c1d82224203a3a1a982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 18:20:14 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 18:20:17 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 18:20:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 18:20:17 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 18:20:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7669d67fb4cfb54da583e883237da0b279b1fb366b087a0a503ca26d962042`  
		Last Modified: Thu, 24 Jun 2021 18:21:21 GMT  
		Size: 4.6 MB (4615300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a63d38912003c0b7e278dc2e07a5e3595d926f114688e1eba7453d10771507`  
		Last Modified: Thu, 24 Jun 2021 18:21:20 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50aa5d23eab2b64578272b85b1840118f8ce74d4c8a076fd9fdbbf112b389a15`  
		Last Modified: Thu, 24 Jun 2021 18:21:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:afafd733f206092cfbf83b03d0d219e3ad9fc986d7b9bd1bcc813ba9a164e831
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6897059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a08095811cc4b9caf05423603dec24983d69af81a39a2b582c3fed0698cbcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 19:17:03 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 19:17:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 19:17:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 19:17:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 19:17:09 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 19:17:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072466ad1c8b3759328223593e85cddeedd93281cc285d4fbcc43c2aa77cff8b`  
		Last Modified: Thu, 24 Jun 2021 19:19:11 GMT  
		Size: 4.3 MB (4273957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040948b8c4aa41212a8812f47174f14427d9e2e336d534553442231f4f521882`  
		Last Modified: Thu, 24 Jun 2021 19:19:08 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7ac2240a33c4d9b574bff55265289f9093dcbe62577c93ce04d3b9b145e45e`  
		Last Modified: Thu, 24 Jun 2021 19:19:08 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:7f77835f7df0ca3c3fbc680a5df2e3a52df9b2bad2ad85a61c9c93588d554e1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6694378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31819633e547bc5673c5be989286c3fa84b4fa83c1cc7e1daac4586d53072bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 23:15:15 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Tue, 15 Jun 2021 23:15:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Jun 2021 04:21:38 GMT
ENV NATS_SERVER=2.3.0
# Fri, 25 Jun 2021 04:21:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 25 Jun 2021 04:21:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 25 Jun 2021 04:21:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Jun 2021 04:21:44 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:21:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Jun 2021 04:21:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b4716e8d6c6e6f099e638134cd5d5cb8d04256d758ebdfe9d484831feb75f6`  
		Last Modified: Fri, 25 Jun 2021 04:23:48 GMT  
		Size: 4.3 MB (4269265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b992d0d507b7fcd3c04c8337fde6b65f98ef5711af47b760054e79a2568c0990`  
		Last Modified: Fri, 25 Jun 2021 04:23:45 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ae15dff3a871a17e97c8114db82e6e7af74fdbb011e105314060415dcc93a3`  
		Last Modified: Fri, 25 Jun 2021 04:23:45 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e7be6da297d4e47e1cbf0cebebb0b28db6ceeb50f8e06e87609dce41de682f92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6953599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0539985a8e92b6e078f0f65ffce3ff416cfa3401034c750ec07b9da7150efce8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 19:06:45 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 19:06:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 19:06:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 19:06:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 19:06:48 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:06:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 19:06:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27d0993acd4f2a9aa99219b53b130917cfcaa7b5ab8f75f92c6853892b1fbd8`  
		Last Modified: Thu, 24 Jun 2021 19:08:02 GMT  
		Size: 4.2 MB (4240601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89210891c944f9ecbd826fe696a7f0a1399ac8628705331d9eb011d633fe7b2`  
		Last Modified: Thu, 24 Jun 2021 19:08:01 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e288f0bb2545133bb23a02793719cdc1076dc77f7c61c80c05c6351f9dc2c482`  
		Last Modified: Thu, 24 Jun 2021 19:08:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.13`

```console
$ docker pull nats@sha256:ff5570b8f85ec8849d5b58316e2984352cc44e7f65a3cfeabb0cbbe9933db4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.13` - linux; amd64

```console
$ docker pull nats@sha256:11ac3d707fd53db8987f4e5432397c58bcd7fcd98e9c056088f709a58b4fc3a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2523bcf697d78fbb44315448e0c04248daa07f5741fc4c1d82224203a3a1a982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 18:20:14 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 18:20:17 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 18:20:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 18:20:17 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 18:20:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7669d67fb4cfb54da583e883237da0b279b1fb366b087a0a503ca26d962042`  
		Last Modified: Thu, 24 Jun 2021 18:21:21 GMT  
		Size: 4.6 MB (4615300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a63d38912003c0b7e278dc2e07a5e3595d926f114688e1eba7453d10771507`  
		Last Modified: Thu, 24 Jun 2021 18:21:20 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50aa5d23eab2b64578272b85b1840118f8ce74d4c8a076fd9fdbbf112b389a15`  
		Last Modified: Thu, 24 Jun 2021 18:21:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.13` - linux; arm variant v6

```console
$ docker pull nats@sha256:afafd733f206092cfbf83b03d0d219e3ad9fc986d7b9bd1bcc813ba9a164e831
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6897059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a08095811cc4b9caf05423603dec24983d69af81a39a2b582c3fed0698cbcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 19:17:03 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 19:17:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 19:17:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 19:17:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 19:17:09 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 19:17:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072466ad1c8b3759328223593e85cddeedd93281cc285d4fbcc43c2aa77cff8b`  
		Last Modified: Thu, 24 Jun 2021 19:19:11 GMT  
		Size: 4.3 MB (4273957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040948b8c4aa41212a8812f47174f14427d9e2e336d534553442231f4f521882`  
		Last Modified: Thu, 24 Jun 2021 19:19:08 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7ac2240a33c4d9b574bff55265289f9093dcbe62577c93ce04d3b9b145e45e`  
		Last Modified: Thu, 24 Jun 2021 19:19:08 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.13` - linux; arm variant v7

```console
$ docker pull nats@sha256:7f77835f7df0ca3c3fbc680a5df2e3a52df9b2bad2ad85a61c9c93588d554e1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6694378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31819633e547bc5673c5be989286c3fa84b4fa83c1cc7e1daac4586d53072bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 23:15:15 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Tue, 15 Jun 2021 23:15:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Jun 2021 04:21:38 GMT
ENV NATS_SERVER=2.3.0
# Fri, 25 Jun 2021 04:21:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 25 Jun 2021 04:21:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 25 Jun 2021 04:21:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Jun 2021 04:21:44 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:21:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Jun 2021 04:21:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b4716e8d6c6e6f099e638134cd5d5cb8d04256d758ebdfe9d484831feb75f6`  
		Last Modified: Fri, 25 Jun 2021 04:23:48 GMT  
		Size: 4.3 MB (4269265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b992d0d507b7fcd3c04c8337fde6b65f98ef5711af47b760054e79a2568c0990`  
		Last Modified: Fri, 25 Jun 2021 04:23:45 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ae15dff3a871a17e97c8114db82e6e7af74fdbb011e105314060415dcc93a3`  
		Last Modified: Fri, 25 Jun 2021 04:23:45 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e7be6da297d4e47e1cbf0cebebb0b28db6ceeb50f8e06e87609dce41de682f92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6953599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0539985a8e92b6e078f0f65ffce3ff416cfa3401034c750ec07b9da7150efce8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 19:06:45 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 19:06:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 19:06:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 19:06:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 19:06:48 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:06:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 19:06:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27d0993acd4f2a9aa99219b53b130917cfcaa7b5ab8f75f92c6853892b1fbd8`  
		Last Modified: Thu, 24 Jun 2021 19:08:02 GMT  
		Size: 4.2 MB (4240601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89210891c944f9ecbd826fe696a7f0a1399ac8628705331d9eb011d633fe7b2`  
		Last Modified: Thu, 24 Jun 2021 19:08:01 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e288f0bb2545133bb23a02793719cdc1076dc77f7c61c80c05c6351f9dc2c482`  
		Last Modified: Thu, 24 Jun 2021 19:08:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:6aa7af6180050c241f606d59de7b4be510dbaddac5ae8855e5d84e4aae54ca42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1999; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:9ee8674607d72a7993a833da50a04bb798dc906079f7d4a3ff386ae9c7dad1b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24690f4c9243082798de0d5d0dcf537f0d65e65ba0e4c324f576019af6e88b71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:574cacffaccc18c0ebb219863832f97c5b4a301f1311490b79ebc4f7c91df1c5 in /nats-server 
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 18:20:54 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:55 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 18:20:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff7c72aa6eac78de3e8d419804aa418bec0a1d109825baafe6f27f8d5463c862`  
		Last Modified: Thu, 24 Jun 2021 18:21:47 GMT  
		Size: 4.3 MB (4335042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2e05cfe23a1b83926a7784d3a6f32ee581b1b20019023a53e605a28e098280`  
		Last Modified: Thu, 24 Jun 2021 18:21:45 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4d7fa672d2e979a1f71013d6c0ced4762a775e52c5fa1c597061e0661a4f564
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d818a3d14ec5abc722d14eefa80fd1bbb0cf49078b6a2fb3e54632e211c176c9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:f297049dd293f8bd69f8b37a6337b711a278a532e801780056f74049b995408b in /nats-server 
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:17:28 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:17:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f861ae2df753d566752887dd69fa7c0770cc5d866cf63d89323d119e6e132631`  
		Last Modified: Thu, 24 Jun 2021 19:20:11 GMT  
		Size: 4.0 MB (3992918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442ea4dc62b81dd101ec8289e6ef95821857d589dd412611e32dd41affe68138`  
		Last Modified: Thu, 24 Jun 2021 19:20:08 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:6796429bd41a95837772476ae383c344688bbfa91067d66187cff0919bb9bff5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f262b07aad3ac9672f6fdfdafb0486d87b7afa1949afa2bab951305a9191f6e4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Jun 2021 04:22:05 GMT
COPY file:e739b42ab72b567be37f2b08b7cc64858dc247505c5f9065cbc349f3f7cde026 in /nats-server 
# Fri, 25 Jun 2021 04:22:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 25 Jun 2021 04:22:06 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:22:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Jun 2021 04:22:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4eead17c506be0458b8b300048220b15977a1fb9f1dabb07031134fe7cd321bd`  
		Last Modified: Fri, 25 Jun 2021 04:24:25 GMT  
		Size: 4.0 MB (3987827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71186d5a22ac8937ee584ce8ff166469d1d6e857b4bca58533fb852beaf49aff`  
		Last Modified: Fri, 25 Jun 2021 04:24:23 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9af64abe7058267802b82eea320c8900f01e2900fc14c7819215cc38249b6a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b6ba9c13a2b4e06ce837ee797073c343df1705b660c37b3331e4afc500b19e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:5beb421ec5105e31f6e0b0a14e99795c4d0ca457385b898e67e502f8c1168b1c in /nats-server 
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:07:11 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:07:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:07:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4fa9662b0eb20e8acff5f956ac375b9e6d6bae55ed10b15783f5bdea6e212ca2`  
		Last Modified: Thu, 24 Jun 2021 19:08:34 GMT  
		Size: 4.0 MB (3958114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae902de5ccdf10f5ab555454aaf3ce99d7642bbc3961ef684412f5d45cd03ab`  
		Last Modified: Thu, 24 Jun 2021 19:08:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:c3d85580c0f97e9e7525ac25ff6dd2b46e30d0a28d8eae5922200f692c5f5420
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107067292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60db2a891b8d4acaed25bf0dfdd41e93f36804395b740b4fdc1e2bb452c6c1b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 15:55:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:39 GMT
RUN cmd /S /C #(nop) COPY file:bac1db2af96d2ddad22da9ae2b1252ad143dce10623146a5898a15a4e3f18d81 in C:\nats-server.exe 
# Thu, 24 Jun 2021 18:16:42 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:80d93ce19113bbf944b699f12e59395e0eabeb00ccd1fd5dc7df46bb115eba2f`  
		Last Modified: Wed, 09 Jun 2021 15:59:58 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec670391ee18da96972d36cee7981927664f13e0189b3d1f31b2c62e5ca0d4b`  
		Last Modified: Thu, 24 Jun 2021 18:21:31 GMT  
		Size: 4.4 MB (4389381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ee48b932f6c168a30dd680d51235836a69ad93983a5aa6ae510649498009d`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47216eb523d03d9b262b596ac92cdee9995cea672a4b3914a9f02a41a5ff422`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26d8e3fee7dfa3f7bf9b8af44b5f640be79d646bbcb96459100b6b39fe7bda`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348ad20da8616571c92e671840d54b660df38b670f5bf015aeaa2f6bed084657`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:80eb5023b4f9a6a43ccb90613913d8bbd7fb1d60ed202af2e7e7425add895c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:9ee8674607d72a7993a833da50a04bb798dc906079f7d4a3ff386ae9c7dad1b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24690f4c9243082798de0d5d0dcf537f0d65e65ba0e4c324f576019af6e88b71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:574cacffaccc18c0ebb219863832f97c5b4a301f1311490b79ebc4f7c91df1c5 in /nats-server 
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 18:20:54 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:55 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 18:20:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff7c72aa6eac78de3e8d419804aa418bec0a1d109825baafe6f27f8d5463c862`  
		Last Modified: Thu, 24 Jun 2021 18:21:47 GMT  
		Size: 4.3 MB (4335042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2e05cfe23a1b83926a7784d3a6f32ee581b1b20019023a53e605a28e098280`  
		Last Modified: Thu, 24 Jun 2021 18:21:45 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4d7fa672d2e979a1f71013d6c0ced4762a775e52c5fa1c597061e0661a4f564
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d818a3d14ec5abc722d14eefa80fd1bbb0cf49078b6a2fb3e54632e211c176c9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:f297049dd293f8bd69f8b37a6337b711a278a532e801780056f74049b995408b in /nats-server 
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:17:28 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:17:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f861ae2df753d566752887dd69fa7c0770cc5d866cf63d89323d119e6e132631`  
		Last Modified: Thu, 24 Jun 2021 19:20:11 GMT  
		Size: 4.0 MB (3992918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442ea4dc62b81dd101ec8289e6ef95821857d589dd412611e32dd41affe68138`  
		Last Modified: Thu, 24 Jun 2021 19:20:08 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:6796429bd41a95837772476ae383c344688bbfa91067d66187cff0919bb9bff5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f262b07aad3ac9672f6fdfdafb0486d87b7afa1949afa2bab951305a9191f6e4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Jun 2021 04:22:05 GMT
COPY file:e739b42ab72b567be37f2b08b7cc64858dc247505c5f9065cbc349f3f7cde026 in /nats-server 
# Fri, 25 Jun 2021 04:22:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 25 Jun 2021 04:22:06 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:22:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Jun 2021 04:22:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4eead17c506be0458b8b300048220b15977a1fb9f1dabb07031134fe7cd321bd`  
		Last Modified: Fri, 25 Jun 2021 04:24:25 GMT  
		Size: 4.0 MB (3987827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71186d5a22ac8937ee584ce8ff166469d1d6e857b4bca58533fb852beaf49aff`  
		Last Modified: Fri, 25 Jun 2021 04:24:23 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9af64abe7058267802b82eea320c8900f01e2900fc14c7819215cc38249b6a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b6ba9c13a2b4e06ce837ee797073c343df1705b660c37b3331e4afc500b19e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:5beb421ec5105e31f6e0b0a14e99795c4d0ca457385b898e67e502f8c1168b1c in /nats-server 
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:07:11 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:07:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:07:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4fa9662b0eb20e8acff5f956ac375b9e6d6bae55ed10b15783f5bdea6e212ca2`  
		Last Modified: Thu, 24 Jun 2021 19:08:34 GMT  
		Size: 4.0 MB (3958114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae902de5ccdf10f5ab555454aaf3ce99d7642bbc3961ef684412f5d45cd03ab`  
		Last Modified: Thu, 24 Jun 2021 19:08:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:4ebe0f8afa0791f4642839c39904f87117ae2b491ef7cc3af12fe3ea313999b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `nats:nanoserver` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:c3d85580c0f97e9e7525ac25ff6dd2b46e30d0a28d8eae5922200f692c5f5420
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107067292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60db2a891b8d4acaed25bf0dfdd41e93f36804395b740b4fdc1e2bb452c6c1b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 15:55:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:39 GMT
RUN cmd /S /C #(nop) COPY file:bac1db2af96d2ddad22da9ae2b1252ad143dce10623146a5898a15a4e3f18d81 in C:\nats-server.exe 
# Thu, 24 Jun 2021 18:16:42 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:80d93ce19113bbf944b699f12e59395e0eabeb00ccd1fd5dc7df46bb115eba2f`  
		Last Modified: Wed, 09 Jun 2021 15:59:58 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec670391ee18da96972d36cee7981927664f13e0189b3d1f31b2c62e5ca0d4b`  
		Last Modified: Thu, 24 Jun 2021 18:21:31 GMT  
		Size: 4.4 MB (4389381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ee48b932f6c168a30dd680d51235836a69ad93983a5aa6ae510649498009d`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47216eb523d03d9b262b596ac92cdee9995cea672a4b3914a9f02a41a5ff422`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26d8e3fee7dfa3f7bf9b8af44b5f640be79d646bbcb96459100b6b39fe7bda`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348ad20da8616571c92e671840d54b660df38b670f5bf015aeaa2f6bed084657`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:4ebe0f8afa0791f4642839c39904f87117ae2b491ef7cc3af12fe3ea313999b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:c3d85580c0f97e9e7525ac25ff6dd2b46e30d0a28d8eae5922200f692c5f5420
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107067292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60db2a891b8d4acaed25bf0dfdd41e93f36804395b740b4fdc1e2bb452c6c1b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 15:55:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:39 GMT
RUN cmd /S /C #(nop) COPY file:bac1db2af96d2ddad22da9ae2b1252ad143dce10623146a5898a15a4e3f18d81 in C:\nats-server.exe 
# Thu, 24 Jun 2021 18:16:42 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:80d93ce19113bbf944b699f12e59395e0eabeb00ccd1fd5dc7df46bb115eba2f`  
		Last Modified: Wed, 09 Jun 2021 15:59:58 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec670391ee18da96972d36cee7981927664f13e0189b3d1f31b2c62e5ca0d4b`  
		Last Modified: Thu, 24 Jun 2021 18:21:31 GMT  
		Size: 4.4 MB (4389381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ee48b932f6c168a30dd680d51235836a69ad93983a5aa6ae510649498009d`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47216eb523d03d9b262b596ac92cdee9995cea672a4b3914a9f02a41a5ff422`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26d8e3fee7dfa3f7bf9b8af44b5f640be79d646bbcb96459100b6b39fe7bda`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348ad20da8616571c92e671840d54b660df38b670f5bf015aeaa2f6bed084657`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:80eb5023b4f9a6a43ccb90613913d8bbd7fb1d60ed202af2e7e7425add895c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:9ee8674607d72a7993a833da50a04bb798dc906079f7d4a3ff386ae9c7dad1b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24690f4c9243082798de0d5d0dcf537f0d65e65ba0e4c324f576019af6e88b71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:574cacffaccc18c0ebb219863832f97c5b4a301f1311490b79ebc4f7c91df1c5 in /nats-server 
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 18:20:54 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:55 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 18:20:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff7c72aa6eac78de3e8d419804aa418bec0a1d109825baafe6f27f8d5463c862`  
		Last Modified: Thu, 24 Jun 2021 18:21:47 GMT  
		Size: 4.3 MB (4335042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2e05cfe23a1b83926a7784d3a6f32ee581b1b20019023a53e605a28e098280`  
		Last Modified: Thu, 24 Jun 2021 18:21:45 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4d7fa672d2e979a1f71013d6c0ced4762a775e52c5fa1c597061e0661a4f564
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d818a3d14ec5abc722d14eefa80fd1bbb0cf49078b6a2fb3e54632e211c176c9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:f297049dd293f8bd69f8b37a6337b711a278a532e801780056f74049b995408b in /nats-server 
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:17:28 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:17:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f861ae2df753d566752887dd69fa7c0770cc5d866cf63d89323d119e6e132631`  
		Last Modified: Thu, 24 Jun 2021 19:20:11 GMT  
		Size: 4.0 MB (3992918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442ea4dc62b81dd101ec8289e6ef95821857d589dd412611e32dd41affe68138`  
		Last Modified: Thu, 24 Jun 2021 19:20:08 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:6796429bd41a95837772476ae383c344688bbfa91067d66187cff0919bb9bff5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f262b07aad3ac9672f6fdfdafb0486d87b7afa1949afa2bab951305a9191f6e4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Jun 2021 04:22:05 GMT
COPY file:e739b42ab72b567be37f2b08b7cc64858dc247505c5f9065cbc349f3f7cde026 in /nats-server 
# Fri, 25 Jun 2021 04:22:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 25 Jun 2021 04:22:06 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:22:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Jun 2021 04:22:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4eead17c506be0458b8b300048220b15977a1fb9f1dabb07031134fe7cd321bd`  
		Last Modified: Fri, 25 Jun 2021 04:24:25 GMT  
		Size: 4.0 MB (3987827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71186d5a22ac8937ee584ce8ff166469d1d6e857b4bca58533fb852beaf49aff`  
		Last Modified: Fri, 25 Jun 2021 04:24:23 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9af64abe7058267802b82eea320c8900f01e2900fc14c7819215cc38249b6a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b6ba9c13a2b4e06ce837ee797073c343df1705b660c37b3331e4afc500b19e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:5beb421ec5105e31f6e0b0a14e99795c4d0ca457385b898e67e502f8c1168b1c in /nats-server 
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:07:11 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:07:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:07:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4fa9662b0eb20e8acff5f956ac375b9e6d6bae55ed10b15783f5bdea6e212ca2`  
		Last Modified: Thu, 24 Jun 2021 19:08:34 GMT  
		Size: 4.0 MB (3958114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae902de5ccdf10f5ab555454aaf3ce99d7642bbc3961ef684412f5d45cd03ab`  
		Last Modified: Thu, 24 Jun 2021 19:08:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:0a82183999395fc7ff72a6528b06205f06ca31baa3e914a3c43496de2242b3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64
	-	windows version 10.0.14393.4467; amd64

### `nats:windowsservercore` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:2b5fc0956f7fa5e8a5d73443e2b2cff10b2c5a1d750238f0c39d388ad230e889
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2646697143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3296c025e7c6bdec1087e1cd78a2af9c8398fde53f8acc26c4c2c62dade1e2fc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 13:15:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 15:52:54 GMT
ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:14:27 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:14:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.0/nats-server-v2.3.0-windows-amd64.zip
# Thu, 24 Jun 2021 18:14:33 GMT
ENV NATS_SERVER_SHASUM=4cf3cad0f3fc635a7be429ab13d852b1eea41c8f81b5d9ef7f21d93dd99a1f6f
# Thu, 24 Jun 2021 18:15:14 GMT
RUN Set-PSDebug -Trace 2
# Thu, 24 Jun 2021 18:16:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 24 Jun 2021 18:16:20 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:22 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae7d2dc4b590128efeafd375d02122e65a2525623ac2be100c1a390caf8a4b49`  
		Last Modified: Wed, 09 Jun 2021 15:28:02 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507a90d55d261855b42c7b5905599cdc274ca135ad962fffffe1fa6246c9bba7`  
		Last Modified: Wed, 09 Jun 2021 15:59:38 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29775406c1781fcc27d8bf50b4b0bfcd9418dda6cfae494e4d9383e0213df24b`  
		Last Modified: Thu, 24 Jun 2021 18:21:11 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3bf008ba6d0a427891ae36a26107b3e1f386cb9be8dbd0427623920c08cb93`  
		Last Modified: Thu, 24 Jun 2021 18:21:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35cb02232de3ac8c2255dee0bc6a718b0b3cb29b7baa3caf9825fae6519353c`  
		Last Modified: Thu, 24 Jun 2021 18:21:12 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8811ca1ef9b5e7b658fe9eb6dcf4145a8c7fc2108cddf27604a32625196d9435`  
		Last Modified: Thu, 24 Jun 2021 18:21:12 GMT  
		Size: 363.9 KB (363906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07799fa10e1ce0eeb453bb8919dd2756d7f46df37096e364eaef1cf48ee4d27b`  
		Last Modified: Thu, 24 Jun 2021 18:21:11 GMT  
		Size: 4.7 MB (4734976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7d8a61897a84ba84d3157167674e44f39375855accec3dbfd1bfcc8fb1911d`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.9 KB (1921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5675249b0aafebc9b96c1c5359219fa68fe30b7e67d7877c5d2a8c6083b153da`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42271808b9146dc5744c45edba3f979ab16c9a382b62c44320fa4f04f9ab0f97`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dd08bcc8b2cc2e24a6318d63fcc471176adf3acdf78b10ac15b1fa5527c568`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.4467; amd64

```console
$ docker pull nats@sha256:845b27a65fd56c97937856e216d7771d144a8b90c4cce3b45562de4761576f93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6270853814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87d244a19fd78d48d37bc35a9b3997f8dafc00fcce0da603d7a5aa6aa095429`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 13:26:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 15:55:27 GMT
ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:58 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:17:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.0/nats-server-v2.3.0-windows-amd64.zip
# Thu, 24 Jun 2021 18:17:03 GMT
ENV NATS_SERVER_SHASUM=4cf3cad0f3fc635a7be429ab13d852b1eea41c8f81b5d9ef7f21d93dd99a1f6f
# Thu, 24 Jun 2021 18:18:18 GMT
RUN Set-PSDebug -Trace 2
# Thu, 24 Jun 2021 18:20:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 24 Jun 2021 18:20:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:20:17 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:20:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2f52abeee6d6f4a925ad418b5e6200d4fca9bf92834ffc918b8bbaccd34251db`  
		Size: 2.2 GB (2195741359 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fa4e6085e5538e957ef06561fe1e62dff898da7f4bb577e81da74323aecab2d7`  
		Last Modified: Wed, 09 Jun 2021 15:28:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db57f94547be7109ad927e2f9d04a0501a2a5f0cb91ad8c4385eb32758f86b9`  
		Last Modified: Wed, 09 Jun 2021 16:00:21 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385a2e510feddc0676b3c17e1654e2430eb4ac4a8a775b78e89afaccc5fdc804`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c18a811e26704bd4bb49d57454d177eb277d065d5841d36f6fe5dce50a4fda`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154f452c578ee0bf6e0aa67510a192c41adaf4a94d974a0909c227cc29bf6b18`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45d0a6fab2e6e94ed71f11798975da67d62cc86ebc458ce3e3a12bbe7f250d8`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 352.1 KB (352114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d373c50c3af9ea67008c088d5b13b3963be0c55dea90c371d8a1be5ba44d2a84`  
		Last Modified: Thu, 24 Jun 2021 18:21:51 GMT  
		Size: 4.8 MB (4761699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1065e6f071db7571880f6c942f08e2565dde2da5ee37a3d79bdeca96583d8`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f1549b605bdde25fa57f56f24f602d8605121787ac6d452d1eae704c173ba5`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6659b0e6d881d37794c4ac62633dad4743618a980578bdbe8e7a4e5d617211`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c424710ae455acf452bd0eba0e1e696916ed091e236132a564e02b266431cc3`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:a673dfea57d51e9d21677796f5f72f60d13dab15b74dd8b2dfe32518cd6ca782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:2b5fc0956f7fa5e8a5d73443e2b2cff10b2c5a1d750238f0c39d388ad230e889
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2646697143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3296c025e7c6bdec1087e1cd78a2af9c8398fde53f8acc26c4c2c62dade1e2fc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 13:15:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 15:52:54 GMT
ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:14:27 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:14:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.0/nats-server-v2.3.0-windows-amd64.zip
# Thu, 24 Jun 2021 18:14:33 GMT
ENV NATS_SERVER_SHASUM=4cf3cad0f3fc635a7be429ab13d852b1eea41c8f81b5d9ef7f21d93dd99a1f6f
# Thu, 24 Jun 2021 18:15:14 GMT
RUN Set-PSDebug -Trace 2
# Thu, 24 Jun 2021 18:16:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 24 Jun 2021 18:16:20 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:22 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae7d2dc4b590128efeafd375d02122e65a2525623ac2be100c1a390caf8a4b49`  
		Last Modified: Wed, 09 Jun 2021 15:28:02 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507a90d55d261855b42c7b5905599cdc274ca135ad962fffffe1fa6246c9bba7`  
		Last Modified: Wed, 09 Jun 2021 15:59:38 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29775406c1781fcc27d8bf50b4b0bfcd9418dda6cfae494e4d9383e0213df24b`  
		Last Modified: Thu, 24 Jun 2021 18:21:11 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3bf008ba6d0a427891ae36a26107b3e1f386cb9be8dbd0427623920c08cb93`  
		Last Modified: Thu, 24 Jun 2021 18:21:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35cb02232de3ac8c2255dee0bc6a718b0b3cb29b7baa3caf9825fae6519353c`  
		Last Modified: Thu, 24 Jun 2021 18:21:12 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8811ca1ef9b5e7b658fe9eb6dcf4145a8c7fc2108cddf27604a32625196d9435`  
		Last Modified: Thu, 24 Jun 2021 18:21:12 GMT  
		Size: 363.9 KB (363906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07799fa10e1ce0eeb453bb8919dd2756d7f46df37096e364eaef1cf48ee4d27b`  
		Last Modified: Thu, 24 Jun 2021 18:21:11 GMT  
		Size: 4.7 MB (4734976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7d8a61897a84ba84d3157167674e44f39375855accec3dbfd1bfcc8fb1911d`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.9 KB (1921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5675249b0aafebc9b96c1c5359219fa68fe30b7e67d7877c5d2a8c6083b153da`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42271808b9146dc5744c45edba3f979ab16c9a382b62c44320fa4f04f9ab0f97`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dd08bcc8b2cc2e24a6318d63fcc471176adf3acdf78b10ac15b1fa5527c568`  
		Last Modified: Thu, 24 Jun 2021 18:21:09 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:0e0a6967d374622f82cf5383e0c8751541a791a255a4c728eaa86e51af9560c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4467; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.4467; amd64

```console
$ docker pull nats@sha256:845b27a65fd56c97937856e216d7771d144a8b90c4cce3b45562de4761576f93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6270853814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87d244a19fd78d48d37bc35a9b3997f8dafc00fcce0da603d7a5aa6aa095429`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 13:26:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 15:55:27 GMT
ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:58 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:17:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.0/nats-server-v2.3.0-windows-amd64.zip
# Thu, 24 Jun 2021 18:17:03 GMT
ENV NATS_SERVER_SHASUM=4cf3cad0f3fc635a7be429ab13d852b1eea41c8f81b5d9ef7f21d93dd99a1f6f
# Thu, 24 Jun 2021 18:18:18 GMT
RUN Set-PSDebug -Trace 2
# Thu, 24 Jun 2021 18:20:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 24 Jun 2021 18:20:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:20:17 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:20:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2f52abeee6d6f4a925ad418b5e6200d4fca9bf92834ffc918b8bbaccd34251db`  
		Size: 2.2 GB (2195741359 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fa4e6085e5538e957ef06561fe1e62dff898da7f4bb577e81da74323aecab2d7`  
		Last Modified: Wed, 09 Jun 2021 15:28:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db57f94547be7109ad927e2f9d04a0501a2a5f0cb91ad8c4385eb32758f86b9`  
		Last Modified: Wed, 09 Jun 2021 16:00:21 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385a2e510feddc0676b3c17e1654e2430eb4ac4a8a775b78e89afaccc5fdc804`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c18a811e26704bd4bb49d57454d177eb277d065d5841d36f6fe5dce50a4fda`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154f452c578ee0bf6e0aa67510a192c41adaf4a94d974a0909c227cc29bf6b18`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45d0a6fab2e6e94ed71f11798975da67d62cc86ebc458ce3e3a12bbe7f250d8`  
		Last Modified: Thu, 24 Jun 2021 18:21:49 GMT  
		Size: 352.1 KB (352114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d373c50c3af9ea67008c088d5b13b3963be0c55dea90c371d8a1be5ba44d2a84`  
		Last Modified: Thu, 24 Jun 2021 18:21:51 GMT  
		Size: 4.8 MB (4761699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1065e6f071db7571880f6c942f08e2565dde2da5ee37a3d79bdeca96583d8`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f1549b605bdde25fa57f56f24f602d8605121787ac6d452d1eae704c173ba5`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6659b0e6d881d37794c4ac62633dad4743618a980578bdbe8e7a4e5d617211`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c424710ae455acf452bd0eba0e1e696916ed091e236132a564e02b266431cc3`  
		Last Modified: Thu, 24 Jun 2021 18:21:46 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.14`](#nats2-alpine314)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2-windowsservercore-ltsc2016`](#nats2-windowsservercore-ltsc2016)
-	[`nats:2.6`](#nats26)
-	[`nats:2.6-alpine`](#nats26-alpine)
-	[`nats:2.6-alpine3.14`](#nats26-alpine314)
-	[`nats:2.6-linux`](#nats26-linux)
-	[`nats:2.6-nanoserver`](#nats26-nanoserver)
-	[`nats:2.6-nanoserver-1809`](#nats26-nanoserver-1809)
-	[`nats:2.6-scratch`](#nats26-scratch)
-	[`nats:2.6-windowsservercore`](#nats26-windowsservercore)
-	[`nats:2.6-windowsservercore-1809`](#nats26-windowsservercore-1809)
-	[`nats:2.6-windowsservercore-ltsc2016`](#nats26-windowsservercore-ltsc2016)
-	[`nats:2.6.4`](#nats264)
-	[`nats:2.6.4-alpine`](#nats264-alpine)
-	[`nats:2.6.4-alpine3.14`](#nats264-alpine314)
-	[`nats:2.6.4-linux`](#nats264-linux)
-	[`nats:2.6.4-nanoserver`](#nats264-nanoserver)
-	[`nats:2.6.4-nanoserver-1809`](#nats264-nanoserver-1809)
-	[`nats:2.6.4-scratch`](#nats264-scratch)
-	[`nats:2.6.4-windowsservercore`](#nats264-windowsservercore)
-	[`nats:2.6.4-windowsservercore-1809`](#nats264-windowsservercore-1809)
-	[`nats:2.6.4-windowsservercore-ltsc2016`](#nats264-windowsservercore-ltsc2016)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.14`](#natsalpine314)
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
$ docker pull nats@sha256:2511f2a913b84b7a39dd6411d1dbb19ceae4006a5b8a8de7caadff42898e5d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2300; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:ce50109292cf290d1f6559a806f7e6f1b202f4d97678700dbb386b1d6c021964
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa4b152b84f6a4cc5da9b870074d5807b7dc42dbf1f922c1ff7e3059d6ec1be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:f554ccd652a698194b4adc9f60df406473cf580a258d4b425944a529b6b7b718 in /nats-server 
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:00 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe57332791af252fb9335dd0de8a36fe319e51fdde00636db3fee85f1adcb22f`  
		Last Modified: Fri, 05 Nov 2021 01:41:48 GMT  
		Size: 4.6 MB (4573985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc9e783378fba5ac033e418e7db34fb0215aeaa59658adf4924ad46455f261e`  
		Last Modified: Fri, 05 Nov 2021 01:41:47 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:a94f85ec4b90db46b3c8d59ed4c35fa9033482dd0e50679775145fc0f2528b20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4236770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bee36fb33e6c4d4ec54bcbd1778a2d3a19dcd7706111ffaf4d1711e916f6dea`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:0e12b4e14d681c94ae627c578bd9cc8a3fc9bec59e0062a772ad0933b7947e38 in /nats-server 
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:03 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a273e90687e1ad496ce74eecec787df7511839c5e770850a184f261ed706fc98`  
		Last Modified: Fri, 05 Nov 2021 01:43:23 GMT  
		Size: 4.2 MB (4236294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6825ddc1425c3e1cfde24c7f0c22b2ad39646ecc4d15d72b1d4769687206880`  
		Last Modified: Fri, 05 Nov 2021 01:43:21 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:f2419d713943dd432426211cc6035a9e4cbb06b0cb63d5bca91017fabec840e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf917eacaf24a0ae8a3e5b85a3f2795362e8333bf2b527cb7a5470e0d6cd02b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 04:34:29 GMT
COPY file:f8c8928a8edabd057aa0fe0c8e12f7e68c80845a6af865b9263be1face1e988c in /nats-server 
# Fri, 05 Nov 2021 04:34:30 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 04:34:30 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 04:34:31 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 04:34:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:791f22945fc593348a417c1bdef534cefaa5f1d33df489dddc334de30b713a78`  
		Last Modified: Fri, 05 Nov 2021 04:36:53 GMT  
		Size: 4.2 MB (4232017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3b77fec3826280fc07c1e66876ec0d673939258c3a1dd1320cbc1c3d56b86`  
		Last Modified: Fri, 05 Nov 2021 04:36:50 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d7e28f91b2fc35b9a0ed2eb9a5e16070e4c2d1dff3f18076e465958b997cce01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089ea638210c9c36041b15aac4bf873a36e3b4bdca7b8e25d6c1b4cc9a274094`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:25:26 GMT
COPY file:2327a2e0254f808bd88c7e734365e343ac6cf801c454a43bf9035cd435fbf8d0 in /nats-server 
# Fri, 05 Nov 2021 01:25:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:25:27 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:25:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:25:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fd5084aec62b3e936e8b267729c530280fe1646e8e9d0e09ef842b74beccff33`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 4.2 MB (4182491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963e399425efdeb20d2700e846b7b3f5c36a5ecef7204cb3fe1476b7b835b2e6`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:85fc53257b869566352af427b00b1e4eb3be4d9c158473d05955a95358569c49
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107420117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efad7f25530c39976e06f9cd49e8bf8ccf60e961cf32e240771c3311fa8ecb24`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:08 GMT
RUN cmd /S /C #(nop) COPY file:d04f5d85a8b0edde975ace8d01e615862e9872904d6e700eb5be4601ac26087b in C:\nats-server.exe 
# Wed, 10 Nov 2021 17:03:09 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:03:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1d3f90d67d7551be12e9caf53f786235234151f513c0aadc754e5f033e183641`  
		Last Modified: Wed, 10 Nov 2021 17:06:32 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd8a5c6e6a53ddd4f3cdd7ae34bbe9c780fe53c7245304716909425bc26f7bb`  
		Last Modified: Wed, 10 Nov 2021 17:06:31 GMT  
		Size: 4.6 MB (4630764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7360e968604c4d5db8c901e6f52100633b1b227a9ac4c29b0308c424910d02`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c245f1add19193bc4fd407354089b6c244fe2d37ea9a0c7f3b55c4cd0abf678`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4949fe8ad7bd6aa73121e77f2feb4a983ddb04e9a8b68110350fe11533fd556`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5345772ce5a94a4d4b36bcc445defff481e83b2af0be6506b3bb8865ef9de4`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:e213dbb5f30da5582cdfb387f306db0e5a756d5cfa0c71ad04012c62c8364299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:f98772e0f2222bf626db93d8f4dab31459a0d859e901c5554cc076088bdc9f47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b229b8720408fa48ff27cb600c243a0ea34ae241af9a532a457dd1302ad60d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:47:45 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 05:47:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 05:47:49 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 05:47:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 05:47:49 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 05:47:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:47:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2de72945075aec3a93ecb6af12474a3623374dac5d6eb467826bb3f176d9db`  
		Last Modified: Sat, 13 Nov 2021 05:48:24 GMT  
		Size: 4.9 MB (4856278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a7e2c9925a779c559f1381de66066f54c7545dd547ab50f181fdf5bad8b76a`  
		Last Modified: Sat, 13 Nov 2021 05:48:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d123a218501888dc051dc9935a6248b5dc7f0ddad4256c03157e4ea9a4f76af6`  
		Last Modified: Sat, 13 Nov 2021 05:48:23 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:21253e09b5390b390f4a098fed97b8bce94d3c69d0aee847355ba4f5e9cc13ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7154888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3b3aae48860f1adc793dd60464e9b29d707ac7c543ae92201954544d2847a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 03:04:03 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 03:04:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 03:04:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 03:04:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 03:04:09 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 03:04:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 03:04:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f8239d892b947974d364086747c970b38caaebc528256b37602cbdda9d832`  
		Last Modified: Sat, 13 Nov 2021 03:06:15 GMT  
		Size: 4.5 MB (4518522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8850b565bedb3a41ba36fa532b68d4c035cb73bde2cc2fe456a21cff33f105`  
		Last Modified: Sat, 13 Nov 2021 03:06:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b231dc9db1099c1f0e27d1e668c4c7f7ba23cf94fd95e1edf541ae73ec20eabc`  
		Last Modified: Sat, 13 Nov 2021 03:06:13 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:927653b6f646dceb6d518c8d58652ae16f07a585f56e2083b8dc640aa54032bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6952724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed121c45beb860b69d68c3e2e94a2ac7015107c8968ea2a40307dc587a0756c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 10:49:53 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 10:49:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 10:49:59 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 10:49:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 10:50:00 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 10:50:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 10:50:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7667eb269dc08efac3da01b8675c36b733dbbe274c782a02e4a86b8361d5b942`  
		Last Modified: Sat, 13 Nov 2021 10:52:16 GMT  
		Size: 4.5 MB (4513136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e575668b5d7e7f7152f80542c775ccba3f377141e747e329fb23896bfe23e9`  
		Last Modified: Sat, 13 Nov 2021 10:52:14 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528edb88e91f872a79a50cc2def03d40caacfed6b26567bb649719c78bcadf70`  
		Last Modified: Sat, 13 Nov 2021 10:52:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb0858f816f57a2924dbf3c42b77a5601301f210b6a1f33c04b97bb399e76610
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb6a42e1013c13029a69794fd8a6f185e0fedd050fbb50e18fd15650344c8e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:53:10 GMT
ENV NATS_SERVER=2.6.4
# Fri, 12 Nov 2021 17:53:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 12 Nov 2021 17:53:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 12 Nov 2021 17:53:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Nov 2021 17:53:17 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Nov 2021 17:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 17:53:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b88cb6acca7834e23464b3b30fde201b2ccc92123018a6780943e447dbf390`  
		Last Modified: Fri, 12 Nov 2021 17:54:17 GMT  
		Size: 4.5 MB (4467169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41bb7b84481f686821765af47edff89c043129ad18d2fb7ff6946b5b9b9501a8`  
		Last Modified: Fri, 12 Nov 2021 17:54:16 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dced30908382b5bc20e0ba23d2a27c9af4578273423b5d10399b70774b3f4571`  
		Last Modified: Fri, 12 Nov 2021 17:54:16 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.14`

```console
$ docker pull nats@sha256:e213dbb5f30da5582cdfb387f306db0e5a756d5cfa0c71ad04012c62c8364299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:f98772e0f2222bf626db93d8f4dab31459a0d859e901c5554cc076088bdc9f47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b229b8720408fa48ff27cb600c243a0ea34ae241af9a532a457dd1302ad60d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:47:45 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 05:47:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 05:47:49 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 05:47:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 05:47:49 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 05:47:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:47:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2de72945075aec3a93ecb6af12474a3623374dac5d6eb467826bb3f176d9db`  
		Last Modified: Sat, 13 Nov 2021 05:48:24 GMT  
		Size: 4.9 MB (4856278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a7e2c9925a779c559f1381de66066f54c7545dd547ab50f181fdf5bad8b76a`  
		Last Modified: Sat, 13 Nov 2021 05:48:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d123a218501888dc051dc9935a6248b5dc7f0ddad4256c03157e4ea9a4f76af6`  
		Last Modified: Sat, 13 Nov 2021 05:48:23 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:21253e09b5390b390f4a098fed97b8bce94d3c69d0aee847355ba4f5e9cc13ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7154888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3b3aae48860f1adc793dd60464e9b29d707ac7c543ae92201954544d2847a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 03:04:03 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 03:04:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 03:04:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 03:04:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 03:04:09 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 03:04:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 03:04:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f8239d892b947974d364086747c970b38caaebc528256b37602cbdda9d832`  
		Last Modified: Sat, 13 Nov 2021 03:06:15 GMT  
		Size: 4.5 MB (4518522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8850b565bedb3a41ba36fa532b68d4c035cb73bde2cc2fe456a21cff33f105`  
		Last Modified: Sat, 13 Nov 2021 03:06:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b231dc9db1099c1f0e27d1e668c4c7f7ba23cf94fd95e1edf541ae73ec20eabc`  
		Last Modified: Sat, 13 Nov 2021 03:06:13 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:927653b6f646dceb6d518c8d58652ae16f07a585f56e2083b8dc640aa54032bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6952724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed121c45beb860b69d68c3e2e94a2ac7015107c8968ea2a40307dc587a0756c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 10:49:53 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 10:49:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 10:49:59 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 10:49:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 10:50:00 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 10:50:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 10:50:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7667eb269dc08efac3da01b8675c36b733dbbe274c782a02e4a86b8361d5b942`  
		Last Modified: Sat, 13 Nov 2021 10:52:16 GMT  
		Size: 4.5 MB (4513136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e575668b5d7e7f7152f80542c775ccba3f377141e747e329fb23896bfe23e9`  
		Last Modified: Sat, 13 Nov 2021 10:52:14 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528edb88e91f872a79a50cc2def03d40caacfed6b26567bb649719c78bcadf70`  
		Last Modified: Sat, 13 Nov 2021 10:52:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb0858f816f57a2924dbf3c42b77a5601301f210b6a1f33c04b97bb399e76610
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb6a42e1013c13029a69794fd8a6f185e0fedd050fbb50e18fd15650344c8e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:53:10 GMT
ENV NATS_SERVER=2.6.4
# Fri, 12 Nov 2021 17:53:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 12 Nov 2021 17:53:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 12 Nov 2021 17:53:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Nov 2021 17:53:17 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Nov 2021 17:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 17:53:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b88cb6acca7834e23464b3b30fde201b2ccc92123018a6780943e447dbf390`  
		Last Modified: Fri, 12 Nov 2021 17:54:17 GMT  
		Size: 4.5 MB (4467169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41bb7b84481f686821765af47edff89c043129ad18d2fb7ff6946b5b9b9501a8`  
		Last Modified: Fri, 12 Nov 2021 17:54:16 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dced30908382b5bc20e0ba23d2a27c9af4578273423b5d10399b70774b3f4571`  
		Last Modified: Fri, 12 Nov 2021 17:54:16 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:bc46b51540ff5a3d27c3cb3cb61878d610144d728bd3c8836244b063a96b1601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:ce50109292cf290d1f6559a806f7e6f1b202f4d97678700dbb386b1d6c021964
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa4b152b84f6a4cc5da9b870074d5807b7dc42dbf1f922c1ff7e3059d6ec1be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:f554ccd652a698194b4adc9f60df406473cf580a258d4b425944a529b6b7b718 in /nats-server 
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:00 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe57332791af252fb9335dd0de8a36fe319e51fdde00636db3fee85f1adcb22f`  
		Last Modified: Fri, 05 Nov 2021 01:41:48 GMT  
		Size: 4.6 MB (4573985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc9e783378fba5ac033e418e7db34fb0215aeaa59658adf4924ad46455f261e`  
		Last Modified: Fri, 05 Nov 2021 01:41:47 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:a94f85ec4b90db46b3c8d59ed4c35fa9033482dd0e50679775145fc0f2528b20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4236770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bee36fb33e6c4d4ec54bcbd1778a2d3a19dcd7706111ffaf4d1711e916f6dea`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:0e12b4e14d681c94ae627c578bd9cc8a3fc9bec59e0062a772ad0933b7947e38 in /nats-server 
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:03 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a273e90687e1ad496ce74eecec787df7511839c5e770850a184f261ed706fc98`  
		Last Modified: Fri, 05 Nov 2021 01:43:23 GMT  
		Size: 4.2 MB (4236294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6825ddc1425c3e1cfde24c7f0c22b2ad39646ecc4d15d72b1d4769687206880`  
		Last Modified: Fri, 05 Nov 2021 01:43:21 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:f2419d713943dd432426211cc6035a9e4cbb06b0cb63d5bca91017fabec840e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf917eacaf24a0ae8a3e5b85a3f2795362e8333bf2b527cb7a5470e0d6cd02b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 04:34:29 GMT
COPY file:f8c8928a8edabd057aa0fe0c8e12f7e68c80845a6af865b9263be1face1e988c in /nats-server 
# Fri, 05 Nov 2021 04:34:30 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 04:34:30 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 04:34:31 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 04:34:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:791f22945fc593348a417c1bdef534cefaa5f1d33df489dddc334de30b713a78`  
		Last Modified: Fri, 05 Nov 2021 04:36:53 GMT  
		Size: 4.2 MB (4232017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3b77fec3826280fc07c1e66876ec0d673939258c3a1dd1320cbc1c3d56b86`  
		Last Modified: Fri, 05 Nov 2021 04:36:50 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d7e28f91b2fc35b9a0ed2eb9a5e16070e4c2d1dff3f18076e465958b997cce01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089ea638210c9c36041b15aac4bf873a36e3b4bdca7b8e25d6c1b4cc9a274094`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:25:26 GMT
COPY file:2327a2e0254f808bd88c7e734365e343ac6cf801c454a43bf9035cd435fbf8d0 in /nats-server 
# Fri, 05 Nov 2021 01:25:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:25:27 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:25:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:25:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fd5084aec62b3e936e8b267729c530280fe1646e8e9d0e09ef842b74beccff33`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 4.2 MB (4182491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963e399425efdeb20d2700e846b7b3f5c36a5ecef7204cb3fe1476b7b835b2e6`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:ec6b3505bf01f1bdcd96d7f858771ad6e53c16075defda5d8046c83998c3a251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:85fc53257b869566352af427b00b1e4eb3be4d9c158473d05955a95358569c49
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107420117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efad7f25530c39976e06f9cd49e8bf8ccf60e961cf32e240771c3311fa8ecb24`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:08 GMT
RUN cmd /S /C #(nop) COPY file:d04f5d85a8b0edde975ace8d01e615862e9872904d6e700eb5be4601ac26087b in C:\nats-server.exe 
# Wed, 10 Nov 2021 17:03:09 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:03:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1d3f90d67d7551be12e9caf53f786235234151f513c0aadc754e5f033e183641`  
		Last Modified: Wed, 10 Nov 2021 17:06:32 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd8a5c6e6a53ddd4f3cdd7ae34bbe9c780fe53c7245304716909425bc26f7bb`  
		Last Modified: Wed, 10 Nov 2021 17:06:31 GMT  
		Size: 4.6 MB (4630764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7360e968604c4d5db8c901e6f52100633b1b227a9ac4c29b0308c424910d02`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c245f1add19193bc4fd407354089b6c244fe2d37ea9a0c7f3b55c4cd0abf678`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4949fe8ad7bd6aa73121e77f2feb4a983ddb04e9a8b68110350fe11533fd556`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5345772ce5a94a4d4b36bcc445defff481e83b2af0be6506b3bb8865ef9de4`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:ec6b3505bf01f1bdcd96d7f858771ad6e53c16075defda5d8046c83998c3a251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:85fc53257b869566352af427b00b1e4eb3be4d9c158473d05955a95358569c49
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107420117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efad7f25530c39976e06f9cd49e8bf8ccf60e961cf32e240771c3311fa8ecb24`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:08 GMT
RUN cmd /S /C #(nop) COPY file:d04f5d85a8b0edde975ace8d01e615862e9872904d6e700eb5be4601ac26087b in C:\nats-server.exe 
# Wed, 10 Nov 2021 17:03:09 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:03:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1d3f90d67d7551be12e9caf53f786235234151f513c0aadc754e5f033e183641`  
		Last Modified: Wed, 10 Nov 2021 17:06:32 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd8a5c6e6a53ddd4f3cdd7ae34bbe9c780fe53c7245304716909425bc26f7bb`  
		Last Modified: Wed, 10 Nov 2021 17:06:31 GMT  
		Size: 4.6 MB (4630764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7360e968604c4d5db8c901e6f52100633b1b227a9ac4c29b0308c424910d02`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c245f1add19193bc4fd407354089b6c244fe2d37ea9a0c7f3b55c4cd0abf678`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4949fe8ad7bd6aa73121e77f2feb4a983ddb04e9a8b68110350fe11533fd556`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5345772ce5a94a4d4b36bcc445defff481e83b2af0be6506b3bb8865ef9de4`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:bc46b51540ff5a3d27c3cb3cb61878d610144d728bd3c8836244b063a96b1601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:ce50109292cf290d1f6559a806f7e6f1b202f4d97678700dbb386b1d6c021964
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa4b152b84f6a4cc5da9b870074d5807b7dc42dbf1f922c1ff7e3059d6ec1be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:f554ccd652a698194b4adc9f60df406473cf580a258d4b425944a529b6b7b718 in /nats-server 
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:00 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe57332791af252fb9335dd0de8a36fe319e51fdde00636db3fee85f1adcb22f`  
		Last Modified: Fri, 05 Nov 2021 01:41:48 GMT  
		Size: 4.6 MB (4573985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc9e783378fba5ac033e418e7db34fb0215aeaa59658adf4924ad46455f261e`  
		Last Modified: Fri, 05 Nov 2021 01:41:47 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:a94f85ec4b90db46b3c8d59ed4c35fa9033482dd0e50679775145fc0f2528b20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4236770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bee36fb33e6c4d4ec54bcbd1778a2d3a19dcd7706111ffaf4d1711e916f6dea`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:0e12b4e14d681c94ae627c578bd9cc8a3fc9bec59e0062a772ad0933b7947e38 in /nats-server 
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:03 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a273e90687e1ad496ce74eecec787df7511839c5e770850a184f261ed706fc98`  
		Last Modified: Fri, 05 Nov 2021 01:43:23 GMT  
		Size: 4.2 MB (4236294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6825ddc1425c3e1cfde24c7f0c22b2ad39646ecc4d15d72b1d4769687206880`  
		Last Modified: Fri, 05 Nov 2021 01:43:21 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:f2419d713943dd432426211cc6035a9e4cbb06b0cb63d5bca91017fabec840e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf917eacaf24a0ae8a3e5b85a3f2795362e8333bf2b527cb7a5470e0d6cd02b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 04:34:29 GMT
COPY file:f8c8928a8edabd057aa0fe0c8e12f7e68c80845a6af865b9263be1face1e988c in /nats-server 
# Fri, 05 Nov 2021 04:34:30 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 04:34:30 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 04:34:31 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 04:34:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:791f22945fc593348a417c1bdef534cefaa5f1d33df489dddc334de30b713a78`  
		Last Modified: Fri, 05 Nov 2021 04:36:53 GMT  
		Size: 4.2 MB (4232017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3b77fec3826280fc07c1e66876ec0d673939258c3a1dd1320cbc1c3d56b86`  
		Last Modified: Fri, 05 Nov 2021 04:36:50 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d7e28f91b2fc35b9a0ed2eb9a5e16070e4c2d1dff3f18076e465958b997cce01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089ea638210c9c36041b15aac4bf873a36e3b4bdca7b8e25d6c1b4cc9a274094`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:25:26 GMT
COPY file:2327a2e0254f808bd88c7e734365e343ac6cf801c454a43bf9035cd435fbf8d0 in /nats-server 
# Fri, 05 Nov 2021 01:25:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:25:27 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:25:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:25:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fd5084aec62b3e936e8b267729c530280fe1646e8e9d0e09ef842b74beccff33`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 4.2 MB (4182491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963e399425efdeb20d2700e846b7b3f5c36a5ecef7204cb3fe1476b7b835b2e6`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:c5b7ed794ed1ea3bc9973244e683bd5dfb902e0bab7882855f15fb1696802bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:ad29bbedb595a4b3fc815bb5013d6af6deb55f459d016ed438c89308084ab2ae
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711460012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c235da1808d9829823250ce435b177c85ddd1340f0878343bb5e4a1521602a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 14:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:00:40 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:00:41 GMT
ENV NATS_SERVER=2.6.4
# Wed, 10 Nov 2021 17:00:42 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.4/nats-server-v2.6.4-windows-amd64.zip
# Wed, 10 Nov 2021 17:00:43 GMT
ENV NATS_SERVER_SHASUM=e287764a6e8b8ec132dcbe294aa3b96d779678079b7ada20a9bde1b81d5f5bbc
# Wed, 10 Nov 2021 17:01:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Nov 2021 17:02:51 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Nov 2021 17:02:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:02:53 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:02:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:02:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db1ba835bccbdc73ef254c175ca6ae0dc3f0bd759c1910c3b123cfb9613223be`  
		Last Modified: Wed, 10 Nov 2021 16:21:11 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3df59793c391e0eb7e6a2ddb65801dfa94397b370daa52d04e242ba0274e3d`  
		Last Modified: Wed, 10 Nov 2021 17:06:13 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46075e93c469fbc556a996840e6ebbd02849d7518dcb4fb9feed459795714e03`  
		Last Modified: Wed, 10 Nov 2021 17:06:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a915f8554b2287a16ae0945b328b1d7d315b85bd0eda548bfde73d7686a79c`  
		Last Modified: Wed, 10 Nov 2021 17:06:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4eabf66e1adaa7841404639039b5becdbfb43fc726b93da058b0552478b7`  
		Last Modified: Wed, 10 Nov 2021 17:06:11 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f61c483196bb419b4709f89f9df78e12e7f6dab4ad8094a5aee57e021c97eb0`  
		Last Modified: Wed, 10 Nov 2021 17:06:12 GMT  
		Size: 352.3 KB (352252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e167a3b21bfb85235d9775123ea38ca0d4a4c71383ca34a95f3e203f6afddfc9`  
		Last Modified: Wed, 10 Nov 2021 17:06:15 GMT  
		Size: 5.0 MB (4973372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1d94f1b880ea3ea631c3f6e7ddeffdb30d7af80b037e2fdb55db516d018dd5`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.9 KB (1939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb1edd94e1965c70a2bb20e8bac08446704c452ce9342438e89afe2febe9906`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2d4b3e56ee1751a9373a33f5b9d58f1843e22f5ec7cc88f00e6ef369d7d9f7`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfe4f9233effe09d6160c4278ac3a375234523f40d18c3a826dd9e741139be8`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:b8b34e3ddc6569eda34bb1d124a6c427fc3820313fea9618b702a1fe9a281914
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278456953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c0d6fd779bb5acd23d794cab7a62d0a39d140ff94c890f83cdb2814d63808d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 14:32:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:03:18 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:19 GMT
ENV NATS_SERVER=2.6.4
# Wed, 10 Nov 2021 17:03:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.4/nats-server-v2.6.4-windows-amd64.zip
# Wed, 10 Nov 2021 17:03:21 GMT
ENV NATS_SERVER_SHASUM=e287764a6e8b8ec132dcbe294aa3b96d779678079b7ada20a9bde1b81d5f5bbc
# Wed, 10 Nov 2021 17:04:06 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Nov 2021 17:05:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Nov 2021 17:05:31 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:05:32 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:05:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:05:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f6f303e73635c7923a8c64f8938e7ba4c10210fd15a6ce63aa8a62d5a8ea8c0a`  
		Last Modified: Wed, 10 Nov 2021 16:21:33 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5db4062c12269959ca71caf00b70e9baebf61b90c49c74db0e2cdb04cf83e8`  
		Last Modified: Wed, 10 Nov 2021 17:06:51 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4a229bc6e55d797c98ddd01e4d2dde702cc15dfa57f7822427f4b0c7520a1f`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99e43798e75fd46299bad03217fa38c7f0b36023271b5ded075984cbf2df237`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cc0e5c4cac5fdb636f2f1103de5fe3668597d85350d0d91b1834cc44a83b44`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb570dbf36f38785df2fc8983ad0725e443f375bdd45954981931f0137e26ea6`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 350.2 KB (350227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007ae15590fbd4c2fc97f92a5fd9f4bbee82f5e8d9da82ac218b4d5002f1a50d`  
		Last Modified: Wed, 10 Nov 2021 17:06:52 GMT  
		Size: 5.0 MB (5002607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbf9bfc6a773256d2ac9289665265759ec89a55717d181030cc64c706b5be9a`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92c772d8667daf25c2468b4b149536c7e9fe55a5896143d2e4eba0ca861cede`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca4dbf235f9fc558316b5e2119a389936545de68e74f1ad4acd18c7282eff43`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990cb23cac15d214ca7bac2df486570024c5eb19e214014a88b247c684605ee5`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:b4394e47153d08bdfa6f28759e02e8c37aa9dd5dd759f4a07417b010722de909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:ad29bbedb595a4b3fc815bb5013d6af6deb55f459d016ed438c89308084ab2ae
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711460012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c235da1808d9829823250ce435b177c85ddd1340f0878343bb5e4a1521602a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 14:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:00:40 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:00:41 GMT
ENV NATS_SERVER=2.6.4
# Wed, 10 Nov 2021 17:00:42 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.4/nats-server-v2.6.4-windows-amd64.zip
# Wed, 10 Nov 2021 17:00:43 GMT
ENV NATS_SERVER_SHASUM=e287764a6e8b8ec132dcbe294aa3b96d779678079b7ada20a9bde1b81d5f5bbc
# Wed, 10 Nov 2021 17:01:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Nov 2021 17:02:51 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Nov 2021 17:02:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:02:53 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:02:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:02:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db1ba835bccbdc73ef254c175ca6ae0dc3f0bd759c1910c3b123cfb9613223be`  
		Last Modified: Wed, 10 Nov 2021 16:21:11 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3df59793c391e0eb7e6a2ddb65801dfa94397b370daa52d04e242ba0274e3d`  
		Last Modified: Wed, 10 Nov 2021 17:06:13 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46075e93c469fbc556a996840e6ebbd02849d7518dcb4fb9feed459795714e03`  
		Last Modified: Wed, 10 Nov 2021 17:06:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a915f8554b2287a16ae0945b328b1d7d315b85bd0eda548bfde73d7686a79c`  
		Last Modified: Wed, 10 Nov 2021 17:06:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4eabf66e1adaa7841404639039b5becdbfb43fc726b93da058b0552478b7`  
		Last Modified: Wed, 10 Nov 2021 17:06:11 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f61c483196bb419b4709f89f9df78e12e7f6dab4ad8094a5aee57e021c97eb0`  
		Last Modified: Wed, 10 Nov 2021 17:06:12 GMT  
		Size: 352.3 KB (352252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e167a3b21bfb85235d9775123ea38ca0d4a4c71383ca34a95f3e203f6afddfc9`  
		Last Modified: Wed, 10 Nov 2021 17:06:15 GMT  
		Size: 5.0 MB (4973372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1d94f1b880ea3ea631c3f6e7ddeffdb30d7af80b037e2fdb55db516d018dd5`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.9 KB (1939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb1edd94e1965c70a2bb20e8bac08446704c452ce9342438e89afe2febe9906`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2d4b3e56ee1751a9373a33f5b9d58f1843e22f5ec7cc88f00e6ef369d7d9f7`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfe4f9233effe09d6160c4278ac3a375234523f40d18c3a826dd9e741139be8`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:9c7dc9b1c133e0e5541993a156235c85c3a299c4666f96653fccd33e794fb1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:b8b34e3ddc6569eda34bb1d124a6c427fc3820313fea9618b702a1fe9a281914
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278456953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c0d6fd779bb5acd23d794cab7a62d0a39d140ff94c890f83cdb2814d63808d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 14:32:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:03:18 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:19 GMT
ENV NATS_SERVER=2.6.4
# Wed, 10 Nov 2021 17:03:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.4/nats-server-v2.6.4-windows-amd64.zip
# Wed, 10 Nov 2021 17:03:21 GMT
ENV NATS_SERVER_SHASUM=e287764a6e8b8ec132dcbe294aa3b96d779678079b7ada20a9bde1b81d5f5bbc
# Wed, 10 Nov 2021 17:04:06 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Nov 2021 17:05:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Nov 2021 17:05:31 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:05:32 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:05:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:05:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f6f303e73635c7923a8c64f8938e7ba4c10210fd15a6ce63aa8a62d5a8ea8c0a`  
		Last Modified: Wed, 10 Nov 2021 16:21:33 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5db4062c12269959ca71caf00b70e9baebf61b90c49c74db0e2cdb04cf83e8`  
		Last Modified: Wed, 10 Nov 2021 17:06:51 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4a229bc6e55d797c98ddd01e4d2dde702cc15dfa57f7822427f4b0c7520a1f`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99e43798e75fd46299bad03217fa38c7f0b36023271b5ded075984cbf2df237`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cc0e5c4cac5fdb636f2f1103de5fe3668597d85350d0d91b1834cc44a83b44`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb570dbf36f38785df2fc8983ad0725e443f375bdd45954981931f0137e26ea6`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 350.2 KB (350227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007ae15590fbd4c2fc97f92a5fd9f4bbee82f5e8d9da82ac218b4d5002f1a50d`  
		Last Modified: Wed, 10 Nov 2021 17:06:52 GMT  
		Size: 5.0 MB (5002607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbf9bfc6a773256d2ac9289665265759ec89a55717d181030cc64c706b5be9a`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92c772d8667daf25c2468b4b149536c7e9fe55a5896143d2e4eba0ca861cede`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca4dbf235f9fc558316b5e2119a389936545de68e74f1ad4acd18c7282eff43`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990cb23cac15d214ca7bac2df486570024c5eb19e214014a88b247c684605ee5`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6`

```console
$ docker pull nats@sha256:2511f2a913b84b7a39dd6411d1dbb19ceae4006a5b8a8de7caadff42898e5d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6` - linux; amd64

```console
$ docker pull nats@sha256:ce50109292cf290d1f6559a806f7e6f1b202f4d97678700dbb386b1d6c021964
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa4b152b84f6a4cc5da9b870074d5807b7dc42dbf1f922c1ff7e3059d6ec1be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:f554ccd652a698194b4adc9f60df406473cf580a258d4b425944a529b6b7b718 in /nats-server 
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:00 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe57332791af252fb9335dd0de8a36fe319e51fdde00636db3fee85f1adcb22f`  
		Last Modified: Fri, 05 Nov 2021 01:41:48 GMT  
		Size: 4.6 MB (4573985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc9e783378fba5ac033e418e7db34fb0215aeaa59658adf4924ad46455f261e`  
		Last Modified: Fri, 05 Nov 2021 01:41:47 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6` - linux; arm variant v6

```console
$ docker pull nats@sha256:a94f85ec4b90db46b3c8d59ed4c35fa9033482dd0e50679775145fc0f2528b20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4236770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bee36fb33e6c4d4ec54bcbd1778a2d3a19dcd7706111ffaf4d1711e916f6dea`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:0e12b4e14d681c94ae627c578bd9cc8a3fc9bec59e0062a772ad0933b7947e38 in /nats-server 
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:03 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a273e90687e1ad496ce74eecec787df7511839c5e770850a184f261ed706fc98`  
		Last Modified: Fri, 05 Nov 2021 01:43:23 GMT  
		Size: 4.2 MB (4236294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6825ddc1425c3e1cfde24c7f0c22b2ad39646ecc4d15d72b1d4769687206880`  
		Last Modified: Fri, 05 Nov 2021 01:43:21 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6` - linux; arm variant v7

```console
$ docker pull nats@sha256:f2419d713943dd432426211cc6035a9e4cbb06b0cb63d5bca91017fabec840e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf917eacaf24a0ae8a3e5b85a3f2795362e8333bf2b527cb7a5470e0d6cd02b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 04:34:29 GMT
COPY file:f8c8928a8edabd057aa0fe0c8e12f7e68c80845a6af865b9263be1face1e988c in /nats-server 
# Fri, 05 Nov 2021 04:34:30 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 04:34:30 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 04:34:31 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 04:34:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:791f22945fc593348a417c1bdef534cefaa5f1d33df489dddc334de30b713a78`  
		Last Modified: Fri, 05 Nov 2021 04:36:53 GMT  
		Size: 4.2 MB (4232017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3b77fec3826280fc07c1e66876ec0d673939258c3a1dd1320cbc1c3d56b86`  
		Last Modified: Fri, 05 Nov 2021 04:36:50 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d7e28f91b2fc35b9a0ed2eb9a5e16070e4c2d1dff3f18076e465958b997cce01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089ea638210c9c36041b15aac4bf873a36e3b4bdca7b8e25d6c1b4cc9a274094`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:25:26 GMT
COPY file:2327a2e0254f808bd88c7e734365e343ac6cf801c454a43bf9035cd435fbf8d0 in /nats-server 
# Fri, 05 Nov 2021 01:25:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:25:27 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:25:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:25:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fd5084aec62b3e936e8b267729c530280fe1646e8e9d0e09ef842b74beccff33`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 4.2 MB (4182491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963e399425efdeb20d2700e846b7b3f5c36a5ecef7204cb3fe1476b7b835b2e6`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:85fc53257b869566352af427b00b1e4eb3be4d9c158473d05955a95358569c49
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107420117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efad7f25530c39976e06f9cd49e8bf8ccf60e961cf32e240771c3311fa8ecb24`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:08 GMT
RUN cmd /S /C #(nop) COPY file:d04f5d85a8b0edde975ace8d01e615862e9872904d6e700eb5be4601ac26087b in C:\nats-server.exe 
# Wed, 10 Nov 2021 17:03:09 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:03:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1d3f90d67d7551be12e9caf53f786235234151f513c0aadc754e5f033e183641`  
		Last Modified: Wed, 10 Nov 2021 17:06:32 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd8a5c6e6a53ddd4f3cdd7ae34bbe9c780fe53c7245304716909425bc26f7bb`  
		Last Modified: Wed, 10 Nov 2021 17:06:31 GMT  
		Size: 4.6 MB (4630764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7360e968604c4d5db8c901e6f52100633b1b227a9ac4c29b0308c424910d02`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c245f1add19193bc4fd407354089b6c244fe2d37ea9a0c7f3b55c4cd0abf678`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4949fe8ad7bd6aa73121e77f2feb4a983ddb04e9a8b68110350fe11533fd556`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5345772ce5a94a4d4b36bcc445defff481e83b2af0be6506b3bb8865ef9de4`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-alpine`

```console
$ docker pull nats@sha256:e213dbb5f30da5582cdfb387f306db0e5a756d5cfa0c71ad04012c62c8364299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6-alpine` - linux; amd64

```console
$ docker pull nats@sha256:f98772e0f2222bf626db93d8f4dab31459a0d859e901c5554cc076088bdc9f47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b229b8720408fa48ff27cb600c243a0ea34ae241af9a532a457dd1302ad60d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:47:45 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 05:47:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 05:47:49 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 05:47:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 05:47:49 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 05:47:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:47:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2de72945075aec3a93ecb6af12474a3623374dac5d6eb467826bb3f176d9db`  
		Last Modified: Sat, 13 Nov 2021 05:48:24 GMT  
		Size: 4.9 MB (4856278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a7e2c9925a779c559f1381de66066f54c7545dd547ab50f181fdf5bad8b76a`  
		Last Modified: Sat, 13 Nov 2021 05:48:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d123a218501888dc051dc9935a6248b5dc7f0ddad4256c03157e4ea9a4f76af6`  
		Last Modified: Sat, 13 Nov 2021 05:48:23 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:21253e09b5390b390f4a098fed97b8bce94d3c69d0aee847355ba4f5e9cc13ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7154888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3b3aae48860f1adc793dd60464e9b29d707ac7c543ae92201954544d2847a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 03:04:03 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 03:04:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 03:04:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 03:04:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 03:04:09 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 03:04:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 03:04:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f8239d892b947974d364086747c970b38caaebc528256b37602cbdda9d832`  
		Last Modified: Sat, 13 Nov 2021 03:06:15 GMT  
		Size: 4.5 MB (4518522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8850b565bedb3a41ba36fa532b68d4c035cb73bde2cc2fe456a21cff33f105`  
		Last Modified: Sat, 13 Nov 2021 03:06:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b231dc9db1099c1f0e27d1e668c4c7f7ba23cf94fd95e1edf541ae73ec20eabc`  
		Last Modified: Sat, 13 Nov 2021 03:06:13 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:927653b6f646dceb6d518c8d58652ae16f07a585f56e2083b8dc640aa54032bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6952724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed121c45beb860b69d68c3e2e94a2ac7015107c8968ea2a40307dc587a0756c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 10:49:53 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 10:49:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 10:49:59 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 10:49:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 10:50:00 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 10:50:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 10:50:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7667eb269dc08efac3da01b8675c36b733dbbe274c782a02e4a86b8361d5b942`  
		Last Modified: Sat, 13 Nov 2021 10:52:16 GMT  
		Size: 4.5 MB (4513136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e575668b5d7e7f7152f80542c775ccba3f377141e747e329fb23896bfe23e9`  
		Last Modified: Sat, 13 Nov 2021 10:52:14 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528edb88e91f872a79a50cc2def03d40caacfed6b26567bb649719c78bcadf70`  
		Last Modified: Sat, 13 Nov 2021 10:52:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb0858f816f57a2924dbf3c42b77a5601301f210b6a1f33c04b97bb399e76610
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb6a42e1013c13029a69794fd8a6f185e0fedd050fbb50e18fd15650344c8e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:53:10 GMT
ENV NATS_SERVER=2.6.4
# Fri, 12 Nov 2021 17:53:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 12 Nov 2021 17:53:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 12 Nov 2021 17:53:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Nov 2021 17:53:17 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Nov 2021 17:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 17:53:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b88cb6acca7834e23464b3b30fde201b2ccc92123018a6780943e447dbf390`  
		Last Modified: Fri, 12 Nov 2021 17:54:17 GMT  
		Size: 4.5 MB (4467169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41bb7b84481f686821765af47edff89c043129ad18d2fb7ff6946b5b9b9501a8`  
		Last Modified: Fri, 12 Nov 2021 17:54:16 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dced30908382b5bc20e0ba23d2a27c9af4578273423b5d10399b70774b3f4571`  
		Last Modified: Fri, 12 Nov 2021 17:54:16 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-alpine3.14`

```console
$ docker pull nats@sha256:e213dbb5f30da5582cdfb387f306db0e5a756d5cfa0c71ad04012c62c8364299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6-alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:f98772e0f2222bf626db93d8f4dab31459a0d859e901c5554cc076088bdc9f47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b229b8720408fa48ff27cb600c243a0ea34ae241af9a532a457dd1302ad60d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:47:45 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 05:47:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 05:47:49 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 05:47:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 05:47:49 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 05:47:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:47:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2de72945075aec3a93ecb6af12474a3623374dac5d6eb467826bb3f176d9db`  
		Last Modified: Sat, 13 Nov 2021 05:48:24 GMT  
		Size: 4.9 MB (4856278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a7e2c9925a779c559f1381de66066f54c7545dd547ab50f181fdf5bad8b76a`  
		Last Modified: Sat, 13 Nov 2021 05:48:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d123a218501888dc051dc9935a6248b5dc7f0ddad4256c03157e4ea9a4f76af6`  
		Last Modified: Sat, 13 Nov 2021 05:48:23 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-alpine3.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:21253e09b5390b390f4a098fed97b8bce94d3c69d0aee847355ba4f5e9cc13ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7154888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3b3aae48860f1adc793dd60464e9b29d707ac7c543ae92201954544d2847a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 03:04:03 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 03:04:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 03:04:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 03:04:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 03:04:09 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 03:04:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 03:04:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f8239d892b947974d364086747c970b38caaebc528256b37602cbdda9d832`  
		Last Modified: Sat, 13 Nov 2021 03:06:15 GMT  
		Size: 4.5 MB (4518522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8850b565bedb3a41ba36fa532b68d4c035cb73bde2cc2fe456a21cff33f105`  
		Last Modified: Sat, 13 Nov 2021 03:06:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b231dc9db1099c1f0e27d1e668c4c7f7ba23cf94fd95e1edf541ae73ec20eabc`  
		Last Modified: Sat, 13 Nov 2021 03:06:13 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-alpine3.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:927653b6f646dceb6d518c8d58652ae16f07a585f56e2083b8dc640aa54032bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6952724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed121c45beb860b69d68c3e2e94a2ac7015107c8968ea2a40307dc587a0756c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 10:49:53 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 10:49:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 10:49:59 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 10:49:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 10:50:00 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 10:50:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 10:50:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7667eb269dc08efac3da01b8675c36b733dbbe274c782a02e4a86b8361d5b942`  
		Last Modified: Sat, 13 Nov 2021 10:52:16 GMT  
		Size: 4.5 MB (4513136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e575668b5d7e7f7152f80542c775ccba3f377141e747e329fb23896bfe23e9`  
		Last Modified: Sat, 13 Nov 2021 10:52:14 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528edb88e91f872a79a50cc2def03d40caacfed6b26567bb649719c78bcadf70`  
		Last Modified: Sat, 13 Nov 2021 10:52:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb0858f816f57a2924dbf3c42b77a5601301f210b6a1f33c04b97bb399e76610
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb6a42e1013c13029a69794fd8a6f185e0fedd050fbb50e18fd15650344c8e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:53:10 GMT
ENV NATS_SERVER=2.6.4
# Fri, 12 Nov 2021 17:53:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 12 Nov 2021 17:53:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 12 Nov 2021 17:53:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Nov 2021 17:53:17 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Nov 2021 17:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 17:53:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b88cb6acca7834e23464b3b30fde201b2ccc92123018a6780943e447dbf390`  
		Last Modified: Fri, 12 Nov 2021 17:54:17 GMT  
		Size: 4.5 MB (4467169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41bb7b84481f686821765af47edff89c043129ad18d2fb7ff6946b5b9b9501a8`  
		Last Modified: Fri, 12 Nov 2021 17:54:16 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dced30908382b5bc20e0ba23d2a27c9af4578273423b5d10399b70774b3f4571`  
		Last Modified: Fri, 12 Nov 2021 17:54:16 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-linux`

```console
$ docker pull nats@sha256:bc46b51540ff5a3d27c3cb3cb61878d610144d728bd3c8836244b063a96b1601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6-linux` - linux; amd64

```console
$ docker pull nats@sha256:ce50109292cf290d1f6559a806f7e6f1b202f4d97678700dbb386b1d6c021964
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa4b152b84f6a4cc5da9b870074d5807b7dc42dbf1f922c1ff7e3059d6ec1be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:f554ccd652a698194b4adc9f60df406473cf580a258d4b425944a529b6b7b718 in /nats-server 
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:00 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe57332791af252fb9335dd0de8a36fe319e51fdde00636db3fee85f1adcb22f`  
		Last Modified: Fri, 05 Nov 2021 01:41:48 GMT  
		Size: 4.6 MB (4573985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc9e783378fba5ac033e418e7db34fb0215aeaa59658adf4924ad46455f261e`  
		Last Modified: Fri, 05 Nov 2021 01:41:47 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:a94f85ec4b90db46b3c8d59ed4c35fa9033482dd0e50679775145fc0f2528b20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4236770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bee36fb33e6c4d4ec54bcbd1778a2d3a19dcd7706111ffaf4d1711e916f6dea`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:0e12b4e14d681c94ae627c578bd9cc8a3fc9bec59e0062a772ad0933b7947e38 in /nats-server 
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:03 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a273e90687e1ad496ce74eecec787df7511839c5e770850a184f261ed706fc98`  
		Last Modified: Fri, 05 Nov 2021 01:43:23 GMT  
		Size: 4.2 MB (4236294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6825ddc1425c3e1cfde24c7f0c22b2ad39646ecc4d15d72b1d4769687206880`  
		Last Modified: Fri, 05 Nov 2021 01:43:21 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:f2419d713943dd432426211cc6035a9e4cbb06b0cb63d5bca91017fabec840e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf917eacaf24a0ae8a3e5b85a3f2795362e8333bf2b527cb7a5470e0d6cd02b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 04:34:29 GMT
COPY file:f8c8928a8edabd057aa0fe0c8e12f7e68c80845a6af865b9263be1face1e988c in /nats-server 
# Fri, 05 Nov 2021 04:34:30 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 04:34:30 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 04:34:31 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 04:34:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:791f22945fc593348a417c1bdef534cefaa5f1d33df489dddc334de30b713a78`  
		Last Modified: Fri, 05 Nov 2021 04:36:53 GMT  
		Size: 4.2 MB (4232017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3b77fec3826280fc07c1e66876ec0d673939258c3a1dd1320cbc1c3d56b86`  
		Last Modified: Fri, 05 Nov 2021 04:36:50 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d7e28f91b2fc35b9a0ed2eb9a5e16070e4c2d1dff3f18076e465958b997cce01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089ea638210c9c36041b15aac4bf873a36e3b4bdca7b8e25d6c1b4cc9a274094`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:25:26 GMT
COPY file:2327a2e0254f808bd88c7e734365e343ac6cf801c454a43bf9035cd435fbf8d0 in /nats-server 
# Fri, 05 Nov 2021 01:25:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:25:27 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:25:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:25:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fd5084aec62b3e936e8b267729c530280fe1646e8e9d0e09ef842b74beccff33`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 4.2 MB (4182491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963e399425efdeb20d2700e846b7b3f5c36a5ecef7204cb3fe1476b7b835b2e6`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-nanoserver`

```console
$ docker pull nats@sha256:ec6b3505bf01f1bdcd96d7f858771ad6e53c16075defda5d8046c83998c3a251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6-nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:85fc53257b869566352af427b00b1e4eb3be4d9c158473d05955a95358569c49
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107420117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efad7f25530c39976e06f9cd49e8bf8ccf60e961cf32e240771c3311fa8ecb24`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:08 GMT
RUN cmd /S /C #(nop) COPY file:d04f5d85a8b0edde975ace8d01e615862e9872904d6e700eb5be4601ac26087b in C:\nats-server.exe 
# Wed, 10 Nov 2021 17:03:09 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:03:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1d3f90d67d7551be12e9caf53f786235234151f513c0aadc754e5f033e183641`  
		Last Modified: Wed, 10 Nov 2021 17:06:32 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd8a5c6e6a53ddd4f3cdd7ae34bbe9c780fe53c7245304716909425bc26f7bb`  
		Last Modified: Wed, 10 Nov 2021 17:06:31 GMT  
		Size: 4.6 MB (4630764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7360e968604c4d5db8c901e6f52100633b1b227a9ac4c29b0308c424910d02`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c245f1add19193bc4fd407354089b6c244fe2d37ea9a0c7f3b55c4cd0abf678`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4949fe8ad7bd6aa73121e77f2feb4a983ddb04e9a8b68110350fe11533fd556`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5345772ce5a94a4d4b36bcc445defff481e83b2af0be6506b3bb8865ef9de4`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-nanoserver-1809`

```console
$ docker pull nats@sha256:ec6b3505bf01f1bdcd96d7f858771ad6e53c16075defda5d8046c83998c3a251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6-nanoserver-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:85fc53257b869566352af427b00b1e4eb3be4d9c158473d05955a95358569c49
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107420117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efad7f25530c39976e06f9cd49e8bf8ccf60e961cf32e240771c3311fa8ecb24`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:08 GMT
RUN cmd /S /C #(nop) COPY file:d04f5d85a8b0edde975ace8d01e615862e9872904d6e700eb5be4601ac26087b in C:\nats-server.exe 
# Wed, 10 Nov 2021 17:03:09 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:03:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1d3f90d67d7551be12e9caf53f786235234151f513c0aadc754e5f033e183641`  
		Last Modified: Wed, 10 Nov 2021 17:06:32 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd8a5c6e6a53ddd4f3cdd7ae34bbe9c780fe53c7245304716909425bc26f7bb`  
		Last Modified: Wed, 10 Nov 2021 17:06:31 GMT  
		Size: 4.6 MB (4630764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7360e968604c4d5db8c901e6f52100633b1b227a9ac4c29b0308c424910d02`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c245f1add19193bc4fd407354089b6c244fe2d37ea9a0c7f3b55c4cd0abf678`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4949fe8ad7bd6aa73121e77f2feb4a983ddb04e9a8b68110350fe11533fd556`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5345772ce5a94a4d4b36bcc445defff481e83b2af0be6506b3bb8865ef9de4`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-scratch`

```console
$ docker pull nats@sha256:bc46b51540ff5a3d27c3cb3cb61878d610144d728bd3c8836244b063a96b1601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6-scratch` - linux; amd64

```console
$ docker pull nats@sha256:ce50109292cf290d1f6559a806f7e6f1b202f4d97678700dbb386b1d6c021964
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa4b152b84f6a4cc5da9b870074d5807b7dc42dbf1f922c1ff7e3059d6ec1be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:f554ccd652a698194b4adc9f60df406473cf580a258d4b425944a529b6b7b718 in /nats-server 
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:00 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe57332791af252fb9335dd0de8a36fe319e51fdde00636db3fee85f1adcb22f`  
		Last Modified: Fri, 05 Nov 2021 01:41:48 GMT  
		Size: 4.6 MB (4573985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc9e783378fba5ac033e418e7db34fb0215aeaa59658adf4924ad46455f261e`  
		Last Modified: Fri, 05 Nov 2021 01:41:47 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:a94f85ec4b90db46b3c8d59ed4c35fa9033482dd0e50679775145fc0f2528b20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4236770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bee36fb33e6c4d4ec54bcbd1778a2d3a19dcd7706111ffaf4d1711e916f6dea`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:0e12b4e14d681c94ae627c578bd9cc8a3fc9bec59e0062a772ad0933b7947e38 in /nats-server 
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:03 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a273e90687e1ad496ce74eecec787df7511839c5e770850a184f261ed706fc98`  
		Last Modified: Fri, 05 Nov 2021 01:43:23 GMT  
		Size: 4.2 MB (4236294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6825ddc1425c3e1cfde24c7f0c22b2ad39646ecc4d15d72b1d4769687206880`  
		Last Modified: Fri, 05 Nov 2021 01:43:21 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:f2419d713943dd432426211cc6035a9e4cbb06b0cb63d5bca91017fabec840e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf917eacaf24a0ae8a3e5b85a3f2795362e8333bf2b527cb7a5470e0d6cd02b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 04:34:29 GMT
COPY file:f8c8928a8edabd057aa0fe0c8e12f7e68c80845a6af865b9263be1face1e988c in /nats-server 
# Fri, 05 Nov 2021 04:34:30 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 04:34:30 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 04:34:31 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 04:34:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:791f22945fc593348a417c1bdef534cefaa5f1d33df489dddc334de30b713a78`  
		Last Modified: Fri, 05 Nov 2021 04:36:53 GMT  
		Size: 4.2 MB (4232017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3b77fec3826280fc07c1e66876ec0d673939258c3a1dd1320cbc1c3d56b86`  
		Last Modified: Fri, 05 Nov 2021 04:36:50 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d7e28f91b2fc35b9a0ed2eb9a5e16070e4c2d1dff3f18076e465958b997cce01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089ea638210c9c36041b15aac4bf873a36e3b4bdca7b8e25d6c1b4cc9a274094`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:25:26 GMT
COPY file:2327a2e0254f808bd88c7e734365e343ac6cf801c454a43bf9035cd435fbf8d0 in /nats-server 
# Fri, 05 Nov 2021 01:25:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:25:27 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:25:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:25:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fd5084aec62b3e936e8b267729c530280fe1646e8e9d0e09ef842b74beccff33`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 4.2 MB (4182491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963e399425efdeb20d2700e846b7b3f5c36a5ecef7204cb3fe1476b7b835b2e6`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-windowsservercore`

```console
$ docker pull nats@sha256:c5b7ed794ed1ea3bc9973244e683bd5dfb902e0bab7882855f15fb1696802bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `nats:2.6-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:ad29bbedb595a4b3fc815bb5013d6af6deb55f459d016ed438c89308084ab2ae
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711460012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c235da1808d9829823250ce435b177c85ddd1340f0878343bb5e4a1521602a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 14:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:00:40 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:00:41 GMT
ENV NATS_SERVER=2.6.4
# Wed, 10 Nov 2021 17:00:42 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.4/nats-server-v2.6.4-windows-amd64.zip
# Wed, 10 Nov 2021 17:00:43 GMT
ENV NATS_SERVER_SHASUM=e287764a6e8b8ec132dcbe294aa3b96d779678079b7ada20a9bde1b81d5f5bbc
# Wed, 10 Nov 2021 17:01:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Nov 2021 17:02:51 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Nov 2021 17:02:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:02:53 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:02:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:02:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db1ba835bccbdc73ef254c175ca6ae0dc3f0bd759c1910c3b123cfb9613223be`  
		Last Modified: Wed, 10 Nov 2021 16:21:11 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3df59793c391e0eb7e6a2ddb65801dfa94397b370daa52d04e242ba0274e3d`  
		Last Modified: Wed, 10 Nov 2021 17:06:13 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46075e93c469fbc556a996840e6ebbd02849d7518dcb4fb9feed459795714e03`  
		Last Modified: Wed, 10 Nov 2021 17:06:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a915f8554b2287a16ae0945b328b1d7d315b85bd0eda548bfde73d7686a79c`  
		Last Modified: Wed, 10 Nov 2021 17:06:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4eabf66e1adaa7841404639039b5becdbfb43fc726b93da058b0552478b7`  
		Last Modified: Wed, 10 Nov 2021 17:06:11 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f61c483196bb419b4709f89f9df78e12e7f6dab4ad8094a5aee57e021c97eb0`  
		Last Modified: Wed, 10 Nov 2021 17:06:12 GMT  
		Size: 352.3 KB (352252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e167a3b21bfb85235d9775123ea38ca0d4a4c71383ca34a95f3e203f6afddfc9`  
		Last Modified: Wed, 10 Nov 2021 17:06:15 GMT  
		Size: 5.0 MB (4973372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1d94f1b880ea3ea631c3f6e7ddeffdb30d7af80b037e2fdb55db516d018dd5`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.9 KB (1939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb1edd94e1965c70a2bb20e8bac08446704c452ce9342438e89afe2febe9906`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2d4b3e56ee1751a9373a33f5b9d58f1843e22f5ec7cc88f00e6ef369d7d9f7`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfe4f9233effe09d6160c4278ac3a375234523f40d18c3a826dd9e741139be8`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:b8b34e3ddc6569eda34bb1d124a6c427fc3820313fea9618b702a1fe9a281914
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278456953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c0d6fd779bb5acd23d794cab7a62d0a39d140ff94c890f83cdb2814d63808d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 14:32:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:03:18 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:19 GMT
ENV NATS_SERVER=2.6.4
# Wed, 10 Nov 2021 17:03:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.4/nats-server-v2.6.4-windows-amd64.zip
# Wed, 10 Nov 2021 17:03:21 GMT
ENV NATS_SERVER_SHASUM=e287764a6e8b8ec132dcbe294aa3b96d779678079b7ada20a9bde1b81d5f5bbc
# Wed, 10 Nov 2021 17:04:06 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Nov 2021 17:05:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Nov 2021 17:05:31 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:05:32 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:05:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:05:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f6f303e73635c7923a8c64f8938e7ba4c10210fd15a6ce63aa8a62d5a8ea8c0a`  
		Last Modified: Wed, 10 Nov 2021 16:21:33 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5db4062c12269959ca71caf00b70e9baebf61b90c49c74db0e2cdb04cf83e8`  
		Last Modified: Wed, 10 Nov 2021 17:06:51 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4a229bc6e55d797c98ddd01e4d2dde702cc15dfa57f7822427f4b0c7520a1f`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99e43798e75fd46299bad03217fa38c7f0b36023271b5ded075984cbf2df237`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cc0e5c4cac5fdb636f2f1103de5fe3668597d85350d0d91b1834cc44a83b44`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb570dbf36f38785df2fc8983ad0725e443f375bdd45954981931f0137e26ea6`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 350.2 KB (350227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007ae15590fbd4c2fc97f92a5fd9f4bbee82f5e8d9da82ac218b4d5002f1a50d`  
		Last Modified: Wed, 10 Nov 2021 17:06:52 GMT  
		Size: 5.0 MB (5002607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbf9bfc6a773256d2ac9289665265759ec89a55717d181030cc64c706b5be9a`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92c772d8667daf25c2468b4b149536c7e9fe55a5896143d2e4eba0ca861cede`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca4dbf235f9fc558316b5e2119a389936545de68e74f1ad4acd18c7282eff43`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990cb23cac15d214ca7bac2df486570024c5eb19e214014a88b247c684605ee5`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-windowsservercore-1809`

```console
$ docker pull nats@sha256:b4394e47153d08bdfa6f28759e02e8c37aa9dd5dd759f4a07417b010722de909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:ad29bbedb595a4b3fc815bb5013d6af6deb55f459d016ed438c89308084ab2ae
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711460012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c235da1808d9829823250ce435b177c85ddd1340f0878343bb5e4a1521602a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 14:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:00:40 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:00:41 GMT
ENV NATS_SERVER=2.6.4
# Wed, 10 Nov 2021 17:00:42 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.4/nats-server-v2.6.4-windows-amd64.zip
# Wed, 10 Nov 2021 17:00:43 GMT
ENV NATS_SERVER_SHASUM=e287764a6e8b8ec132dcbe294aa3b96d779678079b7ada20a9bde1b81d5f5bbc
# Wed, 10 Nov 2021 17:01:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Nov 2021 17:02:51 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Nov 2021 17:02:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:02:53 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:02:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:02:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db1ba835bccbdc73ef254c175ca6ae0dc3f0bd759c1910c3b123cfb9613223be`  
		Last Modified: Wed, 10 Nov 2021 16:21:11 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3df59793c391e0eb7e6a2ddb65801dfa94397b370daa52d04e242ba0274e3d`  
		Last Modified: Wed, 10 Nov 2021 17:06:13 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46075e93c469fbc556a996840e6ebbd02849d7518dcb4fb9feed459795714e03`  
		Last Modified: Wed, 10 Nov 2021 17:06:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a915f8554b2287a16ae0945b328b1d7d315b85bd0eda548bfde73d7686a79c`  
		Last Modified: Wed, 10 Nov 2021 17:06:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4eabf66e1adaa7841404639039b5becdbfb43fc726b93da058b0552478b7`  
		Last Modified: Wed, 10 Nov 2021 17:06:11 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f61c483196bb419b4709f89f9df78e12e7f6dab4ad8094a5aee57e021c97eb0`  
		Last Modified: Wed, 10 Nov 2021 17:06:12 GMT  
		Size: 352.3 KB (352252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e167a3b21bfb85235d9775123ea38ca0d4a4c71383ca34a95f3e203f6afddfc9`  
		Last Modified: Wed, 10 Nov 2021 17:06:15 GMT  
		Size: 5.0 MB (4973372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1d94f1b880ea3ea631c3f6e7ddeffdb30d7af80b037e2fdb55db516d018dd5`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.9 KB (1939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb1edd94e1965c70a2bb20e8bac08446704c452ce9342438e89afe2febe9906`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2d4b3e56ee1751a9373a33f5b9d58f1843e22f5ec7cc88f00e6ef369d7d9f7`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfe4f9233effe09d6160c4278ac3a375234523f40d18c3a826dd9e741139be8`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:9c7dc9b1c133e0e5541993a156235c85c3a299c4666f96653fccd33e794fb1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `nats:2.6-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:b8b34e3ddc6569eda34bb1d124a6c427fc3820313fea9618b702a1fe9a281914
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278456953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c0d6fd779bb5acd23d794cab7a62d0a39d140ff94c890f83cdb2814d63808d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 14:32:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:03:18 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:19 GMT
ENV NATS_SERVER=2.6.4
# Wed, 10 Nov 2021 17:03:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.4/nats-server-v2.6.4-windows-amd64.zip
# Wed, 10 Nov 2021 17:03:21 GMT
ENV NATS_SERVER_SHASUM=e287764a6e8b8ec132dcbe294aa3b96d779678079b7ada20a9bde1b81d5f5bbc
# Wed, 10 Nov 2021 17:04:06 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Nov 2021 17:05:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Nov 2021 17:05:31 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:05:32 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:05:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:05:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f6f303e73635c7923a8c64f8938e7ba4c10210fd15a6ce63aa8a62d5a8ea8c0a`  
		Last Modified: Wed, 10 Nov 2021 16:21:33 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5db4062c12269959ca71caf00b70e9baebf61b90c49c74db0e2cdb04cf83e8`  
		Last Modified: Wed, 10 Nov 2021 17:06:51 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4a229bc6e55d797c98ddd01e4d2dde702cc15dfa57f7822427f4b0c7520a1f`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99e43798e75fd46299bad03217fa38c7f0b36023271b5ded075984cbf2df237`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cc0e5c4cac5fdb636f2f1103de5fe3668597d85350d0d91b1834cc44a83b44`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb570dbf36f38785df2fc8983ad0725e443f375bdd45954981931f0137e26ea6`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 350.2 KB (350227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007ae15590fbd4c2fc97f92a5fd9f4bbee82f5e8d9da82ac218b4d5002f1a50d`  
		Last Modified: Wed, 10 Nov 2021 17:06:52 GMT  
		Size: 5.0 MB (5002607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbf9bfc6a773256d2ac9289665265759ec89a55717d181030cc64c706b5be9a`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92c772d8667daf25c2468b4b149536c7e9fe55a5896143d2e4eba0ca861cede`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca4dbf235f9fc558316b5e2119a389936545de68e74f1ad4acd18c7282eff43`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990cb23cac15d214ca7bac2df486570024c5eb19e214014a88b247c684605ee5`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.4`

```console
$ docker pull nats@sha256:2511f2a913b84b7a39dd6411d1dbb19ceae4006a5b8a8de7caadff42898e5d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6.4` - linux; amd64

```console
$ docker pull nats@sha256:ce50109292cf290d1f6559a806f7e6f1b202f4d97678700dbb386b1d6c021964
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa4b152b84f6a4cc5da9b870074d5807b7dc42dbf1f922c1ff7e3059d6ec1be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:f554ccd652a698194b4adc9f60df406473cf580a258d4b425944a529b6b7b718 in /nats-server 
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:00 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe57332791af252fb9335dd0de8a36fe319e51fdde00636db3fee85f1adcb22f`  
		Last Modified: Fri, 05 Nov 2021 01:41:48 GMT  
		Size: 4.6 MB (4573985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc9e783378fba5ac033e418e7db34fb0215aeaa59658adf4924ad46455f261e`  
		Last Modified: Fri, 05 Nov 2021 01:41:47 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.4` - linux; arm variant v6

```console
$ docker pull nats@sha256:a94f85ec4b90db46b3c8d59ed4c35fa9033482dd0e50679775145fc0f2528b20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4236770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bee36fb33e6c4d4ec54bcbd1778a2d3a19dcd7706111ffaf4d1711e916f6dea`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:0e12b4e14d681c94ae627c578bd9cc8a3fc9bec59e0062a772ad0933b7947e38 in /nats-server 
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:03 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a273e90687e1ad496ce74eecec787df7511839c5e770850a184f261ed706fc98`  
		Last Modified: Fri, 05 Nov 2021 01:43:23 GMT  
		Size: 4.2 MB (4236294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6825ddc1425c3e1cfde24c7f0c22b2ad39646ecc4d15d72b1d4769687206880`  
		Last Modified: Fri, 05 Nov 2021 01:43:21 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.4` - linux; arm variant v7

```console
$ docker pull nats@sha256:f2419d713943dd432426211cc6035a9e4cbb06b0cb63d5bca91017fabec840e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf917eacaf24a0ae8a3e5b85a3f2795362e8333bf2b527cb7a5470e0d6cd02b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 04:34:29 GMT
COPY file:f8c8928a8edabd057aa0fe0c8e12f7e68c80845a6af865b9263be1face1e988c in /nats-server 
# Fri, 05 Nov 2021 04:34:30 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 04:34:30 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 04:34:31 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 04:34:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:791f22945fc593348a417c1bdef534cefaa5f1d33df489dddc334de30b713a78`  
		Last Modified: Fri, 05 Nov 2021 04:36:53 GMT  
		Size: 4.2 MB (4232017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3b77fec3826280fc07c1e66876ec0d673939258c3a1dd1320cbc1c3d56b86`  
		Last Modified: Fri, 05 Nov 2021 04:36:50 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.4` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d7e28f91b2fc35b9a0ed2eb9a5e16070e4c2d1dff3f18076e465958b997cce01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089ea638210c9c36041b15aac4bf873a36e3b4bdca7b8e25d6c1b4cc9a274094`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:25:26 GMT
COPY file:2327a2e0254f808bd88c7e734365e343ac6cf801c454a43bf9035cd435fbf8d0 in /nats-server 
# Fri, 05 Nov 2021 01:25:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:25:27 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:25:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:25:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fd5084aec62b3e936e8b267729c530280fe1646e8e9d0e09ef842b74beccff33`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 4.2 MB (4182491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963e399425efdeb20d2700e846b7b3f5c36a5ecef7204cb3fe1476b7b835b2e6`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.4` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:85fc53257b869566352af427b00b1e4eb3be4d9c158473d05955a95358569c49
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107420117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efad7f25530c39976e06f9cd49e8bf8ccf60e961cf32e240771c3311fa8ecb24`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:08 GMT
RUN cmd /S /C #(nop) COPY file:d04f5d85a8b0edde975ace8d01e615862e9872904d6e700eb5be4601ac26087b in C:\nats-server.exe 
# Wed, 10 Nov 2021 17:03:09 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:03:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1d3f90d67d7551be12e9caf53f786235234151f513c0aadc754e5f033e183641`  
		Last Modified: Wed, 10 Nov 2021 17:06:32 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd8a5c6e6a53ddd4f3cdd7ae34bbe9c780fe53c7245304716909425bc26f7bb`  
		Last Modified: Wed, 10 Nov 2021 17:06:31 GMT  
		Size: 4.6 MB (4630764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7360e968604c4d5db8c901e6f52100633b1b227a9ac4c29b0308c424910d02`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c245f1add19193bc4fd407354089b6c244fe2d37ea9a0c7f3b55c4cd0abf678`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4949fe8ad7bd6aa73121e77f2feb4a983ddb04e9a8b68110350fe11533fd556`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5345772ce5a94a4d4b36bcc445defff481e83b2af0be6506b3bb8865ef9de4`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.4-alpine`

```console
$ docker pull nats@sha256:e213dbb5f30da5582cdfb387f306db0e5a756d5cfa0c71ad04012c62c8364299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6.4-alpine` - linux; amd64

```console
$ docker pull nats@sha256:f98772e0f2222bf626db93d8f4dab31459a0d859e901c5554cc076088bdc9f47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b229b8720408fa48ff27cb600c243a0ea34ae241af9a532a457dd1302ad60d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:47:45 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 05:47:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 05:47:49 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 05:47:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 05:47:49 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 05:47:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:47:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2de72945075aec3a93ecb6af12474a3623374dac5d6eb467826bb3f176d9db`  
		Last Modified: Sat, 13 Nov 2021 05:48:24 GMT  
		Size: 4.9 MB (4856278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a7e2c9925a779c559f1381de66066f54c7545dd547ab50f181fdf5bad8b76a`  
		Last Modified: Sat, 13 Nov 2021 05:48:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d123a218501888dc051dc9935a6248b5dc7f0ddad4256c03157e4ea9a4f76af6`  
		Last Modified: Sat, 13 Nov 2021 05:48:23 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.4-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:21253e09b5390b390f4a098fed97b8bce94d3c69d0aee847355ba4f5e9cc13ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7154888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3b3aae48860f1adc793dd60464e9b29d707ac7c543ae92201954544d2847a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 03:04:03 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 03:04:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 03:04:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 03:04:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 03:04:09 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 03:04:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 03:04:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f8239d892b947974d364086747c970b38caaebc528256b37602cbdda9d832`  
		Last Modified: Sat, 13 Nov 2021 03:06:15 GMT  
		Size: 4.5 MB (4518522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8850b565bedb3a41ba36fa532b68d4c035cb73bde2cc2fe456a21cff33f105`  
		Last Modified: Sat, 13 Nov 2021 03:06:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b231dc9db1099c1f0e27d1e668c4c7f7ba23cf94fd95e1edf541ae73ec20eabc`  
		Last Modified: Sat, 13 Nov 2021 03:06:13 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.4-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:927653b6f646dceb6d518c8d58652ae16f07a585f56e2083b8dc640aa54032bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6952724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed121c45beb860b69d68c3e2e94a2ac7015107c8968ea2a40307dc587a0756c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 10:49:53 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 10:49:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 10:49:59 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 10:49:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 10:50:00 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 10:50:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 10:50:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7667eb269dc08efac3da01b8675c36b733dbbe274c782a02e4a86b8361d5b942`  
		Last Modified: Sat, 13 Nov 2021 10:52:16 GMT  
		Size: 4.5 MB (4513136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e575668b5d7e7f7152f80542c775ccba3f377141e747e329fb23896bfe23e9`  
		Last Modified: Sat, 13 Nov 2021 10:52:14 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528edb88e91f872a79a50cc2def03d40caacfed6b26567bb649719c78bcadf70`  
		Last Modified: Sat, 13 Nov 2021 10:52:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.4-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb0858f816f57a2924dbf3c42b77a5601301f210b6a1f33c04b97bb399e76610
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb6a42e1013c13029a69794fd8a6f185e0fedd050fbb50e18fd15650344c8e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:53:10 GMT
ENV NATS_SERVER=2.6.4
# Fri, 12 Nov 2021 17:53:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 12 Nov 2021 17:53:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 12 Nov 2021 17:53:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Nov 2021 17:53:17 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Nov 2021 17:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 17:53:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b88cb6acca7834e23464b3b30fde201b2ccc92123018a6780943e447dbf390`  
		Last Modified: Fri, 12 Nov 2021 17:54:17 GMT  
		Size: 4.5 MB (4467169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41bb7b84481f686821765af47edff89c043129ad18d2fb7ff6946b5b9b9501a8`  
		Last Modified: Fri, 12 Nov 2021 17:54:16 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dced30908382b5bc20e0ba23d2a27c9af4578273423b5d10399b70774b3f4571`  
		Last Modified: Fri, 12 Nov 2021 17:54:16 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.4-alpine3.14`

```console
$ docker pull nats@sha256:e213dbb5f30da5582cdfb387f306db0e5a756d5cfa0c71ad04012c62c8364299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6.4-alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:f98772e0f2222bf626db93d8f4dab31459a0d859e901c5554cc076088bdc9f47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b229b8720408fa48ff27cb600c243a0ea34ae241af9a532a457dd1302ad60d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:47:45 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 05:47:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 05:47:49 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 05:47:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 05:47:49 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 05:47:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:47:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2de72945075aec3a93ecb6af12474a3623374dac5d6eb467826bb3f176d9db`  
		Last Modified: Sat, 13 Nov 2021 05:48:24 GMT  
		Size: 4.9 MB (4856278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a7e2c9925a779c559f1381de66066f54c7545dd547ab50f181fdf5bad8b76a`  
		Last Modified: Sat, 13 Nov 2021 05:48:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d123a218501888dc051dc9935a6248b5dc7f0ddad4256c03157e4ea9a4f76af6`  
		Last Modified: Sat, 13 Nov 2021 05:48:23 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.4-alpine3.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:21253e09b5390b390f4a098fed97b8bce94d3c69d0aee847355ba4f5e9cc13ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7154888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3b3aae48860f1adc793dd60464e9b29d707ac7c543ae92201954544d2847a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 03:04:03 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 03:04:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 03:04:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 03:04:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 03:04:09 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 03:04:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 03:04:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f8239d892b947974d364086747c970b38caaebc528256b37602cbdda9d832`  
		Last Modified: Sat, 13 Nov 2021 03:06:15 GMT  
		Size: 4.5 MB (4518522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8850b565bedb3a41ba36fa532b68d4c035cb73bde2cc2fe456a21cff33f105`  
		Last Modified: Sat, 13 Nov 2021 03:06:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b231dc9db1099c1f0e27d1e668c4c7f7ba23cf94fd95e1edf541ae73ec20eabc`  
		Last Modified: Sat, 13 Nov 2021 03:06:13 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.4-alpine3.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:927653b6f646dceb6d518c8d58652ae16f07a585f56e2083b8dc640aa54032bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6952724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed121c45beb860b69d68c3e2e94a2ac7015107c8968ea2a40307dc587a0756c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 10:49:53 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 10:49:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 10:49:59 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 10:49:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 10:50:00 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 10:50:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 10:50:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7667eb269dc08efac3da01b8675c36b733dbbe274c782a02e4a86b8361d5b942`  
		Last Modified: Sat, 13 Nov 2021 10:52:16 GMT  
		Size: 4.5 MB (4513136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e575668b5d7e7f7152f80542c775ccba3f377141e747e329fb23896bfe23e9`  
		Last Modified: Sat, 13 Nov 2021 10:52:14 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528edb88e91f872a79a50cc2def03d40caacfed6b26567bb649719c78bcadf70`  
		Last Modified: Sat, 13 Nov 2021 10:52:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.4-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb0858f816f57a2924dbf3c42b77a5601301f210b6a1f33c04b97bb399e76610
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb6a42e1013c13029a69794fd8a6f185e0fedd050fbb50e18fd15650344c8e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:53:10 GMT
ENV NATS_SERVER=2.6.4
# Fri, 12 Nov 2021 17:53:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 12 Nov 2021 17:53:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 12 Nov 2021 17:53:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Nov 2021 17:53:17 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Nov 2021 17:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 17:53:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b88cb6acca7834e23464b3b30fde201b2ccc92123018a6780943e447dbf390`  
		Last Modified: Fri, 12 Nov 2021 17:54:17 GMT  
		Size: 4.5 MB (4467169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41bb7b84481f686821765af47edff89c043129ad18d2fb7ff6946b5b9b9501a8`  
		Last Modified: Fri, 12 Nov 2021 17:54:16 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dced30908382b5bc20e0ba23d2a27c9af4578273423b5d10399b70774b3f4571`  
		Last Modified: Fri, 12 Nov 2021 17:54:16 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.4-linux`

```console
$ docker pull nats@sha256:bc46b51540ff5a3d27c3cb3cb61878d610144d728bd3c8836244b063a96b1601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6.4-linux` - linux; amd64

```console
$ docker pull nats@sha256:ce50109292cf290d1f6559a806f7e6f1b202f4d97678700dbb386b1d6c021964
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa4b152b84f6a4cc5da9b870074d5807b7dc42dbf1f922c1ff7e3059d6ec1be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:f554ccd652a698194b4adc9f60df406473cf580a258d4b425944a529b6b7b718 in /nats-server 
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:00 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe57332791af252fb9335dd0de8a36fe319e51fdde00636db3fee85f1adcb22f`  
		Last Modified: Fri, 05 Nov 2021 01:41:48 GMT  
		Size: 4.6 MB (4573985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc9e783378fba5ac033e418e7db34fb0215aeaa59658adf4924ad46455f261e`  
		Last Modified: Fri, 05 Nov 2021 01:41:47 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.4-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:a94f85ec4b90db46b3c8d59ed4c35fa9033482dd0e50679775145fc0f2528b20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4236770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bee36fb33e6c4d4ec54bcbd1778a2d3a19dcd7706111ffaf4d1711e916f6dea`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:0e12b4e14d681c94ae627c578bd9cc8a3fc9bec59e0062a772ad0933b7947e38 in /nats-server 
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:03 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a273e90687e1ad496ce74eecec787df7511839c5e770850a184f261ed706fc98`  
		Last Modified: Fri, 05 Nov 2021 01:43:23 GMT  
		Size: 4.2 MB (4236294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6825ddc1425c3e1cfde24c7f0c22b2ad39646ecc4d15d72b1d4769687206880`  
		Last Modified: Fri, 05 Nov 2021 01:43:21 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.4-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:f2419d713943dd432426211cc6035a9e4cbb06b0cb63d5bca91017fabec840e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf917eacaf24a0ae8a3e5b85a3f2795362e8333bf2b527cb7a5470e0d6cd02b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 04:34:29 GMT
COPY file:f8c8928a8edabd057aa0fe0c8e12f7e68c80845a6af865b9263be1face1e988c in /nats-server 
# Fri, 05 Nov 2021 04:34:30 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 04:34:30 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 04:34:31 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 04:34:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:791f22945fc593348a417c1bdef534cefaa5f1d33df489dddc334de30b713a78`  
		Last Modified: Fri, 05 Nov 2021 04:36:53 GMT  
		Size: 4.2 MB (4232017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3b77fec3826280fc07c1e66876ec0d673939258c3a1dd1320cbc1c3d56b86`  
		Last Modified: Fri, 05 Nov 2021 04:36:50 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.4-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d7e28f91b2fc35b9a0ed2eb9a5e16070e4c2d1dff3f18076e465958b997cce01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089ea638210c9c36041b15aac4bf873a36e3b4bdca7b8e25d6c1b4cc9a274094`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:25:26 GMT
COPY file:2327a2e0254f808bd88c7e734365e343ac6cf801c454a43bf9035cd435fbf8d0 in /nats-server 
# Fri, 05 Nov 2021 01:25:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:25:27 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:25:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:25:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fd5084aec62b3e936e8b267729c530280fe1646e8e9d0e09ef842b74beccff33`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 4.2 MB (4182491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963e399425efdeb20d2700e846b7b3f5c36a5ecef7204cb3fe1476b7b835b2e6`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.4-nanoserver`

```console
$ docker pull nats@sha256:ec6b3505bf01f1bdcd96d7f858771ad6e53c16075defda5d8046c83998c3a251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6.4-nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:85fc53257b869566352af427b00b1e4eb3be4d9c158473d05955a95358569c49
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107420117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efad7f25530c39976e06f9cd49e8bf8ccf60e961cf32e240771c3311fa8ecb24`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:08 GMT
RUN cmd /S /C #(nop) COPY file:d04f5d85a8b0edde975ace8d01e615862e9872904d6e700eb5be4601ac26087b in C:\nats-server.exe 
# Wed, 10 Nov 2021 17:03:09 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:03:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1d3f90d67d7551be12e9caf53f786235234151f513c0aadc754e5f033e183641`  
		Last Modified: Wed, 10 Nov 2021 17:06:32 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd8a5c6e6a53ddd4f3cdd7ae34bbe9c780fe53c7245304716909425bc26f7bb`  
		Last Modified: Wed, 10 Nov 2021 17:06:31 GMT  
		Size: 4.6 MB (4630764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7360e968604c4d5db8c901e6f52100633b1b227a9ac4c29b0308c424910d02`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c245f1add19193bc4fd407354089b6c244fe2d37ea9a0c7f3b55c4cd0abf678`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4949fe8ad7bd6aa73121e77f2feb4a983ddb04e9a8b68110350fe11533fd556`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5345772ce5a94a4d4b36bcc445defff481e83b2af0be6506b3bb8865ef9de4`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.4-nanoserver-1809`

```console
$ docker pull nats@sha256:ec6b3505bf01f1bdcd96d7f858771ad6e53c16075defda5d8046c83998c3a251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6.4-nanoserver-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:85fc53257b869566352af427b00b1e4eb3be4d9c158473d05955a95358569c49
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107420117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efad7f25530c39976e06f9cd49e8bf8ccf60e961cf32e240771c3311fa8ecb24`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:08 GMT
RUN cmd /S /C #(nop) COPY file:d04f5d85a8b0edde975ace8d01e615862e9872904d6e700eb5be4601ac26087b in C:\nats-server.exe 
# Wed, 10 Nov 2021 17:03:09 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:03:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1d3f90d67d7551be12e9caf53f786235234151f513c0aadc754e5f033e183641`  
		Last Modified: Wed, 10 Nov 2021 17:06:32 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd8a5c6e6a53ddd4f3cdd7ae34bbe9c780fe53c7245304716909425bc26f7bb`  
		Last Modified: Wed, 10 Nov 2021 17:06:31 GMT  
		Size: 4.6 MB (4630764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7360e968604c4d5db8c901e6f52100633b1b227a9ac4c29b0308c424910d02`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c245f1add19193bc4fd407354089b6c244fe2d37ea9a0c7f3b55c4cd0abf678`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4949fe8ad7bd6aa73121e77f2feb4a983ddb04e9a8b68110350fe11533fd556`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5345772ce5a94a4d4b36bcc445defff481e83b2af0be6506b3bb8865ef9de4`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.4-scratch`

```console
$ docker pull nats@sha256:bc46b51540ff5a3d27c3cb3cb61878d610144d728bd3c8836244b063a96b1601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6.4-scratch` - linux; amd64

```console
$ docker pull nats@sha256:ce50109292cf290d1f6559a806f7e6f1b202f4d97678700dbb386b1d6c021964
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa4b152b84f6a4cc5da9b870074d5807b7dc42dbf1f922c1ff7e3059d6ec1be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:f554ccd652a698194b4adc9f60df406473cf580a258d4b425944a529b6b7b718 in /nats-server 
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:00 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe57332791af252fb9335dd0de8a36fe319e51fdde00636db3fee85f1adcb22f`  
		Last Modified: Fri, 05 Nov 2021 01:41:48 GMT  
		Size: 4.6 MB (4573985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc9e783378fba5ac033e418e7db34fb0215aeaa59658adf4924ad46455f261e`  
		Last Modified: Fri, 05 Nov 2021 01:41:47 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.4-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:a94f85ec4b90db46b3c8d59ed4c35fa9033482dd0e50679775145fc0f2528b20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4236770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bee36fb33e6c4d4ec54bcbd1778a2d3a19dcd7706111ffaf4d1711e916f6dea`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:0e12b4e14d681c94ae627c578bd9cc8a3fc9bec59e0062a772ad0933b7947e38 in /nats-server 
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:03 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a273e90687e1ad496ce74eecec787df7511839c5e770850a184f261ed706fc98`  
		Last Modified: Fri, 05 Nov 2021 01:43:23 GMT  
		Size: 4.2 MB (4236294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6825ddc1425c3e1cfde24c7f0c22b2ad39646ecc4d15d72b1d4769687206880`  
		Last Modified: Fri, 05 Nov 2021 01:43:21 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.4-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:f2419d713943dd432426211cc6035a9e4cbb06b0cb63d5bca91017fabec840e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf917eacaf24a0ae8a3e5b85a3f2795362e8333bf2b527cb7a5470e0d6cd02b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 04:34:29 GMT
COPY file:f8c8928a8edabd057aa0fe0c8e12f7e68c80845a6af865b9263be1face1e988c in /nats-server 
# Fri, 05 Nov 2021 04:34:30 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 04:34:30 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 04:34:31 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 04:34:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:791f22945fc593348a417c1bdef534cefaa5f1d33df489dddc334de30b713a78`  
		Last Modified: Fri, 05 Nov 2021 04:36:53 GMT  
		Size: 4.2 MB (4232017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3b77fec3826280fc07c1e66876ec0d673939258c3a1dd1320cbc1c3d56b86`  
		Last Modified: Fri, 05 Nov 2021 04:36:50 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.4-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d7e28f91b2fc35b9a0ed2eb9a5e16070e4c2d1dff3f18076e465958b997cce01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089ea638210c9c36041b15aac4bf873a36e3b4bdca7b8e25d6c1b4cc9a274094`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:25:26 GMT
COPY file:2327a2e0254f808bd88c7e734365e343ac6cf801c454a43bf9035cd435fbf8d0 in /nats-server 
# Fri, 05 Nov 2021 01:25:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:25:27 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:25:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:25:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fd5084aec62b3e936e8b267729c530280fe1646e8e9d0e09ef842b74beccff33`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 4.2 MB (4182491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963e399425efdeb20d2700e846b7b3f5c36a5ecef7204cb3fe1476b7b835b2e6`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.4-windowsservercore`

```console
$ docker pull nats@sha256:c5b7ed794ed1ea3bc9973244e683bd5dfb902e0bab7882855f15fb1696802bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `nats:2.6.4-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:ad29bbedb595a4b3fc815bb5013d6af6deb55f459d016ed438c89308084ab2ae
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711460012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c235da1808d9829823250ce435b177c85ddd1340f0878343bb5e4a1521602a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 14:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:00:40 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:00:41 GMT
ENV NATS_SERVER=2.6.4
# Wed, 10 Nov 2021 17:00:42 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.4/nats-server-v2.6.4-windows-amd64.zip
# Wed, 10 Nov 2021 17:00:43 GMT
ENV NATS_SERVER_SHASUM=e287764a6e8b8ec132dcbe294aa3b96d779678079b7ada20a9bde1b81d5f5bbc
# Wed, 10 Nov 2021 17:01:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Nov 2021 17:02:51 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Nov 2021 17:02:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:02:53 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:02:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:02:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db1ba835bccbdc73ef254c175ca6ae0dc3f0bd759c1910c3b123cfb9613223be`  
		Last Modified: Wed, 10 Nov 2021 16:21:11 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3df59793c391e0eb7e6a2ddb65801dfa94397b370daa52d04e242ba0274e3d`  
		Last Modified: Wed, 10 Nov 2021 17:06:13 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46075e93c469fbc556a996840e6ebbd02849d7518dcb4fb9feed459795714e03`  
		Last Modified: Wed, 10 Nov 2021 17:06:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a915f8554b2287a16ae0945b328b1d7d315b85bd0eda548bfde73d7686a79c`  
		Last Modified: Wed, 10 Nov 2021 17:06:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4eabf66e1adaa7841404639039b5becdbfb43fc726b93da058b0552478b7`  
		Last Modified: Wed, 10 Nov 2021 17:06:11 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f61c483196bb419b4709f89f9df78e12e7f6dab4ad8094a5aee57e021c97eb0`  
		Last Modified: Wed, 10 Nov 2021 17:06:12 GMT  
		Size: 352.3 KB (352252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e167a3b21bfb85235d9775123ea38ca0d4a4c71383ca34a95f3e203f6afddfc9`  
		Last Modified: Wed, 10 Nov 2021 17:06:15 GMT  
		Size: 5.0 MB (4973372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1d94f1b880ea3ea631c3f6e7ddeffdb30d7af80b037e2fdb55db516d018dd5`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.9 KB (1939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb1edd94e1965c70a2bb20e8bac08446704c452ce9342438e89afe2febe9906`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2d4b3e56ee1751a9373a33f5b9d58f1843e22f5ec7cc88f00e6ef369d7d9f7`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfe4f9233effe09d6160c4278ac3a375234523f40d18c3a826dd9e741139be8`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.4-windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:b8b34e3ddc6569eda34bb1d124a6c427fc3820313fea9618b702a1fe9a281914
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278456953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c0d6fd779bb5acd23d794cab7a62d0a39d140ff94c890f83cdb2814d63808d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 14:32:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:03:18 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:19 GMT
ENV NATS_SERVER=2.6.4
# Wed, 10 Nov 2021 17:03:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.4/nats-server-v2.6.4-windows-amd64.zip
# Wed, 10 Nov 2021 17:03:21 GMT
ENV NATS_SERVER_SHASUM=e287764a6e8b8ec132dcbe294aa3b96d779678079b7ada20a9bde1b81d5f5bbc
# Wed, 10 Nov 2021 17:04:06 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Nov 2021 17:05:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Nov 2021 17:05:31 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:05:32 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:05:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:05:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f6f303e73635c7923a8c64f8938e7ba4c10210fd15a6ce63aa8a62d5a8ea8c0a`  
		Last Modified: Wed, 10 Nov 2021 16:21:33 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5db4062c12269959ca71caf00b70e9baebf61b90c49c74db0e2cdb04cf83e8`  
		Last Modified: Wed, 10 Nov 2021 17:06:51 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4a229bc6e55d797c98ddd01e4d2dde702cc15dfa57f7822427f4b0c7520a1f`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99e43798e75fd46299bad03217fa38c7f0b36023271b5ded075984cbf2df237`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cc0e5c4cac5fdb636f2f1103de5fe3668597d85350d0d91b1834cc44a83b44`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb570dbf36f38785df2fc8983ad0725e443f375bdd45954981931f0137e26ea6`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 350.2 KB (350227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007ae15590fbd4c2fc97f92a5fd9f4bbee82f5e8d9da82ac218b4d5002f1a50d`  
		Last Modified: Wed, 10 Nov 2021 17:06:52 GMT  
		Size: 5.0 MB (5002607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbf9bfc6a773256d2ac9289665265759ec89a55717d181030cc64c706b5be9a`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92c772d8667daf25c2468b4b149536c7e9fe55a5896143d2e4eba0ca861cede`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca4dbf235f9fc558316b5e2119a389936545de68e74f1ad4acd18c7282eff43`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990cb23cac15d214ca7bac2df486570024c5eb19e214014a88b247c684605ee5`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.4-windowsservercore-1809`

```console
$ docker pull nats@sha256:b4394e47153d08bdfa6f28759e02e8c37aa9dd5dd759f4a07417b010722de909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6.4-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:ad29bbedb595a4b3fc815bb5013d6af6deb55f459d016ed438c89308084ab2ae
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711460012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c235da1808d9829823250ce435b177c85ddd1340f0878343bb5e4a1521602a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 14:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:00:40 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:00:41 GMT
ENV NATS_SERVER=2.6.4
# Wed, 10 Nov 2021 17:00:42 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.4/nats-server-v2.6.4-windows-amd64.zip
# Wed, 10 Nov 2021 17:00:43 GMT
ENV NATS_SERVER_SHASUM=e287764a6e8b8ec132dcbe294aa3b96d779678079b7ada20a9bde1b81d5f5bbc
# Wed, 10 Nov 2021 17:01:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Nov 2021 17:02:51 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Nov 2021 17:02:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:02:53 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:02:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:02:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db1ba835bccbdc73ef254c175ca6ae0dc3f0bd759c1910c3b123cfb9613223be`  
		Last Modified: Wed, 10 Nov 2021 16:21:11 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3df59793c391e0eb7e6a2ddb65801dfa94397b370daa52d04e242ba0274e3d`  
		Last Modified: Wed, 10 Nov 2021 17:06:13 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46075e93c469fbc556a996840e6ebbd02849d7518dcb4fb9feed459795714e03`  
		Last Modified: Wed, 10 Nov 2021 17:06:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a915f8554b2287a16ae0945b328b1d7d315b85bd0eda548bfde73d7686a79c`  
		Last Modified: Wed, 10 Nov 2021 17:06:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4eabf66e1adaa7841404639039b5becdbfb43fc726b93da058b0552478b7`  
		Last Modified: Wed, 10 Nov 2021 17:06:11 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f61c483196bb419b4709f89f9df78e12e7f6dab4ad8094a5aee57e021c97eb0`  
		Last Modified: Wed, 10 Nov 2021 17:06:12 GMT  
		Size: 352.3 KB (352252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e167a3b21bfb85235d9775123ea38ca0d4a4c71383ca34a95f3e203f6afddfc9`  
		Last Modified: Wed, 10 Nov 2021 17:06:15 GMT  
		Size: 5.0 MB (4973372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1d94f1b880ea3ea631c3f6e7ddeffdb30d7af80b037e2fdb55db516d018dd5`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.9 KB (1939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb1edd94e1965c70a2bb20e8bac08446704c452ce9342438e89afe2febe9906`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2d4b3e56ee1751a9373a33f5b9d58f1843e22f5ec7cc88f00e6ef369d7d9f7`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfe4f9233effe09d6160c4278ac3a375234523f40d18c3a826dd9e741139be8`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.4-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:9c7dc9b1c133e0e5541993a156235c85c3a299c4666f96653fccd33e794fb1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `nats:2.6.4-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:b8b34e3ddc6569eda34bb1d124a6c427fc3820313fea9618b702a1fe9a281914
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278456953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c0d6fd779bb5acd23d794cab7a62d0a39d140ff94c890f83cdb2814d63808d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 14:32:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:03:18 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:19 GMT
ENV NATS_SERVER=2.6.4
# Wed, 10 Nov 2021 17:03:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.4/nats-server-v2.6.4-windows-amd64.zip
# Wed, 10 Nov 2021 17:03:21 GMT
ENV NATS_SERVER_SHASUM=e287764a6e8b8ec132dcbe294aa3b96d779678079b7ada20a9bde1b81d5f5bbc
# Wed, 10 Nov 2021 17:04:06 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Nov 2021 17:05:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Nov 2021 17:05:31 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:05:32 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:05:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:05:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f6f303e73635c7923a8c64f8938e7ba4c10210fd15a6ce63aa8a62d5a8ea8c0a`  
		Last Modified: Wed, 10 Nov 2021 16:21:33 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5db4062c12269959ca71caf00b70e9baebf61b90c49c74db0e2cdb04cf83e8`  
		Last Modified: Wed, 10 Nov 2021 17:06:51 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4a229bc6e55d797c98ddd01e4d2dde702cc15dfa57f7822427f4b0c7520a1f`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99e43798e75fd46299bad03217fa38c7f0b36023271b5ded075984cbf2df237`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cc0e5c4cac5fdb636f2f1103de5fe3668597d85350d0d91b1834cc44a83b44`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb570dbf36f38785df2fc8983ad0725e443f375bdd45954981931f0137e26ea6`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 350.2 KB (350227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007ae15590fbd4c2fc97f92a5fd9f4bbee82f5e8d9da82ac218b4d5002f1a50d`  
		Last Modified: Wed, 10 Nov 2021 17:06:52 GMT  
		Size: 5.0 MB (5002607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbf9bfc6a773256d2ac9289665265759ec89a55717d181030cc64c706b5be9a`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92c772d8667daf25c2468b4b149536c7e9fe55a5896143d2e4eba0ca861cede`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca4dbf235f9fc558316b5e2119a389936545de68e74f1ad4acd18c7282eff43`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990cb23cac15d214ca7bac2df486570024c5eb19e214014a88b247c684605ee5`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:e213dbb5f30da5582cdfb387f306db0e5a756d5cfa0c71ad04012c62c8364299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:f98772e0f2222bf626db93d8f4dab31459a0d859e901c5554cc076088bdc9f47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b229b8720408fa48ff27cb600c243a0ea34ae241af9a532a457dd1302ad60d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:47:45 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 05:47:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 05:47:49 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 05:47:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 05:47:49 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 05:47:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:47:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2de72945075aec3a93ecb6af12474a3623374dac5d6eb467826bb3f176d9db`  
		Last Modified: Sat, 13 Nov 2021 05:48:24 GMT  
		Size: 4.9 MB (4856278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a7e2c9925a779c559f1381de66066f54c7545dd547ab50f181fdf5bad8b76a`  
		Last Modified: Sat, 13 Nov 2021 05:48:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d123a218501888dc051dc9935a6248b5dc7f0ddad4256c03157e4ea9a4f76af6`  
		Last Modified: Sat, 13 Nov 2021 05:48:23 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:21253e09b5390b390f4a098fed97b8bce94d3c69d0aee847355ba4f5e9cc13ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7154888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3b3aae48860f1adc793dd60464e9b29d707ac7c543ae92201954544d2847a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 03:04:03 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 03:04:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 03:04:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 03:04:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 03:04:09 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 03:04:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 03:04:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f8239d892b947974d364086747c970b38caaebc528256b37602cbdda9d832`  
		Last Modified: Sat, 13 Nov 2021 03:06:15 GMT  
		Size: 4.5 MB (4518522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8850b565bedb3a41ba36fa532b68d4c035cb73bde2cc2fe456a21cff33f105`  
		Last Modified: Sat, 13 Nov 2021 03:06:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b231dc9db1099c1f0e27d1e668c4c7f7ba23cf94fd95e1edf541ae73ec20eabc`  
		Last Modified: Sat, 13 Nov 2021 03:06:13 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:927653b6f646dceb6d518c8d58652ae16f07a585f56e2083b8dc640aa54032bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6952724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed121c45beb860b69d68c3e2e94a2ac7015107c8968ea2a40307dc587a0756c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 10:49:53 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 10:49:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 10:49:59 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 10:49:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 10:50:00 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 10:50:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 10:50:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7667eb269dc08efac3da01b8675c36b733dbbe274c782a02e4a86b8361d5b942`  
		Last Modified: Sat, 13 Nov 2021 10:52:16 GMT  
		Size: 4.5 MB (4513136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e575668b5d7e7f7152f80542c775ccba3f377141e747e329fb23896bfe23e9`  
		Last Modified: Sat, 13 Nov 2021 10:52:14 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528edb88e91f872a79a50cc2def03d40caacfed6b26567bb649719c78bcadf70`  
		Last Modified: Sat, 13 Nov 2021 10:52:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb0858f816f57a2924dbf3c42b77a5601301f210b6a1f33c04b97bb399e76610
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb6a42e1013c13029a69794fd8a6f185e0fedd050fbb50e18fd15650344c8e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:53:10 GMT
ENV NATS_SERVER=2.6.4
# Fri, 12 Nov 2021 17:53:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 12 Nov 2021 17:53:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 12 Nov 2021 17:53:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Nov 2021 17:53:17 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Nov 2021 17:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 17:53:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b88cb6acca7834e23464b3b30fde201b2ccc92123018a6780943e447dbf390`  
		Last Modified: Fri, 12 Nov 2021 17:54:17 GMT  
		Size: 4.5 MB (4467169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41bb7b84481f686821765af47edff89c043129ad18d2fb7ff6946b5b9b9501a8`  
		Last Modified: Fri, 12 Nov 2021 17:54:16 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dced30908382b5bc20e0ba23d2a27c9af4578273423b5d10399b70774b3f4571`  
		Last Modified: Fri, 12 Nov 2021 17:54:16 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.14`

```console
$ docker pull nats@sha256:e213dbb5f30da5582cdfb387f306db0e5a756d5cfa0c71ad04012c62c8364299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:f98772e0f2222bf626db93d8f4dab31459a0d859e901c5554cc076088bdc9f47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b229b8720408fa48ff27cb600c243a0ea34ae241af9a532a457dd1302ad60d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:47:45 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 05:47:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 05:47:49 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 05:47:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 05:47:49 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 05:47:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:47:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2de72945075aec3a93ecb6af12474a3623374dac5d6eb467826bb3f176d9db`  
		Last Modified: Sat, 13 Nov 2021 05:48:24 GMT  
		Size: 4.9 MB (4856278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a7e2c9925a779c559f1381de66066f54c7545dd547ab50f181fdf5bad8b76a`  
		Last Modified: Sat, 13 Nov 2021 05:48:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d123a218501888dc051dc9935a6248b5dc7f0ddad4256c03157e4ea9a4f76af6`  
		Last Modified: Sat, 13 Nov 2021 05:48:23 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:21253e09b5390b390f4a098fed97b8bce94d3c69d0aee847355ba4f5e9cc13ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7154888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3b3aae48860f1adc793dd60464e9b29d707ac7c543ae92201954544d2847a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 03:04:03 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 03:04:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 03:04:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 03:04:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 03:04:09 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 03:04:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 03:04:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f8239d892b947974d364086747c970b38caaebc528256b37602cbdda9d832`  
		Last Modified: Sat, 13 Nov 2021 03:06:15 GMT  
		Size: 4.5 MB (4518522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8850b565bedb3a41ba36fa532b68d4c035cb73bde2cc2fe456a21cff33f105`  
		Last Modified: Sat, 13 Nov 2021 03:06:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b231dc9db1099c1f0e27d1e668c4c7f7ba23cf94fd95e1edf541ae73ec20eabc`  
		Last Modified: Sat, 13 Nov 2021 03:06:13 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:927653b6f646dceb6d518c8d58652ae16f07a585f56e2083b8dc640aa54032bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6952724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed121c45beb860b69d68c3e2e94a2ac7015107c8968ea2a40307dc587a0756c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 10:49:53 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 10:49:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 10:49:59 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 10:49:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 10:50:00 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 10:50:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 10:50:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7667eb269dc08efac3da01b8675c36b733dbbe274c782a02e4a86b8361d5b942`  
		Last Modified: Sat, 13 Nov 2021 10:52:16 GMT  
		Size: 4.5 MB (4513136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e575668b5d7e7f7152f80542c775ccba3f377141e747e329fb23896bfe23e9`  
		Last Modified: Sat, 13 Nov 2021 10:52:14 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528edb88e91f872a79a50cc2def03d40caacfed6b26567bb649719c78bcadf70`  
		Last Modified: Sat, 13 Nov 2021 10:52:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb0858f816f57a2924dbf3c42b77a5601301f210b6a1f33c04b97bb399e76610
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb6a42e1013c13029a69794fd8a6f185e0fedd050fbb50e18fd15650344c8e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:53:10 GMT
ENV NATS_SERVER=2.6.4
# Fri, 12 Nov 2021 17:53:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 12 Nov 2021 17:53:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 12 Nov 2021 17:53:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Nov 2021 17:53:17 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Nov 2021 17:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 17:53:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b88cb6acca7834e23464b3b30fde201b2ccc92123018a6780943e447dbf390`  
		Last Modified: Fri, 12 Nov 2021 17:54:17 GMT  
		Size: 4.5 MB (4467169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41bb7b84481f686821765af47edff89c043129ad18d2fb7ff6946b5b9b9501a8`  
		Last Modified: Fri, 12 Nov 2021 17:54:16 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dced30908382b5bc20e0ba23d2a27c9af4578273423b5d10399b70774b3f4571`  
		Last Modified: Fri, 12 Nov 2021 17:54:16 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:2511f2a913b84b7a39dd6411d1dbb19ceae4006a5b8a8de7caadff42898e5d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2300; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:ce50109292cf290d1f6559a806f7e6f1b202f4d97678700dbb386b1d6c021964
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa4b152b84f6a4cc5da9b870074d5807b7dc42dbf1f922c1ff7e3059d6ec1be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:f554ccd652a698194b4adc9f60df406473cf580a258d4b425944a529b6b7b718 in /nats-server 
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:00 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe57332791af252fb9335dd0de8a36fe319e51fdde00636db3fee85f1adcb22f`  
		Last Modified: Fri, 05 Nov 2021 01:41:48 GMT  
		Size: 4.6 MB (4573985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc9e783378fba5ac033e418e7db34fb0215aeaa59658adf4924ad46455f261e`  
		Last Modified: Fri, 05 Nov 2021 01:41:47 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:a94f85ec4b90db46b3c8d59ed4c35fa9033482dd0e50679775145fc0f2528b20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4236770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bee36fb33e6c4d4ec54bcbd1778a2d3a19dcd7706111ffaf4d1711e916f6dea`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:0e12b4e14d681c94ae627c578bd9cc8a3fc9bec59e0062a772ad0933b7947e38 in /nats-server 
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:03 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a273e90687e1ad496ce74eecec787df7511839c5e770850a184f261ed706fc98`  
		Last Modified: Fri, 05 Nov 2021 01:43:23 GMT  
		Size: 4.2 MB (4236294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6825ddc1425c3e1cfde24c7f0c22b2ad39646ecc4d15d72b1d4769687206880`  
		Last Modified: Fri, 05 Nov 2021 01:43:21 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:f2419d713943dd432426211cc6035a9e4cbb06b0cb63d5bca91017fabec840e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf917eacaf24a0ae8a3e5b85a3f2795362e8333bf2b527cb7a5470e0d6cd02b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 04:34:29 GMT
COPY file:f8c8928a8edabd057aa0fe0c8e12f7e68c80845a6af865b9263be1face1e988c in /nats-server 
# Fri, 05 Nov 2021 04:34:30 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 04:34:30 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 04:34:31 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 04:34:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:791f22945fc593348a417c1bdef534cefaa5f1d33df489dddc334de30b713a78`  
		Last Modified: Fri, 05 Nov 2021 04:36:53 GMT  
		Size: 4.2 MB (4232017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3b77fec3826280fc07c1e66876ec0d673939258c3a1dd1320cbc1c3d56b86`  
		Last Modified: Fri, 05 Nov 2021 04:36:50 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d7e28f91b2fc35b9a0ed2eb9a5e16070e4c2d1dff3f18076e465958b997cce01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089ea638210c9c36041b15aac4bf873a36e3b4bdca7b8e25d6c1b4cc9a274094`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:25:26 GMT
COPY file:2327a2e0254f808bd88c7e734365e343ac6cf801c454a43bf9035cd435fbf8d0 in /nats-server 
# Fri, 05 Nov 2021 01:25:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:25:27 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:25:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:25:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fd5084aec62b3e936e8b267729c530280fe1646e8e9d0e09ef842b74beccff33`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 4.2 MB (4182491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963e399425efdeb20d2700e846b7b3f5c36a5ecef7204cb3fe1476b7b835b2e6`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:85fc53257b869566352af427b00b1e4eb3be4d9c158473d05955a95358569c49
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107420117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efad7f25530c39976e06f9cd49e8bf8ccf60e961cf32e240771c3311fa8ecb24`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:08 GMT
RUN cmd /S /C #(nop) COPY file:d04f5d85a8b0edde975ace8d01e615862e9872904d6e700eb5be4601ac26087b in C:\nats-server.exe 
# Wed, 10 Nov 2021 17:03:09 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:03:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1d3f90d67d7551be12e9caf53f786235234151f513c0aadc754e5f033e183641`  
		Last Modified: Wed, 10 Nov 2021 17:06:32 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd8a5c6e6a53ddd4f3cdd7ae34bbe9c780fe53c7245304716909425bc26f7bb`  
		Last Modified: Wed, 10 Nov 2021 17:06:31 GMT  
		Size: 4.6 MB (4630764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7360e968604c4d5db8c901e6f52100633b1b227a9ac4c29b0308c424910d02`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c245f1add19193bc4fd407354089b6c244fe2d37ea9a0c7f3b55c4cd0abf678`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4949fe8ad7bd6aa73121e77f2feb4a983ddb04e9a8b68110350fe11533fd556`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5345772ce5a94a4d4b36bcc445defff481e83b2af0be6506b3bb8865ef9de4`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:bc46b51540ff5a3d27c3cb3cb61878d610144d728bd3c8836244b063a96b1601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:ce50109292cf290d1f6559a806f7e6f1b202f4d97678700dbb386b1d6c021964
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa4b152b84f6a4cc5da9b870074d5807b7dc42dbf1f922c1ff7e3059d6ec1be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:f554ccd652a698194b4adc9f60df406473cf580a258d4b425944a529b6b7b718 in /nats-server 
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:00 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe57332791af252fb9335dd0de8a36fe319e51fdde00636db3fee85f1adcb22f`  
		Last Modified: Fri, 05 Nov 2021 01:41:48 GMT  
		Size: 4.6 MB (4573985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc9e783378fba5ac033e418e7db34fb0215aeaa59658adf4924ad46455f261e`  
		Last Modified: Fri, 05 Nov 2021 01:41:47 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:a94f85ec4b90db46b3c8d59ed4c35fa9033482dd0e50679775145fc0f2528b20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4236770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bee36fb33e6c4d4ec54bcbd1778a2d3a19dcd7706111ffaf4d1711e916f6dea`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:0e12b4e14d681c94ae627c578bd9cc8a3fc9bec59e0062a772ad0933b7947e38 in /nats-server 
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:03 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a273e90687e1ad496ce74eecec787df7511839c5e770850a184f261ed706fc98`  
		Last Modified: Fri, 05 Nov 2021 01:43:23 GMT  
		Size: 4.2 MB (4236294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6825ddc1425c3e1cfde24c7f0c22b2ad39646ecc4d15d72b1d4769687206880`  
		Last Modified: Fri, 05 Nov 2021 01:43:21 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:f2419d713943dd432426211cc6035a9e4cbb06b0cb63d5bca91017fabec840e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf917eacaf24a0ae8a3e5b85a3f2795362e8333bf2b527cb7a5470e0d6cd02b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 04:34:29 GMT
COPY file:f8c8928a8edabd057aa0fe0c8e12f7e68c80845a6af865b9263be1face1e988c in /nats-server 
# Fri, 05 Nov 2021 04:34:30 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 04:34:30 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 04:34:31 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 04:34:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:791f22945fc593348a417c1bdef534cefaa5f1d33df489dddc334de30b713a78`  
		Last Modified: Fri, 05 Nov 2021 04:36:53 GMT  
		Size: 4.2 MB (4232017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3b77fec3826280fc07c1e66876ec0d673939258c3a1dd1320cbc1c3d56b86`  
		Last Modified: Fri, 05 Nov 2021 04:36:50 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d7e28f91b2fc35b9a0ed2eb9a5e16070e4c2d1dff3f18076e465958b997cce01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089ea638210c9c36041b15aac4bf873a36e3b4bdca7b8e25d6c1b4cc9a274094`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:25:26 GMT
COPY file:2327a2e0254f808bd88c7e734365e343ac6cf801c454a43bf9035cd435fbf8d0 in /nats-server 
# Fri, 05 Nov 2021 01:25:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:25:27 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:25:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:25:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fd5084aec62b3e936e8b267729c530280fe1646e8e9d0e09ef842b74beccff33`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 4.2 MB (4182491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963e399425efdeb20d2700e846b7b3f5c36a5ecef7204cb3fe1476b7b835b2e6`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:ec6b3505bf01f1bdcd96d7f858771ad6e53c16075defda5d8046c83998c3a251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:85fc53257b869566352af427b00b1e4eb3be4d9c158473d05955a95358569c49
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107420117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efad7f25530c39976e06f9cd49e8bf8ccf60e961cf32e240771c3311fa8ecb24`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:08 GMT
RUN cmd /S /C #(nop) COPY file:d04f5d85a8b0edde975ace8d01e615862e9872904d6e700eb5be4601ac26087b in C:\nats-server.exe 
# Wed, 10 Nov 2021 17:03:09 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:03:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1d3f90d67d7551be12e9caf53f786235234151f513c0aadc754e5f033e183641`  
		Last Modified: Wed, 10 Nov 2021 17:06:32 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd8a5c6e6a53ddd4f3cdd7ae34bbe9c780fe53c7245304716909425bc26f7bb`  
		Last Modified: Wed, 10 Nov 2021 17:06:31 GMT  
		Size: 4.6 MB (4630764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7360e968604c4d5db8c901e6f52100633b1b227a9ac4c29b0308c424910d02`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c245f1add19193bc4fd407354089b6c244fe2d37ea9a0c7f3b55c4cd0abf678`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4949fe8ad7bd6aa73121e77f2feb4a983ddb04e9a8b68110350fe11533fd556`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5345772ce5a94a4d4b36bcc445defff481e83b2af0be6506b3bb8865ef9de4`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:ec6b3505bf01f1bdcd96d7f858771ad6e53c16075defda5d8046c83998c3a251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:85fc53257b869566352af427b00b1e4eb3be4d9c158473d05955a95358569c49
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107420117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efad7f25530c39976e06f9cd49e8bf8ccf60e961cf32e240771c3311fa8ecb24`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:08 GMT
RUN cmd /S /C #(nop) COPY file:d04f5d85a8b0edde975ace8d01e615862e9872904d6e700eb5be4601ac26087b in C:\nats-server.exe 
# Wed, 10 Nov 2021 17:03:09 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:03:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:03:11 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1d3f90d67d7551be12e9caf53f786235234151f513c0aadc754e5f033e183641`  
		Last Modified: Wed, 10 Nov 2021 17:06:32 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd8a5c6e6a53ddd4f3cdd7ae34bbe9c780fe53c7245304716909425bc26f7bb`  
		Last Modified: Wed, 10 Nov 2021 17:06:31 GMT  
		Size: 4.6 MB (4630764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7360e968604c4d5db8c901e6f52100633b1b227a9ac4c29b0308c424910d02`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c245f1add19193bc4fd407354089b6c244fe2d37ea9a0c7f3b55c4cd0abf678`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4949fe8ad7bd6aa73121e77f2feb4a983ddb04e9a8b68110350fe11533fd556`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5345772ce5a94a4d4b36bcc445defff481e83b2af0be6506b3bb8865ef9de4`  
		Last Modified: Wed, 10 Nov 2021 17:06:30 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:bc46b51540ff5a3d27c3cb3cb61878d610144d728bd3c8836244b063a96b1601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:ce50109292cf290d1f6559a806f7e6f1b202f4d97678700dbb386b1d6c021964
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa4b152b84f6a4cc5da9b870074d5807b7dc42dbf1f922c1ff7e3059d6ec1be`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:f554ccd652a698194b4adc9f60df406473cf580a258d4b425944a529b6b7b718 in /nats-server 
# Fri, 05 Nov 2021 01:41:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:00 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe57332791af252fb9335dd0de8a36fe319e51fdde00636db3fee85f1adcb22f`  
		Last Modified: Fri, 05 Nov 2021 01:41:48 GMT  
		Size: 4.6 MB (4573985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc9e783378fba5ac033e418e7db34fb0215aeaa59658adf4924ad46455f261e`  
		Last Modified: Fri, 05 Nov 2021 01:41:47 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:a94f85ec4b90db46b3c8d59ed4c35fa9033482dd0e50679775145fc0f2528b20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4236770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bee36fb33e6c4d4ec54bcbd1778a2d3a19dcd7706111ffaf4d1711e916f6dea`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:0e12b4e14d681c94ae627c578bd9cc8a3fc9bec59e0062a772ad0933b7947e38 in /nats-server 
# Fri, 05 Nov 2021 01:41:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:41:03 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:41:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:41:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a273e90687e1ad496ce74eecec787df7511839c5e770850a184f261ed706fc98`  
		Last Modified: Fri, 05 Nov 2021 01:43:23 GMT  
		Size: 4.2 MB (4236294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6825ddc1425c3e1cfde24c7f0c22b2ad39646ecc4d15d72b1d4769687206880`  
		Last Modified: Fri, 05 Nov 2021 01:43:21 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:f2419d713943dd432426211cc6035a9e4cbb06b0cb63d5bca91017fabec840e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf917eacaf24a0ae8a3e5b85a3f2795362e8333bf2b527cb7a5470e0d6cd02b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 04:34:29 GMT
COPY file:f8c8928a8edabd057aa0fe0c8e12f7e68c80845a6af865b9263be1face1e988c in /nats-server 
# Fri, 05 Nov 2021 04:34:30 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 04:34:30 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 04:34:31 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 04:34:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:791f22945fc593348a417c1bdef534cefaa5f1d33df489dddc334de30b713a78`  
		Last Modified: Fri, 05 Nov 2021 04:36:53 GMT  
		Size: 4.2 MB (4232017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3b77fec3826280fc07c1e66876ec0d673939258c3a1dd1320cbc1c3d56b86`  
		Last Modified: Fri, 05 Nov 2021 04:36:50 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d7e28f91b2fc35b9a0ed2eb9a5e16070e4c2d1dff3f18076e465958b997cce01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089ea638210c9c36041b15aac4bf873a36e3b4bdca7b8e25d6c1b4cc9a274094`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Nov 2021 01:25:26 GMT
COPY file:2327a2e0254f808bd88c7e734365e343ac6cf801c454a43bf9035cd435fbf8d0 in /nats-server 
# Fri, 05 Nov 2021 01:25:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 05 Nov 2021 01:25:27 GMT
EXPOSE 4222 6222 8222
# Fri, 05 Nov 2021 01:25:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 05 Nov 2021 01:25:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fd5084aec62b3e936e8b267729c530280fe1646e8e9d0e09ef842b74beccff33`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 4.2 MB (4182491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963e399425efdeb20d2700e846b7b3f5c36a5ecef7204cb3fe1476b7b835b2e6`  
		Last Modified: Fri, 05 Nov 2021 01:26:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:c5b7ed794ed1ea3bc9973244e683bd5dfb902e0bab7882855f15fb1696802bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `nats:windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:ad29bbedb595a4b3fc815bb5013d6af6deb55f459d016ed438c89308084ab2ae
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711460012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c235da1808d9829823250ce435b177c85ddd1340f0878343bb5e4a1521602a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 14:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:00:40 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:00:41 GMT
ENV NATS_SERVER=2.6.4
# Wed, 10 Nov 2021 17:00:42 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.4/nats-server-v2.6.4-windows-amd64.zip
# Wed, 10 Nov 2021 17:00:43 GMT
ENV NATS_SERVER_SHASUM=e287764a6e8b8ec132dcbe294aa3b96d779678079b7ada20a9bde1b81d5f5bbc
# Wed, 10 Nov 2021 17:01:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Nov 2021 17:02:51 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Nov 2021 17:02:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:02:53 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:02:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:02:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db1ba835bccbdc73ef254c175ca6ae0dc3f0bd759c1910c3b123cfb9613223be`  
		Last Modified: Wed, 10 Nov 2021 16:21:11 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3df59793c391e0eb7e6a2ddb65801dfa94397b370daa52d04e242ba0274e3d`  
		Last Modified: Wed, 10 Nov 2021 17:06:13 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46075e93c469fbc556a996840e6ebbd02849d7518dcb4fb9feed459795714e03`  
		Last Modified: Wed, 10 Nov 2021 17:06:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a915f8554b2287a16ae0945b328b1d7d315b85bd0eda548bfde73d7686a79c`  
		Last Modified: Wed, 10 Nov 2021 17:06:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4eabf66e1adaa7841404639039b5becdbfb43fc726b93da058b0552478b7`  
		Last Modified: Wed, 10 Nov 2021 17:06:11 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f61c483196bb419b4709f89f9df78e12e7f6dab4ad8094a5aee57e021c97eb0`  
		Last Modified: Wed, 10 Nov 2021 17:06:12 GMT  
		Size: 352.3 KB (352252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e167a3b21bfb85235d9775123ea38ca0d4a4c71383ca34a95f3e203f6afddfc9`  
		Last Modified: Wed, 10 Nov 2021 17:06:15 GMT  
		Size: 5.0 MB (4973372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1d94f1b880ea3ea631c3f6e7ddeffdb30d7af80b037e2fdb55db516d018dd5`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.9 KB (1939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb1edd94e1965c70a2bb20e8bac08446704c452ce9342438e89afe2febe9906`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2d4b3e56ee1751a9373a33f5b9d58f1843e22f5ec7cc88f00e6ef369d7d9f7`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfe4f9233effe09d6160c4278ac3a375234523f40d18c3a826dd9e741139be8`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:b8b34e3ddc6569eda34bb1d124a6c427fc3820313fea9618b702a1fe9a281914
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278456953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c0d6fd779bb5acd23d794cab7a62d0a39d140ff94c890f83cdb2814d63808d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 14:32:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:03:18 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:19 GMT
ENV NATS_SERVER=2.6.4
# Wed, 10 Nov 2021 17:03:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.4/nats-server-v2.6.4-windows-amd64.zip
# Wed, 10 Nov 2021 17:03:21 GMT
ENV NATS_SERVER_SHASUM=e287764a6e8b8ec132dcbe294aa3b96d779678079b7ada20a9bde1b81d5f5bbc
# Wed, 10 Nov 2021 17:04:06 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Nov 2021 17:05:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Nov 2021 17:05:31 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:05:32 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:05:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:05:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f6f303e73635c7923a8c64f8938e7ba4c10210fd15a6ce63aa8a62d5a8ea8c0a`  
		Last Modified: Wed, 10 Nov 2021 16:21:33 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5db4062c12269959ca71caf00b70e9baebf61b90c49c74db0e2cdb04cf83e8`  
		Last Modified: Wed, 10 Nov 2021 17:06:51 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4a229bc6e55d797c98ddd01e4d2dde702cc15dfa57f7822427f4b0c7520a1f`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99e43798e75fd46299bad03217fa38c7f0b36023271b5ded075984cbf2df237`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cc0e5c4cac5fdb636f2f1103de5fe3668597d85350d0d91b1834cc44a83b44`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb570dbf36f38785df2fc8983ad0725e443f375bdd45954981931f0137e26ea6`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 350.2 KB (350227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007ae15590fbd4c2fc97f92a5fd9f4bbee82f5e8d9da82ac218b4d5002f1a50d`  
		Last Modified: Wed, 10 Nov 2021 17:06:52 GMT  
		Size: 5.0 MB (5002607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbf9bfc6a773256d2ac9289665265759ec89a55717d181030cc64c706b5be9a`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92c772d8667daf25c2468b4b149536c7e9fe55a5896143d2e4eba0ca861cede`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca4dbf235f9fc558316b5e2119a389936545de68e74f1ad4acd18c7282eff43`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990cb23cac15d214ca7bac2df486570024c5eb19e214014a88b247c684605ee5`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:b4394e47153d08bdfa6f28759e02e8c37aa9dd5dd759f4a07417b010722de909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:ad29bbedb595a4b3fc815bb5013d6af6deb55f459d016ed438c89308084ab2ae
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711460012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c235da1808d9829823250ce435b177c85ddd1340f0878343bb5e4a1521602a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 14:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:00:40 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:00:41 GMT
ENV NATS_SERVER=2.6.4
# Wed, 10 Nov 2021 17:00:42 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.4/nats-server-v2.6.4-windows-amd64.zip
# Wed, 10 Nov 2021 17:00:43 GMT
ENV NATS_SERVER_SHASUM=e287764a6e8b8ec132dcbe294aa3b96d779678079b7ada20a9bde1b81d5f5bbc
# Wed, 10 Nov 2021 17:01:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Nov 2021 17:02:51 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Nov 2021 17:02:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:02:53 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:02:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:02:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db1ba835bccbdc73ef254c175ca6ae0dc3f0bd759c1910c3b123cfb9613223be`  
		Last Modified: Wed, 10 Nov 2021 16:21:11 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3df59793c391e0eb7e6a2ddb65801dfa94397b370daa52d04e242ba0274e3d`  
		Last Modified: Wed, 10 Nov 2021 17:06:13 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46075e93c469fbc556a996840e6ebbd02849d7518dcb4fb9feed459795714e03`  
		Last Modified: Wed, 10 Nov 2021 17:06:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a915f8554b2287a16ae0945b328b1d7d315b85bd0eda548bfde73d7686a79c`  
		Last Modified: Wed, 10 Nov 2021 17:06:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4eabf66e1adaa7841404639039b5becdbfb43fc726b93da058b0552478b7`  
		Last Modified: Wed, 10 Nov 2021 17:06:11 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f61c483196bb419b4709f89f9df78e12e7f6dab4ad8094a5aee57e021c97eb0`  
		Last Modified: Wed, 10 Nov 2021 17:06:12 GMT  
		Size: 352.3 KB (352252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e167a3b21bfb85235d9775123ea38ca0d4a4c71383ca34a95f3e203f6afddfc9`  
		Last Modified: Wed, 10 Nov 2021 17:06:15 GMT  
		Size: 5.0 MB (4973372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1d94f1b880ea3ea631c3f6e7ddeffdb30d7af80b037e2fdb55db516d018dd5`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.9 KB (1939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb1edd94e1965c70a2bb20e8bac08446704c452ce9342438e89afe2febe9906`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2d4b3e56ee1751a9373a33f5b9d58f1843e22f5ec7cc88f00e6ef369d7d9f7`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfe4f9233effe09d6160c4278ac3a375234523f40d18c3a826dd9e741139be8`  
		Last Modified: Wed, 10 Nov 2021 17:06:09 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:9c7dc9b1c133e0e5541993a156235c85c3a299c4666f96653fccd33e794fb1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:b8b34e3ddc6569eda34bb1d124a6c427fc3820313fea9618b702a1fe9a281914
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278456953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c0d6fd779bb5acd23d794cab7a62d0a39d140ff94c890f83cdb2814d63808d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 14:32:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Nov 2021 17:03:18 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Nov 2021 17:03:19 GMT
ENV NATS_SERVER=2.6.4
# Wed, 10 Nov 2021 17:03:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.4/nats-server-v2.6.4-windows-amd64.zip
# Wed, 10 Nov 2021 17:03:21 GMT
ENV NATS_SERVER_SHASUM=e287764a6e8b8ec132dcbe294aa3b96d779678079b7ada20a9bde1b81d5f5bbc
# Wed, 10 Nov 2021 17:04:06 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Nov 2021 17:05:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Nov 2021 17:05:31 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Nov 2021 17:05:32 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Nov 2021 17:05:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Nov 2021 17:05:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f6f303e73635c7923a8c64f8938e7ba4c10210fd15a6ce63aa8a62d5a8ea8c0a`  
		Last Modified: Wed, 10 Nov 2021 16:21:33 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5db4062c12269959ca71caf00b70e9baebf61b90c49c74db0e2cdb04cf83e8`  
		Last Modified: Wed, 10 Nov 2021 17:06:51 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4a229bc6e55d797c98ddd01e4d2dde702cc15dfa57f7822427f4b0c7520a1f`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99e43798e75fd46299bad03217fa38c7f0b36023271b5ded075984cbf2df237`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cc0e5c4cac5fdb636f2f1103de5fe3668597d85350d0d91b1834cc44a83b44`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb570dbf36f38785df2fc8983ad0725e443f375bdd45954981931f0137e26ea6`  
		Last Modified: Wed, 10 Nov 2021 17:06:49 GMT  
		Size: 350.2 KB (350227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007ae15590fbd4c2fc97f92a5fd9f4bbee82f5e8d9da82ac218b4d5002f1a50d`  
		Last Modified: Wed, 10 Nov 2021 17:06:52 GMT  
		Size: 5.0 MB (5002607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbf9bfc6a773256d2ac9289665265759ec89a55717d181030cc64c706b5be9a`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92c772d8667daf25c2468b4b149536c7e9fe55a5896143d2e4eba0ca861cede`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca4dbf235f9fc558316b5e2119a389936545de68e74f1ad4acd18c7282eff43`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990cb23cac15d214ca7bac2df486570024c5eb19e214014a88b247c684605ee5`  
		Last Modified: Wed, 10 Nov 2021 17:06:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

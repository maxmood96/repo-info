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
-	[`nats:2.6.5`](#nats265)
-	[`nats:2.6.5-alpine`](#nats265-alpine)
-	[`nats:2.6.5-alpine3.14`](#nats265-alpine314)
-	[`nats:2.6.5-linux`](#nats265-linux)
-	[`nats:2.6.5-nanoserver`](#nats265-nanoserver)
-	[`nats:2.6.5-nanoserver-1809`](#nats265-nanoserver-1809)
-	[`nats:2.6.5-scratch`](#nats265-scratch)
-	[`nats:2.6.5-windowsservercore`](#nats265-windowsservercore)
-	[`nats:2.6.5-windowsservercore-1809`](#nats265-windowsservercore-1809)
-	[`nats:2.6.5-windowsservercore-ltsc2016`](#nats265-windowsservercore-ltsc2016)
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
$ docker pull nats@sha256:c341fb7513aebc4acafd1241c921bf6e2d448d5a4994adf72c4f2a8240774ff2
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
$ docker pull nats@sha256:a432c76b3a2a54bb6fb3b86e877366d6aa21583ebe4f2ac823e64c45eaa8fca6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df40d7176d11e40e19fccfad2680ae991e2c854614f48d103ab2113c0bbaa764`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 22:58:51 GMT
COPY file:96d98498cda3c5da3dc5832a7d618a3bb7f4a096b3ea637e2f8cabbfb29aafda in /nats-server 
# Fri, 19 Nov 2021 22:58:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 22:58:52 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 22:58:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ccbcbf096ecb0f4372da6ec705628eb29f193a58043de9630df8acf8cc054adb`  
		Last Modified: Fri, 19 Nov 2021 23:01:12 GMT  
		Size: 4.2 MB (4238884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acebffb1f0ae9c7c56391d05ec7a9017310843497ef8f788ccb7fdf9487811c8`  
		Last Modified: Fri, 19 Nov 2021 23:01:09 GMT  
		Size: 474.0 B  
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
$ docker pull nats@sha256:a2128869e3ca420fafa695c880ff2e5c081643a029a8779a6eeec898629e36d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08762624e57d46383c02de1abccfc4c29555fa4bb40f315d659a023ac90098d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:01:53 GMT
COPY file:e12b786ebded388f1ce441cbb64f5164d1e259a5f4da426728fd95521a79c6b6 in /nats-server 
# Fri, 19 Nov 2021 23:01:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:01:54 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:01:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d5938b236103203b9eb22184fe7e2ec0ffbd51bc371b4d86b56ad8ce19084cd`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
		Size: 4.2 MB (4186496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e926f0e8ecd40b008d6f98741369d8c9c17aeb7cb228b7af14e7b9424c6cc56`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
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
$ docker pull nats@sha256:dfd8407f92396bbe19df492a8f5cea86bd1869320960e53572649f6c9d7369fd
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
$ docker pull nats@sha256:7a4fd7de980bb6490a47bcd0c467aee772f96096c57bb1cc724482627e8858a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3600d1d6d1896742ff5eec4447636481412e3bc1b57e8cbd60a97569dba12952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 22:58:24 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 22:58:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 22:58:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 22:58:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 22:58:30 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 22:58:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1253cc1a0f998799434cc5feb134e39c976d785e8abd825d4b70f7bc811e673`  
		Last Modified: Fri, 19 Nov 2021 23:00:36 GMT  
		Size: 4.5 MB (4521082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e38c6e4a411f96e627ed56d7d4604c289a6959fb5ce2f3da2962c900637e8a`  
		Last Modified: Fri, 19 Nov 2021 23:00:33 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695fd12986a53d165bec7fcb2f87f7665233f1257568f6c9cadb7ba6f47ebe81`  
		Last Modified: Fri, 19 Nov 2021 23:00:33 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:997a3f7ffb28c81b50b72fd56de75846feeb26e3bc7fb84dafb6cf16021d2f08
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7191230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d42142abd80ea09ebcaf23e32e6f07df05bb7a0ff2b315b06974c8b84b47a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:01:35 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:01:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:01:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:01:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:01:41 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:01:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ccc03d25ac63e171bfd865f61964d69fd96ea152dd4815b71be6c4368e219d`  
		Last Modified: Fri, 19 Nov 2021 23:02:44 GMT  
		Size: 4.5 MB (4472588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068e4494ae13d5594c2de7cd17ec2ee17d2f4082f3591dfad74cc76496ba1957`  
		Last Modified: Fri, 19 Nov 2021 23:02:43 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acfa78644ce575170cba7d1bcfdecd361469b3345c4d31c56683436b9f9db55`  
		Last Modified: Fri, 19 Nov 2021 23:02:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.14`

```console
$ docker pull nats@sha256:dfd8407f92396bbe19df492a8f5cea86bd1869320960e53572649f6c9d7369fd
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
$ docker pull nats@sha256:7a4fd7de980bb6490a47bcd0c467aee772f96096c57bb1cc724482627e8858a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3600d1d6d1896742ff5eec4447636481412e3bc1b57e8cbd60a97569dba12952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 22:58:24 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 22:58:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 22:58:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 22:58:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 22:58:30 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 22:58:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1253cc1a0f998799434cc5feb134e39c976d785e8abd825d4b70f7bc811e673`  
		Last Modified: Fri, 19 Nov 2021 23:00:36 GMT  
		Size: 4.5 MB (4521082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e38c6e4a411f96e627ed56d7d4604c289a6959fb5ce2f3da2962c900637e8a`  
		Last Modified: Fri, 19 Nov 2021 23:00:33 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695fd12986a53d165bec7fcb2f87f7665233f1257568f6c9cadb7ba6f47ebe81`  
		Last Modified: Fri, 19 Nov 2021 23:00:33 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:997a3f7ffb28c81b50b72fd56de75846feeb26e3bc7fb84dafb6cf16021d2f08
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7191230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d42142abd80ea09ebcaf23e32e6f07df05bb7a0ff2b315b06974c8b84b47a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:01:35 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:01:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:01:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:01:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:01:41 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:01:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ccc03d25ac63e171bfd865f61964d69fd96ea152dd4815b71be6c4368e219d`  
		Last Modified: Fri, 19 Nov 2021 23:02:44 GMT  
		Size: 4.5 MB (4472588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068e4494ae13d5594c2de7cd17ec2ee17d2f4082f3591dfad74cc76496ba1957`  
		Last Modified: Fri, 19 Nov 2021 23:02:43 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acfa78644ce575170cba7d1bcfdecd361469b3345c4d31c56683436b9f9db55`  
		Last Modified: Fri, 19 Nov 2021 23:02:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:5342f492dee0891ba6f57492d099b6caa7582a46ad449d9337f18ee9d811b7bf
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
$ docker pull nats@sha256:a432c76b3a2a54bb6fb3b86e877366d6aa21583ebe4f2ac823e64c45eaa8fca6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df40d7176d11e40e19fccfad2680ae991e2c854614f48d103ab2113c0bbaa764`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 22:58:51 GMT
COPY file:96d98498cda3c5da3dc5832a7d618a3bb7f4a096b3ea637e2f8cabbfb29aafda in /nats-server 
# Fri, 19 Nov 2021 22:58:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 22:58:52 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 22:58:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ccbcbf096ecb0f4372da6ec705628eb29f193a58043de9630df8acf8cc054adb`  
		Last Modified: Fri, 19 Nov 2021 23:01:12 GMT  
		Size: 4.2 MB (4238884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acebffb1f0ae9c7c56391d05ec7a9017310843497ef8f788ccb7fdf9487811c8`  
		Last Modified: Fri, 19 Nov 2021 23:01:09 GMT  
		Size: 474.0 B  
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
$ docker pull nats@sha256:a2128869e3ca420fafa695c880ff2e5c081643a029a8779a6eeec898629e36d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08762624e57d46383c02de1abccfc4c29555fa4bb40f315d659a023ac90098d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:01:53 GMT
COPY file:e12b786ebded388f1ce441cbb64f5164d1e259a5f4da426728fd95521a79c6b6 in /nats-server 
# Fri, 19 Nov 2021 23:01:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:01:54 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:01:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d5938b236103203b9eb22184fe7e2ec0ffbd51bc371b4d86b56ad8ce19084cd`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
		Size: 4.2 MB (4186496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e926f0e8ecd40b008d6f98741369d8c9c17aeb7cb228b7af14e7b9424c6cc56`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
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
$ docker pull nats@sha256:5342f492dee0891ba6f57492d099b6caa7582a46ad449d9337f18ee9d811b7bf
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
$ docker pull nats@sha256:a432c76b3a2a54bb6fb3b86e877366d6aa21583ebe4f2ac823e64c45eaa8fca6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df40d7176d11e40e19fccfad2680ae991e2c854614f48d103ab2113c0bbaa764`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 22:58:51 GMT
COPY file:96d98498cda3c5da3dc5832a7d618a3bb7f4a096b3ea637e2f8cabbfb29aafda in /nats-server 
# Fri, 19 Nov 2021 22:58:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 22:58:52 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 22:58:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ccbcbf096ecb0f4372da6ec705628eb29f193a58043de9630df8acf8cc054adb`  
		Last Modified: Fri, 19 Nov 2021 23:01:12 GMT  
		Size: 4.2 MB (4238884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acebffb1f0ae9c7c56391d05ec7a9017310843497ef8f788ccb7fdf9487811c8`  
		Last Modified: Fri, 19 Nov 2021 23:01:09 GMT  
		Size: 474.0 B  
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
$ docker pull nats@sha256:a2128869e3ca420fafa695c880ff2e5c081643a029a8779a6eeec898629e36d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08762624e57d46383c02de1abccfc4c29555fa4bb40f315d659a023ac90098d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:01:53 GMT
COPY file:e12b786ebded388f1ce441cbb64f5164d1e259a5f4da426728fd95521a79c6b6 in /nats-server 
# Fri, 19 Nov 2021 23:01:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:01:54 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:01:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d5938b236103203b9eb22184fe7e2ec0ffbd51bc371b4d86b56ad8ce19084cd`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
		Size: 4.2 MB (4186496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e926f0e8ecd40b008d6f98741369d8c9c17aeb7cb228b7af14e7b9424c6cc56`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
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
$ docker pull nats@sha256:c341fb7513aebc4acafd1241c921bf6e2d448d5a4994adf72c4f2a8240774ff2
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
$ docker pull nats@sha256:a432c76b3a2a54bb6fb3b86e877366d6aa21583ebe4f2ac823e64c45eaa8fca6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df40d7176d11e40e19fccfad2680ae991e2c854614f48d103ab2113c0bbaa764`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 22:58:51 GMT
COPY file:96d98498cda3c5da3dc5832a7d618a3bb7f4a096b3ea637e2f8cabbfb29aafda in /nats-server 
# Fri, 19 Nov 2021 22:58:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 22:58:52 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 22:58:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ccbcbf096ecb0f4372da6ec705628eb29f193a58043de9630df8acf8cc054adb`  
		Last Modified: Fri, 19 Nov 2021 23:01:12 GMT  
		Size: 4.2 MB (4238884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acebffb1f0ae9c7c56391d05ec7a9017310843497ef8f788ccb7fdf9487811c8`  
		Last Modified: Fri, 19 Nov 2021 23:01:09 GMT  
		Size: 474.0 B  
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
$ docker pull nats@sha256:a2128869e3ca420fafa695c880ff2e5c081643a029a8779a6eeec898629e36d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08762624e57d46383c02de1abccfc4c29555fa4bb40f315d659a023ac90098d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:01:53 GMT
COPY file:e12b786ebded388f1ce441cbb64f5164d1e259a5f4da426728fd95521a79c6b6 in /nats-server 
# Fri, 19 Nov 2021 23:01:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:01:54 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:01:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d5938b236103203b9eb22184fe7e2ec0ffbd51bc371b4d86b56ad8ce19084cd`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
		Size: 4.2 MB (4186496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e926f0e8ecd40b008d6f98741369d8c9c17aeb7cb228b7af14e7b9424c6cc56`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
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
$ docker pull nats@sha256:dfd8407f92396bbe19df492a8f5cea86bd1869320960e53572649f6c9d7369fd
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
$ docker pull nats@sha256:7a4fd7de980bb6490a47bcd0c467aee772f96096c57bb1cc724482627e8858a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3600d1d6d1896742ff5eec4447636481412e3bc1b57e8cbd60a97569dba12952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 22:58:24 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 22:58:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 22:58:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 22:58:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 22:58:30 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 22:58:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1253cc1a0f998799434cc5feb134e39c976d785e8abd825d4b70f7bc811e673`  
		Last Modified: Fri, 19 Nov 2021 23:00:36 GMT  
		Size: 4.5 MB (4521082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e38c6e4a411f96e627ed56d7d4604c289a6959fb5ce2f3da2962c900637e8a`  
		Last Modified: Fri, 19 Nov 2021 23:00:33 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695fd12986a53d165bec7fcb2f87f7665233f1257568f6c9cadb7ba6f47ebe81`  
		Last Modified: Fri, 19 Nov 2021 23:00:33 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:997a3f7ffb28c81b50b72fd56de75846feeb26e3bc7fb84dafb6cf16021d2f08
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7191230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d42142abd80ea09ebcaf23e32e6f07df05bb7a0ff2b315b06974c8b84b47a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:01:35 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:01:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:01:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:01:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:01:41 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:01:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ccc03d25ac63e171bfd865f61964d69fd96ea152dd4815b71be6c4368e219d`  
		Last Modified: Fri, 19 Nov 2021 23:02:44 GMT  
		Size: 4.5 MB (4472588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068e4494ae13d5594c2de7cd17ec2ee17d2f4082f3591dfad74cc76496ba1957`  
		Last Modified: Fri, 19 Nov 2021 23:02:43 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acfa78644ce575170cba7d1bcfdecd361469b3345c4d31c56683436b9f9db55`  
		Last Modified: Fri, 19 Nov 2021 23:02:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-alpine3.14`

```console
$ docker pull nats@sha256:dfd8407f92396bbe19df492a8f5cea86bd1869320960e53572649f6c9d7369fd
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
$ docker pull nats@sha256:7a4fd7de980bb6490a47bcd0c467aee772f96096c57bb1cc724482627e8858a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3600d1d6d1896742ff5eec4447636481412e3bc1b57e8cbd60a97569dba12952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 22:58:24 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 22:58:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 22:58:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 22:58:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 22:58:30 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 22:58:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1253cc1a0f998799434cc5feb134e39c976d785e8abd825d4b70f7bc811e673`  
		Last Modified: Fri, 19 Nov 2021 23:00:36 GMT  
		Size: 4.5 MB (4521082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e38c6e4a411f96e627ed56d7d4604c289a6959fb5ce2f3da2962c900637e8a`  
		Last Modified: Fri, 19 Nov 2021 23:00:33 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695fd12986a53d165bec7fcb2f87f7665233f1257568f6c9cadb7ba6f47ebe81`  
		Last Modified: Fri, 19 Nov 2021 23:00:33 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:997a3f7ffb28c81b50b72fd56de75846feeb26e3bc7fb84dafb6cf16021d2f08
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7191230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d42142abd80ea09ebcaf23e32e6f07df05bb7a0ff2b315b06974c8b84b47a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:01:35 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:01:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:01:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:01:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:01:41 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:01:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ccc03d25ac63e171bfd865f61964d69fd96ea152dd4815b71be6c4368e219d`  
		Last Modified: Fri, 19 Nov 2021 23:02:44 GMT  
		Size: 4.5 MB (4472588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068e4494ae13d5594c2de7cd17ec2ee17d2f4082f3591dfad74cc76496ba1957`  
		Last Modified: Fri, 19 Nov 2021 23:02:43 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acfa78644ce575170cba7d1bcfdecd361469b3345c4d31c56683436b9f9db55`  
		Last Modified: Fri, 19 Nov 2021 23:02:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-linux`

```console
$ docker pull nats@sha256:5342f492dee0891ba6f57492d099b6caa7582a46ad449d9337f18ee9d811b7bf
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
$ docker pull nats@sha256:a432c76b3a2a54bb6fb3b86e877366d6aa21583ebe4f2ac823e64c45eaa8fca6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df40d7176d11e40e19fccfad2680ae991e2c854614f48d103ab2113c0bbaa764`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 22:58:51 GMT
COPY file:96d98498cda3c5da3dc5832a7d618a3bb7f4a096b3ea637e2f8cabbfb29aafda in /nats-server 
# Fri, 19 Nov 2021 22:58:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 22:58:52 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 22:58:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ccbcbf096ecb0f4372da6ec705628eb29f193a58043de9630df8acf8cc054adb`  
		Last Modified: Fri, 19 Nov 2021 23:01:12 GMT  
		Size: 4.2 MB (4238884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acebffb1f0ae9c7c56391d05ec7a9017310843497ef8f788ccb7fdf9487811c8`  
		Last Modified: Fri, 19 Nov 2021 23:01:09 GMT  
		Size: 474.0 B  
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
$ docker pull nats@sha256:a2128869e3ca420fafa695c880ff2e5c081643a029a8779a6eeec898629e36d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08762624e57d46383c02de1abccfc4c29555fa4bb40f315d659a023ac90098d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:01:53 GMT
COPY file:e12b786ebded388f1ce441cbb64f5164d1e259a5f4da426728fd95521a79c6b6 in /nats-server 
# Fri, 19 Nov 2021 23:01:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:01:54 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:01:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d5938b236103203b9eb22184fe7e2ec0ffbd51bc371b4d86b56ad8ce19084cd`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
		Size: 4.2 MB (4186496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e926f0e8ecd40b008d6f98741369d8c9c17aeb7cb228b7af14e7b9424c6cc56`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
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
$ docker pull nats@sha256:5342f492dee0891ba6f57492d099b6caa7582a46ad449d9337f18ee9d811b7bf
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
$ docker pull nats@sha256:a432c76b3a2a54bb6fb3b86e877366d6aa21583ebe4f2ac823e64c45eaa8fca6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df40d7176d11e40e19fccfad2680ae991e2c854614f48d103ab2113c0bbaa764`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 22:58:51 GMT
COPY file:96d98498cda3c5da3dc5832a7d618a3bb7f4a096b3ea637e2f8cabbfb29aafda in /nats-server 
# Fri, 19 Nov 2021 22:58:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 22:58:52 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 22:58:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ccbcbf096ecb0f4372da6ec705628eb29f193a58043de9630df8acf8cc054adb`  
		Last Modified: Fri, 19 Nov 2021 23:01:12 GMT  
		Size: 4.2 MB (4238884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acebffb1f0ae9c7c56391d05ec7a9017310843497ef8f788ccb7fdf9487811c8`  
		Last Modified: Fri, 19 Nov 2021 23:01:09 GMT  
		Size: 474.0 B  
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
$ docker pull nats@sha256:a2128869e3ca420fafa695c880ff2e5c081643a029a8779a6eeec898629e36d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08762624e57d46383c02de1abccfc4c29555fa4bb40f315d659a023ac90098d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:01:53 GMT
COPY file:e12b786ebded388f1ce441cbb64f5164d1e259a5f4da426728fd95521a79c6b6 in /nats-server 
# Fri, 19 Nov 2021 23:01:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:01:54 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:01:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d5938b236103203b9eb22184fe7e2ec0ffbd51bc371b4d86b56ad8ce19084cd`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
		Size: 4.2 MB (4186496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e926f0e8ecd40b008d6f98741369d8c9c17aeb7cb228b7af14e7b9424c6cc56`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
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

## `nats:2.6.5`

```console
$ docker pull nats@sha256:f2d5e7f28dfc4eb2077a25c7f5b46a382bda3f44263dab0b5b3445aea229c7f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `nats:2.6.5` - linux; arm variant v6

```console
$ docker pull nats@sha256:a432c76b3a2a54bb6fb3b86e877366d6aa21583ebe4f2ac823e64c45eaa8fca6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df40d7176d11e40e19fccfad2680ae991e2c854614f48d103ab2113c0bbaa764`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 22:58:51 GMT
COPY file:96d98498cda3c5da3dc5832a7d618a3bb7f4a096b3ea637e2f8cabbfb29aafda in /nats-server 
# Fri, 19 Nov 2021 22:58:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 22:58:52 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 22:58:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ccbcbf096ecb0f4372da6ec705628eb29f193a58043de9630df8acf8cc054adb`  
		Last Modified: Fri, 19 Nov 2021 23:01:12 GMT  
		Size: 4.2 MB (4238884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acebffb1f0ae9c7c56391d05ec7a9017310843497ef8f788ccb7fdf9487811c8`  
		Last Modified: Fri, 19 Nov 2021 23:01:09 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.5` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a2128869e3ca420fafa695c880ff2e5c081643a029a8779a6eeec898629e36d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08762624e57d46383c02de1abccfc4c29555fa4bb40f315d659a023ac90098d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:01:53 GMT
COPY file:e12b786ebded388f1ce441cbb64f5164d1e259a5f4da426728fd95521a79c6b6 in /nats-server 
# Fri, 19 Nov 2021 23:01:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:01:54 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:01:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d5938b236103203b9eb22184fe7e2ec0ffbd51bc371b4d86b56ad8ce19084cd`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
		Size: 4.2 MB (4186496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e926f0e8ecd40b008d6f98741369d8c9c17aeb7cb228b7af14e7b9424c6cc56`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.5-alpine`

```console
$ docker pull nats@sha256:8603c81ef253bc8de7dccdbb910cebc0fd2fd310dfba118dde52dd01d9aec57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `nats:2.6.5-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:7a4fd7de980bb6490a47bcd0c467aee772f96096c57bb1cc724482627e8858a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3600d1d6d1896742ff5eec4447636481412e3bc1b57e8cbd60a97569dba12952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 22:58:24 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 22:58:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 22:58:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 22:58:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 22:58:30 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 22:58:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1253cc1a0f998799434cc5feb134e39c976d785e8abd825d4b70f7bc811e673`  
		Last Modified: Fri, 19 Nov 2021 23:00:36 GMT  
		Size: 4.5 MB (4521082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e38c6e4a411f96e627ed56d7d4604c289a6959fb5ce2f3da2962c900637e8a`  
		Last Modified: Fri, 19 Nov 2021 23:00:33 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695fd12986a53d165bec7fcb2f87f7665233f1257568f6c9cadb7ba6f47ebe81`  
		Last Modified: Fri, 19 Nov 2021 23:00:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.5-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:997a3f7ffb28c81b50b72fd56de75846feeb26e3bc7fb84dafb6cf16021d2f08
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7191230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d42142abd80ea09ebcaf23e32e6f07df05bb7a0ff2b315b06974c8b84b47a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:01:35 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:01:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:01:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:01:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:01:41 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:01:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ccc03d25ac63e171bfd865f61964d69fd96ea152dd4815b71be6c4368e219d`  
		Last Modified: Fri, 19 Nov 2021 23:02:44 GMT  
		Size: 4.5 MB (4472588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068e4494ae13d5594c2de7cd17ec2ee17d2f4082f3591dfad74cc76496ba1957`  
		Last Modified: Fri, 19 Nov 2021 23:02:43 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acfa78644ce575170cba7d1bcfdecd361469b3345c4d31c56683436b9f9db55`  
		Last Modified: Fri, 19 Nov 2021 23:02:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.5-alpine3.14`

```console
$ docker pull nats@sha256:8603c81ef253bc8de7dccdbb910cebc0fd2fd310dfba118dde52dd01d9aec57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `nats:2.6.5-alpine3.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:7a4fd7de980bb6490a47bcd0c467aee772f96096c57bb1cc724482627e8858a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3600d1d6d1896742ff5eec4447636481412e3bc1b57e8cbd60a97569dba12952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 22:58:24 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 22:58:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 22:58:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 22:58:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 22:58:30 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 22:58:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1253cc1a0f998799434cc5feb134e39c976d785e8abd825d4b70f7bc811e673`  
		Last Modified: Fri, 19 Nov 2021 23:00:36 GMT  
		Size: 4.5 MB (4521082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e38c6e4a411f96e627ed56d7d4604c289a6959fb5ce2f3da2962c900637e8a`  
		Last Modified: Fri, 19 Nov 2021 23:00:33 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695fd12986a53d165bec7fcb2f87f7665233f1257568f6c9cadb7ba6f47ebe81`  
		Last Modified: Fri, 19 Nov 2021 23:00:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.5-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:997a3f7ffb28c81b50b72fd56de75846feeb26e3bc7fb84dafb6cf16021d2f08
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7191230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d42142abd80ea09ebcaf23e32e6f07df05bb7a0ff2b315b06974c8b84b47a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:01:35 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:01:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:01:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:01:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:01:41 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:01:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ccc03d25ac63e171bfd865f61964d69fd96ea152dd4815b71be6c4368e219d`  
		Last Modified: Fri, 19 Nov 2021 23:02:44 GMT  
		Size: 4.5 MB (4472588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068e4494ae13d5594c2de7cd17ec2ee17d2f4082f3591dfad74cc76496ba1957`  
		Last Modified: Fri, 19 Nov 2021 23:02:43 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acfa78644ce575170cba7d1bcfdecd361469b3345c4d31c56683436b9f9db55`  
		Last Modified: Fri, 19 Nov 2021 23:02:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.5-linux`

```console
$ docker pull nats@sha256:f2d5e7f28dfc4eb2077a25c7f5b46a382bda3f44263dab0b5b3445aea229c7f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `nats:2.6.5-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:a432c76b3a2a54bb6fb3b86e877366d6aa21583ebe4f2ac823e64c45eaa8fca6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df40d7176d11e40e19fccfad2680ae991e2c854614f48d103ab2113c0bbaa764`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 22:58:51 GMT
COPY file:96d98498cda3c5da3dc5832a7d618a3bb7f4a096b3ea637e2f8cabbfb29aafda in /nats-server 
# Fri, 19 Nov 2021 22:58:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 22:58:52 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 22:58:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ccbcbf096ecb0f4372da6ec705628eb29f193a58043de9630df8acf8cc054adb`  
		Last Modified: Fri, 19 Nov 2021 23:01:12 GMT  
		Size: 4.2 MB (4238884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acebffb1f0ae9c7c56391d05ec7a9017310843497ef8f788ccb7fdf9487811c8`  
		Last Modified: Fri, 19 Nov 2021 23:01:09 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.5-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a2128869e3ca420fafa695c880ff2e5c081643a029a8779a6eeec898629e36d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08762624e57d46383c02de1abccfc4c29555fa4bb40f315d659a023ac90098d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:01:53 GMT
COPY file:e12b786ebded388f1ce441cbb64f5164d1e259a5f4da426728fd95521a79c6b6 in /nats-server 
# Fri, 19 Nov 2021 23:01:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:01:54 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:01:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d5938b236103203b9eb22184fe7e2ec0ffbd51bc371b4d86b56ad8ce19084cd`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
		Size: 4.2 MB (4186496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e926f0e8ecd40b008d6f98741369d8c9c17aeb7cb228b7af14e7b9424c6cc56`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.5-nanoserver`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `nats:2.6.5-nanoserver-1809`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `nats:2.6.5-scratch`

```console
$ docker pull nats@sha256:f2d5e7f28dfc4eb2077a25c7f5b46a382bda3f44263dab0b5b3445aea229c7f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `nats:2.6.5-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:a432c76b3a2a54bb6fb3b86e877366d6aa21583ebe4f2ac823e64c45eaa8fca6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df40d7176d11e40e19fccfad2680ae991e2c854614f48d103ab2113c0bbaa764`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 22:58:51 GMT
COPY file:96d98498cda3c5da3dc5832a7d618a3bb7f4a096b3ea637e2f8cabbfb29aafda in /nats-server 
# Fri, 19 Nov 2021 22:58:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 22:58:52 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 22:58:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ccbcbf096ecb0f4372da6ec705628eb29f193a58043de9630df8acf8cc054adb`  
		Last Modified: Fri, 19 Nov 2021 23:01:12 GMT  
		Size: 4.2 MB (4238884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acebffb1f0ae9c7c56391d05ec7a9017310843497ef8f788ccb7fdf9487811c8`  
		Last Modified: Fri, 19 Nov 2021 23:01:09 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.5-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a2128869e3ca420fafa695c880ff2e5c081643a029a8779a6eeec898629e36d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08762624e57d46383c02de1abccfc4c29555fa4bb40f315d659a023ac90098d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:01:53 GMT
COPY file:e12b786ebded388f1ce441cbb64f5164d1e259a5f4da426728fd95521a79c6b6 in /nats-server 
# Fri, 19 Nov 2021 23:01:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:01:54 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:01:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d5938b236103203b9eb22184fe7e2ec0ffbd51bc371b4d86b56ad8ce19084cd`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
		Size: 4.2 MB (4186496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e926f0e8ecd40b008d6f98741369d8c9c17aeb7cb228b7af14e7b9424c6cc56`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.5-windowsservercore`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `nats:2.6.5-windowsservercore-1809`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `nats:2.6.5-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `nats:alpine`

```console
$ docker pull nats@sha256:dfd8407f92396bbe19df492a8f5cea86bd1869320960e53572649f6c9d7369fd
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
$ docker pull nats@sha256:7a4fd7de980bb6490a47bcd0c467aee772f96096c57bb1cc724482627e8858a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3600d1d6d1896742ff5eec4447636481412e3bc1b57e8cbd60a97569dba12952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 22:58:24 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 22:58:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 22:58:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 22:58:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 22:58:30 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 22:58:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1253cc1a0f998799434cc5feb134e39c976d785e8abd825d4b70f7bc811e673`  
		Last Modified: Fri, 19 Nov 2021 23:00:36 GMT  
		Size: 4.5 MB (4521082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e38c6e4a411f96e627ed56d7d4604c289a6959fb5ce2f3da2962c900637e8a`  
		Last Modified: Fri, 19 Nov 2021 23:00:33 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695fd12986a53d165bec7fcb2f87f7665233f1257568f6c9cadb7ba6f47ebe81`  
		Last Modified: Fri, 19 Nov 2021 23:00:33 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:997a3f7ffb28c81b50b72fd56de75846feeb26e3bc7fb84dafb6cf16021d2f08
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7191230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d42142abd80ea09ebcaf23e32e6f07df05bb7a0ff2b315b06974c8b84b47a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:01:35 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:01:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:01:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:01:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:01:41 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:01:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ccc03d25ac63e171bfd865f61964d69fd96ea152dd4815b71be6c4368e219d`  
		Last Modified: Fri, 19 Nov 2021 23:02:44 GMT  
		Size: 4.5 MB (4472588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068e4494ae13d5594c2de7cd17ec2ee17d2f4082f3591dfad74cc76496ba1957`  
		Last Modified: Fri, 19 Nov 2021 23:02:43 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acfa78644ce575170cba7d1bcfdecd361469b3345c4d31c56683436b9f9db55`  
		Last Modified: Fri, 19 Nov 2021 23:02:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.14`

```console
$ docker pull nats@sha256:dfd8407f92396bbe19df492a8f5cea86bd1869320960e53572649f6c9d7369fd
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
$ docker pull nats@sha256:7a4fd7de980bb6490a47bcd0c467aee772f96096c57bb1cc724482627e8858a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3600d1d6d1896742ff5eec4447636481412e3bc1b57e8cbd60a97569dba12952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 22:58:24 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 22:58:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 22:58:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 22:58:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 22:58:30 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 22:58:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1253cc1a0f998799434cc5feb134e39c976d785e8abd825d4b70f7bc811e673`  
		Last Modified: Fri, 19 Nov 2021 23:00:36 GMT  
		Size: 4.5 MB (4521082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e38c6e4a411f96e627ed56d7d4604c289a6959fb5ce2f3da2962c900637e8a`  
		Last Modified: Fri, 19 Nov 2021 23:00:33 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695fd12986a53d165bec7fcb2f87f7665233f1257568f6c9cadb7ba6f47ebe81`  
		Last Modified: Fri, 19 Nov 2021 23:00:33 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:997a3f7ffb28c81b50b72fd56de75846feeb26e3bc7fb84dafb6cf16021d2f08
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7191230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d42142abd80ea09ebcaf23e32e6f07df05bb7a0ff2b315b06974c8b84b47a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:01:35 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:01:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:01:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:01:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:01:41 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:01:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ccc03d25ac63e171bfd865f61964d69fd96ea152dd4815b71be6c4368e219d`  
		Last Modified: Fri, 19 Nov 2021 23:02:44 GMT  
		Size: 4.5 MB (4472588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068e4494ae13d5594c2de7cd17ec2ee17d2f4082f3591dfad74cc76496ba1957`  
		Last Modified: Fri, 19 Nov 2021 23:02:43 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acfa78644ce575170cba7d1bcfdecd361469b3345c4d31c56683436b9f9db55`  
		Last Modified: Fri, 19 Nov 2021 23:02:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:c341fb7513aebc4acafd1241c921bf6e2d448d5a4994adf72c4f2a8240774ff2
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
$ docker pull nats@sha256:a432c76b3a2a54bb6fb3b86e877366d6aa21583ebe4f2ac823e64c45eaa8fca6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df40d7176d11e40e19fccfad2680ae991e2c854614f48d103ab2113c0bbaa764`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 22:58:51 GMT
COPY file:96d98498cda3c5da3dc5832a7d618a3bb7f4a096b3ea637e2f8cabbfb29aafda in /nats-server 
# Fri, 19 Nov 2021 22:58:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 22:58:52 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 22:58:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ccbcbf096ecb0f4372da6ec705628eb29f193a58043de9630df8acf8cc054adb`  
		Last Modified: Fri, 19 Nov 2021 23:01:12 GMT  
		Size: 4.2 MB (4238884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acebffb1f0ae9c7c56391d05ec7a9017310843497ef8f788ccb7fdf9487811c8`  
		Last Modified: Fri, 19 Nov 2021 23:01:09 GMT  
		Size: 474.0 B  
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
$ docker pull nats@sha256:a2128869e3ca420fafa695c880ff2e5c081643a029a8779a6eeec898629e36d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08762624e57d46383c02de1abccfc4c29555fa4bb40f315d659a023ac90098d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:01:53 GMT
COPY file:e12b786ebded388f1ce441cbb64f5164d1e259a5f4da426728fd95521a79c6b6 in /nats-server 
# Fri, 19 Nov 2021 23:01:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:01:54 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:01:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d5938b236103203b9eb22184fe7e2ec0ffbd51bc371b4d86b56ad8ce19084cd`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
		Size: 4.2 MB (4186496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e926f0e8ecd40b008d6f98741369d8c9c17aeb7cb228b7af14e7b9424c6cc56`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
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
$ docker pull nats@sha256:5342f492dee0891ba6f57492d099b6caa7582a46ad449d9337f18ee9d811b7bf
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
$ docker pull nats@sha256:a432c76b3a2a54bb6fb3b86e877366d6aa21583ebe4f2ac823e64c45eaa8fca6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df40d7176d11e40e19fccfad2680ae991e2c854614f48d103ab2113c0bbaa764`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 22:58:51 GMT
COPY file:96d98498cda3c5da3dc5832a7d618a3bb7f4a096b3ea637e2f8cabbfb29aafda in /nats-server 
# Fri, 19 Nov 2021 22:58:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 22:58:52 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 22:58:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ccbcbf096ecb0f4372da6ec705628eb29f193a58043de9630df8acf8cc054adb`  
		Last Modified: Fri, 19 Nov 2021 23:01:12 GMT  
		Size: 4.2 MB (4238884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acebffb1f0ae9c7c56391d05ec7a9017310843497ef8f788ccb7fdf9487811c8`  
		Last Modified: Fri, 19 Nov 2021 23:01:09 GMT  
		Size: 474.0 B  
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
$ docker pull nats@sha256:a2128869e3ca420fafa695c880ff2e5c081643a029a8779a6eeec898629e36d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08762624e57d46383c02de1abccfc4c29555fa4bb40f315d659a023ac90098d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:01:53 GMT
COPY file:e12b786ebded388f1ce441cbb64f5164d1e259a5f4da426728fd95521a79c6b6 in /nats-server 
# Fri, 19 Nov 2021 23:01:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:01:54 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:01:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d5938b236103203b9eb22184fe7e2ec0ffbd51bc371b4d86b56ad8ce19084cd`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
		Size: 4.2 MB (4186496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e926f0e8ecd40b008d6f98741369d8c9c17aeb7cb228b7af14e7b9424c6cc56`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
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
$ docker pull nats@sha256:5342f492dee0891ba6f57492d099b6caa7582a46ad449d9337f18ee9d811b7bf
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
$ docker pull nats@sha256:a432c76b3a2a54bb6fb3b86e877366d6aa21583ebe4f2ac823e64c45eaa8fca6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df40d7176d11e40e19fccfad2680ae991e2c854614f48d103ab2113c0bbaa764`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 22:58:51 GMT
COPY file:96d98498cda3c5da3dc5832a7d618a3bb7f4a096b3ea637e2f8cabbfb29aafda in /nats-server 
# Fri, 19 Nov 2021 22:58:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 22:58:52 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 22:58:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ccbcbf096ecb0f4372da6ec705628eb29f193a58043de9630df8acf8cc054adb`  
		Last Modified: Fri, 19 Nov 2021 23:01:12 GMT  
		Size: 4.2 MB (4238884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acebffb1f0ae9c7c56391d05ec7a9017310843497ef8f788ccb7fdf9487811c8`  
		Last Modified: Fri, 19 Nov 2021 23:01:09 GMT  
		Size: 474.0 B  
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
$ docker pull nats@sha256:a2128869e3ca420fafa695c880ff2e5c081643a029a8779a6eeec898629e36d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08762624e57d46383c02de1abccfc4c29555fa4bb40f315d659a023ac90098d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:01:53 GMT
COPY file:e12b786ebded388f1ce441cbb64f5164d1e259a5f4da426728fd95521a79c6b6 in /nats-server 
# Fri, 19 Nov 2021 23:01:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:01:54 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:01:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d5938b236103203b9eb22184fe7e2ec0ffbd51bc371b4d86b56ad8ce19084cd`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
		Size: 4.2 MB (4186496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e926f0e8ecd40b008d6f98741369d8c9c17aeb7cb228b7af14e7b9424c6cc56`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
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

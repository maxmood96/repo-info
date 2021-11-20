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
$ docker pull nats@sha256:dba2bbbe7e9dd7c39a43a53a5d4beeaae542ee98dae82b64aed895c6589e8f21
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
$ docker pull nats@sha256:4c4e804a1650e91fbfbf07efa44afc479755a6ace2ab57050b950475ddc93442
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acde872f934ff8c9ad3505d331c4827e3285ad4314e92f69ae0abe1d455ff77f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:42:18 GMT
COPY file:148643ead7a90f9c3416e4455a70bf4638bf9c77005e258d6ec4dcf605560028 in /nats-server 
# Fri, 19 Nov 2021 23:42:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:42:19 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:42:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe89a8c692b8dabfd4ac3062f9232c753d0c2db79be5dca06811cfd9dbcbdc1c`  
		Last Modified: Fri, 19 Nov 2021 23:43:09 GMT  
		Size: 4.6 MB (4575375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5645a0f80ddde9dcce3a4aecfc7a9ab65b20f5c4fcab9897e75302b2b4bf404`  
		Last Modified: Fri, 19 Nov 2021 23:43:08 GMT  
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
$ docker pull nats@sha256:c3e6b4d51c17fa68c6e4c70ce519e1035c89a232b96c9ca59d1aa9932f7b4687
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514f8bdd0d1db9adfcc78eb1a00c34ad3eefd5e7135852bcd277023ebe30f0c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:48132b2177bf3ca4d978b99a66b7a228cae6937450ee016ac753a4c4ffb567a6 in /nats-server 
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:22:49 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:49 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:22:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:92ac13b7cd582c606500bbb3364dbf1a7e0a85030b4deeabfba3a44d94b2c66e`  
		Last Modified: Fri, 19 Nov 2021 23:25:11 GMT  
		Size: 4.2 MB (4235210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b8c68cfe1eeaa6a60a3863fceb15216ecc6b46b1ff00255bffe9a638b3b768`  
		Last Modified: Fri, 19 Nov 2021 23:25:08 GMT  
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
$ docker pull nats@sha256:905989f3a6b51bca9680b352fd5a4cc271c355fe1f97bc891436699220a6dc15
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107424291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc5b97cb5590745b1ceee71f3fa39e6182c08aa0778a902b59edef61785e388`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 19 Nov 2021 23:16:56 GMT
RUN cmd /S /C #(nop) COPY file:cb348e461b3d96ac80f8049551e5a2f64ad993b7e0766d87ab5ab5fdd94589b6 in C:\nats-server.exe 
# Fri, 19 Nov 2021 23:16:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:17:00 GMT
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
	-	`sha256:ba9a2a1dd5182104e73dd0b99871b9421cef25f8493a107f6c5851e604a0c805`  
		Last Modified: Fri, 19 Nov 2021 23:20:49 GMT  
		Size: 4.6 MB (4634936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea376684ddbfce1b9e46c526a7dbe800a8e6a7423d96f16cca44e1ac0610b13b`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdadde7749a61c1e452864079f7e483484220f0ae3fa7f7bd7244e01c51564e`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c305401f02bde38a326c77b9088b6a7a2a01a5babed79ec98c244a5c6006588`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4957be82dbf1c2d1fdab2d9f4604991c3bbf7c9ff6fa46efeee39dd1086ed3`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:7f36c22a7e0cb76ce2e06235022b20aa5ed52736f6c363dbeeaca8dab69ecf4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:06e24692a80300ca5bd9671ab4ab80c1b048d6887c18ca32aa073887fa1fd359
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7686268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e413df78b5a846b18ac33bc0aaf255770267bebcbc0618ab7f297560f31587ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:41:57 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:42:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:42:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:42:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:42:01 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:42:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a26961feb3858523c0a38d5decbabc61ce2fdecfc03c3f118db9ae38e2a2081`  
		Last Modified: Fri, 19 Nov 2021 23:42:44 GMT  
		Size: 4.9 MB (4862314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0833c09ffb63b8898f80abd7a90f5bdecefb7a10a771e96779648ca03137643`  
		Last Modified: Fri, 19 Nov 2021 23:42:43 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2219d94c89a69f8eb02e5fcbb9cc203e77bbc833a538b83c6cff697ea6e410e3`  
		Last Modified: Fri, 19 Nov 2021 23:42:43 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:1492db6aaab11ff0408a18ccd0b9c4e05a6a09bf27b989ba06df650f3c4daa35
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5380995e0b783165a76fcab9a147c18e8154d4e6cc310236294f54d9adeba4e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:22:19 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:22:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:22:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:22:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:22:24 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:22:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0676a94d1c25310146837eb95390f211b55367bbbc41c86020b28b00375b7baf`  
		Last Modified: Fri, 19 Nov 2021 23:24:33 GMT  
		Size: 4.5 MB (4516168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f024b09adefc2b21cfad2f2279a279604f371cfe6bbfcf1dd11f412d031a7e5d`  
		Last Modified: Fri, 19 Nov 2021 23:24:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c6d7089949b487c17d10a9a94548058005f51c80e94429659ff9dd9093a4cf`  
		Last Modified: Fri, 19 Nov 2021 23:24:31 GMT  
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
$ docker pull nats@sha256:7f36c22a7e0cb76ce2e06235022b20aa5ed52736f6c363dbeeaca8dab69ecf4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:06e24692a80300ca5bd9671ab4ab80c1b048d6887c18ca32aa073887fa1fd359
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7686268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e413df78b5a846b18ac33bc0aaf255770267bebcbc0618ab7f297560f31587ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:41:57 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:42:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:42:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:42:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:42:01 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:42:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a26961feb3858523c0a38d5decbabc61ce2fdecfc03c3f118db9ae38e2a2081`  
		Last Modified: Fri, 19 Nov 2021 23:42:44 GMT  
		Size: 4.9 MB (4862314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0833c09ffb63b8898f80abd7a90f5bdecefb7a10a771e96779648ca03137643`  
		Last Modified: Fri, 19 Nov 2021 23:42:43 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2219d94c89a69f8eb02e5fcbb9cc203e77bbc833a538b83c6cff697ea6e410e3`  
		Last Modified: Fri, 19 Nov 2021 23:42:43 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:1492db6aaab11ff0408a18ccd0b9c4e05a6a09bf27b989ba06df650f3c4daa35
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5380995e0b783165a76fcab9a147c18e8154d4e6cc310236294f54d9adeba4e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:22:19 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:22:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:22:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:22:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:22:24 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:22:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0676a94d1c25310146837eb95390f211b55367bbbc41c86020b28b00375b7baf`  
		Last Modified: Fri, 19 Nov 2021 23:24:33 GMT  
		Size: 4.5 MB (4516168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f024b09adefc2b21cfad2f2279a279604f371cfe6bbfcf1dd11f412d031a7e5d`  
		Last Modified: Fri, 19 Nov 2021 23:24:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c6d7089949b487c17d10a9a94548058005f51c80e94429659ff9dd9093a4cf`  
		Last Modified: Fri, 19 Nov 2021 23:24:31 GMT  
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
$ docker pull nats@sha256:85deef40c1d54f42dc99207f542c78162bd9cee6cccc9ee62d4a68e5e8155e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:4c4e804a1650e91fbfbf07efa44afc479755a6ace2ab57050b950475ddc93442
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acde872f934ff8c9ad3505d331c4827e3285ad4314e92f69ae0abe1d455ff77f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:42:18 GMT
COPY file:148643ead7a90f9c3416e4455a70bf4638bf9c77005e258d6ec4dcf605560028 in /nats-server 
# Fri, 19 Nov 2021 23:42:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:42:19 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:42:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe89a8c692b8dabfd4ac3062f9232c753d0c2db79be5dca06811cfd9dbcbdc1c`  
		Last Modified: Fri, 19 Nov 2021 23:43:09 GMT  
		Size: 4.6 MB (4575375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5645a0f80ddde9dcce3a4aecfc7a9ab65b20f5c4fcab9897e75302b2b4bf404`  
		Last Modified: Fri, 19 Nov 2021 23:43:08 GMT  
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
$ docker pull nats@sha256:c3e6b4d51c17fa68c6e4c70ce519e1035c89a232b96c9ca59d1aa9932f7b4687
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514f8bdd0d1db9adfcc78eb1a00c34ad3eefd5e7135852bcd277023ebe30f0c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:48132b2177bf3ca4d978b99a66b7a228cae6937450ee016ac753a4c4ffb567a6 in /nats-server 
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:22:49 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:49 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:22:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:92ac13b7cd582c606500bbb3364dbf1a7e0a85030b4deeabfba3a44d94b2c66e`  
		Last Modified: Fri, 19 Nov 2021 23:25:11 GMT  
		Size: 4.2 MB (4235210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b8c68cfe1eeaa6a60a3863fceb15216ecc6b46b1ff00255bffe9a638b3b768`  
		Last Modified: Fri, 19 Nov 2021 23:25:08 GMT  
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
$ docker pull nats@sha256:b398d37048c28628fc4321bc540446f3ee812011e7c9a16d3dd19009eb5884ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:905989f3a6b51bca9680b352fd5a4cc271c355fe1f97bc891436699220a6dc15
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107424291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc5b97cb5590745b1ceee71f3fa39e6182c08aa0778a902b59edef61785e388`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 19 Nov 2021 23:16:56 GMT
RUN cmd /S /C #(nop) COPY file:cb348e461b3d96ac80f8049551e5a2f64ad993b7e0766d87ab5ab5fdd94589b6 in C:\nats-server.exe 
# Fri, 19 Nov 2021 23:16:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:17:00 GMT
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
	-	`sha256:ba9a2a1dd5182104e73dd0b99871b9421cef25f8493a107f6c5851e604a0c805`  
		Last Modified: Fri, 19 Nov 2021 23:20:49 GMT  
		Size: 4.6 MB (4634936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea376684ddbfce1b9e46c526a7dbe800a8e6a7423d96f16cca44e1ac0610b13b`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdadde7749a61c1e452864079f7e483484220f0ae3fa7f7bd7244e01c51564e`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c305401f02bde38a326c77b9088b6a7a2a01a5babed79ec98c244a5c6006588`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4957be82dbf1c2d1fdab2d9f4604991c3bbf7c9ff6fa46efeee39dd1086ed3`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:b398d37048c28628fc4321bc540446f3ee812011e7c9a16d3dd19009eb5884ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:905989f3a6b51bca9680b352fd5a4cc271c355fe1f97bc891436699220a6dc15
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107424291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc5b97cb5590745b1ceee71f3fa39e6182c08aa0778a902b59edef61785e388`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 19 Nov 2021 23:16:56 GMT
RUN cmd /S /C #(nop) COPY file:cb348e461b3d96ac80f8049551e5a2f64ad993b7e0766d87ab5ab5fdd94589b6 in C:\nats-server.exe 
# Fri, 19 Nov 2021 23:16:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:17:00 GMT
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
	-	`sha256:ba9a2a1dd5182104e73dd0b99871b9421cef25f8493a107f6c5851e604a0c805`  
		Last Modified: Fri, 19 Nov 2021 23:20:49 GMT  
		Size: 4.6 MB (4634936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea376684ddbfce1b9e46c526a7dbe800a8e6a7423d96f16cca44e1ac0610b13b`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdadde7749a61c1e452864079f7e483484220f0ae3fa7f7bd7244e01c51564e`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c305401f02bde38a326c77b9088b6a7a2a01a5babed79ec98c244a5c6006588`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4957be82dbf1c2d1fdab2d9f4604991c3bbf7c9ff6fa46efeee39dd1086ed3`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:85deef40c1d54f42dc99207f542c78162bd9cee6cccc9ee62d4a68e5e8155e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:4c4e804a1650e91fbfbf07efa44afc479755a6ace2ab57050b950475ddc93442
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acde872f934ff8c9ad3505d331c4827e3285ad4314e92f69ae0abe1d455ff77f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:42:18 GMT
COPY file:148643ead7a90f9c3416e4455a70bf4638bf9c77005e258d6ec4dcf605560028 in /nats-server 
# Fri, 19 Nov 2021 23:42:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:42:19 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:42:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe89a8c692b8dabfd4ac3062f9232c753d0c2db79be5dca06811cfd9dbcbdc1c`  
		Last Modified: Fri, 19 Nov 2021 23:43:09 GMT  
		Size: 4.6 MB (4575375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5645a0f80ddde9dcce3a4aecfc7a9ab65b20f5c4fcab9897e75302b2b4bf404`  
		Last Modified: Fri, 19 Nov 2021 23:43:08 GMT  
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
$ docker pull nats@sha256:c3e6b4d51c17fa68c6e4c70ce519e1035c89a232b96c9ca59d1aa9932f7b4687
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514f8bdd0d1db9adfcc78eb1a00c34ad3eefd5e7135852bcd277023ebe30f0c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:48132b2177bf3ca4d978b99a66b7a228cae6937450ee016ac753a4c4ffb567a6 in /nats-server 
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:22:49 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:49 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:22:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:92ac13b7cd582c606500bbb3364dbf1a7e0a85030b4deeabfba3a44d94b2c66e`  
		Last Modified: Fri, 19 Nov 2021 23:25:11 GMT  
		Size: 4.2 MB (4235210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b8c68cfe1eeaa6a60a3863fceb15216ecc6b46b1ff00255bffe9a638b3b768`  
		Last Modified: Fri, 19 Nov 2021 23:25:08 GMT  
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
$ docker pull nats@sha256:7e0428dba71a73c21cf18a83990daccd695802963a5066161b005c0fa2aee2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:8d78380851c70c44eea273d3aaff4c424ad191c679708c42bc171878d9500fac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711490510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a201f7790c138296ade85180ca7a6fb58d90b5c11b47fcf00561b8c1f8912412`
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
# Fri, 19 Nov 2021 23:14:14 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:14:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.5/nats-server-v2.6.5-windows-amd64.zip
# Fri, 19 Nov 2021 23:14:16 GMT
ENV NATS_SERVER_SHASUM=0aba30ddd630fddd7ecd49c18a0666b0f78386d2e623d701c00f0b18351e4529
# Fri, 19 Nov 2021 23:15:20 GMT
RUN Set-PSDebug -Trace 2
# Fri, 19 Nov 2021 23:16:41 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 19 Nov 2021 23:16:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:43 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:44 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:16:45 GMT
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
	-	`sha256:66ee32c5b0f8d0e25d55f2155058787d912af133c85d6e693f1b829b4247b631`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8dc647b82c6c8b1c1e07221e4f9d39e1a2ab5d5ba52da0c81f7787c5ae5999`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509fa0ab98575757356ace0336d5e3c425b48de9137d943b065c182545960785`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3745b3fbaa0d3f89421d0a9f02890206569705c76260367007a8ec3958a6f8ce`  
		Last Modified: Fri, 19 Nov 2021 23:20:33 GMT  
		Size: 368.7 KB (368732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2736dce76765262fdaa9b8f1cb72e12a54be251a592faebc20887d9ffdf021`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 5.0 MB (4987456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d319abe61026f65f2bd4bfc0ced76d5d6e68d5636948772c2ecbae70bf85da2`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786db0a3988ce428787cfe588a08d3b9c1c897c7ebfc24a579e54bb19f546fcb`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab8b864113ad6fef653342907be67b1f880316a291dde505550e5eddac3e870`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d6b4b4f014b764cb75cc10988c8c9fcc2c6943f0c7ba3f24115f2bedf602c5`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:6ab359fa36226d90c1aafd6638846ec1a0bd53484f30e04842e1efc41cf6eda1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278475967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f606e5e79c17f6ad740d2394f5ab64d8d281e6ccd57599ec6138371bc5578`
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
# Fri, 19 Nov 2021 23:17:07 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:17:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.5/nats-server-v2.6.5-windows-amd64.zip
# Fri, 19 Nov 2021 23:17:09 GMT
ENV NATS_SERVER_SHASUM=0aba30ddd630fddd7ecd49c18a0666b0f78386d2e623d701c00f0b18351e4529
# Fri, 19 Nov 2021 23:18:18 GMT
RUN Set-PSDebug -Trace 2
# Fri, 19 Nov 2021 23:19:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 19 Nov 2021 23:19:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:19:50 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:19:51 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:19:52 GMT
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
	-	`sha256:f6e3554a67b57f2a9aa17f80c9675be949b9372a709bb0f7fdf1dc7a3954a8a7`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eeda6412c8ef4a5587519bccde86a7d03ede9e3d88c0c2ee7b4edaa24a9d25c`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ca635911cf274a387f2d940588371058db1949e9b10f093b7fd1da6d1a30fc`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672969c6f430af654d3a77eecadafcc5149020360859599bfac5eadbdf52388`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 360.6 KB (360571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf6b57aeb7766a77d7c0ba1400216f6aa339f8607b7fd2302e8b30f4ff8f140`  
		Last Modified: Fri, 19 Nov 2021 23:21:03 GMT  
		Size: 5.0 MB (5011302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b11540a8a97137b66a8f28531a07e5ec3db99e327ab93821000188e02bc98bf`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca98906943111b8c8be9af092d51081d9ff4e7ff0613c220636cb567764349`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d92f48165676375740936c62ff6e30aca04671b4204790a0b8c7a481a64e77`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5b6e62a393187d7daea5065dc7e4285f6ff881d7575c53739d47f068b86803`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:181df5142aea41aa0901309ffd02c00ae7926e3af39dbda47800de6129b6945b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:8d78380851c70c44eea273d3aaff4c424ad191c679708c42bc171878d9500fac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711490510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a201f7790c138296ade85180ca7a6fb58d90b5c11b47fcf00561b8c1f8912412`
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
# Fri, 19 Nov 2021 23:14:14 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:14:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.5/nats-server-v2.6.5-windows-amd64.zip
# Fri, 19 Nov 2021 23:14:16 GMT
ENV NATS_SERVER_SHASUM=0aba30ddd630fddd7ecd49c18a0666b0f78386d2e623d701c00f0b18351e4529
# Fri, 19 Nov 2021 23:15:20 GMT
RUN Set-PSDebug -Trace 2
# Fri, 19 Nov 2021 23:16:41 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 19 Nov 2021 23:16:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:43 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:44 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:16:45 GMT
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
	-	`sha256:66ee32c5b0f8d0e25d55f2155058787d912af133c85d6e693f1b829b4247b631`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8dc647b82c6c8b1c1e07221e4f9d39e1a2ab5d5ba52da0c81f7787c5ae5999`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509fa0ab98575757356ace0336d5e3c425b48de9137d943b065c182545960785`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3745b3fbaa0d3f89421d0a9f02890206569705c76260367007a8ec3958a6f8ce`  
		Last Modified: Fri, 19 Nov 2021 23:20:33 GMT  
		Size: 368.7 KB (368732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2736dce76765262fdaa9b8f1cb72e12a54be251a592faebc20887d9ffdf021`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 5.0 MB (4987456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d319abe61026f65f2bd4bfc0ced76d5d6e68d5636948772c2ecbae70bf85da2`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786db0a3988ce428787cfe588a08d3b9c1c897c7ebfc24a579e54bb19f546fcb`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab8b864113ad6fef653342907be67b1f880316a291dde505550e5eddac3e870`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d6b4b4f014b764cb75cc10988c8c9fcc2c6943f0c7ba3f24115f2bedf602c5`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:630d3ef14aa6aec84c68d0bd075afde8c6649479ff6be8acd513d89d1bce6db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:6ab359fa36226d90c1aafd6638846ec1a0bd53484f30e04842e1efc41cf6eda1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278475967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f606e5e79c17f6ad740d2394f5ab64d8d281e6ccd57599ec6138371bc5578`
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
# Fri, 19 Nov 2021 23:17:07 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:17:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.5/nats-server-v2.6.5-windows-amd64.zip
# Fri, 19 Nov 2021 23:17:09 GMT
ENV NATS_SERVER_SHASUM=0aba30ddd630fddd7ecd49c18a0666b0f78386d2e623d701c00f0b18351e4529
# Fri, 19 Nov 2021 23:18:18 GMT
RUN Set-PSDebug -Trace 2
# Fri, 19 Nov 2021 23:19:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 19 Nov 2021 23:19:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:19:50 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:19:51 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:19:52 GMT
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
	-	`sha256:f6e3554a67b57f2a9aa17f80c9675be949b9372a709bb0f7fdf1dc7a3954a8a7`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eeda6412c8ef4a5587519bccde86a7d03ede9e3d88c0c2ee7b4edaa24a9d25c`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ca635911cf274a387f2d940588371058db1949e9b10f093b7fd1da6d1a30fc`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672969c6f430af654d3a77eecadafcc5149020360859599bfac5eadbdf52388`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 360.6 KB (360571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf6b57aeb7766a77d7c0ba1400216f6aa339f8607b7fd2302e8b30f4ff8f140`  
		Last Modified: Fri, 19 Nov 2021 23:21:03 GMT  
		Size: 5.0 MB (5011302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b11540a8a97137b66a8f28531a07e5ec3db99e327ab93821000188e02bc98bf`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca98906943111b8c8be9af092d51081d9ff4e7ff0613c220636cb567764349`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d92f48165676375740936c62ff6e30aca04671b4204790a0b8c7a481a64e77`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5b6e62a393187d7daea5065dc7e4285f6ff881d7575c53739d47f068b86803`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6`

```console
$ docker pull nats@sha256:dba2bbbe7e9dd7c39a43a53a5d4beeaae542ee98dae82b64aed895c6589e8f21
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
$ docker pull nats@sha256:4c4e804a1650e91fbfbf07efa44afc479755a6ace2ab57050b950475ddc93442
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acde872f934ff8c9ad3505d331c4827e3285ad4314e92f69ae0abe1d455ff77f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:42:18 GMT
COPY file:148643ead7a90f9c3416e4455a70bf4638bf9c77005e258d6ec4dcf605560028 in /nats-server 
# Fri, 19 Nov 2021 23:42:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:42:19 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:42:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe89a8c692b8dabfd4ac3062f9232c753d0c2db79be5dca06811cfd9dbcbdc1c`  
		Last Modified: Fri, 19 Nov 2021 23:43:09 GMT  
		Size: 4.6 MB (4575375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5645a0f80ddde9dcce3a4aecfc7a9ab65b20f5c4fcab9897e75302b2b4bf404`  
		Last Modified: Fri, 19 Nov 2021 23:43:08 GMT  
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
$ docker pull nats@sha256:c3e6b4d51c17fa68c6e4c70ce519e1035c89a232b96c9ca59d1aa9932f7b4687
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514f8bdd0d1db9adfcc78eb1a00c34ad3eefd5e7135852bcd277023ebe30f0c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:48132b2177bf3ca4d978b99a66b7a228cae6937450ee016ac753a4c4ffb567a6 in /nats-server 
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:22:49 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:49 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:22:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:92ac13b7cd582c606500bbb3364dbf1a7e0a85030b4deeabfba3a44d94b2c66e`  
		Last Modified: Fri, 19 Nov 2021 23:25:11 GMT  
		Size: 4.2 MB (4235210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b8c68cfe1eeaa6a60a3863fceb15216ecc6b46b1ff00255bffe9a638b3b768`  
		Last Modified: Fri, 19 Nov 2021 23:25:08 GMT  
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
$ docker pull nats@sha256:905989f3a6b51bca9680b352fd5a4cc271c355fe1f97bc891436699220a6dc15
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107424291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc5b97cb5590745b1ceee71f3fa39e6182c08aa0778a902b59edef61785e388`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 19 Nov 2021 23:16:56 GMT
RUN cmd /S /C #(nop) COPY file:cb348e461b3d96ac80f8049551e5a2f64ad993b7e0766d87ab5ab5fdd94589b6 in C:\nats-server.exe 
# Fri, 19 Nov 2021 23:16:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:17:00 GMT
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
	-	`sha256:ba9a2a1dd5182104e73dd0b99871b9421cef25f8493a107f6c5851e604a0c805`  
		Last Modified: Fri, 19 Nov 2021 23:20:49 GMT  
		Size: 4.6 MB (4634936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea376684ddbfce1b9e46c526a7dbe800a8e6a7423d96f16cca44e1ac0610b13b`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdadde7749a61c1e452864079f7e483484220f0ae3fa7f7bd7244e01c51564e`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c305401f02bde38a326c77b9088b6a7a2a01a5babed79ec98c244a5c6006588`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4957be82dbf1c2d1fdab2d9f4604991c3bbf7c9ff6fa46efeee39dd1086ed3`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-alpine`

```console
$ docker pull nats@sha256:7f36c22a7e0cb76ce2e06235022b20aa5ed52736f6c363dbeeaca8dab69ecf4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6-alpine` - linux; amd64

```console
$ docker pull nats@sha256:06e24692a80300ca5bd9671ab4ab80c1b048d6887c18ca32aa073887fa1fd359
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7686268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e413df78b5a846b18ac33bc0aaf255770267bebcbc0618ab7f297560f31587ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:41:57 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:42:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:42:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:42:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:42:01 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:42:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a26961feb3858523c0a38d5decbabc61ce2fdecfc03c3f118db9ae38e2a2081`  
		Last Modified: Fri, 19 Nov 2021 23:42:44 GMT  
		Size: 4.9 MB (4862314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0833c09ffb63b8898f80abd7a90f5bdecefb7a10a771e96779648ca03137643`  
		Last Modified: Fri, 19 Nov 2021 23:42:43 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2219d94c89a69f8eb02e5fcbb9cc203e77bbc833a538b83c6cff697ea6e410e3`  
		Last Modified: Fri, 19 Nov 2021 23:42:43 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:1492db6aaab11ff0408a18ccd0b9c4e05a6a09bf27b989ba06df650f3c4daa35
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5380995e0b783165a76fcab9a147c18e8154d4e6cc310236294f54d9adeba4e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:22:19 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:22:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:22:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:22:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:22:24 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:22:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0676a94d1c25310146837eb95390f211b55367bbbc41c86020b28b00375b7baf`  
		Last Modified: Fri, 19 Nov 2021 23:24:33 GMT  
		Size: 4.5 MB (4516168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f024b09adefc2b21cfad2f2279a279604f371cfe6bbfcf1dd11f412d031a7e5d`  
		Last Modified: Fri, 19 Nov 2021 23:24:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c6d7089949b487c17d10a9a94548058005f51c80e94429659ff9dd9093a4cf`  
		Last Modified: Fri, 19 Nov 2021 23:24:31 GMT  
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
$ docker pull nats@sha256:7f36c22a7e0cb76ce2e06235022b20aa5ed52736f6c363dbeeaca8dab69ecf4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6-alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:06e24692a80300ca5bd9671ab4ab80c1b048d6887c18ca32aa073887fa1fd359
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7686268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e413df78b5a846b18ac33bc0aaf255770267bebcbc0618ab7f297560f31587ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:41:57 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:42:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:42:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:42:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:42:01 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:42:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a26961feb3858523c0a38d5decbabc61ce2fdecfc03c3f118db9ae38e2a2081`  
		Last Modified: Fri, 19 Nov 2021 23:42:44 GMT  
		Size: 4.9 MB (4862314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0833c09ffb63b8898f80abd7a90f5bdecefb7a10a771e96779648ca03137643`  
		Last Modified: Fri, 19 Nov 2021 23:42:43 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2219d94c89a69f8eb02e5fcbb9cc203e77bbc833a538b83c6cff697ea6e410e3`  
		Last Modified: Fri, 19 Nov 2021 23:42:43 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:1492db6aaab11ff0408a18ccd0b9c4e05a6a09bf27b989ba06df650f3c4daa35
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5380995e0b783165a76fcab9a147c18e8154d4e6cc310236294f54d9adeba4e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:22:19 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:22:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:22:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:22:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:22:24 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:22:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0676a94d1c25310146837eb95390f211b55367bbbc41c86020b28b00375b7baf`  
		Last Modified: Fri, 19 Nov 2021 23:24:33 GMT  
		Size: 4.5 MB (4516168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f024b09adefc2b21cfad2f2279a279604f371cfe6bbfcf1dd11f412d031a7e5d`  
		Last Modified: Fri, 19 Nov 2021 23:24:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c6d7089949b487c17d10a9a94548058005f51c80e94429659ff9dd9093a4cf`  
		Last Modified: Fri, 19 Nov 2021 23:24:31 GMT  
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
$ docker pull nats@sha256:85deef40c1d54f42dc99207f542c78162bd9cee6cccc9ee62d4a68e5e8155e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6-linux` - linux; amd64

```console
$ docker pull nats@sha256:4c4e804a1650e91fbfbf07efa44afc479755a6ace2ab57050b950475ddc93442
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acde872f934ff8c9ad3505d331c4827e3285ad4314e92f69ae0abe1d455ff77f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:42:18 GMT
COPY file:148643ead7a90f9c3416e4455a70bf4638bf9c77005e258d6ec4dcf605560028 in /nats-server 
# Fri, 19 Nov 2021 23:42:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:42:19 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:42:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe89a8c692b8dabfd4ac3062f9232c753d0c2db79be5dca06811cfd9dbcbdc1c`  
		Last Modified: Fri, 19 Nov 2021 23:43:09 GMT  
		Size: 4.6 MB (4575375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5645a0f80ddde9dcce3a4aecfc7a9ab65b20f5c4fcab9897e75302b2b4bf404`  
		Last Modified: Fri, 19 Nov 2021 23:43:08 GMT  
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
$ docker pull nats@sha256:c3e6b4d51c17fa68c6e4c70ce519e1035c89a232b96c9ca59d1aa9932f7b4687
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514f8bdd0d1db9adfcc78eb1a00c34ad3eefd5e7135852bcd277023ebe30f0c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:48132b2177bf3ca4d978b99a66b7a228cae6937450ee016ac753a4c4ffb567a6 in /nats-server 
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:22:49 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:49 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:22:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:92ac13b7cd582c606500bbb3364dbf1a7e0a85030b4deeabfba3a44d94b2c66e`  
		Last Modified: Fri, 19 Nov 2021 23:25:11 GMT  
		Size: 4.2 MB (4235210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b8c68cfe1eeaa6a60a3863fceb15216ecc6b46b1ff00255bffe9a638b3b768`  
		Last Modified: Fri, 19 Nov 2021 23:25:08 GMT  
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
$ docker pull nats@sha256:b398d37048c28628fc4321bc540446f3ee812011e7c9a16d3dd19009eb5884ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6-nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:905989f3a6b51bca9680b352fd5a4cc271c355fe1f97bc891436699220a6dc15
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107424291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc5b97cb5590745b1ceee71f3fa39e6182c08aa0778a902b59edef61785e388`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 19 Nov 2021 23:16:56 GMT
RUN cmd /S /C #(nop) COPY file:cb348e461b3d96ac80f8049551e5a2f64ad993b7e0766d87ab5ab5fdd94589b6 in C:\nats-server.exe 
# Fri, 19 Nov 2021 23:16:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:17:00 GMT
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
	-	`sha256:ba9a2a1dd5182104e73dd0b99871b9421cef25f8493a107f6c5851e604a0c805`  
		Last Modified: Fri, 19 Nov 2021 23:20:49 GMT  
		Size: 4.6 MB (4634936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea376684ddbfce1b9e46c526a7dbe800a8e6a7423d96f16cca44e1ac0610b13b`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdadde7749a61c1e452864079f7e483484220f0ae3fa7f7bd7244e01c51564e`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c305401f02bde38a326c77b9088b6a7a2a01a5babed79ec98c244a5c6006588`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4957be82dbf1c2d1fdab2d9f4604991c3bbf7c9ff6fa46efeee39dd1086ed3`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-nanoserver-1809`

```console
$ docker pull nats@sha256:b398d37048c28628fc4321bc540446f3ee812011e7c9a16d3dd19009eb5884ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6-nanoserver-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:905989f3a6b51bca9680b352fd5a4cc271c355fe1f97bc891436699220a6dc15
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107424291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc5b97cb5590745b1ceee71f3fa39e6182c08aa0778a902b59edef61785e388`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 19 Nov 2021 23:16:56 GMT
RUN cmd /S /C #(nop) COPY file:cb348e461b3d96ac80f8049551e5a2f64ad993b7e0766d87ab5ab5fdd94589b6 in C:\nats-server.exe 
# Fri, 19 Nov 2021 23:16:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:17:00 GMT
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
	-	`sha256:ba9a2a1dd5182104e73dd0b99871b9421cef25f8493a107f6c5851e604a0c805`  
		Last Modified: Fri, 19 Nov 2021 23:20:49 GMT  
		Size: 4.6 MB (4634936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea376684ddbfce1b9e46c526a7dbe800a8e6a7423d96f16cca44e1ac0610b13b`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdadde7749a61c1e452864079f7e483484220f0ae3fa7f7bd7244e01c51564e`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c305401f02bde38a326c77b9088b6a7a2a01a5babed79ec98c244a5c6006588`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4957be82dbf1c2d1fdab2d9f4604991c3bbf7c9ff6fa46efeee39dd1086ed3`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-scratch`

```console
$ docker pull nats@sha256:85deef40c1d54f42dc99207f542c78162bd9cee6cccc9ee62d4a68e5e8155e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6-scratch` - linux; amd64

```console
$ docker pull nats@sha256:4c4e804a1650e91fbfbf07efa44afc479755a6ace2ab57050b950475ddc93442
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acde872f934ff8c9ad3505d331c4827e3285ad4314e92f69ae0abe1d455ff77f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:42:18 GMT
COPY file:148643ead7a90f9c3416e4455a70bf4638bf9c77005e258d6ec4dcf605560028 in /nats-server 
# Fri, 19 Nov 2021 23:42:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:42:19 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:42:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe89a8c692b8dabfd4ac3062f9232c753d0c2db79be5dca06811cfd9dbcbdc1c`  
		Last Modified: Fri, 19 Nov 2021 23:43:09 GMT  
		Size: 4.6 MB (4575375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5645a0f80ddde9dcce3a4aecfc7a9ab65b20f5c4fcab9897e75302b2b4bf404`  
		Last Modified: Fri, 19 Nov 2021 23:43:08 GMT  
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
$ docker pull nats@sha256:c3e6b4d51c17fa68c6e4c70ce519e1035c89a232b96c9ca59d1aa9932f7b4687
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514f8bdd0d1db9adfcc78eb1a00c34ad3eefd5e7135852bcd277023ebe30f0c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:48132b2177bf3ca4d978b99a66b7a228cae6937450ee016ac753a4c4ffb567a6 in /nats-server 
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:22:49 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:49 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:22:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:92ac13b7cd582c606500bbb3364dbf1a7e0a85030b4deeabfba3a44d94b2c66e`  
		Last Modified: Fri, 19 Nov 2021 23:25:11 GMT  
		Size: 4.2 MB (4235210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b8c68cfe1eeaa6a60a3863fceb15216ecc6b46b1ff00255bffe9a638b3b768`  
		Last Modified: Fri, 19 Nov 2021 23:25:08 GMT  
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
$ docker pull nats@sha256:7e0428dba71a73c21cf18a83990daccd695802963a5066161b005c0fa2aee2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `nats:2.6-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:8d78380851c70c44eea273d3aaff4c424ad191c679708c42bc171878d9500fac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711490510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a201f7790c138296ade85180ca7a6fb58d90b5c11b47fcf00561b8c1f8912412`
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
# Fri, 19 Nov 2021 23:14:14 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:14:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.5/nats-server-v2.6.5-windows-amd64.zip
# Fri, 19 Nov 2021 23:14:16 GMT
ENV NATS_SERVER_SHASUM=0aba30ddd630fddd7ecd49c18a0666b0f78386d2e623d701c00f0b18351e4529
# Fri, 19 Nov 2021 23:15:20 GMT
RUN Set-PSDebug -Trace 2
# Fri, 19 Nov 2021 23:16:41 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 19 Nov 2021 23:16:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:43 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:44 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:16:45 GMT
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
	-	`sha256:66ee32c5b0f8d0e25d55f2155058787d912af133c85d6e693f1b829b4247b631`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8dc647b82c6c8b1c1e07221e4f9d39e1a2ab5d5ba52da0c81f7787c5ae5999`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509fa0ab98575757356ace0336d5e3c425b48de9137d943b065c182545960785`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3745b3fbaa0d3f89421d0a9f02890206569705c76260367007a8ec3958a6f8ce`  
		Last Modified: Fri, 19 Nov 2021 23:20:33 GMT  
		Size: 368.7 KB (368732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2736dce76765262fdaa9b8f1cb72e12a54be251a592faebc20887d9ffdf021`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 5.0 MB (4987456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d319abe61026f65f2bd4bfc0ced76d5d6e68d5636948772c2ecbae70bf85da2`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786db0a3988ce428787cfe588a08d3b9c1c897c7ebfc24a579e54bb19f546fcb`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab8b864113ad6fef653342907be67b1f880316a291dde505550e5eddac3e870`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d6b4b4f014b764cb75cc10988c8c9fcc2c6943f0c7ba3f24115f2bedf602c5`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:6ab359fa36226d90c1aafd6638846ec1a0bd53484f30e04842e1efc41cf6eda1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278475967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f606e5e79c17f6ad740d2394f5ab64d8d281e6ccd57599ec6138371bc5578`
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
# Fri, 19 Nov 2021 23:17:07 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:17:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.5/nats-server-v2.6.5-windows-amd64.zip
# Fri, 19 Nov 2021 23:17:09 GMT
ENV NATS_SERVER_SHASUM=0aba30ddd630fddd7ecd49c18a0666b0f78386d2e623d701c00f0b18351e4529
# Fri, 19 Nov 2021 23:18:18 GMT
RUN Set-PSDebug -Trace 2
# Fri, 19 Nov 2021 23:19:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 19 Nov 2021 23:19:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:19:50 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:19:51 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:19:52 GMT
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
	-	`sha256:f6e3554a67b57f2a9aa17f80c9675be949b9372a709bb0f7fdf1dc7a3954a8a7`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eeda6412c8ef4a5587519bccde86a7d03ede9e3d88c0c2ee7b4edaa24a9d25c`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ca635911cf274a387f2d940588371058db1949e9b10f093b7fd1da6d1a30fc`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672969c6f430af654d3a77eecadafcc5149020360859599bfac5eadbdf52388`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 360.6 KB (360571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf6b57aeb7766a77d7c0ba1400216f6aa339f8607b7fd2302e8b30f4ff8f140`  
		Last Modified: Fri, 19 Nov 2021 23:21:03 GMT  
		Size: 5.0 MB (5011302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b11540a8a97137b66a8f28531a07e5ec3db99e327ab93821000188e02bc98bf`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca98906943111b8c8be9af092d51081d9ff4e7ff0613c220636cb567764349`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d92f48165676375740936c62ff6e30aca04671b4204790a0b8c7a481a64e77`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5b6e62a393187d7daea5065dc7e4285f6ff881d7575c53739d47f068b86803`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-windowsservercore-1809`

```console
$ docker pull nats@sha256:181df5142aea41aa0901309ffd02c00ae7926e3af39dbda47800de6129b6945b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:8d78380851c70c44eea273d3aaff4c424ad191c679708c42bc171878d9500fac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711490510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a201f7790c138296ade85180ca7a6fb58d90b5c11b47fcf00561b8c1f8912412`
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
# Fri, 19 Nov 2021 23:14:14 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:14:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.5/nats-server-v2.6.5-windows-amd64.zip
# Fri, 19 Nov 2021 23:14:16 GMT
ENV NATS_SERVER_SHASUM=0aba30ddd630fddd7ecd49c18a0666b0f78386d2e623d701c00f0b18351e4529
# Fri, 19 Nov 2021 23:15:20 GMT
RUN Set-PSDebug -Trace 2
# Fri, 19 Nov 2021 23:16:41 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 19 Nov 2021 23:16:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:43 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:44 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:16:45 GMT
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
	-	`sha256:66ee32c5b0f8d0e25d55f2155058787d912af133c85d6e693f1b829b4247b631`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8dc647b82c6c8b1c1e07221e4f9d39e1a2ab5d5ba52da0c81f7787c5ae5999`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509fa0ab98575757356ace0336d5e3c425b48de9137d943b065c182545960785`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3745b3fbaa0d3f89421d0a9f02890206569705c76260367007a8ec3958a6f8ce`  
		Last Modified: Fri, 19 Nov 2021 23:20:33 GMT  
		Size: 368.7 KB (368732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2736dce76765262fdaa9b8f1cb72e12a54be251a592faebc20887d9ffdf021`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 5.0 MB (4987456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d319abe61026f65f2bd4bfc0ced76d5d6e68d5636948772c2ecbae70bf85da2`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786db0a3988ce428787cfe588a08d3b9c1c897c7ebfc24a579e54bb19f546fcb`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab8b864113ad6fef653342907be67b1f880316a291dde505550e5eddac3e870`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d6b4b4f014b764cb75cc10988c8c9fcc2c6943f0c7ba3f24115f2bedf602c5`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:630d3ef14aa6aec84c68d0bd075afde8c6649479ff6be8acd513d89d1bce6db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `nats:2.6-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:6ab359fa36226d90c1aafd6638846ec1a0bd53484f30e04842e1efc41cf6eda1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278475967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f606e5e79c17f6ad740d2394f5ab64d8d281e6ccd57599ec6138371bc5578`
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
# Fri, 19 Nov 2021 23:17:07 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:17:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.5/nats-server-v2.6.5-windows-amd64.zip
# Fri, 19 Nov 2021 23:17:09 GMT
ENV NATS_SERVER_SHASUM=0aba30ddd630fddd7ecd49c18a0666b0f78386d2e623d701c00f0b18351e4529
# Fri, 19 Nov 2021 23:18:18 GMT
RUN Set-PSDebug -Trace 2
# Fri, 19 Nov 2021 23:19:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 19 Nov 2021 23:19:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:19:50 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:19:51 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:19:52 GMT
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
	-	`sha256:f6e3554a67b57f2a9aa17f80c9675be949b9372a709bb0f7fdf1dc7a3954a8a7`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eeda6412c8ef4a5587519bccde86a7d03ede9e3d88c0c2ee7b4edaa24a9d25c`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ca635911cf274a387f2d940588371058db1949e9b10f093b7fd1da6d1a30fc`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672969c6f430af654d3a77eecadafcc5149020360859599bfac5eadbdf52388`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 360.6 KB (360571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf6b57aeb7766a77d7c0ba1400216f6aa339f8607b7fd2302e8b30f4ff8f140`  
		Last Modified: Fri, 19 Nov 2021 23:21:03 GMT  
		Size: 5.0 MB (5011302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b11540a8a97137b66a8f28531a07e5ec3db99e327ab93821000188e02bc98bf`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca98906943111b8c8be9af092d51081d9ff4e7ff0613c220636cb567764349`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d92f48165676375740936c62ff6e30aca04671b4204790a0b8c7a481a64e77`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5b6e62a393187d7daea5065dc7e4285f6ff881d7575c53739d47f068b86803`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.5`

```console
$ docker pull nats@sha256:dba2bbbe7e9dd7c39a43a53a5d4beeaae542ee98dae82b64aed895c6589e8f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6.5` - linux; amd64

```console
$ docker pull nats@sha256:4c4e804a1650e91fbfbf07efa44afc479755a6ace2ab57050b950475ddc93442
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acde872f934ff8c9ad3505d331c4827e3285ad4314e92f69ae0abe1d455ff77f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:42:18 GMT
COPY file:148643ead7a90f9c3416e4455a70bf4638bf9c77005e258d6ec4dcf605560028 in /nats-server 
# Fri, 19 Nov 2021 23:42:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:42:19 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:42:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe89a8c692b8dabfd4ac3062f9232c753d0c2db79be5dca06811cfd9dbcbdc1c`  
		Last Modified: Fri, 19 Nov 2021 23:43:09 GMT  
		Size: 4.6 MB (4575375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5645a0f80ddde9dcce3a4aecfc7a9ab65b20f5c4fcab9897e75302b2b4bf404`  
		Last Modified: Fri, 19 Nov 2021 23:43:08 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

### `nats:2.6.5` - linux; arm variant v7

```console
$ docker pull nats@sha256:c3e6b4d51c17fa68c6e4c70ce519e1035c89a232b96c9ca59d1aa9932f7b4687
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514f8bdd0d1db9adfcc78eb1a00c34ad3eefd5e7135852bcd277023ebe30f0c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:48132b2177bf3ca4d978b99a66b7a228cae6937450ee016ac753a4c4ffb567a6 in /nats-server 
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:22:49 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:49 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:22:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:92ac13b7cd582c606500bbb3364dbf1a7e0a85030b4deeabfba3a44d94b2c66e`  
		Last Modified: Fri, 19 Nov 2021 23:25:11 GMT  
		Size: 4.2 MB (4235210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b8c68cfe1eeaa6a60a3863fceb15216ecc6b46b1ff00255bffe9a638b3b768`  
		Last Modified: Fri, 19 Nov 2021 23:25:08 GMT  
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

### `nats:2.6.5` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:905989f3a6b51bca9680b352fd5a4cc271c355fe1f97bc891436699220a6dc15
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107424291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc5b97cb5590745b1ceee71f3fa39e6182c08aa0778a902b59edef61785e388`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 19 Nov 2021 23:16:56 GMT
RUN cmd /S /C #(nop) COPY file:cb348e461b3d96ac80f8049551e5a2f64ad993b7e0766d87ab5ab5fdd94589b6 in C:\nats-server.exe 
# Fri, 19 Nov 2021 23:16:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:17:00 GMT
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
	-	`sha256:ba9a2a1dd5182104e73dd0b99871b9421cef25f8493a107f6c5851e604a0c805`  
		Last Modified: Fri, 19 Nov 2021 23:20:49 GMT  
		Size: 4.6 MB (4634936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea376684ddbfce1b9e46c526a7dbe800a8e6a7423d96f16cca44e1ac0610b13b`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdadde7749a61c1e452864079f7e483484220f0ae3fa7f7bd7244e01c51564e`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c305401f02bde38a326c77b9088b6a7a2a01a5babed79ec98c244a5c6006588`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4957be82dbf1c2d1fdab2d9f4604991c3bbf7c9ff6fa46efeee39dd1086ed3`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.5-alpine`

```console
$ docker pull nats@sha256:7f36c22a7e0cb76ce2e06235022b20aa5ed52736f6c363dbeeaca8dab69ecf4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6.5-alpine` - linux; amd64

```console
$ docker pull nats@sha256:06e24692a80300ca5bd9671ab4ab80c1b048d6887c18ca32aa073887fa1fd359
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7686268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e413df78b5a846b18ac33bc0aaf255770267bebcbc0618ab7f297560f31587ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:41:57 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:42:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:42:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:42:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:42:01 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:42:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a26961feb3858523c0a38d5decbabc61ce2fdecfc03c3f118db9ae38e2a2081`  
		Last Modified: Fri, 19 Nov 2021 23:42:44 GMT  
		Size: 4.9 MB (4862314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0833c09ffb63b8898f80abd7a90f5bdecefb7a10a771e96779648ca03137643`  
		Last Modified: Fri, 19 Nov 2021 23:42:43 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2219d94c89a69f8eb02e5fcbb9cc203e77bbc833a538b83c6cff697ea6e410e3`  
		Last Modified: Fri, 19 Nov 2021 23:42:43 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

### `nats:2.6.5-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1492db6aaab11ff0408a18ccd0b9c4e05a6a09bf27b989ba06df650f3c4daa35
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5380995e0b783165a76fcab9a147c18e8154d4e6cc310236294f54d9adeba4e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:22:19 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:22:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:22:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:22:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:22:24 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:22:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0676a94d1c25310146837eb95390f211b55367bbbc41c86020b28b00375b7baf`  
		Last Modified: Fri, 19 Nov 2021 23:24:33 GMT  
		Size: 4.5 MB (4516168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f024b09adefc2b21cfad2f2279a279604f371cfe6bbfcf1dd11f412d031a7e5d`  
		Last Modified: Fri, 19 Nov 2021 23:24:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c6d7089949b487c17d10a9a94548058005f51c80e94429659ff9dd9093a4cf`  
		Last Modified: Fri, 19 Nov 2021 23:24:31 GMT  
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
$ docker pull nats@sha256:7f36c22a7e0cb76ce2e06235022b20aa5ed52736f6c363dbeeaca8dab69ecf4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6.5-alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:06e24692a80300ca5bd9671ab4ab80c1b048d6887c18ca32aa073887fa1fd359
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7686268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e413df78b5a846b18ac33bc0aaf255770267bebcbc0618ab7f297560f31587ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:41:57 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:42:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:42:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:42:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:42:01 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:42:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a26961feb3858523c0a38d5decbabc61ce2fdecfc03c3f118db9ae38e2a2081`  
		Last Modified: Fri, 19 Nov 2021 23:42:44 GMT  
		Size: 4.9 MB (4862314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0833c09ffb63b8898f80abd7a90f5bdecefb7a10a771e96779648ca03137643`  
		Last Modified: Fri, 19 Nov 2021 23:42:43 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2219d94c89a69f8eb02e5fcbb9cc203e77bbc833a538b83c6cff697ea6e410e3`  
		Last Modified: Fri, 19 Nov 2021 23:42:43 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

### `nats:2.6.5-alpine3.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:1492db6aaab11ff0408a18ccd0b9c4e05a6a09bf27b989ba06df650f3c4daa35
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5380995e0b783165a76fcab9a147c18e8154d4e6cc310236294f54d9adeba4e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:22:19 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:22:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:22:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:22:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:22:24 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:22:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0676a94d1c25310146837eb95390f211b55367bbbc41c86020b28b00375b7baf`  
		Last Modified: Fri, 19 Nov 2021 23:24:33 GMT  
		Size: 4.5 MB (4516168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f024b09adefc2b21cfad2f2279a279604f371cfe6bbfcf1dd11f412d031a7e5d`  
		Last Modified: Fri, 19 Nov 2021 23:24:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c6d7089949b487c17d10a9a94548058005f51c80e94429659ff9dd9093a4cf`  
		Last Modified: Fri, 19 Nov 2021 23:24:31 GMT  
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
$ docker pull nats@sha256:85deef40c1d54f42dc99207f542c78162bd9cee6cccc9ee62d4a68e5e8155e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6.5-linux` - linux; amd64

```console
$ docker pull nats@sha256:4c4e804a1650e91fbfbf07efa44afc479755a6ace2ab57050b950475ddc93442
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acde872f934ff8c9ad3505d331c4827e3285ad4314e92f69ae0abe1d455ff77f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:42:18 GMT
COPY file:148643ead7a90f9c3416e4455a70bf4638bf9c77005e258d6ec4dcf605560028 in /nats-server 
# Fri, 19 Nov 2021 23:42:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:42:19 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:42:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe89a8c692b8dabfd4ac3062f9232c753d0c2db79be5dca06811cfd9dbcbdc1c`  
		Last Modified: Fri, 19 Nov 2021 23:43:09 GMT  
		Size: 4.6 MB (4575375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5645a0f80ddde9dcce3a4aecfc7a9ab65b20f5c4fcab9897e75302b2b4bf404`  
		Last Modified: Fri, 19 Nov 2021 23:43:08 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

### `nats:2.6.5-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:c3e6b4d51c17fa68c6e4c70ce519e1035c89a232b96c9ca59d1aa9932f7b4687
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514f8bdd0d1db9adfcc78eb1a00c34ad3eefd5e7135852bcd277023ebe30f0c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:48132b2177bf3ca4d978b99a66b7a228cae6937450ee016ac753a4c4ffb567a6 in /nats-server 
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:22:49 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:49 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:22:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:92ac13b7cd582c606500bbb3364dbf1a7e0a85030b4deeabfba3a44d94b2c66e`  
		Last Modified: Fri, 19 Nov 2021 23:25:11 GMT  
		Size: 4.2 MB (4235210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b8c68cfe1eeaa6a60a3863fceb15216ecc6b46b1ff00255bffe9a638b3b768`  
		Last Modified: Fri, 19 Nov 2021 23:25:08 GMT  
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
$ docker pull nats@sha256:b398d37048c28628fc4321bc540446f3ee812011e7c9a16d3dd19009eb5884ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6.5-nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:905989f3a6b51bca9680b352fd5a4cc271c355fe1f97bc891436699220a6dc15
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107424291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc5b97cb5590745b1ceee71f3fa39e6182c08aa0778a902b59edef61785e388`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 19 Nov 2021 23:16:56 GMT
RUN cmd /S /C #(nop) COPY file:cb348e461b3d96ac80f8049551e5a2f64ad993b7e0766d87ab5ab5fdd94589b6 in C:\nats-server.exe 
# Fri, 19 Nov 2021 23:16:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:17:00 GMT
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
	-	`sha256:ba9a2a1dd5182104e73dd0b99871b9421cef25f8493a107f6c5851e604a0c805`  
		Last Modified: Fri, 19 Nov 2021 23:20:49 GMT  
		Size: 4.6 MB (4634936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea376684ddbfce1b9e46c526a7dbe800a8e6a7423d96f16cca44e1ac0610b13b`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdadde7749a61c1e452864079f7e483484220f0ae3fa7f7bd7244e01c51564e`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c305401f02bde38a326c77b9088b6a7a2a01a5babed79ec98c244a5c6006588`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4957be82dbf1c2d1fdab2d9f4604991c3bbf7c9ff6fa46efeee39dd1086ed3`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.5-nanoserver-1809`

```console
$ docker pull nats@sha256:b398d37048c28628fc4321bc540446f3ee812011e7c9a16d3dd19009eb5884ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6.5-nanoserver-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:905989f3a6b51bca9680b352fd5a4cc271c355fe1f97bc891436699220a6dc15
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107424291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc5b97cb5590745b1ceee71f3fa39e6182c08aa0778a902b59edef61785e388`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 19 Nov 2021 23:16:56 GMT
RUN cmd /S /C #(nop) COPY file:cb348e461b3d96ac80f8049551e5a2f64ad993b7e0766d87ab5ab5fdd94589b6 in C:\nats-server.exe 
# Fri, 19 Nov 2021 23:16:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:17:00 GMT
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
	-	`sha256:ba9a2a1dd5182104e73dd0b99871b9421cef25f8493a107f6c5851e604a0c805`  
		Last Modified: Fri, 19 Nov 2021 23:20:49 GMT  
		Size: 4.6 MB (4634936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea376684ddbfce1b9e46c526a7dbe800a8e6a7423d96f16cca44e1ac0610b13b`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdadde7749a61c1e452864079f7e483484220f0ae3fa7f7bd7244e01c51564e`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c305401f02bde38a326c77b9088b6a7a2a01a5babed79ec98c244a5c6006588`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4957be82dbf1c2d1fdab2d9f4604991c3bbf7c9ff6fa46efeee39dd1086ed3`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.5-scratch`

```console
$ docker pull nats@sha256:85deef40c1d54f42dc99207f542c78162bd9cee6cccc9ee62d4a68e5e8155e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6.5-scratch` - linux; amd64

```console
$ docker pull nats@sha256:4c4e804a1650e91fbfbf07efa44afc479755a6ace2ab57050b950475ddc93442
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acde872f934ff8c9ad3505d331c4827e3285ad4314e92f69ae0abe1d455ff77f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:42:18 GMT
COPY file:148643ead7a90f9c3416e4455a70bf4638bf9c77005e258d6ec4dcf605560028 in /nats-server 
# Fri, 19 Nov 2021 23:42:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:42:19 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:42:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe89a8c692b8dabfd4ac3062f9232c753d0c2db79be5dca06811cfd9dbcbdc1c`  
		Last Modified: Fri, 19 Nov 2021 23:43:09 GMT  
		Size: 4.6 MB (4575375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5645a0f80ddde9dcce3a4aecfc7a9ab65b20f5c4fcab9897e75302b2b4bf404`  
		Last Modified: Fri, 19 Nov 2021 23:43:08 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

### `nats:2.6.5-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:c3e6b4d51c17fa68c6e4c70ce519e1035c89a232b96c9ca59d1aa9932f7b4687
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514f8bdd0d1db9adfcc78eb1a00c34ad3eefd5e7135852bcd277023ebe30f0c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:48132b2177bf3ca4d978b99a66b7a228cae6937450ee016ac753a4c4ffb567a6 in /nats-server 
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:22:49 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:49 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:22:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:92ac13b7cd582c606500bbb3364dbf1a7e0a85030b4deeabfba3a44d94b2c66e`  
		Last Modified: Fri, 19 Nov 2021 23:25:11 GMT  
		Size: 4.2 MB (4235210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b8c68cfe1eeaa6a60a3863fceb15216ecc6b46b1ff00255bffe9a638b3b768`  
		Last Modified: Fri, 19 Nov 2021 23:25:08 GMT  
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
$ docker pull nats@sha256:7e0428dba71a73c21cf18a83990daccd695802963a5066161b005c0fa2aee2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `nats:2.6.5-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:8d78380851c70c44eea273d3aaff4c424ad191c679708c42bc171878d9500fac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711490510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a201f7790c138296ade85180ca7a6fb58d90b5c11b47fcf00561b8c1f8912412`
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
# Fri, 19 Nov 2021 23:14:14 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:14:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.5/nats-server-v2.6.5-windows-amd64.zip
# Fri, 19 Nov 2021 23:14:16 GMT
ENV NATS_SERVER_SHASUM=0aba30ddd630fddd7ecd49c18a0666b0f78386d2e623d701c00f0b18351e4529
# Fri, 19 Nov 2021 23:15:20 GMT
RUN Set-PSDebug -Trace 2
# Fri, 19 Nov 2021 23:16:41 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 19 Nov 2021 23:16:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:43 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:44 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:16:45 GMT
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
	-	`sha256:66ee32c5b0f8d0e25d55f2155058787d912af133c85d6e693f1b829b4247b631`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8dc647b82c6c8b1c1e07221e4f9d39e1a2ab5d5ba52da0c81f7787c5ae5999`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509fa0ab98575757356ace0336d5e3c425b48de9137d943b065c182545960785`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3745b3fbaa0d3f89421d0a9f02890206569705c76260367007a8ec3958a6f8ce`  
		Last Modified: Fri, 19 Nov 2021 23:20:33 GMT  
		Size: 368.7 KB (368732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2736dce76765262fdaa9b8f1cb72e12a54be251a592faebc20887d9ffdf021`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 5.0 MB (4987456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d319abe61026f65f2bd4bfc0ced76d5d6e68d5636948772c2ecbae70bf85da2`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786db0a3988ce428787cfe588a08d3b9c1c897c7ebfc24a579e54bb19f546fcb`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab8b864113ad6fef653342907be67b1f880316a291dde505550e5eddac3e870`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d6b4b4f014b764cb75cc10988c8c9fcc2c6943f0c7ba3f24115f2bedf602c5`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.5-windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:6ab359fa36226d90c1aafd6638846ec1a0bd53484f30e04842e1efc41cf6eda1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278475967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f606e5e79c17f6ad740d2394f5ab64d8d281e6ccd57599ec6138371bc5578`
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
# Fri, 19 Nov 2021 23:17:07 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:17:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.5/nats-server-v2.6.5-windows-amd64.zip
# Fri, 19 Nov 2021 23:17:09 GMT
ENV NATS_SERVER_SHASUM=0aba30ddd630fddd7ecd49c18a0666b0f78386d2e623d701c00f0b18351e4529
# Fri, 19 Nov 2021 23:18:18 GMT
RUN Set-PSDebug -Trace 2
# Fri, 19 Nov 2021 23:19:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 19 Nov 2021 23:19:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:19:50 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:19:51 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:19:52 GMT
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
	-	`sha256:f6e3554a67b57f2a9aa17f80c9675be949b9372a709bb0f7fdf1dc7a3954a8a7`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eeda6412c8ef4a5587519bccde86a7d03ede9e3d88c0c2ee7b4edaa24a9d25c`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ca635911cf274a387f2d940588371058db1949e9b10f093b7fd1da6d1a30fc`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672969c6f430af654d3a77eecadafcc5149020360859599bfac5eadbdf52388`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 360.6 KB (360571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf6b57aeb7766a77d7c0ba1400216f6aa339f8607b7fd2302e8b30f4ff8f140`  
		Last Modified: Fri, 19 Nov 2021 23:21:03 GMT  
		Size: 5.0 MB (5011302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b11540a8a97137b66a8f28531a07e5ec3db99e327ab93821000188e02bc98bf`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca98906943111b8c8be9af092d51081d9ff4e7ff0613c220636cb567764349`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d92f48165676375740936c62ff6e30aca04671b4204790a0b8c7a481a64e77`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5b6e62a393187d7daea5065dc7e4285f6ff881d7575c53739d47f068b86803`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.5-windowsservercore-1809`

```console
$ docker pull nats@sha256:181df5142aea41aa0901309ffd02c00ae7926e3af39dbda47800de6129b6945b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6.5-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:8d78380851c70c44eea273d3aaff4c424ad191c679708c42bc171878d9500fac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711490510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a201f7790c138296ade85180ca7a6fb58d90b5c11b47fcf00561b8c1f8912412`
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
# Fri, 19 Nov 2021 23:14:14 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:14:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.5/nats-server-v2.6.5-windows-amd64.zip
# Fri, 19 Nov 2021 23:14:16 GMT
ENV NATS_SERVER_SHASUM=0aba30ddd630fddd7ecd49c18a0666b0f78386d2e623d701c00f0b18351e4529
# Fri, 19 Nov 2021 23:15:20 GMT
RUN Set-PSDebug -Trace 2
# Fri, 19 Nov 2021 23:16:41 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 19 Nov 2021 23:16:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:43 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:44 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:16:45 GMT
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
	-	`sha256:66ee32c5b0f8d0e25d55f2155058787d912af133c85d6e693f1b829b4247b631`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8dc647b82c6c8b1c1e07221e4f9d39e1a2ab5d5ba52da0c81f7787c5ae5999`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509fa0ab98575757356ace0336d5e3c425b48de9137d943b065c182545960785`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3745b3fbaa0d3f89421d0a9f02890206569705c76260367007a8ec3958a6f8ce`  
		Last Modified: Fri, 19 Nov 2021 23:20:33 GMT  
		Size: 368.7 KB (368732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2736dce76765262fdaa9b8f1cb72e12a54be251a592faebc20887d9ffdf021`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 5.0 MB (4987456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d319abe61026f65f2bd4bfc0ced76d5d6e68d5636948772c2ecbae70bf85da2`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786db0a3988ce428787cfe588a08d3b9c1c897c7ebfc24a579e54bb19f546fcb`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab8b864113ad6fef653342907be67b1f880316a291dde505550e5eddac3e870`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d6b4b4f014b764cb75cc10988c8c9fcc2c6943f0c7ba3f24115f2bedf602c5`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.5-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:630d3ef14aa6aec84c68d0bd075afde8c6649479ff6be8acd513d89d1bce6db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `nats:2.6.5-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:6ab359fa36226d90c1aafd6638846ec1a0bd53484f30e04842e1efc41cf6eda1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278475967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f606e5e79c17f6ad740d2394f5ab64d8d281e6ccd57599ec6138371bc5578`
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
# Fri, 19 Nov 2021 23:17:07 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:17:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.5/nats-server-v2.6.5-windows-amd64.zip
# Fri, 19 Nov 2021 23:17:09 GMT
ENV NATS_SERVER_SHASUM=0aba30ddd630fddd7ecd49c18a0666b0f78386d2e623d701c00f0b18351e4529
# Fri, 19 Nov 2021 23:18:18 GMT
RUN Set-PSDebug -Trace 2
# Fri, 19 Nov 2021 23:19:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 19 Nov 2021 23:19:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:19:50 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:19:51 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:19:52 GMT
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
	-	`sha256:f6e3554a67b57f2a9aa17f80c9675be949b9372a709bb0f7fdf1dc7a3954a8a7`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eeda6412c8ef4a5587519bccde86a7d03ede9e3d88c0c2ee7b4edaa24a9d25c`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ca635911cf274a387f2d940588371058db1949e9b10f093b7fd1da6d1a30fc`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672969c6f430af654d3a77eecadafcc5149020360859599bfac5eadbdf52388`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 360.6 KB (360571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf6b57aeb7766a77d7c0ba1400216f6aa339f8607b7fd2302e8b30f4ff8f140`  
		Last Modified: Fri, 19 Nov 2021 23:21:03 GMT  
		Size: 5.0 MB (5011302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b11540a8a97137b66a8f28531a07e5ec3db99e327ab93821000188e02bc98bf`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca98906943111b8c8be9af092d51081d9ff4e7ff0613c220636cb567764349`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d92f48165676375740936c62ff6e30aca04671b4204790a0b8c7a481a64e77`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5b6e62a393187d7daea5065dc7e4285f6ff881d7575c53739d47f068b86803`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:7f36c22a7e0cb76ce2e06235022b20aa5ed52736f6c363dbeeaca8dab69ecf4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:06e24692a80300ca5bd9671ab4ab80c1b048d6887c18ca32aa073887fa1fd359
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7686268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e413df78b5a846b18ac33bc0aaf255770267bebcbc0618ab7f297560f31587ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:41:57 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:42:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:42:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:42:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:42:01 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:42:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a26961feb3858523c0a38d5decbabc61ce2fdecfc03c3f118db9ae38e2a2081`  
		Last Modified: Fri, 19 Nov 2021 23:42:44 GMT  
		Size: 4.9 MB (4862314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0833c09ffb63b8898f80abd7a90f5bdecefb7a10a771e96779648ca03137643`  
		Last Modified: Fri, 19 Nov 2021 23:42:43 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2219d94c89a69f8eb02e5fcbb9cc203e77bbc833a538b83c6cff697ea6e410e3`  
		Last Modified: Fri, 19 Nov 2021 23:42:43 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:1492db6aaab11ff0408a18ccd0b9c4e05a6a09bf27b989ba06df650f3c4daa35
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5380995e0b783165a76fcab9a147c18e8154d4e6cc310236294f54d9adeba4e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:22:19 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:22:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:22:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:22:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:22:24 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:22:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0676a94d1c25310146837eb95390f211b55367bbbc41c86020b28b00375b7baf`  
		Last Modified: Fri, 19 Nov 2021 23:24:33 GMT  
		Size: 4.5 MB (4516168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f024b09adefc2b21cfad2f2279a279604f371cfe6bbfcf1dd11f412d031a7e5d`  
		Last Modified: Fri, 19 Nov 2021 23:24:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c6d7089949b487c17d10a9a94548058005f51c80e94429659ff9dd9093a4cf`  
		Last Modified: Fri, 19 Nov 2021 23:24:31 GMT  
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
$ docker pull nats@sha256:7f36c22a7e0cb76ce2e06235022b20aa5ed52736f6c363dbeeaca8dab69ecf4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:06e24692a80300ca5bd9671ab4ab80c1b048d6887c18ca32aa073887fa1fd359
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7686268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e413df78b5a846b18ac33bc0aaf255770267bebcbc0618ab7f297560f31587ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:41:57 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:42:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:42:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:42:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:42:01 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:42:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a26961feb3858523c0a38d5decbabc61ce2fdecfc03c3f118db9ae38e2a2081`  
		Last Modified: Fri, 19 Nov 2021 23:42:44 GMT  
		Size: 4.9 MB (4862314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0833c09ffb63b8898f80abd7a90f5bdecefb7a10a771e96779648ca03137643`  
		Last Modified: Fri, 19 Nov 2021 23:42:43 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2219d94c89a69f8eb02e5fcbb9cc203e77bbc833a538b83c6cff697ea6e410e3`  
		Last Modified: Fri, 19 Nov 2021 23:42:43 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:1492db6aaab11ff0408a18ccd0b9c4e05a6a09bf27b989ba06df650f3c4daa35
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5380995e0b783165a76fcab9a147c18e8154d4e6cc310236294f54d9adeba4e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:22:19 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:22:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:22:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:22:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:22:24 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:22:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0676a94d1c25310146837eb95390f211b55367bbbc41c86020b28b00375b7baf`  
		Last Modified: Fri, 19 Nov 2021 23:24:33 GMT  
		Size: 4.5 MB (4516168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f024b09adefc2b21cfad2f2279a279604f371cfe6bbfcf1dd11f412d031a7e5d`  
		Last Modified: Fri, 19 Nov 2021 23:24:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c6d7089949b487c17d10a9a94548058005f51c80e94429659ff9dd9093a4cf`  
		Last Modified: Fri, 19 Nov 2021 23:24:31 GMT  
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
$ docker pull nats@sha256:dba2bbbe7e9dd7c39a43a53a5d4beeaae542ee98dae82b64aed895c6589e8f21
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
$ docker pull nats@sha256:4c4e804a1650e91fbfbf07efa44afc479755a6ace2ab57050b950475ddc93442
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acde872f934ff8c9ad3505d331c4827e3285ad4314e92f69ae0abe1d455ff77f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:42:18 GMT
COPY file:148643ead7a90f9c3416e4455a70bf4638bf9c77005e258d6ec4dcf605560028 in /nats-server 
# Fri, 19 Nov 2021 23:42:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:42:19 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:42:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe89a8c692b8dabfd4ac3062f9232c753d0c2db79be5dca06811cfd9dbcbdc1c`  
		Last Modified: Fri, 19 Nov 2021 23:43:09 GMT  
		Size: 4.6 MB (4575375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5645a0f80ddde9dcce3a4aecfc7a9ab65b20f5c4fcab9897e75302b2b4bf404`  
		Last Modified: Fri, 19 Nov 2021 23:43:08 GMT  
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
$ docker pull nats@sha256:c3e6b4d51c17fa68c6e4c70ce519e1035c89a232b96c9ca59d1aa9932f7b4687
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514f8bdd0d1db9adfcc78eb1a00c34ad3eefd5e7135852bcd277023ebe30f0c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:48132b2177bf3ca4d978b99a66b7a228cae6937450ee016ac753a4c4ffb567a6 in /nats-server 
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:22:49 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:49 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:22:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:92ac13b7cd582c606500bbb3364dbf1a7e0a85030b4deeabfba3a44d94b2c66e`  
		Last Modified: Fri, 19 Nov 2021 23:25:11 GMT  
		Size: 4.2 MB (4235210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b8c68cfe1eeaa6a60a3863fceb15216ecc6b46b1ff00255bffe9a638b3b768`  
		Last Modified: Fri, 19 Nov 2021 23:25:08 GMT  
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
$ docker pull nats@sha256:905989f3a6b51bca9680b352fd5a4cc271c355fe1f97bc891436699220a6dc15
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107424291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc5b97cb5590745b1ceee71f3fa39e6182c08aa0778a902b59edef61785e388`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 19 Nov 2021 23:16:56 GMT
RUN cmd /S /C #(nop) COPY file:cb348e461b3d96ac80f8049551e5a2f64ad993b7e0766d87ab5ab5fdd94589b6 in C:\nats-server.exe 
# Fri, 19 Nov 2021 23:16:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:17:00 GMT
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
	-	`sha256:ba9a2a1dd5182104e73dd0b99871b9421cef25f8493a107f6c5851e604a0c805`  
		Last Modified: Fri, 19 Nov 2021 23:20:49 GMT  
		Size: 4.6 MB (4634936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea376684ddbfce1b9e46c526a7dbe800a8e6a7423d96f16cca44e1ac0610b13b`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdadde7749a61c1e452864079f7e483484220f0ae3fa7f7bd7244e01c51564e`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c305401f02bde38a326c77b9088b6a7a2a01a5babed79ec98c244a5c6006588`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4957be82dbf1c2d1fdab2d9f4604991c3bbf7c9ff6fa46efeee39dd1086ed3`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:85deef40c1d54f42dc99207f542c78162bd9cee6cccc9ee62d4a68e5e8155e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:4c4e804a1650e91fbfbf07efa44afc479755a6ace2ab57050b950475ddc93442
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acde872f934ff8c9ad3505d331c4827e3285ad4314e92f69ae0abe1d455ff77f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:42:18 GMT
COPY file:148643ead7a90f9c3416e4455a70bf4638bf9c77005e258d6ec4dcf605560028 in /nats-server 
# Fri, 19 Nov 2021 23:42:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:42:19 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:42:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe89a8c692b8dabfd4ac3062f9232c753d0c2db79be5dca06811cfd9dbcbdc1c`  
		Last Modified: Fri, 19 Nov 2021 23:43:09 GMT  
		Size: 4.6 MB (4575375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5645a0f80ddde9dcce3a4aecfc7a9ab65b20f5c4fcab9897e75302b2b4bf404`  
		Last Modified: Fri, 19 Nov 2021 23:43:08 GMT  
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
$ docker pull nats@sha256:c3e6b4d51c17fa68c6e4c70ce519e1035c89a232b96c9ca59d1aa9932f7b4687
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514f8bdd0d1db9adfcc78eb1a00c34ad3eefd5e7135852bcd277023ebe30f0c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:48132b2177bf3ca4d978b99a66b7a228cae6937450ee016ac753a4c4ffb567a6 in /nats-server 
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:22:49 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:49 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:22:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:92ac13b7cd582c606500bbb3364dbf1a7e0a85030b4deeabfba3a44d94b2c66e`  
		Last Modified: Fri, 19 Nov 2021 23:25:11 GMT  
		Size: 4.2 MB (4235210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b8c68cfe1eeaa6a60a3863fceb15216ecc6b46b1ff00255bffe9a638b3b768`  
		Last Modified: Fri, 19 Nov 2021 23:25:08 GMT  
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
$ docker pull nats@sha256:b398d37048c28628fc4321bc540446f3ee812011e7c9a16d3dd19009eb5884ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:905989f3a6b51bca9680b352fd5a4cc271c355fe1f97bc891436699220a6dc15
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107424291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc5b97cb5590745b1ceee71f3fa39e6182c08aa0778a902b59edef61785e388`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 19 Nov 2021 23:16:56 GMT
RUN cmd /S /C #(nop) COPY file:cb348e461b3d96ac80f8049551e5a2f64ad993b7e0766d87ab5ab5fdd94589b6 in C:\nats-server.exe 
# Fri, 19 Nov 2021 23:16:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:17:00 GMT
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
	-	`sha256:ba9a2a1dd5182104e73dd0b99871b9421cef25f8493a107f6c5851e604a0c805`  
		Last Modified: Fri, 19 Nov 2021 23:20:49 GMT  
		Size: 4.6 MB (4634936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea376684ddbfce1b9e46c526a7dbe800a8e6a7423d96f16cca44e1ac0610b13b`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdadde7749a61c1e452864079f7e483484220f0ae3fa7f7bd7244e01c51564e`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c305401f02bde38a326c77b9088b6a7a2a01a5babed79ec98c244a5c6006588`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4957be82dbf1c2d1fdab2d9f4604991c3bbf7c9ff6fa46efeee39dd1086ed3`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:b398d37048c28628fc4321bc540446f3ee812011e7c9a16d3dd19009eb5884ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:905989f3a6b51bca9680b352fd5a4cc271c355fe1f97bc891436699220a6dc15
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107424291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc5b97cb5590745b1ceee71f3fa39e6182c08aa0778a902b59edef61785e388`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 19 Nov 2021 23:16:56 GMT
RUN cmd /S /C #(nop) COPY file:cb348e461b3d96ac80f8049551e5a2f64ad993b7e0766d87ab5ab5fdd94589b6 in C:\nats-server.exe 
# Fri, 19 Nov 2021 23:16:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:17:00 GMT
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
	-	`sha256:ba9a2a1dd5182104e73dd0b99871b9421cef25f8493a107f6c5851e604a0c805`  
		Last Modified: Fri, 19 Nov 2021 23:20:49 GMT  
		Size: 4.6 MB (4634936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea376684ddbfce1b9e46c526a7dbe800a8e6a7423d96f16cca44e1ac0610b13b`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdadde7749a61c1e452864079f7e483484220f0ae3fa7f7bd7244e01c51564e`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c305401f02bde38a326c77b9088b6a7a2a01a5babed79ec98c244a5c6006588`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4957be82dbf1c2d1fdab2d9f4604991c3bbf7c9ff6fa46efeee39dd1086ed3`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:85deef40c1d54f42dc99207f542c78162bd9cee6cccc9ee62d4a68e5e8155e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:4c4e804a1650e91fbfbf07efa44afc479755a6ace2ab57050b950475ddc93442
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acde872f934ff8c9ad3505d331c4827e3285ad4314e92f69ae0abe1d455ff77f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:42:18 GMT
COPY file:148643ead7a90f9c3416e4455a70bf4638bf9c77005e258d6ec4dcf605560028 in /nats-server 
# Fri, 19 Nov 2021 23:42:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:42:19 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:42:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe89a8c692b8dabfd4ac3062f9232c753d0c2db79be5dca06811cfd9dbcbdc1c`  
		Last Modified: Fri, 19 Nov 2021 23:43:09 GMT  
		Size: 4.6 MB (4575375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5645a0f80ddde9dcce3a4aecfc7a9ab65b20f5c4fcab9897e75302b2b4bf404`  
		Last Modified: Fri, 19 Nov 2021 23:43:08 GMT  
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
$ docker pull nats@sha256:c3e6b4d51c17fa68c6e4c70ce519e1035c89a232b96c9ca59d1aa9932f7b4687
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514f8bdd0d1db9adfcc78eb1a00c34ad3eefd5e7135852bcd277023ebe30f0c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:48132b2177bf3ca4d978b99a66b7a228cae6937450ee016ac753a4c4ffb567a6 in /nats-server 
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:22:49 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:49 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:22:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:92ac13b7cd582c606500bbb3364dbf1a7e0a85030b4deeabfba3a44d94b2c66e`  
		Last Modified: Fri, 19 Nov 2021 23:25:11 GMT  
		Size: 4.2 MB (4235210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b8c68cfe1eeaa6a60a3863fceb15216ecc6b46b1ff00255bffe9a638b3b768`  
		Last Modified: Fri, 19 Nov 2021 23:25:08 GMT  
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
$ docker pull nats@sha256:7e0428dba71a73c21cf18a83990daccd695802963a5066161b005c0fa2aee2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `nats:windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:8d78380851c70c44eea273d3aaff4c424ad191c679708c42bc171878d9500fac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711490510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a201f7790c138296ade85180ca7a6fb58d90b5c11b47fcf00561b8c1f8912412`
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
# Fri, 19 Nov 2021 23:14:14 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:14:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.5/nats-server-v2.6.5-windows-amd64.zip
# Fri, 19 Nov 2021 23:14:16 GMT
ENV NATS_SERVER_SHASUM=0aba30ddd630fddd7ecd49c18a0666b0f78386d2e623d701c00f0b18351e4529
# Fri, 19 Nov 2021 23:15:20 GMT
RUN Set-PSDebug -Trace 2
# Fri, 19 Nov 2021 23:16:41 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 19 Nov 2021 23:16:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:43 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:44 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:16:45 GMT
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
	-	`sha256:66ee32c5b0f8d0e25d55f2155058787d912af133c85d6e693f1b829b4247b631`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8dc647b82c6c8b1c1e07221e4f9d39e1a2ab5d5ba52da0c81f7787c5ae5999`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509fa0ab98575757356ace0336d5e3c425b48de9137d943b065c182545960785`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3745b3fbaa0d3f89421d0a9f02890206569705c76260367007a8ec3958a6f8ce`  
		Last Modified: Fri, 19 Nov 2021 23:20:33 GMT  
		Size: 368.7 KB (368732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2736dce76765262fdaa9b8f1cb72e12a54be251a592faebc20887d9ffdf021`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 5.0 MB (4987456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d319abe61026f65f2bd4bfc0ced76d5d6e68d5636948772c2ecbae70bf85da2`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786db0a3988ce428787cfe588a08d3b9c1c897c7ebfc24a579e54bb19f546fcb`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab8b864113ad6fef653342907be67b1f880316a291dde505550e5eddac3e870`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d6b4b4f014b764cb75cc10988c8c9fcc2c6943f0c7ba3f24115f2bedf602c5`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:6ab359fa36226d90c1aafd6638846ec1a0bd53484f30e04842e1efc41cf6eda1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278475967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f606e5e79c17f6ad740d2394f5ab64d8d281e6ccd57599ec6138371bc5578`
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
# Fri, 19 Nov 2021 23:17:07 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:17:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.5/nats-server-v2.6.5-windows-amd64.zip
# Fri, 19 Nov 2021 23:17:09 GMT
ENV NATS_SERVER_SHASUM=0aba30ddd630fddd7ecd49c18a0666b0f78386d2e623d701c00f0b18351e4529
# Fri, 19 Nov 2021 23:18:18 GMT
RUN Set-PSDebug -Trace 2
# Fri, 19 Nov 2021 23:19:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 19 Nov 2021 23:19:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:19:50 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:19:51 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:19:52 GMT
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
	-	`sha256:f6e3554a67b57f2a9aa17f80c9675be949b9372a709bb0f7fdf1dc7a3954a8a7`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eeda6412c8ef4a5587519bccde86a7d03ede9e3d88c0c2ee7b4edaa24a9d25c`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ca635911cf274a387f2d940588371058db1949e9b10f093b7fd1da6d1a30fc`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672969c6f430af654d3a77eecadafcc5149020360859599bfac5eadbdf52388`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 360.6 KB (360571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf6b57aeb7766a77d7c0ba1400216f6aa339f8607b7fd2302e8b30f4ff8f140`  
		Last Modified: Fri, 19 Nov 2021 23:21:03 GMT  
		Size: 5.0 MB (5011302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b11540a8a97137b66a8f28531a07e5ec3db99e327ab93821000188e02bc98bf`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca98906943111b8c8be9af092d51081d9ff4e7ff0613c220636cb567764349`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d92f48165676375740936c62ff6e30aca04671b4204790a0b8c7a481a64e77`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5b6e62a393187d7daea5065dc7e4285f6ff881d7575c53739d47f068b86803`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:181df5142aea41aa0901309ffd02c00ae7926e3af39dbda47800de6129b6945b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:8d78380851c70c44eea273d3aaff4c424ad191c679708c42bc171878d9500fac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711490510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a201f7790c138296ade85180ca7a6fb58d90b5c11b47fcf00561b8c1f8912412`
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
# Fri, 19 Nov 2021 23:14:14 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:14:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.5/nats-server-v2.6.5-windows-amd64.zip
# Fri, 19 Nov 2021 23:14:16 GMT
ENV NATS_SERVER_SHASUM=0aba30ddd630fddd7ecd49c18a0666b0f78386d2e623d701c00f0b18351e4529
# Fri, 19 Nov 2021 23:15:20 GMT
RUN Set-PSDebug -Trace 2
# Fri, 19 Nov 2021 23:16:41 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 19 Nov 2021 23:16:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:43 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:44 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:16:45 GMT
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
	-	`sha256:66ee32c5b0f8d0e25d55f2155058787d912af133c85d6e693f1b829b4247b631`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8dc647b82c6c8b1c1e07221e4f9d39e1a2ab5d5ba52da0c81f7787c5ae5999`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509fa0ab98575757356ace0336d5e3c425b48de9137d943b065c182545960785`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3745b3fbaa0d3f89421d0a9f02890206569705c76260367007a8ec3958a6f8ce`  
		Last Modified: Fri, 19 Nov 2021 23:20:33 GMT  
		Size: 368.7 KB (368732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2736dce76765262fdaa9b8f1cb72e12a54be251a592faebc20887d9ffdf021`  
		Last Modified: Fri, 19 Nov 2021 23:20:32 GMT  
		Size: 5.0 MB (4987456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d319abe61026f65f2bd4bfc0ced76d5d6e68d5636948772c2ecbae70bf85da2`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786db0a3988ce428787cfe588a08d3b9c1c897c7ebfc24a579e54bb19f546fcb`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab8b864113ad6fef653342907be67b1f880316a291dde505550e5eddac3e870`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d6b4b4f014b764cb75cc10988c8c9fcc2c6943f0c7ba3f24115f2bedf602c5`  
		Last Modified: Fri, 19 Nov 2021 23:20:30 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:630d3ef14aa6aec84c68d0bd075afde8c6649479ff6be8acd513d89d1bce6db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:6ab359fa36226d90c1aafd6638846ec1a0bd53484f30e04842e1efc41cf6eda1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278475967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f606e5e79c17f6ad740d2394f5ab64d8d281e6ccd57599ec6138371bc5578`
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
# Fri, 19 Nov 2021 23:17:07 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:17:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.5/nats-server-v2.6.5-windows-amd64.zip
# Fri, 19 Nov 2021 23:17:09 GMT
ENV NATS_SERVER_SHASUM=0aba30ddd630fddd7ecd49c18a0666b0f78386d2e623d701c00f0b18351e4529
# Fri, 19 Nov 2021 23:18:18 GMT
RUN Set-PSDebug -Trace 2
# Fri, 19 Nov 2021 23:19:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 19 Nov 2021 23:19:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:19:50 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:19:51 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:19:52 GMT
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
	-	`sha256:f6e3554a67b57f2a9aa17f80c9675be949b9372a709bb0f7fdf1dc7a3954a8a7`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eeda6412c8ef4a5587519bccde86a7d03ede9e3d88c0c2ee7b4edaa24a9d25c`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ca635911cf274a387f2d940588371058db1949e9b10f093b7fd1da6d1a30fc`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672969c6f430af654d3a77eecadafcc5149020360859599bfac5eadbdf52388`  
		Last Modified: Fri, 19 Nov 2021 23:21:04 GMT  
		Size: 360.6 KB (360571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf6b57aeb7766a77d7c0ba1400216f6aa339f8607b7fd2302e8b30f4ff8f140`  
		Last Modified: Fri, 19 Nov 2021 23:21:03 GMT  
		Size: 5.0 MB (5011302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b11540a8a97137b66a8f28531a07e5ec3db99e327ab93821000188e02bc98bf`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca98906943111b8c8be9af092d51081d9ff4e7ff0613c220636cb567764349`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d92f48165676375740936c62ff6e30aca04671b4204790a0b8c7a481a64e77`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5b6e62a393187d7daea5065dc7e4285f6ff881d7575c53739d47f068b86803`  
		Last Modified: Fri, 19 Nov 2021 23:21:02 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

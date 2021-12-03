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
-	[`nats:2.6.6`](#nats266)
-	[`nats:2.6.6-alpine`](#nats266-alpine)
-	[`nats:2.6.6-alpine3.14`](#nats266-alpine314)
-	[`nats:2.6.6-linux`](#nats266-linux)
-	[`nats:2.6.6-nanoserver`](#nats266-nanoserver)
-	[`nats:2.6.6-nanoserver-1809`](#nats266-nanoserver-1809)
-	[`nats:2.6.6-scratch`](#nats266-scratch)
-	[`nats:2.6.6-windowsservercore`](#nats266-windowsservercore)
-	[`nats:2.6.6-windowsservercore-1809`](#nats266-windowsservercore-1809)
-	[`nats:2.6.6-windowsservercore-ltsc2016`](#nats266-windowsservercore-ltsc2016)
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
$ docker pull nats@sha256:d7c4ed424636fe2c5a0b293b592519c471de2e769be000e0a3bfec5458ed45b9
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
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
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
$ docker pull nats@sha256:99c7322b540961f363b09f8639858695602351709ff4bd8b883dd5ccd0ff2670
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107426609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfeb0ce069f091d552a8ecdaf57a0e8f47fffc5d34d7aff5cc5d3d60886d002`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Dec 2021 23:17:27 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Thu, 02 Dec 2021 23:17:28 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:31 GMT
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
	-	`sha256:24c80f67e6bdb94f78501d521f07fb2bf8634fec39442b25df7fe32a479d4a84`  
		Last Modified: Thu, 02 Dec 2021 23:21:20 GMT  
		Size: 4.6 MB (4637256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be64ef39306c1a5d7e6a283c3a0269013221313695bdacb6a5135799347e477`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da9f12dc4664d0ec4aea4094087fba83f2fbfaf0e55c8329fd5f87cbe76f65d`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083e9d445c6220eda3b7812fdda284918ddf4ed878f984e4ccdfa2b98e5adba8`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de499b1ce88b906fea231dff65edaabb6610c8b553c2be0238dce603e9b5589`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:147ab0dbc6afc221b0f11bb92594c1123618dd94b95183a7c5b10a358bcc76f1
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
$ docker pull nats@sha256:d42d25248435c99492dd0fbcd97688486c692c680069bc9a1eb8a7b1c85eebff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7161537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae84a8c7e689bc4d7fd2915ef9aaf1fb624c094cb183af5863d4b20984f29cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Thu, 02 Dec 2021 22:49:35 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 22:49:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Dec 2021 22:49:41 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 22:49:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c7b89c441a056fc0e4d867cd4fd28308f188bd0f6b306e5feee96fee47cbdf`  
		Last Modified: Thu, 02 Dec 2021 22:51:52 GMT  
		Size: 4.5 MB (4525169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67a5f3b97f233f2d6d30a90acd85b9e856cb9b98c298b71e2b5cbae3e0268cf`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706486ffe19b237b40203ebf10cb1110d7566cba5a3c10bf738be70173a1aa69`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:147ab0dbc6afc221b0f11bb92594c1123618dd94b95183a7c5b10a358bcc76f1
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
$ docker pull nats@sha256:d42d25248435c99492dd0fbcd97688486c692c680069bc9a1eb8a7b1c85eebff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7161537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae84a8c7e689bc4d7fd2915ef9aaf1fb624c094cb183af5863d4b20984f29cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Thu, 02 Dec 2021 22:49:35 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 22:49:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Dec 2021 22:49:41 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 22:49:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c7b89c441a056fc0e4d867cd4fd28308f188bd0f6b306e5feee96fee47cbdf`  
		Last Modified: Thu, 02 Dec 2021 22:51:52 GMT  
		Size: 4.5 MB (4525169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67a5f3b97f233f2d6d30a90acd85b9e856cb9b98c298b71e2b5cbae3e0268cf`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706486ffe19b237b40203ebf10cb1110d7566cba5a3c10bf738be70173a1aa69`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:0b5a8f4425cfd3e7862cf336a9e6bf5dd4507a07e1e164e0dcb063ff39bb776e
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
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
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
$ docker pull nats@sha256:f5979f4957523aed037c96a5b739e5257e3fc7e6825cf1be143384b38be4fb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:99c7322b540961f363b09f8639858695602351709ff4bd8b883dd5ccd0ff2670
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107426609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfeb0ce069f091d552a8ecdaf57a0e8f47fffc5d34d7aff5cc5d3d60886d002`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Dec 2021 23:17:27 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Thu, 02 Dec 2021 23:17:28 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:31 GMT
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
	-	`sha256:24c80f67e6bdb94f78501d521f07fb2bf8634fec39442b25df7fe32a479d4a84`  
		Last Modified: Thu, 02 Dec 2021 23:21:20 GMT  
		Size: 4.6 MB (4637256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be64ef39306c1a5d7e6a283c3a0269013221313695bdacb6a5135799347e477`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da9f12dc4664d0ec4aea4094087fba83f2fbfaf0e55c8329fd5f87cbe76f65d`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083e9d445c6220eda3b7812fdda284918ddf4ed878f984e4ccdfa2b98e5adba8`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de499b1ce88b906fea231dff65edaabb6610c8b553c2be0238dce603e9b5589`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:f5979f4957523aed037c96a5b739e5257e3fc7e6825cf1be143384b38be4fb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:99c7322b540961f363b09f8639858695602351709ff4bd8b883dd5ccd0ff2670
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107426609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfeb0ce069f091d552a8ecdaf57a0e8f47fffc5d34d7aff5cc5d3d60886d002`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Dec 2021 23:17:27 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Thu, 02 Dec 2021 23:17:28 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:31 GMT
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
	-	`sha256:24c80f67e6bdb94f78501d521f07fb2bf8634fec39442b25df7fe32a479d4a84`  
		Last Modified: Thu, 02 Dec 2021 23:21:20 GMT  
		Size: 4.6 MB (4637256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be64ef39306c1a5d7e6a283c3a0269013221313695bdacb6a5135799347e477`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da9f12dc4664d0ec4aea4094087fba83f2fbfaf0e55c8329fd5f87cbe76f65d`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083e9d445c6220eda3b7812fdda284918ddf4ed878f984e4ccdfa2b98e5adba8`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de499b1ce88b906fea231dff65edaabb6610c8b553c2be0238dce603e9b5589`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:0b5a8f4425cfd3e7862cf336a9e6bf5dd4507a07e1e164e0dcb063ff39bb776e
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
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
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
$ docker pull nats@sha256:25a1153221ba966594f15b142ebfed48aef0c6ec8902d23e6b515a52c5e6bcf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:b9e11aa370b882bf61581ff2698b0b9d55401db1280366e98f2e14ffd1cd69b9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711501133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0c15ceb80c8095fea0cd84ad705434bf6614e49356a5d2a037de1a12ef7d9f`
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
# Thu, 02 Dec 2021 23:14:44 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 23:14:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Thu, 02 Dec 2021 23:14:46 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Thu, 02 Dec 2021 23:15:51 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Dec 2021 23:17:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Dec 2021 23:17:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:16 GMT
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
	-	`sha256:dab177cdaf49ad94a156c4f388a50ac14957029df2cbe964a46b6ed9847895fe`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8f81125cc8b875e7a756f42608aaea23d09c1722ea5a87d844ed9cd4715410`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca24678cb52f6ba95c9250fe07f2a161451187bde03568cbc9d8003d7c043ff0`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706a2eccd2cd19eb81b2c6e8eb150747e211be02023516e871267d1489402afb`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 368.7 KB (368700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fb04d845145a8b24cc67d70d7a3fa070075403a4b832822ad93ef89043d341`  
		Last Modified: Thu, 02 Dec 2021 23:21:03 GMT  
		Size: 5.0 MB (4998013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17902cd0bf41b5fb4f1490d11b5d320dd9ed425e0abdbb0663adbbede06e88a5`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303bbcc7b45ec8cff1e92c50975c02992191b9e3a26f87f27577de70a6618ab1`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bea1379c4df28329a2e2ab8e33f4ce9a2c6da33099e9ffb4f2bd87bde95235`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cc8d1a4eefbce0fefa0ad09cdbf5123267a4da9e8f9dfdbad654f5c69798fa`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:fdcf94ff9f56185e96e2d34c14a819b244e403758d7013151609dbfcb360c5e2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278478824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af4423e4e1bb0fc02b0a493270852db3199a402c345f19d3d87a57cbfe0845d`
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
# Thu, 02 Dec 2021 23:17:38 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 23:17:39 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Thu, 02 Dec 2021 23:17:39 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Thu, 02 Dec 2021 23:18:43 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Dec 2021 23:20:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Dec 2021 23:20:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:20:20 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:20:20 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:20:21 GMT
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
	-	`sha256:b7f30fc57b535f4a7dc20a4d1e1b43e91c4163d15d8d67ce035aa644e312a15e`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74da680686aa5c2ba65208b2c6cdcd1bbd18c45f58aaef8256cfdf8cbc32a03`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10729ec66b57b11f89be7b5130e80d980cf37a601f683c399e671662cac1a110`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0763c02a9f5763cfe1dd77eea65dfc154b93bf42b877a34e753f1c2449c3e70d`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 359.0 KB (359036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c875dd2ccaee8f5e6d8ccf71f31d170077b75efb53b7e75b3fab222c6e823ef9`  
		Last Modified: Thu, 02 Dec 2021 23:21:40 GMT  
		Size: 5.0 MB (5015739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa98d451592563d3d6480b9a59e70f5f5fee7ea754916118efdca39bd399a86`  
		Last Modified: Thu, 02 Dec 2021 23:21:34 GMT  
		Size: 1.9 KB (1938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b28f7a1a71fd2916d9a8178df2cc31b372a0c5b39b207c9b5ba959495536b33`  
		Last Modified: Thu, 02 Dec 2021 23:21:35 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24851a6f0e21f835dc6befed813f920721c0485952726b8ef9ffef97d32fe88c`  
		Last Modified: Thu, 02 Dec 2021 23:21:34 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa050e14310da7375267a60873fd4a6aef2356ad89388b9737efc083526bdf`  
		Last Modified: Thu, 02 Dec 2021 23:21:35 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:2abe9a0b6cc57888006cfe48cfbc570948fe94c54998432b2853289da339960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:b9e11aa370b882bf61581ff2698b0b9d55401db1280366e98f2e14ffd1cd69b9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711501133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0c15ceb80c8095fea0cd84ad705434bf6614e49356a5d2a037de1a12ef7d9f`
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
# Thu, 02 Dec 2021 23:14:44 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 23:14:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Thu, 02 Dec 2021 23:14:46 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Thu, 02 Dec 2021 23:15:51 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Dec 2021 23:17:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Dec 2021 23:17:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:16 GMT
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
	-	`sha256:dab177cdaf49ad94a156c4f388a50ac14957029df2cbe964a46b6ed9847895fe`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8f81125cc8b875e7a756f42608aaea23d09c1722ea5a87d844ed9cd4715410`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca24678cb52f6ba95c9250fe07f2a161451187bde03568cbc9d8003d7c043ff0`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706a2eccd2cd19eb81b2c6e8eb150747e211be02023516e871267d1489402afb`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 368.7 KB (368700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fb04d845145a8b24cc67d70d7a3fa070075403a4b832822ad93ef89043d341`  
		Last Modified: Thu, 02 Dec 2021 23:21:03 GMT  
		Size: 5.0 MB (4998013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17902cd0bf41b5fb4f1490d11b5d320dd9ed425e0abdbb0663adbbede06e88a5`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303bbcc7b45ec8cff1e92c50975c02992191b9e3a26f87f27577de70a6618ab1`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bea1379c4df28329a2e2ab8e33f4ce9a2c6da33099e9ffb4f2bd87bde95235`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cc8d1a4eefbce0fefa0ad09cdbf5123267a4da9e8f9dfdbad654f5c69798fa`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:b78771ff3e48ef90ba8b2f574b397da1d6d109e52976b268bbdb9feca65b219b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:fdcf94ff9f56185e96e2d34c14a819b244e403758d7013151609dbfcb360c5e2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278478824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af4423e4e1bb0fc02b0a493270852db3199a402c345f19d3d87a57cbfe0845d`
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
# Thu, 02 Dec 2021 23:17:38 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 23:17:39 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Thu, 02 Dec 2021 23:17:39 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Thu, 02 Dec 2021 23:18:43 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Dec 2021 23:20:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Dec 2021 23:20:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:20:20 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:20:20 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:20:21 GMT
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
	-	`sha256:b7f30fc57b535f4a7dc20a4d1e1b43e91c4163d15d8d67ce035aa644e312a15e`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74da680686aa5c2ba65208b2c6cdcd1bbd18c45f58aaef8256cfdf8cbc32a03`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10729ec66b57b11f89be7b5130e80d980cf37a601f683c399e671662cac1a110`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0763c02a9f5763cfe1dd77eea65dfc154b93bf42b877a34e753f1c2449c3e70d`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 359.0 KB (359036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c875dd2ccaee8f5e6d8ccf71f31d170077b75efb53b7e75b3fab222c6e823ef9`  
		Last Modified: Thu, 02 Dec 2021 23:21:40 GMT  
		Size: 5.0 MB (5015739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa98d451592563d3d6480b9a59e70f5f5fee7ea754916118efdca39bd399a86`  
		Last Modified: Thu, 02 Dec 2021 23:21:34 GMT  
		Size: 1.9 KB (1938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b28f7a1a71fd2916d9a8178df2cc31b372a0c5b39b207c9b5ba959495536b33`  
		Last Modified: Thu, 02 Dec 2021 23:21:35 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24851a6f0e21f835dc6befed813f920721c0485952726b8ef9ffef97d32fe88c`  
		Last Modified: Thu, 02 Dec 2021 23:21:34 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa050e14310da7375267a60873fd4a6aef2356ad89388b9737efc083526bdf`  
		Last Modified: Thu, 02 Dec 2021 23:21:35 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6`

```console
$ docker pull nats@sha256:d7c4ed424636fe2c5a0b293b592519c471de2e769be000e0a3bfec5458ed45b9
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
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
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
$ docker pull nats@sha256:99c7322b540961f363b09f8639858695602351709ff4bd8b883dd5ccd0ff2670
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107426609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfeb0ce069f091d552a8ecdaf57a0e8f47fffc5d34d7aff5cc5d3d60886d002`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Dec 2021 23:17:27 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Thu, 02 Dec 2021 23:17:28 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:31 GMT
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
	-	`sha256:24c80f67e6bdb94f78501d521f07fb2bf8634fec39442b25df7fe32a479d4a84`  
		Last Modified: Thu, 02 Dec 2021 23:21:20 GMT  
		Size: 4.6 MB (4637256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be64ef39306c1a5d7e6a283c3a0269013221313695bdacb6a5135799347e477`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da9f12dc4664d0ec4aea4094087fba83f2fbfaf0e55c8329fd5f87cbe76f65d`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083e9d445c6220eda3b7812fdda284918ddf4ed878f984e4ccdfa2b98e5adba8`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de499b1ce88b906fea231dff65edaabb6610c8b553c2be0238dce603e9b5589`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-alpine`

```console
$ docker pull nats@sha256:147ab0dbc6afc221b0f11bb92594c1123618dd94b95183a7c5b10a358bcc76f1
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
$ docker pull nats@sha256:d42d25248435c99492dd0fbcd97688486c692c680069bc9a1eb8a7b1c85eebff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7161537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae84a8c7e689bc4d7fd2915ef9aaf1fb624c094cb183af5863d4b20984f29cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Thu, 02 Dec 2021 22:49:35 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 22:49:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Dec 2021 22:49:41 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 22:49:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c7b89c441a056fc0e4d867cd4fd28308f188bd0f6b306e5feee96fee47cbdf`  
		Last Modified: Thu, 02 Dec 2021 22:51:52 GMT  
		Size: 4.5 MB (4525169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67a5f3b97f233f2d6d30a90acd85b9e856cb9b98c298b71e2b5cbae3e0268cf`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706486ffe19b237b40203ebf10cb1110d7566cba5a3c10bf738be70173a1aa69`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:147ab0dbc6afc221b0f11bb92594c1123618dd94b95183a7c5b10a358bcc76f1
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
$ docker pull nats@sha256:d42d25248435c99492dd0fbcd97688486c692c680069bc9a1eb8a7b1c85eebff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7161537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae84a8c7e689bc4d7fd2915ef9aaf1fb624c094cb183af5863d4b20984f29cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Thu, 02 Dec 2021 22:49:35 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 22:49:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Dec 2021 22:49:41 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 22:49:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c7b89c441a056fc0e4d867cd4fd28308f188bd0f6b306e5feee96fee47cbdf`  
		Last Modified: Thu, 02 Dec 2021 22:51:52 GMT  
		Size: 4.5 MB (4525169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67a5f3b97f233f2d6d30a90acd85b9e856cb9b98c298b71e2b5cbae3e0268cf`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706486ffe19b237b40203ebf10cb1110d7566cba5a3c10bf738be70173a1aa69`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:0b5a8f4425cfd3e7862cf336a9e6bf5dd4507a07e1e164e0dcb063ff39bb776e
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
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
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
$ docker pull nats@sha256:f5979f4957523aed037c96a5b739e5257e3fc7e6825cf1be143384b38be4fb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6-nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:99c7322b540961f363b09f8639858695602351709ff4bd8b883dd5ccd0ff2670
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107426609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfeb0ce069f091d552a8ecdaf57a0e8f47fffc5d34d7aff5cc5d3d60886d002`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Dec 2021 23:17:27 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Thu, 02 Dec 2021 23:17:28 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:31 GMT
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
	-	`sha256:24c80f67e6bdb94f78501d521f07fb2bf8634fec39442b25df7fe32a479d4a84`  
		Last Modified: Thu, 02 Dec 2021 23:21:20 GMT  
		Size: 4.6 MB (4637256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be64ef39306c1a5d7e6a283c3a0269013221313695bdacb6a5135799347e477`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da9f12dc4664d0ec4aea4094087fba83f2fbfaf0e55c8329fd5f87cbe76f65d`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083e9d445c6220eda3b7812fdda284918ddf4ed878f984e4ccdfa2b98e5adba8`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de499b1ce88b906fea231dff65edaabb6610c8b553c2be0238dce603e9b5589`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-nanoserver-1809`

```console
$ docker pull nats@sha256:f5979f4957523aed037c96a5b739e5257e3fc7e6825cf1be143384b38be4fb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6-nanoserver-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:99c7322b540961f363b09f8639858695602351709ff4bd8b883dd5ccd0ff2670
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107426609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfeb0ce069f091d552a8ecdaf57a0e8f47fffc5d34d7aff5cc5d3d60886d002`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Dec 2021 23:17:27 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Thu, 02 Dec 2021 23:17:28 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:31 GMT
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
	-	`sha256:24c80f67e6bdb94f78501d521f07fb2bf8634fec39442b25df7fe32a479d4a84`  
		Last Modified: Thu, 02 Dec 2021 23:21:20 GMT  
		Size: 4.6 MB (4637256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be64ef39306c1a5d7e6a283c3a0269013221313695bdacb6a5135799347e477`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da9f12dc4664d0ec4aea4094087fba83f2fbfaf0e55c8329fd5f87cbe76f65d`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083e9d445c6220eda3b7812fdda284918ddf4ed878f984e4ccdfa2b98e5adba8`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de499b1ce88b906fea231dff65edaabb6610c8b553c2be0238dce603e9b5589`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-scratch`

```console
$ docker pull nats@sha256:0b5a8f4425cfd3e7862cf336a9e6bf5dd4507a07e1e164e0dcb063ff39bb776e
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
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
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
$ docker pull nats@sha256:25a1153221ba966594f15b142ebfed48aef0c6ec8902d23e6b515a52c5e6bcf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `nats:2.6-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:b9e11aa370b882bf61581ff2698b0b9d55401db1280366e98f2e14ffd1cd69b9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711501133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0c15ceb80c8095fea0cd84ad705434bf6614e49356a5d2a037de1a12ef7d9f`
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
# Thu, 02 Dec 2021 23:14:44 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 23:14:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Thu, 02 Dec 2021 23:14:46 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Thu, 02 Dec 2021 23:15:51 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Dec 2021 23:17:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Dec 2021 23:17:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:16 GMT
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
	-	`sha256:dab177cdaf49ad94a156c4f388a50ac14957029df2cbe964a46b6ed9847895fe`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8f81125cc8b875e7a756f42608aaea23d09c1722ea5a87d844ed9cd4715410`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca24678cb52f6ba95c9250fe07f2a161451187bde03568cbc9d8003d7c043ff0`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706a2eccd2cd19eb81b2c6e8eb150747e211be02023516e871267d1489402afb`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 368.7 KB (368700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fb04d845145a8b24cc67d70d7a3fa070075403a4b832822ad93ef89043d341`  
		Last Modified: Thu, 02 Dec 2021 23:21:03 GMT  
		Size: 5.0 MB (4998013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17902cd0bf41b5fb4f1490d11b5d320dd9ed425e0abdbb0663adbbede06e88a5`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303bbcc7b45ec8cff1e92c50975c02992191b9e3a26f87f27577de70a6618ab1`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bea1379c4df28329a2e2ab8e33f4ce9a2c6da33099e9ffb4f2bd87bde95235`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cc8d1a4eefbce0fefa0ad09cdbf5123267a4da9e8f9dfdbad654f5c69798fa`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:fdcf94ff9f56185e96e2d34c14a819b244e403758d7013151609dbfcb360c5e2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278478824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af4423e4e1bb0fc02b0a493270852db3199a402c345f19d3d87a57cbfe0845d`
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
# Thu, 02 Dec 2021 23:17:38 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 23:17:39 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Thu, 02 Dec 2021 23:17:39 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Thu, 02 Dec 2021 23:18:43 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Dec 2021 23:20:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Dec 2021 23:20:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:20:20 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:20:20 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:20:21 GMT
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
	-	`sha256:b7f30fc57b535f4a7dc20a4d1e1b43e91c4163d15d8d67ce035aa644e312a15e`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74da680686aa5c2ba65208b2c6cdcd1bbd18c45f58aaef8256cfdf8cbc32a03`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10729ec66b57b11f89be7b5130e80d980cf37a601f683c399e671662cac1a110`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0763c02a9f5763cfe1dd77eea65dfc154b93bf42b877a34e753f1c2449c3e70d`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 359.0 KB (359036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c875dd2ccaee8f5e6d8ccf71f31d170077b75efb53b7e75b3fab222c6e823ef9`  
		Last Modified: Thu, 02 Dec 2021 23:21:40 GMT  
		Size: 5.0 MB (5015739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa98d451592563d3d6480b9a59e70f5f5fee7ea754916118efdca39bd399a86`  
		Last Modified: Thu, 02 Dec 2021 23:21:34 GMT  
		Size: 1.9 KB (1938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b28f7a1a71fd2916d9a8178df2cc31b372a0c5b39b207c9b5ba959495536b33`  
		Last Modified: Thu, 02 Dec 2021 23:21:35 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24851a6f0e21f835dc6befed813f920721c0485952726b8ef9ffef97d32fe88c`  
		Last Modified: Thu, 02 Dec 2021 23:21:34 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa050e14310da7375267a60873fd4a6aef2356ad89388b9737efc083526bdf`  
		Last Modified: Thu, 02 Dec 2021 23:21:35 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-windowsservercore-1809`

```console
$ docker pull nats@sha256:2abe9a0b6cc57888006cfe48cfbc570948fe94c54998432b2853289da339960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:b9e11aa370b882bf61581ff2698b0b9d55401db1280366e98f2e14ffd1cd69b9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711501133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0c15ceb80c8095fea0cd84ad705434bf6614e49356a5d2a037de1a12ef7d9f`
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
# Thu, 02 Dec 2021 23:14:44 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 23:14:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Thu, 02 Dec 2021 23:14:46 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Thu, 02 Dec 2021 23:15:51 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Dec 2021 23:17:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Dec 2021 23:17:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:16 GMT
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
	-	`sha256:dab177cdaf49ad94a156c4f388a50ac14957029df2cbe964a46b6ed9847895fe`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8f81125cc8b875e7a756f42608aaea23d09c1722ea5a87d844ed9cd4715410`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca24678cb52f6ba95c9250fe07f2a161451187bde03568cbc9d8003d7c043ff0`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706a2eccd2cd19eb81b2c6e8eb150747e211be02023516e871267d1489402afb`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 368.7 KB (368700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fb04d845145a8b24cc67d70d7a3fa070075403a4b832822ad93ef89043d341`  
		Last Modified: Thu, 02 Dec 2021 23:21:03 GMT  
		Size: 5.0 MB (4998013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17902cd0bf41b5fb4f1490d11b5d320dd9ed425e0abdbb0663adbbede06e88a5`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303bbcc7b45ec8cff1e92c50975c02992191b9e3a26f87f27577de70a6618ab1`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bea1379c4df28329a2e2ab8e33f4ce9a2c6da33099e9ffb4f2bd87bde95235`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cc8d1a4eefbce0fefa0ad09cdbf5123267a4da9e8f9dfdbad654f5c69798fa`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:b78771ff3e48ef90ba8b2f574b397da1d6d109e52976b268bbdb9feca65b219b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `nats:2.6-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:fdcf94ff9f56185e96e2d34c14a819b244e403758d7013151609dbfcb360c5e2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278478824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af4423e4e1bb0fc02b0a493270852db3199a402c345f19d3d87a57cbfe0845d`
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
# Thu, 02 Dec 2021 23:17:38 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 23:17:39 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Thu, 02 Dec 2021 23:17:39 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Thu, 02 Dec 2021 23:18:43 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Dec 2021 23:20:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Dec 2021 23:20:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:20:20 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:20:20 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:20:21 GMT
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
	-	`sha256:b7f30fc57b535f4a7dc20a4d1e1b43e91c4163d15d8d67ce035aa644e312a15e`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74da680686aa5c2ba65208b2c6cdcd1bbd18c45f58aaef8256cfdf8cbc32a03`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10729ec66b57b11f89be7b5130e80d980cf37a601f683c399e671662cac1a110`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0763c02a9f5763cfe1dd77eea65dfc154b93bf42b877a34e753f1c2449c3e70d`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 359.0 KB (359036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c875dd2ccaee8f5e6d8ccf71f31d170077b75efb53b7e75b3fab222c6e823ef9`  
		Last Modified: Thu, 02 Dec 2021 23:21:40 GMT  
		Size: 5.0 MB (5015739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa98d451592563d3d6480b9a59e70f5f5fee7ea754916118efdca39bd399a86`  
		Last Modified: Thu, 02 Dec 2021 23:21:34 GMT  
		Size: 1.9 KB (1938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b28f7a1a71fd2916d9a8178df2cc31b372a0c5b39b207c9b5ba959495536b33`  
		Last Modified: Thu, 02 Dec 2021 23:21:35 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24851a6f0e21f835dc6befed813f920721c0485952726b8ef9ffef97d32fe88c`  
		Last Modified: Thu, 02 Dec 2021 23:21:34 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa050e14310da7375267a60873fd4a6aef2356ad89388b9737efc083526bdf`  
		Last Modified: Thu, 02 Dec 2021 23:21:35 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6`

```console
$ docker pull nats@sha256:31eebab223d7768011897342fe68dee94b79314b190fbe7cc17cbe654afb52fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6.6` - linux; arm variant v6

```console
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:99c7322b540961f363b09f8639858695602351709ff4bd8b883dd5ccd0ff2670
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107426609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfeb0ce069f091d552a8ecdaf57a0e8f47fffc5d34d7aff5cc5d3d60886d002`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Dec 2021 23:17:27 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Thu, 02 Dec 2021 23:17:28 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:31 GMT
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
	-	`sha256:24c80f67e6bdb94f78501d521f07fb2bf8634fec39442b25df7fe32a479d4a84`  
		Last Modified: Thu, 02 Dec 2021 23:21:20 GMT  
		Size: 4.6 MB (4637256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be64ef39306c1a5d7e6a283c3a0269013221313695bdacb6a5135799347e477`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da9f12dc4664d0ec4aea4094087fba83f2fbfaf0e55c8329fd5f87cbe76f65d`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083e9d445c6220eda3b7812fdda284918ddf4ed878f984e4ccdfa2b98e5adba8`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de499b1ce88b906fea231dff65edaabb6610c8b553c2be0238dce603e9b5589`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6-alpine`

```console
$ docker pull nats@sha256:e6435f83cf50ae36ab1605a21af8cdbc287b522c3643af53eacb2175b6d64ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v6

### `nats:2.6.6-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d42d25248435c99492dd0fbcd97688486c692c680069bc9a1eb8a7b1c85eebff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7161537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae84a8c7e689bc4d7fd2915ef9aaf1fb624c094cb183af5863d4b20984f29cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Thu, 02 Dec 2021 22:49:35 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 22:49:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Dec 2021 22:49:41 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 22:49:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c7b89c441a056fc0e4d867cd4fd28308f188bd0f6b306e5feee96fee47cbdf`  
		Last Modified: Thu, 02 Dec 2021 22:51:52 GMT  
		Size: 4.5 MB (4525169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67a5f3b97f233f2d6d30a90acd85b9e856cb9b98c298b71e2b5cbae3e0268cf`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706486ffe19b237b40203ebf10cb1110d7566cba5a3c10bf738be70173a1aa69`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6-alpine3.14`

```console
$ docker pull nats@sha256:e6435f83cf50ae36ab1605a21af8cdbc287b522c3643af53eacb2175b6d64ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v6

### `nats:2.6.6-alpine3.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:d42d25248435c99492dd0fbcd97688486c692c680069bc9a1eb8a7b1c85eebff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7161537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae84a8c7e689bc4d7fd2915ef9aaf1fb624c094cb183af5863d4b20984f29cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Thu, 02 Dec 2021 22:49:35 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 22:49:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Dec 2021 22:49:41 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 22:49:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c7b89c441a056fc0e4d867cd4fd28308f188bd0f6b306e5feee96fee47cbdf`  
		Last Modified: Thu, 02 Dec 2021 22:51:52 GMT  
		Size: 4.5 MB (4525169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67a5f3b97f233f2d6d30a90acd85b9e856cb9b98c298b71e2b5cbae3e0268cf`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706486ffe19b237b40203ebf10cb1110d7566cba5a3c10bf738be70173a1aa69`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6-linux`

```console
$ docker pull nats@sha256:b47913bd56613d7687b92a8d352e6857bcbe0004c62e4948cf2d916021aa462f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v6

### `nats:2.6.6-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6-nanoserver`

```console
$ docker pull nats@sha256:f5979f4957523aed037c96a5b739e5257e3fc7e6825cf1be143384b38be4fb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6.6-nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:99c7322b540961f363b09f8639858695602351709ff4bd8b883dd5ccd0ff2670
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107426609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfeb0ce069f091d552a8ecdaf57a0e8f47fffc5d34d7aff5cc5d3d60886d002`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Dec 2021 23:17:27 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Thu, 02 Dec 2021 23:17:28 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:31 GMT
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
	-	`sha256:24c80f67e6bdb94f78501d521f07fb2bf8634fec39442b25df7fe32a479d4a84`  
		Last Modified: Thu, 02 Dec 2021 23:21:20 GMT  
		Size: 4.6 MB (4637256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be64ef39306c1a5d7e6a283c3a0269013221313695bdacb6a5135799347e477`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da9f12dc4664d0ec4aea4094087fba83f2fbfaf0e55c8329fd5f87cbe76f65d`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083e9d445c6220eda3b7812fdda284918ddf4ed878f984e4ccdfa2b98e5adba8`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de499b1ce88b906fea231dff65edaabb6610c8b553c2be0238dce603e9b5589`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6-nanoserver-1809`

```console
$ docker pull nats@sha256:f5979f4957523aed037c96a5b739e5257e3fc7e6825cf1be143384b38be4fb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6.6-nanoserver-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:99c7322b540961f363b09f8639858695602351709ff4bd8b883dd5ccd0ff2670
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107426609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfeb0ce069f091d552a8ecdaf57a0e8f47fffc5d34d7aff5cc5d3d60886d002`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Dec 2021 23:17:27 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Thu, 02 Dec 2021 23:17:28 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:31 GMT
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
	-	`sha256:24c80f67e6bdb94f78501d521f07fb2bf8634fec39442b25df7fe32a479d4a84`  
		Last Modified: Thu, 02 Dec 2021 23:21:20 GMT  
		Size: 4.6 MB (4637256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be64ef39306c1a5d7e6a283c3a0269013221313695bdacb6a5135799347e477`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da9f12dc4664d0ec4aea4094087fba83f2fbfaf0e55c8329fd5f87cbe76f65d`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083e9d445c6220eda3b7812fdda284918ddf4ed878f984e4ccdfa2b98e5adba8`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de499b1ce88b906fea231dff65edaabb6610c8b553c2be0238dce603e9b5589`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6-scratch`

```console
$ docker pull nats@sha256:b47913bd56613d7687b92a8d352e6857bcbe0004c62e4948cf2d916021aa462f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v6

### `nats:2.6.6-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6-windowsservercore`

```console
$ docker pull nats@sha256:25a1153221ba966594f15b142ebfed48aef0c6ec8902d23e6b515a52c5e6bcf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `nats:2.6.6-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:b9e11aa370b882bf61581ff2698b0b9d55401db1280366e98f2e14ffd1cd69b9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711501133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0c15ceb80c8095fea0cd84ad705434bf6614e49356a5d2a037de1a12ef7d9f`
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
# Thu, 02 Dec 2021 23:14:44 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 23:14:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Thu, 02 Dec 2021 23:14:46 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Thu, 02 Dec 2021 23:15:51 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Dec 2021 23:17:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Dec 2021 23:17:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:16 GMT
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
	-	`sha256:dab177cdaf49ad94a156c4f388a50ac14957029df2cbe964a46b6ed9847895fe`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8f81125cc8b875e7a756f42608aaea23d09c1722ea5a87d844ed9cd4715410`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca24678cb52f6ba95c9250fe07f2a161451187bde03568cbc9d8003d7c043ff0`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706a2eccd2cd19eb81b2c6e8eb150747e211be02023516e871267d1489402afb`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 368.7 KB (368700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fb04d845145a8b24cc67d70d7a3fa070075403a4b832822ad93ef89043d341`  
		Last Modified: Thu, 02 Dec 2021 23:21:03 GMT  
		Size: 5.0 MB (4998013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17902cd0bf41b5fb4f1490d11b5d320dd9ed425e0abdbb0663adbbede06e88a5`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303bbcc7b45ec8cff1e92c50975c02992191b9e3a26f87f27577de70a6618ab1`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bea1379c4df28329a2e2ab8e33f4ce9a2c6da33099e9ffb4f2bd87bde95235`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cc8d1a4eefbce0fefa0ad09cdbf5123267a4da9e8f9dfdbad654f5c69798fa`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6-windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:fdcf94ff9f56185e96e2d34c14a819b244e403758d7013151609dbfcb360c5e2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278478824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af4423e4e1bb0fc02b0a493270852db3199a402c345f19d3d87a57cbfe0845d`
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
# Thu, 02 Dec 2021 23:17:38 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 23:17:39 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Thu, 02 Dec 2021 23:17:39 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Thu, 02 Dec 2021 23:18:43 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Dec 2021 23:20:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Dec 2021 23:20:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:20:20 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:20:20 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:20:21 GMT
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
	-	`sha256:b7f30fc57b535f4a7dc20a4d1e1b43e91c4163d15d8d67ce035aa644e312a15e`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74da680686aa5c2ba65208b2c6cdcd1bbd18c45f58aaef8256cfdf8cbc32a03`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10729ec66b57b11f89be7b5130e80d980cf37a601f683c399e671662cac1a110`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0763c02a9f5763cfe1dd77eea65dfc154b93bf42b877a34e753f1c2449c3e70d`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 359.0 KB (359036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c875dd2ccaee8f5e6d8ccf71f31d170077b75efb53b7e75b3fab222c6e823ef9`  
		Last Modified: Thu, 02 Dec 2021 23:21:40 GMT  
		Size: 5.0 MB (5015739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa98d451592563d3d6480b9a59e70f5f5fee7ea754916118efdca39bd399a86`  
		Last Modified: Thu, 02 Dec 2021 23:21:34 GMT  
		Size: 1.9 KB (1938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b28f7a1a71fd2916d9a8178df2cc31b372a0c5b39b207c9b5ba959495536b33`  
		Last Modified: Thu, 02 Dec 2021 23:21:35 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24851a6f0e21f835dc6befed813f920721c0485952726b8ef9ffef97d32fe88c`  
		Last Modified: Thu, 02 Dec 2021 23:21:34 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa050e14310da7375267a60873fd4a6aef2356ad89388b9737efc083526bdf`  
		Last Modified: Thu, 02 Dec 2021 23:21:35 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6-windowsservercore-1809`

```console
$ docker pull nats@sha256:2abe9a0b6cc57888006cfe48cfbc570948fe94c54998432b2853289da339960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:2.6.6-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:b9e11aa370b882bf61581ff2698b0b9d55401db1280366e98f2e14ffd1cd69b9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711501133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0c15ceb80c8095fea0cd84ad705434bf6614e49356a5d2a037de1a12ef7d9f`
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
# Thu, 02 Dec 2021 23:14:44 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 23:14:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Thu, 02 Dec 2021 23:14:46 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Thu, 02 Dec 2021 23:15:51 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Dec 2021 23:17:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Dec 2021 23:17:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:16 GMT
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
	-	`sha256:dab177cdaf49ad94a156c4f388a50ac14957029df2cbe964a46b6ed9847895fe`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8f81125cc8b875e7a756f42608aaea23d09c1722ea5a87d844ed9cd4715410`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca24678cb52f6ba95c9250fe07f2a161451187bde03568cbc9d8003d7c043ff0`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706a2eccd2cd19eb81b2c6e8eb150747e211be02023516e871267d1489402afb`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 368.7 KB (368700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fb04d845145a8b24cc67d70d7a3fa070075403a4b832822ad93ef89043d341`  
		Last Modified: Thu, 02 Dec 2021 23:21:03 GMT  
		Size: 5.0 MB (4998013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17902cd0bf41b5fb4f1490d11b5d320dd9ed425e0abdbb0663adbbede06e88a5`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303bbcc7b45ec8cff1e92c50975c02992191b9e3a26f87f27577de70a6618ab1`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bea1379c4df28329a2e2ab8e33f4ce9a2c6da33099e9ffb4f2bd87bde95235`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cc8d1a4eefbce0fefa0ad09cdbf5123267a4da9e8f9dfdbad654f5c69798fa`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:b78771ff3e48ef90ba8b2f574b397da1d6d109e52976b268bbdb9feca65b219b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `nats:2.6.6-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:fdcf94ff9f56185e96e2d34c14a819b244e403758d7013151609dbfcb360c5e2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278478824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af4423e4e1bb0fc02b0a493270852db3199a402c345f19d3d87a57cbfe0845d`
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
# Thu, 02 Dec 2021 23:17:38 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 23:17:39 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Thu, 02 Dec 2021 23:17:39 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Thu, 02 Dec 2021 23:18:43 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Dec 2021 23:20:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Dec 2021 23:20:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:20:20 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:20:20 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:20:21 GMT
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
	-	`sha256:b7f30fc57b535f4a7dc20a4d1e1b43e91c4163d15d8d67ce035aa644e312a15e`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74da680686aa5c2ba65208b2c6cdcd1bbd18c45f58aaef8256cfdf8cbc32a03`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10729ec66b57b11f89be7b5130e80d980cf37a601f683c399e671662cac1a110`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0763c02a9f5763cfe1dd77eea65dfc154b93bf42b877a34e753f1c2449c3e70d`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 359.0 KB (359036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c875dd2ccaee8f5e6d8ccf71f31d170077b75efb53b7e75b3fab222c6e823ef9`  
		Last Modified: Thu, 02 Dec 2021 23:21:40 GMT  
		Size: 5.0 MB (5015739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa98d451592563d3d6480b9a59e70f5f5fee7ea754916118efdca39bd399a86`  
		Last Modified: Thu, 02 Dec 2021 23:21:34 GMT  
		Size: 1.9 KB (1938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b28f7a1a71fd2916d9a8178df2cc31b372a0c5b39b207c9b5ba959495536b33`  
		Last Modified: Thu, 02 Dec 2021 23:21:35 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24851a6f0e21f835dc6befed813f920721c0485952726b8ef9ffef97d32fe88c`  
		Last Modified: Thu, 02 Dec 2021 23:21:34 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa050e14310da7375267a60873fd4a6aef2356ad89388b9737efc083526bdf`  
		Last Modified: Thu, 02 Dec 2021 23:21:35 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:147ab0dbc6afc221b0f11bb92594c1123618dd94b95183a7c5b10a358bcc76f1
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
$ docker pull nats@sha256:d42d25248435c99492dd0fbcd97688486c692c680069bc9a1eb8a7b1c85eebff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7161537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae84a8c7e689bc4d7fd2915ef9aaf1fb624c094cb183af5863d4b20984f29cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Thu, 02 Dec 2021 22:49:35 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 22:49:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Dec 2021 22:49:41 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 22:49:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c7b89c441a056fc0e4d867cd4fd28308f188bd0f6b306e5feee96fee47cbdf`  
		Last Modified: Thu, 02 Dec 2021 22:51:52 GMT  
		Size: 4.5 MB (4525169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67a5f3b97f233f2d6d30a90acd85b9e856cb9b98c298b71e2b5cbae3e0268cf`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706486ffe19b237b40203ebf10cb1110d7566cba5a3c10bf738be70173a1aa69`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:147ab0dbc6afc221b0f11bb92594c1123618dd94b95183a7c5b10a358bcc76f1
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
$ docker pull nats@sha256:d42d25248435c99492dd0fbcd97688486c692c680069bc9a1eb8a7b1c85eebff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7161537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae84a8c7e689bc4d7fd2915ef9aaf1fb624c094cb183af5863d4b20984f29cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Thu, 02 Dec 2021 22:49:35 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 22:49:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Dec 2021 22:49:41 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 22:49:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c7b89c441a056fc0e4d867cd4fd28308f188bd0f6b306e5feee96fee47cbdf`  
		Last Modified: Thu, 02 Dec 2021 22:51:52 GMT  
		Size: 4.5 MB (4525169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67a5f3b97f233f2d6d30a90acd85b9e856cb9b98c298b71e2b5cbae3e0268cf`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706486ffe19b237b40203ebf10cb1110d7566cba5a3c10bf738be70173a1aa69`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:d7c4ed424636fe2c5a0b293b592519c471de2e769be000e0a3bfec5458ed45b9
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
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
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
$ docker pull nats@sha256:99c7322b540961f363b09f8639858695602351709ff4bd8b883dd5ccd0ff2670
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107426609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfeb0ce069f091d552a8ecdaf57a0e8f47fffc5d34d7aff5cc5d3d60886d002`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Dec 2021 23:17:27 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Thu, 02 Dec 2021 23:17:28 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:31 GMT
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
	-	`sha256:24c80f67e6bdb94f78501d521f07fb2bf8634fec39442b25df7fe32a479d4a84`  
		Last Modified: Thu, 02 Dec 2021 23:21:20 GMT  
		Size: 4.6 MB (4637256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be64ef39306c1a5d7e6a283c3a0269013221313695bdacb6a5135799347e477`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da9f12dc4664d0ec4aea4094087fba83f2fbfaf0e55c8329fd5f87cbe76f65d`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083e9d445c6220eda3b7812fdda284918ddf4ed878f984e4ccdfa2b98e5adba8`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de499b1ce88b906fea231dff65edaabb6610c8b553c2be0238dce603e9b5589`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:0b5a8f4425cfd3e7862cf336a9e6bf5dd4507a07e1e164e0dcb063ff39bb776e
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
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
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
$ docker pull nats@sha256:f5979f4957523aed037c96a5b739e5257e3fc7e6825cf1be143384b38be4fb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:99c7322b540961f363b09f8639858695602351709ff4bd8b883dd5ccd0ff2670
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107426609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfeb0ce069f091d552a8ecdaf57a0e8f47fffc5d34d7aff5cc5d3d60886d002`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Dec 2021 23:17:27 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Thu, 02 Dec 2021 23:17:28 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:31 GMT
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
	-	`sha256:24c80f67e6bdb94f78501d521f07fb2bf8634fec39442b25df7fe32a479d4a84`  
		Last Modified: Thu, 02 Dec 2021 23:21:20 GMT  
		Size: 4.6 MB (4637256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be64ef39306c1a5d7e6a283c3a0269013221313695bdacb6a5135799347e477`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da9f12dc4664d0ec4aea4094087fba83f2fbfaf0e55c8329fd5f87cbe76f65d`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083e9d445c6220eda3b7812fdda284918ddf4ed878f984e4ccdfa2b98e5adba8`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de499b1ce88b906fea231dff65edaabb6610c8b553c2be0238dce603e9b5589`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:f5979f4957523aed037c96a5b739e5257e3fc7e6825cf1be143384b38be4fb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:99c7322b540961f363b09f8639858695602351709ff4bd8b883dd5ccd0ff2670
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107426609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfeb0ce069f091d552a8ecdaf57a0e8f47fffc5d34d7aff5cc5d3d60886d002`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Dec 2021 23:17:27 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Thu, 02 Dec 2021 23:17:28 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:31 GMT
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
	-	`sha256:24c80f67e6bdb94f78501d521f07fb2bf8634fec39442b25df7fe32a479d4a84`  
		Last Modified: Thu, 02 Dec 2021 23:21:20 GMT  
		Size: 4.6 MB (4637256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be64ef39306c1a5d7e6a283c3a0269013221313695bdacb6a5135799347e477`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da9f12dc4664d0ec4aea4094087fba83f2fbfaf0e55c8329fd5f87cbe76f65d`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083e9d445c6220eda3b7812fdda284918ddf4ed878f984e4ccdfa2b98e5adba8`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de499b1ce88b906fea231dff65edaabb6610c8b553c2be0238dce603e9b5589`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:0b5a8f4425cfd3e7862cf336a9e6bf5dd4507a07e1e164e0dcb063ff39bb776e
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
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
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
$ docker pull nats@sha256:25a1153221ba966594f15b142ebfed48aef0c6ec8902d23e6b515a52c5e6bcf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `nats:windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:b9e11aa370b882bf61581ff2698b0b9d55401db1280366e98f2e14ffd1cd69b9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711501133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0c15ceb80c8095fea0cd84ad705434bf6614e49356a5d2a037de1a12ef7d9f`
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
# Thu, 02 Dec 2021 23:14:44 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 23:14:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Thu, 02 Dec 2021 23:14:46 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Thu, 02 Dec 2021 23:15:51 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Dec 2021 23:17:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Dec 2021 23:17:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:16 GMT
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
	-	`sha256:dab177cdaf49ad94a156c4f388a50ac14957029df2cbe964a46b6ed9847895fe`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8f81125cc8b875e7a756f42608aaea23d09c1722ea5a87d844ed9cd4715410`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca24678cb52f6ba95c9250fe07f2a161451187bde03568cbc9d8003d7c043ff0`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706a2eccd2cd19eb81b2c6e8eb150747e211be02023516e871267d1489402afb`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 368.7 KB (368700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fb04d845145a8b24cc67d70d7a3fa070075403a4b832822ad93ef89043d341`  
		Last Modified: Thu, 02 Dec 2021 23:21:03 GMT  
		Size: 5.0 MB (4998013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17902cd0bf41b5fb4f1490d11b5d320dd9ed425e0abdbb0663adbbede06e88a5`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303bbcc7b45ec8cff1e92c50975c02992191b9e3a26f87f27577de70a6618ab1`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bea1379c4df28329a2e2ab8e33f4ce9a2c6da33099e9ffb4f2bd87bde95235`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cc8d1a4eefbce0fefa0ad09cdbf5123267a4da9e8f9dfdbad654f5c69798fa`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:fdcf94ff9f56185e96e2d34c14a819b244e403758d7013151609dbfcb360c5e2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278478824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af4423e4e1bb0fc02b0a493270852db3199a402c345f19d3d87a57cbfe0845d`
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
# Thu, 02 Dec 2021 23:17:38 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 23:17:39 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Thu, 02 Dec 2021 23:17:39 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Thu, 02 Dec 2021 23:18:43 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Dec 2021 23:20:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Dec 2021 23:20:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:20:20 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:20:20 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:20:21 GMT
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
	-	`sha256:b7f30fc57b535f4a7dc20a4d1e1b43e91c4163d15d8d67ce035aa644e312a15e`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74da680686aa5c2ba65208b2c6cdcd1bbd18c45f58aaef8256cfdf8cbc32a03`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10729ec66b57b11f89be7b5130e80d980cf37a601f683c399e671662cac1a110`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0763c02a9f5763cfe1dd77eea65dfc154b93bf42b877a34e753f1c2449c3e70d`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 359.0 KB (359036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c875dd2ccaee8f5e6d8ccf71f31d170077b75efb53b7e75b3fab222c6e823ef9`  
		Last Modified: Thu, 02 Dec 2021 23:21:40 GMT  
		Size: 5.0 MB (5015739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa98d451592563d3d6480b9a59e70f5f5fee7ea754916118efdca39bd399a86`  
		Last Modified: Thu, 02 Dec 2021 23:21:34 GMT  
		Size: 1.9 KB (1938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b28f7a1a71fd2916d9a8178df2cc31b372a0c5b39b207c9b5ba959495536b33`  
		Last Modified: Thu, 02 Dec 2021 23:21:35 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24851a6f0e21f835dc6befed813f920721c0485952726b8ef9ffef97d32fe88c`  
		Last Modified: Thu, 02 Dec 2021 23:21:34 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa050e14310da7375267a60873fd4a6aef2356ad89388b9737efc083526bdf`  
		Last Modified: Thu, 02 Dec 2021 23:21:35 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:2abe9a0b6cc57888006cfe48cfbc570948fe94c54998432b2853289da339960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:b9e11aa370b882bf61581ff2698b0b9d55401db1280366e98f2e14ffd1cd69b9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711501133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0c15ceb80c8095fea0cd84ad705434bf6614e49356a5d2a037de1a12ef7d9f`
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
# Thu, 02 Dec 2021 23:14:44 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 23:14:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Thu, 02 Dec 2021 23:14:46 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Thu, 02 Dec 2021 23:15:51 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Dec 2021 23:17:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Dec 2021 23:17:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:16 GMT
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
	-	`sha256:dab177cdaf49ad94a156c4f388a50ac14957029df2cbe964a46b6ed9847895fe`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8f81125cc8b875e7a756f42608aaea23d09c1722ea5a87d844ed9cd4715410`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca24678cb52f6ba95c9250fe07f2a161451187bde03568cbc9d8003d7c043ff0`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706a2eccd2cd19eb81b2c6e8eb150747e211be02023516e871267d1489402afb`  
		Last Modified: Thu, 02 Dec 2021 23:21:04 GMT  
		Size: 368.7 KB (368700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fb04d845145a8b24cc67d70d7a3fa070075403a4b832822ad93ef89043d341`  
		Last Modified: Thu, 02 Dec 2021 23:21:03 GMT  
		Size: 5.0 MB (4998013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17902cd0bf41b5fb4f1490d11b5d320dd9ed425e0abdbb0663adbbede06e88a5`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303bbcc7b45ec8cff1e92c50975c02992191b9e3a26f87f27577de70a6618ab1`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bea1379c4df28329a2e2ab8e33f4ce9a2c6da33099e9ffb4f2bd87bde95235`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cc8d1a4eefbce0fefa0ad09cdbf5123267a4da9e8f9dfdbad654f5c69798fa`  
		Last Modified: Thu, 02 Dec 2021 23:21:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:b78771ff3e48ef90ba8b2f574b397da1d6d109e52976b268bbdb9feca65b219b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull nats@sha256:fdcf94ff9f56185e96e2d34c14a819b244e403758d7013151609dbfcb360c5e2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278478824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af4423e4e1bb0fc02b0a493270852db3199a402c345f19d3d87a57cbfe0845d`
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
# Thu, 02 Dec 2021 23:17:38 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 23:17:39 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Thu, 02 Dec 2021 23:17:39 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Thu, 02 Dec 2021 23:18:43 GMT
RUN Set-PSDebug -Trace 2
# Thu, 02 Dec 2021 23:20:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 02 Dec 2021 23:20:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:20:20 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:20:20 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:20:21 GMT
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
	-	`sha256:b7f30fc57b535f4a7dc20a4d1e1b43e91c4163d15d8d67ce035aa644e312a15e`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74da680686aa5c2ba65208b2c6cdcd1bbd18c45f58aaef8256cfdf8cbc32a03`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10729ec66b57b11f89be7b5130e80d980cf37a601f683c399e671662cac1a110`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0763c02a9f5763cfe1dd77eea65dfc154b93bf42b877a34e753f1c2449c3e70d`  
		Last Modified: Thu, 02 Dec 2021 23:21:37 GMT  
		Size: 359.0 KB (359036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c875dd2ccaee8f5e6d8ccf71f31d170077b75efb53b7e75b3fab222c6e823ef9`  
		Last Modified: Thu, 02 Dec 2021 23:21:40 GMT  
		Size: 5.0 MB (5015739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa98d451592563d3d6480b9a59e70f5f5fee7ea754916118efdca39bd399a86`  
		Last Modified: Thu, 02 Dec 2021 23:21:34 GMT  
		Size: 1.9 KB (1938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b28f7a1a71fd2916d9a8178df2cc31b372a0c5b39b207c9b5ba959495536b33`  
		Last Modified: Thu, 02 Dec 2021 23:21:35 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24851a6f0e21f835dc6befed813f920721c0485952726b8ef9ffef97d32fe88c`  
		Last Modified: Thu, 02 Dec 2021 23:21:34 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa050e14310da7375267a60873fd4a6aef2356ad89388b9737efc083526bdf`  
		Last Modified: Thu, 02 Dec 2021 23:21:35 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.15`](#nats2-alpine315)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.8`](#nats28)
-	[`nats:2.8-alpine`](#nats28-alpine)
-	[`nats:2.8-alpine3.15`](#nats28-alpine315)
-	[`nats:2.8-linux`](#nats28-linux)
-	[`nats:2.8-nanoserver`](#nats28-nanoserver)
-	[`nats:2.8-nanoserver-1809`](#nats28-nanoserver-1809)
-	[`nats:2.8-scratch`](#nats28-scratch)
-	[`nats:2.8-windowsservercore`](#nats28-windowsservercore)
-	[`nats:2.8-windowsservercore-1809`](#nats28-windowsservercore-1809)
-	[`nats:2.8.2`](#nats282)
-	[`nats:2.8.2-alpine`](#nats282-alpine)
-	[`nats:2.8.2-alpine3.15`](#nats282-alpine315)
-	[`nats:2.8.2-linux`](#nats282-linux)
-	[`nats:2.8.2-nanoserver`](#nats282-nanoserver)
-	[`nats:2.8.2-nanoserver-1809`](#nats282-nanoserver-1809)
-	[`nats:2.8.2-scratch`](#nats282-scratch)
-	[`nats:2.8.2-windowsservercore`](#nats282-windowsservercore)
-	[`nats:2.8.2-windowsservercore-1809`](#nats282-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.15`](#natsalpine315)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:96a588729683ea9af318903261e4f7e8f475c5691503062f78076c9687a81597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2803; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:d7022e467f53812285667fd004413e8cb15920efbb01d1d0f7c4194a2e084959
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4580109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71863590dea616f7cf93b753e1e7a3baf16f89747f06004d08f65d3fa907ee9a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 21:19:54 GMT
COPY file:1b0e004de765c2bffa3154a8b1990e8a621636f4f1d7ff504c566b8ba440d227 in /nats-server 
# Wed, 04 May 2022 21:19:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 21:19:54 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:19:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 21:19:54 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 21:19:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cf7d6008a72749fed702f25d8a1bb63636b75bf34655ba074286dc54d0db2b5b`  
		Last Modified: Wed, 04 May 2022 21:20:43 GMT  
		Size: 4.6 MB (4579600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ef91ad4507cb0bd768e027792377ba07aaaebc8d89981a6ee648d58561273b`  
		Last Modified: Wed, 04 May 2022 21:20:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:bb39905ea888630c30250ffee5dc2c940c3b95d2a2898b74a7aa139a7007f159
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ce28f90865945806936cfae5ee78d8f2f2598db1ac7086ad1929992f0b3c3a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:50:00 GMT
COPY file:3de61978a9e8a2b166b752a33898d5f146479cdb1ce6ed9df10727fe98f55f51 in /nats-server 
# Fri, 22 Apr 2022 16:50:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:50:01 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:50:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:50:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:50:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a90933979a2530bf92d8ed3112add5a8debe6da238f9becc07b90b414323e402`  
		Last Modified: Fri, 22 Apr 2022 16:52:22 GMT  
		Size: 4.2 MB (4237584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd95754400d2efb409a2eeed76406fade3b92c929c465f6a5c2189183a4e072`  
		Last Modified: Fri, 22 Apr 2022 16:52:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73d094a3eecc53745106d79abcf92f7f2c4959f2c7a607aa8a02aaecf2adc92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d797593dddfb2960ff1bd893323d195aa2e61be166f83abcae8693f1f538cf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 23 Apr 2022 00:08:29 GMT
COPY file:91842064305817f2463830e9925a5bf281c10fa892125e096aa8c52cd100a677 in /nats-server 
# Sat, 23 Apr 2022 00:08:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 23 Apr 2022 00:08:30 GMT
EXPOSE 4222 6222 8222
# Sat, 23 Apr 2022 00:08:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 23 Apr 2022 00:08:31 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 23 Apr 2022 00:08:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ca5997c585d7b90d306ca9e3facb866e5a008db5cfbecedf401e3de574c4445`  
		Last Modified: Sat, 23 Apr 2022 00:10:52 GMT  
		Size: 4.2 MB (4231620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a7a0c9aabdc2939a750f95344dfaf1abde695b5028a9ee42e0b11353fa7c91`  
		Last Modified: Sat, 23 Apr 2022 00:10:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc2a7ab98b1adfcf8b16328efe3416e98bbed6146cffb9289d48b7f1d710f399
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4217735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd22baaa9b7fcf519609324f45785cad127c98aa25e6945ec3bd9144c6b100c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:40:25 GMT
COPY file:a82c07c2e7d51d414d1e87aec6f9d2718447b772505fba86d5ea7617fc1992ac in /nats-server 
# Fri, 22 Apr 2022 16:40:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:40:26 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:40:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:40:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:40:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:308394282a0e57ba139c96f20347213771c895947b7f9625212d7d91ac26cffd`  
		Last Modified: Fri, 22 Apr 2022 16:41:46 GMT  
		Size: 4.2 MB (4217229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a021323d331516d6b6519db1b4d42a2e922c74d6a39588a87e4859c26a9bd85`  
		Last Modified: Fri, 22 Apr 2022 16:41:45 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats@sha256:2b4914d94facbb6299c5ef2598f655a224c0f671a265bd2986f62c70b978582c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107725201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762896cf7b68aecb4d2820c48789eeee8a8cbc7a58862c4bec5f4ad9d2ecd8f3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 04 May 2022 21:17:46 GMT
RUN cmd /S /C #(nop) COPY file:1e690007468fe11473f18dc8fbc8b7aa29351e71d03ca73f75d9fcfbf1fd7911 in C:\nats-server.exe 
# Wed, 04 May 2022 21:17:47 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 04 May 2022 21:17:48 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:17:49 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 04 May 2022 21:17:49 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1e5f9285a324194ea2fae24594852b07a0fc1cec1388dcbc367215de23c29e`  
		Last Modified: Wed, 04 May 2022 21:18:39 GMT  
		Size: 4.6 MB (4622651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde4044fa24dd3365cdc6ba5dff0779813bd4d34e566af1a5c4458c0a232fdc1`  
		Last Modified: Wed, 04 May 2022 21:18:38 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405a229a99882e5792c0dad43c80fb315b37c8b9c347f514baccd7d05c6c9f1c`  
		Last Modified: Wed, 04 May 2022 21:18:38 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1037a060f2ca6801837d7d720ec02ed6916e48ce1cfa49e6c7558ba04de8235`  
		Last Modified: Wed, 04 May 2022 21:18:38 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29f6c2056586ca9353c7019499d854ba31068b682d59304ed4267576ebc5286`  
		Last Modified: Wed, 04 May 2022 21:18:38 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:7347f8953fc53551e6fa6c27db5252c50b6537ae979c39b60ff1ec77e6321c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:4e7d4fe05ce93c6c712e1789435da0c99e1bf3ef74db43eaeaef6ca272397766
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7668256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23d872d0d10133874978b8503e1da0a875478f9c36d18274df90f4499c03019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:22:11 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:22:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:22:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:22:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:22:13 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:22:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:22:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e0d861b124a1ab454d3802b3afed8c07d3ec1392b2b86e1dfd9d0d5d6a1f11`  
		Last Modified: Fri, 22 Apr 2022 16:22:48 GMT  
		Size: 4.9 MB (4852697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0473f2dce7bc79ef8358c50e032d4fdf17e3cc1b93deb8a87ba3085118feb4`  
		Last Modified: Fri, 22 Apr 2022 16:22:47 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0efed31ac2d8993794bd5b44f6e003ec74ea05fb15e0385ef8b1048c904f60`  
		Last Modified: Fri, 22 Apr 2022 16:22:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:7091220455f290bada50edec48a24908cbbe489e0aac009ddafe3e9d540fb036
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7133695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd13715b15026d21466ab186bb33954a7a9df237fce3098e994c544a0d58f606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:49:33 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:49:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:49:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:49:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:49:38 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:49:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:49:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6250a52fe67317e7257391e6c81cf0ea21e47617fd095740a0d3607da4130de7`  
		Last Modified: Fri, 22 Apr 2022 16:51:45 GMT  
		Size: 4.5 MB (4510720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26bd4087b8ffb0f3db8c2e503ba7fb78bceadf9db85e703ebe84ed37074a6df`  
		Last Modified: Fri, 22 Apr 2022 16:51:42 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fdd060af20879eea02ac88ca5a8585f86f5a55e2cd469952ede5eec778a11e`  
		Last Modified: Fri, 22 Apr 2022 16:51:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1887a7edb6da6e2a20b927cd6fbecb48badeb2db3b7221fc977cbb9eec8918cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6929602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cda1a747d2d0a65fcb4c9fd4afedda3e72a3e1180cd20b0b3dced91305f2786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Sat, 23 Apr 2022 00:07:56 GMT
ENV NATS_SERVER=2.8.1
# Sat, 23 Apr 2022 00:08:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 23 Apr 2022 00:08:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 23 Apr 2022 00:08:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 23 Apr 2022 00:08:01 GMT
EXPOSE 4222 6222 8222
# Sat, 23 Apr 2022 00:08:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 23 Apr 2022 00:08:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0a1ab4dd191d0a9443e0df830fa3f17872c0fe4e8d5974dc57b3caeec5f2e4`  
		Last Modified: Sat, 23 Apr 2022 00:10:15 GMT  
		Size: 4.5 MB (4504279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2933c6c28dbd5f01a84c1e2dfe6d247cb7a41211d4c1b312c984b49281780c`  
		Last Modified: Sat, 23 Apr 2022 00:10:12 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b7537ba35c1f1dc2e2bf343cc9f4dfac0789e8606e1c365901ee35a69a3620`  
		Last Modified: Sat, 23 Apr 2022 00:10:12 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:01abf8e1249f3267774047ec264d815aa57af333eecb3558e40bf86924f3c7b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7207790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb5bc49254cd7eb6d816b2d62ecd8a1052ce0be9a8fbe0c89cd81ecc053de8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:40:04 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:40:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:40:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:40:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:40:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:40:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2ab5ff26c46d1d386429d02952195bc7699ceedb0288794e9b35e45c82a117`  
		Last Modified: Fri, 22 Apr 2022 16:41:17 GMT  
		Size: 4.5 MB (4490338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e92c2bb8c325e21d94887f856d4590cf00b7a236989ce3f58f00e0e4bd400ea`  
		Last Modified: Fri, 22 Apr 2022 16:41:16 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203649ff8695131a6ebe7b59382b10c48667e76e75bdff0fd07cf378d45aad00`  
		Last Modified: Fri, 22 Apr 2022 16:41:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.15`

```console
$ docker pull nats@sha256:7347f8953fc53551e6fa6c27db5252c50b6537ae979c39b60ff1ec77e6321c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:4e7d4fe05ce93c6c712e1789435da0c99e1bf3ef74db43eaeaef6ca272397766
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7668256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23d872d0d10133874978b8503e1da0a875478f9c36d18274df90f4499c03019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:22:11 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:22:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:22:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:22:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:22:13 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:22:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:22:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e0d861b124a1ab454d3802b3afed8c07d3ec1392b2b86e1dfd9d0d5d6a1f11`  
		Last Modified: Fri, 22 Apr 2022 16:22:48 GMT  
		Size: 4.9 MB (4852697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0473f2dce7bc79ef8358c50e032d4fdf17e3cc1b93deb8a87ba3085118feb4`  
		Last Modified: Fri, 22 Apr 2022 16:22:47 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0efed31ac2d8993794bd5b44f6e003ec74ea05fb15e0385ef8b1048c904f60`  
		Last Modified: Fri, 22 Apr 2022 16:22:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:7091220455f290bada50edec48a24908cbbe489e0aac009ddafe3e9d540fb036
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7133695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd13715b15026d21466ab186bb33954a7a9df237fce3098e994c544a0d58f606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:49:33 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:49:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:49:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:49:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:49:38 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:49:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:49:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6250a52fe67317e7257391e6c81cf0ea21e47617fd095740a0d3607da4130de7`  
		Last Modified: Fri, 22 Apr 2022 16:51:45 GMT  
		Size: 4.5 MB (4510720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26bd4087b8ffb0f3db8c2e503ba7fb78bceadf9db85e703ebe84ed37074a6df`  
		Last Modified: Fri, 22 Apr 2022 16:51:42 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fdd060af20879eea02ac88ca5a8585f86f5a55e2cd469952ede5eec778a11e`  
		Last Modified: Fri, 22 Apr 2022 16:51:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:1887a7edb6da6e2a20b927cd6fbecb48badeb2db3b7221fc977cbb9eec8918cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6929602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cda1a747d2d0a65fcb4c9fd4afedda3e72a3e1180cd20b0b3dced91305f2786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Sat, 23 Apr 2022 00:07:56 GMT
ENV NATS_SERVER=2.8.1
# Sat, 23 Apr 2022 00:08:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 23 Apr 2022 00:08:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 23 Apr 2022 00:08:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 23 Apr 2022 00:08:01 GMT
EXPOSE 4222 6222 8222
# Sat, 23 Apr 2022 00:08:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 23 Apr 2022 00:08:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0a1ab4dd191d0a9443e0df830fa3f17872c0fe4e8d5974dc57b3caeec5f2e4`  
		Last Modified: Sat, 23 Apr 2022 00:10:15 GMT  
		Size: 4.5 MB (4504279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2933c6c28dbd5f01a84c1e2dfe6d247cb7a41211d4c1b312c984b49281780c`  
		Last Modified: Sat, 23 Apr 2022 00:10:12 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b7537ba35c1f1dc2e2bf343cc9f4dfac0789e8606e1c365901ee35a69a3620`  
		Last Modified: Sat, 23 Apr 2022 00:10:12 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:01abf8e1249f3267774047ec264d815aa57af333eecb3558e40bf86924f3c7b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7207790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb5bc49254cd7eb6d816b2d62ecd8a1052ce0be9a8fbe0c89cd81ecc053de8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:40:04 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:40:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:40:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:40:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:40:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:40:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2ab5ff26c46d1d386429d02952195bc7699ceedb0288794e9b35e45c82a117`  
		Last Modified: Fri, 22 Apr 2022 16:41:17 GMT  
		Size: 4.5 MB (4490338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e92c2bb8c325e21d94887f856d4590cf00b7a236989ce3f58f00e0e4bd400ea`  
		Last Modified: Fri, 22 Apr 2022 16:41:16 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203649ff8695131a6ebe7b59382b10c48667e76e75bdff0fd07cf378d45aad00`  
		Last Modified: Fri, 22 Apr 2022 16:41:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:9addad33a841b1ca50669b2abe41b55d8d36358b26c33a9ab4d16277e0ac0d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:e22bfb7fdf9006c8d295782e24a70c2197e340f216b649650ea67288ef841319
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4580124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913890b0a2d48e5c381bcf8b123528904a57150fa69138277620e0ff995dff8b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:3454a426bcdf428c59f748013f6bd917cddf529f8a5032532fee8e7783f2d5e4 in /nats-server 
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:22:23 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:22:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:22:23 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:22:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:804b81b2249803c39d50d8d9262ec5bdb230411989987b9116527a02dbf021a8`  
		Last Modified: Fri, 22 Apr 2022 16:23:12 GMT  
		Size: 4.6 MB (4579616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebd8666e9d6549b9ab43c6349958c6dbb767c779117f02d727d356e3daaf3d`  
		Last Modified: Fri, 22 Apr 2022 16:23:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:bb39905ea888630c30250ffee5dc2c940c3b95d2a2898b74a7aa139a7007f159
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ce28f90865945806936cfae5ee78d8f2f2598db1ac7086ad1929992f0b3c3a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:50:00 GMT
COPY file:3de61978a9e8a2b166b752a33898d5f146479cdb1ce6ed9df10727fe98f55f51 in /nats-server 
# Fri, 22 Apr 2022 16:50:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:50:01 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:50:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:50:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:50:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a90933979a2530bf92d8ed3112add5a8debe6da238f9becc07b90b414323e402`  
		Last Modified: Fri, 22 Apr 2022 16:52:22 GMT  
		Size: 4.2 MB (4237584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd95754400d2efb409a2eeed76406fade3b92c929c465f6a5c2189183a4e072`  
		Last Modified: Fri, 22 Apr 2022 16:52:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73d094a3eecc53745106d79abcf92f7f2c4959f2c7a607aa8a02aaecf2adc92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d797593dddfb2960ff1bd893323d195aa2e61be166f83abcae8693f1f538cf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 23 Apr 2022 00:08:29 GMT
COPY file:91842064305817f2463830e9925a5bf281c10fa892125e096aa8c52cd100a677 in /nats-server 
# Sat, 23 Apr 2022 00:08:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 23 Apr 2022 00:08:30 GMT
EXPOSE 4222 6222 8222
# Sat, 23 Apr 2022 00:08:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 23 Apr 2022 00:08:31 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 23 Apr 2022 00:08:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ca5997c585d7b90d306ca9e3facb866e5a008db5cfbecedf401e3de574c4445`  
		Last Modified: Sat, 23 Apr 2022 00:10:52 GMT  
		Size: 4.2 MB (4231620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a7a0c9aabdc2939a750f95344dfaf1abde695b5028a9ee42e0b11353fa7c91`  
		Last Modified: Sat, 23 Apr 2022 00:10:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc2a7ab98b1adfcf8b16328efe3416e98bbed6146cffb9289d48b7f1d710f399
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4217735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd22baaa9b7fcf519609324f45785cad127c98aa25e6945ec3bd9144c6b100c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:40:25 GMT
COPY file:a82c07c2e7d51d414d1e87aec6f9d2718447b772505fba86d5ea7617fc1992ac in /nats-server 
# Fri, 22 Apr 2022 16:40:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:40:26 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:40:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:40:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:40:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:308394282a0e57ba139c96f20347213771c895947b7f9625212d7d91ac26cffd`  
		Last Modified: Fri, 22 Apr 2022 16:41:46 GMT  
		Size: 4.2 MB (4217229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a021323d331516d6b6519db1b4d42a2e922c74d6a39588a87e4859c26a9bd85`  
		Last Modified: Fri, 22 Apr 2022 16:41:45 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:188160bd678c2674cf45d1685ee2a9c297a10c1ed2cf173855e1dff975e5cb60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats@sha256:227efc1752210cbcc77743dc885b3f5ffa9966413a8b7a1ccf182248232c1024
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107725502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b05969443a7a68a122354a2d829e013a0df166ddeec0eff010d310a4b388b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 22 Apr 2022 16:23:26 GMT
RUN cmd /S /C #(nop) COPY file:6453f9106eda3f02af709c31de2264cc25ab8c381441246ced6125fb4dd22377 in C:\nats-server.exe 
# Fri, 22 Apr 2022 16:23:27 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 22 Apr 2022 16:23:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:23:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 22 Apr 2022 16:23:29 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32761659ca35235e4a77458923e43649ba35fc6f6912dffaefb6c1c688212635`  
		Last Modified: Fri, 22 Apr 2022 16:24:23 GMT  
		Size: 4.6 MB (4622930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e54c47f94a9e95b59dd25be3be3811c5356ec1102f4404d94152641988b2a9`  
		Last Modified: Fri, 22 Apr 2022 16:24:18 GMT  
		Size: 1.8 KB (1775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa66f1ddbe51efb72028472b1a3aab1c927cfeb371c3c672134f884cc417a0e`  
		Last Modified: Fri, 22 Apr 2022 16:24:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e4233f94da42224e5744acf20ce233bdf62ca614e821fc6846e7a9c67eb65c`  
		Last Modified: Fri, 22 Apr 2022 16:24:18 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436a600cc67e9fb632157ae49c6290622f0d1e1d7507f692487081fc42681632`  
		Last Modified: Fri, 22 Apr 2022 16:24:17 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:188160bd678c2674cf45d1685ee2a9c297a10c1ed2cf173855e1dff975e5cb60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats@sha256:227efc1752210cbcc77743dc885b3f5ffa9966413a8b7a1ccf182248232c1024
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107725502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b05969443a7a68a122354a2d829e013a0df166ddeec0eff010d310a4b388b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 22 Apr 2022 16:23:26 GMT
RUN cmd /S /C #(nop) COPY file:6453f9106eda3f02af709c31de2264cc25ab8c381441246ced6125fb4dd22377 in C:\nats-server.exe 
# Fri, 22 Apr 2022 16:23:27 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 22 Apr 2022 16:23:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:23:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 22 Apr 2022 16:23:29 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32761659ca35235e4a77458923e43649ba35fc6f6912dffaefb6c1c688212635`  
		Last Modified: Fri, 22 Apr 2022 16:24:23 GMT  
		Size: 4.6 MB (4622930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e54c47f94a9e95b59dd25be3be3811c5356ec1102f4404d94152641988b2a9`  
		Last Modified: Fri, 22 Apr 2022 16:24:18 GMT  
		Size: 1.8 KB (1775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa66f1ddbe51efb72028472b1a3aab1c927cfeb371c3c672134f884cc417a0e`  
		Last Modified: Fri, 22 Apr 2022 16:24:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e4233f94da42224e5744acf20ce233bdf62ca614e821fc6846e7a9c67eb65c`  
		Last Modified: Fri, 22 Apr 2022 16:24:18 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436a600cc67e9fb632157ae49c6290622f0d1e1d7507f692487081fc42681632`  
		Last Modified: Fri, 22 Apr 2022 16:24:17 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:9addad33a841b1ca50669b2abe41b55d8d36358b26c33a9ab4d16277e0ac0d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:e22bfb7fdf9006c8d295782e24a70c2197e340f216b649650ea67288ef841319
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4580124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913890b0a2d48e5c381bcf8b123528904a57150fa69138277620e0ff995dff8b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:3454a426bcdf428c59f748013f6bd917cddf529f8a5032532fee8e7783f2d5e4 in /nats-server 
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:22:23 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:22:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:22:23 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:22:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:804b81b2249803c39d50d8d9262ec5bdb230411989987b9116527a02dbf021a8`  
		Last Modified: Fri, 22 Apr 2022 16:23:12 GMT  
		Size: 4.6 MB (4579616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebd8666e9d6549b9ab43c6349958c6dbb767c779117f02d727d356e3daaf3d`  
		Last Modified: Fri, 22 Apr 2022 16:23:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:bb39905ea888630c30250ffee5dc2c940c3b95d2a2898b74a7aa139a7007f159
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ce28f90865945806936cfae5ee78d8f2f2598db1ac7086ad1929992f0b3c3a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:50:00 GMT
COPY file:3de61978a9e8a2b166b752a33898d5f146479cdb1ce6ed9df10727fe98f55f51 in /nats-server 
# Fri, 22 Apr 2022 16:50:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:50:01 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:50:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:50:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:50:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a90933979a2530bf92d8ed3112add5a8debe6da238f9becc07b90b414323e402`  
		Last Modified: Fri, 22 Apr 2022 16:52:22 GMT  
		Size: 4.2 MB (4237584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd95754400d2efb409a2eeed76406fade3b92c929c465f6a5c2189183a4e072`  
		Last Modified: Fri, 22 Apr 2022 16:52:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73d094a3eecc53745106d79abcf92f7f2c4959f2c7a607aa8a02aaecf2adc92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d797593dddfb2960ff1bd893323d195aa2e61be166f83abcae8693f1f538cf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 23 Apr 2022 00:08:29 GMT
COPY file:91842064305817f2463830e9925a5bf281c10fa892125e096aa8c52cd100a677 in /nats-server 
# Sat, 23 Apr 2022 00:08:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 23 Apr 2022 00:08:30 GMT
EXPOSE 4222 6222 8222
# Sat, 23 Apr 2022 00:08:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 23 Apr 2022 00:08:31 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 23 Apr 2022 00:08:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ca5997c585d7b90d306ca9e3facb866e5a008db5cfbecedf401e3de574c4445`  
		Last Modified: Sat, 23 Apr 2022 00:10:52 GMT  
		Size: 4.2 MB (4231620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a7a0c9aabdc2939a750f95344dfaf1abde695b5028a9ee42e0b11353fa7c91`  
		Last Modified: Sat, 23 Apr 2022 00:10:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc2a7ab98b1adfcf8b16328efe3416e98bbed6146cffb9289d48b7f1d710f399
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4217735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd22baaa9b7fcf519609324f45785cad127c98aa25e6945ec3bd9144c6b100c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:40:25 GMT
COPY file:a82c07c2e7d51d414d1e87aec6f9d2718447b772505fba86d5ea7617fc1992ac in /nats-server 
# Fri, 22 Apr 2022 16:40:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:40:26 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:40:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:40:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:40:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:308394282a0e57ba139c96f20347213771c895947b7f9625212d7d91ac26cffd`  
		Last Modified: Fri, 22 Apr 2022 16:41:46 GMT  
		Size: 4.2 MB (4217229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a021323d331516d6b6519db1b4d42a2e922c74d6a39588a87e4859c26a9bd85`  
		Last Modified: Fri, 22 Apr 2022 16:41:45 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:4331838044198073df8afe0ad453fd1eb97f51ec7bde9025303fbbb1189e155d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats@sha256:ae5ea527d83182c720c7d1ed179661da4d518fcd64cb5f5dee86948254dcb62c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2721254090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88151b674d5d60f9b53098f2888cdb2b6934a2f3b54d108de2cdb34972019f07`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 12:43:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 14:42:30 GMT
ENV NATS_DOCKERIZED=1
# Fri, 22 Apr 2022 16:20:42 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:20:43 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.1/nats-server-v2.8.1-windows-amd64.zip
# Fri, 22 Apr 2022 16:20:44 GMT
ENV NATS_SERVER_SHASUM=a8c4535897e7973cce5005f7fa71ef0f681a7faf014f8875b5a35e865261ff1f
# Fri, 22 Apr 2022 16:21:42 GMT
RUN Set-PSDebug -Trace 2
# Fri, 22 Apr 2022 16:23:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 22 Apr 2022 16:23:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 22 Apr 2022 16:23:14 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:23:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 22 Apr 2022 16:23:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ebb23aa64bff633cfa3c62b190d84f0e870b04fecb1910f65d0870b5c7f8981`  
		Last Modified: Wed, 13 Apr 2022 14:12:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838c7a98a95bee63894bac798124e8c8572bcacc23e22d85332d453a03a7d7c`  
		Last Modified: Wed, 13 Apr 2022 14:46:17 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8987265b365755a0b758f78710e444da1b49314f15f64aa591dd344430d3fb`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5265b75522ed436be37427e2b945e79901d0288c294b04bea492dbd522b2cfe`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0142ce0f758e44db725dfe50c5e3b301364181c2e9e8505003ea5e5faeb50ab`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1718491c665ff5c4180c99f48ca54ffd756d9e28ce78d0177dc4f5d8974185`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 359.7 KB (359679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4331728196114862c2dc2e870fbee9fb2f0e1f51778d0c228ed319a2a43739c7`  
		Last Modified: Fri, 22 Apr 2022 16:24:02 GMT  
		Size: 5.0 MB (4960879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b500a22154605ab8b08473544c72dc700dc6f83895c4efc82544f82f544bbf`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728c706f26744001339dc27c514f27f211b217c21f5fe860bd3e565365cef023`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bf4bee55391723a25240f8a0bd0dfe04b2c3fa9dca71af7f792425ff3aec92`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0f4247067242fb22fccdaa011c8629357ed677cf22255e88d521e5781f0290`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:4331838044198073df8afe0ad453fd1eb97f51ec7bde9025303fbbb1189e155d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats@sha256:ae5ea527d83182c720c7d1ed179661da4d518fcd64cb5f5dee86948254dcb62c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2721254090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88151b674d5d60f9b53098f2888cdb2b6934a2f3b54d108de2cdb34972019f07`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 12:43:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 14:42:30 GMT
ENV NATS_DOCKERIZED=1
# Fri, 22 Apr 2022 16:20:42 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:20:43 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.1/nats-server-v2.8.1-windows-amd64.zip
# Fri, 22 Apr 2022 16:20:44 GMT
ENV NATS_SERVER_SHASUM=a8c4535897e7973cce5005f7fa71ef0f681a7faf014f8875b5a35e865261ff1f
# Fri, 22 Apr 2022 16:21:42 GMT
RUN Set-PSDebug -Trace 2
# Fri, 22 Apr 2022 16:23:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 22 Apr 2022 16:23:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 22 Apr 2022 16:23:14 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:23:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 22 Apr 2022 16:23:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ebb23aa64bff633cfa3c62b190d84f0e870b04fecb1910f65d0870b5c7f8981`  
		Last Modified: Wed, 13 Apr 2022 14:12:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838c7a98a95bee63894bac798124e8c8572bcacc23e22d85332d453a03a7d7c`  
		Last Modified: Wed, 13 Apr 2022 14:46:17 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8987265b365755a0b758f78710e444da1b49314f15f64aa591dd344430d3fb`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5265b75522ed436be37427e2b945e79901d0288c294b04bea492dbd522b2cfe`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0142ce0f758e44db725dfe50c5e3b301364181c2e9e8505003ea5e5faeb50ab`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1718491c665ff5c4180c99f48ca54ffd756d9e28ce78d0177dc4f5d8974185`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 359.7 KB (359679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4331728196114862c2dc2e870fbee9fb2f0e1f51778d0c228ed319a2a43739c7`  
		Last Modified: Fri, 22 Apr 2022 16:24:02 GMT  
		Size: 5.0 MB (4960879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b500a22154605ab8b08473544c72dc700dc6f83895c4efc82544f82f544bbf`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728c706f26744001339dc27c514f27f211b217c21f5fe860bd3e565365cef023`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bf4bee55391723a25240f8a0bd0dfe04b2c3fa9dca71af7f792425ff3aec92`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0f4247067242fb22fccdaa011c8629357ed677cf22255e88d521e5781f0290`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8`

```console
$ docker pull nats@sha256:22c41abdefb5143365ea5d081624e871375d842dbbc08be9dbad1b39ac647693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2803; amd64

### `nats:2.8` - linux; amd64

```console
$ docker pull nats@sha256:e22bfb7fdf9006c8d295782e24a70c2197e340f216b649650ea67288ef841319
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4580124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913890b0a2d48e5c381bcf8b123528904a57150fa69138277620e0ff995dff8b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:3454a426bcdf428c59f748013f6bd917cddf529f8a5032532fee8e7783f2d5e4 in /nats-server 
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:22:23 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:22:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:22:23 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:22:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:804b81b2249803c39d50d8d9262ec5bdb230411989987b9116527a02dbf021a8`  
		Last Modified: Fri, 22 Apr 2022 16:23:12 GMT  
		Size: 4.6 MB (4579616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebd8666e9d6549b9ab43c6349958c6dbb767c779117f02d727d356e3daaf3d`  
		Last Modified: Fri, 22 Apr 2022 16:23:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8` - linux; arm variant v6

```console
$ docker pull nats@sha256:bb39905ea888630c30250ffee5dc2c940c3b95d2a2898b74a7aa139a7007f159
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ce28f90865945806936cfae5ee78d8f2f2598db1ac7086ad1929992f0b3c3a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:50:00 GMT
COPY file:3de61978a9e8a2b166b752a33898d5f146479cdb1ce6ed9df10727fe98f55f51 in /nats-server 
# Fri, 22 Apr 2022 16:50:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:50:01 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:50:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:50:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:50:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a90933979a2530bf92d8ed3112add5a8debe6da238f9becc07b90b414323e402`  
		Last Modified: Fri, 22 Apr 2022 16:52:22 GMT  
		Size: 4.2 MB (4237584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd95754400d2efb409a2eeed76406fade3b92c929c465f6a5c2189183a4e072`  
		Last Modified: Fri, 22 Apr 2022 16:52:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73d094a3eecc53745106d79abcf92f7f2c4959f2c7a607aa8a02aaecf2adc92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d797593dddfb2960ff1bd893323d195aa2e61be166f83abcae8693f1f538cf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 23 Apr 2022 00:08:29 GMT
COPY file:91842064305817f2463830e9925a5bf281c10fa892125e096aa8c52cd100a677 in /nats-server 
# Sat, 23 Apr 2022 00:08:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 23 Apr 2022 00:08:30 GMT
EXPOSE 4222 6222 8222
# Sat, 23 Apr 2022 00:08:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 23 Apr 2022 00:08:31 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 23 Apr 2022 00:08:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ca5997c585d7b90d306ca9e3facb866e5a008db5cfbecedf401e3de574c4445`  
		Last Modified: Sat, 23 Apr 2022 00:10:52 GMT  
		Size: 4.2 MB (4231620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a7a0c9aabdc2939a750f95344dfaf1abde695b5028a9ee42e0b11353fa7c91`  
		Last Modified: Sat, 23 Apr 2022 00:10:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc2a7ab98b1adfcf8b16328efe3416e98bbed6146cffb9289d48b7f1d710f399
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4217735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd22baaa9b7fcf519609324f45785cad127c98aa25e6945ec3bd9144c6b100c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:40:25 GMT
COPY file:a82c07c2e7d51d414d1e87aec6f9d2718447b772505fba86d5ea7617fc1992ac in /nats-server 
# Fri, 22 Apr 2022 16:40:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:40:26 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:40:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:40:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:40:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:308394282a0e57ba139c96f20347213771c895947b7f9625212d7d91ac26cffd`  
		Last Modified: Fri, 22 Apr 2022 16:41:46 GMT  
		Size: 4.2 MB (4217229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a021323d331516d6b6519db1b4d42a2e922c74d6a39588a87e4859c26a9bd85`  
		Last Modified: Fri, 22 Apr 2022 16:41:45 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats@sha256:227efc1752210cbcc77743dc885b3f5ffa9966413a8b7a1ccf182248232c1024
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107725502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b05969443a7a68a122354a2d829e013a0df166ddeec0eff010d310a4b388b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 22 Apr 2022 16:23:26 GMT
RUN cmd /S /C #(nop) COPY file:6453f9106eda3f02af709c31de2264cc25ab8c381441246ced6125fb4dd22377 in C:\nats-server.exe 
# Fri, 22 Apr 2022 16:23:27 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 22 Apr 2022 16:23:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:23:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 22 Apr 2022 16:23:29 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32761659ca35235e4a77458923e43649ba35fc6f6912dffaefb6c1c688212635`  
		Last Modified: Fri, 22 Apr 2022 16:24:23 GMT  
		Size: 4.6 MB (4622930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e54c47f94a9e95b59dd25be3be3811c5356ec1102f4404d94152641988b2a9`  
		Last Modified: Fri, 22 Apr 2022 16:24:18 GMT  
		Size: 1.8 KB (1775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa66f1ddbe51efb72028472b1a3aab1c927cfeb371c3c672134f884cc417a0e`  
		Last Modified: Fri, 22 Apr 2022 16:24:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e4233f94da42224e5744acf20ce233bdf62ca614e821fc6846e7a9c67eb65c`  
		Last Modified: Fri, 22 Apr 2022 16:24:18 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436a600cc67e9fb632157ae49c6290622f0d1e1d7507f692487081fc42681632`  
		Last Modified: Fri, 22 Apr 2022 16:24:17 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-alpine`

```console
$ docker pull nats@sha256:7347f8953fc53551e6fa6c27db5252c50b6537ae979c39b60ff1ec77e6321c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.8-alpine` - linux; amd64

```console
$ docker pull nats@sha256:4e7d4fe05ce93c6c712e1789435da0c99e1bf3ef74db43eaeaef6ca272397766
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7668256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23d872d0d10133874978b8503e1da0a875478f9c36d18274df90f4499c03019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:22:11 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:22:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:22:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:22:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:22:13 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:22:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:22:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e0d861b124a1ab454d3802b3afed8c07d3ec1392b2b86e1dfd9d0d5d6a1f11`  
		Last Modified: Fri, 22 Apr 2022 16:22:48 GMT  
		Size: 4.9 MB (4852697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0473f2dce7bc79ef8358c50e032d4fdf17e3cc1b93deb8a87ba3085118feb4`  
		Last Modified: Fri, 22 Apr 2022 16:22:47 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0efed31ac2d8993794bd5b44f6e003ec74ea05fb15e0385ef8b1048c904f60`  
		Last Modified: Fri, 22 Apr 2022 16:22:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:7091220455f290bada50edec48a24908cbbe489e0aac009ddafe3e9d540fb036
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7133695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd13715b15026d21466ab186bb33954a7a9df237fce3098e994c544a0d58f606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:49:33 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:49:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:49:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:49:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:49:38 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:49:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:49:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6250a52fe67317e7257391e6c81cf0ea21e47617fd095740a0d3607da4130de7`  
		Last Modified: Fri, 22 Apr 2022 16:51:45 GMT  
		Size: 4.5 MB (4510720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26bd4087b8ffb0f3db8c2e503ba7fb78bceadf9db85e703ebe84ed37074a6df`  
		Last Modified: Fri, 22 Apr 2022 16:51:42 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fdd060af20879eea02ac88ca5a8585f86f5a55e2cd469952ede5eec778a11e`  
		Last Modified: Fri, 22 Apr 2022 16:51:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1887a7edb6da6e2a20b927cd6fbecb48badeb2db3b7221fc977cbb9eec8918cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6929602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cda1a747d2d0a65fcb4c9fd4afedda3e72a3e1180cd20b0b3dced91305f2786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Sat, 23 Apr 2022 00:07:56 GMT
ENV NATS_SERVER=2.8.1
# Sat, 23 Apr 2022 00:08:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 23 Apr 2022 00:08:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 23 Apr 2022 00:08:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 23 Apr 2022 00:08:01 GMT
EXPOSE 4222 6222 8222
# Sat, 23 Apr 2022 00:08:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 23 Apr 2022 00:08:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0a1ab4dd191d0a9443e0df830fa3f17872c0fe4e8d5974dc57b3caeec5f2e4`  
		Last Modified: Sat, 23 Apr 2022 00:10:15 GMT  
		Size: 4.5 MB (4504279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2933c6c28dbd5f01a84c1e2dfe6d247cb7a41211d4c1b312c984b49281780c`  
		Last Modified: Sat, 23 Apr 2022 00:10:12 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b7537ba35c1f1dc2e2bf343cc9f4dfac0789e8606e1c365901ee35a69a3620`  
		Last Modified: Sat, 23 Apr 2022 00:10:12 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:01abf8e1249f3267774047ec264d815aa57af333eecb3558e40bf86924f3c7b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7207790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb5bc49254cd7eb6d816b2d62ecd8a1052ce0be9a8fbe0c89cd81ecc053de8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:40:04 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:40:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:40:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:40:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:40:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:40:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2ab5ff26c46d1d386429d02952195bc7699ceedb0288794e9b35e45c82a117`  
		Last Modified: Fri, 22 Apr 2022 16:41:17 GMT  
		Size: 4.5 MB (4490338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e92c2bb8c325e21d94887f856d4590cf00b7a236989ce3f58f00e0e4bd400ea`  
		Last Modified: Fri, 22 Apr 2022 16:41:16 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203649ff8695131a6ebe7b59382b10c48667e76e75bdff0fd07cf378d45aad00`  
		Last Modified: Fri, 22 Apr 2022 16:41:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-alpine3.15`

```console
$ docker pull nats@sha256:7347f8953fc53551e6fa6c27db5252c50b6537ae979c39b60ff1ec77e6321c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.8-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:4e7d4fe05ce93c6c712e1789435da0c99e1bf3ef74db43eaeaef6ca272397766
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7668256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23d872d0d10133874978b8503e1da0a875478f9c36d18274df90f4499c03019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:22:11 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:22:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:22:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:22:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:22:13 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:22:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:22:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e0d861b124a1ab454d3802b3afed8c07d3ec1392b2b86e1dfd9d0d5d6a1f11`  
		Last Modified: Fri, 22 Apr 2022 16:22:48 GMT  
		Size: 4.9 MB (4852697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0473f2dce7bc79ef8358c50e032d4fdf17e3cc1b93deb8a87ba3085118feb4`  
		Last Modified: Fri, 22 Apr 2022 16:22:47 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0efed31ac2d8993794bd5b44f6e003ec74ea05fb15e0385ef8b1048c904f60`  
		Last Modified: Fri, 22 Apr 2022 16:22:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:7091220455f290bada50edec48a24908cbbe489e0aac009ddafe3e9d540fb036
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7133695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd13715b15026d21466ab186bb33954a7a9df237fce3098e994c544a0d58f606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:49:33 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:49:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:49:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:49:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:49:38 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:49:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:49:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6250a52fe67317e7257391e6c81cf0ea21e47617fd095740a0d3607da4130de7`  
		Last Modified: Fri, 22 Apr 2022 16:51:45 GMT  
		Size: 4.5 MB (4510720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26bd4087b8ffb0f3db8c2e503ba7fb78bceadf9db85e703ebe84ed37074a6df`  
		Last Modified: Fri, 22 Apr 2022 16:51:42 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fdd060af20879eea02ac88ca5a8585f86f5a55e2cd469952ede5eec778a11e`  
		Last Modified: Fri, 22 Apr 2022 16:51:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:1887a7edb6da6e2a20b927cd6fbecb48badeb2db3b7221fc977cbb9eec8918cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6929602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cda1a747d2d0a65fcb4c9fd4afedda3e72a3e1180cd20b0b3dced91305f2786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Sat, 23 Apr 2022 00:07:56 GMT
ENV NATS_SERVER=2.8.1
# Sat, 23 Apr 2022 00:08:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 23 Apr 2022 00:08:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 23 Apr 2022 00:08:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 23 Apr 2022 00:08:01 GMT
EXPOSE 4222 6222 8222
# Sat, 23 Apr 2022 00:08:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 23 Apr 2022 00:08:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0a1ab4dd191d0a9443e0df830fa3f17872c0fe4e8d5974dc57b3caeec5f2e4`  
		Last Modified: Sat, 23 Apr 2022 00:10:15 GMT  
		Size: 4.5 MB (4504279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2933c6c28dbd5f01a84c1e2dfe6d247cb7a41211d4c1b312c984b49281780c`  
		Last Modified: Sat, 23 Apr 2022 00:10:12 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b7537ba35c1f1dc2e2bf343cc9f4dfac0789e8606e1c365901ee35a69a3620`  
		Last Modified: Sat, 23 Apr 2022 00:10:12 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:01abf8e1249f3267774047ec264d815aa57af333eecb3558e40bf86924f3c7b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7207790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb5bc49254cd7eb6d816b2d62ecd8a1052ce0be9a8fbe0c89cd81ecc053de8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:40:04 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:40:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:40:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:40:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:40:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:40:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2ab5ff26c46d1d386429d02952195bc7699ceedb0288794e9b35e45c82a117`  
		Last Modified: Fri, 22 Apr 2022 16:41:17 GMT  
		Size: 4.5 MB (4490338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e92c2bb8c325e21d94887f856d4590cf00b7a236989ce3f58f00e0e4bd400ea`  
		Last Modified: Fri, 22 Apr 2022 16:41:16 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203649ff8695131a6ebe7b59382b10c48667e76e75bdff0fd07cf378d45aad00`  
		Last Modified: Fri, 22 Apr 2022 16:41:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-linux`

```console
$ docker pull nats@sha256:9addad33a841b1ca50669b2abe41b55d8d36358b26c33a9ab4d16277e0ac0d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.8-linux` - linux; amd64

```console
$ docker pull nats@sha256:e22bfb7fdf9006c8d295782e24a70c2197e340f216b649650ea67288ef841319
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4580124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913890b0a2d48e5c381bcf8b123528904a57150fa69138277620e0ff995dff8b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:3454a426bcdf428c59f748013f6bd917cddf529f8a5032532fee8e7783f2d5e4 in /nats-server 
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:22:23 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:22:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:22:23 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:22:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:804b81b2249803c39d50d8d9262ec5bdb230411989987b9116527a02dbf021a8`  
		Last Modified: Fri, 22 Apr 2022 16:23:12 GMT  
		Size: 4.6 MB (4579616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebd8666e9d6549b9ab43c6349958c6dbb767c779117f02d727d356e3daaf3d`  
		Last Modified: Fri, 22 Apr 2022 16:23:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:bb39905ea888630c30250ffee5dc2c940c3b95d2a2898b74a7aa139a7007f159
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ce28f90865945806936cfae5ee78d8f2f2598db1ac7086ad1929992f0b3c3a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:50:00 GMT
COPY file:3de61978a9e8a2b166b752a33898d5f146479cdb1ce6ed9df10727fe98f55f51 in /nats-server 
# Fri, 22 Apr 2022 16:50:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:50:01 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:50:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:50:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:50:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a90933979a2530bf92d8ed3112add5a8debe6da238f9becc07b90b414323e402`  
		Last Modified: Fri, 22 Apr 2022 16:52:22 GMT  
		Size: 4.2 MB (4237584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd95754400d2efb409a2eeed76406fade3b92c929c465f6a5c2189183a4e072`  
		Last Modified: Fri, 22 Apr 2022 16:52:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73d094a3eecc53745106d79abcf92f7f2c4959f2c7a607aa8a02aaecf2adc92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d797593dddfb2960ff1bd893323d195aa2e61be166f83abcae8693f1f538cf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 23 Apr 2022 00:08:29 GMT
COPY file:91842064305817f2463830e9925a5bf281c10fa892125e096aa8c52cd100a677 in /nats-server 
# Sat, 23 Apr 2022 00:08:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 23 Apr 2022 00:08:30 GMT
EXPOSE 4222 6222 8222
# Sat, 23 Apr 2022 00:08:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 23 Apr 2022 00:08:31 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 23 Apr 2022 00:08:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ca5997c585d7b90d306ca9e3facb866e5a008db5cfbecedf401e3de574c4445`  
		Last Modified: Sat, 23 Apr 2022 00:10:52 GMT  
		Size: 4.2 MB (4231620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a7a0c9aabdc2939a750f95344dfaf1abde695b5028a9ee42e0b11353fa7c91`  
		Last Modified: Sat, 23 Apr 2022 00:10:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc2a7ab98b1adfcf8b16328efe3416e98bbed6146cffb9289d48b7f1d710f399
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4217735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd22baaa9b7fcf519609324f45785cad127c98aa25e6945ec3bd9144c6b100c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:40:25 GMT
COPY file:a82c07c2e7d51d414d1e87aec6f9d2718447b772505fba86d5ea7617fc1992ac in /nats-server 
# Fri, 22 Apr 2022 16:40:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:40:26 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:40:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:40:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:40:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:308394282a0e57ba139c96f20347213771c895947b7f9625212d7d91ac26cffd`  
		Last Modified: Fri, 22 Apr 2022 16:41:46 GMT  
		Size: 4.2 MB (4217229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a021323d331516d6b6519db1b4d42a2e922c74d6a39588a87e4859c26a9bd85`  
		Last Modified: Fri, 22 Apr 2022 16:41:45 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-nanoserver`

```console
$ docker pull nats@sha256:188160bd678c2674cf45d1685ee2a9c297a10c1ed2cf173855e1dff975e5cb60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats:2.8-nanoserver` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats@sha256:227efc1752210cbcc77743dc885b3f5ffa9966413a8b7a1ccf182248232c1024
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107725502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b05969443a7a68a122354a2d829e013a0df166ddeec0eff010d310a4b388b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 22 Apr 2022 16:23:26 GMT
RUN cmd /S /C #(nop) COPY file:6453f9106eda3f02af709c31de2264cc25ab8c381441246ced6125fb4dd22377 in C:\nats-server.exe 
# Fri, 22 Apr 2022 16:23:27 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 22 Apr 2022 16:23:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:23:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 22 Apr 2022 16:23:29 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32761659ca35235e4a77458923e43649ba35fc6f6912dffaefb6c1c688212635`  
		Last Modified: Fri, 22 Apr 2022 16:24:23 GMT  
		Size: 4.6 MB (4622930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e54c47f94a9e95b59dd25be3be3811c5356ec1102f4404d94152641988b2a9`  
		Last Modified: Fri, 22 Apr 2022 16:24:18 GMT  
		Size: 1.8 KB (1775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa66f1ddbe51efb72028472b1a3aab1c927cfeb371c3c672134f884cc417a0e`  
		Last Modified: Fri, 22 Apr 2022 16:24:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e4233f94da42224e5744acf20ce233bdf62ca614e821fc6846e7a9c67eb65c`  
		Last Modified: Fri, 22 Apr 2022 16:24:18 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436a600cc67e9fb632157ae49c6290622f0d1e1d7507f692487081fc42681632`  
		Last Modified: Fri, 22 Apr 2022 16:24:17 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-nanoserver-1809`

```console
$ docker pull nats@sha256:188160bd678c2674cf45d1685ee2a9c297a10c1ed2cf173855e1dff975e5cb60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats:2.8-nanoserver-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats@sha256:227efc1752210cbcc77743dc885b3f5ffa9966413a8b7a1ccf182248232c1024
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107725502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b05969443a7a68a122354a2d829e013a0df166ddeec0eff010d310a4b388b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 22 Apr 2022 16:23:26 GMT
RUN cmd /S /C #(nop) COPY file:6453f9106eda3f02af709c31de2264cc25ab8c381441246ced6125fb4dd22377 in C:\nats-server.exe 
# Fri, 22 Apr 2022 16:23:27 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 22 Apr 2022 16:23:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:23:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 22 Apr 2022 16:23:29 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32761659ca35235e4a77458923e43649ba35fc6f6912dffaefb6c1c688212635`  
		Last Modified: Fri, 22 Apr 2022 16:24:23 GMT  
		Size: 4.6 MB (4622930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e54c47f94a9e95b59dd25be3be3811c5356ec1102f4404d94152641988b2a9`  
		Last Modified: Fri, 22 Apr 2022 16:24:18 GMT  
		Size: 1.8 KB (1775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa66f1ddbe51efb72028472b1a3aab1c927cfeb371c3c672134f884cc417a0e`  
		Last Modified: Fri, 22 Apr 2022 16:24:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e4233f94da42224e5744acf20ce233bdf62ca614e821fc6846e7a9c67eb65c`  
		Last Modified: Fri, 22 Apr 2022 16:24:18 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436a600cc67e9fb632157ae49c6290622f0d1e1d7507f692487081fc42681632`  
		Last Modified: Fri, 22 Apr 2022 16:24:17 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-scratch`

```console
$ docker pull nats@sha256:9addad33a841b1ca50669b2abe41b55d8d36358b26c33a9ab4d16277e0ac0d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.8-scratch` - linux; amd64

```console
$ docker pull nats@sha256:e22bfb7fdf9006c8d295782e24a70c2197e340f216b649650ea67288ef841319
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4580124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913890b0a2d48e5c381bcf8b123528904a57150fa69138277620e0ff995dff8b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:3454a426bcdf428c59f748013f6bd917cddf529f8a5032532fee8e7783f2d5e4 in /nats-server 
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:22:23 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:22:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:22:23 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:22:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:804b81b2249803c39d50d8d9262ec5bdb230411989987b9116527a02dbf021a8`  
		Last Modified: Fri, 22 Apr 2022 16:23:12 GMT  
		Size: 4.6 MB (4579616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebd8666e9d6549b9ab43c6349958c6dbb767c779117f02d727d356e3daaf3d`  
		Last Modified: Fri, 22 Apr 2022 16:23:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:bb39905ea888630c30250ffee5dc2c940c3b95d2a2898b74a7aa139a7007f159
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ce28f90865945806936cfae5ee78d8f2f2598db1ac7086ad1929992f0b3c3a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:50:00 GMT
COPY file:3de61978a9e8a2b166b752a33898d5f146479cdb1ce6ed9df10727fe98f55f51 in /nats-server 
# Fri, 22 Apr 2022 16:50:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:50:01 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:50:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:50:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:50:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a90933979a2530bf92d8ed3112add5a8debe6da238f9becc07b90b414323e402`  
		Last Modified: Fri, 22 Apr 2022 16:52:22 GMT  
		Size: 4.2 MB (4237584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd95754400d2efb409a2eeed76406fade3b92c929c465f6a5c2189183a4e072`  
		Last Modified: Fri, 22 Apr 2022 16:52:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73d094a3eecc53745106d79abcf92f7f2c4959f2c7a607aa8a02aaecf2adc92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d797593dddfb2960ff1bd893323d195aa2e61be166f83abcae8693f1f538cf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 23 Apr 2022 00:08:29 GMT
COPY file:91842064305817f2463830e9925a5bf281c10fa892125e096aa8c52cd100a677 in /nats-server 
# Sat, 23 Apr 2022 00:08:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 23 Apr 2022 00:08:30 GMT
EXPOSE 4222 6222 8222
# Sat, 23 Apr 2022 00:08:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 23 Apr 2022 00:08:31 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 23 Apr 2022 00:08:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ca5997c585d7b90d306ca9e3facb866e5a008db5cfbecedf401e3de574c4445`  
		Last Modified: Sat, 23 Apr 2022 00:10:52 GMT  
		Size: 4.2 MB (4231620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a7a0c9aabdc2939a750f95344dfaf1abde695b5028a9ee42e0b11353fa7c91`  
		Last Modified: Sat, 23 Apr 2022 00:10:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc2a7ab98b1adfcf8b16328efe3416e98bbed6146cffb9289d48b7f1d710f399
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4217735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd22baaa9b7fcf519609324f45785cad127c98aa25e6945ec3bd9144c6b100c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:40:25 GMT
COPY file:a82c07c2e7d51d414d1e87aec6f9d2718447b772505fba86d5ea7617fc1992ac in /nats-server 
# Fri, 22 Apr 2022 16:40:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:40:26 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:40:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:40:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:40:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:308394282a0e57ba139c96f20347213771c895947b7f9625212d7d91ac26cffd`  
		Last Modified: Fri, 22 Apr 2022 16:41:46 GMT  
		Size: 4.2 MB (4217229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a021323d331516d6b6519db1b4d42a2e922c74d6a39588a87e4859c26a9bd85`  
		Last Modified: Fri, 22 Apr 2022 16:41:45 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-windowsservercore`

```console
$ docker pull nats@sha256:4331838044198073df8afe0ad453fd1eb97f51ec7bde9025303fbbb1189e155d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats:2.8-windowsservercore` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats@sha256:ae5ea527d83182c720c7d1ed179661da4d518fcd64cb5f5dee86948254dcb62c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2721254090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88151b674d5d60f9b53098f2888cdb2b6934a2f3b54d108de2cdb34972019f07`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 12:43:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 14:42:30 GMT
ENV NATS_DOCKERIZED=1
# Fri, 22 Apr 2022 16:20:42 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:20:43 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.1/nats-server-v2.8.1-windows-amd64.zip
# Fri, 22 Apr 2022 16:20:44 GMT
ENV NATS_SERVER_SHASUM=a8c4535897e7973cce5005f7fa71ef0f681a7faf014f8875b5a35e865261ff1f
# Fri, 22 Apr 2022 16:21:42 GMT
RUN Set-PSDebug -Trace 2
# Fri, 22 Apr 2022 16:23:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 22 Apr 2022 16:23:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 22 Apr 2022 16:23:14 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:23:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 22 Apr 2022 16:23:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ebb23aa64bff633cfa3c62b190d84f0e870b04fecb1910f65d0870b5c7f8981`  
		Last Modified: Wed, 13 Apr 2022 14:12:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838c7a98a95bee63894bac798124e8c8572bcacc23e22d85332d453a03a7d7c`  
		Last Modified: Wed, 13 Apr 2022 14:46:17 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8987265b365755a0b758f78710e444da1b49314f15f64aa591dd344430d3fb`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5265b75522ed436be37427e2b945e79901d0288c294b04bea492dbd522b2cfe`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0142ce0f758e44db725dfe50c5e3b301364181c2e9e8505003ea5e5faeb50ab`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1718491c665ff5c4180c99f48ca54ffd756d9e28ce78d0177dc4f5d8974185`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 359.7 KB (359679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4331728196114862c2dc2e870fbee9fb2f0e1f51778d0c228ed319a2a43739c7`  
		Last Modified: Fri, 22 Apr 2022 16:24:02 GMT  
		Size: 5.0 MB (4960879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b500a22154605ab8b08473544c72dc700dc6f83895c4efc82544f82f544bbf`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728c706f26744001339dc27c514f27f211b217c21f5fe860bd3e565365cef023`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bf4bee55391723a25240f8a0bd0dfe04b2c3fa9dca71af7f792425ff3aec92`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0f4247067242fb22fccdaa011c8629357ed677cf22255e88d521e5781f0290`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-windowsservercore-1809`

```console
$ docker pull nats@sha256:4331838044198073df8afe0ad453fd1eb97f51ec7bde9025303fbbb1189e155d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats:2.8-windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats@sha256:ae5ea527d83182c720c7d1ed179661da4d518fcd64cb5f5dee86948254dcb62c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2721254090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88151b674d5d60f9b53098f2888cdb2b6934a2f3b54d108de2cdb34972019f07`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 12:43:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 14:42:30 GMT
ENV NATS_DOCKERIZED=1
# Fri, 22 Apr 2022 16:20:42 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:20:43 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.1/nats-server-v2.8.1-windows-amd64.zip
# Fri, 22 Apr 2022 16:20:44 GMT
ENV NATS_SERVER_SHASUM=a8c4535897e7973cce5005f7fa71ef0f681a7faf014f8875b5a35e865261ff1f
# Fri, 22 Apr 2022 16:21:42 GMT
RUN Set-PSDebug -Trace 2
# Fri, 22 Apr 2022 16:23:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 22 Apr 2022 16:23:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 22 Apr 2022 16:23:14 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:23:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 22 Apr 2022 16:23:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ebb23aa64bff633cfa3c62b190d84f0e870b04fecb1910f65d0870b5c7f8981`  
		Last Modified: Wed, 13 Apr 2022 14:12:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838c7a98a95bee63894bac798124e8c8572bcacc23e22d85332d453a03a7d7c`  
		Last Modified: Wed, 13 Apr 2022 14:46:17 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8987265b365755a0b758f78710e444da1b49314f15f64aa591dd344430d3fb`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5265b75522ed436be37427e2b945e79901d0288c294b04bea492dbd522b2cfe`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0142ce0f758e44db725dfe50c5e3b301364181c2e9e8505003ea5e5faeb50ab`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1718491c665ff5c4180c99f48ca54ffd756d9e28ce78d0177dc4f5d8974185`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 359.7 KB (359679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4331728196114862c2dc2e870fbee9fb2f0e1f51778d0c228ed319a2a43739c7`  
		Last Modified: Fri, 22 Apr 2022 16:24:02 GMT  
		Size: 5.0 MB (4960879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b500a22154605ab8b08473544c72dc700dc6f83895c4efc82544f82f544bbf`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728c706f26744001339dc27c514f27f211b217c21f5fe860bd3e565365cef023`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bf4bee55391723a25240f8a0bd0dfe04b2c3fa9dca71af7f792425ff3aec92`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0f4247067242fb22fccdaa011c8629357ed677cf22255e88d521e5781f0290`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8.2`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `nats:2.8.2-alpine`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `nats:2.8.2-alpine3.15`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `nats:2.8.2-linux`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `nats:2.8.2-nanoserver`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `nats:2.8.2-nanoserver-1809`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `nats:2.8.2-scratch`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `nats:2.8.2-windowsservercore`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `nats:2.8.2-windowsservercore-1809`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `nats:alpine`

```console
$ docker pull nats@sha256:7347f8953fc53551e6fa6c27db5252c50b6537ae979c39b60ff1ec77e6321c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:4e7d4fe05ce93c6c712e1789435da0c99e1bf3ef74db43eaeaef6ca272397766
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7668256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23d872d0d10133874978b8503e1da0a875478f9c36d18274df90f4499c03019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:22:11 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:22:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:22:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:22:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:22:13 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:22:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:22:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e0d861b124a1ab454d3802b3afed8c07d3ec1392b2b86e1dfd9d0d5d6a1f11`  
		Last Modified: Fri, 22 Apr 2022 16:22:48 GMT  
		Size: 4.9 MB (4852697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0473f2dce7bc79ef8358c50e032d4fdf17e3cc1b93deb8a87ba3085118feb4`  
		Last Modified: Fri, 22 Apr 2022 16:22:47 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0efed31ac2d8993794bd5b44f6e003ec74ea05fb15e0385ef8b1048c904f60`  
		Last Modified: Fri, 22 Apr 2022 16:22:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:7091220455f290bada50edec48a24908cbbe489e0aac009ddafe3e9d540fb036
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7133695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd13715b15026d21466ab186bb33954a7a9df237fce3098e994c544a0d58f606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:49:33 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:49:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:49:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:49:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:49:38 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:49:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:49:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6250a52fe67317e7257391e6c81cf0ea21e47617fd095740a0d3607da4130de7`  
		Last Modified: Fri, 22 Apr 2022 16:51:45 GMT  
		Size: 4.5 MB (4510720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26bd4087b8ffb0f3db8c2e503ba7fb78bceadf9db85e703ebe84ed37074a6df`  
		Last Modified: Fri, 22 Apr 2022 16:51:42 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fdd060af20879eea02ac88ca5a8585f86f5a55e2cd469952ede5eec778a11e`  
		Last Modified: Fri, 22 Apr 2022 16:51:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1887a7edb6da6e2a20b927cd6fbecb48badeb2db3b7221fc977cbb9eec8918cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6929602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cda1a747d2d0a65fcb4c9fd4afedda3e72a3e1180cd20b0b3dced91305f2786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Sat, 23 Apr 2022 00:07:56 GMT
ENV NATS_SERVER=2.8.1
# Sat, 23 Apr 2022 00:08:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 23 Apr 2022 00:08:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 23 Apr 2022 00:08:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 23 Apr 2022 00:08:01 GMT
EXPOSE 4222 6222 8222
# Sat, 23 Apr 2022 00:08:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 23 Apr 2022 00:08:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0a1ab4dd191d0a9443e0df830fa3f17872c0fe4e8d5974dc57b3caeec5f2e4`  
		Last Modified: Sat, 23 Apr 2022 00:10:15 GMT  
		Size: 4.5 MB (4504279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2933c6c28dbd5f01a84c1e2dfe6d247cb7a41211d4c1b312c984b49281780c`  
		Last Modified: Sat, 23 Apr 2022 00:10:12 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b7537ba35c1f1dc2e2bf343cc9f4dfac0789e8606e1c365901ee35a69a3620`  
		Last Modified: Sat, 23 Apr 2022 00:10:12 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:01abf8e1249f3267774047ec264d815aa57af333eecb3558e40bf86924f3c7b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7207790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb5bc49254cd7eb6d816b2d62ecd8a1052ce0be9a8fbe0c89cd81ecc053de8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:40:04 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:40:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:40:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:40:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:40:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:40:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2ab5ff26c46d1d386429d02952195bc7699ceedb0288794e9b35e45c82a117`  
		Last Modified: Fri, 22 Apr 2022 16:41:17 GMT  
		Size: 4.5 MB (4490338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e92c2bb8c325e21d94887f856d4590cf00b7a236989ce3f58f00e0e4bd400ea`  
		Last Modified: Fri, 22 Apr 2022 16:41:16 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203649ff8695131a6ebe7b59382b10c48667e76e75bdff0fd07cf378d45aad00`  
		Last Modified: Fri, 22 Apr 2022 16:41:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.15`

```console
$ docker pull nats@sha256:7347f8953fc53551e6fa6c27db5252c50b6537ae979c39b60ff1ec77e6321c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:4e7d4fe05ce93c6c712e1789435da0c99e1bf3ef74db43eaeaef6ca272397766
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7668256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23d872d0d10133874978b8503e1da0a875478f9c36d18274df90f4499c03019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:22:11 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:22:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:22:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:22:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:22:13 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:22:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:22:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e0d861b124a1ab454d3802b3afed8c07d3ec1392b2b86e1dfd9d0d5d6a1f11`  
		Last Modified: Fri, 22 Apr 2022 16:22:48 GMT  
		Size: 4.9 MB (4852697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0473f2dce7bc79ef8358c50e032d4fdf17e3cc1b93deb8a87ba3085118feb4`  
		Last Modified: Fri, 22 Apr 2022 16:22:47 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0efed31ac2d8993794bd5b44f6e003ec74ea05fb15e0385ef8b1048c904f60`  
		Last Modified: Fri, 22 Apr 2022 16:22:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:7091220455f290bada50edec48a24908cbbe489e0aac009ddafe3e9d540fb036
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7133695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd13715b15026d21466ab186bb33954a7a9df237fce3098e994c544a0d58f606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:49:33 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:49:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:49:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:49:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:49:38 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:49:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:49:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6250a52fe67317e7257391e6c81cf0ea21e47617fd095740a0d3607da4130de7`  
		Last Modified: Fri, 22 Apr 2022 16:51:45 GMT  
		Size: 4.5 MB (4510720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26bd4087b8ffb0f3db8c2e503ba7fb78bceadf9db85e703ebe84ed37074a6df`  
		Last Modified: Fri, 22 Apr 2022 16:51:42 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fdd060af20879eea02ac88ca5a8585f86f5a55e2cd469952ede5eec778a11e`  
		Last Modified: Fri, 22 Apr 2022 16:51:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:1887a7edb6da6e2a20b927cd6fbecb48badeb2db3b7221fc977cbb9eec8918cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6929602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cda1a747d2d0a65fcb4c9fd4afedda3e72a3e1180cd20b0b3dced91305f2786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Sat, 23 Apr 2022 00:07:56 GMT
ENV NATS_SERVER=2.8.1
# Sat, 23 Apr 2022 00:08:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 23 Apr 2022 00:08:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 23 Apr 2022 00:08:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 23 Apr 2022 00:08:01 GMT
EXPOSE 4222 6222 8222
# Sat, 23 Apr 2022 00:08:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 23 Apr 2022 00:08:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0a1ab4dd191d0a9443e0df830fa3f17872c0fe4e8d5974dc57b3caeec5f2e4`  
		Last Modified: Sat, 23 Apr 2022 00:10:15 GMT  
		Size: 4.5 MB (4504279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2933c6c28dbd5f01a84c1e2dfe6d247cb7a41211d4c1b312c984b49281780c`  
		Last Modified: Sat, 23 Apr 2022 00:10:12 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b7537ba35c1f1dc2e2bf343cc9f4dfac0789e8606e1c365901ee35a69a3620`  
		Last Modified: Sat, 23 Apr 2022 00:10:12 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:01abf8e1249f3267774047ec264d815aa57af333eecb3558e40bf86924f3c7b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7207790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb5bc49254cd7eb6d816b2d62ecd8a1052ce0be9a8fbe0c89cd81ecc053de8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:40:04 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:40:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:40:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:40:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:40:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:40:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2ab5ff26c46d1d386429d02952195bc7699ceedb0288794e9b35e45c82a117`  
		Last Modified: Fri, 22 Apr 2022 16:41:17 GMT  
		Size: 4.5 MB (4490338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e92c2bb8c325e21d94887f856d4590cf00b7a236989ce3f58f00e0e4bd400ea`  
		Last Modified: Fri, 22 Apr 2022 16:41:16 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203649ff8695131a6ebe7b59382b10c48667e76e75bdff0fd07cf378d45aad00`  
		Last Modified: Fri, 22 Apr 2022 16:41:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:22c41abdefb5143365ea5d081624e871375d842dbbc08be9dbad1b39ac647693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2803; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:e22bfb7fdf9006c8d295782e24a70c2197e340f216b649650ea67288ef841319
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4580124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913890b0a2d48e5c381bcf8b123528904a57150fa69138277620e0ff995dff8b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:3454a426bcdf428c59f748013f6bd917cddf529f8a5032532fee8e7783f2d5e4 in /nats-server 
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:22:23 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:22:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:22:23 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:22:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:804b81b2249803c39d50d8d9262ec5bdb230411989987b9116527a02dbf021a8`  
		Last Modified: Fri, 22 Apr 2022 16:23:12 GMT  
		Size: 4.6 MB (4579616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebd8666e9d6549b9ab43c6349958c6dbb767c779117f02d727d356e3daaf3d`  
		Last Modified: Fri, 22 Apr 2022 16:23:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:bb39905ea888630c30250ffee5dc2c940c3b95d2a2898b74a7aa139a7007f159
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ce28f90865945806936cfae5ee78d8f2f2598db1ac7086ad1929992f0b3c3a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:50:00 GMT
COPY file:3de61978a9e8a2b166b752a33898d5f146479cdb1ce6ed9df10727fe98f55f51 in /nats-server 
# Fri, 22 Apr 2022 16:50:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:50:01 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:50:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:50:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:50:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a90933979a2530bf92d8ed3112add5a8debe6da238f9becc07b90b414323e402`  
		Last Modified: Fri, 22 Apr 2022 16:52:22 GMT  
		Size: 4.2 MB (4237584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd95754400d2efb409a2eeed76406fade3b92c929c465f6a5c2189183a4e072`  
		Last Modified: Fri, 22 Apr 2022 16:52:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73d094a3eecc53745106d79abcf92f7f2c4959f2c7a607aa8a02aaecf2adc92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d797593dddfb2960ff1bd893323d195aa2e61be166f83abcae8693f1f538cf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 23 Apr 2022 00:08:29 GMT
COPY file:91842064305817f2463830e9925a5bf281c10fa892125e096aa8c52cd100a677 in /nats-server 
# Sat, 23 Apr 2022 00:08:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 23 Apr 2022 00:08:30 GMT
EXPOSE 4222 6222 8222
# Sat, 23 Apr 2022 00:08:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 23 Apr 2022 00:08:31 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 23 Apr 2022 00:08:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ca5997c585d7b90d306ca9e3facb866e5a008db5cfbecedf401e3de574c4445`  
		Last Modified: Sat, 23 Apr 2022 00:10:52 GMT  
		Size: 4.2 MB (4231620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a7a0c9aabdc2939a750f95344dfaf1abde695b5028a9ee42e0b11353fa7c91`  
		Last Modified: Sat, 23 Apr 2022 00:10:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc2a7ab98b1adfcf8b16328efe3416e98bbed6146cffb9289d48b7f1d710f399
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4217735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd22baaa9b7fcf519609324f45785cad127c98aa25e6945ec3bd9144c6b100c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:40:25 GMT
COPY file:a82c07c2e7d51d414d1e87aec6f9d2718447b772505fba86d5ea7617fc1992ac in /nats-server 
# Fri, 22 Apr 2022 16:40:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:40:26 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:40:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:40:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:40:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:308394282a0e57ba139c96f20347213771c895947b7f9625212d7d91ac26cffd`  
		Last Modified: Fri, 22 Apr 2022 16:41:46 GMT  
		Size: 4.2 MB (4217229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a021323d331516d6b6519db1b4d42a2e922c74d6a39588a87e4859c26a9bd85`  
		Last Modified: Fri, 22 Apr 2022 16:41:45 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats@sha256:227efc1752210cbcc77743dc885b3f5ffa9966413a8b7a1ccf182248232c1024
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107725502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b05969443a7a68a122354a2d829e013a0df166ddeec0eff010d310a4b388b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 22 Apr 2022 16:23:26 GMT
RUN cmd /S /C #(nop) COPY file:6453f9106eda3f02af709c31de2264cc25ab8c381441246ced6125fb4dd22377 in C:\nats-server.exe 
# Fri, 22 Apr 2022 16:23:27 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 22 Apr 2022 16:23:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:23:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 22 Apr 2022 16:23:29 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32761659ca35235e4a77458923e43649ba35fc6f6912dffaefb6c1c688212635`  
		Last Modified: Fri, 22 Apr 2022 16:24:23 GMT  
		Size: 4.6 MB (4622930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e54c47f94a9e95b59dd25be3be3811c5356ec1102f4404d94152641988b2a9`  
		Last Modified: Fri, 22 Apr 2022 16:24:18 GMT  
		Size: 1.8 KB (1775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa66f1ddbe51efb72028472b1a3aab1c927cfeb371c3c672134f884cc417a0e`  
		Last Modified: Fri, 22 Apr 2022 16:24:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e4233f94da42224e5744acf20ce233bdf62ca614e821fc6846e7a9c67eb65c`  
		Last Modified: Fri, 22 Apr 2022 16:24:18 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436a600cc67e9fb632157ae49c6290622f0d1e1d7507f692487081fc42681632`  
		Last Modified: Fri, 22 Apr 2022 16:24:17 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:9addad33a841b1ca50669b2abe41b55d8d36358b26c33a9ab4d16277e0ac0d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:e22bfb7fdf9006c8d295782e24a70c2197e340f216b649650ea67288ef841319
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4580124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913890b0a2d48e5c381bcf8b123528904a57150fa69138277620e0ff995dff8b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:3454a426bcdf428c59f748013f6bd917cddf529f8a5032532fee8e7783f2d5e4 in /nats-server 
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:22:23 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:22:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:22:23 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:22:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:804b81b2249803c39d50d8d9262ec5bdb230411989987b9116527a02dbf021a8`  
		Last Modified: Fri, 22 Apr 2022 16:23:12 GMT  
		Size: 4.6 MB (4579616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebd8666e9d6549b9ab43c6349958c6dbb767c779117f02d727d356e3daaf3d`  
		Last Modified: Fri, 22 Apr 2022 16:23:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:bb39905ea888630c30250ffee5dc2c940c3b95d2a2898b74a7aa139a7007f159
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ce28f90865945806936cfae5ee78d8f2f2598db1ac7086ad1929992f0b3c3a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:50:00 GMT
COPY file:3de61978a9e8a2b166b752a33898d5f146479cdb1ce6ed9df10727fe98f55f51 in /nats-server 
# Fri, 22 Apr 2022 16:50:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:50:01 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:50:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:50:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:50:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a90933979a2530bf92d8ed3112add5a8debe6da238f9becc07b90b414323e402`  
		Last Modified: Fri, 22 Apr 2022 16:52:22 GMT  
		Size: 4.2 MB (4237584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd95754400d2efb409a2eeed76406fade3b92c929c465f6a5c2189183a4e072`  
		Last Modified: Fri, 22 Apr 2022 16:52:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73d094a3eecc53745106d79abcf92f7f2c4959f2c7a607aa8a02aaecf2adc92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d797593dddfb2960ff1bd893323d195aa2e61be166f83abcae8693f1f538cf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 23 Apr 2022 00:08:29 GMT
COPY file:91842064305817f2463830e9925a5bf281c10fa892125e096aa8c52cd100a677 in /nats-server 
# Sat, 23 Apr 2022 00:08:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 23 Apr 2022 00:08:30 GMT
EXPOSE 4222 6222 8222
# Sat, 23 Apr 2022 00:08:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 23 Apr 2022 00:08:31 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 23 Apr 2022 00:08:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ca5997c585d7b90d306ca9e3facb866e5a008db5cfbecedf401e3de574c4445`  
		Last Modified: Sat, 23 Apr 2022 00:10:52 GMT  
		Size: 4.2 MB (4231620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a7a0c9aabdc2939a750f95344dfaf1abde695b5028a9ee42e0b11353fa7c91`  
		Last Modified: Sat, 23 Apr 2022 00:10:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc2a7ab98b1adfcf8b16328efe3416e98bbed6146cffb9289d48b7f1d710f399
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4217735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd22baaa9b7fcf519609324f45785cad127c98aa25e6945ec3bd9144c6b100c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:40:25 GMT
COPY file:a82c07c2e7d51d414d1e87aec6f9d2718447b772505fba86d5ea7617fc1992ac in /nats-server 
# Fri, 22 Apr 2022 16:40:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:40:26 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:40:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:40:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:40:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:308394282a0e57ba139c96f20347213771c895947b7f9625212d7d91ac26cffd`  
		Last Modified: Fri, 22 Apr 2022 16:41:46 GMT  
		Size: 4.2 MB (4217229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a021323d331516d6b6519db1b4d42a2e922c74d6a39588a87e4859c26a9bd85`  
		Last Modified: Fri, 22 Apr 2022 16:41:45 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:188160bd678c2674cf45d1685ee2a9c297a10c1ed2cf173855e1dff975e5cb60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats:nanoserver` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats@sha256:227efc1752210cbcc77743dc885b3f5ffa9966413a8b7a1ccf182248232c1024
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107725502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b05969443a7a68a122354a2d829e013a0df166ddeec0eff010d310a4b388b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 22 Apr 2022 16:23:26 GMT
RUN cmd /S /C #(nop) COPY file:6453f9106eda3f02af709c31de2264cc25ab8c381441246ced6125fb4dd22377 in C:\nats-server.exe 
# Fri, 22 Apr 2022 16:23:27 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 22 Apr 2022 16:23:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:23:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 22 Apr 2022 16:23:29 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32761659ca35235e4a77458923e43649ba35fc6f6912dffaefb6c1c688212635`  
		Last Modified: Fri, 22 Apr 2022 16:24:23 GMT  
		Size: 4.6 MB (4622930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e54c47f94a9e95b59dd25be3be3811c5356ec1102f4404d94152641988b2a9`  
		Last Modified: Fri, 22 Apr 2022 16:24:18 GMT  
		Size: 1.8 KB (1775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa66f1ddbe51efb72028472b1a3aab1c927cfeb371c3c672134f884cc417a0e`  
		Last Modified: Fri, 22 Apr 2022 16:24:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e4233f94da42224e5744acf20ce233bdf62ca614e821fc6846e7a9c67eb65c`  
		Last Modified: Fri, 22 Apr 2022 16:24:18 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436a600cc67e9fb632157ae49c6290622f0d1e1d7507f692487081fc42681632`  
		Last Modified: Fri, 22 Apr 2022 16:24:17 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:188160bd678c2674cf45d1685ee2a9c297a10c1ed2cf173855e1dff975e5cb60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats@sha256:227efc1752210cbcc77743dc885b3f5ffa9966413a8b7a1ccf182248232c1024
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107725502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b05969443a7a68a122354a2d829e013a0df166ddeec0eff010d310a4b388b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 22 Apr 2022 16:23:26 GMT
RUN cmd /S /C #(nop) COPY file:6453f9106eda3f02af709c31de2264cc25ab8c381441246ced6125fb4dd22377 in C:\nats-server.exe 
# Fri, 22 Apr 2022 16:23:27 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 22 Apr 2022 16:23:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:23:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 22 Apr 2022 16:23:29 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32761659ca35235e4a77458923e43649ba35fc6f6912dffaefb6c1c688212635`  
		Last Modified: Fri, 22 Apr 2022 16:24:23 GMT  
		Size: 4.6 MB (4622930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e54c47f94a9e95b59dd25be3be3811c5356ec1102f4404d94152641988b2a9`  
		Last Modified: Fri, 22 Apr 2022 16:24:18 GMT  
		Size: 1.8 KB (1775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa66f1ddbe51efb72028472b1a3aab1c927cfeb371c3c672134f884cc417a0e`  
		Last Modified: Fri, 22 Apr 2022 16:24:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e4233f94da42224e5744acf20ce233bdf62ca614e821fc6846e7a9c67eb65c`  
		Last Modified: Fri, 22 Apr 2022 16:24:18 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436a600cc67e9fb632157ae49c6290622f0d1e1d7507f692487081fc42681632`  
		Last Modified: Fri, 22 Apr 2022 16:24:17 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:9addad33a841b1ca50669b2abe41b55d8d36358b26c33a9ab4d16277e0ac0d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:e22bfb7fdf9006c8d295782e24a70c2197e340f216b649650ea67288ef841319
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4580124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913890b0a2d48e5c381bcf8b123528904a57150fa69138277620e0ff995dff8b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:3454a426bcdf428c59f748013f6bd917cddf529f8a5032532fee8e7783f2d5e4 in /nats-server 
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:22:23 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:22:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:22:23 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:22:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:804b81b2249803c39d50d8d9262ec5bdb230411989987b9116527a02dbf021a8`  
		Last Modified: Fri, 22 Apr 2022 16:23:12 GMT  
		Size: 4.6 MB (4579616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebd8666e9d6549b9ab43c6349958c6dbb767c779117f02d727d356e3daaf3d`  
		Last Modified: Fri, 22 Apr 2022 16:23:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:bb39905ea888630c30250ffee5dc2c940c3b95d2a2898b74a7aa139a7007f159
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ce28f90865945806936cfae5ee78d8f2f2598db1ac7086ad1929992f0b3c3a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:50:00 GMT
COPY file:3de61978a9e8a2b166b752a33898d5f146479cdb1ce6ed9df10727fe98f55f51 in /nats-server 
# Fri, 22 Apr 2022 16:50:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:50:01 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:50:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:50:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:50:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a90933979a2530bf92d8ed3112add5a8debe6da238f9becc07b90b414323e402`  
		Last Modified: Fri, 22 Apr 2022 16:52:22 GMT  
		Size: 4.2 MB (4237584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd95754400d2efb409a2eeed76406fade3b92c929c465f6a5c2189183a4e072`  
		Last Modified: Fri, 22 Apr 2022 16:52:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73d094a3eecc53745106d79abcf92f7f2c4959f2c7a607aa8a02aaecf2adc92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d797593dddfb2960ff1bd893323d195aa2e61be166f83abcae8693f1f538cf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 23 Apr 2022 00:08:29 GMT
COPY file:91842064305817f2463830e9925a5bf281c10fa892125e096aa8c52cd100a677 in /nats-server 
# Sat, 23 Apr 2022 00:08:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 23 Apr 2022 00:08:30 GMT
EXPOSE 4222 6222 8222
# Sat, 23 Apr 2022 00:08:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 23 Apr 2022 00:08:31 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 23 Apr 2022 00:08:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ca5997c585d7b90d306ca9e3facb866e5a008db5cfbecedf401e3de574c4445`  
		Last Modified: Sat, 23 Apr 2022 00:10:52 GMT  
		Size: 4.2 MB (4231620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a7a0c9aabdc2939a750f95344dfaf1abde695b5028a9ee42e0b11353fa7c91`  
		Last Modified: Sat, 23 Apr 2022 00:10:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc2a7ab98b1adfcf8b16328efe3416e98bbed6146cffb9289d48b7f1d710f399
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4217735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd22baaa9b7fcf519609324f45785cad127c98aa25e6945ec3bd9144c6b100c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:40:25 GMT
COPY file:a82c07c2e7d51d414d1e87aec6f9d2718447b772505fba86d5ea7617fc1992ac in /nats-server 
# Fri, 22 Apr 2022 16:40:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:40:26 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:40:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:40:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:40:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:308394282a0e57ba139c96f20347213771c895947b7f9625212d7d91ac26cffd`  
		Last Modified: Fri, 22 Apr 2022 16:41:46 GMT  
		Size: 4.2 MB (4217229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a021323d331516d6b6519db1b4d42a2e922c74d6a39588a87e4859c26a9bd85`  
		Last Modified: Fri, 22 Apr 2022 16:41:45 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:4331838044198073df8afe0ad453fd1eb97f51ec7bde9025303fbbb1189e155d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats:windowsservercore` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats@sha256:ae5ea527d83182c720c7d1ed179661da4d518fcd64cb5f5dee86948254dcb62c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2721254090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88151b674d5d60f9b53098f2888cdb2b6934a2f3b54d108de2cdb34972019f07`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 12:43:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 14:42:30 GMT
ENV NATS_DOCKERIZED=1
# Fri, 22 Apr 2022 16:20:42 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:20:43 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.1/nats-server-v2.8.1-windows-amd64.zip
# Fri, 22 Apr 2022 16:20:44 GMT
ENV NATS_SERVER_SHASUM=a8c4535897e7973cce5005f7fa71ef0f681a7faf014f8875b5a35e865261ff1f
# Fri, 22 Apr 2022 16:21:42 GMT
RUN Set-PSDebug -Trace 2
# Fri, 22 Apr 2022 16:23:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 22 Apr 2022 16:23:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 22 Apr 2022 16:23:14 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:23:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 22 Apr 2022 16:23:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ebb23aa64bff633cfa3c62b190d84f0e870b04fecb1910f65d0870b5c7f8981`  
		Last Modified: Wed, 13 Apr 2022 14:12:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838c7a98a95bee63894bac798124e8c8572bcacc23e22d85332d453a03a7d7c`  
		Last Modified: Wed, 13 Apr 2022 14:46:17 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8987265b365755a0b758f78710e444da1b49314f15f64aa591dd344430d3fb`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5265b75522ed436be37427e2b945e79901d0288c294b04bea492dbd522b2cfe`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0142ce0f758e44db725dfe50c5e3b301364181c2e9e8505003ea5e5faeb50ab`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1718491c665ff5c4180c99f48ca54ffd756d9e28ce78d0177dc4f5d8974185`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 359.7 KB (359679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4331728196114862c2dc2e870fbee9fb2f0e1f51778d0c228ed319a2a43739c7`  
		Last Modified: Fri, 22 Apr 2022 16:24:02 GMT  
		Size: 5.0 MB (4960879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b500a22154605ab8b08473544c72dc700dc6f83895c4efc82544f82f544bbf`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728c706f26744001339dc27c514f27f211b217c21f5fe860bd3e565365cef023`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bf4bee55391723a25240f8a0bd0dfe04b2c3fa9dca71af7f792425ff3aec92`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0f4247067242fb22fccdaa011c8629357ed677cf22255e88d521e5781f0290`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:4331838044198073df8afe0ad453fd1eb97f51ec7bde9025303fbbb1189e155d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats@sha256:ae5ea527d83182c720c7d1ed179661da4d518fcd64cb5f5dee86948254dcb62c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2721254090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88151b674d5d60f9b53098f2888cdb2b6934a2f3b54d108de2cdb34972019f07`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 12:43:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 14:42:30 GMT
ENV NATS_DOCKERIZED=1
# Fri, 22 Apr 2022 16:20:42 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:20:43 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.1/nats-server-v2.8.1-windows-amd64.zip
# Fri, 22 Apr 2022 16:20:44 GMT
ENV NATS_SERVER_SHASUM=a8c4535897e7973cce5005f7fa71ef0f681a7faf014f8875b5a35e865261ff1f
# Fri, 22 Apr 2022 16:21:42 GMT
RUN Set-PSDebug -Trace 2
# Fri, 22 Apr 2022 16:23:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 22 Apr 2022 16:23:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 22 Apr 2022 16:23:14 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:23:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 22 Apr 2022 16:23:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ebb23aa64bff633cfa3c62b190d84f0e870b04fecb1910f65d0870b5c7f8981`  
		Last Modified: Wed, 13 Apr 2022 14:12:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838c7a98a95bee63894bac798124e8c8572bcacc23e22d85332d453a03a7d7c`  
		Last Modified: Wed, 13 Apr 2022 14:46:17 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8987265b365755a0b758f78710e444da1b49314f15f64aa591dd344430d3fb`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5265b75522ed436be37427e2b945e79901d0288c294b04bea492dbd522b2cfe`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0142ce0f758e44db725dfe50c5e3b301364181c2e9e8505003ea5e5faeb50ab`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1718491c665ff5c4180c99f48ca54ffd756d9e28ce78d0177dc4f5d8974185`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 359.7 KB (359679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4331728196114862c2dc2e870fbee9fb2f0e1f51778d0c228ed319a2a43739c7`  
		Last Modified: Fri, 22 Apr 2022 16:24:02 GMT  
		Size: 5.0 MB (4960879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b500a22154605ab8b08473544c72dc700dc6f83895c4efc82544f82f544bbf`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728c706f26744001339dc27c514f27f211b217c21f5fe860bd3e565365cef023`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bf4bee55391723a25240f8a0bd0dfe04b2c3fa9dca71af7f792425ff3aec92`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0f4247067242fb22fccdaa011c8629357ed677cf22255e88d521e5781f0290`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

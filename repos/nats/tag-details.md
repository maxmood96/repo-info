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
-	[`nats:2.7`](#nats27)
-	[`nats:2.7-alpine`](#nats27-alpine)
-	[`nats:2.7-alpine3.15`](#nats27-alpine315)
-	[`nats:2.7-linux`](#nats27-linux)
-	[`nats:2.7-nanoserver`](#nats27-nanoserver)
-	[`nats:2.7-nanoserver-1809`](#nats27-nanoserver-1809)
-	[`nats:2.7-scratch`](#nats27-scratch)
-	[`nats:2.7-windowsservercore`](#nats27-windowsservercore)
-	[`nats:2.7-windowsservercore-1809`](#nats27-windowsservercore-1809)
-	[`nats:2.7.2`](#nats272)
-	[`nats:2.7.2-alpine`](#nats272-alpine)
-	[`nats:2.7.2-alpine3.15`](#nats272-alpine315)
-	[`nats:2.7.2-linux`](#nats272-linux)
-	[`nats:2.7.2-nanoserver`](#nats272-nanoserver)
-	[`nats:2.7.2-nanoserver-1809`](#nats272-nanoserver-1809)
-	[`nats:2.7.2-scratch`](#nats272-scratch)
-	[`nats:2.7.2-windowsservercore`](#nats272-windowsservercore)
-	[`nats:2.7.2-windowsservercore-1809`](#nats272-windowsservercore-1809)
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
$ docker pull nats@sha256:cad2f8a76874a8011aede58fc3d064dbe5cd6ca5f244cd127c2614fd6eefc62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2458; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:3d7301d591b5ac27e95a6632733f104f9507986c46feb51ab911a8410f0264c8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107575564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948555d0919d6e1d2b1500bd9f7e11a9dc09dccd1da752619916a751bc03a84b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 26 Jan 2022 01:18:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:18:33 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Fri, 04 Feb 2022 23:18:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5cb841e15906c5eda43ff713132f917ee3c8f180a706900af652f1e93eeb1790`  
		Last Modified: Wed, 26 Jan 2022 01:19:36 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b67013be4d12b054b27a0b91ace36c3f8222cd350392424ced1c970747994d`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 4.5 MB (4522588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1805e78a4fad9c9cb97d2814ce2dbb2df363473ddf91ce6461544ffbd2070d`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a09a68fc240bc35491ff997dbab51436d375aa293b751496f953d06e84e07`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db154e2963b998e6bb84fff4b0a7796597d4cbe0e5cee24be6e4652a7c1356fe`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb7933f5f3359a26b455d45dccb368fd5783bccc73c1a2d7faac4001e95c6d0`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:8b3fb2423a8cce4607ef30a990b35545afe0a3c613cd05b8eec7b483df268b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:89eb697c14f6556d6fb2703240e48d9600b40b408dda60ae36e262425a4431e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cd50aa7198f5c12f156d09daa0ddc1112236fff6860f120a2251d96ff9eb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 05:59:05 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 05:59:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 05:59:08 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 05:59:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802d7c7e4ac6a66227b2370fdcdf5a6a23823257ca471179abfd0902b956fd7`  
		Last Modified: Sat, 05 Feb 2022 06:00:25 GMT  
		Size: 4.8 MB (4753836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426dd83cc6600f256ef35338c32eaf3d0399bab79c1246ec09184bdd1ea5b1f`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93f969dc9e9707d1fb2f5eaf6e9636680ca5b3cdfe45b8466a97b0105f036ba`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:26c9fd5ce79bfefe188314878ab0f821a0fbca95fcfbe50f92e81d7f4484ec10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7052346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b52e6eb1b52cca05de6f415e6236b2bd399ce0fb9f1d1ce06066a1558de8e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 00:57:59 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 00:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 00:58:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 00:58:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e778c855e77141dc3829b1882837f8ec9f4bc5a650dd40a2917a225e1c15d0d`  
		Last Modified: Sat, 05 Feb 2022 01:00:11 GMT  
		Size: 4.4 MB (4419922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8accecf8efa4c43a09a141647ccf09dc6a56558b970610993d7fdbee2275956f`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7dff5d8e4ec08b7521acbd3a01a86b9f803f821c99252b840a0491493b43b`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9f1dff6dca496cefa436b4db1fa8fa857eb557bd0a6e6760c9b296f096bde9e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6847919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc4a088149c39457ad06caa0dedec762d0dcf09f2ae4743592c4d418f8e890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 06:12:22 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 06:12:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 06:12:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 06:12:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 06:12:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 06:12:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603aa49db7f9a89152dcd7cdf78b402ef16aff3bb40294f6c66a933f07378ee0`  
		Last Modified: Sat, 05 Feb 2022 06:14:40 GMT  
		Size: 4.4 MB (4412155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ab40c3eba476ac4d53154b86201d8626e858e7ed7651fc1045021e03587fee`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ec7b9832ec0d741d78be9c59991717e8a0a7b188c6ac0252cee24c879dcfcf`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b23b110a6166fdd559bbdf992cff078caa3eeb7e37fa86d2cf2765bdddd7898
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7114722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c3ca4ead676b4547ea7e17b1a67ffc43fc9e9a70f9fbbc6dfbe03a6615799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 04:08:44 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 04:08:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 04:08:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 04:08:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 04:08:50 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 04:08:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039e8b74114ddf2278e01658eb7e01be08056565bae8a2955645300b982fb0f2`  
		Last Modified: Sat, 05 Feb 2022 04:09:53 GMT  
		Size: 4.4 MB (4398315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76361110853d49e5895bb2123f92f8e3f8f1a08ce01c8ccda76acb70a73d7e22`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a80240856cec2d4b5bcd8aaff898e547e4b7572d85156a941620aaf5d1b432`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.15`

```console
$ docker pull nats@sha256:8b3fb2423a8cce4607ef30a990b35545afe0a3c613cd05b8eec7b483df268b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:89eb697c14f6556d6fb2703240e48d9600b40b408dda60ae36e262425a4431e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cd50aa7198f5c12f156d09daa0ddc1112236fff6860f120a2251d96ff9eb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 05:59:05 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 05:59:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 05:59:08 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 05:59:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802d7c7e4ac6a66227b2370fdcdf5a6a23823257ca471179abfd0902b956fd7`  
		Last Modified: Sat, 05 Feb 2022 06:00:25 GMT  
		Size: 4.8 MB (4753836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426dd83cc6600f256ef35338c32eaf3d0399bab79c1246ec09184bdd1ea5b1f`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93f969dc9e9707d1fb2f5eaf6e9636680ca5b3cdfe45b8466a97b0105f036ba`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:26c9fd5ce79bfefe188314878ab0f821a0fbca95fcfbe50f92e81d7f4484ec10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7052346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b52e6eb1b52cca05de6f415e6236b2bd399ce0fb9f1d1ce06066a1558de8e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 00:57:59 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 00:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 00:58:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 00:58:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e778c855e77141dc3829b1882837f8ec9f4bc5a650dd40a2917a225e1c15d0d`  
		Last Modified: Sat, 05 Feb 2022 01:00:11 GMT  
		Size: 4.4 MB (4419922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8accecf8efa4c43a09a141647ccf09dc6a56558b970610993d7fdbee2275956f`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7dff5d8e4ec08b7521acbd3a01a86b9f803f821c99252b840a0491493b43b`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:9f1dff6dca496cefa436b4db1fa8fa857eb557bd0a6e6760c9b296f096bde9e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6847919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc4a088149c39457ad06caa0dedec762d0dcf09f2ae4743592c4d418f8e890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 06:12:22 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 06:12:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 06:12:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 06:12:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 06:12:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 06:12:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603aa49db7f9a89152dcd7cdf78b402ef16aff3bb40294f6c66a933f07378ee0`  
		Last Modified: Sat, 05 Feb 2022 06:14:40 GMT  
		Size: 4.4 MB (4412155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ab40c3eba476ac4d53154b86201d8626e858e7ed7651fc1045021e03587fee`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ec7b9832ec0d741d78be9c59991717e8a0a7b188c6ac0252cee24c879dcfcf`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b23b110a6166fdd559bbdf992cff078caa3eeb7e37fa86d2cf2765bdddd7898
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7114722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c3ca4ead676b4547ea7e17b1a67ffc43fc9e9a70f9fbbc6dfbe03a6615799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 04:08:44 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 04:08:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 04:08:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 04:08:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 04:08:50 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 04:08:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039e8b74114ddf2278e01658eb7e01be08056565bae8a2955645300b982fb0f2`  
		Last Modified: Sat, 05 Feb 2022 04:09:53 GMT  
		Size: 4.4 MB (4398315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76361110853d49e5895bb2123f92f8e3f8f1a08ce01c8ccda76acb70a73d7e22`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a80240856cec2d4b5bcd8aaff898e547e4b7572d85156a941620aaf5d1b432`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:7d5e0768fec0607c8aca58d0f15fa00ca535c5abffaef46aaf4196657521a605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:d42ce25d3289b63f8d1b14bed47669d1c5b632d31e74a78f86b3734d1a25e0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:3d7301d591b5ac27e95a6632733f104f9507986c46feb51ab911a8410f0264c8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107575564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948555d0919d6e1d2b1500bd9f7e11a9dc09dccd1da752619916a751bc03a84b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 26 Jan 2022 01:18:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:18:33 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Fri, 04 Feb 2022 23:18:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5cb841e15906c5eda43ff713132f917ee3c8f180a706900af652f1e93eeb1790`  
		Last Modified: Wed, 26 Jan 2022 01:19:36 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b67013be4d12b054b27a0b91ace36c3f8222cd350392424ced1c970747994d`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 4.5 MB (4522588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1805e78a4fad9c9cb97d2814ce2dbb2df363473ddf91ce6461544ffbd2070d`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a09a68fc240bc35491ff997dbab51436d375aa293b751496f953d06e84e07`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db154e2963b998e6bb84fff4b0a7796597d4cbe0e5cee24be6e4652a7c1356fe`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb7933f5f3359a26b455d45dccb368fd5783bccc73c1a2d7faac4001e95c6d0`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:d42ce25d3289b63f8d1b14bed47669d1c5b632d31e74a78f86b3734d1a25e0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:3d7301d591b5ac27e95a6632733f104f9507986c46feb51ab911a8410f0264c8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107575564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948555d0919d6e1d2b1500bd9f7e11a9dc09dccd1da752619916a751bc03a84b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 26 Jan 2022 01:18:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:18:33 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Fri, 04 Feb 2022 23:18:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5cb841e15906c5eda43ff713132f917ee3c8f180a706900af652f1e93eeb1790`  
		Last Modified: Wed, 26 Jan 2022 01:19:36 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b67013be4d12b054b27a0b91ace36c3f8222cd350392424ced1c970747994d`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 4.5 MB (4522588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1805e78a4fad9c9cb97d2814ce2dbb2df363473ddf91ce6461544ffbd2070d`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a09a68fc240bc35491ff997dbab51436d375aa293b751496f953d06e84e07`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db154e2963b998e6bb84fff4b0a7796597d4cbe0e5cee24be6e4652a7c1356fe`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb7933f5f3359a26b455d45dccb368fd5783bccc73c1a2d7faac4001e95c6d0`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:7d5e0768fec0607c8aca58d0f15fa00ca535c5abffaef46aaf4196657521a605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:9d847fd779f302f9d241623f856ab3521eb8d5375d35312ca8a0293987c409ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:50d24781f65efa4753d3f69caa810d9876b7b78f38e89f24316aaf00260288c1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718570973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5dd0772263590a54e8fd596675ca09934aba47b6f0562a6df8fcec11d7da36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Mon, 24 Jan 2022 23:18:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 26 Jan 2022 01:15:08 GMT
ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:15:51 GMT
ENV NATS_SERVER=2.7.2
# Fri, 04 Feb 2022 23:15:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.2/nats-server-v2.7.2-windows-amd64.zip
# Fri, 04 Feb 2022 23:15:53 GMT
ENV NATS_SERVER_SHASUM=12706f570a4d237c4d59ad8308e40f86b5322338b51e67e84b9c26ea019221b2
# Fri, 04 Feb 2022 23:16:53 GMT
RUN Set-PSDebug -Trace 2
# Fri, 04 Feb 2022 23:18:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 04 Feb 2022 23:18:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:23 GMT
EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:24 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1e63a09e013659f9cb51a44694cf1487fd0ea2ae5528ca387357386508f2b93c`  
		Last Modified: Tue, 25 Jan 2022 00:07:22 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d2d5bbe3c541fe8decf0e3c04bd30aaa74313119e1269d9b03d461638babbd`  
		Last Modified: Wed, 26 Jan 2022 01:19:16 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3ee08d029d143858e524a3f871d67ab08883f876c9dfb98e00ba4d07896130`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8215fd70836c74bf673367169f6c48b8683e1bf07655ccb33834d5bd9817e010`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c38ade2d53ceeced34948ca25473c5112d3a98d579b3fc97616cf3ab1d1a44`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89942494ebde2b32297c9120eb73fb52237c786054b320ef2253f93595e72e57`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 368.3 KB (368299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886bb1ccd4c447ad4705d7ee2026bca172826fcdf3ac6172f4e3a954b55826b0`  
		Last Modified: Fri, 04 Feb 2022 23:19:09 GMT  
		Size: 4.9 MB (4867790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dc3006c1eb769eefbc435fb9fd9df5c5693d6d6dcb54963d04281196928a97`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 2.0 KB (2008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af99d7e3732a21b5c82dcb9cbf6e9fd0f8321231aa773ed3180fedf3b8df6d76`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f7d7190f43b971dc09434fbc244ad13f02e0cd6fd3baa7e19a601afc3c3727`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba1ff369fef52867e63aa5f9b1afec5c370b95d40580395dcaebbe90fbe3cd7`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:9d847fd779f302f9d241623f856ab3521eb8d5375d35312ca8a0293987c409ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:50d24781f65efa4753d3f69caa810d9876b7b78f38e89f24316aaf00260288c1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718570973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5dd0772263590a54e8fd596675ca09934aba47b6f0562a6df8fcec11d7da36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Mon, 24 Jan 2022 23:18:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 26 Jan 2022 01:15:08 GMT
ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:15:51 GMT
ENV NATS_SERVER=2.7.2
# Fri, 04 Feb 2022 23:15:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.2/nats-server-v2.7.2-windows-amd64.zip
# Fri, 04 Feb 2022 23:15:53 GMT
ENV NATS_SERVER_SHASUM=12706f570a4d237c4d59ad8308e40f86b5322338b51e67e84b9c26ea019221b2
# Fri, 04 Feb 2022 23:16:53 GMT
RUN Set-PSDebug -Trace 2
# Fri, 04 Feb 2022 23:18:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 04 Feb 2022 23:18:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:23 GMT
EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:24 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1e63a09e013659f9cb51a44694cf1487fd0ea2ae5528ca387357386508f2b93c`  
		Last Modified: Tue, 25 Jan 2022 00:07:22 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d2d5bbe3c541fe8decf0e3c04bd30aaa74313119e1269d9b03d461638babbd`  
		Last Modified: Wed, 26 Jan 2022 01:19:16 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3ee08d029d143858e524a3f871d67ab08883f876c9dfb98e00ba4d07896130`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8215fd70836c74bf673367169f6c48b8683e1bf07655ccb33834d5bd9817e010`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c38ade2d53ceeced34948ca25473c5112d3a98d579b3fc97616cf3ab1d1a44`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89942494ebde2b32297c9120eb73fb52237c786054b320ef2253f93595e72e57`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 368.3 KB (368299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886bb1ccd4c447ad4705d7ee2026bca172826fcdf3ac6172f4e3a954b55826b0`  
		Last Modified: Fri, 04 Feb 2022 23:19:09 GMT  
		Size: 4.9 MB (4867790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dc3006c1eb769eefbc435fb9fd9df5c5693d6d6dcb54963d04281196928a97`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 2.0 KB (2008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af99d7e3732a21b5c82dcb9cbf6e9fd0f8321231aa773ed3180fedf3b8df6d76`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f7d7190f43b971dc09434fbc244ad13f02e0cd6fd3baa7e19a601afc3c3727`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba1ff369fef52867e63aa5f9b1afec5c370b95d40580395dcaebbe90fbe3cd7`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7`

```console
$ docker pull nats@sha256:cad2f8a76874a8011aede58fc3d064dbe5cd6ca5f244cd127c2614fd6eefc62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2458; amd64

### `nats:2.7` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:3d7301d591b5ac27e95a6632733f104f9507986c46feb51ab911a8410f0264c8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107575564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948555d0919d6e1d2b1500bd9f7e11a9dc09dccd1da752619916a751bc03a84b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 26 Jan 2022 01:18:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:18:33 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Fri, 04 Feb 2022 23:18:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5cb841e15906c5eda43ff713132f917ee3c8f180a706900af652f1e93eeb1790`  
		Last Modified: Wed, 26 Jan 2022 01:19:36 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b67013be4d12b054b27a0b91ace36c3f8222cd350392424ced1c970747994d`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 4.5 MB (4522588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1805e78a4fad9c9cb97d2814ce2dbb2df363473ddf91ce6461544ffbd2070d`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a09a68fc240bc35491ff997dbab51436d375aa293b751496f953d06e84e07`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db154e2963b998e6bb84fff4b0a7796597d4cbe0e5cee24be6e4652a7c1356fe`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb7933f5f3359a26b455d45dccb368fd5783bccc73c1a2d7faac4001e95c6d0`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-alpine`

```console
$ docker pull nats@sha256:8b3fb2423a8cce4607ef30a990b35545afe0a3c613cd05b8eec7b483df268b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-alpine` - linux; amd64

```console
$ docker pull nats@sha256:89eb697c14f6556d6fb2703240e48d9600b40b408dda60ae36e262425a4431e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cd50aa7198f5c12f156d09daa0ddc1112236fff6860f120a2251d96ff9eb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 05:59:05 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 05:59:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 05:59:08 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 05:59:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802d7c7e4ac6a66227b2370fdcdf5a6a23823257ca471179abfd0902b956fd7`  
		Last Modified: Sat, 05 Feb 2022 06:00:25 GMT  
		Size: 4.8 MB (4753836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426dd83cc6600f256ef35338c32eaf3d0399bab79c1246ec09184bdd1ea5b1f`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93f969dc9e9707d1fb2f5eaf6e9636680ca5b3cdfe45b8466a97b0105f036ba`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:26c9fd5ce79bfefe188314878ab0f821a0fbca95fcfbe50f92e81d7f4484ec10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7052346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b52e6eb1b52cca05de6f415e6236b2bd399ce0fb9f1d1ce06066a1558de8e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 00:57:59 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 00:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 00:58:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 00:58:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e778c855e77141dc3829b1882837f8ec9f4bc5a650dd40a2917a225e1c15d0d`  
		Last Modified: Sat, 05 Feb 2022 01:00:11 GMT  
		Size: 4.4 MB (4419922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8accecf8efa4c43a09a141647ccf09dc6a56558b970610993d7fdbee2275956f`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7dff5d8e4ec08b7521acbd3a01a86b9f803f821c99252b840a0491493b43b`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9f1dff6dca496cefa436b4db1fa8fa857eb557bd0a6e6760c9b296f096bde9e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6847919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc4a088149c39457ad06caa0dedec762d0dcf09f2ae4743592c4d418f8e890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 06:12:22 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 06:12:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 06:12:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 06:12:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 06:12:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 06:12:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603aa49db7f9a89152dcd7cdf78b402ef16aff3bb40294f6c66a933f07378ee0`  
		Last Modified: Sat, 05 Feb 2022 06:14:40 GMT  
		Size: 4.4 MB (4412155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ab40c3eba476ac4d53154b86201d8626e858e7ed7651fc1045021e03587fee`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ec7b9832ec0d741d78be9c59991717e8a0a7b188c6ac0252cee24c879dcfcf`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b23b110a6166fdd559bbdf992cff078caa3eeb7e37fa86d2cf2765bdddd7898
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7114722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c3ca4ead676b4547ea7e17b1a67ffc43fc9e9a70f9fbbc6dfbe03a6615799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 04:08:44 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 04:08:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 04:08:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 04:08:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 04:08:50 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 04:08:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039e8b74114ddf2278e01658eb7e01be08056565bae8a2955645300b982fb0f2`  
		Last Modified: Sat, 05 Feb 2022 04:09:53 GMT  
		Size: 4.4 MB (4398315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76361110853d49e5895bb2123f92f8e3f8f1a08ce01c8ccda76acb70a73d7e22`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a80240856cec2d4b5bcd8aaff898e547e4b7572d85156a941620aaf5d1b432`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-alpine3.15`

```console
$ docker pull nats@sha256:8b3fb2423a8cce4607ef30a990b35545afe0a3c613cd05b8eec7b483df268b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:89eb697c14f6556d6fb2703240e48d9600b40b408dda60ae36e262425a4431e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cd50aa7198f5c12f156d09daa0ddc1112236fff6860f120a2251d96ff9eb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 05:59:05 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 05:59:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 05:59:08 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 05:59:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802d7c7e4ac6a66227b2370fdcdf5a6a23823257ca471179abfd0902b956fd7`  
		Last Modified: Sat, 05 Feb 2022 06:00:25 GMT  
		Size: 4.8 MB (4753836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426dd83cc6600f256ef35338c32eaf3d0399bab79c1246ec09184bdd1ea5b1f`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93f969dc9e9707d1fb2f5eaf6e9636680ca5b3cdfe45b8466a97b0105f036ba`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:26c9fd5ce79bfefe188314878ab0f821a0fbca95fcfbe50f92e81d7f4484ec10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7052346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b52e6eb1b52cca05de6f415e6236b2bd399ce0fb9f1d1ce06066a1558de8e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 00:57:59 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 00:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 00:58:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 00:58:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e778c855e77141dc3829b1882837f8ec9f4bc5a650dd40a2917a225e1c15d0d`  
		Last Modified: Sat, 05 Feb 2022 01:00:11 GMT  
		Size: 4.4 MB (4419922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8accecf8efa4c43a09a141647ccf09dc6a56558b970610993d7fdbee2275956f`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7dff5d8e4ec08b7521acbd3a01a86b9f803f821c99252b840a0491493b43b`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:9f1dff6dca496cefa436b4db1fa8fa857eb557bd0a6e6760c9b296f096bde9e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6847919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc4a088149c39457ad06caa0dedec762d0dcf09f2ae4743592c4d418f8e890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 06:12:22 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 06:12:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 06:12:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 06:12:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 06:12:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 06:12:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603aa49db7f9a89152dcd7cdf78b402ef16aff3bb40294f6c66a933f07378ee0`  
		Last Modified: Sat, 05 Feb 2022 06:14:40 GMT  
		Size: 4.4 MB (4412155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ab40c3eba476ac4d53154b86201d8626e858e7ed7651fc1045021e03587fee`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ec7b9832ec0d741d78be9c59991717e8a0a7b188c6ac0252cee24c879dcfcf`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b23b110a6166fdd559bbdf992cff078caa3eeb7e37fa86d2cf2765bdddd7898
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7114722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c3ca4ead676b4547ea7e17b1a67ffc43fc9e9a70f9fbbc6dfbe03a6615799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 04:08:44 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 04:08:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 04:08:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 04:08:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 04:08:50 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 04:08:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039e8b74114ddf2278e01658eb7e01be08056565bae8a2955645300b982fb0f2`  
		Last Modified: Sat, 05 Feb 2022 04:09:53 GMT  
		Size: 4.4 MB (4398315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76361110853d49e5895bb2123f92f8e3f8f1a08ce01c8ccda76acb70a73d7e22`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a80240856cec2d4b5bcd8aaff898e547e4b7572d85156a941620aaf5d1b432`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-linux`

```console
$ docker pull nats@sha256:7d5e0768fec0607c8aca58d0f15fa00ca535c5abffaef46aaf4196657521a605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-linux` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-nanoserver`

```console
$ docker pull nats@sha256:d42ce25d3289b63f8d1b14bed47669d1c5b632d31e74a78f86b3734d1a25e0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `nats:2.7-nanoserver` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:3d7301d591b5ac27e95a6632733f104f9507986c46feb51ab911a8410f0264c8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107575564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948555d0919d6e1d2b1500bd9f7e11a9dc09dccd1da752619916a751bc03a84b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 26 Jan 2022 01:18:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:18:33 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Fri, 04 Feb 2022 23:18:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5cb841e15906c5eda43ff713132f917ee3c8f180a706900af652f1e93eeb1790`  
		Last Modified: Wed, 26 Jan 2022 01:19:36 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b67013be4d12b054b27a0b91ace36c3f8222cd350392424ced1c970747994d`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 4.5 MB (4522588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1805e78a4fad9c9cb97d2814ce2dbb2df363473ddf91ce6461544ffbd2070d`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a09a68fc240bc35491ff997dbab51436d375aa293b751496f953d06e84e07`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db154e2963b998e6bb84fff4b0a7796597d4cbe0e5cee24be6e4652a7c1356fe`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb7933f5f3359a26b455d45dccb368fd5783bccc73c1a2d7faac4001e95c6d0`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-nanoserver-1809`

```console
$ docker pull nats@sha256:d42ce25d3289b63f8d1b14bed47669d1c5b632d31e74a78f86b3734d1a25e0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `nats:2.7-nanoserver-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:3d7301d591b5ac27e95a6632733f104f9507986c46feb51ab911a8410f0264c8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107575564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948555d0919d6e1d2b1500bd9f7e11a9dc09dccd1da752619916a751bc03a84b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 26 Jan 2022 01:18:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:18:33 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Fri, 04 Feb 2022 23:18:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5cb841e15906c5eda43ff713132f917ee3c8f180a706900af652f1e93eeb1790`  
		Last Modified: Wed, 26 Jan 2022 01:19:36 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b67013be4d12b054b27a0b91ace36c3f8222cd350392424ced1c970747994d`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 4.5 MB (4522588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1805e78a4fad9c9cb97d2814ce2dbb2df363473ddf91ce6461544ffbd2070d`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a09a68fc240bc35491ff997dbab51436d375aa293b751496f953d06e84e07`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db154e2963b998e6bb84fff4b0a7796597d4cbe0e5cee24be6e4652a7c1356fe`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb7933f5f3359a26b455d45dccb368fd5783bccc73c1a2d7faac4001e95c6d0`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-scratch`

```console
$ docker pull nats@sha256:7d5e0768fec0607c8aca58d0f15fa00ca535c5abffaef46aaf4196657521a605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-scratch` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-windowsservercore`

```console
$ docker pull nats@sha256:9d847fd779f302f9d241623f856ab3521eb8d5375d35312ca8a0293987c409ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `nats:2.7-windowsservercore` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:50d24781f65efa4753d3f69caa810d9876b7b78f38e89f24316aaf00260288c1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718570973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5dd0772263590a54e8fd596675ca09934aba47b6f0562a6df8fcec11d7da36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Mon, 24 Jan 2022 23:18:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 26 Jan 2022 01:15:08 GMT
ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:15:51 GMT
ENV NATS_SERVER=2.7.2
# Fri, 04 Feb 2022 23:15:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.2/nats-server-v2.7.2-windows-amd64.zip
# Fri, 04 Feb 2022 23:15:53 GMT
ENV NATS_SERVER_SHASUM=12706f570a4d237c4d59ad8308e40f86b5322338b51e67e84b9c26ea019221b2
# Fri, 04 Feb 2022 23:16:53 GMT
RUN Set-PSDebug -Trace 2
# Fri, 04 Feb 2022 23:18:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 04 Feb 2022 23:18:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:23 GMT
EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:24 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1e63a09e013659f9cb51a44694cf1487fd0ea2ae5528ca387357386508f2b93c`  
		Last Modified: Tue, 25 Jan 2022 00:07:22 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d2d5bbe3c541fe8decf0e3c04bd30aaa74313119e1269d9b03d461638babbd`  
		Last Modified: Wed, 26 Jan 2022 01:19:16 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3ee08d029d143858e524a3f871d67ab08883f876c9dfb98e00ba4d07896130`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8215fd70836c74bf673367169f6c48b8683e1bf07655ccb33834d5bd9817e010`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c38ade2d53ceeced34948ca25473c5112d3a98d579b3fc97616cf3ab1d1a44`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89942494ebde2b32297c9120eb73fb52237c786054b320ef2253f93595e72e57`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 368.3 KB (368299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886bb1ccd4c447ad4705d7ee2026bca172826fcdf3ac6172f4e3a954b55826b0`  
		Last Modified: Fri, 04 Feb 2022 23:19:09 GMT  
		Size: 4.9 MB (4867790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dc3006c1eb769eefbc435fb9fd9df5c5693d6d6dcb54963d04281196928a97`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 2.0 KB (2008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af99d7e3732a21b5c82dcb9cbf6e9fd0f8321231aa773ed3180fedf3b8df6d76`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f7d7190f43b971dc09434fbc244ad13f02e0cd6fd3baa7e19a601afc3c3727`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba1ff369fef52867e63aa5f9b1afec5c370b95d40580395dcaebbe90fbe3cd7`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-windowsservercore-1809`

```console
$ docker pull nats@sha256:9d847fd779f302f9d241623f856ab3521eb8d5375d35312ca8a0293987c409ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `nats:2.7-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:50d24781f65efa4753d3f69caa810d9876b7b78f38e89f24316aaf00260288c1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718570973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5dd0772263590a54e8fd596675ca09934aba47b6f0562a6df8fcec11d7da36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Mon, 24 Jan 2022 23:18:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 26 Jan 2022 01:15:08 GMT
ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:15:51 GMT
ENV NATS_SERVER=2.7.2
# Fri, 04 Feb 2022 23:15:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.2/nats-server-v2.7.2-windows-amd64.zip
# Fri, 04 Feb 2022 23:15:53 GMT
ENV NATS_SERVER_SHASUM=12706f570a4d237c4d59ad8308e40f86b5322338b51e67e84b9c26ea019221b2
# Fri, 04 Feb 2022 23:16:53 GMT
RUN Set-PSDebug -Trace 2
# Fri, 04 Feb 2022 23:18:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 04 Feb 2022 23:18:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:23 GMT
EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:24 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1e63a09e013659f9cb51a44694cf1487fd0ea2ae5528ca387357386508f2b93c`  
		Last Modified: Tue, 25 Jan 2022 00:07:22 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d2d5bbe3c541fe8decf0e3c04bd30aaa74313119e1269d9b03d461638babbd`  
		Last Modified: Wed, 26 Jan 2022 01:19:16 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3ee08d029d143858e524a3f871d67ab08883f876c9dfb98e00ba4d07896130`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8215fd70836c74bf673367169f6c48b8683e1bf07655ccb33834d5bd9817e010`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c38ade2d53ceeced34948ca25473c5112d3a98d579b3fc97616cf3ab1d1a44`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89942494ebde2b32297c9120eb73fb52237c786054b320ef2253f93595e72e57`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 368.3 KB (368299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886bb1ccd4c447ad4705d7ee2026bca172826fcdf3ac6172f4e3a954b55826b0`  
		Last Modified: Fri, 04 Feb 2022 23:19:09 GMT  
		Size: 4.9 MB (4867790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dc3006c1eb769eefbc435fb9fd9df5c5693d6d6dcb54963d04281196928a97`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 2.0 KB (2008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af99d7e3732a21b5c82dcb9cbf6e9fd0f8321231aa773ed3180fedf3b8df6d76`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f7d7190f43b971dc09434fbc244ad13f02e0cd6fd3baa7e19a601afc3c3727`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba1ff369fef52867e63aa5f9b1afec5c370b95d40580395dcaebbe90fbe3cd7`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.2`

```console
$ docker pull nats@sha256:cad2f8a76874a8011aede58fc3d064dbe5cd6ca5f244cd127c2614fd6eefc62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2458; amd64

### `nats:2.7.2` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:3d7301d591b5ac27e95a6632733f104f9507986c46feb51ab911a8410f0264c8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107575564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948555d0919d6e1d2b1500bd9f7e11a9dc09dccd1da752619916a751bc03a84b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 26 Jan 2022 01:18:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:18:33 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Fri, 04 Feb 2022 23:18:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5cb841e15906c5eda43ff713132f917ee3c8f180a706900af652f1e93eeb1790`  
		Last Modified: Wed, 26 Jan 2022 01:19:36 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b67013be4d12b054b27a0b91ace36c3f8222cd350392424ced1c970747994d`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 4.5 MB (4522588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1805e78a4fad9c9cb97d2814ce2dbb2df363473ddf91ce6461544ffbd2070d`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a09a68fc240bc35491ff997dbab51436d375aa293b751496f953d06e84e07`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db154e2963b998e6bb84fff4b0a7796597d4cbe0e5cee24be6e4652a7c1356fe`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb7933f5f3359a26b455d45dccb368fd5783bccc73c1a2d7faac4001e95c6d0`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.2-alpine`

```console
$ docker pull nats@sha256:8b3fb2423a8cce4607ef30a990b35545afe0a3c613cd05b8eec7b483df268b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:89eb697c14f6556d6fb2703240e48d9600b40b408dda60ae36e262425a4431e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cd50aa7198f5c12f156d09daa0ddc1112236fff6860f120a2251d96ff9eb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 05:59:05 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 05:59:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 05:59:08 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 05:59:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802d7c7e4ac6a66227b2370fdcdf5a6a23823257ca471179abfd0902b956fd7`  
		Last Modified: Sat, 05 Feb 2022 06:00:25 GMT  
		Size: 4.8 MB (4753836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426dd83cc6600f256ef35338c32eaf3d0399bab79c1246ec09184bdd1ea5b1f`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93f969dc9e9707d1fb2f5eaf6e9636680ca5b3cdfe45b8466a97b0105f036ba`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:26c9fd5ce79bfefe188314878ab0f821a0fbca95fcfbe50f92e81d7f4484ec10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7052346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b52e6eb1b52cca05de6f415e6236b2bd399ce0fb9f1d1ce06066a1558de8e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 00:57:59 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 00:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 00:58:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 00:58:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e778c855e77141dc3829b1882837f8ec9f4bc5a650dd40a2917a225e1c15d0d`  
		Last Modified: Sat, 05 Feb 2022 01:00:11 GMT  
		Size: 4.4 MB (4419922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8accecf8efa4c43a09a141647ccf09dc6a56558b970610993d7fdbee2275956f`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7dff5d8e4ec08b7521acbd3a01a86b9f803f821c99252b840a0491493b43b`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9f1dff6dca496cefa436b4db1fa8fa857eb557bd0a6e6760c9b296f096bde9e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6847919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc4a088149c39457ad06caa0dedec762d0dcf09f2ae4743592c4d418f8e890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 06:12:22 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 06:12:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 06:12:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 06:12:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 06:12:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 06:12:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603aa49db7f9a89152dcd7cdf78b402ef16aff3bb40294f6c66a933f07378ee0`  
		Last Modified: Sat, 05 Feb 2022 06:14:40 GMT  
		Size: 4.4 MB (4412155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ab40c3eba476ac4d53154b86201d8626e858e7ed7651fc1045021e03587fee`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ec7b9832ec0d741d78be9c59991717e8a0a7b188c6ac0252cee24c879dcfcf`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b23b110a6166fdd559bbdf992cff078caa3eeb7e37fa86d2cf2765bdddd7898
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7114722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c3ca4ead676b4547ea7e17b1a67ffc43fc9e9a70f9fbbc6dfbe03a6615799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 04:08:44 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 04:08:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 04:08:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 04:08:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 04:08:50 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 04:08:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039e8b74114ddf2278e01658eb7e01be08056565bae8a2955645300b982fb0f2`  
		Last Modified: Sat, 05 Feb 2022 04:09:53 GMT  
		Size: 4.4 MB (4398315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76361110853d49e5895bb2123f92f8e3f8f1a08ce01c8ccda76acb70a73d7e22`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a80240856cec2d4b5bcd8aaff898e547e4b7572d85156a941620aaf5d1b432`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.2-alpine3.15`

```console
$ docker pull nats@sha256:8b3fb2423a8cce4607ef30a990b35545afe0a3c613cd05b8eec7b483df268b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.2-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:89eb697c14f6556d6fb2703240e48d9600b40b408dda60ae36e262425a4431e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cd50aa7198f5c12f156d09daa0ddc1112236fff6860f120a2251d96ff9eb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 05:59:05 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 05:59:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 05:59:08 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 05:59:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802d7c7e4ac6a66227b2370fdcdf5a6a23823257ca471179abfd0902b956fd7`  
		Last Modified: Sat, 05 Feb 2022 06:00:25 GMT  
		Size: 4.8 MB (4753836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426dd83cc6600f256ef35338c32eaf3d0399bab79c1246ec09184bdd1ea5b1f`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93f969dc9e9707d1fb2f5eaf6e9636680ca5b3cdfe45b8466a97b0105f036ba`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:26c9fd5ce79bfefe188314878ab0f821a0fbca95fcfbe50f92e81d7f4484ec10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7052346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b52e6eb1b52cca05de6f415e6236b2bd399ce0fb9f1d1ce06066a1558de8e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 00:57:59 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 00:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 00:58:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 00:58:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e778c855e77141dc3829b1882837f8ec9f4bc5a650dd40a2917a225e1c15d0d`  
		Last Modified: Sat, 05 Feb 2022 01:00:11 GMT  
		Size: 4.4 MB (4419922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8accecf8efa4c43a09a141647ccf09dc6a56558b970610993d7fdbee2275956f`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7dff5d8e4ec08b7521acbd3a01a86b9f803f821c99252b840a0491493b43b`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:9f1dff6dca496cefa436b4db1fa8fa857eb557bd0a6e6760c9b296f096bde9e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6847919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc4a088149c39457ad06caa0dedec762d0dcf09f2ae4743592c4d418f8e890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 06:12:22 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 06:12:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 06:12:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 06:12:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 06:12:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 06:12:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603aa49db7f9a89152dcd7cdf78b402ef16aff3bb40294f6c66a933f07378ee0`  
		Last Modified: Sat, 05 Feb 2022 06:14:40 GMT  
		Size: 4.4 MB (4412155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ab40c3eba476ac4d53154b86201d8626e858e7ed7651fc1045021e03587fee`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ec7b9832ec0d741d78be9c59991717e8a0a7b188c6ac0252cee24c879dcfcf`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b23b110a6166fdd559bbdf992cff078caa3eeb7e37fa86d2cf2765bdddd7898
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7114722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c3ca4ead676b4547ea7e17b1a67ffc43fc9e9a70f9fbbc6dfbe03a6615799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 04:08:44 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 04:08:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 04:08:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 04:08:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 04:08:50 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 04:08:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039e8b74114ddf2278e01658eb7e01be08056565bae8a2955645300b982fb0f2`  
		Last Modified: Sat, 05 Feb 2022 04:09:53 GMT  
		Size: 4.4 MB (4398315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76361110853d49e5895bb2123f92f8e3f8f1a08ce01c8ccda76acb70a73d7e22`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a80240856cec2d4b5bcd8aaff898e547e4b7572d85156a941620aaf5d1b432`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.2-linux`

```console
$ docker pull nats@sha256:7d5e0768fec0607c8aca58d0f15fa00ca535c5abffaef46aaf4196657521a605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.2-linux` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.2-nanoserver`

```console
$ docker pull nats@sha256:d42ce25d3289b63f8d1b14bed47669d1c5b632d31e74a78f86b3734d1a25e0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `nats:2.7.2-nanoserver` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:3d7301d591b5ac27e95a6632733f104f9507986c46feb51ab911a8410f0264c8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107575564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948555d0919d6e1d2b1500bd9f7e11a9dc09dccd1da752619916a751bc03a84b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 26 Jan 2022 01:18:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:18:33 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Fri, 04 Feb 2022 23:18:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5cb841e15906c5eda43ff713132f917ee3c8f180a706900af652f1e93eeb1790`  
		Last Modified: Wed, 26 Jan 2022 01:19:36 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b67013be4d12b054b27a0b91ace36c3f8222cd350392424ced1c970747994d`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 4.5 MB (4522588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1805e78a4fad9c9cb97d2814ce2dbb2df363473ddf91ce6461544ffbd2070d`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a09a68fc240bc35491ff997dbab51436d375aa293b751496f953d06e84e07`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db154e2963b998e6bb84fff4b0a7796597d4cbe0e5cee24be6e4652a7c1356fe`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb7933f5f3359a26b455d45dccb368fd5783bccc73c1a2d7faac4001e95c6d0`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.2-nanoserver-1809`

```console
$ docker pull nats@sha256:d42ce25d3289b63f8d1b14bed47669d1c5b632d31e74a78f86b3734d1a25e0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `nats:2.7.2-nanoserver-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:3d7301d591b5ac27e95a6632733f104f9507986c46feb51ab911a8410f0264c8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107575564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948555d0919d6e1d2b1500bd9f7e11a9dc09dccd1da752619916a751bc03a84b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 26 Jan 2022 01:18:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:18:33 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Fri, 04 Feb 2022 23:18:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5cb841e15906c5eda43ff713132f917ee3c8f180a706900af652f1e93eeb1790`  
		Last Modified: Wed, 26 Jan 2022 01:19:36 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b67013be4d12b054b27a0b91ace36c3f8222cd350392424ced1c970747994d`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 4.5 MB (4522588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1805e78a4fad9c9cb97d2814ce2dbb2df363473ddf91ce6461544ffbd2070d`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a09a68fc240bc35491ff997dbab51436d375aa293b751496f953d06e84e07`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db154e2963b998e6bb84fff4b0a7796597d4cbe0e5cee24be6e4652a7c1356fe`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb7933f5f3359a26b455d45dccb368fd5783bccc73c1a2d7faac4001e95c6d0`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.2-scratch`

```console
$ docker pull nats@sha256:7d5e0768fec0607c8aca58d0f15fa00ca535c5abffaef46aaf4196657521a605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.2-windowsservercore`

```console
$ docker pull nats@sha256:9d847fd779f302f9d241623f856ab3521eb8d5375d35312ca8a0293987c409ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `nats:2.7.2-windowsservercore` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:50d24781f65efa4753d3f69caa810d9876b7b78f38e89f24316aaf00260288c1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718570973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5dd0772263590a54e8fd596675ca09934aba47b6f0562a6df8fcec11d7da36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Mon, 24 Jan 2022 23:18:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 26 Jan 2022 01:15:08 GMT
ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:15:51 GMT
ENV NATS_SERVER=2.7.2
# Fri, 04 Feb 2022 23:15:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.2/nats-server-v2.7.2-windows-amd64.zip
# Fri, 04 Feb 2022 23:15:53 GMT
ENV NATS_SERVER_SHASUM=12706f570a4d237c4d59ad8308e40f86b5322338b51e67e84b9c26ea019221b2
# Fri, 04 Feb 2022 23:16:53 GMT
RUN Set-PSDebug -Trace 2
# Fri, 04 Feb 2022 23:18:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 04 Feb 2022 23:18:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:23 GMT
EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:24 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1e63a09e013659f9cb51a44694cf1487fd0ea2ae5528ca387357386508f2b93c`  
		Last Modified: Tue, 25 Jan 2022 00:07:22 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d2d5bbe3c541fe8decf0e3c04bd30aaa74313119e1269d9b03d461638babbd`  
		Last Modified: Wed, 26 Jan 2022 01:19:16 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3ee08d029d143858e524a3f871d67ab08883f876c9dfb98e00ba4d07896130`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8215fd70836c74bf673367169f6c48b8683e1bf07655ccb33834d5bd9817e010`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c38ade2d53ceeced34948ca25473c5112d3a98d579b3fc97616cf3ab1d1a44`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89942494ebde2b32297c9120eb73fb52237c786054b320ef2253f93595e72e57`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 368.3 KB (368299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886bb1ccd4c447ad4705d7ee2026bca172826fcdf3ac6172f4e3a954b55826b0`  
		Last Modified: Fri, 04 Feb 2022 23:19:09 GMT  
		Size: 4.9 MB (4867790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dc3006c1eb769eefbc435fb9fd9df5c5693d6d6dcb54963d04281196928a97`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 2.0 KB (2008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af99d7e3732a21b5c82dcb9cbf6e9fd0f8321231aa773ed3180fedf3b8df6d76`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f7d7190f43b971dc09434fbc244ad13f02e0cd6fd3baa7e19a601afc3c3727`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba1ff369fef52867e63aa5f9b1afec5c370b95d40580395dcaebbe90fbe3cd7`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.2-windowsservercore-1809`

```console
$ docker pull nats@sha256:9d847fd779f302f9d241623f856ab3521eb8d5375d35312ca8a0293987c409ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `nats:2.7.2-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:50d24781f65efa4753d3f69caa810d9876b7b78f38e89f24316aaf00260288c1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718570973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5dd0772263590a54e8fd596675ca09934aba47b6f0562a6df8fcec11d7da36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Mon, 24 Jan 2022 23:18:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 26 Jan 2022 01:15:08 GMT
ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:15:51 GMT
ENV NATS_SERVER=2.7.2
# Fri, 04 Feb 2022 23:15:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.2/nats-server-v2.7.2-windows-amd64.zip
# Fri, 04 Feb 2022 23:15:53 GMT
ENV NATS_SERVER_SHASUM=12706f570a4d237c4d59ad8308e40f86b5322338b51e67e84b9c26ea019221b2
# Fri, 04 Feb 2022 23:16:53 GMT
RUN Set-PSDebug -Trace 2
# Fri, 04 Feb 2022 23:18:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 04 Feb 2022 23:18:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:23 GMT
EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:24 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1e63a09e013659f9cb51a44694cf1487fd0ea2ae5528ca387357386508f2b93c`  
		Last Modified: Tue, 25 Jan 2022 00:07:22 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d2d5bbe3c541fe8decf0e3c04bd30aaa74313119e1269d9b03d461638babbd`  
		Last Modified: Wed, 26 Jan 2022 01:19:16 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3ee08d029d143858e524a3f871d67ab08883f876c9dfb98e00ba4d07896130`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8215fd70836c74bf673367169f6c48b8683e1bf07655ccb33834d5bd9817e010`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c38ade2d53ceeced34948ca25473c5112d3a98d579b3fc97616cf3ab1d1a44`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89942494ebde2b32297c9120eb73fb52237c786054b320ef2253f93595e72e57`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 368.3 KB (368299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886bb1ccd4c447ad4705d7ee2026bca172826fcdf3ac6172f4e3a954b55826b0`  
		Last Modified: Fri, 04 Feb 2022 23:19:09 GMT  
		Size: 4.9 MB (4867790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dc3006c1eb769eefbc435fb9fd9df5c5693d6d6dcb54963d04281196928a97`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 2.0 KB (2008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af99d7e3732a21b5c82dcb9cbf6e9fd0f8321231aa773ed3180fedf3b8df6d76`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f7d7190f43b971dc09434fbc244ad13f02e0cd6fd3baa7e19a601afc3c3727`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba1ff369fef52867e63aa5f9b1afec5c370b95d40580395dcaebbe90fbe3cd7`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:8b3fb2423a8cce4607ef30a990b35545afe0a3c613cd05b8eec7b483df268b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:89eb697c14f6556d6fb2703240e48d9600b40b408dda60ae36e262425a4431e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cd50aa7198f5c12f156d09daa0ddc1112236fff6860f120a2251d96ff9eb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 05:59:05 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 05:59:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 05:59:08 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 05:59:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802d7c7e4ac6a66227b2370fdcdf5a6a23823257ca471179abfd0902b956fd7`  
		Last Modified: Sat, 05 Feb 2022 06:00:25 GMT  
		Size: 4.8 MB (4753836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426dd83cc6600f256ef35338c32eaf3d0399bab79c1246ec09184bdd1ea5b1f`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93f969dc9e9707d1fb2f5eaf6e9636680ca5b3cdfe45b8466a97b0105f036ba`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:26c9fd5ce79bfefe188314878ab0f821a0fbca95fcfbe50f92e81d7f4484ec10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7052346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b52e6eb1b52cca05de6f415e6236b2bd399ce0fb9f1d1ce06066a1558de8e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 00:57:59 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 00:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 00:58:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 00:58:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e778c855e77141dc3829b1882837f8ec9f4bc5a650dd40a2917a225e1c15d0d`  
		Last Modified: Sat, 05 Feb 2022 01:00:11 GMT  
		Size: 4.4 MB (4419922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8accecf8efa4c43a09a141647ccf09dc6a56558b970610993d7fdbee2275956f`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7dff5d8e4ec08b7521acbd3a01a86b9f803f821c99252b840a0491493b43b`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9f1dff6dca496cefa436b4db1fa8fa857eb557bd0a6e6760c9b296f096bde9e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6847919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc4a088149c39457ad06caa0dedec762d0dcf09f2ae4743592c4d418f8e890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 06:12:22 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 06:12:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 06:12:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 06:12:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 06:12:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 06:12:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603aa49db7f9a89152dcd7cdf78b402ef16aff3bb40294f6c66a933f07378ee0`  
		Last Modified: Sat, 05 Feb 2022 06:14:40 GMT  
		Size: 4.4 MB (4412155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ab40c3eba476ac4d53154b86201d8626e858e7ed7651fc1045021e03587fee`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ec7b9832ec0d741d78be9c59991717e8a0a7b188c6ac0252cee24c879dcfcf`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b23b110a6166fdd559bbdf992cff078caa3eeb7e37fa86d2cf2765bdddd7898
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7114722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c3ca4ead676b4547ea7e17b1a67ffc43fc9e9a70f9fbbc6dfbe03a6615799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 04:08:44 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 04:08:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 04:08:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 04:08:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 04:08:50 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 04:08:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039e8b74114ddf2278e01658eb7e01be08056565bae8a2955645300b982fb0f2`  
		Last Modified: Sat, 05 Feb 2022 04:09:53 GMT  
		Size: 4.4 MB (4398315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76361110853d49e5895bb2123f92f8e3f8f1a08ce01c8ccda76acb70a73d7e22`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a80240856cec2d4b5bcd8aaff898e547e4b7572d85156a941620aaf5d1b432`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.15`

```console
$ docker pull nats@sha256:8b3fb2423a8cce4607ef30a990b35545afe0a3c613cd05b8eec7b483df268b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:89eb697c14f6556d6fb2703240e48d9600b40b408dda60ae36e262425a4431e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cd50aa7198f5c12f156d09daa0ddc1112236fff6860f120a2251d96ff9eb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 05:59:05 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 05:59:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 05:59:08 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 05:59:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802d7c7e4ac6a66227b2370fdcdf5a6a23823257ca471179abfd0902b956fd7`  
		Last Modified: Sat, 05 Feb 2022 06:00:25 GMT  
		Size: 4.8 MB (4753836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426dd83cc6600f256ef35338c32eaf3d0399bab79c1246ec09184bdd1ea5b1f`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93f969dc9e9707d1fb2f5eaf6e9636680ca5b3cdfe45b8466a97b0105f036ba`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:26c9fd5ce79bfefe188314878ab0f821a0fbca95fcfbe50f92e81d7f4484ec10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7052346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b52e6eb1b52cca05de6f415e6236b2bd399ce0fb9f1d1ce06066a1558de8e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 00:57:59 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 00:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 00:58:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 00:58:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e778c855e77141dc3829b1882837f8ec9f4bc5a650dd40a2917a225e1c15d0d`  
		Last Modified: Sat, 05 Feb 2022 01:00:11 GMT  
		Size: 4.4 MB (4419922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8accecf8efa4c43a09a141647ccf09dc6a56558b970610993d7fdbee2275956f`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7dff5d8e4ec08b7521acbd3a01a86b9f803f821c99252b840a0491493b43b`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:9f1dff6dca496cefa436b4db1fa8fa857eb557bd0a6e6760c9b296f096bde9e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6847919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc4a088149c39457ad06caa0dedec762d0dcf09f2ae4743592c4d418f8e890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 06:12:22 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 06:12:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 06:12:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 06:12:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 06:12:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 06:12:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603aa49db7f9a89152dcd7cdf78b402ef16aff3bb40294f6c66a933f07378ee0`  
		Last Modified: Sat, 05 Feb 2022 06:14:40 GMT  
		Size: 4.4 MB (4412155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ab40c3eba476ac4d53154b86201d8626e858e7ed7651fc1045021e03587fee`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ec7b9832ec0d741d78be9c59991717e8a0a7b188c6ac0252cee24c879dcfcf`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b23b110a6166fdd559bbdf992cff078caa3eeb7e37fa86d2cf2765bdddd7898
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7114722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c3ca4ead676b4547ea7e17b1a67ffc43fc9e9a70f9fbbc6dfbe03a6615799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 04:08:44 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 04:08:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 04:08:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 04:08:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 04:08:50 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 04:08:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039e8b74114ddf2278e01658eb7e01be08056565bae8a2955645300b982fb0f2`  
		Last Modified: Sat, 05 Feb 2022 04:09:53 GMT  
		Size: 4.4 MB (4398315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76361110853d49e5895bb2123f92f8e3f8f1a08ce01c8ccda76acb70a73d7e22`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a80240856cec2d4b5bcd8aaff898e547e4b7572d85156a941620aaf5d1b432`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:cad2f8a76874a8011aede58fc3d064dbe5cd6ca5f244cd127c2614fd6eefc62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2458; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:3d7301d591b5ac27e95a6632733f104f9507986c46feb51ab911a8410f0264c8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107575564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948555d0919d6e1d2b1500bd9f7e11a9dc09dccd1da752619916a751bc03a84b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 26 Jan 2022 01:18:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:18:33 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Fri, 04 Feb 2022 23:18:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5cb841e15906c5eda43ff713132f917ee3c8f180a706900af652f1e93eeb1790`  
		Last Modified: Wed, 26 Jan 2022 01:19:36 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b67013be4d12b054b27a0b91ace36c3f8222cd350392424ced1c970747994d`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 4.5 MB (4522588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1805e78a4fad9c9cb97d2814ce2dbb2df363473ddf91ce6461544ffbd2070d`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a09a68fc240bc35491ff997dbab51436d375aa293b751496f953d06e84e07`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db154e2963b998e6bb84fff4b0a7796597d4cbe0e5cee24be6e4652a7c1356fe`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb7933f5f3359a26b455d45dccb368fd5783bccc73c1a2d7faac4001e95c6d0`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:7d5e0768fec0607c8aca58d0f15fa00ca535c5abffaef46aaf4196657521a605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:d42ce25d3289b63f8d1b14bed47669d1c5b632d31e74a78f86b3734d1a25e0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `nats:nanoserver` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:3d7301d591b5ac27e95a6632733f104f9507986c46feb51ab911a8410f0264c8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107575564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948555d0919d6e1d2b1500bd9f7e11a9dc09dccd1da752619916a751bc03a84b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 26 Jan 2022 01:18:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:18:33 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Fri, 04 Feb 2022 23:18:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5cb841e15906c5eda43ff713132f917ee3c8f180a706900af652f1e93eeb1790`  
		Last Modified: Wed, 26 Jan 2022 01:19:36 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b67013be4d12b054b27a0b91ace36c3f8222cd350392424ced1c970747994d`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 4.5 MB (4522588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1805e78a4fad9c9cb97d2814ce2dbb2df363473ddf91ce6461544ffbd2070d`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a09a68fc240bc35491ff997dbab51436d375aa293b751496f953d06e84e07`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db154e2963b998e6bb84fff4b0a7796597d4cbe0e5cee24be6e4652a7c1356fe`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb7933f5f3359a26b455d45dccb368fd5783bccc73c1a2d7faac4001e95c6d0`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:d42ce25d3289b63f8d1b14bed47669d1c5b632d31e74a78f86b3734d1a25e0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:3d7301d591b5ac27e95a6632733f104f9507986c46feb51ab911a8410f0264c8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107575564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948555d0919d6e1d2b1500bd9f7e11a9dc09dccd1da752619916a751bc03a84b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 26 Jan 2022 01:18:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:18:33 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Fri, 04 Feb 2022 23:18:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5cb841e15906c5eda43ff713132f917ee3c8f180a706900af652f1e93eeb1790`  
		Last Modified: Wed, 26 Jan 2022 01:19:36 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b67013be4d12b054b27a0b91ace36c3f8222cd350392424ced1c970747994d`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 4.5 MB (4522588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1805e78a4fad9c9cb97d2814ce2dbb2df363473ddf91ce6461544ffbd2070d`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a09a68fc240bc35491ff997dbab51436d375aa293b751496f953d06e84e07`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db154e2963b998e6bb84fff4b0a7796597d4cbe0e5cee24be6e4652a7c1356fe`  
		Last Modified: Fri, 04 Feb 2022 23:19:24 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb7933f5f3359a26b455d45dccb368fd5783bccc73c1a2d7faac4001e95c6d0`  
		Last Modified: Fri, 04 Feb 2022 23:19:25 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:7d5e0768fec0607c8aca58d0f15fa00ca535c5abffaef46aaf4196657521a605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:9d847fd779f302f9d241623f856ab3521eb8d5375d35312ca8a0293987c409ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `nats:windowsservercore` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:50d24781f65efa4753d3f69caa810d9876b7b78f38e89f24316aaf00260288c1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718570973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5dd0772263590a54e8fd596675ca09934aba47b6f0562a6df8fcec11d7da36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Mon, 24 Jan 2022 23:18:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 26 Jan 2022 01:15:08 GMT
ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:15:51 GMT
ENV NATS_SERVER=2.7.2
# Fri, 04 Feb 2022 23:15:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.2/nats-server-v2.7.2-windows-amd64.zip
# Fri, 04 Feb 2022 23:15:53 GMT
ENV NATS_SERVER_SHASUM=12706f570a4d237c4d59ad8308e40f86b5322338b51e67e84b9c26ea019221b2
# Fri, 04 Feb 2022 23:16:53 GMT
RUN Set-PSDebug -Trace 2
# Fri, 04 Feb 2022 23:18:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 04 Feb 2022 23:18:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:23 GMT
EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:24 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1e63a09e013659f9cb51a44694cf1487fd0ea2ae5528ca387357386508f2b93c`  
		Last Modified: Tue, 25 Jan 2022 00:07:22 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d2d5bbe3c541fe8decf0e3c04bd30aaa74313119e1269d9b03d461638babbd`  
		Last Modified: Wed, 26 Jan 2022 01:19:16 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3ee08d029d143858e524a3f871d67ab08883f876c9dfb98e00ba4d07896130`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8215fd70836c74bf673367169f6c48b8683e1bf07655ccb33834d5bd9817e010`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c38ade2d53ceeced34948ca25473c5112d3a98d579b3fc97616cf3ab1d1a44`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89942494ebde2b32297c9120eb73fb52237c786054b320ef2253f93595e72e57`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 368.3 KB (368299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886bb1ccd4c447ad4705d7ee2026bca172826fcdf3ac6172f4e3a954b55826b0`  
		Last Modified: Fri, 04 Feb 2022 23:19:09 GMT  
		Size: 4.9 MB (4867790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dc3006c1eb769eefbc435fb9fd9df5c5693d6d6dcb54963d04281196928a97`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 2.0 KB (2008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af99d7e3732a21b5c82dcb9cbf6e9fd0f8321231aa773ed3180fedf3b8df6d76`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f7d7190f43b971dc09434fbc244ad13f02e0cd6fd3baa7e19a601afc3c3727`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba1ff369fef52867e63aa5f9b1afec5c370b95d40580395dcaebbe90fbe3cd7`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:9d847fd779f302f9d241623f856ab3521eb8d5375d35312ca8a0293987c409ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull nats@sha256:50d24781f65efa4753d3f69caa810d9876b7b78f38e89f24316aaf00260288c1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718570973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5dd0772263590a54e8fd596675ca09934aba47b6f0562a6df8fcec11d7da36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Mon, 24 Jan 2022 23:18:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 26 Jan 2022 01:15:08 GMT
ENV NATS_DOCKERIZED=1
# Fri, 04 Feb 2022 23:15:51 GMT
ENV NATS_SERVER=2.7.2
# Fri, 04 Feb 2022 23:15:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.2/nats-server-v2.7.2-windows-amd64.zip
# Fri, 04 Feb 2022 23:15:53 GMT
ENV NATS_SERVER_SHASUM=12706f570a4d237c4d59ad8308e40f86b5322338b51e67e84b9c26ea019221b2
# Fri, 04 Feb 2022 23:16:53 GMT
RUN Set-PSDebug -Trace 2
# Fri, 04 Feb 2022 23:18:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 04 Feb 2022 23:18:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 04 Feb 2022 23:18:23 GMT
EXPOSE 4222 6222 8222
# Fri, 04 Feb 2022 23:18:24 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Feb 2022 23:18:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1e63a09e013659f9cb51a44694cf1487fd0ea2ae5528ca387357386508f2b93c`  
		Last Modified: Tue, 25 Jan 2022 00:07:22 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d2d5bbe3c541fe8decf0e3c04bd30aaa74313119e1269d9b03d461638babbd`  
		Last Modified: Wed, 26 Jan 2022 01:19:16 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3ee08d029d143858e524a3f871d67ab08883f876c9dfb98e00ba4d07896130`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8215fd70836c74bf673367169f6c48b8683e1bf07655ccb33834d5bd9817e010`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c38ade2d53ceeced34948ca25473c5112d3a98d579b3fc97616cf3ab1d1a44`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89942494ebde2b32297c9120eb73fb52237c786054b320ef2253f93595e72e57`  
		Last Modified: Fri, 04 Feb 2022 23:19:10 GMT  
		Size: 368.3 KB (368299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886bb1ccd4c447ad4705d7ee2026bca172826fcdf3ac6172f4e3a954b55826b0`  
		Last Modified: Fri, 04 Feb 2022 23:19:09 GMT  
		Size: 4.9 MB (4867790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dc3006c1eb769eefbc435fb9fd9df5c5693d6d6dcb54963d04281196928a97`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 2.0 KB (2008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af99d7e3732a21b5c82dcb9cbf6e9fd0f8321231aa773ed3180fedf3b8df6d76`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f7d7190f43b971dc09434fbc244ad13f02e0cd6fd3baa7e19a601afc3c3727`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba1ff369fef52867e63aa5f9b1afec5c370b95d40580395dcaebbe90fbe3cd7`  
		Last Modified: Fri, 04 Feb 2022 23:19:08 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
